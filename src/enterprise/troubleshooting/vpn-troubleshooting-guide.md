---
summary: Guide to establish a stable VPN connection to OutSystems PaaS
tags: support-Cloud_Platform
locale: en-us
guid: eee4da25-8b13-4bac-b8e7-dae4ece8c3ec
app_type: traditional web apps, mobile apps, reactive web apps
platform-version: o11
figma:
---
# VPN connectivity and troubleshooting guide

## Overview

OutSystems VPN is a fully automated and orchestrated service, with a defined set of possible configurations.

After completing the initial [configuration steps](../maintenance/vpn/vpn-support.md#configure-gateway), should you experience any issues, you'll need to perform some troubleshooting steps and take actions. This article aims to assist you in that process.

## Requirements

Before starting with the VPN configuration itself, it's mandatory that your VPN Device/Firewall meets all the requirements to establish a VPN connection between the OutSystems Cloud and your private network. OutSystems accepts what customers propose as long as it meets the [OutSystems VPN Requirements](../maintenance/vpn/vpn-support.md#configure-gateway).

## Naming resolution solutions (DNS resolution)

While setting up the VPN, OutSystems provisions internal DNS servers that should be used to:

1. Connect to your environments via VPN using the default public domain names instead of its private IP addresses. This ensures the usage of the internal load balancers to connect to your environment while maintaining the connection via VPN. To enable this, a conditional forwarder must be set on your network with the following information:

    * DNS Servers: As detailed in the initial VPN configuration

    * Protocol / Port : UDP/TCP 53

    * Domain to be resolved: outsystemsenterprise.com

1. Resolve your network's internal domain names (for those hostnames that are local to your network and aren't publicly accessible) using OutSystems Cloud DNS service. When this is necessary, you may request to configure a conditional forwarder. When opting to for this service, you'll need to provide the following details:

    * Private IP address(es) of the onsite DNS server(s).

    * Port and protocol (UDP/TCP) of the onsite DNS server(s).

    * The internal domain you wish to resolve from the Cloud environments (example: company.local).

1. To retrieve the private IP address of the database server, we recommend using OutSystems DNS service. You can configure your DNS to connect to the following IP addresses that will resolve the database server's private address:

    * DNS Servers: As detailed in the initial VPN configuration

    * Protocol/Port: UDP/TCP 53

    * Domain to be resolved: xxxx.rds.amazonaws.com (provided in the database access configuration).


## Establishing a stable connection

To establish a stable VPN connection to OutSystems Cloud you need to take in consideration the following:

1. Ensure there is constant inbound traffic from your network to the VPN tunnels. OutSystems Cloud VPN can only act as a "responder", meaning that your network side should always be the traffic "initiator" to activate the VPN tunnels and keep the connection active.

1. OutSystems VPN can only support a single pair (inbound/outbound) of security associations (SAs). This means that if you have more than one internal subnet to propose to the OutSystems Cloud, you’ll need to accommodate those to a one single IP range or use "any" case (0.0.0.0/0). You can then implement firewall ACL rules to limit the number of IP addresses from reaching your internal network in case you have restricted security policies.

    * For example, if you are using **policy-based** routing, verify that you have correctly defined the source and destination networks in your encryption domain to one single Security Association (SA).

    * Likewise, if your VPN tunnels are **route-based**, confirm that you have correctly configured one single route pair (inbound/outbound) in your Phase 2 IPSEC SA.

1. When both tunnels are active for failover purposes, ensure that the VPN device supports asymmetric routing, since it can receive traffic from the primary tunnel and send the response back through the secondary one. This behavior can't be changed and to avoid this, you may use one of the following scenarios:

    * **VPN Static Routes**: use an active/passive setup where only 1 tunnel is active/UP per VPN connection at a time. This ensures that both sides use the same tunnel to route traffic between the networks. For failover, use Dead Peer Detection (DPD) with VPN monitoring to track the liveliness of the active tunnel. Should a failure be detected, the failover should be triggered to bring up the second tunnel UP and route traffic over it while keeping the primary tunnel down.

    * **Dynamic VPNs (BGP)**: make use of the AS-PATH prepending or BGP Local Preference on one of the tunnels to influence which tunnel is used to send traffic towards the OutSystems VPN.

## Troubleshooting the VPN connection

If after all the required configurations and recommendations there is still any instability or connectivity issues with the VPN, please revise the following list of common situations and their respective solutions.

### Common reasons for VPN tunnel inactivity or instability issues

* Problems with Internet Protocol Security (IPSec) Dead Peer Detection (DPD) monitoring.

* Idle timeouts due to low traffic on a VPN Tunnel or vendor-specific Firewall device configuration issues.

OutSystems VPN has a mechanism called DPD that validates periodically the tunnel activity and if your network doesn't respond to three successive DPD requests, the peer is considered dead and by consequence, the tunnel is automatically closed.

#### Solution

Check the Dead Peer Detection (DPD) settings and ensure that:

* It's configured to [receive and respond to DPD messages](https://docs.aws.amazon.com/vpc/latest/adminguide/Introduction.html#FirewallRules).
* It's not too busy to respond to DPD messages from OutSystems VPN peers.
* It isn't rated limiting DPD messages due to IPS features enabled in the firewall.

### Tunnel drop every 60 minutes while using IKEv2

#### Solution

Change the Phase 2 lifetime setting to 51 minutes instead of 60 minutes. This is a known pattern that's identified and this workaround mitigates the issue.

#### Related articles

* [How do I troubleshoot VPN tunnel inactivity or instability on my customer gateway device?](https://aws.amazon.com/pt/premiumsupport/knowledge-center/vpn-tunnel-instability-inactivity/ "How do I troubleshoot VPN tunnel inactivity or instability on my customer gateway device?")

### Pinging front-end servers or databases

ICMP requests to the OutSystems Cloud environment front-ends and database servers aren't allowed for security reasons.

OutSystems security rules only allow ICMP requests (ping) to the OutSystems Cloud DNS servers. All the other servers of the OutSystems Cloud won't reply back to ICMP requests.

#### Solution

You can ping the OutSystems Cloud DNS servers to keep-alive the VPN connection or to test the connectivity between both sites.

`ping -t  <DNS_SERVER_PRIVATE_IP_ADDRESS>`

You can check the **Common issues testing VPN connectivity** section down below for more details.

### Common issues testing VPN connectivity

By design, and for security reasons direct access to the environment front-end servers isn't allowed.

We force traffic over the internal load balancers that resolve to non-static IP addresses, which then redirect the traffic to the environment front-end machines.

#### Solution 1

1. **Ping** directly the OutSystems Cloud DNS private IP address(es) from your private network that has access to the VPN. This information is provided on the initial VPN configuration setup.

    `$ ping  <DNS_SERVER_PRIVATE_IP_ADDRESS>`

1. Run a **traceroute** utility from your internal network to a DNS private IP address or domain:

    * If the output stops at an IP address associated with your internal network, verify that the routing path to your VPN edge device is correct.

    * If the output reaches your Firewall device but not the private IP address of the DNS Server, check your VPN device settings, namely if the configuration itself, policies NAT settings are correct.

    `$ traceroute  <DNS_SERVER_PRIVATE_IP_ADDRESS>`

#### Solution 2

<div class="info" markdown="1">

For this option, ensure that the DNS conditional forwarder mentioned in the requirements section is configured beforehand.
</div>

1. Perform a **telnet** session to one of the Fully Qualified Domain Names (FQDNs) of the OutSystems Cloud environments (outsystemsenterprise.com) over TCP/IP network protocol on port(s) 80 and 443. For Sentry editions allow only port 443.

    `$ telnet  example-dev.outsystemsenterprise.com 443`

1. Perform a **nslookup** command to one of the FQDNs of the OutSystems Cloud environments to check if the name resolution works and resolve the domain name(s) to a private IP address(es).

    `$ nslookup  example-dev.outsystemsenterprise.com`

### Pinging OutSystems Cloud DNS servers

As soon as the VPN is created, the DNS servers become available to be queried for DNS and to respond to ICMP requests.

By design, the OutSystems Cloud DNS servers respond to ICMP requests as long as your network's source IP address belongs to the routes configured in the VPN.

#### Solution

You'll need to ensure your network's servers are reachable from your internal network and allow ICMP requests. For that, verify your firewall settings and/or routing requirements (according to the initial communication email you received on the VPN setup).

Your network team should be able to help you with this topic.

### Issues connecting to an external database

OutSystems Cloud architecture allows all outbound traffic by design, and only filters inbound rules to the front-end machines. Therefore, you should be able to connect without issues to a database, server, or web service within your network.

#### Solution

If you can't connect from inside your VPN, you'll need to check with your network team your internal firewall settings and validate if your inbound rules are allowing the full [internal IP range of your OutSystems cloud](../maintenance/ip-range-cloud.md).

Your network team should be able to help you with this topic.

### How can I connect to my OutSystems Cloud environments from my internal network?

OutSystems Cloud is a public cloud, meaning that by default the environment hostnames resolve to public addresses and outside of VPN connection. So that you can use the public hostnames, your internal network must be configured to be able to resolve them.

#### Solution

1. You'll need to set up a conditional forwarder in your internal DNS servers as detailed on the communication email you received when the VPN was set up. This means that you should use OutSystems Cloud DNS servers as conditional forwarders for the main domain name (*.outsystemsenterprise.com).

1. Revise the conditional forwarder setting on your DNS server to understand if it's configured properly.

1. Ensure that you are allowing the protocol UDP and port 53 on your side.

Your network team should be able to help you with this topic.

### Why do I need to allow the full internal IP range of OutSystems Cloud in my firewall?

The private IP addresses of the internal load balancers aren't static and may change frequently due to security reasons. This behavior can't change. Direct access to the front-end servers isn't allowed, so all traffic should come from load balancers to the front-end machines.

In addition, the private IP addresses of the database servers change upon maintenance.

#### Solution

Allow the full [internal IP range of your OutSystems Cloud](../maintenance/ip-range-cloud.md) to guarantee that you'll be able to reach the servers even when its private IP changes.

Your network team should be able to help you with this topic.

### Retrieving the front-end's private IP address(es)

OutSystems doesn't provide direct visibility about the private IP addresses of the front-end servers.

#### Solution

You can check our [documentation on how to obtain the IP range](../maintenance/ip-range-cloud.md) instead.

### Typical reasons for the VPN tunnel phase 1 IKE negotiation to fail

When setting up the OutSystems VPN, the Internet Key Exchange (IKE) phase of the configuration fails.

#### Solution

1. Check the following VPN settings and verify that you:

    * Meet all the Phase 1 OutSystems VPN Requirements.

    * Set the IKE (phase 1) lifetime to 28800 seconds (480 minutes or 8 hours).

    * Configured the VPN device with the correct pre-shared key (PSK) provided In the configuration file.

    * You can ping the OutSystems VPN endpoints from your firewall device.

1. If your VPN device endpoint is behind a network address translation (NAT), be sure that:

    * IKE traffic leaving your network is sourced from your configured peer IP address on UDP port 500. To test this setting, disable NAT traversal on your customer gateway device.

    * UDP packets on port 500 (and port 4500, if you're using NAT traversal) are allowed to pass between your network and OutSystems VPN endpoints.

    * Your internet service provider (ISP) isn't blocking UDP ports 500 and 4500.

Your network team should be able to help you with this topic.

### VPN tunnel phase 2 internet protocol security (IPsec) fails to negotiate

#### Solution

Check the following VPN settings and ensure that:

1. Meet all the Phase 1 OutSystems VPN requirements.

1. Encapsulating Security Payload (ESP) protocol 50 isn't blocked (inbound/outbound).

1. The security association lifetime is equal or lower than 3600 seconds (60 minutes).

1. There are no Firewall ACLs interfering with IPsec traffic.

1. Perfect forward secrecy (PFS) is enabled.

1. If you are using policy-based routing, verify that you have correctly defined the source and destination networks in your encryption domain.

Your network team should be able to help you with this topic.

#### Related articles

* [VPN Tunnel Phase 2 IPsec](https://aws.amazon.com/pt/premiumsupport/knowledge-center/vpn-tunnel-phase-2-ipsec/ "VPN Tunnel Phase 2 IPsec")
  
* [Your Customer Gateway](http://docs.aws.amazon.com/AmazonVPC/latest/NetworkAdminGuide/Introduction.html "Your Customer Gateway")

### Can OutSystems reset the tunnels to bring the VPN up again?

It wouldn't solve the underlying issue. OutSystems VPN acts as a "responder", and can't initiate traffic or reset the tunnels to bring the connection UP.

Your network should initiate the VPN tunnels by generating interesting traffic or by activating a keep-alive mechanism to activate the tunnels and maintain the connection alive.

#### Solution 1

Configure a keep-alive feature on your VPN device. Some firewalls don't have the keep-alive feature, so you'll need to use a continuous ping instead (Solution 2).

#### Solution 2

Perform a continuous ping every 5 seconds from a set of your internal servers to one of DNS Server's private IP addresses provided on the initial configuration setup communication.

Your network team should be able to help you with this topic.

#### Related articles

* [VPN Inactivity](https://aws.amazon.com/pt/premiumsupport/knowledge-center/vpn-tunnel-instability-inactivity/ "VPN Inactivity")

### Issues using the VPN configuration file

OutSystems provides a configuration file that should be enough to perform the configuration and activate the VPN tunnels.

However, there are some cases where this information can be not very straightforward or any device software version changes or updates which might difficult the setup or the connection troubleshooting.

#### Solution 1

Check the list of numerous configuration examples for the most common VPN devices:

* For [Static Routing](https://docs.aws.amazon.com/vpn/latest/s2svpn/cgw-static-routing-examples.html "Static Routing")
* For [Dynamic (BGP) Routing](https://docs.aws.amazon.com/vpn/latest/s2svpn/cgw-dynamic-routing-examples.html "Dynamic (BGP) Routing")

#### Solution 2

See specific [troubleshooting guides](https://docs.aws.amazon.com/vpn/latest/s2svpn/Troubleshooting.html "troubleshooting guides") for the most common VPN devices.

Your network team should be able to help you with this topic.

#### Related articles

* [Troubleshooting](https://docs.aws.amazon.com/vpn/latest/s2svpn/Troubleshooting.html "Troubleshooting")
* [Checkpoint and Static Routing](https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit_doGoviewsolutiondetails=&solutionid=sk100726 "Checkpoint and Static Routing")
* [Checkpoint (non-VTI) using Static Routing](https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit_doGoviewsolutiondetails=&solutionid=sk113840 "Checkpoint (non-VTI) using Static Routing")
* [Connect OutSystems VPN to Azure](https://cloudmonix.com/blog/connect-amazon-vpc-to-azure/ "Connect OutSystems VPN to Azure")

### The internal IP range of my on-premises network changed and now I can’t access OutSystems Cloud environments

If the internal IP range of your on-premises network that accesses the VPN changed (for example, because your network team changed the internal IP range or because you use dynamic VPN), you won’t be able to access the OutSystems Cloud environments from the new IP range, because OutSystems security groups are configured to the previous IP range.

#### Solution 1

If your VPN uses **static** routing, make sure you [change the internal IP range of your VPN in LifeTime](../maintenance/vpn/vpn-support.md#change-vpn-route) (applies only to LifeTime Management Console 11.7.0 or later).

#### Solution 2

If your VPN uses **dynamic** routing, or your LifeTime version still doesn't support changing static VPN routing in self-service mode, [open a support case](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/02_How_to_Open_a_Support_Case) and ensure to include the new IP range of your on-premises network. OutSystems will then change the security groups according to your new IP range.

## Further assistance

Still not working? If the issue persists, [contact OutSystems Support](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/01_Contact_OutSystems_technical_support "contact OutSystems Support").
