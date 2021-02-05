---

copyright:
  years: 2017, 2019
lastupdated: "2019-11-13"

keywords: faqs, questions, firewall, gateway, traffic, server, vpn, nat

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
{:faq: data-hd-content-type='faq'}
{:support: data-reuse='support'}

# FAQs for Hardware Firewall (Dedicated)
{: #faqs-for-hardware-firewall-dedicated-}

The following frequently asked questions can help you when working with the Hardware Firewall (Dedicated).
{: shortdesc}

## What is a firewall?
{: faq}

A firewall is a network device that is connected upstream from a server. The firewall blocks unwanted traffic from a server before the server is reached.

## Why should I use a firewall?
{: faq}

The primary advantage of having a firewall is that your server has to handle only “good” traffic – this means that your resource is solely being used for its intended purpose as opposed to handling unwanted traffic.

## What firewall products does IBM offer?
{: #products}
{: faq}
{: support}

You can find a detailed comparison of all firewall products offered in the IBM Cloud by reviewing [Exploring firewalls](/docs/fortigate-10g?topic=fortigate-10g-exploring-firewalls).

## Is the Hardware Firewall (Dedicated) compatible with IBM's load balancer products?
{: #compatibility}
{: faq}
{: support}

Yes. Hardware Firewall (Dedicated) is compatible with the standard and dedicated load balancers, as well as the Citrix Netscaler VPX and MPX.

## Can I have a dedicated hardware firewall and a network gateway associated with the same VLAN?
{: #vlan}
{: faq}
{: support}

No, it is not possible to have a firewall service (standard or dedicated) and a network gateway device assigned to the same VLAN.

## Does public traffic pass through my load balancer or hardware firewall first?
{: faq}

Coming from the public internet in, the local load balancer, dedicated load balancer or enterprise load balancer products are first, the hardware firewall products are next, and the NetScaler products are last (along with the customer's servers).

## Does IBM Cloud charge for firewall bandwidth?
{: #bandwidth}
{: faq}
{: support}

The Hardware Firewall (Shared), Hardware Firewall (Dedicated), and Fortigate Security Appliance are not metered for bandwidth.  Additionally, these products can reduce total bandwidth use by limiting the traffic that servers must respond to.

## What are the greyed out ports in my Windows Firewall?
{: #greyed-ports}
{: faq}
{: support}

IBM Cloud offers many different services that you can use with your server including Evault, SNMP, and Nagios monitoring. These services require that our internal systems communicate with your server to some degree. The grayed out ports you see in the Exceptions list are ports open on the internal network port only. They are still blocked on the public (internet) network connection. Because the internal network is a secured network, having these ports open is considered secure.

These ports generally cannot be modified; however, if you reset the firewall rules, it clears them from the Exceptions list. Beware that resetting the firewall rules can have an adverse affect, not only on these additional services, but could cause other issues as well with your server depending on its current configuration.

## What hardware firewall options are available for 10 Gbps servers?
{: faq}

If 10 Gbps is required only on the private network (for database, backup, storage, and so on), then customers can request a downgrade of only their public uplinks and order any of the hardware firewall products. If 10 Gbps is required on the public network, a network gateway or Fortigate Security Appliance 10 Gbps is required.

## What IP ranges do I allow through the firewall?
{: #ip-ranges}
{: faq}
{: support}

For the list of IP addresses and IP ranges to allow through the firewall, see [IBM Cloud IP ranges](/docs/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-ibm-cloud-ip-ranges).

## What is the maximum number of servers that the Hardware Firewall (Dedicated) or Fortigate Security Appliance can protect?
{: #max-servers}
{: faq}
{: support}

Both the Dedicated Hardware Firewall and the Fortigate Security Appliance can protect every server on a public VLAN. However, it is important to note that since these firewall devices are connected with 2 Gbps Uplink, IBM recommends scaling the number of firewall instances to meet the performance needs of your application. You can do so by deploying additional public VLAN firewalls within a pod to allow for the addition of firewall and associated compute resources.

## What VPN options are included with each firewall product?
{: #vpn}
{: faq}
{: support}

Not all firewalls offer VPN, and not all VPN options are the same. The general options for VPN are:

* Each customer receives unlimited SSL VPN connections to our private network. These connections can be established by clicking the VPN link while logged in to the IBM Cloud console.
* IBM Cloud offers a basic multi-tenant IPsec VPN service starting at $99/month.
* The Fortigate Security Appliance provides SSL and IPsec VPN options with public network access only (no access to the IBM Cloud private network).
* The network gateway provides SSL, IPsec and OpenVPN capabilities on the public or private network.
* The NetScaler products can provide SSL and IPsec VPN on the public or private network.
* Customers can also deploy a VPN solution onto a server within their IBM Cloud environment.

## When I select the High Availability (HA) option for the Hardware Firewall (Dedicated) or the Fortigate Security Appliance, what steps do I have to take to leverage this feature?
{: faq}

None. When ordered in HA, IBM Cloud automatically provisions the appliances in HA configuration. In the event that the primary device fails, a secondary passive device takes over as the primary active instance and begins passing traffic. While this failover is typically automatic, it is best practice to monitor servers and ensure traffic is being passed successfully.

## Which firewall products support public-to-private NAT and/or private VLAN segmentation?
{: faq}

Fortigate Security Appliance 10 Gbps supports public-to-private NAT and private VLAN segmentation.
