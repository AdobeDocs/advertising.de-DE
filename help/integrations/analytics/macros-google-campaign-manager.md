---
title: Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags
description: Erfahren Sie, warum und wie Sie  [!DNL Analytics for Advertising] -Makros zu Ihren  [!DNL Google Campaign Manager 360]  hinzufügen
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: aa41ba08ba83bfacbc2541c0f0d90336b3c36305
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# [!DNL Analytics for Advertising] an [!DNL Google Campaign Manager 360]-Anzeigen-Tags anhängen

*Nur Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

*Gilt nur für Advertising DSP*

Wenn Sie Anzeigen-Tags aus [!DNL Google Campaign Manager 360] für Ihre Advertising DSP-Anzeigen verwenden, hängen Sie [!DNL Analytics for Advertising] mithilfe des [`%p`-Makros an Ihre Landingpage-URLs an](https://support.google.com/campaignmanager/table/6096962). Die Parameter zeichnen AMO-ID (`s_kwcid`) und `ef_id` Abfragezeichenfolgenparameter in der Landingpage-URL auf, sodass Adobe Advertising Klickdaten für die Anzeigen an Adobe Analytics senden kann.

Verwenden Sie Makros für [!DNL Campaign Manager 360] Anzeige- und Videoanzeigen für die folgenden Arten von [!DNL Analytics for Advertising]:

* **Werbetreibende mit dem [!DNL Adobe] [!DNL Analytics for Advertising] JavaScript-Code, der auf ihren Websites implementiert ist**: Der JavaScript-Code zeichnet bereits die AMO-ID (`s_kwcid`) und `ef_id` Abfragezeichenfolgenparameter auf. Die Verwendung von Makros erweitert das Tracking jedoch, um klickbasierte Konversionen einzuschließen, wenn Drittanbieter-Cookies nicht unterstützt werden. Es empfiehlt sich, die Makros in den folgenden Abschnitten zu Ihren Anzeigen-Tags hinzuzufügen, um zusätzliche Clickthrough-Daten zu erfassen, die nicht über den JavaScript-Code erfasst werden.

>[!NOTE]
>
>Der JavaScript-Code ist nur dann eine Lösung für das Klick-Tracking, wenn noch Cookies verfügbar sind. Sobald Cookies eingestellt wurden, ist die Implementierung der folgenden Makros erforderlich.

* **Werbetreibende, deren Websites nicht den [!DNL Analytics for Advertising] JavaScript-Code verwenden und stattdessen [!DNL Analytics] Server-seitige Weiterleitung nur für Clickthrough-Daten verwenden** (ohne Viewthrough-Daten): Die folgenden Makros sind erforderlich, um Klickaktivitäten auf der Site zu melden, die von Anzeigen gesteuert werden, die Sie über Adobe Advertising kaufen.

## Anhängen der Makros an Ihre [!DNL Google Campaign Manager 360] Anzeigen

Fügen Sie in [!DNL Google Campaign Manager 360] für jede Ihrer Anzeige- und Videoanzeigen den folgenden Parameter an die Landingpage-URL an: `%pamo=!;`

Sie haben verschiedene Möglichkeiten, die URL der Landingpage anzugeben. Anweisungen zu den einzelnen Optionen finden Sie in den folgenden Unterabschnitten.

Im Folgenden finden Sie ein Beispiel für die Landingpage-URL, die mit dem Suffix formatiert ist.

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>&#x200B;>* Wenn die Landingpage-URL ein Hash-Symbol (#) enthält, was nicht üblich ist, platzieren Sie den `amo` vor dem Hash-Symbol.
>* Wenn nach dem `amo` Parameter keine anderen Parameter enthalten sind, fügen Sie nach diesem Parameter einen Parameter hinzu (z. B. &quot;&amp;a=b„). Beispiel: `https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### Konfigurieren des URL-Suffix der Landingpage auf Advertiser-Ebene

1. Weitere Informationen finden [ in den Anweisungen zum Öffnen der Advertiser-Eigenschaften](https://support.google.com/campaignmanager/answer/2829344).
1. Fügen Sie in den [!UICONTROL Landing page URL suffix] Einstellungen `%pamo!;` in das Feld [!UICONTROL URL suffix] ein.

### Konfigurieren des URL-Suffix der Landingpage auf Kampagnenebene

1. Weitere Informationen finden [ in den Anweisungen zum Öffnen der Kampagneneigenschaften](https://support.google.com/campaignmanager/answer/2838056#set).
1. Fügen Sie in den [!UICONTROL Landing page URL suffix] Einstellungen `%pamo!;` in das Feld [!UICONTROL URL suffix] ein.

### Konfigurieren des URL-Suffix der Landingpage auf Kreativebene

1. Öffnen Sie die Kreativ-Eigenschaften.
1. Fügen Sie in der [!UICONTROL Click tags]-Einstellung `%pamo!;` in die Spalte [!UICONTROL Landing page] für das Klick-Tag ein.

## Wie [!DNL Analytics for Advertising] Makros in DSP erweitert werden

Wenn Sie in DSP eine Anzeige erstellen, die den [!DNL Analytics for Advertising] (`amo`) enthält, werden die `ef_id`- und `s_kwcid` automatisch an die Klick-URL angehängt. Es empfiehlt sich, das -Tag in DSP zu überprüfen, um sicherzustellen, dass die `ef_id`- und `s_kwcid` vorhanden sind.

Im Folgenden finden Sie ein Beispiel für ein [!DNL Google Campaign Manager 360]-Tag [ins](https://support.google.com/campaignmanager/answer/6080468) wie es in DSP angezeigt wird.

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

[!DNL Google Campaign Manager 360] Wenn ein(e) Benutzende(r) auf die Anzeige klickt, wird `%pamo` im URL-Suffix angezeigt und der Wert des `amo`-Parameters wird dynamisch in die URL eingefügt.

>[!MORELIKETHIS]
>
>* [Überblick über [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising-IDs verwendet von [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](macros-flashtalking.md)
