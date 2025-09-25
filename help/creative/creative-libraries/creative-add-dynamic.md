---
title: Hinzufügen dynamischer Kreativer zu einer Kreativbibliothek
description: Erfahren Sie, wie Sie einer Kreativbibliothek dynamische Kreative hinzufügen.
feature: Creative Dynamic Creatives
source-git-commit: f0bbbfb528000babbcb2c4c6915b62e81f477bda
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Hinzufügen dynamischer Kreativer zu einer Kreativbibliothek

Fügen Sie dynamische Kreative zu Ihren [kreativen Bibliotheken](creative-library-manage.md) hinzu, um sie mit dynamischen [Anzeigenerlebnissen](/help/creative/experiences/experience-about.md) zu verwenden. Sie können entweder eine einzelne statische HTML5-Anzeige oder dynamische HTML5-Anzeigen aus einer einzigen Anzeigenvorlage erstellen. Verwenden Sie für dynamische HTML5-Anzeigen Assets in angegebenen Katalogen, die aus Feed-Dateien erstellt wurden.

>[!PREREQUISITES]
>
>Bevor Sie einer Kreativbibliothek dynamische Kreative hinzufügen können, müssen Sie andere Schritte ausführen, z. B. die Anzeigenvorlage erstellen, Assets hochladen und (dynamische HTML5-Anzeigen) eine Feed-Vorlage und einen Katalog erstellen. Siehe &quot;[ für dynamische Anzeigen](/help/creative/introduction/workflow-dynamic-ads.md).“

<!-- This does't work for me 9/24 -- I still have to select a catalog:

## Add dynamic creatives using a static HTML5 ad template

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Dynamic Ad]**.

1. Specify the [dynamic ad settings](/help/creative/creative-libraries/creative-settings-dynamic.md#dynamic-ad-settings-static-html5):

   1. On the [!UICONTROL Basic Details] tab, specify the ad details and the clickURL.

   1. Click **[!UICONTROL Process]**.

   1. On the [!UICONTROL Attributes Details] tab, specify the dynamic ad attributes.

1. Click **[!UICONTROL Save]**.

-->

## Dynamische Kreative mithilfe einer dynamischen HTML5-Anzeigenvorlage hinzufügen

1. Führen Sie einen der folgenden Schritte aus:

   * Aus einer Kreativ-Bibliothek:

      1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

      1. Klicken Sie auf den Bibliotheksnamen.

      1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Dynamic Ad]**.

   * Aus einer Anzeigenvorlage:

      1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**.

      1. Halten Sie den Cursor über die Zeile mit der Anzeigenvorlage und klicken Sie auf **[!UICONTROL Create Dynamic Ad]**.

1. Geben Sie die [Einstellungen für dynamische Anzeigen](/help/creative/creative-libraries/creative-settings-dynamic.md) an:

   1. Geben Sie die grundlegenden Anzeigendetails an.

   1. Wählen Sie die Anzeigenvorlage aus, die für die Kreativen verwendet werden soll.

   1. Wählen Sie den Katalog aus, aus dem die Anzeigen erstellt werden sollen.

   1. Wählen Sie die Kriterien aus, für die Katalogzeilen zum Erstellen von Anzeigen verwendet werden sollen.

   1. Ordnen Sie jedes Attribut (dynamisches Anzeigenfeld) in der angegebenen Anzeigenvorlage einer Spalte in der angegebenen Feed-Datei (Katalogbeschriftung) zu oder geben Sie statische Werte ein.

   1. Klicken Sie auf **[!UICONTROL Continue]** , um eine Vorschau der zu generierenden Kreativen anzuzeigen. Sie können in der Vorschau einen der folgenden Schritte ausführen:

      * Um die Kreativen nach Katalog, Filterwert <!-- explain more--> Anzeigengröße zu filtern, verwenden Sie die Filter über dem Vorschaubereich.

      * So suchen Sie anhand der eindeutigen ID im Suchfeld unter dem Vorschaubereich nach einem Produkt.

      * Um die angezeigten Spalten zu ändern, klicken Sie auf ![Spaltenfilter](/help/creative/assets/custom-columns.png "Spaltenfilter") unterhalb des Vorschaubereichs.

      * Um eine bestimmte Kreative in der Vorschau anzuzeigen, aktivieren Sie das Kontrollkästchen für die Zeile.

      * Inhalt ändern:

         * Um den Wert einer Zelle in der Tabelle zu bearbeiten, klicken Sie in die Zelle und bearbeiten Sie den Wert. Klicken Sie auf eine Stelle außerhalb der Zelle oder drücken Sie die **[!DNL Enter]**, um die Änderungen zu speichern.

         * Um ein einzelnes Produkt als Standard zu markieren<!--Explain what this means. --> halten Sie den Cursor über der Zeile und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Set as Default]**.

         * (Wenn die Anzeige mehr als ein Angebot enthält) Um mehrere Produkte als Standard zu markieren, wählen Sie die Zeilen (bis zur Anzahl der Angebote) aus und klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Set as Default]**.

      * Um ein Produkt aus dem Katalog zu löschen, halten Sie den Cursor über die Zeile und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Delete Row]**.

      * (Wenn die Anzeige mehr als ein Angebot enthält) Um mehrere Produkte aus dem Katalog zu löschen, wählen Sie die Zeilen (bis zur Anzahl der Angebote) aus und klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Delete Row]** .

1. Speichern Sie die Kreativen:

   * So speichern Sie die Anzeigen und fügen sie einem &quot;[-Bundle](/help/creative/creative-libraries/bundle-manage.md) in der Bibliothek hinzu:

      1. Klicken Sie auf **[!UICONTROL Save and Attach to Bundle]**.

      1. Klicken Sie auf **[!UICONTROL Save]** , um die Anzeigen zu speichern.

      1. Wählen Sie die Bundles aus und klicken Sie dann auf **[!UICONTROL Attach Creative to Bundles]**.

   * Um die Anzeigen zu speichern und das Setup zu beenden, klicken Sie auf **[!UICONTROL Save]** und anschließend erneut auf **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Dynamische kreative Einstellungen](creative-settings-dynamic.md)
>* [Bearbeiten eines dynamischen Kreativen in einer Kreativbibliothek](creative-edit-dynamic.md)
>* [Workflows für dynamische Anzeigen](/help/creative/introduction/workflow-dynamic-ads.md)
