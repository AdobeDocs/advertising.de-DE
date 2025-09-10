---
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---
# Adobe Advertising EF-IDs

Die EF ID ist ein eindeutiges Token, das Adobe Advertising verwendet, um Aktivitäten mit einem Online-Klick oder einer Anzeigenbelichtung auf individueller Browser- oder Geräteebene zu verknüpfen. EF-IDs dienen hauptsächlich als Schlüssel zum Senden von [!DNL Analytics] und Customer Journey Analytics-Daten an Adobe Advertising für die Berichterstellung und Angebotsoptimierung innerhalb von Adobe Advertising.

[!DNL Analytics] wird die EF-ID in der Dimension [eine [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=de) oder [!DNL rVar] (reservierte [!DNL eVar]) (Adobe Advertising EF ID) gespeichert.

Bei Customer Journey Analytics wird die EF-ID in der `trackingIdentities`-Eigenschaft des `conversionDetails`-Objekts gespeichert, das Teil der [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension] ist.
