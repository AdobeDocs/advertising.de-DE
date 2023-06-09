---
title: Konversions-Tracking mit einem EF ID-Feed
description: Erfahren Sie mehr über die Verwendung eines EF ID-Feeds für Konversions-Tracking-Daten.
source-git-commit: 46e918418bf2e5c412efa8825dda22bc1953e439
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Konversions-Tracking mit einem EF ID-Feed

Bei dieser Methode erfasst Advertising Cloud eine `ef_id` jedes Mal, wenn ein Benutzer klickt und eine Anzeige aufruft und auf die Landingpage gelangt, wird der Werber `ef_id` -Wert mit den Konversionsdaten und sendet sie in einem Daten-Feed.

## Implementierungsübersicht

*Agenturkontoverwalter, [!DNL Adobe] Nur Konto-Manager und Administrator-Benutzerrollen*

1. Verwenden Sie die Konto- oder Kampagnen-Tracking-Optionen &quot;[!UICONTROL EF Redirect],&quot;der Umleitungstyp &quot;[!UICONTROL Token],&quot; und &quot;[!UICONTROL Auto Upload]&quot;, um automatisch eine Ziel-URL oder eine endgültige URL mit einem Adobe Advertising-Token (ef_id) für jeden Suchbegriff (für das Keyword-Level-Tracking) oder jede Anzeige (für das Tracking auf Anzeigenebene) im Konto oder in der Kampagne zu generieren.

   >[!NOTE]
   >* Für diese Methode muss der Advertiser keine Adobe Advertising-Konversions-Tracking-Tags verwenden.
   >* Wenn Sie den Weiterleitungstyp für ein bestehendes Konto oder eine bestehende Kampagne von [!UICONTROL Standard] nach [!UICONTROL Token]oder umgekehrt, müssen Sie alle entsprechenden Tracking-URLs neu generieren.

   Die ef_id wird ausgefüllt und an die Landingpage-URL angehängt, wenn der Endbenutzer auf die Anzeige klickt, und an einen Adobe Advertising-Server umgeleitet. Die ef_id wird dann an den Advertiser in der Ziel-URL oder der endgültigen URL für die Anzeige oder das Keyword übergeben. Im Folgenden finden Sie ein Beispiel für eine Ziel-URL, die beim Umleiten an den Advertiser weitergeleitet wird:

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. Der Advertiser extrahiert die ef_id aus der Weiterleitung und speichert sie mit den relevanten Konversionsdaten, die in die Feed-Datei aufgenommen werden sollen. Ändern Sie die ef_id nicht oder den Groß-/Kleinschreibung.

1. (Optional, jedoch empfohlen) Der Advertiser kann für jede Transaktion eine eindeutige Transaktions-ID erstellen, die in die Feed-Datei aufgenommen werden soll.

1. Der Advertiser lädt eine Datei mit der [erforderliche Konversionsdaten](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) zum angegebenen Serverstandort.

1. Der technische Dienst analysiert die Konversionsdaten in den hochgeladenen Dateien und lädt die Daten dann in den Adobe Advertising hoch. Adobe Advertising verfolgt dann die Daten anhand einzelner Suchbegriffe, Anzeigen und Platzierungen und erstellt eine Umsatzprognostizierung für jede dieser Suchbegriffe.

1. Der technische Dienst validiert die verarbeiteten Daten mit den Feed-Daten und prüft alle [verwaiste Transaktionen](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Dateianforderungen für Konversions-Feed-Dateien](feed-file-requirements.md)
>* [Datenanforderungen für Daten-Feeds mit EF IDs](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)


