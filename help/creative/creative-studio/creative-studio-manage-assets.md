---
title: Verwalten von Assets in Creative Studio
description: Erfahren Sie, wie Sie Assets hochladen, durchsuchen und verwalten können, indem Sie in Adobe Advertising Creative die Registerkarte Creative Studio Assets verwenden.
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a6ab21a588f5b069ea0783dee711f52d906a46f9
workflow-type: tm+mt
source-wordcount: 292
ht-degree: 0%

---

# Verwalten von Assets in [!UICONTROL Creative Studio]

*Beta-Funktion*

Laden Sie Bild-, Video-, Audio- und Schriftarten-Assets hoch, um sie in Anzeigenvorlagen zu referenzieren und während der Sitzungen zur Anzeigengenerierung an Chat-Nachrichten des KI-Agenten anzuhängen.

## Die Ansicht [!UICONTROL Creative Studio] > [!UICONTROL Assets]

Auf der Registerkarte **[!UICONTROL Assets]** werden Ihre vorhandenen Assets in einer Kartenansicht aufgelistet.

### Verfügbare Aktionen

<!--  * [Browse and search assets](#assets-search) -->

* [Hochladen von Assets](#assets-upload)

* [Umbenennen eines Assets](#assets-rename)

* [Herunterladen von Assets](#assets-download)

* [Löschen eines Assets](#assets-delete)

<!--
Should be in "Common Tasks" chapter

## Browse and search assets {#assets-search}

* Use the **[!UICONTROL Search assets]** field to find assets by name. Enter at least three characters to trigger a search; shorter queries don't filter results.
* Click **[!UICONTROL Filter]** to filter the asset library by type or other attributes.
-->

## Hochladen von Assets {#assets-upload}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio].**

1. Klicken Sie auf die Registerkarte **[!UICONTROL Assets]** .

1. Klicken Sie auf **[!UICONTROL Upload Assets]**.

1. Wählen Sie eine oder mehrere Dateien von Ihrem Computer oder Netzwerk aus.

   Die folgenden Dateitypen werden unterstützt:

   | Typ | Unterstützte Formate | Maximale Dateigröße |
   | --- | --- | --- |
   | Bilder | JPG/JPEG, PNG, GIF, WebP, SVG | 10 MB |
   | Video | MP4, MOV, AVI, WebM | 512 MB |
   | Audio | MP3, WAV, AAC, OGG | 50 MB |

   Leere Dateien und nicht unterstützte Dateitypen werden mit einer Fehlerbenachrichtigung zurückgewiesen.

   Der Asset-Name wird als hochgeladener Dateiname ohne Erweiterung gespeichert. Leerzeichen und Nicht-ASCII-Zeichen im Dateinamen werden durch Unterstriche ersetzt (beim Hochladen `My Logo.png` Erstellen eines Assets mit dem Namen `My_Logo`). Sie können das Asset anschließend umbenennen.

<!--
(from Bob) Moved from above step. Content in your repo failed to publish, and I'm testing several possible issues. Comment syntax between steps is sometimes problematic.

Verified 2026-07-09 against creative-api TemplateMediaValidator.java (IMAGE_EXTENSIONS, VIDEO_EXTENSIONS, AUDIO_EXTENSIONS), which backs the /v1/creative/template-medias upload/initiate endpoint used by this tab. The Assets tab file input has no client-side accept restriction (TemplateBrowser.tsx) and relies entirely on this backend validator, so it is authoritative.


maybe later:

   | Fonts | TTF, OTF, WOFF, WOFF2 | 5 MB |
   
-->

## Asset-Namen bearbeiten {#asset-rename}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio].**

1. Klicken Sie auf die Registerkarte **[!UICONTROL Assets]** .

1. Halten Sie den Cursor über die Asset-Karte und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Edit name]**.

1. Aktualisieren Sie den Asset-Namen.

   Asset-Namen können bis zu 512 Zeichen lang sein.

1. Klicken Sie auf **[!UICONTROL Update]**.

## Herunterladen von Assets {#asset-download}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio].**

1. Klicken Sie auf die Registerkarte **[!UICONTROL Assets]** .

1. Halten Sie den Cursor über die Asset-Karte und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   Das Asset wird gemäß dem normalen Verfahren Ihres Browsers heruntergeladen.

## Löschen eines Assets {#asset-delete}

>[!NOTE]
>
>Ein gelöschtes Asset kann nicht reaktiviert werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio].**

1. Klicken Sie auf die Registerkarte **[!UICONTROL Assets]** .

1. Halten Sie den Cursor über die Asset-Karte und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Über Creative Studio in Advertising Creative](creative-studio-about.md)
>* [Verwalten von Vorlagen in Creative Studio](creative-studio-manage-templates.md)
>* [Generieren von Standardanzeigen in Creative Studio](creative-studio-manage-standard-ads.md)
