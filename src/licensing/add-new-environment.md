---
summary: Guide on adding a new environment to OutSystems 11 (O11) infrastructure, covering both cloud and self-managed setups.
locale: en-us
guid: fa47e66e-155d-4b3c-b64d-945de079d123
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
tags: outsystems infrastructure, cloud setups, self-managed setups, licensing, system requirements
audience:
  - platform administrators
  - full stack developers
  - infrastructure managers
outsystems-tools:
  - lifetime
  - service studio
coverage-type:
  - apply
---

# Add a new environment to your infrastructure

To add a new environment to your infrastructure, first contact your sales representative to discuss the requirements for the new environment and the details about obtaining an additional license.

For Cloud customers OutSystems will process your order, set up the new environment, and notify you by email when the new environment is available for use.

For self-managed installations:

1. Before installing any component of OutSystems, make sure your hardware and software comply with the minimum requirements. For this, be sure to check:
    * [System requirements](https://success.outsystems.com/documentation/11/setup_and_maintain_your_outsystems_infrastructure/setting_up_outsystems/outsystems_system_requirements/)
    * [Network requirements](https://success.outsystems.com/documentation/11/setup_and_maintain_your_outsystems_infrastructure/setting_up_outsystems/outsystems_network_requirements/)
1. Install and prepare the new environment. See [Setting Up OutSystems](https://success.outsystems.com/Documentation/11/Setup_and_maintain_your_OutSystems_infrastructure/Setting_Up_OutSystems) for more information.
1. Register the serial number, download, and install the license in your new environment. See [here](../enterprise/licensing/manage/get-license-for-env.md) the complete instructions.
1. Register the new environment in the management console, LifeTime. See [Configure the infrastructure management console](https://success.outsystems.com/Documentation/11/Setup_and_maintain_your_OutSystems_infrastructure/Setting_Up_OutSystems/Configure_the_infrastructure_management_console) for more information.

In case you experience problems when registering an environment in LifeTime, you can refer to [this documentation](https://success.outsystems.com/support/troubleshooting/application_lifecycle/error_registering_an_environment_in_lifetime/) to troubleshoot that issue.

Customers with a hybrid configuration (with some should environments in the OutSystems Cloud and others as self-managed) should contact [technical support](https://www.outsystems.com/legal/success/support-terms-and-service-level-agreements-sla-of-the-outsystems-software/#contact-channels) for instructions about how to add a new environment.

<div class="info" markdown="1">

Hybrid configurations are supported only in OutSystems licenses purchased **before January 2020**.

</div>
