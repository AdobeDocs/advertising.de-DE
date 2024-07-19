---
title: Konversions-Tracking mit einem Transaktions-ID-Feed
description: Erfahren Sie mehr über die Verwendung eines Transaktions-ID-Feeds für Konversions-Tracking-Daten.
exl-id: 3341ac20-d435-4387-99da-7b874e53c2e7
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Konversions-Tracking mit einem Transaktions-ID-Feed

Wenn ein Advertiser sowohl Online- als auch Offline-Transaktionen durchführt, kann Adobe Advertising die Online-Transaktionen über das Adobe Advertising-Konversions-Tracking-Pixel verfolgen und der Advertiser kann die Offline-Transaktionen mithilfe einer Transaktions-ID verfolgen und über einen Feed bereitstellen:

* Für die Online-Transaktionen verfolgt Adobe Advertising die Klicks auf Ihre Anzeigen und die daraus resultierenden Transaktionen auf Ihrer Website.

* Der Werbetreibende muss Offline-Konversionen verfolgen und Transaktions-Feed-Dateien an Adobe Advertising senden.

## Implementierungsübersicht

*Nur Agentur-Kundenbetreuer, [!DNL Adobe] -Kundenbetreuer und Administrator-Benutzerrollen*

1. Verwenden Sie die Konto- oder Kampagnen-Tracking-Optionen &quot;[!UICONTROL EF Redirect]&quot;und &quot;[!UICONTROL Auto Upload]&quot;, um automatisch eine Ziel-URL oder eine endgültige URL für jeden Suchbegriff (für das Keyword-Level-Tracking) oder jede Anzeige (für das Tracking auf Anzeigenebene) im Konto oder in der Kampagne zu generieren.

1. Richten Sie das Adobe Advertising-Konversions-Tracking für die Online-Konversionen ein. Dieser Prozess ist mit dem für Advertiser mit Adobe Advertising-pixelbasiertem Konversions-Tracking identisch. Es ist wichtig, Konversions-Tags zu generieren, die einen Parameter für eine eindeutige Transaktions-ID (`ev_transid=<transid>`) enthalten.

1. Für den Offline-Teil jeder Transaktion generiert der Advertiser dieselbe Transaktions-ID, die im Online-Teil der Transaktion verwendet wurde, um ihn in die Feed-Datei aufzunehmen.

1. Der Advertiser lädt eine Datei mit den [erforderlichen Konversionsdaten](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) an den angegebenen Server-Speicherort hoch.

1. Der technische Dienst analysiert die Konversionsdaten in den hochgeladenen Dateien und lädt die Daten dann in Adobe Advertising hoch. Adobe Advertising verfolgt dann die Daten anhand einzelner Suchbegriffe, Anzeigen und Platzierungen und erstellt eine Umsatzprognostizierung für jeden einzelnen.

1. Der technische Dienst validiert die verarbeiteten Daten mit den Feed-Daten und prüft, ob [verwaiste Transaktionen](/help/search-social-commerce/glossary.md#o-p) vorliegen.

>[!MORELIKETHIS]
>
>* [Dateianforderungen für Konversions-Feed-Dateien](feed-file-requirements.md)
>* [Datenanforderungen für Daten-Feeds mit einer Transaktions-ID](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
