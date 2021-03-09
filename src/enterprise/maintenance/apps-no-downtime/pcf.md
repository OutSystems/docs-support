# No-downtime deployments with Pivotal Cloud Foundry (PCF)

The following instructions are based on PCF's [Blue-Green deployment guidelines](https://docs.pivotal.io/pivotalcf/2-2/devguide/deploy-apps/blue-green.html) with some adaptations.

## Staging from Classic Virtual Machines to PCF

1. **Publish the application to PCF.**

    Follow the guide on [Deploying an Application to PCF](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Deploying_to_Containers/Running_Your_Application_in_a_Container/Deploying_an_Application_to_Pivotal_Cloud_Foundry) up to updating the "Main Load Balancer and Reverse Proxy" to redirect requests to the application in PCF (step 4).

    <div class="info" markdown="1">

    _Note:_ Complete the step where routes are mapped in PCF but **do not create** the `.deploydone` result file.  
    This would cause the un-deployment of the application from the deployment zone configured with "Classic Virtual Machines" hosting technology.
    
    </div>

1. **Verify the status of the application before switching it between deployment zones.**

    Check that the application modules are accessible at the following address:

    `https://<zone_address>/<module_name_N>`

    <div class="info" markdown="1">
    
    _Note:_ This step is targeted at **simple and fast connectivity validations**. Until the deployment process is completed, i.e. until you create the `.deploydone` result file in the `results` folder, **no other deployment** can be completed.  
    Also, keep in mind that the deployment process will time out after 30 minutes. 
    
    </div>

1.  **Complete the switch between deployment zones.**

    Follow the remaining steps mentioned on [Deploying an Application to PCF](<https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Deploying_to_Containers/Running_Your_Application_in_a_Container/Deploying_an_Application_to_Pivotal_Cloud_Foundry>):

    1. Create a rewrite rule in your "Main Load Balancer and Reverse Proxy" making the application modules deployed to PCF available to users;

    1. Create the `.deploydone` result file.

## Upgrading application versions/Updating configurations of an app on PCF

1. **Publish the upgraded/updated application to PCF.**

    1. Follow [Deploying an Application to PCF](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Deploying_to_Containers/Running_Your_Application_in_a_Container/Deploying_an_Application_to_Pivotal_Cloud_Foundry) up until `cf push` (end of step 2).

        <div class="info" markdown="1">

        _Note:_ Complete the step where routes are mapped in PCF but **do not** create the `.deploydone` result file.  
        This would cause the un-deployment of the application from the deployment zone configured with "Classic Virtual Machines" hosting technology.
        
        </div>

    1. To avoid replacing the previous application version, the new version must be pushed to PCF with a different name, e.g. `app_name_ver_2`.  

        Execute the following command:

        `cf push <app_name_ver_2> --no-route`

        The `--no-route` parameter is **optional**. PCF will create a default route for new applications; since this route is not necessary, it can be omitted by adding the `--no-route` parameter.

1. **Verify the status of the application before switching versions.**

    1. To check the availability of new application versions, [create a new subdomain for your org](https://docs.cloudfoundry.org/devguide/deploy-apps/routes-domains.html#private-domains) (e.g. `<test_subdomain>.<shared_pcf_domain>`).

    1. Create the routes for each application module (repeat for each module name):

        `cf map-route <app_name_ver_2> <test_subdomain>.<shared_pcf_domain> --path <module_name_N>`

    1. Check that application modules are accessible at `<test_subdomain>.<shared_pcf_domain>/<module_name_N>`

    <div class="info" markdown="1">
    
    _Note:_ This step is targeted at **simple and fast connectivity validations**. Until the deployment process is completed, i.e. until you create the `.deploydone` result file in the `results` folder, **no other deployment** can be completed.  
    Also, keep in mind that the deployment process will time out after 30 minutes. 
    
    </div>

1. **Complete the switch between versions.**

    1. Switch between the previous version of the application (e.g. `app_name`) and the new version (e.g. `app_name_ver_2`) for each of the applications modules.  
        Run the following commands on a PowerShell console (repeat for each module name):

        `cf map-route <app_name_ver_2> <public_address> --path <module_name_N> ;`

        `cf map-route <app_name_ver_2> <subdomain>.<shared_pcf_domain> --path <module_name_N> ;`

        `cf unmap-route <app_name> <public_address> --path <module_name_N> ;`

        `cf unmap-route <app_name> <subdomain>.<shared_pcf_domain> --path <module_name_N> ;`

    1. _(Optional)_ If you verified the status of the application before switching versions as described in step 2, you can unmap that route:

        `cf unmap-route <app_name_ver_2> <test_subdomain>.<shared_pcf_domain> --path <module_name_N>`

1. **Create the `.deploydone` result file.**

After performing these steps, no additional configurations should be required for the "Main Load Balancer and Reverse Proxy".
