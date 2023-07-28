---
title: Format der Tracking-Tags für die Bildkonvertierung
description: Verweisen Sie auf das Format der Tracking-Tags für die Bildkonvertierung.
exl-id: 019981cd-37b6-4b80-bb48-26e0d7ac7665
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Format der Tracking-Tags für die Bildkonvertierung

>[!NOTE]
>
>Informationen dazu, wann Sie Bild-Tags und JavaScript-Tags verwenden können, finden Sie unter [Häufig gestellte Fragen zum Verfolgen von Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* Nicht sichere Tags für Sites mit HTTP:

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* Sichere Tags für Sites mit HTTPS:

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

wobei:

* `<ef-userid>` ist eine eindeutige, numerische Benutzer-ID, die Search, Social und Commerce dem Advertiser zuweist.

* `<propertyname>` ist die Konversion, die verfolgt wird. Wenn Sie beispielsweise eine Konversion mit dem Namen &quot;Registrierung&quot;verfolgen, würde das Tag den Parameter enthalten. `ev_registration=<registration>`und Sie müssen den tatsächlichen Umsatz für jede Transaktion (z. B. `ev_registration=1`). Wenn mehrere Eigenschaften verfolgt werden, werden sie durch ein Und-Zeichen (`&`), z. B. `ev_registration=<registration>&ev_sale=<sale>` (zum Beispiel: `ev_registration=1&ev_sale=12.99`). **Hinweis:**  Der Eigenschaftsname darf keine Sonderzeichen enthalten.

* `<transid>` ist eine eindeutige Transaktions-ID (z. B. eine tatsächliche Bestell-ID), die der Advertiser generiert und übergibt, um eine Transaktion zu identifizieren. Sie ist nur enthalten, wenn die[!UICONTROL Include unique transaction IDs]&quot;.

  Search, Social und Commerce verwenden die Transaktions-ID, um doppelte Transaktionen mit derselben Transaktions-ID und demselben Eigenschaftswert zu vermeiden. Die Transaktions-ID ist im [!UICONTROL Transaction Report], mit dem Sie Daten in Adobe Advertising mit den Daten des Advertisers validieren können. **Hinweis:** Wenn die Daten des Advertisers keine eindeutige ID pro Transaktion enthalten, wird in Search, Social und Commerce immer noch eine auf der Transaktionszeit basierende ID generiert.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Über Adobe Advertising-Konversions-Tracking-Tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generieren eines Adobe Advertising-Konversions-Tags](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Häufig gestellte Fragen zu Konversions- und Seitenansichts-Tracking-Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format der JavaScript-Konversions-Trackingtags, Version 2](format-conversion-tag-jsv2.md)
>* [Format der JavaScript-Konversions-Trackingtags, Version 3](format-conversion-tag-jsv3.md)
