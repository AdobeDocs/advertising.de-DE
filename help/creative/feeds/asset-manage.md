---
title: Verwalten von Asset-Dateien
description: Erfahren Sie, wie Sie eine Asset-Datei für einen Advertiser hochladen und verwalten.
feature: Creative Dynamic Creatives
exl-id: 2fe2d778-8456-490a-bf44-234dbc08649f
source-git-commit: ad7d2b02103b5a45dadcd51b60621c31e9db0d29
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---

# Verwalten von Asset-Dateien

* Für dynamische HTML5-Anzeigen ist eine Feed-Datei im Microsoft Excel-Tabellenformat (XLSX) und die tatsächlichen Bild-Assets erforderlich, auf die in der Tabelle verwiesen wird.

* Für statische HTML5-Anzeigen ist nur ein Bild-Asset pro Anzeige erforderlich.

* Für Videoanzeigen ist eine Feed-Datei im XLSX-Format (Microsoft Excel Spreadsheet) und die in der Tabelle referenzierten Video-Assets erforderlich.

>[!NOTE]
>
> Jede Feed-Datei kann nur für einen Katalog verwendet werden.

## Dateianforderungen

* Dynamic HTML5-Anzeigen:

   * Eine Feed-Datei im CSV-, TSV- oder Microsoft Excel-Tabellenformat (XLSX) mit einer Kopfzeile und einer Datenzeile für jede Anzeigenvariante. Fügen Sie in jede Zeile einen Bildnamen ein, indem Sie das `images/image_name` Format verwenden (z. B. `images/300x250_acme_logo.png`).

     Die Advertiser-spezifischen Feldnamen müssen den (verfügbaren [ für dynamische Anzeigenfeed-Dateien) ](/help/creative/appendix-available-feed-fields.md).

   * Die zugehörigen Bild-Assets im GIF-, JPEG-, JPG- oder PNG-Format.<!-- Is this true: The maximum file size is two (2) MB. --> Siehe die [Unterstützte Kreativgrößen](/help/creative/creative-libraries/creative-sizes.md).

  Sie können eine einzelne XLSX-Datei, eine einzelne Bilddatei oder eine einzelne ZIP-Datei hochladen, die eine beliebige Kombination aus XLSX- und Bilddateien enthält.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Statische HTML5-Anzeigen:

   * Ein Bild-Asset pro Anzeige im Format GIF, JPG, JPEG oder PNG.

     Sie können entweder ein einzelnes Bild oder mehrere Bilder in eine ZIP-Datei hochladen.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Dynamische Videoanzeigen:

   * Eine Feed-Datei im CSV-, TSV- oder Microsoft Excel-Tabellenformat (XLSX) mit einer Kopfzeile und einer Datenzeile für jede Anzeigenvariante. Fügen Sie in jeder Zeile einen Videonamen mit dem `videos/image_name` Format ein (z. B. `videos/300x250_acme_logo.png`). Die ZIP-Datei darf maximal 512 MB mit maximal 500 Zeilen umfassen.

     Die Advertiser-spezifischen Feldnamen müssen den (verfügbaren [ für dynamische Anzeigenfeed-Dateien) ](/help/creative/appendix-available-feed-fields.md).

     Für alle Konten mit dynamischen Videos empfiehlt es sich, [Katalog zu erstellen](catalog-manage.md) indem Sie die Asset-Datei zusammen mit einer Kopie der [ &quot;[!UICONTROL Adobe Creative Template]](feed-template-manage.md)Universal Feed Template“ verwenden, in der Sie jedes Feld in der Asset-Datei einem Feld im Advertising Creative-Backend zuordnen.

   * Die zugehörigen Video-Assets im MP4-, MOV- oder WEBM-Format. Unterstützte Anzeigenvorlagen umfassen Startkarte, Endkarte, obere Überlagerung, untere Überlagerung oder L-förmig. Die Dauer jedes Videos muss zwischen 1 und 90 Sekunden liegen. Siehe [Unterstützte Kreativgrößen](/help/creative/creative-libraries/creative-sizes.md).

  Sie können eine einzelne XLSX-Datei, eine einzelne Bilddatei oder eine einzelne ZIP-Datei hochladen, die eine beliebige Kombination aus XLSX- und Videodateien enthält.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

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
>* [Verfügbare Felder für dynamische Anzeigen-Feed-Dateien](/help/creative/appendix-available-feed-fields.md)
>* [Workflows für dynamische Anzeigen](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Verwalten von Feed-Vorlagen](/help/creative/feeds/feed-template-manage.md)
>* [Kataloge verwalten](/help/creative/feeds/catalog-manage.md)
>* [Verwalten dynamischer Anzeigenvorlagen](/help/creative/ad-templates/ad-template-manage.md)
>* [Hinzufügen dynamischer Kreativer zu einer Kreativbibliothek](/help/creative/creative-libraries/creative-add-dynamic.md)
