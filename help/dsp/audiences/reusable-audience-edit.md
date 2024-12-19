---
title: Bearbeiten einer wiederverwendbaren Zielgruppe
description: Erfahren Sie, wie Sie eine wiederverwendbare Zielgruppe bearbeiten.
feature: DSP Audiences
exl-id: 4de6b9a4-2907-474d-92bf-83686a1f0b31
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Bearbeiten einer wiederverwendbaren Zielgruppe

Wenn Sie eine Zielgruppe bearbeiten, die in Platzierungen oder anderen wiederverwendbaren Zielgruppen verwendet wird, werden die Änderungen sofort auf diese Platzierungen und Zielgruppen angewendet.<!-- verify -->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL All audiences]**.

1. Halten Sie den Cursor über die Zeile Audience und klicken Sie auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie die Zielgruppeneinstellungen auf eine der folgenden Arten:

   >[!NOTE]
   >
   >Wenn Sie die Zielgruppensegmentlogik bearbeiten, werden [Daten zur Zielgruppengröße](audience-about.md) im rechten Bedienfeld aktualisiert.

   * (Optional) Um den **[!UICONTROL Audience Name]** zu bearbeiten![ klicken Sie neben ](/help/dsp/assets/edit.png) Zielgruppennamen auf „Bearbeiten“, geben Sie einen eindeutigen Zielgruppennamen ein und klicken Sie dann auf &quot;**[!UICONTROL Apply]**&quot;.

   * (Optional) Gehen Sie wie folgt vor, um die Segmentlogik mithilfe der Segmente, die auf den Registerkarten [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments] und [!UICONTROL Saved Audiences] verfügbar ](audience-settings.md), manuell zu bearbeiten.

      * So fügen Sie ein Segment zu einer vorhandenen Segmentgruppe hinzu:

      1. Klicken Sie auf die Segmentgruppe im rechten Bedienfeld.

      1. (Optional) Ändern Sie die Gruppenlogik nach Bedarf in *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* oder *[!UICONTROL Exclude All]*.

         *[!UICONTROL Exclude All]* ist nicht für die erste Segmentgruppe verfügbar. Für eine Zielgruppe, die nur Ausschlüsse enthält, erstellen Sie diese Zielgruppe als *[!UICONTROL Include Any]* und wählen Sie dann innerhalb einer Platzierung diese Zielgruppe aus dem Menü Ausgeschlossene Zielgruppen aus.

      1. Suchen Sie das neue Segment im linken Bereich und aktivieren Sie das Kontrollkästchen neben dem Segmentnamen.

         Die Segmentgruppe wird automatisch mit dem neuen Segment aktualisiert.

   * Hinzufügen einer neuen Segmentgruppe:

      1. Klicken Sie im rechten Bedienfeld auf **[!UICONTROL + New Group]** .

      1. (Optional) Ändern Sie bei Bedarf die Logik zwischen der vorherigen Gruppe und der neuen Gruppe in *[!UICONTROL And]* oder *[!UICONTROL Or]*.

      1. Suchen Sie die Segmente für die neue Gruppe im linken Bereich und aktivieren Sie die Kontrollkästchen neben den Segmentnamen.

      1. (Optional) Ändern Sie die Gruppenlogik nach Bedarf in *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* oder *[!UICONTROL Exclude All]*.

   * So verwenden Sie die Segmentlogik einer bestehenden Audience:

      1. Kopieren Sie die Segmentlogik aus der bestehenden Audience auf eine der folgenden Arten:

         * Halten Sie in der Ansicht Alle Zielgruppen den Cursor über die Zeile Zielgruppe und klicken Sie dann auf **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Klicken Sie in den Einstellungen für die vorhandene Zielgruppe oben im Bedienfeld Segmentlogik auf **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Erstellen Sie in einem Texteditor manuell die Segmentlogik mit alphanumerischen Segment-IDs und [boolesche Syntax](audience-segment-logic-syntax.md) und kopieren Sie sie in die Zwischenablage.

      1. Klicken Sie auf **[!UICONTROL paste in an audience rule to begin building]**, fügen Sie die vorhandene Segmentlogik in das Eingabefeld ein und klicken Sie dann auf **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Wenn die Zielgruppe bereits eine Segmentlogik enthält, überschreibt das Einfügen einer neuen Segmentlogik die vorhandene Logik.

1. Klicken Sie auf **[!UICONTROL Save]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Continue]**.

>[!MORELIKETHIS]
>
>* [Über die Zielgruppenverwaltung](audience-about.md)
>* [Erstellen einer wiederverwendbaren Zielgruppe](reusable-audience-create.md)
>* [Duplizieren Sie eine wiederverwendbare Zielgruppe](reusable-audience-duplicate.md)
>* [Anzeigen von Details zu wiederverwendbaren Zielgruppen](reusable-audience-view-details.md)
>* [Freigeben einer wiederverwendbaren Zielgruppe](reusable-audience-share.md)
>* [Exportieren Sie eine wiederverwendbare Zielgruppe](reusable-audience-export.md)
>* [Kopieren Sie den Segmentschlüssel für eine wiederverwendbare Zielgruppe in die Zwischenablage](reusable-audience-clipboard.md)
>* [Löschen einer wiederverwendbaren Zielgruppe](reusable-audience-delete.md)
>* [Zielgruppeneinstellungen](audience-settings.md)
>* [Syntax für die Logik von Zielgruppensegmenten](audience-segment-logic-syntax.md)
>* [Verfügbare Datenanbieter von Drittanbietern](third-party-data-providers.md)
