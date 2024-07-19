---
title: Daten nach Datumsbereich filtern
description: Erfahren Sie, wie Sie den Filter für den globalen Datumsbereich verwenden.
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Daten nach Datumsbereich filtern

Derselbe Filter für den globalen Datumsbereich wird auf die meisten Datenansichten Ihrer Kampagnen in allen Ihren Advertisern angewendet, mit Ausnahme der standardmäßigen und benutzerdefinierten Ansichten, in denen Sie bestimmte Datumsbereiche gespeichert haben. Der standardmäßige Datumsbereich für Kampagnenverwaltungsansichten ist &quot;Gestern&quot;.

Ihre Datumsbereichseinstellungen werden in einem browserspezifischen Cookie gespeichert, sodass Änderungen am Datumsbereichsfilter für alle Advertiser bei jeder Anmeldung mit derselben Browser-Anwendung verwendet werden, bis Sie den Filter ändern oder das Cookie löschen. Jede von Ihnen verwendete Browser-Anwendung speichert die Filtereinstellungen für Datumsbereiche in einem anderen Cookie.

Wenn Sie einen bestimmten Datumsbereich für eine Standardansicht oder eine benutzerdefinierte Ansicht speichern, wird dieser Bereich immer angewendet, wenn Sie die Ansicht anwenden, unabhängig von der verwendeten Browser-Anwendung.

>[!NOTE]
>
>* Sie können Daten aus den letzten 13 Monaten anzeigen. Vorhandene benutzerdefinierte Ansichten können jedoch nur Daten aus den letzten 180 Tagen enthalten.
>* Um frühere Daten anzuzeigen, gehen Sie zur Ansicht [[!UICONTROL Reports] ](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) und führen Sie einen einfachen Bericht aus.
>* Sie können auch einen Datumsbereich für eine [Standardansicht oder benutzerdefinierte Ansicht](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) speichern.

## Globalen Datumsfilter in Kampagnenansichten ändern

1. Klicken Sie über einer Datentabelle in Suche \> Kampagnen \> Kampagnen auf den aktuellen Datumsbereich.

1. Geben Sie im Feld **[!UICONTROL Date Range]** den Bereich an:

   * Für einen voreingestellten Bereich: Wählen Sie aus der Liste der gängigen Zeitabstände zwischen *[!UICONTROL Today]* und *[!UICONTROL Last 180 Days]* aus. Der Standardwert ist *[!UICONTROL Yesterday]*.

   * Für einen bestimmten Bereich: Wählen Sie **[!UICONTROL Custom Date Range]** aus und geben Sie dann das Start- und das Enddatum an.

     Geben Sie Datumsangaben in das Format MM/TT/JJJJ oder MM-TT-JJJJ ein oder klicken Sie neben jedem Feld auf das Kalendersymbol](/help/search-social-commerce/assets/calendar.png "Kalendersymbol") , um den Kalender zu öffnen und ein Datum auszuwählen.![

1. (Optional) Vergleichen Sie Daten für den angegebenen Datumsbereich mit Daten für einen zweiten Datumsbereich:

   1. Verschieben Sie den Regler **[!UICONTROL Comparison]** auf *[!UICONTROL On]*.

      Wenn Sie diese Option auswählen, werden für jede reguläre Datenspalte zwei zusätzliche Spalten hinzugefügt. Anstatt beispielsweise nur eine Spalte für &quot;[!UICONTROL Impressions]&quot;einzuschließen, enthält die Tabelle Spalten für &quot;[!UICONTROL Impressions R1]&quot;, &quot;[!UICONTROL Impressions R2]&quot;und &quot;[!UICONTROL Impressions Diff]&quot;.  Wenn Sie die Daten exportieren, werden dieselben Spalten wie &quot;[!UICONTROL Impressions Range 1]&quot;, &quot;[!UICONTROL Impressions Range 2]&quot;und &quot;[!UICONTROL Impressions Difference]&quot;angegeben.

   1. Geben Sie den zweiten Datumsbereich an.

   1. Wählen Sie aus, wie der Unterschied zwischen den Daten in den beiden ausgewählten Datumsbereichen in der Spalte &quot;\[_Datenfeld_\] Unterschied&quot;ausgedrückt werden soll:

      * *[!UICONTROL Variance]* (Standard): Zeigt die Differenz als numerischen Wert an.

      * *[!UICONTROL % Change]:* Zeigt die Differenz als Prozentsatz an.

1. Klicken Sie auf **[!UICONTROL Apply]**.
