---
summary:
locale: en-us
guid: 95d95b60-3661-48aa-b75d-e2f670cf6b92
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# Timezone considerations in the OutSystems Platform

In an OutSystems Platform environment the database, controller and all front-ends are required to be in the same timezone.

The rationale for this is to ensure a simpler mental model for both developers and operators. If the time is consistent across the environment, it's easier for all to understand when time-dependent events (timers, BPT) are supposed to occur. This also makes programming with times simpler as the developer does not need to do complicated code to normalize timestamps in their applications.

In addition to being in the same timezone, OutSystems also recommends that all parts of an environment be synchronized in terms of time. Time drifts greater than a few seconds can lead to unexpected behavior. It is recommended by OutSystems that customers sync all their front-ends and database with the same NTP time server.

