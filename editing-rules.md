---

copyright:
  years: 2017,2019
lastupdated: "2019-11-13"

keywords: edit, rules, firewall

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

# Configuring the Hardware Firewall (Dedicated)
{: #configuring-the-hardware-firewall-dedicated-}

When the Hardware Firewall (Dedicated) is first added to the VLAN, a set of rules is initially put in place that allows all traffic through the firewall. Configuring the firewall is as simple as creating a set of rules to allow access to certain IP addresses/ports from specific internet addresses while denying traffic from other sources.
{: shortdesc}

## Editing firewall rules
{: edit-rules}

To edit the firewall rules:

1. From your browser, open the [IBM Cloud catalog ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com){:new_window} and log in to your account.
1. Select the Menu icon ![Menu icon](../../icons/icon_hamburger.svg), then click **Classic Infrastructure**.
1. Select **Network > IP Management > VLANs**.
  Each row represents a VLAN in your infrastructure. Click the Firewall-vlanXXXX.networklayer.com link associated with the VLAN that you want to manage to take you to the **Device Details** page. In "Configuration > Status", you can see "Routing THROUGH firewall". If rules exist, the "Status" indicates that the firewall is "Processing All Rules."  Users can choose to bypass the rules in the event that implemented rules have an unintended impact on their environment by clicking "Bypass Rules" in this area.
1. To start updating rules, click the **Rules** tab. The page shows the current rules in effect for IPv4 and IPv6 addresses. If no rules are implemented, a faded placeholder is displayed. Edit individual rules by clicking on the corresponding row. This list of rules is known as the 'working config'. A 'working config' is a set of rules that is in the process of being created, but has not yet been applied to the firewall. A user can edit, add, and delete rules until the rule set is completed. Rules are shown in the order in which they are processed with lower numbered rules having precedence over higher number rules (if rule 1 allows a packet through, rules 2 and beyond are not applied to the packet).
1. Click a rule to edit it, or click the plus sign at the end of the table to add an additional rule. Clicking on the minus icon deletes the rule. The rules are automatically validated as you enter them.

    The fields are:

    **Action:** 'permit' or 'deny' traffic matching this rule

    **Source:** Can be either 'any', a specific IP address, or the network address for a specific subnet.

    **CIDR:** Indicates the standard CIDR notation for the selected source. "32" implements the rule for a single IP while, for example, "24" implements the rule for 256 IPs.

    **Destination:** Can be either 'any', a specific IP address, or the network address for a specific subnet.

    **CIDR:** Indicates the standard CIDR notation for the selected destination.

    **Port Range:** These two fields indicate the range of ports (between 1 and 65535) that the rule will apply to.

    **Protocol:** The protocol that the rule will apply to (TCP/GRE/ICMP/UDP/PPTP/AH/ESP)

    **Notes:** Field to enter any note about this rule.

1. After the 'working config' is complete, click the **Update Rules** button to have the 'working config' applied to the firewall. The rules take effect within two minutes. If you delete all the rules or no valid rule when you click on **Update Rules** button, an error states "At least one valid rule is required to create a firewall update request." If you don't want any rules applied to your firewall, use the **Bypass Rules** button on the Configuration page.

## Common ports

| Protocol | Port |
| :-----: | :-----: |
| FTP | 21 |
| SSH | 22 |
| Telnet | 23 |
| SMTP | 25 |
| DNS | 53 |
| HTTP | 80 |
| POP3 | 110 |
| IMAP | 143 |
| HTTPS | 443 |
| MSSQL | 1433 |
| MySQL | 3306 |
| Remote Desktop | 3389 |
| PostgreSQL | 5432 |
| VNC Web | 5800 |
| VNC Client | 5900 |
| Urchin | 9999 or 10000 |
