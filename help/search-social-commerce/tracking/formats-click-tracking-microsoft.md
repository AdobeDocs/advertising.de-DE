---
title: Klick-Tracking-Formate für [!DNL Microsoft Advertising]
description: Informationen zu den Klick-Tracking-Formaten für [!DNL Microsoft Advertising] Konten.
exl-id: 725981db-1b9a-4c89-b95d-98d07ec99756
feature: Search Tracking
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# Klick-Tracking-Formate für [!DNL Microsoft Advertising]

Im Folgenden finden Sie die Basis-Tracking-Vorlage und das Suffix-Format der Landingpage (endgültiges URL-Suffix), für das Search, Social und Commerce erforderlich sind [!DNL Microsoft Advertising].

## Tracking-Vorlagenformate

### Such- und Zielgruppennetzwerke (außer Sitelinks)

Das folgende Format gilt für alle verfolgbaren Anzeigentypen in Such- und Zielgruppennetzwerken.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Beispiel:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Advertisers in Adobe Advertising.
>
>* Dieses Format gibt an, dass die Übergabe des Tokens für die Kampagne aktiviert ist (Standardeinstellung). Wenn die Tokenübergabe deaktiviert ist, ersetzen Sie `cq?` after `<advertiser_ID>` mit `c?`.
>
>* `{TargetId}` entspricht der ID a) des Suchbegriffs oder b) der Suchbegriff- und Remarketing-Liste (Zielgruppe), die die Anzeige ausgelöst hat (z. B. &quot;kwd-123:aud-456&quot;für einen Suchbegriff und eine Remarketing-Liste oder &quot;kwd-123&quot;nur für Suchbegriffe).

### Sitelinks

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Beispiel:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Advertisers in Adobe Advertising.
>
>* Dieses Format gibt an, dass die Übergabe des Tokens für die Kampagne aktiviert ist (Standardeinstellung). Wenn die Tokenübergabe deaktiviert ist, ersetzen Sie `cq?` after `<advertiser_ID>` mit `c?`.
>
>* `{TargetId}` entspricht der ID a) des Suchbegriffs oder b) der Suchbegriff- und Remarketing-Liste (Zielgruppe), die die Anzeige ausgelöst hat (z. B. &quot;kwd-123:aud-456&quot;für einen Suchbegriff und eine Remarketing-Liste oder &quot;kwd-123&quot;nur für Suchbegriffe).
>
>* `{adextensionid}` nicht verwendet.
>
>* (Sitelinks) Sie können sehen, welche Konversionen durch einen Klick auf einen Sitelink entstanden sind, indem Sie eine [!UICONTROL Transaction Report]. Die [!UICONTROL Link Type] Spaltenwert für einen Sitelink ist `sl:<Sitelink text>`, beispielsweise `sl:See Current Offers`.

### Shopping-Netzwerk

Die folgenden Formate gelten für Shopping-Anzeigen in Shopping-Netzwerken. Sie können eine Tracking-Vorlage auf Konto-, Kampagnen-, Anzeigengruppen- oder Produktgruppenebene angeben.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

Beispiel:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` ist eine Variable für die eindeutige ID des Advertisers in Adobe Advertising.
>
>* Dieses Format gibt an, dass die Übergabe des Tokens für die Kampagne aktiviert ist (Standardeinstellung). Wenn die Tokenübergabe deaktiviert ist, ersetzen Sie `cq?` after `<advertiser_ID>` mit `c?`.
>
>* `{TargetId}` entspricht der ID a) des Suchbegriffs oder b) der Suchbegriff- und Remarketing-Liste (Zielgruppe), die die Anzeige ausgelöst hat (z. B. &quot;kwd-123:aud-456&quot;für einen Suchbegriff und eine Remarketing-Liste oder &quot;kwd-123&quot;nur für Suchbegriffe).
>
>* (Optional) Anstatt Tracking-Vorlagen auf Konto-, Kampagnen-, Anzeigengruppen- oder Produktgruppenebene einzugeben, können Sie die Tracking-URL den Produktdaten innerhalb der [!DNL Microsoft Merchant Center] -Konto. Fügen Sie dazu die Tracking-URL sowie den Wert in die`link`&quot; oder &quot;`mobile_link`&quot; in einer benutzerdefinierten Spalte &quot;[bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0)&quot;im Produkt-Feed. Der Wert im`bingads_redirect`&quot; ersetzt die Werte im`link`&quot; und &quot;`mobile_link`&quot;. Die mit dieser Methode generierten URLs enthalten keine Tracking-Parameter, die in den Einstellungen für das Konto &quot;Search, Social, &amp; Commerce&quot;oder &quot;Kampagne&quot;angegeben sind.

## Formate für das Suffix von Landingpages (endgültiges URL-Suffix)

>[!NOTE]
>
>Die Suffixe der Landingpage auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Verwenden Sie zur einfacheren Wartung nur das Suffix auf Kontoebene, es sei denn, es ist eine unterschiedliche Verfolgung für einzelne Kontokomponenten erforderlich. Verwenden Sie den Editor des Werbenetzwerks, um ein Suffix auf Anzeigengruppenebene oder niedriger zu konfigurieren.

### Netzwerke für Suche und Zielgruppe

Konten, die das Adobe Advertising-Konversions-Tracking verwenden, müssen die Klick-ID des Anzeigennetzwerks enthalten (`msclkid` für [!DNL Microsoft Advertising]) im Suffix:

* Wenn der Advertiser über eine Adobe Analytics-Integration verfügt, muss das Suffix Folgendes enthalten:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Wenn der Advertiser keine Adobe Analytics-Integration hat, muss das Suffix Folgendes enthalten:

  `&ev_efid={msclkid}:G:s`

### Shopping-Netzwerk

Konten, die das Adobe Advertising-Konversions-Tracking verwenden, müssen die Klick-ID des Anzeigennetzwerks enthalten (`msclkid` für [!DNL Microsoft Advertising]) im Suffix:

* Wenn der Advertiser über eine Adobe Analytics-Integration verfügt, muss das Suffix Folgendes enthalten:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Wenn der Advertiser keine Adobe Analytics-Integration hat, muss das Suffix Folgendes enthalten:

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [Über Klick-Tracking-URL-Formate für den Adobe Advertising-Konversions-Tracking-Dienst](formats-click-tracking-about.md)
>* [AMO-ID-Formate](/help/integrations/analytics/ids.md#amo-id-formats)
