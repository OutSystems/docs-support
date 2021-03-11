---
summary:
---

# Daylight Savings time change can cause some BPT activities to not be processed

## Overview

We have identified a potentially critical bug which manifests itself during Daylight Savings time change. This causes that some BPT activities may not get processed by the OutSystems Platform. In severe situations this can cause a complete lockdown of the BPT system, meaning that no more activities are processed altogether.

The issue is that activities scheduled to be executed during the missing hour are never started, but they remain scheduled to be executed. There are even critical situations where the BPT system will only try to execute these activities and thus may be unable to start any other activities.

This is causing a delay in the execution of the activities, not repetition, so it’s not expected to cause data corruption.

Affected Stacks and Versions

**.NET**: this stack is affected by this problem

**Java**: this stack is not affected by this problem

**Cloud**: default cloud configurations are not affected by this problem as they use UTC. Customers who have requested their infrastructure to have its timezone changed may be affected by this problem if they use the BPT functionality.

**Versions**:

* 7.0.1.25+

* 8.0.1.8+

* 9.0 (all versions)

* 9.1 (all versions)

## How do I detect if the issue is affecting me

If you go to **Service Center > Monitoring > Environment Health** and don’t have any Pending Activities, this means that you are not experiencing the issue.

However, if you are constantly seeing some Pending activities, you might be affected by this problem.

To confirm whether you are affected or not, please execute the following query in the OutSystems Platform’s database and check if any results are returned. Remember you’ll need to adapt the dates to the ones that are relevant for your time zone.

```
SELECT
  OSSYS_ESPACE.NAME ESPACE_NAME,
  OSSYS_TENANT.NAME TENANT_NAME,
  OSSYS_BPM_PROCESS_DEFINITION.NAME PROCESS_NAME,
  OSSYS_BPM_ACTIVITY_DEFINITION.NAME ACTIVITY_NAME,
  OSSYS_BPM_ACTIVITY.ID ACTIVITY_ID,
  OSSYS_BPM_ACTIVITY.PROCESS_ID,
  OSSYS_BPM_ACTIVITY.NEXT_RUN
FROM OSSYS_BPM_ACTIVITY
  INNER JOIN OSSYS_BPM_PROCESS ON OSSYS_BPM_PROCESS.ID = OSSYS_BPM_ACTIVITY.PROCESS_ID
  INNER JOIN OSSYS_BPM_ACTIVITY_DEFINITION ON OSSYS_BPM_ACTIVITY_DEFINITION.ID = OSSYS_BPM_ACTIVITY.ACTIVITY_DEF_ID AND OSSYS_BPM_ACTIVITY_DEFINITION.IS_ACTIVE = 1
  INNER JOIN OSSYS_BPM_PROCESS_DEFINITION ON OSSYS_BPM_PROCESS_DEFINITION.ID = OSSYS_BPM_ACTIVITY_DEFINITION.PROCESS_DEF_ID AND OSSYS_BPM_PROCESS_DEFINITION.IS_ACTIVE = 1 AND OSSYS_BPM_PROCESS_DEFINITION.IS_LOCKED = 0
  INNER JOIN OSSYS_ESPACE ON OSSYS_ESPACE.ID = OSSYS_BPM_PROCESS_DEFINITION.ESPACE_ID AND OSSYS_ESPACE.IS_ACTIVE = 1 AND OSSYS_ESPACE.IS_LOCKED = 0
  INNER JOIN OSSYS_TENANT ON OSSYS_TENANT.ID = OSSYS_BPM_PROCESS.TENANT_ID AND OSSYS_TENANT.IS_ACTIVE = 1
WHERE
  (IS_RUNNING_SINCE IS NULL OR IS_RUNNING_SINCE = '1900-01-01 00:00:00')
  AND (NEXT_RUN IS NOT NULL AND NEXT_RUN <> '1900-01-01 00:00:00' AND NEXT_RUN <= GETDATE())
  AND OSSYS_BPM_ACTIVITY.STATUS_ID NOT IN (5, 11, 12, 13)
  AND OSSYS_BPM_PROCESS.STATUS_ID NOT IN (2, 4, 5)
  -- replace with the missing time in your timezone. Example for GMT.
  AND NEXT_RUN BETWEEN '2016-03-27 01:00:00' AND '2016-03-27 02:00:00'
ORDER BY NEXT_RUN ASC
```


## What do I do to fix the issue, if I am affected?

If you are affected by this problem, all you need to do is schedule the activity to be executed outside the missing hour from Daylight Savings. You can do this with the following query:

`update ossys_bpm_activity set next_run = getdate() where next_run between '<start_date>' and '<end_date>'`



If, for some reason, you do not want these activities to be processed anymore, you can use the information from the query in "How do I detect if the issue is affecting me" section to identify the processes that have the problematic activities and terminate them in Service Center. You can also use the BPT API if you have a large number of processes in this state and terminating them in Service Center is not a viable option.

## Next steps from OutSystems

* This will be fixed for all Cloud Customers suffering from the issue.

* OutSystems is working on a fix for this issue for all currently supported versions of the OutSystems Platform (8.0, 9.0, 9.1).
Refer to defect ID #1188860 in the change log to know when the fix is available.

We recommend all customers to update to this revision as soon as it is made available.

OutSystems will not be issuing a fix for customers running on Platform 7 (7.0.1.25). For these customers, the workaround indicated above will allow restoring normal operations; to prevent future occurrences of the issue, we advise such customers to plan an upgrade to a supported version.

## Final notes

If you have further questions regarding this problem, feel free to contact OutSystems Support through the [usual means](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/01_Contact_OutSystems_technical_support).

