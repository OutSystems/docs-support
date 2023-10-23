---
summary: Learn about how OutSystems is PCI compliant with Sentry
tags:
locale: en-us
guid: 1fcf38a0-15c1-486a-b022-a9d21dea89b6
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---

# PCI compliance with OutSystems Sentry

The PCI (Payment Card Industry) Security Standards Council aims to help secure payments worldwide. This council is also responsible for ensuring that organizations meet the requirements through validation and certification.

The Sentry edition of the OutSystems Cloud shares all the features and benefits of the OutSystems platform with additional layers of compliance. OutSystems Sentry is compliant with PCI DSS SAQ D service provider standards.

To comply with the PCI eData Security Standard (DSS), those companies processing credit card data must ensure that cardholder data is safe.

You can ensure the compliance of your applications with PCI DSS by delegating credit card payments to a 3rd party PCI-compliant payment gateway using one of the following methods:

* **URL Redirection**:  When users are ready to make a payment on your website, they’re redirected to the PCI DSS compliant Service Provider's secure payment page. Payment information is entered directly on the secure payment page hosted by the payment gateway. After the payment is processed, the user may be redirected to your website for confirmation or to complete the transaction.

* **iFrame Integration**:  Use an iFrame integration, where the payment form is embedded within an iFrame on your website. The actual payment data is entered into the PCI DSS-compliant provider's site, reducing your exposure to sensitive information.

If you need more control over the payment process, you can use tokenization, where sensitive cardholder data is replaced with a unique token. This token can be used for transactions without exposing the actual card data. By using tokenization, you have a few additional options available:

* **Direct Post Method**: Employ a direct post method where the payment form is hosted on the PCI DSS Service Provider's infrastructure. The sensitive data is posted directly to the service provider’s servers, bypassing your application systems.
  
* **Secure APIs**: Use secure APIs provided by your service provider to transmit and receive payment data securely.

You should always ensure that no payment card information is ever stored or processed in OutSystems applications. For more details on the supported integration options, refer to your PCI DSS-certified processor.

When developing apps in OutSystems that require PCI compliance, it’s imperative that you strictly adhere to a few security rules and regulations. You can easily do so with OutSystems Sentry by following these instructions:

* **HSTS** (HTTP Strict Transport Security) is implemented in OutSystems by default to protect websites. If you decide to turn it off, your app is no longer compliant. For more information, see the [Enforce HTTPS Security](https://success.outsystems.com/documentation/11/managing_the_applications_lifecycle/secure_the_applications/enforce_https_security/) document.
  
* **CSP** (Content Security Policy) isn't turned on by default. This provides another level of security that helps detect certain types of attacks. With CSP, you define rules that help protect your users and apps from web attacks. For more information, see the [Apply Content Security Policy](https://success.outsystems.com/documentation/11/managing_the_applications_lifecycle/secure_the_applications/apply_content_security_policy/) document.

If you complete all these steps, you are ready for the PCI DSS SAQ attestation of compliance. You can achieve attestation using the services of a PCI Qualified Security Assessor.