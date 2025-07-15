---
title: (Neue Benutzeroberfläche) Anzeigen von Details zur Portfolioleistung
description: Erfahren Sie, wie Sie Details zur Portfolioleistung anzeigen, einschließlich tatsächlicher und prognostizierter Metriken auf Portfolioebene und für jede zugewiesene Kampagne.
feature: Search Portfolios, Search Optimization
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Anzeigen von Details zur Portfolioleistung

*Beta-Funktion*

<!-- Verify all, including why (if) the first report is for active and optimized portfolios(?), and why the other reports are for active portfolios, not optimized ones -->

Die Portfoliodetailansicht enthält die folgenden Informationen zu einem Portfolio:

* Die tatsächlichen und prognostizierten Werte für bis zu drei Leistungsmetriken. Die Berichte enthalten die Gesamtmetrikwerte für das Portfolio und die Metrikaufschlüsselung nach Datum.<!-- Not for active portfolios only?  -->

* Modellgenauigkeitsdaten für aktive Portfolios, die zeigen, wie stark die Modelle von den Prognosen abwichen. Der Bericht zeigt die tägliche oder rollierende Kostengenauigkeit für sieben Tage, die Klickgenauigkeit und die objektive Wertgenauigkeit an.

  Sie können Daten nach Klickdatum (Standard) oder Transaktionsdatum anzeigen.   Sie können die Daten auch entweder als Trenddiagramm (Standard) oder als Tabelle anzeigen.

* Die Zielausgaben im Vergleich zu den tatsächlichen Ausgaben für aktive Portfolios. Optional können Sie auch die gesamten Kampagnenbudgets für das Portfolio einbeziehen.

* Die Genauigkeit von Kosten-, Klick- oder [Zielwert](/help/search-social-commerce/glossary.md#o-p)-Prognosen für aktive Portfolios nach Anzeigennetzwerk.<!-- Verify -->

* Die Portfolioeinstellungen.

  Optional können Sie die Portfolioeinstellungen öffnen, um sie zu bearbeiten.

## Leistungsdetails für ein Portfolio öffnen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Klicken Sie auf den Portfolionamen.

1. (Optional) Ändern Sie im Menü **[!UICONTROL Granularity]** die Datengranularität zwischen *[!UICONTROL Daily],* *[!UICONTROL Weekly],* oder *[!UICONTROL Monthly].*

1. (Optional) Um den Datumsbereich für die Portfoliodetails zu ändern, klicken Sie auf den Datumsbereich oben rechts, geben Sie den Datumsbereich an und klicken Sie dann auf **[!UICONTROL Apply]**.

## Anpassen der Registerkarte [!UICONTROL Portfolio Overview]

* (Optional) Führen Sie einen der folgenden Schritte aus, um die [!UICONTROL Portfolio Performance] Berichte anzupassen:

   * Um die Leistungsmetriken zu ändern, die sowohl für die Gesamtmetriken als auch für die detaillierten Metriken verwendet werden, klicken Sie auf **[!UICONTROL Metrics]** und wählen Sie bis zu drei Metriken aus.

     Die Standardmetriken sind *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* und *[!UICONTROL Objective Value]*.<!-- What else is available: the advertiser's revenue metrics? Anything else from the ad networks? -->

   * Für die detaillierten Metriken:

      * Bewegen Sie den Schalter neben **[!UICONTROL Display predictions]**, um die prognostizierten Metrikwerte ein- oder auszublenden.

      * Wechseln Sie zwischen der Diagrammansicht ![Diagrammansicht](/help/search-social-commerce/assets/chart-view.png "Diagrammansicht") und Tabellenansicht (![Tabellenansicht](/help/search-social-commerce/assets/table-view.png "Tabellenansicht")).

      * (In der Diagrammansicht) Um Daten für einen beliebigen Punkt im Diagramm anzuzeigen, halten Sie den Cursor über diesen Punkt.

* (Optional) Führen Sie einen der folgenden Schritte aus, um das Diagramm &quot;[!UICONTROL Model accuracy]-Trend“ anzupassen:

   * Wechseln Sie zwischen der Diagrammansicht ![Diagrammansicht](/help/search-social-commerce/assets/chart-view.png "Diagrammansicht") und Tabellenansicht (![Tabellenansicht](/help/search-social-commerce/assets/table-view.png "Tabellenansicht")).

   * Wechseln Sie zwischen der Datenanzeige nach *[!UICONTROL Click Date]* und *[!UICONTROL Transaction Date]*.

   * Wechseln Sie zwischen der Anzeige von Daten über die *[!UICONTROL Daily Accuracy]* und die *[!UICONTROL 7 Day Rolling Accuracy]*.

     [!UICONTROL 7 Day Rolling Accuracy] ist die durchschnittliche Genauigkeit der Prognose für die letzten sieben Tage, ausgedrückt in Prozent. Beispielsweise entspricht der Wert für den 8. Mai 2025 der durchschnittlichen Genauigkeit für den Zeitraum vom 1. Mai bis 7. Mai 2025.

   * (In der Diagrammansicht) Um Daten für einen beliebigen Punkt im Diagramm anzuzeigen, halten Sie den Cursor über diesen Punkt.

* (Optional) Führen Sie einen der folgenden Schritte aus, um das Diagramm &quot;[!UICONTROL Target vs actual spend]-Trend“ anzupassen:

   * Bewegen Sie den Schalter neben **[!UICONTROL Display budget]**, um das gesamte Kampagnenbudget für jedes Datum ein- oder auszublenden.

   * Um Daten für einen beliebigen Punkt im Diagramm anzuzeigen, halten Sie den Cursor über diesen Punkt.

* (Optional) Führen Sie einen der folgenden Schritte aus, um das Diagramm &quot;[!UICONTROL Network Accuracy]-Trend“ anzupassen:

   * Ändern Sie die gemeldete Metrik in *[!UICONTROL Cost]*, *[!UICONTROL Clicks]* oder *[!UICONTROL Objective Value]*.

   * Um Daten für einen beliebigen Punkt im Diagramm anzuzeigen, halten Sie den Cursor über diesen Punkt.

## Auflisten der Kampagnen im Portfolio

* Klicken Sie auf die Registerkarte **[!UICONTROL Campaigns]** .

## Auflisten der Anzeigengruppen im Portfolio

* Um alle Anzeigengruppen in einer Kampagne innerhalb des Portfolios anzuzeigen, klicken Sie auf die Registerkarte **[!UICONTROL Campaigns]** und dann auf den Namen der Kampagne.

## Auflisten der Keywords im Portfolio

* Um alle Keywords im Portfolio anzuzeigen, klicken Sie auf die Registerkarte **[!UICONTROL Keywords]** .

* Um alle Keywords in einer Anzeigengruppe innerhalb des Portfolios anzuzeigen, klicken Sie auf die Registerkarte **[!UICONTROL Ad Groups]** und dann auf den Namen der Anzeigengruppe.

## Portfolioeinstellungen anzeigen und bearbeiten

* Um die Portfolioeinstellungen anzuzeigen oder auszublenden, klicken Sie auf **[!UICONTROL Portfolio Settings]**.

   * Um sichtbare Portfolioeinstellungen zu bearbeiten, klicken Sie ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten") neben dem Abschnitt Einstellungen und [Portfolioeinstellungen bearbeiten](portfolio-edit.md).

Weitere Informationen zu den Portfolioeinstellungen finden Sie im Optimierungshandbuch , das bei Search, Social und Commerce verfügbar ist.

>[!MORELIKETHIS]
>
>* [(Neue Benutzeroberfläche) Über Portfolios](portfolio-about.md)
>* [(Neue Benutzeroberfläche) Bearbeiten eines Portfolios](portfolio-edit.md)
>* [(Neue Benutzeroberfläche) Herunterladen von Daten in der [!UICONTROL Portfolios] Ansicht](portfolio-view-report.md)
