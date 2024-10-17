---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: Erfahren Sie mehr über die [!UICONTROL Forecast Accuracy (Actuals) Report], einschließlich der Datenspalten.
exl-id: 659e11c7-5fed-4d91-a73f-7c435d36634f
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Der [!UICONTROL Forecast Accuracy (Actuals) Report]

Dieser Bericht zeigt die tatsächlichen Impressions-, Klick-, Kosten- und Umsatzdaten aus dem Werbenetzwerk nach Tag für jedes Portfolio.

## Verfügbare Spalten

Im Folgenden finden Sie die Spalten, die automatisch in den einzelnen Berichten enthalten sind. Sie können keine zusätzlichen Spalten hinzufügen.

| Spalte | Standard? | Beschreibung |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | Standard | Der Name der Portfoliogruppe, zu der das Portfolio gehört. |
| [!UICONTROL Portfolio ID] | Standard | Die numerische Portfolio-ID. |
| [!UICONTROL EF Portfolio Group ID] | Standard | Die numerische ID für die Portfoliogruppe, zu der das Portfolio gehört. |
| [!UICONTROL Portfolio] | Standard | Das Portfolio. |
| [!UICONTROL Portfolio Status] | Standard | Der Portfoliostatus:<ul><li><i>[!UICONTROL Optimize]:</i> Die Optimierungsfunktion erfasst Klick- und Umsatzdaten für die relevanten Kampagnen, modelliert die für die Optimierung verwendeten Daten und optimiert Gebote, Kampagnenbudgets und Ziele der Kampagnenangebotsstrategie (je nach Optimierungstyp und Angebotsstrategien).</li><li><i>[!UICONTROL Active]:</i> Die Optimierungsfunktion erfasst Klick- und Umsatzdaten für die relevanten Kampagnen und modelliert die Daten, optimiert jedoch keine Angebote oder Kampagnenbudgets.</li><li><i>[!UICONTROL Inactive]:</i> Die Optimierungsfunktion erfasst Klickdaten für die relevanten Kampagnen zu Berichtszwecken, modelliert aber weder die Daten noch optimiert sie Gebote oder Kampagnenbudgets. |
| [!UICONTROL Day of Week] | Standard | Der Tag der berichteten Woche: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i> oder <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Event Date] | Standard | Das gemeldete Datum. |
| [!UICONTROL Device] | Standard | (Google Ads, Microsoft Advertising, Yahoo! Display Network, Yahoo! Japan Ads (Japan Ads) und Yahoo Native campaigns) Der Gerätetyp, auf dem Anzeigen angezeigt wurden: <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i> oder <i>[!UICONTROL N/A]</i> (kein Wert). Zeilen für andere Anzeigennetzwerke haben den Wert &quot;<i>[!UICONTROL N/A]</i>&quot;.<br><br>Wenn in Suchkampagnen die Tracking-Vorlagen oder Ziel-URLs für die Suchbegriffe, Anzeigen und/oder Anzeigenerweiterungen Parameter zur Verfolgung von Daten nach Gerät enthielten (<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel}</code>) zum Zeitpunkt, zu dem auf die Anzeige geklickt wurde, dann werden auch Konversionsdaten für jeden Gerätetyp in die Zeile aufgenommen. Andernfalls werden Konversionsdaten, die keinem Gerätetyp zugeordnet werden können, in einer separaten Zeile mit dem Wert &quot;[!UICONTROL Device]&quot; von <i>[!UICONTROL N/A]</i> aggregiert. |
| [!UICONTROL Revenue] | Standard | Der Gesamtumsatz. |
| [!UICONTROL Impressions] | Standard | Die Gesamtimpressionen. |
| [!UICONTROL Clicks] | Standard | Die Gesamtzahl der Klicks. |
| [!UICONTROL Cost] | Standard | Die Gesamtkosten. |

>[!MORELIKETHIS]
>
>* [Über Berichte zur Modellgenauigkeit](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [Der [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [ Modellgenauigkeitsbericht erzeugen](model-accuracy-report-generate.md)
>* [Berichtseinstellungen für Modellgenauigkeit](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
