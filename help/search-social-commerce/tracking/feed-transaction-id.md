---
title: Konversionsverfolgung mit einem Transaktions-ID-Feed
description: Erfahren Sie mehr über die Verwendung eines Transaktions-ID-Feeds für Konversions-Tracking-Daten.
exl-id: 3341ac20-d435-4387-99da-7b874e53c2e7
feature: Search Tracking
TQID: https://experienceleague.adobe.com/wGlR5tUF7ajbnQLUnW0c-U84BskLzr63Wet-e-x823M
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 293
ht-degree: 0%

---

# Konversionsverfolgung mit einem Transaktions-ID-Feed

Wenn ein Advertiser sowohl Online- als auch Offline-Transaktionen hat, kann Adobe Advertising die Online-Transaktionen über das Adobe Advertising-Konversionsverfolgungspixel verfolgen, und der Advertiser kann die Offline-Transaktionen mithilfe einer Transaktions-ID verfolgen und über einen Feed bereitstellen:

* Bei Online-Transaktionen verfolgt Adobe Advertising die Klicks auf Ihre Anzeigen und die resultierenden Transaktionen auf Ihrer Website.

* Der Werbetreibende muss Offline-Konversionen verfolgen und Feed-Dateien auf Transaktionsebene an Adobe Advertising senden.

## Implementierungsübersicht

*Nur Agenturkonto-Manager, [!DNL Adobe]-Account-Manager und Admin-Benutzerrollen*

1. Verwenden Sie die Tracking-Optionen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; für Konten oder Kampagnen, um automatisch eine Ziel-URL oder endgültige URL für jedes Keyword (für das Tracking auf Keyword-Ebene) oder jede Anzeige (für das Tracking auf Anzeigenebene) im Konto oder in der Kampagne zu generieren.

1. Einrichten des Adobe Advertising-Konversions-Trackings für die Online-Konversionen. Dieser Prozess ist der gleiche wie für Werbetreibende mit Adobe Advertising-pixelbasiertem Konversions-Tracking. Es ist wichtig, Konversions-Tags zu generieren, die einen Parameter für eine eindeutige Transaktions-ID (`ev_transid=<transid>`) enthalten.

1. Für den Offline-Teil jeder Transaktion generiert der Advertiser dieselbe Transaktions-ID, die im Online-Teil der Transaktion verwendet wurde, um sie in die Feed-Datei aufzunehmen.

1. Der Werbetreibende lädt eine Datei mit den [erforderlichen Konvertierungsdaten](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) auf den angegebenen Serverspeicherort hoch.

1. Der technische Dienst analysiert die Konversionsdaten in den hochgeladenen Dateien und lädt die Daten dann in Adobe Advertising hoch. Adobe Advertising vergleicht die Daten dann mit einzelnen Keywords, Anzeigen und Platzierungen und erstellt für jedes Element eine Umsatzprognose.

1. Technical Services validiert die verarbeiteten Daten anhand der Feed-Daten und prüft auf „verwaiste [&quot; ](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Dateianforderungen für Konversions-Feed-Dateien](feed-file-requirements.md)
>* [Datenanforderungen für Daten-Feeds mit einer Transaktions-ID](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
