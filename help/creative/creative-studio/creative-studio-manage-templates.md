---
title: Verwalten von Anzeigenvorlagen in Creative Studio
description: Erfahren Sie, wie Sie Anzeigenvorlagen in Adobe Advertising Creative erstellen, importieren, organisieren und verwalten.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: fcd97d29c5009d22100283970892d258043b2d90
workflow-type: tm+mt
source-wordcount: '3697'
ht-degree: 1%
---
# Verwalten von Anzeigenvorlagen in [!UICONTROL Creative Studio]

Erstellen, importieren und verwalten Sie Anzeige- und Video-Anzeigenvorlagen zur Verwendung in Anzeigengenerierungssitzungen.

## Die Ansicht [!UICONTROL Creative Studio] > [!UICONTROL Templates]

Die Registerkarte **[!UICONTROL Templates]** bietet schnelle Aktionen zum Erstellen oder Importieren neuer Anzeigenvorlagen.

Auf der Registerkarte &quot;[!UICONTROL Templates]&quot; werden Ihre vorhandenen Anzeigenvorlagen auch unten auf der Seite aufgeführt <!-- Only in the Templates tab -->als [ (Standard) oder als Tabellen/Listen](/help/creative/introduction/customize-data-views.md). Die Liste der Anzeigenvorlagen enthält Registerkarten für [!UICONTROL All], [!UICONTROL System Templates] (die Ihr Adobe-Konto-Team in Ihr Konto hochlädt) und [!UICONTROL User Templates]. Standardmäßig werden Anzeigenvorlagen für alle Ihre Werbetreibenden angezeigt. Um nur Anzeigenvorlagen für einen bestimmten Advertiser anzuzeigen, wählen Sie oben auf der Seite in der Liste der Advertiser aus.

<!--
Probably not necessary:

* **[!UICONTROL Card view]** &mdash; Displays templates as cards. Each card shows a preview thumbnail and the ad dimensions. Hovering a card reveals action controls.

* **[!UICONTROL Table view]** &mdash; Displays templates in a table with columns for **[!UICONTROL Name]**, **[!UICONTROL Type]**, **[!UICONTROL Status]**, **[!UICONTROL Size/Duration]**, **[!UICONTROL Advertiser]**, and **[!UICONTROL Updated]**. Click the **[!UICONTROL Name]** or **[!UICONTROL Updated]** column header to sort ascending or descending. Pagination controls appear at the bottom of the list.
-->

### Verfügbare Aktionen

<!--  Figure out how to handle these, which relate to the template list at the bottom of the page: * [Browse and search templates](#browse-search) -->

Erstellung:

* [Erstellen einer Anzeigenvorlage mithilfe von KI](#template-generate)

* [Manuelles Erstellen einer Anzeigenvorlage](#template-create)

* [HTML5-Anzeigenvorlagen importieren](#templates-import)

Aktionen für vorhandene Vorlagen:

* [Erzeugen von Anzeigenvarianten aus einer Anzeigenvorlage](#ad-variations-generate)

* [Bearbeiten einer Anzeigenvorlage](#template-edit)

* [Hinzufügen oder Entfernen von Kennzeichnungen für eine Anzeigenvorlage](#template-labels)

* [Anzeigen-Vorschau einer Vorlage](#template-preview)

* [Herunterladen einer Anzeigenvorlage](#template-download)

* [Hinzufügen oder Entfernen einer Anzeigenvorlage als Favorit](#template-favorite)

* [Löschen einer Anzeigenvorlage](#template-delete)

<!--

Move to a Common Tasks chapter:

## Browse and search templates {#browse-search}

### Search

Type in the **[!UICONTROL Search templates]** field and press **[!UICONTROL Enter]** to find templates by name. Click the **[!UICONTROL Clear search]** button to reset.

### Filter by source

Use the filter pills in the toolbar to show a subset of templates:

* **[!UICONTROL All]** &mdash; Shows all templates.
* **[!UICONTROL System Templates]** &mdash; Shows Adobe-provided templates only.
* **[!UICONTROL User Templates]** &mdash; Shows templates you or your team have created or imported.

### Filter by status or format

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Click **[!UICONTROL Filter]** in the toolbar.

1. In the **[!UICONTROL Filters]** dialog, select a filter category:

   * **[!UICONTROL Status]:** Filter by **[!UICONTROL Live]** or **[!UICONTROL Draft]**.
   * **[!UICONTROL Ad Format]:** Filter by **[!UICONTROL Display]** or **[!UICONTROL Video]**.

1. Select one or more options in the category, then click **[!UICONTROL Apply]**.

Applied filters appear as chips below the toolbar. To refine or remove an active filter, click its chip to open a popover where you can toggle options, then click **[!UICONTROL Apply]** or **[!UICONTROL Delete]** to remove the filter. To remove all active filters at once, click **[!UICONTROL Clear All]**.

-->

## Erstellen einer Anzeigenvorlage mithilfe von KI {#template-generate}

*Beta-Funktion*

Verwenden Sie KI in [!UICONTROL Creative Studio] , um ein vorhandenes statisches Display-Anzeigenbild in eine bearbeitbare Display-Anzeigenvorlage zu konvertieren. Ein dreistufiger Assistent unterstützt Sie bei der Erstellung und Überprüfung der Vorlage, beim Anfordern von Änderungen in natürlicher Sprache und beim Öffnen des Vorlageneditors, um manuelle Änderungen vorzunehmen und die Vorlage zu speichern.

### Voraussetzungen

Sie benötigen eine statische Bildanzeige in einer Creative-Bibliothek. Dieser Workflow wählt Anzeigen aus Ihren Bibliotheken aus und lädt kein neues Bild direkt in den Erstellungsdialog hoch.

<!--

Publish this when prompt-based generation becomes available:

To generate a template from an existing image, you need a static image ad in a Creative Library. This option selects ads from your libraries; it doesn't upload a new image directly in the generation dialog. You don't need an existing ad image to generate a template from a prompt.

-->

### Schritt 1: Erstellen und Überprüfen der Vorlage

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. (Optional) Wählen Sie oben auf der Seite einen Advertiser aus der Advertiser-Liste aus, um die Bibliotheken dieses Advertisers anzuzeigen.

1. Klicken Sie im **[!UICONTROL Use AI to Generate a New Display Ad Template]** auf **[!UICONTROL Generate]**.

1. Wählen Sie im Dialogfeld **[!UICONTROL Generate New Ad Template]** die Option **[!UICONTROL Generate from Existing Standard Ad Image]** aus, falls sie nicht bereits ausgewählt ist.

1. Wählen Sie in der Liste **[!UICONTROL Ad Library]** die Bibliothek aus, die die Bildanzeige enthält.

1. Halten Sie den Cursor über die Bild-Anzeigenkarte und klicken Sie auf **[!UICONTROL Use this Standard Ad]**.

   Die Generierung beginnt automatisch mit der Breite und Höhe der ausgewählten Anzeige.

<!--

Switch to this when prompt-based generation becomes available:

1. In the **[!UICONTROL Generate New Ad Template]** dialog, choose how to generate the template:

   * **[!UICONTROL Generate from Prompt]:** Describe the ad template you want to create using a text prompt.

   * **[!UICONTROL Generate from Existing Standard Ad Image]:** Convert an existing static image ad into an editable template.

1. Follow the steps for your selected option:

   * From a prompt:

      1. Enter a description of the template you want to create. Include details such as the layout, headline, call to action, and visual style.

      1. Follow the on-screen instructions to generate the template.

   * From an existing standard ad image:

      1. Select the library containing the image ad from the **[!UICONTROL Ad Library]** list.

      1. Hold the cursor over the image ad card and click **[!UICONTROL Use this Standard Ad]**.

         Generation begins automatically, using the selected ad's width and height.

-->

1. [Überprüfen und verfeinern Sie die generierte Vorlage](#template-review).

### Schritt 2: Vorlage überprüfen und verfeinern {#template-review}

1. Warten Sie, bis die Generierung abgeschlossen ist, und überprüfen Sie dann die Vorlagenvorschau und das Bedienfeld &quot;**[!UICONTROL Layers]**&quot;, falls verfügbar.

   Überprüfen Sie den Text, die Bilder und das Layout, bevor Sie die Vorlage verwenden. Die hier angezeigten Ebenen werden überprüft. Nehmen Sie manuelle Änderungen im Vorlageneditor vor.

1. (Optional) Anfordern von Änderungen an der generierten Vorlage:

   1. Beschreiben Sie im Feld **[!UICONTROL Ask the AI for any changes]** die gewünschten Änderungen. Geben Sie beispielsweise `Change the headline to "Limited Time Offer" and the button text to "Shop Now"` ein.

   1. Klicken Sie auf **[!UICONTROL Regenerate]**.

   1. Überprüfen Sie die aktualisierte Vorschau. Wiederholen Sie dies nach Bedarf.

1. Wenn Sie bereit zum Fortfahren sind, klicken Sie auf **[!UICONTROL Use this Ad Template]**.

   Die generierte Vorlage wird im Anzeigevorlageneditor geöffnet.

### Schritt 3: Vorlage bearbeiten und speichern {#template-save}

>[!TIP]
>
> Der KI-Assistent verwendet eine Open-Source-Schriftartenbibliothek, um eine genaue Übereinstimmung für die Schriftart in Ihrer Anzeige zu finden. Um Ihre eigene Schriftart zu verwenden, laden Sie sie auf die Registerkarte &quot;[!UICONTROL Assets]&quot; oder aus dem Vorlageneditor hoch und ersetzen Sie dann die generierte Schriftart im Editor.
>
> Um optimale Ergebnisse zu erzielen, ersetzen Sie im Vorlageneditor das von KI generierte Logo durch Ihr originales, pixelgenaues Logo.

1. Überprüfen Sie im Vorlageneditor die generierten Elemente und nehmen Sie die verbleibenden Änderungen mithilfe der Steuerelemente [Vorlageneditor) ](#template-controls).

1. Klicken Sie auf **[!UICONTROL Save]**.

1. Geben Sie im Dialogfeld &quot;**[!UICONTROL Update Template]**&quot; die **[!UICONTROL Template name]** ein, aktualisieren Sie sie, wählen Sie die **[!UICONTROL Advertiser]** aus und fügen Sie optional Tags hinzu.

1. Klicken Sie auf **[!UICONTROL Update]** , um die Vorlage zu speichern und zur **[!UICONTROL Templates]** zurückzukehren.

   Um stattdessen eine separate Kopie zu speichern, klicken Sie auf **[!UICONTROL Save As New]**.

Anschließend können Sie die Vorlage verwenden, um [Anzeigenvarianten zu generieren](#ad-variations-generate).

### Fehlerbehebung {#troubleshooting}

| Problem | Vorgehensweise |
| --- | --- |
| Beim Generieren aus einem Bild werden keine Bibliotheken oder Bildanzeigen aufgelistet | Markieren Sie den ausgewählten Advertiser und die **[!UICONTROL Ad Library]**. Wenn die Bibliothek keine Standard-Anzeigenbilder enthält, wählen Sie eine andere Bibliothek aus, die eine vorhandene statische Bildanzeige enthält. |
| Die bildbasierte Generierung schlägt fehl oder das Bild kann nicht konvertiert werden | Überprüfen Sie die angezeigte Nachricht, klicken Sie auf **[!UICONTROL Back to library]** und wählen Sie eine Bildanzeige aus, um es erneut zu versuchen. |

<!--

Add when prompt-based generation is available:

| Prompt-based generation fails | Review the displayed message and revise your prompt before trying again. |

-->

## Manuelles Erstellen einer Anzeigenvorlage {#template-create}

Erstellen Sie eine leere Anzeige- oder Videovorlage mit dem Vorlageneditor.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio].**

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Klicken Sie im **[!UICONTROL Create New Ad Template]** auf **[!UICONTROL Create]** und wählen Sie dann **[!UICONTROL Display Ad Template]** oder **[!UICONTROL Video Ad Template]** aus.

1. (Anzeigen-Anzeigen) Wählen Sie die Größe der Anzeigenvorlage aus und klicken Sie dann auf **[!UICONTROL Continue]**.

1. Konfigurieren Sie die Vorlageneinstellungen mithilfe der [Steuerelemente im Vorlageneditor](#template-controls).

1. (Optional) Um eine Kopie der Vorlage wie definiert herunterzuladen, klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

1. Speichern Sie die Vorlage:

   1. Führen Sie einen der folgenden Schritte aus:

      * Klicken Sie auf **[!UICONTROL Save]**.

      * Um die Vorlage als Entwurf zu speichern, klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**.

   1. Geben Sie die **[!UICONTROL Template name]** ein, wählen Sie die **[!UICONTROL Advertiser]** aus, wählen Sie optional vorhandene Tags aus oder fügen Sie neue Tags zur Vorlage hinzu und klicken Sie dann auf **[!UICONTROL Save]**.

## HTML5-Anzeigenvorlagen importieren {#templates-import}

Laden Sie eine oder mehrere vordefinierte HTML5-Vorlagen hoch, die als ZIP-Dateien gepackt sind. Vorlagen werden beim Import validiert. Der Import schlägt fehl, wenn der HTML 200.000 Zeichen oder das CSS 60.000 Zeichen oder die Vorlage mehr als 5.000 DOM-Elemente enthält oder nicht unterstützte Skript-Tags enthält.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio].**

1. Wählen Sie den Advertiser oben auf der Seite aus.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Klicken Sie im **[!UICONTROL Upload HTML5 Templates]** auf **[!UICONTROL Upload]** und wählen Sie dann **[!UICONTROL Display Ad Template]** oder **[!UICONTROL Video Ad Template]** aus.

1. Wählen Sie eine oder mehrere ZIP-Dateien von Ihrem Gerät oder Netzwerk aus.

1. Im Dialogfeld **[!UICONTROL Import Templates]** :

   1. **[!UICONTROL Advertiser]** auswählen.

      Wenn Sie oben auf der Seite bereits einen bestimmten Advertiser ausgewählt haben, ist dieser Advertiser vorausgewählt.

   1. (Optional) Bearbeiten Sie für jede Datei die **[!UICONTROL Template Name]**.

      Der Dateiname wird standardmäßig verwendet.

   1. (Optional) Um weitere Dateien hinzuzufügen, klicken Sie auf **[!UICONTROL Add more]** und wählen Sie zusätzliche ZIP-Dateien aus. Geben Sie die **[!UICONTROL Template Name]** für jede zusätzliche Datei an.

1. Klicken Sie auf **[!UICONTROL Import Templates]**.

>[!NOTE]
>
>Wenn der Import fehlschlägt, vereinfachen Sie die Vorlage oder wenden Sie sich an Ihr Adobe Account Team.

## Bearbeiten einer Anzeigenvorlage {#template-edit}

*Nur Anzeigenvorlagen anzeigen.*

>[!IMPORTANT]
>
>Der KI-Agent kann das Vorlagenlayout, die Elementpositionen, den Abstand oder die Typografie nicht ändern. Nehmen Sie vor dem Generieren von Inhalten strukturelle Änderungen im Vorlageneditor vor.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio].**

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Halten Sie den Cursor über die Vorlagenkarte oder Tabellenzeile und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Edit Template]**.

1. Bearbeiten Sie das Vorlagenlayout oder die Vorlagenelemente mithilfe der [Steuerelemente im Vorlageneditor](#template-controls).

1. (Optional) Um eine Kopie der Vorlage wie definiert herunterzuladen, klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

1. Speichern Sie die Vorlage:

   * Klicken Sie auf **[!UICONTROL Save]**.

   * Um die Vorlage als Entwurf zu speichern, klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**. Geben Sie die **[!UICONTROL Template name]** ein, wählen Sie die **[!UICONTROL Advertiser]** aus, wählen Sie optional vorhandene Tags aus oder fügen Sie neue Tags zur Vorlage hinzu und klicken Sie dann auf **[!UICONTROL Save]**.

<!--

I don't see this anywhere:

1. Click **[!UICONTROL Generate Ad Variations]** to proceed to content generation, or navigate away to save your changes.

-->

## Erzeugen von Anzeigenvarianten aus einer Anzeigenvorlage {#ad-variations-generate}

*Nur Anzeigenvorlagen anzeigen.*

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio].**

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Halten Sie den Cursor über die Vorlagenkarte oder Tabellenzeile und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**.

   Die [!UICONTROL Ad Variations Generator] wird geöffnet, wobei die Vorlage bereits geladen ist.

1. Verwenden Sie die KI-Chat-Oberfläche, um Anzeigeninhalte zu generieren und zu verfeinern. Siehe [Verwalten von Standardanzeigen in Creative Studio](creative-studio-manage-standard-ads.md) für den vollständigen Workflow.

## Hinzufügen oder Entfernen von Kennzeichnungen für eine Anzeigenvorlage {#template-labels}

*Nur Anzeigenvorlagen anzeigen.*

Mit Beschriftungen können Sie Benutzervorlagen organisieren und filtern. Sie können Systemvorlagen keine Kennzeichnungen hinzufügen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio].**

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Halten Sie den Cursor über die Vorlagenkarte oder Tabellenzeile und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Edit Labels]**.

1. Im Dialogfeld **[!UICONTROL Edit Labels]** :

   * Um einen Titel hinzuzufügen, wählen Sie entweder einen vorhandenen Titel aus oder geben Sie einen Namen in das Eingabefeld ein und klicken Sie auf **[!UICONTROL Add Tag]**.

   * Um eine Bezeichnung zu entfernen, klicken Sie **[!UICONTROL X]** neben der Bezeichnung Tag .

1. Klicken Sie auf **[!UICONTROL Save]**.

## Anzeigen-Vorschau einer Vorlage {#template-preview}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio].**

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Halten Sie den Cursor über die Vorlagenkarte.

1. Führen Sie einen der folgenden Schritte aus:

   * (Kartenansicht) Klicken Sie auf das **[!UICONTROL Preview template]** oder auf **[!UICONTROL ...]** > **[!UICONTROL Preview]**.

   * (Tabellenansicht) Klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Preview]**.

1. Klicken Sie für Videovorlagen auf ![Play](/help/creative/assets/play.png "Play").

## Herunterladen einer Anzeigenvorlage {#template-download}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio].**

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Halten Sie den Cursor über die Vorlagenkarte oder Tabellenzeile und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Download]**.

   Die Vorlage wird als ZIP-Datei gemäß dem normalen Verfahren Ihres Browsers heruntergeladen.

## Hinzufügen oder Entfernen einer Anzeigenvorlage als Favorit {#template-favorite}

*Nur Kartenansicht*

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio].**

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Halten Sie den Cursor über die Vorlagenkarte.

1. Führen Sie einen der folgenden Schritte aus:

   * Um eine Vorlage als Favorit hinzuzufügen, klicken Sie auf ![Favorit](/help/creative/assets/favorite-null.png "Favorit").

   * Um eine Vorlage als Favorit zu entfernen, klicken Sie auf ![Favorit](/help/creative/assets/favorite.png "Favorit").

## Löschen einer Anzeigenvorlage {#template-delete}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio].**

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Halten Sie den Cursor über die Vorlagenkarte oder Tabellenzeile und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

## Steuerelemente des Vorlageneditors {#template-controls}

Sowohl der Anzeige- als auch der Videovorlageneditor bieten eine Symbolleiste über der Arbeitsfläche, um Änderungen rückgängig zu machen und die Ansicht anzupassen, Bedienfelder auf der linken Seite zum Hinzufügen von Assets und Elementen und ein [!UICONTROL Layers] Bedienfeld auf der rechten Seite zum Verwalten von Ebenen. Die Werkzeuge zum Bearbeiten ausgewählter Elemente und zum Steuern des Timings und der Wiedergabe unterscheiden sich zwischen Anzeige- und Videovorlagen.

<!--

Removing -- these are actions that are used within specific procedures:

### Top toolbar

The top toolbar above the canvas is the same for both display and video templates.

| Control | Description |
| --- | --- |
| Template name | The current template name, shown at the top of the editor. Click the **[!UICONTROL Edit name]** icon next to the name to rename it inline. |
| **[!UICONTROL Save]** | Saves and publishes the template. |
| **[!UICONTROL ...]** > **[!UICONTROL Save As Draft]** | Saves the template as a draft without publishing. Enter or update the name, select the advertiser, optionally add tags, and click **[!UICONTROL Save]**. |
| **[!UICONTROL ...]** > **[!UICONTROL Download]** | Downloads the current template as a ZIP file. |
| **[!UICONTROL Cancel]** | Discards unsaved changes and returns to the Templates list. |

-->

### Rückgängigmachen von Änderungen und Anpassen der Arbeitsflächenansicht

Die Symbolleiste mit allgemeinen Aktionen befindet sich über der Arbeitsfläche für die Bearbeitung im Anzeigenvorlagen-Editor und ist in zwei Teile (links und rechts) unterteilt.

#### Anzeigen von Anzeigenvorlagen

| Kontrolle | Beschreibung |
| --- | --- |
| **[!UICONTROL Undo]** | Macht die letzte Aktion rückgängig. |
| ![Wiederholen](/help/creative/assets/cs-icon-redo.png "Wiederholen") **[!UICONTROL Redo]** | Stellt die letzte rückgängig gemachte Aktion wieder her. |
| **[!UICONTROL Links]** | Öffnet ein Bedienfeld zur Verwaltung der Clickthrough-URLs, die an Elemente in der Vorlage angehängt sind. |
| Zoom-Steuerung | Klicken Sie auf **[!UICONTROL Zoom out]** oder **[!UICONTROL Zoom in]**, um die Vergrößerung der Arbeitsfläche anzupassen (10 %-150 % in Schritten von 10 %). Klicken Sie auf die Beschriftung Zoom-Ebene , die **[!UICONTROL Auto]** anzeigt, wenn die Arbeitsfläche automatisch angepasst wird, oder einen Prozentsatz, wenn er manuell festgelegt wird, um ein Menü mit Optionen zu öffnen: **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]** und **[!UICONTROL Zoom Out]**. |
| Anzeigengröße | Zeigt die aktuellen Werbedimensionen an (z. B. 300 × 250). Klicken Sie hier, um die Größenauswahl zu öffnen, die sechs häufig verwendete IAB-Standardgrößen als Karten sowie eine Dropdown-Liste mit allen 19 standardmäßigen IAB-Anzeigengrößen bietet. Die Standardgröße für neue Vorlagen beträgt 300 × 250 (Medium-Rechteck). |
| ![Ebenenbedienfeld öffnen](/help/creative/assets/layers-panel-open.png "Ebenenbedienfeld öffnen") | Öffnet das [!UICONTROL Layers]. Wird nur angezeigt, wenn das Bedienfeld [!UICONTROL Layers] geschlossen ist. |

#### Video-Anzeigenvorlagen

| Kontrolle | Beschreibung |
| --- | --- |
| **[!UICONTROL Undo]** / ![Wiederholen](/help/creative/assets/cs-icon-redo.png "Wiederholen") **[!UICONTROL Redo]** | Macht die letzte Aktion rückgängig oder wiederholt sie. |
| Zoom-Steuerung | Klicken Sie auf **[!UICONTROL Zoom out]** oder **[!UICONTROL Zoom in]**, um die Vergrößerung der Arbeitsfläche anzupassen. Klicken Sie auf die Zoomstufe, um ein Menü mit Optionen zu öffnen: **[!UICONTROL Auto-Fit Page]**, **[!UICONTROL 100% Zoom]**, **[!UICONTROL 50% Zoom]**, **[!UICONTROL Zoom In]** und **[!UICONTROL Zoom Out]**. |
| ![Ebenenbedienfeld öffnen](/help/creative/assets/layers-panel-open.png "Ebenenbedienfeld öffnen") | Öffnet das [!UICONTROL Layers]. Wird nur angezeigt, wenn das Bedienfeld [!UICONTROL Layers] geschlossen ist. |

<!--

Not there as of 10/15:

| Page resize | Opens the page-size controls to change the video template dimensions. |
| **[!UICONTROL Preview]** | Opens a preview of the video template. |

   -->

### Hinzufügen von Assets und Elementen

Im linken Bereich können Sie der Vorlage Assets und Elemente hinzufügen. Klicken Sie auf ein Symbol, um das Inhaltsbedienfeld zu öffnen. Klicken Sie zum Schließen erneut auf dasselbe Symbol.

#### Anzeigen von Anzeigenvorlagen

| Symbol | Beschreibung |
| --- | --- |
| **[!UICONTROL Search]** | Suchen Sie nach allen Asset-Typen in Ihrer Bibliothek. |
| **[!UICONTROL Upload]** | Laden Sie Bilder oder Schriftarten zur Verwendung in der aktuellen Vorlage in den Editor hoch. Sie können bis zu 20 Dateien gleichzeitig hochladen. |
| **[!UICONTROL Templates]** | Durchsuchen Sie Anzeigenvorlagen aus Ihrer Creative Studio-Bibliothek, die als Basisebene oder Referenzelement verwendet werden sollen. |
| **[!UICONTROL My Assets]** | Durchsuchen Sie die Registerkarte Creative Studio-[!UICONTROL Assets] nach allen hochgeladenen Assets. |
| **[!UICONTROL Images]** | Durchsuchen Sie die Registerkarte Creative Studio-[!UICONTROL Assets] nur nach den hochgeladenen Bild-Assets. |
| **[!UICONTROL Text]** | Fügen Sie der Arbeitsfläche ein Textelement hinzu, einschließlich aller hochgeladenen benutzerdefinierten Schriftarten. |
| **[!UICONTROL Elements]** | Hinzufügen von Formen und Layout-Elementen wie Schaltflächen und Rechtecken. |

Sie können ein Element aus einem beliebigen Bedienfeld direkt auf die Arbeitsfläche ziehen oder darauf klicken, um es an einer Standardposition zu platzieren.

#### Video-Anzeigenvorlagen

| Symbol | Beschreibung |
| --- | --- |
| **[!UICONTROL Search]** | Suchen Sie nach allen Asset-Typen in Ihrer Bibliothek. |
| **[!UICONTROL Upload]** | Laden Sie Bild-, Video-, Audio- oder Schriftdateien (TTF, OTF, WOFF, WOFF2) in den Editor hoch, um sie in der aktuellen Vorlage zu verwenden. Sie können bis zu 20 Dateien gleichzeitig hochladen. |
| **[!UICONTROL Templates]** | Durchsuchen von Anzeigenvorlagen aus Ihrer Creative Studio-Bibliothek. |
| **[!UICONTROL My Assets]** | Durchsuchen Sie die Registerkarte Creative Studio-[!UICONTROL Assets] nach allen hochgeladenen Assets. |
| **[!UICONTROL Images]** | Durchsuchen Sie die Registerkarte Creative Studio-[!UICONTROL Assets] nur nach den hochgeladenen Bild-Assets. |
| **[!UICONTROL Video]** | Durchsuchen Sie die Registerkarte Creative Studio-[!UICONTROL Assets] nur nach hochgeladenen Video-Assets. |
| **[!UICONTROL Audio]** | Durchsuchen Sie die Registerkarte Creative Studio-[!UICONTROL Assets] nur nach hochgeladenen Audio-Assets. |
| **[!UICONTROL Text]** | Fügen Sie der Arbeitsfläche ein Textelement hinzu, einschließlich aller hochgeladenen benutzerdefinierten Schriftarten. |
| **[!UICONTROL Elements]** | Hinzufügen von Formen und Vektorelementen. |

Sie können ein Element aus einem beliebigen Bedienfeld direkt auf die Arbeitsfläche ziehen oder darauf klicken, um es an einer Standardposition zu platzieren.

### Ausgewählte Elemente bearbeiten

Klicken Sie auf ein Element auf der Arbeitsfläche für die Bearbeitung, um es auszuwählen. Je nach Vorlagentyp werden eine oder mehrere Symbolleisten mit Steuerelementen für dieses Element angezeigt.

Die Steuerelemente variieren je nach Elementtyp.

<!-- From inspectorbar.ts -->

#### Symbolleiste zur Bearbeitung von Vorlagen anzeigen

| Kontrolle | Elementtypen | Beschreibung |
| --- | --- | --- |
| **[!UICONTROL Properties]** | Alle | Öffnet ein Bedienfeld, in dem Sie den Ebenennamen bearbeiten, die Ebene als dynamisch markieren (kann während der Anzeigengenerierung ausgetauscht werden) und eine Clickthrough-URL festlegen können (nur Links). Wählen Sie darunter einen **[!UICONTROL Default]**-, **[!UICONTROL Hover]**-, **[!UICONTROL Click]**- oder **[!UICONTROL Focus]**, um das Element für diesen Interaktionsstatus zu gestalten, und passen Sie dann Stile an - Typografie (nur Text und Links), Dekorationen (Füllung, Rahmen, Eckenradius), Abmessungen, Position - je nach Elementtyp. |
| **[!UICONTROL Effects]** | Alle | Öffnet ein Bedienfeld, in dem Sie einen **[!UICONTROL Default]**-, **[!UICONTROL Hover]**-, **[!UICONTROL Click]**- oder **[!UICONTROL Focus]** auswählen, auf den Sie Effekte für diesen Interaktionsstatus anwenden möchten, und dann die Abschnitte **[!UICONTROL Transform]**, **[!UICONTROL Transition]**, **[!UICONTROL Box Shadow]**, **[!UICONTROL Filter]**, **[!UICONTROL Blend Mode]** und **[!UICONTROL Cursor]** anpassen können. Textelemente enthalten auch einen **[!UICONTROL Text Shadow]**. |
| **[!UICONTROL Animations]** | Alle | Öffnet ein Bedienfeld, um die Eintritts- und Austrittszeit der Ebene auf der Zeitleiste festzulegen und **[!UICONTROL Entrance Animation]**-, **[!UICONTROL Loop Animation]**- und **[!UICONTROL Exit Animation]**-Vorgaben mit Dauer und Erleichterung zu konfigurieren. Umfasst **[!UICONTROL Copy]**-, **[!UICONTROL Paste]**- und **[!UICONTROL Reset]**. |
| **[!UICONTROL Crop]** | Bilder | Öffnet eine Symbolleiste zum Zuschneiden des Bildes. Wählen Sie eine **[!UICONTROL Aspect Ratio]** (oder **[!UICONTROL Free]**) aus und klicken Sie dann auf **[!UICONTROL Apply]** oder **[!UICONTROL Cancel]**. |
| **[!UICONTROL Position]** | Alle | Öffnet ein Menü mit **[!UICONTROL Move]** Optionen (**[!UICONTROL Forward]**, **[!UICONTROL Backward]**, **[!UICONTROL To front]**, **[!UICONTROL To back]**), **[!UICONTROL Align to Page]** Optionen (**[!UICONTROL Top]**, **[!UICONTROL Left]**, **[!UICONTROL Middle]**, **[!UICONTROL Center]**, **[!UICONTROL Bottom]**, **[!UICONTROL Right]**, **[!UICONTROL Fit Vertically]**, **[!UICONTROL Fit Horizontally]**, **[!UICONTROL Fit to Page]**) und für Nicht-Bild-Elemente **[!UICONTROL Layer Level Alignment]** Optionen (dieselben sechs Ausrichtungsoptionen plus **[!UICONTROL Fit to Content]**). |

#### Symbolleiste zum Bearbeiten von Videovorlagen

| Kontrolle | Elementtypen | Beschreibung |
| --- | --- | --- |
| **[!UICONTROL Shape]** | Shapes | Legt formspezifische Optionen fest. |
| Abschaltsteuerungen | Bilder | Ausschnitttyp, Versatz und Glättung einstellen. |
| **[!UICONTROL Group]** / **[!UICONTROL Ungroup]** | Mehrere ausgewählte Elemente oder eine Gruppe | Gruppiert die ausgewählten Elemente zusammen oder hebt die Gruppierung einer ausgewählten Gruppe auf. |
| **[!UICONTROL Combine]** | Kompatible Formen | Kombiniert ausgewählte Formen zu einer einzigen Form. |
| **[!UICONTROL Audio replace]** | Audio und Video | Ersetzt die Audiospur durch eine Datei aus Ihrer Asset-Bibliothek. |
| **[!UICONTROL Typeface]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]**, **[!UICONTROL Font size]**, **[!UICONTROL Align horizontal]**, **[!UICONTROL Advanced]** | Text | Passt Schriftfamilie, Stärke, Größe, horizontale Ausrichtung und andere erweiterte Typografieeinstellungen an. |
| **[!UICONTROL Image]** / **[!UICONTROL Video]** | Bilder und Videos | Legt die Bild- oder Videoquelle zum Ausfüllen des Elements fest. |
| **[!UICONTROL Trim]** | Video und Audio | Öffnet den Trimmmodus, um den Start- und Endpunkt des Clips festzulegen. |
| ![Volume](/help/creative/assets/volume.png "Volume") ([!UICONTROL Volume]) | Video und Audio | Einstellung des Audiopegels |
| ![Wiedergabegeschwindigkeit](/help/creative/assets/speed.png "Wiedergabegeschwindigkeit") ([!UICONTROL Playback speed]) | Video und Audio | Einstellung der Wiedergabegeschwindigkeit. |
| ![Zuschneiden](/help/creative/assets/crop.png "Zuschneiden") ([!UICONTROL Crop]) | Alle | Schneidet das Element auf einen benutzerdefinierten Bereich zu. |
| Dreh- und Kippsteuerung | Alle | Das ausgewählte Element drehen oder spiegeln. |
| ![Stroke](/help/creative/assets/stroke.png "Stroke") ([!UICONTROL Stroke]) | Alle | Legt die Rahmenfarbe und -breite fest. |
| **[!UICONTROL Text Background]** | Text | Fügt eine Hintergrundfarbe hinter dem Text hinzu. |
| **[!UICONTROL Animations]** | Alle | Fügt Animationen zum Eintreten, Beenden oder Schleifen hinzu oder bearbeitet sie. |
| **[!UICONTROL Style]** | Alle | Öffnet ein Menü mit den Optionen **[!UICONTROL Adjustments]**, **[!UICONTROL Filter]**, **[!UICONTROL Effect]** und **[!UICONTROL Blur]**. |
| **[!UICONTROL Shadow]** | Alle | Fügt einen Schlagschatten hinzu oder bearbeitet ihn. |
| **[!UICONTROL Opacity]** | Alle | Legt die Transparenzstufe des Elements fest. |
| **[!UICONTROL Position]** | Alle | Passt die Größe, Position und numerische Drehung des Elements an. |
| ![Bearbeitungsbereich](/help/creative/assets/cs-template-video-editing-panel.png "Bearbeitungsbereich") | Alle | Öffnet oder schließt ein [Bearbeitungsfenster](#detailed-element-properties-for-video-templates) für das ausgewählte Element mit mehr Bearbeitungsmöglichkeiten. |

#### Detaillierte Elementeigenschaften für Videovorlagen

Klicken Sie im Videovorlageneditor auf ![Bearbeitungsbereich](/help/creative/assets/cs-template-video-editing-panel.png "Bearbeitungsbereich") in der Symbolleiste, um einen Bearbeitungsbereich für das ausgewählte Element mit weiteren Bearbeitungsfunktionen zu öffnen. Das Bearbeitungsfenster wird auf der linken Seite der Arbeitsfläche angezeigt und ist vom [!UICONTROL Layers]-Panel getrennt, in dem die Ebenen in der Vorlage aufgeführt sind.

##### Einzelne Elemente

Wenn Sie ein einzelnes Bild, Video, eine Form oder ein Textelement auswählen, werden im Bearbeitungsbereich die entsprechenden Abschnitte unten angezeigt.

| Bedienfeld-Abschnitt | Tool | Kontrollen |
| --- | --- | --- |
| [!UICONTROL Layer] | Ausrichtung und Ebenenpositionierung | Richtet die ausgewählte Ebene links, horizontal zentriert, rechts, oben, vertikal zentriert oder unten aus. Das Menü Anordnung ändert seine Stapelreihenfolge von vorne nach hinten. Diese Steuerelemente positionieren die Ebene selbst, sie richten keinen Text innerhalb der Ebene aus. |
| | [!UICONTROL Rotate & Flip] | Geben Sie einen Drehwinkel in Grad ein. Spiegeln Sie mit ![Horizontal spiegeln](/help/creative/assets/cs-template-video-flip.png "Horizontal spiegeln") die Ebene horizontal oder ![Vertikal spiegeln](/help/creative/assets/cs-template-video-flip-vertical.png "Vertikal spiegeln") die Ebene vertikal. |
| | ![Opacity](/help/creative/assets/cs-template-video-opacity.png "Opacity") [!UICONTROL Opacity] | Macht die ausgewählte Ebene mehr oder weniger transparent. |
| | ![Mischmodus](/help/creative/assets/cs-template-video-blend-mode.png "Mischmodus") [!UICONTROL Blend Mode] | Ändert die Kombination der Farben der ausgewählten Ebene mit den dahinter liegenden Ebenen. |
| | [!UICONTROL Transform]: [!UICONTROL Position & Size] | Öffnet zusätzliche Steuerelemente für die Position und Bemaßungen des Layers. Die Verfügbarkeit hängt von den Transformationsberechtigungen der ausgewählten Ebene ab. |
| [!UICONTROL Shape] | ![Formoptionen](/help/creative/assets/cs-template-video-shape-options.png "Formoptionen") [!UICONTROL Shape] und formspezifische Eigenschaften | Ändert die Form und die verfügbaren Eigenschaften, z. B. Punkte, Seiten, Innendurchmesser, Linienbreite oder Eckenradius. Die Steuerelemente hängen von der ausgewählten Form ab. |
| | [!UICONTROL Vector]: [!UICONTROL Edit Path] | Wechselt in den Modus für die Vektorbearbeitung, um den Pfad des Shapes zu bearbeiten, sofern verfügbar. |
| [!UICONTROL Character] | ![Typeface](/help/creative/assets/cs-template-video-typeface.png "Typeface") Typeface, ![Text style](/help/creative/assets/cs-template-video-text-style.png "Text style") Textstyle, ![Bold](/help/creative/assets/cs-template-video-text-bold.png "Bold") fett, ![Italic](/help/creative/assets/cs-template-video-text-italic.png "Italic") und ![Font size](/help/creative/assets/cs-template-video-font-size.png "Font size") | (Textebenen) Ändert die Schriftfamilie, den Schriftstil und die Größe des ausgewählten Textes. |
| | ![Linksbündig](/help/creative/assets/cs-template-video-text-align-l.png "Linksbündig")/![Zentriert](/help/creative/assets/cs-template-video-text-align-c.png "Zentriert ausrichten")/![Rechtsbündig](/help/creative/assets/cs-template-video-text-align-r.png "Rechtsbündig") Textausrichtung | (Textebenen) Richtet den Text innerhalb des Rahmens links, zentriert oder rechts aus oder erkennt die Ausrichtung automatisch. |
| | ![Erweiterte Texteinstellungen](/help/creative/assets/cs-template-video-advanced-text.png " Erweiterte Texteinstellungen") Erweiterte Texteinstellungen | (Textebenen) Öffnet zusätzliche Typografie-Einstellungen. |
| [!UICONTROL Fill] | ![Fill](/help/creative/assets/cs-template-video-fill.png "Fill") Fill-Steuerelemente | Ändert die Farbe, das Bild oder die Videofüllung der ausgewählten Ebene. Die Steuerelemente spiegeln den aktuellen Fülltyp wider und öffnen dessen Einstellungen. Für Text ändert die Textfarbe. |
| [!UICONTROL Stroke] | ![Stroke](/help/creative/assets/cs-template-video-stroke.png "Stroke") Stroke-Steuerelemente | Aktiviert oder deaktiviert die Kontur und ändert ihre Farbe, Breite, Stil und Platzierung. Zusätzliche Steuerelemente werden angezeigt, wenn der Strich aktiviert ist. |
| [!UICONTROL Text Background] | ![Text-Hintergrund](/help/creative/assets/cs-template-video-text-bg.png "Text-Hintergrund") Hintergrundsteuerelemente | (Textebenen) Fügt den Hintergrund hinter dem Text hinzu oder ändert ihn. |
| [!UICONTROL Animations] | ![Animation](/help/creative/assets/cs-template-video-animation.png "Animation") [!UICONTROL Presets] | Öffnet Animationsvorgaben für die ausgewählte Ebene, einschließlich Eintritts-, Austritts- und Schleifenanimationen. |
| [!UICONTROL Appearance] | ![Anpassungen](/help/creative/assets/cs-template-video-adjustments.png "Anpassungen") [!UICONTROL Adjustments] | Ändert die visuellen Eigenschaften der ausgewählten Ebene. |
| | ![filter](/help/creative/assets/cs-template-video-filter.png "filter") [!UICONTROL Filter] | Wendet einen visuellen Filter auf die ausgewählte Ebene an. |
| | ![EFFECTS](/help/creative/assets/cs-template-video-effects.png "EFFECTS") [!UICONTROL Effect] | Wendet einen Effekt auf die ausgewählte Ebene an. |
| | ![blur](/help/creative/assets/cs-template-video-blur.png "blur") [!UICONTROL Blur] | Wendet einen Weichzeichner auf die ausgewählte Ebene an. |
| | ![Shadow](/help/creative/assets/cs-template-video-shadow.png "Shadow") [!UICONTROL Shadow] | Fügt den Schatten der ausgewählten Ebene hinzu oder ändert ihn. |

##### Mehrfachauswahl und spezialisierte Elemente

Wenn Sie mehrere Elemente, eine Gruppe, ein Ausschnittselement oder einen Audio-Clip auswählen, werden im Bearbeitungsfenster die folgenden Auswahlbereiche angezeigt. Mehrere Elemente, Gruppen und Ausschnitte behalten auch den [!UICONTROL Layer] bei.

| Bedienfeld-Abschnitt | Tool | Kontrollen |
| --- | --- | --- |
| [!UICONTROL Layer] | Ausrichtung und Ebenenpositionierung | Richtet mehrere ausgewählte Elemente oder eine Gruppe aus. Das Menü Anordnung ändert die Stapelreihenfolge von vorne nach hinten. |
| | [!UICONTROL Rotate & Flip] | Dreht oder kippt die ausgewählten Elemente oder Gruppen. |
| | ![Opacity](/help/creative/assets/cs-template-video-opacity.png "Opacity") [!UICONTROL Opacity] | Macht die ausgewählten Elemente oder Gruppen mehr oder weniger transparent. |
| | ![Mischmodus](/help/creative/assets/cs-template-video-blend-mode.png "Mischmodus") [!UICONTROL Blend Mode] | Ändert, wie die Farben der ausgewählten Elemente oder Gruppen mit den dahinter liegenden Ebenen kombiniert werden. |
| | [!UICONTROL Transform]: [!UICONTROL Position & Size] | Öffnet die Steuerelemente für die Position und Abmessungen der ausgewählten Elemente oder Gruppen. Die verfügbaren Steuerelemente hängen von den ausgewählten Elementen ab. |
| [!UICONTROL Selection] | ![group](/help/creative/assets/cs-template-video-group.png "group") group/![ungroup](/help/creative/assets/cs-template-video-ungroup.png "ungroup") ungroup | Wird unter [!UICONTROL Layer] für mehrere ausgewählte Ebenen oder eine ausgewählte Gruppe angezeigt. Gruppiert ausgewählte Ebenen, damit sie gemeinsam verwaltet werden können, oder trennt eine Gruppe in einzelne Ebenen. |
| [!UICONTROL Settings] | ![Ausschnitt-Clip](/help/creative/assets/cs-template-video-cutout-clip.png "Ausschnitt-Clip")/![Ausschnitt-Überlagerung](/help/creative/assets/cs-template-video-cutout-overlay.png "Ausschnitt-Überlagerung") Ausschnitt-Steuerelemente | (Ausgeschnittene Ebenen) Erscheint unter [!UICONTROL Layer]. Wählt den Ausschnitttyp aus und passt dessen Versatz und Kantenglättung an. |
| [!UICONTROL Audio Properties] | ![Trim](/help/creative/assets/cs-template-video-trim.png "Trim") Trim, ![Volume](/help/creative/assets/cs-template-video-volume.png "Volume") Volume und ![Wiedergabegeschwindigkeit](/help/creative/assets/cs-template-video-playback-speed.png "Wiedergabegeschwindigkeit") Wiedergabegeschwindigkeit | (Audio-Ebenen) Legt die Start- und Endpunkte eines Clips sowie den Audiopegel und die Wiedergabegeschwindigkeit fest. |

#### Elemente direkt auf der Arbeitsfläche bearbeiten

##### Anzeigen von Anzeigenvorlagen

| Aktion | Beschreibung |
| --- | --- |
| **[!UICONTROL Replace]** | (Nur Bildelemente) Öffnet das Bedienfeld Bilder , in dem Sie das Bild durch ein Bild aus Ihrer Asset-Bibliothek ersetzen können. |
| ![Vorwärts](/help/creative/assets/cs-icon-move-forward.png "Vorwärts") **[!UICONTROL Move forward]** | Verschiebt das Element einen Schritt nach vorne in der Stapelreihenfolge (nach vorne). |
| ![Rückwärts](/help/creative/assets/cs-icon-move-backward.png "Rückwärts") **[!UICONTROL Move backward]** | Verschiebt das Element in der Stapelreihenfolge um einen Schritt nach hinten (nach hinten). |
| ![Duplicate](/help/creative/assets/cs-icon-duplicate.png "Duplicate") **[!UICONTROL Duplicate]** | Erstellt eine Kopie des Elements. |
| ![delete](/help/creative/assets/cs-icon-delete.png "delete") **[!UICONTROL Delete]** | Entfernt das Element von der Arbeitsfläche. |
| Drehgriff | Klicken und ziehen Sie den Ziehgriff über einem ausgewählten Element, um es zu drehen. Halten Sie die **[!UICONTROL Shift]** beim Ziehen gedrückt, um die Drehung in 15-Grad-Inkrementen auszurichten. |

Sie können auch auf ein ausgewähltes Element klicken und es ziehen, um es neu zu positionieren, und auf die Griffe klicken und ziehen, um die Größe zu ändern.

##### Video-Anzeigenvorlagen

| Aktion | Beschreibung |
| --- | --- |
| **[!UICONTROL Edit text]** | (Nur Textelemente) Wechselt in den Textbearbeitungsmodus, damit Sie Text direkt auf der Arbeitsfläche eingeben und formatieren können. Im Textbearbeitungsmodus bietet ein sekundäres Menü **[!UICONTROL Text color]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]** und **[!UICONTROL Text variables]** (Vorlagenplatzhalter). |
| **[!UICONTROL Replace]** | (Nur Bildelemente) Öffnet die Asset-Bibliothek, in der Sie das Bild austauschen können. |
| **[!UICONTROL Bring forward]** | Verschiebt das Element in der Stapelreihenfolge um einen Schritt nach vorn. |
| **[!UICONTROL Send backward]** | Verschiebt das Element in der Stapelreihenfolge um einen Schritt zurück. |
| **[!UICONTROL Duplicate]** | Erstellt eine Kopie des Elements. |
| **[!UICONTROL Delete]** | Entfernt das Element von der Arbeitsfläche. |
| **... >[!UICONTROL Flip horizontal]** | Spiegelt das Element horizontal um 180 Grad. |
| **... >[!UICONTROL Flip vertical]** | Spiegelt das Element vertikal um 180 Grad. |
| **... >[!UICONTROL Copy Element]** | Kopiert das Element in die Zwischenablage der Arbeitsfläche. |
| **... >[!UICONTROL Pastes Element]** | Fügt das kopierte Element ein. |

Sie können auch auf ein ausgewähltes Element klicken und es ziehen, um es neu zu positionieren, und auf die Griffe klicken und ziehen, um die Größe zu ändern.

### Zeitsteuerung und Wiedergabe

Sowohl der Anzeige- als auch der Videoeditor zeigen unten auf der Arbeitsfläche ein Zeitleistenfenster an.

#### Anzeigen von Anzeigenvorlagen

In der Zeitleiste wird für jede Ebene auf der Arbeitsfläche eine Spur angezeigt. Sie erstreckt sich über den Zeitraum, in dem die Ebene sichtbar ist, basierend auf dem Timing der Ein- und Austritts-Animation. Ziehen Sie den Anfangs- oder Endpunkt einer Spur, um ihre Eintritts- oder Austrittszeit anzupassen, oder ziehen Sie eine Spur, um Ebenen neu anzuordnen. Klicken Sie auf das Lineal oder ziehen Sie den Abspielkopf, um zu einem bestimmten Zeitpunkt zu wechseln.

Die Zeitleisten-Symbolleiste enthält ein **[!UICONTROL Duration]** (0-60 Sekunden), **[!UICONTROL Play]**/**[!UICONTROL Pause]**, eine aktuelle Zeit-/Gesamtdauer-Anzeige, einen Schleifen-Umschalter, **[!UICONTROL Timeline Scale]** Zoom-Steuerelemente, eine **[!UICONTROL Fit View]**-Schaltfläche und einen Umschalter zum Reduzieren/Erweitern.

#### Video-Anzeigenvorlagen

In der Zeitleiste werden alle Video- und Audioclips in der Vorlage angezeigt. Verwenden Sie die Zeitleiste, um die zeitliche Anordnung der Clips zu überprüfen und Clips durch Ziehen ihrer Start- und Endgriffe zu trimmen. Sie können einen neuen Clip nicht direkt auf der Zeitleiste hinzufügen. Fügen Sie ihn stattdessen aus dem linken Bedienfeld oder der linken Arbeitsfläche hinzu, und er wird dann als Clip auf der Zeitleiste angezeigt.

### Ebenen verwalten

Im [!UICONTROL Layers] auf der rechten Seite der Arbeitsfläche werden alle Elemente in der Vorlage aufgelistet und Sie können ihre Reihenfolge, Sichtbarkeit und Eigenschaften verwalten. Klicken Sie bei Anzeigevorlagen in der Symbolleiste der Arbeitsfläche auf **[!UICONTROL Open Layers]** , um sie zu öffnen. Bei Videovorlagen ist das Bedienfeld standardmäßig geöffnet.

Klicken Sie auf eine beliebige Ebene, um das entsprechende Element auf der Arbeitsfläche auszuwählen.

**Registerkarten (nur Anzeigenvorlagen anzeigen)**

Anzeigevorlagen verfügen oben im [!UICONTROL Layers] über zwei Registerkarten:

* **[!UICONTROL Dynamic]** - Listet nur die Ebenen auf, die während der Anzeigengenerierung ausgetauscht werden können, z. B. Bilder und Text, die der KI-Agent ersetzen kann. Dies ist die Standardansicht zum Generieren von Anzeigenvarianten.
* **[!UICONTROL All]** - Zeigt die vollständige Ebenenhierarchie für die Vorlage an, einschließlich der strukturellen Container. Verwenden Sie diese Ansicht, um zu überprüfen oder neu zu organisieren, wie Elemente verschachtelt werden.

In Videovorlagen werden alle Ebenen in einer Liste ohne Registerkarten angezeigt.

**Aktionen pro Ebene**

Halten Sie den Cursor über eine Ebene, um die folgenden Aktionen anzuzeigen.

| Aktion | Beschreibung |
| --- | --- |
| ![Ebene umbenennen](/help/creative/assets/edit.png "Ebene umbenennen") **[!UICONTROL Rename layer]** | Ermöglicht die Eingabe eines neuen Ebenennamen im Bedienfeld. |
| ![Sperrschicht](/help/creative/assets/cs-icon-lock.png " Sperrschicht") **[!UICONTROL Lock layer]** / ![Sperrschicht](/help/creative/assets/cs-icon-unlock.png "Sperrschicht")**[!UICONTROL Unlock layer]** | Verhindert oder ermöglicht, dass die Ebene verschoben, bearbeitet oder neu angeordnet wird. |
| ![Ebene ausblenden](/help/creative/assets/cs-icon-hidden.png "Ebene ausblenden") **[!UICONTROL Hide layer]** / ![Ebene anzeigen](/help/creative/assets/cs-icon-visible.png "Ebene anzeigen")**[!UICONTROL Show layer]** | Blendet die Ebene auf der Arbeitsfläche aus oder ein. Ausgeblendete Ebenen werden in der Vorlage beibehalten, werden jedoch nicht angezeigt, wenn die Vorlage gerendert wird. |
| ![Ziehen zur Neuanordnung](/help/creative/assets/cs-icon-drag.png "Ziehen zur Neuanordnung") Ziehen zur Neuanordnung | (Nur Anzeigenvorlagen anzeigen) Ziehen Sie das Symbol zur Neuanordnung, um die Position des Layers in der Stapelreihenfolge zu ändern. Die Ebene muss entsperrt sein, um sie neu anzuordnen. |

**Panel-Fußzeile**

| Aktion | Beschreibung |
| --- | --- |
| ![Ausgewählte Ebene duplizieren](/help/creative/assets/cs-icon-duplicate.png "Ausgewählte Ebene duplizieren") **[!UICONTROL Duplicate selected layer]** | Erstellt eine Kopie der ausgewählten Ebene. |
| ![Ausgewählte Ebene löschen](/help/creative/assets/cs-icon-delete.png "Ausgewählte Ebene löschen") **[!UICONTROL Delete selected layer]** | Löscht die ausgewählte Ebene. |
| **[!UICONTROL Group selected layers]** (nur Videovorlagen) | Gruppiert zwei oder mehr ausgewählte Ebenen zu einer Gruppe. Wird nur angezeigt, wenn zwei oder mehr Ebenen ausgewählt sind. Sie können die Gruppierung von Ebenen aufheben oder einzelne Ebenen mithilfe der Steuerelemente in der Gruppenzeile aus der Gruppe entfernen. |

<!--

These are all saved with the template, but they aren't what you see, as-is, in the template settings per se. Rethink if I should include this, and how to frame it:

## Template settings {#template-settings}

### Display ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Type]** | (Required) The HTML5 template type: **[!UICONTROL Static HTML5]** or **[!UICONTROL Dynamic HTML]**. |
| **[!UICONTROL Size]** | (Required) The ad dimensions. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **[!UICONTROL Tags]** | (Optional) One or more labels. Click **[!UICONTROL Add More]** to add additional tags. |
| **ZIP file** | The HTML5 creative ZIP file. For **[!UICONTROL Dynamic HTML]** templates, also upload the template data file (TDF). |

### Video ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **ZIP file** | The video ad template ZIP file. |

-->

>[!MORELIKETHIS]
>
>* [Über Creative Studio in Advertising Creative](creative-studio-about.md)
>* [Verwalten von Assets in Creative Studio](creative-studio-manage-assets.md)
>* [Verwalten von Standardanzeigen in Creative Studio](creative-studio-manage-standard-ads.md)
>* [Verwalten von dynamischen Kreativen in Creative Studio](creative-studio-manage-dynamic-ads.md)
