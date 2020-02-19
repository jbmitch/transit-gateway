---

copyright:
  years: 2020
lastupdated: "2020-02-07"

keywords: transit, gateway, connecting, vpc, region, order

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
{:external: target="_blank" .external}
{:term: .term}
{:help: data-hd-content-type='help'}
{:support: data-reuse='support'}

# Ordering an IBM Cloud Transit Gateway
{: #ordering-transit-gateway}
{: help} 
{: support}

To create an {{site.data.keyword.tg_full_notm}}, follow these steps.
{: shortdesc}

1. Review requirements and configuration considerations in [Planning for Transit Gateway](/docs/transit-gateway?topic=transit-gateway-helpful-tips).
2. From your browser, open the [{{site.data.keyword.cloud_notm}} catalog](https://cloud.ibm.com/catalog){: external} and log in to your account.
3. Select **Networking** in the navigation pane, then click the Transit Gateway tile.

  Alternatively, you can access the ordering page from the [{{site.data.keyword.cloud_notm}} console](https://cloud.ibm.com){:external} by selecting the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) on the upper left of the page. Select **Hybrid Networking** > **Transit Gateway** and then click the **Order Transit Gateway** button.
  {: tip}

4. From the ordering page, enter a name for the transit gateway and select a resource group. You can select a resource group from the list, or keep the default selection.
5. Choose a routing option:

   * Select **Local routing** if you want this gateway to only connect VPCs in the same [Multi-Zone Region (MZR)](#x9774820){: term}.
   * Select **Global routing** if you want this gateway to connect to VPCs in different regions.

   You can upgrade routing options at a later point, if your needs change. Pricing is changed accordingly.
   {: note}

6. Select a location. If you selected local routing, data centers within the MZR are shown. For global routing, all data centers are accessible.

7. You can add connections to your transit gateway now or after it has been provisioned.

  To add them now, select the network connection to be attached to the transit gateway, and then type a name for the connection. To add multiple network connections to the transit gateway, click **Add connection**.

  To add them later, refer to [Adding a connection](/docs/infrastructure/transit-gateway?topic=transit-gateway-edit-gateway#adding-connections).

  You can add the following connection types to your gateway:

   * **VPC** networks can contain either first or second generation compute resources, allowing you to connect to your account’s VPC resources.
   * **Classic Infrastructure** networks allow you to connect to IBM Cloud classic resources. Only one classic infrastructure connection is allowed per transit gateway.

8. **View Terms** on the right of the page.
9. Click **Create** to complete your order. You can request assistance from the IBM Cloud Sales team at any time.   
