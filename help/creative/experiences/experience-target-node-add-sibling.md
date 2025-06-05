---
title: Hinzufügen eines gleichrangigen Zielknotens zwischen Knoten in einem Erlebnis
description: Erfahren Sie, wie Sie einen gleichrangigen Knoten zu jedem Knoten hinzufügen, der ein Ziel hat oder sich auf derselben Ebene wie ein Knoten mit einem Ziel befindet.
feature: Creative Experiences
exl-id: 915fd399-1c55-49af-94ed-cf49a4154a53
source-git-commit: dac7252e118e467fbc924cf162756d7ecd69892f
workflow-type: tm+mt
source-wordcount: '587'
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

   * Gehen Sie bei Adobe-Zielgruppenzielen wie folgt vor:

      1. Klicken Sie auf **[!UICONTROL Click to Browse]** , um Ihre [!UICONTROL Audience Targeting] Optionen zu öffnen, öffnen Sie die Registerkarte **[!UICONTROL Adobe Segments]** , geben Sie ein oder mehrere [!DNL Adobe] Zielgruppenziele des Werbetreibenden an und klicken Sie dann auf **[!UICONTROL Save]**.

      1. (Optional) Um mehrere Zielknoten zu erstellen, wenn mehrere Zielgruppen angegeben sind, wählen Sie **[!UICONTROL Split targets to create nodes]** aus.

         Diese Funktion erstellt für jede angegebene Zielgruppe einen separaten Zielknoten (mit separaten kreativen Bundles). Wenn Sie die Ziele nicht aufteilen, muss der Benutzer allen angegebenen Zielgruppen angehören.

      1. Klicken Sie auf **[!UICONTROL Apply]**.

   * Gehen Sie bei geografischen Zielen wie folgt vor:

      1. Klicken Sie auf **[!UICONTROL Click to Browse]** , um Ihre [!UICONTROL Geo Targeting] zu öffnen, geben Sie eines oder mehrere der geografischen Ziele an und klicken Sie dann auf **[!UICONTROL Save]**.

         Postleitzahlziele verfügen über Massenbearbeitungsoptionen. Um mehrere Postleitzahlen einzufügen, klicken Sie auf die Registerkarte **[!UICONTROL Paste postal codes]** , wählen Sie das Land aus, fügen Sie Postleitzahlen ein oder geben Sie sie durch Kommas oder separate Zeilen getrennt ein und klicken Sie dann auf **[!UICONTROL Include All]**. Um eine enthaltene Postleitzahl zu entfernen, halten Sie den Cursor über dem Ziel und klicken Sie auf ![Entfernen](/help/creative/assets/delete.png "Entfernen") **[!UICONTROL Remove]**.

      1. (Optional) Um mehrere Zielknoten zu erstellen, wenn mehrere geografische Ziele angegeben sind, wählen Sie **[!UICONTROL Split targets to create nodes]** aus.

         Diese Funktion erstellt für jedes angegebene geografische Ziel einen separaten Zielknoten (mit separaten kreativen Bundles). Wenn Sie die Ziele nicht aufteilen, muss der Benutzer zu allen angegebenen Speicherorten gehören.

      1. Klicken Sie auf **[!UICONTROL Apply]**.

   * Für Datenübergabeziele können Sie optional den Datenübergabeschlüssel anpassen, einen einzelnen Datenübergabewert eingeben und dann auf &quot;**[!UICONTROL Apply]**&quot; klicken.

     Ein Standardwert für den Schlüssel im Schlüssel-Wert-Paar ist bereits im Feld **[!UICONTROL Data Pass]** im Abschnitt [!UICONTROL Advanced] der [Erlebniseinstellungen](experience-settings-targeting.md) festgelegt. Sie können optional den Schlüssel anpassen.

   * Wählen Sie für die erneute Zielgruppenbestimmung von Pixelzielen das zu verwendende Retargeting-Pixel und die erforderlichen Werte für eines der Pixelattribute aus, die vorhanden sein müssen, um den Kreativen angezeigt zu werden. Klicken Sie dann auf **[!UICONTROL Apply]**.

     Die Attribute für das Retargeting-Pixel werden unter [Einstellungen für Retargeting-Pixel](/help/creative/pixels/retargeting-pixel-manage.md) konfiguriert.

   * Gehen Sie für Geräteziele wie folgt vor:

      1. Wählen Sie die Ziele aus.

      1. (Optional) Um mehrere Zielknoten zu erstellen, wenn mehrere geografische Ziele angegeben sind, wählen Sie **[!UICONTROL Split targets to create nodes]** aus.

         Diese Funktion erstellt für jedes angegebene geografische Ziel einen separaten Zielknoten (mit separaten kreativen Bundles). Wenn Sie die Ziele nicht aufteilen, muss der Benutzer zu allen angegebenen Speicherorten gehören.

      1. Klicken Sie auf **[!UICONTROL Apply]**.

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
