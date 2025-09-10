---
source-git-commit: c56a8caf8db4c76a41a96c48cbe3996078924cc6
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---
# Adobe Advertising AMO-IDs

## Adobe Advertising AMO-IDs {#amo-id}

Die AMO ID verfolgt jede einzelne Anzeigenkombination auf einer weniger detaillierten Ebene und wird für die [!DNL Analytics] und Customer Journey Analytics-Datenklassifizierung und die Aufnahme von Werbemetriken (wie Impressionen, Klicks und Kosten) aus Adobe Advertising verwendet.

[!DNL Analytics] wird die AMO-ID in einer [eVar- oder ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)-Dimension (AMO-ID) gespeichert.

Bei Customer Journey Analytics wird die AMO-ID in der `trackingCode`-Eigenschaft des `conversionDetails`-Objekts gespeichert, das Teil der [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension] ist.

Die AMO-ID wird auch als `s_kwcid` bezeichnet, was manchmal als &quot;[!DNL squid]&quot; ausgesprochen wird.
