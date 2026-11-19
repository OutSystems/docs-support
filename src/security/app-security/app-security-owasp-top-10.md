---
summary: Learn how OutSystems 11 (O11) and OutSystems Developer Cloud (ODC) help you address the OWASP Top 10 security risks for web and mobile apps.
tags:
  - Authentication
  - Authorization
  - Mobile app
  - Monitoring
  - OWASP
  - Security
  - Web
locale: en-us
guid: 74924eac-d729-4c99-bcb4-09b40a483cfa
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11, odc
figma:
audience:
  - Architect
  - Developer
  - Front-end developer
  - Platform administrator
outsystems-tools:
  - service studio
  - odc studio
  - odc portal
coverage-type:
  - understand
  - apply
isautopublish: true
---

# How OutSystems helps you address OWASP top 10

The [OWASP Top 10](https://owasp.org/www-project-top-ten/), [OWASP Low Code Top 10](https://owasp.org/www-project-top-10-low-code-no-code-security-risks/), and [OWASP Mobile Top 10](https://owasp.org/www-project-mobile-top-10/) represent a broad consensus about the most critical security risks to web and mobile applications.

When you assess how a platform handles application security, use the OWASP Top 10 as a baseline for awareness. The OWASP Top 10 isn't a security standard or a certification, and it doesn't cover every security risk. To verify security requirements in detail, OWASP publishes the [Application Security Verification Standard (ASVS)](https://owasp.org/www-project-application-security-verification-standard/).

Security in OutSystems Cloud, which includes OutSystems Developer Cloud (ODC) and OutSystems 11 (O11) Cloud, is a shared responsibility. OutSystems operates and secures the components from the platform down to the infrastructure. You're responsible for your apps, their data, and the access and permissions of their users. For more information, refer to [OutSystems Cloud shared responsibility model](../../enterprise/maintenance/cloud-shared-responsibility.md).

This article describes how OutSystems helps you address the risks in these lists. The OWASP Top 10:2025 section covers O11 and ODC. The sections about the Low Code/No Code list and the Mobile list cover O11.

For more information about how to secure your OutSystems apps, refer to [Application security overview](intro.md).

## OWASP top 10:2025

The following table summarizes, for each category, what OutSystems covers by default, what you configure or apply with OutSystems mechanisms, and what remains your responsibility. The sections after the table describe each mechanism and the platform it applies to.

| Category | Covered by default | You configure or apply | Your responsibility |
| --- | --- | --- | --- |
| Broken Access Control (A01) | O11: CSRF tokens in Reactive Web Apps.<br/>ODC: Access token validation before each request reaches the target service. This validation isn't a permission check. | End-user roles on screens, actions, and data, and role checks in server-side logic.<br/>ODC: IP filter rules, with Sentry for ODC. | Define a role model that matches your business rules. |
| Security Misconfiguration (A02) | O11 Cloud: Load balancer with WAF capabilities, as a first layer of defense.<br/>ODC: WAF, infrastructure policy checks, CIS benchmarks, hardened container images, and enforced TLS for REST services. | Content Security Policy. In O11 Reactive Web Apps, the platform adds `'unsafe-inline'` and `'unsafe-eval'` at runtime unless you turn them off.<br/>O11: Secure cookies.<br/>O11 Cloud: Secure endpoints, which OutSystems enables through a support request. | Keep the app and stage settings that you control aligned with your security requirements. |
| Software Supply Chain Failures (A03) | Vulnerability policy for OutSystems components and supported Forge components.<br/>O11 Cloud: Operating system and application server updates about every 60 days.<br/>ODC: Daily container registry scans and immutable library revisions. | O11: Supported or Trusted Forge components.<br/>ODC: Patch apps with 1-Click Publish, and review library updates. | Assess the components that OutSystems doesn't support before you use them. |
| Cryptographic Failures (A04) | O11: HTTPS for Reactive Web Apps and Mobile Apps, hashed credentials for built-in authentication, and encrypted view state.<br/>O11 Cloud: Encrypted communication between application servers and databases.<br/>ODC: HTTPS, HSTS, and encryption at rest. | Secret site properties and settings.<br/>O11: Forced HTTPS and HSTS for Traditional Web Apps.<br/>O11 Cloud: Database encryption at rest, with availability that depends on your subscription. | Protect the sensitive data that your custom logic and integrations handle. |
| Injection (A05) | Prepared statements for SQL elements and escaped content in expressions, unless you enable **Expand Inline**.<br/>ODC: WAF policies that include protection against SQL injection. | Sanitization and encode functions when you build code dynamically. | Validate the input that you add to queries, HTML, or JavaScript. |
| Insecure Design (A06) | O11: Security Warnings in Service Studio.<br/>ODC: Secure-by-design platform and stage isolation. | Code Quality analysis. In O11, you onboard your infrastructure to Code Quality first.<br/>O11: SAST on generated source code. | Design your apps for security, for example with threat modeling. |
| Authentication Failures (A07) | O11: Cookie validation, and brute force protection for apps that use the Users provider.<br/>ODC: Password policy, lockout, refresh token rotation, session identifier change on login, and PKCE. | External IdPs, including MFA through the IdP.<br/>O11 self-managed: Active Directory.<br/>ODC: Session duration for each stage. | Apply your organization's authentication policies through an external IdP. |
| Software or Data Integrity Failures (A08) | O11: Tamper checks on authentication cookies, signed view state, and MABS update checksums.<br/>ODC: Signed JWTs and unmodified Platform services images. | O11: Session-bound view state for Traditional Web Apps, with the **Use session token to encrypt view state** setting.<br/>Mobile apps: AppShield, with an AppShield license. | Verify the code and data that your apps get from external sources. |
| Security Logging and Alerting Failures (A09) | O11: Service Center and LifeTime logs.<br/>ODC: Immutable audit trail and infrastructure monitoring by OutSystems. | O11 Cloud: Log streaming, with a log streaming subscription.<br/>O11: Log Redaction.<br/>ODC: Audit trail streaming with Sentry for ODC, and Analytics Stream. | Set up alerts and monitor your apps in your SIEM or APM tool. |
| Mishandling of Exceptional Conditions (A10) | Rollback of uncommitted changes in the OutSystems database when an exception isn't handled, and a default Global Exception Handler.<br/>HTTP status code 500 for unhandled exceptions in exposed REST APIs.<br/>ODC: Platform timeouts. | Exception handlers in actions, UI flows, and modules or apps.<br/>O11: **Abort Transaction** property in server-side logic and Traditional Web Apps. | Handle errors in your logic, and control the messages that users see. |

The table and the sections use the following labels for the platform that a mechanism applies to:

* **O11**: OutSystems 11, in both OutSystems Cloud and self-managed installations.
* **O11 Cloud**: OutSystems 11, in OutSystems Cloud only.
* **O11 self-managed**: OutSystems 11, in self-managed installations only.
* **ODC**: OutSystems Developer Cloud.

The **Covered by default** column lists only what applies without setup, a subscription, a support request, or a minimum platform version. Mechanisms that need one of these appear in the **You configure or apply** column, with the prerequisite stated.

The O11 and ODC entries differ in depth. ODC is a managed service, so its entries include controls that OutSystems operates, such as infrastructure checks and key management. The O11 entries mostly describe features that you use in your apps. The entries labeled O11 Cloud describe the controls that OutSystems operates for O11 in OutSystems Cloud. In a self-managed installation, you operate the infrastructure and its controls. The ODC entries describe stages that run in the OutSystems Cloud. In ODC self-hosted stages, you operate the infrastructure, and some controls differ. For example, the OutSystems WAF and IP filters don't apply. For more information, refer to [Self-hosted ODC shared responsibility model](https://www.outsystems.com/tk/redirect?g=7d901e26-3b77-4d4f-923d-956d78cd146d).

For Software Supply Chain Failures, Cryptographic Failures, Insecure Design, and Software or Data Integrity Failures, OutSystems provides supporting mechanisms, but the risk depends mostly on decisions that you make. For these categories, the **Your responsibility** column matters most.

### A01:2025 broken access control

Broken access control lets users act outside their intended permissions. OutSystems provides role-based access control for screens, logic, and data, and flags insecure access patterns in your code.

The following mechanisms address broken access control:

* **O11 and ODC**: You restrict access to screens, actions, and data with end-user roles. The `Check<RoleName>Role` action validates a role in server-side logic. Code Quality flags security patterns such as screens accessible to anonymous users and insecure usage of the `GetUserId` function in client-side logic.
* **O11**: Reactive Web Apps protect against Cross-Site Request Forgery (CSRF) by sending a CSRF token in the `X-CSRFToken` request header with each server call. Traditional Web Apps sign the view state with the `osVisitor` cookie, and the server checks that the signature matches the cookie on each submit or Ajax request. The Open Redirect Warning tells you to wrap redirect input parameters in the `ReplaceURLDomain()` function.
* **ODC**: ODC validates the access token, a signed JSON Web Token (JWT), of every request before the request reaches the target service. The validation checks that the token hasn't expired, is active, was issued in the past, and has a valid signature. If a check fails, ODC rejects the request. The token validation isn't a permission check. After the validation succeeds, the service checks the permissions of the user. With a Sentry for ODC subscription, you restrict access to the apps in each stage with IP filter rules.

For more information about O11, refer to [Validate End User Permissions in the Application](https://www.outsystems.com/tk/redirect?g=68463867-fb0c-4e54-9fe5-d0e117dbf9bb), [Protecting OutSystems apps from Cross Site Request Forgery attacks](../develop-secure-apps/csrf-attacks.md), and [Open Redirect Warning](https://www.outsystems.com/tk/redirect?g=8e3aa9ec-bcb4-4d64-b16c-1a0a77110b8b).

For more information about ODC, refer to [Secure your app with end-user roles](https://www.outsystems.com/tk/redirect?g=BDA3A144-0EB0-4C04-953F-9DED85A477FE), [Architecture of authentication and authorization mechanism](https://www.outsystems.com/tk/redirect?g=5f50a67f-d8c9-444a-9615-090062255870), and [Manage IP filters](https://www.outsystems.com/tk/redirect?g=269db566-d03b-49ae-84d8-c4aa181d8a88).

### A02:2025 security misconfiguration

Security misconfiguration covers insecure defaults, missing hardening, and settings that expose more than an app needs. OutSystems manages the configuration of its cloud infrastructure and provides settings that you use to harden your apps.

The following mechanisms address security misconfiguration:

* **O11 and ODC**: To control the sources from which app pages load resources such as scripts, images, and frames, you define a Content Security Policy (CSP). In O11, you set the CSP for each environment and override it for each app. In O11 Reactive Web Apps, the platform adds `'unsafe-inline'` and `'unsafe-eval'` to the `script-src` directive and `'unsafe-inline'` to the `style-src` directive at runtime, which makes the policy less strict than the directives you set. To remove them, set the **Enforce Unsafe Inline Reactive** and **Enforce Unsafe Eval Reactive** checkboxes in the Factory Configuration Forge component to **False**. In ODC, the CSP is inactive by default, and you activate it for each stage. The `frame-ancestors` directive controls the domains that can embed your app pages in a frame.
* **O11 Cloud**: Each environment has an Application Load Balancer with Web Application Firewall (WAF) capabilities, as a first layer of defense. You also configure secure endpoints that validate the host header of incoming requests. OutSystems enables secure endpoints for the first time through a support request, and then you manage the list of allowed endpoints in LifeTime.
* **O11**: In Service Center and LifeTime, you configure secure session cookies and the SameSite and Secure attributes of cookies.
* **ODC**: A WAF runs on the Content Delivery Network and protects the Platform and the Runtime against common web exploits and bots. OutSystems deploys the ODC infrastructure as code, and a policy enforcement tool checks it for misconfigurations. OutSystems applies the CIS benchmarks for all systems and hardens the base container image of each app to minimize the attack surface. ODC enforces SSL/TLS for all REST services, and you can't disable it.

For more information about O11, refer to [Apply Content Security Policy](https://www.outsystems.com/tk/redirect?g=e59d9233-7c2d-43ae-b8a2-f55d75263c68), [Implementing a WAF for your applications on OutSystems Cloud](https://www.outsystems.com/tk/redirect?g=E0B721A4-C4F7-47AD-8E33-529F6383145C), [Configuring secure endpoints](https://www.outsystems.com/tk/redirect?g=6c1dcebe-0c55-4fb3-b94b-21d162a23053), and [Enable secure session cookies and set application cookies as secure](https://www.outsystems.com/tk/redirect?g=e65820c4-3550-4a5d-be8d-54531bada121).

For more information about ODC, refer to [Implement content security policy](https://www.outsystems.com/tk/redirect?g=6575ff95-52d4-4f2b-acf8-945066b73217) and [Security of OutSystems Developer Cloud](https://www.outsystems.com/tk/redirect?g=bffd8c9e-16b6-4458-a146-ddb6f8077e12).

### A03:2025 software supply chain failures

Software supply chain failures happen when the components, tools, or pipelines that build and deliver software are vulnerable or compromised. OutSystems scans and patches the components it ships, and the OutSystems Curation Team validates the Forge components that carry the Trusted label. Before you use a component that OutSystems doesn't support, you assess it.

The following mechanisms address software supply chain failures:

* **O11 and ODC**: The OutSystems vulnerability policy covers OutSystems components, including Platform Server, LifeTime, Service Studio, MABS, ODC, and ODC Studio, and the Forge components supported by OutSystems. OutSystems rates each vulnerability with the Common Vulnerability Scoring System (CVSS).
* **O11**: Forge labels components as Supported or Trusted. OutSystems develops, maintains, and supports a Supported component. The OutSystems Curation Team validates a Trusted component against security requirements, and the Community supports it. A Trusted component depends only on components that are trusted or supported by OutSystems.
* **O11 Cloud**: OutSystems installs updates of the operating system and application server approximately every 60 days. When a platform vendor reports a vulnerability, OutSystems Cloud support reassesses the risk and presents a mitigation plan for any critical vulnerability within 7 days. AWS schedules security patches for the database, and OutSystems notifies you.
* **ODC**: At each stage of the deployment pipeline of the Platform services, admission control verifies that the previous stage completed and that the container image is unmodified. ODC scans the container registry daily, including the images of all deployed apps. In the ODC Portal, the **App security** tab lists the apps with known vulnerabilities, the classification of the vulnerabilities, and the fixing schedule. OutSystems patches these vulnerabilities automatically, or you patch them with 1-Click Publish. Library revision numbers are immutable, and ODC Studio asks you to review or dismiss each library update.

For more information about O11, refer to [Vulnerabilities](../vulnerabilities/intro.md), [Curating Projects](../../forge/forge-faqs/curate-project.md), [Trusted asset requirements](../../forge/forge-faqs/trusted-requirements.md), and [Deploy an infrastructure on OutSystems Cloud](https://www.outsystems.com/tk/redirect?g=de7c085b-1c0b-4a1f-9d36-4a7e3f1c3ebc).

For more information about ODC, refer to [Security of OutSystems Developer Cloud](https://www.outsystems.com/tk/redirect?g=bffd8c9e-16b6-4458-a146-ddb6f8077e12) and [Libraries](https://www.outsystems.com/tk/redirect?g=5102d9d1-9716-46aa-9ab7-3c9640a7f79c).

### A04:2025 cryptographic failures

Cryptographic failures expose data in transit or at rest. OutSystems encrypts communication and protects secrets and credentials. You protect the sensitive data that your custom logic and integrations handle.

The following mechanisms address cryptographic failures:

* **O11**: Reactive Web Apps and Mobile Apps serve all requests over HTTPS. For Traditional Web Apps, you force HTTPS for screens and exposed integrations, and you enable HTTP Strict Transport Security (HSTS) for the environment. Secret site properties are encrypted before OutSystems stores them. For built-in end-user authentication, OutSystems stores only the result of a cryptographic hash function computed from the credentials. The view state of Traditional Web Apps is encrypted by default.
* **O11 Cloud**: The communication between the application servers and the databases is encrypted by default. OutSystems encrypts production databases and their automated backups at rest with the AES-256 algorithm, and the availability of database encryption depends on your subscription.
* **ODC**: All incoming requests terminate at an HTTPS endpoint and are encrypted end to end. ODC implements HSTS as a native default and supports TLS 1.3. ODC encrypts data at rest, including backups, with the AES-256-GCM algorithm. Production runtime app data is encrypted with a per-customer key that OutSystems manages. Settings that you set as secret are always encrypted and never show as plain text. Logs and traces are encrypted in transit with TLS and at rest with AES-256.

For more information about O11, refer to [Enforce HTTPS Security](https://www.outsystems.com/tk/redirect?g=a152ecbb-2419-489f-87c5-000918d502f0), [Site property](https://www.outsystems.com/tk/redirect?g=dc811245-bcef-4579-bcee-3530a997eecd), [End users authentication](https://www.outsystems.com/tk/redirect?g=eaa92f05-a00d-4e75-a937-8c100b81d6df), [Encrypt web apps view state](https://www.outsystems.com/tk/redirect?g=a07b13f4-d8a9-4d32-8c52-57544422ce46), [Deploy an infrastructure on OutSystems Cloud](https://www.outsystems.com/tk/redirect?g=de7c085b-1c0b-4a1f-9d36-4a7e3f1c3ebc), and [Securing data at rest with encryption](https://www.outsystems.com/tk/redirect?g=5f4a803b-5b64-4b4b-bef7-eba1cc149941).

For more information about ODC, refer to [Security of OutSystems Developer Cloud](https://www.outsystems.com/tk/redirect?g=bffd8c9e-16b6-4458-a146-ddb6f8077e12) and [Set as secret](https://www.outsystems.com/tk/redirect?g=3a5f56e7-2515-4e97-914e-b8a503f82c7f).

### A05:2025 injection

Injection happens when untrusted input runs as part of a query, a script, or a page. OutSystems separates input from code by default and provides functions to encode and sanitize input when you build code dynamically.

The following mechanisms address injection:

* **O11 and ODC**: OutSystems runs the SQL queries of SQL elements as prepared statements by default, so parameters hold values and not code. Code Quality flags query parameters with the **Expand Inline** property enabled, which removes this protection. The Sanitization library provides functions such as `SanitizeHtml` that remove malicious content from input. The `EncodeSql`, `EncodeHtml`, `EncodeJavaScript`, and `EncodeUrl` functions encode values for each context. OutSystems also escapes content in expressions by default, and the **Expand Inline** property deactivates this escaping. Service Studio and ODC Studio show warnings for potential SQL, HTML, and JavaScript injection.
* **O11**: Service Studio also shows warnings for potential LDAP filter injection.
* **ODC**: The policies of the WAF include protection against SQL injection attacks.

For more information about O11, refer to [Injection and Cross Site Script - XSS](https://www.outsystems.com/tk/redirect?g=f2de9e37-9a7e-4f1d-951a-271954eaa4f2), [SQL Injection Warning](https://www.outsystems.com/tk/redirect?g=fb90dea0-5413-4871-8e16-ee2b0ce89a73), and [Sanitization API](https://www.outsystems.com/tk/redirect?g=6193f89c-cf98-4f38-8308-6eb0eee24f86).

For more information about ODC, refer to [SQL injection](https://www.outsystems.com/tk/redirect?g=de111634-1c2f-4d83-b60b-1b8ede727ce4) and [Sanitization](https://www.outsystems.com/tk/redirect?g=09b3e01c-e0ee-4ead-be0e-3e30f2ca2262).

### A06:2025 insecure design

Insecure design covers weaknesses in how an app is planned, which correct code alone doesn't fix. Code Quality flags insecure code patterns, and OutSystems applies secure-by-design principles to the platform. These mechanisms don't assess the design of your app, such as threat models and authorization rules. You design your apps for security, for example with threat modeling.

The following mechanisms address insecure design:

* **O11 and ODC**: Code Quality analyzes your apps for security patterns, such as exposed REST services without authentication and screen aggregates that expose system entities on anonymous screens. In O11, you onboard your infrastructure to Code Quality before it analyzes your apps.
* **O11**: Service Studio shows a Security Warning when you expose a database operation in client-side logic or create anonymous Server Actions. To run static application security testing (SAST), you analyze the source code that OutSystems generates for your apps.
* **ODC**: OutSystems designs ODC with the secure-by-design principles from the OWASP Developer Guide, such as defense in depth and least privilege. A network namespace isolates each stage within the Runtime of each organization.

For more information about O11, refer to [Security Warning](https://www.outsystems.com/tk/redirect?g=2dd8aae1-92e8-4901-a1d4-95e98c968ae7), [Code analysis patterns](https://www.outsystems.com/tk/redirect?g=a7187cf7-6f1d-4f7c-8141-03f856639f08), and [Static application security testing](../static-application-security-testing.md).

For more information about ODC, refer to [Manage technical debt in ODC](https://www.outsystems.com/tk/redirect?g=6be15662-74c5-4c35-9a7d-16a28816614c) and [Security of OutSystems Developer Cloud](https://www.outsystems.com/tk/redirect?g=bffd8c9e-16b6-4458-a146-ddb6f8077e12).

### A07:2025 authentication failures

Authentication failures let attackers take over accounts or sessions. OutSystems protects sign-in and sessions, and integrates with external identity providers (IdPs) that apply your authentication policies, such as multi-factor authentication (MFA).

The following mechanisms address authentication failures:

* **O11**: OutSystems validates the authentication cookies of each request. Brute force protection blocks a user from signing in from the attacking IP address, or blocks the attacking IP address, after repeated failed attempts. For end users, this protection applies to apps that use the Users provider or a provider cloned from Users. End users authenticate with the built-in method, LDAP, SAML 2.0, Microsoft Entra, or Okta. In O11 self-managed installations, end users can also authenticate with Active Directory, which isn't available in OutSystems Cloud. IT users authenticate with the built-in method or, when you activate OpenID Connect (OIDC), with an external IdP that applies its own policies, such as MFA.
* **ODC**: Passwords have at least 12 characters, including one numeric digit and one upper-case letter. ODC temporarily locks users out after five consecutive failed sign-in or password change attempts. You set the maximum and idle session duration for each stage. ODC enforces refresh token rotation and changes the session identifier on each login, which protects against session fixation. You use an external OIDC IdP to apply MFA and a custom password policy to the Platform services and your apps. With OIDC providers, ODC supports only the Authorization Code flow with Proof Key for Code Exchange (PKCE).

For more information about O11, refer to [Configure app authentication](https://www.outsystems.com/tk/redirect?g=74fffe9e-d6fa-4ea9-a8ae-aa7a34a37511), [Protection against brute force attacks](https://www.outsystems.com/tk/redirect?g=12783fed-7ac1-41f3-8d46-544892ff8b58), and [IT Users Integration with External IdP via OpenId Connect](https://www.outsystems.com/tk/redirect?g=595C5E6F-7C59-4314-9BDE-4EF1400A670F).

For more information about ODC, refer to [Passwords](https://www.outsystems.com/tk/redirect?g=41b86768-295e-4aeb-98ed-9a0f6db4cfd2), [Configure user session](https://www.outsystems.com/tk/redirect?g=596ba2aa-7ea4-4498-9f65-242e0b24e047), and [Configuring authentication with external identity providers](https://www.outsystems.com/tk/redirect?g=5aa8692d-68bf-41a1-89ec-5e8fc7069e29).

### A08:2025 software or data integrity failures

Integrity failures happen when an app trusts code or data that an attacker can modify. OutSystems signs or validates the cookies, tokens, view state, and platform artifacts that it issues and delivers. You verify the code and data that your apps get from external sources.

The following mechanisms address software or data integrity failures:

* **O11**: The server rejects authentication cookies that were tampered with. Traditional Web Apps sign the view state with the `osVisitor` cookie and encrypt it by default. With the **Use session token to encrypt view state** setting, each page is valid only within the user session. MABS over-the-air updates validate file integrity through checksums.
* **ODC**: ODC signs JSON Web Tokens (JWTs) with a public and private key pair, which protects them from modification. For the Platform services, the container image released to production is identical to the one built.
* **Mobile apps in O11 and ODC**: With an AppShield license, AppShield detects when an app bundle was modified or signed with a different keystore.

For more information about O11, refer to [Configure app authentication](https://www.outsystems.com/tk/redirect?g=74fffe9e-d6fa-4ea9-a8ae-aa7a34a37511), [Encrypt web apps view state](https://www.outsystems.com/tk/redirect?g=a07b13f4-d8a9-4d32-8c52-57544422ce46), [Protecting OutSystems apps from Cross Site Request Forgery attacks](../develop-secure-apps/csrf-attacks.md), and [AppShield protection features](https://www.outsystems.com/tk/redirect?g=7696c5bc-71ab-4eeb-ac4c-2805bd79f5b1).

For more information about ODC, refer to [Architecture of authentication and authorization mechanism](https://www.outsystems.com/tk/redirect?g=5f50a67f-d8c9-444a-9615-090062255870) and [Harden the protection of mobile apps with AppShield](https://www.outsystems.com/tk/redirect?g=5b3d48c3-ddcb-461c-a05d-414fceeb1eb4).

### A09:2025 security logging and alerting failures

Logging and alerting failures delay the detection of attacks. OutSystems records platform and app activity, and streams logs to the tools where you set up alerts.

The following mechanisms address security logging and alerting failures:

* **O11**: Service Center logs screen requests, including the username, and integration calls. LifeTime keeps audit logs of IT user activity for 365 days by default. In OutSystems Cloud, with a log streaming subscription, you stream app and platform logs to your Application Performance Monitoring (APM) tool through OpenTelemetry. The **Log Redaction** property removes sensitive input parameters of consumed REST APIs from logs.
* **ODC**: The audit trail is an immutable record of significant actions and changes in your organization. The ODC Portal shows the last 30 days, and you export up to 3 months to CSV. With a Sentry for ODC subscription, you stream the audit trail to your Security Information and Event Management (SIEM) tool and configure custom alerts. With an Analytics Stream subscription, you stream logs, traces, and metrics to your APM tool through OpenTelemetry. OutSystems monitors the ODC infrastructure, events, and availability 24 hours a day, seven days a week.

For more information about O11, refer to [Log data reference](https://www.outsystems.com/tk/redirect?g=cfc99287-9b0a-46d6-9daf-b62d281dcbef), [Monitor Usage with Audit Logs](https://www.outsystems.com/tk/redirect?g=ff41a92e-5717-4a6c-9016-12acdb4de71f), [Introduction to log streaming](https://www.outsystems.com/tk/redirect?g=75f48471-6193-4149-abf4-29c15e75c1f6), and [Redacting information from REST API logs](https://www.outsystems.com/tk/redirect?g=966c33e2-bdc0-4847-91b3-9fbda9b29d9f).

For more information about ODC, refer to [Audit trail](https://www.outsystems.com/tk/redirect?g=3f3bc6b9-7335-4d8b-bb41-2eb396b86f3c), [Stream audit trail logs](https://www.outsystems.com/tk/redirect?g=000ca25b-a3c6-42d5-9ab9-8f3219f0a283), and [Streaming observability data](https://www.outsystems.com/tk/redirect?g=43e08fbf-f050-4946-aad2-289ab110be44).

### A10:2025 mishandling of exceptional conditions

Mishandled errors leave apps in an inconsistent state or expose details to users. OutSystems provides exception handling at the action, flow, and app levels, and rolls back uncommitted database changes when an exception isn't handled.

The following mechanisms address mishandling of exceptional conditions:

* **O11 and ODC**: You handle exceptions with Exception Handler elements in actions, the On Exception action of UI flows, and the Global Exception Handler of the module or app. By default, the Global Exception Handler is the On Exception action of the Common UI flow. The Global Exception Handler doesn't cover the **OnApplicationReady** event handler. If an exception isn't caught, OutSystems rolls back the uncommitted changes in the OutSystems database. Changes that were already committed stay in the database. When a consumed REST API returns an HTTP status code of 400 or above, OutSystems throws an exception that you handle in your logic. When an exposed REST API method raises an exception that isn't handled, OutSystems rolls back the database changes and returns the HTTP status code 500 with the error message in the response body.
* **O11**: The **Abort Transaction** property of the Exception Handler is available in server-side logic and in Traditional Web Apps. It sets whether OutSystems rolls back the uncommitted database changes. If you set it to **No**, the transaction continues and OutSystems commits it with the next `CommitTransaction` action or at the end of the request.
* **ODC**: In an Exception Handler, you can roll back or commit the transaction of the OutSystems database only. Service actions and external entities use their own transactions. When a service action ends, ODC commits its transaction, and you can't roll it back. Platform limits set timeouts, such as 60 seconds for an exposed REST API method and 100 seconds for a service action.

For more information about O11, refer to [Exception Handling Mechanism](https://www.outsystems.com/tk/redirect?g=aa97807f-3db5-4d86-a746-7fe2506481a6), [Handling transactions](https://www.outsystems.com/tk/redirect?g=cb6c0a9e-1714-484f-90ed-74f2afa98f67), [Exception Handler](https://www.outsystems.com/tk/redirect?g=9d318909-8caa-4f44-85fd-ef3ada5d566c), and [Handling REST Errors](https://www.outsystems.com/tk/redirect?g=5a815098-ae36-4134-91ac-761a1087c31f).

For more information about ODC, refer to [Exception Handling Mechanism](https://www.outsystems.com/tk/redirect?g=7f5c109f-a887-4f50-bd5d-ead38e50ff53), [Transactions in external entities](https://www.outsystems.com/tk/redirect?g=05934d09-1852-40c7-8b4f-cafd0f93f2a3), [Throw a Custom Error in an Exposed REST API](https://www.outsystems.com/tk/redirect?g=e1d028a0-d688-4cbb-93c1-caecb302ee9a), and [OutSystems system requirements for ODC](https://www.outsystems.com/tk/redirect?g=D940C32D-0409-4D49-B6FE-BB831E5EF12C).

## OWASP low code/no code top 10 - July 2022

This section describes how OutSystems helps you address the Top 10  Low Code/No Code Security Risks as  identified by OWASP.

For more information on how to achieve the highest level of security for your OutSystems applications, see [Application security overview](https://success.outsystems.com/Support/Security/Develop_secure_OutSystems_apps).

### Account impersonation (LCNC-SEC-01)

OutSystems creates and manages application credentials without requiring developer access. Developers cannot access or change the credentials applications use to run and access resources.

Apps are staged across multiple environments, from Development to Production and custom integrations with third-party services can leverage environment-wide configurations, that will not propagate to other environments.

To further increase security, you can use roles to allow developers to publish applications only to non-production environments and reserve the privilege to change environment configurations for a small set of DevOps staff.

For more information, refer to the following:

* [Protecting OutSystems apps from access control / permissions vulnerabilities](https://success.outsystems.com/Support/Security/How_the_OutSystems_Platform_Helps_You_Develop_Secure_Applications/Protecting_OutSystems_apps_from_access_control_/_permissions_vulnerabilities)
* [Configure Web Service Authentication](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Consuming_SOAP_Web_Services/Configure_Web_Service_Authentication)
* [Consume REST APIs](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/REST/Consume_REST_APIs)

### Authorization misuse (LCNC-SEC-02)

OutSystems was built with productivity and speed of development in mind, but no shortcuts to authentication and authorization exist that may put your applications in danger.

Each application can create its own authentication and authorization flows for itself or for integration with third-party services with no shared connections.

Furthermore, OutSystems role-based access control restricts access to the application’s pages depending on specific application-level roles. Developers define application-level permissions for roles using visual building blocks.

Once users are registered to use an application, role-based access control ensures that only authorized users are allowed to perform specific business functions.

See also [Protecting OutSystems apps from access control / permissions vulnerabilities](https://success.outsystems.com/Support/Security/How_the_OutSystems_Platform_Helps_You_Develop_Secure_Applications/Protecting_OutSystems_apps_from_access_control_/_permissions_vulnerabilities).

### Data leakage (LCNC-SEC-03)

OutSystems and the applications you develop do not perform any data movement or any data processing for that matter without explicit coding from the application developer.

As with other development tools, development privileges should be restricted to dedicated personnel. OutSystems provides roles that can be leveraged to provide developers different levels of access to different applications, environments, and data.  

### Authentication and secure communication failures (LCNC-SEC-04)

OutSystems environments can easily be configured to accept only secure encrypted connections. Configurations can be done per application or enforced across all applications via environment settings.

Applications are staged across multiple environments, and role-based authorization can be used to restrict access to environment settings.

### Security misconfiguration (LCNC-SEC-05)

OutSystems follows best practices in governance and security to ensure that proper defaults are in place, providing an optimal balance between security by design and out-of-the-box functionality.

OutSystems provides configuration settings both at the application level and at the environment level.

Environment-level configurations can be used combined with role-based authorization to ensure, for example, that developers only have access to their applications or to non-production environments and that any production environment configuration can only be made by high-privileged DevOps staff.

OutSystems includes a set of capabilities that enable you to define and implement the security controls required by your applications. See [Application security overview](https://success.outsystems.com/Support/Security/Develop_secure_OutSystems_apps).

Moreover, [AI Mentor Studio can scan your applications and identify risky patterns](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_technical_debt/Code_Analysis_Patterns#Security)

### Injection handling failures (LCNC-SEC-06)

Injection handling failures or injection / input validation failures are common to all applications in all technologies. For more information about how OutSystems addresses injection, refer to [A05:2025 injection](#a052025-injection).

### Vulnerable and untrusted components (LCNC-SEC-07)

OutSystems constantly monitors for vulnerabilities in the platform and the generated code, using a continuous delivery approach to constantly release incremental value with minimal disruptions to the customers’ operations and business.

OutSystems enables the use of shared components. For this, OutSystems recommends using the OutSystems Forge where components, modules and applications are published, shared and scrutinized by the community.

As with open-source projects, OutSystems components shared in Forge can be downloaded, opened, analyzed, tested, and changed before use or being published to production. The platform provides full visibility over all application components and dependencies making it easier to spot and address unauthorized components.

You can also choose to only download and use OutSystems [Supported or Trusted Forge components](https://success.outsystems.com/Support/Forge_Components/Forge_FAQs/Curating_Projects) to make sure you only use components that have been curated and validated by OutSystems.

### Data and secret handling failures (LCNC-SEC-08)

OutSystems recommends not hardcoding secrets in the code but using other provided methods.

For example, you can use site properties to store configuration data to be available to applications in an environment and have different configuration data or credentials across environments.

Role-based authorization can again be used to make sure the developers only have access to code and reserve the permission to change environment configuration and particularly production configuration for high-privileged IT users.

If the preference is to store that data away from the managed database, applications built with OutSystems can be extended through extensions and can be integrated with third-party services and external databases.

Integration with third-party services, for example, can be used to store sensitive data in a secret management service. It’s up to the customer, however, to choose where and how to store the data. Moreover, OutSystems will never move any data out of its original geo-location in compliance with data residency regulations.

### Asset management failures (LCNC-SEC-09)

OutSystems provides tools that enable full visibility and management of the platform, applications, application dependencies and integration with third-party services.

[**LifeTime**](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_Your_OutSystems_Infrastructure) is the centralized console for managing your OutSystems environments, applications, IT users, and security, covering the full application life cycle from development to deployment.

On the other hand, Service Center provides further details and visibility for each environment. OutSystems customers have, therefore, access to all the tools and information required for proper governance of their applications throughout the whole application lifecycle.

### Security logging & monitoring failures (LCNC-SEC-10)

[Lifetime](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_Your_OutSystems_Infrastructure) provides full governance over applications throughout the full lifecycle. From Lifetime you can monitor every application version across all environments. Lifetime also provides user management and auditing capabilities for IT users access, configuration and application changes. [Service Center](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Monitor_and_Troubleshoot/View_the_Environment_Logs_and_Status) provides further logging details per environment.

OutSystems out-of-the-box logs all access to external systems through web services, custom integration logic, or web service requests to applications running inside the platform. The logs keep a record of who made the request, the request’s target, the method called, how long the request took, and the exact time of the request. This enables you to track down any security issues efficiently.

OutSystems applications can be built and extended through built-in logging actions to generate further logging according to application and business needs.

Customers who choose to manage their own OutSystems installation benefit from the OutSystems standard runtime architecture to leverage their know-how and tools for logging and monitoring all system components.

OutSystems Cloud customers benefit from the logging and monitoring capabilities bundled in the service with a choice between the secure baseline of the standard configuration and the more advanced [Sentry add-on](https://www.outsystems.com/tk/redirect?g=9e584e22-a5a0-4ae9-8338-e1c4b33dcfbb).

## OWASP mobile top 10 - final list 2016

Find below the set of OutSystems capabilities that help you address each vulnerability identified by [OWASP Mobile Top 10](https://owasp.org/www-project-mobile-top-10/).

### M1 improper platform usage

The OutSystems approach to mobile is a React-based hybrid client built on top of the Open-Source Apache Cordova library.

Special care is taken to guarantee that our generated code complies with all Android and iOS specifications.

Additionally, the [AppShield add-on](https://www.outsystems.com/forge/component-overview/9379/outsystems-appshield) includes root and jailbreak detection, blocks emulators, and identifies the permissions enabled on the device.

### M2 insecure data storage

OutSystems provides you a set of pre-built components, such as the [Key Store Plugin](https://www.outsystems.com/forge/component-overview/1550/key-store-plugin) or the [Ciphered Local Storage Plugin](https://www.outsystems.com/forge/component-overview/1500/ciphered-local-storage-plugin), to handle the storage of sensitive data in the device.

The AppShield add-on blocks screen readers and key loggers. It also provides a secure local storage mechanism that blocks the copying of data to another device.

### M3 insecure communication

OutSystems mobile apps communicate with the server endpoints over HTTPS and therefore encrypts all communication. Any attempt to use one of these endpoints over HTTP issues an error on the server-side.

To add an extra layer of security on top of HTTPS communications, you can use the [SSL Pinning Plugin](https://www.outsystems.com/forge/component-overview/1873/ssl-pinning-plugin) to prevent man-in-the-middle attacks.

### M4 insecure authentication

OutSystems includes a robust built-in authentication mechanism that keeps user authentication information encrypted within authentication cookies. You are able to adjust the authentication cache, idle, and expiration periods per environment according to your application requirements.

See [Configure App Authentication](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Secure_the_Applications/Configure_App_Authentication) for further details.

### M5 insufficient cryptography

You can use pre-built components, such as the [Key Store Plugin](https://www.outsystems.com/forge/component-overview/1550/key-store-plugin) or the [Ciphered Local Storage Plugin](https://www.outsystems.com/forge/component-overview/1500/ciphered-local-storage-plugin), to encrypt the application sensitive data in the device.

Additionally, the AppShield add-on blocks the copying of local data and assures it’s properly encrypted, includes repackaging protection, and ensures the security mechanisms can’t be removed from the app.

### M6 insecure authorization

OutSystems role-based access control restricts access to the application’s pages depending on specific application-level roles. Developers define application-level permissions for roles using visual building blocks.

Once users are registered to use an application, role-based access control ensures that only authorized users are allowed to perform specific business functions.

### M7 client code quality

As visual application models translate into standard code-React.JS for the device, .NET for the backend-OutSystems uses secure code patterns that protect applications from common vulnerabilities.

When developers need to override the default secure code patterns for advanced customization scenarios, they receive design-time warnings for potential injection flaw patterns, along with guidelines to fix them. Additionally, OutSystems provides a set of sanitization functions that developers can use in advanced scenarios to avoid code injection.

Additionally, the AppShield add-on includes code injection protection, repackaging detection, and verification of the application signature. It removes debug information from the application code, and blocks debugger and emulator access. Also, it allows the report of security controls and device anomalies to application code for specific handling.

### M8 code tampering

To prevent code modification of the apps via malicious forms, the AppShield add-on includes root, jailbreak, and repackaging detection. Also, it blocks debugger and emulator access.

### M9 reverse engineering

The AppShield add-on includes code obfuscation, and blocks debugger and emulator access, thus preventing reverse engineering of your mobile app.

### M10 extraneous functionality

Using OutSystems built-in application debugging capabilities during the development and testing stages reduces the need of creating extraneous code for testing and debugging purposes. This reduces the risk of deploying extraneous code to production.
