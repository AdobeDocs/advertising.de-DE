---
title: Verwalten [!DNL ChatGPT Ads] konversativen Anzeigenkampagnen
description: Erfahren Sie, wie Sie [!DNL ChatGPT Ads] Kampagnen, Anzeigengruppen und Chat-Card-Anzeigen erstellen und verwalten. Dies ist eine Beta-Funktion, mit der Anzeigen in Konversationen mit KI-Assistenten platziert werden.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: cb25ab04e8fef5d00935e5325a897b1de97e2674
workflow-type: tm+mt
source-wordcount: '1188'
ht-degree: 0%
---
# Verwalten [!DNL ChatGPT Ads] konversativen Anzeigenkampagnen, Anzeigengruppen und Anzeigen

*Beta-Funktion*

Verwalten Sie [!DNL ChatGPT Ads] Kampagnen, Anzeigengruppen und Chat-Card-Anzeigen in einem [Conversational Ads-Konto](account-manage.md).

Die [!DNL ChatGPT Ads] wird Ihnen am Ende des Monats zusammen mit Ihren anderen Rechnungen in Rechnung gestellt. Bei Fragen zur Rechnungsstellung wenden Sie sich an Ihr Adobe Account Team.

## Die Ansicht [!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns] {#campaign-views-about}

Die Ansicht [!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns] umfasst drei Registerkarten: [!UICONTROL Campaigns], [!UICONTROL Ad Groups] und [!UICONTROL Ads]. Auf jeder Registerkarte werden die Kampagnen, Anzeigengruppen oder Anzeigen für das ausgewählte Konto zusammen mit Leistungsdaten für den ausgewählten Datumsbereich aufgelistet. Leistungsdaten auf Kampagnen-, Anzeigengruppen- und Anzeigenebene umfassen [!UICONTROL Impressions], [!UICONTROL Clicks], [!UICONTROL Spend], [!UICONTROL CTR], [!UICONTROL Avg CPC] und [!UICONTROL Avg CPM].

>[!NOTE]
>
>* Organisationen, die für die Anzeige von Steuerwerten in Berichtsansichten konfiguriert sind, sehen diese nicht für [!DNL ChatGPT Ads]. Berechnen Sie Ihre Steuerwerte manuell.

### Verfügbare Aktionen

<!-- * [Refresh information about your campaigns](#refresh) -- Add topic below. -->

* [Erstellen](#campaign-create) oder [Bearbeiten](#campaign-edit) einer Kampagne

* [Erstellen](#ad-group-create) oder [Bearbeiten](#ad-group-edit) einer Anzeigengruppe für eine vorhandene Kampagne

* [Erstellen](#ad-create) oder [Bearbeiten](#ad-edit) einer Anzeige für eine bestehende Anzeigengruppe

* [Aktivieren oder Anhalten einer Kampagne, Anzeigengruppe oder Anzeige](#pause-activate)

* [Archivieren einer Kampagne, Anzeigengruppe oder Anzeige](#archive)

* [Drilldown von Kampagnen zu Anzeigengruppen und Anzeigen](#drill-down)

* [Kampagne, Anzeigengruppe oder Anzeigenliste aktualisieren](#refresh)

## Kampagnen

### Erstellen einer [!DNL ChatGPT Ads] konversativen Anzeigenkampagne {#campaign-create}

Wenn Sie eine Kampagne erstellen, können Sie optional ihre erste Anzeigengruppe und -anzeige erstellen. Jeder Schritt erstellt diese Entität, sobald Sie auf **[!UICONTROL Next]** klicken, sodass Sie nicht zu einem vorherigen Schritt zurückkehren können. Wenn Sie später etwas ändern müssen, bearbeiten Sie es, sobald der Assistent geschlossen wurde.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Conversational Ads Beta]**.

1. Klicken Sie im Untermenü auf die Registerkarte **[!UICONTROL Campaigns]** .

1. Wählen Sie oben rechts einen Advertiser und ein [!DNL ChatGPT Ads] Konto aus.

1. Klicken Sie oben rechts auf **[!UICONTROL Create]>[!UICONTROL Campaign]**.

1. Geben Sie die [Kampagneneinstellungen](#campaign-settings) an.

1. Klicken Sie auf **[!UICONTROL Next]** , um die Kampagneneinstellungen zu speichern.

1. Führen Sie einen der folgenden Schritte aus:

   * Wenn Sie keine Anzeigengruppe für die Kampagne erstellen möchten, klicken Sie auf **[!UICONTROL Close]**.

     >[!TIP]
     >
     >Informationen zum Erstellen einer Anzeigengruppe oder Anzeige später finden Sie unter &quot;[Erstellen einer Anzeigengruppe](#ad-group-create) oder &quot;[Erstellen einer Anzeige](#ad-create)&quot;.

   * (Optional) Erstellen Sie eine Anzeigengruppe:

     1. Geben Sie die [Anzeigengruppeneinstellungen“ &#x200B;](#ad-group-settings).

     1. Klicken Sie auf **[!UICONTROL Next]** , um die Anzeigengruppeneinstellungen zu speichern.

     1. (Optional) Wenn Sie keine Anzeige für die Kampagne erstellen möchten, klicken Sie auf **[!UICONTROL Close]**.

   * (Optional, nachdem Sie eine Anzeigengruppe erstellt haben) Erstellen einer Anzeige:

     1. Geben Sie die [Anzeigeneinstellungen](#ad-settings) an.

     1. Klicken Sie auf **[!UICONTROL Create ad]**.

### Bearbeiten [!DNL ChatGPT Ads] Konversations-Anzeigenkampagneneinstellungen {#campaign-edit}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Conversational Ads Beta]**.

1. Klicken Sie im Untermenü auf der linken Seite auf **[!UICONTROL Campaigns]**.

1. Wählen Sie oben rechts einen Advertiser und ein [!DNL ChatGPT Ads] Konto aus.

1. Klicken Sie (falls erforderlich) über der Datentabelle auf die Registerkarte **[!UICONTROL Campaigns]** .

1. Halten Sie den Cursor über der Zeile und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Edit]**.

1. Bearbeiten Sie eine der [Kampagneneinstellungen](#campaign-settings), [Anzeigengruppeneinstellungen](#ad-group-settings) und [Anzeigeneinstellungen](#ad-settings).

1. Klicken Sie auf **[!UICONTROL Save]**.

### [!DNL ChatGPT Ads] der Einstellungen für konversative Anzeigenkampagnen {#campaign-settings}

**[!UICONTROL Campaign name]:** Ein eindeutiger Name für die Kampagne. Der Name muss mindestens drei Zeichen enthalten.

**[!UICONTROL Campaign type]:** (Schreibgeschützt) *Standard* ist der einzige verfügbare Typ.

**[!UICONTROL Objective]:** Die Metrik, auf die sich die Kampagne konzentrieren soll: *Reichweite* oder *Klicks*. Das Ziel bestimmt den Bid-Typ für die Anzeigengruppen der Kampagne.

**[!UICONTROL Locations]:** (Optional) Ein oder mehrere spezifische Speicherorte für das Targeting. Lassen Sie diese Einstellung leer, um alle Standorte auszuwählen. Um einen bestimmten Speicherort anzugeben, geben Sie mindestens zwei Buchstaben ein, die an einer beliebigen Stelle innerhalb des Namens angezeigt werden, und klicken Sie dann in den Suchergebnissen auf den Namen.

**[!UICONTROL Budget type]:** *Tägliches* oder *Lebenszeitbudget*.

**[!UICONTROL Budget]:** Das Budget für den angegebenen Budgettyp. Der Wert muss größer als null (0) sein.

**[!UICONTROL Start date]:** Das Startdatum der Kampagne in der Zeitzone des Kontos.

**[!UICONTROL Set an end date]:** (Optional) Ermöglicht die Angabe eines Enddatums für die Kampagne. Wenn Sie diese Option auswählen, geben Sie die **[!UICONTROL End date]** an.

## Anzeigengruppen

### Erstellen einer [!DNL ChatGPT Ads] Anzeigengruppe für eine vorhandene Kampagne {#ad-group-create}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Conversational Ads Beta]**.

1. Klicken Sie im Untermenü auf die Registerkarte **[!UICONTROL Campaigns]** .

1. Wählen Sie oben rechts einen Advertiser und ein [!DNL ChatGPT Ads] Konto aus.

1. Klicken Sie oben rechts auf **[!UICONTROL Create]>[!UICONTROL Ad Group]**.

1. Geben Sie die [Anzeigengruppeneinstellungen](#ad-group-settings) einschließlich der übergeordneten Kampagne an.

1. Klicken Sie auf **[!UICONTROL Create ad group]**.

## Bearbeiten einer [!DNL ChatGPT Ads] Anzeigengruppe {#ad-group-edit}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Conversational Ads Beta]**.

1. Klicken Sie im Untermenü auf der linken Seite auf **[!UICONTROL Campaigns]**.

1. Wählen Sie oben rechts einen Advertiser und ein [!DNL ChatGPT Ads] Konto aus.

1. Klicken Sie über der Datentabelle auf die Registerkarte **[!UICONTROL Ad Groups]** .

1. Halten Sie den Cursor über der Zeile und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Edit]**.

1. Bearbeiten Sie die Einstellungen [Anzeigengruppe](#ad-group-settings).

1. Klicken Sie auf **[!UICONTROL Save]**.

### Einstellungen für Anzeigengruppen [!DNL ChatGPT Ads] {#ad-group-settings}

**[!UICONTROL Parent campaign]:** (Anzeigengruppen nur für bestehende Kampagnen) Die Kampagne, zu der die Anzeigengruppe gehört.

**[!UICONTROL Ad group name]:** Ein eindeutiger Name für die Anzeigengruppe. Der Name muss mindestens drei Zeichen enthalten.

**[!UICONTROL Maximum CPC bid]** oder **[!UICONTROL Maximum CPM bid]:** Der maximale Betrag, den Sie für jeden Klick oder für 1.000 Impressionen zahlen. Der Wert muss größer als null (0) sein. Das Ziel der Kampagne bestimmt das Bid-Feld: *Klicks* Kampagnen zeigen **[!UICONTROL Maximum CPC bid]** und *Reichweite* Kampagnen zeigen **[!UICONTROL Maximum CPM bid]**.

>[!TIP]
>
>Höhere Gebote können mehr Auktionen gewinnen.

**[!UICONTROL Context hints]:** (Optional) Eine Beschreibung der Konversationen, Themen oder Schlüsselwörter, für die Ihre Produkte oder Services relevant sind. Diese Hinweise leiten den Abgleich an, sind aber keine exakt übereinstimmenden Zielgruppenbestimmungsregeln.

## Anzeigen

### Erstellen einer [!DNL ChatGPT Ads]-Chat-Kartenanzeige für eine bestehende Anzeigengruppe {#ad-create}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Conversational Ads Beta]**.

1. Klicken Sie im Untermenü auf die Registerkarte **[!UICONTROL Campaigns]** .

1. Wählen Sie oben rechts einen Advertiser und ein [!DNL ChatGPT Ads] Konto aus.

1. Klicken Sie oben rechts auf **[!UICONTROL Create]>[!UICONTROL Ad]**.

1. Geben Sie die [Anzeigeneinstellungen](#ad-settings) einschließlich der übergeordneten Kampagne und Anzeigengruppe an.

1. Klicken Sie auf **[!UICONTROL Create ad]**.

## Bearbeiten einer [!DNL ChatGPT Ads]-Chat-Kartenanzeige {#ad-edit}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Conversational Ads Beta]**.

1. Klicken Sie im Untermenü auf der linken Seite auf **[!UICONTROL Campaigns]**.

1. Wählen Sie oben rechts einen Advertiser und ein [!DNL ChatGPT Ads] Konto aus.

1. Klicken Sie über der Datentabelle auf die Registerkarte **[!UICONTROL Ads]** .

1. Halten Sie den Cursor über der Zeile und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Edit]**.

1. Bearbeiten Sie die [ad](#ad-settings)-Einstellungen.

1. Klicken Sie auf **[!UICONTROL Save]**.

### Einstellungen für [!DNL ChatGPT Ads]-Chat-Karte {#ad-settings}

**[!UICONTROL Parent campaign]** und **[!UICONTROL Parent ad group]:** (Nur Anzeigen in vorhandenen Anzeigengruppen) Die Kampagne und Anzeigengruppe, zu der die Anzeige gehört.

**[!UICONTROL Ad name]:** Ein eindeutiger Name für die Anzeige. Der Name muss mindestens drei Zeichen enthalten.

**[!UICONTROL Ad URL (Link)]:** Die Landingpage-URL, beginnend mit `http://` oder `https://`.

**[!UICONTROL Title (headline)]:** Die Überschrift der Anzeige. Der Titel muss zwischen 3 und 50 Zeichen lang sein. **Hinweis:** Der Titel kann in einigen Platzierungstypen abgeschnitten werden.

**[!UICONTROL Description]:** Der Haupttext der Anzeige. Die Beschreibung muss zwischen 3 und 100 Zeichen lang sein.

**[!UICONTROL Ad image]:** Ein JPG- oder PNG-Bild, das in die Anzeige aufgenommen werden soll. Um ein Bild hochzuladen, klicken Sie auf (neue Anzeigen) **[!UICONTROL Upload image (PNG/JPG)]** oder **[!UICONTROL Change image]** und suchen und wählen Sie dann eine Datei auf Ihrem Gerät oder Netzwerk aus.

**[!UICONTROL Preview]:** eine Vorschau der Anzeige basierend auf den Anzeigeneinstellungen.

## Aktivieren oder Anhalten einer [!DNL ChatGPT Ads] Kampagne, Anzeigengruppe oder Anzeige {#pause-activate}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Conversational Ads Beta]**.

1. Klicken Sie im Untermenü auf der linken Seite auf **[!UICONTROL Campaigns]**.

1. Wählen Sie oben rechts einen Advertiser und ein [!DNL ChatGPT Ads] Konto aus.

1. Suchen Sie auf der Registerkarte **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]** oder **[!UICONTROL Ads]** die Zeile.

1. Führen Sie in der Spalte **[!UICONTROL Active]** eine der folgenden Aktionen aus:

   * Um ein pausiertes Element zu aktivieren, aktivieren Sie den Umschalter (rechts).

   * Um ein aktives Element anzuhalten, deaktivieren Sie den Umschalter (links).

## Archivieren einer [!DNL ChatGPT Ads] Kampagne, Anzeigengruppe oder Anzeige {#archive}

Durch die Archivierung wird die Kampagne, die Anzeigengruppe oder die Anzeige dauerhaft aus den [!UICONTROL Conversational Ads] entfernt.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Conversational Ads Beta]**.

1. Klicken Sie im Untermenü auf der linken Seite auf **[!UICONTROL Campaigns]**.

1. Wählen Sie oben rechts einen Advertiser und ein [!DNL ChatGPT Ads] Konto aus.

1. Halten Sie auf der Registerkarte **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]** oder **[!UICONTROL Ads]** den Cursor über der Zeile und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Archive]**.

## Drilldown von [!DNL ChatGPT Ads] Kampagnen zu Anzeigengruppen und Anzeigen {#drill-down}

* Klicken Sie auf eine Kampagnenzeile, um nur deren Anzeigengruppen auf der Registerkarte **[!UICONTROL Ad Groups]** anzuzeigen, oder klicken Sie auf eine Anzeigengruppenzeile, um nur deren Anzeigen auf der Registerkarte **[!UICONTROL Ads]** anzuzeigen.

Um den Filter zu entfernen und alle Zeilen in der Ansicht anzuzeigen, klicken Sie **X** im Filter über der Datentabelle.

## Kampagne, Anzeigengruppe oder Anzeigenliste aktualisieren {#refresh}

Zeigen Sie erneut die Liste der Kampagnen, Anzeigengruppen oder Anzeigen an, wenn andere Benutzer Änderungen oder Ergänzungen vorgenommen haben.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Conversational Ads Beta]**.

1. Klicken Sie in der **[!UICONTROL Campaigns]**-, **[!UICONTROL Ad Groups]**- oder **[!UICONTROL Ads]** auf **[!UICONTROL Refresh]** über der Datentabelle.

>[!MORELIKETHIS]
>
>* [Verwalten von Werbekonten für Konversationen](account-manage.md)
