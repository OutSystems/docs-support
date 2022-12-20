---
summary:  What to do when your app is unexpectedly renamed after staging it to the target environment.
Tags:
locale: en-us
guid: 828DA276-1480-4EA6-B5B1-66E488182743
app_type: traditional web apps, mobile apps, reactive web apps
---

# Application renamed unexpectedly after staging 

## Symptoms

Your app is unexpectedly renamed after staging your app to the target environment.

**Example**:

- You have 3 environments registered in LifeTime - Development, QA, and Production.
- You have AppA in the 3 environments.
- In the Dev environment, you change the name of the app to ToBeDeleted_AppA.
- You execute the staging process (which includes your app) between the QA and Production environments.
- When staging is complete, the application name in the Production environment is ToBeDeleted_AppA.

## Cause

LifeTime has a centralized copy with app details such as name, icon, and color. This copy has the last change made in the applications across the infrastructure. When a staging occurs, the application details sent to the target environment are those present in LifeTime.

Going back to the example above, you changed the name of the application in the Development environment to ToBeDeleted_AppA, so when the Dev environment syncs in LifeTime, LifeTime updates the name in its copy. Therefore, when you execute the staging process for the changed app, the name of the app in the target environment will be the name displayed in LifeTime.

## Resolution

Before starting the staging process, always confirm the application name that is displayed in LifeTime. The target environment will be updated with that name.
