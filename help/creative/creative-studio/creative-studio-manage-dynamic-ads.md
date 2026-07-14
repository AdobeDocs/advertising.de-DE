---
title: Verwalten von dynamischen Kreativen in Creative Studio
description: Erfahren Sie, wie Sie kataloggesteuerte dynamische Kreative in Adobe Advertising Creative Studio erstellen, bearbeiten, duplizieren und löschen.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a6ab21a588f5b069ea0783dee711f52d906a46f9
workflow-type: tm+mt
source-wordcount: 1044
ht-degree: 0%

---

# Verwalten dynamischer Kreative in [!UICONTROL Creative Studio]

*Beta-Funktion*

Auf der Registerkarte **[!UICONTROL Creatives]** in [!UICONTROL Creative Studio] werden Ihre dynamischen Kreativen nach Bibliothek aufgelistet. Hier können Sie neue kataloggesteuerte dynamische Kreative erstellen, die Details und Attributzuordnungen vorhandener Kreativer bearbeiten, Änderungsprotokolle anzeigen, Kreative duplizieren und Kreative löschen.

## Erstellen eines dynamischen Kreativen {#build-dynamic-creative}

Verwenden Sie diesen Workflow, um kataloggesteuerte dynamische Kreative zu erstellen. Ein vierstufiger geführter Assistent führt Sie durch die Auswahl einer Vorlage, das Verbinden eines Katalogs und das Zuordnen von Katalogfeldern zu Vorlagenelementen. Nach der Einrichtung hilft Ihnen die [!UICONTROL AI Assistant], jede aus den Katalogdaten generierte Anzeigenkombination in der Vorschau anzuzeigen und ihre Qualität zu überprüfen.

Dynamische Kreative unterscheiden sich von Standardanzeigen in einer wichtigen Hinsicht: Der KI-Agent kann Kataloginhalte nicht ändern. Sie kann Probleme filtern, analysieren und kennzeichnen - aber um Anzeigeninhalte zu ändern, müssen Sie den Quellkatalog aktualisieren.

### Voraussetzungen

* In Ihrer Vorlagenbibliothek muss mindestens eine benutzerdefinierte Anzeige-Vorlage (keine Systemvorlage) vorhanden sein.
* Ein Produkt- oder Inhaltskatalog (Feed) ist in Ihrem Konto verfügbar.

### Schritt 1: [!UICONTROL Build Dynamic Creative] öffnen {#open-wizard}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio]**.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf **[!UICONTROL Build]** auf der Karte Schnellaktion **[!UICONTROL Build dynamic creatives from catalog data]** .

   Das Dialogfeld Vier-Schritte-**[!UICONTROL Build Dynamic Creative]** wird geöffnet.

### Schritt 2: Vorlage auswählen {#select-template}

>[!NOTE]
>
>Im Vorlagenkatalog werden nur die von Ihnen erstellten Anzeigenvorlagen angezeigt. Systemvorlagen und Video-Anzeigenvorlagen sind nicht als Ausgangspunkt für dynamische Kreative verfügbar.

1. Klicken Sie im Vorlagenkatalog auf eine Vorlage, um sie auszuwählen.

   Die Schaltfläche **[!UICONTROL Next]** ist deaktiviert, bis eine Vorlage ausgewählt wird.

1. Klicken Sie auf **[!UICONTROL Use this template]**.

### Schritt 3: Katalog auswählen {#select-catalog}

1. Konfigurieren Sie die kreativen Einstellungen:

   * **[!UICONTROL Ad Library]:** Wählen Sie die Kreativbibliothek aus, in der die Kreativen gespeichert werden sollen.
   * **[!UICONTROL Dynamic creative name]:** Geben Sie einen Namen für den dynamischen Kreativen ein.
   * **[!UICONTROL Number of cards]:** Geben Sie die Anzahl der Katalogangebote ein, die in jeder Anzeigenkombination enthalten sein sollen (1-50).
   * **[!UICONTROL Assign dynamic creative to a bundle]:** (Optional) Wenn diese Option aktiviert ist, werden die gespeicherten Kreativen an ein Bundle angehängt. Wählen Sie ein Bundle aus der Bibliothek aus.

1. Einen oder mehrere Kataloge auswählen:

   1. (Optional) Verwenden Sie **[!UICONTROL Catalog template]**, um die Katalogliste nach einer bestimmten Vorlagenfamilie zu filtern. Um optional die Vorlagendatei zur Überprüfung herunterzuladen, klicken Sie auf **[!UICONTROL Download feed template]**.

   1. Suchen Sie nach Katalogen in der Liste und wählen Sie diese aus. Alle ausgewählten Kataloge müssen derselben Katalogvorlagenfamilie angehören. Beim Versuch, Familien zu mischen, wird eine Warnung angezeigt.

   1. (Optional) Um eine neue Katalogdatei hochzuladen, ziehen Sie die Datei per Drag-and-Drop in den Upload-Bereich oder klicken Sie auf **[!UICONTROL Browse Files]**. Unterstützte Formate: JPG, PNG, JPEG, XLS, XLSX, CSV, TSV, ZIP und MP4. Maximale Dateigröße: 25 MB. Sie können jeweils nur eine Datei hochladen. Hochgeladene Kataloge erscheinen in der Chipliste mit der Bezeichnung **(hochgeladen)**.

1. Klicken Sie auf **[!UICONTROL Continue]**.

### Schritt 4: Zuordnen von Katalogfeldern zu Vorlagenelementen {#attribute-mapping}

Ordnen Sie jedes Katalogfeld dem entsprechenden Element in Ihrer Vorlage zu. Ordnen Sie beispielsweise das Feld für den Produktnamen des Katalogs dem Überschriftenelement der Vorlage und das Feld für das Produktbild dem Hintergrundbildelement zu.

1. Wählen Sie unter **[!UICONTROL Targeting]** mindestens eine Datenquelle für die Personalisierung des Kreativen aus: **[!UICONTROL Profile data]**, **[!UICONTROL Geographic data]**, **[!UICONTROL Data pass]** oder **[!UICONTROL Audience Segment]**.

1. Wählen Sie für jedes Vorlagenelement das entsprechende Katalogfeld aus der Dropdown-Liste aus.

1. Klicken Sie auf **[!UICONTROL Continue]**.

### Schritt 5: Vorschau und Qualitätssicherung mit KI {#qa}

1. Wählen Sie aus, ob *[!UICONTROL Save Dynamic Creative & Skip QA]* oder *[!UICONTROL Continue to QA]* werden soll.

   Wenn Sie mit der Qualitätssicherung fortfahren, zeigt die Arbeitsfläche alle aus dem Katalog generierten Anzeigenkombinationen als Zeilen mit einer Vorschau jedes in der Vorlage gerenderten Katalogeintrags an.

1. Wenn Sie mit der Qualitätssicherung fortfahren:

   1. Führen Sie einen der folgenden Schritte aus:

      * Verwenden Sie die Steuerelemente **[!UICONTROL Zoom in]** und **[!UICONTROL Zoom out]** , um die Arbeitsflächenansicht anzupassen.

      * Verwenden Sie die Steuerelemente für die Paginierung (**X-Y von Z**), um durch Katalogzeilen zu blättern.

      * So bearbeiten Sie eine Anzeigenkombination:

         1. Halten Sie den Cursor über der Katalogzeile und klicken Sie auf **[!UICONTROL Edit]**.

         1. Aktualisieren Sie im Dialogfeld &quot;**[!UICONTROL Edit Row]**&quot; die Feldwerte.

         1. Klicken Sie auf **[!UICONTROL Save]**.

        Die Arbeitsfläche wird aktualisiert, um die aktualisierten Werte widerzuspiegeln.

      * Verwenden Sie das **[!UICONTROL AI Assistant]** Chat-Bedienfeld, um Katalogkombinationen zu analysieren und zu filtern. Geben Sie Ihre Anfrage in das Feld **[!UICONTROL Ask anything]** ein oder klicken Sie auf eine der vorgeschlagenen Eingabeaufforderungen:

         * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
         * **[!UICONTROL Show me side-by-side comparisons of A/B testing creatives]**
         * **[!UICONTROL Show me all ads for millennial women in urban markets]**

        Der KI-Agent kann:

         * Filtern Sie die Arbeitsfläche nach Anzeigen, die einem bestimmten Zielgruppensegment, einer bestimmten Geografie, Sprache, Kategorie oder einem anderen Katalogfeld entsprechen.
         * Prüfen Sie auf Qualitätsprobleme wie Überschreitungen der Zeichenbeschränkung, Inhaltsüberlauf oder Anschnitt, fehlerhafte Bild-Links und Sichtbarkeit des Haftungsausschlusses.
         * Vergleichen Sie Anzeigenkombinationen für die A/B-Testanalyse.
         * Organisieren Sie Anzeigen in Gruppen, um sie nebeneinander anzuzeigen.

        Der KI-Agent kann Kataloginhalte nicht ändern. Um Anzeigeninhalte zu ändern, aktualisieren Sie den Quellkatalog.

   1. Speichern Sie **[!UICONTROL Save Dynamic Creative]** in der Kopfzeile.

   1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Create]**.

## Bearbeiten eines dynamischen Kreativen {#edit-dynamic-creative}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio]**.

1. Halten Sie auf der Registerkarte **[!UICONTROL Creatives]** den Cursor über die Kreativkarte und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Edit]**.

   Ein Vollbild-Editor wird mit einer Anzeigenvorschau auf der linken Seite und einem Einstellungsbedienfeld auf der rechten Seite geöffnet.

1. Bearbeiten Sie die kreativen Einstellungen auf den Registerkarten **[!UICONTROL Details]** und **[!UICONTROL Attribute Mapping]** :

   Registerkarte **[!UICONTROL Details]**:

   * **[!UICONTROL Advertiser]**, **[!UICONTROL Ad Library]** und **[!UICONTROL Ad template]** sind schreibgeschützt.
   * **[!UICONTROL Dynamic creative name]:** Der Anzeigename für den Kreativen.
   * **[!UICONTROL Number of cards]:** Die Anzahl der in jeder Anzeigenkombination enthaltenen Katalogangebote (1-50).
   * (Optional) Aktualisieren Sie unter **[!UICONTROL Catalogs]** die Katalogauswahl:
      * Verwenden Sie **[!UICONTROL Catalog template]**, um verfügbare Kataloge zu filtern. Um optional die Vorlagendatei herunterzuladen, klicken Sie auf **[!UICONTROL Download feed template]**.
      * Suchen und wählen Sie Kataloge aus der Liste aus oder laden Sie eine neue Katalogdatei hoch, indem Sie sie in den Upload-Bereich ziehen oder auf **[!UICONTROL Browse Files]** klicken (unterstützte Formate: JPG, PNG, JPEG, XLS, XLSX, CSV, TSV, ZIP, MP4; maximal 25 MB; jeweils eine Datei). Hochgeladene Kataloge sind in der **mit** (hochgeladen) gekennzeichnet.

     Alle Kataloge müssen derselben Katalogvorlagenfamilie angehören.

   Registerkarte **[!UICONTROL Attribute Mapping]**:

   * Wählen Sie unter **[!UICONTROL Targeting]** mindestens eine Datenquelle aus: **[!UICONTROL Profile data]**, **[!UICONTROL Geographic data]**, **[!UICONTROL Data pass]** oder **[!UICONTROL Audience Segment]**.
   * Aktualisieren Sie unter **[!UICONTROL Attribute Mapping]** die Zuordnung von jedem Vorlagenebenennamen zur entsprechenden Katalogspaltenbeschriftung.

1. Klicken Sie auf **[!UICONTROL Update Creative]**.

## Öffnen Sie den QA-Assistenten für dynamische Kreative erneut. {#qa-dynamic-creative}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio]**.

1. Halten Sie auf der Registerkarte **[!UICONTROL Creatives]** den Cursor über die Kreativkarte und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**.

   Der QA-Bildschirm wird geöffnet. Siehe &quot;[Schritt 5: Vorschau und QS mit KI](#qa)&quot; für die verfügbaren Arbeitsflächen-Steuerelemente und KI-Assistenten-Funktionen.

## Anzeigen des Änderungsprotokolls für ein dynamisches Kreativ-Tool {#view-change-log}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio]**.

1. Halten Sie auf der Registerkarte **[!UICONTROL Creatives]** den Cursor über die Kreativkarte und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Change Log]**.

## Dynamische Kreative duplizieren {#duplicate-dynamic-creative}

Duplizieren Sie ein dynamisches Kreativ, um ein neues Kreativ mit denselben Einstellungen zur Bibliothek hinzuzufügen. Sie können die neue Kreative später umbenennen und die Einstellungen nach Bedarf bearbeiten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio]**.

1. Halten Sie auf der Registerkarte **[!UICONTROL Creatives]** den Cursor über die Kreativkarte und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

   Der neue Kreative heißt `<original name> (copy)`.

## Löschen eines dynamischen Kreativen {#delete-dynamic-creative}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio]**.

1. Halten Sie auf der Registerkarte **[!UICONTROL Creatives]** den Cursor über die Kreativkarte und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Über Creative Studio in Advertising Creative](creative-studio-about.md)
>* [Verwalten von Standardanzeigen in Creative Studio](creative-studio-manage-standard-ads.md)
>* [Verwalten von Vorlagen in Creative Studio](creative-studio-manage-templates.md)

