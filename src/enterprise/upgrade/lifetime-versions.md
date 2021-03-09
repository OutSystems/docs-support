---
summary: This article describes which are the Platform Server versions, installed in the OutSystems environments, that LifeTime can manage.
tags: lifetime;
---

# Which versions of Platform Server can LifeTime manage?

LifeTime is the centralized management console for managing your OutSystems application environments, such as development, quality, and production environments.

The interaction between LifeTime and the OutSystems environments managed by this console depends on the Platform Server version that is installed in each of those OutSystems environments.

This article describes which are the Platform Server versions, installed in the OutSystems environments, that LifeTime can manage.

## Platform Server versions managed by LifeTime

The range of Platform Server versions that can be managed by LifeTime is different since version OutSystems 11.  

### Up to OutSystems 10

Up to version OutSystems 10, **LifeTime can manage** OutSystems environments running the **same Platform Server major version** than LifeTime environment. Except during [the infrastructure upgrade period](#what-happens-during-an-upgrade-period), LifeTime cannot manage OutSystems environments running a different Platform Server major version.

Also, to guarantee its correct behavior, the LifeTime environment must be **the most up-to-date environment** in the infrastructure, meaning that all the OutSystems environments managed by LifeTime must be running the same or lower Platform Server version than the LifeTime environment.

Examples:

![](images/lifetime-versions-1.png?width=800)

### From OutSystems 11 onwards

From version OutSystems 11 onwards, LifeTime is distributed separately from the Platform Server, which enables both components to have different upgrading pace.

Therefore, from version OutSystems 11 onwards, **LifeTime can manage** OutSystems environments running all the **supported Platform Server versions**. This means that for OutSystems 11, LifeTime can manage OutSystems environments running Platform Server 10.0.105.0 or higher. Except during [the infrastructure upgrade period](#what-happens-during-an-upgrade-period), LifeTime cannot manage OutSystems environments running Platform Server version lower than 10.0.105.0.

Examples:

![](images/lifetime-versions-2.png?width=800)

In this scenario, a feature will be available in LifeTime if it is known by both LifeTime and the managed environment. A new feature included in the installed LifeTime version, but that is not available yet in the Platform Server version installed in the managed OutSystems environments, will not be available in LifeTime.

For example, deployment zones is a new feature of OutSystems 11. In OutSystems 11, LifeTime knows how to handle deployment zones when managing OutSystems environments running Platform Server version 11. However, if the managed environments are running Platform Server version 10, the deployment zones feature is not available in LifeTime.

To deploy an application throughout your OutSystems infrastructure, from development to production, all your OutSystems environments must be running the same Platform Server major version. 

## What happens during an upgrade period?

Depending on the size of your infrastructure and applications portfolio, upgrading all your OutSystems environments to a major Platform Server version might take some time, since you need to upgrade the Platform Server in each environment and test the applications before proceeding to the next environment.

During this upgrade period, the OutSystems environments managed by LifeTime may have different Platform Server major versions and some LifeTime features will be unavailable for those environments, such as deployments and analytics. You will not be able to deploy between environments having different Platform Server major versions.

Although with limited features, LifeTime can still manage OutSystems environments within a specific range of Platform Server versions, so you should keep the environments registered in LifeTime during the upgrade period. 

### Up to OutSystems 10

Up to version OutSystems 10, during an upgrade period **LifeTime can manage with limited features** OutSystems environments **from Platform Server version 7.0**.

### From version OutSystems 11

From version OutSystems 11, during an upgrade period **LifeTime can manage with limited features** OutSystems environments **from Platform Server version 9.0.1**.
