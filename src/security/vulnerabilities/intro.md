---
summary: OutSystems 11 (O11) implements a comprehensive vulnerability management policy to guide customers on how to report and handle security issues effectively.
locale: en-us
guid: bc76e550-bfca-40a6-ad24-7fe3db432331
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/vTtFn5nl44ZLjUBYo2anCO/Security?type=design&node-id=0%3A1&mode=design&t=kgeN4DPQGpzW3OrE-1
---

# Vulnerabilities

## OutSystems public vulnerability policy

This policy was created to provide our customers guidance and information in the event of a vulnerability reported in an OutSystems product. It's essential to ensure that our customers have a consistent and unambiguous resource to understand how OutSystems responds to events of this nature.

The OutSystems vulnerability policy covers:

* OutSystems components

    * Platform Server
    * LifeTime
    * Service Studio and Integration Studio
    * Mobile Apps Builder Service (MABS)
    * AI Mentor Studio
    * Integration Builder
    * Workflow Builder
    * OutSystems Developer Cloud (ODC)
    * OutSystems Developer Cloud (ODC) Studio

* Forge components supported by OutSystems
* Any property under outsystems.com domain

OutSystems Product Security Incident Response Team (PSIRT) investigates all reports regardless of the OutSystems software code version or product lifecycle status until the product reaches the [end of mainstream support](https://www.outsystems.com/legal/success/support-terms-and-service-level-agreements-sla-of-the-outsystems-software/#end-of-support-for-older-software-versions).

Issues will be prioritized based on the risk score and severity. The resolution of a reported vulnerability may require installing new software versions of products that are [under active support from OutSystems](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/Support_terms_and_service_level_agreements_(SLA)_of_the_OutSystems_software/OutSystems_Product_Lifecycle_and_Support_calendar#What_is_the_support_calendar_for_OutSystems_releases.3F). As a best practice, OutSystems strongly recommends that customers periodically verify if their products are under mainstream support to ensure access to the latest software updates.

During any investigation, the OutSystems PSIRT manages all sensitive information on a highly confidential basis. Internal distribution is limited to those individuals who have a legitimate need-to-know and can actively assist in the resolution.

Similarly, the OutSystems PSIRT asks reporters to maintain strict confidentiality until complete resolutions are available for customers and have been published by the OutSystems PSIRT on the OutSystems website through the appropriate coordinated disclosure.

## Reporting or obtaining support for a vulnerability

### For OutSystems customers and partners

If you are an OutSystems customer or partner and have access to our [Support Portal](https://www.outsystems.com/supportportal/), please report your vulnerability reports through OutSystems Support using the [available channels](https://www.outsystems.com/legal/success/contact-outsystems-technical-support/#Contact_Channels).

#### Before submitting a vulnerability report  { #submit-report }

Often, vulnerability scans, static code analysis, or dynamic code analysis are performed by third-party tools that output a report. Those reports shouldn’t be sent untreated to OutSystems. Instead, they should first be analyzed.

This means that customers and partners must first analyze the findings in such reports and determine if:

1. It’s related to application logic and was introduced during the development (related to application logic). In this case, it’s the customer's responsibility to address it.
1. The finding is a false positive or not. It’s the customer's responsibility to consult the available documentation.
1. Understand if the vulnerability falls under the customer's or OutSystems' responsibility.

Read the following articles before performing any type of testing on your OutSystems applications:

* [Static application security testing](https://success.outsystems.com/Support/Security/Static_Application_Security_Testing)
* [Penetration testing](https://success.outsystems.com/Support/Security/Penetration_testing)

##### Assistance in analyzing reports

For customers who require help in analyzing reports from third-party tools, OutSystems has made available a service.
To obtain more information about this service, customers should reach out to their Customer Success Managers (CSM), Account Representative, or Solution Design Manager (SDM).

After analysis, if the findings are related to the OutSystems platform, please submit a vulnerability report. The instructions to submit such a report to OutSystems support can be found next.

#### How to submit a vulnerability report

To submit a vulnerability report, use [Support Portal](https://www.outsystems.com/supportportal) by raising an incident.

Vulnerability reports must contain the following information:

1. Provide a detailed vulnerability summary. This section must contain a summary of the vulnerability and its impact.

    **Example (not real):**

    LifeTime contains an insecure object reference vulnerability where any user can view the details of any other user. This may lead to data leak since details of the users can be accessed by any user.

1. Proof of concept or detailed steps to reproduce or exploit the vulnerability

    **Example (not real):**

    1. Login into LifeTime
    1. Go to https://[URL]/users?uid=2
    1. Confirm you’re seeing the details of another user.

If this information isn't consistently provided, the support case may ultimately be closed. There should be only one vulnerability being addressed per incident in order to facilitate the communication and the proper investigation.

Reports will be handled within the [scope and SLA's](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/Support_terms_and_service_level_agreements_(SLA)_of_the_OutSystems_software) of customers' and partners' contracts.

### For community members

Any person that’s not an OutSystems customer or partner is welcome to report a vulnerability to OutSystems PSIRT by [using this form](https://www.outsystems.com/security/report-a-vulnerability) and filling in all the mandatory information.

OutSystems PSIRT may return to the reporter with additional questions or clarifications and provides the reporter with regular updates when relevant information comes to light.

## OutSystems management of a reported vulnerability { #management }

The phases of tackling a vulnerability found for OutSystems products are based on the CVSS severity score for the vulnerability.  All vulnerabilities follow the following methodology:

* Identify
* Verify (classification)
* Remediate (plan and fix)
* Release

For **Low** and **Medium** severity vulnerabilities, once the fix is released, information about the vulnerability is published in the Release Notes  [Release Notes](https://success.outsystems.com/support/release_notes/) for the impacted products.

For **High** and **Critical** severity vulnerabilities the following steps are as follows:

![Flowchart illustrating the OutSystems vulnerability management process, including the embargo phase with steps for identification, classification, risk assessment, plan and fix, security bulletin publication, and fix release, followed by the public disclosure phase.](images/vulnerabilities-diag.png "OutSystems Vulnerability Management Process")

It consists of 2 phases, the **embargo phase** and **public disclosure**.

### Embargo phase { #embargo }

During this phase, and to protect customers, OutSystems doesn't disclose further details about the vulnerability. It’s important to note that the more details are divulged, the more probable it is that such information may be used to exploit the vulnerability. Therefore, OutSystems allows reasonable time for customers to protect their infrastructures before disclosing further.

During the embargo phase, the following steps occur:

1. **Identification:**
OutSystems learns about the vulnerability.

1. **Classification:**
OutSystems classifies reported vulnerabilities and attributes a risk score and severity. This is done using the version 3.1 of the [Common Vulnerability Scoring System](https://www.first.org/cvss/) (CVSS). This framework assigns a vulnerability score to a vulnerability which is then translated into five possible severities, ranging from **Info** up to **Critical**, according to the risk score.

1. **Risk Assessment:**
For all vulnerabilities, study the vulnerability and come up with a recommended mitigation strategy. The mitigation can range from shutting a service down to releasing a patch.
  
1. **Plan and fix:**
For all vulnerabilities planned to be fixed, OutSystems defines a schedule and a deadline for the fix, according to internal criteria defined to mitigate vulnerabilities. The fix and / or workaround for the vulnerability is prepared.

1. **Publish security bulletin and fix release:**
A fix is publicly released along with installation details. A security bulletin for each vulnerability is published and listed under this section (expand the tree on the left to see the list). At this point, the bulletins don't disclose any technical details.

1. **Patch OutSystems Cloud and ODC:**
For OutSystems Cloud customers, a patch schedule may also be communicated for all affected environments. If the patch has no impact on normal operations and availability, it won’t require scheduling. OutSystems reserves the right to start scheduling patches to OutSystems Cloud environments as soon as a fix or workaround is found.
Self-managed infrastructures can be patched at the customer’s discretion.
For OutSystems Developer Cloud (ODC) customers, all fixes are automatically propagated to all customer accounts.

### Public disclosure { #disclosure }

Approximately 90 days after the fix release, OutSystems discloses further details about the vulnerability by updating the respective security bulletin.
