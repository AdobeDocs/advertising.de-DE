---
title: Berechnung der Attributionsregeln
description: Erfahren Sie, wie Adobe Advertising die verschiedenen Arten von Attributionsregeln berechnet.
exl-id: b61561fa-8c01-4989-9ef7-620d2b4c2c0b
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '2439'
ht-degree: 0%

---

# Berechnung der Attributionsregeln für den Adobe Advertising

*Werbetreibende, die nur Adobe Advertising-Konversions-Tracking verwenden*

<!-- Verify statements about cross-device events -->

Die Attributionsregel auf Advertiser-Ebene wird verwendet, um Konversionsdaten - potenziell über mehrere Anzeigenkanäle - in einer Reihe von Ereignissen zu ordnen, die zu einer Konversion führen.

In Berichten, Standardansichten und benutzerdefinierten Ansichten für Advertising Search, Social, &amp; Commerce (Suche, Social und Commerce) und (einige Benutzerrollen) Portfoliosimulationen für Search, Social und Commerce wird die ausgewählte Regel nur für Ansicht-, Berichts- oder Simulationsdaten verwendet. Die verschiedenen Attributionsregeln werden wie folgt angewendet.

>[!NOTE]
>
>* Zuordnungsregeln gelten für Klicks auf gebührenpflichtige Anzeigen in beliebigen Kanälen sowie für Impressionen auf Display- und Social-Anzeigen. Sie gelten nicht für Impressionen für Paid Search-Anzeigen, die nicht auf Ereignisebene verfolgt werden können.
>* Adobe Advertising speichert für jeden Web-Surfer vor einer Konversion immer die folgenden Ereignisse: a) den ersten bezahlten Klick, b) bis zu 10 Klicks für jeden Kanal (Suche, Social oder Anzeige), einschließlich des ersten Klick, und c) bis zu 10 Anzeigenimpressionen. <!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
* In der Advertising-DSP und -Advertising Creative berücksichtigen geräteübergreifende Definitionen nur den Ereignispfad aus der ausgewählten Attributionsregel.<!-- cross-device attribution via LiveRamp only -->
* In Berichten und Verwaltungsansichten hängt die Anzahl der für einen Wert angezeigten Dezimalstellen von der Währung ab, Adobe Advertising speichert jedoch genauere Werte.

## Letztes Ereignis (Standard)

Ordnet die Konversion dem letzten gebührenpflichtigen Klick in der Serie im Advertiser zu. [Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) oder, wenn keine gebührenpflichtigen Klicks aufgetreten sind, zum letzten Impression innerhalb der [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j).

Wenn der Konversion nur Impressionen vorangehen, wird die Konversion als *Durchsicht*, die entweder nach der des Werbetreibenden gewichtet wird [Viewthrough-Gewichtungseinstellung](/help/search-social-commerce/glossary.md#uv) oder — wie angegeben — gemäß der im Bericht, in der Ansicht oder in den benutzerdefinierten Simulationsparametern angegebenen Sichtbarkeitsbewertungsmethode.

![Prozentsätze der letzten Ereigniszuordnung](/help/search-social-commerce/assets/attribution-percent-last-event.png "Prozentsätze der letzten Ereigniszuordnung")

<!-- start examples as collapsible content -->

+++ Beispiele für Ereignisberechnungen

### Beispiel mit allen Klicks

Veranstaltungspfad: Click1, Click2, Click3, Konversion von 120 USD

Die Konversion wird Klicks 3 in Höhe von 120 USD zugeordnet.

### Beispiel mit Impressionen und Klicks

**Hinweis:** Impressionen sind nur auf Display- und Social-Anzeigen anwendbar.

Ereignispfad: Impression 1, Click 1, Impression 2, Konversion von 120 USD

Die Konversion wird Klicks 1 in Höhe von 120 USD zugeordnet.

### Beispiel mit allen Impressionen

**Hinweis:** Es gelten nur Impressionen für Display- und Social-Anzeigen.

Ereignispfad: Impression 1, Impression 2, Impression 3, Konversion von 120 USD

Die Konversion wird Impression 3 zugeordnet. Da es sich bei der Konversion um eine Durchsicht handelt, wird die im Abschnitt &quot;Konversionszuordnung&quot;der Berichtseinstellungen ausgewählte Viewthrough-Bewertungsmethode angewendet:

* Wenn der Berichtsparameter eine gewichtete Durchsichtsgewichtung angibt, wird diese Gewichtung auf die Durchsicht angewendet. Wenn das Durchsichtsgewicht des Werbetreibenden beispielsweise 40 % beträgt, dann 120 USD x 40 % = 48 USD, sodass 48 USD Impression 3 zugeordnet werden.

* Wenn der Berichtsparameter die Verwendung von Rohwerten für Durchsichten angibt, wird keine Durchsichtsgewichtung auf die Durchsicht angewendet und der vollständige Betrag von 120 USD wird Impression 3 zugeordnet.

+++

<!-- end examples as collapsible content -->

## Erstes Ereignis

Ordnet die Konversion dem ersten gebührenpflichtigen Klick in der Reihe innerhalb des Advertisers zu. [Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) oder, wenn keine gebührenpflichtigen Klicks aufgetreten sind, zum ersten Impression innerhalb der [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j). Diese Regel ist nur für Ereignisse auf einzelnen Geräten verfügbar.

Wenn der Konversion nur Impressionen vorangehen, wird die Konversion als *Durchsicht*, die entweder nach der des Werbetreibenden gewichtet wird [Viewthrough-Gewichtungseinstellung](/help/search-social-commerce/glossary.md#uv) oder — wie angegeben — gemäß der im Bericht, in der Ansicht oder in den benutzerdefinierten Simulationsparametern angegebenen Sichtbarkeitsbewertungsmethode.

![Prozentsätze der ersten Ereigniszuordnung](/help/search-social-commerce/assets/attribution-percent-first-event.png "Prozentsätze der ersten Ereigniszuordnung")

<!-- start examples as collapsible content -->

+++ Beispiele für Ereignisberechnungen

### Beispiel mit allen Klicks

Ereignispfad: Klicken Sie auf 1, klicken Sie auf 2, klicken Sie auf 3, Konvertierung von 120 USD

Die Konversion wird Klicks 1 in Höhe von 120 USD zugeordnet.

### Beispiel mit Impressionen und Klicks

**Hinweis:** Impressionen sind nur auf Display- und Social-Anzeigen anwendbar.

Ereignispfad: Impression 1, Click 1, Impression 2, Konversion von 120 USD

Die Konversion wird Klicks 1 in Höhe von 120 USD zugeordnet.

### Beispiel mit allen Impressionen

**Hinweis:** Es gelten nur Impressionen für Display- und Social-Anzeigen.

Ereignispfad: Impression 1, Impression 2, Impression 3, Konversion von 120 USD

Die Konversion wird Impression 1 zugeordnet. Da es sich bei der Konversion um eine Durchsicht handelt, wird die im Abschnitt &quot;Konversionszuordnung (Display-Kampagnen)&quot;der Berichtseinstellungen ausgewählte Durchsichts-Bewertungsmethode angewendet:

* Wenn der Berichtsparameter eine gewichtete Durchsichtsgewichtung angibt, wird diese Gewichtung auf die Durchsicht angewendet. Wenn das Durchsichtsgewicht des Werbetreibenden beispielsweise 40 % beträgt, dann 120 x 40 % = 48 USD, sodass 48 USD Impression 1 zugeordnet werden.

* Wenn der Berichtsparameter die Verwendung von Rohwerten für Durchsichten angibt, wird keine Durchsichtsgewichtung auf die Durchsicht angewendet und der vollständige Betrag von 120 USD wird Impression 1 zugeordnet.

+++

<!-- end examples as collapsible content -->

## Gewichtung des ersten Ereignisses - Mehr

Ordnet die Konversion allen Ereignissen in der Reihe zu, die innerhalb der [Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j), jedoch erhält das erste Ereignis die höchste Gewichtung und die folgenden Ereignisse eine schrittweise geringere Gewichtung. Diese Regel ist nur für Ereignisse auf einzelnen Geräten verfügbar.

Wenn der Konversion nur Impressionen vorangehen, wird die Konversion als *Durchsicht*, die entweder nach der des Werbetreibenden gewichtet wird [Viewthrough-Gewichtungseinstellung](/help/search-social-commerce/glossary.md#uv) oder — wie angegeben — gemäß der im Bericht, in der Ansicht oder in den benutzerdefinierten Simulationsparametern angegebenen Sichtbarkeitsbewertungsmethode.

Wenn der Konversionspfad sowohl gebührenpflichtige Klicks als auch Impressionen enthält, werden die Impressionen von verschiedenen Adobe Advertising-Produkten unterschiedlich behandelt:

* In Search, Social und Commerce wird die [Impressionsübergewicht](/help/search-social-commerce/glossary.md#i-j) - die in der Einstellung für die Impressions-Überschreibung des Werbetreibenden und in Berichten, Ansichten oder benutzerdefinierten Simulationsparametern angegeben ist - wird zuerst auf die Impressionen angewendet.

* In DSP werden die Impressionen ignoriert und nur Klicks gewichtet. DSP berücksichtigt die Gewichtungen für Impressionen bei der Zuordnung nicht.

![Gewichtung der ersten Ereignis- und Zuordnungsprozentsätze](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "Gewichtung der ersten Ereignis- und Zuordnungsprozentsätze")

<!-- start examples as collapsible content -->

+++ Beispiele für Ereignisberechnungen

### Beispiel mit allen Klicks

Ereignispfad: Klicken Sie auf 1, klicken Sie auf 2, klicken Sie auf 3, Konvertierung von 120 USD

Attribution: Klicken Sie auf 1 = 60 USD, klicken Sie auf 2 = 40 USD, klicken Sie auf 3 = 20 USD (insgesamt 120 USD)

### Beispiele mit Impressionen und Klicks

**Hinweis:** Impressionen sind nur auf Display- und Social-Anzeigen anwendbar.

Ereignispfad: Impression 1, Click 1, Impression 2, Click 2, Konversion von 120 USD

#### (Nur Suche, Social und Commerce) Verwendung der standardmäßigen &quot;Impression Override Weight&quot;(Impression Override Weight) von 10 %

Da die Ereignisreihe sowohl Impressionen als auch Klicks enthält, gilt die Gewichtung für Impressionen.

Attribution: Impression 1 = 8 USD, Klick 1 = 72 USD, Impression 2 = 4 USD, Klick 2 = 36 USD (insgesamt 120 USD)

#### Verwendung (nur DSP) eines Impressions-Überschreibungsgewichts von 0 % oder (nur Suche, Social und Commerce) eines &quot;Impressions-Überschreibungsgewichts&quot;

Da die Ereignisreihe sowohl Impressionen als auch Klicks enthält, werden die Impressionen ignoriert.

Attribution: Impression 1 = 0 USD, Klick 1 = 80 USD, Impression 2 = 0 USD, Klick 2 = 40 USD (insgesamt 120 USD)

### Beispiel mit allen Impressionen

**Hinweis:** Es gelten nur Impressionen für Display-Anzeigen.

Ereignispfad: Impression 1, Impression 2, Impression 3, Konversion von 120 USD

Da es sich bei der Konversion um eine Durchsicht handelt, wird zur Bestimmung des Werts jeder Impression die Viewthrough-Bewertungsmethode - und nicht die Impressionsüberschreibungsgewichtung - angewendet:

* Wenn der Berichtsparameter eine gewichtete Durchsichtsgewichtung angegeben hat, wird diese Gewichtung auf die Impressionswerte angewendet. Wenn das Durchsichtsgewicht beispielsweise 40 % beträgt, dann Impression 1 = 24 USD, Impression 2 = 16 USD, Impression 3 = 8 USD (insgesamt 48 USD)

* Wenn der Berichtsparameter die Verwendung von Rohwerten für Durchsichten angibt, wird keine Durchsichtsgewichtung auf die Impression angewendet und der vollständige Betrag von 120 USD wird auf die drei Impressionen aufgeteilt: Impression 1 = 60 USD, Impression 2 = 40 USD, Impression 3 = 20 USD (insgesamt 120 USD)

+++

<!-- end examples as collapsible content -->

## Sogar Distribution

>[!NOTE]
>
>Diese Regel ist nur für Ereignisse auf einzelnen Geräten verfügbar.

Weist die Konversion gleichmäßig jedem Ereignis in der Reihe zu, das innerhalb der [Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j).

Wenn der Konversion nur Impressionen vorangehen, wird die Konversion als *Durchsicht*, die entweder nach der des Werbetreibenden gewichtet wird [Viewthrough-Gewichtungseinstellung](/help/search-social-commerce/glossary.md#uv) oder — wie angegeben — gemäß der im Bericht, in der Ansicht oder in den benutzerdefinierten Simulationsparametern angegebenen Sichtbarkeitsbewertungsmethode.

Wenn der Konversionspfad sowohl gebührenpflichtige Klicks als auch Impressionen enthält, werden die Impressionen von verschiedenen Adobe Advertising-Produkten unterschiedlich behandelt:

* In Search, Social und Commerce wird die [Impressionsübergewicht](/help/search-social-commerce/glossary.md#i-j) - die in der Einstellung für die Impressions-Überschreibung des Werbetreibenden und in Berichten, Ansichten oder benutzerdefinierten Simulationsparametern angegeben ist - wird zuerst auf die Impressionen angewendet.

* In DSP werden die Impressionen ignoriert und nur Klicks gewichtet. DSP berücksichtigt die Gewichtungen für Impressionen bei der Zuordnung nicht.

![Sogar Attributionsprozentsätze](/help/search-social-commerce/assets/attribution-percent-even.png "Sogar Attributionsprozentsätze")

<!-- start examples as collapsible content -->

+++ Beispiele für Ereignisberechnungen

### Beispiel mit allen Klicks

Ereignispfad: Klicken Sie auf 1, klicken Sie auf 2, klicken Sie auf 3, Konvertierung von 120 USD

Keine Impressionen führten zur Konversion, sodass die Gewichtung der Impressionen nicht anwendbar ist und die Konversion gleichmäßig zwischen den drei Klicks aufgeteilt ist:

Attribution: Klicken Sie auf 1 = 40 USD, klicken Sie auf 2 = 40 USD, klicken Sie auf 3 = 40 USD (insgesamt 120 USD)

### Beispiele mit Impressionen und Klicks

**Hinweis:** Impressionen sind nur auf Display- und Social-Anzeigen anwendbar.

Ereignispfad: Impression 1, Click 1, Impression 2, Click 2, Konversion von 120 USD

#### (Nur Suche, Social und Commerce) Verwendung der standardmäßigen &quot;Impression Override Weight&quot;(Impression Override Weight) von 10 %

Da die Ereignisreihe sowohl Impressionen als auch Klicks enthält, gilt die Gewichtung für Impressionen.

Attribution: Impression 1 = 6 USD, Klick 1 = 54 USD, Impression 2 = 6 USD, Klick 2 = 54 USD (insgesamt 120 USD)

#### Verwendung (nur Adobe Advertising DSP) des Werts &quot;Impression Override Weight&quot;oder (nur Suche, Social und Commerce) des Werts &quot;Impression Override Weight&quot;von 0 %

Da die Ereignisreihe sowohl Impressionen als auch Klicks enthält, werden die Impressionen ignoriert.

Attribution: Impression 1 = 0 USD, Klick 1 = 60 USD, Impression 2 = 0 USD, Klick 2 = 60 USD (insgesamt 120 USD)

## Beispiel mit allen Impressionen

**Hinweis:** Es gelten nur Impressionen für Display-Anzeigen.

Ereignispfad: Impression 1, Impression 2, Impression 3, Konversion von 120 USD

Da es sich bei der Konversion um eine Durchsicht handelt, wird zur Bestimmung des Werts jeder Impression die Viewthrough-Bewertungsmethode - und nicht die Impressionsüberschreibungsgewichtung - angewendet:

* Wenn der Berichtsparameter eine gewichtete Durchsichtsgewichtung angegeben hat, wird diese Gewichtung auf die Impressionswerte angewendet. Wenn das Durchsichtsgewicht beispielsweise 40 % beträgt, dann Impression 1 = 16 USD, Impression 2 = 16 USD, Impression 3 = 16 USD (insgesamt 48 USD)

* Wenn der Berichtsparameter die Verwendung von Rohwerten für Durchsichten angibt, wird keine Durchsichtsgewichtung auf die Impression angewendet und der vollständige Betrag von 120 USD wird auf die drei Impressionen aufgeteilt: Impression 1 = 40 USD, Impression 2 = 40 USD, Impression 3 = 40 USD (insgesamt 120 USD)

+++

<!-- end examples as collapsible content -->

## Last Event-Mehr

Ordnet die Konversion allen Ereignissen in der Reihe zu, die innerhalb der [Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j), gibt jedoch dem letzten Ereignis die höchste Gewichtung und den vorhergehenden Ereignissen schrittweise eine geringere Gewichtung.

Wenn der Konversion nur Impressionen vorangehen, wird die Konversion als *Durchsicht*, die entweder nach der des Werbetreibenden gewichtet wird [Viewthrough-Gewichtungseinstellung](/help/search-social-commerce/glossary.md#uv) oder — wie angegeben — gemäß der im Bericht, in der Ansicht oder in den benutzerdefinierten Simulationsparametern angegebenen Sichtbarkeitsbewertungsmethode.

Wenn der Konversionspfad sowohl gebührenpflichtige Klicks als auch Impressionen enthält, werden die Impressionen von verschiedenen Adobe Advertising-Produkten unterschiedlich behandelt:

* In Search, Social und Commerce wird die [Impressionsübergewicht](/help/search-social-commerce/glossary.md#i-j) - die in der Einstellung für die Impressions-Überschreibung des Werbetreibenden und in Berichten, Ansichten oder benutzerdefinierten Simulationsparametern angegeben ist - wird zuerst auf die Impressionen angewendet.

* In DSP werden die Impressionen ignoriert und nur Klicks gewichtet. DSP berücksichtigt die Gewichtungen für Impressionen bei der Zuordnung nicht.

![Gewichtung des letzten Ereignisses - weitere Attributionsprozentsätze](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png "Gewichtung des letzten Ereignisses - weitere Attributionsprozentsätze")

<!-- start examples as collapsible content -->

+++ Beispiele für Ereignisberechnungen

### Beispiel mit allen Klicks

Ereignispfad: Klicken Sie auf 1, klicken Sie auf 2, klicken Sie auf 3, Konvertierung von 120 USD

Attribution: Klicken Sie auf 3 = 60 USD, klicken Sie auf 2 = 40 USD, klicken Sie auf 1 = 20 USD (insgesamt 120 USD)

### Beispiele mit Impressionen und Klicks

**Hinweis:** Impressionen sind nur auf Display- und Social-Anzeigen anwendbar.

Ereignispfad: Impression 1, Click 1, Impression 2, Click 2, Konversion von 120 USD

#### (Nur Suche, Social und Commerce) Verwendung der standardmäßigen &quot;Impression Override Weight&quot;(Impression Override Weight) von 10 %

Da die Ereignisreihe sowohl Impressionen als auch Klicks enthält, gilt die Gewichtung für Impressionen.

Attribution: Impression 1 = 4 USD, Klick 1 = 36 USD, Impression 2 = 8 USD, Klick 2 = 72 USD (insgesamt 120 USD)

#### Verwendung (nur DSP) eines Impressions-Überschreibungsgewichts von 0 % oder (nur Suche, Social und Commerce) eines &quot;Impressions-Überschreibungsgewichts&quot;

Da die Ereignisreihe sowohl Impressionen als auch Klicks enthält, werden die Impressionen ignoriert.

Attribution: Impression 1 = 0 USD, Klick 1 = 40 USD, Impression 2 = 0 USD, Klick 2 = 80 USD (insgesamt 120 USD)

### Beispiel mit allen Impressionen

**Hinweis:** Impressionen sind nur auf Display- und Social-Anzeigen anwendbar.

Ereignispfad: Impression 1, Impression 2, Impression 3, Konversion von 120 USD

Da es sich bei der Konversion um eine Durchsicht handelt, wird zur Bestimmung des Werts jeder Impression die Viewthrough-Bewertungsmethode - und nicht die Impressionsüberschreibungsgewichtung - angewendet:

* Wenn der Berichtsparameter eine gewichtete Durchsichtsgewichtung angegeben hat, wird diese Gewichtung auf die Impressionswerte angewendet. Wenn das Durchsichtsgewicht beispielsweise 40 % beträgt, multiplizieren Sie jeden Wert im &quot;Beispiel mit allen Klicks&quot;mit 40 %: Impression 3 = 24 USD, Impression 2 = 16 USD, Impression 1 = 8 USD (insgesamt 48 USD)

* Wenn der Berichtsparameter die Verwendung von Rohwerten für Durchsichten angibt, wird der volle Betrag von 120 USD zwischen den Impressionen aufgeteilt: Impression 3 = 60 USD, Impression 2 = 40 USD, Impression 1 = 20 USD (insgesamt 120 USD)

+++

<!-- end examples as collapsible content -->

## U-förmig

Ordnet die Konversion allen Ereignissen in der Reihe zu, die innerhalb der [Lookback-Fenster](/help/search-social-commerce/glossary.md#c-d) und [Impression-Lookback-Fenster](/help/search-social-commerce/glossary.md#i-j), gibt jedoch das erste Ereignis und das letzte Ereignis mit der höchsten Gewichtung an, wobei die Ereignisse in der Mitte des Konversionspfads nach und nach weniger berücksichtigt werden.

Wenn der Konversion nur Impressionen vorangehen, wird die Konversion als *Durchsicht*, die entweder nach der des Werbetreibenden gewichtet wird [Viewthrough-Gewichtungseinstellung](/help/search-social-commerce/glossary.md#uv) oder — wie angegeben — gemäß der im Bericht, in der Ansicht oder in den benutzerdefinierten Simulationsparametern angegebenen Sichtbarkeitsbewertungsmethode.

Wenn der Konversionspfad sowohl gebührenpflichtige Klicks als auch Impressionen enthält, werden die Impressionen von verschiedenen Adobe Advertising-Produkten unterschiedlich behandelt:

* In Search, Social und Commerce wird die [Impressionsübergewicht](/help/search-social-commerce/glossary.md#i-j) - die in der Einstellung für die Impressions-Überschreibung des Werbetreibenden und in Berichten, Ansichten oder benutzerdefinierten Simulationsparametern angegeben ist - wird zuerst auf die Impressionen angewendet.

* In DSP werden die Impressionen ignoriert und nur Klicks gewichtet. DSP berücksichtigt die Gewichtungen für Impressionen bei der Zuordnung nicht.

![U-förmige Attributionsprozentsätze](/help/search-social-commerce/assets/attribution-percent-u-shaped.png "U-förmige Attributionsprozentsätze")

<!-- start examples as collapsible content -->

+++ Beispiele für Ereignisberechnungen

### Beispiel mit allen Klicks

Ereignispfad: Klicken Sie auf 1, klicken Sie auf 2, klicken Sie auf 3, klicken Sie auf 4, Konvertierung auf 120 USD

Attribution: Klicken Sie auf 1 = 36 USD, klicken Sie auf 2 = 24 USD, klicken Sie auf 3 = 24 USD, klicken Sie auf 4 = 36 USD (insgesamt 120 USD)

### Beispiele mit Impressionen und Klicks

**Hinweis:** Impressionen sind nur auf Display- und Social-Anzeigen anwendbar.

Ereignispfad: Impression 1, Click 1, Impression 2, Click 2, Konversion von 120 USD

#### (Nur Suche, Social und Commerce) Verwendung der standardmäßigen &quot;Impression Override Weight&quot;(Impression Override Weight) von 10 %

Da die Ereignisreihe sowohl Impressionen als auch Klicks enthält, gilt die Gewichtung für Impressionen.

Attribution: Impression 1 = 6 USD, Klick 1 = 54 USD, Impression 2 = 6 USD, Klick 2 = 54 USD (insgesamt 120 USD)

#### Verwendung (nur DSP) einer Impressionsüberschreibungsgewichtung oder (nur Suche, Social und Commerce) einer &quot;Impressions-Überschreibungsgewichtung&quot;von 0 %

Da die Ereignisreihe sowohl Impressionen als auch Klicks enthält, werden die Impressionen ignoriert.

Attribution: Impression 1 = 0 USD, Klick 1 = 60 USD, Impression 2 = 0 USD, Klick 2 = 60 USD (insgesamt 120 USD)

### Beispiel mit allen Impressionen

**Hinweis:** Es gelten nur Impressionen für Display-Anzeigen.

Ereignispfad: Impression 1, Impression 2, Impression 3, Impression 4, Konversion von 120 USD

Da es sich bei der Konversion um eine Durchsicht handelt, wird zur Bestimmung des Werts jeder Impression die Viewthrough-Bewertungsmethode - und nicht die Impressionsüberschreibungsgewichtung - angewendet:

* Wenn der Berichtsparameter eine gewichtete Durchsichtsgewichtung angegeben hat, wird diese Gewichtung auf die Impressionswerte angewendet. Wenn das Durchsichtsgewicht beispielsweise 40 % beträgt, klicken Sie auf 1 = 14,40 USD, klicken Sie auf 2 = 9,60 USD, klicken Sie auf 3 = 9,60 USD, klicken Sie auf 4 = 14,40 USD (insgesamt 48 USD)

* Wenn der Berichtsparameter die Verwendung von Rohwerten für Durchsichten angibt, wird der volle Betrag von 120 USD zwischen den Impressionen aufgeteilt: Klick 1 = 36 USD, Klick 2 = 24 USD, Klick 3 = 24 USD, Klick 4 = 36 USD (insgesamt 120 USD)

+++

<!-- end examples as collapsible content -->
