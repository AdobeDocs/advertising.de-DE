---
title: Konversions-Tracking-Optionen für Search, Social und Commerce
description: Erfahren Sie mehr über die Konversions-Tracking-Optionen für Search, Social und Commerce.
exl-id: 263da6a4-8d72-4882-8784-290a3be6f8fa
feature: Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# Konversions-Tracking-Optionen für Search, Social und Commerce

Search, Social und Commerce können Konversionsdaten verwenden, die wie folgt verfolgt werden:

* **Adobe Advertising-verfolgte Konversionen:** Der Advertiser fügt auf jeder Konversionsseite ein Adobe Advertising-Konversions-Tracking-Tag ein. Das Tag sendet die Konversionsdaten an einen Tracking-Server. Sie können entweder das ältere Pixel eines Drittanbieters oder das neuere Pixel eines Erstanbieters verwenden. Siehe &quot;[Vergleich der einzelnen Konversions-Tracking-Methoden](#conversion-tracking-comparison)&quot;.

* **Adobe Analytics-Konversionen:** Der Advertiser verwendet das Adobe Analytics-Tracking für alle Konversionen. Für diese Option ist eine Adobe Advertising-Adobe Analytics-Integration erforderlich. Weitere Informationen finden Sie unter &quot;[Adobe Analytics-Konversions-Tracking](conversion-tracking-analytics.md)&quot;.

* **[!DNL Google Analytics]Konversionen:** Der Advertiser verwendet das Tag [!DNL Google Analytics] , um alle Konversionen zu verfolgen. Weitere Informationen zu den automatisch synchronisierten Konversionen finden Sie unter &quot;[[!DNL Google Ads] Konversionsdaten in Search, Social und Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)&quot;.

* **Vom Advertiser verfolgte Konversionen:** (Nur Kunden von Search, Social und Commerce) Der Advertiser stellt eine Feed-Datei mit einer beliebigen Kombination aus Online- und Offline-Konversionsdaten bereit. Siehe &quot;[Konversions-Tracking mit einem EF ID-Feed](feed-efid.md)&quot;und &quot;[Konversions-Tracking mit einem Transaktions-ID-Feed](feed-transaction-id.md)&quot;.

## Vergleich der einzelnen Konversions-Tracking-Methoden {#conversion-tracking-comparison}

Da die Cookie-Richtlinien des Browsers immer strenger werden, müssen Sie Ihre aktuellen Tracking-Funktionen verstehen und Ihre besten Optionen längerfristig ermitteln.

| Tracking-Methode | Beschreibung | Einschränkungen | Vorteile | Empfohlen? |
|----|----|----|----|----|
| Adobe Analytics | Werbetreibende mit [Adobe Analytics für Advertising](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) importieren zur Berichterstellung und Optimierung automatisch ihre [!DNL Analytics] standardmäßigen und benutzerdefinierten Ereignisse in Adobe Advertising. | <ul><li>[!DNL Safari] erlaubt nur ein Konversions-Lookback von sieben Tagen, das bei wiederholten Site-Besuchen während des Lookback-Fensters zurückgesetzt wird.</li><li> Rechnen Sie für 2024 mit ähnlichen Einschränkungen in [!DNL Chrome].</li></ul> | <ul><li>Nahtlose Integration mit [!DNL Analytics]</li> <li>Siehe Paid Search-Daten in [!DNL Analytics] Analysis Workspace</li><li>Vorteile außerhalb der gebührenpflichtigen Suche</li></ul> | Ja |
| Legacy-Adobe Advertising-Pixel | Advertiser fügen ihren Konversionsseiten Legacy-Adobe Advertising-Bild oder JavaScript-Pixel hinzu. Das Pixel wird ausgelöst, wenn ein Benutzer, der auf eine Anzeige geklickt hat, die Seite erreicht. Diese Methode beruht auf Drittanbieter-Cookies. | <ul><li>[!DNL Safari] blockiert das gesamte Konversions-Tracking mit dieser Methode.</li><li>Rechnen Sie für 2024 mit ähnlichen Einschränkungen in [!DNL Chrome].</li></ul> | Das Pixel ist bereits implementiert. Sie müssen jedoch weiterhin [das zusätzliche ITP-Zuordnungs-Tag](itp-conversion-mapping-tag.md) implementieren.<br><br>Empfehlung: Wechseln Sie zum Erstanbieter-Pixel. | Nein |
| Adobe Advertising Erstanbieter-Pixel | Advertiser gehen wie folgt vor: <ul><li>Implementieren Sie die JavaScript-Bibliothek für den Dienst [Adobe Experience Cloud ID (ECID) Service](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) auf der gesamten Site.</li><li>Fügen Sie die Adobe Advertising [JavaScript-Tags mit ITP-Zuordnung](itp-conversion-mapping-tag.md) zu allen Seiten hinzu, die von einem Suchklick aus eine Landingpage sein könnten (idealerweise auf allen Seiten, da sich Landingpages im Laufe der Zeit ändern können). Mit dem -Tag kann Adobe Advertising ein Konversionsereignis verfolgen, das auf einer Seite auftritt, die große Zahlen in wissenschaftliche Schreibweise der Landingpage konvertiert.</li><li>Fügen Sie die Adobe Advertising [JavaScript-Konversions-Trackingtag v3](format-conversion-tag-jsv3.md) zu Konversionsseiten hinzu.</li></ul> | <ul><li>[!DNL Safari] erlaubt nur ein Konversions-Lookback von sieben Tagen, das bei wiederholten Site-Besuchen während des Lookback-Fensters zurückgesetzt wird.</li><li>Rechnen Sie für 2022 mit ähnlichen Einschränkungen in [!DNL Chrome].</li></ul> | [!DNL Safari] verfolgt Konversionen während des 7-Tage-Lookbacks. Da das Lookback bei wiederholten Site-Besuchen während des Lookback-Fensters zurückgesetzt wird, wirkt sich die Beschränkung nicht auf alle [!DNL Safari] -Benutzer aus. | Nein |
| EFID-Feed | Die Suchkonten des Advertisers werden so eingerichtet, dass Ziel-URLs/endgültige URLs mit eindeutigen Adobe Advertising-IDs (Token) generiert werden. Wenn ein Benutzer auf eine Anzeige klickt, erstellt Adobe Advertising eine eindeutige ID (`EFID`) und zeigt sie am Ende der endgültigen URL an. Das Kundensystem des Advertisers erfasst die EFID als eindeutige Kennung für Konversionen, die aus dem Klick resultieren, und sendet sie an Adobe Advertising in einem Umsatz-Feed, der die Metrik &quot;EFID&quot;, &quot;Transaktionsdatum&quot;und &quot;Konversion&quot;enthält. Adobe Advertising verwendet dann die EFID, um die Konversion mit dem ursprünglichen Klick abzugleichen. | <ul><li>Der Werbetreibende muss über eine Möglichkeit verfügen, die EFID zu erfassen und täglich automatisierte Feeds an Adobe Advertising zu senden.</li><li>Konversionen können bis zu 180 Tage (pro Adobe Advertising) oder nach den Einschränkungen des Werbetreibers nachverfolgt werden.</li></ul> | <ul><li>Diese Methode verwendet Erstanbieter-Konversionsdaten, sodass sie nicht von Drittanbieter-Cookie-Beschränkungen betroffen ist.</li><li>Online- und Offline-Konversionen können in einem Feed gesendet werden.</li><li>Für die Site sind keine Code-Änderungen oder Tags erforderlich.</li></ul> | Ja |
| Transaktions-ID-Feed [Kombinations-Feed] | Advertiser fügen ihren Webseiten Adobe Advertising-Pixel hinzu, die einen Parameter für eine eindeutige Transaktions-ID (`ev_transid=&lt;transid&gt;`) enthalten, und Adobe Advertising erfasst die eindeutige Transaktions-ID, die beim Auslösen des Pixels erstellt wird. Das Client-System des Advertisers erfasst auch die [!UICONTROL Transaction ID] und sendet Adobe Advertising einen Umsatz-Feed für Offline-Konversionen mit übereinstimmenden [!UICONTROL Transaction ID] -Werten | <ul><li>Wenn der Werbetreibende das veraltete Pixel verwendet, das von [!DNL Safari] nicht ausgelöst werden kann, wird die ID nicht für Offline-Daten erfasst.</li><li>Der Feed ist nicht automatisiert.</li></ul> | <ul><li>Wenn Sie das Erstanbieter-Pixel implementieren, wird der [!UICONTROL Transaction ID] in [!DNL Safari] erfasst.</li><li>Ermöglicht die Verfolgung von Offline-/genehmigten Konversionsereignissen.</li></ul> | Nein |
| [!DNL Google] Konversionen | Mit [!DNL Google Analytics] -Tags verfolgte Konversionen werden über eine API-Verbindung automatisch in Adobe Advertising importiert. Jeder Konversionsname hat ein &quot;`&quot;GGL_&quot;`&quot;-Präfix. | <ul><li>[!DNL Google] verfolgt in der Regel keine Offline-Daten.</li><li>[!DNL Microsoft Advertising] Konversionen sind nicht enthalten.</li></ul> | [!DNL Google] verwendet maschinelles Lernen, um &quot;[modellierte Konversionen](https://support.google.com/google-ads/answer/10081327)&quot;zu extrapolieren. | Nein |

<!--
| [!DNL Microsoft Advertising] Conversions | Conversions tracked with [!DNL Microsoft Advertising] universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | [!DNL Microsoft Advertising] typically doesn't track offline data. [!DNL Google] conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Über Adobe Advertising von Konversions-Tracking-Tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Analytics-Konversions-Tracking](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Konversions-Tracking mit einem EF ID-Feed](/help/search-social-commerce/tracking/feed-efid.md)
>* [Konversions-Tracking mit einem Transaktions-ID-Feed](/help/search-social-commerce/tracking/feed-transaction-id.md)
