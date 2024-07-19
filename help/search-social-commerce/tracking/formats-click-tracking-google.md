---
title: Klick-Tracking-Formate für  [!DNL Google Ads]
description: Erfahren Sie mehr über die Klick-Tracking-Formate für [!DNL Google Ads] Konten.
exl-id: d09c3b4e-1274-45fb-abb6-dddfe60f1477
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Klick-Tracking-Formate für [!DNL Google Ads]

Im Folgenden finden Sie die Basis-Tracking-Vorlage und die Suffix-Formate für Landingpages (endgültiges URL-Suffix), die für Search, Social und Commerce für [!DNL Google Ads] erforderlich sind.

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
>* Dieses Format gibt an, dass die Übergabe des Tokens für die Kampagne aktiviert ist (Standardeinstellung). Wenn die Übergabe des Tokens deaktiviert ist, ersetzen Sie `cq?` nach `<advertiser_ID>` durch `c?`.
>
>* Die Parameter [!DNL ValueTrack] zur Angabe der endgültigen URLs in Tracking-Vorlagen müssen entweder `{lpurl}` oder `!{unescapedurl}` sein.
>
>* (Textanzeigen) Wenn Sie ein Angebot nach Keyword erstellen, hat der Parameter `ev_pl` (für Platzierungen) keinen Wert. Wenn Sie ein Angebot nach Platzierung machen, hat `ev_ln` (für Suchbegriffe) keinen Wert. Wenn Sie ein Angebot nach Anzeigengruppe oder einer anderen Dimension einreichen, haben sowohl `ev_ln` als auch `ev_pl` keine Werte.
>
>* (Dynamische Suchanzeigen) `{keyword}` gibt den Ausdruck für das dynamische Suchziel an, z. B. `_cat:[VALUE]` oder `_url:[VALUE]`.
>
>* (Dynamische Suchanzeigen) [!DNL Google Ads] bestimmt dynamisch die endgültige URL, sodass Sie keine eingeben müssen.
>
>* (Sitelinks) Sie können sehen, welche Konversionen durch einen Klick auf einen Sitelink entstanden sind, indem Sie eine &quot;[!UICONTROL Transaction Report]&quot; generieren. Der Spaltenwert [!UICONTROL Link Type] für einen Sitelink ist `sl:<Sitelink text>`, z. B. `sl:See Current Offers`.

### Shopping-Netzwerk

Das folgende Format gilt für Shopping-Anzeigen und Produktgruppen in Shopping-Netzwerken. Sie können eine Tracking-Vorlage auf Konto-, Kampagnen-, Anzeigengruppen- oder Produktgruppenebene angeben.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Beispiel:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Advertisers innerhalb von Adobe Advertising.
>
>* Dieses Format gibt an, dass die Übergabe des Tokens für die Kampagne aktiviert ist (Standardeinstellung). Wenn die Übergabe des Tokens deaktiviert ist, ersetzen Sie `cq?` nach `<advertiser_ID>` durch `c?`.
>
>* Die Parameter [!DNL ValueTrack] zur Angabe der endgültigen URLs in Tracking-Vorlagen müssen entweder `{lpurl}` oder `!{unescapedurl}` sein.
>
>* [!DNL Google Ads] verwendet Produkt-URLs im Google Merchant Center-Feed als endgültige URLs, sodass Sie keine endgültigen URLs für Ihre Produktdaten oder Produktgruppen eingeben müssen.
>
>* Sie können sehen, welche Konversionen durch einen Klick auf eine Shopping-Anzeige entstanden sind, indem Sie eine [!UICONTROL Transaction Report] generieren. Der Spaltenwert [!UICONTROL Link Type] für eine Produktanzeige ist platziert:`<product ID>`, z. B. `pla:8525822`.

## Formate für das Suffix von Landingpages (endgültiges URL-Suffix)

Konten, die das Adobe Advertising-Konversions-Tracking verwenden, müssen die Klick-ID des Anzeigennetzwerks (`gclid` für [!DNL Google Ads]) im Suffix enthalten:

* Wenn der Advertiser über eine Adobe Analytics-Integration verfügt, muss das Suffix eines der folgenden enthalten:

   * [!DNL Google Ads] Konten, die das neueste [AMO-ID-Format](/help/integrations/analytics/ids.md#amo-id-formats) verwenden (beginnend mit `s_kwcid`), das Berichte auf Kampagnen- und Anzeigengruppenebene für Performance-Max-Kampagnen, -Entwürfe und -Experimentkampagnen unterstützt:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

     Wenn das Konto über eine serverseitige AMO-ID-Implementierung verfügt und die Konto- oder Kampagneneinstellung &quot;[!UICONTROL Auto Upload]&quot; aktiviert ist, wird der Parameter automatisch hinzugefügt. Andernfalls müssen Sie sie manuell hinzufügen. Siehe &quot;[Von  [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id-implement) verwendete Adobe Advertising-IDs&quot;.

   * Alle anderen [!DNL Google Ads]-Konten:

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
