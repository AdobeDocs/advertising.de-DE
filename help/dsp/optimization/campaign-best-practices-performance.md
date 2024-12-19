---
title: Best Practices für das Einrichten von Leistungskampagnen
description: Erfahren Sie mehr über die Best Practices für die Einrichtung Ihrer leistungsorientierten Kampagnen, zu denen Platzierungen gehören, die für den niedrigsten CPA oder den höchsten ROAS optimiert sind.
feature: DSP Optimization, DSP Best Practices
exl-id: bc297796-0c89-4d91-87aa-0668462526ae
source-git-commit: 802c75920bb11f262cbe0d76d2554971aaf35831
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 0%

---

# Best Practices für das Einrichten von Leistungskampagnen

DSP kann leistungsorientierte Kampagnen optimieren. Siehe die folgenden Best Practices für Leistungskampagnen:

* Schritt 1: Definieren des Ziels
* Schritt 2: Definieren der Strategie
* Schritt 3: Erstellen von Paketen
* Schritt 4: Erstellen der Platzierungsstruktur
* Schritt 5: Verwenden der richtigen Creative Assets

## Schritt 1: Definieren des Ziels

Es ist wichtig, das Ziel der Kampagne zu verstehen, z. B. die höchstmögliche ROAS oder die niedrigstmögliche CPA zu erreichen. Leistungskampagnen haben die [Optimierungsziele](/help/dsp/optimization/optimization-goals.md) &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"]&quot; oder &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;. Geben Sie für jedes Paket in der Kampagne das entsprechende Optimierungsziel an.

![Optimierungsziel](/help/dsp/assets/optimization-goals.png)

Sie müssen auch die Erfolgsereignisse ermitteln, die zum Gesamtziel führen, und dementsprechend benutzerdefinierte Ziele erstellen. Geben Sie für jedes Paket ein benutzerdefiniertes Ziel an, das mit dem übergeordneten Optimierungsziel für die Berichterstellung und algorithmische Optimierung mithilfe von [!DNL Adobe Sensei] verwendet werden soll. Weitere Informationen zum Erstellen benutzerdefinierter Ziele, einschließlich Best Practices, finden Sie unter [Benutzerdefinierte Ziele](custom-goal.md).

## Schritt 2: Definieren Sie Ihre Strategie

### Strategien zur Kundenakquise

Obere Trichterpakete enthalten Platzierungen mit sehr breitem Targeting, um neue Kunden zu erreichen.

#### Empfohlene Platzierungsstrategien für Interessenten

* Mit den folgenden Taktiken können Sie neue Zielgruppen finden, die wahrscheinlich konvertieren werden:

   * Lookalike-Modellierung über eine Datenverwaltungsplattform (DMP) wie Adobe Audience Manager.
   * Verhaltens-Targeting mithilfe von Drittanbieterdaten.
   * Kontextuelles Targeting.
   * Website-/Kategorie-Targeting.

* Verwenden des RON-Targeting (Run of Network): Es ist wichtig, eine Reihe von Netzwerkplatzierungen ohne Zielgruppen-Targeting und mit breitem Inventar-Targeting einzubeziehen. Auf diese Weise kann der [!DNL Adobe Sensei]-Algorithmus wertvolle Benutzer finden, die möglicherweise über neuere Cookies verfügen, die noch nicht in eine Zielgruppe kategorisiert wurden.

### Retargeting-Strategien

Untere Trichterpakete enthalten Platzierungen, die auf Benutzende abzielen, die bereits auf der Web-Seite des Werbetreibenden waren oder für die der Werbetreibende CRM-Daten hat.

#### Empfohlene Platzierungsstrategien für das Retargeting

* Wenn der Advertiser Adobe Analytics- oder Adobe Audience Manager-Kunde ist, können Sie Erstanbietersegmente (z. B. Homepage-Besucher, Produktseiten oder Warenkorbabbrüche) erstellen und als Platzierungsziele in DSP verwenden.

* Vermeiden Sie es, einer zielgruppenorientierten Platzierung zu viel Budget zuzuweisen. Im Allgemeinen kostet ein Budget von 30 USD pro 1.000 Benutzer und Monat.

## Schritt 3: Erstellen von Paketen

Es empfiehlt sich, separate Pakete für die Prospektion des oberen und des unteren Trichters zu erstellen. Die Optimierung erfolgt auf Paketebene, sodass Leistungsdaten aus allen Platzierungen innerhalb eines Pakets in Pools zusammengefasst werden. Gruppieren Sie daher Platzierungen in Paketen mit ähnlicher erwarteter Leistung.

![Beispiel für separate Pakete für die Prospektion und das Retargeting](/help/dsp/assets/p-r.png)

Verwenden Sie außerdem die folgenden Einstellungen.

### Ziele und Budget

* **Pacing und Begrenzung:** Um ein CPA- oder ROAS-Optimierungsziel auszuwählen, muss das Paket eine Geschwindigkeit auf Paketebene verwenden. Dadurch wird sichergestellt, dass alle Platzierungen innerhalb des Pakets so optimiert sind, dass die Ausgaben anhand von Leistung und Skalierung auf die ausgewählten Ziele verteilt werden.

* **Flugdaten:** (Interessenten-Pakete) Wenn Ihre Kampagne länger als 25 Tage läuft, verwenden Sie die [!UICONTROL Activate Custom Flighting]. Legen Sie zunächst einen benutzerdefinierten Flug für die ersten 10 Tage auf etwa 75 % des erforderlichen Tagesbudgets fest, um die Ausgaben während der *Lernphase“* reduzieren. Legen Sie dann einen zweiten benutzerdefinierten Flug für den Rest des Budgets fest.

  Wenn Sie beispielsweise 100.000 $ in 30 Tagen ausgeben können, legen Sie das Budget für Flug 1 (Tage 1-10) auf 25.000 $ fest (75 % x 100.000 $/30 Tage = 2.500 $ pro Tag). Verwenden Sie das verbleibende Budget von $75.000 für Flug 2 (Tage 11-30).

* **Budget:** DSP versucht immer, 100 % des Paketbudgets gleichmäßig auf alle Platzierungen in einem Paket aufzuteilen. Wenn eine Platzierung geringe Ausgaben oder keine Ausgaben hat, empfehlen wir eine Budgetbegrenzung für die Platzierung, damit mehr Budget für Platzierungen mit Skalierung zugewiesen werden kann. Warten Sie 24-48 Stunden, bis die Budgetänderungen kalibriert sind.

* **Optimierungsziele:** Verwenden Sie je nach Paketziel eines der beiden Leistungsoptimierungsziele, *[!UICONTROL Highest Return on Ad Spend]* oder *[!UICONTROL Lowest Cost per Acquisition]*. Diese Ziele optimieren das Paket automatisch entsprechend den höchsten ROAS- bzw. niedrigsten CPA-Platzierungen.

* **Benutzerdefinierte Ziele:**
   * Wenn ein neues Paket dasselbe Ziel wie ein vorhandenes Paket hat, können Sie optional das vorhandene Paket verknüpfen, damit der Algorithmus die vorhandenen Daten für maschinelles Lernen verwenden kann.
   * Geben Sie die entsprechende [!UICONTROL Target CPA] oder [!UICONTROL Target ROAS] ein.

* **Schalt- und Intraday-Geschwindigkeit:** Wählen Sie für beide Arten der Geschwindigkeit *[!UICONTROL Even]* aus, um Ihre Leistungsziele zu maximieren, indem Sie während jedes Tages und über den gesamten Flug gleichmäßig am Tempo arbeiten.

  >[!CAUTION]
  >
  >Verwenden Sie *[!UICONTROL FrontLoad]* und *[!UICONTROL Aggressive Front Load]* für Schalt- und *[!UICONTROL ASAP]*-Geschwindigkeit nur dann für die Intraday-Geschwindigkeit, wenn Sie die Bereitstellung vollständig priorisieren und die Ausgaben der Leistungsoptimierung vorziehen, da diese Strategien sich negativ auf die gewünschten Leistungs-KPIs auswirken können.

## Schritt 4: Erstellen der Platzierungsstruktur

Weniger ist mehr. Wenn Sie weniger als sechs Platzierungen pro Paket einrichten können, kann das verfügbare Budget dynamisch zu den Platzierungen mit der besten Leistung verschoben werden.

Stellen Sie außerdem sicher, dass Sie jede Platzierung einem Paket mit dem Package-Zieltyp *[!UICONTROL Prospecting]* oder *[!UICONTROL Retargeting]* hinzufügen.

Im Folgenden finden Sie die empfohlenen Platzierungseinstellungen für Leistungskampagnen.

### Ziele

Sie müssen die CPA- oder ROAS-Optimierung auf Paketebene konfigurieren (siehe Schritt 3 - Erstellen von Paketen), Sie können jedoch zusätzliche Einstellungen auf Platzierungsebene hinzufügen.

* **Max. Angebot:**
   * Nutzen Sie für Interessenten-Platzierungen ein niedriges Maximalgebot ($5).
   * Verwenden Sie für Retargeting-Platzierungen ein hohes Maximalgebot ($12).

* **Pre-Bid-Filter:** Minimieren oder idealerweise vermeiden Sie das Festlegen aggressiver Pre-Bid-Filter, die verhindern, dass die Platzierung eine Skalierung erreicht. Best Practices umfassen Folgendes:

   * Verwenden Sie einen (1) Pre-Bid-Filter pro Platzierung. Die Verwendung mehrerer Pre-Bid-Filter erfordert, dass beide erfüllt werden, was die Skalierung reduziert.

   * In Fällen, in denen zusätzliches Targeting (z. B. Zielgruppe, Geografie und Site-Targeting) angewendet wird, sollten Sie ggf. weniger strikte Filter vor dem Bid festlegen.

Siehe Beschreibungen der Verwendung der einzelnen Pre-Bid-Filter auf [Platzierungsebene Pre-Bid-Filter und deren Verwendung](/help/dsp/optimization/optimization-pre-bid-filters.md).

### Inventar

Um die Skalierung zu maximieren, verwenden Sie [!UICONTROL Public] (Open Exchange) und [!UICONTROL On Demand] Inventar.

### Site-Targeting

* **[!UICONTROL Traffic Type]**: nur [!UICONTROL Websites]
* **[!UICONTROL Site Tier]**: [!UICONTROL All sites]

### Zielgruppen-Targeting

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]:**
   * Gruppieren Sie bei Interessenten-Platzierungen ähnliche Zielgruppenkategorien und ähnliche Zielgruppengrößen in einer Platzierung. Führen Sie dann je nach Leistung einen der folgenden Schritte aus:
      * Entfernen Sie Zielgruppen mit geringer Leistung aus vorhandenen Platzierungen.
      * Verschieben Sie die Zielgruppen mit der besten Leistung an eine separate Platzierung, um die Budgets besser kontrollieren zu können.
   * Bei Retargeting-Platzierungen sollten Sie idealerweise ein Zielgruppensegment pro Platzierung einbeziehen, um Gebote und Budgets einfach zu steuern.

>[!NOTE]
>
>Ihre Anzeigen funktionieren am besten, wenn ein Benutzer nur von einer Platzierung erreicht werden kann. Signifikante Überschneidungen bei den Benutzenden über Platzierungen hinweg können zu einem Wettbewerb führen, der einen Zyklus kontinuierlich steigender Gebote zur Folge hat, wodurch die Kosten pro Benutzenden in die Höhe getrieben werden. Wenn Sie also mehrere Zielgruppen einbeziehen, stellen Sie sicher, dass sie nicht aus sich überschneidenden Benutzern/Zielgruppenmitgliedern bestehen.
>
> Sie können sich überschneidende Zielgruppen vermeiden, indem Sie Ihre Zielgruppen in Ebenen erstellen, sodass Sie die höheren, inklusiveren Ebenen bei Bedarf aus Platzierungen unterdrücken können.

* **[!UICONTROL Frequency Capping]:**
   * Setzen Sie bei Interessenten-Platzierungen enge Frequenzlimits (eine Impression pro Tag) ein.
   * Legen Sie für Retargeting-Platzierungen die primäre Platzierungsbegrenzung auf 6-10 Impressionen pro Tag und die sekundäre Begrenzung auf eine Impression pro Stunde fest.

* **[!UICONTROL Device Targeting]**:
   * [!UICONTROL Computer], [!UICONTROL Mobile] und [!UICONTROL Tablet] einschließen.
   * [!UICONTROL Firefox] und [!UICONTROL Safari] aufgrund von Einschränkungen bei Zielgruppenbestimmung und Messung nicht als Ziel auswählen. Wenden Sie sich an Ihr Adobe-Account-Team , um weitere Informationen zum [!DNL Adobe]-Support für [!DNL Safari ITP] zu erhalten.
   * Wenn Sie mobilen Web-Traffic als Ziel wählen, deaktivieren Sie alle mobilen Browser mit Ausnahme von [!UICONTROL Chrome] und [!UICONTROL Edge].

### Markensicherheit und Medienqualität

Durch die Verwendung von kontextueller Filterung, die Blockierung von Betrug vor dem Bid und/oder die [!UICONTROL Ads.txt] Filterung wird der Umfang Ihrer Platzierungen begrenzt. Sie können diese jedoch bei Bedarf verwenden.

## Schritt 5: Verwenden der richtigen Creative Assets

* Es empfiehlt sich, so viele einzigartige Anzeigengrößen wie möglich einzubeziehen, um die Reichweite zu maximieren. Mit der universellen Anzeigevorlage können Sie eine beliebige standardmäßige Anzeigegröße hochladen.
* Stellen Sie sicher, dass alle Platzierungen *mindestens* alle primären Anzeigengrößen (300x250, 728x90, 160x600, 300x600, 320x50 und 300x50) enthalten.
* Aktualisieren Sie Kreative häufig, um kreative Müdigkeit zu vermeiden.

>[!MORELIKETHIS]
>
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
> * [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)
>* [Optimierungsziele und ihre Verwendung](optimization-goals.md)
>* [Pre-Bid-Filter auf Platzierungsebene und deren Verwendung](optimization-pre-bid-filters.md)
>* [Checkliste für den Kampagnenstart](/help/dsp/campaign-management/campaign-launch-checklist.md)
