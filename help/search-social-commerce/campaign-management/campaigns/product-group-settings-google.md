---
title: "[!DNL Google Ads] Produktgruppeneinstellungen"
description: Verweisen Sie auf die Einstellungen für [!DNL Google Ads] Einkaufsproduktgruppen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# [!DNL Google Ads] Produktgruppeneinstellungen

## Produktgruppen &quot;Alle Produkte&quot;

**[!UICONTROL Condition]:** (schreibgeschützt) Alle Produkte

**[!UICONTROL Bid]:** (Nur Produktgruppen eingeschlossen) Die maximalen Kosten pro Klick (CPC), der höchste Betrag, der für einen Klick auf die Anzeige bezahlt wird. Dieser Wert wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet und anstelle des Wertes auf Anzeigengruppenebene verwendet.

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

Diese Vorlage überschreibt Vorlagen auf höheren Ebenen und wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet.

## Alle anderen Produktgruppen

**[!UICONTROL Condition/Value]:** (Schreibgeschützt für bestehende Produktgruppen) Die Produktdimensionen, die als Ziel ausgewählt werden sollen. Geben Sie für neue Produktgruppen die Dimension an, mit der Produkte angesprochen werden sollen, und das qualifizierende Attribut für die ausgewählte Informationskategorie (z. B. &quot;Acme&quot;, wenn Sie ein Targeting nach Marke durchführen, oder &quot;Neu&quot;, wenn Sie ein Targeting nach Bedingung durchführen).

Nachdem Sie eine Produktgruppe für bestimmte Produktdimensionen erstellt haben (d. h. nicht &quot;Alle Produkte&quot;), erstellt Search, Social und Commerce automatisch eine Produktgruppe für &quot;Alles andere&quot;.

Eine Liste der verfügbaren Produktdimensionen finden Sie unter[Produktfilter für Shopping-Kampagnen](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot; Die Liste der Dimensionen kann je nach Kampagnenart begrenzt sein. [!UICONTROL Inventory Filter] -Einstellung.

**[!UICONTROL Excluded]:** (Optional für neue Produktgruppen; schreibgeschützt für bestehende Produktgruppen) Schließt Gebote auf Anzeigen für übereinstimmende Produkte aus.

**[!UICONTROL Bid]:** (Nur Produktgruppen eingeschlossen) Die maximalen Kosten pro Klick (CPC), der höchste Betrag, der für einen Klick auf die Anzeige bezahlt wird. Dieser Wert wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet und anstelle des Wertes auf Anzeigengruppenebene verwendet.

<!-- **[!UICONTROL Tracking Template]:** -->

<!-- ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

Diese Vorlage überschreibt Vorlagen auf höheren Ebenen und wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet.

>[!MORELIKETHIS]
>
>* [Über Einkaufsproduktgruppen](product-group-about.md)
>* [Verwalten von Einkaufsproduktgruppen](product-group-manage.md)
>* [Produktfilter für Shopping-Kampagnen](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)
>* [Implementierung [!DNL Google Ads] Warenkorb](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)

