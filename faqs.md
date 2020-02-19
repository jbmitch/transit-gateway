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
{:support: data-reuse='support'}

# FAQs for IBM Cloud Transit Gateway
{: #faqs-for-transit-gateway}

These frequently asked questions can help you when working with the {{site.data.keyword.tg_full}}.
{: shortdesc}

## What are the differences between IBM Cloud Transit Gateway and IBM Cloud Direct Link?
{: #differences}
{: faq}
{: support}

The [IBM Cloud™ Direct Link](/docs/dl?topic=dl-get-started-with-ibm-cloud-dl) offerings provide connectivity from an external source into a customer's {{site.data.keyword.cloud_notm}} private network. The {{site.data.keyword.tg_full_notm}} offering provides interconnectivity between resources within a customer's {{site.data.keyword.cloud_notm}} private network.

## Can I create more than one transit gateway in my account?
{: #gateways}
{: faq}
{: support}

Yes. Each transit gateway (and its connections) are securely isolated from other transit gateways in your account.

## Can I create more than two connections for a given transit gateway?
{: #connections}
{: faq}
{: support}

Yes. Keep in mind that all of a transit gateway's network connections are interconnected, so carefully consider all resources you want to connect. Make sure each connection receives a unique name in the gateway, and that you choose the appropriate routing type (local or global) based on the location of the connections.

## Classic access VPCs cannot be attached to a transit gateway. How can I connect and access classic resources in those VPCs?
{: #classic-resources}
{: faq}
{: support}

Although [classic access VPCs](/docs/vpc?topic=vpc-setting-up-access-to-classic-infrastructure) cannot be attached to a transit gateway, access to classic access VPC resources can be achieved by adding the [{{site.data.keyword.cloud_notm}} classic infrastructure connection](/docs/transit-gateway?topic=transit-gateway-connecting-classic-infrastructure-vpcs) to a transit gateway.

## How can "VPC Peering" be achieved on IBM Cloud?
{: #vpc-peering}
{: faq}
{: support}

{{site.data.keyword.tg_full_notm}} can be used to connect multiple VPCs to each other. As such, connecting/peering two VPCs is just a part of the functionality that the transit gateway service offers. {{site.data.keyword.cloud_notm}} does not provide a standalone VPC peering service or capability.

## Can I connect a VPN or a Direct Link to a transit gateway?
{: #vpn}
{: faq}
{: support}

These capabilities do not exist today. However, they might be offered in the future.

## Can I create a global transit network using the IBM Cloud Transit Gateway?
{: #global-transit}
{: faq}
{: support}

{{site.data.keyword.tg_full_notm}} enables standard IP routing between networks (for example, global VPCs) that are connected to it. Additional functionality can be added by configuring {{site.data.keyword.IBM_notm}} or third-party virtual network functions, such as VPN, NAT, and firewalls, within one or more of the interconnected networks (for instance, using the "Transit VPC" concept).
