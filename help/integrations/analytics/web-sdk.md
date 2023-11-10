---
title: Verwenden der [!DNL Last Event Service] JavaScript-Bibliothek mit [!DNL Web SDK]
description: Erfahren Sie, wie Sie mit dem [!DNL Analytics] [!DNL visitorAPI] -Bibliothek [!DNL Experience Platform] [!DNL Web SDK] Bibliothek für Ihre [!DNL Analytics for Advertising] Implementierung.
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: 687f146b27765d59f172284e4cff7ab5c0e57b50
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# Verwenden der [!DNL Last Event Service] JavaScript-Bibliothek mit Adobe Experience Platform [!DNL Web SDK]

*Advertiser mit nur Adobe Advertising-Adobe Analytics-Integration*

Wenn Ihr Unternehmen die veraltete Adobe Analytics verwendet `visitorAPI.js` -Bibliothek für die Datenerfassung können Sie optional zur Verwendung der [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) Bibliothek (`alloy.js`), die Ihnen die Interaktion mit den verschiedenen Experience Cloud-Diensten über die [!DNL Edge Network].

Die [!DNL Analytics for Advertising] [!DNL Last Event Service] Die JavaScript-Bibliothek zeichnet im Istzustand Durchsichts- und Clickthrough-Ereignisse auf und ordnet sie mithilfe einer zusätzlichen ID (`SDID`). Die [!DNL Web SDK] -Bibliothek bietet jedoch keine [!DNL stitch ID]. So verwenden Sie die [!DNL Web SDK] für [!DNL Analytics for Advertising], müssen Sie 1) der Variablen [!DNL Last Event Service] Tag, das Sie auf Ihren Webseiten verwenden, und 2) Ihre [!DNL Web SDK] `sendEvent` -Befehle entsprechend.

## Schritt 1: Bearbeiten Ihrer [!DNL Last Event Service] Tag zum Generieren eines `[!DNL StitchID]`

Im [!DNL Analytics for Advertising] [!DNL Last Event Service] Tag, das Sie auf Ihren Webseiten verwenden, fügen Sie Code hinzu, um die `[!DNL StitchID]` mit dem zufälligen ID-Generator, der in der Bibliothek gebündelt ist.

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
          stitchId = AdCloudEvent('IMS ORG Id''rsid').generateRandomId();
</script>
```

## Schritt 2: Verwenden Sie [!DNL Web SDK] , um die [!DNL StitchID] als XDM-Daten für [!DNL Analytics]

Fügen Sie die folgende Eigenschaft in Ihre [!DNL Web SDK] `sendEvent` -Befehl zum Senden der [!DNL StitchID] nach [!DNL Experience Edge] as [!DNL Experience Data Model] (XDM)-Daten für [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] verwendet den Wert als `SDID`.

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
>* [Übersicht über [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript-Code für [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)
