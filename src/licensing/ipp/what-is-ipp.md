---
summary: OutSystems 11 (O11) features Intellectual Property Protection (IPP) to control the deployment of applications across different infrastructures.
locale: en-us
guid: ab6146f9-8d06-44cb-9753-96c701e290f1
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11, odc
figma: https://www.figma.com/file/TzqCbVlN2j4nadunA7q8VU/Licensing?node-id=1318:604
tags: intellectual property protection, application deployment, licensing, outsystems platform, error handling
audience:
  - platform administrators
  - full stack developers
  - backend developers
outsystems-tools:
  - service studio
  - ipp portal
coverage-type:
  - understand
---

# OutSystems Intellectual Property Protection - IPP

## For OutSystems 11 infrastructures

<div class="info" markdown="1">

**Important update**: License files made available from April 2021 onwards are issued with IPP **unprotected** to ensure you can share your apps with other infrastructures.

</div>

The Intellectual Property Protection (IPP) feature **ensures that your apps can't be deployed to another infrastructure without your consent**. You should always be able to deploy apps between environments of the same infrastructure.
By default, IPP is **unprotected**, which means your application can be deployed to other infrastructures. To request your IPP be **protected**, refer to [OutSystems support](https://www.outsystems.com/legal/success/support-terms-and-service-level-agreements-sla-of-the-outsystems-software/#contacting-outsystems-support).

When IPP is **protected**, you can deploy applications across all the environments of the same infrastructure, but you can't deploy applications to environments belonging to other infrastructures.​

<div class="info" markdown="1">

IPP focuses only on protecting the application logic. No data is transmitted or shared during this process.

</div>

If you're trying to deploy modules from other infrastructures, you may get the error message:

```error
Invalid Intellectual Property: You are trying to upload or publish a solution that was created in a Platform Server and its intellectual Property is protected
```

For more information about resolving IPP errors, refer to [Troubleshoot IPP errors](../../troubleshooting/application-development/ipp-error.md).

To deploy applications to an infrastructure to which they don't belong, use the [IPP portal](http://www.outsystems.com/ipp/). Using the IPP portal service you can change the activation code of your applications. When you complete the process, you can publish applications in different infrastructures.

OutSystems logs all IPP portal operations. To check the IPP operations performed in your applications, refer to [OutSystems support](https://www.outsystems.com/legal/success/support-terms-and-service-level-agreements-sla-of-the-outsystems-software/#contacting-outsystems-support).

### IPP unprotected

With IPP unprotected, when you publish a **new module**, it's not marked with the [Activation Code](https://success.outsystems.com/support/licensing/identify_outsystems_infrastructure_and_runtime_environments/) of your infrastructure. This means you can share your modules with other infrastructures.

![Diagram showing applications in an ACME environment can be deployed to any ACME environment and to the EMCA infrastructure, indicating IPP is unprotected.](images/what-is-ipp_unprotected.png "IPP Unprotected Deployment Flow")

In this example, applications developed in an ACME environment can be deployed to any ACME environment and to the EMCA infrastructure.

### IPP protected

With IPP protected, when you publish a module, it's marked with the [activation code](https://success.outsystems.com/support/licensing/identify_outsystems_infrastructure_and_runtime_environments/) of your infrastructure. This means you can only deploy this module to environments with the same activation code. In addition, you can't copy and paste parts of applications that are IPP-protected.

![Diagram showing applications in an ACME environment can only be deployed within the ACME infrastructure, with a cross mark indicating deployment to EMCA infrastructure is not allowed due to IPP protection.](images/what-is-ipp_protected.png "IPP Protected Deployment Flow")

In this example, applications developed in an ACME environment can be deployed to any ACME environment. However, you can't deploy those applications to the EMCA infrastructure.

## For ODC

In OutSystems Developer Cloud (ODC), you don't need to transfer IPP through the IPP portal. Assets can be opened, published, and deployed in ODC Studio.
