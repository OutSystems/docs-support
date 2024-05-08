---
summary: OutSystems 11 (O11) addresses app synchronization issues by allowing users to manually sync app definitions across environments in LifeTime.
locale: en-us
guid: 12e41bb0-8e98-41a5-b186-b32d9cf1be46
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/6tXLupLiqfG9FOElATTGQU/Troubleshooting?type=design&node-id=3599%3A53&mode=design&t=42fmTjympCA6AMpf-1
---

# Synchronize app definition

## Symptoms

LifeTime shows an app's name, icon, or color that doesn’t reflect the actual values these attributes have for a particular environment in your factory.

## Cause

At the infrastructure level, LifeTime presents a unified view of an app, including its name, color, and icon. However, this can sometimes lead to confusion, as these attributes can vary across different environments. For example, if you modify any of these attributes using the **Edit Application** screen in Service Studio within the Development environment, LifeTime reflects those changes, even if the updated version of the app hasn't been propagated to other environments yet. Therefore, LifeTime displays an app's most recently modified values, regardless of the infrastructure environment in which the changes were made.

## Resolution

In LifeTime, to display an application's name, icon, and color from a particular environment, go to the Application's details screen, and from the **Environment Options** dropdown, click **Synchronize App Definition**.

![Sync app definition in LifeTime](images/sync-app-def-lt.png "Sync app definition in LifeTime")
