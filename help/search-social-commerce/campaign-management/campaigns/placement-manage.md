---
title: Verwalten [!DNL Google Ads] Platzierungen
description: Erfahren Sie, wie Sie bidbare Platzierungen für [!DNL Google Ads] Anzeigengruppen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Verwalten [!DNL Google Ads] Platzierungen

*[!DNL Google Ads]Nur Konten*

Sie können Platzierungen für Anzeigengruppen in [unterstützte Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md) , die das Display-Netzwerk in einem [Synchronisiertes Anzeigennetzkonto](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)

## Erstellen [!DNL Google Ads] Platzierungen

>[!TIP]
>
>Um mehrere Platzierungen gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]**.

1. 
   1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Wählen Sie das Werbenetzwerk, das Konto, die Kampagne und die Anzeigengruppe aus und klicken Sie auf **[!UICONTROL Continue]**.

1. Konfigurieren Sie die [Platzierungseinstellungen](#placement-settings).

1. Klicken **[!UICONTROL Post]**.

## Bearbeiten [!DNL Google Ads] Platzierungen

>[!TIP]
>
>Um viele Platzierungen gleichzeitig zu bearbeiten, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder zu bearbeitenden Zeile.

   Tipps zur Auswahl mehrerer Zeilen finden Sie unter[Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten") .

1. Bearbeiten Sie die [Platzierungseinstellungen](#placement-settings).

   Bei mehreren Platzierungen werden Ihre Änderungen auf alle ausgewählten Platzierungen angewendet. Bei einigen alphanumerischen Feldern können Sie vorhandene Werte in einen angegebenen Wert ändern, eine vorhandene Zeichenfolge durch eine angegebene Zeichenfolge ersetzen, am Anfang jedes Werts ein angegebenes Präfix hinzufügen oder ein Suffix an das Ende jedes Werts anhängen. Bei einigen monetären Feldern können Sie die vorhandenen Werte in einen bestimmten Wert ändern oder den Betrag um einen bestimmten Prozentsatz oder Geldbetrag mit einer Begrenzung erhöhen oder verringern.

1. Speichern Sie die Daten:

   * (Einzelplatzierungen) Klicken Sie auf **[!UICONTROL Post]**.

   * (Mehrere Platzierungen) Klicken Sie auf **[!UICONTROL Post Now]**.

## Platzierungseinstellungen {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** Sites im Inhaltsnetzwerk, auf denen Ihre Anzeige erscheinen kann. Geben Sie eine gültige URL ein, z. B. www.example.com, example.com oder www.example.com/shoes/kids. Um mehrere Zeichenfolgen anzugeben, trennen Sie sie durch Kommas oder geben Sie sie in separate Zeilen ein. Die URL darf kein Fragezeichen (`?`). **Hinweis:** Sie können [Website-Platzierungen ausschließen](placement-negative-create.md) von [!UICONTROL Placements] > [!UICONTROL Negatives] und in den Einstellungen für Anzeigengruppe und Kampagne anzeigen.

**[!UICONTROL Status]:** Der Anzeigestatus der Platzierung: *Aktiv* (Bietbarkeit; Standard), *Angehalten* (um Gebote zu deaktivieren) oder *Gelöscht* (Löschen der Platzierung; nur vorhandene Platzierungen).

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (Optional) Die maximalen Kosten pro Klick (CPC) oder Kosten pro tausend sichtbaren Impressionen (vCPM) für die platzierungsbasierte Anzeige, je nach Kampagnen-Angebotsstrategie. Dieser Wert überschreibt das Angebot auf Anzeigengruppenebene.

<!-- If the placement is in a standard optimized portfolio, then the specified bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations. -->

### [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URL]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- note -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [Informationen zu Platzierungen](placement-about.md)
>* [Erstellen negativer Platzierungen](placement-negative-create.md)
>* [Ändern des Status von Platzierungen und negativen Platzierungen](placement-status-edit.md)

