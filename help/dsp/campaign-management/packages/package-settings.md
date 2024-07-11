---
title: Paketeinstellungen
description: Siehe Beschreibungen der verfügbaren Paketeinstellungen.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 9a7d73a281dba1331f00dd9ff75fafdc057413d0
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# Paketeinstellungen

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** Der Paketname. Die maximale Länge beträgt 60 Zeichen.

**[!UICONTROL Description]:** (Optional) Eine Beschreibung des Pakets.

**[!UICONTROL 3rd Party Billed Fees]:** (Optional) Eine statische Drittanbietergebühr, die als nicht abrechnungsfähige Kosten verfolgt werden soll:

* **[!UICONTROL CPM]:** Die Kosten pro 1000 Impressionen (CPM).

* **[!UICONTROL Description]:** Beschreibung der CPM-Gebühr.

>[!NOTE]
>
>Abrechenbare Gebühren werden im [!UICONTROL Net CPM] Metrik.

Sie können die Einstellung auf Paketebene auf der [Platzierungsebene](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Schreibgeschützt für vorhandene Pakete) Auf welcher Ebene Platzierungen im Paket platziert und begrenzt werden sollen:

* **[!UICONTROL Package level pacing]:** Diese Schrittstrategie funktioniert durch Geschwindigkeit und Begrenzung aller enthaltenen Platzierungen als *Gruppe*. Diese Strategie stellt sicher, dass alle Platzierungen innerhalb eines Pakets ganzheitlich optimiert werden, indem die Ausgaben auf der Grundlage von Leistung und Skalierung auf ausgewählte KPIs (Key Performance Indicators) verteilt werden.

* **[!UICONTROL Placement level pacing]:**  Diese Schrittstrategie funktioniert durch Geschwindigkeit und Begrenzung aller enthaltenen Platzierungen *einzeln*. Die Best Practice ist, diese Strategie nur zu verwenden, um garantierte private Marktplatzierungen auszuführen.

**[!UICONTROL Flight Dates]:** Das Startdatum und Enddatum des Pakets insgesamt. Die Flugdaten müssen innerhalb der Flugdaten der Kampagne angegeben werden.

>[!NOTE]
>
>* Die Flugdaten für alle Platzierungen, die diesem Package zugewiesen werden, müssen innerhalb dieser Daten enthalten sein.
> * Sie können das Startdatum des Pakets nicht bearbeiten, wenn die benutzerdefinierte Beleuchtung aktiviert ist.

**[!UICONTROL *Activate Custom Flighting]:** Ermöglicht Ihnen die Erstellung von nicht gerade Geschwindigkeitsflügen für das Paket im [!UICONTROL Flighting] unten. Nachdem Sie die benutzerdefinierte Beleuchtung aktiviert und das Paket gespeichert haben, können Sie die benutzerdefinierte Beleuchtung nicht deaktivieren und das Startdatum des Pakets nicht bearbeiten.

**[!UICONTROL Budget]:** (Nur Pakete mit Geschwindigkeit auf Paketebene) Die Obergrenze des Bruttobudgets und das Budgetintervall.

Bei Paketen mit benutzerdefiniertem Flight ist das Budgetintervall immer *[!UICONTROL All time]*. Geben Sie für Pakete ohne benutzerdefinierte Beleuchtung das Budgetintervall an: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* oder *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Nur Pakete mit Geschwindigkeit auf Paketebene und dynamischem Margenmanagement) Die Bruttobudgetsobergrenze für die Dauer des Pakets.

**[!UICONTROL Optimization Goal]:** (Nur Pakete mit Geschwindigkeit auf Paketebene) Das Optimierungsziel für das Paket. Beschreibungen der einzelnen Optimierungsziele finden Sie unter [Optimierungsziele und Verwendung](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]:** (Pakete mit dem[!UICONTROL Highest Return on Ad Spend]&quot; und &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;Nur Optimierungsziele) A [benutzerdefiniertes Ziel](/help/dsp/optimization/custom-goal.md) , das die Umsatz- oder Konversionsereignisse enthält, die zur Berechnung der CPA- oder ROAS-Metrik verwendet werden. Das benutzerdefinierte Ziel kann optional zusätzliche gewichtete obere Trichterereignisse (wie Seitenbesuche und Zusatz zum Warenkorb) enthalten, die zusätzlich zur CPA- oder ROAS-Metrik zur Paketoptimierung verwendet werden. Weitere Informationen zu benutzerdefinierten Zielen, einschließlich Best Practices für die Erstellung für benutzerdefinierte Ziele und Kampagnen, die diese Ziele verwenden, finden Sie unter &quot;[Benutzerdefinierte Ziele](/help/dsp/optimization/custom-goal.md)&quot; und &quot;[Best Practices zum Einrichten von Leistungskampagnen](/help/dsp/optimization/campaign-best-practices-performance.md).&quot;<!-- At some point, all of the objectives will be prefixed with "ADSP_," but probably that won't show up in the Custom Goal list in the DSP UI. -->

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Optional; Pakete mit &quot;[!UICONTROL Highest Return on Ad Spend]&quot; und &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; Nur Optimierungsziele) Weist das Optimierungsmodell an, nur aus klickbasierten Konversionen zu lernen. Andernfalls lernt das Optimierungsmodell sowohl aus Klick- als auch aus impressionsbasierten Konversionen.

**[!UICONTROL Conversion Metric]:** (Optional; Pakete mit &quot;[!UICONTROL Highest Return on Ad Spend]&quot; und &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; Nur Optimierungsziele) Das endgültige Konversionsereignis (z. B. Anmeldungen) oder der Umsatz-/Verkaufsbetrag (z. B. Käufe und Kaufwerte), das zur Berechnung der Rendite aus Werbeausgaben oder der Kosten pro Akquise verwendet wird. Wählen Sie aus einer Liste aller primären Ereignisse (&quot;Zielmetriken&quot;), die dem ausgewählten benutzerdefinierten Ziel zugeordnet sind. Wenn die Liste leer ist, bearbeiten Sie das benutzerdefinierte Ziel, um mindestens eines der zugrunde liegenden Ereignisse als Zielmetrik einzuschließen.

**[!UICONTROL Package Goal Type]:** (Nur Pakete mit benutzerdefinierten Optimierungszielen) Der Zweck des Pakets. Diese Einstellung hilft bei der Bestimmung der Optimierung des Pakets:

* *[!UICONTROL Prospecting]:* Interessante Pakete konzentrieren sich auf die Akquise neuer Kunden.

* *[!UICONTROL Retargeting]:* Retargeting-Pakete konzentrieren sich auf die Wiederbelebung früherer Besucher oder Kunden.

* *[!UICONTROL Other]:* Alle anderen Zwecke.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Nur Pakete mit benutzerdefinierten Optimierungszielen) Ein weiteres Paket, dessen historische Daten als Eingabe für die Optimierung des Pakets verwendet werden.

**[!UICONTROL Target]:** (Nur Pakete mit Geschwindigkeit auf Paketebene) Das Zielziel, das zum Tracking der Leistung verwendet wird.

>[!NOTE]
>
>Dieses Feld ist nur ein Benchmark und wird nicht für die Entscheidungsfindung verwendet.

**[!UICONTROL Frequency Cap]:** (Nur Pakete mit Geschwindigkeit auf Paketebene) Die Häufigkeit, mit der ein eindeutiges Gerät, eine universelle ID oder eine Person (je nach angegebenem [!UICONTROL Cross Device Level] für die Kampagne und die Platzierung [!UICONTROL Targeting] -Einstellung) können Anzeigen aus dem Paket bereitgestellt werden. Optionen umfassen *[!UICONTROL Unlimited]* oder einen bestimmten Betrag pro Tag, Woche oder Monat.

>[!NOTE]
>
>* Sie können Frequenzobergrenzen auf Kampagnen-, Paket- und Platzierungsebene festlegen. DSP respektiert die strengste Frequenzgrenze in der Kampagnenhierarchie.
>* Die Best Practice besteht darin, Frequenzobergrenzen für die Prospektion und Retargeting auf Paketebene festzulegen.
> * Höhere Frequenzobergrenzen führen zu höheren Ausgaben und Impressionen, aber geringerer Reichweite. Niedrigere Frequenzobergrenzen führen zu geringeren Ausgaben und Impressionen, aber zu höherer Reichweite.

**[!UICONTROL Pace on]:** (Nur Pakete mit Pacing auf Paketebene) Worauf basiert:

* *[!UICONTROL Budget]:* (Standard) Diese Option liefert so viele Impressionen wie möglich innerhalb des zugewiesenen Package-Budgets.

* *[!UICONTROL Impressions]:* Diese Option liefert Impressionen, bis eine angegebene Menge innerhalb eines bestimmten Intervalls erreicht wird. Wenn Sie diese Option auswählen, geben Sie die Anzahl der Impressionen und das Intervall an: *Ganzzeit,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* oder *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Nur Pakete mit Geschwindigkeit auf Paketebene) So beschleunigen Sie die Bereitstellung von Anzeigen über den gesamten Flug:

* *[!UICONTROL Even]:* sorgt für eine gleichmäßige Auslieferung während jedes Fluges mit einer Zielvorgabe von 50 % des Versands in der ersten Hälfte des Fluges.

* *[!UICONTROL Slightly Ahead]:* (Standardeinstellung) Beschleunigt den Versand, sodass er 55-65 % vollständig während der gesamten Flugdauer ist.

* *[!UICONTROL Frontload]:* Beschleunigen Sie den Versand, sodass er 65-75 % vollständig während des Fluges ist.

* *[!UICONTROL Aggressive Frontload]:* Beschleunigt den Versand, sodass 75-85 % des gesamten Fluges vollständig sind.

**[!UICONTROL Intraday pacing]:** (Nur Pakete mit Geschwindigkeit auf Paketebene) So beschleunigen Sie die Bereitstellung von Anzeigen über jeden Tag innerhalb des Fluges:

* *[!UICONTROL Even]:* (Standard) Skaliert die Bereitstellung auf der Grundlage der Lagerverfügbarkeit. Im Allgemeinen werden pro Stunde mehr Anzeigen zur Verfügung gestellt, wenn das Auktionsvolumen höher ist, und morgens und abends weniger Anzeigen geliefert.

* *[!UICONTROL ASAP]:* Beschleunigt die Bereitstellung auf die doppelte Geschwindigkeit von *Selbst*.

  >[!CAUTION]
  >
  >Diese Option kann sich negativ auf die Leistung auswirken. Verwenden Sie diese Option nur, wenn Sie die Bereitstellung vollständig priorisieren und die Leistungsoptimierung vorziehen.

## [!UICONTROL Flighting]

(Pakete mit Geschwindigkeit auf Paketebene) Die Flugzeiten des Pauschalangebots, einschließlich benutzerspezifischer Flugzeiten innerhalb der Gesamtdauer [!UICONTROL Flight Dates] für das Paket. Sie können benutzerdefinierte Flüge nur konfigurieren, wenn die Variable [!UICONTROL Activate Custom Flighting] ist in der [!UICONTROL Goals & Budget] Abschnitt.

**[!DNL Flight N]:** (Nur verfügbar, wenn die Variable [!UICONTROL Activate Custom Flighting] -Option aktiviert ist) Geben Sie für jeden Flug das Startdatum, das Enddatum und das Zielausgabenziel an. Um einen weiteren Flug hinzuzufügen, klicken Sie auf **[!UICONTROL Add Flight]**.

Bei vorhandenen Paketen können Sie optional einen Wert in die [!UICONTROL Rollover] Spalte für jeden Flug, um dem nächsten Flug potenziell nicht verbrauchte Mittel hinzuzufügen. Der projizierte Wert im [!UICONTROL Adjusted Goal (Goal + Rollover)] entsprechend geändert.<!-- clarify usage -->

>[!MORELIKETHIS]
>
>* [Über Package Management](package-about.md)
>* [Erstellen eines Pakets](package-create.md)
>* [Bearbeiten eines Pakets](package-edit.md)
>* [Platzierung an ein Paket anhängen](package-attach-placement.md)
>* [Anzeigen des Änderungsprotokolls für ein Paket](package-change-log.md)
>* [Häufig gestellte Fragen zu Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
