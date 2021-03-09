---
summary:
---
# Pivotal Cloud Foundry - Define PCF Routes and Configure IIS Routing Rules

<div class="info" markdown="1">

**Note:** Make sure that you meet the [systems requirements](<https://success.outsystems.com/Support/Archive/11/OutSystems_Platform_system_requirements#Pivotal_Cloud_Foundry>) and [network requirements](<https://success.outsystems.com/Support/Archive/11/OutSystems_network_requirements#Containers_considerations>) for deploying to Pivotal Cloud Foundry.

</div>

During the process of deploying an application to Pivotal Cloud Foundry (PCF) (detailed steps available in [Deploying an Application to Pivotal Cloud Foundry](<https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Deploying_to_Containers/Running_Your_Application_in_a_Container/Deploying_an_Application_to_Pivotal_Cloud_Foundry>)), you will push, set up and start your application running in a PCF container. 

After this step, you will need to make sure that the application inside the container is accessible through its configured deployment zone address and through the same public address of your Platform Server. 

<div class="info" markdown="1">

In this example, we will leverage as a simplified **main load balancer and reverse proxy** the Internet Information Services (IIS) running on the machine where Platform Server is installed.

If you are using another routing or reverse proxy software, follow the general configuration guidelines provided below and adapt the instructions accordingly.

We also assume that your PCF infrastructure has a configured SSL certificate, trusted by IIS.

This example presents one of several possible solutions for handling the routing associated with applications running in containers. Be sure to validate your routing configuration with your Network and DevOps teams, but remember that this is **not** a recommended production scenario.

</div>

The instructions provided below allow you to define the minimum configurations on PCF and IIS routing rules needed to ensure the connectivity:

* Between the OutSystems platform and the example application modules running on PCF
* Between external users and the example application modules running on PCF

## Example: The "Directory" Web Application

We will configure routing rules for a simple application called "Directory" containing two modules: **Directory** and **Employees**. 

Our goal is to make sure that the two application modules are reachable using the configured address for the application deployment zone and the public address, i.e. in this example the two modules **Directory** and **Employees** must be reachable via internal network at addresses [`<zone_address>/Directory/`, `<zone_address>/Employees/`] and via public network on [`<public_address>/Directory/`, `<public_address>/Employees/`].

To ensure this, you can configure the IIS used by the Platform Server as a reverse proxy (responding on `<public_address>`) to route the request to the PCF Application where the container was launched.  

As an example, lets consider you have the following domains in your Pivotal Apps Manager:

![](<images/iis-pcf-org-domain.png>)

Where:

* `<zone_address>` is defined as `os.pcf.example.com`
* `<public_address>` is defined as `public.domain.example.com`

Take the following steps:

<div class="info" markdown="1">

_Note:_ You can skip steps 1 to 3 if you already completed them.

</div>

1. Download the [`PCFUtils.psm1` PowerShell module](<https://github.com/OutSystems/ContainerAutomation/blob/master/misc/pcf/PCFUtils.psm1>) into a given folder.  
_Note:_ This script requires that the PowerShell Execution Policy is set to `unsigned`. For more information [check Microsoft's documentation](<https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-6>).

1. In a PowerShell console, run the following command to import the module:

        Import-Module <path>/PCFUtils.psm1
    
    Replace `<path>` with the parent folder you chose for the script.

1. In the same PowerShell console, execute the following command to add the routes for each module of your application to PCF:

        Add-CFRoutes -Filepath <bundle_path> -AppName <app_name> -PublicAddress <public_address> -ZoneAddress <zone_address>

    Replace:

    * `<bundle_path>` with the path to the application bundle ZIP file
    * `<app_name>` with the application name in PCF, as stated in the output of the previous `cf push` command
    * `<public_address>` with your public address of your main load balancer and reverse proxy, as described in the [PCF requirements](<https://success.outsystems.com/Support/Archive/11/OutSystems_Platform_system_requirements#Pivotal_Cloud_Foundry>)
    * `<zone_address>` with your PCF zone address (also as described in the PCF requirements)

    This will ensure that PCF can route requests to your application modules.

    Following our previous example:

        Add-CFRoutes -Filepath "C:\Program Files\OutSystems\Platform Server\pcf\3949aa6b-0d51-4fb6-aa60-f974b4c6b2aa_172afb7a-a333-429c-a06c-fe9e352cdd3f.zip" -AppName Directory-PublicAddress public.domain.example.com -ZoneAddress os.pcf.example.com

1. Install the [Application Request Routing](https://www.iis.net/downloads/microsoft/application-request-routing) and [URL Rewrite](<https://www.iis.net/downloads/microsoft/url-rewrite>) extensions in IIS. The former allows you to define rule-based routing configurations, while the latter allows you to define rules for implementing user-friendly URLs.

1. Obtain the list of routes associated with your container:

    `cf app <app_name>`

    Example output:

        >cf app "Directory"
        Showing health and status for app Directory in org myorganization / space Default as admin...
        name:              Directory
        requested state:   started
        instances:         1/1
        usage:             512M x 1 instances
        routes:            directory.pcf.example.com,
                           public.domain.example.com/Directory,
                           os.pcf.example.com/Directory, 
                           public.domain.example.com/Employees,
                           os.pcf.example.com/Employees
        last uploaded:     Fri 3 Aug 10:57:57 BST 2018
        stack:             windows2016
        buildpack:         binary_buildpack
            state     since                  cpu    memory           disk          details
        #0   running   2018-07-04T21:48:36Z   0.2%   110.7M of 512M   88.4M of 1G

1. Configure the Application Request Routing proxy settings. 

    1. Open IIS Manager, click on the **server** name, open the "Application Request Routing Cache" module and click the "Server Proxy Settings..." link on the right sidebar. 

    1. Change your settings to match the ones presented in the following image and then click "Apply" on the right sidebar:

        ![](images/iis-enable-proxy.png)

    Make sure that:  
– "Enable Proxy" is **checked**  
– "Reverse rewrite host in response headers" is **unchecked**  
– "Preserve client IP in the following header" is set to `X-Forwarded-For`.

1. Create a new blank routing rule for **each module** according to the following image. You will need to check the routes list obtained in step 3. Give the rule a name of your choice.

    _Tip:_ Check Microsoft's documentation on [how to create a rewrite rule](https://docs.microsoft.com/en-us/iis/extensions/url-rewrite-module/creating-rewrite-rules-for-the-url-rewrite-module#creating-a-rewrite-rule).

    ![](<images/iis-pcf-module-rule.png>)

    Relevant field values:  
*Match URL* – Pattern: `^<module_name>/(.*)`  
*Action*  
– Action type: `Rewrite`  
– Rewrite URL: `https://<zone_address>/<module_name>/{R:1}`  
– "Stop processing of subsequent rules" is **checked**

    Following our example, in this step you would create two routing rules, one for the **Directory** module and another one for the **Employees** module.

    Click "Apply" at the top of the right panel to create the rule.

1. Check that you can access the modules using the deployment zone address.  
Following our example, check if the modules **Directory** and **Employees** are reachable at addresses [`<zone_address>/Directory/`, `<zone_address>/Employees/`] and also [`<public_address>/Directory/`, `<public_address>/Employees/`].

_Note:_ You will need to remove the rewrite rules added to IIS if you deploy the application back to the "Global" deployment zone.
