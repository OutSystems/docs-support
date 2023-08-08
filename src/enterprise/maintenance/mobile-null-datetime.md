---
summary: This article describes the differences in the null DateTime value between different OutSystems versions. It is relevant to the development of mobile apps.
tags: support-maintenance;
locale: en-us
guid: 9a463cd2-53c3-4e1f-8040-e71ac11ae99b
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# Behavior of the Null DateTime Value in Mobile Apps

Depending on the Platform Server version at the first installation of your environment, the DateTime null value may change in mobile apps when written to or read from the local storage. It may also change when sent to the server. This is due to the resolution of an issue regarding the null DateTime
value.

The value `#1900-01-01 00:00:00` represents the null for DateTime data type and can be assigned manually or by the value returned after calling the built-in `NullDate()` function. In Platform Server 10.0.804.0 and lower there was an issue which caused the null DateTime value to not be treated as the
null value, which made the default `#1900-01-01 00:00:00#` behave as any other time and date value. This issue can become critical if you have mobile apps that store and handle the null value. Web applications are not affected.

OutSystems decided to keep the previous behavior in all current Platform Server installations and their future updates. The behavior is being kept to prevent breaking the workarounds that developers may have already adopted. Read the following sections to learn more.

## Environments installed before Platform Server 10.0.804.0

When writing the null DateTime value from local storage or saving it to the local storage, as well as when sending it to the server, the time and date are adjusted for the time zone difference in relation to the UTC time.

For example, a mobile device in New York initializes a variable `myDateTime` with `myDateTime = NullDate()`. What is saved in the local storage is `myDateTime = #1900-01-01 05:00:00#`, because the UTC-5 time zone is converted to UTC. If the value is read in Paris, in UTC+1, the returned value is
`myDateTime = #1900-01-01 06:00:00#`due to UTC to UTC+1 adjustment. The system adjusts the value for the time zone difference.

This applies to mobile apps in all environments installed before Platform Server 10.0.804.0, regardless of any future upgrade to the version number 10.0.804.0 or above.

## New installations of Platform Server 10.0.804.0 and later

When writing the null DateTime value from local storage or saving it to the local storage, or when exchanging it on the server, the time and date remain the null value.

For example, a mobile device in New York initializes a variable `myDateTime` with `myDateTime = NullDate()`. What is saved in the local storage is `myDateTime = #1900-01-01 00:00:00# `, because the UTC-5 time zone is not converted to UTC. If the value is read in Paris, in UTC+1, the returned value
is still `myDateTime = #1900-01-01 00:00:00#`.

This applies to mobile apps in all new environment installations with the version number 10.0.804.0 or greater.

## Changing the DateTime null behavior

Refer to the instructions in this section if you want the DateTime null to behave like the DateTime null in the new installations of Platform Server 10.0.804.0 and later.

For these instructions to work, you need to be using Platform Server 10.0.804.0 and later.

### In On-Premises Environments

Follow these steps if your have Platform Server deployed to your own infrastructure.

1. In the Database, and for the OSSYS_PARAMETER table, run the following query:
`INSERT INTO ossys_parameter (NAME, VAL, HOST, HOST_SERIAL) VALUES ('Compiler.MobileRuntime.ApplyTZForNullDates', 'false', null, null);`
1. Restart OutSystems Deployment Controller Service on the server.
1. Publish the affected module(s).
1. Confirm the changes were successfully applied.

### In Cloud Environments

Please contact Support and request changes to your Platform settings. 



