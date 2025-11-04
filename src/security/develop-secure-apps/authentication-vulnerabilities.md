---
summary: Explore how OutSystems 11 (O11) enhances app security by mandating HTTPS and HSTS to protect against authentication vulnerabilities.
locale: en-us
guid: bb010468-9ea8-42d8-815d-c5f8cf3ce2cd
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
tags: application security, https, hsts, vulnerability management, authentication security
audience:
  - mobile developers
  - frontend developers
  - full stack developers
outsystems-tools:
  - none
coverage-type:
  - evaluate
---

# Protecting OutSystems Apps From Authentication Vulnerabilities

Authentication is the way your users let your application know who they are. When vulnerable, your application can take actions or show information to someone who shouldn't be allowed to have access.

Generally, these vulnerabilities allow someone to easily fool the system. The system can accept that they are an accredited user without needing to provide actual proof.

## How to do it with OutSystems Platform

The recommended strategy is that you **always** use an **HTTPS** channel.

Specifically for the following use cases, the corresponding actions are recommended:

|Use case    |Actions    |
|------------|-----------|
|Send sensitive information in clear text   |Use **HTTPS**, enable [**HSTS**](https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html) (see [Enforce HTTPS Security](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Secure_the_Applications/Enforce_HTTPS_Security)) |
|Send session ID in clear text  |Use **HTTPS**, enable [**HSTS**](https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html) (see [Enforce HTTPS Security](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Secure_the_Applications/Enforce_HTTPS_Security)) |

## More Information

To learn how to protect your OutSystems apps against other common types of attacks, check [how OutSystems Platfom helps you develop secure applications](intro.md).
