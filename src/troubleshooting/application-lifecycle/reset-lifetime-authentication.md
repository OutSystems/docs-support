---
summary:
locale: en-us
guid: ee89babf-f053-4269-8485-d75ff21a2a27
---

# Reset LifeTime authentication preferences

This articles applies to: on-premise infrastructures

## Symptoms

You've been locked out of LifeTime/Service Center and cannot login.

## Cause

Usually this happens when you activate Active Directory (with Windows Integrated) authentication with incorrect configurations, thus failing all logins.

## Resolution

To resolve this issue, please run the following script in the databases of the Lifetime environment and all the environments that are registered in it:

`UPDATE OSSYS_AUTHPROVIDER SET ISACTIVE = 0;`

`commit;`

After that you will be able to login on LifeTime/Service Center with your previous credentials.

