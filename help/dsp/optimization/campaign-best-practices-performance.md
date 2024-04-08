---
title: Best Practices für die Einrichtung von Leistungskampagnen
description: Erfahren Sie mehr über Best Practices für die Einrichtung Ihrer leistungsorientierten Kampagnen, darunter Platzierungen, die für den niedrigsten CPA oder den höchsten ROAS optimiert sind.
feature: DSP Optimization, DSP Best Practices
exl-id: bc297796-0c89-4d91-87aa-0668462526ae
source-git-commit: c2c2ddb18b100dc0592d07af3ed1d9f030178eca
workflow-type: tm+mt
source-wordcount: '1273'
ht-degree: 0%

---

# Best Practices für die Einrichtung von Leistungskampagnen

DSP kann leistungsorientierte Kampagnen optimieren. Siehe die folgenden Best Practices für Leistungskampagnen:

* Schritt 1: Definieren des Ziels
* Schritt 2: Definieren der Strategie
* Schritt 3: Erstellen von Paketen
* Schritt 4: Erstellen einer Platzierungsstruktur
* Schritt 5: Verwenden der richtigen Kreativ-Assets

## Schritt 1: Definieren des Ziels

Es ist wichtig, das Ziel der Kampagne zu verstehen, z. B. die höchstmögliche ROAS oder die niedrigstmögliche CPA zu erreichen. Leistungskampagnen haben die folgenden Eigenschaften [Optimierungsziele](/help/dsp/optimization/optimization-goals.md) &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] oder &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)].“ Für jedes Paket in der Kampagne geben Sie das Optimierungsziel entsprechend an.

![Optimierungsziel](/help/dsp/assets/optimization-goals.png)

Außerdem müssen Sie die Erfolgsereignisse ermitteln, die zum Gesamtziel führen, und dementsprechend benutzerdefinierte Ziele erstellen. Für jedes Paket geben Sie ein benutzerdefiniertes Ziel an, das mit dem übergeordneten Optimierungsziel für das Reporting und die algorithmische Optimierung verwendet werden soll, indem Sie Folgendes verwenden [!DNL Adobe Sensei]. Weitere Informationen zum Erstellen benutzerdefinierter Ziele finden Sie unter [Best Practices zum Erstellen eines benutzerdefinierten Ziels](custom-goal.md#custom-goal-best-practices).

![Benutzerdefinierte Ziele](/help/dsp/assets/objective-goals.png)

## Schritt 2: Definieren Sie Ihre Strategie

### Strategien zur Kundenakquise

Obere Trichterpakete enthalten Platzierungen mit sehr breitem Targeting, um neue Verbraucher zu erreichen.

#### Empfohlene Platzierungsstrategien für Interessenten

* Mit den folgenden Taktiken können Sie neue Zielgruppen finden, die wahrscheinlich konvertieren werden:

   * Lookalike-Modellierung über eine Daten-Management-Plattform (DMP) wie Adobe Audience Manager.
   * Verhaltens-Targeting mithilfe von Drittanbieterdaten.
   * Kontextuelles Targeting.
   * Website-/Kategorie-Targeting.

* Verwenden des RON-Targeting (Run of Network): Es ist wichtig, eine Reihe von Netzwerkplatzierungen ohne Zielgruppen-Targeting und mit breitem Inventar-Targeting einzubeziehen. Dies ermöglicht die [!DNL Adobe Sensei] Algorithmus, um wertvolle Benutzer zu finden, die möglicherweise über neuere Cookies verfügen, die noch nicht in eine Zielgruppe kategorisiert wurden.

### Retargeting-Strategien

Untere Trichterpakete enthalten Platzierungen, die auf Benutzende abzielen, die bereits auf der Website des Werbetreibenden waren oder für die der Werbetreibende CRM-Daten hat.

#### Empfohlene Platzierungsstrategien für das Retargeting

* Wenn der Werbetreibende ein Adobe Analytics- oder Adobe Audience Manager-Kunde ist, können Sie Erstanbietersegmente (z. B. Homepage-Besucher, Produktseiten oder Warenkorbabbrüche) erstellen und als Platzierungsziele in DSP verwenden.

* Vermeiden Sie es, einer zielgruppenorientierten Platzierung zu viel Budget zuzuweisen. In der Regel kostet ein Budget von 30 USD pro 1.000 Benutzer und Monat.

## Schritt 3: Erstellen von Paketen

Es empfiehlt sich, separate Pakete für die Prospektion des oberen und des unteren Trichters zu erstellen. Die Optimierung erfolgt auf Paketebene, sodass Leistungsdaten aus allen Platzierungen innerhalb eines Pakets in einem Pool zusammengefasst werden. Gruppieren Sie daher Platzierungen in Paketen mit ähnlicher erwarteter Leistung.

![Beispiel für separate Pakete für die Kundenakquise und das Retargeting](/help/dsp/assets/p-r.png)

Verwenden Sie außerdem die folgenden Einstellungen.

### Ziele und Budget

* **Geschwindigkeit und Begrenzung:** Um ein CPA- oder ROAS-Optimierungsziel auszuwählen, muss das Paket eine Geschwindigkeit auf Paketebene verwenden. Dadurch wird sichergestellt, dass alle Platzierungen innerhalb des Pakets so optimiert sind, dass die Ausgaben auf der Grundlage von Leistung und Skalierung auf die ausgewählten Ziele verteilt werden.

* **Flugdaten:** (Akzeptierte Pakete) Wenn Ihre Kampagne länger als 25 Tage läuft, verwenden Sie den [!UICONTROL Activate Custom Flighting] Funktion. Legen Sie zunächst einen benutzerdefinierten Flug für die ersten 10 Tage auf etwa 75 % des erforderlichen Tagesbudgets fest, um die Ausgaben während des *Lernphase*. Legen Sie dann einen zweiten benutzerdefinierten Flug für den Rest des Budgets fest.

  Wenn Sie beispielsweise 100.000 $ in 30 Tagen ausgeben können, legen Sie das Budget für Flug 1 (Tage 1-10) auf 25.000 $ fest (75 % x 100.000 $/30 Tage = 2.500 $ pro Tag). Verwenden Sie das verbleibende Budget von $75.000 für Flug 2 (Tage 11-30).

* **Budget:** DSP versucht immer, 100 % des Paketbudgets gleichmäßig auf alle Platzierungen in einem Paket aufzuteilen. Wenn eine Platzierung geringe Ausgaben oder keine Ausgaben hat, empfehlen wir eine Budgetbegrenzung für die Platzierung, damit mehr Budget für Platzierungen mit Skalierung zugewiesen werden kann. Warten Sie 24-48 Stunden, bis die Budgetänderungen kalibriert sind.

* **Optimierungsziele:** Verwenden Sie eines der beiden Leistungsoptimierungsziele, *[!UICONTROL Highest Return on Ad Spend]* oder *[!UICONTROL Lowest Cost per Acquisition]*, abhängig vom Paketziel. Diese Ziele optimieren das Paket automatisch in Richtung der höchsten ROAS- bzw. niedrigsten CPA-Platzierungen.

* **Benutzerdefinierte Ziele:**
   * Wenn ein neues Paket dasselbe Ziel wie ein vorhandenes Paket hat, können Sie optional das vorhandene Paket verknüpfen, damit der Algorithmus die vorhandenen Daten für maschinelles Lernen verwenden kann.
   * Geben Sie das entsprechende [!UICONTROL Target CPA] oder [!UICONTROL Target ROAS].

* **Geschwindigkeit und Intraday-Geschwindigkeit:** Wählen Sie für beide Geschwindigkeitstypen *[!UICONTROL Even]* Maximieren Sie Ihre Leistungsziele durch ein gleichmäßiges Tempo an jedem Tag und während des gesamten Fluges.

  >[!CAUTION]
  >
  >Verwenden von *[!UICONTROL FrontLoad]* und *[!UICONTROL Aggressive Front Load]* für Schalt- und *[!UICONTROL ASAP]* Die Geschwindigkeit für die Intraday-Geschwindigkeit wird nur dann festgelegt, wenn Sie die Bereitstellung und die Ausgaben vollständig priorisieren und die Leistungsoptimierung übertreffen, da diese Strategien negative Auswirkungen auf die gewünschten Leistungs-KPIs haben können.

## Schritt 4: Erstellen einer Platzierungsstruktur

Weniger ist mehr. Wenn Sie weniger als sechs Platzierungen pro Paket einrichten können, kann das verfügbare Budget dynamisch zu den Platzierungen mit der besten Leistung verschoben werden.

Stellen Sie außerdem sicher, dass Sie jede Platzierung einem Paket mit dem folgenden Paketzieltyp hinzufügen *[!UICONTROL Prospecting]* oder *[!UICONTROL Retargeting]*, soweit erforderlich.

Im Folgenden finden Sie die empfohlenen Platzierungseinstellungen für Leistungskampagnen.

### Ziele

Sie konfigurieren die CPA- oder ROAS-Optimierung auf Paketebene (siehe Schritt 3 - Erstellen von Paketen), können jedoch zusätzliche Einstellungen auf Platzierungsebene hinzufügen.

* **Max. Angebot:**
   * Verwenden Sie für Interessenten-Platzierungen ein niedriges Maximalangebot ($5).
   * Verwenden Sie für Retargeting-Platzierungen ein hohes Maximalgebot ($12).

* **Pre-Bid-Filter:** Minimieren oder idealerweise vermeiden Sie das Festlegen aggressiver Pre-Bid-Filter, die verhindern, dass die Platzierung eine Skalierung erreicht. Best Practices umfassen Folgendes:

   * Verwenden Sie einen (1) Pre-Bid-Filter pro Platzierung. Mehrere Pre-Bid-Filter erfordern, dass beide erfüllt werden, was die Skalierung reduziert.

   * In Fällen, in denen zusätzliches Targeting (z. B. Zielgruppe, Geografie und Site-Targeting) angewendet wird, sollten Sie ggf. weniger strikte Vorangebotfilter festlegen.

Siehe Beschreibungen zur Verwendung der einzelnen Pre-Bid-Filter unter [Pre-Bid-Filter auf Platzierungsebene und deren Verwendung](/help/dsp/optimization/optimization-pre-bid-filters.md).

### Inventar

Um die Skalierung zu maximieren, verwenden Sie [!UICONTROL Public] (Open Exchange) und [!UICONTROL On Demand] Inventar.

### Site-Targeting

* **[!UICONTROL Traffic Type]**: [!UICONTROL Websites] Nur
* **[!UICONTROL Site Tier]**: [!UICONTROL All sites]

### Zielgruppen-Targeting

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]:**
   * Gruppieren Sie bei Interessenten-Platzierungen ähnliche Zielgruppenkategorien und ähnliche Zielgruppengrößen in einer Platzierung. Führen Sie dann je nach Leistung einen der folgenden Schritte aus:
      * Entfernen Sie nicht leistungsfähige Zielgruppen aus vorhandenen Platzierungen.
      * Verschieben Sie die Zielgruppen mit der besten Leistung an eine separate Platzierung, um die Budgets besser kontrollieren zu können.
   * Für Retargeting-Platzierungen sollten Sie idealerweise ein Zielgruppensegment pro Platzierung einbeziehen, um Gebote und Budgets einfach steuern zu können.

>[!NOTE]
>
>Ihre Anzeigen funktionieren am besten, wenn ein Benutzer nur von einer Platzierung erreicht werden kann. Erhebliche Überschneidungen bei den Benutzenden über Platzierungen hinweg können zu einem Wettbewerb führen, der einen Zyklus kontinuierlich steigender Angebote zur Folge hat, wodurch die Kosten pro Benutzenden steigen. Wenn Sie also mehrere Zielgruppen einbeziehen, stellen Sie sicher, dass sie nicht aus sich überschneidenden Benutzern/Zielgruppenmitgliedern bestehen.
>
> Sie können sich überschneidende Zielgruppen vermeiden, indem Sie Ihre Zielgruppen in Ebenen erstellen, sodass Sie die höheren, inklusiveren Ebenen bei Bedarf von Platzierungen unterdrücken können.

* **[!UICONTROL Frequency Capping]:**
   * Setzen Sie bei der Platzierung von Interessenten enge Häufigkeitsbegrenzungen ein (eine Impression pro Tag).
   * Legen Sie für Retargeting-Platzierungen die primäre Platzierungs-Begrenzung auf 6-10 Impressionen pro Tag und die sekundäre Begrenzung auf eine Impression pro Stunde fest.

* **[!UICONTROL Device Targeting]**:
   * Einschließen [!UICONTROL Computer], [!UICONTROL Mobile], und [!UICONTROL Tablet].
   * Nicht ins Visier nehmen [!UICONTROL Firefox] und [!UICONTROL Safari] aufgrund von Einschränkungen bei Zielgruppenbestimmung und Messung. Weitere Informationen zu erhalten Sie von Ihrem Adobe-Account-Team [!DNL Adobe] Unterstützung für [!DNL Safari ITP].
   * Wenn Sie mobilen Web-Traffic als Ziel wählen, deaktivieren Sie alle mobilen Browser außer [!UICONTROL Chrome] und [!UICONTROL Edge].

### Markensicherheit und Medienqualität

Verwenden von kontextueller Filterung, Blockierung von Betrug vor dem Bid und/oder [!UICONTROL Ads.txt] Durch das Filtern wird der Umfang Ihrer Platzierungen begrenzt, sie werden jedoch bei Bedarf verwendet.

## Schritt 5: Verwenden der richtigen Kreativ-Assets

* Es empfiehlt sich, so viele einzigartige Anzeigengrößen wie möglich einzubeziehen, um die Reichweite zu maximieren. Die universelle Anzeigevorlage ermöglicht das Hochladen beliebiger Standard-Anzeigengrößen.
* Stellen Sie sicher, dass alle Platzierungen Folgendes enthalten *mindestens* Alle primären Anzeigengrößen (300 x 250, 728 x 90, 160 x 600, 300 x 600, 320 x 50 und 300 x 50).
* Aktualisieren Sie Kreative häufig, um kreative Müdigkeit zu vermeiden.

>[!MORELIKETHIS]
>
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
> * [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)
>* [Optimierungsziele und ihre Verwendung](optimization-goals.md)
>* [Pre-Bid-Filter auf Platzierungsebene und deren Verwendung](optimization-pre-bid-filters.md)
>* [Checkliste für den Kampagnenstart](/help/dsp/campaign-management/campaign-launch-checklist.md)
