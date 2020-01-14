---

copyright:
  years: 2019
lastupdated: "2019-12-04"

keywords: transit, gateway, deleting

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

# Deleting your transit gateways
{: #delete-gateway}

You can delete your IBM Cloud™ Transit Gateways using this procedure.
{: shortdesc}

1. From your browser, open the [IBM Cloud catalog ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com){:new_window} and log into your account.
2. Select the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) from the top left, then click **Hybrid Networking** to bring up the Direct Link page.
3. Click **Transit Gateway** from the left navigation panel.
4. Click the name of the transit gateway you want edit.

  If you are in the expanded view, click on **View Full Details**.
  {: tip}

5. Ensure the transit gateway has no attached connections - if it does, delete all connections.
  For each connection you want to delete, click the trashcan icon ![Trashcan icon](../../icons/icon_trash.svg) next to it to delete.
6. After the connections are removed, you can delete the transit gateway. You can do this in two ways:
  * From the transit gateway's details page, click the Options menu icon ![Options icon](../../icons/actions-icon-vertical.svg) next to the gateway you want to delete and select **Delete**.
  ![Delete gateways with the Options menu](images/delete-tg-1.png "Delete gateways with the Options menu")
  * From an individual transit gateway page, select **Actions > Delete**.
  ![Delete gateways with the Actions menu](images/delete-tg-2.png "Delete gateways with the Actions menu")
