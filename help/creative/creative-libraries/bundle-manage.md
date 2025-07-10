---
title: Verwalten von kreativen Bundles
description: Informationen zu xxxx.
feature: Creative Bundles
exl-id: a9ed4e8f-db93-46d5-9231-2b3bb0aa072a
source-git-commit: 4b780760e5a7a0c3d370054fce8b1c15fbc6802d
workflow-type: tm+mt
source-wordcount: '1462'
ht-degree: 0%

---

# Verwalten von kreativen Bundles

*Geschlossene Beta-Version*

<!--
**I'll probably split this up into multiple pages since the creative-related topics are separate**
-->

Bundles sind Gruppen von Kreativen, die Sie einem Erlebnis als eine Einheit hinzufügen können. Nachdem Sie einen Bundle-Container erstellt haben, können Sie Kreative an das Bundle anhängen. Standard-Display-Bundles können nur Standard-Display-Anzeigen enthalten, Standard-Video-Bundles können nur Standard-Video-Anzeigen enthalten und dynamische Display-Bundles können nur dynamische Display-Anzeigen enthalten. Sie können die Landingpages, Impression-Tracking-Tags und Klick-Tracking-Tags für alle Kreativen in einem Bundle, das einem Erlebnis aus der Erlebnis-Entscheidungsstruktur zugewiesen ist, überschreiben, ohne die Basis-Kreativen zu beeinflussen.

[!DNL Creative] rotiert durch die Kreativen im Bundle, wie für jedes Erlebnis angegeben, dem das Bundle zugewiesen ist. Optional können Sie [!DNL Creative] erlauben, die Anzeigenelemente für jedes Erlebnis auf der Grundlage der Leistung mithilfe der algorithmischen Anzeigenrotation zu optimieren, die von Adobe Sensei unterstützt wird.

Um die Optimierung von Anzeigenelementen über Bundles hinweg in einem Anzeigenerlebnis zu ermöglichen, kann jedes Bundle nur eine der \[Creative Size + Language\]-Kombinationen enthalten. Beispiel: Wenn ein Bundle eine 250x250-Kreative mit der Standardsprache „Französisch“ enthält, können Sie keine zweite 250x250-Kreative mit der Standardsprache „Französisch“ hinzufügen. Wenn Sie mehrere Kreative derselben Größe in derselben Sprache haben, fügen Sie sie separat zum -Erlebnis hinzu.

Kreative, die an Bundles angehängt sind, sind weiterhin als individuelle Kreative verfügbar. Sie können ein einzelnes Kreativ zu mehreren Bundles hinzufügen. Wenn Sie Einstellungen für ein Kreativ bearbeiten, das an ein Bundle angehängt ist, werden die Änderungen an das Bundle weitergegeben. Allerdings werden für das Erlebnis immer benutzerdefinierte Landingpages, Impression-Tracking-Tags und Klick-Tracking-Tags verwendet, die für die Kreativen in einem Erlebnis konfiguriert sind.

<!-- multiselect only to duplicate and delete -->

## Bundle für eine Kreativbibliothek erstellen

Sie können ein Kreativ-Asset an mehrere Bundles anhängen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Bundles]** .

1. Klicken Sie oben rechts auf **[!UICONTROL Create]** > **[!UICONTROL Bundles]** > **[!UICONTROL Bundle]**.

1. Geben Sie eine eindeutige **[!UICONTROL Bundle Name]** ein und **[!UICONTROL Bundle Type]Sie Folgendes** *Standardanzeige* (für Kreative von Standardbildschirmen), *Dynamisches Display* (für Kreative von dynamischen Bildschirmen), *Standardvideo* (für Kreative von Standardvideos).

1. Klicken Sie auf **[!UICONTROL Create]**.

## Auflisten der Kreativen in einem Paket

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Passen Sie die Ansicht an](/help/creative/introduction/customize-data-views.md) um bestimmte Bibliotheken einzuschließen.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Bundles]** .

1. Klicken Sie auf die Bundle-Karte oder -Zeile, um alle Kreativen im Bundle anzuzeigen.

## Bundles duplizieren

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Passen Sie die Ansicht an](/help/creative/introduction/customize-data-views.md) um bestimmte Bibliotheken einzuschließen.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Bundles]** .

1. Zu duplizierende Pakete auswählen:

   * So duplizieren Sie ein einzelnes Bundle:

      * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Bundle-Namen und dann auf **[!UICONTROL Duplicate]**.

      * Halten Sie in der Tabellenansicht den Cursor über der Zeile und klicken Sie auf **[!UICONTROL Duplicate]**.

   * Um ein oder mehrere Bundles zu duplizieren, aktivieren Sie das Kontrollkästchen für jedes Bundle, das Sie duplizieren möchten. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Duplicate].**

     Um alle Zeilen auszuwählen, aktivieren Sie das Kontrollkästchen Global oben links.

   Die neuen Bundles erhalten den Namen `<original name> (copy) # 1` (oder die nächste Nummer in der Sequenz). Wenn Sie beispielsweise zwei Duplikate von „Testpaket“ erstellen, werden die Duplikate „Testpaket (Kopie) # 1“ und „Testpaket (Kopie) # 2“ genannt.

## Bundle-Namen bearbeiten

Änderungen an einem Bundle-Namen werden auf alle zugehörigen Erlebnisse übertragen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Bundles]** .

1. Bundle auswählen:

   * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Bibliotheksnamen und dann auf **[!UICONTROL Edit]**.

   * Halten Sie in der Tabellenansicht den Cursor über der Zeile und klicken Sie auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie die **[!UICONTROL Bundle Name]**.

   Der [!UICONTROL Bundle Name] muss eindeutig sein.

1. Klicken Sie auf **[!UICONTROL Update]**.<!-- inconsistent with "Edit" for creative libraries and creatives -->

## Kreative an Bundle anhängen

Sie können bestehende Kreative von Standardbildschirmen an ein Bundle mit Standardbildschirmen, Kreative von Standardvideos an Standard-Videopakete und Kreative von dynamischen Anzeigen an ein dynamisches Bundle anhängen. Wenn Sie ein Kreativ-Asset an ein Bundle anhängen, ist das Kreativ-Asset in allen Erlebnissen verfügbar, denen das Bundle zugewiesen ist. Jedes Bundle kann nur eine der \[Creative Size + Language\]-Kombinationen enthalten.

>[!NOTE]
>
>Sie können auch [Kreative an Pakete aus den Ansichten Standardanzeigen und Dynamische Anzeigen anhängen](creative-attach-detach-bundles.md).

### Kreative von der Bundles-Liste an ein Bundle anhängen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Passen Sie die Ansicht an](/help/creative/introduction/customize-data-views.md) um bestimmte Bibliotheken einzuschließen.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Bundles]** .

1. Bundle auswählen:

   * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Bundle-Namen und dann auf **[!UICONTROL Attach Creatives]**.

   * Halten Sie in der Tabellenansicht den Cursor über der Zeile und klicken Sie auf **[!UICONTROL Attach Creatives]**.

   Alle Kreativen, die für den Bundle-Typ infrage kommen, werden im rechten Rahmen aufgelistet. Kreative, die bereits mit dem Bundle verbunden sind, werden aufgelistet, können jedoch nicht ausgewählt werden.

1. (Optional) Wechseln Sie zwischen der Standard-Tabellenansicht und einer Kartenansicht der verfügbaren Bundles, indem Sie auf ![Kartenansicht](/help/creative/assets/card-view-button.png "Kartenansicht") klicken, um die Kartenansicht zu öffnen, oder ![Tabellen-/Listenansicht](/help/creative/assets/table-view-button.png "Tabellenansicht"), um zur Tabellenansicht zurückzukehren.

1. Aktivieren Sie im rechten Rahmen das Kontrollkästchen neben den einzelnen Kreativen, die an das Bundle angehängt werden sollen, und klicken Sie dann auf **[!UICONTROL Attach Creative to Bundle]**.

### Kreative aus der Kreativliste des Bundles an ein Bundle anhängen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Passen Sie die Ansicht an](/help/creative/introduction/customize-data-views.md) um bestimmte Bibliotheken einzuschließen.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Bundles]** .

1. Klicken Sie auf die Bundle-Karte oder -Zeile, um alle Kreativen im Bundle anzuzeigen.

1. Klicken Sie oben rechts auf **[!UICONTROL Attach Creatives]**.

1. Aktivieren Sie im rechten Bedienfeld das Kontrollkästchen für jeden Kreativen, den Sie anhängen möchten.

1. Klicken Sie auf **[!UICONTROL Attach Creatives to Bundle]**.

## Trennen von Kreativen von einem Bundle {#bundle-detach-creatives}

Wenn Sie ein Kreativ aus einem Bundle entfernen, wird die Verknüpfung zwischen den beiden aufgehoben, sodass das Kreativ-Tool nicht mehr für Erlebnisse verwendet wird, die auf das Bundle abzielen.

Wenn Sie eine Kreative aus dem Bundle entfernen, wird die Kreative nicht aus der Registerkarte „Kreative“ in Ihrer Kreativbibliothek gelöscht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Passen Sie die Ansicht an](/help/creative/introduction/customize-data-views.md) um bestimmte Bibliotheken einzuschließen.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Bundles]** .

1. Klicken Sie auf die Bundle-Karte oder -Zeile, um alle Kreativen im Bundle anzuzeigen.

1. Wählen Sie die Kreativen aus, die vom Bundle getrennt werden sollen:

   * So trennen Sie einen einzelnen Kreativen:

      * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Namen der Kreativen, und klicken Sie dann auf **[!UICONTROL Detach]**.

      * Halten Sie in der Tabellenansicht den Cursor über der Zeile und klicken Sie auf **[!UICONTROL Detach]**.

   * Um einen oder mehrere Kreative zu trennen, aktivieren Sie das Kontrollkästchen für jeden Kreativen, den Sie trennen möchten. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Detach]**.

     Um alle Zeilen auszuwählen, aktivieren Sie das Kontrollkästchen Global oben links.

## Vorschau eines einzelnen Kreativs in einem Bundle

Sie können ein Kreativ, einschließlich Hyperlinks, so in der Vorschau anzeigen, wie es den Betrachtern angezeigt wird.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Passen Sie die Ansicht an](/help/creative/introduction/customize-data-views.md) um bestimmte Bibliotheken einzuschließen.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Bundles]** .

1. Klicken Sie auf die Bundle-Karte oder -Zeile, um alle Kreativen im Bundle anzuzeigen.

1. Wählen Sie das Kreative aus:

   * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Namen der Kreativen, und klicken Sie dann auf **[!UICONTROL Preview]**.

   * Halten Sie in der Tabellenansicht den Cursor über der Zeile und klicken Sie auf **[!UICONTROL Preview]**.

1. (Optional) Um die Größe des Bildes auf dem Bildschirm zu ändern, wählen Sie eine Option in der **[!UICONTROL Zoom]**-Liste aus, die 10 % bis 100 % der Bildgröße beträgt.

<!-- Not there as of 1/22/24:  1. (Flexible HTML5 creatives; optional) To show all frames for the creative, select **Show frames**. -->

1. (Optional) Um die Landingpage für den Kreativen zu öffnen, klicken Sie auf den Kreativen.

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Optional) Um das Kreativ-Asset herunterzuladen, klicken Sie auf ![Download](/help/creative/assets/download.png "Download").

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

## Vorschau aller Kreativen in einem Bundle

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Bundles]** .

1. Bundle auswählen:

   * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Bundle-Namen und dann auf **[!UICONTROL Preview]**.

   * Halten Sie in der Tabellenansicht den Cursor über der Zeile und klicken Sie auf **[!UICONTROL Preview]**.

1. (Optional) Um die Kreativen nach Sprache zu filtern, wählen Sie eine Option in der **[!UICONTROL Language]** Liste aus und klicken Sie dann oben rechts in der Vorschau auf **[!UICONTROL Preview]** .

1. (Optional) Um die Kreativen nach Größe zu filtern, wählen Sie eine Option in der **[!UICONTROL Size]** Liste aus und klicken Sie dann oben rechts in der Vorschau auf **[!UICONTROL Preview]** .

1. (Optional) Um die Größe der Bilder auf dem Bildschirm zu ändern, wählen Sie eine Option in der **[!UICONTROL Zoom]**-Liste aus, die 10 % bis 100 % der Bildgröße beträgt.

1. (Optional) Um die Landingpage für einen Kreativen zu öffnen, klicken Sie auf den Kreativen.

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Optional) So geben Sie eine Demo-URL frei, damit andere Personen ohne Anmeldung bei [!DNL Creative] eine Vorschau der Kreativen anzeigen können:

   1. Klicken ![ oben rechts in ](/help/creative/assets/share.png " Vorschau auf ")Freigeben/Freigeben“.

   1. Klicken Sie im Dialogfeld [!UICONTROL Share Demo URL] auf **[!UICONTROL Copy]** , um die URL in die Zwischenablage zu kopieren, sodass Sie sie für andere freigeben können.

<!-- Not there as of 1/22/25:

## Edit the landing page and tracking tags for the creatives in a standard creative bundle

*Standard creative bundles only*

[Verify and edit all this, including the command names and where they're available. This is supposed to be a single and bulk action from within the right frame when you've open bundle details for a single bundle -- not from the Bundles table view.]

This procedure customizes the landing page, impression-tracking tags, and click-tracking tags for the creatives only within the context of the bundle. It doesn't change the settings for the base creative in [!UICONTROL Creative Libraries].

The custom URL and tags are applied to a creative when the bundle is assigned to an experience and the creative is served for the experience.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Click the bundle name.

1. In the right pane, XXXXXXXXXXXX.

1. 

1. Edit any of the following settings: **[!UICONTROL Landing Page]**, **[!UICONTROL Click Tags]**, **[!UICONTROL Impression Tags]**.[Verify, and is can you do this for only one creative or is multiselect available?]

1.

 -->

## Bundles löschen

Sie können Bundles löschen, die keinem Live-Erlebnis [ sind](/help/creative/experiences/experience-about.md#experience-statuses-experience-statuses). Wenn ein Bundle einem Live-Erlebnis zugewiesen ist, [ Sie das Bundle aus der Entscheidungsstruktur ](/help/creative/experiences/experience-target-node-delete.md), bevor Sie fortfahren.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Passen Sie die Ansicht an](/help/creative/introduction/customize-data-views.md) um bestimmte Bibliotheken einzuschließen.

1. Klicken Sie auf den Bibliotheksnamen.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Bundles]** .

1. Zu löschende Pakete auswählen:

   * So löschen Sie ein einzelnes Bundle:

      * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Bundle-Namen und dann auf **[!UICONTROL Delete]**.

      * Halten Sie in der Tabellenansicht den Cursor über der Zeile und klicken Sie auf **[!UICONTROL Delete]**.

   * Um ein oder mehrere Bundles zu löschen, aktivieren Sie das Kontrollkästchen für jedes Bundle, das Sie löschen möchten. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Delete].**

     Um alle Zeilen auszuwählen, aktivieren Sie das Kontrollkästchen Global oben links.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete].**

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Zuweisen und Aufheben der Zuweisung von kreativen Bundles zu einem endgültigen Knoten in einem Erlebnis](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Vorschau eines Kreativen anzeigen](/help/creative/creative-libraries/creative-preview.md)
>* [Standard-Kreative zu einer Kreativbibliothek hinzufügen](/help/creative/creative-libraries/creative-add-standard.md)
>* [Verwalten von Kreativbibliotheken](/help/creative/creative-libraries/creative-library-manage.md)
>* [Über Ihre Kreativbibliotheken](/help/creative/creative-libraries/creative-libraries-about.md)
