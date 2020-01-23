---

copyright:
  years: 2020
lastupdated: "2020-01-14"

keywords: transit, gateway, ordering, getting, started

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
{:external: target="_blank_" .external}
{:term: .term}

# Getting started with IBM Cloud Transit Gateway (Beta)
{: #getting-started}

IBM Cloud™ Transit Gateway (currently in Beta) is only available to whitelisted users. Contact your IBM sales representative if you are interested in getting early access.  
{: note}

Use IBM Cloud Transit Gateway to securely connect IBM Cloud Classic and Virtual Private Cloud (VPC) infrastructures worldwide, keeping traffic within the IBM Cloud network. With Transit Gateway, organizations can define and control communications between resources on the IBM Cloud network, providing dynamic scalability, high availability, and secure, in-transit data between IBM Cloud data centers. These transit gateways are commonly implemented to support hybrid workloads, frequent data transfers, private workloads, or to ease administration of the IBM Cloud environment.
{: shortdesc}

To use the Transit Gateway capability to connect your VPCs, you must have two or more VPCs created in your IBM Cloud account. To use the Transit Gateway capability to connect your VPCs to your IBM Cloud classic infrastructure, you must have at least one VPC created in your IBM Cloud account, and your classic account must be VRF-enabled and linked to your IBM Cloud account. For more information, refer to [Linking IBMid accounts](/docs/account?topic=account-unifyingaccounts).
{: note}

To get started using IBM Cloud Transit Gateway:

1. From your browser, open the [IBM Cloud console](https://cloud.ibm.com/catalog){: external} and log in to your account.
2. Select **Networking** from the left, then click the Transit Gateway tile.

You can also access the ordering page from the [IBM Cloud catalog ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com){:new_window} by selecting the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) from the top left, then selecting **Hybrid Networking** to bring up the Direct Link page. From there, select **Transit Gateway** in the left navigation panel, then click the **Order Transit Gateway** button.
{: note}

You can configure several types of connections with Transit Gateway. Refer to the following "How To" topics for detailed information.

* [Connecting VPCs in the same region](/docs/infrastructure/transit-gateway?topic=transit-gateway-connecting-vpcs-same-region)
* [Connecting VPCs in different regions](/docs/infrastructure/transit-gateway?topic=transit-gateway-connecting-different-vpcs)
* [Connecting VPCs to your IBM Cloud classic infrastructure](/docs/infrastructure/transit-gateway?topic=transit-gateway-connecting-classic-infrastructure-vpcs)

## Routing considerations
{: #routing-considerations}

All connections to a transit gateway are connected to each other, so carefully consider all resources you want to interconnect before deciding whether local or global routing is right for each gateway.

All routing options remain within the IBM Cloud infrastructure and are optimized for security and performance.

While you have the option to edit a gateway's routing type after it is provisioned, changing the routing type from global to local requires that the gateway only connects to resources that are considered local to the location of the gateway. Refer to the "How To" section for detailed scenarios.
{: tip}

For more guidelines on creating and using transit gateways, refer to [Helpful tips](/docs/infrastructure/transit-gateway?topic=transit-gateway-helpful-tips).

## Local routing
{: #local-routing}

If you plan to use the gateway to connect resources at the same [Multi-Zone Region (MZR)](#x9774820){: term}, then local routing provides connectivity to all accessible resources within the same MZR; for example, `Dallas`.

![Local routing](images/1-aboutLocalRoutingExample.png "Local routing"){: caption="Figure 1. Simple local routing example" caption-side="bottom"}

## Global routing
{: #global-routing}

If you plan to use the gateway to connect resources between different MZRs, then global routing expands the connection capabilities to include all accessible global regions and resources.

![Global routing](images/2-aboutGlobalRoutingExample.png "Global routing"){: caption="Figure 2. Simple global routing example" caption-side="bottom"}

If you need more help getting started with IBM Cloud Transit Gateway, you can open an IBM Support case through the IBM Cloud console, or contact your IBM Cloud Sales representative.
