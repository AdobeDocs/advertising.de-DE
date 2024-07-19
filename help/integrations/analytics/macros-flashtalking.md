---
title: Anhängen von [!DNL Analytics for Advertising] Makros an  [!DNL Flashtalking] Anzeigen-Tags
description: Erfahren Sie, warum und wie Sie [!DNL Analytics for Advertising] Makros zu Ihren [!DNL Flashtalking] Anzeigen-Tags hinzufügen
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# Anhängen von [!DNL Analytics for Advertising] Makros an [!DNL Flashtalking] Anzeigen-Tags

*Advertiser mit nur einer Adobe Advertising-Adobe Analytics-Integration*

*Nur für Advertising DSP anwendbar*

Wenn Sie Anzeigen-Tags von [!DNL Flashtalking] für Ihre Advertising DSP-Anzeigen verwenden, hängen Sie Analytics für Advertising-Parameter an Ihre Landingpage-URLs an. In den Parametern werden AMO-ID-Parameter (`s_kwcid`) und `ef_id` Abfragezeichenfolgenparameter in der URL der Landingpage aufgezeichnet, sodass Adobe Advertising Klick-Daten für die Anzeigen an Adobe Analytics senden kann.

Verwenden Sie Makros für [!DNL Flashtalking] Display- und Videoanzeigen für die folgenden Typen von [!DNL Analytics for Advertising] -Implementierungen:

* **Advertiser mit dem auf ihren Websites implementierten JavaScript-Code [!DNL Adobe] [!DNL Analytics for Advertising]**: Der JavaScript-Code zeichnet bereits die Abfragezeichenfolgenparameter AMO ID (`s_kwcid`) und `ef_id` auf. Durch die Verwendung von Makros wird das Tracking jedoch auch auf klickbasierte Konversionen erweitert, wenn Drittanbieter-Cookies nicht unterstützt werden. Es empfiehlt sich, die Makros in den folgenden Abschnitten zu Ihren Anzeigen-Tags hinzuzufügen, um zusätzliche Clickthrough-Daten zu erfassen, die nicht über den JavaScript-Code erfasst werden.

>[!NOTE]
>
>Der JavaScript-Code ist eine Lösung für Klick-Tracking, solange Cookies noch verfügbar sind. Sobald Cookies beendet sind, ist die Implementierung der folgenden Makros erforderlich.

* **Werbetreibende, deren Websites nicht den JavaScript-Code von [!DNL Analytics for Advertising] verwenden und stattdessen die serverseitige Weiterleitung nur für Clickthrough-Daten verwenden** (ohne Viewthrough-Daten): Die folgenden Makros sind erforderlich, um die Klick-Aktivität auf der Site über Anzeigen zu melden, die Sie über Adobe Advertising kaufen.[!DNL Analytics]

## Anzeigen von Anzeigen-Tags

Hängen Sie in den Einstellungen für das Anzeigen-Tag [!DNL Flashtalking] das folgende Makro am Ende der Clickthrough-URL im Feld `Clicktag` an:

```
[ftqs:[AdobeAMO]]
```

Wenn es die erste oder einzige Abfragezeichenfolge nach der Basis-URL ist, trennen Sie sie von der Basis-URL mit einem &quot;`?`&quot;. Wenn die Basis-URL mehrere Abfragezeichenfolgen enthält, beginnen Sie die erste Zeichenfolge mit einem `?` und jede nachfolgende Zeichenfolge mit einem `&`.

Beispiele:

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## Videoanzeigen-Tags

Hängen Sie in den Einstellungen für das Anzeigen-Tag [!DNL Flashtalking] das folgende Makro am Ende der Clickthrough-URL im Feld `Clicktag` an:

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Wenn es die erste oder einzige Abfragezeichenfolge nach der Basis-URL ist, trennen Sie sie von der Basis-URL mit einem &quot;`?`&quot;. Wenn die Basis-URL mehrere Abfragezeichenfolgen enthält, beginnen Sie die erste Zeichenfolge mit einem `?` und jede nachfolgende Zeichenfolge mit einem `&`.

Beispiele:

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Überblick über  [!DNL Analytics for Advertising]](overview.md)
>* [Von  [!DNL Analytics]](/help/integrations/analytics/ids.md) verwendete Adobe Advertising-IDs
>* [Anhängen von [!DNL Analytics for Advertising] Makros an  [!DNL Google Campaign Manager 360] Anzeigen-Tags](/help/integrations/analytics/macros-google-campaign-manager.md)

