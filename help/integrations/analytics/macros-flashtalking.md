---
title: Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Flashtalking] Anzeigen-Tags
description: Erfahren Sie, warum und wie Sie [!DNL Analytics for Advertising] Makros für Ihre [!DNL Flashtalking] Adtags
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Flashtalking] Anzeigen-Tags

*Werbetreibende, die nur über eine Adobe Advertising-Adobe Analytics-Integration verfügen*

*Gilt nur für DSP*

Wenn Sie Anzeigen-Tags aus [!DNL Flashtalking] Hängen Sie für Ihre Advertising DSP Anzeigen Analytics for Advertising-Parameter an Ihre Landingpage-URLs an. Die Parameter zeichnen die AMO-ID (`s_kwcid`) und `ef_id` Abfragezeichenfolgenparameter in der Landingpage-URL, sodass Adobe Advertising Klickdaten für die Anzeigen an Adobe Analytics senden können.

Verwenden Sie Makros für [!DNL Flashtalking] Anzeigen und Videoanzeigen für die folgenden Typen [!DNL Analytics for Advertising] Implementierungen:

* **Werbetreibende mit [!DNL Adobe] [!DNL Analytics for Advertising] Auf ihren Websites implementierter JavaScript-Code**: Der JavaScript-Code zeichnet die AMO-ID (`s_kwcid`) und `ef_id` Abfragezeichenfolgenparameter. Durch die Verwendung von Makros wird das Tracking jedoch auch auf klickbasierte Konversionen erweitert, wenn Drittanbieter-Cookies nicht unterstützt werden. Es empfiehlt sich, die Makros in den folgenden Abschnitten zu Ihren Anzeigen-Tags hinzuzufügen, um zusätzliche Clickthrough-Daten zu erfassen, die nicht über den JavaScript-Code erfasst werden.

>[!NOTE]
>
>Der JavaScript-Code ist eine Lösung für Klick-Tracking, während Cookies weiterhin verfügbar sind. Sobald Cookies beendet sind, ist die Implementierung der folgenden Makros erforderlich.

* **Advertiser, deren Websites die [!DNL Analytics for Advertising] JavaScript-Code und stattdessen auf [!DNL Analytics] Serverseitige Weiterleitung nur für Clickthrough-Daten** (ohne Durchsichtsdaten): Die folgenden Makros sind erforderlich, um die Klick-Aktivität auf der Site zu melden, die von Anzeigen gesteuert wird, die Sie über den Adobe Advertising kaufen.

## Anzeigen von Anzeigen-Tags

Innerhalb der [!DNL Flashtalking] Fügen Sie das folgende Makro an das Ende der Clickthrough-URL in der `Clicktag` -Feld:

```html
?[ftqs:[AdobeAMO]]
```

Beispiel:  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

## Videoanzeigen-Tags

Innerhalb der [!DNL Flashtalking] Fügen Sie das folgende Makro an das Ende der Clickthrough-URL in der `Clicktag` -Feld:

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Beispiel:  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising]](overview.md)
>* [Von verwendete Adobe Advertising-IDs [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Google Campaign Manager 360] Anzeigen-Tags](/help/integrations/analytics/macros-google-campaign-manager.md)
