---
title: Hinzufügen von Standard-Kreativen zu einer Kreativbibliothek
description: Erfahren Sie, wie Sie einer Kreativbibliothek standardmäßige (nicht dynamische) Kreative hinzufügen.
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
source-git-commit: ecc0f6ac900292825b23b648be40dcc68ae15c64
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# Hinzufügen von Standard-Kreativen zu einer Kreativbibliothek

Fügen Sie Ihren [kreativen Bibliotheken“ Kreative hinzu](creative-library-manage.md) die mit standardmäßigen [Anzeigenerlebnissen“ verwendet ](/help/creative/experiences/experience-about.md).

>[!NOTE]
>
> Sie können einzelne Kreative direkt in Anzeigenerlebnisse einbeziehen, für die keine Benutzerziele definiert sind. Sie können Ihre Kreativen auch in [Bundles](bundle-manage.md) gruppieren, die Sie in zielgerichtete Anzeigenerlebnisse einschließen können.

## Hinzufügen flexibler HTML-Anzeigen zu einer Kreativbibliothek {#flexible-creative-add}

Sie können einen der folgenden Schritte ausführen:

* Laden Sie Ihre eigenen flexiblen Kreativen in ZIP-Dateien hoch.

* Verwenden Sie eine der vordefinierten flexiblen Kreativvorlagen, die auf Ihr Konto hochgeladen wurden, als Ausgangspunkt für Ihre eigenen flexiblen Kreativvorlagen.

### Hochladen Ihrer eigenen flexiblen Kreativen {#flexible-creative-upload}

Sie können mehrere flexible kreative Einheiten hochladen. Flexible Kreative müssen im ZIP-Format vorliegen und können bis zu 2 MB groß sein. Informationen zu Dateianforderungen finden Sie in der [Creative Specification für HTML5](html5-creative-specification.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Flexible]**.

1. Klicken Sie auf **[!UICONTROL Upload New]**.

1. Geben Sie ZIP-Dateien auf eine der folgenden Arten an:

   * Ziehen Sie Dateien per Drag-and-Drop auf Ihr Gerät oder Netzwerk in das Feld.

   * Klicken Sie auf **[!UICONTROL Select a file]** , um die Dateien auf Ihrem Gerät oder Netzwerk zu suchen.

   Siehe &quot;[ Anzeigenspezifikationen](#flexible-ad-spec).

1. Flexible kreative Dateien hinzufügen oder entfernen:

   * Um eine Datei hinzuzufügen, klicken Sie auf ![Hinzufügen](/help/creative/assets/create.png "Hinzufügen") oben links und suchen Sie die Datei auf Ihrem Gerät oder Netzwerk.

   * Um eine Datei zu entfernen, deaktivieren Sie das Kontrollkästchen daneben.

1. (Optional) Um ein Kreativ in der Vorschau anzuzeigen, klicken ![ über dem Bild ](/help/creative/assets/preview.png "Vorschau").

1. Geben Sie die [flexiblen HTML5-Anzeigeneinstellungen](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) an.

   Standardmäßig werden alle Kreativen ausgewählt, die Sie gerade hochgeladen haben. Alle Einstellungen mit nur einem Wert gelten für alle ausgewählten Kreativen. Für einige Einstellungen können Sie einzelne Werte angeben. Um Einstellungen für bestimmte Kreative einzugeben, deaktivieren Sie das Kontrollkästchen neben den einzelnen nicht anwendbaren Kreativen.

1. **[!UICONTROL Create]** klicken

### Hinzufügen flexibler Kreativer mithilfe einer Vorlage {#flexible-creative-use-template}

Sie können jede der flexiblen Kreativvorlagen verwenden, die in Ihr Konto hochgeladen wurden, um Anzeigen einer vordefinierten Größe zu erstellen. Nachdem Sie eine zu verwendende Vorlage ausgewählt haben, bearbeiten Sie die Click-Tags und -Attribute.&lt;!— Ersetzen Sie den letzten Satz durch diesen, wenn wir die Funktion zum Herunterladen von Vorlagen wieder hinzufügen: Sie können entweder a\) eine zu verwendende Vorlage auswählen und dann die Klicktags und -attribute bearbeiten; oder b\) [eine Vorlage als ZIP-Datei herunterladen](#download-flexible-creative-template) den Inhalt offline bearbeiten, um Ihr eigenes Kreativ zu erstellen, und dann [die bearbeitete Datei als neues Kreativ hochladen](flexible-creative-upload)>

<!-- Not currently an option:
You can use any of the [predefined flexible creative templates](flexible-html5-templates.md) included with [!DNL Creative] to build 160x600, 300x250, 300x600, or 728x90 ads.

For information about the attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."
-->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Flexible]**.

1. Klicken Sie auf **[!UICONTROL Browse System Flexible Templates]**.

1. (Optional) Um eine Vorschau der Vorlage anzuzeigen, klicken Sie auf **[!UICONTROL ...]** neben dem Vorlagennamen und dann auf **[!UICONTROL Preview]**.

   Sie können optional die Vorlage herunterladen: Klicken Sie **[!UICONTROL ...]** neben dem Vorlagennamen und dann auf **[!UICONTROL Download]**.

1. Klicken Sie neben dem Vorlagennamen auf **[!UICONTROL ...]** und dann auf **[!UICONTROL Use Selected]**.

1. Bearbeiten Sie die [flexiblen Kreativeinstellungen von HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5), um die Sprache anzugeben und Ihre eigenen Klick-Tags, Bilder und andere Attribute einzuschließen.

   Die maximale Dateigröße des Kreativen beträgt nach dem Komprimieren 2 MB.<!-- Still true? -->

1. Fügen Sie Ihre eigenen flexiblen kreativen Dateien hinzu oder entfernen Sie sie:

   * Um eine Datei von Ihrem Gerät oder Netzwerk hinzuzufügen, klicken Sie auf ![Hinzufügen](/help/creative/assets/create.png "Hinzufügen") oben links und suchen Sie die Datei. Aktivieren Sie das Kontrollkästchen neben dem Kreativen, deaktivieren Sie das Kontrollkästchen neben den anderen Kreativen und bearbeiten Sie die [flexiblen HTML5-Kreativeinstellungen](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5), um die Sprache anzugeben und Ihre eigenen Click-Tags, Bilder und andere Attribute einzuschließen.

   * Um eine Datei zu entfernen, deaktivieren Sie das Kontrollkästchen daneben.

1. (Optional) Um ein Kreativ in der Vorschau anzuzeigen, klicken ![ über dem Bild ](/help/creative/assets/preview.png "Vorschau").

1. Klicken Sie auf **[!UICONTROL Create]**.

## Hinzufügen eines HTML5-Creative zu einer Kreativbibliothek

Sie können mehrere HTML5-Kreative eines einzelnen Typs (einfach oder statisch) gleichzeitig hinzufügen.

<!-- Add in when we add this feature back:
You can optionally download a sample HTML5 creative as a ZIP file, edit the contents to build your own creative, and then add the edited file as a new creative.
-->

>[!NOTE]
>
>Sie können auch [flexible HTML5-Kreative hinzufügen](#flexible-creative-add) wobei es sich um HTML5-Kreative mit allen Attributen als standardmäßige HTML-Tags handelt, die Sie direkt in [!DNL Creative] bearbeiten können.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL HTML5]**.

<!-- Not an option as of 3/4:

1. (Optional) To download a sample HTML5 creative as a ZIP file, click **Sample HTML5 Creatives**.

   The ZIP file is downloaded according to your browser's normal procedure, usually to the folder that is specified for downloads. 
   
   To create your own HTML5 creative using the sample, unzip the file and edit the contents to include your own ad images and attributes. Then, rename the folder and zip it, and continue below.

-->

1. Geben Sie die Dateien auf eine der folgenden Arten an:

   * Ziehen Sie Dateien per Drag-and-Drop auf Ihr Gerät oder Netzwerk in das Feld.

   * Klicken Sie auf **[!UICONTROL Select a file]** , um die Datei auf Ihrem Gerät oder Netzwerk zu suchen.

   Siehe die [HTML5-Anzeigenspezifikation](/help/creative/creative-libraries/html5-creative-specification.md).

1. Geben Sie die Einstellungen für die [HTML5-Anzeige an](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5).

Standardmäßig werden alle Kreativen ausgewählt, die Sie gerade hochgeladen haben. Alle Einstellungen mit nur einem Wert gelten für alle ausgewählten Kreativen. Für einige Einstellungen können Sie einzelne Werte angeben. Um Einstellungen für bestimmte Kreative einzugeben, deaktivieren Sie das Kontrollkästchen neben den einzelnen nicht anwendbaren Kreativen.

1. **[!UICONTROL Create]** klicken

## Hinzufügen eines Kreativbilds zu einer Kreativbibliothek

Bildkreative können im GIF-, JPEG-, JPG- oder PNG-Format vorliegen. Die maximale Dateigröße beträgt zwei (2) MB. Siehe [Unterstützte Kreativgrößen](/help/creative/creative-libraries/creative-sizes.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Image]**.

1. Legen Sie die Bilder fest:

   * Führen Sie für lokale Bild-Assets einen der folgenden Schritte aus:

      * Ziehen Sie Dateien per Drag-and-Drop auf Ihr Gerät oder Netzwerk in das Feld.

      * Klicken Sie auf **[!UICONTROL Select a file]** , um Dateien auf Ihrem Gerät oder Netzwerk zu suchen.

   * Gehen Sie für genehmigte Bilder in einer [Adobe Experience Manager-Bibliothek, die mit Ihrem DSP](/help/creative/creative-libraries/aem-assets-configure.md)Konto verbunden ist, wie folgt vor:

      1. Klicken Sie auf **[!UICONTROL AEM Asset Library]**.

      1. Melden Sie sich bei Ihrem Experience Manager-Konto an.

      1. Suchen Sie die Dateien in Ihrer [!UICONTROL Assets]- oder [!UICONTROL Collections]-Ansicht, wählen Sie sie aus und klicken Sie dann oben rechts auf **[!UICONTROL Select]** .

         <!-- If the existing asset has multiple quality options, [!DNL Creative] downloads the primary asset, or the asset with the highest resolution within some upper limit [verify what it is and how this works]. [If an asset is part of an image set, ... primary asset in the image set. -->

1. Bilder hinzufügen oder entfernen:

   * Um ein Bild hinzuzufügen, klicken Sie ![Hinzufügen](/help/creative/assets/create.png "Hinzufügen") oben links und suchen Sie die Datei auf Ihrem Gerät oder Netzwerk.

   * Um ein Bild zu entfernen, deaktivieren Sie das Kontrollkästchen daneben.

1. Geben Sie die [Image Creative Settings](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image) an.

   Standardmäßig werden alle Kreativen, die Sie gerade hochgeladen haben, ausgewählt. Alle von Ihnen angegebenen Einstellungen gelten für alle ausgewählten Kreativen. Alle Einstellungen mit nur einem Wert gelten für alle ausgewählten Kreativen. Um Einstellungen für bestimmte Kreative einzugeben, heben Sie die Auswahl der nicht zutreffenden Kreativen auf.

1. **[!UICONTROL Create]** klicken

## Hinzufügen von Kreativen von Drittanbietern zu einer Kreativbibliothek {#creative-add-third-party}

[!DNL Creative] unterstützt Tracking-Tags von JavaScript für Kreative, die auf den meisten Werbeservern von Drittanbietern gehostet werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL 3rd Party]**.

1. Geben Sie das JavaScript-Tag und andere Einstellungen für das Kreativ-Tool in [Kreative Einstellungen von Drittanbietern“ ](#creative-settings-third-party).

   Sie können jedes der [verfügbaren Makros) kopieren ](/help/creative/creative-macros.md) in das JavaScript-Tag einfügen.

1. **[!UICONTROL Create]** klicken

## Hinzufügen eines Kreativvideos zu einer Kreativbibliothek

Siehe [Video Creative Specifications](/help/creative/creative-libraries/creative-libraries-about.md#creative-video-specs) und die [unterstützten Kreativgrößen](/help/creative/creative-libraries/creative-sizes.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Video]**.

1. Geben Sie die Videodateien auf eine der folgenden Arten an:

   * Ziehen Sie Dateien per Drag-and-Drop auf Ihr Gerät oder Netzwerk in das Feld.

   * Klicken Sie auf **[!UICONTROL Select a file]** , um Dateien auf Ihrem Gerät oder Netzwerk zu suchen.

1. Legen Sie die [kreativen Videoeinstellungen](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-video) fest.

   Standardmäßig wird das gerade hochgeladene Kreativ-Asset ausgewählt und alle angegebenen Einstellungen gelten für das ausgewählte Kreativ-Asset.<!-- By default, all creatives you just uploaded are selected, and any settings you specify apply to all selected creatives. Any settings with only one value apply to all selected creatives. To enter settings for specific creatives, deselect each inapplicable creative. -->

1. **[!UICONTROL Create]** klicken

>[!MORELIKETHIS]
>
>* [Standard-Kreative bearbeiten](/help/creative/creative-libraries/creative-edit-standard.md)
>* [Kreative Standardeinstellungen](/help/creative/creative-libraries/creative-settings-standard.md)
>* [Verfügbare Makros zum Tracking von URLs](/help/creative/creative-macros.md)
>* [Unterstützte Kreativgrößen](/help/creative/creative-libraries/creative-sizes.md)
>* [Vorschau eines Kreativen anzeigen](/help/creative/creative-libraries/creative-preview.md)
>* [Kreative an Bundles anhängen und von ihnen trennen](/help/creative/creative-libraries/creative-attach-detach-bundles.md)
>* [Über Ihre Kreativbibliotheken](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Verwalten von Kreativbibliotheken](/help/creative/creative-libraries/creative-library-manage.md)
