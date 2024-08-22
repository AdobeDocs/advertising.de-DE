---
title: Überprüfen und Bearbeiten von Paketeinstellungen mithilfe von Tabellen
description: Erfahren Sie, wie Sie wichtige Paketeinstellungen mithilfe von Tabellen überprüfen und bearbeiten können.
feature: DSP Packages
source-git-commit: 230a169611aa3094365a877476f2e5e1c6b3cb9b
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 0%

---

# Überprüfen und Bearbeiten von Paketeinstellungen mithilfe von Tabellen

Sie können die Einstellungen für ein oder mehrere Pakete im XLSX-Format ([!DNL Microsoft Excel] Tabelle) zur Überprüfung herunterladen. Die Tabelle enthält einen separaten Tab mit Fluginformationen. Anschließend können Sie auf beiden Registerkarten Änderungen an den ausgewählten Feldern vornehmen und die Daten wieder DSP alle gleichzeitig hochladen. Zu bearbeitbaren Feldern gehören die meisten Einstellungen, die normalerweise bearbeitbar sind.

>[!TIP]
>
>Informationen zum Bearbeiten von mehr Feldern für ein oder mehrere Pakete finden Sie unter &quot;[Bearbeiten von Paketen](/help/dsp/campaign-management/packages/package-edit.md)&quot;.

## Download-Einstellungen für ein oder mehrere Pakete

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Packages]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem Paket, dessen Einstellungen Sie herunterladen möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL ...]** > **[!UICONTROL Download Edit in Excel Sheet]**.

Die Datei wird automatisch im Ordner Download des Browsers gespeichert. Eine Liste der enthaltenen Spalten finden Sie unter &quot;[Spalten in heruntergeladenen/hochgeladenen Arbeitsblättern verpacken](#qa-sheet-columns-packages)&quot;.

## Upload-Einstellungen für ein oder mehrere Pakete

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Packages]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem Paket, dessen Einstellungen Sie hochladen möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL ...]** > **[!UICONTROL Upload Edit in Excel Sheet]**.

1. Im Dialogfeld [!UICONTROL Edit in Excel] :

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
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Nur Pakete mit benutzerdefinierten Optimierungszielen) Der Zweck des Pakets, der bei der Bestimmung der Optimierung des Pakets hilft: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]* oder *[!UICONTROL Other]* . | — |
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

### [!UICONTROL Package_Flights] Tab

| Abschnitt | Spalte | Beschreibung | Bearbeitbar? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | Die numerische ID des Pakets. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | Numerische Kennung des Fluges. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] | Das erste Datum des Fluges. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | Das Enddatum des Fluges. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | Das Zielausgabenziel für den Flug. | — |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Vorhandene Pakete ohne aktivierte &quot;[!UICONTROL Automatically rollover remaining flight budget to next flight]&quot;-Option) Ein Betrag an potenziell nicht verwendetem Budget, der zum nächsten Flug hinzugefügt werden soll. | — |

>[!MORELIKETHIS]
>
>* [Bearbeiten von Paketen](/help/dsp/campaign-management/packages/package-edit.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
