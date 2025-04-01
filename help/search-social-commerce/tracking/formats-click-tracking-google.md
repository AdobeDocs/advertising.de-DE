---
title: Klick-Tracking-Formate für [!DNL Google Ads]
description: Erfahren Sie mehr über die Klick-Tracking-Formate für  [!DNL Google Ads] .
exl-id: d09c3b4e-1274-45fb-abb6-dddfe60f1477
feature: Search Tracking
source-git-commit: 70629247a18a78b12a7fc8b166a0272764bb20b8
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Klick-Tracking-Formate für [!DNL Google Ads]

Im Folgenden finden Sie die Formate für Basis-Tracking-Vorlage und Landingpage-Suffix (endgültiges URL-Suffix) , die Search, Social und Commerce für die [!DNL Google Ads] erfordern.

## Formate von Tracking-Vorlagen

### Netzwerk suchen/anzeigen, einschließlich Sitelinks

Das folgende Format gilt für alle verfolgbaren Anzeigenarten in Such- und Anzeigennetzen und für Sitelinks.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Beispiel:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Werbetreibenden in Adobe Advertising.
>
>* Dieses Format gibt an, dass die Token-Übergabe für die Kampagne aktiviert ist (Standard). Wenn die Token-Übergabe deaktiviert ist, ersetzen Sie `cq?` nach der `<advertiser_ID>` durch `c?`.
>
>* Die [!DNL ValueTrack], die die endgültigen URLs in Tracking-Vorlagen angeben, müssen entweder `{lpurl}` oder `!{unescapedurl}` sein.
>
>* (Textanzeigen) Wenn Sie nach Keyword bieten, hat der Parameter `ev_pl` (für Platzierungen) keinen Wert. Wenn Sie nach Platzierung bieten, hat `ev_ln` (für Keywords) keinen Wert. Wenn Sie nach Anzeigengruppe oder einer anderen Dimension bieten, haben sowohl `ev_ln` als auch `ev_pl` keine Werte.
>
>* (Dynamische Suchanzeigen) `{keyword}` Gibt den Ausdruck für die dynamische Suche an, z. B. `_cat:[VALUE]` oder `_url:[VALUE]`.
>
>* (Dynamische Suchanzeigen) [!DNL Google Ads] bestimmt die endgültige URL dynamisch, sodass Sie keine eingeben müssen.
>
>* (Sitelinks) Durch Generieren eines [!UICONTROL Transaction Report] können Sie sehen, welche Konversionen durch einen Klick auf einen Sitelink entstanden sind. Der [!UICONTROL Link Type] Spaltenwert für einen Sitelink ist `sl:<Sitelink text>`, z. B. `sl:See Current Offers`.

### Einkaufsnetzwerk

Das folgende Format gilt für Shopping-Anzeigen und Produktgruppen in Shopping-Netzwerken. Sie können eine Tracking-Vorlage auf Konto-, Kampagnen-, Anzeigengruppen- oder Produktgruppenebene angeben.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Beispiel:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Werbetreibenden in Adobe Advertising.
>
>* Dieses Format gibt an, dass die Token-Übergabe für die Kampagne aktiviert ist (Standard). Wenn die Token-Übergabe deaktiviert ist, ersetzen Sie `cq?` nach der `<advertiser_ID>` durch `c?`.
>
>* Die [!DNL ValueTrack], die die endgültigen URLs in Tracking-Vorlagen angeben, müssen entweder `{lpurl}` oder `!{unescapedurl}` sein.
>
>* [!DNL Google Ads] verwendet Produkt-URLs im Google Merchant Center-Feed als endgültige URLs, sodass Sie keine endgültigen URLs für Ihre Produktdaten oder Produktgruppen eingeben müssen.
>
>* Sie können sehen, welche Konversionen durch einen Klick auf eine Shopping-Anzeige entstanden sind, indem Sie eine [!UICONTROL Transaction Report] generieren. Der [!UICONTROL Link Type] Spaltenwert für eine Produktanzeige lautet pla:`<product ID>`, z. B. `pla:8525822`.

## Formate für Landingpage-Suffixe (endgültiges URL-Suffix)

Konten, die das Adobe Advertising-Konversions-Tracking verwenden, müssen die Klick-Kennung des Werbenetzwerks (`gclid` für [!DNL Google Ads]) im Suffix enthalten:

* Wenn der Advertiser über eine Adobe Analytics-Integration verfügt, muss das Suffix eines der folgenden Elemente enthalten:

   * [!DNL Google Ads] Konten, die das neueste [AMO ID-Format](/help/integrations/analytics/ids.md#amo-id-formats) verwenden (beginnend mit `s_kwcid`), das Reporting auf Kampagnen- und Anzeigengruppenebene für Kampagnen, Entwürfe und Experimente mit dem Wert „Performance Max“ unterstützt:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

     Wenn das Konto über eine serverseitige AMO ID-Implementierung verfügt und die Konto- oder Kampagneneinstellung &quot;[!UICONTROL Auto Upload]&quot; aktiviert ist, wird der Parameter automatisch hinzugefügt. Andernfalls müssen Sie es manuell hinzufügen. Siehe &quot;[Adobe Advertising-IDs verwendet von [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id-implement)&quot;.

   * Alle anderen [!DNL Google Ads]:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* Wenn der Advertiser keine Adobe Analytics-Integration hat, muss das Suffix Folgendes enthalten:

  `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* Landingpage-Suffixe auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Zur einfacheren Wartung verwenden Sie nur das Suffix auf Kontoebene, es sei denn, eine andere Nachverfolgung für einzelne Kontokomponenten ist erforderlich. Um ein Suffix auf Anzeigengruppenebene oder darunter zu konfigurieren, verwenden Sie den Editor des Anzeigennetzwerks.
>
>* (Dynamische Suchanzeigen; Werbetreibende mit Adobe Analytics und ohne Server-seitiges Tracking) Wenn Sie Tracking für den Reverse-Feed von Adobe Advertising an Analytics einbeziehen möchten, hängen Sie den AMO-ID-Tracking-Code an das Ende des Suffix der Landingpage auf Kontoebene an.

>[!MORELIKETHIS]
>
>* [Über Klick-Tracking-URL-Formate für den Konversionsverfolgungs-Service von Adobe Advertising](formats-click-tracking-about.md)
>* [AMO ID-Formate](/help/integrations/analytics/ids.md#amo-id-formats)
