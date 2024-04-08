---
title: Paketeinstellungen
description: Siehe Beschreibungen der verfügbaren Paketeinstellungen.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 54e8dec0f31d1f18931d12d868ba162879a7acfb
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 0%

---

# Paketeinstellungen

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** Der Paketname. Die maximale Länge beträgt 60 Zeichen.

**[!UICONTROL Description]:** (Optional) Eine Beschreibung des Pakets.

**[!UICONTROL 3rd Party Billed Fees]:** (Optional) Eine statische Drittanbietergebühr, die als nicht fakturierbare Kosten erfasst werden soll:

>[!NOTE]
>
>Fakturierbare Gebühren werden in der [!UICONTROL Net CPM] Metrik.
>
* **[!UICONTROL CPM]:** Die Kosten pro 1000 Impressionen (CPM).

* **[!UICONTROL CPM Description]:** Eine Beschreibung der CPM-Gebühr.

Sie können die Einstellung auf Paketebene unter überschreiben. [Platzierungsebene](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Schreibgeschützt für vorhandene Pakete) Auf welcher Ebene Platzierungen im Paket platziert und begrenzt werden sollen:

* **[!UICONTROL Package level pacing]:** Diese Geschwindigkeits-Strategie arbeitet mit der Geschwindigkeit und Begrenzung aller eingeschlossenen Platzierungen als *Gruppe*. Diese Strategie stellt sicher, dass alle Platzierungen innerhalb eines bestimmten Pakets ganzheitlich optimiert werden, indem die Ausgaben basierend auf Leistung und Skalierung auf ausgewählte wichtige Leistungsindikatoren (KPIs) verteilt werden.

* **[!UICONTROL Placement level pacing]:**  Diese Geschwindigkeits-Strategie arbeitet mit der Geschwindigkeit und Begrenzung aller eingeschlossenen Platzierungen *einzeln*. Es empfiehlt sich, diese Strategie nur zu verwenden, um garantierte private Marktplatzangebote auszuführen.

**[!UICONTROL Flight Dates]:** Start- und Enddatum des Pakets.

Um optional ungleiche Schrittmacherflüge für das Paket zu erstellen, wählen Sie *[!UICONTROL *Activate Custom Flighting]** und richten Sie die benutzerdefinierten Flüge in der [!UICONTROL Flighting] Abschnitt unten. Nachdem Sie benutzerdefinierte Flüge aktiviert und das Paket gespeichert haben, können Sie benutzerdefinierte Flüge nicht mehr deaktivieren.

>[!NOTE]
>
>* Die Flugdaten müssen in den Kampagnenflugdaten enthalten sein. Darüber hinaus müssen die Flugdaten für alle Platzierungen, die diesem Paket zugewiesen sind, in diesen Daten enthalten sein.
> * Sie können das Startdatum des Pakets nicht bearbeiten, wenn benutzerdefinierte Flüge aktiviert sind.

**[!UICONTROL Budget]:** (Nur Pakete mit Geschwindigkeit auf Paketebene) Die Bruttobudgetgrenze und das Budgetintervall.

Bei Paketen mit benutzerdefiniertem Flug ist das Budgetintervall immer *[!UICONTROL All time]*. Geben Sie für Pakete ohne benutzerdefinierte Flüge das Budgetintervall an: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* oder *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Nur Pakete mit Geschwindigkeit auf Paketebene und dynamischem Margin-Management) Die Bruttobudgetgrenze für die Laufzeit des Pakets.

**[!UICONTROL Optimization Goal]:** (Pakete nur mit Geschwindigkeit auf Paketebene) Das Optimierungsziel für das Paket. Beschreibungen der einzelnen Optimierungsziele finden Sie unter [Optimierungsziele und ihre Verwendung](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]:** (Pakete mit dem &quot;[!UICONTROL Highest Return on Ad Spend]&quot; und &quot;[!UICONTROL Lowest Cost per Acquisition]„Nur Optimierungsziele) A [Benutzerdefiniertes Ziel](/help/dsp/optimization/custom-goal.md) Dazu gehören die Umsatz- oder Konversionsereignisse, die zur Berechnung der CPA- oder ROAS-Metrik verwendet werden. Das benutzerdefinierte Ziel kann optional zusätzliche gewichtete Ereignisse im oberen Trichter (wie Seitenbesuche und Hinzufügungen zum Warenkorb) enthalten, die zusätzlich zur CPA- oder ROAS-Metrik für die Paketoptimierung verwendet werden. Weitere Informationen zu den Best Practices für benutzerdefinierte Ziele und Kampagnen, die sie verwenden, finden Sie unter [Best Practices zum Erstellen eines benutzerdefinierten Ziels](/help/dsp/optimization/custom-goal.md#custom-goal-best-practices) und [Best Practices für die Einrichtung von Leistungskampagnen](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Optional) Pakete mit dem &quot;[!UICONTROL Highest Return on Ad Spend]&quot; und &quot;[!UICONTROL Lowest Cost per Acquisition]„Nur Optimierungsziele) Weist das Optimierungsmodell an, nur aus klickbasierten Konversionen zu lernen. Andernfalls lernt das Optimierungsmodell sowohl aus Click- als auch aus Impression-basierten Konversionen.

**[!UICONTROL Conversion Metric]:** (Optional) Pakete mit dem &quot;[!UICONTROL Highest Return on Ad Spend]&quot; und &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; Nur Optimierungsziele) Das endgültige Konversionsereignis (z. B. Anmeldungen) oder Umsatzereignis-/Verkaufsbetrag (z. B. Käufe und Kaufwerte), das zur Berechnung der Rendite auf Werbeausgaben oder der Kosten pro Akquise verwendet werden soll. Wählen Sie aus einer Liste aller primären Ereignisse („Zielmetriken„) aus, die dem ausgewählten benutzerdefinierten Ziel zugeordnet sind. Wenn die Liste leer ist, bearbeiten Sie das benutzerdefinierte Ziel, um mindestens eines der zugrunde liegenden Ereignisse als Zielmetrik einzuschließen.

**[!UICONTROL Package Goal Type]:** (Nur Pakete mit benutzerdefinierten Optimierungszielen) Der Zweck des Pakets. Mit dieser Einstellung können Sie bestimmen, wie das Paket optimiert werden soll:

* *[!UICONTROL Prospecting]:* Interessentenpakete konzentrieren sich auf die Akquise neuer Kunden.

* *[!UICONTROL Retargeting]:* Retargeting-Pakete konzentrieren sich darauf, frühere Besucher oder Kunden erneut verfügbar zu machen.

* *[!UICONTROL Other]:* Alle anderen Zwecke.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Nur Pakete mit benutzerdefinierten Optimierungszielen) Ein weiteres Paket, dessen historische Daten als Eingabe für die Optimierung des Pakets verwendet werden.

**[!UICONTROL Target]:** (Nur Pakete mit Geschwindigkeit auf Paketebene) Das Zielziel, mit dem die Leistung verfolgt wird.

>[!NOTE]
>
>Dieses Feld ist nur ein Benchmark und wird nicht für die Entscheidungsfindung verwendet.

**[!UICONTROL Frequency Cap]:** (Nur Pakete mit Geschwindigkeit auf Paketebene) Die Häufigkeit, mit der ein eindeutiges Gerät oder eine eindeutige Person (abhängig vom angegebenen [!UICONTROL Cross Device Level] für die Kampagne) können Anzeigen aus dem Paket bereitgestellt werden. Zu den Optionen gehören *[!UICONTROL Unlimited]* oder ein bestimmter Betrag pro Tag, Woche oder Monat.

>[!NOTE]
>
>* Sie können Häufigkeitsbegrenzungen auf Kampagnen-, Paket- und Platzierungsebene festlegen. DSP berücksichtigt die strengste Häufigkeitsbegrenzung in der Kampagnenhierarchie.
>* Es empfiehlt sich, Häufigkeitsbegrenzungen sowohl für die Kundenakquise als auch für das Retargeting auf Paketebene festzulegen.
> * Höhere Frequenzlimitierungen führen zu höheren Ausgaben und Impressionen, aber geringerer Reichweite. Niedrigere Frequenzlimits führen zu geringeren Ausgaben und Impressionen, aber höherer Reichweite.

**[!UICONTROL Pace on]:** (Pakete nur mit Geschwindigkeit auf Paketebene) Welche Geschwindigkeit basiert auf:

* *[!UICONTROL Budget]:* (Standard) Diese Option liefert so viele Impressionen wie möglich innerhalb des zugewiesenen Paketbudgets.

* *[!UICONTROL Impressions]:* Diese Option liefert Impressionen, bis innerhalb eines bestimmten Intervalls eine bestimmte Menge erreicht wird. Wenn Sie diese Option wählen, geben Sie die Anzahl der Impressionen und das Intervall an: *Immer,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* oder *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Pakete nur mit Geschwindigkeit auf Paketebene) Anleitung zum Platzieren und Bereitstellen von Nachrichten über den gesamten Flug:

* *[!UICONTROL Even]:* Die Lieferung wird auf jedem Flug einheitlich durchgeführt, mit einem Ziel von 50 % der Lieferung in der ersten Hälfte des Fluges.

* *[!UICONTROL Slightly Ahead]:* (Standard) Beschleunigt den Versand, sodass nach der Hälfte des Flugs 55-65 % abgeschlossen sind.

* *[!UICONTROL Frontload]:* Beschleunigt den Versand, sodass nach der Hälfte des Fluges 65-75 % abgeschlossen sind.

* *[!UICONTROL Aggressive Frontload]:* Beschleunigt den Versand, sodass 75-85 % nach der Hälfte des Fluges abgeschlossen sind.

**[!UICONTROL Intraday pacing]:** (Pakete nur mit Geschwindigkeit auf Paketebene) Wie Sie die Geschwindigkeit und Bereitstellung auf jedem einzelnen Tag innerhalb des Fluges festlegen:

* *[!UICONTROL Even]:* (Standard) Skaliert den Versand anhand der Verfügbarkeit des Bestands. Im Allgemeinen werden mehr Anzeigen pro Stunde am Tag ausgeliefert, wenn das Auktionsvolumen höher ist, und weniger Anzeigen werden morgens und abends ausgeliefert.

* *[!UICONTROL ASAP]:* Beschleunigt den Versand auf die doppelte Geschwindigkeit von *gerade*.

  >[!CAUTION]
  >
  >Diese Option kann sich negativ auf die Leistung auswirken. Verwenden Sie sie nur, wenn Sie die Bereitstellung vollständig priorisieren und die Ausgaben der Leistungsoptimierung vorziehen.

## [!UICONTROL Flighting]

(Pakete mit Geschwindigkeit auf Paketebene und mit &quot;[!UICONTROL Activate Custom Flighting]&quot; aktiviert) Benutzerdefinierte Flugzeiten innerhalb der [!UICONTROL Flight Dates] angegeben in der [!UICONTROL Goals & Budget] -Abschnitt.

Geben Sie für jeden Flug das Start- und Enddatum sowie die Zielanzahl der Impressionen ein. Um einen weiteren Flug hinzuzufügen, klicken Sie auf **[!UICONTROL Add Flight]**.

>[!MORELIKETHIS]
>
>* [Über die Paketverwaltung](package-about.md)
>* [Erstellen eines Pakets](package-create.md)
>* [Bearbeiten eines Pakets](package-edit.md)
>* [Platzierung an Paket anhängen](package-attach-placement.md)
>* [Anzeigen des Änderungsprotokolls für ein Paket](package-change-log.md)
>* [Häufig gestellte Fragen zu Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
