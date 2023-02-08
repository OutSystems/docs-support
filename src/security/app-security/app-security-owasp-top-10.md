---
summary: See how OutSystems helps you address the vulnerabilities identified by OWASP. 
tags: support-Security-overview
locale: en-us
guid: 74924eac-d729-4c99-bcb4-09b40a483cfa
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
---

# How OutSystems helps you address OWASP Top 10

The [OWASP Top 10](https://owasp.org/www-project-top-ten/), [OWASP Low Code Top 10](https://owasp.org/www-project-top-10-low-code-no-code-security-risks/) and [OWASP Mobile Top 10](https://owasp.org/www-project-mobile-top-10/) represent a broad consensus about the most critical security risks to web and mobile applications.

This article describes how OutSystems helps you address the vulnerabilities identified by OWASP.

For more information on how to achieve the highest level of security for your OutSystems applications, see [Application security overview](intro.md).

## OWASP Top 10 - Final List 2021

### Broken Access Control (A1)

OutSystems role-based access control restricts access to the application’s pages depending on specific application-level roles. Developers define application-level permissions for roles using visual building blocks.

Once users are registered to use an application, role-based access control ensures that only authorized users are allowed to perform specific business functions.

See also [Protecting OutSystems apps from access control / permissions vulnerabilities](../develop-secure-apps/access-control-vulnerabilities.md).

### Cryptographic Failures (A2)

To protect your data in transit, OutSystems allows you to enable SSL in your infrastructure, thus you can use HTTPS to ensure that any content will load over a secure connection. You can enforce the HTTPS security for the applications running in an environment, and enable HTTP Strict Transport Security (HSTS) for the whole environment.

If you need extra layers of compliance, and opt for a [high-compliance OutSystems Cloud](https://www.outsystems.com/sentry/), you have enforced HTTPS communications for all web applications.

To protect your application-sensitive data, OutSystems enables integration with existing cryptographic pre-built components.

In OutSystems Cloud environments, you can activate the database encryption service, which includes the underlying storage for database server instances, its automated backups, and snapshots.

See also [Protecting OutSystems apps using encryption and SSL/TLS](../develop-secure-apps/encryption-ssl-tls.md).

### Injection (A3)

By default, OutSystems escapes content before showing it on the UI. Escaping untrusted HTTP request data based on the context in the HTML output (body, attribute, JavaScript, CSS, or URL) resolves reflected and stored XSS vulnerabilities. When developers need to override the default secure code patterns for advanced customization scenarios, they receive design-time warnings for potential injection flaw patterns, along with guidelines to fix them.

Additionally, OutSystems provides a set of sanitization functions that developers can use in advanced scenarios to avoid code injection in HTML, JavaScript, and SQL snippets. Using these functions, developers can remove potential malicious content, coming from user input before it’s stored in the database or rendered on the UI.

Architects, operators, or administrators can use OutSystems mechanisms to define content security policies-the domains from which application pages can retrieve resources (images, CSS, scripts, media). You can configure this setting for each environment, generically applying to all applications, or defining it for specific applications. Limiting the sources from which the applications can load resources effectively mitigates XSS attacks, which require loading a script from a malicious site.

You can also use content security policies to prevent application pages from being embedded in frames and thus prevent clickJacking attacks.

See also [Protecting OutSystems apps from code injection / Cross Site Scripting attacks](../develop-secure-apps/code-injection-css-attacks.md).

### Insecure Design (A4)

OutSystems allows developers to override the default secure code patterns for advanced customization scenarios. In this case, OutSystems security checks proactively warn developers of potential security issues as they publish their applications.

OutSystems generates standard applications from its runtime, enabling standard security assessment tools, such as static code analysis.

### Security Misconfiguration (A5)

OutSystems Cloud infrastructures are automatically provisioned, configured, and tuned for high performance, security, and reliability. The physical infrastructure of the OutSystems Cloud is hosted in the secure data centers of Amazon Web Services.

If you need extra layers of security and compliance, you can opt for the [OutSystems Sentry](https://www.outsystems.com/sentry/) offer.

For self-managed deployments, OutSystems provides system administrators with clear and concise instructions on how to make the platform installation secure.

Additionally, OutSystems includes a set of capabilities that enable you to define and implement the security controls required by your applications. See [Application security overview](intro.md) for further details.

For both exposure and consumption of SOAP Web Services, OutSystems escapes XML parsing. Additionally, to help you protect your applications from XML External Entity attacks, OutSystems supports the use of the latest deserialization and XML processor library versions, and SOAP 1.2.

### Vulnerable and Outdated Components (A6)

OutSystems constantly monitors for vulnerabilities in the product and the generated code, using a continuous delivery approach to constantly release incremental value with minimal disruptions to the customers’ operations and business.

[This policy](../vulnerabilities/intro.md) describes the OutSystems response to vulnerabilities that might affect customer applications. Security fixes are proactively applied in OutSystems Cloud.

### Identification and Authentication Failures (A7)

By default, OutSystems ensures that:

* Session identifiers aren't sent in URLs

* Sessions time out at their expiration time

* All password handling uses strong cryptographic algorithms

Also, OutSystems ensures that the session identifier is transparently changed on each login, and validates this on every request, thus preventing session fixation attacks.

Cookies may contain sensitive information that shouldn't be accessible to an attacker eavesdropping on a channel. To prevent browsers from sending cookies over an unencrypted channel, administrators can enable the secure flag in cookies, which makes Web browsers that support this flag to send secure cookies only when the request uses HTTPS.

Additionally, OutSystems provides built-in protection mechanisms against brute force attacks for the application end users and IT users.

### Software and Data Integrity Failures (A8)

OutSystems serializes and deserializes session data using a built-in anti-tampering JSON deserialization mechanism. This mechanism compares incoming JSON data with predefined application models and performs strict type verification during deserialization. Additionally, it runs a salted hash-based algorithm over the serialized session data to validate potential tampering before deserialization.

### Security Logging and Monitoring Failures (A9)

OutSystems tracks the details of every access to application screens. These logs include the component and screen accessed, which end users accessed it, when the access occurred, and exactly which node served the screen.

OutSystems also logs all access to external systems through web services, custom integration logic, or web service requests to applications running inside the platform. The logs keep a record of who made the request, the request’s target, the method called, how long the request took, and the exact time of the request. This enables you to track down any security issues efficiently.

Customers who choose to manage their own OutSystems installation benefit from the OutSystems standard runtime architecture to leverage their know-how and tools for logging and monitoring all system components.

OutSystems Cloud customers benefit from the logging and monitoring capabilities bundled in the service with a choice between the secure baseline of the standard configuration and the more advanced [OutSystems Sentry](https://www.outsystems.com/sentry/) offer.

### Server-Side Request Forgery (SSRF) (A10)

OutSystems enables integration with external systems that you can statically configure. For example, when using the development environment to consume a third-party REST API, you must explicitly set the service's external fully qualified domain name (FQDN) as the base URL. This address can then be overwritten with a static configuration for each environment.

In case you need a more dynamic way of setting third-party addresses, OutSystems recommends using server-side data from the database or site properties to build the FQDN instead of relying on external data. If you really need external data, such as a URL shared on demand by a third-party service,  make sure your applications validate that URL. For example, check the FQDN against a predefined list of valid, allowed third-party addresses. Then, use the OnBeforeRequest event action to set the customized base URL. Any time you want to make sure you only use static addresses throughout all your services, check all your OnBeforeRequest and make sure the base URL is not being customized there.

## OWASP Low Code/No Code Top 10 - July 2022

This section describes how OutSystems helps you address the Top 10  Low Code/No Code Security Risks as  identified by OWASP.

For more information on how to achieve the highest level of security for your OutSystems applications, see [Application security overview](https://success.outsystems.com/Support/Security/Develop_secure_OutSystems_apps).

### Account Impersonation (LCNC-SEC-01)

OutSystems creates and manages application credentials without requiring developer access. Developers cannot access or change the credentials applications use to run and access resources. 

Apps are staged across multiple environments, from Development to Production and custom integrations with third-party services can leverage environment-wide configurations, that will not propagate to other environments. 

To further increase security, you can use roles to allow developers to publish applications only to non-production environments and reserve the privilege to change environment configurations for a small set of DevOps staff.

**See also** 

[Protecting OutSystems apps from access control / permissions vulnerabilities](https://success.outsystems.com/Support/Security/How_the_OutSystems_Platform_Helps_You_Develop_Secure_Applications/Protecting_OutSystems_apps_from_access_control_/_permissions_vulnerabilities)
[Configure Web Service Authentication](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Consuming_SOAP_Web_Services/Configure_Web_Service_Authentication)
[Consume REST APIs](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/REST/Consume_REST_APIs)
  
### Authorization Misuse (LCNC-SEC-02)

OutSystems was built with productivity and speed of development in mind, but no shortcuts to authentication and authorization exist that may put your applications in danger. 

Each application can create its own authentication and authorization flows for itself or for integration with third-party services with no shared connections. 

Furthermore, OutSystems role-based access control restricts access to the application’s pages depending on specific application-level roles. Developers define application-level permissions for roles using visual building blocks.

Once users are registered to use an application, role-based access control ensures that only authorized users are allowed to perform specific business functions.

See also [Protecting OutSystems apps from access control / permissions vulnerabilities](https://success.outsystems.com/Support/Security/How_the_OutSystems_Platform_Helps_You_Develop_Secure_Applications/Protecting_OutSystems_apps_from_access_control_/_permissions_vulnerabilities).

### Data Leakage (LCNC-SEC-03)

OutSystems and the applications you develop do not perform any data movement or any data processing for that matter without explicit coding from the application developer. 

As with other development tools, development privileges should be restricted to dedicated personnel. OutSystems provides roles that can be leveraged to provide developers different levels of access to different applications, environments, and data.  

### Authentication and Secure Communication Failures (LCNC-SEC-04)

OutSystems environments can easily be configured to accept only secure encrypted connections. Configurations can be done per application or enforced across all applications via environment settings. 

Applications are staged across multiple environments, and role-based authorization can be used to restrict access to environment settings.

### Security Misconfiguration (LCNC-SEC-05)

OutSystems follows best practices in governance and security to ensure that proper defaults are in place, providing an optimal balance between security by design and out-of-the-box functionality.

OutSystems provides configuration settings both at the application level and at the environment level. 

Environment-level configurations can be used combined with role-based authorization to ensure, for example, that developers only have access to their applications or to non-production environments and that any production environment configuration can only be made by high-privileged DevOps staff.

OutSystems includes a set of capabilities that enable you to define and implement the security controls required by your applications. See [Application security overview](https://success.outsystems.com/Support/Security/Develop_secure_OutSystems_apps). 

Moreover, [AI Mentor Studio can scan your applications and identify risky patterns](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_technical_debt/Code_Analysis_Patterns#Security)

### Injection Handling Failures (LCNC-SEC-06)

Injection handling failures or injection / input validation failures are common to all applications in all technologies. OutSystems defenses are described in [How OutSystems helps you address (generic) OWASP Top 10](#injection-a3).

### Vulnerable and Untrusted Components (LCNC-SEC-07)

OutSystems constantly monitors for vulnerabilities in the platform and the generated code, using a continuous delivery approach to constantly release incremental value with minimal disruptions to the customers’ operations and business.

OutSystems enables the use of shared components. For this, OutSystems recommends using the OutSystems Forge where components, modules and applications are published, shared and scrutinized by the community. 

As with open-source projects, OutSystems components shared in Forge can be downloaded, opened, analyzed, tested, and changed before use or being published to production. The platform provides full visibility over all application components and dependencies making it easier to spot and address unauthorized components.

You can also choose to only download and use OutSystems [Supported or Trusted Forge components](https://success.outsystems.com/Support/Forge_Components/Forge_FAQs/Curating_Projects) to make sure you only use components that have been curated and validated by OutSystems. 

### Data and Secret Handling Failures (LCNC-SEC-08)

OutSystems recommends not hardcoding secrets in the code but using other provided methods. 

For example, you can use site properties to store configuration data to be available to applications in an environment and have different configuration data or credentials across environments. 

Role-based authorization can again be used to make sure the developers only have access to code and reserve the permission to change environment configuration and particularly production configuration for high-privileged IT users. 

If the preference is to store that data away from the managed database, applications built with OutSystems can be extended through extensions and can be integrated with third-party services and external databases. 

Integration with third-party services, for example, can be used to store sensitive data in a secret management service. It’s up to the customer, however, to choose where and how to store the data. Moreover, OutSystems will never move any data out of its original geo-location in compliance with data residency regulations.

### Asset Management Failures (LCNC-SEC-09)

OutSystems provides tools that enable full visibility and management of the platform, applications, application dependencies and integration with third-party services.

[**LifeTime**](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_Your_OutSystems_Infrastructure) is the centralized console for managing your OutSystems environments, applications, IT users, and security, covering the full application life cycle from development to deployment. 

On the other hand, Service Center provides further details and visibility for each environment. OutSystems customers have, therefore, access to all the tools and information required for proper governance of their applications throughout the whole application lifecycle.
 
### Security Logging & Monitoring Failures (LCNC-SEC-10)

[Lifetime](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_Your_OutSystems_Infrastructure) provides full governance over applications throughout the full lifecycle. From Lifetime you can monitor every application version across all environments. Lifetime also provides user management and auditing capabilities for IT users access, configuration and application changes. [Service Center](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Monitor_and_Troubleshoot/View_the_Environment_Logs_and_Status) provides further logging details per environment. 

OutSystems out-of-the-box logs all access to external systems through web services, custom integration logic, or web service requests to applications running inside the platform. The logs keep a record of who made the request, the request’s target, the method called, how long the request took, and the exact time of the request. This enables you to track down any security issues efficiently. 

OutSystems applications can be built and extended through built-in logging actions to generate further logging according to application and business needs.

Customers who choose to manage their own OutSystems installation benefit from the OutSystems standard runtime architecture to leverage their know-how and tools for logging and monitoring all system components.

OutSystems Cloud customers benefit from the logging and monitoring capabilities bundled in the service with a choice between the secure baseline of the standard configuration and the more advanced [OutSystems Sentry](https://www.outsystems.com/sentry/) offer.


## OWASP Mobile Top 10 - Final List 2016

Find below the set of OutSystems capabilities that help you address each vulnerability identified by [OWASP Mobile Top 10](https://owasp.org/www-project-mobile-top-10/).

### Improper Platform Usage (M1)

The OutSystems approach to mobile is a React-based hybrid client built on top of the Open-Source Apache Cordova library.

Special care is taken to guarantee that our generated code complies with all Android and iOS specifications.

Additionally, the [AppShield add-on](https://www.outsystems.com/forge/component-overview/9379/outsystems-appshield) includes root and jailbreak detection, blocks emulators, and identifies the permissions enabled on the device.

### Insecure Data Storage (M2)

OutSystems provides you a set of pre-built components, such as the [Key Store Plugin](https://www.outsystems.com/forge/component-overview/1550/key-store-plugin) or the [Ciphered Local Storage Plugin](https://www.outsystems.com/forge/component-overview/1500/ciphered-local-storage-plugin), to handle the storage of sensitive data in the device.

The AppShield add-on blocks screen readers and key loggers. It also provides a secure local storage mechanism that blocks the copying of data to another device.

### Insecure Communication (M3)

OutSystems mobile apps communicate with the server endpoints over HTTPS and therefore encrypts all communication. Any attempt to use one of these endpoints over HTTP issues an error on the server-side.

To add an extra layer of security on top of HTTPS communications, you can use the [SSL Pinning Plugin](https://www.outsystems.com/forge/component-overview/1873/ssl-pinning-plugin) to prevent man-in-the-middle attacks.

### Insecure Authentication (M4)

OutSystems includes a robust built-in authentication mechanism that keeps user authentication information encrypted within authentication cookies. You are able to adjust the authentication cache, idle, and expiration periods per environment according to your application requirements.

See [Configure App Authentication](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Secure_the_Applications/Configure_App_Authentication) for further details.

### Insufficient Cryptography (M5)

You can use pre-built components, such as the [Key Store Plugin](https://www.outsystems.com/forge/component-overview/1550/key-store-plugin) or the [Ciphered Local Storage Plugin](https://www.outsystems.com/forge/component-overview/1500/ciphered-local-storage-plugin), to encrypt the application sensitive data in the device.

Additionally, the AppShield add-on blocks the copying of local data and assures it’s properly encrypted, includes repackaging protection, and ensures the security mechanisms can’t be removed from the app.

### Insecure Authorization (M6)

OutSystems role-based access control restricts access to the application’s pages depending on specific application-level roles. Developers define application-level permissions for roles using visual building blocks.

Once users are registered to use an application, role-based access control ensures that only authorized users are allowed to perform specific business functions.

### Client Code Quality (M7)

As visual application models translate into standard code-React.JS for the device, .NET for the backend-OutSystems uses secure code patterns that protect applications from common vulnerabilities.

When developers need to override the default secure code patterns for advanced customization scenarios, they receive design-time warnings for potential injection flaw patterns, along with guidelines to fix them. Additionally, OutSystems provides a set of sanitization functions that developers can use in advanced scenarios to avoid code injection.

Additionally, the AppShield add-on includes code injection protection, repackaging detection, and verification of the application signature. It removes debug information from the application code, and blocks debugger and emulator access. Also, it allows the report of security controls and device anomalies to application code for specific handling.

### Code Tampering (M8)

To prevent code modification of the apps via malicious forms, the AppShield add-on includes root, jailbreak, and repackaging detection. Also, it blocks debugger and emulator access.

### Reverse engineering (M9)

The AppShield add-on includes code obfuscation, and blocks debugger and emulator access, thus preventing reverse engineering of your mobile app.

### Extraneous Functionality (M10)

Using OutSystems built-in application debugging capabilities during the development and testing stages reduces the need of creating extraneous code for testing and debugging purposes. This reduces the risk of deploying extraneous code to production.
