---
title: Einstellungen der Shopping-Anzeigenvorlage für Inventar-Feeds [!DNL Google Ads]
description: Verweisen Sie auf die Einstellungen für  [!DNL Google Ads] -Shopping-Anzeigenvorlagen für Inventar-Feeds.
exl-id: 36cbe719-f984-4456-8575-94b9d3e6094e
feature: Search Inventory Feeds
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Einstellungen der Shopping-Anzeigenvorlage für Inventar-Feeds [!DNL Google Ads]

Verwenden Sie Shopping-Anzeigenvorlagen, um Shopping-Anzeigen zu konfigurieren.

>[!NOTE]
>
>* Die folgenden Zeichen sind für die Bezeichnung von Spaltennamen und Modifikatornamen in der Vorlage reserviert und dürfen daher nicht als Text in allen Attributfeldern verwendet werden: `[ ] < > `

## \[Vor allen Registerkarten\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[Linker Bereich\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

<!-- **[!UICONTROL Campaign Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-only.md}}

<!-- **[!UICONTROL Campaign Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-method.md}}

**[!UICONTROL Campaign Tracking Template]:** (Optional für Vorlagen für Client-Feed-Dateien) Die Tracking-Vorlage auf Kampagnenebene, die alle Weiterleitungs- und Tracking-Parameter für ausgelagerte Domains angibt und die endgültige URL in einen Parameter einbettet. Dieser Wert überschreibt die Einstellung auf Kontoebene, aber Tracking-Vorlagen auf detaillierteren Ebenen (mit Keyword als am detailliertesten) überschreiben diesen Wert.

Verwenden Sie für das Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; enthalten, das [Tracking-Vorlagenformat für Google Ads-Shopping-Kampagnen](/help/search-social-commerce/tracking/formats-click-tracking-google.md). Wenn das gesamte Konto Shopping-Anzeigen gewidmet ist, können Sie stattdessen eine Tracking-Vorlage auf Kontoebene definieren.

Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]:** Die Kunden-ID des Händlerkontos, dessen Produkte für die Kampagne verwendet werden.

**[!UICONTROL Sales Country]:** Das Land, in dem die Kampagnenprodukte verkauft werden. Weil Produkte verknüpft sind
Bei Zielländern bestimmt diese Einstellung, für welche Produkte in der Kampagne geworben wird.

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Networks]:** Die Netzwerke, in denen Anzeigen geschaltet werden. *[!UICONTROL Search]* ist bereits ausgewählt. Um Angebote in Angebote für [!DNL Google Ads] Suchpartner aufzunehmen, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Search partners]**.

**[!UICONTROL Campaign Priority]:** Die Priorität, mit der die Kampagne verwendet wird, wenn mehrere Kampagnen für das werben.
Gleiches Produkt: *[!UICONTROL Low]* (Standard für neue Kampagnen), *[!UICONTROL Medium]* oder *[!UICONTROL High]*. Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, verwendet das Werbenetzwerk
Die Kampagnenpriorität wird zuerst festgelegt, welche Kampagne (und das zugehörige Angebot) für die Anzeigenauktion infrage kommt. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot geeignet.

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

**[!UICONTROL Has EU Political Ads]:**(Nur [!DNL Google Ads]- und [!DNL Microsoft Advertising]-Kampagnen; anwendbar auf Kampagnen, die sich an Zielgruppen in der Europäischen Union (EU) richten Unabhängig davon, ob die Kampagne politische Werbung gemäß den Anforderungen für in der Europäischen Union gemäß der EU-Verordnung 2024/90 geschaltete Anzeigen enthält: *[!UICONTROL Yes]* oder *[!UICONTROL No]*.

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Optional) Eine Tracking-Vorlage auf Anzeigengruppenebene, die alle off-landing-domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen Parameter einbettet. Dieser Wert überschreibt die Einstellungen auf Konto- und Kampagnenebene, aber Tracking-Vorlagen auf detaillierteren Ebenen überschreiben diesen Wert.

Für das Adobe Advertising-Konversionstracking müssen Sie keinen Wert eingeben. Der Wert auf Kampagnenebene ist ausreichend.

Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]:** Die standardmäßige, alle einbeziehende Produktgruppe, &quot;[!UICONTROL All products]&quot;. Sie können diese übergeordnete Produktgruppe nicht löschen, sie wird jedoch automatisch gelöscht, wenn alle unteren Ebenen im Feed fehlen.

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** (Einheiten ohne untergeordnete Produktgruppen; optional) Die Tracking-Vorlage für das Produkt
Gruppe, die alle Umleitungs- und Tracking-Parameter für die Off-Landing-Domain angibt und die endgültige URL in einen [!DNL ValueTrack] einbettet. Diese Vorlage überschreibt Vorlagen auf höheren Ebenen.

Für das Adobe Advertising-Konversionstracking müssen Sie keinen Wert eingeben. Der Wert auf Kampagnenebene ist ausreichend.

Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein.

**[!UICONTROL Initial Bid]:** Das erste Gebot für jede Anzeige.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [Über die Automatisierung der Anzeigenverwaltung mithilfe von Inventar-Feeds](../inventory-feeds-about.md)
>* [Verwalten von Modifikatoren](../modifiers-manage.md)
>* [Verwalten von Inventardaten-Feed-Dateien](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Verbreiten von Feed-Daten über Vorlagen](../feed-data-propagate.md)
>* [Kampagnendaten aus Inventar-Feeds in Werbenetzwerke posten](../propagated-data-post.md)
