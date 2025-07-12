---
title: Exportieren und Implementieren eines Anzeigen-Erlebnis-Tags für ein Live-Erlebnis
description: Erfahren Sie, wie Sie ein Anzeigen-Erlebnis-Tag exportieren und optional in eine Advertising DSP-Kampagne hochladen.
feature: Creative Experiences
exl-id: 4ae05142-8319-4329-96d7-f87d77f02745
source-git-commit: 95e17af996cb3171667ef3cd5ac662f08112691b
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# Exportieren und Implementieren eines Anzeigen-Erlebnis-Tags für ein Live-Erlebnis

*Geschlossene Beta-Version*

Sobald ein Anzeigen-Tag für eine bestimmte Kreativgröße für ein [Live](experience-about.md#experience-statuses)-Erlebnis verfügbar ist, können Sie das Tag in den Formaten JavaScript und iframe zur Implementierung auf Advertising DSP oder anderen DSPs generieren und kopieren. Die Tags für DSP enthalten alle für DSP erforderlichen Makros.

Werbetreibende mit Advertising DSP können optional Tags direkt als Anzeigen mit dem Werbetyp „Standardanzeige“ oder „Universelles Video“ in eine Advertising DSP-Kampagne hochladen.

>[!NOTE]
>
>* Beim Erstellen eines Erlebnisses mit Entscheidungsbaum-Targeting erstellt [!DNL Creative] automatisch ein Anzeigen-Tag für jede anwendbare Kreativgröße.
>* Wenn Sie ein Erlebnis ohne Targeting mit einem Entscheidungsbaum erstellen, müssen Sie für jede [ Kreativgröße ](experience-tag-create-manually.md)manuell ein Anzeigen-Tag erstellen).
>* Experience Tags sind dynamisch. Sie müssen die Tags nicht aktualisieren, wenn Sie ein Erlebnis bearbeiten.
>* Stellen Sie sicher, dass die Kampagnen, in denen Sie ein Anzeigen-Erlebnis implementieren, ein mit dem Erlebnis kompatibles Targeting enthalten. Das hierarchische Targeting-Verhalten kann je nach DSP variieren. In Advertising DSP wird das Targeting auf Anzeigenebene zusätzlich zum Targeting auf Platzierungsebene (nicht anstelle des Targeting) angewendet.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Führen Sie einen der folgenden Schritte aus:<!-- I see multiselect, but it's not actually working for me as of 2/3 so I don't know how exporting multiple tags works.-->

   * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Erlebnisnamen und dann auf **[!UICONTROL Tag Manager]**.

   * Halten Sie in der Tabellenansicht den Cursor über der Zeile, klicken Sie auf **[!UICONTROL More]** und dann auf **[!UICONTROL Tag Manager]**.

1. Halten Sie den Cursor über die Zeile für das entsprechende Anzeigen-Tag und klicken Sie entweder ![Anzeigen-Tags ](/help/creative/assets/export.png "Anzeigen-Tags exportieren") **[!UICONTROL Export ad tags]** oder **[!UICONTROL ... More] > **[!UICONTROL Export ad tags]**.

>[!NOTE]
>
>Warten Sie bei Standard-Videoanzeigen, bis die Spalte [!UICONTROL Tag Status] &quot;[!UICONTROL Ready]&quot; anzeigt. Dies bedeutet, dass alle Videos im Erlebnis transcodiert wurden. Alle Video-Kreativen werden automatisch von DSP transkodiert, aber Sie können optional [publisher-spezifische Transkodierung](experience-tag-video-transcoding.md) auf jedes Video- und Erlebnis-Tag anwenden.

<!-- Tag Manager has only a list view, but no card view, as of 2/2. -->

1. (Optional) Geben Sie auf der Registerkarte [!UICONTROL Macros] bis zu fünf benutzerdefinierte Makros an, die in das Tag aufgenommen werden sollen. Für jedes einzuschließende Makro:

   1. Aktivieren Sie ein Kontrollkästchen.<!-- Explain more -->

   1. Benutzerdefiniertes Makro eingeben.<!-- Explain more -->

1. Klicken Sie oben rechts auf **[!UICONTROL Next]** oder im Menü links auf **[!UICONTROL Generate ad tags]**.

1. Wählen Sie den Tag-Typ aus: ** *JavaScript<!-- sic -->* ** oder ** *IFRAME* ** <!-- sic -->.

1. Wählen Sie in der Liste [!UICONTROL Destinations] aus, wo Sie Anzeigen für das Erlebnis erstellen möchten.

   * *Generisch:* Für Anzeigen, die Sie in anderen DSPs erstellen werden. **Hinweis:** Sie müssen ggf. [zusätzliche Makros](/help/creative/creative-macros.md) manuell einbeziehen.

   * *Adobe AdCloud:* Für Anzeigen, die Sie in Advertising DSP erstellen werden.

   * *Google CM360:* Für Anzeigen, die Sie in [!DNL Google Campaign Manager 360] erstellen werden. **Hinweis:** Sie müssen ggf. [zusätzliche Makros](/help/creative/creative-macros.md) manuell einbeziehen.

1. Klicken Sie auf **[!UICONTROL Generate tags]**.

1. Kopieren Sie die Tags oder laden Sie sie herunter:

   * Um ein Tag für eine einzelne Anzeigengröße zu kopieren, erweitern Sie die Tag-Zeile, halten Sie den Cursor über der Zeile und klicken Sie dann auf ![Kopieren](/help/creative/assets/copy.png "Kopieren") **[!UICONTROL Copy]**.<!-- why diff than "Copy to clipboard icon used to copy macros for creatives? -->

   * Um alle generierten Tags als Datei zum standardmäßigen Download-Speicherort Ihres Browsers herunterzuladen, klicken Sie auf ![Tags herunterladen](/help/creative/assets/download.png "Tags herunterladen").

   Sie können die Datei in einem Texteditor öffnen, um jedes Tag zu kopieren. Bei JavaScript-Tags wird das Tag in `<script></script>`- und `<noscript></noscript>`Tags eingeschlossen. Bei iframe-Tags wird das Tag in `<iframe></iframe>` Tags eingeschlossen.

1. Implementieren Sie die Tags für die entsprechende DSP:

   * Geben Sie bei anderen DSPs als Advertising DSP die Tags an die Person weiter, die die Anzeigen in der DSP erstellen wird.

   * Für Advertising DSP:

      1. Klicken Sie oben rechts auf **[!UICONTROL Next]** oder im Menü links auf **[!UICONTROL DSP link]**.

      1. Wählen Sie die Kampagne aus, in die Sie das Anzeigen-Tag hochladen möchten.

      1. Klicken Sie auf **[!UICONTROL Assign Tags]**.

         DSP öffnet die [!UICONTROL Ads] für die ausgewählte Kampagne.

      1. Überprüfen Sie in der [!UICONTROL Create ads] die Anzeigen-Tags, wählen Sie jedes Tag aus, für das Sie eine Anzeige erstellen möchten, und klicken Sie dann auf **[!UICONTROL Create]**.

<!-- no way to get back to the Creative Tag Manager -- you have to click back through the main menu -->

<!-- Add this info, with descriptions:

## Ad tag formats

### JavaScript

### Iframe

-->

>[!MORELIKETHIS]
>
>* [Manuelles Erstellen eines Anzeigen-Tags für eine entsprechende Kreativgröße](experience-tag-create-manually.md)
>* [Zuweisen von Kreativen zu einem Anzeigen-Tag für Erlebnisse ohne Targeting](experience-tag-assign-creatives.md)
>* [Umbenennen eines Anzeigen-Tags](experience-tag-rename.md)
>* [Anpassen der Transkodierungsoptionen für ein Video- und Erlebnis-Tag](experience-tag-video-transcoding.md)
