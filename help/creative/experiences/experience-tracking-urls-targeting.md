---
title: Anpassen der Tracking-URLs für ein Erlebnis
description: Erfahren Sie, wie Sie die Tracking-URLs für jedes Kreative in einem Erlebnis mit Entscheidungsbaum-Targeting anpassen.
feature: Creative Experiences
exl-id: ba3b15b4-116e-4caa-8ce1-4d2e488a6362
TQID: 'https://experienceleague.adobe.com/LjeF7eYU8V93W28VbV-D6NNWWwdKqywOP2BwzDwQAgo'
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
source-wordcount: '448'
ht-degree: 0%
---
# Anpassen der Tracking-URLs für Kreative in einem Erlebnis mit Entscheidungsbaum-Targeting

*Targeting von Knoten nur mit vorhandenen Kreativen*

Für Erlebnisse mit Entscheidungsbaum-Targeting können Sie bis zu fünf benutzerdefinierte Impression-Tracking-URLs und fünf benutzerdefinierte Klick-Tracking-URLs für jeden einzelnen für das Erlebnis verwendeten Kreativen erstellen. Wenn die Überschreibung der Landingpage verfügbar ist, können Sie auch eine benutzerdefinierte Landingpage-URL angeben. Sie können die Tracking-URLs in jedem Entscheidungsbaum-Editor anpassen.

Die benutzerdefinierten URLs werden nur für Anzeigen verwendet, die aus dem Erlebnis erstellt wurden, und nicht in den kreativen Basiseinstellungen in [!UICONTROL Creative Libraries] gespeichert.

Die Überschreibung der Landingpage ist für Standarderlebnisse und für Knoten verfügbar, die standardmäßige Kreative verwenden. Bei zugewiesenen dynamischen Bundles werden Landingpages durch den Feed bestimmt und die Registerkarte Landingpage wird nicht angezeigt.

## Verwenden des KI-gesteuerten Editors (Beta) {#ai-editor}

Verwenden Sie beim [ (Erstellen](experience-create-targeting.md#ai-editor) oder [Bearbeiten](experience-edit-targeting.md#ai-editor) des Erlebnisses die Canvas-Steuerelemente:

1. Klicken Sie im kreativen Blattknoten unter dem Zielknoten auf **[!UICONTROL ...]** > **[!UICONTROL Edit Tracking URLs]**.

1. Wählen Sie die Registerkarte **[!UICONTROL Click Tracking URLs]**, **[!UICONTROL Impression Tracking URLs]** oder (falls verfügbar) **[!UICONTROL Landing URL]** aus.

   Kreative werden nach Bundle gruppiert. Die standardmäßigen Kreativgrößen für das Erlebnis bestimmen die verfügbaren Kreativgrößen.

1. Erweitern Sie das Kreativ, das Sie bearbeiten möchten, und führen Sie einen der folgenden Schritte aus:

   * Um eine benutzerdefinierte URL hinzuzufügen oder zu bearbeiten, geben Sie die URL in das Eingabefeld ein.

   * Um eine weitere benutzerdefinierte Tracking-URL hinzuzufügen, klicken Sie auf **[!UICONTROL Add URL]** und geben Sie die URL in das Eingabefeld ein.

   * Um eine benutzerdefinierte URL zu entfernen, klicken Sie auf **[!UICONTROL Delete URL]**.

   Klicken Sie außerhalb eines bearbeiteten Felds und korrigieren Sie etwaige Validierungsfehler vor dem Speichern.

1. Klicken Sie im Dialogfeld auf **[!UICONTROL Save]** , um die Arbeitsstruktur zu aktualisieren.

1. [Speichern Sie das Erlebnis](#save) über die Baumkopfzeile.

## Verwenden des manuellen Editors {#manual-editor}

[Öffnen Sie den manuellen Editor](experience-edit-targeting.md#experience-open) bevor Sie diese Schritte ausführen.

1. Klicken Sie im kreativen Blattknoten unter dem Zielknoten auf **[!UICONTROL ...]** > **[!UICONTROL Edit Tracking URLs]**.

1. Wählen Sie die Registerkarte **[!UICONTROL Click Tracking URLs]**, **[!UICONTROL Impression Tracking URLs]** oder (falls verfügbar) **[!UICONTROL Landing URLs]** aus.

   Auf den Registerkarten werden die Kreativen in den zugewiesenen Bundles aufgelistet. Die standardmäßigen Kreativgrößen für das Erlebnis bestimmen die verfügbaren Kreativgrößen.<!-- There's no distinct "Creative Sizes" setting. -->

1. Erweitern Sie das Kreativ, das Sie bearbeiten möchten, und führen Sie einen der folgenden Schritte aus:

   * Um eine benutzerdefinierte URL hinzuzufügen oder zu bearbeiten, geben Sie die URL in das Eingabefeld ein.

   * Um eine weitere benutzerdefinierte Tracking-URL hinzuzufügen, klicken Sie auf **[!UICONTROL +]** und geben Sie die URL in das Eingabefeld ein.

   * Um eine benutzerdefinierte URL zu entfernen, halten Sie den Cursor über der kreativen Zeile und klicken Sie auf ![Löschen](/help/creative/assets/delete.png "Löschen").

1. Klicken Sie im Dialogfeld auf **[!UICONTROL Save]** , um die Arbeitsstruktur zu aktualisieren.

1. [Speichern Sie das Erlebnis](#save) über die Baumkopfzeile.

## Erlebnis speichern {#save}

Die folgenden Schritte gelten für beide Editoren. Wenn Sie das Tracking-URL-Dialogfeld allein speichern, wird das Erlebnis nicht gespeichert oder veröffentlicht.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Zuweisen und Aufheben der Zuweisung von kreativen Bundles zu einem endgültigen Knoten in einem Erlebnis](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Anpassen der Tracking-URLs für ein Erlebnis ohne Targeting mit Entscheidungsbaum](experience-tracking-urls-no-targeting.md)
