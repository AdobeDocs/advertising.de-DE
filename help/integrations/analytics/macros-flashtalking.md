---
title: Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags
description: Erfahren Sie, warum und wie Sie  [!DNL Analytics for Advertising] -Makros zu Ihren  [!DNL Flashtalking]  hinzufügen
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: 8d9bd2aeed8fa7c6d34be9dbb813b35205ba72b4
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# [!DNL Analytics for Advertising] an [!DNL Flashtalking]-Anzeigen-Tags anhängen

*Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

*Organisationen ohne direkte Partnerschaft nur mit [!DNL Flashtalking]*

*Gilt nur für Advertising DSP*

Wenn Sie Anzeigen-Tags aus [!DNL Flashtalking] für Ihre Advertising DSP-Anzeigen verwenden, müssen Sie Tracking-Parameter an Ihre Landingpage-URLs anhängen. Um die Advertising DSP-Partnerschaft mit [!DNL Flashtalking] zu verwenden, hängen Sie die Parameter für Analytics for Advertising an Ihre Landingpage-URLs an. Die Parameter zeichnen AMO-ID (`s_kwcid`) und `ef_id` Abfragezeichenfolgenparameter in der Landingpage-URL auf, sodass Adobe Advertising Klickdaten für die Anzeigen an Adobe Analytics senden kann.

>[!NOTE]
>
>Wenn Ihr Unternehmen eine direkte Partnerschaft mit [!DNL Flashtalking] hat, ist dieses Verfahren für Sie nicht erforderlich. Melden Sie sich stattdessen bei Ihrem [!DNL Flashtalking]-Konto an und befolgen Sie die [!DNL Flashtalking]-Support-Dokumentation unter `https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros` , um Datenweiterleitungsmakros zur Verfolgung der `s_kwcid` und `ef_id` Tracking-Parameter zu verwenden.

Verwenden Sie Makros für [!DNL Flashtalking] Anzeige- und Videoanzeigen für die folgenden Arten von [!DNL Analytics for Advertising]:

* **Werbetreibende mit dem [!DNL Adobe] [!DNL Analytics for Advertising] JavaScript-Code, der auf ihren Websites implementiert ist**: Der JavaScript-Code zeichnet bereits die AMO-ID (`s_kwcid`) und `ef_id` Abfragezeichenfolgenparameter auf. Die Verwendung von Makros erweitert das Tracking jedoch, um klickbasierte Konversionen einzuschließen, wenn Drittanbieter-Cookies nicht unterstützt werden. Es empfiehlt sich, die Makros in den folgenden Abschnitten zu Ihren Anzeigen-Tags hinzuzufügen, um zusätzliche Clickthrough-Daten zu erfassen, die nicht über den JavaScript-Code erfasst werden.

  >[!NOTE]
  >
  >Der JavaScript-Code ist nur dann eine Lösung für das Klick-Tracking, wenn noch Cookies verfügbar sind. Sobald Cookies eingestellt wurden, ist die Implementierung der folgenden Makros erforderlich.

* **Werbetreibende, deren Websites nicht den [!DNL Analytics for Advertising] JavaScript-Code verwenden und stattdessen [!DNL Analytics] Server-seitige Weiterleitung nur für Clickthrough-Daten verwenden** (ohne Viewthrough-Daten): Die folgenden Makros sind erforderlich, um Klickaktivitäten auf der Site zu melden, die von Anzeigen gesteuert werden, die Sie über Adobe Advertising kaufen.

## Anzeigen-Tags

Hängen Sie in den [!DNL Flashtalking]-Tag-Einstellungen das folgende Makro an das Ende der Clickthrough-URL im `Clicktag` an:

```
[ftqs:[AdobeAMO]]
```

Wenn es sich um die erste oder einzige Abfragezeichenfolge nach der Basis-URL handelt, trennen Sie sie mit einer -`?` von der Basis-URL. Wenn die Basis-URL mehrere Abfragezeichenfolgen enthält, beginnen Sie die erste Zeichenfolge mit einer `?` und jede nachfolgende Zeichenfolge mit einer `&`.

Beispiele:

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## Video-Anzeigen-Tags

Hängen Sie in den [!DNL Flashtalking]-Tag-Einstellungen das folgende Makro an das Ende der Clickthrough-URL im `Clicktag` an:

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Wenn es sich um die erste oder einzige Abfragezeichenfolge nach der Basis-URL handelt, trennen Sie sie mit einer -`?` von der Basis-URL. Wenn die Basis-URL mehrere Abfragezeichenfolgen enthält, beginnen Sie die erste Zeichenfolge mit einer `?` und jede nachfolgende Zeichenfolge mit einer `&`.

Beispiele:

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Überblick über [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising-IDs verwendet von [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md)

