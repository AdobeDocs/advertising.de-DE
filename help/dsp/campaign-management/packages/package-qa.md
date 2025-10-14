---
title: Überprüfen und Bearbeiten von Paketeinstellungen mithilfe von Bulksheets
description: Erfahren Sie, wie Sie wichtige Paketeinstellungen mithilfe von Tabellen stapelweise überprüfen und bearbeiten können.
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
source-git-commit: c482f476de5b79ee9a363791d62ba8c2ada12cbc
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# Überprüfen und Bearbeiten von Paketeinstellungen mithilfe von Bulksheets

Sie können die Einstellungen für ein oder mehrere Pakete im XLSX-Format ([!DNL Microsoft Excel]-Arbeitsblatt) zur Überprüfung herunterladen. Die *Bulksheet*-Datei enthält eine separate Registerkarte mit Fluginformationen.

Um mehrere Einstellungen gleichzeitig zu aktualisieren, haben Sie folgende Möglichkeiten:

* Nehmen Sie Änderungen an den Feldern vor, speichern Sie die Datei und laden Sie die bearbeitete Bulksheet-Datei wieder in DSP hoch.

* Um Änderungen an zusätzlichen Paketen, Platzierungen oder Anzeigen in der Kampagne vorzunehmen, laden Sie ein Bulksheet für die Kampagne herunter. Geben Sie aktualisierte Einstellungen ein oder fügen Sie sie in die Datei ein und laden Sie dann die Datei hoch, um die Änderungen vorzunehmen. Anweisungen finden Sie unter [Überprüfen und Bearbeiten der Einstellungen von Kampagnenkomponenten mithilfe von Bulksheets](/help/dsp/campaign-management/campaign-components-review-edit.md).

Bearbeitbare Felder enthalten die meisten Einstellungen, die normalerweise bearbeitet werden können.

>[!TIP]
>
>Informationen zum schnellen Bearbeiten mehrerer Felder für ein oder mehrere Pakete finden Sie unter [Bearbeiten von Paketen](/help/dsp/campaign-management/packages/package-edit.md).

## Download-Einstellungen für alle Pakete in einer Kampagne

Wenn Sie Einstellungen für alle Pakete in einer Kampagne herunterladen, enthält die Bulksheet separate Registerkarten für die Paketeinstellungen und für die Fluginformationen. Sie können optional Einstellungen für die Platzierungen und Anzeigen einbeziehen, die mit den Paketen verknüpft sind. Zusätzliche Registerkarten sind für die Platzierungs- und Anzeigeneinstellungen enthalten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie neben der Kampagne auf **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   * Klicken Sie auf den Namen der Kampagne. Klicken Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

1. Heben Sie im Dialogfeld [!UICONTROL Bulksheet Download] die Auswahl aller Kampagnenkomponenten auf, deren Einstellungen Sie aus der heruntergeladenen Datei ausschließen möchten, und klicken Sie dann auf **[!UICONTROL Download]**.

Standardmäßig sind Einstellungen für alle Platzierungen und Anzeigen ausgewählt, die mit den Paketen verknüpft sind.

Eine Benachrichtigung gibt an, wann die Datei zum Herunterladen verfügbar ist.

1. Führen Sie einen der folgenden Schritte aus, um die Datei herunterzuladen:

   * Klicken Sie in der Benachrichtigung auf **[!UICONTROL Download].**

   * Klicken Sie oben rechts in der Menüleiste auf ![Aufträge](/help/dsp/assets/downloads.png). Klicken Sie neben dem Auftrag auf **[!UICONTROL Download]** .

     Die Datei wird im Ordner „Downloads“ des Browsers gespeichert.<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

     Um eine der Einstellungen zu bearbeiten, bearbeiten Sie die Datei direkt und laden Sie dann die Änderungen hoch. Alle bearbeitbaren Spalten sind blau hervorgehoben.

## Download-Einstellungen für bestimmte Pakete

Wenn Sie Einstellungen für bestimmte Pakete herunterladen, enthält die Bulksheet-Datei separate Registerkarten für die Paketeinstellungen und für die Fluginformationen, und die Datei kann bearbeitet werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Packages]**.

1. Aktivieren Sie die Kontrollkästchen der Pakete, deren Einstellungen Sie herunterladen möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   Eine Benachrichtigung zeigt an, wann die Bulksheet-Datei zum Download verfügbar ist.

1. Führen Sie einen der folgenden Schritte aus, um das Bulksheet herunterzuladen:

   * Klicken Sie in der Benachrichtigung auf **[!UICONTROL Download].**

   * Klicken Sie oben rechts in der Menüleiste auf ![Aufträge](/help/dsp/assets/downloads.png). Klicken Sie neben dem Auftrag auf **[!UICONTROL Download]** .

     Die Datei wird im Ordner Downloads des Browsers gespeichert. Unter &quot;[&#x200B; in heruntergeladenen/hochgeladenen Bulksheets](#qa-sheet-columns) finden Sie eine Liste der eingeschlossenen Spalten.

     Um eine der Einstellungen zu bearbeiten, bearbeiten Sie die Datei direkt und laden Sie dann die Änderungen hoch. Alle bearbeitbaren Spalten sind blau hervorgehoben. Um das richtige Format für ein Feld zu verwenden, wählen Sie den Wert aus der entsprechenden Paketeinstellung oder Platzierungseinstellung aus und kopieren Sie ihn. Für einige Zieleinstellungen, wie z. B. DayParting, benutzerdefinierte Ziele und Konversionsmetriken, ist eine Kopieroption innerhalb der Einstellung verfügbar.

## Hochladen einer Bulksheet mit Paketeinstellungen {#upload-bulksheet-package}

Sie können Einstellungen für Ihre Pakete, einschließlich der Platzierungen und Anzeigen, die mit den Paketen verknüpft sind, in eine Bulksheet-Datei hochladen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie neben der übergeordneten Kampagne auf **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

   * Klicken Sie auf den Namen der Kampagne. Klicken Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

     Diese Option ist auf der Registerkarte [!UICONTROL Packages], [!UICONTROL Placements] oder [!UICONTROL Ads] verfügbar.

   * Klicken Sie im Untermenü auf **[!UICONTROL Packages]** und aktivieren Sie das Kontrollkästchen für jedes Paket. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Im Dialogfeld [!UICONTROL Upload Bulksheet] :

   1. Ziehen Sie eine Datei per Drag-and-Drop in das Feld oder klicken Sie in das Feld, um eine Datei auf Ihrem Gerät oder Netzwerk auszuwählen.

   1. Klicken Sie auf **[!UICONTROL Upload]**.

1. (Optional) Um sicherzustellen, dass die Aktualisierungen verarbeitet wurden, klicken ![&#x200B; rechts &#x200B;](/help/dsp/assets/downloads.png) der oberen Menüleiste auf „Vorgänge“.

Wenn eine Aktualisierung der Einstellungen fehlschlägt, können Sie eine Bulksheet-Fehlerdatei mit Farbcodierung herunterladen, um anzuzeigen, welche Einstellungen (Zeilen) gespeichert wurden und welche fehlgeschlagen sind, wobei für jeden Fehler ein Grund angegeben wird. Sie können dann die Probleme in derselben Datei beheben und sie erneut hochladen, um die korrigierten Informationen zu verarbeiten.

<!--
## Package Setting Columns in Downloaded/Uploaded Bulksheets{#qa-sheet-columns-packages}

>[!TIP]
>
> In a downloaded bulksheet file, all editable columns are highlighted in blue.

### [!UICONTROL Package] Tab

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | The name of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Status] | The package status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL Description] | An optional description of the package. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | Yes |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | An optional description of the third-party fee rate, if applicable. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | The start date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | The end date of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | At which level to pace and cap placements in the package: *[!UICONTROL Package]* or *[!UICONTROL Placement]*. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | The package budget. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | An optional budget interval cap. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | The interval for the optional budget interval cap: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | The objective of the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | The target value of the goal. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only)A [custom goal](/help/dsp/optimization/custom-goal.md) that includes the revenue or conversion events used to calculate the CPA or ROAS metric. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Optional; packages with the "[!UICONTROL Highest Return on Ad Spend]" and "[!UICONTROL Lowest Cost per Acquisition]" optimization goals only) The final conversion event or revenue event/sale amount to use for computing the return on ad spend or the cost per acquisition. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Packages with custom optimization goals only) The purpose of the package, which helps determine how to optimize the package: *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]*, or *[!UICONTROL Other]* . | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Packages with custom optimization goals only) The package ID for another package whose historic data is used as input for optimizing the package. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Packages with custom optimization goals only) Another package whose historic data is used as input for optimizing the package. | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Whether the package is pacing towards the *[!UICONTROL budget]* or *[!UICONTROL primary_goal]* (for impressions). | &mdash; |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (When you pace the package on impressions) The target number of impressions during the specified time interval. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (When you pace the package on impressions) The time interval for the target number of impressions. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the package: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the package: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | The primary frequency cap for the package during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the primary [!UICONTROL Frequency Cap] applies. For example, if the primary cap is 12 impressions per month, then the value here would be `12`. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the package during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Whether or not to create non-even pacing flights for the package*T* (true) or *F* (false). Once you enable custom flighting and save the package, you can't disable custom flighting nor edit the package start date. | &mdash; |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Available only when the [!UICONTROL Activate Custom Flighting] option is enabled) Whether or not to automatically add any remaining budget from the previous flight to the existing budget for the next flight: *T* (true) or *F* (false). | Yes |
| [!UICONTROL Error] | [!UICONTROL Error] | Any relevant errors. | &mdash; |

### [!UICONTROL Package_Flights] Tab {#qa-sheet-columns-package-flights}

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | The numeric ID of the package. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | The numeric ID of the flight. | &mdash; |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] |The first date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | The final date of the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | The target spend goal for the flight. | Yes |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Existing packages without the "[!UICONTROL Automatically rollover remaining flight budget to next flight]" option enabled) An amount of potentially unspent budget to add to the next flight. | Yes |
-->

>[!MORELIKETHIS]
>
>* [Überprüfen und Bearbeiten der Einstellungen der Kampagnenkomponenten mithilfe von Bulksheets](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [Pakete bearbeiten](/help/dsp/campaign-management/packages/package-edit.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
