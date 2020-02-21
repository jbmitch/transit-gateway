---

copyright:
  years: 2020
lastupdated: "2020-02-20"

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
{:external: target="_blank_" .external}
{:term: .term}

# High availability and disaster recovery
{: #ha-dr}

{{site.data.keyword.tg_full}} is highly available within any {{site.data.keyword.cloud_notm}} location (for example, Dallas or Washington, DC). However, recovering from disasters that affect an entire location requires planning and preparation.
{: shortdesc}

You are responsible for understanding your configuration, customization, and usage of the service. You are also responsible for being ready to re-create an instance of the service in a new location and to restore your data in a new location.

## High availability
{: #high-availability}

{{site.data.keyword.cloud_notm}} supports high availability with no single point of failure. The service achieves high availability automatically and transparently by means of the multi-zone region (MZR) feature provided by {{site.data.keyword.cloud_notm}}.

When you create a Transit Gateway instance in a particular region, the system automatically enables multiple zones which do not share a single point of failure.

## Disaster recovery
{: #disaster-recovery}

In the event of a catastrophic failure impacting an entire region, the Transit Gateway management service will automatically failover to a secondary region. However, you may need to recreate specific instances of your transit gateway, as well as its connections in a different region.

Your disaster recovery plan should include knowing, preserving, and being prepared to restore all data that is maintained on {{site.data.keyword.cloud_notm}}. This includes data about all deployed transit gateways and their connections.

### Disaster recovery for Transit Gateways
{: #disaster-recovery-tgw}

You must be prepared to recreate your transit gateways and connections. The following section helps ensure you have all the data needed for this purpose.

#### Backing up Transit Gateways
{: #disaster-recovery-tgw-backup}

The following steps illustrate using the IBM Cloud CLI, but you can also use the IBM Cloud console or API.
{: note}

Preserve a list of all of your transit gateways and their connections. To do so, perform the following procedure:

  1. Use the `ibmcloud tg gateways` command to list details about all your transit gateways. Save this output.
  2. For each gateway, use the `ibmcloud tg connections GATEWAY_ID` method to list information about its connections. Save this output.

  For more information, see the [Transit Gateway CLI reference](/docs/infrastructure/transit-gateway?topic=tg-cli-plugin-transit-gateway-cli).
  {: tip}

Preserving the information returned from these commands will help you recover for a potential failure as quickly as possible.

In the event of a failure, this information allows you to use the `ibmcloud tg gateway-create` and `ibmcloud tg connection-create` commands needed to recreate your transit gateways and connections, using the CLI reference as your guide. Again, note that you can perform the equivalent tasks using the IBM Cloud console or programmatic APIs, as well.
