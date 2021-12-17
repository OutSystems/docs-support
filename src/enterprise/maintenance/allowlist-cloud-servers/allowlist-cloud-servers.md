---
summary: How to obtain the addresses of your OutSystems Cloud servers to allowlist on your firewall. Please note we recently replaced the term whitelist with allowlist across all OutSystems documentation.
tags: support-Cloud_Platform; support-Cloud_Platform-featured
---

# Allowlist your OutSystems cloud environments on your firewall

In the OutSystems Cloud you can integrate with several external services. And sometimes, those services are behind a firewall or have strict access rules. To establish a connection, you'll need to allowlist the addresses of your OutSystems Cloud environments. 
This article guides on how to find the right IP addresses to allow on your network.

## Connecting over the internet

Over the internet, OutSystems Cloud environments announce the public IP of the front-end that initiates the outgoing connection.

The OutSystems Cloud front-ends are AWS EC2 instances with [elastic IPs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html). So, they have static public IPs that won't change over time and can be allowlisted on your network.

### Obtaining the front-ends' public IPs

To get the public IPs of your environments front-ends execute these 2 steps in sequence:

1. Get the servers' hostnames.

    In Service Center access **Monitoring** > **Environment Health** and note the **Front-end Servers** name. Take that value and add ``.outsystemsenterprise.com``. In the image below the end result would be ``hostname.outsystemsenterprise.com``.

    ![](images/allowlist-cloud-servers-sc.png?width=800)


1. Resolve the hostnames to their respective public IPs.

    You can use any method or tool such as, for example, [this one](https://mxtoolbox.com/DnsLookup.aspx).

    It's important to allowlist all the IP addresses. If in Service Center (step 1) you have more than one Front-end Server you should resolve and allowlist all. Outgoing requests can originate from any of the front-end servers. And if they're not all allowlisted, some requests may be blocked.

    
    <div class="warning" markdown="1">

    When new front ends are added to an environment make sure to retrieve and allowlist its public IP. Existing integrations can be affected until you do so.

    </div>


### Common mistakes

It's important not to use the IPs obtained when resolving the environment address. For example: ``<my_production>.outsystemsenterprise.com``.   

Some of your environments have load balancers (LB) and if you resolve ``<my_production>.outsystemsenterprise.com`` what you'll get is the LB IPs.

In outgoing requests to external servers, the connection originates from the front-end servers. The load balancer isn't involved in the communication. It's only involved in incoming requests to the OutSystems environment.

Thus, the LB address isn't the correct one to allowlist. As a note, OutSystems Cloud LBs **do not** have static IP addresses.

## Connecting via VPN
 
When the external servers are not publicly accessible, you can establish a VPN connection to the OutSystems Cloud. In that case, you'll need to allowlist the full [private IP range of your OutSystems PaaS](https://success.outsystems.com/Support/Enterprise_Customers/Maintenance_and_Operations/Find_out_Internal_IP_Address_Range_of_Your_OutSystems_Cloud) on your firewall.

The **private** IP addresses **are not static** so it's important to allowlist the entire range.

