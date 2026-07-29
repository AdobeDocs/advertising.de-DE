---
title: '[!DNL Baidu] Kampagneneinstellungen'
description: Verweisen Sie auf die Einstellungen für  [!DNL Baidu] -Kampagnen.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 3a5c2507f3acb08419e143ba906cf55df2496d0f
workflow-type: tm+mt
source-wordcount: 309
ht-degree: 0%

---

# [!DNL Baidu] Kampagneneinstellungen

## \[Seitenanfang]

**[!UICONTROL Campaign Name]:** Ein Kampagnenname, der innerhalb des Kontos eindeutig ist.

**[!UICONTROL Status]:** Der Anzeigestatus der Kampagne: *Aktiv* oder *Paused*. Der Standardwert für neue Anzeigenkampagnen lautet *Aktiv*.

## Registerkarte [!UICONTROL Basic Settings]

*Nur neue Kampagnen*

**[!UICONTROL Network]:** Das Werbenetzwerk.

**[!UICONTROL Account]:** Das Netzwerkkonto der Anzeige.

**[!UICONTROL Campaign Type]:** Wo werden Anzeigen geschaltet und welche Anzeigentypen kann die Kampagne enthalten. Die einzige Option ist *Nur Netzwerk durchsuchen*.

## Registerkarte [!UICONTROL Campaign Details]

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Contains EU Political Ads]:**(Gilt für Kampagnen, die sich an Zielgruppen in der Europäischen Union (EU) richten) Gibt an, ob die Kampagne politische Werbung gemäß den Anforderungen für in der Europäischen Union gemäß der EU-Verordnung 2024/90 geschaltete Anzeigen enthält: *[!UICONTROL Yes]* oder *[!UICONTROL No]*.

## Registerkarte [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

<!--VERIFY OPTIMIZATION BEHAVIOR -->**[!UICONTROL Bid strategy]:** Die Bid-Strategie für die Kampagne:

* *[!UICONTROL Maximize Conversions]:* Das Werbenetzwerk - nicht Search, Social und Commerce - optimiert Angebote, um Konversionen zu maximieren. Geben Sie optional einen **[!UICONTROL Target CPA]** ein (Kosten pro Akquise). **Hinweis** Verwenden Sie diese Option für Kampagnen in Portfolios mit Optimierung auf Kampagnenebene. In Portfolios mit Optimierung auf Kampagnenebene optimieren Search, Social und Commerce die Target-CPA.

* *[!UICONTROL Maximize Conversion Value]:* Das Werbenetzwerk - nicht Search, Social und Commerce - optimiert Angebote, um den Konversionswert zu maximieren. Geben Sie optional einen **[!UICONTROL Target Return on Ad Spend]** (ROAS) als Prozentsatz ein. **Hinweis** Verwenden Sie diese Option für Kampagnen in Portfolios mit Optimierung auf Kampagnenebene. In Portfolios mit Optimierung auf Kampagnenebene optimieren Search, Social und Commerce die Target-ROAS.

## Registerkarte [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** Die Sprache der Anzeige, die mit der Sprache der Websites übereinstimmen sollte, auf denen Ihre Anzeige erscheinen kann. Das Anzeigennetzwerk bestimmt die Sprache eines Benutzers aus verschiedenen Signalen, einschließlich der Abfrage des Benutzers, des Landes des Herausgebers und der Spracheinstellung des Benutzers.

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

## Registerkarte [!UICONTROL Additional Campaign Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-baidu.md}}

### Registerkarte [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** (Nur für [!UICONTROL EF Redirect]) Die Ebene, auf der Klicks und Umsatz verfolgt werden sollen, indem eine Umleitung hinzugefügt wird (falls relevant) und Parameter an die entsprechenden URLs angehängt werden:

* *[!UICONTROL Keyword]:* Zum Nachverfolgen von Daten nur auf Keyword-Ebene.

* *[!UICONTROL Creative]:* Zum Nachverfolgen von Daten nur auf Anzeigenebene (kreativ).

* *[!UICONTROL Creative and Keyword]:* Verfolgen Sie Daten sowohl auf Anzeigenebene (kreativ) als auch auf Schlüsselwortebene.

**[!UICONTROL Enable conversion reporting in Adobe Analytics]:** Fügt den Anzeigen im Konto oder in der Kampagne einen URL-Parameter für das Konversions-Tracking hinzu.

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

<!--

Not there as of 7/22 -- what's going on here? If we're removing it, then I need to update many references throughout the whole doc:

[               **[!UICONTROL Auto Upload]:**      ]

{{$include /help/_includes/auto-upload.md}}

-->

>[!MORELIKETHIS]
>
>* [Kampagnen verwalten](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
