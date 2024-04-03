---
title: Konversions-Tracking-Optionen für Suche, Social und Commerce
description: Erfahren Sie mehr über die Konversions-Tracking-Optionen für Search, Social und Commerce.
exl-id: 263da6a4-8d72-4882-8784-290a3be6f8fa
feature: Search Tracking
source-git-commit: c23028701ff0064bae04135d9e7a70da4c85e937
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# Konversions-Tracking-Optionen für Suche, Social und Commerce

Search, Social und Commerce können Konversionsdaten verwenden, die wie folgt verfolgt werden:

* **Adobe Advertising-verfolgte Konvertierungen:** Der Advertiser fügt auf jeder Konversionsseite ein Adobe Advertising-Konversions-Tracking-Tag ein. Das Tag sendet die Konversionsdaten an einen Tracking-Server. Sie können entweder das ältere Pixel eines Drittanbieters oder das neuere Pixel eines Erstanbieters verwenden. Siehe &quot;[Vergleich der einzelnen Konversions-Tracking-Methoden](#conversion-tracking-comparison).&quot;

* **Adobe Analytics-Konversionen:** Der Advertiser verwendet das Adobe Analytics-Tracking für alle Konversionen. Für diese Option ist eine Adobe Advertising-Adobe Analytics-Integration erforderlich. Siehe &quot;[Adobe Analytics-Konversions-Tracking](conversion-tracking-analytics.md)&quot; für weitere Informationen.

* **[!DNL Google Analytics]Konvertierungen:** Der Advertiser verwendet die [!DNL Google Analytics] -Tag, um alle Konversionen zu verfolgen. Siehe &quot;[[!DNL Google Ads] Konversionsdaten in Search, Social und Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)&quot;, um weitere Informationen zu den automatisch synchronisierten Konvertierungen zu erhalten.

* **Vom Advertiser verfolgte Konversionen:** (Nur Kunden von Search, Social und Commerce) Der Advertiser stellt eine Feed-Datei für Search, Social und Commerce mit einer beliebigen Kombination aus Online- und Offline-Konversionsdaten bereit. Siehe &quot;[Konversions-Tracking mit einem EF ID-Feed](feed-efid.md)&quot; und &quot;[Konversions-Tracking mit einem Transaktions-ID-Feed](feed-transaction-id.md).&quot;

## Vergleich der einzelnen Konversions-Tracking-Methoden {#conversion-tracking-comparison}

Da die Cookie-Richtlinien des Browsers immer strenger werden, müssen Sie Ihre aktuellen Tracking-Funktionen verstehen und Ihre besten Optionen längerfristig ermitteln.

| Tracking-Methode | Beschreibung | Einschränkungen | Vorteile | Empfohlen? |
|----|----|----|----|----|
| Adobe Analytics | Advertiser mit [Adobe Analytics für Werbung](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) automatisch importieren [!DNL Analytics] Standardereignisse und benutzerspezifische Ereignisse zur Adobe Advertising zur Berichterstellung und Optimierung. | <ul><li>[!DNL Safari] erlaubt nur ein Konversions-Lookback von sieben Tagen, das bei wiederholten Site-Besuchen während des Lookback-Fensters zurückgesetzt wird.</li><li> Erwarten Sie ähnliche Einschränkungen in [!DNL Chrome] 2024.</li></ul> | <ul><li>Nahtlose Integration mit [!DNL Analytics]</li> <li>Siehe Paid Search-Daten in [!DNL Analytics] Analysis Workspace</li><li>Vorteile außerhalb der gebührenpflichtigen Suche</li></ul> | Ja |
| Legacy-Adobe Advertising-Pixel | Advertiser fügen ihren Konvertierungsseiten Legacy-Adobe Advertising-Bild- oder JavaScript-Pixel hinzu. Das Pixel wird ausgelöst, wenn ein Benutzer, der auf eine Anzeige geklickt hat, die Seite erreicht. Diese Methode beruht auf Drittanbieter-Cookies. | <ul><li>[!DNL Safari] blockiert das gesamte Konversions-Tracking mit dieser Methode.</li><li>Erwarten Sie ähnliche Einschränkungen in [!DNL Chrome] 2024.</li></ul> | Das Pixel ist bereits implementiert. Sie müssen jedoch [das zusätzliche ITP-Zuordnungstag implementieren](itp-conversion-mapping-tag.md).<br><br>Empfehlung: Wechseln Sie zum Erstanbieter-Pixel. | Nein |
| Adobe Advertising Erstanbieter-Pixel | Advertiser gehen wie folgt vor: <ul><li>JavaScript-Bibliothek für implementieren [Adobe Experience Cloud ID-Dienst (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) über ihre gesamte Site hinweg.</li><li>Adobe Advertising hinzufügen [JavaScript-Tags mit ITP-Zuordnung](itp-conversion-mapping-tag.md) auf eine Seite zu gelangen, bei der es sich um eine Landingpage über einen Suchklick handeln könnte (idealerweise auf allen Seiten, da sich Landingpages im Laufe der Zeit ändern können). Mit dem -Tag kann Adobe Advertising ein Konversionsereignis verfolgen, das auf einer Seite auftritt, die große Zahlen in wissenschaftliche Schreibweise der Landingpage konvertiert.</li><li>Adobe Advertising hinzufügen [JavaScript-Konversions-Tracking-Tag v3](format-conversion-tag-jsv3.md) auf Konversionsseiten.</li></ul> | <ul><li>[!DNL Safari] erlaubt nur ein Konversions-Lookback von sieben Tagen, das bei wiederholten Site-Besuchen während des Lookback-Fensters zurückgesetzt wird.</li><li>Erwarten Sie ähnliche Einschränkungen in [!DNL Chrome] 2022.</li></ul> | [!DNL Safari] verfolgt Konversionen während des 7-Tage-Lookbacks. Da das Lookback bei wiederholten Site-Besuchen während des Lookback-Fensters zurückgesetzt wird, wirkt sich die Beschränkung nicht auf alle [!DNL Safari] Benutzer. | Nein |
| EFID-Feed | Die Suchkonten des Advertisers werden so eingerichtet, dass Ziel-URLs/endgültige URLs mit eindeutigen Adobe Advertising-IDs (Token) generiert werden. Wenn ein Benutzer auf eine Anzeige klickt, erstellt Adobe Advertising eine eindeutige ID (`EFID`) und zeigt sie am Ende der endgültigen URL an. Das Kundensystem des Advertisers erfasst die EFID als eindeutige Kennung für Konversionen, die aus dem Klick resultieren, und sendet sie an Adobe Advertising in einem Umsatz-Feed, der die Metrik &quot;EFID&quot;, &quot;Transaktionsdatum&quot;und &quot;Konversion&quot;enthält. Adobe Advertising verwendet dann die EFID, um die Konversion mit dem ursprünglichen Klick abzugleichen. | <ul><li>Der Werbetreibende muss über eine Möglichkeit verfügen, die EFID zu erfassen und täglich automatisierte Feeds an Adobe Advertising zu senden.</li><li>Konversionen können bis zu 180 Tage (pro Adobe Advertising) oder nach den Einschränkungen des Werbetreibers nachverfolgt werden.</li></ul> | <ul><li>Diese Methode verwendet Erstanbieter-Konversionsdaten, sodass sie nicht von Drittanbieter-Cookie-Beschränkungen betroffen ist.</li><li>Online- und Offline-Konversionen können in einem Feed gesendet werden.</li><li>Für die Site sind keine Code-Änderungen oder Tags erforderlich.</li></ul> | Ja |
| Transaktions-ID-Feed [Kombinations-Feed] | Advertiser fügen Adobe Advertising-Pixel hinzu, die einen Parameter für eine eindeutige Transaktions-ID enthalten (`ev_transid=&lt;transid&gt;`) auf ihren Webseiten speichern und Adobe Advertising die eindeutige Transaktions-ID erfassen, die beim Auslösen des Pixels erstellt wird. Das Kundensystem des Advertisers erfasst auch die [!UICONTROL Transaction ID] und sendet Adobe Advertising einen Umsatz-Feed für Offline-Konversionen mit übereinstimmenden [!UICONTROL Transaction ID] values | <ul><li>Wenn der Werbetreibende das veraltete Pixel verwendet, das [!DNL Safari] -Bausteinen ausgelöst haben, wird die ID nicht für Offline-Daten erfasst.</li><li>Der Feed ist nicht automatisiert.</li></ul> | <ul><li>Wenn Sie das Erstanbieter-Pixel implementieren, wird die [!UICONTROL Transaction ID] erfasst in [!DNL Safari].</li><li>Ermöglicht die Verfolgung von Offline-/genehmigten Konversionsereignissen.</li></ul> | Nein |
| [!DNL Google] Konversionen | Getrackte Konversionen mit [!DNL Google Analytics] -Tags werden über eine API-Verbindung automatisch in Adobe Advertising importiert. Jeder Konversionsname enthält eine `&quot;GGL_&quot;` -Präfix. | <ul><li>[!DNL Google] verfolgt normalerweise keine Offline-Daten.</li><li>[!DNL Microsoft® Advertising] -Konversionen sind nicht enthalten.</li></ul> | [!DNL Google] nutzt maschinelles Lernen zum Extrahieren von &quot;[modellierte Konversionen](https://support.google.com/google-ads/answer/10081327).&quot; | Nein |

<!--
| [!DNL Microsoft Advertising] Conversions | Conversions tracked with [!DNL Microsoft Advertising] universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | [!DNL Microsoft Advertising] typically doesn't track offline data. [!DNL Google] conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Über Adobe Advertising von Konversions-Tracking-Tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Analytics-Konversions-Tracking](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Konversions-Tracking mit einem EF ID-Feed](/help/search-social-commerce/tracking/feed-efid.md)
>* [Konversions-Tracking mit einem Transaktions-ID-Feed](/help/search-social-commerce/tracking/feed-transaction-id.md)
