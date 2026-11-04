---
title: Dynamische Kreative bearbeiten und auf Qualität überprüfen
description: Erfahren Sie, wie Sie dynamische kreative Einstellungen bearbeiten und Kataloginhalte mit Qualitätsprüfungen in einer Kreativbibliothek überprüfen können.
feature: Creative Dynamic Creatives
exl-id: b75b9aeb-ffd0-4b86-aa7a-bd6a22e7a8e4
TQID: 'https://experienceleague.adobe.com/QoQ5p4sFV-ARIMNDbPkp7axfqkVEC3sxJ6MTlPIG22Y'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d70c54b0-f069-4a3c-8056-7069a25e110c
    internal-label: Creative Dynamic Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: ed1682eff9ce28df30a5314de90f6f67c10f338a
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 0%
---
# Dynamische Kreative bearbeiten und auf Qualität überprüfen

Bearbeiten Sie die kreativen Einstellungen, um die Konfiguration der Kreativen zu ändern, z. B. den Namen, die Kataloge und die Attributzuordnung. Verwenden Sie den QA Agent, um die resultierenden Anzeigen zu überprüfen und die Katalogwerte zu korrigieren.

## Kreative Einstellungen bearbeiten {#edit-creative-settings}

### Über die neue Benutzeroberfläche {#from-the-new-ui}

1. Öffnen Sie die Kreativeinstellungen:

   * Aus einer Kreativ-Bibliothek:

     1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

     1. Öffnen Sie die Bibliothek auf eine der folgenden Arten:

        * Klicken Sie auf den Bibliotheksnamen.

        * Klicken Sie neben dem Bibliotheksnamen auf **[!UICONTROL ...]** > **[!UICONTROL Open]**.

     1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf **[!UICONTROL ...]** neben dem Namen der Kreativen, und klicken Sie dann auf **[!UICONTROL Edit]**.

   * Von [!UICONTROL Creative Studio]:

     1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]>[!UICONTROL Creative Studio]**.

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

### Von der alten Benutzeroberfläche {#from-the-legacy-ui}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Klicken Sie auf **[!UICONTROL Switch to classic UI]**.

1. Klicken Sie auf den Bibliotheksnamen.

1. Halten Sie den Cursor über die Zeile für Kreativ und klicken Sie auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie die [Einstellungen für dynamische Anzeigen](creative-settings-dynamic.md).

1. Klicken Sie auf **[!UICONTROL Continue]** , um eine Vorschau der zu generierenden Kreativen anzuzeigen. Sie können in der Vorschau einen der folgenden Schritte ausführen:

   * Um die Kreativen nach Katalog, Filterwert <!-- explain more--> Anzeigengröße zu filtern, verwenden Sie die Filter über dem Vorschaubereich.

   * So suchen Sie anhand der eindeutigen ID im Suchfeld unter dem Vorschaubereich nach einem Produkt.

   * Um die angezeigten Spalten zu ändern, klicken Sie auf ![Spaltenfilter](/help/creative/assets/custom-columns.png "Spaltenfilter") unterhalb des Vorschaubereichs.

   * Um eine bestimmte Kreative in der Vorschau anzuzeigen, aktivieren Sie das Kontrollkästchen für die Zeile.

   * Inhalt ändern:

     * (Nur Anzeigen) Um den Wert einer Zelle in der Tabelle zu bearbeiten, klicken Sie in die Zelle und bearbeiten Sie den Wert. Klicken Sie auf eine Stelle außerhalb der Zelle oder drücken Sie die **[!DNL Enter]**, um die Änderungen zu speichern.

     * Um ein einzelnes Produkt als Standard zu markieren<!--Explain what this means. --> halten Sie den Cursor über der Zeile und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Set as Default]**.

     * (Wenn die Anzeige mehr als ein Angebot enthält) Um mehrere Produkte als Standard zu markieren, wählen Sie die Zeilen (bis zur Anzahl der Angebote) aus und klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Set as Default]**.

     * Um ein Produkt aus dem Katalog zu löschen, halten Sie den Cursor über die Zeile und klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Delete Row]**.

     * (Wenn die Anzeige mehr als ein Angebot enthält) Um mehrere Produkte aus dem Katalog zu löschen, wählen Sie die Zeilen (bis zur Anzahl der Angebote) aus und klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Delete Row]** .

1. Speichern Sie die Kreativen:

   * So speichern Sie die Anzeigen und fügen sie einem &quot;[-Bundle](bundle-manage.md) in der Bibliothek hinzu:

     1. Klicken Sie auf **[!UICONTROL Save and Attach to Bundle]**.

     1. Klicken Sie auf **[!UICONTROL Save]** , um die Anzeigen zu speichern.

     1. Wählen Sie die Bundles aus und klicken Sie dann auf **[!UICONTROL Attach Creative to Bundles]**.

   * Um die Anzeigen zu speichern und das Setup zu beenden, klicken Sie auf **[!UICONTROL Save]** und anschließend erneut auf **[!UICONTROL Save]**.

## Qualitätsprüfung einer dynamischen kreativen Benutzeroberfläche (nur neue Benutzeroberfläche) {#qa-dynamic-creative}

Verwenden Sie den QA Agent in der neuen Benutzeroberfläche, um Katalogzeilen anhand der Vorlage eines dynamischen Kreativen zu analysieren, die resultierenden Anzeigen in der Vorschau anzuzeigen und potenzielle Inhaltsprobleme zu identifizieren. Sie können Anzeigen mithilfe der **[!UICONTROL AI Assistant]** filtern und gruppieren, Katalogwarnhinweise überprüfen und Katalogwerte manuell korrigieren, bevor Sie die Änderungen veröffentlichen.

>[!NOTE]
>
>Sie können dynamische Kreative aus [!UICONTROL Creative Libraries] oder [!UICONTROL Creative Studio] auf ihre Qualität überprüfen. Weitere Einstiegspunkte [ Sie unter „Qualitätsprüfung eines dynamischen ](/help/creative/creative-studio/creative-studio-manage-dynamic-ads.md#qa-dynamic-creative) aus Creative Studio“.

Der QA Agent ist nur für dynamische Display-Kreative verfügbar, die auf dynamischen Vorlagen basieren, nicht für Standard-Kreative oder dynamische Video-Kreative.

### Öffnen Sie den QA Agent {#open-qa-agent}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Öffnen Sie die Bibliothek auf eine der folgenden Arten:

   * Klicken Sie auf den Bibliotheksnamen.
   * Klicken Sie neben dem Bibliotheksnamen auf **[!UICONTROL ...]** > **[!UICONTROL Open]**.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Creatives]** auf **[!UICONTROL ...]** neben dem Namen des dynamischen Kreativen, und klicken Sie dann auf **[!UICONTROL QA Agent]**.

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

* So speichern Sie die vorhandenen dynamischen kreativen Inhalte und veröffentlichen Katalogbearbeitungen:

  1. Klicken Sie in der Kopfzeile auf **[!UICONTROL Save Dynamic Creative]**.

  1. Klicken Sie im **[!UICONTROL Update Dynamic Creative]** Bestätigungsdialogfeld auf **[!UICONTROL Update]**.

     Kehren Sie zur Kreativbibliothek zurück.

* Um den Katalog zu verlassen, ohne ausstehende Katalogbearbeitungen zu veröffentlichen, klicken Sie in der Kopfzeile der Seite auf **[!UICONTROL Cancel]** .

>[!MORELIKETHIS]
>
>* [Dynamische kreative Einstellungen](creative-settings-dynamic.md)
>* [Hinzufügen dynamischer Kreativer zu einer Kreativbibliothek](creative-add-dynamic.md)
>* [Anzeigen des Änderungsprotokolls für einen Kreativen](/help/creative/creative-libraries/creative-view-change-log.md)
>* [Workflows für dynamische Anzeigen](/help/creative/introduction/workflow-dynamic-ads.md)
