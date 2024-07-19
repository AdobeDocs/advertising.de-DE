---
title: Konversions-Tracking mit einem EF ID-Feed
description: Erfahren Sie mehr über die Verwendung eines EF ID-Feeds für Konversions-Tracking-Daten.
exl-id: fd065313-3d27-4bb9-a934-e815e02cf405
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Konversions-Tracking mit einem EF ID-Feed

Bei dieser Methode erfasst Advertising Cloud jedes Mal, wenn ein Benutzer klickt und eine Anzeige aufruft und auf die Landingpage gelangt, einen `ef_id` -Wert. Der Werbetreibende speichert den `ef_id` -Wert mit den Konversionsdaten und sendet ihn in einem Daten-Feed.

## Implementierungsübersicht

*Nur Agentur-Kundenbetreuer, [!DNL Adobe] -Kundenbetreuer und Administrator-Benutzerrollen*

1. Verwenden Sie die Konto- oder Kampagnen-Tracking-Optionen &quot;[!UICONTROL EF Redirect]&quot;, den Umleitungstyp &quot;[!UICONTROL Token]&quot;und &quot;[!UICONTROL Auto Upload]&quot;, um automatisch eine Ziel-URL oder eine endgültige URL mit einem Adobe Advertising-Token (ef_id) für jeden Suchbegriff (für Tracking auf Suchbegriffebene) oder jede Anzeige (für Tracking auf Anzeigenebene) im Konto oder in der Kampagne zu generieren.

   >[!NOTE]
   >* Für diese Methode muss der Advertiser keine Adobe Advertising-Konversions-Tracking-Tags verwenden.
   >* Wenn Sie den Weiterleitungstyp für ein vorhandenes Konto oder eine bestehende Kampagne von [!UICONTROL Standard] auf [!UICONTROL Token] umschalten oder umgekehrt, müssen Sie alle entsprechenden Tracking-URLs neu generieren.

   Die ef_id wird ausgefüllt und an die Landingpage-URL angehängt, wenn der Endbenutzer auf die Anzeige klickt, und an einen Adobe Advertising-Server umgeleitet. Die ef_id wird dann an den Advertiser in der Ziel-URL oder der endgültigen URL für die Anzeige oder das Keyword übergeben. Im Folgenden finden Sie ein Beispiel für eine Ziel-URL, die beim Umleiten an den Advertiser weitergeleitet wird:

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. Der Advertiser extrahiert die ef_id aus der Weiterleitung und speichert sie mit den relevanten Konversionsdaten, die in die Feed-Datei aufgenommen werden sollen. Ändern Sie die ef_id nicht oder den Groß-/Kleinschreibung.

1. (Optional, jedoch empfohlen) Der Advertiser kann für jede Transaktion eine eindeutige Transaktions-ID erstellen, die in die Feed-Datei aufgenommen werden soll.

1. Der Advertiser lädt eine Datei mit den [erforderlichen Konversionsdaten](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) an den angegebenen Server-Speicherort hoch.

1. Der technische Dienst analysiert die Konversionsdaten in den hochgeladenen Dateien und lädt die Daten dann in Adobe Advertising hoch. Adobe Advertising verfolgt dann die Daten anhand einzelner Suchbegriffe, Anzeigen und Platzierungen und erstellt eine Umsatzprognostizierung für jeden einzelnen.

1. Der technische Dienst validiert die verarbeiteten Daten mit den Feed-Daten und prüft, ob [verwaiste Transaktionen](/help/search-social-commerce/glossary.md#o-p) vorliegen.

>[!MORELIKETHIS]
>
>* [Dateianforderungen für Konversions-Feed-Dateien](feed-file-requirements.md)
>* [Datenanforderungen für Daten-Feeds mit EF IDs](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
