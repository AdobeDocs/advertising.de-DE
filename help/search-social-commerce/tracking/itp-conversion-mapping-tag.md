---
title: Das Adobe Advertising-Konversions-Zuordnungs-Tag
description: Erfahren Sie mehr über das JavaScript-basierte Konversions-Mapping-Tag für ITP 2.2, das es Adobe Advertisingen ermöglicht, Konversionsereignisse zu verfolgen, die auf einer Seite auftreten, die nicht die Landingpage ist.
exl-id: 6e2515da-2552-4f19-8344-1dee96cbf706
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---

# Das Adobe Advertising-Tag für die JavaScript-Konversions-Zuordnung

*Werbetreibende, die nur Adobe Advertising-Konversions-Tracking verwenden*

Das JavaScript-basierte Konversions-Mapping-Tag des Adobe Advertisings ermöglicht es Adobe Advertisingen, ein Konversionsereignis zu verfolgen, das auf einer Seite auftritt, die nicht auf der Landingpage enthalten ist, wenn es zusätzlich zum Adobe Advertising-JavaScript-v2- oder v3-Konversions-Tracking-Tag verwendet wird. Die ITP 2.2-Lösung speichert das Cookie eines Benutzers im lokalen Speicher in einem von Advertisern verwalteten iFrame. Der lokale Speicher kann dann den Cookie-Wert vom Klick nachgelagert zur Konvertierungsseite beibehalten.

Verwenden Sie das Konversions-Mapping-Tag, um sicherzustellen, dass Adobe Advertising alle Konversionen verfolgen können, die in Apple Safari und Mozilla Firefox-Browsern auftreten, wodurch die Persistenz von Erstanbieter-Cookies eingeschränkt wird. <!-- For all requirements to track conversions from Safari, see "Track Conversions from Apple Safari Browsers." -->

So verwenden Sie das Konversions-Mapping-Tag:

1. [Bereitstellen des Konversions-Mapping-Tags](#deploy-conversion-mapping-tag).

1. Wenn Ihr Unternehmen mehrere Adobe Experience Cloud Identity Service-Organisations-IDs (ehemals &quot;IMS-Organisations-IDs&quot;) verwendet, dann [Konversions-Tags aktualisieren](#update-conversion-tags) , um die Organisations-ID einzuschließen.

1. [Validieren der Tag-Bereitstellung](#validate-conversion-mapping).

## Bereitstellen des JavaScript-Tags für die Konversions-Zuordnung für ITP 2.2 {#deploy-conversion-mapping-tag}

>[!NOTE]
>
>Wenn Sie das JavaScript-Tag für die Konversions-Zuordnung für ITP 2.0 verwenden, ersetzen Sie das vorhandene Tag auf allen Konversionsseiten durch eines der folgenden Tags.<!-- any other instructions, too? Point them to the other page on Track Conversions from Safari...." -->

* Wenn Ihr Unternehmen eine einzige Organisations-ID verwendet, die für Ihr Search-, Social- und Commerce-Konto verwendet wird, verwenden Sie das folgende Tag:

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" userid="{AMO User ID}"></script>`

  wo Sie `{AMO User ID}` mit der eindeutigen Benutzer-ID für Ihr Search-, Social- und Commerce-Konto.

* Wenn Ihr Unternehmen mehrere Organisations-IDs verwendet, verwenden Sie das folgende Tag:

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="{xxxxxx@AdobeOrg}" userid="{AMO User ID}"></script>`

  wobei:

   * Sie ersetzen den Wert `{xxxxxx@AdobeOrg}` mit der Organisations-ID, für die die Konversionen der Seite verfolgt werden. Verwenden Sie für alle Konversionsseiten dieselbe Organisations-ID.

   * ersetzen `{AMO User ID}` mit der eindeutigen Benutzer-ID für Ihr Search-, Social- und Commerce-Konto.

* Wenn Sie ein Tag-Management-System verwenden, das das Hinzufügen von `imsorgid` zum Skript-Tag hinzu und verwenden Sie stattdessen den folgenden Code:

  *Wenn Ihr Unternehmen eine einzige Organisations-ID verwendet:

  ```
  <script>
  window.ad_cloud = window.ad_cloud || {};
  window.ad_cloud.userid = "{AMO User ID}"
  </script>
  <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
  ```

  wo Sie `{AMO User ID}` mit der eindeutigen Benutzer-ID für Ihr Search-, Social- und Commerce-Konto.

   * Wenn Ihr Unternehmen mehrere Organisations-IDs verwendet:

     ```
     <script>
     window.ad_cloud = window.ad_cloud || {};
     window.ad_cloud.imsorgid = "{xxxxxx@AdobeOrg}"
     window.ad_cloud.userid = "{AMO User ID}"
     </script>
     <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
     ```

     wobei:

      * Sie ersetzen den Wert `{xxxxxx@AdobeOrg}` mit der Organisations-ID, für die die Konversionen der Seite verfolgt werden. Verwenden Sie für alle Konversionsseiten dieselbe Organisations-ID.

      * ersetzen `{AMO User ID}` mit der eindeutigen Benutzer-ID für Ihr Search-, Social- und Commerce-Konto.

Wenn Sie den Wert Ihrer Organisations-ID oder Ihrer Benutzer-ID für Search, Social und Commerce nicht kennen, fragen Sie Ihren Adobe Account Manager.

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

### Wo wird das Tag hinzugefügt?

Fügen Sie das Tag zu jeder Seite hinzu, bei der es sich um eine Landingpage aus einem Suchklick handeln könnte (idealerweise auf allen Seiten, da sich Landingpages im Laufe der Zeit ändern können). Sie muss vor dem Konversions-Tracking-Tag für JavaScript v3-Konversionen in Adobe Advertising geladen werden.

Wenn sie in einem iframe- oder container-Tag platziert wird, gehen Sie wie folgt vor:

* Der iframe sollte sich auf derselben Ebene wie die Domäne der obersten Ebene befinden.

* Das Konversions-Mapping-Tag sollte nur eine (1) Ebene unter der Domäne der obersten Ebene sein.

## Aktualisieren der JavaScript-Konversions-Tags {#update-conversion-tags}

Wenn Ihr Unternehmen mehrere Organisations-IDs verwendet, fügen Sie die Organisations-ID, für die die Konversionen einer Seite verfolgt werden, zu Ihren vorhandenen JavaScript-Konversions-Tags hinzu.

Wenn Ihr Unternehmen eine Organisations-ID verwendet, ist dieser Schritt nicht erforderlich.

### JavaScript V2-Tags

Fügen Sie am Anfang des Konvertierungsskript-Tags die folgende Zeichenfolge hinzu:

`ef_imsorgid="{xxxxxx@AdobeOrg}";`

wo Sie den Wert ersetzen `{xxxxxx@AdobeOrg}` mit der Organisations-ID, für die die Konversionen der Seite verfolgt werden.

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

### JavaScript V3-Tags

Nachher `window.EF` definiert ist, fügen Sie die folgende Zeichenfolge hinzu:

`window.EF.imsorgid = "{xxxxxx@AdobeOrg}";`

wo Sie den Wert ersetzen `{xxxxxx@AdobeOrg}` mit der Organisations-ID, für die die Konversionen der Seite verfolgt werden.

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

Wenden Sie sich an Ihr Adobe Account Team, um Hilfe bei der Validierung des Konversions-Mapping-Tags und des normalen Konversions-Tags zu erhalten (sofern Sie es aktualisiert haben).
