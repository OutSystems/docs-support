---
summary: See how OutSystems helps you address the vulnerabilities identified by OWASP. 
tags: support-Security-overview
---

# How OutSystems helps you address OWASP Top 10

The [OWASP Top 10](https://owasp.org/www-project-top-ten/) and [OWASP Mobile Top 10](https://owasp.org/www-project-mobile-top-10/) represent a broad consensus about the most critical security risks to web and mobile applications.

This article describes how OutSystems helps you address the vulnerabilities identified by OWASP.

For more information on how to achieve the highest level of security for your OutSystems applications, see [Application security overview](intro.md).

## OWASP Top 10 - Final List 2017

### Injection (A1) and Cross-Site Scripting (XSS) (A7)

By default, OutSystems escapes content before showing it on the UI. Escaping untrusted HTTP request data based on the context in the HTML output (body, attribute, JavaScript, CSS, or URL) resolves reflected and stored XSS vulnerabilities. When developers need to override the default secure code patterns for advanced customization scenarios, they receive design-time warnings for potential injection flaw patterns, along with guidelines to fix them.

Additionally, OutSystems provides a set of sanitization functions that developers can use in advanced scenarios to avoid code injection in HTML, JavaScript, and SQL snippets. Using these functions, developers can remove potential malicious content, coming from user input before it’s stored in the database or rendered on the UI.

Architects, operators, or administrators can use OutSystems mechanisms to define content security policies-the domains from which application pages can retrieve resources (images, CSS, scripts, media). You can configure this setting for each environment, generically applying to all applications, or defining it for specific applications. Limiting the sources from which the applications can load resources effectively mitigates XSS attacks, which require loading a script from a malicious site.

You can also use content security policies to prevent application pages from being embedded in frames and thus prevent clickJacking attacks.

See also [Protecting OutSystems apps from code injection / Cross Site Scripting attacks](../develop-secure-apps/code-injection-css-attacks.md).

### Broken Authentication (A2)

By default, OutSystems ensures that:

* Session identifiers aren't sent in URLs
* Sessions time out at their expiration time
* All password handling uses strong cryptographic algorithms

Also, OutSystems ensures that the session identifier is transparently changed on each login, and validates this on every request, thus preventing session fixation attacks.

Cookies may contain sensitive information that shouldn't be accessible to an attacker eavesdropping on a channel. To prevent browsers from sending cookies over an unencrypted channel, administrators can enable the secure flag in cookies, which makes Web browsers that support this flag to send secure cookies only when the request uses HTTPS.

Additionally, OutSystems provides built-in protection mechanisms against brute force attacks for the application end users and IT users.

### Sensitive Data Exposure (A3)

To protect your data in transit, OutSystems allows you to enable SSL in your infrastructure, thus you can use HTTPS to ensure that any content will load over a secure connection. You can enforce the HTTPS security for the applications running in an environment, and enable HTTP Strict Transport Security (HSTS) for the whole environment.

If you need extra layers of compliance, and opt for a [high-compliance OutSystems Cloud](https://www.outsystems.com/sentry/), you have enforced HTTPS communications for all web applications.

To protect your application-sensitive data, OutSystems enables integration with existing cryptographic pre-built components.

In OutSystems Cloud environments, you can activate the database encryption service, which includes the underlying storage for database server instances, its automated backups, and snapshots.

See also [Protecting OutSystems apps using encryption and SSL/TLS](../develop-secure-apps/encryption-ssl-tls.md).

### XML External Entities (XXE) (A4)

For both exposure and consumption of SOAP Web Services, OutSystems escapes XML parsing. Additionally, to help you protect your applications from XML External Entity attacks, OutSystems supports the use of the latest deserialization and XML processor library versions, and SOAP 1.2.

### Broken Access Control (A5)

OutSystems role-based access control restricts access to the application’s pages depending on specific application-level roles. Developers define application-level permissions for roles using visual building blocks.

Once users are registered to use an application, role-based access control ensures that only authorized users are allowed to perform specific business functions.

See also [Protecting OutSystems apps from access control / permissions vulnerabilities](../develop-secure-apps/access-control-vulnerabilities.md).

### Security Misconfiguration (A6)

OutSystems Cloud infrastructures are automatically provisioned, configured, and tuned for high performance, security, and reliability. The physical infrastructure of the OutSystems Cloud is hosted in the secure data centers of Amazon Web Services.

If you need extra layers of security and compliance, you can opt for the [OutSystems Sentry](https://www.outsystems.com/sentry/) offer.

For self-managed deployments, OutSystems provides system administrators with clear and concise instructions on how to make the platform installation secure.

Additionally, OutSystems includes a set of capabilities that enable you to define and implement the security controls required by your applications. See [Application security overview](intro.md) for further details.

### Insecure Deserialization (A8)

OutSystems serializes and deserializes session data using a built-in anti-tampering JSON deserialization mechanism. This mechanism compares incoming JSON data with predefined application models and performs strict type verification during deserialization. Additionally, it runs a salted hash-based algorithm over the serialized session data to validate potential tampering before deserialization.

### Using Components with Known Vulnerabilities (A9)

OutSystems constantly monitors for vulnerabilities in the product and the generated code, using a continuous delivery approach to constantly release incremental value with minimal disruptions to the customers’ operations and business.

[This policy](../vulnerabilities/intro.md) describes the OutSystems response to vulnerabilities that might affect customer applications. Security fixes are proactively applied in OutSystems Cloud.

### Insufficient Logging & Monitoring (A10)

OutSystems tracks the details of every access to application screens. These logs include the component and screen accessed, which end users accessed it, when the access occurred, and exactly which node served the screen.

OutSystems also logs all access to external systems through web services, custom integration logic, or web service requests to applications running inside the platform. The logs keep a record of who made the request, the request’s target, the method called, how long the request took, and the exact time of the request. This enables you to track down any security issues efficiently.

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
