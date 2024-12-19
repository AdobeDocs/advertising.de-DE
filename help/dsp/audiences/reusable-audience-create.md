---
title: Erstellen einer wiederverwendbaren Zielgruppe
description: Erfahren Sie, wie Sie wiederverwendbare Zielgruppen erstellen, die aus Zielgruppensegmenten und anderen gespeicherten Zielgruppen bestehen.
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Erstellen einer wiederverwendbaren Zielgruppe

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

Sie können wiederverwendbare Zielgruppen, d. h. Gruppen von Zielgruppensegmenten und sogar andere gespeicherte Zielgruppen, speichern und verwalten. Diese können Sie als Ziele oder Ausschlüsse für mehrere Platzierungen verwenden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**.

1. Eindeutige **[!UICONTROL Audience Name]** eingeben.

1. (Optional) Deaktivieren Sie die zu **[!UICONTROL Share with all advertisers in my account]** Option.

   Wenn Sie eine Zielgruppe freigeben, wird die Zielgruppe als Ziel oder Ausschluss für alle Advertiser im Konto verfügbar. Die einzelnen Segmente in der Zielgruppe stehen jedoch nur Benutzenden zur Verfügung, für die die Segmente freigegeben sind. Wenn Sie beispielsweise eine Zielgruppe mit Adobe Analytics-Segmenten für einen Advertiser freigeben, der nicht demselben [!DNL Analytics] zugeordnet ist, wird das Segment in dieser Zielgruppe für diesen Advertiser nicht in der Vorschau angezeigt. Nur die Segmente, die diesem Advertiser zur Verfügung stehen, werden in der Zielgruppe in der Vorschau angezeigt.

1. Klicken Sie auf **[!UICONTROL Save]**.

1. Erstellen Sie die Zielgruppe:

   >[!NOTE]
   >
   >Beim Erstellen der Zielgruppe werden [ Daten zur ](audience-about.md) im rechten Bedienfeld aktualisiert

   * Gehen Sie wie folgt vor, um die Segmentlogik mithilfe der Segmente auf den Registerkarten [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments] und [!UICONTROL Saved Audiences] manuell ](audience-settings.md) erstellen.

      * Um das erste Segment hinzuzufügen, suchen Sie das Segment im linken Bereich und aktivieren Sie das Kontrollkästchen neben dem Segmentnamen.

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

1. Klicken Sie auf **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Über die Zielgruppenverwaltung](audience-about.md)
>* [Zielgruppeneinstellungen](audience-settings.md)
>* [Syntax für die Logik von Zielgruppensegmenten](audience-segment-logic-syntax.md)
>* [Verfügbare Datenanbieter von Drittanbietern](third-party-data-providers.md)
>* [Erstellen und Implementieren eines benutzerdefinierten Segments](custom-segment-create.md)
>* [Erstellen und Implementieren eines [!UICONTROL CCPA Opt-Out-of-Sale] Segments](ccpa-opt-out-segment-create.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
