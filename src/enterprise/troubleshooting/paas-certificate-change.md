---
summary:
---

# OutSystems PaaS certificate change - May 2020

## Overview

OutSystems PaaS certificate *.outsystemsenterprise.com will reach its expiration date on May 8, 2020. Due to this, OutSystems needs to install a new certificate during April 2020.

The new certificate will remain valid until November 3, 2021.

This article contains a FAQ for possible questions that you, as a customer, may have about the certificate change.

## FAQs

**Q: I am using SSL Pinning Plugin on my mobile apps. Do I need to do anything?**

As long as you are "pinning" your mobile applications on your own certificate this operation will not impact your mobile applications.

However, if you are "pinning" your mobile apps on the *.outsystemsenterprise.com certificate, this rotation will cause your applications to stop connecting to the cloud environment. In order to avoid this situation, you can add the following fingerprint which represents the certificate that will be installed in April 2020 to the SSL Pinning component.

                    Fingerprint: wBQyMhRmymJ2b9XBo4nHjBqE5KGTT0LUPiNk6rLUSYs=

Please note that you should keep the current fingerprint and add the new one so that your application continues to function as expected before and after the certificate renewal. For more information on how to add a new fingerprint to your SSL Pinning component please visit the component official documentation [here](https://www.outsystems.com/forge/Component_Documentation.aspx?ProjectId=1873&ProjectName=ssl-pinning-plugin).

**Q: I am using my own domain certificate in my cloud environment. Does this operation have any impact on it?**

No. This operation will not impact in any way your certificate.

**Q: Does this operation present a risk or threat to the data present on my cloud environments?**

No. This operation does not present any risk or threat to the data present in your cloud environments.

**Q: Do I need to do anything after the new certificate is installed?**

No actions are required from your side.

**Q: Can I opt-out from or postpone this certificate renewal?**

Security best practices indicate that expired certificates should not be presented to any device. As such, you cannot opt-out or postpone this certificate renewal.

**Q: When will the next certificate renewal occur?**

Since the new certificate will expire on November 3rd 2021, OutSystems expects to perform a new certificate installation during October 2021.

