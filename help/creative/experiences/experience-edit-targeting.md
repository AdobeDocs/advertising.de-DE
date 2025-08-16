---
title: Bearbeiten eines Erlebnisses mit Entscheidungsbaum-Targeting
description: Erfahren Sie, wie Sie die Einstellungen für ein zielgerichtetes Anzeigen-Erlebnis mithilfe eines Entscheidungsbaums bearbeiten.
feature: Creative Experiences
exl-id: 8c5e8f9b-c405-41b2-98a9-da7c5debd3e1
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# Bearbeiten eines Erlebnisses mit Entscheidungsbaum-Targeting

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Optional) [Passen Sie die Ansicht an](/help/creative/introduction/customize-data-views.md) um bestimmte Erlebnisse einzuschließen.

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Erlebnisnamen und dann auf **[!UICONTROL Edit]**.

   * Halten Sie in der Tabellenansicht den Cursor über der Zeile, klicken Sie auf **[!UICONTROL More]** und dann auf **[!UICONTROL Edit]**.

   Der Entscheidungsbaum wird standardmäßig geöffnet.

1. (Optional) Wechseln Sie bei Bedarf zwischen dem Entscheidungsbaum und den allgemeinen Einstellungen:

   * Um die allgemeinen Einstellungen im Entscheidungsbaum zu öffnen, klicken Sie oben rechts auf **[!UICONTROL Experience Form]** .

   * Um den Entscheidungsbaum über die allgemeinen Einstellungen zu öffnen, klicken Sie oben rechts auf **[!UICONTROL Decision Tree]** .

1. (Optional) Führen Sie einen der folgenden Schritte aus, um den Entscheidungsbaum zu bearbeiten:

   * ([Verarbeitung](experience-about.md#experience-statuses) Erlebnisse) Führen Sie einen der folgenden Schritte aus:

      * Um die vorhandenen, nicht veröffentlichten Änderungen am Live-Erlebnis zu verwerfen, klicken Sie auf **[!UICONTROL Discard and start again]**.

      * Um die vorhandenen, nicht veröffentlichten Änderungen beizubehalten, klicken Sie auf **[!UICONTROL Continue editing draft]**.

      * Um die Erlebnisdetails zu bearbeiten, klicken Sie auf **[!UICONTROL Edit Experience Details]**.

   * (Optional) Ändern Sie die Anzeigeeinstellungen für den Entscheidungsbaum.

     Ihre Einstellungen werden gespeichert, bis Sie sich abmelden.

   * Vergrößern oder verkleinern Sie die Ansicht, indem Sie den Schieberegler bewegen.

   * Wechseln Sie zwischen der Anzeige einer vertikalen Liste und einer horizontalen Liste, indem Sie auf ![Als vertikale Baumstruktur anzeigen](/help/creative/assets/tree-vertical.png "Als vertikale Baumstruktur anzeigen") bzw. ![Als horizontalen Baum anzeigen](/help/creative/assets/tree-horizontal.png "Als horizontalen Baum anzeigen") klicken.

   * (Optional) Ändern Sie die Anzeigenziele und die entsprechenden Kreativen auf eine der folgenden Arten:

      * Zielgruppen:

        *[Zielknoten zur letzten Ebene hinzufügen](experience-target-node-add-final.md) in einem Erlebnis.

         * [Fügen Sie einen Zielknoten zwischen Knoten ein](experience-target-node-add-inner.md).

         * [Fügen Sie zwischen Knoten einen gleichrangigen Zielknoten hinzu](experience-target-node-add-sibling.md).

         * [Kopieren Sie untergeordnete Knoten und Kreative auf derselben Ebene in einen anderen Knoten](experience-target-node-copy.md).

      * Creative-Bundles:

         * [Zuweisung und Aufhebung der Zuweisung von Kreativen zu einem endgültigen Knoten](experience-assign-creative-bundles.md).

           Wenn Sie nicht jedem endgültigen Knoten mindestens ein Bundle zuweisen, können Sie beim Speichern des Erlebnisses die standardmäßigen Kreativen für jeden nicht zugewiesenen Knoten verwenden. Um ein Erlebnis zu veröffentlichen, müssen Sie für jeden endgültigen Knoten entweder Bundles zuweisen oder die standardmäßigen Kreativen verwenden.

         * [Passen Sie die Tracking-URLs für Kreative in den zugewiesenen Bundles ](experience-tracking-urls-targeting.md).

         * [Passen Sie die kreative Optimierung und ](experience-optimization-scheduling-targeting.md) für die zugewiesenen Bundles an.

1. (Optional) Bearbeiten Sie die [allgemeinen Erlebniseinstellungen](experience-settings-targeting.md).

1. Klicken Sie auf **[!UICONTROL Save]**, und führen Sie dann folgende Schritte aus.

   * (Wenn jeder Knoten auf der untersten Ebene mindestens ein Kreativ-Bundle enthält) Klicken Sie auf **[!UICONTROL OK]**.

   * (Wenn jeder Knoten auf der untersten Ebene nicht mindestens ein kreatives Bundle enthält) Führen Sie einen der folgenden Schritte aus:

      * Um das Erlebnis ohne alle erforderlichen Kreativ-Bundles zu speichern, klicken Sie auf **[!UICONTROL Save as Draft]**.

        Sie können kein Anzeigen-Tag für ein Erlebnis [Entwurf](experience-about.md#experience-statuses) erstellen.

      * Um jedem Ziel, dem noch kein Kreativ-Bundle zugewiesen wurde, das Standardkreativ-Paket zuzuweisen, klicken Sie auf **[!UICONTROL Assign Default Creatives]**. Nachdem Sie die aktualisierte Baumstruktur mit den standardmäßig zugewiesenen Kreativen überprüft haben, klicken Sie auf **[!UICONTROL Save]** und **[!UICONTROL OK]**.

      * Um mit der Bearbeitung des Entscheidungsbaums fortzufahren, klicken Sie auf **[!UICONTROL Continue Edit]**.

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
>* [Erstellen eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-create-targeting.md)
