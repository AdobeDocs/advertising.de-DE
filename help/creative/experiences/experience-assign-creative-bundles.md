---
title: Zuweisen und Aufheben der Zuweisung von kreativen Bundles zu einem endgültigen Knoten in einem Erlebnis
description: Erfahren Sie, wie Sie jedem einzelnen Ziel in Ihren Anzeigenerlebnissen Kreative zuweisen.
feature: Creative Experiences
exl-id: 5449a760-6ade-41c0-9cab-bd92026b150b
source-git-commit: 115b769c2880936c422747b44f43b4be7281916d
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Zuweisen und Aufheben der Zuweisung von kreativen Bundles zu einem endgültigen Knoten in einem Erlebnis

*Nur Erlebnisse mit Targeting mit Entscheidungsbäumen*
*Geschlossene Beta-Version*

Sie können einem Zielknoten auf der untersten Ebene eines Erlebnis-Entscheidungsbaums kreative Bundles zuweisen. Für Erlebnisse, für die Sie keine Ziele konfiguriert haben, befindet sich die unterste Ebene unter „Alle“.

Für Standard-Anzeigenerlebnisse können Sie nur standardmäßige kreative Bundles zuweisen. Für dynamische Anzeigenerlebnisse können Sie nur dynamische kreative Bundles zuweisen.

>[!NOTE]
>
>Wenn Sie nicht jedem endgültigen Knoten mindestens ein Kreativ-Bundle zuweisen, können Sie beim Speichern des Erlebnisses ([) die Standard-Kreativen für jeden nicht zugewiesenen Knoten ](experience-create-targeting.md). Um ein Erlebnis zu veröffentlichen, müssen Sie für jeden endgültigen Knoten entweder Bundles zuweisen oder die standardmäßigen Kreativen verwenden.

<!-- 1. [ways to get to the decision tree] -->

1. Führen Sie einen der folgenden Schritte aus:

   * (Abschließende Knoten ohne Kreative) Klicken Sie unter dem Knoten auf ![Hinzufügen](/help/creative/assets/add.png "Hinzufügen") und wählen Sie dann **[!UICONTROL Assign Bundles]** aus.

   * (Knoten mit vorhandenen Kreativen) Halten Sie den Cursor über das Feld für das kreative Bundle unter dem Zielknoten <!-- wording???? --> und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem Bundle, das Sie dem Zielknoten zuweisen möchten, und deaktivieren Sie das Kontrollkästchen neben jedem Bundle, dessen Zuweisung Sie aufheben möchten.

   Es werden nur Bundles des relevanten Bundle-Typs für das Erlebnis (Standard oder dynamisch) aufgelistet.

1. Klicken Sie auf **[!UICONTROL Attach to Bundles]**.

1. (Optional) [Anpassen der Tracking-URLs für Kreative in den zugewiesenen Bundles](experience-tracking-urls-targeting.md).

1. (Optional) [Anpassung der kreativen Optimierung und Planung](experience-optimization-scheduling-targeting.md) für die zugewiesenen Bundles.

<!--
1. (Optional) To save the experience, click **[!UICONTROL Save]**, and then do the following.
...

These formatted steps are inserted automatically from text in the following file in the _includes folder, which reused in multiple places.
-->

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Fügen Sie einen Zielknoten zur endgültigen Ebene hinzu](experience-target-node-add-final.md)
>* [Fügen Sie zwischen Knoten einen Zielknoten ein](experience-target-node-add-inner.md)
>* [Fügen Sie zwischen Knoten einen gleichrangigen Zielknoten hinzu](experience-target-node-add-sibling.md)
>* [Kopieren Sie untergeordnete Knoten und Kreative auf derselben Ebene in einen anderen Knoten](experience-target-node-copy.md)
>* [Erstellen eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-create-targeting.md)
>* [Bearbeiten eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-edit-targeting.md)
>* [Einstellungen für zielgerichtete Erlebnisse](experience-settings-targeting.md)
>* [Exportieren und Implementieren eines Anzeigen-Erlebnis-Tags für ein Live-Erlebnis](experience-tag-export.md)
