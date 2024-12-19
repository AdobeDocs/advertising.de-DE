---
title: '[!UICONTROL Forecast Accuracy Report]'
description: Erfahren Sie mehr über den Prognosegenauigkeitsbericht, einschließlich der Datenspalten.
exl-id: f0c42323-eb0d-461a-ab09-440fd1bfc960
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# Die [!UICONTROL Forecast Accuracy Report]

Der Bericht zeigt die Genauigkeit der Kosten- und Umsatzmodelle nach Tag für bestimmte Portfolios. Standardmäßig enthält sie für jedes Portfolio den täglichen prognostizierten und tatsächlichen Umsatz, die Kosten und Klicks sowie die Genauigkeit der Prognosen. Sie enthält Daten aus Kampagnen, die derzeit den Portfolios zugeordnet sind.

Sie können Daten der vorherigen 18 Monate anzeigen.

>[!NOTE]
>
>* Dieser Bericht liefert dieselben Daten wie die [!UICONTROL Model Accuracy Report] auf Portfolioebene, mit dem Unterschied, dass Sie sie über mehrere Portfolios hinweg ausführen und die Attributionsregel ändern können. Sie können den Bericht auch mithilfe benutzerdefinierter Parameter ausführen und planen. Außerdem können Sie damit Tabellen-Feeds erstellen.
>
>* Es empfiehlt sich, die [!UICONTROL Forecast Accuracy Report] mindestens für die letzten sieben Tage anzuzeigen, da die meisten Portfolios unabhängig von der Ausgabenstrategie des Portfolios einen inhärenten Trend am Wochentag sehen. Die Optimierungsfunktion berücksichtigt diesen Trend und ordnet die Ausgaben entsprechend zu.
>
>* Bei Kostenprognosen gilt eine Abweichung von 10 % in den letzten sieben Tagen als akzeptabel, sodass tatsächliche Ausgaben zwischen 90 % und 110 % der prognostizierten Ausgaben in Ordnung sind. Bei Einnahmenprognosen gilt eine Abweichung von 15 % in den letzten sieben Tagen als akzeptabel, sodass tatsächliche Einnahmen zwischen 85 % und 115 % der prognostizierten Ausgaben in Ordnung sind. Prognosen mit höheren Abweichungen sollten untersucht werden.
>
>* Wenn Schlüsselwörter im Portfolio mit Einschränkungen der Angebotsverschiebung verknüpft sind, gibt das Portfolio um den durch die Angebotsverschiebung verursachten Gesamtbetrag zu viel oder zu wenig aus. Infolgedessen weichen die prognostizierten Kostenspalten durch die Erhöhung oder Verringerung der Ausgaben von der Zielvorgabe ab.

## Verfügbare Spalten

Im Folgenden finden Sie die Spalten, die für jeden Bericht verfügbar sind. Die Standardspalten werden standardmäßig automatisch eingefügt. Sie können die verfügbaren benutzerdefinierten Spalten aus dem Abschnitt [!UICONTROL Columns] der Berichtseinstellungen hinzufügen.

| Spalte | Standard? | Beschreibung |
|----|----|----|
| [!UICONTROL Portfolio] | Standard | Das Portfolio. |
| [!UICONTROL Day of Week] | Standard | Der Tag der gemeldeten Woche: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i> oder <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Start Date] | Standard | Der erste Tag, der berichtet wurde. |
| [!UICONTROL End Date] | Standard | Der letzte gemeldete Tag. |
| [!UICONTROL Predicted Revenue] | Standard | Der prognostizierte Umsatz für das Portfolio. |
| [!UICONTROL Revenue] | Standard | Die tatsächlichen Einnahmen für das Portfolio. |
| [!UICONTROL Revenue Accuracy] | Standard | Die Genauigkeit der Umsatzprognose, ausgedrückt in Prozent. |
| [!UICONTROL Predicted Cost] | Standard | Die prognostizierten Kosten für das Portfolio. |
| [!UICONTROL Cost] | Standard | Die tatsächlichen Kosten für das Portfolio. |
| [!UICONTROL Cost Accuracy] | Standard | Die Genauigkeit der Kostenprognose, ausgedrückt als Prozentsatz. |
| [!UICONTROL Predicted Clicks] | Standard | Die für das Portfolio vorhergesagte Anzahl an Klicks. |
| [!UICONTROL Clicks] | Standard | Die tatsächliche Anzahl an Klicks für das Portfolio. |
| [!UICONTROL Click Accuracy] | Standard | Die Genauigkeit der Klick-Prognose, ausgedrückt in Prozent. |
| [!UICONTROL EF Portfolio Group ID] | Standard | Die numerische ID für die Portfoliogruppe, zu der das Portfolio gehört. |
| [!UICONTROL Portfolio Group Name] | Standard | Der Name der Portfoliogruppe, zu der das Portfolio gehört. |
| [!UICONTROL Portfolio ID] | Standard | Die numerische Portfolio-ID. |

>[!MORELIKETHIS]
>
>* [Über Berichte zur Modellgenauigkeit](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [Die [!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [Modellgenauigkeitsbericht erstellen](model-accuracy-report-generate.md)
>* [Berichteinstellungen für Modellgenauigkeit](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
