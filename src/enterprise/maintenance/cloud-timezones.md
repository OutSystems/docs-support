---
locale: en-us
guid: 5207df8b-21b6-4050-89b1-4f582f04e04f
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# OutSystems Cloud and time zones

The OutSystems platform has a strong requirement regarding time settings for the involved parts (front-ends and databases): they all have to be in the same time, and with little offsets. This is explained in this [article](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Timezone_considerations_in_the_OutSystems_Platform).

In the OutSystems Cloud all servers are set to work in the UTC time zone. This configuration cannot be changed.

Applications that need to deal with time zone differences from UTC need to consider that from the early phases of development.

Techniques for achieving the result can be found in components such as the (unsupported) [Timezone forge component](http://www.outsystems.com/forge/component/500/time-zone/).

Other techniques may be used to obtain the same effect.

