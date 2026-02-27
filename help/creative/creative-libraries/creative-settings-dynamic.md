---
title: Dynamische kreative Einstellungen
description: Verweisen Sie auf die Einstellungen für dynamische Kreative.
feature: Creative Dynamic Creatives
exl-id: 9dcd7245-fa02-4082-9abb-8c0792322a68
source-git-commit: 164ee92f85c0e649dc2bd6c0224a531eb72d1962
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Dynamische kreative Einstellungen

<!-- add a description -->

## Dynamische Anzeigeneinstellungen<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### Grundlegende Details

**[!UICONTROL Creative Type]:** Ob es sich bei dem Kreativen um eine *[!UICONTROL Display]* Anzeige (HTML5) oder eine *[!UICONTROL Video]* Anzeige handelt.

**[!UICONTROL Dynamic Display Ad Name]** oder **[!UICONTROL Dynamic Video Ad Name]:** Eindeutiger Name für den Kreativen.

**[!UICONTROL Advertiser]:** Der Werbetreibende, für den die Anzeigen erstellt werden sollen. Wenn Sie die Anzeigen in [!UICONTROL Creatives] > [!UICONTROL Creative Libraries] erstellen, ist der Advertiser bereits ausgewählt und schreibgeschützt.

**[!UICONTROL Library]:** Die Kreativbibliothek, in der die Anzeigen erstellt werden sollen. Wenn Sie die Anzeigen in [!UICONTROL Creatives] > [!UICONTROL Creative Libraries] erstellen, ist der Bibliotheksname bereits ausgewählt und schreibgeschützt.

## Anzeigenvorlage

**[!UICONTROL Ad Template]:** Die Anzeigenvorlage, aus der die Anzeigen erstellt werden sollen. Wählen Sie eine vorhandene Anzeigenvorlage aus oder laden Sie eine neue Anzeigenvorlage hoch und wählen Sie den Vorlagentyp aus *statisch* oder *dynamisch*. Die Vorlage muss im ZIP-Format vorliegen und Folgendes enthalten:<!-- Need to add more specs for templates -->

* Kreative anzeigen: HTML5-Dateien mit dem gewünschten Anzeigenformat und (nur für dynamische HTML5-Anzeigen) eine -Datei mit den Anzeigenattributen (.tdf)

* Video-Kreative: Eine Scene-Datei mit dem gewünschten Anzeigenformat. Die ZIP-Datei darf maximal 512 MB groß sein.

Um fortzufahren, klicken Sie auf **[!UICONTROL Select Ad Template]**.

**[!UICONTROL Size]:** (Nur dynamische Anzeigen; schreibgeschützt) Die [Anzeigendimensionen](/help/creative/creative-libraries/creative-sizes.md) für die ausgewählte Anzeigenvorlage, die zum Erstellen der Anzeigen verwendet wird.

**[!UICONTROL Card Count (Max 50)]:** (Nur Anzeigen) Die Anzahl der Produkte, die in einem Karussell angezeigt werden sollen.

**[!UICONTROL Duration]:** (Nur Videoanzeigen; schreibgeschützt) Die Videodauer, die von der ausgewählten Anzeigenvorlage abgeleitet wird. Die Dauer jedes Videos muss zwischen 1 und 90 Sekunden liegen.

## Kataloge

**\[Catalogs\]**: Ein oder mehrere Kataloge, aus denen Anzeigen generiert werden sollen. Wählen Sie einen vorhandenen Katalog aus oder erstellen Sie einen neuen Katalog, indem Sie eine vorhandene Feed-Vorlage herunterladen und den neuen Katalog erstellen und hochladen. Klicken Sie auf **[!UICONTROL Select Catalog]**.

Hochgeladene Kataloge müssen im ZIP-Format vorliegen und Folgendes enthalten:

* (Dynamische Anzeige- und Videoanzeigen) Eine oder mehrere Feeddateien im CSV-, TSV- oder Microsoft Excel-Tabellenformat (XLSX). Die maximale Dateigröße beträgt 512 MB.<!-- Need to add more specs for the feed files -->

* (Anzeigen) Bild-Assets im GIF-, JPEG-, JPG- oder PNG-Format

* (Videoanzeigen) Video-Assets im MP4-, MOV- oder WEBM-Format. Unterstützte Anzeigenvorlagen umfassen Startkarte, Endkarte, obere Überlagerung, untere Überlagerung oder L-förmig. Die Dauer jedes Videos muss zwischen 1 und 90 Sekunden liegen.

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**: <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP -->Die Typen von Spalten in der Feed-Datei, für die Werte vorhanden sein müssen, um Anzeigen zu erstellen: *[!UICONTROL Profile data]*, *[!UICONTROL Geographic data], *[!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Hinweis:** Diese Einstellungen funktionieren unabhängig von den erweiterten Einstellungen in den Einstellungen für das Anzeigen-Erlebnis.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]**/**[!UICONTROL Maps to Catalog Labels]:**

Ordnen Sie jedes Attribut (dynamisches Anzeigenfeld) in der angegebenen Anzeigenvorlage einer Spalte im angegebenen Katalog zu (Katalogbeschriftung) oder geben Sie einen statischen Wert ein.

>[!MORELIKETHIS]
>
>* [Hinzufügen dynamischer Kreativer zu einer Kreativbibliothek](creative-add-dynamic.md)
>* [Dynamische Kreative in einer Kreativbibliothek bearbeiten](creative-edit-dynamic.md)
>* [Workflows für dynamische Anzeigen](/help/creative/introduction/workflow-dynamic-ads.md)
