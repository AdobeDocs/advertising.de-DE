---
title: Anpassen der Tracking-URLs für ein Erlebnis ohne Targeting
description: Erfahren Sie, wie Sie die Tracking-URLs für jedes Kreative in einem Erlebnis ohne Targeting mit einem Entscheidungsbaum anpassen.
feature: Creative Experiences
exl-id: 03a10285-c0df-4bc3-92c7-c1c2ea3f8129
source-git-commit: 5d8b511708008c77e817ccdb00ae02c158dfe63e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# Anpassen der Tracking-URLs für ein Erlebnis ohne Targeting mit Entscheidungsbaum

*Geschlossene Beta-Version*

Für Erlebnisse ohne Targeting mit Entscheidungsbäumen können Sie bis zu fünf benutzerdefinierte Impression-Tracking-URLs, fünf benutzerdefinierte Klick-Tracking-URLs und eine benutzerdefinierte Landingpage-URL für jeden einzelnen Kreativen erstellen, der für das Anzeigen-Erlebnis-Tag verwendet wird. Sie können die Tracking-URLs in [!UICONTROL Tag Manager] anpassen.

Die benutzerdefinierten URLs werden nur für Anzeigen verwendet, die aus dem Ad-Erlebnis-Tag erstellt wurden, und werden nicht in den kreativen Basiseinstellungen in [!UICONTROL Creative Libraries] gespeichert.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie in der Kartenansicht auf **[!UICONTROL ...]** neben dem Erlebnisnamen und dann auf **[!UICONTROL Tag Manager]**.

   * Halten Sie in der Tabellenansicht den Cursor über der Zeile, klicken Sie auf **[!UICONTROL More]** und dann auf **[!UICONTROL Tag Manager]**

1. (Wenn kein Tag für die Anzeigengröße vorhanden ist) Erstellen Sie ein Tag für die entsprechende Kreativgröße.

   Sie können für jede für das Erlebnis verwendete Kreativgröße ein oder mehrere Tags erstellen.

   1. Klicken Sie oben rechts auf **[!UICONTROL Create Tag]**.

   1. Geben Sie eine eindeutige **[!UICONTROL Tag name]** ein und wählen Sie die **[!UICONTROL Tag size]** aus.

      Die Größen der standardmäßigen Image-Kreativen für das Erlebnis bestimmen die verfügbaren Größen.

   1. Klicken Sie auf **[!UICONTROL Create]**.

1. Halten Sie den Cursor über die Zeile für das entsprechende Anzeigen-Tag und klicken Sie auf ![Tracking-URLs bearbeiten](/help/creative/assets/edit-gray.png " Tracking-URLs ") bearbeiten **[!UICONTROL Tracking URLs]**. <!-- For targeted experiences, this is "EDIT Tracking URLs" -->&lt;!— Tag Manager hat ab 2/2 nur eine Listenansicht, aber keine Kartenansicht. >

   Auf den Registerkarten [!UICONTROL Click Tracking URLs], [!UICONTROL Impression Tracking URLs] und [!UICONTROL Landing URLs] werden die Namen aller Kreativen in den entsprechenden Größen in den zugewiesenen Bundles aufgelistet. Die Größen der standardmäßigen Image-Kreativen für das Erlebnis bestimmen die verfügbaren Größen.<!-- There's no distinct "Creative Sizes" setting. -->

1. Gehen Sie auf den Registerkarten **[!UICONTROL Click Tracking URLs]**, **[!UICONTROL Impression Tracking URLs]** und **[!UICONTROL Landing URLs]** für jeden Kreativen nach Bedarf wie folgt vor:

   1. Erweitern Sie die Zeile für die Kreativen.

   1. Führen Sie einen der folgenden Schritte aus:

      * Um eine benutzerdefinierte URL hinzuzufügen oder zu bearbeiten, geben Sie die URL in das Eingabefeld ein.

      * Um eine weitere benutzerdefinierte URL hinzuzufügen, klicken Sie auf **[!UICONTROL +]** und geben Sie die URL in das Eingabefeld ein.

      * Um eine benutzerdefinierte URL zu entfernen, halten Sie den Cursor über der kreativen Zeile und klicken Sie auf ![Löschen](/help/creative/assets/delete.png "Löschen").

      Sie können bis zu fünf benutzerdefinierte Impression-Tracking-URLs, fünf benutzerdefinierte Klick-Tracking-URLs und eine benutzerdefinierte Landingpage-URL angeben.

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Zuweisen von Kreativen zu einem Anzeigen-Tag für Erlebnisse ohne Targeting](experience-tag-assign-creatives.md)
>* [Passen Sie die Tracking-URLs für ein Erlebnis mit Entscheidungsbaum-Targeting an](experience-tracking-urls-targeting.md)
