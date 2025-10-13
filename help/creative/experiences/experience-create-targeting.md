---
title: Erstellen eines Erlebnisses mit Targeting mit Entscheidungsbäumen
description: Erfahren Sie, wie Sie mithilfe eines Entscheidungsbaums ein zielgerichtetes Anzeigen-Erlebnis erstellen.
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
source-git-commit: 7031347edb4491a91d622c0357ea2d3fb63f0a8a
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# Erstellen eines Erlebnisses mit Targeting mit Entscheidungsbäumen

Erstellen Sie ein zielgerichtetes Anzeigen-Erlebnis mithilfe eines Entscheidungsbaums. Jedes Erlebnis verwendet Anzeigen aus einer einzigen Kreativbibliothek.

>[!NOTE]
>
>* Nachdem Sie ein zielgerichtetes Erlebnis erstellt haben, können Sie es später nicht mehr in ein nicht zielgerichtetes Erlebnis ändern, das einen anderen Workflow verwendet.
>* Stellen Sie sicher, dass Ihre Anzeigenerlebnisse ein Targeting enthalten, das mit den Kampagnen kompatibel ist, in denen Sie es implementieren werden. Das hierarchische Targeting-Verhalten kann je nach DSP variieren. Wenn Sie ein Anzeigen-Erlebnis-Tag in Advertising DSP hochladen und es an eine Platzierung anhängen, wird das Targeting auf Anzeigenebene über dem Targeting auf Platzierungsebene (nicht anstelle des Targetings auf Platzierungsebene) angewendet. Wenn sich eine Platzierung beispielsweise an Benutzende in Australien und eine Anzeige an Benutzende in Japan richtet, zielt die Anzeige auf den Zweig „Alle anderen“ ab.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Klicken Sie auf **[!UICONTROL Create New Experience]**.

1. Geben Sie die [allgemeinen Erlebniseinstellungen](experience-settings-targeting.md) ein.

1. Klicken Sie auf **[!UICONTROL Create]**.

1. Gehen Sie in der Entscheidungsstruktur wie folgt vor:

   1. (Optional) Ändern Sie die Anzeigeeinstellungen für den Entscheidungsbaum.

      Ihre Einstellungen werden gespeichert, bis Sie sich abmelden.

      * Vergrößern oder verkleinern Sie die Ansicht, indem Sie den Schieberegler bewegen.

      * Wechseln Sie zwischen der Anzeige einer vertikalen Liste und einer horizontalen Liste, indem Sie auf ![Als vertikale Baumstruktur anzeigen](/help/creative/assets/tree-vertical.png "Als vertikale Baumstruktur anzeigen") bzw. ![Als horizontalen Baum anzeigen](/help/creative/assets/tree-horizontal.png "Als horizontalen Baum anzeigen") klicken.

   1. (Optional) Richten Sie die Anzeigenziele und die entsprechenden Kreativen auf eine der folgenden Arten ein:

      * Zielgruppen:

         * [Fügen Sie einen Zielknoten zur endgültigen Ebene hinzu](experience-target-node-add-final.md).

         * [Fügen Sie einen Zielknoten zwischen Knoten ein](experience-target-node-add-inner.md).

         * [Fügen Sie zwischen Knoten einen gleichrangigen Zielknoten hinzu](experience-target-node-add-sibling.md).

         * [Kopieren Sie untergeordnete Knoten und Kreative auf derselben Ebene in einen anderen Knoten](experience-target-node-copy.md).

      * Creative-Bundles:

         * [Zuweisung und Aufhebung der Zuweisung von Kreativen zu einem endgültigen Knoten](experience-assign-creative-bundles.md).

           Wenn Sie nicht jedem endgültigen Knoten mindestens ein Bundle zuweisen, können Sie beim Speichern des Erlebnisses die standardmäßigen Kreativen für jeden nicht zugewiesenen Knoten verwenden. Um ein Erlebnis zu veröffentlichen, müssen Sie für jeden endgültigen Knoten entweder Bundles zuweisen oder die standardmäßigen Kreativen verwenden.

         * [Passen Sie die Tracking-URLs für Kreative in den zugewiesenen Bundles &#x200B;](experience-tracking-urls-targeting.md).

         * [Passen Sie die kreative Optimierung und &#x200B;](experience-optimization-scheduling-targeting.md) für die zugewiesenen Bundles an.

1. (Optional) Wechseln zwischen Entscheidungsbaum und allgemeinen Einstellungen:

   * Um die allgemeinen Einstellungen im Entscheidungsbaum zu öffnen, klicken Sie oben rechts auf **[!UICONTROL Experience Form]** .

   * Um den Entscheidungsbaum über die allgemeinen Einstellungen zu öffnen, klicken Sie oben rechts auf **[!UICONTROL Decision Tree]** .

1. Klicken Sie auf **[!UICONTROL Save]**, und führen Sie dann folgende Schritte aus.

   * (Wenn jeder Knoten auf der untersten Ebene mindestens ein Kreativ-Bundle enthält) Klicken Sie auf **[!UICONTROL OK]**.

   * (Wenn jeder Knoten auf der untersten Ebene nicht mindestens ein kreatives Bundle enthält) Führen Sie einen der folgenden Schritte aus:

      * Um das Erlebnis ohne alle erforderlichen kreativen Bundles zu speichern, klicken Sie auf **[!UICONTROL Save as Draft]**.

        Sie können kein Anzeigen-Tag für ein Erlebnis [Entwurf](experience-about.md#experience-statuses) erstellen.

      * Um jedem Ziel, dem noch kein Kreativ-Bundle zugewiesen wurde, das Standardkreativ-Paket zuzuweisen, klicken Sie auf **[!UICONTROL Assign Default Creatives]**. Nachdem Sie die aktualisierte Baumstruktur mit den standardmäßig zugewiesenen Kreativen überprüft haben, klicken Sie auf **[!UICONTROL Save]** und **[!UICONTROL OK]**.

      * Um mit der Bearbeitung des Entscheidungsbaums fortzufahren, klicken Sie auf **[!UICONTROL Continue Edit]**.

Wenn das Erlebnis live ist, erstellt [!DNL Creative] automatisch ein Anzeigen-Tag für jede entsprechende kreative Größe oder Videodauer. Anschließend können Sie [ein Anzeigen-Tag exportieren und in einer DSP implementieren](/help/creative/experiences/experience-tag-export.md).

Für Videowerberlebnisse werden Videokreative von Adobe Advertising DSP automatisch als VAST 2.0-Tags transkodiert, damit Sie eine Vorschau davon anzeigen können. Sie können optional [Transkodierung für eine andere DSP anwenden](experience-tag-video-transcoding.md) auf jedes Video-Werbe-Erlebnis-Tag anwenden.

>[!MORELIKETHIS]
>
>* [Einstellungen für zielgerichtete Erlebnisse](experience-settings-targeting.md)
>* [Fügen Sie einen Zielknoten zur endgültigen Ebene hinzu](experience-target-node-add-final.md)
>* [Fügen Sie zwischen Knoten einen Zielknoten ein](experience-target-node-add-inner.md)
>* [Fügen Sie zwischen Knoten einen gleichrangigen Zielknoten hinzu](experience-target-node-add-sibling.md)
>* [Kopieren Sie untergeordnete Knoten und Kreative auf derselben Ebene in einen anderen Knoten](experience-target-node-copy.md)
>* [Zuweisen von Kreativen zu einem endgültigen Knoten](experience-assign-creative-bundles.md)
>* [Passen Sie die Tracking-URLs für Kreative in den zugewiesenen Bundles an](experience-tracking-urls-targeting.md)
>* [Anpassung der kreativen Optimierung und Planung](experience-optimization-scheduling-targeting.md)
>* [Exportieren und Implementieren eines Anzeigen-Erlebnis-Tags für ein Live-Erlebnis](/help/creative/experiences/experience-tag-export.md)
>* [Bearbeiten eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-edit-targeting.md)
