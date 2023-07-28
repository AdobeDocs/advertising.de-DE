---
title: Format der JavaScript-Konversions-Trackingtags, Version 2
description: Verweisen Sie auf das Format der JavaScript-Konversions-Trackingtags, Version 2.
exl-id: c4845694-10ac-41f8-bafb-ca813e42d190
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# Format der JavaScript-Konversions-Trackingtags, Version 2

Das folgende Format gilt für Sites, die HTTPS verwenden. Bei Sites, die HTTP verwenden, sollten die URLs mit &quot;http&quot;beginnen.

>[!NOTE]
>
>Informationen dazu, wann Version 2 und Version 3 verwendet werden sollen, finden Sie unter [Häufig gestellte Fragen zum Verfolgen von Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

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
>* [Format der Tracking-Tags für die Bildkonvertierung](format-conversion-tag-image.md)
