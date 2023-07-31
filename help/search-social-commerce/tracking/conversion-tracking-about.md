---
title: Konversions-Tracking-Optionen für Suche, Social und Commerce
description: Erfahren Sie mehr über die Konversions-Tracking-Optionen für Search, Social und Commerce.
exl-id: 098efaf8-6ffb-4811-8b20-41c7c85df812
feature: Search Tracking
source-git-commit: f21283731d7a1830af585cec43805c54c81c72ff
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Konversions-Tracking-Optionen für Suche, Social und Commerce

Search, Social und Commerce können Konversionsdaten verwenden, die wie folgt verfolgt werden:

* **Vom Adobe Advertising verfolgte Konversionen:** Der Advertiser fügt auf jeder Konversionsseite ein Adobe Advertising-Konversions-Tracking-Tag ein. Das Tag sendet die Konversionsdaten an einen Tracking-Server. Sie können entweder das ältere Pixel eines Drittanbieters oder das neuere Pixel eines Erstanbieters verwenden. Siehe &quot;[Vergleich der einzelnen Konversions-Tracking-Methoden](#conversion-tracking-comparison).&quot;

* **Adobe Analytics-Konversionen:** Der Advertiser verwendet das Adobe Analytics-Tracking für alle Konversionen. Für diese Option ist eine Adobe Advertising-Adobe Analytics-Integration erforderlich. Siehe &quot;[Adobe Analytics-Konversions-Tracking](conversion-tracking-analytics.md)&quot; für weitere Informationen.

* **[!DNL Google Analytics]Konvertierungen:** Der Advertiser verwendet die [!DNL Google Analytics] -Tag, um alle Konversionen zu verfolgen. Siehe &quot;[[!DNL Google Ads] Konversionsdaten in Search, Social und Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)&quot;, um weitere Informationen zu den automatisch synchronisierten Konvertierungen zu erhalten.

* **Vom Advertiser verfolgte Konversionen:** (Nur Kunden von Search, Social und Commerce) Der Advertiser stellt eine Feed-Datei für Search, Social und Commerce mit einer beliebigen Kombination aus Online- und Offline-Konversionsdaten bereit. Siehe &quot;[Konversions-Tracking mit einem EF ID-Feed](feed-efid.md)&quot; und &quot;[Konversions-Tracking mit einem Transaktions-ID-Feed](feed-transaction-id.md).&quot;

## Vergleich der einzelnen Konversions-Tracking-Methoden {#conversion-tracking-comparison}

Da die Cookie-Richtlinien des Browsers immer strenger werden, müssen Sie Ihre aktuellen Tracking-Funktionen verstehen und Ihre besten Optionen längerfristig ermitteln.

| Tracking-Methode | Beschreibung | Einschränkungen | Vorteile | Empfohlen? |
|----|----|----|----|----|
| Adobe Analytics | Advertiser mit [Adobe Analytics für Werbung](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) automatisch importieren [!DNL Analytics] standardmäßigen und benutzerspezifischen Ereignissen in Adobe Advertising für die Berichterstellung und Optimierung. | <ul><li>[!DNL Safari] erlaubt nur ein Konversions-Lookback von sieben Tagen, das bei wiederholten Site-Besuchen während des Lookback-Fensters zurückgesetzt wird.</li><li> Erwarten Sie ähnliche Einschränkungen in [!DNL Chrome] 2024.</li></ul> | <ul><li>Nahtlose Integration mit [!DNL Analytics]</li> <li>Siehe Paid Search-Daten in [!DNL Analytics] Analysis Workspace</li><li>Vorteile außerhalb der gebührenpflichtigen Suche</li></ul> | Ja |
| Veraltetes Adobe Advertising-Pixel | Advertiser fügen ihren Konvertierungsseiten Legacy-Adobe Advertising- oder JavaScript-Pixel hinzu. Das Pixel wird ausgelöst, wenn ein Benutzer, der auf eine Anzeige geklickt hat, die Seite erreicht. Diese Methode beruht auf Drittanbieter-Cookies. | <ul><li>[!DNL Safari] blockiert das gesamte Konversions-Tracking mit dieser Methode.</li><li>Erwarten Sie ähnliche Einschränkungen in [!DNL Chrome] 2024.</li></ul> | Das Pixel ist bereits implementiert. Sie müssen jedoch [das zusätzliche ITP-Zuordnungstag implementieren](itp-conversion-mapping-tag.md).<br><br>Empfehlung: Wechseln Sie zum Erstanbieter-Pixel. | Nein |
| Adobe Advertising-Erstanbieter-Pixel | Advertiser gehen wie folgt vor: <ul><li>JavaScript-Bibliothek für implementieren [Adobe Experience Cloud ID-Dienst (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) über ihre gesamte Site hinweg.</li><li>Adobe Advertising hinzufügen [JavaScript-Tags mit ITP-Zuordnung](itp-conversion-mapping-tag.md) auf eine Seite zu gelangen, bei der es sich um eine Landingpage über einen Suchklick handeln könnte (idealerweise auf allen Seiten, da sich Landingpages im Laufe der Zeit ändern können). Mit dem -Tag kann der Adobe Advertising ein Konversionsereignis verfolgen, das auf einer Seite auftritt, die große Zahlen in wissenschaftliche Schreibweise auf der Landingpage konvertiert.</li><li>Adobe Advertising hinzufügen [JavaScript-Konversions-Tracking-Tag v3](format-conversion-tag-jsv3.md) auf Konversionsseiten.</li></ul> | <ul><li>[!DNL Safari] erlaubt nur ein Konversions-Lookback von sieben Tagen, das bei wiederholten Site-Besuchen während des Lookback-Fensters zurückgesetzt wird.</li><li>Erwarten Sie ähnliche Einschränkungen in [!DNL Chrome] 2022.</li></ul> | [!DNL Safari] verfolgt Konversionen während des 7-Tage-Lookbacks. Da das Lookback bei wiederholten Site-Besuchen während des Lookback-Fensters zurückgesetzt wird, wirkt sich die Beschränkung nicht auf alle [!DNL Safari] Benutzer. | Nein |
| EFID-Feed | Die Suchkonten des Advertisers werden eingerichtet, um Ziel-URLs/endgültige URLs mit eindeutigen IDs (Token) für den Adobe Advertising zu generieren. Wenn ein Benutzer auf eine Anzeige klickt, erstellt der Adobe Advertising eine eindeutige ID (`EFID`) und zeigt sie am Ende der endgültigen URL an. Das Kundensystem des Advertisers erfasst die EFID als eindeutige Kennung für Konversionen, die aus dem Klick resultieren, und sendet sie an den Adobe Advertising in einem Umsatz-Feed, der die Metrik für EFID, Transaktionsdatum und Konversion enthält. Adobe Advertising verwendet dann die EFID, um die Konversion mit dem ursprünglichen Klick abzugleichen. | <ul><li>Der Werbetreibende muss über eine Möglichkeit verfügen, die EFID zu erfassen und täglich automatisierte Feeds an den Adobe Advertising zu senden.</li><li>Konversionen können bis zu 180 Tage (pro Adobe Advertising) oder nach den gesetzlichen Vorgaben des Werbetreibenden verfolgt werden.</li></ul> | <ul><li>Diese Methode verwendet Erstanbieter-Konversionsdaten, sodass sie nicht von Drittanbieter-Cookie-Beschränkungen betroffen ist.</li><li>Online- und Offline-Konversionen können in einem Feed gesendet werden.</li><li>Für die Site sind keine Code-Änderungen oder Tags erforderlich.</li></ul> | Ja |
| Transaktions-ID-Feed [Kombinations-Feed] | Advertiser fügen Adobe Advertising-Pixel hinzu, die einen Parameter für eine eindeutige Transaktions-ID enthalten (`ev_transid=&lt;transid&gt;`) auf ihren Webseiten speichern, und Adobe Advertising erfasst die eindeutige Transaktions-ID, die beim Auslösen des Pixels erstellt wird. Das Kundensystem des Advertisers erfasst auch die [!UICONTROL Transaction ID] und sendet dem Adobe Advertising einen Umsatz-Feed für Offline-Konversionen mit übereinstimmenden [!UICONTROL Transaction ID] values | <ul><li>Wenn der Werbetreibende das veraltete Pixel verwendet, das [!DNL Safari] -Bausteinen ausgelöst haben, wird die ID nicht für Offline-Daten erfasst.</li><li>Der Feed ist nicht automatisiert.</li></ul> | <ul><li>Wenn Sie das Erstanbieter-Pixel implementieren, wird die [!UICONTROL Transaction ID] erfasst in [!DNL Safari].</li><li>Ermöglicht die Verfolgung von Offline-/genehmigten Konversionsereignissen.</li></ul> | Nein |
| Google-Konversionen | Getrackte Konversionen mit [!DNL Google Analytics] -Tags werden über eine API-Verbindung automatisch in Adobe Advertising importiert. Jeder Konversionsname enthält eine `&quot;GGL_&quot;` -Präfix. | <ul><li>Google verfolgt in der Regel keine Offline-Daten.</li><li>Microsoft® Advertising-Konversionen sind nicht enthalten.</li></ul> | Google verwendet maschinelles Lernen, um &quot;[modellierte Konversionen](https://support.google.com/google-ads/answer/10081327).&quot; | Nein |

<!--
| Microsoft Advertising Conversions | Conversions tracked with Microsoft Advertising universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | Microsoft Advertising typically doesn't track offline data. Google conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Über Adobe Advertising-Konversions-Tracking-Tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Analytics-Konversions-Tracking](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Konversions-Tracking mit einem EF ID-Feed](/help/search-social-commerce/tracking/feed-efid.md)
>* [Konversions-Tracking mit einem Transaktions-ID-Feed](/help/search-social-commerce/tracking/feed-transaction-id.md)
