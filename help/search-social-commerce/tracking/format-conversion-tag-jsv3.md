---
title: Format der JavaScript-Konversionsverfolgungstags Version 3
description: Verweisen Sie auf das Format von JavaScript-Konversionsverfolgungstags Version 3.
exl-id: 9fc6bb15-d880-4353-a8c5-260b7932ab34
feature: Search Tracking
source-git-commit: dda4ff8e7538bc742caa50862575cb4e46a1371d
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Format der JavaScript-Konversionsverfolgungstags Version 3

Das folgende Format ist für Sites, die HTTPS verwenden. Bei Sites, die HTTP verwenden, sollten die URLs mit „http“ beginnen.

>[!NOTE]
>
>Informationen dazu, wann Version 2 und Version 3 verwendet werden sollten, finden Sie in den [Häufig gestellte Fragen zu Tracking-Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

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
        window.id5PartnerId=<ID5_PartnerID>
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

Dabei gilt:

* `<ef-userid>` ist eine eindeutige numerische Benutzer-ID, die Search, Social und Commerce dem Advertiser zuweist.

* `<ID5_PartnerID>` ist die ID5-Partner-ID des Unternehmens, die das Unternehmen nach Unterzeichnung einer Vereinbarung mit [!DNL ID5] erhält. Schließen Sie diese Variable nur ein, wenn das Unternehmen DSP verwendet und über [benutzerdefinierte Segmente verfügt, die Benutzer verfolgen, die mit universellen ID5-IDs verknüpft sind](/help/dsp/audiences/universal-ids.md).

* `<propertyname>` ist die Konvertierung in „Track“. Wenn Sie z. B. eine Konversion mit dem Namen „Registrierung“ verfolgen, enthält das Tag den Parameter `ev_registration=<registration>` und Sie müssen den tatsächlichen Umsatz für jede Transaktion (z. B. `ev_registration=1`) übergeben. Wenn mehrere Eigenschaften verfolgt werden, werden sie durch ein kaufmännisches Und-Zeichen (`&`) verbunden, z. B. `ev_registration=<registration>&ev_sale=<sale>` (z. B. `ev_registration=1&ev_sale=12.99`). **Hinweis:** Der Eigenschaftsname darf keine Sonderzeichen enthalten.

* `<transid>` ist eine eindeutige Transaktions-ID (z. B. eine tatsächliche Auftrags-ID), die der Advertiser generiert und übergibt, um eine Transaktion zu identifizieren. Sie ist nur enthalten, wenn die Option &quot;[!UICONTROL Include unique transaction IDs]&quot; ausgewählt ist.

  Search, Social und Commerce verwenden die Transaktions-ID, um doppelte Transaktionen mit derselben Transaktions-ID und demselben Eigenschaftswert zu eliminieren. Die Transaktions-ID ist im [!UICONTROL Transaction Report] enthalten, mit dem Sie Daten auf dem Adobe Advertising mit den Daten des Werbetreibenden validieren können. **Hinweis:** Wenn die Daten des Werbetreibenden keine eindeutige ID pro Transaktion enthalten, generiert Search, Social und Commerce weiterhin eine ID basierend auf der Transaktionszeit.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Über Adobe Advertising-Konversions-Tracking-Tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Erzeugen eines Adobe Advertising-Konvertierungs-Tags](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Häufig gestellte Fragen zu Konversions- und Seitenansichts-Tracking-Tags](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Format von JavaScript-Konversionsverfolgungstags, Version 2](format-conversion-tag-jsv2.md)
>* [Format der Tracking-Tags für die Bildkonvertierung](format-conversion-tag-image.md)
