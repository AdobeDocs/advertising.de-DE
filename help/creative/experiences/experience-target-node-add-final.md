---
title: Hinzufügen eines Zielknotens zur letzten Ebene eines Erlebnisses
description: Erfahren Sie, wie Sie einen Zielknoten zur endgültigen Zielebene eines Anzeigenerlebnisses hinzufügen.
feature: Creative Experiences
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 0%

---

# Hinzufügen eines Zielknotens zur letzten Ebene eines Erlebnisses

*Nur Erlebnisse mit Targeting mit Entscheidungsbäumen*
*Geschlossene Beta-Version*

Wenn Sie einen Zielknoten zur untersten Ebene des Erlebnisses hinzufügen - sei es den Stammknoten „Alle“, einen zielspezifischen Knoten oder einen „Alles andere“-Knoten - definieren Sie das Ziel direkt, ohne einen gleichrangigen Knoten erstellen zu müssen. Dadurch werden der Zielknoten und ein zusätzlicher Knoten „Alles andere“ auf derselben Ebene erstellt.

>[!NOTE]
>
>Informationen zum Einfügen eines Zielknotens zwischen vorhandenen Ebenen eines Entscheidungsbaums finden Sie unter &quot;[ eines Zielknotens zwischen Knoten in einem Erlebnis einfügen](experience-target-node-add-inner.md).

<!-- 1. [ways to get to the decision tree] -->

1. Klicken Sie unter dem Knoten, an dem Sie das Ziel einfügen möchten, auf ![Hinzufügen](/help/creative/assets/add.png "Hinzufügen") und wählen Sie dann **[!UICONTROL Insert New Target]** aus.

1. Geben Sie die Ziele an:

   * Wählen Sie für das Adobe von Zielgruppenzielen &quot;**[!UICONTROL Adobe Audience]**&quot; aus und führen Sie dann folgende Schritte aus:

      1. Klicken Sie auf **[!UICONTROL Click to Browse]** , um Ihre [!UICONTROL Audience Targeting] Optionen zu öffnen, öffnen Sie die Registerkarte **[!UICONTROL Adobe Segments]** , geben Sie ein oder mehrere [!DNL Adobe] Zielgruppenziele des Werbetreibenden an und klicken Sie dann auf **[!UICONTROL Create]**.

      1. (Optional) Um mehrere Zielknoten zu erstellen, wenn mehrere Zielgruppen angegeben sind, wählen Sie **[!UICONTROL Split targets to create nodes]** aus.

         Dadurch wird für jede angegebene Zielgruppe ein separater Zielknoten (mit separaten kreativen Bundles) erstellt. Wenn Sie die Ziele nicht aufteilen, muss der Benutzer allen angegebenen Zielgruppen angehören.

      1. Klicken Sie auf **[!UICONTROL Apply]**.

   * Wählen Sie für geografische Ziele eine einzelne geografische Kategorie aus (z. B. [!UICONTROL Geo: Country]), und führen Sie dann die folgenden Schritte aus:

      1. Klicken Sie auf **[!UICONTROL Click to Browse]** , um Ihre [!UICONTROL Geo Targeting] zu öffnen, geben Sie eines oder mehrere der geografischen Ziele an und klicken Sie dann auf **[!UICONTROL Save]**.

         Postleitzahlziele verfügen über Massenbearbeitungsoptionen. Um mehrere Postleitzahlen einzufügen, klicken Sie auf die Registerkarte **[!UICONTROL Paste postal codes]** , wählen Sie das Land aus, fügen Sie Postleitzahlen ein oder geben Sie sie durch Kommas oder separate Zeilen getrennt ein und klicken Sie dann auf **[!UICONTROL Include All]**. Um eine enthaltene Postleitzahl zu entfernen, halten Sie den Cursor über dem Ziel und klicken Sie auf ![Entfernen](/help/creative/assets/delete.png "Entfernen") **[!UICONTROL Remove]**.

      1. (Optional) Um mehrere Zielknoten zu erstellen, wenn mehrere geografische Ziele angegeben sind, wählen Sie **[!UICONTROL Split targets to create nodes]** aus.

         Dadurch wird ein separater Zielknoten (mit separaten kreativen Bundles) für jedes angegebene geografische Ziel erstellt. Wenn Sie die Ziele nicht aufteilen, muss der Benutzer zu allen angegebenen Speicherorten gehören.

      1. Klicken Sie auf **[!UICONTROL Apply]**.

   * Wählen Sie als Ziel für die Datenübergabe &quot;**[!UICONTROL Data Pass]**&quot; aus, geben Sie einen einzelnen Datenübergabewert ein und klicken Sie dann auf &quot;**[!UICONTROL Apply]**&quot;.

   Der Schlüssel für das Schlüssel-Wert-Paar ist bereits im Feld **[!UICONTROL Data Pass]** im Abschnitt [!UICONTROL Advanced] der [Erlebniseinstellungen](experience-settings-targeting.md) festgelegt.

   * Wählen Sie für ein Pixel-Ziel für die erneute Zielgruppenbestimmung **[!UICONTROL RT Pixel]**, wählen Sie ein einzelnes Pixel für die erneute Zielgruppenbestimmung und die erforderlichen Werte für alle Attribute des Pixels aus, die vorhanden sein müssen, um den Kreativen angezeigt zu werden, und klicken Sie dann auf **[!UICONTROL Apply]**.

     Die Attribute für das Retargeting-Pixel werden unter [Einstellungen für Retargeting-Pixel](/help/creative/pixels/retargeting-pixel-manage.md) konfiguriert.

   * Gehen Sie für Geräteziele wie folgt vor:

      1. Wählen Sie eine einzelne Zielkategorie (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** oder **[!UICONTROL Device: Browser]**) und wählen Sie dann die Ziele aus.

      1. (Optional) Um mehrere Zielknoten zu erstellen, wenn mehrere geografische Ziele angegeben sind, wählen Sie **[!UICONTROL Split targets to create nodes]** aus.

         Dadurch wird ein separater Zielknoten (mit separaten kreativen Bundles) für jedes angegebene geografische Ziel erstellt. Wenn Sie die Ziele nicht aufteilen, muss der Benutzer zu allen angegebenen Speicherorten gehören.

      1. Klicken Sie auf **[!UICONTROL Apply]**.

1. Führen Sie einen der folgenden Schritte aus:

   * (Optional) [Weisen Sie dem neuen ](experience-assign-creative-bundles.md) und dem Knoten „Alles andere“ Kreative zu.

   * (Optional) So speichern Sie das Erlebnis:

      1. Klicken Sie auf **[!UICONTROL Save]** und dann auf **[!UICONTROL OK]**.

      1. (Wenn jeder Knoten auf der untersten Ebene nicht mindestens einen Kreativen enthält): Führen Sie einen der folgenden Schritte aus:

         * Um das Erlebnis ohne alle erforderlichen kreativen Bundles zu speichern, klicken Sie auf **[!UICONTROL Save as Draft]**.

           Sie können kein Anzeigen-Tag für ein Entwurfserlebnis erstellen.

         * Um jedem Ziel, dem noch kein Kreativ-Bundle zugewiesen wurde, das Standardkreativ-Paket zuzuweisen, klicken Sie auf **[!UICONTROL Assign Default Creatives]**. Nachdem Sie die aktualisierte Baumstruktur mit den standardmäßig zugewiesenen Kreativen überprüft haben, klicken Sie auf **[!UICONTROL Save]** und **[!UICONTROL OK]**.

         * Um mit der Bearbeitung des Entscheidungsbaums fortzufahren, klicken Sie auf **[!UICONTROL Continue Edit]**.

>[!MORELIKETHIS]
>
>* [Fügen Sie zwischen Knoten einen Zielknoten ein](experience-target-node-add-inner.md)
>* [Fügen Sie zwischen Knoten einen gleichrangigen Zielknoten hinzu](experience-target-node-add-sibling.md)
>* [Kopieren Sie untergeordnete Knoten und Kreative auf derselben Ebene in einen anderen Knoten](experience-target-node-copy.md)
>* [Zuweisen von Kreativen zu einem endgültigen Knoten](experience-assign-creative-bundles.md)
>* [Löschen eines Zielknotens oder eines kreativen Blattknotens](/help/creative/experiences/experience-target-node-delete.md)
>* [Erstellen eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-create-targeting.md)
>* [Bearbeiten eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-edit-targeting.md)
>* [Einstellungen für zielgerichtete Erlebnisse](experience-settings-targeting.md)
