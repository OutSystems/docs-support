---
summary: Since most web browsers will no longer trust certificates with a validity that exceeds one year, OutSystems will rotate the outsystemsenterprise.com certificate. This document provides further details about the operation and how it may impact you. It's especially relevant if you're using SSL pinning on your mobile apps.
---

# OutSystems Cloud certificate rotation

## Overview

Most web browser vendors shared they'll be distrusting certificates with a validity that exceeds one year.

To accommodate these changes, OutSystems will be rotating the `outsystemsenterprise.com` certificate, starting late September 2020, by issuing a new certificate every year.

This article addresses questions you may have about the certificate change.

## FAQs

### I am using SSL Pinning plugin on my mobile apps. Do I need to do anything?

As long as you are pinning your mobile applications to your own certificate, this operation won't impact your mobile apps.

However, if you are pinning your mobile apps on the `outsystemsenterprise.com`.com certificate, this rotation will cause your applications to stop connecting to the OutSystems Cloud environment. 

If you're already using the `outsystemsenterprise.com` certificate for SSL Pinning:

* To avoid any downtime, take this opportunity to [use your own certificate](https://success.outsystems.com/Support/Enterprise_Customers/Installation/Use_your_SSL_domain_in_OutSystems_Cloud), for which you have the certificate keys, and use your certificate fingerprint on your mobile apps.
* In the transition process it's possible to add the following fingerprint that represents the certificate that will be installed in late September/early October 2020 to the SSL Pinning component.
    ```Fingerprint: U6vSutzZQ4RuSJwV2i0vUO6qtGcX5vGltvpGnNd5BEg=```
* Make sure to plan and switch to use your own SSL certificate for SSL Pinning.


<div class="warning" markdown="1">

Please beware that OutSystems **will no longer** provide the `outsystemsenterprise.com` certificate fingerprint in advance for future certificate changes. For this reason, the `outsystemsenterprise.com` should **never** be used for SSL Pinning.

</div>


Note that you should keep the current fingerprint and add the new one so that your app continues to function as expected before and after the certificate renewal. For more information on how to add a new fingerprint to your SSL Pinning component please visit the component official documentation [here](https://www.outsystems.com/forge/Component_Documentation.aspx?ProjectId=1873&ProjectName=ssl-pinning-plugin).

### I am using my own domain certificate in my OutSystems Cloud environments. Will this operation have any impact?

No. This operation won't impact in any way your certificate.

### Does this operation present a risk or threat to the data present on my cloud environments?

No. This operation doesn't present any risk or threat to the data present in your cloud environments.

### Do I need to do anything after the new certificate is installed?

If you're using SSL Pinning in mobile apps, please check the recommendations above. Apart from that, no further actions are required from your side.

### Can I opt-out from the certificate renewal?

No.

### When will the next certificate renewal occur?

As described in [this article](https://success.outsystems.com/Support/Security/outsystems_certificate_management) OutSystems will communicate the rotation whenever possible, however **OutSystems reserves the right to rotate the certificate without prior communication or in short notice**. Shall you depend on a specific definition of the `outsystemsenterprise.com` certificate, switch to [use your own certificate](https://success.outsystems.com/Support/Enterprise_Customers/Installation/Use_your_SSL_domain_in_OutSystems_Cloud) and remove that dependency.
