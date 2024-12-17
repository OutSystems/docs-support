---
summary: Explore the shared responsibility model and security roles in ODC and OutSystems 11 Cloud.
tags: cloud security, cloud deployment, shared responsibility model, enterprise applications, aws
locale: en-us
guid: b04339ce-7b9f-4c93-94b7-e4cf397eab47
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11, odc
figma: https://www.figma.com/file/cPLNnZfDOZ1NX3avcjmq3g/Enterprise%20Customers?node-id=618:22
audience:
  - platform administrators
  - tech leads
  - full stack developers
outsystems-tools:
  - none
coverage-type:
  - understand
---

# OutSystems Cloud shared responsibility model

OutSystems allows the development of enterprise web and mobile applications that run in different infrastructure models:

* **OutSystems Developer Cloud (ODC)**: a [cloud-native app development platform](https://www.outsystems.com/tk/redirect?g=9a0cb62a-f11b-4d1a-9e79-0ca7d398e57b) with a modern architecture.
  
* **OutSystems 11 Cloud**: deployed on Amazon Web Services (AWS) and managed by OutSystems

* **OutSystems 11 self-managed**: including on-premises, public, and private cloud

Depending on infrastructure choice, all environments are deployed to either ODC Cloud, the OutSystems 11 Cloud, or the self-managed infrastructure. This shared responsibility model applies to ODC Cloud and OutSystems 11 Cloud deployments, collectively referred to as **OutSystems Cloud**.

## Shared responsibility model

In the OutSystems Cloud, OutSystems shares control of the cloud environments with you. Although OutSystems provides secure and compliant services to protect customer data and applications, you are solely responsible for properly configuring and operating those services as required by your organization.  

This approach relieves you of the operational burden as OutSystems operates, manages, and controls the components from the platform down to the infrastructure as explained in the following diagram.

![Diagram illustrating the shared responsibility model in OutSystems Cloud, showing customer responsibilities for applications and data, OutSystems responsibilities for platform and infrastructure, and AWS infrastructure layers.](images/outsystems-cloud-shared-responsibility-model-diag.png "OutSystems Cloud Shared Responsibility Model Diagram")

OutSystems uses several layers of defense to prevent various types of threats and achieve compliance with security frameworks such as  SOC 2, SOC 3, PCI-DSS, and ISO 27001 without compromising application performance. 

The following sections explain the shared responsibilities between OutSystems and its customers.

## Customer responsibilities

OutSystems customers are responsible for securing data and user access and permissions to their applications. Customers are responsible for the management of their applications throughout the entire lifecycle: from when it's developed to when it's deployed to production. Ultimately, OutSystems Cloud customers are responsible for:

* Managing their data (including encryption options), classifying their assets, and using Identity and Access ManagementAM tools to apply for the appropriate permissions.

* Applying secure development techniques and conducting code security reviews on developed applications.

* Identifying application vulnerabilities through vulnerability assessments and penetration testing.

* Mitigating application vulnerabilities and associated risks.

* Adopting application development, testing, and monitoring practices recommended for their performance and scalability goals.

OutSystems provides extensive [training options](https://www.outsystems.com/evaluation-guide/getting-started-with-outsystems/training/) and a [range of success offers](https://www.outsystems.com/evaluation-guide/getting-started-with-outsystems/app-support/) to ensure customers can follow and adopt best practices.

## OutSystems responsibilities

OutSystems is responsible for protecting the infrastructure that runs all of the services offered in OutSystems Cloud. This infrastructure is composed of the hardware, software, networking, and facilities that run OutSystems Cloud services. OutSystems is responsible for the following:

* **Platform security**. OutSystems provides its customers computing platform for designing, building, deploying, and managing business applications. OutSystems implements many layers of security defense architecture to resist various types of threats and ensure the entire computing platform. OutSystems responsibility is to protect the business values of its customers' applications while helping them to achieve compliance with industry security frameworks and standards.
Identity and access management: OutSystems integrates with Active Directory and Single-Sign-on to allow customers to manage the access controls as they would for any enterprise software. OutSystems offers its customers the capabilities to define, enforce and manage individual user accounts with permissions across its services.

* **Operating systems, network & firewall configuration**. OutSystems is responsible for configuring and deploying the underlying operating systems, network components, and firewalls that supports customers' developed and managed applications. OutSystems implements industry-accepted best practices to harden its network security as a practice of reducing system vulnerability by reducing its attack surface. OutSystems deploy security infrastructure for comprehensive monitoring of its environments using the following tools:

    * Intrusion Detection Systems
    * Logging and Alerting Systems
    * Vulnerability Scanning
    * Perimeter Monitoring
    * Patch Management, and
    * Security Incident Monitoring
    
* **Encryptions**. OutSystems platform offers the ability to add a layer of security to customers' data at rest in the cloud. OutSystems is responsible for providing customers the capabilities for encrypting data at rest and in transit, allowing customers to satisfy their security compliance requirements.

* **Compute/Storage/Database/Networking**. OutSystems delivers hardware and software tools to its customers over the internet. Therefore, OutSystems is responsible for managing the underlying infrastructure such as servers, storage, database management systems, and networking resources that supports its customers complete application lifecycle: developing, testing, deploying, managing, and updating.  

* **Availability Zones & Regions**. OutSystems is responsible for managing remote data center infrastructures such as computing environments, data storage, and network resources. OutSystems performs replication at each datacenter (availability zones/region), annual disaster recovery tests for the service to verify the project recovery times. OutSystems ensures customer data between datacenters are performed through encrypted channels. OutSystems ensures its customers' applications inherit cloud characteristics such as scalability, high-availability, multi-tenancy.

OutSystems communicates its cloud security and controls in a number of different ways:

* Obtaining industry certifications and independent third-party attestations;

* Publishing information about OutSystems security and control practices;

* Providing [trust certificates and reports](https://security.outsystems.com/), and other documentation to OutSystems customers, some of them under NDA (as required).

Refer to OutSystems [SOC 2](https://security.outsystems.com/?_gl=1*3it0c4*_gcl_au*MTc0NzUyNDM2OC4xNzI3MTA5NDI3*_ga*MTE0NzEzNzg3My4xNzAzMDk0NzA3*_ga_ZD4DTMHWR2*MTcyOTI2NTI3Ny42Ni4xLjE3MjkyNzQ4NzguNjAuMC4w*_ga_HGKNZZMWJS*MTcyOTI3NDM1OC4yMDAuMS4xNzI5Mjc0ODc4LjYwLjEuMTIxNzc5MDg1MA..*_ga_G11QMS1MBT*MTcyOTI3NDM1OC4xMDAuMS4xNzI5Mjc0ODc4LjAuMC4w&itemUid=7bfa66da-33ab-49de-8391-e329738a1ae9&source=click) and  [ISO 27017 documentation](https://security.outsystems.com/?itemUid=0c1fdf36-c946-4670-9354-8fa3e4260ab1&source=documents_card) for details on cloud-specific information security controls, and the shared responsibility model.
