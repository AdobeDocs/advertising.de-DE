---
title: '[!UICONTROL Google AI Max Search Term Combination Report]'
description: Erfahren Sie mehr über die [!UICONTROL Google AI Max Search Term Combination Report].
feature: Search Reports, Search Specialty Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
  - id: 7de556b7-2c2a-599d-853b-8c282aafa6e3
    internal-label: Search Specialty Reports
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%
---
# [!UICONTROL Google AI Max Search Term Combination Report]

*Gilt für [!DNL Google Ads] Konten, bei denen Kampagnen nur für KI-Max aktiviert sind*

Die [!UICONTROL Google AI Max Search Term Combination Report] zeigt, wie bestimmte Suchabfragen KI-generierten Überschriften und dynamischen Landingpages sowie Konversionsaktionen für Anzeigen in [!DNL Google Ads AI Max]-aktivierten Kampagnen innerhalb bestimmter Konten zugeordnet werden. Der Bericht umfasst zwei Blätter:

* [!UICONTROL AI Max Search Term]: Die Leistung bestimmter Anzeigenkombinationen und Landingpages auf der Grundlage von Suchvorgängen innerhalb des Suchnetzwerks. Das Blatt enthält Impressions-, Klicks- und Kostendaten sowie optionale [!DNL Google Ads]-Tracking-Konversionsmetriken, die in den Berichtseinstellungen angegeben sind. Standardmäßig enthalten die Daten eine Zeile für jede Suchbegriff-, Überschriften- und Landingpage-Kombination, die mindestens eine Impression im angegebenen Datenbereich erhalten hat. Die Zeilen werden standardmäßig nach Kampagne und dann nach einer anderen Spalte Ihrer Wahl in aufsteigender Reihenfolge sortiert.

  Verwenden Sie dieses Blatt, um die Absicht und die Leistung der resultierenden Anzeigenelemente pro Abfrage zu analysieren, damit Sie zuverlässige negative Keyword-Listen erstellen können.

* &#x200B;<!-- [!UICONTROL Search Term x Conversion Action] sheet? -->[!UICONTROL AI Max Search Term #1] Blatt: [!DNL Google Ads] Konversionsdaten nach Konversionsaktion für jeden Suchbegriff und Übereinstimmungstyp. Jede Zeile enthält die Konversionsaktion, die Anzahl der Konversionen und den Konversionswert sowie alle anderen optionalen [!DNL Google Ads]-Tracking-Konversionsmetriken, die in den Berichtseinstellungen angegeben sind. Standardmäßig enthalten die Daten eine Zeile für jede Kombination aus Suchbegriff und Konversionsaktion im angegebenen Datenbereich. Die Zeilen befinden sich in der gleichen Reihenfolge wie die Zeilen auf dem ersten Blatt.

  <!-- Should it be this?  The sheet includes the number of conversions and the conversion value, all conversions and the all conversions value, and cross-device conversions. -->

  In diesem Blatt erfahren Sie, wie die einzelnen Suchbegriffe zu den Konversionen geführt haben, aufgeschlüsselt nach Konversionsaktionen.

<!-- We're pulling data directly from GGL and not storing it, so no limitations on our end WRT date range. -->

## Standardspalten

Beschreibungen aller standardmäßigen und benutzerdefinierten Spalten finden Sie unter [Berichtsspalten für Sonderberichte](specialty-report-columns.md).

<!-- VERIFY -- probably more will be included by default -->

* [!UICONTROL Event Date]
* [!UICONTROL Account Name]
* [!UICONTROL Network Campaign ID]
* [!UICONTROL Campaign Name]
* [!UICONTROL Ad Group Name]
* [!UICONTROL Search Term]
* [!UICONTROL Headline 1]
* [!UICONTROL Headline 2]
* [!UICONTROL Landing Page]
* [!UICONTROL Impressions]
* [!UICONTROL Clicks]
* [!UICONTROL Cost]
* [!UICONTROL Conversion Action] (wird automatisch in die [!UICONTROL AI Max Search Term #1] aufgenommen, auch wenn Sie sie nicht explizit einbeziehen)
* [!UICONTROL Conversions] (wird automatisch in die [!UICONTROL AI Max Search Term #1] aufgenommen, auch wenn Sie sie nicht explizit einbeziehen)
* [!UICONTROL Conversions Value] (wird automatisch in die [!UICONTROL AI Max Search Term #1] aufgenommen, auch wenn Sie sie nicht explizit einbeziehen)

>[!MORELIKETHIS]
>
>* [Über Spezialberichte](specialty-report-about.md)
>* [Terminierte Berichte verwalten](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [Einstellungen für Spezialberichte](specialty-report-settings.md)
>* [Berichtsspalten für Sonderberichte](specialty-report-columns.md)
