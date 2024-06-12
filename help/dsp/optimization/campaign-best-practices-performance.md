---
title: Best Practices zum Einrichten von Leistungskampagnen
description: Lernen Sie Best Practices für die Einrichtung Ihrer leistungsorientierten Kampagnen kennen, darunter Platzierungen, die für den niedrigsten CPA oder den höchsten ROAS optimiert sind.
feature: DSP Optimization, DSP Best Practices
exl-id: bc297796-0c89-4d91-87aa-0668462526ae
source-git-commit: 802c75920bb11f262cbe0d76d2554971aaf35831
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 0%

---

# Best Practices zum Einrichten von Leistungskampagnen

DSP können Ihre leistungsorientierten Kampagnen optimieren. Siehe die folgenden Best Practices für Leistungskampagnen:

* Schritt 1: Definieren Sie Ihr Ziel
* 2. Schritt - Strategie definieren
* Schritt 3: Erstellen von Paketen
* Schritt 4: Erstellen einer Platzierungsstruktur
* Schritt 5: Verwenden der richtigen kreativen Assets

## Schritt 1: Definieren Ihres Ziels

Es ist wichtig, das Ziel der Kampagne zu verstehen, z. B. das höchstmögliche ROAS oder den niedrigstmöglichen CPA zu erreichen. Leistungskampagnen verfügen über [Optimierungsziele](/help/dsp/optimization/optimization-goals.md) &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] oder &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)].&quot; Geben Sie für jedes Kampagnenkit das Optimierungsziel entsprechend an.

![Optimierungsziel](/help/dsp/assets/optimization-goals.png)

Sie müssen auch die Erfolgsereignisse bestimmen, die zum Gesamtziel führen, und benutzerdefinierte Ziele entsprechend erstellen. Geben Sie für jedes Paket ein benutzerdefiniertes Ziel an, das mit dem übergeordneten Optimierungsziel für die Berichterstellung und algorithmische Optimierung verwendet werden soll, indem Sie [!DNL Adobe Sensei]. Weitere Informationen zum Erstellen benutzerdefinierter Ziele, einschließlich Best Practices, finden Sie unter [Benutzerdefinierte Ziele](custom-goal.md).

## 2. Schritt - Strategie definieren

### Prognosestrategien

Obertrichter-Pakete enthalten Platzierungen mit sehr breitem Targeting, um neue Nettonutzer zu erreichen.

#### Empfohlene Platzierungsstrategien für die Vorschau

* Suchen Sie mithilfe der folgenden Taktik nach neuen Zielgruppen, die wahrscheinlich konvertiert werden:

   * Look-alike-Modellierung aus einer Datenverwaltungsplattform (DMP), z. B. Adobe Audience Manager.
   * Behavioral Targeting mit Daten von Drittanbietern.
   * Kontextuelles Targeting.
   * Site-/Kategorie-Targeting.

* Verwenden des Netzwerk-Targeting (RON): Es ist wichtig, eine Netzwerkplatzierung ohne Zielgruppen-Targeting und mit einem umfassenden Inventar-Targeting einzubeziehen. Dies ermöglicht die [!DNL Adobe Sensei] verwenden, um wertvolle Benutzer zu finden, die möglicherweise neuere Cookies haben, die noch nicht in eine Zielgruppe kategorisiert wurden.

### Retargeting-Strategien

Niedrigere Trichterpakete enthalten Platzierungen, die Benutzer ansprechen, die bereits auf der Webseite des Advertisers waren oder für die der Advertiser CRM-Daten hat.

#### Empfohlene Platzierungsstrategien für Retargeting

* Wenn der Advertiser Adobe Analytics- oder Adobe Audience Manager-Kunde ist, können Sie Erstanbietersegmente (wie Startseitenbesucher, Produktseiten oder Warenkorbabbrüche) erstellen und diese als Platzierungsziele in DSP verwenden.

* Vermeiden Sie es, einer zielgruppenorientierten Platzierung zu viel Budget zuzuweisen. In der Regel können Sie ein Budget von 30 $ pro 1.000 Benutzer pro Monat festlegen.

## Schritt 3: Erstellen von Paketen

Die Best Practice besteht darin, separate Pakete für die Prospektion des oberen Trichters und für das Retargeting des unteren Trichters zu erstellen. Die Optimierung erfolgt auf Paketebene, sodass Leistungsdaten aus allen Platzierungen innerhalb eines Pakets gepoolt werden. Gruppieren Sie daher Platzierungen in Paketen mit einer ähnlichen erwarteten Leistung.

![Beispiel für separate Pakete für Prospektion und Retargeting](/help/dsp/assets/p-r.png)

Verwenden Sie außerdem die folgenden Einstellungen.

### Ziele und Budget

* **Platzierung und Begrenzung:** Um ein CPA- oder ROAS-Optimierungsziel auszuwählen, muss das Paket Geschwindigkeit auf Paketebene verwenden. Dadurch wird sichergestellt, dass alle Platzierungen im Paket so optimiert sind, dass Ausgaben basierend auf Leistung und Skalierung an die ausgewählten Ziele verteilt werden.

* **Flugdaten:** (Angebote) Wenn Ihre Kampagne länger als 25 Tage läuft, verwenden Sie die Variable [!UICONTROL Activate Custom Flighting] Funktion. Legen Sie zunächst einen benutzerdefinierten Flug für die ersten 10 Tage auf ca. 75 % des Tagesbudgets fest, um die Ausgaben während der *Lernphase*. Legen Sie dann einen zweiten benutzerdefinierten Flug für den Rest des Budgets fest.

  Wenn Sie beispielsweise über 100.000 USD für 30 Tage verfügen, legen Sie das Budget für Flug 1 (Tage 1-10) auf 25.000 USD fest (75 % x 100.000/30 Tage = 2.500 USD pro Tag). Verwenden Sie das restliche Budget von 75.000 $ für Flug 2 (Tage 11-30).

* **Budget:** DSP versucht immer, 100 % des Package-Budgets gleichmäßig zwischen allen Platzierungen in einem Paket zuzuweisen. Wenn eine Platzierung geringe Ausgaben oder keine Ausgaben aufweist, empfehlen wir eine Budgetbegrenzung für die Platzierung, damit mehr Geld für Platzierungen mit Skalierung bereitgestellt werden kann. Die Kalibrierung von Budgetänderungen kann 24 bis 48 Stunden dauern.

* **Optimierungsziele:** Verwenden Sie eines der beiden Leistungsoptimierungsziele, *[!UICONTROL Highest Return on Ad Spend]* oder *[!UICONTROL Lowest Cost per Acquisition]*, abhängig vom Paketziel. Mit diesen Zielen wird das Paket automatisch für die Platzierungen mit der höchsten ROAS bzw. der niedrigsten CPA optimiert.

* **Benutzerdefinierte Ziele:**
   * Wenn ein neues Paket dasselbe Ziel wie ein vorhandenes Paket hat, können Sie optional das vorhandene Paket verknüpfen, damit der Algorithmus die vorhandenen Daten des maschinellen Lernens verwenden kann.
   * Geben Sie die entsprechende [!UICONTROL Target CPA] oder [!UICONTROL Target ROAS].

* **Flug-Geschwindigkeit und Intraday-Geschwindigkeit:** Wählen Sie für beide Arten von Geschwindigkeit die Option *[!UICONTROL Even]* um Ihre Leistungsziele zu maximieren, indem Sie gleichmäßig über jeden Tag und während des gesamten Fluges fahren.

  >[!CAUTION]
  >
  >Verwendung *[!UICONTROL FrontLoad]* und *[!UICONTROL Aggressive Front Load]* für Flugplatzierungen und *[!UICONTROL ASAP]* Geschwindigkeit für die Intraday-Geschwindigkeit nur dann, wenn Sie die Bereitstellung vollständig priorisieren und Ausgaben der Leistungsoptimierung überlassen, da diese Strategien Ihre gewünschten Performance-KPIs negativ beeinflussen können.

## Schritt 4: Erstellen einer Platzierungsstruktur

Weniger ist mehr. Wenn Sie weniger als sechs Platzierungen pro Paket einrichten können, kann das verfügbare Budget dynamisch zu den Platzierungen mit der besten Performance wechseln.

Stellen Sie außerdem sicher, dass Sie jede Platzierung zu einem Paket mit dem Paketzieltyp *[!UICONTROL Prospecting]* oder *[!UICONTROL Retargeting]*, falls zutreffend.

Im Folgenden finden Sie die empfohlenen Platzierungseinstellungen für Leistungskampagnen.

### Ziele

Sie müssen die CPA- oder ROAS-Optimierung auf Paketebene konfigurieren (siehe Schritt 3 - Erstellen von Paketen), Sie können jedoch zusätzliche Einstellungen auf Platzierungsebene hinzufügen.

* **Max. Angebot:**
   * Verwenden Sie für die Prospektion von Platzierungen ein geringes Höchstgebot ($5).
   * Verwenden Sie für Retargeting-Platzierungen ein Höchstgebot ($12).

* **Vorab-Angebotsfilter:** Minimieren oder idealerweise vermeiden Sie das Festlegen aggressiver Pre-Bid-Filter, die die Platzierung daran hindern, eine Skalierung zu erreichen. Zu den Best Practices zählen:

   * Verwenden Sie einen (1) Filter vor dem Angebot pro Platzierung. Die Verwendung mehrerer Filter vor dem Angebot erfordert, dass beide erfüllt sind, wodurch die Skalierung verringert wird.

   * Erwägen Sie in Fällen, in denen zusätzliches Targeting (wie Zielgruppe, Geo und Site-Targeting) angewendet wird, weniger strenge Filter vor dem Angebot festzulegen.

Siehe Beschreibungen der Verwendung der einzelnen Filter vor dem Angebot unter [Vorab-Angebotsfilter auf Platzierungsebene und deren Verwendung](/help/dsp/optimization/optimization-pre-bid-filters.md).

### Bestand

Um die Skalierung zu maximieren, verwenden Sie [!UICONTROL Public] (Open Exchange) und [!UICONTROL On Demand] Inventar.

### Site-Targeting

* **[!UICONTROL Traffic Type]**: [!UICONTROL Websites] only
* **[!UICONTROL Site Tier]**: [!UICONTROL All sites]

### Zielgruppen-Targeting

<!-- Say something about limiting unnecessary constraints/limitations, including dayparting, which limit your chances for ad exposure. Use only when it's required for your audience. -->

* **[!UICONTROL Included Audiences]:**
   * Gruppieren Sie für die Platzierung ähnliche Zielgruppenkategorien und ähnliche Zielgruppengrößen in einer Platzierung. Führen Sie dann je nach Leistung einen der folgenden Schritte aus:
      * Entfernen Sie leistungsschwache Zielgruppen aus vorhandenen Platzierungen.
      * Verschieben Sie leistungsfähigste Zielgruppen in eine separate Platzierung, um Budgets besser zu steuern.
   * Für Retargeting-Platzierungen sollten Sie idealerweise ein Zielgruppensegment pro Platzierung einbeziehen, um Angebote und Budget einfach zu steuern.

>[!NOTE]
>
>Ihre Anzeigen funktionieren am besten, wenn ein Benutzer nur durch eine Platzierung erreicht werden kann. Eine erhebliche Überlappung der Benutzer zwischen Platzierungen kann zu Wettbewerb führen, was einen Zyklus kontinuierlich steigender Angebote ergibt und die Kosten pro Benutzer erhöht. Wenn Sie daher mehrere Zielgruppen einbeziehen, stellen Sie sicher, dass diese nicht aus überlappenden Benutzern/Zielgruppenmitgliedern bestehen.
>
> Sie können Zielgruppen nicht überschneiden, indem Sie Zielgruppen in Ebenen erstellen, sodass Sie die höheren, integrativeren Ebenen von Platzierungen nach Bedarf unterdrücken können.

* **[!UICONTROL Frequency Capping]:**
   * Verwenden Sie für die Prospektion von Platzierungen enge Frequenzlimitierung (eine Impression pro Tag).
   * Setzen Sie für Retargeting-Platzierungen die primäre Platzierungsbegrenzung auf 6-10 Impressionen pro Tag und die sekundäre Begrenzung auf eine Impression pro Stunde.

* **[!UICONTROL Device Targeting]**:
   * Einschließen [!UICONTROL Computer], [!UICONTROL Mobile], und [!UICONTROL Tablet].
   * Keine Zielgruppe [!UICONTROL Firefox] und [!UICONTROL Safari] aufgrund von Targeting- und Messungsbeschränkungen. Weitere Informationen erhalten Sie von Ihrem Adobe-Account-Team [!DNL Adobe] Unterstützung für [!DNL Safari ITP].
   * Wenn Sie mobilen Webtraffic als Ziel auswählen, deaktivieren Sie alle mobilen Browser außer [!UICONTROL Chrome] und [!UICONTROL Edge].

### Markensicherheit und Medienqualität

Verwendung von kontextueller Filterung, Blockierung von Pre-Bid-Betrug und/oder [!UICONTROL Ads.txt] Die Filterung begrenzt die Größe Ihrer Platzierungen, verwendet sie jedoch bei Bedarf.

## Schritt 5: Verwenden der richtigen kreativen Assets

* Es empfiehlt sich, so viele individuelle Anzeigengrößen wie möglich einzubeziehen, um die Reichweite zu maximieren. Mit der universellen Anzeigevorlage können Sie eine beliebige standardmäßige Anzeigegröße hochladen.
* Stellen Sie sicher, dass alle Platzierungen *mindestens* alle Hauptanzeigengrößen (300 x 250, 728 x 90, 160 x 600, 300 x 600, 320 x 50 und 300 x 50).
* Aktualisieren Sie kreative Inhalte häufig, um kreative Müdigkeit zu verhindern.

>[!MORELIKETHIS]
>
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
> * [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)
>* [Optimierungsziele und Verwendung](optimization-goals.md)
>* [Vorab-Angebotsfilter auf Platzierungsebene und deren Verwendung](optimization-pre-bid-filters.md)
>* [Checkliste für den Kampagnenstart](/help/dsp/campaign-management/campaign-launch-checklist.md)
