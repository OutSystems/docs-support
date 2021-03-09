---
summary:
---

# Timezone considerations in the OutSystems Platform

In an OutSystems Platform environment the database, controller and all front-ends are required to be in the same timezone.

The rationale for this is to ensure a simpler mental model for both developers and operators. If the time is consistent across the environment, it's easier for all to understand when time-dependent events (timers, BPT) are supposed to occur. This also makes programming with times simpler as the developer does not need to do complicated code to normalize timestamps in their applications.

In addition to being in the same timezone, OutSystems also recommends that all parts of an environment be synchronized in terms of time. Time drifts greater than a few seconds can lead to unexpected behavior. It is recommended by OutSystems that customers sync all their front-ends and database with the same NTP time server.

