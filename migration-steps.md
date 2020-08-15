---

copyright:
  years: 2019, 2020
lastupdated: "2020-08-15"

keywords: migrate, update, gateway, firewall, cloud, hardware, firewall, dedicated, vra, vsrx, migration, migrating

subcollection: hardware-firewall-dedicated

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

# Migrating Hardware Firewall (Dedicated)
{: #migration-overview}

Hardware Firewall (Dedicated) customers should start migrating to other security gateway options, as it will no longer be sold after August 15, 2020. You can read the full [end of marketing announcement](/docs/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-FSA-EOM#FSA-EOM) for more information.
{: shortdesc}

The following procedures provide instructions for migrating Hardware Firewall (Dedicated) either to Juniper vSRX or Virtual Router Appliance (VRA 5600).

In a typical migration scenario, you have an existing Hardware Firewall (Dedicated) associated with a public VLAN.

## Migrating from a Hardware Firewall (Dedicated) to Juniper vSRX
{: #fsa-to-vsrx}

This migration option makes use of the Juniper support program to assist you with migrating to a Juniper vSRX. You can submit the request with your configuration using the following [Google form ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://forms.gle/DvkPBdxC6DiXrHAn6){: new_window}.
{: note}

To migrate from an Hardware Firewall (Dedicated) to a vSRX, follow these steps:

1. Order a Juniper vSRX. See [Getting started with IBM Cloud Juniper vSRX](/docs/vsrx?topic=vsrx-getting-started) for details.

2. Complete your basic Juniper vSRX configurations, such as creating system users and hostnames. See [Performing vSRX basics](/docs/vsrx?topic=vsrx-performing-ibm-cloud-juniper-vsrx-basics) for details.

3. Check vSRX readiness to ensure your Juniper vSRX can perform common gateway actions. See [Checking vSRX readiness](/docs/vsrx?topic=vsrx-vsrx-readiness) for details.

  Your Juniper vSRX is not associated with any public VLAN.
  {: note}

4. From the VLAN page, cancel the Hardware Firewall (Dedicated). See [Canceling a firewall](/docs/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-canceling-a-hardware-firewall-dedicated-) for details.

5. Associate the public VLAN that you want to protect with your new Juniper vSRX. See [Associating a VLAN to a gateway appliance](/docs/vsrx?topic=gateway-appliance-managing-vlans-and-gateway-appliances#associate-a-vlan-to-a-gateway-appliance) for details.

## Migrating from Hardware Firewall (Dedicated) to an IBM Cloud Virtual Router Appliance
{: #fsa-to-vra}

To migrate from an Hardware Firewall (Dedicated) to a Virtual Router Appliance (VRA), follow these steps:

1. Order a VRA. See [Getting started with IBM Cloud Virtual Router Appliance](/docs/virtual-router-appliance?topic=virtual-router-appliance-getting-started) for details.

2. Configure your VRA. See [Getting started with IBM Cloud Virtual Router Appliance](/docs/virtual-router-appliance) for details.

3. From the VLAN page, cancel the Hardware Firewall (Dedicated). See [Canceling a firewall](/docs/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-canceling-a-hardware-firewall-dedicated-) for details.

4. Associate the public VLAN that you want to protect with your VRA. See [Managing VLANs with a gateway appliance](/docs/virtual-router-appliance?topic=gateway-appliance-managing-vlans-and-gateway-appliances).
