---
title: Konversionsverfolgungsoptionen für Suche, Social und Commerce
description: Erfahren Sie mehr über Konversionsverfolgungsoptionen für Search, Social und Commerce.
exl-id: 263da6a4-8d72-4882-8784-290a3be6f8fa
feature: Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# Konversionsverfolgungsoptionen für Suche, Social und Commerce

Search, Social und Commerce können Konversionsdaten verwenden, die auf folgende Weise verfolgt werden:

* **Adobe Advertising-getrackte Konversionen:** Der Advertiser fügt auf jeder Konversionsseite ein Adobe Advertising-Conversion-Tracking-Tag ein. Das Tag sendet die Konvertierungsdaten an einen Tracking-Server. Sie können entweder das ältere Pixel eines Drittanbieters oder das neuere Pixel eines Erstanbieters verwenden. Siehe &quot;[Vergleich der einzelnen Konversionsverfolgungsmethoden](#conversion-tracking-comparison)&quot;.

* **Adobe Analytics-Konversionen:** Der Advertiser verwendet Adobe Analytics-Tracking für alle Konversionen. Diese Option erfordert eine Adobe Advertising-Adobe Analytics-Integration. Weitere Informationen finden Sie unter &quot;[Adobe Analytics](conversion-tracking-analytics.md)Konversionsverfolgung“.

* **[!DNL Google Analytics]Konversionen:** Advertiser verwendet das [!DNL Google Analytics]-Tag, um alle Konversionen zu verfolgen. Weitere [[!DNL Google Ads]  zu den automatisch synchronisierten Konversionen finden Sie unter &quot;](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) in Search, Social und Commerce&quot;.

* **Von Advertisern nachverfolgte Konversionen:** (Nur Search-, Social- und Commerce-Kunden) Der Advertiser stellt Search, Social und Commerce eine Feed-Datei mit einer beliebigen Kombination von Online- und Offline-Konversionsdaten bereit. Siehe &quot;[Konversionsverfolgung mit einem EF-ID-](feed-efid.md)&quot; und &quot;[Konversionsverfolgung mit einem Transaktions-ID-Feed](feed-transaction-id.md)&quot;.

## Vergleich der einzelnen Konversionsverfolgungsmethoden {#conversion-tracking-comparison}

Da die Richtlinien für Browser-Cookies immer strenger werden, ist es wichtig, Ihre aktuellen Tracking-Funktionen zu verstehen und längerfristig Ihre besten Optionen zu ermitteln.

| Tracking-Methode | Beschreibung | Einschränkungen | Vorteile | Empfohlen? |
|----|----|----|----|----|
| Adobe Analytics | Werbetreibende mit [Adobe Analytics für Advertising](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) importieren ihre [!DNL Analytics] standardmäßigen und benutzerdefinierten Ereignisse automatisch zum Reporting und zur Optimierung nach Adobe Advertising. | <ul><li>[!DNL Safari] ermöglicht nur einen siebentägigen Konversions-Lookback, der bei wiederholten Site-Besuchen während des Lookback-Fensters zurückgesetzt wird.</li><li> Für 2024 sind ähnliche Einschränkungen in [!DNL Chrome] zu erwarten.</li></ul> | <ul><li>Nahtlose Integration mit [!DNL Analytics]</li> <li>Siehe Paid-Search-Daten in [!DNL Analytics] Analysis Workspace</li><li>Vorteile jenseits der Paid Search</li></ul> | Ja |
| Legacy Adobe Advertising Pixel | Werbetreibende fügen ihren Konversionsseiten ältere Adobe Advertising-Bilder oder JavaScript-Pixel hinzu. Das Pixel wird ausgelöst, wenn ein Benutzer, der auf eine Anzeige geklickt hat, die Seite erreicht. Diese Methode beruht auf Drittanbieter-Cookies. | <ul><li>[!DNL Safari] blockiert mit dieser Methode das gesamte Konversions-Tracking.</li><li>Für 2024 sind ähnliche Einschränkungen in [!DNL Chrome] zu erwarten.</li></ul> | Das Pixel ist bereits implementiert. Sie müssen jedoch weiterhin [das zusätzliche ITP-Zuordnungs-Tag implementieren](itp-conversion-mapping-tag.md).<br><br>Empfehlung: Wechseln Sie zum Erstanbieter-Pixel. | Nein |
| Adobe Advertising-First-Party-Pixel | Werbetreibende führen die folgenden Schritte aus: <ul><li>Implementieren Sie die JavaScript-Bibliothek für den [Adobe Experience Cloud ID (ECID)-](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) auf der gesamten Site.</li><li>Fügen Sie die Adobe Advertising [JavaScript-Tags mit ITP-Zuordnung](itp-conversion-mapping-tag.md) zu jeder Seite hinzu, die eine Landingpage sein könnte, indem Sie auf eine Suche klicken (idealerweise auf allen Seiten, da sich die Landingpages im Laufe der Zeit ändern können). Mit dem Tag kann Adobe Advertising ein Konversionsereignis verfolgen, das auf einer Seite auftritt, die große Zahlen auf der Landingpage in wissenschaftliche Notation konvertiert.</li><li>Fügen Sie den Adobe Advertising [JavaScript Conversion Tracking Tag v3](format-conversion-tag-jsv3.md) zu Konversionsseiten hinzu.</li></ul> | <ul><li>[!DNL Safari] ermöglicht nur einen siebentägigen Konversions-Lookback, der bei wiederholten Site-Besuchen während des Lookback-Fensters zurückgesetzt wird.</li><li>Für 2022 sind ähnliche Einschränkungen in [!DNL Chrome] zu erwarten.</li></ul> | [!DNL Safari] verfolgt Konversionen während des siebentägigen Lookbacks. Da das Lookback bei wiederholten Site-Besuchen während des Lookback-Fensters zurückgesetzt wird, wirkt sich die Einschränkung nicht auf alle [!DNL Safari] aus. | Nein |
| EFID-Feed | Die Suchkonten des Werbetreibenden sind so eingerichtet, dass Ziel-URLs/endgültige URLs mit eindeutigen Adobe Advertising-IDs (Token) generiert werden. Wenn ein(e) Benutzende(r) auf eine Anzeige klickt, erstellt Adobe Advertising eine eindeutige ID (`EFID`) und zeigt sie am Ende der endgültigen URL an. Das Client-System des Advertisers erfasst die EFID als eindeutige Kennung für Konversionen, die aus dem Klick resultieren, und sendet sie in einem Umsatz-Feed an Adobe Advertising. Dieser Feed enthält die EFID, das Transaktionsdatum und die Konversionsmetrik. Adobe Advertising verwendet dann die EFID, um die Konvertierung mit dem ursprünglichen Klick abzugleichen. | <ul><li>Der Werbetreibende muss über eine Möglichkeit verfügen, die EFID zu erfassen und täglich automatisierte Feeds an Adobe Advertising zu senden.</li><li>Konversionen können bis zu 180 Tage (pro Adobe Advertising) oder entsprechend den Limits des Systems des Werbetreibenden verfolgt werden.</li></ul> | <ul><li>Diese Methode verwendet Erstanbieter-Konversionsdaten, sodass sie nicht von den Einschränkungen von Drittanbieter-Cookies betroffen ist.</li><li>Online- und Offline-Konversionen können in einem Feed gesendet werden.</li><li>Für die Site sind keine Code-Änderungen oder Tags erforderlich.</li></ul> | Ja |
| Transaktions-ID-Feed [kombinierter Feed] | Werbetreibende fügen ihren Web-Seiten Adobe Advertising-Pixel hinzu, die einen Parameter für eine eindeutige Transaktions-ID (`ev_transid=&lt;transid&gt;`) enthalten, und Adobe Advertising erfasst die eindeutige Transaktions-ID, die beim Auslösen des Pixels erstellt wird. Das Client-System des Advertisers erfasst auch die [!UICONTROL Transaction ID] und sendet Adobe Advertising einen Umsatz-Feed für Offline-Konversionen mit übereinstimmenden [!UICONTROL Transaction ID] | <ul><li>[!DNL Safari] Wenn der Werbetreibende das veraltete Pixel verwendet, das die Auslösung blockiert, wird die ID nicht erfasst, um sie für Offline-Daten zu verwenden.</li><li>Der Feed ist nicht automatisiert.</li></ul> | <ul><li>Wenn Sie das Erstanbieter-Pixel implementieren, wird das [!UICONTROL Transaction ID] in [!DNL Safari] erfasst.</li><li>Ermöglicht das Tracking von offline/genehmigten Konversionsereignissen.</li></ul> | Nein |
| Konversionen [!DNL Google] | Konversionen, die mit [!DNL Google Analytics] Tags verfolgt werden, werden automatisch über eine API-Verbindung auf Adobe Advertising importiert. Jeder Konversionsname hat ein `&quot;GGL_&quot;` Präfix. | <ul><li>[!DNL Google] verfolgt normalerweise keine Offline-Daten.</li><li>[!DNL Microsoft Advertising] Konversionen sind nicht enthalten.</li></ul> | [!DNL Google] verwendet maschinelles Lernen, um &quot;[&quot; Konversionen ](https://support.google.com/google-ads/answer/10081327) extrapolieren | Nein |

<!--
| [!DNL Microsoft Advertising] Conversions | Conversions tracked with [!DNL Microsoft Advertising] universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | [!DNL Microsoft Advertising] typically doesn't track offline data. [!DNL Google] conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Über Adobe Advertising-Konversions-Tracking-Tags](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Analytics-Konversionsverfolgung](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Konversionsverfolgung mit einem EF-ID-Feed](/help/search-social-commerce/tracking/feed-efid.md)
>* [Konversionsverfolgung mit einem Transaktions-ID-Feed](/help/search-social-commerce/tracking/feed-transaction-id.md)
