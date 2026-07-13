---
title: Verwalten von Standardanzeigen in Creative Studio
description: Erfahren Sie, wie Sie Standard-Display-Anzeigen in der Creative Studio Creatives-Bibliothek erstellen, bearbeiten, duplizieren, herunterladen und löschen.
exl-id: 01d3cdec-80d0-494c-94dd-d9d0ae8ca53c
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a6ab21a588f5b069ea0783dee711f52d906a46f9
workflow-type: tm+mt
source-wordcount: 1181
ht-degree: 0%

---

# Verwalten von Standardanzeigen in [!UICONTROL Creative Studio]

*Beta-Funktion*

Die Registerkarte **[!UICONTROL Creatives]** in [!UICONTROL Creative Studio] ist Ihre Bibliothek mit standardmäßigen Display-Anzeigen, die aus Vorlagen generiert wurden. Von hier aus können Sie Anzeigen mit dem [!UICONTROL Ad Variations Generator] erstellen, gespeicherte Anzeigen bearbeiten, neue Varianten aus einer vorhandenen Anzeige generieren, das Änderungsprotokoll anzeigen, duplizieren, herunterladen und löschen.

## Standardanzeigen erstellen {#create-standard-ads}

Verwenden Sie die [!UICONTROL Ad Variations Generator], um Anzeigeninhalte aus einer Vorlage zu generieren. Der KI-Assistent generiert und verfeinert Überschriften, CTAs, Bilder, Farben und mehr und kann in einer einzigen Sitzung neue Größenvarianten erstellen.

>[!NOTE]
>
>Die standardmäßige Anzeigengenerierung unterstützt derzeit nur Anzeigenvorlagen. Vorlagen für Videoanzeigen sind weder auf der Registerkarte **[!UICONTROL Creatives]** noch auf der Registerkarte **[!UICONTROL Templates]** als Ausgangspunkt verfügbar.

### Voraussetzungen

In Ihrer Vorlagenbibliothek muss mindestens eine Anzeige und Vorlage vorhanden sein.

### Standardanzeigen generieren

1. Öffnen Sie die [!UICONTROL Ad Variations Generator] auf eine der folgenden Arten:

   * **Auf der Registerkarte [!UICONTROL Creatives]:**

      1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio]**.

      1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf **[!UICONTROL Generate]** auf der Karte Schnellaktion **[!UICONTROL Generate standard ads from templates]** .

      1. Klicken Sie im Dialogfeld zur Vorlagenauswahl auf eine Vorlage, um sie auszuwählen, und klicken Sie dann auf **[!UICONTROL Use this template]**.

   * (Nur Anzeigen anzeigen) **Auf der Registerkarte &quot;[!UICONTROL Templates]&quot;:**

      1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio]**.

      1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

      1. Halten Sie den Cursor über eine Vorlagenkarte und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Generate ad variations]**.

   Die [!UICONTROL Ad Variations Generator] wird geöffnet. Auf der Arbeitsfläche wird der Abschnitt **[!UICONTROL Template Sizes]** mit den verfügbaren Anzeigenformaten der Vorlage und ein **[!UICONTROL Ad Concepts]** Abschnitt mit den generierten Inhalten angezeigt.

1. (Optional) Um ein Markenprofil auf die Anzeigen anzuwenden, wählen Sie ein **[!UICONTROL Brand Profile]** in der Symbolleiste der Arbeitsfläche aus.

   Der KI-Assistent verwendet beim Generieren von Inhalten das Logo Ihrer Marke, die Farbpalette, die Sprachrichtlinien, Bildstandards und Kanalrichtlinien.

1. Erstellen Sie Anzeigenvarianten mit dem [!UICONTROL AI Assistant]:

   1. Geben Sie im Feld **[!UICONTROL Ask AI to generate ad variations…]** eine Anfrage ein und drücken Sie **[!UICONTROL Enter]**, oder klicken Sie auf eine der angezeigten Eingabeaufforderungen:

      * **[!UICONTROL Write 3 headline variations for this template]**
      * **[!UICONTROL Generate 3 versions of this ad that will help with performance]**
      * **[!UICONTROL Create a new size template]**

      Die KI generiert Ergebnisse auf der Arbeitsfläche und organisiert sie in *Konzepte* die jeweils eine eigene Inhaltsvariante darstellen. Der Konzeptzähler im **[!UICONTROL Ad Concepts]** Abschnitt verfolgt, wie viele Konzepte vorhanden sind (z. B. **(2/10)**. Pro Sitzung sind bis zu 10 Konzepte zulässig.

   1. Fahren Sie mit der Verfeinerung fort, indem Sie Folgenachrichten senden. Beispiele:

      * „Machen Sie alle Kopien spielerischer und weniger firmenintern.“
      * „Ändern Sie das Logo in die weiße Version.“
      * „Setzen Sie den CTA bei allen Konzepten auf „Jetzt kaufen“.“
      * „Ändern Sie die Größe dieser Anzeige auf alle 6 IAB-Standardanzeigengrößen.“
      * „Geben Sie mir 3 verschiedene Headline-Konzepte mit jeweils einem passenden Hintergrundbild.“

      >[!NOTE]
      >
      >Der KI-Assistent kann Text generieren und ändern (Überschriften, Unterüberschriften, CTAs, Textkörper), Hintergrundbilder austauschen, Markenfarben anwenden, Logo-Versionen wechseln und neue Größenvorlagen erstellen. Die Vorlagenstruktur kann nicht geändert werden: Elementpositionen, Layout, Abstand, Abstand, Schriftfamilie, Schriftgröße oder Rahmen. Nehmen Sie vor Beginn der Sitzung strukturelle Änderungen im Vorlageneditor vor. Siehe [Bearbeiten einer Vorlage](creative-studio-manage-templates.md#edit-template).

   1. (Optional) Um einen visuellen Verweis in eine Anfrage aufzunehmen, klicken Sie auf die Schaltfläche &quot;**[!UICONTROL +]**&quot; im Chat-Eingabebereich. Im Dialogfeld **[!UICONTROL Select from Asset Library]** :

      * Um ein Asset in Ihrer Asset-Bibliothek zu verwenden, klicken Sie auf das Asset und dann auf **[!UICONTROL Add to chat]**. Senden Sie die Nachricht, um das Asset als Kontext einzuschließen.

      * Um ein oder mehrere Assets hochzuladen, klicken Sie auf **[!UICONTROL Upload Assets]** und wählen Sie die Dateien auf Ihrem Gerät oder Netzwerk aus.

1. (Optional) Verwenden Sie die Symbolleiste der Arbeitsfläche, um die generierten Anzeigen zu überprüfen:

   * **[!UICONTROL Brand]:** Wählen Sie das auf die Sitzung angewendete Markenprofil aus oder ändern Sie es.
   * **[!UICONTROL Zoom in]**/**[!UICONTROL Zoom out]:** Passen Sie den Zoom-Faktor der Arbeitsfläche an.
   * **[!UICONTROL Fit to screen]:** Die Ansicht zurücksetzen, um alle Größen anzuzeigen.
   * **[!UICONTROL Replay animations]:** Animationen von Vorlagen wiedergeben.

   Wenn die KI eine neue Größe erstellt, werden auf der neuen Größenkarte die Steuerelemente **[!UICONTROL Adjust]**, **[!UICONTROL Keep]** und Löschen angezeigt. Klicken Sie auf **[!UICONTROL Keep]**, um die Größe unverändert zu übernehmen, klicken Sie auf **[!UICONTROL Adjust]**, um die Vorlage im Anzeigeeditor zu öffnen, wo Sie strukturelle Änderungen vornehmen können, und klicken Sie dann auf **[!UICONTROL Update Ad Format]**, um sie zu speichern, oder klicken Sie auf das Löschsymbol, um die neue Größe zu entfernen.

1. (Optional) Verwalten von Konzepten und Varianten:

   * Um ein Konzept zu verwalten, halten Sie den Cursor über die Konzeptbeschriftung (z. B. **[!UICONTROL Concept 3]**), klicken Sie auf **[!UICONTROL ...]** und wählen Sie dann eine Option aus:

      * **[!UICONTROL Add to chat]:** Verweist auf das Konzept in der nächsten Eingabeaufforderung.
      * **[!UICONTROL Delete]:** Entfernt das Konzept.

   * Um eine einzelne Variante zu verwalten, halten Sie den Cursor über die Variantenkarte und klicken Sie auf **[!UICONTROL ...]** und wählen Sie dann eine Option aus:

      * **[!UICONTROL Add to Chat]:** Verweist auf die Variante in Ihrer nächsten Eingabeaufforderung. Sie können auch direkt auf den Kartenhauptteil der Variante klicken, um die Erwähnung umzuschalten.
      * **[!UICONTROL Edit Data]:** Öffnet ein Dialogfeld, in dem Sie die **[!UICONTROL Name]** und die Clickthrough-URL für jedes in der Vorlage definierte Clicktag aktualisieren können. Zum Anwenden auf **[!UICONTROL Save]** klicken.
      * **[!UICONTROL Delete]:** Entfernt die Variante.

1. Wenn Sie mit den generierten Konzepten zufrieden sind, klicken Sie in der Kopfzeile auf **[!UICONTROL Save Standard Ads]** .

   Die Schaltfläche wird deaktiviert, bis mindestens ein Konzept vorhanden ist.

1. Geben Sie im Dialogfeld **[!UICONTROL Save Standard Ads]** die folgenden Einstellungen an und klicken Sie dann auf **[!UICONTROL Save Standard Ads]**.

   **[!UICONTROL Advertiser]:** (erforderlich) Der Werbetreibende, unter dem die Kreativen gespeichert werden sollen.

   **[!UICONTROL Creative Library]:** (Erforderlich) Die Kreativbibliothek zum Speichern der Kreativen. Die Bibliotheksauswahl wird aktiviert, nachdem Sie einen Advertiser ausgewählt haben.

   **[!UICONTROL Attach to Bundles]:** (Optional) Wenn diese Option aktiviert ist, werden die gespeicherten Kreativen an ein oder mehrere Bundles angehängt. Wählen Sie für jede Anzeigenvariante ein Bundle aus oder geben Sie einen neuen Bundle-Namen ein.

   **\[Einstellungen für jede Anzeige\]:** Für jede Anzeigenvariante können Sie die **[!UICONTROL Name],** **[!UICONTROL Language],** und **[!UICONTROL click URL]anzeigen und optional ändern.**

## Bearbeiten einer Standardanzeige {#edit-standard-ad}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio]**.

1. Halten Sie auf der Registerkarte **[!UICONTROL Creatives]** den Cursor über die Kreativkarte und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

   Ein Vollbild-Editor wird mit einer Live-Anzeigenvorschau auf der linken Seite und einem Einstellungsbedienfeld auf der rechten Seite geöffnet.

1. Bearbeiten Sie die Anzeigeneinstellungen über die Registerkarten **[!UICONTROL Details]** und **[!UICONTROL Attributes]** :

   Registerkarte **[!UICONTROL Details]**:

   * **[!UICONTROL Creative Name]:** (Erforderlich) Der Anzeigename für den Kreativen.
   * **[!UICONTROL Language]:** (Erforderlich) Die Sprache des Anzeigeninhalts.
   * **[!UICONTROL Creative Size]:** (Schreibgeschützt) Die Dimensionen der Anzeige.
   * **Auf Tags klicken** Wenn die Vorlage Klick-Tags definiert, wird jedes Klick-Tag als erforderliches Feld mit der Bezeichnung „Tag“ angezeigt. Geben Sie die Clickthrough-Ziel-URL für jedes Tag ein.
   * **[!UICONTROL Label]:** (Optional) Beschriftungen für die Organisation von Kreativen. Wählen Sie vorhandene Beschriftungen aus, oder geben Sie einen neuen Tag ein und klicken Sie auf **[!UICONTROL Add tag].**

   Registerkarte **[!UICONTROL Attributes]**:

   Die Live-Vorschau wird bei der Bearbeitung in Echtzeit aktualisiert. Die Registerkarte **[!UICONTROL Attributes]** ist nicht verfügbar, während die Vorschau geladen wird.

   * **Textattribute:** Geben Sie den Textwert für jede bearbeitbare Textebene ein, die in der Vorlage definiert ist.
   * **Bildattribute:** Zeigt eine Miniaturansicht des aktuellen Bildes an. Klicken Sie auf **[!UICONTROL Replace Image]** , um einen Ersatz (PNG, JPEG, GIF, WebP oder SVG) hochzuladen.

1. Klicken Sie auf **[!UICONTROL Update Creative]**.

## Erstellen von Anzeigenvarianten für eine Standardanzeige {#generate-ad-variations}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio]**.

1. Halten Sie auf der Registerkarte **[!UICONTROL Creatives]** den Cursor über die Kreativkarte und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**.

   Die [!UICONTROL Ad Variations Generator] wird geöffnet, wobei die ausgewählte Anzeige vorgeladen ist.

1. Verwenden Sie die KI-Chat-Oberfläche, um zusätzliche Varianten zu generieren und zu verfeinern. Siehe &quot;[&#x200B; von Standardanzeigen](#create-standard-ads) für den vollständigen Workflow.

## Duplizieren einer Standardanzeige {#duplicate-standard-ad}

Duplizieren Sie eine Standardanzeige, um eine neue Kreative mit denselben Einstellungen zur Bibliothek hinzuzufügen. Sie können die neue Kreative später umbenennen und die Einstellungen nach Bedarf bearbeiten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio]**.

1. Halten Sie auf der Registerkarte **[!UICONTROL Creatives]** den Cursor über die Kreativkarte und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

   Der neue Kreative heißt `<original name> (copy)`.

## Änderungsprotokoll für eine Standardanzeige anzeigen {#view-change-log}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio]**.

1. Halten Sie auf der Registerkarte **[!UICONTROL Creatives]** den Cursor über die Kreativkarte und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Change Log]**.

   Ein Dialogfeld mit einer Tabelle mit Änderungen an der Anzeige wird geöffnet.

## Herunterladen einer Standardanzeige {#download-standard-ad}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio]**.

1. Halten Sie auf der Registerkarte **[!UICONTROL Creatives]** den Cursor über die Kreativkarte und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   Die kreativen Downloads erfolgen nach dem üblichen Verfahren Ihres Browsers.

## Löschen einer Standardanzeige {#delete-standard-ad}

>[!NOTE]
>
>Diese Aktion kann nicht rückgängig gemacht werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio]**.

1. Halten Sie auf der Registerkarte **[!UICONTROL Creatives]** den Cursor über die Kreativkarte und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Über Creative Studio in Advertising Creative](creative-studio-about.md)
>* [Verwalten von dynamischen Kreativen in Creative Studio](creative-studio-manage-dynamic-ads.md)
>* [Verwalten von Vorlagen in Creative Studio](creative-studio-manage-templates.md)
>* [Verwalten von Markenprofilen in Advertising Creative](/help/creative/brands/brand-manage.md)

