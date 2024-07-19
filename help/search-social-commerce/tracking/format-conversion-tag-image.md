---
title: Format der Tracking-Tags für die Bildkonvertierung
description: Verweisen Sie auf das Format der Tracking-Tags für die Bildkonvertierung.
exl-id: e23107e1-b719-4572-a471-13e51387465d
feature: Search Tracking
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Format der Tracking-Tags für die Bildkonvertierung

>[!NOTE]
>
>Informationen dazu, wann Bild-Tags und JavaScript-Tags verwendet werden sollen, finden Sie in den [FAQs zum Verfolgen von Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* Nicht sichere Tags für Sites mit HTTP:

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* Sichere Tags für Sites mit HTTPS:

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

wobei:

* `<ef-userid>` ist eine eindeutige, numerische Benutzer-ID, die Search, Social und Commerce dem Advertiser zuweisen.

* `<propertyname>` ist die Konvertierung, die verfolgt werden soll. Wenn Sie beispielsweise eine Konversion mit dem Namen &quot;Registrierung&quot;verfolgen, enthält das Tag den Parameter `ev_registration=<registration>` und Sie müssen den tatsächlichen Umsatz für jede Transaktion (z. B. `ev_registration=1`) weitergeben. Wenn mehrere Eigenschaften verfolgt werden, werden sie durch ein kaufmännisches Und-Zeichen (`&`) wie `ev_registration=<registration>&ev_sale=<sale>` (z. B. `ev_registration=1&ev_sale=12.99`) verbunden. **Hinweis:** Der Eigenschaftsname darf keine Sonderzeichen enthalten.

* `<transid>` ist eine eindeutige Transaktions-ID (z. B. eine tatsächliche Bestell-ID), die der Advertiser generiert und weitergibt, um eine Transaktion zu identifizieren. Sie ist nur enthalten, wenn die Option &quot;[!UICONTROL Include unique transaction IDs]&quot; ausgewählt ist.

  Search, Social und Commerce verwenden die Transaktions-ID, um doppelte Transaktionen mit derselben Transaktions-ID und demselben Eigenschaftswert zu vermeiden. Die Transaktions-ID ist im [!UICONTROL Transaction Report] enthalten, mit dem Sie Daten innerhalb von Adobe Advertising mit den Daten des Advertisers validieren können. **Hinweis:** Wenn die Daten des Advertisers keine eindeutige ID pro Transaktion enthalten, wird in Search, Social und Commerce immer noch eine auf der Transaktionszeit basierende ID generiert.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Über Adobe Advertising von Konversions-Tracking-Tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generieren eines Adobe Advertising-Konversions-Tags](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [FAQs über Konversions- und Seitenansichts-Tracking-Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format der JavaScript-Konversions-Tracking-Tags, Version 2](format-conversion-tag-jsv2.md)
>* [Format der JavaScript-Konversions-Trackingtags, Version 3](format-conversion-tag-jsv3.md)
