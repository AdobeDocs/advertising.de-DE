---
title: Über Einkaufsproduktgruppen
description: Erfahren Sie mehr über Einkaufsproduktgruppen in Einkaufskampagnen.
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# Über Einkaufsproduktgruppen

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising] Shopping-Kampagnen*

Bei Einkaufskampagnen bestimmen Ihre Produktgruppen - nicht Suchbegriffe - die Produkte in Ihrem Händlercenter-Konto, für die Shopping-Anzeigen angezeigt werden. Jede Produktgruppe basiert auf einem einzelnen Produktattribut (z. B. Kategorie, Produkttyp, Marke, Bedingung, Produkt-ID oder benutzerdefinierte Beschriftungen) und verwendet dasselbe Angebot für alle übereinstimmenden Produkte. Sie können Angebote für die Produkte in jeder Gruppe ein- oder ausschließen.

Sie konfigurieren Produktgruppen auf Anzeigengruppenebene, um zu bestimmen, welche Produkte in Ihren Händlercenter-Konten in den Shopping-Anzeigen für die Anzeigengruppe angezeigt werden. Selbst wenn die Anzeigengruppe keine Anzeigenentitäten enthält, zeigt das Anzeigennetzwerk weiterhin Anzeigen für die Produkte an.

Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, verwendet das Werbenetzwerk zunächst die Kampagnenpriorität, um zu bestimmen, welche Kampagne (und welches zugehörige Angebot) für die Anzeigenauktion infrage kommt. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot berechtigt.

Weitere Informationen zu [!DNL Google] Shopping-Kampagnen und -Anzeigen finden Sie unter &quot;[Implementieren [!DNL Google Ads] Shopping-Kampagnen](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)&quot;und in der Dokumentation [Google Ads-Dokumentation](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1). Weitere Informationen zu [!DNL Microsoft] Einkaufskampagnen finden Sie unter &quot;[Implementieren [!DNL Microsoft Advertising] Einkaufskampagnen](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)&quot;und in der [[!DNL Microsoft Advertising] Dokumentation](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>Unterstützung ist nicht für [!DNL Google Ads] -Auflistungen von Gruppen in Performance-Max-Kampagnen verfügbar, die Smart-Shopping-Kampagnen ersetzen. Verwenden Sie den Editor [!DNL Google Ads] , um Daten für die Auflistung von Gruppen zu verwalten und anzuzeigen.

## Produktgruppenhierarchie

Bevor Sie Produktgruppen mit bestimmten Attributen für eine Anzeigengruppe erstellen können, müssen Sie zunächst eine inklusive Produktgruppe mit dem Namen &quot;[!UICONTROL All Products]&quot;erstellen. Aus dieser übergeordneten Produktgruppe können Sie untergeordnete Produktgruppen für Untergruppen von Produkten erstellen und aus den untergeordneten Produktgruppen Enkel erstellen. Nachdem Sie die erste untergeordnete Produktgruppe für eine Anzeigengruppe erstellt haben, wird automatisch eine weitere Produktgruppe mit dem Namen &quot;[!UICONTROL Everything Else]&quot; mit dem standardmäßigen Anzeigengruppenangebot erstellt. Wenn Sie weitere Produktgruppen hinzufügen, wird die Gruppe &quot;[!UICONTROL Everything Else]&quot;entsprechend angepasst, sodass sie alle Produkte darstellt, die nicht zu einer anderen Produktgruppe gehören.

Innerhalb einer Anzeigengruppe können Sie bis zu sieben Stufen von Produktgruppen erstellen (ohne &quot;[!UICONTROL All Products]&quot;), die ein- oder ausgeschlossen werden sollen, wobei eine oder mehrere Produktgruppen jeweils dasselbe Attribut auf jeder Ebene ansprechen (z. B. [!UICONTROL Brand]=Acme für eine Produktgruppe und [!UICONTROL Brand]=AcmePlus für eine andere auf derselben Ebene). Übergeordnete Produktgruppen werden als Unterteilungen bezeichnet und die niedrigste Unterteilungsebene wird als Einheit bezeichnet. Sie können Gebote und Tracking-Vorlagen festlegen oder Gebote vollständig ausschließen. Der gesamte Satz aktiver Produktgruppen für eine Anzeigengruppe wird hierarchisch angewendet, um die geeigneten Produkte zu bestimmen. Wenn Sie beispielsweise [!UICONTROL All Products] in [!UICONTROL Brand]=AcmeBasic und [!UICONTROL Brand]=AcmePlus unterteilen und dann jede dieser Produktgruppen weiter in [!UICONTROL Condition]=Neu unterteilen und Gebote festlegen, können nur neue Produkte mit den Marken AcmeBasic und AcmePlus beworben oder von Anzeigen ausgeschlossen werden.

![Beispiel eines Produktgruppensatzes](/help/search-social-commerce/assets/product-group-list.png "Beispiel eines Produktgruppensatzes")

![Beispielproduktgruppenhierarchie](/help/search-social-commerce/assets/product-group-tree.png "Beispiel für eine Produktgruppenhierarchie")

## Die Ansicht [!UICONTROL Product Groups]

Sie können in der Ansicht [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] Produktgruppen erstellen und bearbeiten sowie Produktgruppen und deren untergeordnete Produktgruppen löschen.

## Tracking und Leistungsdaten für Einkaufsproduktgruppen

(Konten/Kampagnen mit der Tracking-Option &quot;[!UICONTROL EF Redirect]&quot;) Damit Search, Social und Commerce Konversionen für Produktgruppen verfolgen können, generieren Sie mit dem Tool Tracking-URLs ](/help/search-social-commerce/tools/click-tracking-url-generate.md) Tracking-URLs für Produktgruppen und führen Sie einen der folgenden Schritte aus:[

* (Erforderlich für [!DNL Google Ads]; Best Practice für [!DNL Microsoft Advertising]) Fügen Sie die Tracking-URL dem Feld [!DNL Tracking Template] in der Einstellung für Konto, Kampagne oder Produktgruppe hinzu. Fügen Sie sie zur einfacheren Wartung auf der höchstmöglichen Ebene hinzu. Alle für das Konto oder die Kampagne angegebenen Anlagenparameter sind nicht enthalten.

  >[!CAUTION]
  >
  >([!DNL Microsoft Advertising]) Verwenden Sie diese Option nur, wenn Sie die Tracking-URLs für Suche, Social und Commerce nicht in eine benutzerdefinierte Spalte im Produkt-Feed einschließen. Wenn Sie beides tun, enthalten die URLs zwei Umleitungen und verursachen fehlerhafte Links.

* ([!DNL Microsoft Advertising] only) Fügen Sie die Tracking-URL den Produktdaten im [!DNL Microsoft Merchant Center] -Konto hinzu. Fügen Sie dazu die Tracking-URL zusammen mit dem Wert im Feld `link` oder `mobile_link` in eine benutzerdefinierte Spalte mit dem Namen [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) im Produkt-Feed ein. Die mit dieser Methode generierten URLs enthalten keine Tracking-Parameter, die in den Konto- oder Kampagneneinstellungen in Search, Social und Commerce angegeben sind.

Sie können Daten zu Produktgruppen in [dem [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md) anzeigen.

>[!MORELIKETHIS]
>
>* [Verwalten von Einkaufsproduktgruppen](product-group-manage.md)
>* [[!DNL Google Ads] Produktgruppeneinstellungen](product-group-settings-google.md)
>* [Implementieren von [!DNL Google Ads] Shopping-Kampagnen](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] Produktgruppeneinstellungen](product-group-settings-microsoft.md)
>* [Implementieren von [!DNL Microsoft Advertising] Shopping-Kampagnen](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
