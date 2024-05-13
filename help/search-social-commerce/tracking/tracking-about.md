---
title: Informationen zum Tracking für Search, Social und Commerce
description: Erfahren Sie mehr über Tracking-Optionen für Search, Social und Commerce.
exl-id: f0fd367a-dd5a-46ec-a3d6-9b491860aae8
feature: Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# Informationen zum Tracking für Search, Social und Commerce

Um die Performance Ihrer Anzeigen zu verfolgen, benötigt Search, Social und Commerce Impressions-, Klick-, Kosten- und Konversionsdaten (Transaktionen) für Ihre Anzeigen. Search, Social und Commerce verwenden diese Daten zum Erstellen der Datenprognosemodelle, die zur Optimierung Ihrer Anzeigen-Portfolios erforderlich sind.

## Kosten-, Klick- und Impressionsdaten

In Search, Social und Commerce werden Impressions-, Klick- und Kostendaten direkt aus abgerufen. [unterstützte Werbenetzwerke](/help/search-social-commerce/introduction/supported-inventory.md) jeden Tag. Darüber hinaus können Sie Ihren Tracking-Vorlagen und Ziel-URLs in Search, Social und Commerce einen eindeutigen Klick-Trackingcode hinzufügen (einschließlich einer Umleitung auf einen Tracking-Server), um Anzeige-/Inhaltsimpressionen, Klicks und Kosten zu verfolgen und die Ereignisse später mit Konversionen zu verknüpfen.

Wenn Sie Kampagnen in Werbenetzwerken verfolgen möchten, mit denen Search, Social und Commerce keine Daten synchronisieren, müssen Sie Daten für diese Kampagnen bereitstellen, indem Sie eine tägliche Feed-Datei mit den Impressions-, Klick- und Kostendaten senden.

### Klick-Tracking-Tags

Ihr Implementierungsteam für Search, Social und Commerce richtet Klick-Tracking ein, indem es die Tracking-Vorlagen und Ziel-URLs für Anzeigen, Suchbegriffe, Platzierungen, Produktgruppen und Sitelink-Erweiterungen in Ihren synchronisierten Werbekampagnen aktualisiert, um eine eindeutige Tracking-ID-Zeichenfolge und eine Adobe Advertising-Umleitung einzuschließen. Sie fügen außerdem Tracking zu den Suffixen der Landingpage (finale URL-Suffixe) für Ihre [!DNL Google Ads] und [!DNL Microsoft Advertising] Konten und Kampagnen.

Die Tracking-Parameter ermöglichen es Adobe Advertising, Klicks auf der Ebene einzelner Keywords (Suchkampagnen) oder Anzeigenvarianten (Suchkampagnen mit Inhalt oder Site-Targeting, Display-Kampagnen und Social-Media-Kampagnen) zu verfolgen. Jedes Mal, wenn ein Benutzer eine Anzeige/Inhaltsanzeige anzeigt oder auf eine Ihrer Anzeigen klickt, sendet das Werbenetzwerk das Ereignis mithilfe eines mit dem Suchbegriff oder der Anzeige verknüpften Klick-Tracking-Tags an die Adobe Advertising-Pixelserver. Für Klicks:

* Für [!DNL Google Ads] und [!DNL Microsoft Advertising] Anzeigen in Browsern, die das parallele Tracking unterstützen, sendet das Werbenetzwerk den Klick zuerst an Ihre Website und dann an die Adobe Advertising-Pixelserver, die dann ein Cookie auf dem Benutzercomputer platzieren, falls noch kein Cookie vorhanden ist.

* In allen anderen Fällen sendet das Werbenetzwerk den Klick direkt an die Adobe Advertising-Pixelserver. Der Pixelserver platziert ein Cookie auf dem Computer des Benutzers (falls noch kein Cookie vorhanden ist) und leitet den Benutzer dann zur entsprechenden URL auf Ihrer Website weiter. Das Gesamterlebnis für den Endbenutzer entspricht dem ohne Umleitung.

Das Cookie wird im [!DNL Adobe] Domäne (`everesttech.net`) als Erstanbieter-Cookie. Nach einer Umleitung befindet sich der Benutzer in der Domäne des Advertisers und das Cookie wird dann als Drittanbieter-Cookie behandelt. Weitere Informationen zu Adobe Advertising-Cookies finden Sie unter &quot;[Adobe Advertising-Cookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html).&quot;

## Konversionsdaten

Wenn ein Kunde auf eine Anzeige klickt oder eine Anzeige oder Social-Anzeige anzeigt, müssen Search, Social und Commerce jede daraus resultierende Konversion wieder dem ursprünglichen Klick bzw. der ursprünglichen Anzeige/Social-Impression zuordnen.

Der Advertiser spielt eine Rolle bei der Bereitstellung der Konversionsdaten für alle Klicks und Anzeige-/Social-Impressionen. Konversionsdaten können Informationen zu allen Ereignistypen enthalten, die auf einer Website auftreten und zur Angebotsoptimierung verwendet werden können. Sie können Konversionsdaten bereitstellen, indem Sie Konversions-Trackingcode auf den Konversionsseiten des Werbetreibenden implementieren (z. B. die Erfolgsseite, die nach Abschluss einer Transaktion von einem Kunden angezeigt wird) oder eine tägliche Feed-Datei mit Konversionsdaten senden, die von einer anderen Methode erfasst wurden.

### Konversions-Tracking-Tags

Sie können [Konversions-Tags verschiedener Anbieter](/help/search-social-commerce/tracking/conversion-tracking-about.md).

Wenn Sie ein Adobe Advertising-Konversions-Tag verwenden und ein Benutzer eine erfolgreiche Transaktion abschließt und auf eine &quot;Erfolgsseite&quot;gelangt, prüft der Adobe Advertising-Pixelserver, ob das Cookie auf dem Benutzercomputer vorhanden ist, das zum Zeitpunkt der Klick-Umleitung festgelegt wurde. Wenn ein Cookie gefunden wird, werden Informationen über das Transaktionsereignis mithilfe des Parameters ef_transid weitergeleitet. Die Transaktion wird als Konversion erkannt und dem vorherigen Anzeigenklick bzw. der Anzeige-Impression gutgeschrieben.

Wenn der Benutzer auf mehr als eine Ihrer Anzeigen geklickt hat, ordnet die Adobe Advertising die Transaktion dem letzten Klick auf die Werbeanzeige oder (für Anzeige- oder Videokampagnen) der endgültigen Anzeigenimpression zu, sofern Sie nichts anderes angeben. Ihre [Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j) die Anzahl der Tage nach einem gebührenpflichtigen Klick oder einer Anzeige-/Videoimpression (bzw. Videoimpressionen) bestimmen, in denen das Ereignis einer Konversion zugeordnet werden kann.

Das Adobe Advertising-Implementierungsteam arbeitet mit dem Advertiser zusammen, um das Format der Konversions-Tags zu ermitteln, die der Advertiser implementieren muss, die Webseiten zu identifizieren, auf die jedes Konversions-Tag eingefügt werden soll, und die Konversions-Tags anzugeben, die implementiert werden sollen.
