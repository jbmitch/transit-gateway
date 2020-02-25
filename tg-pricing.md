---

copyright:
  years: 2020
lastupdated: "2020-02-21"

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

# IBM Cloud Transit Gateway pricing
{: #tg-pricing}

IBM Cloud Transit Gateway has two primary billing options:

* Per connection
* Global routing data transfer per GB.   

Per connection fee pricing is determined by how many total connections you have configured against all provisioned transit gateways on your account, per month. The pricing structure is:

* 1-10 total connections = $20 (usd) per connection/per month
* 11-20 total connections = $15 (usd) per connection/per month
* 21-50 total connections = $10 (usd) per connection/per month
* 50+ total connections = $5 (usd) per connection/per month

Global routing data transfer fee pricing is metered per gigabyte (GB). The first terabyte (TB) per account is free of charge, then a charge of $0.02 per GB thereafter accrues on a monthly basis.

Local routing data transfer fees are free of charge (within the same multizone region data center).
{: note}
