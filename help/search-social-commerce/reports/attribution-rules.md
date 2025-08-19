---
title: Wie Attributionsregeln berechnet werden
description: Erfahren Sie, wie Adobe Advertising die einzelnen Attributionsregeltypen berechnet.
exl-id: 15beeadd-bb65-4efe-8c4f-34c4a48cc775
feature: Search Reports, DSP Custom Reports
source-git-commit: 513d81cf835ccbffa16581799f0dc8306681e3ad
workflow-type: tm+mt
source-wordcount: '2711'
ht-degree: 0%

---

# Berechnen der Attributionsregeln für Adobe Advertising

*Werbetreibende nur mit Adobe Advertising-Konversions-Tracking*

<!-- Verify statements about cross-device events -->

Die Attributionsregel auf Advertiser-Ebene wird verwendet, um Konversionsdaten - möglicherweise über mehrere Anzeigenkanäle hinweg - in einer Reihe von Ereignissen zuzuordnen, die zu einer Konversion führen.

Sie können an den folgenden Stellen auch eine Attributionsregel auswählen, um die Regel nur auf die resultierenden Daten anzuwenden:

* DSP

   * Benutzerdefinierte Berichte mit Multi-Touch-Attribution

* Suche, Social und Commerce

   * Benutzerdefinierte Berichte

   * Standardmäßige und benutzerdefinierte Ansichten

   * (Einige Benutzerrollen) Simulationen auf Portfolio-Ebene.

>[!NOTE]
>
>* Die Zuordnungsregeln gelten für Klicks auf bezahlte Anzeigen in jedem beliebigen Kanal und für Impressionen auf Display- und Social-Media-Anzeigen. Sie gelten nicht für Impressionen für Paid Search-Anzeigen, die nicht auf Ereignisebene verfolgt werden können.
>* Adobe Advertising speichert vor einer Konversion immer die folgenden Ereignisse für jeden Websurfer: a) den ersten gebührenpflichtigen Klick; b) bis zu 10 Klicks für jeden Kanal (Suche, Social oder Display), einschließlich des ersten Klicks; und c) bis zu 10 Display-Impressionen.<!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
>* In Advertising DSP und Advertising Creative berücksichtigen geräteübergreifende Definitionen nur den Ereignispfad, der in der ausgewählten Attributionsregel angegeben ist.<!-- cross-device attribution via LiveRamp only -->
>* In Berichten und Verwaltungsansichten hängt die Anzahl der für einen Wert angezeigten Dezimalstellen von der Währung ab, Adobe Advertising speichert jedoch präzisere Werte.

## Letztes Ereignis (Standard)

ordnet die Konversion dem letzten bezahlten Klick in der Reihe innerhalb des [Klick-Lookback-Fensters des Werbetreibenden ](/help/search-social-commerce/glossary.md#c-d), falls keine bezahlten Klicks aufgetreten sind, der letzten Impression innerhalb des [Impression-Lookback-Fensters des Werbetreibenden ](/help/search-social-commerce/glossary.md#i-j).

Wenn der Konversion nur Impressions vorausgehen, wird die Konversion als *View-Through* betrachtet, die entweder gemäß der [View-Through-Gewichtungseinstellung des Werbetreibenden ](/help/search-social-commerce/glossary.md#uv) — wie angegeben — gemäß der im Bericht, in der Ansicht oder in den benutzerdefinierten Simulationsparametern angegebenen View-Through-Bewertungsmethode gewichtet wird.

![Prozentsatz der Attribution des letzten Ereignisses](/help/search-social-commerce/assets/attribution-percent-last-event.png "Prozentsatz der Attribution des letzten Ereignisses")

<!-- start examples as collapsible content -->

+++Beispiele für Ereignisberechnungen

### Beispiel mit allen Klicks

Ereignispfad: Click1, Click2, Click3, Konversion von 120 USD

Die Konversion wird Click 3 in Höhe von 120 USD zugeordnet.

### Beispiel mit Impressionen und Klicks

**Hinweis:** Impressionen können nur in Display- und Social-Media-Anzeigen verwendet werden.

Ereignispfad: Impression 1, Klick 1, Impression 2, Konversion von 120 USD

Die Konversion wird Click 1 in Höhe von 120 USD zugeordnet.

### Beispiel mit allen Impressionen

**Hinweis:** Es gelten nur Impressionen für Display- und Social-Media-Anzeigen.

Ereignispfad: Impression 1, Impression 2, Impression 3, Konversion von 120 USD

Die Konversion wird Impression 3 zugeordnet. Da es sich bei der Konversion um eine Durchsicht handelt, wird die im Abschnitt „Konversionszuordnung“ der Berichtseinstellungen ausgewählte Durchsichts-Bewertungsmethode angewendet:

* Wenn der Berichtsparameter eine gewichtete View-Through-Gewichtung angibt, wird diese Gewichtung auf die View-Through angewendet. Wenn beispielsweise das Durchsichtsgewicht des Werbetreibenden 40 % beträgt, dann sind 120 USD x 40 % = 48 USD, sodass 48 USD Impression 3 zugeordnet werden.

* Wenn der Berichtsparameter die Verwendung von Rohwerten für Durchsichten angibt, wird keine Durchsichtsgewichtung auf die Durchsicht angewendet, und die vollen 120 USD werden Impression 3 zugeordnet.

+++

<!-- end examples as collapsible content -->

## Erstes Ereignis

ordnet die Konversion dem ersten bezahlten Klick in der Reihe innerhalb des [Klick-Lookback-Fensters des Werbetreibenden ](/help/search-social-commerce/glossary.md#c-d), oder, falls keine bezahlten Klicks aufgetreten sind, der ersten Impression innerhalb des [Impression-Lookback-Fensters des Werbetreibenden zu](/help/search-social-commerce/glossary.md#i-j). Diese Regel ist nur für Ereignisse auf einzelnen Geräten verfügbar.

Wenn der Konversion nur Impressions vorausgehen, wird die Konversion als *View-Through* betrachtet, die entweder gemäß der [View-Through-Gewichtungseinstellung des Werbetreibenden ](/help/search-social-commerce/glossary.md#uv) — wie angegeben — gemäß der im Bericht, in der Ansicht oder in den benutzerdefinierten Simulationsparametern angegebenen View-Through-Bewertungsmethode gewichtet wird.

![Prozentsätze der ersten Ereigniszuordnung](/help/search-social-commerce/assets/attribution-percent-first-event.png "Prozentsätze der ersten Ereigniszuordnung")

<!-- start examples as collapsible content -->

+++Beispiele für Ereignisberechnungen

### Beispiel mit allen Klicks

Ereignispfad: Klicken Sie 1, Klicken Sie 2, Klicken Sie 3, Konversion von 120 USD

Die Konversion wird Click 1 in Höhe von 120 USD zugeordnet.

### Beispiel mit Impressionen und Klicks

**Hinweis:** Impressionen können nur in Display- und Social-Media-Anzeigen verwendet werden.

Ereignispfad: Impression 1, Klick 1, Impression 2, Konversion von 120 USD

Die Konversion wird Click 1 in Höhe von 120 USD zugeordnet.

### Beispiel mit allen Impressionen

**Hinweis:** Es gelten nur Impressionen für Display- und Social-Media-Anzeigen.

Ereignispfad: Impression 1, Impression 2, Impression 3, Konversion von 120 USD

Die Konversion wird Impression 1 zugeordnet. Da es sich bei der Konversion um eine Durchsicht handelt, wird bei der Konversion „Kampagnen anzeigen“ die Durchsichts-Auswertungsmethode ausgewählt
Der Abschnitt „Attribution“ der Berichteinstellungen wird angewendet:

* Wenn der Berichtsparameter eine gewichtete View-Through-Gewichtung angibt, wird diese Gewichtung auf die View-Through angewendet. Wenn beispielsweise das Durchsichtsgewicht des Werbetreibenden 40 % beträgt, dann sind 120 x 40 % = 48 USD, sodass 48 USD Impression 1 zugeordnet werden.

* Wenn der Berichtsparameter die Verwendung von Rohwerten für Durchsichten angibt, wird keine Durchsichtsgewichtung auf die Durchsicht angewendet, und die vollen 120 USD werden Impression 1 zugeordnet.

+++

<!-- end examples as collapsible content -->

## Erstes Ereignis gewichten mehr

ordnet die Konversion allen Ereignissen der Reihe zu, die im [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j) des Advertisers aufgetreten sind, gewichtet jedoch das erste Ereignis am meisten und die folgenden Ereignisse wurden weniger gewichtet. Diese Regel ist nur für Ereignisse auf einzelnen Geräten verfügbar.

Wenn der Konversion nur Impressions vorausgehen, wird die Konversion als *View-Through* betrachtet, die entweder gemäß der [View-Through-Gewichtungseinstellung des Werbetreibenden ](/help/search-social-commerce/glossary.md#uv) — wie angegeben — gemäß der im Bericht, in der Ansicht oder in den benutzerdefinierten Simulationsparametern angegebenen View-Through-Bewertungsmethode gewichtet wird.

Wenn der Konversionspfad sowohl bezahlte Klicks als auch Impressions enthält, werden die Impressions von verschiedenen Adobe Advertising-Produkten unterschiedlich behandelt:

* In Search, Social und Commerce wird die [Impression Override-Gewichtung](/help/search-social-commerce/glossary.md#i-j), die in der Einstellung „Impression Override-Gewichtung“ des Advertisers und in Berichten, Ansichten oder benutzerdefinierten Simulationsparametern angegeben ist, zunächst auf die Impressionen angewendet.

* In DSP werden die Impressionen ignoriert und nur Klicks werden gewichtet. DSP berücksichtigt bei der Attribution nicht die Gewichtung der Impression-Überschreibung.

![Gewicht des ersten Ereignisses - mehr Attributionsprozentsätze](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "Gewicht des ersten Ereignisses - mehr Attributionsprozentsätze")

<!-- start examples as collapsible content -->

+++Beispiele für Ereignisberechnungen

### Beispiel mit allen Klicks

Ereignispfad: Klicken Sie 1, Klicken Sie 2, Klicken Sie 3, Konversion von 120 USD

Attribution: Klick 1 = 60 USD, Klick 2 = 40 USD, Klick 3 = 20 USD (insgesamt 120 USD)

### Beispiele mit sowohl Impressionen als auch Klicks

**Hinweis:** Impressionen können nur in Display- und Social-Media-Anzeigen verwendet werden.

Ereignispfad: Impression 1, Klick 1, Impression 2, Klick 2, Konversion von 120 USD

#### (Nur für Search, Social und Commerce) Verwenden der standardmäßigen Impression Override-Gewichtung von 10 %

Da die Ereignisserie sowohl Impressionen als auch Klicks enthält, gilt die Gewichtung der Impression-Überschreibung für die Impressionen.

Attribution: Impression 1 = 8 USD, Klick 1 = 72 USD, Impression 2 = 4 USD, Klick 2 = 36 USD (insgesamt 120 USD)

#### Verwendung von (nur DSP) ohne Impression Override-Gewichtung oder (Nur Suche, Social und Commerce) einer „Impression Override-Gewichtung“ von 0 %

Da die Ereignisserie sowohl Impressionen als auch Klicks enthält, werden die Impressionen ignoriert.

Attribution: Impression 1 = 0 USD, Klick 1 = 80 USD, Impression 2 = 0 USD, Klick 2 = 40 USD (insgesamt 120 USD)

### Beispiel mit allen Impressionen

**Hinweis** Es können nur Impressionen für Display-Anzeigen verwendet werden.

Ereignispfad: Impression 1, Impression 2, Impression 3, Konversion von 120 USD

Da es sich bei der Konversion um eine Durchsicht handelt, wird die Durchsichts-Bewertungsmethode - anstelle der Impression Override-Gewichtung - angewendet, um den Wert jeder Impression zu bestimmen:

* Wenn der Berichtsparameter eine gewichtete Durchsichtsgewichtung angegeben hat, wird diese Gewichtung auf die Impressionswerte angewendet. Wenn die Durchsichtsgewichtung beispielsweise 40 % beträgt, dann ist Impression 1 = 24 USD, Impression 2 = 16 USD, Impression 3 = 8 USD (insgesamt 48 USD)

* Wenn der Berichtsparameter die Verwendung von Rohwerten für Durchsichten angibt, wird keine Durchsichtsgewichtung auf die Impression angewendet und die vollen 120 USD werden auf die drei Impressionen aufgeteilt: Impression 1 = 60 USD, Impression 2 = 40 USD, Impression 3 = 20 USD (insgesamt 120 USD)

+++

<!-- end examples as collapsible content -->

## gleichmäßige Verteilung

>[!NOTE]
>
>Diese Regel ist nur für Ereignisse auf einzelnen Geräten verfügbar.

Attributiert die Konversion zu gleichen Teilen jedem Ereignis in der Reihe, das innerhalb des (Klick[Lookback-Fensters und ](/help/search-social-commerce/glossary.md#c-d)Impression-Lookback-Fensters[ des Werbetreibenden aufgetreten ](/help/search-social-commerce/glossary.md#i-j).

Wenn der Konversion nur Impressions vorausgehen, wird die Konversion als *View-Through* betrachtet, die entweder gemäß der [View-Through-Gewichtungseinstellung des Werbetreibenden ](/help/search-social-commerce/glossary.md#uv) — wie angegeben — gemäß der im Bericht, in der Ansicht oder in den benutzerdefinierten Simulationsparametern angegebenen View-Through-Bewertungsmethode gewichtet wird.

Wenn der Konversionspfad sowohl bezahlte Klicks als auch Impressions enthält, werden die Impressions von verschiedenen Adobe Advertising-Produkten unterschiedlich behandelt:

* In Search, Social und Commerce wird die [Impression Override-Gewichtung](/help/search-social-commerce/glossary.md#i-j), die in der Einstellung „Impression Override-Gewichtung“ des Advertisers und in Berichten, Ansichten oder benutzerdefinierten Simulationsparametern angegeben ist, zunächst auf die Impressionen angewendet.

* In DSP werden die Impressionen ignoriert und nur Klicks werden gewichtet. DSP berücksichtigt bei der Attribution nicht die Gewichtung der Impression-Überschreibung.

![Gerade Prozentsätze](/help/search-social-commerce/assets/attribution-percent-even.png "Gerade Prozentsätze")

<!-- start examples as collapsible content -->

+++Beispiele für Ereignisberechnungen

### Beispiel mit allen Klicks

Ereignispfad: Klicken Sie 1, Klicken Sie 2, Klicken Sie 3, Konversion von 120 USD

Keine Impressions führten zur Konversion, daher ist die Gewichtung der Impression-Überschreibung nicht anwendbar, und die Konversion wird zu gleichen Teilen auf die drei Klicks aufgeteilt:

Attribution: Klick 1 = 40 USD, Klick 2 = 40 USD, Klick 3 = 40 USD (insgesamt 120 USD)

### Beispiele mit sowohl Impressionen als auch Klicks

**Hinweis:** Impressionen können nur in Display- und Social-Media-Anzeigen verwendet werden.

Ereignispfad: Impression 1, Klick 1, Impression 2, Klick 2, Konversion von 120 USD

#### (Nur für Search, Social und Commerce) Verwenden der standardmäßigen Impression Override-Gewichtung von 10 %

Da die Ereignisserie sowohl Impressionen als auch Klicks enthält, gilt die Gewichtung der Impression-Überschreibung für die Impressionen.

Attribution: Impression 1 = 6 USD, Klick 1 = 54 USD, Impression 2 = 6 USD, Klick 2 = 54 USD (insgesamt 120 USD)

#### Verwendung von (nur Adobe Advertising DSP) ohne Impression Override-Gewichtung oder (Nur Suche, Social und Commerce) einer „Impression Override-Gewichtung“ von 0 %

Da die Ereignisserie sowohl Impressionen als auch Klicks enthält, werden die Impressionen ignoriert.

Attribution: Impression 1 = 0 USD, Klick 1 = 60 USD, Impression 2 = 0 USD, Klick 2 = 60 USD (insgesamt 120 USD)

## Beispiel mit allen Impressionen

**Hinweis** Es können nur Impressionen für Display-Anzeigen verwendet werden.

Ereignispfad: Impression 1, Impression 2, Impression 3, Konversion von 120 USD

Da es sich bei der Konversion um eine Durchsicht handelt, wird die Durchsichts-Bewertungsmethode - anstelle der Impression Override-Gewichtung - angewendet, um den Wert jeder Impression zu bestimmen:

* Wenn der Berichtsparameter eine gewichtete Durchsichtsgewichtung angegeben hat, wird diese Gewichtung auf die Impressionswerte angewendet. Wenn die Durchsichtsgewichtung beispielsweise 40 % beträgt, dann ist Impression 1 = 16 USD, Impression 2 = 16 USD, Impression 3 = 16 USD (insgesamt 48 USD)

* Wenn der Berichtsparameter die Verwendung von Rohwerten für Durchsichten angibt, wird keine Durchsichtsgewichtung auf die Impression angewendet und die vollen 120 USD werden auf die drei Impressionen aufgeteilt: Impression 1 = 40 USD, Impression 2 = 40 USD, Impression 3 = 40 USD (insgesamt 120 USD)

+++

<!-- end examples as collapsible content -->

## Letztes Ereignis gewichten mehr

ordnet die Konversion allen Ereignissen in der Reihe zu, die im [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j) des Werbetreibenden stattfanden, gewichtet jedoch am häufigsten das letzte Ereignis und hat nacheinander weniger Gewicht auf die vorherigen Ereignisse.

Wenn der Konversion nur Impressions vorausgehen, wird die Konversion als *View-Through* betrachtet, die entweder gemäß der [View-Through-Gewichtungseinstellung des Werbetreibenden ](/help/search-social-commerce/glossary.md#uv) — wie angegeben — gemäß der im Bericht, in der Ansicht oder in den benutzerdefinierten Simulationsparametern angegebenen View-Through-Bewertungsmethode gewichtet wird.

Wenn der Konversionspfad sowohl bezahlte Klicks als auch Impressions enthält, werden die Impressions von verschiedenen Adobe Advertising-Produkten unterschiedlich behandelt:

* In Search, Social und Commerce wird die [Impression Override-Gewichtung](/help/search-social-commerce/glossary.md#i-j), die in der Einstellung „Impression Override-Gewichtung“ des Advertisers und in Berichten, Ansichten oder benutzerdefinierten Simulationsparametern angegeben ist, zunächst auf die Impressionen angewendet.

* In DSP werden die Impressionen ignoriert und nur Klicks werden gewichtet. DSP berücksichtigt bei der Attribution nicht die Gewichtung der Impression-Überschreibung.

![Gewicht des letzten Ereignisses - mehr Attributionsprozentsätze](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png "Gewicht des letzten Ereignisses - mehr Attributionsprozentsätze")

<!-- start examples as collapsible content -->

+++Beispiele für Ereignisberechnungen

### Beispiel mit allen Klicks

Ereignispfad: Klicken Sie 1, Klicken Sie 2, Klicken Sie 3, Konversion von 120 USD

Attribution: Klick 3 = 60 USD, Klick 2 = 40 USD, Klick 1 = 20 USD (insgesamt 120 USD)

### Beispiele mit sowohl Impressionen als auch Klicks

**Hinweis:** Impressionen können nur in Display- und Social-Media-Anzeigen verwendet werden.

Ereignispfad: Impression 1, Klick 1, Impression 2, Klick 2, Konversion von 120 USD

#### (Nur für Search, Social und Commerce) Verwenden der standardmäßigen Impression Override-Gewichtung von 10 %

Da die Ereignisserie sowohl Impressionen als auch Klicks enthält, gilt die Gewichtung der Impression-Überschreibung für die Impressionen.

Attribution: Impression 1 = 4 USD, Klick 1 = 36 USD, Impression 2 = 8 USD, Klick 2 = 72 USD (insgesamt 120 USD)

#### Verwendung von (nur DSP) ohne Impression Override-Gewichtung oder (Nur Suche, Social und Commerce) einer „Impression Override-Gewichtung“ von 0 %

Da die Ereignisserie sowohl Impressionen als auch Klicks enthält, werden die Impressionen ignoriert.

Attribution: Impression 1 = 0 USD, Klick 1 = 40 USD, Impression 2 = 0 USD, Klick 2 = 80 USD (insgesamt 120 USD)

### Beispiel mit allen Impressionen

**Hinweis:** Impressionen können nur in Display- und Social-Media-Anzeigen verwendet werden.

Ereignispfad: Impression 1, Impression 2, Impression 3, Konversion von 120 USD

Da es sich bei der Konversion um eine Durchsicht handelt, wird die Durchsichts-Bewertungsmethode - anstelle der Impression Override-Gewichtung - angewendet, um den Wert jeder Impression zu bestimmen:

* Wenn der Berichtsparameter eine gewichtete Durchsichtsgewichtung angegeben hat, wird diese Gewichtung auf die Impressionswerte angewendet. Wenn die Durchsichtsgewichtung beispielsweise 40 % beträgt, multiplizieren Sie jeden Wert im „Beispiel mit allen Klicks“ mit 40 %: Impression 3 = 24 USD, Impression 2 = 16 USD, Impression 1 = 8 USD (insgesamt 48 USD)

* Wenn der Berichtsparameter die Verwendung von Rohwerten für Durchsichten angibt, werden die ganzen 120 USD auf die Impressionen aufgeteilt: Impression 3 = 60 USD, Impression 2 = 40 USD, Impression 1 = 20 USD (insgesamt 120 USD)

+++

<!-- end examples as collapsible content -->

## U-förmig

ordnet die Konversion allen Ereignissen in der Reihe zu, die im [Klick-Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j) des Advertisers aufgetreten sind, gewichtet jedoch am meisten das erste und das letzte Ereignis, wobei den Ereignissen in der Mitte des Konversionspfads sukzessive weniger Gewicht zugewiesen wird.

Wenn der Konversion nur Impressions vorausgehen, wird die Konversion als *View-Through* betrachtet, die entweder gemäß der [View-Through-Gewichtungseinstellung des Werbetreibenden ](/help/search-social-commerce/glossary.md#uv) — wie angegeben — gemäß der im Bericht, in der Ansicht oder in den benutzerdefinierten Simulationsparametern angegebenen View-Through-Bewertungsmethode gewichtet wird.

Wenn der Konversionspfad sowohl bezahlte Klicks als auch Impressions enthält, werden die Impressions von verschiedenen Adobe Advertising-Produkten unterschiedlich behandelt:

* In Search, Social und Commerce wird die [Impression Override-Gewichtung](/help/search-social-commerce/glossary.md#i-j), die in der Einstellung „Impression Override-Gewichtung“ des Advertisers und in Berichten, Ansichten oder benutzerdefinierten Simulationsparametern angegeben ist, zunächst auf die Impressionen angewendet.

* In DSP werden die Impressionen ignoriert und nur Klicks werden gewichtet. DSP berücksichtigt bei der Attribution nicht die Gewichtung der Impression-Überschreibung.

![U-förmige Attributionsprozentsätze](/help/search-social-commerce/assets/attribution-percent-u-shaped.png "U-förmige Attributionsprozentsätze")

<!-- start examples as collapsible content -->

+++Beispiele für Ereignisberechnungen

### Beispiel mit allen Klicks

Ereignispfad: Klicken Sie 1, Klicken Sie 2, Klicken Sie 3, Klicken 4, Konversion von 120 USD

Attribution: Klick 1 = 36 USD, Klick 2 = 24 USD, Klick 3 = 24 USD, Klick 4 = 36 USD (insgesamt 120 USD)

### Beispiele mit sowohl Impressionen als auch Klicks

**Hinweis:** Impressionen können nur in Display- und Social-Media-Anzeigen verwendet werden.

Ereignispfad: Impression 1, Klick 1, Impression 2, Klick 2, Konversion von 120 USD

#### (Nur für Search, Social und Commerce) Verwenden der standardmäßigen Impression Override-Gewichtung von 10 %

Da die Ereignisserie sowohl Impressionen als auch Klicks enthält, gilt die Gewichtung der Impression-Überschreibung für die Impressionen.

Attribution: Impression 1 = 6 USD, Klick 1 = 54 USD, Impression 2 = 6 USD, Klick 2 = 54 USD (insgesamt 120 USD)

#### Verwenden von (nur DSP) kein Impression Override-Gewicht oder (nur Search, Social und Commerce) ein „Impression Override-Gewicht“ von 0 %

Da die Ereignisserie sowohl Impressionen als auch Klicks enthält, werden die Impressionen ignoriert.

Attribution: Impression 1 = 0 USD, Klick 1 = 60 USD, Impression 2 = 0 USD, Klick 2 = 60 USD (insgesamt 120 USD)

### Beispiel mit allen Impressionen

**Hinweis** Es können nur Impressionen für Display-Anzeigen verwendet werden.

Ereignispfad: Impression 1, Impression 2, Impression 3, Impression 4, Konversion von 120 USD

Da es sich bei der Konversion um eine Durchsicht handelt, wird die Durchsichts-Bewertungsmethode - anstelle der Impression Override-Gewichtung - angewendet, um den Wert jeder Impression zu bestimmen:

* Wenn der Berichtsparameter eine gewichtete Durchsichtsgewichtung angegeben hat, wird diese Gewichtung auf die Impressionswerte angewendet. Beispiel: Wenn die Durchsichtsgewichtung 40 % beträgt, klicken Sie auf 1 = 14,40 USD, klicken Sie auf 2 = 9,60 USD, klicken Sie auf 3 = 9,60 USD, klicken Sie auf 4 = 14,40 USD (insgesamt 48 USD)

* Wenn der Berichtsparameter die Verwendung von Rohwerten für Durchsichten angibt, wird der volle 120 USD auf die Impressionen aufgeteilt: Klick 1 = 36 USD, Klick 2 = 24 USD, Klick 3 = 24 USD, Klick 4 = 36 USD (insgesamt 120 USD)

+++

<!-- end examples as collapsible content -->
