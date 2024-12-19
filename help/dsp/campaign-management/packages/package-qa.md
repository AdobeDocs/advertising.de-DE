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

Sie können die Einstellungen für ein oder mehrere Pakete im XLSX-Format ([!DNL Microsoft Excel]-Arbeitsblatt) zur Überprüfung herunterladen. Das Arbeitsblatt enthält eine separate Registerkarte mit Fluginformationen.

Um mehrere Einstellungen gleichzeitig zu aktualisieren, haben Sie folgende Möglichkeiten:

* Nehmen Sie Änderungen an den Feldern vor, speichern Sie die Datei und laden Sie die bearbeitete Bulksheet-Datei wieder in DSP hoch.

* Wenn Sie Änderungen an zusätzlichen Paketen und Einstellungen für eine Platzierung oder Anzeige vornehmen möchten, laden Sie eine leere Bulksheet-Vorlage herunter, die Registerkarten für jeden Kampagnentyp enthält, geben Sie neue oder aktualisierte Einstellungen ein oder fügen Sie sie in die Vorlagendatei ein und laden Sie dann die Datei hoch, um die Änderungen vorzunehmen. Anweisungen finden Sie unter [Überprüfen und Bearbeiten der Einstellungen von Kampagnenkomponenten mithilfe von Bulksheets](/help/dsp/campaign-management/campaign-components-review-edit.md).

Bearbeitbare Felder enthalten die meisten Einstellungen, die normalerweise bearbeitet werden können.

>[!TIP]
>
>Informationen zum schnellen Bearbeiten mehrerer Felder für ein oder mehrere Pakete finden Sie unter [Bearbeiten von Paketen](/help/dsp/campaign-management/packages/package-edit.md).

## Download-Einstellungen für alle Pakete in einer Kampagne

Wenn Sie Einstellungen für alle Pakete in einer Kampagne herunterladen, enthält die Kalkulationstabelle separate Registerkarten für die Paketeinstellungen und für die Fluginformationen. Sie können optional Einstellungen für die Platzierungen und Anzeigen einbeziehen, die mit den Paketen verknüpft sind. Zusätzliche Registerkarten sind für die Platzierungs- und Anzeigeneinstellungen enthalten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Download QA sheet]**.

1. Heben Sie im Dialogfeld [!UICONTROL QA Sheet Download] die Auswahl aller Kampagnenkomponenten auf, deren Einstellungen Sie aus der heruntergeladenen Datei ausschließen möchten, und klicken Sie dann auf **[!UICONTROL Download]**.

Standardmäßig sind Einstellungen für alle Platzierungen und Anzeigen ausgewählt, die mit den Paketen verknüpft sind.

Eine Benachrichtigung gibt an, wann die Datei zum Herunterladen verfügbar ist.

1. Führen Sie einen der folgenden Schritte aus, um die Datei herunterzuladen:

   * Klicken Sie in der Benachrichtigung auf **[!UICONTROL Download].**

   * Klicken Sie oben rechts in der Menüleiste auf ![Aufträge](/help/dsp/assets/downloads.png). Klicken Sie neben dem Auftrag auf **[!UICONTROL Download]** .

     Die Datei wird im Ordner Downloads des Browsers gespeichert. Unter &quot;[ in heruntergeladenen/hochgeladenen ](#qa-sheet-columns)&quot; finden Sie eine Liste der eingeschlossenen Spalten.

>[!NOTE]
>
>QA-Tabellen auf Kampagnenebene können nicht bearbeitet und erneut hochgeladen werden. Um Änderungen an den Einstellungen der Kampagnenkomponenten in diesen Dateien vorzunehmen, laden Sie eine separate Bulksheet-Vorlage herunter, geben oder fügen Sie Zeilen aus dem QA-Blatt in die Bulksheet-Vorlage ein, speichern die Datei und laden Sie dann das ausgefüllte Bulksheet hoch. Anweisungen finden Sie unter [Überprüfen und Bearbeiten der Einstellungen von Kampagnenkomponenten mithilfe von Bulksheets](/help/dsp/campaign-management/campaign-components-review-edit.md).

## Download-Einstellungen für ein oder mehrere Pakete

Wenn Sie Einstellungen für bestimmte Pakete herunterladen, enthält die Bulksheet-Datei separate Registerkarten für die Paketeinstellungen und für die Fluginformationen, und die Datei kann bearbeitet werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Packages]**.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   Eine Benachrichtigung zeigt an, wann die Bulksheet-Datei zum Download verfügbar ist.

1. Führen Sie einen der folgenden Schritte aus, um das Bulksheet herunterzuladen:

   * Klicken Sie in der Benachrichtigung auf **[!UICONTROL Download].**

   * Klicken Sie oben rechts in der Menüleiste auf ![Aufträge](/help/dsp/assets/downloads.png). Klicken Sie neben dem Auftrag auf **[!UICONTROL Download]** .

     Die Datei wird im Ordner Downloads des Browsers gespeichert. Unter &quot;[ in heruntergeladenen/hochgeladenen ](#qa-sheet-columns)&quot; finden Sie eine Liste der eingeschlossenen Spalten.

<!-- I don't think I need this here

## Download a Bulksheet Template {#download-template}

You can optionally download a blank bulksheet template that includes tabs for each type of campaign component. You can later add rows to any tab on the template and [upload the edited file](##upload-bulksheet-package) to make changes. 

1. Click the name of the campaign.

1.  In the upper right, click **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   The file is saved to the browser's Downloads folder. See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns.

-->

## Hochladen einer Bulksheet mit Paketeinstellungen {#upload-bulksheet-package}

Sie können Einstellungen für Ihre Pakete, einschließlich der Platzierungen und Anzeigen, die mit den Paketen verknüpft sind, in eine Bulksheet-Datei hochladen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Im Dialogfeld [!UICONTROL Upload Bulksheet] :

   1. Ziehen Sie eine Datei per Drag-and-Drop in das Feld oder klicken Sie in das Feld, um eine Datei auf Ihrem Gerät oder Netzwerk auszuwählen.

   1. Klicken Sie auf **[!UICONTROL Upload]**.

1. (Optional) Um sicherzustellen, dass die Aktualisierungen verarbeitet wurden, klicken ![ rechts ](/help/dsp/assets/downloads.png) der oberen Menüleiste auf „Vorgänge“.

## Spalten für Paketeinstellungen in heruntergeladenen/hochgeladenen Tabellen{#qa-sheet-columns-packages}

>[!TIP]
>
> In einer heruntergeladenen Tabelle werden alle bearbeitbaren Spalten blau hervorgehoben.

### Registerkarte [!UICONTROL Package]

| Abschnitt | Spalte | Beschreibung | Bearbeitbar? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | Die numerische ID des Pakets. | — |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | Der Name des Pakets. | Ja |
| [!UICONTROL Basic details] | [!UICONTROL Status] | Der Paketstatus: *[!UICONTROL active]* oder *[!UICONTROL inactive]*. | Ja |
| [!UICONTROL Basic details] | [!UICONTROL Description] | Eine optionale Beschreibung des Pakets. | Ja |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | Ein statischer Gebührensatz eines Drittanbieters, der als nicht fakturierbare Kosten pro 1000 Impressionen erfasst werden soll, falls zutreffend. | Ja |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | Gegebenenfalls eine optionale Beschreibung des Gebührensatzes für Dritte. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | Das Startdatum des Pakets. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | Das Enddatum des Pakets. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | Auf welcher Ebene Platzierungen im Paket platziert und begrenzt werden sollen: *[!UICONTROL Package]* oder *[!UICONTROL Placement]*. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | Das Budgetpaket. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | Das Budgetintervall: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* oder *[!UICONTROL All Time]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | Eine optionale Budgetintervallbegrenzung. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | Das Intervall für die optionale Budgetintervallbegrenzung: &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* oder *[!UICONTROL All Time]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | Das Ziel des Pakets. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | Der Zielwert des Ziels. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Nur Pakete mit den Optimierungszielen &quot;[!UICONTROL Highest Return on Ad Spend]&quot; und &quot;[!UICONTROL Lowest Cost per Acquisition]„)Ein [benutzerdefiniertes Ziel](/help/dsp/optimization/custom-goal.md) das die Umsatz- oder Konversionsereignisse enthält, die zur Berechnung der CPA- oder ROAS-Metrik verwendet werden. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Optional, Pakete nur mit den Optimierungszielen &quot;[!UICONTROL Highest Return on Ad Spend]&quot; und &quot;[!UICONTROL Lowest Cost per Acquisition]„) Das endgültige Konversionsereignis oder der Umsatz/Umsatzbetrag, der für die Berechnung der Rendite auf Werbeausgaben oder der Kosten pro Akquise verwendet werden soll. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Nur Pakete mit benutzerdefinierten Optimierungszielen) Der Zweck des Pakets, mit dem bestimmt werden kann, wie das Paket optimiert werden kann: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]* oder *[!UICONTROL Other]* . | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Nur Pakete mit benutzerdefinierten Optimierungszielen) Die Paket-ID für ein anderes Paket, dessen historische Daten als Eingabe für die Optimierung des Pakets verwendet werden. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Nur Pakete mit benutzerdefinierten Optimierungszielen) Ein weiteres Paket, dessen historische Daten als Eingabe für die Optimierung des Pakets verwendet werden. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Gibt an, ob sich das Paket in Richtung *[!UICONTROL budget]* oder *[!UICONTROL primary_goal]* bewegt (bei Impressionen). | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (Wenn Sie das Paket auf Impressionen platzieren) Die Zielanzahl der Impressionen im angegebenen Zeitintervall. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (Wenn Sie das Paket auf Impressionen platzieren) Das Zeitintervall für die Zielanzahl von Impressionen. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | Die Geschwindigkeits-Strategie für das Paket: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* oder *[!UICONTROL aggressive frontload]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | Die Intraday-Geschwindigkeit für das Paket: *[!UICONTROL Even]* oder *[!UICONTROL ASAP]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | Die primäre Häufigkeitsbegrenzung für das Paket während des angegebenen [!UICONTROL Frequency Cap Interval]. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | Das Intervall für die primäre Frequenzbegrenzung: *[!UICONTROL Day]*, *[!UICONTROL Week]* oder *[!UICONTROL Month]*. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | Die Anzahl der Wochen, Tage, Stunden oder Minuten, für die die primäre [!UICONTROL Frequency Cap] gilt. Wenn die primäre Begrenzung beispielsweise 12 Impressions pro Monat ist, würde der Wert hier `12`. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | Die sekundäre Häufigkeitsbegrenzung für das Paket während des angegebenen [!UICONTROL Secondary Frequency Cap Interval] | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | Der Intervalltyp für die sekundäre Frequenzbegrenzung: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* oder *[!UICONTROL Minute]*. Die entsprechende Anzahl von Wochen, Tagen, Stunden oder Minuten wird durch die [!UICONTROL Secondary Frequency Cap Interval Value] angegeben. | Ja |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | Die Anzahl der Wochen, Tage, Stunden oder Minuten, für die die [!UICONTROL Secondary Frequency Cap] gilt. Wenn die sekundäre Begrenzung beispielsweise drei Impressions pro sechs Stunden beträgt, wird der Wert hier `6`. | Ja |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Ob ungleiche Schrittmacherflüge für das Package.T ** (true) oder *F* (false) erstellt werden sollen. Nachdem Sie benutzerdefinierte Flüge aktiviert und das Paket gespeichert haben, können Sie benutzerdefinierte Flüge nicht mehr deaktivieren und auch das Startdatum des Pakets nicht mehr bearbeiten. | — |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Nur verfügbar, wenn die Option &quot;[!UICONTROL Activate Custom Flighting]&quot; aktiviert ist) Gibt an, ob das verbleibende Budget des vorherigen Fluges automatisch zum vorhandenen Budget des nächsten Fluges hinzugefügt werden soll: *T* (true) oder *F* (false). | Ja |
| [!UICONTROL Error] | [!UICONTROL Error] | Alle relevanten Fehler. | — |

### Registerkarte [!UICONTROL Package_Flights] {#qa-sheet-columns-package-flights}

| Abschnitt | Spalte | Beschreibung | Bearbeitbar? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | Die numerische ID des Pakets. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | Die numerische ID des Fluges. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] | Das erste Datum des Fluges. | Ja |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | Das Enddatum des Fluges. | Ja |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | Das Ziel der Ausgaben für den Flug. | Ja |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Bestehende Pakete ohne aktivierte Option &quot;[!UICONTROL Automatically rollover remaining flight budget to next flight]„) Ein Betrag, der möglicherweise nicht ausgegeben wurde und zum nächsten Flug hinzugefügt werden soll. | Ja |

>[!MORELIKETHIS]
>
>* [Überprüfen und Bearbeiten der Einstellungen der Kampagnenkomponenten mithilfe von Bulksheets](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [Pakete bearbeiten](/help/dsp/campaign-management/packages/package-edit.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
