---
title: '''[!DNL Microsoft® Ads] Einkaufs- und Vorlageneinstellungen für Inventar-Feeds'
description: Verweisen Sie auf die Einstellungen für [!DNL Microsoft® Ads] Shopping-Anzeigenvorlagen für Inventar-Feeds.
exl-id: 64d0092a-bd63-48f4-8e15-f5585f7a022a
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# [!DNL Microsoft® Ads] Einkaufs- und Vorlageneinstellungen für Inventar-Feeds

Verwenden Sie Shopping-Anzeigenvorlagen, um Shopping-Anzeigen zu konfigurieren.

>[!NOTE]
>
>* Die folgenden Zeichen sind in der Vorlage für die Bezeichnung von Spaltennamen und Modifikatornamen reserviert und sind daher in allen Attributfeldern als Text verboten:  `[ ] < > `


## \[Über allen Registerkarten\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[linker Bereich\]

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

**[!UICONTROL Campaign Tracking Template]:** (Optional für Vorlagen für Client-Feed-Dateien) Die Tracking-Vorlage auf Kampagnenebene, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen Parameter einbettet. Dieser Wert überschreibt die Einstellung auf Kontoebene, aber Tracking-Vorlagen auf detaillierteren Ebenen (mit Keyword als granularster) überschreiben diesen Wert.

* Für das Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload],&quot; einen der folgenden Schritte ausführen&quot;:

   * (Empfohlen) Verwenden Sie die [Tracking-Vorlagenformat für Microsoft® Shopping-Kampagnen](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md). Wenn das gesamte Konto für Shopping-Anzeigen vorgesehen ist, können Sie stattdessen eine Tracking-Vorlage auf Kontoebene definieren.

   * Wenn Sie stattdessen einen Wert für jedes Produkt in den Feed einschließen, indem Sie die[!DNL bingads_redirect]&quot; (mithilfe der [korrektes Format](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)), geben Sie dann den Parameter ein. `{lpurl}`. Sie können optional Umleitungen und Tracking von Drittanbietern zum `{lpurl}` -Parameter.

* Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein.

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]:** Die Kunden-ID des Händlers, dessen Produkte für die Kampagne verwendet werden.

**[!UICONTROL Sales Country]:** Das Land, in dem die Produkte der Kampagne verkauft werden. Da Produkte mit Zielländern verknüpft sind, bestimmt diese Einstellung, welche Produkte in der Kampagne beworben werden.

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

**[!UICONTROL Campaign Priority]:** Die Priorität, mit der die Kampagne verwendet wird, wenn mehrere Kampagnen für dasselbe Produkt werben: *[!UICONTROL Low]* (Standardeinstellung für neue Kampagnen), *[!UICONTROL Medium]* oder *[!UICONTROL High]*. Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, verwendet das Werbenetzwerk zuerst die Kampagnenpriorität, um zu bestimmen, welche Kampagne (und welches zugehörige Angebot) für die Anzeigenauktion infrage kommt. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot berechtigt.

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** (Optional) Eine Tracking-Vorlage auf Anzeigengruppenebene, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in einen Parameter einbettet. Dieser Wert überschreibt die Einstellungen auf Konto- und Kampagnenebene, aber Tracking-Vorlagen auf detaillierteren Ebenen überschreiben diesen Wert.

Für das Adobe Advertising-Konversions-Tracking müssen Sie keinen Wert eingeben. Der Wert auf Kampagnenebene reicht aus.

Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein.

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]:** Die standardmäßige, umfassende Produktgruppe, &quot;[!UICONTROL All products].&quot; Sie können diese übergeordnete Produktgruppe nicht löschen, sie wird jedoch automatisch gelöscht, wenn alle unteren Ebenen im Feed fehlen.

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** (Einheiten ohne untergeordnete Produktgruppen; optional) Die Tracking-Vorlage für die Produktgruppe, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die endgültige URL in eine [!DNL ValueTrack] -Parameter. Diese Vorlage überschreibt Vorlagen auf höheren Ebenen.

Für das Adobe Advertising-Konversions-Tracking müssen Sie keinen Wert eingeben. Der Wert auf Kampagnenebene reicht aus.

Geben Sie für Umleitungen und Tracking von Drittanbietern einen Wert ein.

**[!UICONTROL Initial Bid]:** Das anfängliche Gebot für jede Anzeige.

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [Über die Automatisierung des Anzeigen-Managements mithilfe von Inventar-Feeds](../inventory-feeds-about.md)
>* [Verwalten von Modifikatoren](../modifiers-manage.md)
>* [Verwalten von Bestandsdaten-Feed-Dateien](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [Feed-Daten über Vorlagen übertragen](../feed-data-propagate.md)
>* [Posten von Kampagnendaten aus Inventar-Feeds in Werbenetzwerke](../propagated-data-post.md)
