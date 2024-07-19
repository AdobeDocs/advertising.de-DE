---
title: Anhängen von [!DNL Analytics for Advertising] Makros an  [!DNL Google Campaign Manager 360] Anzeigen-Tags
description: Erfahren Sie, warum und wie Sie [!DNL Analytics for Advertising] Makros zu Ihren [!DNL Google Campaign Manager 360] Anzeigen-Tags hinzufügen
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: aa41ba08ba83bfacbc2541c0f0d90336b3c36305
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Anhängen von [!DNL Analytics for Advertising] Makros an [!DNL Google Campaign Manager 360] Anzeigen-Tags

*Advertiser mit nur einer Adobe Advertising-Adobe Analytics-Integration*

*Nur für Advertising DSP anwendbar*

Wenn Sie Anzeigen-Tags aus [!DNL Google Campaign Manager 360] für Ihre Advertising DSP-Anzeigen verwenden, hängen Sie [!DNL Analytics for Advertising] -Parameter mithilfe des Makros [`%p` an die URLs der Landingpage an. ](https://support.google.com/campaignmanager/table/6096962) In den Parametern werden AMO-ID-Parameter (`s_kwcid`) und `ef_id` Abfragezeichenfolgenparameter in der URL der Landingpage aufgezeichnet, sodass Adobe Advertising Klick-Daten für die Anzeigen an Adobe Analytics senden kann.

Verwenden Sie Makros für [!DNL Campaign Manager 360] Display- und Videoanzeigen für die folgenden Typen von [!DNL Analytics for Advertising] -Implementierungen:

* **Advertiser mit dem auf ihren Websites implementierten JavaScript-Code [!DNL Adobe] [!DNL Analytics for Advertising]**: Der JavaScript-Code zeichnet bereits die Abfragezeichenfolgenparameter AMO ID (`s_kwcid`) und `ef_id` auf. Durch die Verwendung von Makros wird das Tracking jedoch auch auf klickbasierte Konversionen erweitert, wenn Drittanbieter-Cookies nicht unterstützt werden. Es empfiehlt sich, die Makros in den folgenden Abschnitten zu Ihren Anzeigen-Tags hinzuzufügen, um zusätzliche Clickthrough-Daten zu erfassen, die nicht über den JavaScript-Code erfasst werden.

>[!NOTE]
>
>Der JavaScript-Code ist eine Lösung für Klick-Tracking, solange Cookies noch verfügbar sind. Sobald Cookies beendet sind, ist die Implementierung der folgenden Makros erforderlich.

* **Werbetreibende, deren Websites nicht den JavaScript-Code von [!DNL Analytics for Advertising] verwenden und stattdessen die serverseitige Weiterleitung nur für Clickthrough-Daten verwenden** (ohne Viewthrough-Daten): Die folgenden Makros sind erforderlich, um die Klick-Aktivität auf der Site über Anzeigen zu melden, die Sie über Adobe Advertising kaufen.[!DNL Analytics]

## Anhängen der Makros an Ihre [!DNL Google Campaign Manager 360]-Anzeigen

Hängen Sie innerhalb von [!DNL Google Campaign Manager 360] den folgenden Parameter an die URL der Landingpage für jede Ihrer Anzeigen und Videoanzeigen an: `%pamo=!;`

Sie können die URL der Landingpage auf verschiedene Weise angeben. Anweisungen zu den einzelnen Optionen finden Sie in den folgenden Unterabschnitten.

Im Folgenden finden Sie ein Beispiel für die Landingpage-URL, die mit dem Suffix formatiert wurde.

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>>* Wenn die URL der Landingpage ein nicht übliches Hash-Symbol (#) enthält, platzieren Sie den Parameter `amo` vor dem Hash-Symbol.
>* Wenn nach dem Parameter `amo` keine anderen Parameter enthalten sind, fügen Sie einen Parameter hinzu (z. B. &amp;a=b). Beispiel: `https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### Konfigurieren des Advertiser-Level-URL-Suffixes der Landingpage

1. Siehe die [Anweisungen zum Öffnen der Eigenschaften des Advertisers](https://support.google.com/campaignmanager/answer/2829344).
1. Schließen Sie in den Einstellungen für [!UICONTROL Landing page URL suffix] `%pamo!;` in das Feld [!UICONTROL URL suffix] ein.

### URL-Suffix auf Kampagnenebene konfigurieren

1. Siehe die [Anweisungen zum Öffnen der Kampagneneigenschaften](https://support.google.com/campaignmanager/answer/2838056#set).
1. Schließen Sie in den Einstellungen für [!UICONTROL Landing page URL suffix] `%pamo!;` in das Feld [!UICONTROL URL suffix] ein.

### Konfigurieren des URL-Suffixes der kreativen Einstiegsseite

1. Öffnen Sie die kreativen Eigenschaften.
1. Schließen Sie in der Einstellung [!UICONTROL Click tags] `%pamo!;` in die Spalte [!UICONTROL Landing page] für das Klick-Tag ein.

## Erweitern von [!DNL Analytics for Advertising] Makros in DSP

Wenn Sie DSP eine Anzeige erstellen, die den Parameter [!DNL Analytics for Advertising] (`amo`) enthält, werden die Makros `ef_id` und `s_kwcid` automatisch an die Klick-URL angehängt. Es empfiehlt sich, das Tag in DSP zu überprüfen, um sicherzustellen, dass die Makros `ef_id` und `s_kwcid` vorhanden sind.

Im Folgenden finden Sie ein Beispiel für ein [!DNL Google Campaign Manager 360] [in-Tag](https://support.google.com/campaignmanager/answer/6080468) , wie es in DSP angezeigt wird.

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

Wenn ein Benutzer auf die Anzeige klickt, sieht [!DNL Google Campaign Manager 360] im URL-Suffix `%pamo` und fügt den Wert des Parameters `amo` dynamisch in die URL ein.

>[!MORELIKETHIS]
>
>* [Überblick über  [!DNL Analytics for Advertising]](overview.md)
>* [Von  [!DNL Analytics]](/help/integrations/analytics/ids.md) verwendete Adobe Advertising-IDs
>* [Anhängen von [!DNL Analytics for Advertising] Makros an  [!DNL Flashtalking] Anzeigen-Tags](macros-flashtalking.md)
