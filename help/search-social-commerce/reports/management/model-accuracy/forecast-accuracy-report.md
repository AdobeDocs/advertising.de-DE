---
title: "[!UICONTROL Forecast Accuracy Report]"
description: Erfahren Sie mehr über den Prognosebericht zur Genauigkeit, einschließlich der Datenspalten.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Die [!UICONTROL Forecast Accuracy Report]

Der Bericht zeigt die Genauigkeit der Kosten- und Umsatzmodelle für bestimmte Portfolios nach Tag an. Standardmäßig werden für jedes Portfolio die täglich prognostizierten und tatsächlichen Einnahmen, Kosten und Klicks sowie die Genauigkeit der Prognosen berücksichtigt. Sie enthält Daten aus Kampagnen, die derzeit den Portfolios zugeordnet sind.

Sie können Daten der letzten 18 Monate anzeigen.

>[!NOTE]
>
>* Dieser Bericht liefert dieselben Daten wie die Portfolioebene [!UICONTROL Model Accuracy Report] Sie können sie jedoch über mehrere Portfolios hinweg ausführen und die Attributionsregel ändern. Sie können den Bericht auch mit benutzerdefinierten Parametern ausführen und planen und ihn zur Erstellung von Tabellenfeeds verwenden.
>
>* Die Best Practice ist, die [!UICONTROL Forecast Accuracy Report] für mindestens die letzten sieben Tage, da die meisten Portfolios unabhängig von der Ausgabenstrategie des Portfolios einen inhärenten Wochentagstrend sehen. Die Optimierungsfunktion berücksichtigt diesen Trend und weist die Ausgaben entsprechend zu.
>
>* Für Kostenprognosen wird eine Abweichung von 10% in den letzten sieben Tagen als akzeptabel betrachtet, sodass die tatsächlichen Ausgaben, die zwischen 90% und 110% der prognostizierten Ausgaben liegen, gut sind. Für die Umsatzprognosen wird eine Abweichung von 15% in den letzten sieben Tagen als akzeptabel betrachtet, sodass der tatsächliche Umsatz, der zwischen 85% und 115% der prognostizierten Ausgaben liegt, in Ordnung ist. Prognosen mit höheren Abweichungen sollten untersucht werden.
>
>* Wenn Suchbegriffe im Portfolio mit Gebotsverschiebungsbegrenzungen verknüpft sind, werden die Portfolioausgaben um den durch die Gebotsverschiebung verursachten Gesamtbetrag erhöht oder unterschritten. Infolgedessen weichen die prognostizierten Kostenspalten von den Zielausgaben durch die erhöhten oder verringerten Ausgaben ab.


## Verfügbare Spalten

Im Folgenden finden Sie die Spalten, die für jeden Bericht verfügbar sind. Die Standardspalten werden standardmäßig automatisch eingefügt. Sie können die verfügbaren benutzerdefinierten Spalten aus der [!UICONTROL Columns] -Abschnitt der Berichtseinstellungen.

| Spalte | Standard? | Beschreibung |
|----|----|----|
| [!UICONTROL Portfolio] | Standard | Das Portfolio. |
| [!UICONTROL Day of Week] | Standard | Der Wochentag, der gemeldet wurde: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i>oder <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Start Date] | Standard | Der erste gemeldete Tag. |
| [!UICONTROL End Date] | Standard | Der letzte gemeldete Tag. |
| [!UICONTROL Predicted Revenue] | Standard | Der prognostizierte Umsatz für das Portfolio. |
| [!UICONTROL Revenue] | Standard | Der tatsächliche Umsatz für das Portfolio. |
| [!UICONTROL Revenue Accuracy] | Standard | Die Genauigkeit der Umsatzvorausschätzung, ausgedrückt als Prozentsatz. |
| [!UICONTROL Predicted Cost] | Standard | Die prognostizierten Kosten für das Portfolio. |
| [!UICONTROL Cost] | Standard | Die tatsächlichen Kosten für das Portfolio. |
| [!UICONTROL Cost Accuracy] | Standard | Die Genauigkeit der Kostenvorausschätzung, ausgedrückt als Prozentsatz. |
| [!UICONTROL Predicted Clicks] | Standard | Die Anzahl der für das Portfolio vorhergesagten Klicks. |
| [!UICONTROL Clicks] | Standard | Die tatsächliche Anzahl der Klicks für das Portfolio. |
| [!UICONTROL Click Accuracy] | Standard | Die Genauigkeit der Klickvorhersage, ausgedrückt als Prozentsatz. |
| [!UICONTROL EF Portfolio Group ID] | Standard | Die numerische ID für die Portfoliogruppe, zu der das Portfolio gehört. |
| [!UICONTROL Portfolio Group Name] | Standard | Der Name der Portfoliogruppe, zu der das Portfolio gehört. |
| [!UICONTROL Portfolio ID] | Standard | Die numerische Portfolio-ID. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Über Berichte zur Modellgenauigkeit](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [Die [!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [Modellexaktionsbericht generieren](model-accuracy-report-generate.md)
>* [Berichtseinstellungen für Modellgenauigkeit](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
