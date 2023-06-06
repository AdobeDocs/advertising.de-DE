---
title: Daten aus einer Kampagnenverwaltungsansicht herunterladen
description: Erfahren Sie, wie Sie Daten von den meisten Kampagnenverwaltungsansichten herunterladen können.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Daten aus einer Kampagnenverwaltungsansicht herunterladen

Sie können Daten aus dem [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] Ansichten außer [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences]und [!UICONTROL Extensions] Ansichten. Sie können Folgendes herunterladen:

* Ein Bericht in [!DNL XLSM] (makro-fähig) [!DNL Microsoft® Excel] Tabellenformat). Wenn Sie bestimmte Zeilen in der Ansicht auswählen, enthält der Bericht eine Zeile für jede ausgewählte Zeile. Wenn Sie keine Zeilen auswählen, wird für jede Zeile in der Ansicht eine Zeile erstellt.

* Eine Bulksheet-Datei im TXT-Format, die alle relevanten untergeordneten Entitäten enthält. Wenn Sie Zeilen für Entitäten in mehreren Werbenetzwerken auswählen, wird für jedes relevante Werbenetzwerk eine Datei erstellt. Wenn Sie keine Zeilen auswählen, wird für jedes Anzeigennetzwerk, das in der Ansicht dargestellt wird, eine Datei erstellt. Massenblattdateien, die für verschiedene Werbenetzwerke erstellt werden, enthalten unterschiedliche Datenspalten.

   Wenn Sie Daten für mehrere Kampagnen generieren und die kombinierten Daten aus mehr als 500.000 Zeilen bestehen, werden die Daten je nach Kampagne in zwei oder mehr Dateien mit dem Namen `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt`usw.

   Jede Bulksheet-Datei im [!UICONTROL Downloads] wird auch im Bereich [!UICONTROL Bulksheets] anzeigen. Bei der Erstellung der Datei erhalten Sie eine E-Mail-Benachrichtigung mit einem Link, über den Sie die Datei herunterladen können. Je nach Menge der zu erstellenden Daten kann die Benachrichtigung mehrere Minuten oder länger dauern. Wenn die Dateierstellung jedoch fehlschlägt, wird in der Bulksheets-Ansicht eine Fehlerdatei aufgelistet und Sie erhalten eine E-Mail-Benachrichtigung mit einer Verknüpfung zur Fehlerdatei. Löschen einer Bulksheet-Datei aus der [!UICONTROL Download] oder [!UICONTROL Bulksheets] -Tab löscht ihn aus beiden Speicherorten.

1. (Optional) Wählen Sie einzelne Zeilen aus, die in die Datei aufgenommen werden sollen.

   Andernfalls werden alle Daten in der Ansicht einbezogen.

1. Klicken Sie rechts in der Symbolleiste auf ![Berichtsdownload](/help/search-social-commerce/assets/download.png "Berichtsdownload").

1. Klicken ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen") **[!UICONTROL Create]**, fügen Sie optional den Dateinamen hinzu und klicken Sie dann auf **[!UICONTROL Report]** oder **[!UICONTROL Bulksheet]**.

1. (Optional) Sobald der Berichtsauftrag abgeschlossen ist, klicken Sie auf ![Berichtsdownload](/help/search-social-commerce/assets/download.png "Berichtsdownload") , um die [!UICONTROL Available Reports] und laden Sie dann den Bericht herunter oder löschen Sie ihn:

   * Um die Datei gemäß der üblichen Vorgehensweise Ihres Browsers zu öffnen oder zu speichern, klicken Sie auf ![Tabelle herunterladen](/help/search-social-commerce/assets/download-spreadsheet.png "Tabelle herunterladen").

      Weitere Informationen zum Browservorgang finden Sie in der Online-Hilfe Ihres Browsers.

   * Um die Datei zu löschen, klicken Sie auf ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen").

>[!MORELIKETHIS]
>
>[Löschen Sie einen Leistungsdatenbericht oder eine Bulksheet-Datei aus dem [!UICONTROL Downloads] Menü](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
