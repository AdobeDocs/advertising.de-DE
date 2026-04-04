---
title: Verwenden der  [!DNL Last Event Service] JavaScript-Bibliothek mit [!DNL Web SDK]
description: Erfahren Sie, wie Sie für Ihre -Implementierung von der  [!DNL Analytics] [!DNL visitorAPI]Bibliothek zur  [!DNL Experience Platform] [!DNL Web SDK]-Bibliothek  [!DNL Analytics for Advertising] .
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
TQID: https://experienceleague.adobe.com/zT1lQV1yotCfJJdzTBGzSspsNEKQEB5ulxYE0qyWa9Q
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 0%

---

# Verwenden der [!DNL Last Event Service] JavaScript-Bibliothek mit Adobe Experience Platform [!DNL Web SDK]

*Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

Wenn Ihr Unternehmen die veraltete Adobe Analytics `visitorAPI.js`-Bibliothek für die Datenerfassung verwendet, können Sie optional zur Verwendung der [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de)-Bibliothek (`alloy.js`) wechseln, über die Sie über die [!DNL Edge Network] mit den verschiedenen Experience Cloud-Services interagieren können.

Die [!DNL Analytics for Advertising] [!DNL Last Event Service] JavaScript-Bibliothek zeichnet unverändert die Durchsichts- und Klickereignisse auf und ordnet sie mithilfe einer zusätzlichen ID (`SDID`) den zugehörigen Konversionen zu. Die [!DNL Web SDK]-Bibliothek stellt jedoch keine [!DNL stitch ID] bereit. Um die [!DNL Web SDK] für [!DNL Analytics for Advertising] zu verwenden, müssen Sie 1) das [!DNL Last Event Service]-Tag, das Sie auf Ihren Web-Seiten verwenden, und 2) Ihre [!DNL Web SDK] `sendEvent` entsprechend ändern.

## Schritt 1: [!DNL Last Event Service]-Tag bearbeiten, um eine `[!DNL StitchID]` zu generieren

Fügen Sie in dem [!DNL Analytics for Advertising] [!DNL Last Event Service]-Tag, das Sie auf Ihren Web-Seiten verwenden, Code hinzu, um die `[!DNL StitchID]` mit dem zufälligen ID-Generator zu generieren, der in der Bibliothek gebündelt ist.

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

Fügen Sie die folgende Eigenschaft in Ihren [!DNL Web SDK] `sendEvent`-Befehl ein, um die [!DNL StitchID] zur [!DNL Experience Edge] als [!DNL Experience Data Model] (XDM) an [!DNL Analytics] zu senden.<!-- The library sends the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] verwendet den Wert als `SDID`.

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
>* [Überblick über [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript-Code für [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)
