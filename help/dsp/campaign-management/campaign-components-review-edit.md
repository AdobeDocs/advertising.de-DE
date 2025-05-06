---
title: Überprüfen und Bearbeiten der Einstellungen von Kampagnenkomponenten mithilfe von Bulksheets
description: Erfahren Sie, wie Sie wichtige Paket-, Platzierungs- und Anzeigeneinstellungen mithilfe von Tabellen stapelweise überprüfen und bearbeiten können.
feature: DSP Placements
exl-id: 1ec8362a-d37b-4fd7-becd-3a5b4f0c9504
source-git-commit: 7af6788f2aae3a2fb9e2048676dbe1955c2e56d9
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# Überprüfen und Bearbeiten der Einstellungen von Kampagnenkomponenten mithilfe von Bulksheets

Sie können die Einstellungen für die Pakete, Platzierungen und Anzeigen in einer einzelnen Kampagne im XLSX-Format ([!DNL Microsoft Excel]-Arbeitsblatt) herunterladen, um die Einstellungen zu überprüfen und zu bearbeiten. Standardmäßig enthält die heruntergeladene Datei, die als *bezeichnet wird,* separate Registerkarten für Paketeinstellungen, Paketfluginformationen, Platzierungseinstellungen und Platzierungs-Anzeigenzeitpläne. Optional können Sie die Einstellungen für einige Kampagnenkomponentententypen ausschließen.

Um mehrere Einstellungen gleichzeitig zu aktualisieren, laden Sie eine gültige Bulksheet-Datei mit den Änderungen hoch. Um die Bulksheet zu erstellen, bearbeiten Sie eine heruntergeladene Bulksheet mit den vorhandenen Einstellungen. Bearbeitbare Felder enthalten die meisten Einstellungen, die normalerweise bearbeitet werden können. Felder für nicht verwendete Einstellungen enthalten leere Werte.

>[!NOTE]
>
>Sie können die Einstellungen auch nur für bestimmte Pakete und bestimmte Platzierungen herunterladen und bearbeiten. Siehe [Überprüfen und Bearbeiten von Paketeinstellungen mithilfe von Bulksheets](/help/dsp/campaign-management/packages/package-qa.md) und [Überprüfen und Bearbeiten von Platzierungseinstellungen mithilfe von Bulksheets](/help/dsp/campaign-management/placements/placement-qa.md).

## Download-Einstellungen für die Pakete, Platzierungen und Anzeigen in einer Kampagne {#download-bulksheet-campaign}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie neben der Kampagne auf **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   * Klicken Sie auf den Namen der Kampagne. Klicken Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

1. Heben Sie im Dialogfeld [!UICONTROL Bulksheet Download] die Auswahl aller Kampagnenkomponenten auf, deren Einstellungen Sie aus der heruntergeladenen Datei ausschließen möchten, und klicken Sie dann auf **[!UICONTROL Download]**.

Standardmäßig sind Einstellungen für alle Kampagnenkomponenten ausgewählt.

Eine Benachrichtigung gibt an, wann die Datei zum Herunterladen verfügbar ist.

1. Führen Sie einen der folgenden Schritte aus, um die Datei herunterzuladen:

   * Klicken Sie in der Benachrichtigung auf **[!UICONTROL Download].**

   * Klicken Sie oben rechts in der Menüleiste auf ![Aufträge](/help/dsp/assets/downloads.png). Klicken Sie neben dem Auftrag auf **[!UICONTROL Download]** .

     Die Datei wird im Ordner „Downloads“ des Browsers gespeichert.<!-- See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns. -->

     Um eine der Einstellungen zu bearbeiten, bearbeiten Sie die Datei direkt und laden Sie dann die Änderungen hoch. Alle bearbeitbaren Spalten sind blau hervorgehoben. Um das richtige Format für ein Feld zu verwenden, wählen Sie den Wert aus der entsprechenden Paketeinstellung oder Platzierungseinstellung aus und kopieren Sie ihn. Für einige Zieleinstellungen, wie z. B. DayParting, benutzerdefinierte Ziele und Konversionsmetriken, ist eine Kopieroption innerhalb der Einstellung verfügbar.

## Hochladen einer Bulksheet mit Paket-, Platzierungs- und Anzeigeneinstellungen für eine Kampagne{#upload-bulksheet-campaign-components}

Laden Sie Einstellungen für Pakete, Platzierungen und Anzeigen in einer Kampagne gleichzeitig in einer ausgefüllten Bulksheet hoch.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie neben der Kampagne auf **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

   * Klicken Sie auf den Namen der Kampagne. Klicken Sie oben rechts auf **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Im Dialogfeld [!UICONTROL Upload Bulksheet] :

   1. Ziehen Sie eine Datei per Drag-and-Drop in das Feld oder klicken Sie in das Feld, um eine Datei auf Ihrem Gerät oder Netzwerk auszuwählen.

   1. Klicken Sie auf **[!UICONTROL Upload]**.

1. (Optional) Um sicherzustellen, dass die Aktualisierungen verarbeitet wurden, klicken ![ rechts ](/help/dsp/assets/downloads.png) der oberen Menüleiste auf „Vorgänge“.

Wenn eine Aktualisierung der Einstellungen fehlschlägt, können Sie eine Bulksheet-Fehlerdatei mit Farbcodierung herunterladen, um anzuzeigen, welche Einstellungen (Zeilen) gespeichert wurden und welche fehlgeschlagen sind, wobei für jeden Fehler ein Grund angegeben wird. Sie können dann die Probleme in derselben Datei beheben und sie erneut hochladen, um die korrigierten Informationen zu verarbeiten.


<!--
## Placement Setting Columns in Downloaded/Uploaded Spreadsheets{#qa-sheet-columns}

>[!TIP]
>
> In a downloaded spreadsheet, all editable columns are highlighted in blue.

### Campaign-level Spreadsheets

| Section | Column | Description | Editable? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | The numeric ID of the placement. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | The name of the placement. | Yes |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Any applied labels, for reporting. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | A link to open the placement in Edit mode. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Status] | The placement status: *[!UICONTROL active]* or *[!UICONTROL inactive]*. | Yes |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | The placement type. | &mdash; |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | The name of the parent package, when applicable. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | The start date of the placement. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL End Date] | The end date of the placement. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Whether dayparting is *[!UICONTROL ON]* or *[!UICONTROL OFF]*.<br><b>Note:</b> To check the actual dayparting schedule, open the placement settings in DSP. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Budget] | The placement budget, if there is one. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | The budget interval: <i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*, or *[!UICONTROL All Time]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | The objective of the package. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | The target value of the goal. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Whether the placement is pacing towards the *[!UICONTROL Budget]* or *[!UICONTROL Impressions]*. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | The maximum bid for the placement. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | The flight pacing strategy for the placement: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]*, or *[!UICONTROL aggressive frontload]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | The intraday pacing strategy for the placement: *[!UICONTROL Even]* or *[!UICONTROL ASAP]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Pre-Bid Filters] | Any pre-bid filter criteria to be applied. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Whether bidding rules (deprecated) are *[!UICONTROL ON]* or *[!UICONTROL OFF]*. | &mdash; |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | The primary frequency cap for the placement during the specified [!UICONTROL Frequency Cap Interval]. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | The interval for the primary frequency cap: *[!UICONTROL Day]*, *[!UICONTROL Week]*, or *[!UICONTROL Month]*. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | The secondary frequency cap for the placement during the specified [!UICONTROL Secondary Frequency Cap Interval] | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | The type of interval for the secondary frequency cap: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]*, or *[!UICONTROL Minute]*. The applicable number of weeks, days, hours, or minutes is indicated by the [!UICONTROL Secondary Frequency Cap Interval Value]. | Yes |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | The number of weeks, days, hours, or minutes for which the [!UICONTROL Secondary Frequency Cap] applies. For example, if the secondary cap is three impressions per six hours, then the value here would be `6`. | Yes |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | The number of targeted geographical locations, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | The targeted geographical locations, separated by semi-colons,or *[!UICONTROL All Locations]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | The number of excluded geographical locations or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | The excluded geographical locations, separated by semi-colons,  or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | The number of targeted public inventory deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | The number of excluded public inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | The number of targeted private inventory deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | The number of excluded private inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | The number of targeted [!UICONTROL On-Demand Inventory] deals, if any are specified, *[!UICONTROL All]*, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | The number of excluded On-Demand Inventory deals, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | The targeted type of traffic: *[!UICONTROL Website]* and/or *[!UICONTROL Apps]* | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Whether the Inventory Targeting option to exclude outstream traffic is <i[!UICONTROL >ON]* or *[!UICONTROL OFF]*.<br>Outstream ads usually appear over the content as a pop-up or stuffed into content (in the native experience), rather than as regular video ads in a video player. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | The quality of the sites to target: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]*, or *[!UICONTROL All Sites]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | The number of targeted site categories, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | The number of excluded site categories, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | The excluded sites, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Language] | The targeted site languages. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Standard display placements only) Whether or not to allow ad delivery on non-audited sites: *[!UICONTROL ON]* or *[!UICONTROL OFF]*. When the placement targets private inventory, this option may deliver ads on blocked sites. | &mdash; |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | The number of targeted sites, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | The targeted audiences, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | The excluded audiences, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Whether or not [!DNL Comscore] demographic segments are enabled for the placement (and other placements in the campaign): *[!UICONTROL ON]* or *[!UICONTROL OFF]*. This feature may be enabled only for campaigns for which the [!DNL Audience Verification] feature is enabled for [!DNL Nielsen] and/or [!DNL Comscore].  It incurs additional fees.  | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Whether or not to extend the ad targeting across devices: *[!UICONTROL ON]* or *[!UICONTROL OFF]*. Cross-device targeting extends your targeting across all of a person's known device, per the device graph specified in the campaign settings. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Included # | The number of targeted topic codes, if any are specified, or *[!UICONTROL All]*.   | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | The number of excluded topic codes, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | The number of targeted device targets, if any are specified, or *[!UICONTROL All]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | The number of excluded device targets, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | The number of targeted ISP providers, if any are specified, or *[!UICONTROL All]/i>. | &mdash; |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | The number of excluded ISP providers, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | The number of brand safety filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | The number of pre-bid fraud blocking filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | The number of pre-bid viewability filters applied, if any are specified, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Whether or not Site Safety Block is enabled: *[!UICONTROL ON]* or *[!UICONTROL OFF]*.[Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one?] | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | The number of third-party  event-tracking pixels attached to the placement, or *[!UICONTROL None]*.| &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | The number of conversion tracking pixels attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | A static, third-party fee rate to be tracked as a non-billable cost per 1000 impressions, if applicable. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | The number of ads attached to the placement, if any are attached, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | The names of any ads attached to the placement, or *[!UICONTROL None]*. | &mdash; |
| [!UICONTROL Ads] | [!UICONTROL Attached Ad ID] | The unique DSP-generated Ad IDs of any ads attached to the placement, separated by semi-colons. To download a list of ad names and associated Ad IDs from the [!UICONTROL Ads] view, create a custom view that includes the [!UICONTROL Ad ID] metric, and then [export the data](/help/dsp/campaign-management/reports/campaign-export-data.md). | Yes |
-->

>[!MORELIKETHIS]
>
>* [Überprüfen und Bearbeiten von Paketeinstellungen mithilfe von Bulksheets](/help/dsp/campaign-management/packages/package-qa.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Überprüfen und Bearbeiten von Platzierungseinstellungen mithilfe von Bulksheets](/help/dsp/campaign-management/placements/placement-qa.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Audio-Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Connected TV-Einstellungen](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Anzeigeneinstellungen anzeigen](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Mobile-Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Native Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Pre-roll-Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [Einstellungen für universelle Videoanzeigen](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
