---
title: Erstellen Sie eine [!DNL Excel] Vorlage für einen Tabellenbericht-Feed
description: Erfahren Sie, wie Sie speziell formatierte Tabellenvorlagen erstellen.
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Erstellen Sie eine [!DNL Excel] Vorlage für einen Tabellenbericht-Feed

*Nur für grundlegende Berichte und Modellgenauigkeitsberichte*

Um Tabellen-Feeds zu erstellen, müssen Sie zunächst speziell formatierte [!DNL Microsoft Excel] Tabellenvorlagen mithilfe regulärer Berichtvorlagen. Sie können optional die [!DNL Excel] , um zusätzliche Spalten und Diagramme einzuschließen.

1. In **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**, generieren Sie den gewünschten Berichtstyp mithilfe einer [!UICONTROL Date Aggregation] Einheit von &quot;[!UICONTROL Daily]und mit allen anderen gewünschten Datenparametern speichern Sie den Bericht als Vorlage.

   >[!NOTE]
   >
   > * Sie können Tabellen-Feeds für [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword], und [!UICONTROL Forecast Accuracy] Berichte. Wenn Sie die [!UICONTROL Ad Group Report], begrenzen Sie die Anzahl der enthaltenen Anzeigengruppen für schnellere Ergebnisse.
   > * Die [!UICONTROL Date Range] Die in der Vorlage definierte Einheit wird nicht verwendet. Sie legen die Daten fest, die aktualisiert werden sollen, wenn Sie den Tabellenfeed zu einem späteren Zeitpunkt konfigurieren.

1. Nachdem der Bericht generiert wurde, gehen Sie zu **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** und exportieren Sie eine TSV- oder XLS-Version der Berichtsausgabe in eine Datei.

1. In [!DNL Excel]erstellen Sie eine benutzerdefinierte Vorlage für den Bericht:

   1. Öffnen Sie die Berichtsdatei in [!DNL Excel].

   1. Bereiten Sie die Arbeitsmappe vor:

      1. Löschen Sie die obersten Zeilen, die die Berichtsparameter anzeigen. Löschen Sie für XLS-Dateien auch den[!UICONTROL Total]&quot;. Sie können optional einige Datenzeilen löschen, aber a) die Datenkopfzeile mit allen Spalten in der ursprünglichen Reihenfolge und b) mindestens eine Datenzeile beibehalten. Fügen Sie keine Daten manuell hinzu.

         >[!NOTE]
         >
         > Die letzte Spalte muss Werte ungleich null enthalten.

      2. Sortieren Sie die Daten nach Startdatum in aufsteigender Reihenfolge (vom ältesten zum neuesten).

      3. Ändern Sie den Registerkartennamen des Arbeitsblatts in &quot;[!UICONTROL Sheet1]&quot; zu &quot;[!UICONTROL RAW].&quot;

         Dieser spezifische Tab-Name ermöglicht die Aktualisierung der Daten.

      4. (Optional) Fügen Sie nach Bedarf benutzerdefinierte Spalten rechts neben den Spalten aus der Berichtsvorlage hinzu.

   1. (Optional) Erstellen Sie in einem separaten Arbeitsblatt eine Pivot-Tabelle. Klicken Sie anschließend mit der rechten Maustaste auf eine beliebige Zelle der Pivot-Tabelle und wählen Sie die Option **[!UICONTROL Pivot Table Options]**, klicken Sie auf die **[!UICONTROL Data]** und wählen Sie **[!UICONTROL Refresh data when opening the file]**.

   1. Speichern Sie die Datei als [!DNL Excel] Tabelle im .XLSX-Format.

>[!MORELIKETHIS]
>
>* [Über Tabellenbericht-Feeds](spreadsheet-feed-about.md)
>* [Erstellen eines Tabellenbericht-Feeds](spreadsheet-feed-create.md)
>* [Bearbeiten der Feed-Einstellungen für Tabellenberichte](spreadsheet-feed-edit.md)
>* [Feed-Einstellungen für Tabellenberichte](spreadsheet-feed-settings.md)
>* [Anzeigen oder Speichern einer Tabellenbericht-Feed-Datei](spreadsheet-feed-view-or-save.md)
>* [Manuelles Aktualisieren von Tabellenbericht-Feeds](spreadsheet-feed-refresh.md)
>* [Löschen von Tabellenbericht-Feeds](spreadsheet-feed-delete.md)
