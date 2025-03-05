---
title: Hinzufügen von Standard-Kreativen zu einer Kreativbibliothek
description: Erfahren Sie, wie Sie einer Kreativbibliothek standardmäßige (nicht dynamische) Kreative hinzufügen.
feature: Creative Standard Creatives
exl-id: e6f1265b-9d05-4b3d-9dc6-300dbd9eb52d
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# Hinzufügen von Standard-Kreativen zu einer Kreativbibliothek

*Geschlossene Beta-Version*

Fügen Sie Ihren [kreativen Bibliotheken](creative-library-manage.md) Kreative hinzu, um sie für [Anzeigenerlebnisse](/help/creative/experiences/experience-about.md) zu verwenden.

>[!NOTE]
>
> Sie können einzelne Kreative direkt in Anzeigenerlebnisse einbeziehen, für die keine Benutzerziele definiert sind. Sie können Ihre Kreativen auch in [Bundles](bundle-manage.md) gruppieren, die Sie in zielgerichtete Anzeigenerlebnisse einschließen können.

## Hinzufügen flexibler HTML-Anzeigen zu einer Kreativbibliothek {#flexible-creative-add}

<!-- Later:
You can do either of the following: 

* Upload your own flexible creatives in ZIP files.

* Use any of the predefined flexible creative templates as a starting point for your own flexible creative.

### Upload your own flexible creatives {#flexible-creative-upload}

-->

Sie können mehrere flexible kreative Einheiten hochladen. Flexible Kreative müssen im ZIP-Format vorliegen und können bis zu 2 MB groß sein. Informationen zu Dateianforderungen finden Sie in der [Creative Specification für HTML5](html5-creative-specification.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf die Unterregisterkarte **[!UICONTROL Standard Ads]** .

1. Klicken Sie auf **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Flexible]**.

1. Klicken Sie auf **[!UICONTROL Upload New]**.

1. Geben Sie ZIP-Dateien auf eine der folgenden Arten an:

   * Ziehen Sie Dateien per Drag-and-Drop auf Ihr Gerät oder Netzwerk in das Feld.

   * Klicken Sie auf **[!UICONTROL select a file]** , um die Dateien auf Ihrem Gerät oder Netzwerk zu suchen.

   Siehe &quot;[ Anzeigenspezifikationen](#flexible-ad-spec).

1. Flexible kreative Dateien hinzufügen oder entfernen:

   * Um eine Datei hinzuzufügen, klicken Sie auf ![Hinzufügen](/help/creative/assets/create.png "Hinzufügen") oben links und suchen Sie die Datei auf Ihrem Gerät oder Netzwerk.

   * Um eine Datei zu entfernen, deaktivieren Sie das Kontrollkästchen daneben.

1. Geben Sie die [flexiblen HTML5-Anzeigeneinstellungen](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) an.

   Standardmäßig werden alle Kreativen ausgewählt, die Sie gerade hochgeladen haben. Alle Einstellungen mit nur einem Wert gelten für alle ausgewählten Kreativen. Für einige Einstellungen können Sie einzelne Werte angeben. Um Einstellungen für bestimmte Kreative einzugeben, deaktivieren Sie das Kontrollkästchen neben den einzelnen nicht anwendbaren Kreativen.

1. **[!UICONTROL Create]** klicken

<!-- In a later phase:

### Add flexible creatives using a template {#flexible-creative-use-template}

You can use any of the [predefined flexible creative templates](flexible-html5-templates.md) included with [!DNL Creative] to build 160x600, 300x250, 300x600, or 728x90 ads. Once you select a template to use, you'll edit the click tags and attributes.<!-- Replace last sentence with this if we add the template download feature back:  You can either a\) select a template to use, and then edit the click tags and attributes; or b\) [download a template as a ZIP file](#download-flexible-creative-template), edit the contents offline to build your own creative, and then [upload the edited file as a new creative](flexible-creative-upload).>

For information about the attributes available in predefined templates, see "[Available flexible creative templates](#flexible-creative-templates-available)."

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click the **[!UICONTROL Standard Ads]** subtab.

1. Click **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Flexible]**.

1. Click **[!UICONTROL Browse System Flexible Templates]**.



[The following are old instructions; see how this works in the new UI]


1. In the left panel, select the creative size to see all available templates for that size.

1. Under the template name, click **[!UICONTROL Use This Creative]**.

1. Edit the [flexible HTML5 creative settings](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) to include your own click tags, images, and other attributes.

   The maximum file size of the creative, once it's zipped, is 2 MB.[Will saving the creative zip it??]

1. (Optional) Once you've made your changes, click []()[add image] to preview the new creative. 

1. Click **[!UICONTROL Save]**.

-->

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

1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf die Unterregisterkarte **[!UICONTROL Standard Ads]** .

1. Klicken Sie auf **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL HTML5]**.

<!-- Not an option as of 3/4:

1. (Optional) To download a sample HTML5 creative as a ZIP file, click **Sample HTML5 Creatives**.

   The ZIP file is downloaded according to your browser's normal procedure, usually to the folder that is specified for downloads. 
   
   To create your own HTML5 creative using the sample, unzip the file and edit the contents to include your own ad images and attributes. Then, rename the folder and zip it, and continue below.

-->

1. Geben Sie die Dateien auf eine der folgenden Arten an:

   * Ziehen Sie Dateien per Drag-and-Drop auf Ihr Gerät oder Netzwerk in das Feld.

   * Klicken Sie auf **[!UICONTROL select a file]** , um die Datei auf Ihrem Gerät oder Netzwerk zu suchen.

   Siehe die [HTML5-Anzeigenspezifikation](/help/creative/creative-libraries/html5-creative-specification.md).

1. Geben Sie die Einstellungen für die [HTML5-Anzeige an](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5).

Standardmäßig werden alle Kreativen ausgewählt, die Sie gerade hochgeladen haben. Alle Einstellungen mit nur einem Wert gelten für alle ausgewählten Kreativen. Für einige Einstellungen können Sie einzelne Werte angeben. Um Einstellungen für bestimmte Kreative einzugeben, deaktivieren Sie das Kontrollkästchen neben den einzelnen nicht anwendbaren Kreativen.

1. **[!UICONTROL Create]** klicken

## Hinzufügen eines Kreativbilds zu einer Kreativbibliothek

Bildkreative können im GIF-, JPEG-, JPG- oder PNG-Format vorliegen. Die maximale Dateigröße beträgt zwei (2) MB. Siehe [Unterstützte Kreativgrößen](/help/creative/creative-libraries/creative-sizes.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf die Unterregisterkarte **[!UICONTROL Standard Ads]** .

1. Klicken Sie auf **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL Image]**.

1. Geben Sie die Dateien auf eine der folgenden Arten an:

   * Ziehen Sie Dateien per Drag-and-Drop auf Ihr Gerät oder Netzwerk in das Feld.

   * Klicken Sie auf **[!UICONTROL select a file]** , um die Datei auf Ihrem Gerät oder Netzwerk zu suchen.

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

1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf die Unterregisterkarte **[!UICONTROL Standard Ads]** .

1. Klicken Sie auf **[!UICONTROL Create]** > **[!UICONTROL Creative]** > **[!UICONTROL 3rd Party]**.

1. Geben Sie das JavaScript-Tag und andere Einstellungen für das Kreativ-Tool in [Kreative Einstellungen von Drittanbietern“ ](#creative-settings-third-party).

   Sie können jedes der [verfügbaren Makros) kopieren ](/help/creative/creative-macros.md) in das JavaScript-Tag einfügen.

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
