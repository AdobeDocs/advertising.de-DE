---
title: Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Google Campaign Manager 360] Anzeigen-Tags
description: Erfahren Sie, warum und wie Sie [!DNL Analytics for Advertising] Makros für Ihre [!DNL Google Campaign Manager 360] Adtags
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: 703cda43e96dfa9d80bbce2d64192fc461d5dbae
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Google Campaign Manager 360] Anzeigen-Tags

*Werbetreibende, die nur über eine Adobe Advertising-Adobe Analytics-Integration verfügen*

*Gilt nur für DSP*

Wenn Sie Anzeigen-Tags aus [!DNL Google Campaign Manager 360] für Ihre Advertising DSP Anzeigen anhängen [!DNL Analytics for Advertising] Parameter zu Ihren Landingpage-URLs mithilfe der [`%p` macro](https://support.google.com/campaignmanager/table/6096962). Die Parameter zeichnen die AMO-ID (`s_kwcid`) und `ef_id` Abfragezeichenfolgenparameter in der Landingpage-URL, sodass Adobe Advertising Klickdaten für die Anzeigen an Adobe Analytics senden können.

Verwenden Sie Makros für [!DNL Campaign Manager 360] Anzeigen und Videoanzeigen für die folgenden Typen [!DNL Analytics for Advertising] Implementierungen:

* **Werbetreibende mit [!DNL Adobe] [!DNL Analytics for Advertising] Auf ihren Websites implementierter JavaScript-Code**: Der JavaScript-Code zeichnet die AMO-ID (`s_kwcid`) und `ef_id` Abfragezeichenfolgenparameter. Durch die Verwendung von Makros wird das Tracking jedoch auch auf klickbasierte Konversionen erweitert, wenn Drittanbieter-Cookies nicht unterstützt werden. Es empfiehlt sich, die Makros in den folgenden Abschnitten zu Ihren Anzeigen-Tags hinzuzufügen, um zusätzliche Clickthrough-Daten zu erfassen, die nicht über den JavaScript-Code erfasst werden.

>[!NOTE]
>
>Der JavaScript-Code ist eine Lösung für Klick-Tracking, während Cookies weiterhin verfügbar sind. Sobald Cookies beendet sind, ist die Implementierung der folgenden Makros erforderlich.

* **Advertiser, deren Websites die [!DNL Analytics for Advertising] JavaScript-Code und stattdessen auf [!DNL Analytics] Serverseitige Weiterleitung nur für Clickthrough-Daten** (ohne Durchsichtsdaten): Die folgenden Makros sind erforderlich, um die Klick-Aktivität auf der Site zu melden, die von Anzeigen gesteuert wird, die Sie über den Adobe Advertising kaufen.

## Hängen Sie die Makros an Ihre [!DNL Google Campaign Manager 360] Anzeigen

Within [!DNL Google Campaign Manager 360], hängen Sie den folgenden Parameter an die URL der Landingpage für jede Ihrer Anzeigen und Videoanzeigen an: `%pamo=!;`

Sie können die URL der Landingpage auf verschiedene Weise angeben. Anweisungen zu den einzelnen Optionen finden Sie in den folgenden Unterabschnitten.

Im Folgenden finden Sie ein Beispiel für die Landingpage-URL, die mit dem Suffix formatiert wurde.

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>>* Wenn die URL der Landingpage ein nicht übliches Hash-Symbol (#) enthält, platzieren Sie die `amo` -Parameter vor dem Hash-Symbol.
>* Wenn keine anderen Parameter nach der `amo` , und fügen Sie danach einen Parameter hinzu (z. B. &amp;a=b). Beispiel:`https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### Konfigurieren des Advertiser-Level-URL-Suffixes der Landingpage

1. Siehe [Anweisungen zum Öffnen der Advertiser-Eigenschaften](https://support.google.com/campaignmanager/answer/2829344).
1. Im [!UICONTROL Landing page URL suffix] Einstellungen, einschließen `%pamo!;` im [!UICONTROL URL suffix] -Feld.

### URL-Suffix auf Kampagnenebene konfigurieren

1. Siehe [Anweisungen zum Öffnen der Kampagneneigenschaften](https://support.google.com/campaignmanager/answer/2838056#set).
1. Im [!UICONTROL Landing page URL suffix] Einstellungen, einschließen `%pamo!;` im [!UICONTROL URL suffix] -Feld.

### Konfigurieren des URL-Suffixes der kreativen Einstiegsseite

1. Öffnen Sie die kreativen Eigenschaften.
1. Im [!UICONTROL Click tags] Einstellung, einschließen `%pamo!;` im [!UICONTROL Landing page] Spalte für das Klick-Tag.

## How [!DNL Analytics for Advertising] Makros werden in DSP

DSP, wenn Sie eine Anzeige erstellen, die die [!DNL Analytics for Advertising] Parameter (`amo`), die `ef_id` und `s_kwcid` -Makros werden automatisch an die Klick-URL angehängt. Es empfiehlt sich, das Tag in DSP zu überprüfen, um sicherzustellen, dass die Variable `ef_id` und `s_kwcid` Makros sind vorhanden.

Im Folgenden finden Sie ein Beispiel für eine [!DNL Google Campaign Manager 360] [ins-Tag](https://support.google.com/campaignmanager/answer/6080468) wie in DSP angezeigt.

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

Wenn ein Benutzer auf die Anzeige klickt, [!DNL Google Campaign Manager 360] seen `%pamo` im URL-Suffix und fügt den Wert der `amo` in die URL ein.

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising]](overview.md)
>* [Von verwendete Adobe Advertising-IDs [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Flashtalking] Anzeigen-Tags](macros-flashtalking.md)
