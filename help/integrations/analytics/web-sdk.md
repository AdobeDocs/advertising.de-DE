---
title: Verwenden der [!DNL Last Event Service] JavaScript-Bibliothek mit [!DNL Web SDK]
description: Erfahren Sie, wie Sie für Ihre [!DNL Analytics for Advertising] Implementierung von der Verwendung der Bibliothek  [!DNL Analytics] [!DNL visitorAPI] zur Bibliothek [!DNL Experience Platform] [!DNL Web SDK] wechseln.
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Verwenden der [!DNL Last Event Service] JavaScript-Bibliothek mit Adobe Experience Platform [!DNL Web SDK]

*Advertiser mit nur einer Adobe Advertising-Adobe Analytics-Integration*

Wenn Ihr Unternehmen die veraltete Adobe Analytics `visitorAPI.js` -Bibliothek für die Datenerfassung verwendet, können Sie optional zur Verwendung der [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) -Bibliothek (`alloy.js`) wechseln, mit der Sie über die [!DNL Edge Network] mit den verschiedenen Experience Cloud-Diensten interagieren können.

Die JavaScript-Bibliothek [!DNL Analytics for Advertising] [!DNL Last Event Service] zeichnet unverändert Durchsichts- und Clickthrough-Ereignisse auf und ordnet sie mithilfe einer zusätzlichen ID (`SDID`) den zugehörigen Konversionen zu. Die Bibliothek [!DNL Web SDK] enthält jedoch keine [!DNL stitch ID]. Um den [!DNL Web SDK] für [!DNL Analytics for Advertising] zu verwenden, müssen Sie 1) das auf Ihren Webseiten verwendete [!DNL Last Event Service] -Tag und 2) Ihre [!DNL Web SDK] `sendEvent` -Befehle entsprechend ändern.

## Schritt 1: Bearbeiten Sie Ihr [!DNL Last Event Service]-Tag, um einen `[!DNL StitchID]` zu generieren.

Fügen Sie im Tag [!DNL Analytics for Advertising] [!DNL Last Event Service] , das Sie auf Ihren Webseiten verwenden, Code hinzu, um den `[!DNL StitchID]` mit dem zufälligen ID-Generator zu generieren, der in der Bibliothek gebündelt ist.

**Legacy-Tag:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

**Neues Tag:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

## Schritt 2: Verwenden Sie [!DNL Web SDK], um die [!DNL StitchID] als XDM-Daten für [!DNL Analytics] zu senden.

Fügen Sie die folgende Eigenschaft in Ihren Befehl [!DNL Web SDK] `sendEvent` ein, um die [!DNL StitchID] als [!DNL Experience Data Model] (XDM)-Daten für [!DNL Analytics] an [!DNL Experience Edge] zu senden.<!-- The library sends the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] verwendet den Wert als `SDID`.

**Eigenschaft zum Hinzufügen:**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**Beispiel:**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [Überblick über  [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript-Code für  [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)
