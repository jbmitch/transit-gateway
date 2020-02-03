---

copyright:
  years: 2020
lastupdated: "2020-01-28"

keywords: faq, faqs, questions, transit, gateway, vpc, direct link

subcollection: transit-gateway

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank_"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}
{:faq: data-hd-content-type='faq'}
{:note: .note}
{:important: .important}
{:term: .term}

# FAQs for IBM Cloud Transit Gateway
{: #faqs-for-transit-gateway}

These frequently asked questions can help you when working with the {{site.data.keyword.tg_full}}.
{: shortdesc}

## What are the differences between IBM Cloud Transit Gatewayand IBM Cloud Direct Link?

The [IBM Cloud™ Direct Link](/docs/infrastructure/direct-link?topic=direct-link-overview-of-direct-link-offerings) offerings provide connectivity from an external source into a customer's IBM Cloud private network. The {{site.data.keyword.tg_full_notm}}offering provides interconnectivity between resources within a customer's IBM Cloud private network.

## Can I create more than one transit gateway in my account?

Yes. Each transit gateway (and its connections) will be securely isolated from other transit gateways in your account.

## Can I create more than two connections for a given transit gateway?

Yes. Keep in mind that all connections to a transit gateway are connected to each other, so carefully consider all resources you want to interconnect before deciding whether local or global routing is right for each transit gateway. Refer to the "How To" section for detailed scenarios.

## Classic access VPCs cannot be attached to a transit gateway. How can I connect and access classic resources in those VPCs?

Although [classic access VPCs](/docs/vpc?topic=vpc-setting-up-access-to-classic-infrastructure) cannot be attached to a transit gateway, access to classic access VPC resources can be achieved by adding the [IBM Cloud classic infrastructure connection](/docs/infrastructure/transit-gateway?topic=transit-gateway-connecting-classic-infrastructure-vpcs) to a transit gateway.

## How can "VPC Peering" be achieved on IBM Cloud?

{{site.data.keyword.tg_full_notm}}can be used to connect multiple VPCs to each other. As such, connecting/peering two VPCs is just a part of the functionality that the transit gateway service offers. IBM Cloud does not provide a standalone VPC peering service or capability.

## Can I connect a VPN or direct link to a transit gateway?

These capabilities do not exist today. However, they might be offered in the future.

## Can I create a global transit network using the IBM Cloud Transit Gateway?

{{site.data.keyword.tg_full_notm}}enables standard IP routing between networks (for example, global VPCs) that are connected to it. Additional functionality can be added by configuring IBM or third-party virtual network functions, such as VPN, NAT, and firewalls, within one or more of the interconnected networks (for instance, using the "Transit VPC" concept).

## What is next for IBM Cloud Transit Gateway?

{{site.data.keyword.tg_full_notm}}will include monitoring and activity tracking capabilities, as well as the ability to connect networks across different IBM Cloud accounts.
