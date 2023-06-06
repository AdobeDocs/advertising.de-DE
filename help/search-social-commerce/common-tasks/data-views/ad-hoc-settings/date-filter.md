---
title: Daten nach Datumsbereich filtern
description: Erfahren Sie, wie Sie den Filter für den globalen Datumsbereich verwenden.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Daten nach Datumsbereich filtern

Derselbe Filter für den globalen Datumsbereich wird auf die meisten Datenansichten Ihrer Kampagnen in allen Ihren Advertisern angewendet, mit Ausnahme der standardmäßigen und benutzerdefinierten Ansichten, in denen Sie bestimmte Datumsbereiche gespeichert haben. Der standardmäßige Datumsbereich für Kampagnenverwaltungsansichten ist &quot;Gestern&quot;.

Ihre Datumsbereichseinstellungen werden in einem browserspezifischen Cookie gespeichert, sodass Änderungen am Datumsbereichsfilter für alle Advertiser bei jeder Anmeldung mit derselben Browser-Anwendung verwendet werden, bis Sie den Filter ändern oder das Cookie löschen. Jede von Ihnen verwendete Browser-Anwendung speichert die Filtereinstellungen für Datumsbereiche in einem anderen Cookie.

Wenn Sie einen bestimmten Datumsbereich für eine Standardansicht oder eine benutzerdefinierte Ansicht speichern, wird dieser Bereich immer angewendet, wenn Sie die Ansicht anwenden, unabhängig von der verwendeten Browser-Anwendung.

>[!NOTE]
>
>* Sie können Daten aus den letzten 13 Monaten anzeigen. Vorhandene benutzerdefinierte Ansichten können jedoch nur Daten aus den letzten 180 Tagen enthalten.
>* Um frühere Daten anzuzeigen, gehen Sie zu [[!UICONTROL Reports] Ansicht](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) und führen Sie einen Basisbericht aus.
>* Sie können auch einen Datumsbereich für einen [Standardansicht oder benutzerdefinierte Ansicht](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).


## Globalen Datumsfilter in Kampagnenansichten ändern

1. Klicken Sie über einer Datentabelle in Suche \> Kampagnen \> Kampagnen auf den aktuellen Datumsbereich.

1. Im **[!UICONTROL Date Range]** -Feld geben Sie den Bereich an:

   * Für einen voreingestellten Bereich: Wählen Sie aus der Liste der gängigen Zeitabstände aus: *[!UICONTROL Today]* nach *[!UICONTROL Last 180 Days]*. Der Standardwert ist *[!UICONTROL Yesterday]*.

   * Für einen bestimmten Bereich: Auswählen **[!UICONTROL Custom Date Range]** und geben Sie dann das Startdatum und das Enddatum an.

      Geben Sie Datumsangaben in das Format MM/TT/JJJJ oder MM-TT-JJJJ ein oder klicken Sie auf ![Kalendersymbol](/help/search-social-commerce/assets/calendar.png "Kalendersymbol") neben jedem Feld, um den Kalender zu öffnen und ein Datum auszuwählen.

1. (Optional) Vergleichen Sie Daten für den angegebenen Datumsbereich mit Daten für einen zweiten Datumsbereich:

   1. Verschieben Sie die **[!UICONTROL Comparison]** Regler zu *[!UICONTROL On]*.

      Wenn Sie diese Option auswählen, werden für jede reguläre Datenspalte zwei zusätzliche Spalten hinzugefügt. Anstatt beispielsweise nur eine Spalte für[!UICONTROL Impressions],&quot;enthält die Tabelle Spalten für &quot;[!UICONTROL Impressions R1], &quot;[!UICONTROL Impressions R2],&quot; und &quot;[!UICONTROL Impressions Diff].&quot;  Wenn Sie die Daten exportieren, werden dieselben Spalten als[!UICONTROL Impressions Range 1], &quot;[!UICONTROL Impressions Range 2],&quot; und &quot;[!UICONTROL Impressions Difference].&quot;

   1. Geben Sie den zweiten Datumsbereich an.

   1. Wählen Sie aus, wie der Unterschied zwischen den Daten in den beiden ausgewählten Datumsbereichen im &quot;\[&quot;ausgedrückt werden soll._Datenfeld_\] Differenz&quot;-Spalte:

      * *[!UICONTROL Variance]* (Standardeinstellung): Zeigt die Differenz als numerischen Wert an.

      * *[!UICONTROL % Change]:*  Zeigt die Differenz in Prozent an.

1. Klicken **[!UICONTROL Apply]**.
