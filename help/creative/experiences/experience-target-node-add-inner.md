---
title: Hinzufügen eines Zielknotens zwischen Knoten in einem Erlebnis
description: Erfahren Sie, wie Sie in einem Werbeerlebnis einen Zielknoten zwischen Zielknoten hinzufügen.
feature: Creative Experiences
exl-id: ac9211e5-c6ed-4185-bf9c-c2689f1b2775
TQID: 'https://experienceleague.adobe.com/lPQtymUs3okctV2t6ZEE2rMG-F-BA2tJZO1GuceTxtY'
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
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '1117'
ht-degree: 0%
---
# Hinzufügen eines Zielknotens zwischen Knoten in einem Erlebnis

*Nur Erlebnisse mit Targeting mit Entscheidungsbäumen*

Wenn Sie einen Zielknoten zwischen vorhandenen Ebenen einfügen, behält der neue Zielknoten alle vorhandenen untergeordneten Ziele und Kreativen bei, und der neue Knoten heißt zunächst „Alle“. Optional können Sie den neuen Knoten beibehalten, ohne spezifischere Ziele hinzuzufügen.

Um ein bestimmtes Ziel zu definieren, fügen Sie einen zusätzlichen gleichrangigen Zielknoten auf derselben Ebene hinzu, geben Sie das neue Ziel an und weisen Sie dann nur diesem Ziel Kreative zu. Durch Hinzufügen eines gleichrangigen Zielknotens wird der neue Zielknoten erstellt und alle untergeordneten Ziele und Kreativen, die zuvor „Alle“ zugewiesen waren, werden auf derselben Ebene in einen neuen Knoten „Alles andere“ verschoben. Auf diese Weise wirkt sich das Hinzufügen der neuen Zielgruppe nicht auf die vorhandenen untergeordneten Verzweigungen aus, da nur der neue gleichrangige Knoten die neuen Zielgruppenbestimmungsinformationen enthält.

>[!NOTE]
>
>Informationen zum Hinzufügen eines Zielknotens zur untersten Ebene eines Entscheidungsbaums finden Sie unter &quot;[Hinzufügen eines Zielknotens zur letzten Ebene eines Erlebnisses](experience-target-node-add-final.md)&quot;.

## Verwenden des KI-gesteuerten Editors (Beta) {#ai-editor}

Während Sie das Erlebnis [erstellen](experience-create-targeting.md#ai-editor) oder [bearbeiten](experience-edit-targeting.md#ai-editor) können Sie den KI-Agenten bitten, eine Zielebene einzufügen. Identifizieren Sie, wo es eingefügt werden soll und welche bestehenden Verzweigungen und Kreativen beibehalten werden sollen, und überprüfen Sie das Ergebnis. So fügen Sie die Ebene direkt in die Arbeitsfläche ein:

1. Klicken Sie an der Grenze, an der Sie die Ebene einfügen möchten, auf **[!UICONTROL Add targeting level]**.

   In der horizontalen Ansicht ist dieses Steuerelement ein Symbol mit derselben Beschriftung.

1. Wählen Sie **[!UICONTROL New targeting level]** die Zielkategorie aus und klicken Sie dann auf **[!UICONTROL Add targeting level]**.

   * Wählen Sie für Zielgruppenziele **[!UICONTROL Audience]** aus.

   * Wählen Sie für geografische Ziele eine einzelne geografische Kategorie aus (z. B. **[!UICONTROL Geo: Country]**).

   * Wählen Sie für Ziele zum Übergeben von Daten **[!UICONTROL Data Pass]** aus.

   * Wählen Sie für das Retargeting von Pixel-Zielen **[!UICONTROL RT Pixel]** aus.

   * Wählen Sie für Geräteziele eine einzelne Zielkategorie aus (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** oder **[!UICONTROL Device: Browser]**).

   Beim Einfügen einer Ebene werden keine Zielwerte abgefragt. Die neue Ebene verwendet zunächst „Alle“ und behält die vorhandenen untergeordneten Ziele und Kreativen bei.

1. (Optional) Um ein bestimmtes Ziel auf der neuen Ebene zu definieren, [&#x200B; Sie „einen gleichrangigen Zielknoten hinzufügen](experience-target-node-add-sibling.md#ai-editor). Andernfalls behalten Sie den neuen Knoten „Alle“ bei, ohne spezifische Ziele hinzuzufügen.

1. (Optional) Um einen benutzerdefinierten Zielknoten umzubenennen, klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**, geben Sie den **[!UICONTROL Node Name]** ein und klicken Sie dann auf **[!UICONTROL Save]**.

   Sie können keinen Knoten „Alle“ oder „Alle anderen“ umbenennen.

1. Überprüfen Sie die beibehaltenen Verzweigungen und weisen [&#x200B; neuen endgültigen Knoten &#x200B;](experience-assign-creative-bundles.md#ai-editor)Kreativ-Bundles“ zu.

1. [Speichern Sie das Erlebnis](#save).

## Verwenden des manuellen Editors {#manual-editor}

[Öffnen Sie den manuellen Editor](experience-edit-targeting.md#experience-open) bevor Sie diese Schritte ausführen.

1. Klicken Sie unter dem Knoten, an dem Sie das Ziel einfügen möchten, auf ![Hinzufügen](/help/creative/assets/add.png "Hinzufügen") und wählen Sie dann **[!UICONTROL Insert New Target]** aus.

1. Führen Sie einen der folgenden Schritte aus:

   * Wenn keine gleichrangigen Knoten bereits vorhanden sind, gehen Sie wie folgt vor:

     1. Wählen Sie den Zieltyp aus und klicken Sie dann auf **[!UICONTROL Apply]**:

        * Wählen Sie für Zielgruppenziele **[!UICONTROL Audience]** aus.

        * Wählen Sie für geografische Ziele eine einzelne geografische Kategorie aus (z. B. **[!UICONTROL Geo: Country]**).

        * Wählen Sie für Ziele zum Übergeben von Daten **[!UICONTROL Data Pass]** aus.

        * Wählen Sie für das Retargeting von Pixel-Zielen **[!UICONTROL RT Pixel]** aus.

        * Wählen Sie für Geräteziele eine einzelne Zielkategorie aus (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** oder **[!UICONTROL Device: Browser]**).

   * Wenn gleichrangige Knoten bereits vorhanden sind, führen Sie die folgenden Schritte aus:

     * Für Zielgruppenziele:

       1. Klicken Sie auf **[!UICONTROL Click to Browse]** , um die **[!UICONTROL Audience Targeting]** zu öffnen.

       1. Konfigurieren Sie die Zielgruppensegmente und -gruppen:

          * Um das erste Segment hinzuzufügen, suchen Sie das Segment im linken Bereich und aktivieren Sie das Kontrollkästchen neben dem Segmentnamen.

          * So fügen Sie Segmente zu einer vorhandenen Segmentgruppe hinzu:

            1. Klicken Sie auf die Segmentgruppe im rechten Bedienfeld.

            1. (Optional) Ändern Sie die Gruppenlogik nach Bedarf in **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** oder **[!UICONTROL Exclude All]**.

               **[!UICONTROL Include Any]** entspricht Benutzern in mindestens einem ausgewählten Segment; **[!UICONTROL Include All]** erfordert Mitgliedschaft in allen ausgewählten Segmenten.

               **[!UICONTROL Exclude All]** ist nicht für die erste Segmentgruppe verfügbar. Erstellen Sie bei einer Zielgruppe, die nur Ausschlüsse enthält, die Zielgruppe mithilfe von **[!UICONTROL Include Any]** und schließen Sie diese Zielgruppe aus, wenn Sie sie zu einer Platzierung in Ihrer DSP hinzufügen.

            1. Suchen Sie das neue Segment im linken Bereich und aktivieren Sie das Kontrollkästchen neben dem Segmentnamen. Wiederholen Sie diesen Vorgang für jedes weitere Segment.

               Die Segmentgruppe wird automatisch mit den neuen Segmenten aktualisiert.

          * Hinzufügen einer neuen Segmentgruppe:

            1. Klicken Sie im rechten Bedienfeld auf **[!UICONTROL + New Group]** .

            1. (Optional) Ändern Sie bei Bedarf die Logik zwischen der vorherigen Gruppe und der neuen Gruppe in **[!UICONTROL And]** oder **[!UICONTROL Or]**.

               **[!UICONTROL And]** müssen Benutzer die Bedingungen beider Gruppen erfüllen; **[!UICONTROL Or]** müssen mindestens die Bedingungen einer Gruppe erfüllen.

            1. Suchen Sie die Segmente für die neue Gruppe im linken Bereich und aktivieren Sie die Kontrollkästchen neben den Segmentnamen.

            1. (Optional) Ändern Sie die Gruppenlogik nach Bedarf in **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** oder **[!UICONTROL Exclude All]**.

       1. Klicken Sie auf **[!UICONTROL Create]**.

       1. Klicken Sie auf **[!UICONTROL Apply]**.

     * Gehen Sie bei geografischen Zielen wie folgt vor:

       1. Klicken Sie auf **[!UICONTROL Click to Browse]** , um Ihre [!UICONTROL Geo Targeting] zu öffnen, geben Sie eines oder mehrere der geografischen Ziele an und klicken Sie dann auf **[!UICONTROL Save]**.

          Postleitzahlziele verfügen über Massenbearbeitungsoptionen. Um mehrere Postleitzahlen einzufügen, klicken Sie auf die Registerkarte **[!UICONTROL Paste postal codes]** , wählen Sie das Land aus, fügen Sie Postleitzahlen ein oder geben Sie sie durch Kommas oder separate Zeilen getrennt ein und klicken Sie dann auf **[!UICONTROL Include All]**. Um eine enthaltene Postleitzahl zu entfernen, halten Sie den Cursor über dem Ziel und klicken Sie auf ![Entfernen](/help/creative/assets/delete.png "Entfernen") **[!UICONTROL Remove]**.

       1. (Optional) Um mehrere Zielknoten zu erstellen, wenn mehrere geografische Ziele angegeben sind, wählen Sie **[!UICONTROL Split targets to create nodes]** aus.

          Diese Funktion erstellt für jedes angegebene geografische Ziel einen separaten Zielknoten (mit separaten kreativen Bundles). Wenn Sie die Ziele nicht aufteilen, muss der Benutzer zu allen angegebenen Speicherorten gehören (eine [!DNL Boolean] `AND`).

       1. Klicken Sie auf **[!UICONTROL Apply]**.

     * Für ein Ziel für die Datenübergabe können Sie optional den Datenübergabeschlüssel anpassen, einen einzelnen Datenübergabewert eingeben und dann auf &quot;**[!UICONTROL Apply]**&quot; klicken.

       Der standardmäßige Datenübergabeschlüssel wird im Feld &quot;**[!UICONTROL Data Pass]**&quot; im Abschnitt &quot;**[!UICONTROL Advanced]**&quot; von [Allgemeine Erlebniseinstellungen“ &#x200B;](experience-settings-targeting.md). Passen Sie bei Bedarf den Schlüssel für die Zielgruppe an.

     * Wählen Sie für ein Pixel-Ziel für die erneute Zielgruppenbestimmung ein einzelnes Pixel für die erneute Zielgruppenbestimmung aus und geben Sie die Werte für die Attribute des Pixels an, die zur Anzeige für die Kreativen erforderlich sind. Klicken Sie dann auf **[!UICONTROL Apply]**.

       Die verfügbaren Attribute werden in den [Einstellungen für Retargeting](/help/creative/pixels/retargeting-pixel-manage.md) konfiguriert.

     * Gehen Sie für Geräteziele wie folgt vor:

       1. Wählen Sie die Ziele aus.

       1. (Optional) Um mehrere Zielknoten zu erstellen, wenn mehrere geografische Ziele angegeben sind, wählen Sie **[!UICONTROL Split targets to create nodes]** aus.

          Diese Funktion erstellt für jedes angegebene geografische Ziel einen separaten Zielknoten (mit separaten kreativen Bundles). Wenn Sie die Ziele nicht aufteilen, muss der Benutzer zu allen angegebenen Speicherorten gehören (eine [!DNL Boolean] `AND`).

       1. (Optional) Um mehrere Zielknoten zu erstellen, wenn mehrere geografische Ziele angegeben sind, wählen Sie **[!UICONTROL Split targets to create nodes]** aus.

       1. Klicken Sie auf **[!UICONTROL Apply]**.

1. (Optional) Geben Sie einen benutzerdefinierten Verzweigungsnamen für eine benutzerdefinierte Verzweigung an.

   Standardmäßig werden benutzerdefinierte Verzweigungen mit den angewendeten Zielen gekennzeichnet.

   Es kann kein benutzerdefinierter Verzweigungsname für eine Verzweigung des Typs „Alle“ oder „Alle anderen“ erstellt werden.

   1. Halten Sie den Cursor über den Zielknoten und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**.

   1. Geben Sie den **[!UICONTROL Node Name]** ein, und klicken Sie dann auf **[!UICONTROL Save]**.

1. (Optional) [Weisen Sie dem neuen Zielknoten und &#x200B;](experience-assign-creative-bundles.md#manual-editor) Knoten „Alles andere“ kreative Bundles zu.

1. (Optional) [Einen gleichrangigen Zielknoten hinzufügen](experience-target-node-add-sibling.md#manual-editor) des angegebenen Zieltyps.

## Erlebnis speichern {#save}

Die folgenden Schritte gelten für beide Editoren.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Fügen Sie einen Zielknoten zur endgültigen Ebene hinzu](experience-target-node-add-final.md)
>* [Fügen Sie zwischen Knoten einen gleichrangigen Zielknoten hinzu](experience-target-node-add-sibling.md)
>* [Kopieren Sie untergeordnete Knoten und Kreative auf derselben Ebene in einen anderen Knoten](experience-target-node-copy.md)
>* [Zuweisen von Kreativen zu einem endgültigen Knoten](experience-assign-creative-bundles.md)
>* [Löschen eines Zielknotens oder eines kreativen Blattknotens](/help/creative/experiences/experience-target-node-delete.md)
>* [Erstellen eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-create-targeting.md)
>* [Bearbeiten eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-edit-targeting.md)
>* [Einstellungen für zielgerichtete Erlebnisse](experience-settings-targeting.md)
