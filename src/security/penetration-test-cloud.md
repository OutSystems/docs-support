---
summary: Check what you'll need to request authorization for penetration tests, load tests and vulnerability scans on OutSystems cloud.
tags: support-Cloud_Platform
locale: en-us
guid: 00c90ba4-311d-43b2-a676-0613ad5f60b2
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11, odc
figma:
---

# Load and penetration tests on OutSystems Cloud

## Overview

As a subscription customer, you may wish to perform penetration tests, vulnerability scans, or load tests. This is possible as long as they're limited to your own applications under the **Customer** responsibility as described under the [OutSystems shared responsibility model](../enterprise/maintenance/cloud-shared-responsibility.md). 

As a cloud customer, and particularly if you are a customer of shared infrastructure solutions such as ODC, extra care must be taken to prevent any impact and harm to other customers.

* You must request authorization as described in the next section.
* Services under the responsibility of OutSystems or third-party vendors cannot be part of any security assessments. These include SaaS services built by OutSystems as well as any service provided to OutSystems by OutSystems vendors such as AWS.
* Denial of service (DoS), Distributed Denial of Server (DDoS) or any kind of network flooding attacks are prohibited.
* Protection mechanisms OutSystems and OutSystems vendors have in place protecting the applications and services, such as blocking of suspicious requests and request rate limiting, will not be turned off during any testing. 


## Performing scans in your OutSystems 11 Cloud or ODC

To perform penetration and load tests, and vulnerability scans, you must request authorization from OutSystems at least **5 business days** before the start date, for each test.

You'll need to [open a support case](https://www.outsystems.com/SupportPortal/CaseOpen/) and provide the following information:

1. **Contact Information** - Single point-of-contact managing the scans. Please provide:
    * Contact name
    * Phone number
    * Email address
2. **Scanning IP addresses (Source)** - The IP addresses that will scan the infrastructure.
3. **Environment(s)** - The environments' addresses or serial numbers
4. **Dates and time zone for the tests**:
    * Start date and time (YYYY-MM-DD HH:MM **UTC**)
    * End date and time (YYYY-MM-DD HH:MM **UTC**)

Please note that we require all the above-mentioned information (points 1. to 4.) to approve your request.

In case you need to alter your initial request, it takes an additional 2 business days to provide confirmation.

