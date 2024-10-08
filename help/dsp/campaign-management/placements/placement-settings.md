---
title: Platzierungseinstellungen
description: Siehe Beschreibungen der verfügbaren Platzierungseinstellungen.
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: 7ee798e11375863e776ac3e802efc9112280e750
workflow-type: tm+mt
source-wordcount: '3887'
ht-degree: 0%

---

# Platzierungseinstellungen

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** Der Platzierungsname.

>[!TIP]
>Verwenden Sie eine Benennungskonvention, die für Ihre Situation sinnvoll ist. Eine empfohlene Benennungskonvention ist &quot;*\&lt;Kampagnenname\>: \&lt;Anzeigeneinheit\>: \&lt;Dauer\>: \&lt;Targeting\>*&quot;.

**[!UICONTROL Status]:** Der Platzierungsstatus: *[!UICONTROL Active]* (der Standardwert) oder *[!UICONTROL Paused]*.

>[!TIP]
>Die Best Practice besteht darin, die Platzierung so lange anzuhalten, bis Sie bereit sind, sie zu starten.

**[!UICONTROL Details]:** (Schreibgeschützt) Der zutreffende Anzeigentyp, das Konto, das die Platzierung erstellt oder erstellt, und die übergeordnete Kampagne. Um weitere Details anzuzeigen, klicken Sie auf **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** Öffnet eine Liste vorhandener Platzierungsvorlagen. So füllen Sie die Targeting-Einstellungen aus einer Vorlage automatisch aus:

1. Führen Sie einen der folgenden Schritte aus:

   * Um alle Zielgruppen aus einer Vorlage wiederzuverwenden, aktivieren Sie das Kontrollkästchen neben dem Vorlagennamen.

   * Um einzelne Zieltypen einer Vorlage wiederzuverwenden, erweitern Sie den Vorlagennamen und aktivieren Sie das Kontrollkästchen neben den Zieltypen, die Sie wiederverwenden möchten.

1. Klicken Sie auf **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Nur Videoanzeigenformate) Die Anzeigendauer und/oder Anzeigenspezifikationen, die zur Berechnung der Prognoseprojektion auf der rechten Seite verwendet werden. Die Felder variieren je nach Anzeigentyp.

**[!UICONTROL Environment]:** (Nur universelle Videoanzeigenformat) Die Geräteumgebungen (Desktop, Mobil, vernetztes TV), die als Ziele in die Platzierung aufgenommen werden sollen. Geben Sie mindestens 1 an.

In benutzerspezifischen Berichten zeigt die Dimension auf Platzierungsebene &quot;Geräteumgebung&quot;die Zielumgebung an.

**[!UICONTROL Placement tags]:** (Optional) Suchbegriffe oder Spitznamen, die Sie bei der Suche nach dieser Platzierung unterstützen.

## Ziele

**[!UICONTROL Package]:** (Optional) Ein Paket, dem die Platzierung zugewiesen ist. Klicken Sie auf ![Bearbeiten](/help/dsp/assets/edit.png) , um ein vorhandenes Paket auszuwählen oder ein Paket zu erstellen. Wenn Sie die Platzierung einem Paket zuweisen, wird der Abschnitt &quot;[!UICONTROL Goals]&quot;mit den Flugdaten, dem Versandziel und dem Budget des Pakets aktualisiert.

**[!UICONTROL Flight Dates]:** Das Start- und Enddatum für die Platzierung. Genehmigte Anzeigen können während des Fluges ausgeführt werden, wenn die Platzierung aktiv ist und einem aktiven Paket oder einer aktiven Kampagne zugewiesen wird.

Die Daten für das Paket (falls zutreffend) oder die Kampagne werden standardmäßig automatisch ausgefüllt.

>[!NOTE]
>
>* Die Fluchtdaten müssen innerhalb der Kampagnendaten und der Pauschalflugdaten enthalten sein.

### Platzierungen, die Paketen mit Geschwindigkeit auf Paketebene zugewiesen sind

**[!UICONTROL Placement Funding]:** Wie wird die Platzierung finanziert?

* *[!UICONTROL Optimize based on performance]:* Steuert das Budget auf Paketebene.
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]:* Ermöglicht Ihnen das Festlegen eines Mindest- und/oder eines maximalen Platzierungsbudgets. Geben Sie mindestens einen Budgettyp an:

   * *[!UICONTROL Maximum Budget]*: Geben Sie einen Wert und die Dauer ein (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

   * *[!UICONTROL Minimum Budget]*: Das Mindestbudget als Prozentsatz des Package-Budgets. Wenn eine Intervallbegrenzung angegeben wird, wird der Mindestbudgetwert immer als Prozentsatz der Intervallbegrenzung berechnet. Andernfalls wird sie als Prozentsatz des Package-Budgets berechnet.

**[!UICONTROL Max Bid]:** Das Maximum, das für 1000 Impressionen bezahlt werden kann.

**[!UICONTROL Placement Pre-bid Filters]:** Bis zu fünf KPI-Schwellenwerte (z. B. eine minimale Sichtbarkeitsmetrik oder Clickthrough-Rate), die erfüllt sein müssen, damit Angebote unterbreitet werden können. Sie können als Optimierungstaktiken Pre-Gebot-Filter verwenden, aber Sie wissen, dass jede Regel die Möglichkeiten einschränken kann, für die diese Platzierung Gebote abgeben kann. So fügen Sie Filter hinzu oder bearbeiten sie:

1. Klicken Sie auf ![Bearbeiten](/help/dsp/assets/edit.png).
1. Führen Sie einen der folgenden Schritte aus:
   * So fügen Sie einen Filter hinzu:
      1. Klicken Sie auf **[!UICONTROL Add Filter]**.
      1. Wählen Sie neben **[!UICONTROL Only bid if]** eine Metrik aus und geben Sie dann einen Wert ein.
   * Um einen Filter zu entfernen, klicken Sie in der Filterzeile auf **[!UICONTROL X]** .
1. Klicken Sie auf **[!UICONTROL Save]**.

Beschreibungen der einzelnen Filter vor dem Angebot finden Sie unter &quot;[Vorangebotsfilter auf Platzierungsebene und Verwendung dieser Filter](/help/dsp/optimization/optimization-pre-bid-filters.md)&quot;.

### Alle anderen Platzierungen

**[!UICONTROL Budget Goal]:** Die Obergrenze des Bruttobudgets und das Budgetintervall (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Nur Platzierungen in Kampagnen mit Margenverwaltung) Die Obergrenze des Bruttobudgets und das Budgetintervall (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:** Das Optimierungsziel für das Paket. Beschreibungen der einzelnen Optimierungsziele finden Sie unter &quot;[Optimierungsziele und Verwendung dieser Ziele](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** Das Zielziel, das zur Leistungsverfolgung verwendet wird.

>[!NOTE]
>
>Dieses Feld ist nur ein Benchmark und wird nicht für die Entscheidungsfindung verwendet.

**[!UICONTROL Pace on]:** Die Grundlage für die Geschwindigkeit:

* **[!UICONTROL Budget goal]:** (Standard) Diese Option liefert so viele Impressionen wie möglich innerhalb des zugewiesenen Budgets.

* **[!UICONTROL Impressions]:** Diese Option liefert Impressionen, bis eine angegebene Menge innerhalb eines bestimmten Intervalls erreicht ist. Wenn Sie diese Option auswählen, geben Sie die Anzahl der Impressionen und das Intervall an: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* oder *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** Das Maximum, das für 1000 Impressionen bezahlt werden kann.

**[!UICONTROL Flight pacing]:** (Nur Platzierungen mit Platzierungsebenen-Geschwindigkeit) So beschleunigen Sie die Anzeigenbereitstellung:

* *[!UICONTROL Even]:* (Standard) Die Bereitstellung erfolgt gleichmäßig über jeden Flug hinweg, wobei die Zielgruppe 50 % des Versands in der ersten Hälfte des Fluges beträgt.

* *[!UICONTROL Slightly Ahead]:* (Die Standardeinstellung) Beschleunigt den Versand, sodass er zur Hälfte der Flugdauer zu 55-65 % vollständig ist.

* *[!UICONTROL Frontload]:* Beschleunigt den Versand, sodass er zur Hälfte des Fluges zu 65-75 % abgeschlossen ist.

* *[!UICONTROL Aggressive Frontload]:* Beschleunigt den Versand, sodass 75-85 % des gesamten Fluges vollständig sind.

**[!UICONTROL Intraday pacing]:** (Nur Platzierungen mit Platzierungsebenen-Geschwindigkeit) So können Sie die Anzeigenbereitstellung über jeden Tag innerhalb des Fluges hinweg beschleunigen:

* *[!UICONTROL Even]:* (Die Standardeinstellung) Skaliert die Bereitstellung auf Grundlage der Lagerverfügbarkeit. Im Allgemeinen werden pro Stunde mehr Anzeigen zur Verfügung gestellt, wenn das Auktionsvolumen höher ist, und morgens und abends weniger Anzeigen geliefert.

* *[!UICONTROL ASAP]:* (Der Standardwert) Beschleunigt die Bereitstellung auf die doppelte Geschwindigkeit von *Even*.

  >[!CAUTION]
  >
  >Diese Option kann sich negativ auf die Leistung auswirken. Verwenden Sie diese Option nur, wenn Sie die Bereitstellung vollständig priorisieren und die Leistungsoptimierung vorziehen.

**[!UICONTROL Placement Pre-bid Filters]:** (Optional) Bis zu fünf Filter, die erfüllt sein müssen, damit Angebote unterbreitet werden können. Sie können als Optimierungstaktiken Vorgebotsfilter verwenden. Beachten Sie jedoch, dass jede Regel die Möglichkeiten einschränken kann, für die diese Platzierung Gebote abgeben kann. So fügen Sie Filter hinzu oder bearbeiten sie:

1. Klicken Sie auf ![Bearbeiten](/help/dsp/assets/edit.png).
1. Führen Sie einen der folgenden Schritte aus:
   * So fügen Sie einen Filter hinzu:
      1. Klicken Sie auf **[!UICONTROL Add Filter]**.
      1. Wählen Sie neben **[!UICONTROL Only bid if]** eine Metrik aus und geben Sie dann einen Wert ein.
   * Um einen Filter zu entfernen, klicken Sie in der Filterzeile auf **[!UICONTROL X]** .
1. Klicken Sie auf **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Optional) Bestimmte Orte, an denen Anzeigen in die Platzierung ein- oder ausgeschlossen werden sollen. Wenn Sie keine Orte angeben, werden alle Orte als Ziel ausgewählt.

>[!NOTE]
>
>Orte für Stadt und DMA sind nicht für Roku-Platzierungen verfügbar.

So legen Sie Speicherorte fest:

1. Klicken Sie auf ![Bearbeiten](/help/dsp/assets/edit.png).
1. Führen Sie einen der folgenden Schritte aus:
   * Ein- oder Ausschließen eines Landes, eines Bundesstaates, einer Stadt, DMA, eines Bundesgesetzbezirks oder eines Landbezirks
      1. Wählen Sie den Positionstyp in der linken Spalte aus.
      1. (Nach Bedarf) Klicken Sie auf einen Ort, um ihn zu erweitern.
      1. Klicken Sie neben dem Ort auf *[!UICONTROL Include]* , um ihn als Ziel einzuschließen, oder auf *[!UICONTROL Exclude]* , um ihn als Ziel auszuschließen.
   * So suchen Sie nach einer Postleitzahl und schließen alle ausgewählten Ergebnisse ein oder aus:
      1. Klicken Sie auf **[!UICONTROL Search Postal Code]**.
      1. Wählen Sie das Land aus.
      1. Geben Sie den Namen der Stadt ein und klicken Sie dann auf ![Bearbeiten](/help/dsp/assets/search.png).
      1. Klicken Sie auf das richtige Suchergebnis.
      1. Klicken Sie auf *[!UICONTROL Include All]* , um alle Orte als Ziele einzuschließen, oder auf *[!UICONTROL Exclude All]* , um alle Orte als Ziele auszuschließen.
   * So geben Sie Postleitzahlen ein oder fügen sie ein und schließen sie alle ein oder aus:
      1. Klicken Sie auf **[!UICONTROL Paste Postal Code]**.
      1. Wählen Sie das Land aus.
      1. Geben Sie bis zu 1000 Postleitzahlen ein oder fügen Sie sie ein.
Fügen Sie eine Postleitzahl pro Zeile hinzu oder geben Sie mehrere Werte ein, die durch Kommas oder Tabs getrennt sind.
      1. Klicken Sie auf *[!UICONTROL Include All]* , um alle Orte als Ziele einzuschließen, oder auf *[!UICONTROL Exclude All]* , um alle Orte als Ziele auszuschließen.
   * Um einen Ort aus der Liste [!UICONTROL Included] oder [!UICONTROL Excluded] zu entfernen, klicken Sie auf **[!UICONTROL X]** neben der Position in der rechten Spalte.
1. Klicken Sie auf **[!UICONTROL Done]**.

>[!NOTE]
>
>* Nicht alle Länder verfügen über Standorte für Bundesland-, Stadt- oder Postleitzahlen.
>* DMA (Marktsegment), Federal Legislation Districts und State Legislation Districts sind nur für US-Standorte verfügbar.

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Inventarquellen, die als Ziele ein- oder ausgeschlossen werden sollen. Bei den meisten Platzierungstypen sind standardmäßig alle Inventartypen und alle Quellen für jeden Typ enthalten. Bei [!DNL Roku] -Platzierungen müssen Sie den Inventartyp und die Quellen angeben. Sie können aus den folgenden Lagerbestandsarten wählen:

* [!UICONTROL Public]: (Alle Platzierungstypen außer Roku) Alle offenen Exchange-Lagerbestände, auf die DSP Zugriff hat. Sie können das öffentliche Inventar einbeziehen und ausschließen.

  Sie können die Liste nach Quelle oder Feed anzeigen. Wenn Sie die Liste nach Feed anzeigen, können Sie nach Feed-Name, Feed-Schlüssel oder einem ausgewählten charakteristischen Tag suchen.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: Ihre bestehenden privaten Angebote (oder vorhandenen privaten [!DNL Roku] Angebote für [!DNL Roku] Platzierungen) für Herausgeber, die Sie in DSP eingerichtet haben. Sie können das öffentliche Inventar einbeziehen, aber nicht ausschließen.

  Sie können die Liste nach Keyword, Schlüssel, Deal-ID oder benutzerdefiniertem Tag durchsuchen.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Optional) Überschreibt den Angebotspreisalgorithmus, um mindestens die Festpreis- und Tiefstpreise für Geschäfte zu bieten.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: Alle [Premium-, nicht garantierten [!UICONTROL On Demand] Inventar](/help/dsp/inventory/on-demand-inventory-about.md) (oder [!UICONTROL On Demand] [!DNL Roku]-Angebote für [!DNL Roku]-Platzierungen), die Sie in [!DNL DSP] abonniert haben. Sie können den Lagerbestand für [!UICONTROL On Demand] ein- und ausschließen.

  Sie können die Liste nach Quelle oder Feed anzeigen. Wenn Sie die Liste nach Feed anzeigen, können Sie nach Feed-Name, Feed-Schlüssel oder einem ausgewählten Publisher-Bereich, Kategorie-Tag oder charakteristischen Tag suchen.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Optional) Überschreibt den Angebotspreisalgorithmus, um mindestens die Festpreis- und Tiefstpreise für Geschäfte zu bieten.

So legen Sie das Inventar-Targeting fest:

* Um einen Inventartyp auszuschließen, deaktivieren Sie das Kontrollkästchen neben dem Namen.
* So wählen Sie einen Inventartyp aus:
   1. Aktivieren Sie das Kontrollkästchen neben dem Inventartypnamen.
   1. (Optional) Ändern Sie die Quellen, um Folgendes einzuschließen:
      1. Klicken Sie auf ![Bearbeiten](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] und [!UICONTROL On Demand] inventory) Klicken Sie auf **[!UICONTROL View by Source]** oder **[!UICONTROL View by Feed]** , um die Liste der Quellen zu ändern.
      1. (Falls zutreffend) Filtern Sie den Bestand nach Bedarf.
      1. Geben Sie die Quellen an, die ein- und ausgeschlossen werden sollen:
         * Um eine Quelle vom Typ [!UICONTROL Public] oder [!UICONTROL On Demand] einzuschließen, klicken Sie auf **[!UICONTROL Include]** neben dem Quellnamen.
         * So schließen Sie [!UICONTROL Private] -Quellen ein:
            * Um den gesamten Bestand in einen Deal einzubeziehen, klicken Sie auf **[!UICONTROL Include all]** neben dem Namen des Deals.
            * Um eine einzelne Inventarquelle einzubeziehen, erweitern Sie den Namen des Deals und klicken Sie dann auf das Kontrollkästchen neben dem Quellnamen.
         * Um eine [!UICONTROL Public] oder [!UICONTROL On source] auszuschließen, klicken Sie auf **[!UICONTROL Exclude]** neben dem Quellnamen.
   1. (Optional) Klicken Sie auf &quot;**[!UICONTROL Save & Export]**&quot;, um eine CSV-Datei mit den Targeting-Informationen zum Speicherort der Downloads Ihres Browsers herunterzuladen.
   1. Klicken Sie auf **[!UICONTROL Save]**.

>[!TIP]
>
>Wenn Sie den Lagerbestand von [!UICONTROL On Demand] abonniert haben, aber die Herausgeber oder Angebote, die auf die Zielgruppe ausgerichtet sind, nicht finden können, überprüfen Sie den Status der Angebote. Weitere Informationen zu Status finden Sie unter [Info [!DNL On Demand] Premium Inventory](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (Nur Videoplatzierungen) Schließt den Traffic über den Fluss aus.

Über dem Inhalt angezeigte Werbeanzeigen werden in der Regel als Popup oder als Inhaltsangabe (im nativen Erlebnis) und nicht als normale Videoanzeigen in einem Videoplayer angezeigt.

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** Die Traffic-Typen, die als Ziel ausgewählt werden sollen. Zu den Optionen gehören **[!UICONTROL Websites]** und **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** (Verfügbar, wenn **[!UICONTROL Paste list of targeted sites]** den Wert *[!UICONTROL Off]* hat) Die Qualität der Zielseiten. Die Ebenen 1 bis 3 sind alle markensicher und wurden vom DSP-Zuordnungsteam genehmigt.

* *[!UICONTROL Tier 1]:* Premium-Sites und -Anwendungen, die national erkennbar sind.

* *[!UICONTROL Tier 2]:* Die Zielebene 1 sowie Qualitäts-Sites und -Anwendungen, die weniger bekannt sind als Ebene 1.

* *[!UICONTROL Tier 3]:* Zielebenen 1-2 sowie legitime und markensichere Sites und Anwendungen, die einer Nischenzielgruppe entsprechen. Verwenden Sie Ebene 3 für Zielgruppen- oder Daten-Targeting-Käufe.

* *[!UICONTROL All Sites]:* Zielebenen 1-3 und neuer Bestand, der nicht geprüft oder kategorisiert wurde und den Sie für die Reichweite verwenden können.

>[!NOTE]
>
>Der Bestand ist spezifisch für die Anzeigeneinheiten in der Platzierung.

>[!TIP]
>
>Für Leistungskampagnen wird empfohlen, *[!UICONTROL All Sites]* auszuwählen.

**[!UICONTROL Site Categories]:** (Optional; verfügbar, wenn **[!UICONTROL Paste list of targeted sites]** *[!UICONTROL Off]* ist) Site-Kategorien innerhalb der ausgewählten Site-Ebenen, die entweder als Ziele ein- oder ausgeschlossen werden sollen (aber nicht beide). Wählen Sie aus den Listen der vertikalen Site, die DSP dem Betreff zugeordnet hat:

1. Klicken Sie auf ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die Site-Kategorien an, die entweder ein- oder ausgeschlossen werden sollen:
   * So fügen Sie Site-Kategorien hinzu:
      1. Klicken Sie auf **[!UICONTROL Include categories]**.
      1. Aktivieren Sie das Kontrollkästchen neben den jeweiligen Kategorien, die als Ziel ausgewählt werden sollen.
   * So schließen Sie Site-Kategorien aus:
      1. Klicken Sie auf **[!UICONTROL Exclude categories]**.
      1. Aktivieren Sie das Kontrollkästchen neben den Kategorien, die ausgeschlossen werden sollen.
1. (Optional) Klicken Sie auf &quot;**[!UICONTROL Export]**&quot;, um eine CSV-Datei mit den Targeting-Informationen zum Speicherort der Downloads Ihres Browsers herunterzuladen.
1. Klicken Sie auf **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (Optional; verfügbar, wenn **[!UICONTROL Paste list of targeted sites]** *[!UICONTROL Off]* ist) Sites, die ausgeschlossen werden sollen. Sie können entweder nach Sites suchen und diese auswählen oder Domänennamen eingeben oder einfügen:

1. Klicken Sie auf ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die Sites an:
   * So suchen Sie nach einer Site:
      1. Klicken Sie auf **[!UICONTROL Search]**.
      1. Geben Sie einen Suchbegriff ein, wählen Sie eine Site-Ebene und/oder wählen Sie eine Site-Kategorie aus.
      1. Wählen Sie in den Suchergebnissen die Sites aus, die ausgeschlossen werden sollen:
         * Um eine einzelne Site auszuschließen, aktivieren Sie das Kontrollkästchen daneben.
         * (Wenn mehr als 50 Ergebnisse verfügbar sind) Um die ersten 50 Ergebnisse auszuschließen, klicken Sie auf **[!UICONTROL Exclude these 50]**. Um alle Suchergebnisse auszuschließen, klicken Sie auf **[!UICONTROL Exclude these \<*NN *\>]**.
   * So geben Sie Domänennamen ein:
      1. Klicken Sie auf **[!UICONTROL Paste]**.
      1. Geben Sie einen oder mehrere Domänennamen in separate Zeilen ein.
      1. Klicken Sie auf **[!UICONTROL Exclude All]**.
1. Klicken Sie auf **[!UICONTROL Done]** , wenn Sie fertig sind.

>[!NOTE]
>
>* Zusätzlich zur DSP [global blockierten Site-Liste](/help/dsp/introduction/features/brand-safety-media-quality.md) auf Kontoebene und auf Advertiser-Ebene werden auch blockierte Site-Listen auf Kontoebene angewendet, die Seiten enthalten, die für Anzeigen als unsicher gelten.
>* Blockierte Site-Listen überschreiben immer zielgerichtete Site-Listen. Wenn durch eine Platzierung dieselbe Zielgruppe für eine Anzeige ausgeschlossen und einbezogen wird, wird die Zielgruppe ausgeschlossen.

**[!UICONTROL Language]:** (Optional) Eine einzelne Sprache, die als Ziel ausgewählt werden soll.

**[!UICONTROL Site List Preview]:** (Schreibgeschützt) Alle Targeting- und Blockierungssites für die Platzierung.

Optional können Sie die Liste der Ziel- und Blockierungssites als CSV-Datei (CSV) mit kommagetrennten Werten exportieren. Um die Liste zu exportieren, klicken Sie auf **[!UICONTROL Export full site list]** und öffnen oder speichern Sie dann die Datei entsprechend der üblichen Vorgehensweise Ihres Browsers.

**[!UICONTROL Allow unscreened sites]:** (Nur Standard-Display-Platzierungen) Aktiviert die Anzeigenbereitstellung auf nicht geprüften Sites. Wenn die Platzierung auf den privaten Bestand ausgerichtet ist, kann diese Option Anzeigen auf blockierten Sites bereitstellen.

**[!UICONTROL Paste list of targeted sites]:** Ermöglicht es Ihnen, nur bestimmte Sites als Ziel festzulegen. Wenn Sie diese Option aktivieren, sind die anderen Site-Targeting-Optionen deaktiviert.

**[!UICONTROL Sites]:** (Verfügbar, wenn **[!UICONTROL Paste list of targeted sites]** *[!UICONTROL On]* ist) Sites als Ziel. Sie können entweder nach Sites suchen und diese auswählen oder Domänennamen eingeben oder einfügen:

1. Klicken Sie auf ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die Sites an:
   * So suchen Sie nach einer Site:
      1. Klicken Sie auf **[!UICONTROL Search]**.
      1. Geben Sie einen Suchbegriff ein, wählen Sie eine Site-Ebene und/oder wählen Sie eine Site-Kategorie aus.
      1. Wählen Sie in den Suchergebnissen die Sites aus, die einbezogen werden sollen:
         * Um eine einzelne Site auszuschließen, aktivieren Sie das Kontrollkästchen daneben.
         * (Wenn mehr als 50 Ergebnisse verfügbar sind) Um die ersten 50 Ergebnisse einzubeziehen, klicken Sie auf **[!UICONTROL Include these 50]**. Um alle Suchergebnisse einzubeziehen, klicken Sie auf **[!UICONTROL Include these \<*NN *\>]**.
   * So geben Sie Domänennamen ein:
      1. Klicken Sie auf **[!UICONTROL Paste]**.
      1. Geben Sie einen oder mehrere Domänennamen in separate Zeilen ein.
      1. Klicken Sie auf **[!UICONTROL Include All]**.
1. Klicken Sie auf **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Alle Zielgruppensegmente für die Platzierung, einschließlich [ Drittanbietersegmenten, Erstanbietersegmenten, Adobe-Segmenten, benutzerdefinierten Segmenten und gespeicherten Zielgruppen](/help/dsp/audiences/audience-settings.md). Die gesamte und die aktive deduplizierte Zielgruppengröße für alle ausgewählten Segmente und gespeicherten Zielgruppen wird ebenfalls angezeigt. Sie können eine vorhandene Zielgruppe auswählen, eine Zielgruppe erstellen, die Sie später wiederverwenden können, oder bestimmte Zielgruppensegmente auswählen:

* Um eine vorhandene Zielgruppe auszuwählen, klicken Sie auf ![Auswählen](/help/dsp/assets/chevron-down.png) neben [!UICONTROL Included Audiences] und wählen Sie dann die Zielgruppe aus.
* Um eine Zielgruppe zu erstellen, klicken Sie auf ![Auswählen](/help/dsp/assets/chevron-down.png) neben [!UICONTROL Included Audiences] und dann auf **[!UICONTROL + Create Audience]**. Anweisungen finden Sie unter [Erstellen einer wiederverwendbaren Zielgruppe](/help/dsp/audiences/reusable-audience-create.md), beginnend mit Schritt 3.
* Um bestimmte Zielgruppensegmente auszuwählen, klicken Sie auf **[!UICONTROL Select segments for this placement only]**. Wählen Sie die Segmentlogik aus. Anweisungen finden Sie in Schritt 6 unter &quot;[Erstellen einer wiederverwendbaren Zielgruppe](/help/dsp/audiences/reusable-audience-create.md)&quot;. Wenn Sie fertig sind, klicken Sie auf **Speichern**.

**[!UICONTROL Excluded Audiences]:** Alle Zielgruppen, die für die Platzierung ausgeschlossen werden sollen, einschließlich Zielgruppen mit [ Drittanbietersegmenten, Erstanbietersegmenten, Adobe-Segmenten, benutzerdefinierten Segmenten und gespeicherten Zielgruppen](/help/dsp/audiences/audience-settings.md). Die gesamte und die aktive deduplizierte Zielgruppengröße für alle ausgeschlossenen Zielgruppen wird ebenfalls angezeigt. Sie können eine vorhandene Zielgruppe auswählen oder eine neue Zielgruppe erstellen, die Sie später wiederverwenden können:

* Um eine vorhandene Zielgruppe auszuwählen, klicken Sie auf ![Auswählen](/help/dsp/assets/chevron-down.png) neben [!UICONTROL Excluded Audiences] und wählen Sie dann die Zielgruppe aus.

* Um eine Zielgruppe zu erstellen, klicken Sie auf ![Auswählen](/help/dsp/assets/chevron-down.png) neben [!UICONTROL Excluded Audiences] und dann auf **+ Zielgruppe erstellen**. Anweisungen finden Sie unter [Erstellen einer wiederverwendbaren Zielgruppe](/help/dsp/audiences/reusable-audience-create.md), beginnend mit Schritt 3.

**[!UICONTROL Targeting]:** Die Typen der Benutzer-IDs, die als Ziel dienen sollen. Sie können diese Einstellung nicht ändern, nachdem die Platzierung live ist (d. h. nachdem der Flug begonnen hat).

Wenn Sie sowohl Legacy-IDs als auch universelle IDs auswählen, wird den universellen IDs die Gebotseinstellung vorgezogen.

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]*: (Die Standardeinstellung) Die Zielgruppe richtet sich an Benutzer anhand ihrer Cookies, mobilen Werbe-IDs oder verbundenen TV-IDs (CTV). IDs werden basierend auf dem Browser-, In-App- oder CTV-Bestand ausgewählt.

* *[!UICONTROL Universal ID Beta]*: Ermöglicht die Verwendung datenschutzorientierter IDs durch den Benutzer. Wählen Sie einen ID-Typ aus. Die verfügbaren Optionen werden durch die im Abschnitt [!UICONTROL Geo-Targeting] ausgewählten geografischen Ziele bestimmt. Verwendung mit [[!DNL RampID] direkt in DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md) importierten Segmenten, [Segmenten, für die DSP Ihre personenbezogenen Daten in universelle IDs konvertiert](/help/dsp/audiences/sources/source-about.md) oder [benutzerdefinierten Segmenten, die universelle IDs verfolgen](/help/dsp/audiences/custom-segment-create.md).

   * *[!UICONTROL ID5]*: Ziele [!DNL ID5] IDs, die probabilistisch aus E-Mail-Adressen und anderen Signalen erstellt wurden.<!-- What countries/geos are these available for? Everywhere?--> ID5-IDs sind kostenlos verfügbar. **Hinweis:** Drittanbietersegmente von [!DNL Eyeota] können ID5-IDs enthalten.

   * *[!UICONTROL RampID]*: Die Zielgruppen [!DNL LiveRamp] [!DNL RampIDs] der Benutzer, die mit ihren E-Mail-Adressen bei Ihrer Site angemeldet sind.<!-- Verify --> [!DNL RampIDs] ist für Benutzer in Nordamerika, Australien und Neuseeland verfügbar.

   * *[!UICONTROL Unified ID2.0]*: Ziele [!DNL Unified ID2.0] (UID2) IDs von Benutzern, die mit ihren E-Mail-Adressen bei Ihrer Site angemeldet sind.<!-- Verify -->[!DNL UID2 IDs] stehen Benutzern im Europäischen Wirtschaftsraum und einigen weiteren Ländern nicht zur Verfügung. Siehe die [ Liste der verbotenen Länder](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

  **[!UICONTROL Terms of service]**: Die Nutzungsbedingungen für die Verwendung von universellen IDs. Sie oder ein anderer Benutzer im DSP müssen die Bedingungen einmal akzeptieren, bevor Sie Daten in einen neuen ID-Typ konvertieren können. Für Kunden mit verwalteten Serviceverträgen erhält Ihr Adobe Account Team Ihre Einwilligung und akzeptiert die Bedingungen im Namen Ihres Unternehmens. Um die Begriffe zu lesen, klicken Sie auf **>**. Um die Bedingungen zu akzeptieren, scrollen Sie zum unteren Rand der Bedingungen und klicken Sie auf **[!UICONTROL Accept]**.

**[!UICONTROL Cross Device Targeting]:** (Verfügbar, wenn die [-Kampagne für personenbasiertes geräteübergreifendes Targeting konfiguriert ist](/help/dsp/campaign-management/campaigns/campaign-settings.md), Sie nur ältere IDs als Ziel auswählen (nicht universelle IDs) und Sie mindestens ein Segment oder eine Zielgruppe auswählen. Ermöglicht die Erweiterung des Targetings auf alle bekannten Geräte einer Person (entsprechend dem in den Kampagneneinstellungen angegebenen Gerätediagramm), auch auf Geräte, die nicht in den angegebenen Segmenten enthalten sind. Die Gebühren können je nach dem für die Kampagne angegebenen Diagramm gelten. Gerätediagrammdaten sind nur in Nordamerika verfügbar.

**[!UICONTROL Placement Cap]:** (Optional) Die Häufigkeit, mit der ein eindeutiges Gerät, eine universelle ID oder eine Person (je nach der festgelegten [!UICONTROL Cross Device Level] für die Kampagne und der Einstellung [!UICONTROL Targeting] der Platzierung) mit Anzeigen aus der Platzierung bereitgestellt werden kann. Zu den Optionen gehören *[!UICONTROL Unlimited]* oder ein bestimmter Betrag pro Tag, Woche oder Monat.

>[!NOTE]
>
> Sie können Frequenzobergrenzen auf Kampagnen-, Paket- und Platzierungsebene festlegen. DSP respektiert die strengste Frequenzgrenze in der Kampagnenhierarchie.

**[!UICONTROL Secondary Cap]:** (Optional; verfügbar, wenn Sie eine numerische [!UICONTROL Placement Cap] einschließen) Eine zusätzliche Begrenzung innerhalb der Grenzen der primären Platzierungsbegrenzung. Wählen Sie die Anzahl der Impressionen und den Zeitraum aus (z. B. 3 pro 12 Stunden).

**[!UICONTROL Day Parting]:** (Optional) Bestimmte Wochentage und Tageszeit, an denen Anzeigen ausgeführt werden können. So legen Sie Dayparting-Intervalle fest:

1. Klicken Sie auf ![Bearbeiten](/help/dsp/assets/edit.png).
1. Wählen Sie die gewünschte Zeitzone aus.
1. Geben Sie die Intervalle an:
   * Um ein voreingestelltes Intervall auszuwählen, klicken Sie auf eine der Intervallschaltflächen. Zu den Optionen gehören *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]* oder *[!UICONTROL Prime]* (primetime).
   * Um ein Intervall manuell auszuwählen, klicken Sie in eine Zelle und ziehen Sie optional, um das Intervall auszuwählen.
1. Klicken Sie auf **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Optional; für Advertiser verfügbar, die mit [!DNL Proximic by Comscore] Segmenten konfiguriert sind) Bestimmte Segmentnamen oder IDs aus [!DNL Proximic by Comscore], die als Ziele eingefügt werden sollen. Für diese Funktion können zusätzliche Gebühren anfallen. Wenden Sie sich an Ihr Adobe Account-Team, um diese Funktion zu aktivieren und Themensegmente einzurichten.

So legen Sie das Thema-Targeting fest:

1. Klicken Sie auf ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die Zielsegmente an:
   1. Wählen Sie in der linken Spalte den Partner aus: (*[!UICONTROL Comscore]*)
   1. Geben Sie im Eingabefeld die Segmentnamen oder Segment-IDs ein.
1. (Optional) Klicken Sie auf &quot;**[!UICONTROL Export]**&quot;, um eine CSV-Datei mit den Themeninformationen zum Speicherort der Downloads Ihres Browsers herunterzuladen.
1. Klicken Sie auf **[!UICONTROL Save]**.

>[!TIP]
>
>* Beim Thema-Targeting wird der Bestand begrenzt, für den die Platzierung ein Angebot machen kann. Verwenden Sie daher das Thema-Targeting nur für einen geringen Prozentsatz Ihres Gesamtkaufs.
>
>* Richten Sie ein negatives Targeting im Segment auf [!DNL Proximic by Comscore] ein.

**[!UICONTROL Device Targeting]:** (Optional) Spezifische Geräteinformationen, einschließlich Gerätetypen, Hersteller, Betriebssysteme, Browser und Verbindungstypen, die als Ziele ein- und ausgeschlossen werden sollen. Die Typen variieren je nach Platzierungstyp. So legen Sie das Geräte-Targeting fest:

1. Klicken Sie auf ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die Gerätedetails an, die ein- und ausgeschlossen werden sollen:
   1. Wählen Sie in der linken Spalte die Kategorie aus.
   1. Festlegen der Zielgruppenbestimmung:
      * Um einen Wert einzubeziehen, klicken Sie neben dem Wertnamen auf **[!UICONTROL Include]** .
      * Um einen Wert auszuschließen, klicken Sie neben dem Wertnamen auf **[!UICONTROL Exclude]** .
1. (Optional) Klicken Sie auf &quot;**[!UICONTROL Export]**&quot;, um eine CSV-Datei mit den Geräte-Targeting-Informationen zum Speicherort der Downloads Ihres Browsers herunterzuladen.
1. Klicken Sie auf **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Optional) Bestimmte Internetdienstanbieter (ISPs), die als Ziele entweder ein- oder ausgeschlossen werden (aber nicht beide). So legen Sie das ISP-Targeting fest:

1. Klicken Sie auf ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die ISPs an, die ein- oder ausgeschlossen werden sollen:
   * So schließen Sie ISPs ein:
      1. Klicken Sie auf **[!UICONTROL Include ISPs]**.
      1. (Optional) Filtern Sie die Liste nach Keyword.
      1. Aktivieren Sie das Kontrollkästchen neben den jeweiligen ISP, die als Ziel ausgewählt werden sollen.
   * So schließen Sie ISP aus:
      1. Klicken Sie auf **[!UICONTROL Exclude ISPs]**.
      1. (Optional) Filtern Sie die Liste nach Keyword.
      1. Aktivieren Sie das Kontrollkästchen neben jedem ISP, der ausgeschlossen werden soll.
1. (Optional) Klicken Sie auf &quot;**[!UICONTROL Export]**&quot;, um eine CSV-Datei mit den ISP-Targeting-Informationen zum Speicherort der Downloads Ihres Browsers herunterzuladen.
1. Klicken Sie auf **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** Typen der anzuwendenden kontextuellen Filter [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] und [!DNL Peer39]. Die Standardeinstellungen auf Advertiser-Ebene werden für neue Platzierungen ausgewählt, Sie können jedoch die Einstellungen ändern:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Optional) Ein oder mehrere Arten von Inventarkontext, die standardmäßig blockiert werden sollen. Es können zusätzliche Gebühren erhoben werden.

* [!UICONTROL Peer 39]:

   * **Targeting von Sites, die:** (Optional) Ein oder mehrere Arten von Bestandsattributen sind, die standardmäßig als Ziel dienen sollen. Es können zusätzliche Gebühren erhoben werden.

* [!UICONTROL ComScore]:

   * **Blockieren von Sites, die** (Optional) sind Ein oder mehrere Arten von Bestandsattributen, die standardmäßig blockiert werden sollen. Es können zusätzliche Gebühren erhoben werden.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Optional) Der Grad des Erwachseneninhalts, für den Anzeigen standardmäßig blockiert werden sollen: *[!UICONTROL Do Not Block]* (Standard), *[!UICONTROL Standard]* oder *[!UICONTROL Strict]*. Es können zusätzliche Gebühren erhoben werden.

   * **[!UICONTROL Alcohol Content]:** (Optional) Der Alkoholgehalt, für den Anzeigen standardmäßig blockiert werden sollen: *[!UICONTROL Do Not Block]* (Standard), *[!UICONTROL Standard]* oder *[!UICONTROL Strict]*. Es können zusätzliche Gebühren erhoben werden.

**[!UICONTROL Pre-bid fraud blocking]:** Arten von zu blockierenden Sites basierend auf betrügerischem Traffic und verdächtigen Aktivitäten, die durch [!DNL DoubleVerify], [!DNL Integral Ad Science] und [!DNL Peer39] gemessen werden. Die Standardeinstellungen auf Advertiser-Ebene werden für neue Platzierungen ausgewählt, Sie können jedoch die Einstellungen ändern:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Standardmäßig wird der gesamte 100 % ungültige Traffic, einschließlich des Traffics auf entführten Geräten, für neue Platzierungen blockiert. Es können zusätzliche Gebühren erhoben werden.

   * **[!UICONTROL Also block sites with]:** (Optional) Eine zusätzliche Stufe von Betrug und ungültigem Traffic, die dazu führt, dass DSP Anzeigen standardmäßig blockieren: *[!UICONTROL None]* (der Standard, der zusätzlichen Traffic nicht blockiert), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* oder *[!UICONTROL >25% Average Fraud/IVT levels]*. Es können zusätzliche Gebühren erhoben werden.

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** (Optional) Ein oder mehrere Arten von Betrug, durch den Anzeigen standardmäßig blockiert DSP: *[!UICONTROL Fraud]* (blockiert alle Websites mit Betrug), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* und/oder *[!UICONTROL Fraud: Zero Ads]*. Es können zusätzliche Gebühren erhoben werden.

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** (Optional) Ein Typ verdächtiger Website- oder App-Aktivitäten, der dazu führt, dass DSP Anzeigen standardmäßig blockieren: *[!UICONTROL None]* (der Standard, der Anzeigen nicht aufgrund verdächtiger Aktivitäten blockiert), *[!UICONTROL Suspicious Activity - High Risk]* oder *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Es können zusätzliche Gebühren erhoben werden.

**[!UICONTROL Pre-bid viewability]:**

Welche Sichtbarkeit vor dem Gebot filtert nach [!DNL DoubleVerify] und [!DNL Integral Ad Science], um sie auf die Platzierung anzuwenden. Die Standardeinstellungen auf Advertiser-Ebene werden für neue Platzierungen ausgewählt, Sie können die Einstellungen jedoch ändern. Es können zusätzliche Gebühren erhoben werden.

**[!UICONTROL Ads.txt filtering]:**

Welche Ebene von [Ads.txt](https://iabtechlab.com/ads-txt-about/) vor dem Angebot zu verwenden ist, indem die Liste &quot;Autorisierte digitale Verkäufer&quot;jedes Herausgebers angewendet wird. Die Standardeinstellung auf Advertiser-Ebene wird für neue Platzierungen ausgewählt, Sie können jedoch die Einstellungen ändern:

* *[!UICONTROL Opt out of ads.txt (default)]*: Um Inventar von allen Verkäufern zu kaufen.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Zur Priorisierung des Kaufinventars von autorisierten Direktverkäufern und Wiederverkäufern einer Domain.
* *[!UICONTROL Ads.txt sellers only]*: Um Inventar nur von autorisierten Direktverkäufern und Wiederverkäufern einer Domain zu kaufen.
* *[!UICONTROL Ads.txt sellers only]*: Um Inventar nur von autorisierten Direktverkäufern einer Domain zu kaufen.

**[!UICONTROL Attention Targeting]:** (Anzeigen, Video, Mobilgeräte und standardmäßige angeschlossene TV-Platzierungen) Ziele [!DNL Adelaide] vor dem Angebot für Segmente mit einem bestimmten Aufmerksamkeitsniveau (hoch, mittel oder niedrig) basierend auf der angegebenen Site, dem Format und der angegebenen Anzeigengröße. Die Segmente werden wöchentlich aktualisiert. **Hinweis:** Die Verwendung von [!DNL Adelaide] Segmenten für das Targeting erhält eine CPM-Gebühr für jede mit dem [!DNL Adelaide]-Aufmerksamkeits-Targeting gelieferte Impression. Diese Gebühr ist separat von den Gebühren für die [Aufmerksamkeitsmessung](/help/dsp/campaign-management/campaigns/campaign-settings.md). Für interaktive Pre-Roll-Platzierungen werden Ihnen nur VAST-Impressionen berechnet.

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (Werbetreibende, die mit der [!UICONTROL DoubleVerify Authentic Brand Safety] -Option konfiguriert sind) Aktiviert [!DNL DoubleVerify Authentic Brand Safety], wodurch Impressionen nach dem Gebot blockiert werden, indem die benutzerdefinierten Markensicherheitsregeln verwendet werden, die für die angegebene Segment-ID konfiguriert sind. DSP stellt Ihr Konto für die Verwendung der in den Advertiser-Einstellungen angegebenen Segment-ID in Rechnung.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] Platzierungen) Zu den von [!DNL Roku] zugelassenen Drittanbieter für das Tracking gehören [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] und [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (Optional) Ereignis-Tracking-Pixel von Drittanbietern, die standardmäßig an alle neuen Anzeigen in der Platzierung angehängt werden. So legen Sie Ereignispixel fest:

1. Klicken Sie auf ![Bearbeiten](/help/dsp/assets/edit.png).
1. Führen Sie einen der folgenden Schritte aus:
   * Um ein vorhandenes Pixel auszuwählen, aktivieren Sie das Kontrollkästchen in der Pixelzeile.
   * So erstellen Sie ein Pixel:
      1. Klicken Sie auf **[!UICONTROL Create]**.
      1. Geben Sie die folgenden Informationen ein:
         * **[!UICONTROL Pixel name]:** Der Pixelname; die maximale Länge beträgt 500 Zeichen. Verwenden Sie einen Namen, mit dem Sie das Pixel leicht identifizieren können.
         * **[!UICONTROL Pixel event fires on]:** Das Ereignis, durch das das Pixel ausgelöst wird. Die verfügbaren Ereignisse variieren je nach Anzeigentyp.
         * **[!UICONTROL Pixel type]:** Gibt an, ob das Pixel eine *[!UICONTROL IMG URL]* (1x1-Pixelbilddatei), *[!UICONTROL HTML]* oder *[!UICONTROL JavaScript URL]* ist.
         * **[!UICONTROL Pixel URL]:** Die URL des Pixelbilds.
      1. Klicken Sie auf **[!UICONTROL Create and attach]**.
   1. Klicken Sie auf **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (Optional) Konversions-Tracking-Pixel, die standardmäßig an alle neuen Anzeigen in der Platzierung angehängt werden. So legen Sie Konversionspixel fest:

1. Klicken Sie auf ![Bearbeiten](/help/dsp/assets/edit.png).
1. Führen Sie einen der folgenden Schritte aus:
   * Um ein vorhandenes Pixel auszuwählen, aktivieren Sie das Kontrollkästchen in der Pixelzeile.
   * So erstellen Sie ein Pixel:
      1. Klicken Sie auf **[!UICONTROL Create]**.
      1. Geben Sie die folgenden Informationen ein:
         * **[!UICONTROL Conversion pixel name]:** Der Pixelname; die maximale Länge beträgt 500 Zeichen. Verwenden Sie einen Namen, mit dem Sie das Pixel leicht identifizieren können.
         * **[!UICONTROL Conversion category]:** Der Konversionstyp.
         * **[!UICONTROL Impression conversion window]:** Die Anzahl der Tage, nach denen eine Ad-Impression auftritt, in denen die Impression einer Konversion zugeordnet werden kann. Der Standardwert ist 30 Tage.
         * **[!UICONTROL Click conversion window]:** Die Anzahl der Tage nach einem Anzeigenklick, in denen der Klick einer Konversion zugeordnet werden kann. Der Standardwert ist 30 Tage.
         * **[!UICONTROL Notes]:** (Optional) Eine Beschreibung oder andere Informationen über das Pixel.
      1. Klicken Sie auf **[!UICONTROL Create and attach]**.
      1. Implementieren Sie das Konversionspixel auf den relevanten Webseiten:
         1. Gehen Sie im Hauptmenü zu **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**.
         1. Klicken Sie in der Pixelzeile auf **[!UICONTROL edit]**.
         1. Kopieren Sie die Werte in die Felder [!UICONTROL HTML Tag] und [!UICONTROL Flash Tag] nach Bedarf, um sie dem Advertiser oder Website-Kontakt zur Verfügung zu stellen.

            Möglicherweise muss die IT-Abteilung des Werbetreibenden oder eine andere Gruppe die Tag-Bereitstellung planen oder darüber informiert werden.
   1. Klicken Sie auf **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Optional) Ein statischer Drittanbieter-Gebührensatz, der als nicht abrechnungsfähige Kosten pro 1000 Impressionen verfolgt wird. Die Standardeinstellung auf Paketebene wird bei neuen Platzierungen automatisch angewendet, sofern kein anderer Wert eingegeben wird.

>[!NOTE]
>
>Abrechenbare Gebühren werden in der Metrik [!UICONTROL Net CPM] angezeigt.

>[!MORELIKETHIS]
>
>* [Über die Platzierungsverwaltung](placement-about.md)
>* [Erstellen einer Platzierung](placement-create.md)
>* [Platzierungen bearbeiten](placement-edit.md)
>* [Verwalten von Angebotsmultiplikatoren für Platzierungen](placement-manage-bid-multipliers.md)
>* [Anzeigen des Änderungsprotokolls für eine Platzierung](placement-change-log.md)
>* [Tastaturbefehle](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [FAQs zu Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
