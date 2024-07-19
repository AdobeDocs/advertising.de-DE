---
title: Format der JavaScript-Konversions-Tracking-Tags, Version 2
description: Verweisen Sie auf das Format der JavaScript-Konversions-Trackingtags, Version 2.
exl-id: 75e96f97-a3f0-4f5b-8bbb-4b1e8986f01a
feature: Search Tracking
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Format der JavaScript-Konversions-Tracking-Tags, Version 2

Das folgende Format gilt für Sites, die HTTPS verwenden. Bei Sites, die HTTP verwenden, sollten die URLs mit &quot;http&quot;beginnen.

>[!NOTE]
>
>Informationen dazu, wann Version 2 und Version 3 verwendet werden sollen, finden Sie in den [FAQs zum Verfolgen von Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
var ef_event_type="transaction";
var ef_transaction_properties = "ev_property name=<property name>&ev_transid=<transid>";
/*
 * Do not modify below this line
 */
var ef_segment = "";
var ef_search_segment = "";
var ef_userid="ef-userid";
var ef_pixel_host="pixel.everesttech.net";
var ef_fb_is_app = 0;
var ef_allow_3rd_party_pixels = 1;
effp();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property name=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

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
>* [Format der Tracking-Tags für die Bildkonvertierung](format-conversion-tag-image.md)
