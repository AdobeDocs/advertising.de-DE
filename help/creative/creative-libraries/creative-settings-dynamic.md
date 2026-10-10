---
title: Dynamische kreative Einstellungen
description: Verweisen Sie auf die Einstellungen für dynamische Kreative.
feature: Creative Dynamic Creatives
exl-id: 9dcd7245-fa02-4082-9abb-8c0792322a68
TQID: 'https://experienceleague.adobe.com/b7R-MWHypydFbqdZY2sVwvoaq4sxwK5Wcf-OJc5x0LM'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d70c54b0-f069-4a3c-8056-7069a25e110c
    internal-label: Creative Dynamic Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: b7bf89dafd678490acc0749e2755ea7f0fec67f4
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 2%
---
# Dynamische kreative Einstellungen

<!-- add a description -->

Die folgenden Einstellungen gelten für dynamische Anzeigen, die mit der veralteten Benutzeroberfläche erstellt wurden. Wenn Sie dynamische Anzeigen über die neue Benutzeroberfläche oder [!DNL Creative Studio] erstellen, lesen Sie die Einstellungen unter &quot;[ dynamischer Kreativer in [!UICONTROL Creative Studio]](/help/creative/creative-studio/creative-studio-manage-dynamic-ads.md#select-template) verwalten“.

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

**[!UICONTROL Enable targeting]**: Die Spaltentypen in der Feed-Datei, für die Werte vorhanden sein müssen, um Anzeigen zu erstellen: *[!UICONTROL Profile data]*, *[!UICONTROL Geographic data], *[!UICONTROL Data pass], *[!UICONTROL Audience Segment]*.  **Hinweis:** Diese Einstellungen funktionieren unabhängig von den erweiterten Einstellungen in den Einstellungen für das Anzeigen-Erlebnis.<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

Ordnen Sie jedes Attribut (dynamisches Anzeigenfeld) in der angegebenen Anzeigenvorlage einer Spalte im angegebenen Katalog zu (Katalogbeschriftung) oder geben Sie einen statischen Wert ein.

>[!MORELIKETHIS]
>
>* [Hinzufügen dynamischer Kreativer zu einer Kreativbibliothek](creative-add-dynamic.md)
>* [Dynamische Kreative in einer Kreativbibliothek bearbeiten](creative-edit-dynamic.md)
>* [Workflows für dynamische Anzeigen](/help/creative/introduction/workflow-dynamic-ads.md)
