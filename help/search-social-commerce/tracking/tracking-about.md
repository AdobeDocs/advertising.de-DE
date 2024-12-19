---
title: Über das Tracking für Search, Social und Commerce
description: Erfahren Sie mehr über Tracking-Optionen für Search, Social und Commerce.
exl-id: f0fd367a-dd5a-46ec-a3d6-9b491860aae8
feature: Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Über das Tracking für Search, Social und Commerce

Um die Performance Ihrer Anzeigen zu verfolgen, benötigen Search, Social und Commerce Impression-, Klick-, Kosten- und Konversions(Transaktions)daten für Ihre Anzeigen. Search, Social und Commerce verwenden diese Daten, um die Datenprognosemodelle zu erstellen, die zur Optimierung Ihrer Werbeportfolios erforderlich sind.

## Kosten-, Klick- und Impressionsdaten

Search, Social und Commerce ruft Impressions-, Klick- und Kostendaten täglich direkt aus [unterstützten Werbenetzwerken](/help/search-social-commerce/introduction/supported-inventory.md) ab. Darüber hinaus können Search, Social und Commerce einen eindeutigen Klick-Tracking-Code (einschließlich einer Umleitung zu einem Tracking-Server) in Ihren Tracking-Vorlagen und Ziel-URLs hinzufügen, um Anzeige-/Inhalts-Impressionen, Klicks und Kosten zu verfolgen und die Ereignisse später mit Konversionen zu verknüpfen.

Wenn Sie Kampagnen in Werbenetzwerken verfolgen möchten, mit denen Search, Social und Commerce keine Daten synchronisiert, müssen Sie Daten für diese Kampagnen bereitstellen, indem Sie eine tägliche Feed-Datei mit den Impressions-, Klick- und Kostendaten senden.

### Klick-Tracking-Tags

Ihr Implementierungs-Team für Search, Social und Commerce richtet Klick-Tracking ein, indem es die Tracking-Vorlagen und Ziel-URLs für Anzeigen, Keywords, Platzierungen, Produktgruppen und Sitelink-Erweiterungen in Ihren synchronisierten Anzeigenkampagnen aktualisiert, um eine eindeutige Tracking-ID-Zeichenfolge und eine Adobe Advertising-Umleitung einzuschließen. Sie fügen außerdem Tracking zu den Suffixen der Landingpage (endgültigen URL-Suffixen) für Ihre [!DNL Google Ads] und [!DNL Microsoft Advertising] Konten und Kampagnen hinzu.

Mit den Tracking-Parametern kann Adobe Advertising Klicks auf Ebene einzelner Keywords (Suchkampagnen) oder Anzeigenvarianten (Suchkampagnen mit Inhalts- oder Site-Targeting, Anzeigekampagnen und Social-Media-Kampagnen) verfolgen. Jedes Mal, wenn ein(e) Benutzende(r) eine Display-/Content-Anzeige anzeigt oder auf eine Ihrer Anzeigen klickt, sendet das Anzeigennetzwerk das Ereignis mithilfe eines Klick-Tracking-Tags, das mit dem Keyword oder der Anzeige verknüpft ist, an die Adobe Advertising-Pixel-Server. Für Klicks:

* Für [!DNL Google Ads] und [!DNL Microsoft Advertising] Anzeigen auf Browsern, die paralleles Tracking unterstützen, sendet das Anzeigennetzwerk den Klick zuerst an Ihre Website und dann an die Adobe Advertising-Pixelserver, die dann ein Cookie auf dem Computer des Nutzers platzieren, falls noch keines vorhanden ist.

* In allen anderen Fällen sendet das Anzeigennetzwerk den Klick direkt an die Adobe Advertising-Pixelserver. Der Pixel-Server platziert ein Cookie auf dem Computer des Benutzers (sofern noch nicht vorhanden) und leitet den Benutzer dann an die entsprechende URL auf Ihrer Website weiter. Das Gesamterlebnis für den Endbenutzer ist dasselbe wie ohne eine Umleitung.

Das Cookie wird in der [!DNL Adobe] Domain (`everesttech.net`) als Erstanbieter-Cookie gesetzt. Nach einer Umleitung befindet sich der Benutzer in der Domain des Werbetreibenden, und das Cookie wird dann als Drittanbieter-Cookie behandelt. Weitere Informationen zum Adobe Advertising von Cookies finden Sie unter &quot;[Adobe Advertising-Cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html)&quot;.

## Konvertierungsdaten

Wenn ein Kunde auf eine Anzeige klickt oder sich eine Anzeige oder eine Social-Media-Anzeige ansieht, muss Search, Social und Commerce jede resultierende Konversion wieder dem ursprünglichen Klick oder der Display-/Social-Impression zuordnen.

Der Advertiser spielt eine Rolle bei der Bereitstellung der Konversionsdaten für alle Klicks und Display-/Social-Impressions. Konversionsdaten können Informationen über alle Arten von Ereignissen enthalten, die auf einer Website auftreten und die zur Angebotsoptimierung verwendet werden können. Sie können Konversionsdaten bereitstellen, indem Sie Konversionsverfolgungs-Code in die Konversionsseiten des Advertisers implementieren (z. B. auf der Seite „Erfolg“, die angezeigt wird, nachdem ein Kunde eine Transaktion abgeschlossen hat) oder indem Sie eine tägliche Feed-Datei mit Konversionsdaten senden, die von einer anderen Methode erfasst wurden.

### Conversion-Tracking-Tags

Sie können [Konversions-Tags von verschiedenen Anbietern) ](/help/search-social-commerce/tracking/conversion-tracking-about.md).

Wenn Sie ein Adobe Advertising-Konvertierungs-Tag verwenden und ein Benutzer eine erfolgreiche Transaktion abschließt und auf einer „Erfolgsseite“ landet, prüft der Adobe Advertising-Pixelserver, ob das Cookie auf dem Computer des Benutzers vorhanden ist, das zum Zeitpunkt der Klickumleitung gesetzt wurde. Wenn ein Cookie gefunden wird, werden Informationen über das Transaktionsereignis mit dem Parameter ef_transid übergeben, und die Transaktion wird als Konversion erkannt und dem vorangehenden Anzeigenklick- oder Anzeigeabdruck gutgeschrieben.

Wenn der Nutzer auf mehr als eine Ihrer Anzeigen geklickt hat, schreibt Adobe Advertising die Transaktion dem endgültigen Anzeigenklick oder (bei Anzeige- oder Videokampagnen) dem endgültigen Anzeigenabdruck zu, sofern nicht anders angegeben. Ihr [Klick-Lookback](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j) bestimmen die Anzahl der Tage nach einem gebührenpflichtigen Klick bzw. einer Anzeige-/Video-Impression, in denen das Ereignis einer Konversion zugeordnet werden kann.

Das Adobe Advertising-Implementierungs-Team arbeitet mit dem Advertiser zusammen, um das Format der Konversions-Tags zu bestimmen, die der Advertiser implementieren muss, die Web-Seiten zu identifizieren, auf denen jedes Konversions-Tag eingefügt werden soll, und dann die zu implementierenden Konversions-Tags bereitzustellen.
