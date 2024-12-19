---
title: ' [!DNL Google Ads]  Platzierungen verwalten'
description: Erfahren Sie, wie Sie Bietbare Platzierungen für Anzeigengruppen  [!DNL Google Ads]  und verwalten.
exl-id: 80cb6fc6-e778-4b19-9e52-e0b57bde0d73
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# [!DNL Google Ads] Platzierungen verwalten

Nur *[!DNL Google Ads]Konten*

Sie können Platzierungen für Anzeigengruppen in „Unterstützte Kampagnentypen[ erstellen und bearbeiten](/help/search-social-commerce/introduction/supported-inventory.md) die für das Anzeigennetzwerk in einem [synchronisierten Anzeigennetzwerkkonto vorgesehen sind](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)

## Erstellen [!DNL Google Ads] Platzierungen

>[!TIP]
>
>Um viele Platzierungen gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]**.

1. 
   1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Wählen Sie das Werbenetzwerk, das Konto, die Kampagne und die Anzeigengruppe aus und klicken Sie dann auf **[!UICONTROL Continue]**.

1. Konfigurieren Sie die [Platzierungseinstellungen](#placement-settings).

1. Klicken Sie auf **[!UICONTROL Post]**.

## [!DNL Google Ads] Platzierungen bearbeiten

>[!TIP]
>
>Um viele Platzierungen gleichzeitig zu bearbeiten, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder zu bearbeitenden Zeile.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten") .

1. Bearbeiten Sie die [Platzierungseinstellungen](#placement-settings).

   Bei mehreren Platzierungen werden Ihre Änderungen auf alle ausgewählten Platzierungen angewendet. Bei einigen alphanumerischen Feldern können Sie vorhandene Werte in einen angegebenen Wert ändern, eine vorhandene Zeichenfolge durch eine angegebene Zeichenfolge ersetzen, ein angegebenes Präfix an den Anfang jedes Werts hinzufügen oder ein Suffix an das Ende jedes Werts anhängen. Für einige Währungsfelder können Sie vorhandene Werte in einen bestimmten Wert ändern oder den Betrag um einen bestimmten Prozentsatz oder Geldbetrag mit einer Grenze erhöhen oder verringern.

1. Speichern Sie die Daten:

   * (Einzelne Platzierungen) Klicken Sie auf **[!UICONTROL Post]**.

   * (Mehrere Platzierungen) Klicken Sie auf **[!UICONTROL Post Now]**.

## Platzierungseinstellungen {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** Sites im Content Network, auf denen Ihre Anzeige erscheinen kann. Geben Sie eine gültige URL ein, z. B. www.example.com, example.com oder www.example.com/shoes/kids. Um mehrere Zeichenfolgen anzugeben, trennen Sie sie durch Kommas oder geben Sie sie in separaten Zeilen ein. Die URL darf kein Fragezeichen enthalten (`?`). **Hinweis** Sie können [Website-Platzierungen ausschließen](placement-negative-create.md) in der Ansicht [!UICONTROL Placements] > [!UICONTROL Negatives] sowie in den Anzeigengruppen- und Kampagneneinstellungen anzeigen.

**[!UICONTROL Status]:** Der Anzeigestatus der Platzierung: *Aktiv* (zum Aktivieren von Geboten; der Standard), *Paused* (zum Deaktivieren von Geboten) oder *Deleted* (zum Löschen der Platzierung; nur vorhandene Platzierungen).

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (Optional) Die maximalen Kosten pro Klick (CPC) oder Kosten pro Tausend sichtbarer Impressionen (vCPM) für die platzierungsbasierte Anzeige, abhängig von der Bid-Strategie der Kampagne. Dieser Wert überschreibt das Angebot auf Anzeigengruppenebene.

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
>* [Über Platzierungen](placement-about.md)
>* [Erstellen negativer Platzierungen](placement-negative-create.md)
>* [Ändern des Status von Platzierungen und negativen Platzierungen](placement-status-edit.md)
