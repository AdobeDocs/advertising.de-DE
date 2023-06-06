---
title: Konversions-Tracking mit einem Transaktions-ID-Feed
description: Erfahren Sie mehr über die Verwendung eines Transaktions-ID-Feeds für Konversions-Tracking-Daten.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Konversions-Tracking mit einem Transaktions-ID-Feed

Wenn ein Advertiser sowohl Online- als auch Offline-Transaktionen durchführt, kann Adobe Advertising die Online-Transaktionen über das Adobe Advertising Conversion-Tracking-Pixel verfolgen und der Advertiser kann die Offline-Transaktionen mithilfe einer Transaktions-ID verfolgen und sie über einen Feed bereitstellen:

* Bei Online-Transaktionen verfolgt Adobe Advertising die Klicks auf Ihre Anzeigen und die daraus resultierenden Transaktionen auf Ihrer Website.

* Der Werbetreibende muss Offline-Konversionen verfolgen und Transaktions-Feed-Dateien an Adobe Advertising senden.

## Implementierungsübersicht

*Agenturkontoverwalter, [!DNL Adobe] Nur Konto-Manager und Administrator-Benutzerrollen*

1. Verwenden Sie die Konto- oder Kampagnen-Tracking-Optionen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot;, um automatisch eine Ziel-URL oder endgültige URL für jeden Suchbegriff (für das Tracking auf Suchbegriffebene) oder jede Anzeige (für das Tracking auf Anzeigenebene) im Konto oder in der Kampagne zu generieren.

1. Richten Sie das Adobe Advertising-Konversions-Tracking für die Online-Konversionen ein. Dieser Prozess ist mit dem für Advertiser mit Adobe Advertising pixelbasiertem Konversions-Tracking identisch. Es ist wichtig, Konversions-Tags zu generieren, die einen Parameter für eine eindeutige Transaktions-ID enthalten (`ev_transid=<transid>`).

1. Für den Offline-Teil jeder Transaktion generiert der Advertiser dieselbe Transaktions-ID, die im Online-Teil der Transaktion verwendet wurde, um ihn in die Feed-Datei aufzunehmen.

1. Der Advertiser lädt eine Datei mit der [erforderliche Konversionsdaten](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) zum angegebenen Serverstandort.

1. Der technische Dienst analysiert die Konversionsdaten in den hochgeladenen Dateien und lädt die Daten dann in die Adobe Advertising hoch. Adobe Advertising verfolgt dann die Daten anhand einzelner Suchbegriffe, Anzeigen und Platzierungen und erstellt eine Umsatzprognostizierung für jede dieser Suchbegriffe.

1. Der technische Dienst validiert die verarbeiteten Daten mit den Feed-Daten und prüft alle [verwaiste Transaktionen](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Dateianforderungen für Konversions-Feed-Dateien](feed-file-requirements.md)
>* [Datenanforderungen für Daten-Feeds mit einer Transaktions-ID](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)

