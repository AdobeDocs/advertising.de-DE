---
title: Wie DSP Ihre Kampagnen optimiert
description: Erfahren Sie, wie DSP die Pakete in Ihren Kampagnen optimiert.
feature: DSP Optimization
exl-id: 92d411cf-4307-4449-97b4-da3817f2a0b4
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 0%

---

# So optimiert Advertising DSP Ihre Kampagnen

Auf dieser Seite wird beschrieben, wie die von [!DNL Adobe Sensei] unterstützte DSP Optimierungsmodul die Pakete in Ihren Kampagnen optimiert. Tipps und Tricks zur manuellen Kampagnenoptimierung erhalten Sie von Ihrem Adobe-Account-Team. <!-- add link to trading playbook if we add it to help -->

Die Ziele der Paketoptimierung sind auf zwei Ebenen möglich:

* Für jedes Paket: DSP ordnet jeder Platzierung im Paket basierend auf der Leistung der Platzierung im Vergleich zum ausgewählten KPI das Budget zu.

* Für jede Platzierung/Auktion im Paket: DSP berechnet den Echtzeit-KPI-Wert für jede Auktion pro Platzierung und bestimmt dann anhand dieses Werts das Angebot.

  >[!NOTE]
  >
  >Der wirtschaftliche Wert kann stark gewichtet werden, je nachdem, wie gut eine Platzierung ausgegeben wird. Wenn eine Platzierung hinter ihrem Ausgabenziel liegt, darf sie minderwertige Auktionen kaufen. Wenn eine Platzierung ihr Ausgabenziel leicht erreicht, verlagert sich der Fokus auf qualitativ hochwertigere Auktionen.

## Package-Optimierung

DSP können Ihren Versand auf zwei grundlegende Arten optimieren, wobei 20 Varianten zur Verfügung stehen, um ihn an Ihr spezifisches Leistungsziel anzupassen. Sie haben folgende Möglichkeiten:

* Leistungsrate priorisieren

* Kosteneffizienz mit Leistungsrate im Gleichgewicht priorisieren

Siehe [Optimierungsziele und Verwendung dieser Ziele](optimization-goals.md) , um zu bestimmen, welches Optimierungsziel Ihnen beim Erreichen Ihrer KPIs helfen kann.

### Pakete, die die Leistungsrate priorisieren

Für Optimierungsziele, die die Leistungsrate priorisieren, prognostiziert DSP die Leistung jeder Auktion und gibt immer Gebote zum Max. Angebot. Beispiele für anwendbare Optimierungsziele sind [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate] usw.

Dieser Optimierungsmodus funktioniert gut, wenn:

* Sie kennen bereits die effektive/akzeptable CPM-Ebene (z. B. einen historischen Benchmark).

* Sie sind bereit, die [!UICONTROL Max Bid] für jede Platzierung manuell anzupassen, wenn Sie bei der Skalierung Probleme haben.

* Sie priorisieren Skalierung vor Effizienz.

#### Pacing-Logik {#pacing-logic-performance}

* Wenn die Ausgaben im Tempo sind, wird das Bieten selektiver, sodass Sie nur Gebote für Auktionen abgeben, für die hohe Leistungsraten vorhergesagt werden.

* Wenn die Ausgaben hinter dem Tempo zurückbleiben, wird das Bieten weniger selektiv, sodass Sie auf Auktionen bieten, die mit niedrigeren Leistungsraten rechnen, um das Zwischenziel zu erreichen.

#### Löschen von Preis-/Angebotsschattierung {#clearing-price-performance}

Nachdem es die Schrittlogik ausgeführt hat, führt DSP das vorgeschlagene Angebot über ein Prognosemodell für den Clearingpreis aus. Wenn die Prognose anzeigt, dass das Angebot bei minimaler Verringerung auf die Gewinnrate gesenkt werden kann, wird das Angebot gemäß der Prognose reduziert.

### Pakete, die das Gleichgewicht zwischen Kosteneffizienz und Leistungsrate priorisieren

Für einige Optimierungsziele prognostiziert DSP die Leistung jeder Auktion und passt die Gebotspreise automatisch an, wobei die [!UICONTROL Max Bid] einer Platzierung nie überschritten wird. Beispiele für anwendbare Optimierungsziele sind [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click] usw.

#### Schrittweise Logik {#pacing-logic-balanced}

* Wenn die Ausgaben im Tempo sind, wird DSP preissensibler, indem sie niedrigere Beträge anbieten, um die Gewinnrate mit dem Plan auszugleichen.

* Wenn eine Leistungsmetrik ebenfalls ausgeglichen wird (alle Ziele mit Ausnahme von [!UICONTROL Lowest CPM]), wird der prognostizierte KPI mit dem Angebotsbetrag vermischt. Daher bieten Sie höhere Gebote für Auktionen, die auf der Grundlage der &quot;Kosten pro&quot; als leistungsfähiger vorhergesagt werden.

* Wenn die Ausgaben hinter dem Tempo zurückbleiben, wird DSP weniger preisempfindlich und bietet höhere Beträge bis zum [!UICONTROL Max Bid] an, um die Gewinnrate mit dem Plan auszugleichen.

#### Löschen von Preis-/Angebotsschattierung {#clearing-price-balanced}

Nachdem es die Schrittlogik ausgeführt hat, führt DSP das vorgeschlagene Angebot über ein Prognosemodell für den Clearingpreis aus. Wenn die Prognose anzeigt, dass das Angebot bei minimaler Verringerung auf die Gewinnrate gesenkt werden kann, wird das Angebot gemäß der Prognose reduziert.

## Platzierungsoptimierung

Platzierungs-Filter vor dem Gebot sind die strengste Methode, um eine starke Leistung zu gewährleisten. DSP verwendet vorab angebotene Filter strategisch für verschiedene Anzeigentypen, um Leistungsziele über Platzierungen innerhalb der einzelnen Pakete hinweg zu erreichen. Sie können Filter vor dem Angebot gleichzeitig mit der Optimierung auf Paketebene oder unabhängig voneinander verwenden.

>[!NOTE]
>
>Die verfügbaren Vorangebotsfilter variieren je nach Anzeigentyp. Beispielsweise können Sie für eine standardmäßige Anzeigeplatzierung nach Clickthrough- und Sichtbarkeitsrate, aber nicht nach Abschlussrate filtern.

Siehe [Vorab-Angebotsfilter auf Platzierungsebene und Verwendung dieser Filter](optimization-pre-bid-filters.md), um zu bestimmen, welcher Filter vor dem Angebot Ihnen beim Erreichen Ihrer KPIs helfen kann.

>[!MORELIKETHIS]
>
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Optimierungsziele und deren Verwendung](optimization-goals.md)
>* [Vorab-Angebotsfilter auf Platzierungsebene und deren Verwendung](optimization-pre-bid-filters.md)
>* [Fehlerbehebung bei der Leistung](/help/dsp/optimization/troubleshooting-performance.md)
