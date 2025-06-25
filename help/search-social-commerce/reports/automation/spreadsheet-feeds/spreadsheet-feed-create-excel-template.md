---
title: Erstellen  [!DNL Excel]  Vorlage für einen Tabellenbericht-Feed
description: Erfahren Sie, wie Sie speziell formatierte Tabellenvorlagen erstellen.
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Erstellen einer [!DNL Excel] Vorlage für einen Tabellenbericht-Feed

*Nur für Basisberichte und Berichte zur Modellgenauigkeit*

Um Kalkulationstabellen-Feeds zu erstellen, müssen Sie zunächst speziell formatierte [!DNL Microsoft Excel]-Kalkulationstabellenvorlagen mithilfe regulärer Berichtsvorlagen erstellen. Optional können Sie die [!DNL Excel] Tabelle anpassen, um zusätzliche Spalten und Diagramme einzuschließen.

1. Generieren Sie in **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** den gewünschten Berichtstyp unter Verwendung einer [!UICONTROL Date Aggregation] Einheit von &quot;[!UICONTROL Daily]&quot; und mit allen anderen gewünschten Datenparametern und speichern Sie den Bericht als Vorlage.

   >[!NOTE]
   >
   > * Sie können Tabellen-Feeds für [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword] und [!UICONTROL Forecast Accuracy] Berichte erstellen. Wenn Sie die [!UICONTROL Ad Group Report] verwenden, begrenzen Sie die Anzahl der enthaltenen Anzeigengruppen, um schnellere Ergebnisse zu erzielen.
   > * Die in der Vorlage definierte [!UICONTROL Date Range] wird nicht verwendet. Sie definieren die Daten, für die Daten aktualisiert werden sollen, wenn Sie den Tabellen-Feed später konfigurieren.

1. Nachdem der Bericht generiert wurde, navigieren Sie zu **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** und exportieren Sie eine TSV- oder XLS-Version der Berichtsausgabe in eine -Datei.

1. Erstellen Sie [!DNL Excel] eine benutzerdefinierte Vorlage für den Bericht:

   1. Öffnen Sie die Berichtsdatei in [!DNL Excel].

   1. Arbeitsmappe vorbereiten:

      1. Löschen Sie die obersten Zeilen, die die Berichtsparameter anzeigen. Löschen Sie für XLS-Dateien auch die Zeile &quot;[!UICONTROL Total]&quot;. Sie können optional einige der Datenzeilen löschen, aber behalten Sie a) die Datenkopfzeile mit allen Spalten in der ursprünglichen Reihenfolge und b) mindestens eine Datenzeile bei. Keine Daten manuell hinzufügen.

         >[!NOTE]
         >
         > Die endgültige Spalte muss Werte ungleich null enthalten.

      2. Sortieren Sie die Daten nach Startdatum in aufsteigender Reihenfolge (von der ältesten zur neuesten).

      3. Ändern Sie den Namen der Registerkarte des Arbeitsblatts von &quot;[!UICONTROL Sheet1]&quot; in &quot;[!UICONTROL RAW]&quot;.

         Dieser spezifische Registerkartenname ermöglicht die Aktualisierung der Daten.

      4. (Optional) Fügen Sie bei Bedarf benutzerdefinierte Spalten rechts neben den Spalten aus der Berichtsvorlage hinzu.

   1. (Optional) Erstellen Sie auf einem separaten Arbeitsblatt eine Pivot-Tabelle. Klicken Sie abschließend mit der rechten Maustaste in eine beliebige Zelle der Pivot-Tabelle, wählen Sie **[!UICONTROL Pivot Table Options]**, klicken Sie auf die Registerkarte **[!UICONTROL Data]**, und wählen Sie dann **[!UICONTROL Refresh data when opening the file]** aus.

   1. Speichern Sie die Datei als [!DNL Excel]-Arbeitsblatt im .XLSX-Format.

>[!MORELIKETHIS]
>
>* [Über Tabellenbericht-Feeds](spreadsheet-feed-about.md)
>* [Erstellen eines Tabellenbericht-Feeds](spreadsheet-feed-create.md)
>* [Bearbeiten von Tabellenbericht-Feed-Einstellungen](spreadsheet-feed-edit.md)
>* [Einstellungen für Tabellenbericht-Feeds](spreadsheet-feed-settings.md)
>* [Anzeigen oder Speichern einer Tabellenbericht-Feed-Datei](spreadsheet-feed-view-or-save.md)
>* [Tabellenbericht-Feeds manuell aktualisieren](spreadsheet-feed-refresh.md)
>* [Tabellenbericht-Feeds löschen](spreadsheet-feed-delete.md)
