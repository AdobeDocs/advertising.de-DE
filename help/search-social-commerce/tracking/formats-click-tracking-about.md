---
title: Über Klick-Tracking-URL-Formate für den Adobe Advertising-Konversionsverfolgungs-Service
description: Erfahren Sie mehr über die Klick-Tracking-Formate für unterstützte Werbenetzwerke.
exl-id: b6f225d5-2268-4b2a-9927-063155ba0dc5
feature: Search Tracking
TQID: https://experienceleague.adobe.com/pVSEKmf45CqsfXMbj8HGDltdgV3wUV2UsAzP94vkijg
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 263
ht-degree: 0%

---

# Über Klick-Tracking-URL-Formate für den Adobe Advertising-Konversionsverfolgungs-Service

Die Tracking-Vorlagen, Landingpage-Suffixe (endgültige URL-Suffixe) und Ziel-URLs für Werbekonten und -kampagnen, die den Konversionsverfolgungs-Service von Adobe Advertising verwenden, haben das folgende Format:

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

Dabei gilt:

* `http://pixel.everesttech.net` leitet den Benutzer zu den Adobe Advertising-Pixelservern weiter.

* `<advertiser_ID>` ist eine Variable für die eindeutige Benutzer-ID, die dem Advertiser in Adobe Advertising zugewiesen ist.

* `<token passing parameter>` ist eine Variable für eine der folgenden Aktionen:

   * `cq?` oder `rq` bedeutet, dass die Token-Übergabe aktiviert ist.

   * `c?` oder `r` bedeutet, dass die Token-Übergabe deaktiviert ist.

* `<ad network ID>` ist eine Variable für die numerische ID für das angegebene Werbenetzwerk, z. B. *3* für [!DNL Google Ads], *10* für [!DNL Microsoft Advertising], *45* für [!DNL Meta], *86*, [!DNL Yahoo! Display Network]87 *für*, [!DNL Naver]888 *für*, [!DNL Baidu]90 *, 096*, [!DNL Yandex]105für (veraltet) oder *106*[!DNL Yahoo! Japan Ads] ** [!DNL Yahoo Native] ** [!DNL Pinterest] (veraltet).

* `<tracking ID>` ist eine Variable für eine vom System generierte Tracking-ID-Zeichenfolge, die ein Keyword, eine Anzeige oder eine Platzierung identifiziert, die im Konto eindeutig ist. Die Zeichenfolge variiert je nach Werbenetzwerk.

* `<the landing page>` ist eine Variable, die die URL auf Ihrer Site darstellt, zu der Endbenutzer weitergeleitet werden. Bei Konten mit Ziel-URLs ist dieser Wert eine URL. Bei Konten mit Tracking-Vorlagen ist dieser Wert ein Parameter (z. B. `{lpurl}`), der die endgültige URL darstellt.

Sehen Sie sich die separaten Seiten an, die [[!DNL Baidu] Formate](formats-click-tracking-baidu.md), [[!DNL Google Ads] Formats](formats-click-tracking-google.md), [[!DNL Microsoft Advertising] Formats](formats-click-tracking-microsoft.md), [[!DNL Naver] Formats](formats-click-tracking-naver.md), [[!DNL Yahoo! Display Network] Formats](formats-click-tracking-yahoo-display-network.md), [[!DNL Yahoo! Japan Ads] Formats](formats-click-tracking-yahoo-japan.md) und [[!DNL Yandex] Formats](formats-click-tracking-yandex.md) angeben.

>[!MORELIKETHIS]
>
>* [Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [Klick-Tracking-Formate für [!DNL Google Ads]](formats-click-tracking-google.md)
>* [Klick-Tracking-Formate für [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Naver]](formats-click-tracking-naver.md)
>* [Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Yahoo! Japan Ads]](formats-click-tracking-yahoo-japan.md)
>* [Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)
>* [Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Yandex]](formats-click-tracking-yandex.md)
