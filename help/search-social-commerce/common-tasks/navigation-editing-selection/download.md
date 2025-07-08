---
title: Herunterladen von Daten aus einer Kampagnenverwaltungsansicht
description: Erfahren Sie, wie Sie Daten aus den meisten Ansichten des Kampagnen-Managements herunterladen.
exl-id: f549f03c-ed0b-4d7d-8d7e-91192c17e77e
feature: Search Common Tasks
source-git-commit: 17dfff36a3f3b62be0d8c24d24b222d43cd97d4a
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Herunterladen von Daten aus einer Kampagnenverwaltungsansicht

<!-- Add info about new UI -->

Sie können Daten von den Ansichten [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] herunterladen, mit Ausnahme der Ansichten [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences] und [!UICONTROL Extensions]. Sie können Folgendes herunterladen:

* Ein Bericht im [!DNL XLSM]-Format (Makro-[!DNL Microsoft Excel]-Tabelle). Wenn Sie bestimmte Zeilen in der Ansicht auswählen, enthält der Bericht eine Zeile für jede ausgewählte Zeile. Wenn Sie keine Zeilen auswählen, wird für jede Zeile in der Ansicht eine Zeile erstellt.

* Eine Bulksheet-Datei im TXT-Format, die alle relevanten untergeordneten Entitäten enthält. Wenn Sie Zeilen für Entitäten in mehreren Werbenetzwerken auswählen, wird für jedes relevante Werbenetzwerk eine Datei erstellt. Wenn Sie keine Zeilen auswählen, wird für jedes in der Ansicht dargestellte Werbenetzwerk eine Datei erstellt. Für verschiedene Werbenetzwerke generierte Bulksheet-Dateien enthalten verschiedene Datenspalten.

  Wenn Sie Daten für mehrere Kampagnen generieren und die kombinierten Daten aus mehr als 500.000 Zeilen bestehen, werden die Daten nach Kampagne in zwei oder mehr Dateien (mit den Namen `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt` usw.) aufgeteilt.

  Jede Bulksheet-Datei im [!UICONTROL Downloads] wird auch in der [!UICONTROL Bulksheets] angezeigt. Wenn die Datei erstellt wird, erhalten Sie eine E-Mail-Benachrichtigung mit einem Link, über den Sie die Datei herunterladen können. Je nach Datenmenge, die kompiliert wird, kann die Benachrichtigung mehrere Minuten oder länger dauern. Wenn die Dateigenerierung jedoch fehlschlägt, wird eine Fehlerdatei in der Bulksheets-Ansicht aufgelistet und Sie erhalten eine E-Mail-Benachrichtigung mit einem Link zur Fehlerdatei. Wenn Sie eine Bulksheet-Datei aus dem [!UICONTROL Download] oder der Registerkarte [!UICONTROL Bulksheets] löschen, wird sie aus beiden Speicherorten gelöscht.

1. (Optional) Wählen Sie einzelne Zeilen aus, die in die Datei aufgenommen werden sollen.

   Andernfalls sind alle Daten in der Ansicht enthalten.

1. Klicken Sie rechts in der Symbolleiste auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht herunterladen").

1. Klicken Sie auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen") **[!UICONTROL Create]**, fügen Sie optional den Dateinamen hinzu und klicken Sie dann entweder auf **[!UICONTROL Report]** oder auf **[!UICONTROL Bulksheet]**.

1. (Optional) Klicken Sie nach Abschluss des Berichtsauftrags auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht herunterladen"), um das Bedienfeld &quot;[!UICONTROL Available Reports]&quot; anzuzeigen, und laden Sie dann den Bericht herunter oder löschen Sie ihn:

   * Um die Datei gemäß dem normalen Verfahren Ihres Browsers zu öffnen oder zu speichern, klicken Sie auf ![Tabelle herunterladen](/help/search-social-commerce/assets/download-spreadsheet.png "Tabelle herunterladen").

     Weitere Informationen zu Ihrem Browser-Verfahren finden Sie in der Online-Hilfe Ihres Browsers.

   * Um die Datei zu löschen, klicken Sie auf ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen").

>[!MORELIKETHIS]
>
>[Löschen eines Leistungsdatenberichts oder einer Bulksheet-Datei aus dem [!UICONTROL Downloads] Menü](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
