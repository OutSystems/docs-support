---
summary: Learn how to resolve issues in OutSystems 11 (O11) cloud environments by retrying synchronization or restarting services.
locale: en-us
guid: 814d4a99-9c7c-4418-9788-34b5dcdf6f88
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# Restart services on OutSystems Cloud


## Overview 

Should any issues with OutSystems services arise on a cloud environment, you can check the related errors and:

* Retry synchronization to see if it's just a communication issue.
* Restart the OutSystems services in case they got stuck.


This option isn't available in Personal Environments.


## Resolution 

![Screenshot highlighting the 'Environment Health Problems' notification and detail button in the OutSystems Cloud interface.](images/restart-cloud-health-lt.png "OutSystems Cloud Environment Health Overview")

On 1 you can check the detail of the error and on 2 you can have some more details about that environment:

![Screenshot showing the 'Development Environment Status' with an error message and a 'Retry Synchronization' option.](images/restart-cloud-status-lt.png "OutSystems Cloud Environment Status and Synchronization")

On the error report, you can try to sync your environment again just to see if this was just a communication problem. If it doesn't resolve the issue, then you can go to the environment details and restart OutSystems services:


![Screenshot of the OutSystems Cloud interface with an option to 'Restart Services' for resolving environment health problems.](images/restart-cloud-lt.png "OutSystems Cloud Environment Restart Services Option")

<div class="info" markdown="1">

Clicking **Restart Services** performs an IIS reset, clears the application pools, and Restart all OutSystems Services (OutSystems Deployment Controller Service, OutSystems Deployment Service, OutSystems Scheduler Service) and clears any hanging requests. In the case of multiple front-ends, this restart is balanced (front-end servers are restarted one at a time). 

</div>
