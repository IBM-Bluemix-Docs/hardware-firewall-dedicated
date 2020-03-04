---

copyright:
  years: 2017,2018
lastupdated: "2019-11-13"

keywords: firewall, vlan, view, portal

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

# Viewing your IBM firewalls
{: #viewing-your-ibm-firewalls}

You can see which VLANs are protected with Firewalls and find more details about individual Firewalls by visiting the VLANs page.
{: shortdesc}

1. From your browser, open the [IBM Cloud catalog ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com){:new_window} and log into your account.
2. Select the Menu icon ![Menu icon](../../icons/icon_hamburger.svg) from the top left, then click **Classic Infrastructure**.
3. Select **Network > IP Management > VLANs**.

Each row in the table represents a VLAN in your infrastructure. IBM© Cloud populates the "VLAN Number" and "Primary Router" information automatically indicating the true VLAN number and the router that it is configured on. The "Name" field can be used to give the VLAN a recognizable name (such as DMZ, Intranet, Public, or Database).

The far right column "Gateway/Firewall" contains details about what firewall protection is in place, for example:

* **Add Firewall** indicates that there are no firewalls in place for servers on this VLAN.
* **Individually Protected Servers** indicates that one or more servers is utilizing a Hardware Firewall and that there is no Hardware Firewall (Dedicated), FortiGate Security Appliance, or Network Gateway in place. VLAN firewalls and network gateways are not able to be placed on a VLAN that has individually protected servers.
* **Firewall-vlanXXXX.networklayer.com** indicates that there is a Hardware Firewall (Dedicated) or a FortiGate Security Appliance in place. Only one VLAN firewall or Network Gateway can be associated with a VLAN, but a server can be protected on the public VLAN by a VLAN firewall and associated on the private network with a Network Gateway.
* **GatewayName** indicates the VLAN is associated with that Network Gateway.

## Individually protected servers details
{: #individually-protected-servers-details}

For VLANs that have **Individually Protected Servers** in the "Gateway/Firewall" field, you can click on the associated VLAN number link to display the details of the VLAN, including the associated devices.

In the list of associated devices, you can click on each device and scroll to the bottom of the Configuration tab. You will see **Firewall** in the Addons section with **Installed** or **Not Installed** for the status.

* **Not Installed** indicates that no firewall is in place for this device.
* **Installed** indicates that a firewall is in place. There will be a **Firewall** tab available on the device where you can manage the firewall configuration.

## Dedicated firewall details
{: #dedicated-firewall-details}

For VLANs that have **Firewall-vlanXXXX.networklayer.com** in the "Gateway/Firewall" field, you can click on that firewall link to display the details of the Firewall. The device details include the associated router, VLAN, IPv4/IPv6 subnets, the devices associated with that VLAN, and the controls for routing traffic through or around the firewall.

FortiGate Security Appliance devices will have the management IP, username, and password.  Management of FortiGate Security Appliances is completed through their own GUI or SSH-based console.

## Network gateway details
{: #network-gateway-details}

For VLANs that have a Network Gateway device name in the "Gateway/Firewall" field, you can click on the Network Gateway name to display details of the Network Gateway. The device details include the associated frontend (FCR) and backend (BCR) VLANs and Network Gateway management options.
