---
title: Daten nach Datumsbereich filtern
description: Erfahren Sie, wie Sie den Filter für globale Datumsbereiche verwenden.
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
TQID: 'https://experienceleague.adobe.com/1zB1NSise7wN1B68fUTq6ef824eiJx3zEglI0iUzwKQ'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: bcc57258-3285-5d02-a731-d86f57a58c47
    internal-label: Search Common Tasks
  - id: d6e2ef48-fac7-5a4a-96ff-9ac0264dc826
    internal-label: Search Custom Data Views
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: b5d2d666af6062eb3bf07ae041992819a4cc6780
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 0%
---
# Daten nach Datumsbereich filtern

Verwenden Sie den Datumsbereichsfilter, um den Zeitraum anzugeben, für den Leistungsdaten angezeigt werden sollen. In Ansichten, die einen Datumsvergleich unterstützen, können Sie auch die Leistung für zwei Zeiträume vergleichen.

## (Neue Benutzeroberfläche) Ändern des Datumsbereichs {#date-filter-new-ui}

1. Klicken Sie in der Kopfzeile der Seite mit dem Kalendersymbol auf das Steuerelement für den Datumsbereich.

1. Geben Sie den Datumsbereich an:

   * Um einen voreingestellten Bereich zu verwenden, wählen Sie eine Option aus dem Menü über dem ersten Kalender aus, z. B. **[!UICONTROL Yesterday]** oder **[!UICONTROL Last 7 Days]**.

   * Um einen benutzerdefinierten Bereich zu verwenden, wählen Sie **[!UICONTROL Custom Date Range]** und das Start- und Enddatum im Kalender aus. Verwenden Sie die Kalenderpfeile, um zwischen Monaten zu navigieren.

1. Klicken Sie auf **[!UICONTROL Apply]**.

## (Neue Benutzeroberfläche) Vergleichen von Daten für zwei Zeiträume {#compare-periods-new-ui}

*Ansichten, die nur Datumsvergleiche unterstützen*

1. Klicken Sie in der Kopfzeile der Seite mit dem Kalendersymbol auf das Steuerelement für den Datumsbereich.

1. Schalte **[!UICONTROL Compare Periods]** ein.

   Zwei Kalenderbereiche werden nebeneinander angezeigt. Die erste Periode hat eine echte Markierung, und die Vergleichsperiode hat eine violette Markierung.

1. Geben Sie im ersten Bedienfeld den Datumsbereich an:

   * Um einen voreingestellten Bereich zu verwenden, wählen Sie eine Option aus dem Menü über dem ersten Kalender aus, z. B. **[!UICONTROL Yesterday]** oder **[!UICONTROL Last 7 Days]**.

   * Um einen benutzerdefinierten Bereich zu verwenden, wählen Sie **[!UICONTROL Custom Date Range]** und das Start- und Enddatum im Kalender aus. Verwenden Sie die Kalenderpfeile, um zwischen Monaten zu navigieren.

1. Wählen Sie im zweiten Bedienfeld eine Vergleichsvorgabe aus oder klicken Sie auf ein Startdatum im Kalender.

   Der Vergleichszeitraum hat dieselbe Anzahl von Tagen wie der erste Zeitraum. Überprüfen Sie die vollständigen Datumsbereiche über beiden Kalendern.

1. Wählen Sie **[!UICONTROL Comparison Format]** aus, wie der Unterschied angezeigt werden soll:

   * **[!UICONTROL As percentage]:** Die Differenz als Prozentsatz anzeigen.

   * **[!UICONTROL As variance]:** Zeigt die Differenz als numerischen Wert an.

1. Klicken Sie auf **[!UICONTROL Apply]**.

   Das Datumsbereichssteuerelement zeigt beide vollständigen Datumsbereiche mit ihren Periodenbeschriftungen und Farbmarkierungen an. Jede vergleichbare Metrik wird in zwei Periodenspalten und eine **[!UICONTROL Change]** Spalte gruppiert. Nicht vergleichbare Felder bleiben einzelne Spalten. Die Punktmarken in den Spaltenüberschriften identifizieren die entsprechenden Datumsbereiche.

Um den Vergleich von Zeiträumen zu beenden, öffnen Sie das Steuerelement für den Datumsbereich, deaktivieren Sie **[!UICONTROL Compare Periods]** und klicken Sie auf **[!UICONTROL Apply]**. Durch Deaktivieren des Vergleichs werden Filter auf der Grundlage von Vergleichsdaten gelöscht.

### Ändern des Vergleichsformats über ein Spaltenmenü

1. Wenn der Datumsvergleich aktiviert ist, öffnen Sie für eine vergleichbare Metrik das Menü für die Spaltenüberschrift einer **[!UICONTROL Change]** Spalte oder einer der Periodenspalten.

1. Wählen Sie **[!UICONTROL As percentage]** oder **[!UICONTROL As variance]** aus.

   Die Auswahl gilt für alle Vergleichsmetriken im Raster, nicht nur für die ausgewählte Spalte. Das Datumsbereichssteuerelement wird mit der Auswahl synchronisiert, und das Format wird auf allen entsprechenden Seiten für den aktuellen Advertiser freigegeben, einschließlich Ansichten mit gespeicherten Datumsbereichen.

   Nach der erfolgreichen Aktualisierung des Rasters wird eine Bestätigungsmeldung angezeigt. Wenn das Raster nicht mit dem ausgewählten Format aktualisiert werden kann, wird stattdessen eine Fehlermeldung angezeigt. Wählen Sie das Format erneut aus.

Sortier- und Filteroptionen bleiben, sofern unterstützt, in Spaltenmenüs verfügbar.

## Einstellungen für den Datumsbereich (veraltete Benutzeroberfläche)

Derselbe Filter für den globalen Datumsbereich wird auf die meisten Datenansichten in allen Ihren Werbetreibenden angewendet, mit Ausnahme von standardmäßigen und benutzerdefinierten Ansichten, für die Sie bestimmte Datumsbereiche gespeichert haben. Der standardmäßige Datumsbereich für Kampagnenverwaltungsansichten ist „Gestern“.

Ihre Datumsbereichseinstellungen werden in einem browserspezifischen Cookie gespeichert, sodass alle Änderungen am Datumsbereichsfilter für alle Ihre Werbetreibenden bei jeder Anmeldung mit derselben Browser-Anwendung verwendet werden, bis Sie den Filter ändern oder das Cookie löschen. Jede von Ihnen verwendete Browser-Anwendung speichert die Filtereinstellungen für den Datumsbereich in einem anderen Cookie.

Wenn Sie einen bestimmten Datumsbereich für eine Standardansicht oder benutzerdefinierte Ansicht speichern, wird dieser Bereich unabhängig vom verwendeten Browser-Programm immer dann angewendet, wenn Sie die Ansicht anwenden.

>[!NOTE]
>
>* Sie können Daten der vorherigen 13 Monate anzeigen, aber alle vorhandenen benutzerdefinierten Ansichten können nur Daten für bis zu den vorherigen 180 Tagen enthalten.
>* Um frühere Daten anzuzeigen, wechseln Sie zur [[!UICONTROL Reports] Ansicht ](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) führen Sie einen einfachen Bericht aus.
>* Sie können auch einen Datumsbereich für eine [Standardansicht oder benutzerdefinierte Ansicht) ](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## (Alte Benutzeroberfläche) Ändern des globalen Datumsfilters in Kampagnenansichten

1. Klicken Sie über einer Datentabelle in Suchen \> Kampagnen \> Kampagnen auf den aktuellen Datumsbereich.

1. Geben Sie im Feld **[!UICONTROL Date Range]** den Bereich an:

   * Für einen voreingestellten Bereich: Wählen Sie aus der Liste der gängigen Zeitinkremente von *[!UICONTROL Today]* bis *[!UICONTROL Last 180 Days]*. Der Standardwert lautet *[!UICONTROL Yesterday]*.

   * Für einen bestimmten Bereich: Wählen Sie **[!UICONTROL Custom Date Range]** und geben Sie dann das Anfangs- und das Enddatum an.

     Geben Sie Daten im Format MM/TT/JJJJ oder MM-TT-JJJJ ein oder klicken Sie ![Kalendersymbol](/help/search-social-commerce/assets/calendar.png "Kalendersymbol") neben jedem Feld, um den Kalender zu öffnen und ein Datum auszuwählen.

1. (Optional) Vergleichen von Daten für den angegebenen Datumsbereich mit Daten für einen zweiten Datumsbereich:

   1. Schieben Sie den **[!UICONTROL Comparison]** auf „on“.

      Wenn Sie diese Option auswählen, werden für jede reguläre Datenspalte zwei zusätzliche Spalten hinzugefügt. Beispielsweise enthält die Tabelle nicht nur eine Spalte für &quot;[!UICONTROL Impressions]&quot;, sondern auch Spalten für &quot;[!UICONTROL Impressions R1]&quot;, &quot;[!UICONTROL Impressions R2]&quot; und &quot;[!UICONTROL Impressions Diff]&quot;.  Wenn Sie die Daten exportieren, werden dieselben Spalten als &quot;[!UICONTROL Impressions Range 1]&quot;, &quot;[!UICONTROL Impressions Range 2]&quot; und &quot;[!UICONTROL Impressions Difference]&quot; geschrieben.

   1. Geben Sie den zweiten Datumsbereich an.

   1. Wählen Sie, wie der Unterschied zwischen den Daten in den beiden ausgewählten Datumsbereichen in der Spalte &quot;\[_Datenfeld_\] Differenz“ ausgedrückt werden soll:

      * *[!UICONTROL Variance]* (Standard): Zeigt die Differenz als numerischen Wert an.

      * *[!UICONTROL % Change]:* Zeigt die Differenz als Prozentsatz an.

1. Klicken Sie auf **[!UICONTROL Apply]**.
