---
title: Über Klick-Tracking-URL-Formate für den Adobe Advertising-Konversions-Tracking-Dienst
description: Erfahren Sie mehr über die Klick-Tracking-Formate für unterstützte Werbenetzwerke.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# Über Klick-Tracking-URL-Formate für den Adobe Advertising-Konversions-Tracking-Dienst

Tracking-Vorlagen, Landingpage-Suffixe (endgültige URL-Suffixe) und Ziel-URLs für Anzeigenkonten und Kampagnen, die den Adobe Advertising Conversion-Tracking-Dienst verwenden, haben das folgende Format:

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

wobei:

* `http://pixel.everesttech.net` leitet den Benutzer zu den Adobe Advertising-Pixelservern weiter.

* `<advertiser_ID>` ist eine Variable für die eindeutige Benutzer-ID, die dem Advertiser in Adobe Advertising zugewiesen wird.

* `<token passing parameter>` ist eine Variable für eine der folgenden Optionen:

   * `cq?` oder `rq` gibt an, dass die Übergabe des Tokens aktiviert ist.

   * `c?` oder `r` gibt an, dass die Übergabe des Tokens deaktiviert ist.

* `<ad network ID>` ist eine Variable für die numerische ID für das angegebene Anzeigennetzwerk, z. B. *3* für [!DNL Google Ads], *10* für [!DNL Microsoft Advertising], *45* für [!DNL Meta], *86* für [!DNL Yahoo! Display Network], *87* für [!DNL Naver], *88* für [!DNL Baidu], *90* für [!DNL Yandex], *94* für [!DNL Yahoo! Japan Ads], *105* für [!DNL Yahoo Native] (veraltet) oder *106* für [!DNL Pinterest] (nicht mehr unterstützt).

* `<tracking ID>` ist eine Variable für eine vom System generierte Tracking-ID-Zeichenfolge, die einen Suchbegriff, eine Anzeige oder eine Platzierung identifiziert, der/die im Konto eindeutig ist. Die Zeichenfolge variiert je nach Anzeigennetzwerk.

* `<the landing page>` ist eine Variable, die die URL auf Ihrer Site darstellt, zu der Endbenutzer weitergeleitet werden. Bei Konten mit Ziel-URLs ist dieser Wert eine URL. Bei Konten mit Tracking-Vorlagen ist dieser Wert ein Parameter (z. B. `{lpurl}`), die die endgültige URL darstellt.

Siehe die separaten Seiten, die die [[!DNL Baidu] Formate](formats-click-tracking-baidu.md), [[!DNL Google Ads] Formate](formats-click-tracking-google.md), [[!DNL Microsoft Advertising] Formate](formats-click-tracking-microsoft.md), [[!DNL Naver] Formate](formats-click-tracking-naver.md), [[!DNL Yahoo! Display Network] Formate](formats-click-tracking-yahoo-display-network.md), [[!DNL Yahoo! Japan Ads] Formate](formats-click-tracking-yahoo-japan.md)und [[!DNL Yandex] Formate](formats-click-tracking-yandex.md).

>[!MORELIKETHIS]
>
>* [Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [Klick-Tracking-Formate für [!DNL Google Ads]](formats-click-tracking-google.md)
>* [Klick-Tracking-Formate für [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Naver]](formats-click-tracking-naver.md)
>* [Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Yahoo! Japan Ads]](formats-click-tracking-yahoo-japan.md)
>* [Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)
>* [Klick-Tracking-Formate für gesponserte Anzeigen auf [!DNL Yandex]](formats-click-tracking-yandex.md)

