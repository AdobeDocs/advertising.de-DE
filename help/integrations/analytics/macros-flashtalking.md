---
title: Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Flashtalking] Anzeigen-Tags
description: Erfahren Sie, warum und wie Sie [!DNL Analytics for Advertising] Makros für Ihre [!DNL Flashtalking] Adtags
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: ca8260e643f24787f7918249906f3f38f3bbef6d
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Flashtalking] Anzeigen-Tags

*Advertiser mit nur Adobe Advertising-Adobe Analytics-Integration*

*Gilt nur für DSP*

Wenn Sie Anzeigen-Tags aus [!DNL Flashtalking] Hängen Sie für Ihre Advertising DSP Anzeigen Analytics for Advertising-Parameter an Ihre Landingpage-URLs an. Die Parameter zeichnen die AMO-ID (`s_kwcid`) und `ef_id` Abfragezeichenfolgenparameter in der Landingpage-URL, sodass Adobe Advertising Klick-Daten für die Anzeigen an Adobe Analytics senden kann.

Verwenden Sie Makros für [!DNL Flashtalking] Anzeigen und Videoanzeigen für die folgenden Typen [!DNL Analytics for Advertising] Implementierungen:

* **Werbetreibende mit [!DNL Adobe] [!DNL Analytics for Advertising] Auf ihren Websites implementierter JavaScript-Code**: Der JavaScript-Code zeichnet die AMO-ID (`s_kwcid`) und `ef_id` Abfragezeichenfolgenparameter. Durch die Verwendung von Makros wird das Tracking jedoch auch auf klickbasierte Konversionen erweitert, wenn Drittanbieter-Cookies nicht unterstützt werden. Es empfiehlt sich, die Makros in den folgenden Abschnitten zu Ihren Anzeigen-Tags hinzuzufügen, um zusätzliche Clickthrough-Daten zu erfassen, die nicht über den JavaScript-Code erfasst werden.

>[!NOTE]
>
>Der JavaScript-Code ist eine Lösung für Klick-Tracking, während Cookies weiterhin verfügbar sind. Sobald Cookies beendet sind, ist die Implementierung der folgenden Makros erforderlich.

* **Advertiser, deren Websites die [!DNL Analytics for Advertising] JavaScript-Code und stattdessen auf [!DNL Analytics] Serverseitige Weiterleitung nur für Clickthrough-Daten** (ohne Durchsichtsdaten): Die folgenden Makros sind erforderlich, um die Klick-Aktivität auf der Site zu melden, die von Anzeigen gesteuert wird, die Sie über Adobe Advertising kaufen.

## Anzeigen von Anzeigen-Tags

Innerhalb der [!DNL Flashtalking] Fügen Sie das folgende Makro an das Ende der Clickthrough-URL in der `Clicktag` -Feld:

```
[ftqs:[AdobeAMO]]
```

Hierbei handelt es sich um die erste oder einzige Abfragezeichenfolge nach der Basis-URL, die dann von der Basis-URL durch eine `?`. Wenn die Basis-URL mehrere Abfragezeichenfolgen enthält, beginnen Sie die erste Zeichenfolge mit einer `?` und jeder nachfolgenden Zeichenfolge mit `&`.

Beispiele:

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## Videoanzeigen-Tags

Innerhalb der [!DNL Flashtalking] Fügen Sie das folgende Makro an das Ende der Clickthrough-URL in der `Clicktag` -Feld:

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Hierbei handelt es sich um die erste oder einzige Abfragezeichenfolge nach der Basis-URL, die dann von der Basis-URL durch eine `?`. Wenn die Basis-URL mehrere Abfragezeichenfolgen enthält, beginnen Sie die erste Zeichenfolge mit einer `?` und jeder nachfolgenden Zeichenfolge mit `&`.

Beispiele:

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising]](overview.md)
>* [Von verwendete Adobe Advertising-IDs [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Google Campaign Manager 360] Anzeigen-Tags](/help/integrations/analytics/macros-google-campaign-manager.md)
