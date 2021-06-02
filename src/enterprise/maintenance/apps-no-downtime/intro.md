---
summary: How to perform no-downtime deployments when deploying OutSystems applications to containers (for advanced users).
tags: article-page
---

# Deployment strategies with containers

<div class="info" markdown="1">

**Note:** Though we explicitly mention "applications" throughout this document, since this is the deployment unit for container-based hosting technologies, always have in mind that an "application" represents a set of "modules".

</div>

Previously, when the OutSystems platform interacted directly (and exclusively) with IIS — known as "Classic Virtual Machines" deployment technology in OutSystems 11 —, achieving no-downtime during the deployment of new application versions or when updating configurations had little to no impact.

Now, with the support for applications running in containers, achieving no-downtime when executing these processes requires additional steps specific to the hosting technology being used.

While the information provided in this document is mostly targeted at applications being staged between environments using **LifeTime**, there are a few scenarios where this is also relevant in a single environment scenario, e.g. when updating configurations of an application or when moving an application from "Classic Virtual Machines" to a container-based hosting technology using **Service Center**.

## Before you start

This document assumes that:

* The target container-based infrastructure meets all the [recommended network pre-requisites](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Deploying_to_Containers/Recommended_Network_Architecture);
* All other [container-specific requirements](https://success.outsystems.com/Support/Archive/11/OutSystems_Platform_system_requirements#Containers_considerations) are also guaranteed.

Additionally, the guidelines presented in this section assume that:

* The "Main Load Balancer and Reverse Proxy" has a **default rule** pointing to the OutSystems Platform Server for application modules that have no explicit rules defined.

* The "Main Load Balancer and Reverse Proxy" will have **specific rewrite rules** for the OutSystems applications modules deployed in the selected container-based hosting technology.

Although these steps can be performed manually, they should be performed automatically by using the "Container Run" extensibility hook provided by the "Automated Mode" in the Deployment Zone configuration.

Adapt the provided instructions as needed to your specific network infrastructure setup.

## Deployment strategies

The provided guidelines for achieving no-downtime deployments in different hosting technologies follow one of these two common deployment strategies:

Blue-Green
:   The blue-green deployment strategy is a deployment strategy where we have 2 identical environments, a live one (blue) and an idle one (green), and we can test the green environment separately without impacting the blue one. After testing, we switch traffic from the blue environment to the green one.

    This strategy is ideal for migrating from "Classic Virtual Machines" to container-based hosting technologies, thus minimizing the impact.

    ![Blue-Green deployment strategy diagram](images/strategy-blue-green.jpg?width=750)

Rolling Update
:   The rolling update strategy is a deployment strategy where the application is updated in a incremental fashion. Each container with the new application version is launched, replacing the old version. This process is done incrementally for each replica.

    This strategy optimizes resource usage and it's ideal for version updates.

    ![Rolling Update deployment strategy diagram](images/strategy-rolling-update.jpg?width=750)
