---
title: Über Shopping-Produktgruppen
description: Erfahren Sie mehr über Warengruppen in Shopping-Kampagnen.
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# Über Shopping-Produktgruppen

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising] Shopping-Kampagnen*

In Shopping-Kampagnen bestimmen Ihre Produktgruppen - nicht Keywords - die Produkte in Ihrem Merchant-Center-Konto, für die Shopping-Anzeigen angezeigt werden. Jede Produktgruppe basiert auf einem einzelnen Produktattribut (z. B. Kategorie, Produkttyp, Marke, Bedingung, Produkt-ID oder benutzerdefinierte Beschriftungen) und verwendet dasselbe Angebot für alle übereinstimmenden Produkte. Sie können Angebote für die Produkte in jeder Gruppe ein- oder ausschließen.

Sie konfigurieren Produktgruppen auf Anzeigengruppenebene, um zu bestimmen, welche Produkte in Ihren Merchant-Center-Konten in den Shopping-Anzeigen für die Anzeigengruppe angezeigt werden. Auch wenn die Anzeigengruppe keine Anzeigenentitäten enthält, zeigt das Anzeigennetzwerk weiterhin Anzeigen für die Produkte an.

Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, verwendet das Anzeigennetzwerk zunächst die Kampagnenpriorität, um zu bestimmen, welche Kampagne (und das zugehörige Angebot) für die Anzeigenauktion geeignet ist. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot geeignet.

Weitere Informationen zu [!DNL Google] Shopping-Kampagnen und Anzeigen finden Sie unter [Implementieren von  [!DNL Google Ads] -Shopping-](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)&quot; und in der Dokumentation zu [Google Ads](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&rd=1). Weitere Informationen zu [!DNL Microsoft] Shopping-Kampagnen finden Sie unter [Implementieren [!DNL Microsoft Advertising] Shopping-](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)&quot; und in der [[!DNL Microsoft Advertising] Dokumentation](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>In -Kampagnen mit dem Typ „Performance Max“, die Smart Shopping-Kampagnen ersetzen, werden keine Gruppen in der [!DNL Google Ads]-Auflistung unterstützt. Verwenden Sie zum Verwalten und Anzeigen von Daten für Auflistungsgruppen den [!DNL Google Ads].

## Produktgruppen-Hierarchie

Bevor Sie Produktgruppen mit bestimmten Attributen für eine Anzeigengruppe erstellen können, müssen Sie zunächst eine allumfassende Produktgruppe namens &quot;[!UICONTROL All Products]&quot; erstellen. Über diese übergeordnete Produktgruppe können Sie untergeordnete Produktgruppen für Produktuntergruppen erstellen, und Sie können untergeordnete Produktgruppen aus den untergeordneten Produktgruppen erstellen. Nachdem Sie die erste untergeordnete Produktgruppe für eine Anzeigengruppe erstellt haben, wird automatisch eine andere Produktgruppe mit dem Namen &quot;[!UICONTROL Everything Else]&quot; anhand des Standardangebots für die Anzeigengruppe erstellt. Wenn Sie weitere Produktgruppen hinzufügen, wird die Gruppe &quot;[!UICONTROL Everything Else]&quot; entsprechend angepasst, sodass sie alle Produkte umfasst, die nicht zu einer anderen Produktgruppe gehören.

Innerhalb einer Anzeigengruppe können Sie bis zu sieben Ebenen von Produktgruppen (ohne &quot;[!UICONTROL All Products]„) erstellen, um Angebote ein- oder auszuschließen, wobei eine oder mehrere Produktgruppen auf jeder Ebene auf dasselbe Attribut abzielen (z. B. [!UICONTROL Brand]=Acme für eine Produktgruppe und [!UICONTROL Brand]=AcmePlus für eine andere auf derselben Ebene). Übergeordnete Produktgruppen werden als Unterteilungen bezeichnet. Die unterste Ebene der Unterteilung wird als Einheit bezeichnet. Sie können Gebote und Tracking-Vorlagen auf Einheitenebene festlegen oder Gebote vollständig ausschließen. Der gesamte Satz aktiver Produktgruppen für eine Anzeigengruppe wird hierarchisch angewendet, um die geeigneten Produkte zu bestimmen. Wenn Sie beispielsweise [!UICONTROL All Products] in [!UICONTROL Brand]=AcmeBasic und [!UICONTROL Brand]=AcmePlus unterteilen und dann jede dieser Produktgruppen weiter in [!UICONTROL Condition]=New unterteilen und Gebote abgeben, können nur neue Produkte mit den Marken AcmeBasic und AcmePlus beworben oder von der Werbung ausgeschlossen werden.

![Beispiel eines Produktgruppensatzes](/help/search-social-commerce/assets/product-group-list.png "Beispiel eines Produktgruppensatzes")

![Beispiel für eine Produktgruppenhierarchie](/help/search-social-commerce/assets/product-group-tree.png "Beispiel-Produktgruppenhierarchie")

## Die [!UICONTROL Product Groups]

In der Ansicht [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > Produktgruppen können Sie Produktgruppen erstellen und bearbeiten sowie Produktgruppen und deren untergeordnete Produktgruppen [!UICONTROL Product Groups].

## Tracking- und Leistungsdaten für Shopping-Produktgruppen

(Konten/Kampagnen mit der Tracking-Option &quot;[!UICONTROL EF Redirect]„) Damit Search, Social und Commerce Konversionen für Produktgruppen verfolgen können, [mithilfe des Tools zum Tracking von URLs Tracking-URLs Tracking-URLs für Produktgruppen generieren](/help/search-social-commerce/tools/click-tracking-url-generate.md) und führen Sie dann einen der folgenden Schritte aus:

* (Erforderlich für [!DNL Google Ads]; Best Practice für [!DNL Microsoft Advertising]) Fügen Sie die Tracking-URL zum Feld [!DNL Tracking Template] in der Einstellung des Kontos, der Kampagne oder der Produktgruppe hinzu. Fügen Sie sie für eine einfachere Wartung auf der höchstmöglichen Ebene hinzu. Für das Konto oder die Kampagne angegebene Anlagenparameter sind nicht enthalten.

  >[!CAUTION]
  >
  >([!DNL Microsoft Advertising]) Verwenden Sie diese Option nur, wenn Sie die Tracking-URLs für Search, Social und Commerce nicht in eine benutzerdefinierte Spalte im Produkt-Feed einfügen. In beiden Fällen enthalten die URLs zwei Umleitungen und führen zu fehlerhaften Links.

* (Nur [!DNL Microsoft Advertising]) Fügen Sie die Tracking-URL den Produktdaten im [!DNL Microsoft Merchant Center] hinzu. Fügen Sie dazu die Tracking-URL zusammen mit dem Wert im Feld `link` oder `mobile_link` je nach Bedarf in eine benutzerdefinierte Spalte mit dem Namen [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) im Produkt-Feed ein. Mit dieser Methode generierte URLs enthalten keine Tracking-Parameter, die in den Konto- oder Kampagneneinstellungen in Search, Social und Commerce angegeben sind.

Sie können Daten zu Produktgruppen in der [!UICONTROL Product Group Report][&#128279;](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md) .

>[!MORELIKETHIS]
>
>* [Verwalten von Shopping-Produktgruppen](product-group-manage.md)
>* [[!DNL Google Ads] Produktgruppeneinstellungen](product-group-settings-google.md)
>* [Implementieren [!DNL Google Ads] Shopping-Kampagnen](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] Produktgruppeneinstellungen](product-group-settings-microsoft.md)
>* [Implementieren [!DNL Microsoft Advertising] Shopping-Kampagnen](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
