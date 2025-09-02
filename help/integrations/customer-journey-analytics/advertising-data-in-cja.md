---
title: Adobe Advertising-Metriken und -Dimensionen in Customer Journey Analytics
description: Referenzieren Sie die in Customer Journey Analytics verfügbaren Adobe Advertising-Metriken und -Dimensionen.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: c3836d8af50061701434790b2bd9214df29e8a01
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Adobe Advertising-Metriken und -Dimensionen in Customer Journey Analytics

*Werbetreibende mit einer Adobe Advertising-Customer Journey Analytics-Integration*

Adobe Advertising übergibt Traffic-Metriken und -Dimensionen täglich an [!DNL Customer Journey Analytics]. [!DNL Web SDK] erfasst Clickthroughs und Viewthroughs für Adobe Advertising in Echtzeit und übergibt sie an Customer Journey Analytics.

## Traffic-Metriken in Adobe Advertising

<!-- Verify column names -->

>[!NOTE]
>
>* „XDM-Feldname“ ist der Feldname in Adobe Experience Platform.
>* „XDM-Feldanzeigename“ gibt den Anzeigenamen in Customer Journey Analytics an.

| Adobe Advertising-Feldname | XDM-Feldname | Anzeigename des XDM-Felds | Source |
|------------------------------|----------------|------------------------|--------|
| Datum | Datum | Alle | |
| AMO-ID | skacid | ADOBE ADVERTISING ID | Alle |
| AMO-Impressionen | adobe_advertising_impressions | Adobe Advertising Impressions | Alle |
| AMO-Klicks | adobe_advertising_clicks | Adobe Advertising-Klicks | Alle |
| AMO-Kosten | adobe_advertising_cost | Adobe Advertising-Kosten | Alle |
| Währungs-Code | Währung | Währung | Alle |
| AMO-Ansichten | adobe_advertising_views | Adobe Advertising-Ansichten | Ad Cloud DSP |
| 25 % vollständige AMO-Ansichten | adobe_advertising_views_25_pct | 25 % vollständige Adobe Advertising-Ansichten | Ad Cloud DSP |
| 50 % vollständige AMO-Ansichten | adobe_advertising_views_50_pct | 50 % vollständige Adobe Advertising-Ansichten | Ad Cloud DSP |
| 75 % vollständige AMO-Ansichten | adobe_advertising_views_75_pct | 75 % vollständige Adobe Advertising-Ansichten | Ad Cloud DSP |
| 100 % vollständige AMO-Ansichten | adobe_advertising_views_100_pct | 100 % vollständige Adobe Advertising-Ansichten | Ad Cloud DSP |
| AMO Minuten angesehen | adobe_advertising_minutes_viewed | Adobe Advertising Minuten angesehen | Ad Cloud DSP |
| Anzeigbare AMO-Impressionen | adobe_advertising_viewable_impressions | Anzeigbare Adobe Advertising-Impressionen | Ad Cloud DSP |
| Nicht anzeigbare AMO-Impressionen | adobe_advertising_not_viewable_impressions | Nicht anzeigbare Adobe Advertising-Impressionen | Ad Cloud DSP |
| Messbare AMO-Impressionen | adobe_advertising_measurement_impressions | Messbare Impressionen in Adobe Advertising | Ad Cloud DSP |

<!--
| Adobe Advertising Landing Page Views | adobe_advertising_landing_page_views | Adobe Advertising Landing Page Views | Meta Only |
| Adobe Advertising App Events | adobe_advertising_app_events | Adobe Advertising App Events | Meta Only |
| Adobe Advertising Engagements | adobe_advertising_engagements | Adobe Advertising Engagements | Meta Only |
| Adobe Advertising Ad Platform Conversions | adobe_advertising_ad_platform_conversions | Adobe Advertising Ad Platform Conversions | Meta Only |
| Adobe Advertising App Installs | adobe_advertising_app_installs | Adobe Advertising App Installs | Meta Only |
| Adobe Advertising Ad Platform Conversion Value | adobe_advertising_ad_platform_conversion_value | Adobe Advertising Ad Platform Conversion Value | Meta Only |
| Adobe Advertising Ad Platform Leads | adobe_advertising_ad_platform_leads | Adobe Advertising Ad Platform Leads | Meta Only |
| Adobe Advertising Page Like | adobe_advertising_page_like | Adobe Advertising Page Like | Meta Only |
| Adobe Advertising Phone Calls | adobe_advertising_phone_calls | Adobe Advertising Phone Calls | Meta Only |
| Adobe Advertising Messages | adobe_advertising_messages | Adobe Advertising Messages | Meta Only |
-->

## Adobe Advertising-Dimensionen

>[!NOTE]
>
>* „XDM-Feld“ ist der Feldname in Adobe Experience Platform.
>* „XDM-Feldanzeigename“ gibt den Anzeigenamen in Customer Journey Analytics an.

| Adobe Advertising-Feldname | XDM-Feldname | Anzeigename des XDM-Felds | Source |
|------------------------------|----------------|------------------------|--------|
| Schlüssel | skacid | ADOBE ADVERTISING ID |
| Werbeplattform | adobe_advertising_ad_platform | Adobe Advertising Ad Platform |
| Konto | adobe_advertising_account | Adobe Advertising-Konto |
| Campaign | adobe_advertising_campaign | Adobe Advertising Campaign |
| Anzeigengruppe | adobe_advertising_ad_group | Adobe Advertising-Anzeigengruppe |
| Schlüsselwort | adobe_advertising_keyword | Adobe Advertising-Schlüsselwort |
| Anzeige | adobe_advertising_ad | Adobe Advertising-Anzeige |
| Platzierung | adobe_advertising_placement | Platzierung in Adobe Advertising |
| Übereinstimmungstyp | adobe_advertising_match_type | Adobe Advertising-Übereinstimmungstyp |
| Anzeigentitel | adobe_advertising_ad_title | Adobe Advertising-Anzeigentitel |
| Anzeigenbeschreibung | adobe_advertising_ad_description | Adobe Advertising-Anzeigenbeschreibung |
| Ziel-URL hinzufügen | adobe_advertising_ad_destination_url | Ziel-URL der Adobe Advertising-Anzeige |
| Anzeige-URL | adobe_advertising_ad_display_url | Adobe Advertising Anzeigenansichts-URL |
| Gerät | adobe_advertising_device | Adobe Advertising Device |
| Übereinstimmungstyp des Schlüsselworts | adobe_advertising_keyword_matchType | Adobe Advertising-Schlüsselwort MatchType |
| Netzwerk | adobe_advertising_network | Adobe Advertising-Netzwerk |
| Ad-Typ | adobe_advertising_ad_type | Adobe Advertising Ad Type |
| Produktzielgruppe | adobe_advertising_product_target | Adobe Advertising Product Target |
| Landing-Typ | adobe_advertising_landing_type | Adobe Advertising Landing Type |
| Optimierung | adobe_advertising_optimization | Adobe Advertising-Optimierung |

>[!MORELIKETHIS]
>
>* [Übersicht](overview.md)
>* [Voraussetzungen](prerequisites.md)
>* [Adobe Advertising-IDs verwendet von [!DNL Customer Journey Analytics]](ids.md)
