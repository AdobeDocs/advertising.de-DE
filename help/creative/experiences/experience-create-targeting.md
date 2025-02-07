---
title: Erstellen eines Erlebnisses mit Targeting mit Entscheidungsbäumen
description: Erfahren Sie, wie Sie mithilfe eines Entscheidungsbaums ein zielgerichtetes Anzeigen-Erlebnis erstellen.
feature: Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# Erstellen eines Erlebnisses mit Targeting mit Entscheidungsbäumen

*Geschlossene Beta-Version*

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

        *[Zielknoten zur letzten Ebene hinzufügen](experience-target-node-add-final.md) in einem Erlebnis.

         * [Fügen Sie einen Zielknoten zwischen Knoten ein](experience-target-node-add-inner.md).

         * [Fügen Sie zwischen Knoten einen gleichrangigen Zielknoten hinzu](experience-target-node-add-sibling.md).

         * [Kopieren Sie untergeordnete Knoten und Kreative auf derselben Ebene in einen anderen Knoten](experience-target-node-copy.md).

      * Kreative Bundles:

         * [Zuweisung und Aufhebung der Zuweisung von Kreativen zu einem endgültigen Knoten](experience-assign-creative-bundles.md).

           Wenn Sie nicht jedem endgültigen Knoten mindestens ein Bundle zuweisen, können Sie beim Speichern des Erlebnisses die standardmäßigen Kreativen für jeden nicht zugewiesenen Knoten verwenden. Um veröffentlicht zu werden, muss das Erlebnis entweder als Bundle zugewiesen werden oder die standardmäßigen Kreativen für alle daraus erstellten Anzeigen verwenden.

         * [Passen Sie die Tracking-URLs für Kreative in den zugewiesenen Bundles ](experience-tracking-urls-targeting.md).

         * [Passen Sie die kreative Optimierung und ](experience-optimization-scheduling-targeting.md) für die zugewiesenen Bundles an.

1. Klicken Sie auf **[!UICONTROL Save]**, und führen Sie dann folgende Schritte aus.

   * (Wenn jeder Knoten auf der untersten Ebene mindestens ein Kreativ-Bundle enthält) Klicken Sie auf **[!UICONTROL OK]**.

   * (Wenn jeder Knoten auf der untersten Ebene nicht mindestens ein kreatives Bundle enthält) Führen Sie einen der folgenden Schritte aus:

      * Um das Erlebnis ohne alle erforderlichen kreativen Bundles zu speichern, klicken Sie auf **[!UICONTROL Save as Draft]**.

        Sie können kein Anzeigen-Tag für ein Erlebnis [Entwurf](experience-about.md#experience-statuses) erstellen.

      * Um jedem Ziel, dem noch kein Kreativ-Bundle zugewiesen wurde, das Standardkreativ-Paket zuzuweisen, klicken Sie auf **[!UICONTROL Assign Default Creatives]**. Nachdem Sie die aktualisierte Baumstruktur mit den standardmäßig zugewiesenen Kreativen überprüft haben, klicken Sie auf **[!UICONTROL Save]** und **[!UICONTROL OK]**.

      * Um mit der Bearbeitung des Entscheidungsbaums fortzufahren, klicken Sie auf **[!UICONTROL Continue Edit]**.

Wenn das Erlebnis live ist, erstellt [!DNL Creative] automatisch ein Anzeigen-Tag für jede entsprechende Kreativgröße.

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
