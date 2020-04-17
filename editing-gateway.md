---

copyright:
  years: 2020
lastupdated: "2020-01-28"

keywords: transit, gateway, editing

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

# Managing transit gateways
{: #edit-gateway}

You can add or delete connections from your {{site.data.keyword.tg_full}} using the {{site.data.keyword.cloud_notm}} console.
{: shortdesc}

## Adding a connection
{: #adding-connections}

To add a connection to a transit gateway:
1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](https://cloud.ibm.com){:external} and log in to your account.
2. Select the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) from the upper left, then click **Interconnectivity**.
3. Click **Transit Gateway** from the left navigation pane.
4. Click the name of the transit gateway where you want to add a connection.

  If you are in the expanded view, click **View details**.
  {: tip}

5. Click **Add connection**.

You can now choose and configure the specific network connections that you want to add to your transit gateway.

## Deleting a connection
{: #deleting-connections}

To delete a connection from a transit gateway:
1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](https://cloud.ibm.com){:external} and log in to your account.
2. Select the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) from the upper left, then click **Interconnectivity**.
3. Click **Transit Gateway** from the left navigation pane.
4. Click the name of the transit gateway where you want to delete a connection.

  If you are in the expanded view, click **View details**.
  {: tip}

5. To delete a connection, click the trashcan icon ![Trashcan icon](../../icons/icon_trash.svg) next to its name.
6. Confirm that you want to delete the connection.

## Changing your configuration
{: #change-configuration}

To change your transit gateway configuration:
1. From your browser, open the [{{site.data.keyword.cloud_notm}} console](https://cloud.ibm.com){:external} and log in to your account.
2. Select the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) from the upper left, then click **Interconnectivity**.
3. Click **Transit Gateway** from the left navigation pane.
4. Click the name of the transit gateway you want to edit.

  If you are in the expanded view, click **View details**.
  {: tip}

5. Click **Edit**.

From here you can change the gateway's name, as well as its routing type (Local or Global).

![Editing your configuration](images/7-editingGlobaltoLocalTG.png "Editing your configuration")

To change a transit gateway's routing type from Global to Local, you must delete any connections that are not local to the transit gateway's location. 
{: important}
