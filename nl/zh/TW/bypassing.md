---

copyright:
  years: 2017
lastupdated: "2018-11-30"

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

# 略過 Hardware Firewall (Dedicated) 規則
{: #bypassing-hardware-firewall-dedicated-rules}

若要略過防火牆規則，請執行下列動作：

1. 從您的瀏覽器開啟[客戶入口網站 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com/){: new_window}，然後登入您的帳戶。
2. 在「客戶入口網站」導覽中，前往**網路 > IP 管理 > VLAN**，然後按一下您要略過的防火牆裝置。
3. 在**裝置詳細資料**頁面中，您可以使用**動作**下拉功能表，以選擇**設定規則略過**，或在**狀態**區段中，您可以按一下**略過規則**按鈕。無論哪種方式，您都應該會看到一個確認對話框。按一下**是**以確認動作。略過規則大約需要兩分鐘才能生效。在略過模式下，「狀態」將「略過所有規則」。

	另一個選項是當您執行疑難排解等作業時繞過防火牆，您可以使用**動作**下拉功能表，以選擇**設定路徑略過**，或在**狀態**區段中，您可以按一下**繞過**。

## 再次啟用規則
{: #enable-the-rules-again}

若要再次啟用規則，請遵循上面的指示到達**裝置詳細資料**標籤，然後按一下**動作**下拉功能表，並選擇**設定路徑略過**。您將會看到一個確認對話框。按一下**是**以確認動作。「狀態」將在兩分鐘內變更回「經由防火牆的路徑」。
