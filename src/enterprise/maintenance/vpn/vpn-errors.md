---
summary: Check here the possible errors that you can get when creating a VPN connection to your OutSystems Cloud and how to proceed for each case.
tags:
---

# Possible errors when setting up a VPN to your OutSystems Cloud

During the process to [set up a VPN to your OutSystems Cloud](vpn-support.md), you start by requesting the creation of new a VPN (virtual private network) in the LifeTime console. You can also change the internal IP range of your static VPN in self-service mode in the LifeTime console.

This article describes the possible errors that you can get when [creating a new VPN connection](vpn-support.md#request-vpn) or [changing the internal IP range of a static VPN](vpn-support.md#change-vpn-route) in the LifeTime console, and the guidelines on how to proceed for each case.

## Errors description

Message
:   `<ip address> is not a valid public IP address.`

Cause
:   The **Internet gateway public IP** address you provided isn't valid, or isn't a public IP.

Recommendation
:   Make sure you provide a valid **Internet gateway public IP** address.

---

Message
:   `Maximum number of VPNs has been reached.`

Cause
:   You have reached the maximum of five VPN connections to your OutSystems Cloud. You can't create more VPN connections.

Recommendation
:   Consider managing the connectivity between your data centers and the OutSystems Cloud [using an AWS Transit Gateway](../connect-tgw.md).

---

Message
:   `A VPN already exists in this infrastructure with the public IP address <ip addess>.`

Cause
:   The **Internet gateway public IP** address you provided is already in use by another VPN connection in the infrastructure. You can't use the same Internet gateway public IP for different VPN connections.

Recommendation
:   Make sure you provide an **Internet gateway public IP** address that isn't in use by another VPN connection in the infrastructure. You can check the existing VPN connections in your LifeTime console, under **Environments > Options > VPN Management**. If you are providing the same Internet gateway public IP as an attempt to establish redundancy, see the alternatives in [Set up a VPN to your OutSystems Cloud](vpn-support.md).

---

Message
:   `This infrastructure is already connected to a Transit Gateway. It's not possible to create a VPN.`

Cause
:   You can't create a VPN connection because you are using an AWS Transit Gateway to connect to your OutSystems Cloud.

Recommendation
:   Instead of creating a new VPN connection, connect the target VPN location [using your AWS Transit Gateway](../connect-tgw.md).

---

Message
:   `The chosen ASN value <ASN value> is already in use.`

Cause
:   The ASN value you provided is already in use by another VPN connection in the infrastructure.

Recommendation
:   Make sure you provide an ASN value that isn't in use by another VPN connection in the infrastructure.

---

Message
:   `The chosen ASN value <ASN value> is invalid. The ASN value must be between 0 and 65535.`

Cause
:   The ASN value you provided is out of the allowed range from 0 to 65535.

Recommendation
:   Make sure you provide an ASN value within the range from 0 to 65535.

---

Message
:   `The chosen ASN value <ASN value> is reserved by Amazon.`

Cause
:   The ASN value you provided is reserved by Amazon.

Recommendation
:   Use a different ASN value within the range from 0 to 65535.

---

Message
:   `The chosen ASN value <ASN value>, can't be used because it is a reserved value.`

Cause
:   The ASN value you provided is a reserved ASN.

Recommendation
:   Use a different ASN value within the range from 0 to 65535.

---

Message
:   `The route <IP range> must have a valid IP range, for example 10.10.1.0/24`

Cause
:   The **Internal network IP range** you provided is invalid.

Recommendation
:   Make sure you provide a valid **Internal network IP range**. Example: `10.10.1.0/24`.

---

Message
:   `0.0.0.0/0 is not a valid IP range for VPN routes.`

Cause
:   You can't set `0.0.0.0/0` as the **Internal network IP range**. `0.0.0.0/0` is a special IP range, which effectively means all traffic is sent through this route, including the internal traffic of your OutSystems Cloud VPC. Therefore, this is an invalid configuration.

Recommendation
:   Make sure you provide an **Internal network IP range** different from `0.0.0.0/0`.

---

Message
:   `The route inserted cannot be added to the VPN static routes since it will overlap with the IP range <IP range>, added before.`

Cause
:   The **Internal network IP range** you provided overlaps with an existing route.

Recommendation
:   Make sure you provide an **Internal network IP range** that doesn't overlap with an existing route. You can check the existing routes in your LifeTime console, under **Environments > Options > VPN Management**.

---

Message
:   `The IP range for the VPN Route <IP range> overlaps the reserved private IP range <OutSystems Cloud VPC range>.`

Cause
:   The **Internal network IP range** you provided overlaps with the private IP range of your OutSystems Cloud VPC, which is an invalid configuration for the VPN connection.

Recommendation
:   Make sure you provide an **Internal network IP range** that doesn't overlap with the private IP range of your OutSystems Cloud VPC.

---

Message
:   `It’s not possible to create the VPN connection now. Please try again later.`

Cause
:   It's not possible to create or edit the VPN connection at the moment because there's another operation currently running in the infrastructure.

Recommendation
:   Try to request the creation or edition of your VPN later. If the problem persists, [contact OutSystems Support](https://success.outsystems.com/Support/Enterprise_Customers/OutSystems_Support/02_How_to_Open_a_Support_Case).

---

Message
:   `It is not possible to add <N> routes. The maximum number of routes is <Max> and there are only <N> available.`

Cause
:   You have reached the maximum of 20 routes for your VPN connections. You can't add more routes.

Recommendation
:   Don't use this route, or modify the existing routes to accommodate the required IP range. You can check the existing routes in your LifeTime console, under **Environments > Options > VPN Management**. Alternatively, consider managing the connectivity between your data centers and the OutSystems Cloud [using an AWS Transit Gateway](../connect-tgw.md).
