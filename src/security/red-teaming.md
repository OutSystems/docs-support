# Red Teaming in OutSystems Cloud
In order to simulate real-world attacks, customers may conduct Red Team assessments.
Red Team activities are subject to the same restrictions and guidelines outlined in the Penetration Testing Policy (with the exception that no prior notice to OutSystems is required), including:

* **Limited Scope** – For O11, Red Teaming activities may only target customer-owned applications and their assigned infrastructure (VPC/tenant).
For ODC, Red Teaming activities may only target customer-owned applications and must not include any attempts to exploit or disrupt the shared infrastructure managed by OutSystems.
* **Platform Security** – The customer is responsible for any application–level vulnerabilities found after the Red Team engagement, while platform-related issues must be reported to OutSystems as described in the OutSystems [vulnerability policy](https://success.outsystems.com/support/security/vulnerabilities/).
* **Operational Impact** – Any degradation to performance, service disruptions, system outages, or other adverse effects are the customer’s responsibility and will not count against [OutSystems SLAs](https://www.outsystems.com/legal/success/support-terms-and-service-level-agreements-sla-of-the-outsystems-software/#service-availability).
* **Prohibited Activities** – Denial of Service (DoS), Distributed Denial of Service (DDoS), network flooding, and any attacks targeting OutSystems-managed infrastructure or third-party services are strictly forbidden.
* **Acknowledgement of Responsibility** – For the avoidance of doubt, if customer’s Red Teaming activities result in an adverse impact on any shared infrastructure or shared services, liability for such adverse impact will be the responsibility of customer.

Additionally, OutSystems' security controls—such as blocking of suspicious requests and request rate limiting,—will remain active during testing.
