---
title: Erlebnisvorschau
description: Erfahren Sie, wie Sie eine Vorschau der Kreativen in einem Werbeerlebnis anzeigen.
feature: Creative Experiences
exl-id: 2ac8f580-7d3d-4de6-ba14-5d72b30188d7
source-git-commit: ae226015d1a8a3da4ea2a0db0db31858e750b9a7
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Erlebnisvorschau

*Geschlossene Beta-Version*

Sie können eine Vorschau der Kreativen mit einer bestimmten Anzeigengröße anzeigen, die Target-Betrachterinnen und -Betrachtern für ein Erlebnis angezeigt wird, einschließlich aller Hyperlinks. Für Erlebnisse mit Entscheidungsbaum-Targeting können Sie eine Vorschau eines einzelnen Kreativen, der Kreativen für eine bestimmte Verzweigung (Zieltyp) oder aller Kreativen im Erlebnis anzeigen. Für Erlebnisse ohne Entscheidungsbaum-Targeting können Sie eine Vorschau eines einzelnen Kreativen anzeigen. <!-- verify -->

* Wenn Sie eine Vorschau aller Kreativen für das Erlebnis oder eine bestimmte Verzweigung anzeigen, werden alle entsprechenden Kreativen angezeigt.

* Wenn Sie eine Vorschau eines einzelnen Kreativen anzeigen und mehrere Kreative den Kriterien entsprechen, basiert das Kreativ, das Sie jedes Mal sehen, wenn Sie die Vorschau aktualisieren, auf den Einstellungen für die Anzeigenrotation für das Erlebnis:

   * Für die algorithmische Anzeigenrotation wird der Kreative basierend auf dem Optimierungsziel ausgewählt.

   * Bei einer gewichteten Anzeigenrotation wird das Kreativ jedes Mal anhand der angegebenen Gewichtung ausgewählt (z. B. eine 80%ige Chance, dass Creative A angezeigt wird, und eine 20%ige Chance, dass Creative B angezeigt wird).

   * Für die geplante Anzeigenrotation wird der erste Kreative im Zeitplan angezeigt. Sie können die Vorschau weiter aktualisieren, um die Sequenz zu durchlaufen.<!-- Refresh isn't there as of 2/3 -->

## Kreative in einem Erlebnis in der Vorschau anzeigen mit Targeting in einem Entscheidungsbaum

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Optional) [Passen Sie die Ansicht an](/help/creative/introduction/customize-data-views.md) um bestimmte Erlebnisse einzuschließen.

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Erlebnisnamen und dann auf **[!UICONTROL Preview]**.

   * Halten Sie in der Tabellenansicht den Cursor über der Zeile, klicken Sie auf **[!UICONTROL More]** und dann auf **[!UICONTROL Preview]**.

1. Kreative auswählen, die in der Vorschau angezeigt werden sollen:

   * So zeigen Sie eine Vorschau eines einzelnen Kreativen an:

      1. Klicken Sie auf **[!UICONTROL Creative]**.

      1. Wählen Sie die Anzeigengröße aus.

      1. Wählen Sie im Abschnitt [!UICONTROL Decision Tree Targeting] die kreative Zielgruppe aus.

   * So erstellen Sie eine Vorschau der Kreativen für eine bestimmte Verzweigung:

      1. Klicken Sie auf **[!UICONTROL Particular branch]**.

      1. Wählen Sie die Anzeigengröße aus.

     <!-- I don't see this as of 2/3:
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

      1. Wählen Sie die kreative Zielgruppe aus.

   * Um eine Vorschau aller Kreativen im Erlebnis anzuzeigen, klicken Sie auf **[!UICONTROL Entire Tree]**.

     <!-- I don't see this as of 2/3:
     1. Click **[!UICONTROL Entire Tree]**.
     1. Select the ad size.
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

1. (Optional) Um den Namen des Kreativen, den Kreativtyp und die Größe, die Landingpage-URLs oder Klick-URLs und flexible Attribute unter jedem Kreativen einzuschließen, wählen Sie **[!UICONTROL Display Creative Metadata]**.

1. Klicken Sie auf **[!UICONTROL Preview]**.

1. (Nur Vorschau nach Kreativen; optional) Klicken Sie in der Symbolleiste auf **[!UICONTROL Refresh]**, um je nach den Einstellungen für die Anzeigenrotation eine Vorschau aller weiteren Kreativen anzuzeigen.<!-- I don't see this as of 2/3 -->

1. (Optional) So kopieren Sie eine Demo-URL des Erlebnisses, das Sie ohne Anmeldung für [!DNL Creative] freigeben können:

   1. Klicken Sie oben rechts in der Vorschau auf ![Freigeben](/help/creative/assets/share.png "Freigeben").

   1. Klicken Sie im Dialogfeld [!UICONTROL Share Demo URL] auf **[!UICONTROL Copy]** , um die URL in die Zwischenablage zu kopieren, sodass Sie sie für andere freigeben können.

## Vorschau von Kreativen in einem Erlebnis ohne Targeting mit Entscheidungsbaum

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Optional) [Passen Sie die Ansicht an](/help/creative/introduction/customize-data-views.md) um bestimmte Erlebnisse einzuschließen.

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Erlebnisnamen und dann auf **[!UICONTROL Preview]**.

   * Halten Sie in der Tabellenansicht den Cursor über der Zeile, klicken Sie auf **[!UICONTROL More]** und dann auf **[!UICONTROL Preview]**.

1. (Optional) Begrenzen Sie die Liste der Kreativen, indem Sie eine bestimmte Kreativgröße auswählen.

   Standardmäßig werden Kreative aller Größen aufgelistet.

1. Klicken Sie auf den Namen eines Anzeigen-Tags, um die Zeile zu erweitern und eine Vorschau der Kreativen anzuzeigen.

1. (Optional) Um auf die Landingpage für einen Kreativen zu gelangen, klicken Sie auf den Kreativen.

   <!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Optional) So kopieren Sie eine Demo-URL des Erlebnisses, das Sie ohne Anmeldung für [!DNL Creative] freigeben können:

   1. Klicken Sie oben rechts in der Vorschau auf ![Freigeben](/help/creative/assets/share.png "Freigeben").

   1. Klicken Sie im Dialogfeld [!UICONTROL Share Demo URL] auf **[!UICONTROL Copy]** , um die URL in die Zwischenablage zu kopieren, sodass Sie sie für andere freigeben können.

>[!MORELIKETHIS]
>
>* [Erstellen eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-create-targeting.md)
>* [Erstellen eines Erlebnisses ohne Targeting mit einem Entscheidungsbaum](/help/creative/experiences/experience-create-no-targeting.md)
