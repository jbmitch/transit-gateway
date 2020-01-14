---

copyright:
  years: 2020
lastupdated: "2020-01-14"

keywords: transit, gateway, help, tips, connections, provision

subcollection: transit-gateway

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank_"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}
{:term: .term}

# Helpful tips
{: #helpful-tips}

There are several useful tips for working with IBM Cloud™ Transit Gateway to be aware of.
{: shortdesc}

* Always create your transit gateway in a location that makes sense for your workload. For example, if you are connecting two `Dallas` VPCs and one `Frankfurt` VPC, creating your gateway in `Dallas` would be the most efficient for your workload.

* Name your connections logically. If you do not specify VPC connection names when creating a connection on the IBM Cloud console, default names are selected for you. Creating multiple connections with default names could generate the same name for more than one connection, which can cause issues.

* Transit gateways and their connections can take several minutes after provisioning before they are accessible.

* Classic VSIs will likely have both a private (eth0) and a public (eth1) network interface. Currently, the routing tables for these interfaces point the default gateway to the public interface (eth1). You might have to add routing entries to route the subnets from other VPCs through the private interface.

* To use the transit gateway capability with your classic infrastructure, your account must be enabled for virtual routing and forwarding (VRF). For information on enabling your account for VRF, refer to [Enabling VRF and service endpoints](/docs/account?topic=account-vrf-service-endpoint).
