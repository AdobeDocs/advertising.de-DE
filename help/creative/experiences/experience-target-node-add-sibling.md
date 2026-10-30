---
title: Hinzufügen eines gleichrangigen Zielknotens zwischen Knoten in einem Erlebnis
description: Erfahren Sie, wie Sie einen gleichrangigen Knoten zu jedem Knoten hinzufügen, der ein Ziel hat oder sich auf derselben Ebene wie ein Knoten mit einem Ziel befindet.
feature: Creative Experiences
exl-id: 915fd399-1c55-49af-94ed-cf49a4154a53
TQID: 'https://experienceleague.adobe.com/fRdbFmlTUBzHHkmrfonZ0COJ7-1x6t2HRczwlcVb99o'
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
source-wordcount: '1151'
ht-degree: 0%
---
# Hinzufügen eines gleichrangigen Zielknotens zwischen Knoten in einem Erlebnis

*Nur Erlebnisse mit Targeting mit Entscheidungsbäumen*

Sie können einen gleichrangigen Knoten zu jedem Knoten hinzufügen, der ein Ziel hat oder sich auf derselben Ebene wie ein Knoten mit einem Ziel befindet.

## Verwenden des KI-gesteuerten Editors (Beta) {#ai-editor}

Während Sie das Erlebnis [erstellen](experience-create-targeting.md#ai-editor) oder [bearbeiten](experience-edit-targeting.md#ai-editor) können Sie dem KI-Agenten das neue gleichrangige Ziel beschreiben. Identifizieren Sie den übergeordneten Zweig und die Zielwerte und überprüfen Sie das Ergebnis. So fügen Sie das gleichrangige Element direkt in der Arbeitsfläche hinzu:

1. Halten Sie den Cursor über das übergeordnete Element der Knoten auf der Ebene, auf der Sie ein anderes gleichrangiges Element wünschen, und klicken Sie auf **[!UICONTROL +]**.

   Die Zielkategorie wird durch die vorhandene Ebene bestimmt und der Wertselektor wird für diese Kategorie geöffnet.

1. Geben Sie die Zielwerte für die Kategorie an:

   * Für Zielgruppenziele:

     * Um das erste Segment hinzuzufügen, suchen und wählen Sie das Zielgruppensegment aus.

     * So fügen Sie Segmente zu einer vorhandenen Segmentgruppe hinzu:

       1. Wählen Sie die Segmentgruppe aus.

       1. (Optional) Ändern Sie die Gruppenlogik nach Bedarf in **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** oder **[!UICONTROL Exclude All]**.

          **[!UICONTROL Include Any]** entspricht Benutzern in mindestens einem ausgewählten Segment; **[!UICONTROL Include All]** erfordert Mitgliedschaft in allen ausgewählten Segmenten.

          **[!UICONTROL Exclude All]** ist nicht für die erste Segmentgruppe verfügbar. Erstellen Sie bei einer Zielgruppe, die nur Ausschlüsse enthält, die Zielgruppe mithilfe von **[!UICONTROL Include Any]** und schließen Sie diese Zielgruppe aus, wenn Sie sie zu einer Platzierung in Ihrer DSP hinzufügen.

       1. Suchen und wählen Sie die zusätzlichen Segmente aus.

     * Hinzufügen einer neuen Segmentgruppe:

       1. Fügen Sie eine Gruppe hinzu.

       1. (Optional) Ändern Sie bei Bedarf die Logik zwischen der vorherigen Gruppe und der neuen Gruppe in **[!UICONTROL And]** oder **[!UICONTROL Or]**.

          **[!UICONTROL And]** müssen Benutzer die Bedingungen beider Gruppen erfüllen; **[!UICONTROL Or]** müssen mindestens die Bedingungen einer Gruppe erfüllen.

       1. Suchen und wählen Sie die Segmente für die neue Gruppe aus.

       1. (Optional) Ändern Sie die Gruppenlogik nach Bedarf in **[!UICONTROL Include Any]**, **[!UICONTROL Include All]** oder **[!UICONTROL Exclude All]**.

   * Für geografische Ziele:

     * Wählen Sie die Standorte innerhalb der geografischen Kategorie auf der vorhandenen Ebene aus, z. B. Länder, Regionen oder Städte.

     * Wählen Sie für Zielgruppen der Postleitzahl das Land aus und geben Sie die einzuschließenden Postleitzahlen ein. Wenn Sie mehrere Postleitzahlen in großen Mengen eingeben möchten, trennen Sie sie durch Kommas oder setzen Sie jede Postleitzahl in eine separate Zeile.

   * Geben Sie für Zielgruppen für die Datenübergabe den Schlüssel und den Wert ein, die übereinstimmen sollen.

     Der standardmäßige Datenübergabeschlüssel wird im Feld &quot;**[!UICONTROL Data Pass]**&quot; im Abschnitt &quot;**[!UICONTROL Advanced]**&quot; von [Allgemeine Erlebniseinstellungen“ ](experience-settings-targeting.md). Passen Sie bei Bedarf den Schlüssel für die Zielgruppe an.

   * Wählen Sie für das Retargeting von Pixel-Zielen das Retargeting-Pixel aus und geben Sie die Werte für alle Pixel-Attribute an, die erforderlich sind, um die Kreativen anzuzeigen.

     Die verfügbaren Attribute werden in den [Einstellungen für Retargeting](/help/creative/pixels/retargeting-pixel-manage.md) konfiguriert.

   * Wählen Sie für Geräteziele die Werte innerhalb der Gerätekategorie auf der vorhandenen Ebene aus: Gerätetypen, Betriebssysteme oder Browser.

1. (Falls verfügbar; optional) Wählen Sie **[!UICONTROL Split Nodes]** aus, um für jeden ausgewählten Wert einen separaten Zielknoten mit eigenen Zuweisungen für das Kreativ-Bundle zu erstellen. Andernfalls werden die ausgewählten Werte in einem Zielknoten gruppiert.

1. Klicken Sie auf **[!UICONTROL Add Node]**.

1. (Optional) Um den neuen Knoten umzubenennen, klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**, geben Sie den **[!UICONTROL Node Name]** ein, und klicken Sie dann auf **[!UICONTROL Save]**.

1. [Kreative Bundles zuweisen](experience-assign-creative-bundles.md#ai-editor) wenn der neue Knoten ein endgültiger Knoten ist, und [Erlebnis speichern](#save).

## Verwenden des manuellen Editors {#manual-editor}

[Öffnen Sie den manuellen Editor](experience-edit-targeting.md#experience-open) bevor Sie diese Schritte ausführen.

1. Klicken Sie über dem Knoten, dem Sie den gleichrangigen Knoten hinzufügen möchten, auf ![Hinzufügen](/help/creative/assets/add.png "Hinzufügen") und wählen Sie dann **[!UICONTROL Insert Sibling Target]** aus.

1. Geben Sie die Zielwerte für die Kategorie an:

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

   * Für Datenübergabeziele können Sie optional den Datenübergabeschlüssel anpassen, einen einzelnen Datenübergabewert eingeben und dann auf &quot;**[!UICONTROL Apply]**&quot; klicken.

     Der standardmäßige Datenübergabeschlüssel wird im Feld &quot;**[!UICONTROL Data Pass]**&quot; im Abschnitt &quot;**[!UICONTROL Advanced]**&quot; von [Allgemeine Erlebniseinstellungen“ ](experience-settings-targeting.md). Passen Sie bei Bedarf den Schlüssel für die Zielgruppe an.

   * Wählen Sie für die erneute Zielgruppenbestimmung von Pixelzielen das zu verwendende Retargeting-Pixel und die erforderlichen Werte für eines der Pixelattribute aus, die vorhanden sein müssen, um den Kreativen angezeigt zu werden. Klicken Sie dann auf **[!UICONTROL Apply]**.

     Die verfügbaren Attribute werden in den [Einstellungen für Retargeting](/help/creative/pixels/retargeting-pixel-manage.md) konfiguriert.

   * Gehen Sie für Geräteziele wie folgt vor:

     1. Wählen Sie die Ziele aus.

     1. (Optional) Um mehrere Zielknoten zu erstellen, wenn mehrere geografische Ziele angegeben sind, wählen Sie **[!UICONTROL Split targets to create nodes]** aus.

        Diese Funktion erstellt für jedes angegebene geografische Ziel einen separaten Zielknoten (mit separaten kreativen Bundles). Wenn Sie die Ziele nicht aufteilen, muss der Benutzer zu allen angegebenen Speicherorten gehören (eine [!DNL Boolean] `AND`).

     1. Klicken Sie auf **[!UICONTROL Apply]**.

1. (Optional) Geben Sie einen benutzerdefinierten Verzweigungsnamen für eine benutzerdefinierte Verzweigung an.

   Standardmäßig werden benutzerdefinierte Verzweigungen mit den angewendeten Zielen gekennzeichnet.

   Es kann kein benutzerdefinierter Verzweigungsname für eine Verzweigung des Typs „Alle“ oder „Alle anderen“ erstellt werden.

   1. Halten Sie den Cursor über den Zielknoten und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**.

   1. Geben Sie den **[!UICONTROL Node Name]** ein, und klicken Sie dann auf **[!UICONTROL Save]**.

1. (Optional) [Zuweisen von kreativen Bundles](experience-assign-creative-bundles.md#manual-editor) zum neuen Zielknoten.

## Erlebnis speichern {#save}

Die folgenden Schritte gelten für beide Editoren.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Fügen Sie einen Zielknoten zur endgültigen Ebene hinzu](experience-target-node-add-final.md)
>* [Fügen Sie zwischen Knoten einen Zielknoten ein](experience-target-node-add-inner.md)
>* [Kopieren Sie untergeordnete Knoten und Kreative auf derselben Ebene in einen anderen Knoten](experience-target-node-copy.md)
>* [Zuweisen von Kreativen zu einem endgültigen Knoten](experience-assign-creative-bundles.md)
>* [Löschen eines Zielknotens oder eines kreativen Blattknotens](/help/creative/experiences/experience-target-node-delete.md)
>* [Erstellen eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-create-targeting.md)
>* [Bearbeiten eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-edit-targeting.md)
>* [Einstellungen für zielgerichtete Erlebnisse](experience-settings-targeting.md)
