---
title: Daten aus einer Kampagnenverwaltungsansicht herunterladen
description: Erfahren Sie, wie Sie Daten von den meisten Kampagnenverwaltungsansichten herunterladen können.
exl-id: f549f03c-ed0b-4d7d-8d7e-91192c17e77e
feature: Search Common Tasks
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Daten aus einer Kampagnenverwaltungsansicht herunterladen

Sie können Daten aus den Ansichten [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] mit Ausnahme der Ansichten [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences] und [!UICONTROL Extensions] herunterladen. Sie können Folgendes herunterladen:

* Ein Bericht im Format [!DNL XLSM] (makro-fähige [!DNL Microsoft Excel] Tabelle). Wenn Sie bestimmte Zeilen in der Ansicht auswählen, enthält der Bericht eine Zeile für jede ausgewählte Zeile. Wenn Sie keine Zeilen auswählen, wird für jede Zeile in der Ansicht eine Zeile erstellt.

* Eine Bulksheet-Datei im TXT-Format, die alle relevanten untergeordneten Entitäten enthält. Wenn Sie Zeilen für Entitäten in mehreren Werbenetzwerken auswählen, wird für jedes relevante Werbenetzwerk eine Datei erstellt. Wenn Sie keine Zeilen auswählen, wird für jedes Anzeigennetzwerk, das in der Ansicht dargestellt wird, eine Datei erstellt. Massenblattdateien, die für verschiedene Werbenetzwerke erstellt werden, enthalten unterschiedliche Datenspalten.

  Wenn Sie Daten für mehrere Kampagnen generieren und die kombinierten Daten aus mehr als 500.000 Zeilen bestehen, werden die Daten je nach Kampagne in zwei oder mehr Dateien mit den Namen `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt` usw. aufgeteilt.

  Jede Bulksheet-Datei im Bedienfeld [!UICONTROL Downloads] wird ebenfalls in der Ansicht [!UICONTROL Bulksheets] aufgeführt. Bei der Erstellung der Datei erhalten Sie eine E-Mail-Benachrichtigung mit einem Link, über den Sie die Datei herunterladen können. Je nach Menge der zu erstellenden Daten kann die Benachrichtigung mehrere Minuten oder länger dauern. Wenn die Dateierstellung jedoch fehlschlägt, wird in der Bulksheets-Ansicht eine Fehlerdatei aufgelistet und Sie erhalten eine E-Mail-Benachrichtigung mit einer Verknüpfung zur Fehlerdatei. Wenn Sie eine Bulksheet-Datei aus dem Bedienfeld [!UICONTROL Download] oder der Registerkarte [!UICONTROL Bulksheets] löschen, wird sie aus beiden Speicherorten gelöscht.

1. (Optional) Wählen Sie einzelne Zeilen aus, die in die Datei aufgenommen werden sollen.

   Andernfalls werden alle Daten in der Ansicht einbezogen.

1. Klicken Sie rechts in der Symbolleiste auf ![Berichtsdownload](/help/search-social-commerce/assets/download.png "Berichtsdownload").

1. Klicken Sie auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen") **[!UICONTROL Create]**, fügen Sie optional den Dateinamen hinzu und klicken Sie dann auf **[!UICONTROL Report]** oder **[!UICONTROL Bulksheet]**.

1. (Optional) Sobald der Berichtsauftrag abgeschlossen ist, klicken Sie auf ![Berichtsdownload](/help/search-social-commerce/assets/download.png "Berichtsdownload") , um das Bedienfeld [!UICONTROL Available Reports] anzuzeigen, und laden Sie dann den Bericht herunter oder löschen Sie ihn:

   * Um die Datei gemäß der üblichen Vorgehensweise Ihres Browsers zu öffnen oder zu speichern, klicken Sie auf ![Tabelle herunterladen](/help/search-social-commerce/assets/download-spreadsheet.png "Tabelle herunterladen") .

     Weitere Informationen zum Browservorgang finden Sie in der Online-Hilfe Ihres Browsers.

   * Klicken Sie zum Löschen der Datei auf ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen").

>[!MORELIKETHIS]
>
>[Löschen Sie einen Leistungsdatenbericht oder eine Bulksheet-Datei aus dem [!UICONTROL Downloads] Menü](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
