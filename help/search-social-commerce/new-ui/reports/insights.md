---
title: (Neue Benutzeroberfläche) Advertising Insights
description: Erfahren Sie, wie Sie Advertising insight-Dashboards für Modellgenauigkeit, Leistung, Simulationen, Budgetbeschränkungen und Konversionen konfigurieren und anzeigen.
feature: Search Advertising Insights
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bc8b5578-58f6-5342-a640-fce94e5ff4a7
    internal-label: Search Advertising Insights
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 54920f5e0e08c1bf6f960b4d96aa4161dfa11143
workflow-type: tm+mt
source-wordcount: '1217'
ht-degree: 0%
---
# (Neue Benutzeroberfläche) Advertising Insights

Advertising Insights bietet visuelle, verwertbare Daten, mit denen Sie die Portfolioleistung bewerten, Optimierungsprobleme identifizieren und Konversionsdaten vergleichen können. Jede insight wird bei Bedarf generiert und als On-Screen-Dashboard angezeigt.

Die Ansicht **[!UICONTROL Reports]>[!UICONTROL Insights]** zeigt die verfügbaren Einblicke unter **[!UICONTROL Dashboards]**. Die Seitenüberschrift ist **[!UICONTROL Advertising Insights]**.

>[!NOTE]
>
>Auf dieser Seite werden die insight-Dashboards in der neuen Beta-Benutzeroberfläche beschrieben. Die Verfügbarkeit hängt von Ihrem Zugriff und den Insights ab, die für den ausgewählten Advertiser verfügbar sind. Die [veralteten Advertising Insights](/help/search-social-commerce/advertising-insights/insight-about.md) enthalten einen anderen Satz von Analysen und Verfahren für generierte Dateien.

## Arten von Einblicken {#insight-types}

| Insight | Beschreibung |
| --- | --- |
| [!UICONTROL Model Accuracy] | Gibt an, wie gut Search, Social und Commerce Kosten und Einnahmen für ein Portfolio vorhersagen. Sie können die Modellgenauigkeit auf Portfolio-, Werbenetzwerk- und Kampagnenebene überprüfen. |
| [!UICONTROL Performance Insights] | Vergleicht die Portfolioleistung vor und nach einer Änderung des Optimierungsstatus, einer objektiven Änderung oder eines bestimmten Datums. Das Dashboard enthält Leistungszusammenfassungen, eine Prüfung von Änderungen, die sich auf die Optimierung auswirken, Kampagnenvergleiche, Trends und eine objektive Wertanalyse. |
| [!UICONTROL Portfolio Simulation Analysis] | Vergleicht eine vorhandene benutzerdefinierte Simulation mit der tatsächlichen Leistung. Sie können Portfolio- und Kampagnendaten überprüfen, die Simulationsgenauigkeit analysieren und die geschätzte Leistung auf verschiedenen Zielausgabenebenen untersuchen. |
| [!UICONTROL Campaign Budget Cap Analysis] | Gibt an, ob die Ausgaben eines Portfolios durch Kampagnenbudgetgrenzen begrenzt wurden. Das Dashboard enthält begrenzte Ausgaben, betroffene Kampagnen, geschätzte verlorene Impressionen, tägliche und tägliche Trends sowie Empfehlungen für Portfolioeinstellungen. |
| [!UICONTROL Modeled Conversions] | Vergleicht Adobe-Konversionswerte mit den vom Werbenetzwerk gemeldeten Werten, einschließlich modellierter Daten. Sie können Konten, Portfolios oder Kampagnen analysieren und sowohl in Adobe gemessene als auch in Adobe gemessene und modellierte Werte mit Werten verlegerseitig vergleichen. |
| [!UICONTROL Delayed Revenue Analysis] | Misst die Konversionsverzögerung (die Zeit zwischen einem Anzeigenklick oder einer Durchsicht und einer anschließenden Konvertierung) und zeigt ihre Auswirkungen auf den objektiven Wert, den ROI (Return on Investment) und die Modellgenauigkeit an. Die Analyse ist nur für Portfolios mit Click-basierter oder View-Through-Umsatzzuordnung verfügbar. |

## Erstellen eines insight {#insight-generate}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Insights]**.

1. Klicken Sie auf die insight, die Sie generieren möchten.

1. Geben Sie im Bedienfeld **[!UICONTROL Configure]** die [insight-Einstellungen an](#insight-settings).

1. Klicken Sie auf **[!UICONTROL Generate Insight]**.

   Das Konfigurationsfenster wird geschlossen und die Analyse wird im Dashboard angezeigt.

1. Überprüfen Sie die [insight-](#insight-results).

Um die Einstellungen zu ändern, klicken Sie auf **[!UICONTROL Configure]**, ändern Sie die Werte und klicken Sie erneut auf **[!UICONTROL Generate Insight]**. Um zur insight-Liste zurückzukehren, klicken Sie im Breadcrumb auf **[!UICONTROL Analysis List]** .

## Insight-Einstellungen {#insight-settings}

### Modellgenauigkeit {#model-accuracy-settings}

* **[!UICONTROL Portfolios]:** Ein Portfolio auswählen.

* **[!UICONTROL Choose Revenue Type]:** Wählen Sie **[!UICONTROL Actual Revenue]** (Standard) oder **[!UICONTROL Delayed Revenue]** aus.

* **[!UICONTROL Date Range]:** Wählen Sie die zu analysierenden Daten aus. Siehe [Einstellungen für Datumsbereiche](#date-range-settings).

### Performance Insights {#performance-insights-settings}

* **[!UICONTROL Portfolios]:** Ein Portfolio auswählen.

* **[!UICONTROL Revenue Type]:** Wählen Sie **[!UICONTROL Actual Revenue]** (Standard) oder **[!UICONTROL Delayed Revenue]** aus.

* **Ereignisdatum:** Wählen Sie den Typ des Datums aus, um das die Leistung verglichen werden soll:

  * **[!UICONTROL Optimization Status Change (last 90 days)]** (Standard): Wählen Sie ein verfügbares Änderungsdatum des Optimierungsstatus für das Portfolio aus.

  * **[!UICONTROL Objective Change Date (last 90 days)]:** Wählen Sie ein verfügbares Zieländerungsdatum für das Portfolio aus.

  * **[!UICONTROL Specific Date]:** Geben Sie mithilfe der Datumsauswahl ein Datum an.

  Wählen Sie das Ereignisdatum aus, bevor Sie die Vergleichszeiträume konfigurieren. Wenn für das ausgewählte Portfolio keine Ereignisdaten verfügbar sind, können Sie **[!UICONTROL Specific Date]** verwenden.

* **[!UICONTROL Pre Days]:** Geben Sie den Zeitraum vor dem Ereignisdatum an:

  * Wählen Sie **[!UICONTROL 7]** (Standard), **[!UICONTROL 14]** oder **[!UICONTROL 30]** aus.

  * Wählen Sie **[!UICONTROL Pre Start Date]** und geben Sie die **[!UICONTROL Custom Pre Date]** an.

  * Wählen Sie **[!UICONTROL Custom Pre Days]** aus und geben Sie eine positive Anzahl von Tagen ein.

* **[!UICONTROL Post Days]:** Geben Sie den Zeitraum nach dem Ereignisdatum an:

  * Wählen Sie **[!UICONTROL 7]** (Standard), **[!UICONTROL 14]** oder **[!UICONTROL 30]** aus.

  * Wählen Sie **[!UICONTROL Post End Date]** und geben Sie die **[!UICONTROL Custom Post Date]** an.

  * Wählen Sie **[!UICONTROL Custom Post Days]** aus und geben Sie eine positive Anzahl von Tagen ein.

  Das Ereignisdatum selbst ist in keinem der Vergleichszeiträume enthalten.

* **[!UICONTROL Date Exclusion]:** (Optional) Schließen Sie Datumsangaben aus der Analyse aus:

  1. Klicken Sie auf **[!UICONTROL Select Dates]**.

  1. Auszuschließende Daten auswählen:

     * Klicken Sie auf einzelne Datumsangaben, um sie auszuwählen oder ihre Auswahl aufzuheben.

     * Halten Sie **[!UICONTROL Shift]** gedrückt, während Sie klicken, um einen Bereich auszuwählen.

     * Um alle Ausschlüsse zu entfernen, klicken Sie auf **[!UICONTROL Clear All]**.

  1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Done]** .

### Portfolio-Simulationsanalyse {#simulation-settings}

* **[!UICONTROL Portfolios]:** Wählen Sie ein Portfolio mit einer vorhandenen benutzerdefinierten Simulation aus.

* **[!UICONTROL Simulation Date]:** Wählen Sie das Datum der zu analysierenden Simulation aus. Wenn für dieses Datum mehrere Simulationen verfügbar sind, wählen Sie auch die Simulation nach Namen aus.

  Wenn keine benutzerdefinierten Simulationen verfügbar sind, [ Sie eine benutzerdefinierte Simulation ](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md), bevor Sie diese insight verwenden.

* **[!UICONTROL Actual Days]:** Wählen Sie **[!UICONTROL 7]** (Standard), **[!UICONTROL 14]** oder **[!UICONTROL 30]** Tage der tatsächlichen Leistungsdaten aus. Um eine andere Zahl anzugeben, wählen Sie **[!UICONTROL Enter Actual Days]** und geben Sie einen Wert zwischen 1 und 90 ein.

* **[!UICONTROL Type]:** Wählen Sie **[!UICONTROL Transaction Date]** (Standard) oder **[!UICONTROL Click Date]** für die Konversionsattribution aus.

### Budgetbegrenzungsanalyse für Kampagnen {#budget-cap-settings}

* **[!UICONTROL Portfolio]:** Ein Portfolio auswählen.

* **[!UICONTROL Date Range]:** Wählen Sie die zu analysierenden Daten aus. Siehe [Einstellungen für Datumsbereiche](#date-range-settings).

### Modellierte Konversionen {#modeled-conversions-settings}

* **[!UICONTROL Analysis Level]:** Wählen Sie **[!UICONTROL Account]**, **[!UICONTROL Portfolio]** (Standard) oder **[!UICONTROL Campaign]** aus.

* **[!UICONTROL Accounts]**, **[!UICONTROL Portfolios]** oder **[!UICONTROL Campaigns]:** die entsprechenden Entitäten für die Analyseebene aus. Sie können mehrere Entitäten auswählen.

* **[!UICONTROL Date Range]:** Wählen Sie die zu analysierenden Daten aus. Siehe [Einstellungen für Datumsbereiche](#date-range-settings).

* **[!UICONTROL Adobe Conversion]:** Wählen Sie die zu vergleichende Adobe-Konversionseigenschaft aus.

* **[!UICONTROL Publisher Conversion]:** Wählen Sie die zu vergleichende Publisher-Konvertierungseigenschaft aus.

  Die verfügbaren Konvertierungseigenschaften hängen von der Analyseebene, den ausgewählten Entitäten und dem Datumsbereich ab. Beide Konvertierungseigenschaften sind für den Vergleich erforderlich.

### Verzögerte Umsatzanalyse {#delayed-revenue-settings}

* **[!UICONTROL Portfolios]:** Wählen Sie ein Portfolio mit Click-basierter oder View-Through-Umsatzzuordnung.

* **[!UICONTROL Date Range]:** Wählen Sie die zu analysierenden Daten aus. Siehe [Einstellungen für Datumsbereiche](#date-range-settings).

### Einstellungen für Datumsbereich {#date-range-settings}

Wählen Sie für Einblicke mit einer **[!UICONTROL Date Range]** die Option **[!UICONTROL Last 7 days]** (Standard), **[!UICONTROL Last 14 days]** oder **[!UICONTROL Last 30 days]** aus.

Um einen weiteren Zeitraum festzulegen, wählen Sie **[!UICONTROL Custom Date]** und geben Sie den **[!UICONTROL Start Date]** und die **[!UICONTROL End Date]** ein. Sie können Datumsangaben innerhalb der letzten 90 Tage bis zum aktuellen Datum auswählen.

## Insight-Ergebnisse anzeigen {#insight-results}

### Modellgenauigkeit {#model-accuracy-results}

Überprüfen Sie die Portfoliodetails und verwenden Sie die folgenden Registerkarten:

* **[!UICONTROL Portfolio]:** Überprüfen Sie die Modellgenauigkeit auf Portfolioebene und die Budgetvergleiche.

* **[!UICONTROL Ad Network]:** Überprüfen Sie die Modellgenauigkeit und Budgetvergleiche nach Werbenetzwerk.

* **[!UICONTROL Campaigns]:** Überprüfen Sie die Modellgenauigkeit und -zielgruppe auf Kampagnenebene im Vergleich zur tatsächlichen Leistung.

* **[!UICONTROL Playground Beta]:** Die Modellgenauigkeit für mehrere Kampagnen vergleichen.

Wählen Sie für Diagramme zur Kampagnengenauigkeit die **[!UICONTROL Comparison Options]** und **[!UICONTROL Campaign]**. In **[!UICONTROL Playground Beta]** können Sie mehrere Kampagnen auswählen. Klicken Sie auf **[!UICONTROL Table View]** , um zwischen einem Diagramm und den zugrunde liegenden Daten zu wechseln.

### Performance Insights {#performance-insights-results}

Im Dashboard werden die **[!UICONTROL Pre Period]** und **[!UICONTROL Post Period]**, aggregierte Leistungsmetriken für beide Zeiträume und Portfoliodetails angezeigt.

Die **[!UICONTROL Audit Trail]** fasst Änderungen an Faktoren zusammen, die sich auf die Optimierung auswirken, einschließlich Portfoliobudget, Ausgabenstrategie, minimaler Kampagnenausgaben und Ausgabenlimit für mehrere. Wenn Änderungen Details verfügbar sind, klicken Sie auf **[!UICONTROL View Details]** , um diese zu überprüfen.

Verwenden Sie die Registerkarten **[!UICONTROL Comparative Overview]**, **[!UICONTROL Campaigns Comparison]**, **[!UICONTROL Trends & Patterns]**, **[!UICONTROL Deep Analysis]** und **[!UICONTROL Objective Value And Analysis]** , um den Vergleich zu analysieren.

### Portfolio-Simulationsanalyse {#simulation-results}

Überprüfen Sie die Simulationsdetails und verwenden Sie die folgenden Registerkarten:

* **[!UICONTROL Portfolio]:** Überprüfen Sie Simulationsdaten auf Portfolioebene. In dieser Registerkarte:

  * **[!UICONTROL Simulation Data]** zeigt Simulationsmetriken und die Zielausgabenleistung an.

  * **[!UICONTROL Simulation Vs Actual]** vergleicht die simulierte und die tatsächliche Leistung.

  * **[!UICONTROL Try New Target]** können Sie Zielausgaben in eingeben, **[!UICONTROL Explore Target Spend]** die geschätzten Klicks, Kosten und den Umsatz anzuzeigen. Dies ist eine Analyse der geschätzten Leistung; das Ausgabenziel des Portfolios wird dadurch nicht geändert.

* **[!UICONTROL Campaigns]:** Vergleiche der Simulationen auf Kampagnenebene überprüfen.

* **[!UICONTROL Accuracy Analysis]:** Prüft die Simulationsgenauigkeit.

### Budgetbegrenzungsanalyse für Kampagnen {#budget-cap-results}

Überprüfen Sie die Details des Portfolios und die Zusammenfassungsmetriken:

* **[!UICONTROL Total Capped Spend]:** Der Prozentsatz der Ausgaben an Tagen, an denen Kampagnenbudgets erreicht wurden.

* **[!UICONTROL Capped Campaigns]:** Die Anzahl der Kampagnen, die ihr Budget mindestens einmal erreichen.

* **[!UICONTROL Est. Lost Impressions]:** Geschätzte verpasste Impressionen aufgrund von Budgetbeschränkungen.

* **[!UICONTROL Peak Capping Day]:** Der Wochentag mit den meisten begrenzten Ausgaben.

Die **[!UICONTROL Spend on Capped Campaigns by Day]**- und **[!UICONTROL Capped Spend by Weekday]** zeigen Begrenzungstrends. Überprüfen Sie die **[!UICONTROL Capped Campaign Performance]** auf Kampagnendetails und **[!UICONTROL Portfolio Settings Recommendations]** auf vorgeschlagene Einstellungsänderungen.

### Modellierte Konversionen {#modeled-conversions-results}

Überprüfen Sie die folgenden Tabellen für die ausgewählten Entitäten und den ausgewählten Datumsbereich:

* **[!UICONTROL Adobe Measured vs Publisher Conversions]:** Vergleicht direkt von Adobe gemessene Konversionswerte mit den vom Publisher gemeldeten Werten, einschließlich gemessener und modellierter Daten.

* **[!UICONTROL Adobe Modeled vs Publisher Conversions]:** Vergleicht von Adobe gemessene und modellierte Konversionswerte mit vom Publisher gemeldeten Werten.

Beide Tabellen enthalten den Namen und die ID der Entität, den Adobe-Wert, den vom Publisher gemeldeten Wert, die absolute Differenz und den Prozentunterschied.

Wenn keine Daten verfügbar sind, stellen Sie sicher, dass Sie sowohl Konvertierungseigenschaften ausgewählt haben als auch Daten für die ausgewählten Entitäten und den ausgewählten Datumsbereich vorhanden sind.

### Verzögerte Umsatzanalyse {#delayed-revenue-results}

Die **[!UICONTROL Key Insights Summary]** zeigt den erwarteten gewichteten Umsatz (jetzt [Zielwert](/help/search-social-commerce/glossary.md#o-p) genannt), den ROI und Informationen zur Modellgenauigkeit.

Im Abschnitt **[!UICONTROL Conversion Lag Breakdown by Revenue Property]** wird der Prozentsatz der Konversionen angezeigt, die an Tag 0 sowie an den Tagen 3, 7, 14 und 28 für jede Umsatzeigenschaft realisiert wurden.

Wählen Sie **[!UICONTROL Performance Over Time]** **[!UICONTROL Objective Value]**, **[!UICONTROL ROI]** oder **[!UICONTROL Model Accuracy]** aus, um Klickdatum, Transaktionsdatum und erwartete Leistung zu vergleichen. Klicken Sie auf **[!UICONTROL Table View]** , um zwischen dem Diagramm und den zugrunde liegenden Daten zu wechseln.

Klicken Sie **[!UICONTROL Metrics Definitions]** auf **[!UICONTROL Show]** , um Erläuterungen zu den in der Analyse verwendeten Daten und Metriken zu erhalten, oder auf **[!UICONTROL Hide]** , um sie zu reduzieren.

Wenn die Analyse nicht anwendbar ist, wählen Sie ein Portfolio mit Klick- oder Durchsichtsumsatz-Attribution. Wenn keine Daten verfügbar sind, überprüfen Sie, ob Daten für das ausgewählte Portfolio und den ausgewählten Datumsbereich vorhanden sind.
