---
summary: Scale your environments horizontally by adding new front ends to deal with increased user load and application complexity.
locale: en-us
guid: 41efb22b-80b4-49fa-8c0f-53d1b77a0732
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# Add a new front-end server to your environment

Adding more front-end servers to an environment is a simple process of installation and configuration for your On-Premises installation. Your team can add as many front-end servers as needed for unlimited horizontal scalability. The Platform Server automatically synchronizes applications to the new front-end servers.

## Benefits of this feature

As well as providing [high availability](https://www.outsystems.com/evaluation-guide/how-does-outsystems-provide-horizontal-scalability/#High_availability), scaling horizontally helps to deal with increased:

* User load with more users or more frequent usage
* Business logic complexity or load
* Volume of batch processing
* Data volume or number of transactions

## Add a new front-end server

<div class="info" markdown="1">

When adding a new front-end server to your environment, make sure that:

* There are no ongoing deployments or solution publishes.
* There are no prepared deployments to continue, in case you have [two-stage deployments](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Deploy_Applications/Deploy_in_a_Short_Deployment_Window) enabled in the environment.

Having ongoing or prepared deployments when adding a new front-end server might prevent the correct deployment of the modules.

</div>

### On OutSystems Cloud

Scaling of resources in OutSystems Cloud depends on the customer's subscription.

When scaling is needed, [submit a request to OutSystems support](https://success.outsystems.com/Support/OutSystems_community/Opening_a_support_case_with_OutSystems), which responds according to the request priority and respective SLAs.

* For Horizontal scaling requests, the new front-end server is created and added to the load balancer automatically, becoming immediately available after provisioning ends.
 
* For Vertical scaling of front-end servers, upon customer request, OutSystems proposes a schedule for the upgrade, subject to customer confirmation.

**Note that for environments with only 1 front-end, the front-end scale-up operation causes a downtime of approximately 30 minutes.**

For production environments with 2 or more front-ends, the front-end scale-up causes a reduction of processing capacity, but there is no downtime. All front-ends are scaled up to the same server class.


### On self-managed environments

<div class="info" markdown="1">

Make sure the new front-end server is a clean installation, it doesn't contain settings or deployed applications from a previous OutSystems installation. Otherwise, you might need to republish all the environment modules or the deployment of new applications might fail.

</div>

On the environments you manage, follow a standard server installation:

1. Make sure all the [Installation prerequisites](https://success.outsystems.com/Documentation/11/Setting_Up_OutSystems#Installation_prerequisites) are met.
1. Download the Platform Server installation binaries. Make sure you download the same version that's already running on the other servers of the environment.
1. Follow the installation checklist that's bundled with the Platform Server by:
    * Selecting the **First install** task
    * Choosing the role (the name of the role depends on the Platform Server version):
        * For Platform Server version 11.0.542.0 onwards, choose the **Server** role
        * For all other versions, choose the **Front-end Server** role
    * Select the applicable operating system and database software options

#### Use automation to add new front ends

It's possible to automate horizontal scalability using OutSystems unattended installation commands. The complete instructions can be found at [this document](https://success.outsystems.com/Documentation/11/Setting_Up_OutSystems/Unattended_Installation_and_Upgrade#Adding_a_Front-End).

#### OutSystems on Microsoft Azure

If you're using [OutSystems solution template for Microsoft Azure Marketplace](https://success.outsystems.com/Documentation/11/Setting_Up_OutSystems/OutSystems_on_Microsoft_Azure), you can take advantage of Azure scale sets for horizontal scalability. For complete instructions, check [Using Azure scale sets](https://success.outsystems.com/Documentation/11/Setting_Up_OutSystems/OutSystems_on_Microsoft_Azure/Additional_Configurations_for_OutSystems_on_Microsoft_Azure#Scale_Your_Environments_Using_Azure_Scale_Sets).

