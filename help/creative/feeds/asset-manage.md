---
title: Verwalten von Asset-Dateien
description: Erfahren Sie, wie Sie eine Asset-Datei für einen Advertiser hochladen und verwalten.
feature: Creative Dynamic Creatives
source-git-commit: 40f8fbde0879f2412816a2b08e6e99da67f16219
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# Verwalten von Asset-Dateien

Für dynamische HTML5-Anzeigen sind sowohl eine Feed-Datei im Microsoft Excel-Tabellenformat (XLSX) als auch die in der Tabelle referenzierten Bild-Assets erforderlich (mit Ausnahme von Adobe Experience Manager-Asset-Referenzen). Für statische HTML5-Anzeigen ist nur ein Bild-Asset pro Anzeige erforderlich.

>[!NOTE]
>
> Jede Feed-Datei kann nur für einen Katalog verwendet werden.

## Dateianforderungen

* Dynamic HTML5-Anzeigen:

   * Eine Feed-Datei im CSV-, TSV- oder Microsoft Excel-Tabellenformat (XLSX) mit einer Kopfzeile und einer Datenzeile für jede Anzeigenvariante. Fügen Sie in jeder Zeile einen Bildnamen oder einen Verweis auf eine Adobe Experience Manager ein.<!-- need spec of available column names that the user-created header names must map to; need to reference it in feed template topic too, so make it a separate file/appendix. -->

     Referenzieren Sie das Bild für Bilder, die Sie hochladen möchten, mit dem `images/image_name` Format (z. B. `images/300x250_acme_logo.png`)<!-- Verify.  Also need to include the spec for how to reference images in AEM -->

   * Die zugehörigen Bild-Assets im GIF-, JPEG-, JPG- oder PNG-Format.<!-- NOT GIF still? And is this true: The maximum file size is two (2) MB. --> Siehe die [Unterstützte Kreativgrößen](/help/creative/creative-libraries/creative-sizes.md).

   * (Optional) Video-Assets im MP4- oder WEBM-Format

  Sie können eine einzelne XLSX-Datei, eine einzelne Bild- oder Videodatei oder eine einzelne ZIP-Datei hochladen, die eine beliebige Kombination von XLSX-, Bild- und Videodateien enthält.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Statische HTML5-Anzeigen:

   * Ein Bild-Asset pro Anzeige im Format GIF, JPG, JPEG oder PNG.

     Sie können entweder ein einzelnes Bild oder mehrere Bilder in eine ZIP-Datei hochladen.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

## Hochladen einer Asset-Datei

>[!NOTE]
>
>Anstatt Asset-Dateien hochzuladen, können Sie auch einen Katalog direkt hochladen, wenn Sie [dynamische Kreative zu einer Kreativbibliothek hinzufügen](/help/creative/creative-libraries/creative-add-dynamic.md). Alle dort erstellten Kataloge werden in der [!UICONTROL Catalogs] für die zukünftige Verwendung verfügbar.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Assets]** .

1. Klicken Sie oben rechts auf **[!UICONTROL Create]** > **[!UICONTROL Asset]**.

1. Asset-Datei konfigurieren:

   1. Wählen Sie den Advertiser aus, der auf die Asset-Datei zugreifen kann.

   1. Geben Sie die Asset-Datei auf eine der folgenden Arten an:

      * Ziehen Sie eine Datei per Drag-and-Drop auf Ihr Gerät oder Netzwerk in das Feld.

      * Klicken Sie auf **[!UICONTROL Select a file]** , um die Datei auf Ihrem Gerät oder Netzwerk zu suchen.

   1. Klicken Sie auf **[!UICONTROL Upload]**.

Alle ZIP-Dateien werden automatisch dekomprimiert. Wenn Sie eine Tabellenkalkulationsdatei hochladen, wird die Datei auf der Unterregisterkarte [!UICONTROL Feeds] aufgeführt. Wenn Sie eine Bilddatei hochladen, wird die Bilddatei auf der Unterregisterkarte [!UICONTROL Images] aufgeführt.

## Asset-Datei herunterladen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Assets]** .

1. Halten Sie den Cursor über der Asset-Zeile und klicken Sie auf **[!UICONTROL Download]**.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

## Löschen einer Asset-Datei

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Feeds]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Assets]** .

1. Halten Sie den Cursor über der Asset-Zeile und klicken Sie auf **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Workflows für dynamische Anzeigen](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Verwalten von Feed-Vorlagen](/help/creative/feeds/feed-template-manage.md)
>* [Kataloge verwalten](/help/creative/feeds/catalog-manage.md)
>* [Verwalten dynamischer Anzeigenvorlagen](/help/creative/ad-templates/ad-template-manage.md)
>* [Hinzufügen dynamischer Kreativer zu einer Kreativbibliothek](/help/creative/creative-libraries/creative-add-dynamic.md)
