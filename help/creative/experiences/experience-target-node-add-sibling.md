---
title: Hinzufügen eines gleichrangigen Zielknotens zwischen Knoten in einem Erlebnis
description: Erfahren Sie, wie Sie einen gleichrangigen Knoten zu jedem Knoten hinzufügen, der ein Ziel hat oder sich auf derselben Ebene wie ein Knoten mit einem Ziel befindet.
feature: Creative Experiences
exl-id: 915fd399-1c55-49af-94ed-cf49a4154a53
source-git-commit: f71747a4973ec3f3e2c3a8a5913d27311849883c
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Hinzufügen eines gleichrangigen Zielknotens zwischen Knoten in einem Erlebnis

*Nur Erlebnisse mit Targeting mit Entscheidungsbäumen*
*Geschlossene Beta-Version*

Sie können einen gleichrangigen Knoten zu jedem Knoten hinzufügen, der ein Ziel hat oder sich auf derselben Ebene wie ein Knoten mit einem Ziel befindet.

<!-- 1. Open the decision tree:


In a new experience


In an existing experience,
 -->

1. Klicken Sie über dem Knoten, dem Sie den gleichrangigen Knoten hinzufügen möchten, auf ![Hinzufügen](/help/creative/assets/add.png "Hinzufügen") und wählen Sie dann **[!UICONTROL Insert Sibling Target]** aus.

1. Geben Sie die Ziele an:

   * Gehen Sie bei Audience-Zielen wie folgt vor:

      1. Klicken Sie auf **[!UICONTROL Click to Browse]** , um Ihre [!UICONTROL Audience Targeting] zu öffnen, und führen Sie dann folgende Schritte aus:

         * Um das erste Segment hinzuzufügen, suchen Sie das Segment im linken Bereich und aktivieren Sie das Kontrollkästchen neben dem Segmentnamen.

         * So fügen Sie ein Segment zu einer vorhandenen Segmentgruppe hinzu:

            1. Klicken Sie auf die Segmentgruppe im rechten Bedienfeld.

            1. (Optional) Ändern Sie die Gruppenlogik nach Bedarf in *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* oder *[!UICONTROL Exclude All]*.

               *[!UICONTROL Exclude All]* ist nicht für die erste Segmentgruppe verfügbar. Erstellen Sie für eine Zielgruppe, die nur Ausschlüsse enthält, diese Zielgruppe als *[!UICONTROL Include Any]* und schließen Sie diese Zielgruppe aus, wenn Sie sie zu einer Platzierung in Ihrer DSP hinzufügen.

            1. Suchen Sie das neue Segment im linken Bereich und aktivieren Sie das Kontrollkästchen neben dem Segmentnamen.

               Die Segmentgruppe wird automatisch mit dem neuen Segment aktualisiert.

         * Hinzufügen einer neuen Segmentgruppe:

         1. Klicken Sie im rechten Bedienfeld auf **[!UICONTROL + New Group]** .

         1. (Optional) Ändern Sie bei Bedarf die Logik zwischen der vorherigen Gruppe und der neuen Gruppe in *[!UICONTROL And]* oder *[!UICONTROL Or]*.

         1. Suchen Sie die Segmente für die neue Gruppe im linken Bereich und aktivieren Sie die Kontrollkästchen neben den Segmentnamen.

         1. (Optional) Ändern Sie die Gruppenlogik nach Bedarf in *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* oder *[!UICONTROL Exclude All]*.

      1. Klicken Sie auf **[!UICONTROL Create]**.

      1. Klicken Sie auf **[!UICONTROL Apply]**.

   * Gehen Sie bei geografischen Zielen wie folgt vor:

      1. Klicken Sie auf **[!UICONTROL Click to Browse]** , um Ihre [!UICONTROL Geo Targeting] zu öffnen, geben Sie eines oder mehrere der geografischen Ziele an und klicken Sie dann auf **[!UICONTROL Save]**.

         Postleitzahlziele verfügen über Massenbearbeitungsoptionen. Um mehrere Postleitzahlen einzufügen, klicken Sie auf die Registerkarte **[!UICONTROL Paste postal codes]** , wählen Sie das Land aus, fügen Sie Postleitzahlen ein oder geben Sie sie durch Kommas oder separate Zeilen getrennt ein und klicken Sie dann auf **[!UICONTROL Include All]**. Um eine enthaltene Postleitzahl zu entfernen, halten Sie den Cursor über dem Ziel und klicken Sie auf ![Entfernen](/help/creative/assets/delete.png "Entfernen") **[!UICONTROL Remove]**.

      1. (Optional) Um mehrere Zielknoten zu erstellen, wenn mehrere geografische Ziele angegeben sind, wählen Sie **[!UICONTROL Split targets to create nodes]** aus.

         Diese Funktion erstellt für jedes angegebene geografische Ziel einen separaten Zielknoten (mit separaten kreativen Bundles). Wenn Sie die Ziele nicht aufteilen, muss der Benutzer zu allen angegebenen Speicherorten gehören (eine [!DNL Boolean] `AND`).

      1. Klicken Sie auf **[!UICONTROL Apply]**.

   * Für Datenübergabeziele können Sie optional den Datenübergabeschlüssel anpassen, einen einzelnen Datenübergabewert eingeben und dann auf &quot;**[!UICONTROL Apply]**&quot; klicken.

     Ein Standardwert für den Schlüssel im Schlüssel-Wert-Paar ist bereits im Feld **[!UICONTROL Data Pass]** im Abschnitt [!UICONTROL Advanced] der [Erlebniseinstellungen](experience-settings-targeting.md) festgelegt. Sie können optional den Schlüssel anpassen.

   * Wählen Sie für die erneute Zielgruppenbestimmung von Pixelzielen das zu verwendende Retargeting-Pixel und die erforderlichen Werte für eines der Pixelattribute aus, die vorhanden sein müssen, um den Kreativen angezeigt zu werden. Klicken Sie dann auf **[!UICONTROL Apply]**.

     Die Attribute für das Retargeting-Pixel werden unter [Einstellungen für Retargeting-Pixel](/help/creative/pixels/retargeting-pixel-manage.md) konfiguriert.

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

1. Führen Sie einen der folgenden Schritte aus:

   * (Optional) [Weisen Sie dem neuen Zielknoten ](experience-assign-creative-bundles.md)Kreative“ zu.

   * (Optional) So speichern Sie das Erlebnis:

      1. Klicken Sie auf **[!UICONTROL Save]** und dann auf **[!UICONTROL OK]**.

      1. (Wenn jeder Knoten auf der untersten Ebene nicht mindestens einen Kreativen enthält): Führen Sie einen der folgenden Schritte aus:

         * Um das Erlebnis ohne alle erforderlichen Kreativ-Bundles zu speichern, klicken Sie auf **[!UICONTROL Save as Draft]**.

           Sie können kein Anzeigen-Tag für ein Entwurfserlebnis erstellen.

         * Um jedem Ziel, dem noch kein Kreativ-Bundle zugewiesen wurde, das Standardkreativ-Paket zuzuweisen, klicken Sie auf **[!UICONTROL Assign Default Creatives]**. Nachdem Sie die aktualisierte Baumstruktur mit den standardmäßig zugewiesenen Kreativen überprüft haben, klicken Sie auf **[!UICONTROL Save]** und **[!UICONTROL OK]**.

         * Um mit der Bearbeitung des Entscheidungsbaums fortzufahren, klicken Sie auf **[!UICONTROL Continue Edit]**.

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
