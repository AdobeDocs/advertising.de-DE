---
title: Zuweisen und Aufheben der Zuweisung von kreativen Bundles zu einem endgültigen Knoten in einem Erlebnis
description: Erfahren Sie, wie Sie jedem einzelnen Ziel in Ihren Anzeigenerlebnissen Kreative zuweisen.
feature: Creative Experiences
exl-id: 5449a760-6ade-41c0-9cab-bd92026b150b
TQID: 'https://experienceleague.adobe.com/HqTq2fiJadk-QIBwYkOxC2N9sTMm29LIXRzSubPuv9M'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%
---
# Zuweisen und Aufheben der Zuweisung von kreativen Bundles zu einem endgültigen Knoten in einem Erlebnis

*Nur Erlebnisse mit Targeting mit Entscheidungsbäumen*

Sie können einem Zielknoten auf der untersten Ebene eines Erlebnis-Entscheidungsbaums kreative Bundles zuweisen. Für Erlebnisse, für die Sie keine Ziele konfiguriert haben, befindet sich die unterste Ebene unter „Alle“.

Für Standard-Anzeigenerlebnisse können Sie nur standardmäßige kreative Bundles zuweisen. Für dynamische Anzeigenerlebnisse können Sie nur dynamische kreative Bundles zuweisen.

>[!NOTE]
>
>Wenn Sie nicht jedem endgültigen Knoten mindestens ein Kreativ-Bundle zuweisen, können Sie beim Speichern des Erlebnisses ([) die Standard-Kreativen für jeden nicht zugewiesenen Knoten &#x200B;](experience-create-targeting.md). Um ein Erlebnis zu veröffentlichen, müssen Sie für jeden endgültigen Knoten entweder Bundles zuweisen oder die standardmäßigen Kreativen verwenden.

## Verwenden des KI-gesteuerten Editors (Beta) {#ai-editor}

Verwenden Sie beim [&#x200B; (Erstellen](experience-create-targeting.md#ai-editor) oder [Bearbeiten](experience-edit-targeting.md#ai-editor) des Erlebnisses die Canvas-Steuerelemente:

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie für einen endgültigen Knoten ohne Bundles auf **[!UICONTROL Assign Bundles]**.

   * Klicken Sie bei einem Knoten mit vorhandenen Bundles auf **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]** auf seinem kreativen Blattknoten.

1. Aktivieren Sie auf der Registerkarte **[!UICONTROL Assign Bundles]** das Kontrollkästchen neben jedem Bundle, das zugewiesen werden soll, und deaktivieren Sie das Kontrollkästchen neben jedem Bundle, dessen Zuweisung Sie aufheben möchten.

   Es werden nur Bundles des für das Erlebnis relevanten Typs (Standard oder dynamisch) aufgelistet.

1. (Optional) Öffnen Sie die Registerkarte **[!UICONTROL Creative optimisation]** , um [Rotation und Planung anzupassen](experience-optimization-scheduling-targeting.md).

1. Klicken Sie im Dialogfeld auf **[!UICONTROL Save]** , um die Arbeitsstruktur zu aktualisieren.

1. (Optional) [Tracking-URLs anpassen](experience-tracking-urls-targeting.md#ai-editor).

1. [Speichern Sie das Erlebnis](#save) aus der Baumkopfzeile, um Ihre Änderungen beizubehalten.

## Verwenden des manuellen Editors {#manual-editor}

[Öffnen Sie den manuellen Editor](experience-edit-targeting.md#experience-open) bevor Sie diese Schritte ausführen.

1. Führen Sie einen der folgenden Schritte aus:

   * (Abschließende Knoten ohne Kreative) Klicken Sie unter dem Knoten auf **[!UICONTROL Assign Bundles]**.

   * (Knoten mit vorhandenen Kreativen) Halten Sie den Cursor über das Feld für das kreative Bundle unter dem Zielknoten und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Edit Bundles]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem Bundle, das Sie dem Zielknoten zuweisen möchten, und deaktivieren Sie das Kontrollkästchen neben jedem Bundle, dessen Zuweisung Sie aufheben möchten.

   Es werden nur Bundles des relevanten Bundle-Typs für das Erlebnis (Standard oder dynamisch) aufgelistet.

1. Klicken Sie auf **[!UICONTROL Save]**.

1. (Optional) [Anpassung der kreativen Optimierung und Planung](experience-optimization-scheduling-targeting.md) für die zugewiesenen Bundles.

1. (Optional) [Anpassen der Tracking-URLs für Kreative in den zugewiesenen Bundles](experience-tracking-urls-targeting.md).

## Erlebnis speichern {#save}

Die folgenden Schritte gelten für beide Editoren. Beim Speichern des Bundle-Dialogfelds allein wird das Erlebnis nicht gespeichert oder veröffentlicht.

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
>* [Anzeigen des Änderungsprotokolls für ein Erlebnis](/help/creative/experiences/experience-view-change-log.md)
