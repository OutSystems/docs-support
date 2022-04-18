---
summary: OutSystems allows the development of enterprise web and mobile applications that run in different infrastructure models
tags:
locale: en-us
guid: b04339ce-7b9f-4c93-94b7-e4cf397eab47
app_type: traditional web apps, mobile apps, reactive web apps
---

# OutSystems Cloud Shared Responsibility Model

OutSystems allows the development of enterprise web and mobile applications that run in different infrastructure models:

* **OutSystems cloud**: deployed on Amazon Web Services (AWS) and managed by OutSystems

* **Customer-managed**: including on-premises, public, and private cloud

When activating a subscription, and depending on infrastructure choice, all environments are deployed to either the OutSystems cloud or the customer-managed infrastructure.

Learn more in [Possible setups for an OutSystems infrastructure](https://success.outsystems.com/Documentation/11/Setting_Up_OutSystems/Possible_setups_for_an_OutSystems_infrastructure).

## Shared Responsibility Model

In the OutSystems cloud model, OutSystems shares control of the cloud environments with you. This approach relieves you of the operational burden as OutSystems operates, manages, and controls the components from the platform down to the infrastructure (illustrated in the left red banner of the picture below).

![](images/cloud-shared-responsibility_0.png?width=800)

OutSystems part in this shared responsibility model is to provide a highly secure cloud environment to protect the applications you build and the data they use. OutSystems is responsible for applying security fixes to the platform and underlying infrastructure, and conducting security scans to detect potential vulnerabilities.

Your responsibilities include securing the applications and integrations you develop with OutSystems using approaches such as:

1. Applying secure development techniques and conducting code security reviews

1. Using OutSystems identity and access management capabilities

1. Encrypting sensitive data

1. Identifying application vulnerabilities through vulnerability assessments and penetration testing

1. Cooperating to mitigate product vulnerabilities and associated risks

You are responsible for the management of applications during their life cycle, from development to production. Customers should carefully consider the security and compliance requirements of their applications, applying one or more control layers, as required.

OutSystems communicates its cloud security and controls in a number of different ways:

* Obtaining industry certifications and independent third-party attestations;

* Publishing information about OutSystems security and control practices;

* Providing [trust certificates and reports](https://outsystems.com/trust), and other documentation to OutSystems customers, some of them under NDA (as required).

Refer to OutSystems [ISO 27017 certification](https://www.outsystems.com/-/media/files/generic/trust/iso-27017-ecertificate-2015-cloud-709506.pdf?la=en&hash=9C0F767D040D984E93528D846C43BA7B57A60F01) for details on cloud-specific information security controls, and the shared responsibility model.
