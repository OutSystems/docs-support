---
summary: What to do when LifeTime staging aborts after renaming an app or module.
Tags:
locale: en-us
guid: 970FB4B3-B224-4FFA-A675-1BA893CA0DCE
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# LifeTime staging aborts after renaming an app or module

## Symptoms

While you are staging a new app to your target environment, the staging is aborted and you get the following error message:

`Error uploading version <version_key> of module AppA: Name Conflict: Cannot publish AppA because another module with the same name already exists in the environment.`

## Cause

This happens because during the staging, LifeTime compares the names of all applications and modules in the staging plan with the names of all the applications and modules in the target environment and there's a conflict.

**Example:**

- You have an application called AppA across all environments.
- You change the name of the app in the source environment from AppA to AppB. 
- You then create a new app in the source environment, and call it AppA. When you stage this new app to the target environment, the staging is aborted and you get the error message because the target environment already has an app with the same name (AppA).


## Resolution

Always stage any changed apps to the target environment before creating a new app in the source environment. Going back to the example, to prevent this:

- In the source environment, rename the app from AppA to AppB and stage the changes to the target environment.
- In the source environment, create a new application AppA and stage to the target environment.

