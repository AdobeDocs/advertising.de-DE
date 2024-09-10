---
title: Format der JavaScript-Konversions-Trackingtags, Version 3
description: Verweisen Sie auf das Format der JavaScript-Konversions-Trackingtags, Version 3.
exl-id: 9fc6bb15-d880-4353-a8c5-260b7932ab34
feature: Search Tracking
source-git-commit: 8bed8f22c112abcff67727456ef4aad3b38d0ca6
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Format der JavaScript-Konversions-Trackingtags, Version 3

Das folgende Format gilt für Sites, die HTTPS verwenden. Bei Sites, die HTTP verwenden, sollten die URLs mit &quot;http&quot;beginnen.

>[!NOTE]
>
>Informationen dazu, wann Version 2 und Version 3 verwendet werden sollen, finden Sie in den [FAQs zum Verfolgen von Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script type='text/javascript'>
    (function() {
        var f = function() {
              EF.init({ eventType: "transaction",
                        transactionProperties : "ev_property=<property name>&ev_transid=<transid>",
                        segment : "",
                        searchSegment : "",
                        sku : "",
                        userid : "ef-userid",
                        pixelHost : "pixel.everesttech.net"
                        
                        , allow3rdPartyPixels: 1});
              EF.main();
        };
        window.id5PartnerId=<Your_ID5_PartnerID>
        window.EF = window.EF || {};
        if (window.EF.main) {
            f();
            return;
        }
        window.EF.onloadCallbacks = window.EF.onloadCallbacks || [];
        window.EF.onloadCallbacks[window.EF.onloadCallbacks.length] = f;
        if (!window.EF.jsTagAdded) {
            var efjs = document.createElement('script'); efjs.type = 'text/javascript'; efjs.async = true;
            efjs.src = 'https://www.everestjs.net/static/st.v3.js';
            var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(efjs, s);
            window.EF.jsTagAdded=1;
        }
    })();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

wobei:

* `<ef-userid>` ist eine eindeutige, numerische Benutzer-ID, die Search, Social und Commerce dem Advertiser zuweisen.

* `<Your_ID5_PartnerID>` ist die ID5-Partner-ID des Unternehmens, die das Unternehmen nach Unterzeichnung einer Vereinbarung mit [!DNL ID5] erhält. Schließen Sie diese Variable nur ein, wenn das Unternehmen DSP verwendet und über [benutzerspezifische Segmente verfügt, die Benutzer verfolgen, die mit universellen IDs für ID5 verknüpft sind ](/help/dsp/audiences/universal-ids.md).

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
>* [Format der Tracking-Tags für die Bildkonvertierung](format-conversion-tag-image.md)
