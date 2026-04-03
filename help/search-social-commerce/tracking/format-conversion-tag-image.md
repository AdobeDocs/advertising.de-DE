---
title: Format der Tracking-Tags für die Bildkonvertierung
description: Referenzieren Sie das Format der Bildkonvertierungs-Tracking-Tags.
exl-id: e23107e1-b719-4572-a471-13e51387465d
feature: Search Tracking
TQID: https://experienceleague.adobe.com/TQMACo5-LkbCU2SiMmUE-ZDBRTb8NERQPQ9ISzU0DdU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 249
ht-degree: 0%

---

# Format der Tracking-Tags für die Bildkonvertierung

>[!NOTE]
>
>Informationen dazu, wann Bild-Tags und JavaScript-Tags verwendet werden, finden Sie in den [Häufig gestellte Fragen zu Tracking-Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* Nicht sichere Tags für Sites mit HTTP:

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* Sichere Tags für Sites mit HTTPS:

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

Dabei gilt:

* `<ef-userid>` ist eine eindeutige numerische Benutzer-ID, die Search, Social und Commerce dem Advertiser zuweist.

* `<propertyname>` ist die Konvertierung in „Track“. Wenn Sie z. B. eine Konversion mit dem Namen „Registrierung“ verfolgen, enthält das Tag den Parameter `ev_registration=<registration>` und Sie müssen den tatsächlichen Umsatz für jede Transaktion (z. B. `ev_registration=1`) übergeben. Wenn mehrere Eigenschaften verfolgt werden, werden sie durch ein kaufmännisches Und-Zeichen (`&`) verbunden, z. B. `ev_registration=<registration>&ev_sale=<sale>` (z. B. `ev_registration=1&ev_sale=12.99`). **Hinweis:** Der Eigenschaftsname darf keine Sonderzeichen enthalten.

* `<transid>` ist eine eindeutige Transaktions-ID (z. B. eine tatsächliche Auftrags-ID), die der Advertiser generiert und übergibt, um eine Transaktion zu identifizieren. Sie ist nur enthalten, wenn die Option &quot;[!UICONTROL Include unique transaction IDs]&quot; ausgewählt ist.

  Search, Social und Commerce verwenden die Transaktions-ID, um doppelte Transaktionen mit derselben Transaktions-ID und demselben Eigenschaftswert zu eliminieren. Die Transaktions-ID ist in der [!UICONTROL Transaction Report] enthalten, mit der Sie Daten in Adobe Advertising mit den Daten des Advertisers validieren können. **Hinweis:** Wenn die Daten des Werbetreibenden keine eindeutige ID pro Transaktion enthalten, generiert Search, Social und Commerce weiterhin eine ID basierend auf der Transaktionszeit.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Über Konversionsverfolgungstags in Adobe Advertising](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Generieren eines Adobe Advertising-Konversions-Tags](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Häufig gestellte Fragen zu Konversions- und Seitenansichts-Tracking-Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format von JavaScript-Konversionsverfolgungstags, Version 2](format-conversion-tag-jsv2.md)
>* [Format von JavaScript-Konversionsverfolgungstags Version 3](format-conversion-tag-jsv3.md)
