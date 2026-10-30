---
title: Erstellen eines Erlebnisses mit Targeting mit Entscheidungsbäumen
description: Erfahren Sie, wie Sie mit dem KI-gesteuerten oder manuellen Entscheidungsbaum-Editor ein zielgerichtetes Anzeigenerlebnis erstellen.
feature: Creative Experiences
exl-id: 825fd9af-ca7a-4b44-8e4b-1a6f34edac9e
TQID: 'https://experienceleague.adobe.com/nxegtoNEqfAk7LUyb-3qD6YJYaGfx3M3QdrLx-q5y14'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
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
source-wordcount: '715'
ht-degree: 0%
---
# Erstellen eines Erlebnisses mit Targeting mit Entscheidungsbäumen

Erstellen Sie ein zielgerichtetes Anzeigen-Erlebnis mithilfe eines Entscheidungsbaums. Jedes Erlebnis verwendet Anzeigen aus einer einzigen Kreativbibliothek.

Der KI-gesteuerte Editor (Beta) wird standardmäßig geöffnet. Sie können die Baumstruktur über den KI-Agenten konfigurieren oder die Arbeitsfläche direkt bearbeiten. Sie können auch zum vorhandenen manuellen Editor wechseln.

>[!NOTE]
>
>* Nachdem Sie ein zielgerichtetes Erlebnis erstellt haben, können Sie es später nicht mehr in ein nicht zielgerichtetes Erlebnis ändern, das einen anderen Workflow verwendet.
>* Stellen Sie sicher, dass Ihre Anzeigenerlebnisse ein Targeting enthalten, das mit den Kampagnen kompatibel ist, in denen Sie es implementieren werden. Das hierarchische Targeting-Verhalten kann je nach DSP variieren. Wenn Sie ein Anzeigen-Erlebnis-Tag in Advertising DSP hochladen und es an eine Platzierung anhängen, wird das Targeting auf Anzeigenebene über dem Targeting auf Platzierungsebene (nicht anstelle des Targetings auf Platzierungsebene) angewendet. Wenn sich eine Platzierung beispielsweise an Benutzende in Australien und eine Anzeige an Benutzende in Japan richtet, zielt die Anzeige auf den Zweig „Alle anderen“ ab.

## Erstellen des Erlebnisses

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Klicken Sie auf **[!UICONTROL Create New Experience]**.

1. Geben Sie die [allgemeinen Erlebniseinstellungen](experience-settings-targeting.md) mit aktiviertem **[!UICONTROL Targeting]** ein.

1. Klicken Sie auf **[!UICONTROL Create]**.

   Der KI-gesteuerte Entscheidungsbaum-Editor wird für das neue Erlebnis geöffnet.

1. Konfigurieren Sie die Baumstruktur mit einem der folgenden Verfahren.

## Konfigurieren der Baumstruktur mit dem KI-gesteuerten Editor (Beta) {#ai-editor}

1. Beschreiben Sie im Gespräch die gewünschte Zielgruppenstruktur, einschließlich der Kriterien für jede Verzweigung und des Umgangs mit Viewern, die keiner angegebenen Zielgruppe entsprechen.

1. Überprüfen Sie die Baumstruktur auf der Arbeitsfläche. Um Änderungen anzufordern, beschreiben Sie sie im Gespräch. Warten Sie, bis die Verarbeitung durch den Assistenten abgeschlossen ist, bevor Sie mit der Arbeitsfläche interagieren.

1. (Optional) Verfeinern Sie die Baumstruktur direkt auf der Arbeitsfläche:

   * [Zielgruppe auf letzter Ebene hinzufügen](experience-target-node-add-final.md#ai-editor), [Zielebene einfügen](experience-target-node-add-inner.md#ai-editor) oder [gleichrangiges Ziel hinzufügen](experience-target-node-add-sibling.md#ai-editor).

   * [Kopieren Sie untergeordnete Knoten und Kreative](experience-target-node-copy.md#ai-editor) oder [löschen Sie einen Knoten](experience-target-node-delete.md#ai-editor).

1. [Weisen Sie den endgültigen Knoten kreative Bundles zu](experience-assign-creative-bundles.md#ai-editor) und passen Sie optional [kreative Optimierung und Planung](experience-optimization-scheduling-targeting.md) und [Tracking-URLs](experience-tracking-urls-targeting.md#ai-editor) an.

   Um das Erlebnis zu veröffentlichen, müssen Sie jedem endgültigen Knoten Bundles zuweisen oder die standardmäßigen Kreativen des Erlebnisses verwenden. Beim Speichern können Sie nicht zugewiesenen Knoten Standardwerte zuweisen.

1. (Optional) Bearbeiten Sie die allgemeinen Erlebniseinstellungen:

   1. Klicken Sie auf &quot;**[!UICONTROL Save]**&quot;, um alle gewünschten Strukturänderungen zu speichern.

   1. Klicken Sie auf **[!UICONTROL Experience Form]** und dann auf **[!UICONTROL Yes]** , um nicht gespeicherte Strukturänderungen zu verwerfen und das Formular zu öffnen.

   1. Bearbeiten Sie die [Allgemeine Erlebniseinstellungen](experience-settings-targeting.md) und klicken Sie dann auf **[!UICONTROL Save]**.

      Der KI-gesteuerte Editor wird geöffnet.

1. [Speichern Sie das Erlebnis](#save).

## Konfigurieren der Baumstruktur mit dem manuellen Editor {#manual-editor}

1. Klicken Sie im KI-gesteuerten Editor auf **[!UICONTROL Manual Decision Tree]** und anschließend auf **[!UICONTROL Yes]** , um den KI-gesteuerten Editor zu verlassen.

   Speichern Sie alle KI-Editor-Änderungen, die Sie vor dem Wechsel beibehalten möchten. Durch Bestätigen des Schalters werden nicht gespeicherte Strukturänderungen verworfen.

1. (Optional) Ändern Sie die Anzeigeeinstellungen:

   * Vergrößern oder verkleinern Sie die Ansicht, indem Sie den Schieberegler bewegen.

   * Wechseln Sie zwischen der vertikalen und der horizontalen Ansicht, indem Sie auf ![Als vertikale Baumstruktur anzeigen](/help/creative/assets/tree-vertical.png "Als vertikale Baumstruktur anzeigen") oder ![Als horizontalen Baum anzeigen](/help/creative/assets/tree-horizontal.png "Als horizontalen Baum anzeigen") klicken.

   Ihre Anzeigeeinstellungen werden gespeichert, bis Sie sich abmelden.

1. Konfigurieren Sie die Anzeigenziele und die entsprechenden Kreativen:

   * [Ein Ziel auf letzter Ebene hinzufügen](experience-target-node-add-final.md#manual-editor), [ein Ziel zwischen Knoten einfügen](experience-target-node-add-inner.md#manual-editor) oder [ein gleichrangiges Ziel hinzufügen](experience-target-node-add-sibling.md#manual-editor).

   * [Kopieren Sie untergeordnete Knoten und Kreative](experience-target-node-copy.md#manual-editor) oder [löschen Sie einen Knoten](experience-target-node-delete.md#manual-editor).

   * [Zuweisen von kreativen ](experience-assign-creative-bundles.md#manual-editor) und optional [Anpassen der kreativen Optimierung und Planung](experience-optimization-scheduling-targeting.md) und [Tracking-URLs](experience-tracking-urls-targeting.md#manual-editor).

1. (Optional) Um die allgemeinen Erlebniseinstellungen zu bearbeiten, klicken Sie auf **[!UICONTROL Experience Form]** und bearbeiten Sie die [allgemeinen Erlebniseinstellungen](experience-settings-targeting.md).

1. [Speichern Sie das Erlebnis](#save).

## Erlebnis speichern {#save}

Die folgenden Schritte gelten für beide Editoren.

{{$include /help/_includes/experience-save.md}}

## Hinzufügen von Tags und Videotranskodierung für gespeicherte Erlebnisse

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
>* [Anzeigen des Änderungsprotokolls für ein Erlebnis](/help/creative/experiences/experience-view-change-log.md)
