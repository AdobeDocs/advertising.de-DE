---
title: Konversionsverfolgung mit einem EF-ID-Feed
description: Erfahren Sie mehr über die Verwendung eines EF ID-Feeds für Konversions-Tracking-Daten.
exl-id: fd065313-3d27-4bb9-a934-e815e02cf405
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Konversionsverfolgung mit einem EF-ID-Feed

Bei dieser Methode erfasst Advertising Cloud jedes Mal, wenn ein(e) Benutzende(r) auf die Landingpage klickt und eine Anzeige anzeigt, einen `ef_id` Wert, und der Advertiser speichert den `ef_id` Wert mit den Konversionsdaten und sendet ihn in einem Daten-Feed.

## Implementierungsübersicht

*Nur Agenturkonto-Manager, [!DNL Adobe]-Account-Manager und Admin-Benutzerrollen*

1. Verwenden Sie die Konto- oder Kampagnen-Tracking-Optionen &quot;[!UICONTROL EF Redirect]&quot;, den Umleitungstyp &quot;[!UICONTROL Token]&quot; und &quot;[!UICONTROL Auto Upload]&quot;, um automatisch eine Ziel-URL oder eine endgültige URL mit einem Adobe Advertising-Token (ef_id) für jedes Keyword (für Keyword-Tracking auf Ebene) oder jede Anzeige (für Tracking auf Anzeigenebene) im Konto oder in der Kampagne zu generieren.

   >[!NOTE]
   >* Bei dieser Methode muss der Advertiser keine Adobe Advertising-Konversionsverfolgungstags verwenden.
   >* Wenn Sie den Umleitungstyp für ein vorhandenes Konto oder eine vorhandene Kampagne von [!UICONTROL Standard] in [!UICONTROL Token] oder umgekehrt wechseln, müssen Sie alle entsprechenden Tracking-URLs neu generieren.

   Die ef_id wird ausgefüllt und an die Landingpage-URL angehängt, wenn der Endbenutzer auf die Anzeige klickt und zu einem Adobe Advertising-Server weitergeleitet wird. Die ef_id wird dann in der Ziel-URL oder der endgültigen URL für die Anzeige oder das Keyword an den Advertiser übergeben. Im Folgenden finden Sie ein Beispiel für eine Ziel-URL, die während der Umleitung an den Advertiser übergeben wird:

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. Der Advertiser extrahiert die ef_id aus der Umleitung und speichert sie mit den relevanten Konversionsdaten, die in die Feed-Datei aufgenommen werden sollen. Ändern Sie weder die ef_id noch ändern Sie die Groß-/Kleinschreibung.

1. (Optional, aber empfohlen) Der Advertiser kann für jede Transaktion, die in die Feed-Datei aufgenommen werden soll, eine eindeutige Transaktions-ID erstellen.

1. Der Werbetreibende lädt eine Datei mit den [erforderlichen Konvertierungsdaten](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) auf den angegebenen Serverspeicherort hoch.

1. Der technische Dienst analysiert die Konvertierungsdaten in den hochgeladenen Dateien und lädt die Daten dann auf die Adobe Advertising hoch. Adobe Advertising verfolgt die Daten dann anhand einzelner Keywords, Anzeigen und Platzierungen und erstellt für jedes Element eine Umsatzprognose.

1. Technical Services validiert die verarbeiteten Daten anhand der Feed-Daten und prüft auf „verwaiste [&quot; &#x200B;](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Dateianforderungen für Konversions-Feed-Dateien](feed-file-requirements.md)
>* [Datenanforderungen für Daten-Feeds mit EF-IDs](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
