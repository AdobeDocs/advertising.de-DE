---
title: Klick-Tracking-Formate für [!DNL Google Ads]
description: Informationen zu den Klick-Tracking-Formaten für [!DNL Google Ads] Konten.
exl-id: 68f6da43-3430-4c0a-9369-937fa52c071a
feature: Search Tracking
source-git-commit: ceb2fc07eb5116b3a2bb01cf72fd779f78bba1f0
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Klick-Tracking-Formate für [!DNL Google Ads]

Im Folgenden finden Sie die Basis-Tracking-Vorlage und das Suffix-Format der Landingpage (endgültiges URL-Suffix), für das Search, Social und Commerce erforderlich sind [!DNL Google Ads].

## Tracking-Vorlagenformate

### Such-/Anzeigenetzwerk, einschließlich Sitelinks

Das folgende Format gilt für alle verfolgbaren Anzeigentypen in Such- und Anzeigennetzwerken sowie für Sitelinks.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Beispiel:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Advertisers innerhalb von Adobe Advertising.
>
>* Dieses Format gibt an, dass die Übergabe des Tokens für die Kampagne aktiviert ist (Standardeinstellung). Wenn die Tokenübergabe deaktiviert ist, ersetzen Sie `cq?` after `<advertiser_ID>` mit `c?`.
>
>* Die [!DNL ValueTrack] Parameter, die die endgültigen URLs in Tracking-Vorlagen angeben, müssen entweder `{lpurl}` oder `!{unescapedurl}`.
>
>* (Textanzeigen) Wenn Sie ein Angebot nach Keyword einreichen, wird der Parameter `ev_pl` (für Platzierungen) keinen Wert hat. Wenn Sie ein Angebot nach Platzierung machen, `ev_ln` (für Suchbegriffe) keinen Wert hat. Wenn Sie Gebote nach Anzeigengruppe oder einer anderen Dimension abgeben, `ev_ln` und `ev_pl` keine Werte haben.
>
>* (Dynamische Suchanzeigen) `{keyword}` gibt den Ausdruck des dynamischen Suchziels an, z. B. `_cat:[VALUE]` oder `_url:[VALUE]`.
>
>* (Dynamische Suchanzeigen) [!DNL Google Ads] bestimmt dynamisch die endgültige URL, sodass Sie keine eingeben müssen.
>
>* (Sitelinks) Sie können sehen, welche Konversionen durch einen Klick auf einen Sitelink entstanden sind, indem Sie eine [!UICONTROL Transaction Report]. Die [!UICONTROL Link Type] Spaltenwert für einen Sitelink ist `sl:<Sitelink text>`, beispielsweise `sl:See Current Offers`.

### Shopping-Netzwerk

Das folgende Format gilt für Shopping-Anzeigen und Produktgruppen in Shopping-Netzwerken. Sie können eine Tracking-Vorlage auf Konto-, Kampagnen-, Anzeigengruppen- oder Produktgruppenebene angeben.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Beispiel:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Advertisers innerhalb von Adobe Advertising.
>
>* Dieses Format gibt an, dass die Übergabe des Tokens für die Kampagne aktiviert ist (Standardeinstellung). Wenn die Tokenübergabe deaktiviert ist, ersetzen Sie `cq?` after `<advertiser_ID>` mit `c?`.
>
>* Die [!DNL ValueTrack] Parameter, die die endgültigen URLs in Tracking-Vorlagen angeben, müssen entweder `{lpurl}` oder `!{unescapedurl}`.
>
>* [!DNL Google Ads] verwendet Produkt-URLs im Google Merchant Center-Feed als endgültige URLs, sodass Sie keine endgültigen URLs für Ihre Produktdaten oder Produktgruppen eingeben müssen.
>
>* Sie können sehen, welche Konversionen durch einen Klick auf eine Shopping-Anzeige entstanden sind, indem Sie eine [!UICONTROL Transaction Report]. Die [!UICONTROL Link Type] -Spaltenwert für eine Produktanzeige ist pla:`<product ID>`, beispielsweise `pla:8525822`.

## Formate für das Suffix von Landingpages (endgültiges URL-Suffix)

Konten, die das Adobe Advertising-Konversions-Tracking verwenden, müssen die Klick-ID des Anzeigennetzwerks enthalten (`gclid` für [!DNL Google Ads]) im Suffix:

* Wenn der Advertiser über eine Adobe Analytics-Integration verfügt, muss das Suffix eines der folgenden enthalten:

   * [!DNL Google Ads] Konten, die die neueste [AMO-ID-Format](/help/integrations/analytics/ids.md#amo-id-formats) (beginnt mit `s_kwcid`), das Berichte auf Kampagnen- und Anzeigengruppenebene für Performance-Max-Kampagnen sowie Entwürfe und Experimentkampagnen unterstützt:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

     Wenn das Konto über eine serverseitige AMO-ID-Implementierung verfügt und das Konto oder die Kampagneneinstellung &quot;[!UICONTROL Auto Upload]&quot; aktiviert ist, wird der Parameter automatisch hinzugefügt. Andernfalls müssen Sie sie manuell hinzufügen. Siehe &quot;[Von verwendete Adobe Advertising-IDs [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id-implement).&quot;

   * Alle anderen [!DNL Google Ads] Konten:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* Wenn der Advertiser keine Adobe Analytics-Integration hat, muss das Suffix Folgendes enthalten:

  `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* Die Suffixe der Landingpage auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Verwenden Sie zur einfacheren Wartung nur das Suffix auf Kontoebene, es sei denn, es ist eine unterschiedliche Verfolgung für einzelne Kontokomponenten erforderlich. Verwenden Sie den Editor des Werbenetzwerks, um ein Suffix auf Anzeigengruppenebene oder niedriger zu konfigurieren.
>
>* (Dynamische Suchanzeigen; Advertiser mit Adobe Analytics und ohne serverseitiges Tracking) Wenn Sie das Tracking für den Rückwärtsfeed von Adobe Advertising zu Analytics einbeziehen möchten, hängen Sie den AMO-ID-Trackingcode an das Ende des Suffixes der Landingpage auf Kontoebene an.

>[!MORELIKETHIS]
>
>* [Über Klick-Tracking-URL-Formate für den Adobe Advertising-Konversions-Tracking-Dienst](formats-click-tracking-about.md)
>* [AMO-ID-Formate](/help/integrations/analytics/ids.md#amo-id-formats)
