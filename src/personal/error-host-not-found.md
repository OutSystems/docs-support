---
summary: If you can't connect from the IDE to your personal environment, check if your environment was recycled. Login at outsystems.com to check this.
---

# There was an error contacting outsystemscloud.com: Host not found

## Symptom

When trying to connect to your personal environment from the IDE, you get the error:

`There was an error contacting [my].outsystemscloud.com. Host not found.`

## Cause

This problem can happen due to:

* Bad internet connection;

* Your personal environment has been recycled, after a long period of inactivity.

## Resolution

Since you're reading this, we can assume your internet connection is working fine. On your IDE, try reconnecting to your personal environment again.

If the problem has not been solved yet, it's probable that you haven't used your personal environment in quite some time, so it fell asleep or was closed. 

### Step 1 

Check the state of your personal environment by visiting `https://<yourpersonal>.outsystemscloud.com`.

* If you can see your applications, then your personal environment is up and running and you **should** be able to connect to it from the IDE.

* If you are redirected to [https://www.outsystems.com/home/](https://www.outsystems.com/home/) then your personal environment fell asleep or was closed.

![](images/error-host-not-found_0.png)

### Step 2

If your personal environment fell asleep, you just need to wake it up. Click the **WAKE IT UP NOW** button.

If your personal environment is closed due to a long period of inactivity, click the **FETCH ME A NEW ONE** button. A new environment will be provisioned for you, with the same URL you had before.

Since a new environment has been provisioned your applications will not be available in this new environment. Check the email you received from us warning that your environment was scheduled for recycling. There you have a link to a snapshot of the code of your apps.

