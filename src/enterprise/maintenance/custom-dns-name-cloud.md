---
summary:
locale: en-us
guid: 66ca5c48-0df6-45d5-9e0a-c7db3d3e0c01
app_type: traditional web apps, mobile apps, reactive web apps
---

# Custom DNS names for OutSystems Cloud servers

OutSystems provisions environments in the OutSystems Cloud on your behalf, and assigns a specific DNS name in the *.outsystemsenterprise.com domain to each environment. 

However, your users often expect and prefer to access an application address in your own domain, and this configuration can only be performed on your DNS servers.

## How to configure your DNS 

Create CNAME records in your DNS servers pointing to the servers in the *.outsystemsenterprise.com domain. Then, [upload your own SSL certificates to the OutSystems Cloud](https://success.outsystems.com/Documentation/11/Setup_and_maintain_your_OutSystems_infrastructure/Setting_Up_OutSystems/Use_your_SSL_domain_in_OutSystems_Cloud).

<div class="warning" markdown="1">

The DNS of the OutSystems servers redirects to a load balancer, with an address like *.elb.amazonaws.com. But the address of the load balancer is subject to change. You can't use the load balancer address in your DNS records.

</div>

The diagram below shows the correct configuration in green:

![ ](images/custom-dns-name-cloud_0.png)

