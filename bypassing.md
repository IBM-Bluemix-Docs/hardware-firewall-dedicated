---

copyright:
  years: 2017, 2019
lastupdated: "2019-11-13"

keywords: bypass, firewall, rules,

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

# Bypassing Hardware Firewall (Dedicated) rules
{: #bypassing-hardware-firewall-dedicated-rules}

You can bypass the rules of your Hardware Firewall (Dedicated) by following the instructions here.
{: shortdesc}

1. From your browser, open the [IBM Cloud catalog ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com){:new_window} and log in to your account.
2. Select the Menu icon ![Menu icon](../../icons/icon_hamburger.svg), then click **Classic Infrastructure**.
3. Select **Network > IP Management > VLANs** and click the firewall device that you want to bypass.
4. In the **Device Details** page, you can use the **Actions** menu to choose **Set Rule Bypass**, or in the **Status** section, you can click on the **Bypass Rules** button. Click **Yes** to confirm the action. Bypassing the rules takes approximately two minutes to take effect. While in bypass mode, the "Status" is "Bypassing All Rules".

	Another option is to route around the firewall when you are troubleshooting. You can use the **Actions** menu to choose **Set Route Bypass**, or in the **Status** section, you can click **Route Around**.

## Enabling the rules again
{: #enable-the-rules-again}

To enable the rules again, follow the preceding instructions to reach the **Device Details** page, then click the **Actions** menu and choose **Set Route Bypass**. Click **Yes** to confirm the action. The "Status" changes back to "Routing THROUGH firewall" within two minutes.
