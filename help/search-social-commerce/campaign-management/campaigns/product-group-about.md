---
title: Über Einkaufsproduktgruppen
description: Erfahren Sie mehr über Einkaufsproduktgruppen in Einkaufskampagnen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 0%

---

# Über Einkaufsproduktgruppen

*[!DNL Google Ads]und [!DNL Microsoft Advertising] Nur Warenkorb*

Bei Einkaufskampagnen bestimmen Ihre Produktgruppen - nicht Suchbegriffe - die Produkte in Ihrem Händlercenter-Konto, für die Shopping-Anzeigen angezeigt werden. Jede Produktgruppe basiert auf einem einzelnen Produktattribut (z. B. Kategorie, Produkttyp, Marke, Bedingung, Produkt-ID oder benutzerdefinierte Beschriftungen) und verwendet dasselbe Angebot für alle übereinstimmenden Produkte. Sie können Angebote für die Produkte in jeder Gruppe ein- oder ausschließen.

Sie konfigurieren Produktgruppen auf Anzeigengruppenebene, um zu bestimmen, welche Produkte in Ihren Händlercenter-Konten in den Shopping-Anzeigen für die Anzeigengruppe angezeigt werden. Selbst wenn die Anzeigengruppe keine Anzeigenentitäten enthält, zeigt das Anzeigennetzwerk weiterhin Anzeigen für die Produkte an.

Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, verwendet das Werbenetzwerk zunächst die Kampagnenpriorität, um zu bestimmen, welche Kampagne (und welches zugehörige Angebot) für die Anzeigenauktion infrage kommt. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot berechtigt.

Weitere Informationen finden Sie unter [!DNL Google] Einkaufskampagnen und Anzeigen, siehe[Implementierung [!DNL Google Ads] Warenkorb](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)&quot; und [Dokumentation zu Google Ads](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1). Weitere Informationen zu Microsoft-Shopping-Kampagnen finden Sie unter &quot;[Implementierung [!DNL Microsoft® Advertising] Warenkorb](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)&quot; und [Microsoft-Werbedokumentation](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>Unterstützung ist nicht verfügbar für [!DNL Google Ads] Auflistung von Gruppen in Kampagnen zur Leistungssteigerung, die Smart-Shopping-Kampagnen ersetzen. Um Daten für Auflistungsgruppen zu verwalten und anzuzeigen, verwenden Sie die [!DNL Google Ads] Editor.

## Produktgruppenhierarchie

Bevor Sie Produktgruppen mit bestimmten Attributen für eine Anzeigengruppe erstellen können, müssen Sie zunächst eine inklusive Produktgruppe mit dem Namen[!UICONTROL All Products].&quot; Aus dieser übergeordneten Produktgruppe können Sie untergeordnete Produktgruppen für Untergruppen von Produkten erstellen und aus den untergeordneten Produktgruppen Enkel erstellen. Nachdem Sie die erste untergeordnete Produktgruppe für eine Anzeigengruppe erstellt haben, wird eine weitere Produktgruppe namens[!UICONTROL Everything Else]&quot; wird automatisch mit dem standardmäßigen Anzeigengruppenangebot erstellt. Wenn Sie weitere Produktgruppen hinzufügen, wird die[!UICONTROL Everything Else]&quot;wird entsprechend angepasst, sodass es sich um alle Produkte handelt, die nicht zu einer anderen Produktgruppe gehören.

Innerhalb einer Anzeigengruppe können Sie bis zu sieben Stufen von Produktgruppen erstellen (ohne &quot;[!UICONTROL All Products]&quot;) um ein- oder auszuschließen, wobei eine oder mehrere Produktgruppen jeweils dasselbe Attribut auf jeder Ebene ansprechen (z. B. [!UICONTROL Brand]=Acme für eine Produktgruppe und [!UICONTROL Brand]= AcmePlus für einen anderen auf derselben Ebene). Übergeordnete Produktgruppen werden als Unterteilungen bezeichnet und die niedrigste Unterteilungsebene wird als Einheit bezeichnet. Sie können Gebote und Tracking-Vorlagen festlegen oder Gebote vollständig ausschließen. Der gesamte Satz aktiver Produktgruppen für eine Anzeigengruppe wird hierarchisch angewendet, um die geeigneten Produkte zu bestimmen. Wenn Sie beispielsweise unterteilen [!UICONTROL All Products] in [!UICONTROL Brand]=AcmeBasic und [!UICONTROL Brand]=AcmePlus, und unterteilen Sie dann jede dieser Produktgruppen weiter in [!UICONTROL Condition]=Neue und festgelegte Angebote, dann können nur neue Produkte mit den Marken AcmeBasic und AcmePlus beworben oder von Anzeigen ausgeschlossen werden.

![Beispiel eines Produktgruppensatzes](/help/search-social-commerce/assets/product-group-list.png "Beispiel eines Produktgruppensatzes")

![Beispielhafte Produktgruppenhierarchie](/help/search-social-commerce/assets/product-group-tree.png "Beispielhafte Produktgruppenhierarchie")

## Die [!UICONTROL Product Groups] Ansicht

Sie können Produktgruppen erstellen und bearbeiten sowie Produktgruppen und deren untergeordnete Produktgruppen löschen, indem Sie die [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] anzeigen.

## Tracking und Leistungsdaten für Einkaufsproduktgruppen

(Konten/Kampagnen mit der &quot;[!UICONTROL EF Redirect]&quot;-Tracking-Option) Damit Search, Social und Commerce Konversionen für Produktgruppen verfolgen können, [Generieren von Tracking-URLs für Produktgruppen mit dem Tool Tracking-URLs](/help/search-social-commerce/tools/click-tracking-url-generate.md)und führen Sie dann einen der folgenden Schritte aus:

* (Erforderlich für [!DNL Google Ads]; Best Practice für [!DNL Microsoft Advertising]) Fügen Sie die Tracking-URL zum [!DNL Tracking Template] in der Einstellung für Konto, Kampagne oder Produktgruppe. Fügen Sie sie zur einfacheren Wartung auf der höchstmöglichen Ebene hinzu. Alle für das Konto oder die Kampagne angegebenen Anlagenparameter sind nicht enthalten.

   >[!CAUTION]
   >
   >([!DNL Microsoft Advertising]) Verwenden Sie diese Option nur, wenn Sie die Tracking-URLs für Suche, Social und Commerce nicht in eine benutzerdefinierte Spalte im Produkt-Feed aufnehmen. Wenn Sie beides tun, enthalten die URLs zwei Umleitungen und führen zu fehlerhaften Links.

* ([!DNL Microsoft Advertising] nur) Fügen Sie die Tracking-URL den Produktdaten innerhalb der [!DNL Microsoft Merchant Center] -Konto. Fügen Sie dazu die Tracking-URL sowie den Wert in die `link` oder `mobile_link` in einer benutzerdefinierten Spalte mit dem Namen [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) innerhalb des Produkt-Feeds. Die mit dieser Methode generierten URLs enthalten keine Tracking-Parameter, die in den Konto- oder Kampagneneinstellungen in Search, Social und Commerce angegeben sind.

Sie können Daten zu Produktgruppen in [die [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [Verwalten von Einkaufsproduktgruppen](product-group-manage.md)
>* [[!DNL Google Ads] Produktgruppeneinstellungen](product-group-settings-google.md)
>* [Implementierung [!DNL Google Ads] Warenkorb](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] Produktgruppeneinstellungen](product-group-settings-microsoft.md)
>* [Implementierung [!DNL Microsoft® Advertising] Warenkorb](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)

