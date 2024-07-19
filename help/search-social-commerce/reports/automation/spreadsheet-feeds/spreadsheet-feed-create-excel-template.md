---
title: Erstellen einer [!DNL Excel] Vorlage für einen Tabellenbericht-Feed
description: Erfahren Sie, wie Sie speziell formatierte Tabellenvorlagen erstellen.
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Erstellen einer [!DNL Excel] -Vorlage für einen Tabellenbericht-Feed

*Nur für grundlegende Berichte und Berichte zur Modellgenauigkeit*

Um Tabellen-Feeds zu erstellen, müssen Sie zunächst speziell formatierte [!DNL Microsoft Excel] Tabellenvorlagen mithilfe regulärer Berichtsvorlagen erstellen. Optional können Sie die [!DNL Excel] -Tabelle anpassen, um zusätzliche Spalten und Diagramme einzuschließen.

1. Generieren Sie unter **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** den gewünschten Berichtstyp mithilfe einer [!UICONTROL Date Aggregation]-Einheit von &quot;[!UICONTROL Daily]&quot;und mit allen anderen gewünschten Datenparametern, indem Sie den Bericht als Vorlage speichern.

   >[!NOTE]
   >
   > * Sie können Tabellen-Feeds für die Berichte [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword] und [!UICONTROL Forecast Accuracy] erstellen. Wenn Sie den [!UICONTROL Ad Group Report] verwenden, begrenzen Sie die Anzahl der enthaltenen Anzeigengruppen für schnellere Ergebnisse.
   > * Die in der Vorlage definierte [!UICONTROL Date Range]-Einheit wird nicht verwendet. Sie legen die Daten fest, die aktualisiert werden sollen, wenn Sie den Tabellenfeed zu einem späteren Zeitpunkt konfigurieren.

1. Nachdem der Bericht generiert wurde, gehen Sie zu &quot;**[!UICONTROL Search]&quot;> &quot;[!UICONTROL Insights & Reports]&quot;> &quot;[!UICONTROL Reports]**&quot;und exportieren Sie eine TSV- oder XLS-Version der Berichtsausgabe in eine Datei.

1. Erstellen Sie in [!DNL Excel] eine benutzerdefinierte Vorlage für den Bericht:

   1. Öffnen Sie die Berichtsdatei in &quot;[!DNL Excel]&quot;.

   1. Bereiten Sie die Arbeitsmappe vor:

      1. Löschen Sie die obersten Zeilen, die die Berichtsparameter anzeigen. Löschen Sie für XLS-Dateien auch die Zeile &quot;[!UICONTROL Total]&quot;. Sie können optional einige Datenzeilen löschen, aber a) die Datenkopfzeile mit allen Spalten in der ursprünglichen Reihenfolge und b) mindestens eine Datenzeile beibehalten. Fügen Sie keine Daten manuell hinzu.

         >[!NOTE]
         >
         > Die letzte Spalte muss Werte ungleich null enthalten.

      2. Sortieren Sie die Daten nach Startdatum in aufsteigender Reihenfolge (vom ältesten zum neuesten).

      3. Ändern Sie den Registerkartennamen des Arbeitsblatts von &quot;[!UICONTROL Sheet1]&quot; in &quot;[!UICONTROL RAW]&quot;.

         Dieser spezifische Tab-Name ermöglicht die Aktualisierung der Daten.

      4. (Optional) Fügen Sie nach Bedarf benutzerdefinierte Spalten rechts neben den Spalten aus der Berichtsvorlage hinzu.

   1. (Optional) Erstellen Sie in einem separaten Arbeitsblatt eine Pivot-Tabelle. Klicken Sie anschließend mit der rechten Maustaste in eine beliebige Zelle der Pivot-Tabelle und wählen Sie **[!UICONTROL Pivot Table Options]**, klicken Sie auf die Registerkarte **[!UICONTROL Data]** und wählen Sie dann **[!UICONTROL Refresh data when opening the file]** aus.

   1. Speichern Sie die Datei als [!DNL Excel] -Tabelle im .XLSX-Format.

>[!MORELIKETHIS]
>
>* [Über Tabellenbericht-Feeds](spreadsheet-feed-about.md)
>* [Erstellen eines Tabellenbericht-Feeds](spreadsheet-feed-create.md)
>* [Bearbeiten Sie die Einstellungen des Tabellenbericht-Feeds](spreadsheet-feed-edit.md)
>* [Einstellungen für den Spreadsheet-Bericht](spreadsheet-feed-settings.md)
>* [Anzeigen oder Speichern einer Tabellenbericht-Feed-Datei](spreadsheet-feed-view-or-save.md)
>* [Manuelles Aktualisieren von Tabellenbericht-Feeds](spreadsheet-feed-refresh.md)
>* [Löschen von Tabellenbericht-Feeds](spreadsheet-feed-delete.md)
