---
summary: Learn about security updates on OutSystems 11 (O11) Cloud, including maintenance schedules, PCI DSS compliance, and expected downtime.
tags: cloud infrastructure, system maintenance, security patching, operating systems updates, PCI DSS compliance
locale: en-us
guid: b41ab799-b4e4-4f0f-8141-b36fef030b0d
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
audience:
  - platform administrators
  - infrastructure managers
  - tech leads
outsystems-tools:
  - none
coverage-type:
  - understand
---

# System updates on OutSystems Cloud

OutSystems performs regular security updates on all OutSystems Cloud infrastructure to protect against vulnerabilities and maintain system performance. These updates are required for Microsoft compliance, namely PCI DSS compliance, and help ensure your environment meets industry security standards.

## PCI DSS compliance

These system updates fulfill PCI DSS Requirement 6.2, which mandates that all system components be protected from known vulnerabilities through the timely application of security patches. The regular patching schedule helps maintain your PCI-compliant environment by:

* Installing critical security patches within required timeframes
* Maintaining current security baselines across all infrastructure
* Documenting all security updates for compliance audits

## Maintenance schedule

The following table shows the maintenance frequency and advance notice periods for each platform.

| Platform                | Frequency | Maintenance window        | Advance notice |
| ----------------------- | --------- | ------------------------- | -------------- |
| OutSystems Cloud        | Quarterly | Defined by your settings  | 2 months       |
| OutSystems Cloud Sentry | Monthly   | Defined by your settings  | 3 weeks        |

Emergency security patches may be applied outside scheduled windows, with a minimum of 4 hours' notice.

To configure your maintenance window, see [Define a maintenance window for OutSystems Cloud environments](cloud-maintenance-window.md).

### Rescheduling maintenance

You can reschedule maintenance up to two hours before the scheduled window. To reschedule, contact Support or [create a support case](https://www.outsystems.com/support/portal/).

## What to expect

This section describes the maintenance process and its impact on your services.

### Preparation phase

Background system preparation begins 24 hours before the scheduled maintenance window. There's no impact on your services during this phase.

### Maintenance execution window

During the maintenance window, OutSystems applies security patches and operating system updates. Brief service interruptions are possible depending on your infrastructure configuration.

## High availability

OutSystems uses the following methods to minimize service disruption during maintenance:

* **Rolling updates**: Maintenance is performed using a rolling update methodology
* **Load balancing**: Load balancing ensures continuous service availability
* **Automatic failover**: Failover mechanisms remain active throughout maintenance

## Expected downtime

The following table shows the maximum expected downtime based on your infrastructure configuration.

| Infrastructure configuration | Maximum downtime |
| ---------------------------- | ---------------- |
| Single front-end             | 60 minutes       |
| Multiple front-ends          | No downtime      |
| Load balancer                | No downtime      |

If you experience longer downtime than expected, contact support immediately. OutSystems monitors all maintenance operations and investigates any issues.

## Email notifications

You receive two emails per environment during the maintenance process:

1. **Initial notice**: Sent according to the advance notice period in the maintenance schedule
1. **Confirmation**: Sent after maintenance completes

If maintenance is delayed or cancelled, you receive updated notifications at least 4 hours before any schedule changes.

<div class="info" markdown="1">

To receive notifications, you must be registered as an Infrastructure Admin in your [Customer Portal](https://www.outsystems.com/csportal/).

</div>

## Required actions

No action is required from you throughout this maintenance process.

## Need help?

If you need assistance, contact support through the [Support Portal](https://www.outsystems.com/support/portal/) or one of the [alternative phone contacts](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/01_Contact_OutSystems_technical_support#Phone_Support).
