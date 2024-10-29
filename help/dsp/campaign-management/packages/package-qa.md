---
title: Überprüfen und Bearbeiten von Paketeinstellungen mithilfe von Bulksheets
description: Erfahren Sie, wie Sie wichtige Paketeinstellungen mithilfe von Tabellen stapelweise überprüfen und bearbeiten können.
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 0%

---

# Überprüfen und Bearbeiten von Paketeinstellungen mithilfe von Bulksheets

Sie können die Einstellungen für ein oder mehrere Pakete im XLSX-Format ([!DNL Microsoft Excel] Tabelle) zur Überprüfung herunterladen. Die Tabelle enthält einen separaten Tab mit Fluginformationen.

Um mehrere Einstellungen gleichzeitig zu aktualisieren, können Sie einen der folgenden Schritte ausführen:

* Nehmen Sie Änderungen an den ausgewählten Feldern vor, speichern Sie die Datei und laden Sie die bearbeitete Bulksheet-Datei wieder in DSP hoch.

* Um Änderungen an zusätzlichen Packages vorzunehmen und Einstellungen für beliebige Platzierungen oder Anzeigen vorzunehmen, laden Sie eine leere Bulksheet-Vorlage herunter, die Registerkarten für jeden Kampagnentyp enthält, geben Sie neue oder aktualisierte Einstellungen ein oder fügen Sie sie in die Vorlagendatei ein und laden Sie dann die Datei hoch, um die Änderungen vorzunehmen. Anweisungen finden Sie unter &quot;[Überprüfen und Bearbeiten der Einstellungen der Kampagnenkomponenten mit Bulksheets](/help/dsp/campaign-management/campaign-components-review-edit.md)&quot;.

Zu bearbeitbaren Feldern gehören die meisten Einstellungen, die normalerweise bearbeitbar sind.

>[!TIP]
>
>Informationen zum schnellen Bearbeiten von mehr Feldern für ein oder mehrere Pakete finden Sie unter &quot;[Pakete bearbeiten](/help/dsp/campaign-management/packages/package-edit.md)&quot;.

## Download-Einstellungen für alle Pakete in einer Kampagne

Wenn Sie Einstellungen für alle Kampagnenkits herunterladen, enthält die Tabelle separate Registerkarten für die Paketeinstellungen und für die Fluginformationen. Sie können optional Einstellungen für die Platzierungen und Anzeigen einbeziehen, die mit den Paketen verknüpft sind. Zusätzliche Registerkarten sind für Platzierungs- und Anzeigeneinstellungen enthalten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Download QA sheet]**.

1. Heben Sie im Dialogfeld [!UICONTROL QA Sheet Download] die Auswahl aller Kampagnenkomponenten auf, deren Einstellungen Sie aus der heruntergeladenen Datei ausschließen möchten, und klicken Sie auf **[!UICONTROL Download]**.

Standardmäßig werden Einstellungen für alle Platzierungen und Anzeigen ausgewählt, die mit den Paketen verknüpft sind.

Eine Benachrichtigung gibt an, wann die Datei zum Herunterladen verfügbar ist.

1. Führen Sie einen der folgenden Schritte aus, um die Datei herunterzuladen:

   * Klicken Sie in der Benachrichtigung auf **[!UICONTROL Download].**

   * Klicken Sie rechts oben in der Menüleiste auf ![Aufträge](/help/dsp/assets/downloads.png). Klicken Sie neben dem Auftrag auf **[!UICONTROL Download]** .

     Die Datei wird im Ordner Downloads des Browsers gespeichert. Eine Liste der enthaltenen Spalten finden Sie unter &quot;[Platzierungsspalten in heruntergeladenen/hochgeladenen Arbeitsblättern](#qa-sheet-columns)&quot;.

>[!NOTE]
>
>Sie können QA-Tabellen auf Kampagnenebene nicht bearbeiten und erneut hochladen. Um Änderungen an den Einstellungen der Kampagnenkomponenten in diesen Dateien vorzunehmen, laden Sie eine separate Bulksheet-Vorlage herunter, geben Sie Zeilen aus dem QA-Blatt ein oder fügen Sie sie in die Bulksheet-Vorlage ein, speichern Sie die Datei und laden Sie dann das ausgefüllte Bulksheet hoch. Anweisungen finden Sie unter &quot;[Überprüfen und Bearbeiten der Einstellungen der Kampagnenkomponenten mit Bulksheets](/help/dsp/campaign-management/campaign-components-review-edit.md)&quot;.

## Download-Einstellungen für ein oder mehrere Pakete

Wenn Sie Einstellungen für bestimmte Packages herunterladen, enthält die Bulksheet-Datei separate Registerkarten für die Paketeinstellungen und die Fluginformationen. Die Datei kann bearbeitet werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Packages]**.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   Eine Benachrichtigung gibt an, wann die Bulksheet-Datei zum Herunterladen verfügbar ist.

1. Um das Bulksheet herunterzuladen, führen Sie einen der folgenden Schritte aus:

   * Klicken Sie in der Benachrichtigung auf **[!UICONTROL Download].**

   * Klicken Sie rechts oben in der Menüleiste auf ![Aufträge](/help/dsp/assets/downloads.png). Klicken Sie neben dem Auftrag auf **[!UICONTROL Download]** .

     Die Datei wird im Ordner Downloads des Browsers gespeichert. Eine Liste der enthaltenen Spalten finden Sie unter &quot;[Platzierungsspalten in heruntergeladenen/hochgeladenen Arbeitsblättern](#qa-sheet-columns)&quot;.

<!-- I don't think I need this here

## Download a Bulksheet Template {#download-template}

You can optionally download a blank bulksheet template that includes tabs for each type of campaign component. You can later add rows to any tab on the template and [upload the edited file](##upload-bulksheet-package) to make changes. 

1. Click the name of the campaign.

1.  In the upper right, click **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   The file is saved to the browser's Downloads folder. See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns.

-->

## Hochladen eines Bulksheets mit Paketeinstellungen {#upload-bulksheet-package}

Sie können Einstellungen für Ihre Pakete, einschließlich der Platzierungen und Anzeigen, die mit den Paketen verknüpft sind, in eine Bulksheet-Datei hochladen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Im Dialogfeld [!UICONTROL Upload Bulksheet] :

   1. Ziehen Sie eine Datei in das Feld oder klicken Sie in das Feld, um eine Datei aus Ihrem Gerät oder Netzwerk auszuwählen.

   1. Klicken Sie auf **[!UICONTROL Upload]**.

1. (Optional) Um sicherzustellen, dass die Aktualisierungen verarbeitet wurden, klicken Sie rechts oben in der Menüleiste auf ![Aufträge](/help/dsp/assets/downloads.png) .

## Spalten für Paketeinstellungen in heruntergeladenen/hochgeladenen Tabellen{#qa-sheet-columns-packages}

>[!TIP]
>
> In einer heruntergeladenen Tabelle werden alle bearbeitbaren Spalten blau hervorgehoben.

### [!UICONTROL Package] Tab

| Abschnitt | Spalte | Beschreibung | Bearbeitbar? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | Die numerische ID des Pakets. | — |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | Der Name des Pakets. | Ja |
| [!UICONTROL Basic details] | [!UICONTROL Status] | Der Paketstatus: *[!UICONTROL active]* oder *[!UICONTROL inactive]*. | Ja |
| [!UICONTROL Basic details] | [!UICONTROL Description] | Eine optionale Beschreibung des Pakets. | Ja |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | Ein statischer Drittanbieter-Gebührensatz, der als nicht abrechnungsfähige Kosten pro 1000 Impressionen verfolgt werden kann, falls zutreffend. | Ja |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | Eine optionale Beschreibung des Drittanbieter-Gebührensatzes, falls zutreffend. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | Das Startdatum des Pakets. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | Das Enddatum des Pakets. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | Auf welcher Ebene Platzierungen im Paket zu platzieren und zu verschließen: *[!UICONTROL Package]* oder *[!UICONTROL Placement]*. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | Das Paket-Budget. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | Das Budgetintervall: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* oder *[!UICONTROL All Time]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | Eine optionale Budgetintervallbegrenzung. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | Das Intervall für die optionale Budgetintervallbegrenzung: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* oder *[!UICONTROL All Time]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | Ziel des Pakets. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | Der Zielwert des Ziels. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Nur Pakete mit den Optimierungszielen &quot;[!UICONTROL Highest Return on Ad Spend]&quot; und &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;)Ein [benutzerdefiniertes Ziel](/help/dsp/optimization/custom-goal.md) , das die Umsatz- oder Konversionsereignisse enthält, die zur Berechnung der CPA- oder ROAS-Metrik verwendet werden. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Optional; nur Pakete mit den Optimierungszielen &quot;[!UICONTROL Highest Return on Ad Spend]&quot;und &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;) Das endgültige Konversionsereignis bzw. der endgültige Konversionsereignis/-verkaufsbetrag, der zur Berechnung der Rendite aus Werbeausgaben oder der Kosten pro Akquise verwendet werden soll. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Nur Pakete mit benutzerdefinierten Optimierungszielen) Der Zweck des Pakets, der bei der Bestimmung der Optimierung des Pakets hilft: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]* oder *[!UICONTROL Other]* . | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Nur Pakete mit benutzerdefinierten Optimierungszielen) Die Paket-ID für ein anderes Paket, dessen historische Daten zur Optimierung des Pakets verwendet werden. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Nur Pakete mit benutzerdefinierten Optimierungszielen) Ein weiteres Paket, dessen historische Daten als Eingabe für die Optimierung des Pakets verwendet werden. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Ob das Paket in Richtung *[!UICONTROL budget]* oder *[!UICONTROL primary_goal]* (für Impressionen) bewegt wird. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (Wenn Sie das Paket bei Impressionen platzieren) Die Zielanzahl der Impressionen während des angegebenen Zeitintervalls. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (Wenn Sie das Paket bei Impressionen platzieren) Das Zeitintervall für die Zielanzahl der Impressionen. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | Die Flugplatzstrategie für das Paket: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* oder *[!UICONTROL aggressive frontload]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | Die Intraday-Geschwindigkeit für das Paket: *[!UICONTROL Even]* oder *[!UICONTROL ASAP]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | Die primäre Frequenzbegrenzung für die Verpackung während des angegebenen [!UICONTROL Frequency Cap Interval]. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | Das Intervall für die primäre Frequenzbegrenzung: *[!UICONTROL Day]*, *[!UICONTROL Week]* oder *[!UICONTROL Month]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | Die Anzahl der Wochen, Tage, Stunden oder Minuten, für die der primäre [!UICONTROL Frequency Cap] gilt. Wenn die primäre Obergrenze beispielsweise 12 Impressionen pro Monat beträgt, lautet der Wert hier `12`. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | Die sekundäre Frequenzbegrenzung für die Verpackung während des angegebenen [!UICONTROL Secondary Frequency Cap Interval] | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | Der Intervalltyp für die sekundäre Frequenzbegrenzung: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* oder *[!UICONTROL Minute]*. Die anwendbare Anzahl von Wochen, Tagen, Stunden oder Minuten wird durch die [!UICONTROL Secondary Frequency Cap Interval Value] angegeben. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | Die Anzahl der Wochen, Tage, Stunden oder Minuten, für die der [!UICONTROL Secondary Frequency Cap] gilt. Wenn die sekundäre Begrenzung beispielsweise drei Impressionen pro sechs Stunden beträgt, wäre der Wert hier `6`. | Ja |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Gibt an, ob für das Paket *T* (true) oder *F* (false) nicht gerade Geschwindigkeitsflüge erstellt werden sollen. Nachdem Sie die benutzerdefinierte Beleuchtung aktiviert und das Paket gespeichert haben, können Sie die benutzerdefinierte Beleuchtung nicht deaktivieren und das Startdatum des Pakets nicht bearbeiten. | — |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Nur verfügbar, wenn die Option [!UICONTROL Activate Custom Flighting] aktiviert ist) Gibt an, ob automatisch ein eventuell aus dem vorhergehenden Flug bestehendes Budget für den nächsten Flug hinzugefügt werden soll: *T* (true) oder *F* (false). | Ja |
| [!UICONTROL Error] | [!UICONTROL Error] | Alle relevanten Fehler. | — |

### [!UICONTROL Package_Flights] Tab {#qa-sheet-columns-package-flights}

| Abschnitt | Spalte | Beschreibung | Bearbeitbar? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | Die numerische ID des Pakets. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | Numerische Kennung des Fluges. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] | Das erste Datum des Fluges. | Ja |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | Das Enddatum des Fluges. | Ja |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | Das Zielausgabenziel für den Flug. | Ja |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Vorhandene Pakete ohne aktivierte &quot;[!UICONTROL Automatically rollover remaining flight budget to next flight]&quot;-Option) Ein Betrag an potenziell nicht verwendetem Budget, der zum nächsten Flug hinzugefügt werden soll. | Ja |

>[!MORELIKETHIS]
>
>* [Überprüfen und Bearbeiten der Einstellungen der Kampagnenkomponente mithilfe von Bulksheets](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [Bearbeiten von Paketen](/help/dsp/campaign-management/packages/package-edit.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
