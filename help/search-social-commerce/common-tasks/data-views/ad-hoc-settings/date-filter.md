---
title: Daten nach Datumsbereich filtern
description: Erfahren Sie, wie Sie den Filter für globale Datumsbereiche verwenden.
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Daten nach Datumsbereich filtern

Derselbe Filter für den globalen Datumsbereich wird auf die meisten Datenansichten in Ihren Kampagnen für alle Ihre Werbetreibenden angewendet, mit Ausnahme von standardmäßigen und benutzerdefinierten Ansichten, für die Sie bestimmte Datumsbereiche gespeichert haben. Der standardmäßige Datumsbereich für Kampagnenverwaltungsansichten ist „Gestern“.

Ihre Datumsbereichseinstellungen werden in einem browserspezifischen Cookie gespeichert, sodass alle Änderungen am Datumsbereichsfilter für alle Ihre Werbetreibenden bei jeder Anmeldung mit derselben Browser-Anwendung verwendet werden, bis Sie den Filter ändern oder das Cookie löschen. Jede von Ihnen verwendete Browser-Anwendung speichert die Filtereinstellungen für den Datumsbereich in einem anderen Cookie.

Wenn Sie einen bestimmten Datumsbereich für eine Standardansicht oder benutzerdefinierte Ansicht speichern, wird dieser Bereich unabhängig vom verwendeten Browser-Programm immer dann angewendet, wenn Sie die Ansicht anwenden.

>[!NOTE]
>
>* Sie können Daten der vorherigen 13 Monate anzeigen, aber alle vorhandenen benutzerdefinierten Ansichten können nur Daten für bis zu den vorherigen 180 Tagen enthalten.
>* Um frühere Daten anzuzeigen, wechseln Sie zur [[!UICONTROL Reports] Ansicht ](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) führen Sie einen einfachen Bericht aus.
>* Sie können auch einen Datumsbereich für eine [Standardansicht oder benutzerdefinierte Ansicht) ](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## Ändern des globalen Datumsfilters in Kampagnenansichten

1. Klicken Sie über einer Datentabelle in Suchen \> Kampagnen \> Kampagnen auf den aktuellen Datumsbereich.

1. Geben Sie im Feld **[!UICONTROL Date Range]** den Bereich an:

   * Für einen voreingestellten Bereich: Wählen Sie aus der Liste der gängigen Zeitinkremente von *[!UICONTROL Today]* bis *[!UICONTROL Last 180 Days]*. Der Standardwert lautet *[!UICONTROL Yesterday]*.

   * Für einen bestimmten Bereich: Wählen Sie **[!UICONTROL Custom Date Range]** und geben Sie dann das Anfangs- und das Enddatum an.

     Geben Sie Daten im Format MM/TT/JJJJ oder MM-TT-JJJJ ein oder klicken Sie ![Kalendersymbol](/help/search-social-commerce/assets/calendar.png "Kalendersymbol") neben jedem Feld, um den Kalender zu öffnen und ein Datum auszuwählen.

1. (Optional) Vergleichen von Daten für den angegebenen Datumsbereich mit Daten für einen zweiten Datumsbereich:

   1. Schieben Sie den **[!UICONTROL Comparison]** auf *[!UICONTROL On]*.

      Wenn Sie diese Option auswählen, werden für jede reguläre Datenspalte zwei zusätzliche Spalten hinzugefügt. Beispielsweise enthält die Tabelle nicht nur eine Spalte für &quot;[!UICONTROL Impressions]&quot;, sondern auch Spalten für &quot;[!UICONTROL Impressions R1]&quot;, &quot;[!UICONTROL Impressions R2]&quot; und &quot;[!UICONTROL Impressions Diff]&quot;.  Wenn Sie die Daten exportieren, werden dieselben Spalten als &quot;[!UICONTROL Impressions Range 1]&quot;, &quot;[!UICONTROL Impressions Range 2]&quot; und &quot;[!UICONTROL Impressions Difference]&quot; geschrieben.

   1. Geben Sie den zweiten Datumsbereich an.

   1. Wählen Sie, wie der Unterschied zwischen den Daten in den beiden ausgewählten Datumsbereichen in der Spalte &quot;\[_Datenfeld_\] Differenz“ ausgedrückt werden soll:

      * *[!UICONTROL Variance]* (Standard): Zeigt die Differenz als numerischen Wert an.

      * *[!UICONTROL % Change]:* Zeigt die Differenz als Prozentsatz an.

1. Klicken Sie auf **[!UICONTROL Apply]**.
