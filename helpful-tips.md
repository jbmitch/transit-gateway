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

* Create your transit gateway in a location that makes sense for your workload. For example, if you are connecting two VPCs in the `us-south` (Dallas) region and one VPC in the `eu-de` (Frankfurt) region, creating your gateway in `us-south` region would be the most efficient for your workload.
* Be descriptive when naming your transit gateway connections. If you do not specify a name when adding a connection, the VPC name is used by default. 
* You cannot connect a [classic access VPC](/docs/vpc?topic=vpc-setting-up-access-to-classic-infrastructure) directly to a transit gateway. To connect the classic resources, use the {{site.data.keyword.cloud_notm}} classic infrastructure connection, and then all the resources in your classic access VPC are automatically connected.  
* Even though you can have multiple transit gateways per account, a VPC or classic infrastructure can only be added to one transit gateway.
* Transit gateways and their connections can take several minutes after provisioning before they are available.
* All subnets of the VPC and classic network will be connected to the transit gateway, so it's important that the subnets do not overlap. When creating VPCs that are intended to be connected to a transit gateway, make sure to create the VPCs with non-overlapping prefixes and unique subnets. 

## Classic infrastructure connection considerations

* To use a transit gateway to connect your VPCs to your IBM Cloud classic infrastructure,  your classic account must be enabled for virtual routing and forwarding (VRF) and linked to your IBM Cloud account. For information on enabling your account for VRF, see [Enabling VRF and service endpoints](/docs/account?topic=account-vrf-service-endpoint). For details on linking accounts, see [Linking IBMid accounts](/docs/account?topic=account-unifyingaccounts).
* All subnets in a VPC are shared in the classic infrastructure VRF, which uses IP addresses in the `10.0.0.0/8` space. To avoid IP address conflicts, do not use IP addresses in your VPCs in the `10.0.0.0/14`, `10.200.0.0/14`, `10.198.0.0/15`, and `10.254.0.0/16` blocks. To view a list of your classic infrastructure subnets, see [View all subnets](/docs/subnets?topic=subnets-view-all-subnets){: external}.
* Classic VSIs will likely have both a private (eth0) and a public (eth1) network interface. Currently, the routing tables for these interfaces point the default gateway to the public interface (eth1). You might have to add routing entries to route the subnets from other VPCs through the private interface.
* All of your IBM Cloud classic infrastructure networks across MZRs are accessible through this connection, regardless of the transit gateway’s local or global routing setting. Note that classic infrastructure resources that are not located in an MZR location will not have connectivity through the transit gateway.

## Routing considerations

* All connections to a transit gateway are connected to each other, so carefully consider all resources you want to interconnect before deciding whether local or global routing is right for each gateway.
   All routing options remain within the IBM Cloud infrastructure and are optimized for security and performance.
   {: note}
* If you plan to use the gateway to connect resources in the same multi-zone region (MZR), use local routing to provide connectivity to all accessible resources within the same MZR; for example, `us-south` (Dallas).
   ![Local routing](images/1-aboutLocalRoutingExample.png "Local routing"){: caption="Figure 1. Simple local routing example" caption-side="bottom"}
* If you plan to use the gateway to connect resources between different MZRs, use global routing to expand the connection capabilities to include all accessible global regions and resources.
   ![Global routing](images/2-aboutGlobalRoutingExample.png "Global routing"){: caption="Figure 2. Simple global routing example" caption-side="bottom"}
* You can edit a gateway's routing type after it is provisioned, however, to change the routing type from global to local, you must first remove any global connections (that is, connections that are not in the same location as the gateway). Note that connections to the IBM Cloud classic infrastructure are always considered local.
