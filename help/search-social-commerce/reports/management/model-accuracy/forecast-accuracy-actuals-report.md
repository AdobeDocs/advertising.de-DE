---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: Erfahren Sie mehr über die [!UICONTROL Forecast Accuracy (Actuals) Report], einschließlich der Datenspalten.
exl-id: 659e11c7-5fed-4d91-a73f-7c435d36634f
feature: Search Reports, Search Model Accuracy Reports
TQID: https://experienceleague.adobe.com/wQyO42Dt5McqK23z-adEP-BAxxTrBk9RJi0I-4noP0I
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 318
ht-degree: 0%

---

# Die [!UICONTROL Forecast Accuracy (Actuals) Report]

Dieser Bericht zeigt die tatsächlichen Impressions-, Klick-, Kosten- und Umsatzdaten aus dem Anzeigennetzwerk nach Tag für jedes Portfolio an.

## Verfügbare Spalten

Im Folgenden finden Sie die Spalten, die automatisch in jedem Bericht enthalten sind. Es können keine zusätzlichen Spalten hinzugefügt werden.

| Spalte | Standard? | Beschreibung |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | Standard | Der Name der Portfoliogruppe, zu der das Portfolio gehört. |
| [!UICONTROL Portfolio ID] | Standard | Die numerische Portfolio-ID. |
| [!UICONTROL EF Portfolio Group ID] | Standard | Die numerische ID für die Portfoliogruppe, zu der das Portfolio gehört. |
| [!UICONTROL Portfolio] | Standard | Das Portfolio. |
| [!UICONTROL Portfolio Status] | Standard | Der Portfoliostatus:<ul><li><i>[!UICONTROL Optimize]:</i> Die Optimierungsfunktion sammelt Klick- und Umsatzdaten für die relevanten Kampagnen, modelliert die für die Optimierung verwendeten Daten und optimiert Gebote, Kampagnenbudgets und Kampagnen-Bid-Strategie-Ziele (abhängig vom Optimierungstyp und den Bid-Strategien).</li><li><i>[!UICONTROL Active]:</i> Die Optimierungsfunktion sammelt Klick- und Umsatzdaten für die relevanten Kampagnen und modelliert die Daten, optimiert jedoch keine Angebote oder Kampagnenbudgets.</li><li><i>[!UICONTROL Inactive]:</i> Die Optimierungsfunktion sammelt Klickdaten für die relevanten Kampagnen zu Berichtszwecken, aber sie modelliert weder die Daten noch optimiert sie Gebote oder Kampagnenbudgets. |
| [!UICONTROL Day of Week] | Standard | Der Tag der gemeldeten Woche: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i> oder <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Event Date] | Standard | Das gemeldete Datum. |
| [!UICONTROL Device] | Standard | (Google Ads, [!DNL LY Ads], Microsoft Advertising, Yahoo! Netzwerk anzeigen und native Yahoo-Kampagnen) Der Gerätetyp, auf dem Anzeigen angezeigt wurden: <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i> oder <i>[!UICONTROL N/A]</i> (kein Wert). Zeilen für andere Werbenetzwerke haben Werte von <i>[!UICONTROL N/A]</i>.<br><br>In Suchkampagnen, wenn die Tracking-Vorlagen oder Ziel-URLs für die Keywords, Anzeigen und/oder Anzeigenerweiterungen Parameter zum Tracking von Daten nach Gerät enthalten (<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel}</code>) zu dem Zeitpunkt, als auf die Anzeige geklickt wurde, sind die Konversionsdaten ebenfalls in der Zeile für jeden Gerätetyp enthalten. Andernfalls werden Konversionsdaten, die keinem Gerätetyp zugeordnet werden können, in einer separaten Zeile mit dem Wert &quot;[!UICONTROL Device]&quot; <i>[!UICONTROL N/A]</i> aggregiert. |
| [!UICONTROL Revenue] | Standard | Die Gesamteinnahmen. |
| [!UICONTROL Impressions] | Standard | Die Gesamtzahl der Impressionen. |
| [!UICONTROL Clicks] | Standard | Die Gesamtzahl der Klicks. |
| [!UICONTROL Cost] | Standard | Die Gesamtkosten. |

>[!MORELIKETHIS]
>
>* [Über Berichte zur Modellgenauigkeit](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [Die [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [Modellgenauigkeitsbericht erstellen](model-accuracy-report-generate.md)
>* [Berichteinstellungen für Modellgenauigkeit](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
