---

copyright:
  years: 2020
lastupdated: "2020-01-14"

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

IBM Cloud™ Transit Gateway is a service that enables you to connect IBM Cloud Virtual Private Clouds (VPCs) and IBM Cloud classic infrastructure to a single gateway.
{: shortdesc}

As the number of your VPCs grow, you need an easy way to manage the interconnection between these resources, both locally and globally. IBM Cloud Transit Gateway was designed specifically for this purpose.

With IBM Cloud Transit Gateway, you can create single or multiple transit gateways to connect VPCs together. You can also connect your IBM Cloud classic infrastructure to a transit gateway to provide seamless communication. Any new network you connect to a transit gateway is then automatically made available to every other network connected to it. This makes it easy to scale your network as you grow.

Classic-access VPCs cannot be directly connected to transit gateways. However, access to classic VPC resources can be achieved by adding the IBM Cloud classic infrastructure connection to a transit gateway.
{: note}

## Overview of features
{: #feature-overview}

IBM Cloud Transit Gateway offers the following features:

### Routing
{: #routing}

IBM Cloud Transit Gateway supports local and global routing between VPCs and the IBM Cloud classic infrastructure. It is optimized for performance and security, where all routed traffic passes through the IBM Cloud infrastructure. Traffic stays within the IBM Cloud network and does not traverse the public Internet. Transit Gateway allows customers greater flexibility, redundancy, and speed in scaling their workloads and connecting isolated networks running on IBM Cloud.

### Management
{: #management}

You can use the command-line interface (CLI), API, or the IBM Cloud console to create and manage your transit gateway.

For the Beta, only the IBM Cloud console is currently supported for managing your transit gateway.
{: note}


### Security
IBM Cloud Transit Gateway integrates with Identity and Access Management (IAM), letting you manage access to your transit gateway. Using IAM, you can create and manage [IBM Cloud users and groups](/docs/infrastructure/transit-gateway?topic=transit-gateway-iam), as well as use permissions to allow or deny their access.
