---
title: Über Klick-Tracking-URL-Formate für den Adobe Advertising-Konversions-Tracking-Dienst
description: Erfahren Sie mehr über die Klick-Tracking-Formate für unterstützte Werbenetzwerke.
exl-id: b6f225d5-2268-4b2a-9927-063155ba0dc5
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Über Klick-Tracking-URL-Formate für den Adobe Advertising-Konversions-Tracking-Dienst

Tracking-Vorlagen, Landingpage-Suffixe (endgültige URL-Suffixe) und Ziel-URLs für Anzeigenkonten und Kampagnen, die den Adobe Advertising-Konversions-Tracking-Dienst verwenden, haben das folgende Format:

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

wobei:

* `http://pixel.everesttech.net` leitet den Benutzer zu den Adobe Advertising-Pixelservern um.

* `<advertiser_ID>` ist eine Variable für die eindeutige Benutzer-ID, die dem Advertiser innerhalb von Adobe Advertising zugewiesen wird.

* `<token passing parameter>` ist eine Variable für eine der folgenden Optionen:

   * `cq?` oder `rq` gibt an, dass die Übergabe des Tokens aktiviert ist.

   * `c?` oder `r` bedeutet, dass die Übergabe des Tokens deaktiviert ist.

* `<ad network ID>` ist eine Variable für die numerische ID für das angegebene Anzeigennetzwerk, z. B. *3* für [!DNL Google Ads], *10* für [!DNL Microsoft Advertising], *45* für [!DNL Meta], *86* für [!DNL Yahoo! Display Network], *87* für [!DNL Naver]. 16}88 *für [!DNL Baidu],* 90 *für [!DNL Yandex],* 94 *für [!DNL Yahoo! Japan Ads],* 105 *für [!DNL Yahoo Native] (nicht mehr unterstützt) oder* 106{2 9} für [!DNL Pinterest] (veraltet).**

* `<tracking ID>` ist eine Variable für eine vom System generierte Tracking-ID-Zeichenfolge, die einen Suchbegriff, eine Anzeige oder eine Platzierung identifiziert, der/die im Konto eindeutig ist. Die Zeichenfolge variiert je nach Anzeigennetzwerk.

* `<the landing page>` ist eine Variable, die die URL auf Ihrer Site darstellt, zu der Endbenutzer weitergeleitet werden. Bei Konten mit Ziel-URLs ist dieser Wert eine URL. Bei Konten mit Tracking-Vorlagen ist dieser Wert ein Parameter (z. B. `{lpurl}`), der die endgültige URL darstellt.

Die separaten Seiten mit den Formaten [[!DNL Baidu] ](formats-click-tracking-baidu.md), [[!DNL Google Ads] formats](formats-click-tracking-google.md), [[!DNL Microsoft Advertising] formats](formats-click-tracking-microsoft.md), [[!DNL Naver] formats](formats-click-tracking-naver.md), [[!DNL Yahoo! Display Network] formats](formats-click-tracking-yahoo-display-network.md), [[!DNL Yahoo! Japan Ads] formats](formats-click-tracking-yahoo-japan.md) und [[!DNL Yandex] formats](formats-click-tracking-yandex.md) werden angezeigt.

>[!MORELIKETHIS]
>
>* [Klick-Tracking-Formate für gesponserte Anzeigen auf  [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [Klick-Tracking-Formate für  [!DNL Google Ads]](formats-click-tracking-google.md)
>* [Klick-Tracking-Formate für  [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [Klick-Tracking-Formate für gesponserte Anzeigen auf  [!DNL Naver]](formats-click-tracking-naver.md)
>* [Klick-Tracking-Formate für gesponserte Anzeigen auf  [!DNL Yahoo! Japan Ads]](formats-click-tracking-yahoo-japan.md)
>* [Klick-Tracking-Formate für gesponserte Anzeigen auf  [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)
>* [Klick-Tracking-Formate für gesponserte Anzeigen auf  [!DNL Yandex]](formats-click-tracking-yandex.md)
