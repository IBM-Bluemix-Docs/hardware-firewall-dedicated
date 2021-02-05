---

copyright:
  years: 2017, 2019
lastupdated: "2019-11-13"

keywords: limitations, problems, troubleshooting, nlb, arp, ha, failover, vlan, gateway

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

# Known limitations for Hardware Firewall (Dedicated)
{: #known-limitations-for-hardware-firewall-dedicated-}

Here are some limitations to be aware of when using your Hardware Firewall (Dedicated).
{: shortdesc}

* Incompatible with Windows Network Load Balancing (NLB) due to the way ARP is processed
* High Availability failover functionality is not exposed to the user. If the master firewall malfunctions, but does not fail over automatically, an IBM Support case is required. Device monitoring for critical services is recommended to ensure that firewalls are appropriately passing traffic.
* A Hardware Firewall (Dedicated) cannot be deployed on a VLAN that is currently associated with a network gateway, hardware firewall, or Fortigate Security Appliance (FSA).
