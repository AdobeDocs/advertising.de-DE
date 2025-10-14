---
title: Paketeinstellungen
description: Siehe Beschreibungen der verfügbaren Paketeinstellungen.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 26c9c553dbd4086aa114b97dabdf4d9be10cdebe
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# Paketeinstellungen

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** Der Paketname. Die maximale Länge beträgt 60 Zeichen.

**[!UICONTROL Description]:** (Optional) Eine Beschreibung des Pakets.

**[!UICONTROL 3rd Party Billed Fees]:** (Optional) Eine statische Drittanbietergebühr, die als nicht fakturierbare Kosten erfasst werden soll:

* **[!UICONTROL CPM]:** Die Kosten pro 1000 Impressionen (CPM).

* **[!UICONTROL Description]:** Eine Beschreibung der CPM-Gebühr.

>[!NOTE]
>
>Fakturierbare Gebühren werden in der [!UICONTROL Net CPM] Metrik angezeigt.

Sie können die Einstellung auf Paketebene auf [Platzierungsebene“ &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Schreibgeschützt für vorhandene Pakete) Auf welcher Ebene die Platzierungen im Paket platziert und begrenzt werden sollen:

* **[!UICONTROL Package level pacing]:** Diese Geschwindigkeits-Strategie arbeitet mit der Geschwindigkeit und Begrenzung aller eingeschlossenen Platzierungen als *Gruppe*. Diese Strategie stellt sicher, dass alle Platzierungen innerhalb eines bestimmten Pakets ganzheitlich optimiert werden, indem die Ausgaben basierend auf Leistung und Skalierung auf ausgewählte wichtige Leistungsindikatoren (KPIs) verteilt werden.

* **[!UICONTROL Placement level pacing]:** Diese Geschwindigkeits-Strategie arbeitet mit der Geschwindigkeit und Begrenzung aller eingeschlossenen Platzierungen *einzeln*. Es empfiehlt sich, diese Strategie nur zu verwenden, um garantierte private Marktplatzangebote auszuführen.

**[!UICONTROL Flight Dates]:** Das allgemeine Start- und Enddatum des Pakets. Die Flugdaten müssen in den Kampagnenflugdaten enthalten sein.

>[!NOTE]
>
>* Die Flugdaten für alle Platzierungen, die diesem Paket zugewiesen sind, müssen in diesen Daten enthalten sein.
> * Sie können das Startdatum des Pakets nicht bearbeiten, wenn benutzerdefinierte Flüge aktiviert sind.

**[!UICONTROL Activate Custom Flighting]:** Ermöglicht die Erstellung von ungleichmäßigen Schrittweiten für das Paket im [!UICONTROL Flighting] Abschnitt unten. Nachdem Sie benutzerdefinierte Flüge aktiviert und das Paket gespeichert haben, können Sie benutzerdefinierte Flüge nicht mehr deaktivieren und auch das Startdatum des Pakets nicht mehr bearbeiten.

**[!UICONTROL Budget]:** (Pakete nur mit Geschwindigkeit auf Paketebene) Die Bruttobudgetbegrenzung und das Budgetintervall.

Bei Paketen mit benutzerdefiniertem Flug ist das Budgetintervall immer *[!UICONTROL All time]*. Geben Sie für Pakete ohne benutzerdefinierte Flüge das Budgetintervall an: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* oder *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Pakete nur mit Geschwindigkeit auf Paketebene und dynamischer Margin-Verwaltung) Die Bruttobudgetbegrenzung für die Dauer des Pakets.

**[!UICONTROL Optimization Goal]:** (Pakete nur mit Geschwindigkeit auf Paketebene) Das Optimierungsziel für das Paket. Beschreibungen der einzelnen Optimierungsziele finden Sie unter [Optimierungsziele und ihre Verwendung](/help/dsp/optimization/optimization-goals.md).


**[!UICONTROL Link PG Placements for Incremental Reach Optimization]:** (Pakete mit Geschwindigkeit auf Paketebene und nur mit den Optimierungszielen &quot;[!UICONTROL Always Max Bid & Maximize Reach]&quot; und &quot;[!UICONTROL Lowest Cost per Reach]„) Verwendet Haushaltsreichweiten-Daten aus allen programmgesteuerten garantierten Platzierungen in der Kampagne zur Optimierung für die inkrementelle Reichweite.

**[!UICONTROL Custom Goal for Model Learning]:** (Nur Pakete mit den Optimierungszielen &quot;[!UICONTROL Highest Return on Ad Spend]&quot; und &quot;[!UICONTROL Lowest Cost per Acquisition]„) Ein [benutzerdefiniertes Ziel](/help/dsp/optimization/custom-goal.md) das die Umsatz- oder Konversionsereignisse enthält, die zur Berechnung der CPA- oder ROAS-Metrik verwendet werden. Das benutzerdefinierte Ziel muss zusätzliche gewichtete Ereignisse im oberen Trichter (wie Seitenbesuche und Hinzufügungen zum Warenkorb) enthalten, die zusätzlich zur CPA- oder ROAS-Metrik für die Paketoptimierung verwendet werden. Weitere Informationen zu benutzerdefinierten Zielen, einschließlich der Best Practices zum Erstellen benutzerdefinierter Ziele und Kampagnen, die diese verwenden, finden Sie unter &quot;[Benutzerdefinierte Ziele](/help/dsp/optimization/custom-goal.md) und &quot;[Best Practices zum Einrichten von Leistungskampagnen](/help/dsp/optimization/campaign-best-practices-performance.md).“<!-- At some point, all of the objectives will be prefixed with "ADSP_," but probably that won't show up in the Custom Goal list in the DSP UI. -->

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Optional; Pakete mit den Optimierungszielen &quot;[!UICONTROL Highest Return on Ad Spend]&quot; und &quot;[!UICONTROL Lowest Cost per Acquisition]„) Weist das Optimierungsmodell an, nur aus klickbasierten Konversionen zu lernen. Andernfalls lernt das Optimierungsmodell sowohl aus Klicks- als auch aus Impression-basierten Konversionen.

**[!UICONTROL Conversion Metric]:** (Nur Pakete mit den Optimierungszielen &quot;[!UICONTROL Highest Return on Ad Spend]&quot; und &quot;[!UICONTROL Lowest Cost per Acquisition]„) Das endgültige Konversionsereignis (z. B. Anmeldungen) oder Umsatzereignis-/Verkaufsbetrag (z. B. Käufe und Kaufwerte), das für die Berechnung der Rendite auf Werbeausgaben oder der Kosten pro Akquise verwendet werden soll. Wählen Sie aus einer Liste aller primären Ereignisse („Zielmetriken„) aus, die dem ausgewählten benutzerdefinierten Ziel zugeordnet sind. Wenn die Liste leer ist, bearbeiten Sie das benutzerdefinierte Ziel, um mindestens eines der zugrunde liegenden Ereignisse als Zielmetrik einzuschließen.

**[!UICONTROL Package Goal Type]:** (Nur Pakete mit benutzerdefinierten Optimierungszielen) Der Zweck des Pakets. Mit dieser Einstellung können Sie bestimmen, wie das Paket optimiert werden soll:

* *[!UICONTROL Prospecting]:* Akquise-Pakete konzentrieren sich auf die Akquise neuer Kunden.

* *[!UICONTROL Retargeting]:* Retargeting-Pakete konzentrieren sich auf die erneute Offenlegung früherer Besucher oder Kunden.

* *[!UICONTROL Other]:* Alle anderen Zwecke.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Nur Pakete mit benutzerdefinierten Optimierungszielen) Ein weiteres Paket, dessen historische Daten als Eingabe für die Optimierung des Pakets verwendet werden.

**[!UICONTROL Target]:** (Pakete nur mit Geschwindigkeit auf Paketebene) Das Zielziel, mit dem die Leistung verfolgt wird.

>[!NOTE]
>
>Dieses Feld dient nur als Benchmark und wird nicht für Entscheidungen verwendet.

**[!UICONTROL Frequency Cap]:** (Pakete nur mit Geschwindigkeit auf Paketebene) Die Häufigkeit, mit der ein eindeutiges Gerät, eine universelle ID oder eine Person (je nach dem angegebenen [!UICONTROL Cross Device Level] für die Kampagne und der [!UICONTROL Targeting] der Platzierung) aus dem Paket Anzeigen erhalten kann. Zu den Optionen gehören *[!UICONTROL Unlimited]* oder ein bestimmter Betrag pro Tag, Woche oder Monat.

>[!NOTE]
>
>* Sie können Häufigkeitsbegrenzungen auf Kampagnen-, Paket- und Platzierungsebene festlegen. DSP berücksichtigt die strengste Häufigkeitsbegrenzung in der Kampagnenhierarchie.
>* Es empfiehlt sich, Häufigkeitsbegrenzungen sowohl für die Kundenakquise als auch für das Retargeting auf Paketebene festzulegen.
> * Höhere Frequenzlimitierungen führen zu höheren Ausgaben und Impressionen, aber geringerer Reichweite. Niedrigere Frequenzlimitierungen führen zu geringeren Ausgaben und Impressionen, aber höherer Reichweite.

**[!UICONTROL Pace on]:** (Pakete nur mit Geschwindigkeit auf Paketebene) Worauf basiert die Geschwindigkeit:

* *[!UICONTROL Budget]:* (Standard) Diese Option liefert so viele Impressionen wie möglich innerhalb des zugewiesenen Paketbudgets.

* *[!UICONTROL Impressions]:* Diese Option liefert Impressionen, bis innerhalb eines bestimmten Intervalls eine bestimmte Menge erreicht wird. Wenn Sie diese Option wählen, geben Sie die Anzahl der Impressionen und das Intervall an: *Gesamte Zeit,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* oder *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Pakete nur mit Geschwindigkeit auf Paketebene) Anleitung zum Platzieren der Anzeigenbereitstellung auf dem gesamten Flug:

* *[!UICONTROL Even]:* Die Lieferung wird auf jedem Flug einheitlich durchgeführt, wobei 50 % der Lieferung in der ersten Hälfte des Fluges erfolgen soll.

* *[!UICONTROL Slightly Ahead]:* (Standard) Beschleunigt die Zustellung, sodass nach der Hälfte der Flugdauer 55-65 % abgeschlossen sind.

* *[!UICONTROL Frontload]:* Beschleunigt die Lieferung, sodass nach der Hälfte des Fluges 65-75 % abgeschlossen sind.

* *[!UICONTROL Aggressive Frontload]:* Beschleunigt die Lieferung, sodass nach der Hälfte des Fluges 75-85 % abgeschlossen sind.

**[!UICONTROL Intraday pacing]:** (Pakete nur mit Geschwindigkeit auf Paketebene) Schrittweise Platzierung der Anzeigenbereitstellung an jedem Tag innerhalb des Fluges:

* *[!UICONTROL Even]:* (Standard) Skaliert die Bereitstellung auf der Grundlage der Verfügbarkeit des Bestands. Im Allgemeinen werden mehr Anzeigen pro Stunde am Tag ausgeliefert, wenn das Auktionsvolumen höher ist, und weniger Anzeigen werden morgens und abends ausgeliefert.

* *[!UICONTROL ASAP]:* Beschleunigt den Versand auf die doppelte Geschwindigkeit von *Gleichmäßig*.

  >[!CAUTION]
  >
  >Diese Option kann sich negativ auf die Leistung auswirken. Verwenden Sie sie nur, wenn Sie die Bereitstellung vollständig priorisieren und die Ausgaben der Leistungsoptimierung vorziehen.

## [!UICONTROL Flighting]

(Pakete mit Geschwindigkeit auf Paketebene) Die Flugzeiten des Pakets, einschließlich benutzerdefinierter Flugzeiten innerhalb der [!UICONTROL Flight Dates] für das Paket. Sie können benutzerdefinierte Flüge nur konfigurieren, wenn die Option [!UICONTROL Activate Custom Flighting] im Abschnitt [!UICONTROL Goals & Budget] aktiviert ist.

**[!UICONTROL Automatically rollover remaining flight budget to next flight]:** (nur verfügbar, wenn die Option [!UICONTROL Activate Custom Flighting] aktiviert ist) Fügt automatisch alle verbleibenden Budgets aus dem vorherigen Flug zum vorhandenen Budget für den nächsten Flug hinzu.

In der Ansicht [!UICONTROL Packages] und der Ansicht [!DNL Package Name] > [!UICONTROL Flights] enthält das Feld [!UICONTROL Interval Goal] , das das aktuelle Flugziel anzeigt, jedes Rollover-Budget.

**[!DNL Flight N]:** (nur verfügbar, wenn die Option &quot;[!UICONTROL Activate Custom Flighting]&quot; aktiviert ist) Geben Sie für jeden Flug das Startdatum, das Enddatum und das Ziel der Ausgaben an. Um einen weiteren Flug hinzuzufügen, klicken Sie auf **[!UICONTROL Add Flight]**.

Bei bestehenden Paketen, bei denen die Option &quot;[!UICONTROL Automatically rollover remaining flight budget to next flight]&quot; nicht aktiviert ist, können Sie optional die Einstellungen erneut öffnen, um für jeden Flug einen Wert in der Spalte &quot;**[!UICONTROL Rollover]**&quot; einzugeben, um dem nächsten Flug potenziell nicht ausgegebenes Budget hinzuzufügen.

>[!MORELIKETHIS]
>
>* [Über die Paketverwaltung](package-about.md)
>* [Erstellen eines Pakets](package-create.md)
>* [Bearbeiten eines Pakets](package-edit.md)
>* [Platzierung an Paket anhängen](package-attach-placement.md)
>* [Anzeigen des Änderungsprotokolls für ein Paket](package-change-log.md)
>* [FAQs zu Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
