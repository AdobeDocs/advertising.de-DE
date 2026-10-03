---
title: '[!DNL Google Ads] Produktgruppeneinstellungen'
description: Referenzieren Sie die Einstellungen für [!DNL Google Ads] Shopping-Produktgruppen.
exl-id: 2cfef9de-b265-4fa5-b1bd-84e6cba79914
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/TkiKzm1sNZZdcu1ghpySElcQb7OIjnNZVqsVqzrK2uE'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%
---
# [!DNL Google Ads] Produktgruppeneinstellungen

## „Alle Produkte“-Produktgruppen

**[!UICONTROL Condition]:** (schreibgeschützt) Alle Produkte

**[!UICONTROL Bid]:** (Nur für Produktgruppen) Die maximalen Kosten pro Klick (CPC), die den höchsten Betrag darstellen, der für einen Anzeigenklick bezahlt werden muss. Dieser Wert wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet und anstelle des Werts auf Anzeigengruppenebene.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

Diese Vorlage überschreibt Vorlagen auf höheren Ebenen und wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet.

## Alle anderen Produktgruppen

**[!UICONTROL Condition/Value]:** (Schreibgeschützt für vorhandene Produktgruppen) Die Produktdimensionen, die Sie ansprechen möchten. Geben Sie für neue Produktgruppen die Dimension ein, nach der Produkte ausgewählt werden sollen, sowie das Attribut, das für die ausgewählte Informationskategorie qualifiziert ist (z. B. „Acme“ bei der Zielgruppenbestimmung nach Marke oder „Neu“ bei der Zielgruppenbestimmung nach Bedingung).

Nachdem Sie eine Produktgruppe für bestimmte Produktdimensionen (d. h. nicht für „Alle Produkte„) erstellt haben, erstellt Search, Social und Commerce automatisch eine Produktgruppe für „Alles andere“.

Eine Liste der verfügbaren Produktdimensionen finden Sie unter &quot;[&#x200B; von Kampagnenproduktfiltern](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md). Die Liste der Dimensionen kann je nach [!UICONTROL Inventory Filter] der Kampagne begrenzt sein.

**[!UICONTROL Excluded]:** (optional für neue Produktgruppen; schreibgeschützt für bestehende Produktgruppen) Schließt Angebote für Anzeigen für übereinstimmende Produkte aus.

**[!UICONTROL Bid]:** (Nur für Produktgruppen) Die maximalen Kosten pro Klick (CPC), die den höchsten Betrag darstellen, der für einen Anzeigenklick bezahlt werden muss. Dieser Wert wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet und anstelle des Werts auf Anzeigengruppenebene.

<!-- **[!UICONTROL Tracking Template]:** -->

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

Diese Vorlage überschreibt Vorlagen auf höheren Ebenen und wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet.

>[!MORELIKETHIS]
>
>* [Über Shopping-Produktgruppen](product-group-about.md)
>* [Verwalten von Shopping-Produktgruppen](product-group-manage.md)
>* [Kampagnenproduktfilter kaufen](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [Implementieren [!DNL Google Ads] Shopping-Kampagnen](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
