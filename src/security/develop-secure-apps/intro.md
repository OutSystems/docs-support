---
summary: Learn how OutSystems 11 (O11) helps develop secure applications by mitigating risks and protecting against common vulnerabilities.
tags: application security, owasp top 10, security best practices
locale: en-us
guid: c6a9c1dc-0b63-422a-a299-634ad131e49b
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma: https://www.figma.com/file/vTtFn5nl44ZLjUBYo2anCO/Security?node-id=305:318
audience:
  - full stack developers
  - frontend developers
  - backend developers
  - architects
outsystems-tools:
  - none
coverage-type:
  - understand
---

# How the OutSystems Platform Helps You Develop Secure Applications

Recent years have shown that security breaches have consistently increased both in terms of number of incidents and gravity of the outcome.

Failing to secure your apps may have severely damaging results for your business, such as:

* Loss of customer trust
* Compromised private data
* Damaged credibility
* Identity theft
* Loss of revenue

## Keeping your enterprise secure 

As attackers are moving faster, exploiting far-reaching vulnerabilities, holding files for ransom, stealing identities and deploying more malicious code, it becomes paramount that you know how to develop applications that are as secure as possible against these attacks.

These attacks aren't isolated to well-defined parts of your enterprise, rather having the potential and the capability of affecting every single technological layer. The purpose of this guide is to provide development best practices to mitigate the security risks at the Application layer.

![Diagram showing three layers of enterprise technology: Applications, Network, and Systems Infrastructure.](images/layers.png "Enterprise Technological Layers")

## Protecting your apps against common vulnerabilities

The Open Web Application Security Project (OWASP) is a free and open software security community. OWASP TOP 10 describes the major vulnerabilities that can be found with web applications.

The following articles provide you with coding best practices with OutSystems to protect your apps against these vulnerabilities:

* [Protecting OutSystems apps from access control / permissions vulnerabilities](access-control-vulnerabilities.md)
* [Protecting OutSystems Apps from Authentication Vulnerabilities](authentication-vulnerabilities.md)
* [Protecting OutSystems apps from code injection / Cross Site Scripting attackss](code-injection-css-attacks.md)
* [Protecting OutSystems apps from Cross Site Request Forgery attacks](csrf-attacks.md)
* [Protecting OutSystems apps using encryption and SSL/TLS](encryption-ssl-tls.md)
* [Protecting OutSystems Apps From Redirects / Forwarders Vulnerabilities](redirects-forwarders-vulnerabilities.md)