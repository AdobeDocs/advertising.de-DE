---
title: Varianten flexibler HTML5-Kreativen generieren
description: Erfahren Sie, wie Sie KI-unterstützte Varianten flexibler HTML5-Kreativer aus einer Kreativbibliothek generieren und speichern.
feature: Creative Standard Creatives
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d06c1576-7039-4934-b256-7366e138fbb6
    internal-label: Creative Standard Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 1cc477f531051d94ea88eaae0a4fb83918e95ea5
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%
---
# Varianten flexibler HTML5-Kreativen generieren

Verwenden Sie den [!UICONTROL Ad Variations Generator], um neue Varianten eines bestehenden flexiblen HTML5-Kreativprodukts zu erstellen. Der KI-Assistent generiert und verfeinert Überschriften, CTAs, Bilder, Farben und mehr und kann in einer einzigen Sitzung neue Größenvarianten erstellen. Speichern Sie die resultierenden Varianten als neue Standardanzeigen in der Kreativbibliothek.

>[!NOTE]
>
>Sie können auch Anzeigenvarianten aus [!UICONTROL Creative Studio] generieren. Beide Einstiegspunkte öffnen denselben [!UICONTROL Ad Variations Generator]. Weitere Einstiegspunkte [ Sie unter „Generieren von Anzeigenvarianten für eine Standardanzeige in ](/help/creative/creative-studio/creative-studio-manage-standard-ads.md#generate-ad-variations) Studio“.

## Verfügbarkeit {#availability}

Die **[!UICONTROL Generate Variations]** Aktion ist für flexible HTML5-Kreative, einschließlich solcher, die auf Systemvorlagen basieren, in der neuen [!UICONTROL Creative Libraries]-Benutzeroberfläche verfügbar. Sie ist nicht für andere Kreativtypen verfügbar, einschließlich dynamischer Kreativer.

Die Aktion ist deaktiviert, wenn der Kreative nicht über den internen Verweis auf die übergeordnete Anzeigenvorlage verfügt, der vom Generator benötigt wird. Diese Referenz ist keine Einstellung, die Sie bearbeiten können. Das Hochladen oder Ersetzen einer Datei auf der Registerkarte &quot;**[!UICONTROL Template]**&quot; des Kreativen legt sie nicht explizit fest.

## Öffnen des Anzeigenvarianten-Generators {#open-generator}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Öffnen Sie die Bibliothek auf eine der folgenden Arten:

   * Klicken Sie auf den Bibliotheksnamen.
   * Klicken Sie neben dem Bibliotheksnamen auf **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf **[!UICONTROL ...]** neben dem Namen für das flexible HTML5-Kreativ, und klicken Sie dann auf **[!UICONTROL Generate Variations]**.

   Die [!UICONTROL Ad Variations Generator] wird mit dem ausgewählten kreativen Inhalt geöffnet. Auf der Arbeitsfläche wird der Abschnitt **[!UICONTROL Template Sizes]** mit den verfügbaren Anzeigenformaten der Vorlage und ein **[!UICONTROL Ad Concepts]** Abschnitt mit den generierten Inhalten angezeigt.

## Erzeugen und Verfeinern von Varianten {#generate-variations}

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
      >Der KI-Assistent kann Text generieren und ändern (Überschriften, Unterüberschriften, CTAs, Textkörper), Hintergrundbilder austauschen, Markenfarben anwenden, Logo-Versionen wechseln und neue Größenvorlagen erstellen. Die Vorlagenstruktur kann nicht geändert werden: Elementpositionen, Layout, Abstand, Abstand, Schriftfamilie, Schriftgröße oder Rahmen. Nehmen Sie vor Beginn der Sitzung strukturelle Änderungen im Vorlageneditor vor. Siehe [Bearbeiten einer Vorlage](/help/creative/creative-studio/creative-studio-manage-templates.md#edit-template).

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

## Speichern der Varianten {#save-variations}

1. Wenn Sie mit den generierten Konzepten zufrieden sind, klicken Sie in der Kopfzeile auf **[!UICONTROL Save Standard Ads]** .

   Die Schaltfläche wird deaktiviert, bis mindestens ein Konzept vorhanden ist.

1. Überprüfen Sie im Dialogfeld **[!UICONTROL Save Standard Ads]** die folgenden Einstellungen und klicken Sie dann auf **[!UICONTROL Save Standard Ads]**.

   **[!UICONTROL Advertiser]:** Der Advertiser, der mit der kreativen Quellbibliothek verknüpft ist. Sie können diesen Wert nicht ändern.

   **[!UICONTROL Creative Library]:** Die kreative Quellbibliothek, in der die neuen Anzeigen gespeichert werden. Sie können diesen Wert nicht ändern.

   **[!UICONTROL Attach to Bundles]:** (Optional) Wenn diese Option aktiviert ist, werden die gespeicherten Kreativen an ein oder mehrere Bundles angehängt. Wählen Sie für jede Anzeigenvariante ein Bundle aus oder geben Sie einen neuen Bundle-Namen ein.

   **\[Einstellungen für jede Anzeige\]:** Für jede Anzeigenvariante können Sie die **[!UICONTROL Name]**-, **[!UICONTROL Language]**- und Clickthrough-URL für jedes Klick-Tag anzeigen und optional ändern.

   Kehren Sie zur Kreativbibliothek zurück.

>[!MORELIKETHIS]
>
>* [Standard-Kreative bearbeiten](creative-edit-standard.md)
>* [Verwalten von Standardanzeigen in Creative Studio](/help/creative/creative-studio/creative-studio-manage-standard-ads.md)
>* [Verwalten von Markenprofilen in Advertising Creative](/help/creative/brands/brand-manage.md)
>* [C2PA-Metadaten in [!UICONTROL Creative Studio]](/help/creative/creative-studio/creative-studio-content-credentials.md)
