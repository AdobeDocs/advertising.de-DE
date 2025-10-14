---
title: Hinzufügen eines Zielknotens zur letzten Ebene eines Erlebnisses
description: Erfahren Sie, wie Sie einen Zielknoten zur endgültigen Zielebene eines Anzeigenerlebnisses hinzufügen.
feature: Creative Experiences
exl-id: 3ff657d5-bad1-47f4-a3ec-9ea678fd3c9d
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---

# Hinzufügen eines Zielknotens zur letzten Ebene eines Erlebnisses

*Nur Erlebnisse mit Targeting mit Entscheidungsbäumen*

Wenn Sie einen Zielknoten zur untersten Ebene des Erlebnisses hinzufügen - sei es den Stammknoten „Alle“, einen zielspezifischen Knoten oder einen „Alles andere“-Knoten - definieren Sie das Ziel direkt und müssen keinen gleichrangigen Knoten erstellen. Durch Hinzufügen eines Knotens auf unterster Ebene werden der Zielknoten und ein zusätzlicher Knoten „Alles andere“ auf derselben Ebene erstellt.

>[!NOTE]
>
>Informationen zum Einfügen eines Zielknotens zwischen vorhandenen Ebenen eines Entscheidungsbaums finden Sie unter &quot;[&#x200B; eines Zielknotens zwischen Knoten in einem Erlebnis einfügen](experience-target-node-add-inner.md).

<!-- 1. [ways to get to the decision tree] -->

1. Klicken Sie unter dem Knoten, an dem Sie das Ziel einfügen möchten, auf ![Hinzufügen](/help/creative/assets/add.png "Hinzufügen") und wählen Sie dann **[!UICONTROL Insert New Target]** aus.

1. Geben Sie die Ziele an:

   * Wählen Sie für Zielgruppenziele **[!UICONTROL Audience]** aus, klicken Sie auf **[!UICONTROL Click to Browse]** , um Ihre [!UICONTROL Audience Targeting] Optionen zu öffnen, und führen Sie dann die folgenden Schritte aus:

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

   * Wählen Sie für geografische Ziele eine einzelne geografische Kategorie aus (z. B. [!UICONTROL Geo: Country]), und führen Sie dann die folgenden Schritte aus:

      1. Klicken Sie auf **[!UICONTROL Click to Browse]** , um Ihre [!UICONTROL Geo Targeting] zu öffnen, geben Sie eines oder mehrere der geografischen Ziele an und klicken Sie dann auf **[!UICONTROL Save]**.

         Postleitzahlziele verfügen über Massenbearbeitungsoptionen. Um mehrere Postleitzahlen einzufügen, klicken Sie auf die Registerkarte **[!UICONTROL Paste postal codes]** , wählen Sie das Land aus, fügen Sie Postleitzahlen ein oder geben Sie sie durch Kommas oder separate Zeilen getrennt ein und klicken Sie dann auf **[!UICONTROL Include All]**. Um eine enthaltene Postleitzahl zu entfernen, halten Sie den Cursor über dem Ziel und klicken Sie auf ![Entfernen](/help/creative/assets/delete.png "Entfernen") **[!UICONTROL Remove]**.

      1. (Optional) Um mehrere Zielknoten zu erstellen, wenn mehrere geografische Ziele angegeben sind, wählen Sie **[!UICONTROL Split targets to create nodes]** aus.

         Diese Funktion erstellt für jedes angegebene geografische Ziel einen separaten Zielknoten (mit separaten kreativen Bundles). Wenn Sie die Ziele nicht aufteilen, muss der Benutzer zu allen angegebenen Speicherorten gehören (eine [!DNL Boolean] `AND`).

      1. Klicken Sie auf **[!UICONTROL Apply]**.

   * Wählen Sie für ein Ziel für die Datenübergabe &quot;**[!UICONTROL Data Pass]**&quot; aus, passen Sie optional den Datenübergabeschlüssel an, geben Sie einen einzelnen Datenübergabewert ein und klicken Sie dann auf **[!UICONTROL Apply]**.

   Ein Standardwert für den Schlüssel im Schlüssel-Wert-Paar ist bereits im Feld **[!UICONTROL Data Pass]** im Abschnitt [!UICONTROL Advanced] der [Erlebniseinstellungen](experience-settings-targeting.md) festgelegt. Sie können optional den Schlüssel anpassen.

   * Wählen Sie für ein Pixel-Ziel für die erneute Zielgruppenbestimmung **[!UICONTROL RT Pixel]**, wählen Sie ein einzelnes Pixel für die erneute Zielgruppenbestimmung aus und geben Sie die Werte für alle Attribute des Pixels an, die zur Anzeige für die Kreativen erforderlich sind, und klicken Sie dann auf **[!UICONTROL Apply]**.

     Die Attribute für das Retargeting-Pixel werden unter [Einstellungen für Retargeting-Pixel](/help/creative/pixels/retargeting-pixel-manage.md) konfiguriert.

   * Gehen Sie für Geräteziele wie folgt vor:

      1. Wählen Sie eine einzelne Zielkategorie (**[!UICONTROL Device: Type]**, **[!UICONTROL Device: OS]** oder **[!UICONTROL Device: Browser]**) und wählen Sie dann die Ziele aus.

      1. (Optional) Um mehrere Zielknoten zu erstellen, wenn mehrere geografische Ziele angegeben sind, wählen Sie **[!UICONTROL Split targets to create nodes]** aus.

         Diese Funktion erstellt für jedes angegebene geografische Ziel einen separaten Zielknoten (mit separaten kreativen Bundles). Wenn Sie die Ziele nicht aufteilen, muss der Benutzer zu allen angegebenen Speicherorten gehören (eine [!DNL Boolean] `AND`).

      1. Klicken Sie auf **[!UICONTROL Apply]**.

1. (Optional) Geben Sie einen benutzerdefinierten Verzweigungsnamen für eine benutzerdefinierte Verzweigung an.

   Standardmäßig werden benutzerdefinierte Verzweigungen mit den angewendeten Zielen gekennzeichnet.

   Es kann kein benutzerdefinierter Verzweigungsname für eine Verzweigung des Typs „Alle“ oder „Alle anderen“ erstellt werden.

   1. Halten Sie den Cursor über den Zielknoten und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Edit Name]**.

   1. Geben Sie den **[!UICONTROL Node Name]** ein, und klicken Sie dann auf **[!UICONTROL Save]**.

1. Führen Sie einen der folgenden Schritte aus:

   * (Optional) [Weisen Sie dem neuen &#x200B;](experience-assign-creative-bundles.md) und dem Knoten „Alles andere“ Kreative zu.

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
