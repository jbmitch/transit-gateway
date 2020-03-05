---

copyright:
  years: 2020
lastupdated: "2020-02-07"

keywords: transit, gateway, about, features, overview

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

# About IBM Cloud Transit Gateway
{: #about}

{{site.data.keyword.tg_full}} is a service that enables you to connect {{site.data.keyword.cloud_notm}} Virtual Private Clouds (VPCs) and {{site.data.keyword.cloud_notm}} classic infrastructure to a single gateway.
{: shortdesc}

As the number of your VPCs grow, you need an easy way to manage the interconnection between these resources, both locally and globally. {{site.data.keyword.tg_full_notm}} is designed specifically for this purpose.

With {{site.data.keyword.tg_full_notm}}, you can create single or multiple transit gateways to connect VPCs together. You can also connect your {{site.data.keyword.cloud_notm}} classic infrastructure to a transit gateway to provide seamless communication. Any new network you connect to a transit gateway is then automatically made available to every other network connected to it. This makes it easy to scale your network as it grows.

## Overview of features
{: #feature-overview}

{{site.data.keyword.tg_full_notm}} offers the following features:

### Routing
{: #routing}

{{site.data.keyword.tg_full_notm}} supports local and global routing between VPCs and the {{site.data.keyword.cloud_notm}} classic infrastructure. It is optimized for performance and security, where all routed traffic passes through the {{site.data.keyword.cloud_notm}} infrastructure. Traffic stays within the {{site.data.keyword.cloud_notm}} network and does not traverse the public internet. Transit Gateway allows customers greater flexibility, redundancy, and speed in scaling their workloads, as well as connecting isolated networks running on {{site.data.keyword.cloud_notm}}.

### Management
{: #management}

You can use the command-line interface (CLI), API, or the {{site.data.keyword.cloud_notm}} console to create and manage your transit gateways.

For this Beta release, both the {{site.data.keyword.cloud_notm}} console and the CLI are supported for managing your transit gateways.
{: note}


### Security
{{site.data.keyword.tg_full_notm}} integrates with Identity and Access Management (IAM), letting you manage access to your transit gateway. Using IAM, you can create and manage [{{site.data.keyword.cloud_notm}} users and groups](/docs/transit-gateway?topic=transit-gateway-iam), as well as use permissions to allow or deny their access.
