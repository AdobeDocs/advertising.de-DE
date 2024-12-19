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

# Optimieren von Kampagnen mit Advertising DSP

Auf dieser Seite wird erläutert, wie die DSP-Optimierungs-Engine auf Basis von [!DNL Adobe Sensei] die Kampagnenkits optimiert. Tipps und Tricks zur manuellen Optimierung von Kampagnen erhalten Sie von Ihrem Adobe-Account-Team. <!-- add link to trading playbook if we add it to help -->

Paketoptimierungsziele werden auf zwei Ebenen ausgeführt:

* Für jedes Paket: DSP ordnet Budget für jede Platzierung innerhalb des Pakets basierend auf der Platzierungsleistung gegenüber dem ausgewählten KPI zu.

* Für jede Platzierung/Auktion im Package: DSP berechnet den wirtschaftlichen KPI-Wert in Echtzeit für jede Auktion pro Platzierung und verwendet diesen Wert dann, um das Angebot zu bestimmen.

  >[!NOTE]
  >
  >Der wirtschaftliche Wert kann stark gewichtet werden, je nachdem, wie gut eine Platzierung ausgegeben wird. Wenn eine Platzierung hinter ihrem Ausgabenziel liegt, darf sie minderwertige Auktionen kaufen. Wenn eine Platzierung ihr Ausgabenziel problemlos erreicht, verlagert sich der Fokus auf Auktionen höherer Qualität.

## Paketoptimierung

DSP kann Ihren Versand auf zwei grundlegende Arten optimieren: Es stehen 20 Varianten zur Verfügung, die sich an Ihrem spezifischen Leistungsziel orientieren. Folgende Optionen stehen zur Auswahl:

* Priorisieren der Leistungsrate

* Priorisierung des Ausgleichs zwischen Kosteneffizienz und Leistungsrate

Siehe [Optimierungsziele und ihre Verwendung](optimization-goals.md) um zu bestimmen, welches Optimierungsziel Ihnen beim Erreichen Ihrer KPIs helfen kann.

### Pakete, die die Leistungsrate priorisieren

Bei Optimierungszielen, die die Leistungsrate priorisieren, sagt DSP die Leistung jeder Auktion voraus und bietet immer zum Höchstgebot. Beispiele für anwendbare Optimierungsziele sind [!UICONTROL Highest Viewability Rate], [!UICONTROL Highest Clickthrough Rate] usw.

Dieser Optimierungsmodus funktioniert gut, wenn:

* Sie kennen bereits den effektiven/akzeptablen CPM-Level (z. B. einen historischen Benchmark).

* Sie sind bereit, die [!UICONTROL Max Bid] für jede Platzierung manuell anzupassen, wenn Sie Probleme mit der Skalierung haben.

* Sie priorisieren Größe vor Effizienz.

#### Schrittmacherlogik {#pacing-logic-performance}

* Wenn die Ausgaben im Tempo getätigt werden, wird das Gebot selektiver, sodass Sie nur auf Auktionen bieten, für die hohe Leistungsraten prognostiziert werden.

* Wenn die Ausgaben hinter dem Tempo zurückbleiben, werden Gebote weniger selektiv, sodass Sie auf Auktionen bieten, die voraussichtlich niedrigere Leistungsraten aufweisen, um zum Tempo des Ziels aufzuschließen.

#### Clearing-Preis-/Gebotsschattierung {#clearing-price-performance}

Nach Ausführung der Pacing-Logik führt DSP das vorgeschlagene Gebot über ein Clearing-Preisprognosemodell aus. Wenn die Prognose anzeigt, dass das Angebot mit minimaler Abnahme der Gewinnrate gesenkt werden kann, wird das Angebot gemäß der Prognose verringert.

### Pakete, die den Ausgleich zwischen Kosteneffizienz und Leistungsrate priorisieren

Für einige Optimierungsziele prognostiziert DSP die Leistung jeder Auktion und passt die Gebotspreise automatisch an, wobei die [!UICONTROL Max Bid] einer Platzierung nie überschritten wird. Beispiele für anwendbare Optimierungsziele sind [!UICONTROL Lowest CPM], [!UICONTROL Lowest CPA], [!UICONTROL Lowest Cost per View], [!UICONTROL Lowest Cost per Click] usw.

#### Schrittmacherlogik {#pacing-logic-balanced}

* Wenn die Ausgaben im Tempo getätigt werden, wird das DSP preisempfindlicher und bietet niedrigere Beträge, um die Gewinnquote mit dem Tempo abzuwägen.

* Wenn auch eine Leistungsmetrik ausgeglichen wird (alle Ziele außer [!UICONTROL Lowest CPM]), wird der prognostizierte KPI in den gebotenen Betrag integriert. Sie bieten daher höhere Gebote für Auktionen, bei denen eine höhere Leistung auf der Basis der „Kosten pro“ prognostiziert wird.

* Wenn die Ausgaben im Rückstand sind, wird das DSP weniger preisempfindlich und bietet bis zum [!UICONTROL Max Bid] höhere Summen, um die Gewinnquote mit dem Tempo abzuwägen.

#### Clearing-Preis-/Gebotsschattierung {#clearing-price-balanced}

Nach Ausführung der Pacing-Logik führt DSP das vorgeschlagene Gebot über ein Clearing-Preisprognosemodell aus. Wenn die Prognose anzeigt, dass das Angebot mit minimaler Abnahme der Gewinnrate gesenkt werden kann, wird das Angebot gemäß der Prognose verringert.

## Platzierungsoptimierung

Pre-Bid-Filter für Platzierungen sind die strengste Methode, eine starke Leistung sicherzustellen. DSP verwendet Pre-Bid-Filter strategisch über verschiedene Anzeigentypen hinweg, um Leistungsziele für alle Platzierungen innerhalb jedes Pakets zu erreichen. Sie können Pre-Bid-Filter gleichzeitig mit der Optimierung auf Paketebene oder unabhängig voneinander verwenden.

>[!NOTE]
>
>Die verfügbaren Pre-Bid-Filter variieren je nach Anzeigentyp. Beispielsweise können Sie für eine standardmäßige Anzeigeplatzierung nach Clickthrough-Rate und Sichtbarkeit filtern, jedoch nicht nach Abschlussrate.

Unter [Pre-Bid-Filter auf Platzierungsebene und deren Verwendung](optimization-pre-bid-filters.md) erfahren Sie, welcher Pre-Bid-Filter Ihnen beim Erreichen Ihrer KPIs helfen kann.

>[!MORELIKETHIS]
>
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Optimierungsziele und ihre Verwendung](optimization-goals.md)
>* [Pre-Bid-Filter auf Platzierungsebene und deren Verwendung](optimization-pre-bid-filters.md)
>* [Fehlerbehebung für die Leistung](/help/dsp/optimization/troubleshooting-performance.md)
