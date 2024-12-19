---
title: Das Adobe Advertising-Konversionszuordnungs-Tag
description: Erfahren Sie mehr über das JavaScript-basierte Konversionszuordnungs-Tag für ITP 2.2, mit dem Adobe Advertising ein Konversionsereignis verfolgen kann, das auf einer Seite auftritt, die nicht die Landingpage ist.
exl-id: cbeaf3cd-f1ab-419d-bba8-58a1c8215352
feature: Search Tracking
source-git-commit: 2c755eaa01f5bc7606074bb0fc276901c21ef807
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Das Adobe Advertising JavaScript Conversion Mapping Tag

*Werbetreibende nur mit Adobe Advertising-Konversions-Tracking*

Wenn das Adobe Advertising JavaScript-basierte Konversionszuordnungs-Tag zusätzlich zum Adobe Advertising JavaScript v2- oder v3-Konversionsverfolgungs-Tag verwendet wird, kann Adobe Advertising ein Konversionsereignis verfolgen, das auf einer Seite auftritt, die nicht die Landingpage ist. Die ITP 2.2-Lösung speichert das Cookie eines Benutzers lokal in einem iFrame, der dem Werbetreibenden gehört. Der lokale Speicher kann dann den Cookie-Wert vom Klick stromabwärts zur Konversionsseite beibehalten.

Verwenden Sie das Tag für die Konversionszuordnung , um sicherzustellen, dass Adobe Advertising alle Konvertierungen verfolgen kann, die in Apple Safari- und Mozilla Firefox-Browsern auftreten, welche die Persistenz von Erstanbieter-Cookies einschränken. <!-- For all requirements to track conversions from Safari, see "Track Conversions from Apple Safari Browsers." -->

So verwenden Sie das Konversionszuordnungs-Tag:

1. [Stellen Sie das Konversionszuordnungs-Tag bereit](#deploy-conversion-mapping-tag).

1. Wenn Ihr Unternehmen mehrere Organisations-IDs für den Adobe Experience Cloud Identity Service (früher IMS-Organisations-IDs genannt) verwendet, [aktualisieren Sie Ihre Konversions-Tags](#update-conversion-tags) um die Organisations-ID aufzunehmen.

1. [Validieren Sie die Tag-Bereitstellung](#validate-conversion-mapping).

## Bereitstellen des JavaScript-Konversionszuordnungs-Tags für ITP 2.2 {#deploy-conversion-mapping-tag}

>[!NOTE]
>
>Wenn Sie das Konversionszuordnungs-Tag von JavaScript für ITP 2.0 verwenden, ersetzen Sie das vorhandene Tag auf allen Konversionsseiten durch eines der folgenden Tags.<!-- any other instructions, too? Point them to the other page on Track Conversions from Safari...." -->

* Wenn Ihr Unternehmen eine einzige Organisations-ID verwendet, die für Ihr Search-, Social- und Commerce-Konto verwendet wird, verwenden Sie das folgende Tag:

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" userid="{AMO User ID}"></script>`

  wobei Sie `{AMO User ID}` durch die eindeutige Benutzer-ID für Ihr Search-, Social- und Commerce-Konto ersetzen.

* Wenn Ihr Unternehmen mehrere Organisations-IDs verwendet, verwenden Sie das folgende Tag:

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="{xxxxxx@AdobeOrg}" userid="{AMO User ID}"></script>`

  Dabei gilt:

   * Sie ersetzen den Wert `{xxxxxx@AdobeOrg}` durch die Organisations-ID, für die die Konversionen der Seite verfolgt werden. Verwenden Sie dieselbe Organisations-ID für alle Konversionsseiten.

   * Sie ersetzen `{AMO User ID}` durch die eindeutige Benutzer-ID für Ihr Search-, Social- und Commerce-Konto.

* Wenn Sie ein Tag-Management-System verwenden, das das Hinzufügen der `imsorgid` Variable zum Skript-Tag nicht unterstützt, verwenden Sie stattdessen den folgenden Code:

  *Wenn Ihr Unternehmen eine einzige Organisations-ID verwendet:

  ```
  <script>
  window.ad_cloud = window.ad_cloud || {};
  window.ad_cloud.userid = "{AMO User ID}"
  </script>
  <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
  ```

  wobei Sie `{AMO User ID}` durch die eindeutige Benutzer-ID für Ihr Search-, Social- und Commerce-Konto ersetzen.

   * Wenn Ihr Unternehmen mehrere Organisations-IDs verwendet:

     ```
     <script>
     window.ad_cloud = window.ad_cloud || {};
     window.ad_cloud.imsorgid = "{xxxxxx@AdobeOrg}"
     window.ad_cloud.userid = "{AMO User ID}"
     </script>
     <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
     ```

     Dabei gilt:

      * Sie ersetzen den Wert `{xxxxxx@AdobeOrg}` durch die Organisations-ID, für die die Konversionen der Seite verfolgt werden. Verwenden Sie dieselbe Organisations-ID für alle Konversionsseiten.

      * Sie ersetzen `{AMO User ID}` durch die eindeutige Benutzer-ID für Ihr Search-, Social- und Commerce-Konto.

Wenn Sie den Wert Ihrer Organisations-ID oder Ihrer Benutzer-ID für Search, Social und Commerce nicht kennen, wenden Sie sich an Ihr Adobe-Account-Team.

### Beispiele

```
<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="abc12345@AdobeOrg" userid="99999"></script>`
```

```
<script>
window.ad_cloud = window.ad_cloud || {};
window.ad_cloud.imsorgid = "abc12345@AdobeOrg"
window.ad_cloud.userid = "99999"
</script>
<script src="//www.everestjs.net/static/amo-conversion-mapper.js"></script>
```

### Hinzufügen des Tags

Fügen Sie das Tag auf jeder Seite hinzu, die eine Landingpage aus einem Suchklick sein könnte (idealerweise auf allen Seiten, da sich die Landingpages im Laufe der Zeit ändern können). Es muss vor dem Konversionsverfolgungstag von Adobe Advertising JavaScript v3 geladen werden.

Wenn es in einem iframe- oder Container-Tag platziert ist, dann:

* Der iframe sollte auf derselben Ebene wie die Domain auf oberster Ebene sein.

* Das Konversionszuordnungs-Tag sollte nur eine Ebene (1) unter der Domain der obersten Ebene liegen.

## Aktualisieren von JavaScript-Konversions-Tags {#update-conversion-tags}

Wenn Ihr Unternehmen mehrere Organisations-IDs verwendet, fügen Sie die Organisations-ID, für die die Konversionen einer Seite verfolgt werden, zu Ihren bestehenden JavaScript-Konversions-Tags hinzu.

Wenn Ihr Unternehmen eine Organisations-ID verwendet, ist dieser Schritt nicht erforderlich.

### JavaScript v2-Tags

Fügen Sie die folgende Zeichenfolge am Anfang des Konvertierungsskript-Tags hinzu:

`ef_imsorgid="{xxxxxx@AdobeOrg}";`

wobei Sie den Wert `{xxxxxx@AdobeOrg}` durch die Organisations-ID ersetzen, für die die Konversionen der Seite verfolgt werden.

Beispiel:

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
ef_imsorgid = "abc12345@AdobeOrg";
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

### JavaScript v3-Tags

Nachdem `window.EF` definiert wurde, fügen Sie die folgende Zeichenfolge hinzu:

`window.EF.imsorgid = "{xxxxxx@AdobeOrg}";`

wobei Sie den Wert `{xxxxxx@AdobeOrg}` durch die Organisations-ID ersetzen, für die die Konversionen der Seite verfolgt werden.

Beispiel:

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
        window.EF = window.EF || {};
        window.EF.imsorgid ="abc12345@AdobeOrg";
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

## Validieren der Tag-Bereitstellung {#validate-conversion-mapping}

Bitten Sie Ihr Adobe-Konto-Team um Hilfe bei der Validierung des Konversionszuordnungs-Tags und des regulären Konversions-Tags (wenn Sie es aktualisiert haben).
