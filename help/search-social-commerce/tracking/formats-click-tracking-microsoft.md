---
title: Klick-Tracking-Formate für [!DNL Microsoft Advertising]
description: Erfahren Sie mehr über die Klick-Tracking-Formate für  [!DNL Microsoft Advertising] .
exl-id: 4970ac33-4978-4768-8701-6fdd3252bbd1
feature: Search Tracking
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '579'
ht-degree: 0%

---

# Klick-Tracking-Formate für [!DNL Microsoft Advertising]

Im Folgenden finden Sie die Formate für Basis-Tracking-Vorlage und Landingpage-Suffix (endgültiges URL-Suffix) , die Search, Social und Commerce für die [!DNL Microsoft Advertising] erfordern.

## Formate von Tracking-Vorlagen

### Such- und Zielgruppennetzwerke (außer Sitelinks)

Das folgende Format gilt für alle verfolgbaren Anzeigentypen in Such- und Zielgruppennetzwerken.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Beispiel:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Werbetreibenden in Adobe Advertising.
>
>* Dieses Format gibt an, dass die Token-Übergabe für die Kampagne aktiviert ist (Standard). Wenn die Token-Übergabe deaktiviert ist, ersetzen Sie `cq?` nach der `<advertiser_ID>` durch `c?`.
>
>* `{TargetId}` steht für die ID a) des Keywords oder b) der Keyword- und Remarketing-Liste (Zielgruppe), die die Anzeige ausgelöst hat (z. B. „kwd-123:aud-456&quot; für sowohl ein Keyword als auch eine Remarketing-Liste oder „kwd-123“ nur für Keywords).

### Sitelinks

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Beispiel:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Werbetreibenden in Adobe Advertising.
>
>* Dieses Format gibt an, dass die Token-Übergabe für die Kampagne aktiviert ist (Standard). Wenn die Token-Übergabe deaktiviert ist, ersetzen Sie `cq?` nach der `<advertiser_ID>` durch `c?`.
>
>* `{TargetId}` steht für die ID a) des Keywords oder b) der Keyword- und Remarketing-Liste (Zielgruppe), die die Anzeige ausgelöst hat (z. B. „kwd-123:aud-456&quot; für sowohl ein Keyword als auch eine Remarketing-Liste oder „kwd-123“ nur für Keywords).
>
>* `{adextensionid}` wird nicht verwendet.
>
>* (Sitelinks) Durch Generieren eines [!UICONTROL Transaction Report] können Sie sehen, welche Konversionen durch einen Klick auf einen Sitelink entstanden sind. Der [!UICONTROL Link Type] Spaltenwert für einen Sitelink ist `sl:<Sitelink text>`, z. B. `sl:See Current Offers`.

### Einkaufsnetzwerk

Die folgenden Formate gelten für Shopping-Anzeigen in Shopping-Netzwerken. Sie können eine Tracking-Vorlage auf Konto-, Kampagnen-, Anzeigengruppen- oder Produktgruppenebene angeben.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

Beispiel:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Werbetreibenden in Adobe Advertising.
>
>* Dieses Format gibt an, dass die Token-Übergabe für die Kampagne aktiviert ist (Standard). Wenn die Token-Übergabe deaktiviert ist, ersetzen Sie `cq?` nach der `<advertiser_ID>` durch `c?`.
>
>* `{TargetId}` steht für die ID a) des Keywords oder b) der Keyword- und Remarketing-Liste (Zielgruppe), die die Anzeige ausgelöst hat (z. B. „kwd-123:aud-456&quot; für sowohl ein Keyword als auch eine Remarketing-Liste oder „kwd-123“ nur für Keywords).
>
>* (Optional) Anstatt Tracking-Vorlagen auf Konto-, Kampagnen-, Anzeigengruppen- oder Produktgruppenebene einzugeben, können Sie die Tracking-URL zu den Produktdaten im [!DNL Microsoft Merchant Center]-Konto hinzufügen. Fügen Sie dazu die Tracking-URL zusammen mit dem Wert im Feld &quot;`link`&quot; bzw. &quot;`mobile_link`&quot; in eine benutzerdefinierte Spalte &quot;[bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0)&quot; im Produkt-Feed ein. Der Wert im Feld &quot;`bingads_redirect`&quot; ersetzt die Werte in den Feldern &quot;`link`&quot; und &quot;`mobile_link`&quot;. Mit dieser Methode generierte URLs enthalten keine Tracking-Parameter, die in den Such-, Social- und Commerce-Konto- oder Kampagneneinstellungen angegeben sind.

## Formate für Landingpage-Suffixe (endgültiges URL-Suffix)

>[!NOTE]
>
>Landingpage-Suffixe auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Zur einfacheren Wartung verwenden Sie nur das Suffix auf Kontoebene, es sei denn, eine andere Nachverfolgung für einzelne Kontokomponenten ist erforderlich. Um ein Suffix auf Anzeigengruppenebene oder darunter zu konfigurieren, verwenden Sie den Editor des Anzeigennetzwerks.

### Such- und Zielgruppennetzwerke

Konten, die das Adobe Advertising-Konversions-Tracking verwenden, müssen die Klick-Kennung des Werbenetzwerks (`msclkid` für [!DNL Microsoft Advertising]) im Suffix enthalten:

* Wenn der Advertiser über eine Adobe Analytics-Integration verfügt, muss das Suffix Folgendes enthalten:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}`

* Wenn der Advertiser keine Adobe Analytics-Integration hat, muss das Suffix Folgendes enthalten:

  `&ev_efid={msclkid}:G:s`

### Einkaufsnetzwerk

Konten, die das Adobe Advertising-Konversions-Tracking verwenden, müssen die Klick-Kennung des Werbenetzwerks (`msclkid` für [!DNL Microsoft Advertising]) im Suffix enthalten:

* Wenn der Advertiser über eine Adobe Analytics-Integration verfügt, muss das Suffix Folgendes enthalten:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`

* Wenn der Advertiser keine Adobe Analytics-Integration hat, muss das Suffix Folgendes enthalten:

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [Über Klick-Tracking-URL-Formate für den Konversionsverfolgungs-Service von Adobe Advertising](formats-click-tracking-about.md)
>* [AMO ID-Formate](https://experienceleague.adobe.com/de/docs/analytics/components/dimensions/amo-id#dimension-items)
