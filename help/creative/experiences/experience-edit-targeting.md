---
title: Bearbeiten eines Erlebnisses mit Entscheidungsbaum-Targeting
description: Erfahren Sie, wie Sie ein zielgerichtetes Anzeigenerlebnis mit dem KI-gesteuerten oder manuellen Entscheidungsbaum-Editor bearbeiten.
feature: Creative Experiences
exl-id: 8c5e8f9b-c405-41b2-98a9-da7c5debd3e1
TQID: 'https://experienceleague.adobe.com/0mcPjfiET-DKrm2qaa1Odygv1GIgv4cR7lBRNmrYGBk'
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
source-wordcount: '655'
ht-degree: 0%
---
# Bearbeiten eines Erlebnisses mit Entscheidungsbaum-Targeting

Der KI-gesteuerte Editor (Beta) wird standardmäßig für Erlebnisse mit Targeting geöffnet. Sie können mit dem KI-Agenten arbeiten, die Arbeitsfläche direkt bearbeiten oder den vorhandenen manuellen Editor öffnen.

## Erlebnis öffnen {#experience-open}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Optional) [Passen Sie die Ansicht an](/help/creative/introduction/customize-data-views.md) um bestimmte Erlebnisse einzuschließen.

1. Führen Sie einen der folgenden Schritte aus:

   * So öffnen Sie den KI-gesteuerten Editor:

     * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Erlebnisnamen und dann auf **[!UICONTROL Edit]**.

     * Halten Sie in der Tabellenansicht den Cursor über der Zeile, klicken Sie auf **[!UICONTROL More]** und dann auf **[!UICONTROL Edit]**.

   * So öffnen Sie den manuellen Editor:

     * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Erlebnisnamen und dann auf **[!UICONTROL Create Decision Tree Manually (Legacy)]**.

     * Halten Sie in der Tabellenansicht den Cursor über der Zeile, klicken Sie auf **[!UICONTROL More]** und dann auf **[!UICONTROL Create Decision Tree Manually (Legacy)]**.

     * Im KI-gesteuerten Editor

## Bearbeiten mit dem KI-gesteuerten Editor (Beta) {#ai-editor}

1. [Öffnen Sie das Erlebnis](#experience-open).

1. Beschreiben Sie die Zielgruppenänderungen, die Sie in der Konversation vornehmen möchten. Identifizieren Sie den betroffenen Zweig anhand seiner Ziele oder, wenn auf der Arbeitsfläche angezeigt, seiner Knoten-ID.

1. Überprüfen Sie die aktualisierte Baumstruktur und beschreiben Sie alle weiteren Änderungen. Warten Sie, bis die Verarbeitung durch den Assistenten abgeschlossen ist, bevor Sie mit der Arbeitsfläche interagieren.

1. (Optional) Nehmen Sie Änderungen direkt auf der Arbeitsfläche vor:

   * [Zielgruppe auf letzter Ebene hinzufügen](experience-target-node-add-final.md#ai-editor), [Zielebene einfügen](experience-target-node-add-inner.md#ai-editor) oder [gleichrangiges Ziel hinzufügen](experience-target-node-add-sibling.md#ai-editor).

   * Bearbeiten Sie die Kriterien einer Zielgruppe, indem Sie neben der Zielgruppe auf **[!UICONTROL ...]** > **[!UICONTROL Edit]** klicken, die Werte ändern und dann auf **[!UICONTROL Edit Node]** klicken.

   * [Kopieren Sie untergeordnete Knoten und Kreative](experience-target-node-copy.md#ai-editor) oder [löschen Sie einen Knoten](experience-target-node-delete.md#ai-editor).

   * [Zuweisung von Kreativ-Bundles aufheben](experience-assign-creative-bundles.md#ai-editor).

   * [Anpassen der kreativen Optimierung und Planung](experience-optimization-scheduling-targeting.md) oder [Tracking-URLs](experience-tracking-urls-targeting.md#ai-editor).

1. [Speichern Sie das Erlebnis](#save).

## Bearbeiten mit dem manuellen Editor {#manual-editor}

1. [Öffnen Sie das Erlebnis](#experience-open).

1. (Erlebnisse mit Status `[processing](experience-about.md#experience-statuses)`) Wenn Sie zu einem vorhandenen, nicht veröffentlichten Entwurf aufgefordert werden, führen Sie einen der folgenden Schritte aus:

   * Klicken Sie auf **[!UICONTROL Continue editing draft]** , um den Entwurf zu überprüfen und weiter zu bearbeiten.

   * Klicken Sie auf **[!UICONTROL Discard and start again]** , um den Entwurf zu verwerfen und mit der Live-Version zu beginnen.

   * Klicken Sie auf **[!UICONTROL Cancel this edit]**, um die Bearbeitung zu beenden.

1. (Optional) Stellen Sie den Zoom-Schieberegler ein oder klicken Sie auf ![Als vertikalen Baum anzeigen](/help/creative/assets/tree-vertical.png "Als vertikalen Baum anzeigen") oder ![Als horizontalen Baum anzeigen](/help/creative/assets/tree-horizontal.png "Als horizontalen Baum anzeigen"), um die Ausrichtung zu ändern.

   Ihre Anzeigeeinstellungen werden gespeichert, bis Sie sich abmelden.

1. Ändern Sie die Ziele und Kreativen nach Bedarf:

   * [Ein Ziel auf letzter Ebene hinzufügen](experience-target-node-add-final.md#manual-editor), [ein Ziel zwischen Knoten einfügen](experience-target-node-add-inner.md#manual-editor) oder [ein gleichrangiges Ziel hinzufügen](experience-target-node-add-sibling.md#manual-editor).

   * [Kopieren Sie untergeordnete Knoten und Kreative](experience-target-node-copy.md#manual-editor) oder [löschen Sie einen Knoten](experience-target-node-delete.md#manual-editor).

   * [Zuweisung von Kreativ-Bundles aufheben](experience-assign-creative-bundles.md#manual-editor).

   * [Anpassen der kreativen Optimierung und Planung](experience-optimization-scheduling-targeting.md) oder [Tracking-URLs](experience-tracking-urls-targeting.md#manual-editor).

1. [Speichern Sie das Erlebnis](#save).

## Wechseln von Editoren oder Bearbeiten der Erlebniseinstellungen {#switch-editors}

>[!IMPORTANT]
>
>Bevor Sie den KI-gesteuerten Editor verlassen, speichern Sie alle Baumänderungen, die Sie beibehalten möchten. Beim Wechseln zum manuellen Editor oder Erlebnisformular werden nicht gespeicherte Änderungen nicht übertragen.

* **KI-gesteuerter Editor zum manuellen Editor:** Klicken Sie auf **[!UICONTROL Manual Decision Tree]**. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Yes]** , um nicht gespeicherte Änderungen zu verwerfen und den manuellen Editor zu öffnen, oder auf **[!UICONTROL No]** , um zu bleiben.

* **KI-gesteuerter Editor für allgemeine Einstellungen:** Klicken Sie auf &quot;**[!UICONTROL Experience Form]**&quot; und dann auf &quot;**[!UICONTROL Yes]**&quot;, um nicht gespeicherte Strukturänderungen zu verwerfen und das Formular zu öffnen. Bearbeiten Sie die [Allgemeine Erlebniseinstellungen](experience-settings-targeting.md) und klicken Sie dann auf **[!UICONTROL Save]**.

* **Manueller Editor für allgemeine Einstellungen** Speichern Sie alle Strukturänderungen, die Sie beibehalten möchten, und klicken Sie dann auf **[!UICONTROL Experience Form]**. Bearbeiten Sie die [Allgemeine Erlebniseinstellungen](experience-settings-targeting.md) und klicken Sie dann auf **[!UICONTROL Save]**.

* **Allgemeine Einstellungen für den KI-gesteuerten Editor:** Klicken Sie auf **[!UICONTROL Decision Tree]**. Durch Speichern der Änderungen an den allgemeinen Einstellungen eines zielgerichteten Erlebnisses wird auch der KI-gesteuerte Editor geöffnet.

* **Manueller Editor zum KI-gesteuerten Editor:** Speichern Sie Ihre Strukturänderungen, kehren Sie zur [!UICONTROL Experiences] zurück und wählen Sie **[!UICONTROL Edit]** für das Erlebnis aus.

Um den KI-gesteuerten Editor zu verlassen, ohne einen anderen Editor zu öffnen, klicken Sie auf **[!UICONTROL Cancel]**. Klicken Sie auf **[!UICONTROL Yes]**, um nicht gespeicherte Strukturänderungen zu verwerfen, oder auf **[!UICONTROL No]**, um mit der Bearbeitung fortzufahren.

## Erlebnis speichern {#save}

Die folgenden Schritte gelten für beide Editoren.

{{$include /help/_includes/experience-save.md}}

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
>* [Anzeigen des Änderungsprotokolls für ein Erlebnis](/help/creative/experiences/experience-view-change-log.md)
