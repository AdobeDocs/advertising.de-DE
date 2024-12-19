---
title: Verwenden der  [!DNL Last Event Service] JavaScript-Bibliothek mit [!DNL Web SDK]
description: Erfahren Sie, wie Sie für Ihre -Implementierung von der  [!DNL Analytics] [!DNL visitorAPI]Bibliothek zur  [!DNL Experience Platform] [!DNL Web SDK]-Bibliothek  [!DNL Analytics for Advertising] .
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Verwenden der [!DNL Last Event Service] JavaScript Library mit Adobe Experience Platform [!DNL Web SDK]

*Nur Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

Wenn Ihr Unternehmen die veraltete Adobe Analytics `visitorAPI.js`-Bibliothek für die Datenerfassung verwendet, können Sie optional zur Verwendung der [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html)-Bibliothek (`alloy.js`) wechseln, wodurch Sie über die [!DNL Edge Network] mit den verschiedenen Experience Cloud-Services interagieren können.

Die [!DNL Analytics for Advertising] [!DNL Last Event Service] JavaScript-Bibliothek zeichnet unverändert die Durchsichts- und Klickereignisse auf und ordnet sie mithilfe einer zusätzlichen ID (`SDID`) den zugehörigen Konversionen zu. Die [!DNL Web SDK]-Bibliothek stellt jedoch keine [!DNL stitch ID] bereit. Um die [!DNL Web SDK] für [!DNL Analytics for Advertising] zu verwenden, müssen Sie 1) das [!DNL Last Event Service]-Tag, das Sie auf Ihren Web-Seiten verwenden, und 2) Ihre [!DNL Web SDK] `sendEvent` entsprechend ändern.

## Schritt 1: Bearbeiten Sie Ihr [!DNL Last Event Service]-Tag, um eine `[!DNL StitchID]` zu generieren

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

## Schritt 2: Verwenden Sie [!DNL Web SDK] , um die [!DNL StitchID] als XDM-Daten für [!DNL Analytics] zu senden.

Fügen Sie die folgende Eigenschaft in Ihren [!DNL Web SDK] `sendEvent`-Befehl ein, um die [!DNL StitchID] zur [!DNL Analytics] als [!DNL Experience Data Model] (XDM) an [!DNL Experience Edge] zu senden.<!-- The library sends the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] verwendet den Wert als `SDID`.

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
