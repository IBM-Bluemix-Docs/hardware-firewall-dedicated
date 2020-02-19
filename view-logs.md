---

copyright:
  years: 2017
lastupdated: "2019-11-13"

keywords: logs, logging, troubleshooting, firewall

subcollection: hardware-firewall-dedicated

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}
{:note: .note}
{:important: .important}
{:help: data-hd-content-type='help'}
{:support: data-reuse='support'}

# Viewing Log Reports
{: #viewing-log-reports}
{: help}
{: support}

Logs for your Hardware Firewall (Dedicated) are available on a per-IP basis by navigating to the protected device, selecting the **Firewall** tab, and selecting **Actions > Firewall Logs**.
{: shortdesc}

Logs are presented in .CSV format and contain the following:

**Event Type:** The action taken by the firewall (Deny)

**Protocol:** The protocol used for communication (TCP/PING/UDP/IRD/etc)

**Source IP Address:** IP where the packet originated

**Source Port:** Port where the packet originated

**Destination IP:** Intended target for the packet

**Destination Port:** Intended port for the packet

**Creation Date:** Date and time of action (24-hour format)
