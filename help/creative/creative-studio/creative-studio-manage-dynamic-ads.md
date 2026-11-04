---
title: Verwalten von dynamischen Kreativen in Creative Studio
description: Erfahren Sie, wie Sie kataloggesteuerte dynamische Kreative in Adobe Advertising Creative Studio erstellen, überprüfen, bearbeiten, duplizieren und löschen.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 88fead9ffc4eaa572be090877790422e67831036
workflow-type: tm+mt
source-wordcount: '1469'
ht-degree: 0%
---
# Verwalten dynamischer Kreative in [!UICONTROL Creative Studio]

Auf der Registerkarte **[!UICONTROL Creatives]** in [!UICONTROL Creative Studio] werden Ihre dynamischen Kreativen nach Bibliothek aufgelistet. Von hier aus können Sie neue kataloggesteuerte dynamische Kreative erstellen, Kreative mit KI auf Qualität überprüfen, die Details und Attributzuordnung vorhandener Kreativer bearbeiten, Änderungsprotokolle anzeigen, Kreative duplizieren und Kreative löschen.

## Erstellen eines dynamischen Kreativen {#build-dynamic-creative}

Verwenden Sie diesen Workflow, um kataloggesteuerte dynamische Kreative zu erstellen. Ein vierstufiger geführter Assistent führt Sie durch die Auswahl einer Vorlage, das Verbinden eines Katalogs und das Zuordnen von Katalogfeldern zu Vorlagenelementen. Nach der Einrichtung hilft Ihnen die [!UICONTROL AI Assistant], jede aus den Katalogdaten generierte Anzeigenkombination in der Vorschau anzuzeigen und ihre Qualität zu überprüfen.

Dynamische Kreative unterscheiden sich von Standardanzeigen in einer wichtigen Hinsicht: Der KI-Agent kann Kataloginhalte nicht ändern. Probleme können gefiltert, analysiert und gekennzeichnet werden. Um jedoch Anzeigeninhalte zu ändern, müssen Sie die Katalogwerte manuell aktualisieren, entweder über den QS-Bildschirm oder im Quellkatalog.

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

   Wenn Sie mit der QS fortfahren, wird der **[!UICONTROL Dynamic Creative QA]** mit einer Vorschau-Arbeitsfläche und dem **[!UICONTROL AI Assistant]** Chat-Panel geöffnet.

1. Wenn Sie mit der Qualitätssicherung fortfahren, befolgen Sie die Verfahren unter &quot;[Qualitätsprüfung eines dynamischen Kreativen](#qa-dynamic-creative), um Anzeigen zu [&#x200B; und zu &#x200B;](#analyze-ads), [Vorschauen und Warnhinweise zu überprüfen](#review-previews) und optional [Katalogwerte zu korrigieren](#correct-catalog-values). Wenn Sie fertig sind, speichern [&#x200B; die dynamische &#x200B;](#save-or-exit).

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

## Qualitätsprüfung eines dynamischen Kreativen {#qa-dynamic-creative}

Verwenden Sie den QA-Agenten, um Katalogzeilen anhand der Vorlage eines dynamischen Kreativen zu analysieren, die resultierenden Anzeigen in der Vorschau anzuzeigen und potenzielle Inhaltsprobleme zu identifizieren. Sie können Anzeigen mithilfe der **[!UICONTROL AI Assistant]** filtern und gruppieren, Katalogwarnhinweise überprüfen und Katalogwerte manuell korrigieren, bevor Sie die Änderungen veröffentlichen.

Der Agent öffnet den **[!UICONTROL Dynamic Creative QA]** entweder über [!UICONTROL Creative Libraries] oder [!UICONTROL Creative Studio]. Obwohl die Menübeschriftungen unterschiedlich sind, bieten beide Einstiegspunkte dieselbe QA-Funktionalität. Die Analyse hängt von den ausgewählten Kreativen, Katalogen und Anfragen ab.

>[!NOTE]
>
>Der QA Agent ist für Kreative von dynamischen Displays verfügbar, nicht für Kreative von Standard- oder dynamischen Videos. In [!UICONTROL Creative Libraries] ist die Aktion nur für dynamische Kreative verfügbar, die auf dynamischen Vorlagen basieren.

### Öffnen Sie den QA Agent {#open-qa-agent}

1. Öffnen Sie eine gespeicherte dynamische Datei für die Qualitätssicherung auf eine der folgenden Arten:

   * **Von [!UICONTROL Creative Libraries]:**

     1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

     1. Klicken Sie auf den Bibliotheksnamen, um die Bibliothek zu öffnen.

     1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf **[!UICONTROL ...]** neben dem Namen des dynamischen Kreativen, und klicken Sie dann auf **[!UICONTROL QA Agent]**.

   * **Von [!UICONTROL Creative Studio]:**

     1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Studio]**.

     1. Suchen Sie auf der Registerkarte **[!UICONTROL Creatives]** den dynamischen Kreativen in seiner Kreativbibliothek unter dem Abschnitt [!UICONTROL Generate or Build Creatives] .

     1. Halten Sie den Cursor über die Kreativkarte und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**.

   Der **[!UICONTROL Dynamic Creative QA]** wird mit einer Vorschau-Arbeitsfläche und dem **[!UICONTROL AI Assistant]** Chat-Panel geöffnet.

1. Wenn der Kreative mehrere Kataloge verwendet, wählen Sie in der Kopfzeile den zu überprüfenden Katalog aus **[!UICONTROL Catalog]**.

   Der Assistent analysiert den ausgewählten Katalog. Die Katalogauswahl ist deaktiviert, wenn der Kreative nur einen Katalog verwendet.

### Analysieren und Filtern von Anzeigen mit KI {#analyze-ads}

1. Geben Sie im Bedienfeld **[!UICONTROL AI Assistant]** eine Anfrage in **[!UICONTROL Ask anything]** ein und drücken Sie **[!UICONTROL Enter]** oder klicken Sie auf eine der vorgeschlagenen Eingabeaufforderungen:

   * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
   * **[!UICONTROL Group ads by product]**
   * **[!UICONTROL Filter ads by geography]**
   * **[!UICONTROL Show all ads with headlines over 80 characters]**

   Der Assistent antwortet im Chat-Panel und zeigt übereinstimmende Katalogzeilen als Anzeigenvorschau auf der Arbeitsfläche an. Bis Sie eine Anfrage senden, werden Sie auf der Arbeitsfläche aufgefordert, den Assistenten zur Analyse des Katalogs aufzufordern.

1. Weitere Verfeinerung der Überprüfung durch Folgeanfragen. Der Assistent kann Ihnen dabei helfen:

   * Filtern Sie Anzeigen nach Zielgruppensegment, Sprache, Geografie oder Postleitzahl.
   * Überprüfen Sie die Zeichenlängen anhand eines von Ihnen angegebenen Schwellenwerts.
   * Prüfen Sie auf Feed-Fehler, fehlende Inhalte und verdächtige Inhalte.
   * Übersetzungsstatus überprüfen.
   * Vergleichen Sie A/B-Testvarianten.
   * Gruppieren Sie Anzeigen zur Überprüfung, z. B. nach Produkt oder Problem.

   Überprüfen Sie die Antworten des Assistenten und die Vorschau, bevor Sie die Änderungen speichern.

### Vorschau und Warnhinweise überprüfen {#review-previews}

* Verwenden Sie die Symbolleiste der Arbeitsfläche für Folgendes:

  * Zoom anpassen.
  * Zwischen **[!UICONTROL Thumbnail view]** und **[!UICONTROL Actual size]** wechseln.
  * Klicken Sie auf **[!UICONTROL Replay animations]** , um die Vorschaubilder erneut anzuzeigen.
  * Wählen Sie die Anzahl der Zeilen pro Seite aus, wählen Sie eine Seitenzahl aus oder verwenden Sie **[!UICONTROL Previous page]** und **[!UICONTROL Next page]**.

* Wenn die Ergebnisse der Assistenzgruppen angezeigt werden, klicken Sie auf den Link, um alle Kreativen in einer Gruppe anzuzeigen. Verwenden Sie **[!UICONTROL Back to groups]** , um zu den gruppierten Ergebnissen zurückzukehren, oder **[!UICONTROL Catalog Rows]** , um die gruppierte Ansicht zu verlassen.

* Wenn eine Vorschau **[!UICONTROL Issues detected]** anzeigt, halten Sie den Cursor über die Anzeige, um die Problemdetails anzuzeigen.

* Wenn Katalog-Warnhinweise verfügbar sind, klicken Sie auf **[!UICONTROL View Alerts]**. Im Dialogfeld &quot;**[!UICONTROL Alerts]**&quot; werden Katalog, Zeilennummer, Spalte und Fehlermeldung für jedes Problem aufgeführt. Klicken Sie auf **[!UICONTROL Close]** , um zur Arbeitsfläche zurückzukehren.

### Korrigieren von Katalogwerten {#correct-catalog-values}

Sie können Katalogwerte manuell aus einer Anzeigenvorschau bearbeiten, ohne den QA-Bildschirm zu verlassen.

1. Klicken Sie in der Vorschau, die Sie korrigieren möchten, auf **[!UICONTROL Edit]**.

1. Wählen Sie im Dialogfeld „Bearbeiten“ unter **[!UICONTROL Catalog columns to edit]** die zu ändernden Spalten aus. Um eine Spalte zu finden, verwenden Sie **[!UICONTROL Search columns]**.

1. Aktualisieren Sie unter **[!UICONTROL Columns content]** die ausgewählten Feldwerte.

1. Klicken Sie auf **[!UICONTROL Update]**.

   Die Vorschau wird mit den aktualisierten Werten aktualisiert. Die Katalogänderungen werden erst veröffentlicht, wenn Sie die dynamische kreative Datei speichern.

>[!IMPORTANT]
>
>Durch diese Bearbeitungen werden Katalogdaten aktualisiert, nicht nur die Anzeigenvorschau. Überprüfen Sie die Werte, bevor Sie sie veröffentlichen.

### Änderungen speichern oder beenden {#save-or-exit}

* So speichern Sie die dynamische kreative Datei und veröffentlichen alle Katalogbearbeitungen:

  1. Klicken Sie in der Kopfzeile auf **[!UICONTROL Save Dynamic Creative]**.

  1. Bestätigen Sie das Speichern:

     * Klicken Sie für einen neuen Kreativen im **[!UICONTROL Create Dynamic Creative]** Bestätigungsdialogfeld auf **[!UICONTROL Create]**.
     * Klicken Sie für einen vorhandenen Kreativen im **[!UICONTROL Update Dynamic Creative]** Bestätigungsdialogfeld auf **[!UICONTROL Update]**.

     Sie kehren zur Kreativbibliothek oder zum [!UICONTROL Creative Studio] zurück, je nachdem, wo Sie den QA-Bildschirm geöffnet haben.

* Um den Katalog zu verlassen, ohne ausstehende Katalogbearbeitungen zu veröffentlichen, klicken Sie in der Kopfzeile der Seite auf **[!UICONTROL Cancel]** .

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
