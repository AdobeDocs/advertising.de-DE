---
title: (Neue Benutzeroberfläche) Verwalten von Tabellenbericht-Feeds
description: Erfahren Sie, wie Sie Tabellen-Report-Feeds erstellen, konfigurieren, aktualisieren, anzeigen und löschen, die tägliche Leistungsdaten in einer benutzerdefinierten Tabelle bereitstellen.
feature: Search Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
source-git-commit: b0691683d8b9a02169920645c4220c3737cb9bd9
workflow-type: tm+mt
source-wordcount: '1632'
ht-degree: 0%
---
# (Neue Benutzeroberfläche) Verwalten von Tabellenbericht-Feeds

*Nur für Basisberichte und Berichte zur Modellgenauigkeit*

<!-- Update link to notifications once available -->

Tabellenfeeds liefern tägliche Leistungsdaten für alle Basisberichte und Modellgenauigkeitsberichte in einem benutzerdefinierten Tabellenformat in [!DNL Microsoft Excel] XLSX. Sie können Tabellen-Feeds mithilfe speziell formatierter [!DNL Excel]-Tabellenvorlagen einrichten, die Sie aus regulären Berichtsvorlagen erstellen. Jeden Tag wird die Tabelle zu einem bestimmten Zeitpunkt automatisch mit neuen Rohdaten aktualisiert, die täglich aggregiert werden. Mit den Rohdaten werden alle Spalten und Diagramme ausgefüllt, die Sie in die Tabellenvorlage aufgenommen haben. Sobald eine Kalkulationstabellen-Feed-Datei verfügbar ist oder die Dateigenerierung fehlschlägt, erhält jeder in den Kalkulationstabellen-Feed-Einstellungen angegebene E-Mail-Empfänger eine Benachrichtigung, die auf den konfigurierten [Benachrichtigungseinstellungen für Berichte“ des Benutzers ](/help/search-social-commerce/notifications/notification-about.md).

Sie können den Feed so konfigurieren, dass die Daten der letzten 90 Tage aktualisiert werden. Alle vorherigen vorhandenen Daten bleiben erhalten und werden weiterhin gesammelt.

In der Ansicht [!UICONTROL Reports] > [!UICONTROL Spreadsheet Feeds] werden alle von Ihnen erstellten Tabellen-Feeds aufgelistet. In dieser Ansicht können Sie Tabellen-Feeds erstellen, bearbeiten, manuell aktualisieren oder löschen, die Einstellungen der zugehörigen Berichtsvorlage anzeigen und ausgewählte Zeilendaten kopieren.

## Verfügbare Aktionen

* [Erstellen  [!DNL Excel]  Vorlage für einen Tabellenbericht-Feed](#spreadsheet-feed-create-excel-template)

* [Erstellen eines Tabellenbericht-Feeds](#spreadsheet-feed-create)

* [Bearbeiten von Tabellenbericht-Feed-Einstellungen](#spreadsheet-feed-edit)

* [Anzeigen der Einstellungen der zugehörigen Berichtsvorlage](#spreadsheet-feed-view-template)

* [Anzeigen oder Speichern einer Tabellenbericht-Feed-Datei](#spreadsheet-feed-view-or-save)

* [Tabellenbericht-Feeds manuell aktualisieren](#spreadsheet-feed-refresh)

* [Tabellenbericht-Feeds löschen](#spreadsheet-feed-delete)

* [Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren](#copy-to-clipboard)

## Erstellen einer [!DNL Excel] Vorlage für einen Tabellenbericht-Feed {#spreadsheet-feed-create-excel-template}

Um Kalkulationstabellen-Feeds zu erstellen, müssen Sie zunächst speziell formatierte [!DNL Microsoft Excel]-Kalkulationstabellenvorlagen mithilfe regulärer [Berichtsvorlagen](report-templates-manage.md) erstellen. Optional können Sie die [!DNL Excel] Tabelle anpassen, um zusätzliche Spalten und Diagramme einzuschließen.

1. Generieren Sie in **[!UICONTROL Reports]>[!UICONTROL Reports]** den gewünschten Berichtstyp unter Verwendung einer [!UICONTROL Date Aggregation] Einheit von &quot;[!UICONTROL Daily]&quot; und mit allen anderen gewünschten Datenparametern und speichern Sie den Bericht als Vorlage.

   >[!NOTE]
   >
   > * Sie können Tabellen-Feeds für [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword] und [!UICONTROL Forecast Accuracy] Berichte erstellen. Wenn Sie die [!UICONTROL Ad Group Report] verwenden, begrenzen Sie die Anzahl der enthaltenen Anzeigengruppen, um schnellere Ergebnisse zu erzielen.
   > * Die in der Vorlage definierte [!UICONTROL Date Range] wird nicht verwendet. Sie definieren die Daten, für die Daten aktualisiert werden sollen, wenn Sie den Tabellen-Feed später konfigurieren.

1. Nachdem der Bericht generiert wurde, gehen Sie zu **[!UICONTROL Reports]>[!UICONTROL Reports]** und exportieren Sie eine TSV- oder XLS-Version der Berichtsausgabe in eine Datei.

1. Erstellen Sie [!DNL Excel] eine benutzerdefinierte Vorlage für den Bericht:

   1. Öffnen Sie die Berichtsdatei in [!DNL Excel].

   1. Arbeitsmappe vorbereiten:

      1. Löschen Sie die obersten Zeilen, die die Berichtsparameter anzeigen. Löschen Sie für XLS-Dateien auch die Zeile &quot;[!UICONTROL Total]&quot;. Sie können optional einige der Datenzeilen löschen, aber behalten Sie a) die Datenkopfzeile mit allen Spalten in der ursprünglichen Reihenfolge und b) mindestens eine Datenzeile bei. Keine Daten manuell hinzufügen.

         >[!NOTE]
         >
         > Die endgültige Spalte muss Werte ungleich null enthalten.

      1. Sortieren Sie die Daten nach Startdatum in aufsteigender Reihenfolge (von der ältesten zur neuesten).

      1. Ändern Sie den Namen der Registerkarte des Arbeitsblatts von &quot;[!UICONTROL Sheet1]&quot; in &quot;[!UICONTROL RAW]&quot;.

         Dieser spezifische Registerkartenname ermöglicht die Aktualisierung der Daten.

      1. (Optional) Fügen Sie bei Bedarf benutzerdefinierte Spalten rechts neben den Spalten aus der Berichtsvorlage hinzu.

   1. (Optional) Erstellen Sie auf einem separaten Arbeitsblatt eine Pivot-Tabelle. Klicken Sie abschließend mit der rechten Maustaste in eine beliebige Zelle der Pivot-Tabelle, wählen Sie **[!UICONTROL Pivot Table Options]**, klicken Sie auf die Registerkarte **[!UICONTROL Data]**, und wählen Sie dann **[!UICONTROL Refresh data when opening the file]** aus.

   1. Speichern Sie die Datei als [!DNL Excel]-Arbeitsblatt im .XLSX-Format.

## Erstellen eines Tabellenbericht-Feeds {#spreadsheet-feed-create}

1. [Erstellen Sie die  [!DNL Excel] , die mit den Berichtsdaten aufgefüllt werden soll](#spreadsheet-feed-create-excel-template).

1. Erstellen des Tabellen-Feeds:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

   1. Klicken Sie oben rechts auf **[!UICONTROL Create Spreadsheet]**.

   1. Geben Sie im Dialogfeld **[!UICONTROL Create Spreadsheet Feed]** die [Tabellenvorschubeinstellungen“ ](#spreadsheet-feed-settings).

   1. Klicken Sie auf **[!UICONTROL Submit]**.

   1. (Optional) Klicken Sie nach der *[!UICONTROL Finished]* des Feed-[!UICONTROL Update Status] auf **[!UICONTROL XLSX]** neben dem Feed und öffnen oder speichern Sie die Datei dann entsprechend dem normalen Verfahren Ihres Browsers.

      >[!NOTE]
      >
      >Wenn die mit dem Feed verknüpfte Berichtsvorlage später gelöscht wird, wird der Feed ebenfalls gelöscht.

      Die Tabellen-Feeds werden jeden Tag am konfigurierten [!UICONTROL Schedule Time] automatisch aktualisiert. Die in der [!UICONTROL Email Recipients] des Feeds angegebenen Adressen erhalten Benachrichtigungen, wenn die Tabelle aktualisiert wird.

## Bearbeiten von Tabellenbericht-Feed-Einstellungen {#spreadsheet-feed-edit}

>[!NOTE]
>
> Wenn Sie die Spalten in der Berichtsvorlage bearbeiten oder eine neue oder aktualisierte Berichtsvorlage verwenden, müssen Sie die [!DNL Excel] entsprechend aktualisieren und erneut hochladen.

1. (Optional) So aktualisieren Sie die Berichtsvorlage oder die [!DNL Excel], die für den Tabellen-Feed verwendet wird:

   * (Optional) Um eine andere oder aktualisierte Berichtsvorlage für den Feed zu verwenden, [erstellen Sie eine neue  [!DNL Excel]  für die Berichtsvorlage](#spreadsheet-feed-create-excel-template).

     Sie wählen die Berichtsvorlage aus und laden die neue [!DNL Excel] in den nächsten Schritten hoch.

   * (Optional) Um der [!DNL Excel]-Vorlage einfach benutzerdefinierte Spalten hinzuzufügen, fügen Sie die Spalten rechts neben den Spalten aus der Berichtsvorlage ein und speichern Sie dann die Datei als [!DNL Excel] Kalkulationstabelle im .XLSX-Format. Sie müssen im nächsten Schritt die neue [!DNL Excel]-Datei hochladen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Ändern der Einstellungen für den Tabellenvorschub:

   1. Aktivieren Sie das Kontrollkästchen neben dem Namen des Tabellen-Feeds.

   1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]**.

   1. Ändern Sie im Dialogfeld **[!UICONTROL Edit Spreadsheet Feed]** die [Tabellenvorschub](#spreadsheet-feed-settings).

   1. Klicken Sie auf **[!UICONTROL Submit]**.

   1. (Optional) Klicken Sie nach der *[!UICONTROL Finished]* des Feed-[!UICONTROL Update Status] auf **[!UICONTROL XLSX]** neben dem Feed und öffnen oder speichern Sie die Datei dann entsprechend dem normalen Verfahren Ihres Browsers.

   >[!NOTE]
   >
   > Wenn die mit dem Feed verknüpfte Berichtsvorlage später gelöscht wird, wird der Feed ebenfalls gelöscht.

   Tabellen-Feeds werden jeden Tag am konfigurierten [!UICONTROL Schedule Time] in der Zeitzone des Werbetreibenden automatisch aktualisiert. Die in der [!UICONTROL Email Recipients] des Feeds angegebenen Adressen erhalten Benachrichtigungen, wenn die Tabelle aktualisiert wird.

## Einstellungen für Tabellenbericht-Feeds {#spreadsheet-feed-settings}

| Feld | Beschreibung |
|---|---|
| [!UICONTROL Feed Name] | Ein Name für den Tabellenvorschub mit maximal 120 Zeichen. |
| [!UICONTROL Report Template] | Die Berichtsvorlage, die die erforderlichen Berichtsdaten angibt. Wählen Sie die Berichtsvorlage aus, die Sie zum Erstellen der [!DNL Excel] verwendet haben. Alle grundlegenden Berichtsvorlagen werden aufgelistet.<br><br><b>Hinweis:</b> Wenn Sie die für den Bericht verwendete Berichtsvorlage ändern oder die Spalten in der Vorlage aktualisieren, müssen Sie eine neue [!DNL Excel] erstellen und hochladen. |
| [!UICONTROL Excel Template] | Die speziell formatierte [!DNL Excel], die Sie im .XLSX-Format erstellt haben und die auf die in der Berichtsvorlage angegebenen Daten angewendet wird. Klicken Sie auf <b>[!UICONTROL Choose file]</b> , um die hochzuladende Datei zu suchen. |
| [!UICONTROL Back Fill From] | Das Anfangsdatum, für das die vorhandenen Daten auf der Registerkarte [!UICONTROL RAW] aktualisiert werden, angegeben durch eine Anzahl von Tagen in der Vergangenheit. Geben Sie einen Wert zwischen 1 und 90 ein, der größer als [!UICONTROL Back Fill Until] ist. Der Standardwert ist sieben (7) Tage.<br><br>Wenn der Wert beispielsweise 7 ist und heute der 7. März ist, werden die vorhandenen Daten auf der Registerkarte [!UICONTROL RAW] ab dem 1. März aktualisiert (bis zu dem im Parameter [!UICONTROL Back Fill Until] angegebenen Enddatum). Vorhandene Datenzeilen für Daten vor dem 1. März werden nicht gelöscht, aber nicht aktualisiert. |
| [!UICONTROL Back Fill Until] | Das Enddatum, für das die vorhandenen Daten auf der Registerkarte [!UICONTROL RAW] aktualisiert werden, was in der Vergangenheit durch eine Anzahl von Tagen dargestellt wurde. Geben Sie einen Wert zwischen 1 und 90 ein, der kleiner als [!UICONTROL Back Fill From] ist. Der Standardwert ist ein (1) Tag.<br><br>Wenn dieser Wert beispielsweise 1 ist und heute der 7. März ist, werden die vorhandenen Daten auf der Registerkarte [!UICONTROL RAW] bis zum 6. März aktualisiert (und beginnen mit dem im Parameter [!UICONTROL Back Fill From] angegebenen Startdatum). Wenn dieser Wert 1 ist, der [!UICONTROL Back Fill From] 7 ist und heute der 7. März ist, werden die vorhandenen Daten auf der Registerkarte [!UICONTROL RAW] vom 1. März bis zum 6. März aktualisiert. In beiden Beispielen werden vorhandene Datenzeilen für Daten nach dem 6. März nicht gelöscht, aber sie werden nicht aktualisiert. |
| [!UICONTROL Email Recipients] | E-Mail-Adressen, an die bei jeder Aktualisierung des Tabellen-Feeds Benachrichtigungen gesendet werden sollen. Standardmäßig wird die Adresse für Ihr Benutzerkonto eingegeben. Um mehrere Adressen anzugeben, trennen Sie sie durch Kommas, Leerzeichen oder neue Zeilen. |
| [!UICONTROL Schedule Time] | Der Zeitpunkt, zu dem der Tabellen-Feed jeden Tag in der Zeitzone des Werbetreibenden aktualisiert wird. Uhrzeit aus den verfügbaren Optionen auswählen. Der Standardwert für neue Tabellen-Feeds ist 10:00. |
| [!UICONTROL Email Notification] | Was in E-Mail-Benachrichtigungen an die angegebenen Adressen enthalten sein soll:<ul><li><i>[!UICONTROL Attach Feed (Max 10MB)]</i> — Versand einer Kopie des ausgefüllten Berichts im XLSX-Format. Wenn die Datei größer als 10 MB ist, enthält die Benachrichtigung keine Anlage.</li><li><i>[!UICONTROL Notification Only]</i> (Standard) - Zum Senden nur einer Benachrichtigung über das Abschließen oder Fehlschlagen eines Berichts mit einem Link zum Bericht.</li></ul> |

## Anzeigen der Einstellungen der zugehörigen Berichtsvorlage {#spreadsheet-feed-view-template}

Mit dem Zahnradsymbol **[!UICONTROL Template Settings]** wird ein Duplikat der Berichtsvorlage geöffnet, die mit dem Feed verknüpft ist. Das Öffnen des Duplikats speichert keine neue Vorlage und ändert auch nicht die zugehörige Vorlage des Feeds.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Klicken Sie auf das **[!UICONTROL Template Settings]** Zahnradsymbol neben dem Namen der zugehörigen Berichtsvorlage.

1. Überprüfen Sie die Berichteinstellungen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Cancel]** . Wenn Sie dazu aufgefordert werden, die Einrichtung zu verwerfen, klicken Sie auf **[!UICONTROL Discard]**.

Um die ursprüngliche Berichtsvorlage zu ändern, folgen Sie dem [Bearbeitungsvorgang für Berichtsvorlagen](report-templates-manage.md#template-edit). Um eine andere Vorlage für den Feed zu verwenden, [ Sie die Einstellungen für den Tabellenfeed ](#spreadsheet-feed-edit) und wählen Sie die Vorlage aus.

## Anzeigen oder Speichern einer Tabellenbericht-Feed-Datei {#spreadsheet-feed-view-or-save}

Sie können jeden generierten Tabellenfeed anzeigen oder in einer Datei speichern. Tabellen-Feed-Dateien befinden sich [!DNL Microsoft Excel] XLSX-Format.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Klicken Sie auf **[!UICONTROL XLSX]** neben dem Feed und öffnen oder speichern Sie die Datei dann entsprechend dem normalen Verfahren Ihres Browsers.

## Tabellenbericht-Feeds manuell aktualisieren {#spreadsheet-feed-refresh}

>[!NOTE]
>
>Tabellen-Feeds werden jeden Tag am konfigurierten [!UICONTROL Schedule Time] in der Zeitzone des Werbetreibenden automatisch aktualisiert.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem Feed, den Sie aktualisieren möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Run Spreadsheet]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

1. (Optional) Nachdem die [!UICONTROL Update Status] eines Feeds *[!UICONTROL Finished]* wurde, klicken Sie auf **[!UICONTROL XLSX]** neben dem Feed und öffnen oder speichern Sie dann die Datei entsprechend dem normalen Verfahren Ihres Browsers.

## Tabellenbericht-Feeds löschen {#spreadsheet-feed-delete}

>[!NOTE]
>
>Wenn die mit einem Feed verknüpfte Berichtsvorlage gelöscht wird, wird der Feed automatisch gelöscht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem Feed, den Sie löschen möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

## Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren {#copy-to-clipboard}

Kopieren Sie die sichtbaren Informationen in die ausgewählten Zeilen entsprechend den angewendeten Filtern und Spalten, die in der Ansicht sichtbar sind. Die Informationen werden als tabulatorgetrennte Werte (TSV) gespeichert.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Zeile, deren Daten Sie kopieren möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Copy]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.
