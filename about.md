---

copyright:
  years: 2017
lastupdated: "2019-11-13"

keywords: about, vlan, overview, features

subcollection: hardware-firewall-dedicated

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}
{:deprecated: .deprecated}

# About the Hardware Firewall (Dedicated)
{: #about-the-hardware-firewall-dedicated-}

A Hardware Firewall (Dedicated) is a dedicated single-tenant network device that is connected upstream from a server and protects any or all servers on a public VLAN. It is purchased separately from a server, and it can be added to a VLAN at any time.   
{: shortdesc}

All instances of this service are deprecated. Existing instances can be used until it is no longer supported on 30 May 2021. Use one of the other available [firewall options](/docs/fortigate-10g?topic=fortigate-10g-exploring-firewalls#exploring-firewalls) to get our latest mobile security capabilities on IBM Cloud. For migration information, see [Migrating Hardware Firewall (Dedicated)](/docs/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-migration-overview#migration-overview)
{: deprecated}

With the Hardware Firewall (Dedicated), you have access to advanced features and the ability to fine tune the device to a much higher degree than other products. The firewall blocks or shapes traffic before the traffic ever reaches the server. The main advantages are that a server only has to handle 'good' traffic and that bandwidth can be constrained for less critical communications.

Customers can manage the firewall through the IBM Cloud console. High availability can also be ordered, which provides two appliances in active-passive deployment with synchronized configurations.

Since monthly server bandwidth is recorded at the server switch port, traffic blocked by the Hardware Firewall (Dedicated) is not counted against your monthly allotments, eliminating the need to pay for unwanted traffic.

## Overview and Features
{: #overview-and-features}

**Intended Use:** Single Public VLAN Protection

**User Interface:** Integrated into Classic Infrastructure in IBM Cloud and SL API

**Features:** Stateful Packet Inspection, VLAN Protection, Ingress Firewall Rules, Basic Logging, IPv4, IPv6, High Availability (Optional)

**Throughput:** 2000Mbps
