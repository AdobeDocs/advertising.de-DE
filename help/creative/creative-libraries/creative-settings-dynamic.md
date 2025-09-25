---
title: Dynamische kreative Einstellungen
description: Verweisen Sie auf die Einstellungen für dynamische Kreative.
feature: Creative Dynamic Creatives
source-git-commit: 6f2f6580e8d4fc11f52a97b086ce453e423ab4e6
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Dynamische kreative Einstellungen

<!-- add a description -->

<!-- This looks the same for me for either HTML5 type as of 9/24:

## Dynamic ad settings for static HTML5 ads {#dynamic-ad-settings-static-html5}

### Basic Details

**[!UICONTROL Advertiser]:** The advertiser for which to create the ads.

**[!UICONTROL Library]:** The creative library in which to create the ads.

**[!UICONTROL Dynamic Ad Name]:** A unique name for the creative.

**[!UICONTROL Ad Template Size]:** The ad dimensions for the ad template from which to create the ad. If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template Type]:** The type of ad template from which to create the ad: *[!UICONTROL Static HTML5]* or *[!UICONTROL Dynamic HTML5]*.  If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template]:** The ad template from which to create the ad.

**[!UICONTROL clickURL]:** A valid landing page URL to which users are redirected when they click the ad.

### [!UICONTROL Attributes Details]

-->

## Dynamische Anzeigeneinstellungen<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### Grundlegende Details

**[!UICONTROL Dynamic Ad Name]:** Ein eindeutiger Name für den Kreativen.

**[!UICONTROL Advertiser]:** Der Werbetreibende, für den die Anzeigen erstellt werden sollen.

**[!UICONTROL Library]:** Die Kreativbibliothek, in der die Anzeigen erstellt werden sollen. Wenn Sie die Anzeigen in [!UICONTROL Creatives] > [!UICONTROL Creative Libraries] erstellen, ist der Bibliotheksname bereits ausgewählt und schreibgeschützt.

**[!UICONTROL Ad Template Size]:** Die [Anzeigendimensionen](/help/creative/creative-libraries/creative-sizes.md) für die Anzeigenvorlage, aus der die Anzeige erstellt werden soll. Wenn Sie zuerst eine bestimmte [!UICONTROL Ad Template] auswählen, wird dieser Wert automatisch ausgewählt.

## Anzeigenvorlage

**[!UICONTROL Ad Template]:** Die Anzeigenvorlage, aus der die Anzeigen erstellt werden sollen. Wählen Sie eine vorhandene Anzeigenvorlage aus oder laden Sie eine neue Anzeigenvorlage hoch und wählen Sie den Vorlagentyp aus *statisch* oder *dynamisch*. Eine hochgeladene Vorlage muss im ZIP-Format vorliegen und HTML5-Dateien sowie eine Vorlagendefinitionsdatei (template.tDF) enthalten. <!-- Need to add more specs for that -->

**[!UICONTROL Number of offers (Max 50)]:** Die Anzahl der in einem Karussell anzuzeigenden Produkte.

## Kataloge

**[!UICONTROL Template]:** Die Feed-Vorlage, die zum Erstellen der Anzeigen verwendet werden soll.

**\[Catalogs\]**: Ein oder mehrere Kataloge, aus denen Anzeigen generiert werden sollen. Wählen Sie einen vorhandenen Katalog aus oder erstellen Sie einen neuen Katalog, indem Sie eine vorhandene Feed-Vorlage herunterladen und den neuen Katalog erstellen und hochladen.

Hochgeladene Kataloge müssen im ZIP-Format vorliegen und Folgendes enthalten:

* Eine oder mehrere Feed-Dateien im CSV-, TSV- oder Microsoft Excel-Tabellenformat (XLSX).<!-- Need to add more specs for that -->

* Bild-Assets im GIF-, JPEG-, JPG- oder PNG-Format

* (Optional) Video-Assets im MP4- oder WEBM-Format

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**: <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->Die Typen von Spalten in der Feed-Datei, für die Werte vorhanden sein müssen, um Anzeigen zu erstellen: *[!UICONTROL Profile data]*, *[!UICONTROL Geographic data], *[!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Hinweis:** Diese Einstellungen funktionieren unabhängig von den erweiterten Einstellungen in den Einstellungen für das Anzeigen-Erlebnis.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]**/**[!UICONTROL Maps to Catalog Labels]:**

Ordnen Sie jedes Attribut (dynamisches Anzeigenfeld) in der angegebenen Anzeigenvorlage einer Spalte im angegebenen Katalog (Katalogbeschriftung) zu.

>[!MORELIKETHIS]
>
>* [Hinzufügen dynamischer Kreativer zu einer Kreativbibliothek](creative-add-dynamic.md)
>* [Dynamische Kreative in einer Kreativbibliothek bearbeiten](creative-edit-dynamic.md)
>* [Workflows für dynamische Anzeigen](/help/creative/introduction/workflow-dynamic-ads.md)
