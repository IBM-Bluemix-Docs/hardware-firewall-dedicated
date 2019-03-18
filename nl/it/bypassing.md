---

copyright:
  years: 2017
lastupdated: "2018-11-30"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Esclusione delle regole di Hardware Firewall (Dedicated)
{: #bypassing-hardware-firewall-dedicated-rules}

Per escludere le regole del firewall,

1. Dal tuo browser, apri [Customer Portal ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://control.softlayer.com/){: new_window} e accedi al tuo account.
2. Nella navigazione del portale del cliente, passa a **Network > IP Management > VLANs** e fai clic sul dispositivo firewall che vuoi escludere.
3. Nella pagina **Device Details**, puoi utilizzare il menu a discesa **Actions** per scegliere **Set Route Bypass** oppure nella sezione **Status:**, puoi fare clic su **Bypass Rules**. 

	Un'altra opzione consiste nell'aggirare il firewall. Puoi utilizzare il menu a discesa **Actions** per scegliere **Set Route Bypass** oppure nella sezione **Status:**, puoi fare clic sul pulsante **Route Around**. In ogni caso, dovrebbe comparire una finestra di dialogo di conferma. Fai clic su **Yes** per confermare l'azione. L'esclusione della rotta ha effetto dopo circa due minuti. Durante la modalità di esclusione, "Status" sarà "Routing AROUND firewall".

## Riabilita le regole

Per riabilitare le regole, segui le istruzioni sopra riportate per raggiungere la pagina **Device Details**, fai clic sull'elenco a discesa **Actions** e scegli **Set Route Bypass**. Visualizzerai una finestra di dialogo di conferma. Fai clic su **Yes** per confermare l'azione. "Status" ritornerà "Routing THROUGH firewall" in due minuti.
