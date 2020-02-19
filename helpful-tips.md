---

copyright:
  years: 2020
lastupdated: "2020-02-12"

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

# Planning for Transit Gateway
{: #helpful-tips}

Make sure that you review the following considerations before ordering IBM Cloud Transit Gateway.
{: shortdesc}

## General considerations

* Create your transit gateway in a location that makes sense for your workload. For example, if you are connecting two `Dallas` VPCs and one `Frankfurt` VPC, creating your gateway in `Dallas` would be the most efficient for your workload.
* Name your transit gateway connections logically. If you do not specify a name when adding a network connection, the VPC name is used. Creating a gateway with multiple connections all with the same name can cause issues.
* You cannot connect a classic access VPC directly to a transit gateway. To connect the classic access VPC resources, use the {{site.data.keyword.cloud_notm}} classic infrastructure connection, and then all the resources in your classic access VPC are automatically connected.  
* When creating a transit gateway, the VPC that you want to connect to cannot already be connected to a different transit gateway in your account.
* Transit gateways and their connections can take several minutes after provisioning before they are accessible.

## Classic infrastructure connection considerations

* You can set up access to your IBM Cloud classic infrastructure with only one transit gateway in your IBM Cloud account.
* To use the transit gateway capability to connect your VPCs to an IBM Cloud classic infrastructure, you must have at least one VPC created in your IBM Cloud account, and your classic account must be enabled for virtual routing and forwarding (VRF) and linked to your IBM Cloud account. For information on enabling your account for VRF, see [Enabling VRF and service endpoints](/docs/account?topic=account-vrf-service-endpoint). For details on linking accounts, see [Linking IBMid accounts](/docs/account?topic=account-unifyingaccounts).
* All subnets of the VPC and classic network will be connected to your transit gateway, so it's important that the subnets do not overlap. When creating VPCs that are intended to be connected to a transit gateway, create them with non-overlapping prefixes and unique subnets. All subnets in a VPC are shared in the classic infrastructure VRF, which uses IP addresses in the `10.0.0.0/8` space. To avoid IP address conflicts, do not use IP addresses in the `10.0.0.0/14`, `10.200.0.0/14`, `10.198.0.0/15`, and `10.254.0.0/16` blocks. To view a list of your classic infrastructure subnets, click **View all subnets**  on the ordering page.
* Classic VSIs will likely have both a private (eth0) and a public (eth1) network interface. Currently, the routing tables for these interfaces point the default gateway to the public interface (eth1). You might have to add routing entries to route the subnets from other VPCs through the private interface.

## Routing considerations

* All connections to a transit gateway are connected to each other, so carefully consider all resources you want to interconnect before deciding whether local or global routing is right for each gateway.

   All routing options remain within the IBM Cloud infrastructure and are optimized for security and performance.
   {: note}
   * If you plan to use the gateway to connect resources at the same Multi-Zone Region (MZR), use local routing to provide connectivity to all accessible resources within the same MZR; for example, `Dallas`.
   ![Local routing](images/1-aboutLocalRoutingExample.png "Local routing"){: caption="Figure 1. Simple local routing example" caption-side="bottom"}
   * If you plan to use the gateway to connect resources between different MZRs, use global routing and expand the connection capabilities to include all accessible global regions and resources.
   ![Global routing](images/2-aboutGlobalRoutingExample.png "Global routing"){: caption="Figure 2. Simple global routing example" caption-side="bottom"}

* You can edit a gateway's routing type after it is provisioned, however, to change the routing type from global to local, you must first remove any global connections (that is, connections that are not in the same location as the gateway). Note that connections to the IBM Cloud Classic Infrastructure are always considered local.
