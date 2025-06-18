---
title: Platzierungseinstellungen
description: Siehe Beschreibungen der verfügbaren Platzierungseinstellungen.
feature: DSP Placements
exl-id: 5b2574be-5d08-4cf7-910e-deac48d7e035
source-git-commit: 1478e61ebd7dac59cac7566b86e5b1ea97838508
workflow-type: tm+mt
source-wordcount: '4477'
ht-degree: 0%

---

# Platzierungseinstellungen

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** Der Name der Platzierung.

>[!TIP]
>Verwenden Sie eine Namenskonvention, die für Ihre Situation sinnvoll ist. Eine vorgeschlagene Namenskonvention lautet &quot;*\&lt;Kampagnenname\>: \&lt;Anzeigeneinheit\>: \&lt;Dauer\>: \&lt;Zielgruppenbestimmung\>*&quot;.

**[!UICONTROL Status]:** Der Platzierungsstatus: *[!UICONTROL Active]* (Standard) oder *[!UICONTROL Paused]*.

>[!TIP]
>Es empfiehlt sich, die Platzierung anzuhalten, bis Sie bereit sind, sie zu starten.

**[!UICONTROL Details]:** (Schreibgeschützt) Der entsprechende Anzeigentyp, das Konto, das die Platzierung erstellt oder erstellt hat, und die übergeordnete Kampagne. Um weitere Details anzuzeigen, klicken Sie auf **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** Öffnet eine Liste der vorhandenen Platzierungsvorlagen. So füllen Sie Targeting-Einstellungen automatisch aus einer Vorlage aus:

1. Führen Sie einen der folgenden Schritte aus:

   * Um alle Zielgruppen aus einer Vorlage wiederzuverwenden, aktivieren Sie das Kontrollkästchen neben dem Vorlagennamen.

   * Um einzelne Zieltypen aus einer Vorlage wiederzuverwenden, erweitern Sie den Vorlagennamen und aktivieren Sie das Kontrollkästchen neben den Zieltypen, die Sie wiederverwenden möchten.

1. Klicken Sie auf **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Nur Videoanzeigenformate) Die Anzeigendauer und/oder die Anzeigenspezifikationen, mit denen die Prognose auf der rechten Seite berechnet wird. Die Felder variieren je nach Anzeigentyp.

**[!UICONTROL Environment]:** (Nur universelles Video-Anzeigenformat) Die Geräteumgebungen (Desktop, Mobile, Connected TV), die als Ziele in die Platzierung einbezogen werden sollen. Geben Sie mindestens eines an.

In benutzerdefinierten Berichten gibt die Dimension auf Platzierungsebene „Geräteumgebung“ die Zielumgebung an.

**[!UICONTROL Placement tags]:** (Optional) Schlüsselwörter oder Spitznamen, die Ihnen bei der Suche nach dieser Platzierung helfen.

## Ziele

**[!UICONTROL Package]:** (Optional) Ein Paket, dem die Platzierung zugewiesen wird. Klicken Sie ![Bearbeiten](/help/dsp/assets/edit.png), um ein vorhandenes Paket auszuwählen oder ein Paket zu erstellen. Wenn Sie die Platzierung einem Paket zuweisen, wird der Abschnitt &quot;[!UICONTROL Goals]&quot; mit den Flugdaten, dem Versandziel und dem Budget des Pakets aktualisiert.

**[!UICONTROL Flight Dates]:** Das Start- und Enddatum für die Platzierung. Genehmigte Anzeigen können während des Fluges geschaltet werden, wenn die Platzierung aktiv ist und einem aktiven Paket oder einer aktiven Kampagne zugewiesen wird.

Die Datumsangaben für das Paket (falls zutreffend) oder die Kampagne werden standardmäßig automatisch ausgefüllt.

>[!NOTE]
>
>* Die Flugdaten müssen in den Kampagnenflugdaten und den Paketflugdaten enthalten sein.

### Platzierungen, die Paketen mit Geschwindigkeit auf Paketebene zugewiesen sind

**[!UICONTROL Placement Funding]:** Budgetplanung für die Platzierung:

* *[!UICONTROL Optimize based on performance]:* Steuert das Budget auf Paketebene.
* *[!UICONTROL Set a Fixed Minimum or Maximum Budget]:* Ermöglicht das Festlegen eines minimalen und/oder maximalen Platzierungsbudgets. Geben Sie mindestens eine Budgetart an:

   * *[!UICONTROL Maximum Budget]*: Geben Sie einen Wert und die Dauer ein (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

   * *[!UICONTROL Minimum Budget]*: Das Mindestbudget in Prozent des Paketbudgets. Wenn eine Intervallbegrenzung angegeben ist, wird der minimale Budgetwert immer als Prozentsatz der Intervallbegrenzung berechnet. Andernfalls wird er als Prozentsatz des Paketbudgets berechnet.

**[!UICONTROL Max Bid]:** Das Maximum für 1000 Impressionen zu bezahlen.

**[!UICONTROL Placement Pre-bid Filters]:** Bis zu fünf KPI-Schwellenwerte (z. B. eine Metrik für die minimale Sichtbarkeit oder Clickthrough-Rate), die erfüllt sein müssen, damit Angebote unterbreitet werden können. Sie können Pre-Bid-Filter als Optimierungstaktik verwenden, aber verstehen Sie, dass jede Regel die Chancen einschränken kann, für die diese Platzierung Gebote abgeben kann. So fügen Sie Filter hinzu oder bearbeiten sie:

1. Klicken Sie ![Bearbeiten](/help/dsp/assets/edit.png).
1. Führen Sie einen der folgenden Schritte aus:
   * So fügen Sie einen Filter hinzu:
      1. Klicken Sie auf **[!UICONTROL Add Filter]**.
      1. Wählen Sie neben **[!UICONTROL Only bid if]** eine Metrik aus und geben Sie dann einen Wert ein.
   * Um einen Filter zu entfernen, klicken Sie in der Filterzeile auf **[!UICONTROL X]** .
1. Klicken Sie auf **[!UICONTROL Save]**.

Beschreibungen der einzelnen Pre-Bid-Filter finden Sie unter &quot;[Pre-Bid-Filter auf Platzierungsebene und deren Verwendung](/help/dsp/optimization/optimization-pre-bid-filters.md)&quot;.

### Alle anderen Platzierungen

**[!UICONTROL Budget Goal]:** Brutto-Budgetobergrenze und Budgetzeitraum (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (nur Platzierungen in Kampagnen mit Margin-Verwaltung) Die Bruttobudgetbegrenzung und das Budgetzeitintervall (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:** Das Optimierungsziel für das Paket. Beschreibungen der einzelnen Optimierungsziele finden Sie unter „Optimierungsziele [ Verwendung](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** Das Zielziel, mit dem die Leistung verfolgt wird.

>[!NOTE]
>
>Dieses Feld dient nur als Benchmark und wird nicht für Entscheidungen verwendet.

**[!UICONTROL Pace on]:** Die Grundlage für das Pacing:

* **[!UICONTROL Budget goal]:** (Standard) Diese Option liefert so viele Impressionen wie möglich innerhalb des zugewiesenen Budgets.

* **[!UICONTROL Impressions]:** Diese Option liefert Impressionen, bis innerhalb eines bestimmten Intervalls eine bestimmte Menge erreicht wird. Wenn Sie diese Option wählen, geben Sie die Anzahl der Impressionen und das Intervall an: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* oder *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** Das Maximum für 1000 Impressionen zu bezahlen.

**[!UICONTROL Flight pacing]:** (Platzierungen nur mit Geschwindigkeit auf Platzierungsebene) Platzierung des Versands von Anzeigen:

* *[!UICONTROL Even]:* (Standard) Verfolgt den Versand gleichmäßig auf jedem Flug, mit einem Ziel von 50 % der Lieferung in der ersten Hälfte des Fluges.

* *[!UICONTROL Slightly Ahead]:* (Standard) Beschleunigt die Zustellung, sodass nach der Hälfte der Flugdauer 55-65 % abgeschlossen sind.

* *[!UICONTROL Frontload]:* Beschleunigt die Lieferung, sodass nach der Hälfte des Fluges 65-75 % abgeschlossen sind.

* *[!UICONTROL Aggressive Frontload]:* Beschleunigt die Lieferung, sodass nach der Hälfte des Fluges 75-85 % abgeschlossen sind.

**[!UICONTROL Intraday pacing]:** (Platzierungen nur mit Geschwindigkeit auf Platzierungsebene) Schrittweise Platzierung der Anzeigenbereitstellung an jedem Tag im Flug:

* *[!UICONTROL Even]:* (Standard) Skaliert die Bereitstellung auf der Grundlage der Verfügbarkeit des Bestands. Im Allgemeinen werden mehr Anzeigen pro Stunde am Tag ausgeliefert, wenn das Auktionsvolumen höher ist, und weniger Anzeigen werden morgens und abends ausgeliefert.

* *[!UICONTROL ASAP]:* (Standard) Beschleunigt den Versand auf die doppelte Geschwindigkeit von *Gleichmäßig*.

  >[!CAUTION]
  >
  >Diese Option kann sich negativ auf die Leistung auswirken. Verwenden Sie sie nur, wenn Sie die Bereitstellung vollständig priorisieren und die Ausgaben der Leistungsoptimierung vorziehen.

**[!UICONTROL Placement Pre-bid Filters]:** (Optional) Bis zu fünf Filter, die erfüllt sein müssen, damit Gebote stattfinden. Sie können Pre-Bid-Filter als Optimierungstaktik verwenden. Beachten Sie jedoch, dass jede Regel die Möglichkeiten einschränken kann, für die diese Platzierung ein Angebot unterbreiten kann. So fügen Sie Filter hinzu oder bearbeiten sie:

1. Klicken Sie ![Bearbeiten](/help/dsp/assets/edit.png).
1. Führen Sie einen der folgenden Schritte aus:
   * So fügen Sie einen Filter hinzu:
      1. Klicken Sie auf **[!UICONTROL Add Filter]**.
      1. Wählen Sie neben **[!UICONTROL Only bid if]** eine Metrik aus und geben Sie dann einen Wert ein.
   * Um einen Filter zu entfernen, klicken Sie in der Filterzeile auf **[!UICONTROL X]** .
1. Klicken Sie auf **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Optional) Bestimmte Orte, an denen Anzeigen in die Platzierung ein- oder ausgeschlossen werden sollen. Wenn Sie keine Standorte angeben, werden alle Standorte als Ziel ausgewählt.

>[!NOTE]
>
>Orte in Städten und DMA sind für Roku-Platzierungen nicht verfügbar.

So geben Sie Standorte an:

1. Klicken Sie ![Bearbeiten](/help/dsp/assets/edit.png).
1. Führen Sie einen der folgenden Schritte aus:
   * So schließen Sie ein Land, ein Bundesland, eine Stadt, ein Bundesamt, einen Bundesgesetzgebungsbezirk oder einen Landesgesetzgebungsbezirk ein oder schließen diese aus:
      1. Wählen Sie den Standorttyp in der linken Spalte aus.
      1. (Bei Bedarf) Klicken Sie auf eine Position, um sie zu erweitern.
      1. Klicken Sie neben dem Speicherort auf *[!UICONTROL Include]* , um ihn als Ziel einzubeziehen, oder auf *[!UICONTROL Exclude]* , um ihn als Ziel auszuschließen.
   * So suchen Sie nach einer Postleitzahl und schließen alle ausgewählten Ergebnisse ein oder aus:
      1. Klicken Sie auf **[!UICONTROL Search Postal Code]**.
      1. Land auswählen.
      1. Geben Sie den Namen der Stadt ein und klicken Sie dann auf ![Bearbeiten](/help/dsp/assets/search.png).
      1. Klicken Sie auf das richtige Suchergebnis.
      1. Klicken Sie auf *[!UICONTROL Include All]* , um alle Standorte als Ziele einzubeziehen, oder auf *[!UICONTROL Exclude All]* , um alle Standorte als Ziele auszuschließen.
   * So geben Sie Postleitzahlen ein bzw. fügen sie ein und schließen alle ein oder aus:
      1. Klicken Sie auf **[!UICONTROL Paste Postal Code]**.
      1. Land auswählen.
      1. Bis zu 1000 Postleitzahlen eingeben oder einfügen.
Eine Postleitzahl pro Zeile einschließen oder mehrere Werte durch Kommas oder Tabulatoren getrennt eingeben.
      1. Klicken Sie auf *[!UICONTROL Include All]* , um alle Standorte als Ziele einzubeziehen, oder auf *[!UICONTROL Exclude All]* , um alle Standorte als Ziele auszuschließen.
   * Um einen Speicherort aus der [!UICONTROL Included]- oder [!UICONTROL Excluded] zu entfernen, klicken Sie auf **[!UICONTROL X]** neben dem Speicherort in der rechten Spalte.
1. Klicken Sie auf **[!UICONTROL Done]**.

>[!NOTE]
>
>* Nicht alle Länder verfügen über Bundesstaaten-, Stadt- oder Postleitzahlstandorte.
>* DMA (ausgewiesenes Marktgebiet), Federal Legislative Districts und State Legislative Districts sind nur für US-Standorte verfügbar.

## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Inventarquellen, die als Ziele ein- oder ausgeschlossen werden sollen. Bei den meisten Platzierungstypen sind standardmäßig alle Inventartypen und alle Quellen für jeden Typ enthalten. Für [!DNL Roku] Platzierungen müssen Sie den Inventartyp und die Quellen angeben. Sie können aus den folgenden Inventartypen auswählen:

* [!UICONTROL Public]: (Alle Platzierungstypen außer Roku) Alle offenen Exchange-Inventare, auf die DSP Zugriff hat. Sie können öffentliche Inventare ein- und ausschließen.

  Sie können die Liste nach Quelle oder Feed anzeigen. Wenn Sie die Liste nach Feed anzeigen, können Sie nach Feed-Name, Feed-Schlüssel oder einem ausgewählten charakteristischen Tag suchen.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: Ihre bestehenden privaten Angebote (oder bestehenden privaten [!DNL Roku] für [!DNL Roku] Platzierungen) mit Herausgebern, die Sie in DSP eingerichtet haben, und Ihre bestehenden [privaten Deal-Listen](/help/dsp/inventory/lists-deals-manage.md). Sie können öffentliche Inventare einbeziehen, aber nicht ausschließen.

  Auf der Registerkarte [!UICONTROL Deals] können Sie die Liste nach Keyword, Schlüssel, Angebots-ID oder benutzerdefiniertem Tag durchsuchen. Auf der Registerkarte &quot;[!UICONTROL Deal Lists]&quot; können Sie die Liste nach Name der Angebotsliste oder ID der Angebotsliste durchsuchen.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Optional) Überschreibt den Bid-Price-Algorithmus, um mindestens die Festpreise und Mindestpreise für Angebote zu bieten.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: Alle [Premium-, nicht garantierten [!UICONTROL On Demand]-](/help/dsp/inventory/on-demand-inventory-about.md) (oder [!UICONTROL On Demand] [!DNL Roku] für [!DNL Roku] Platzierungen), die Sie in [!DNL DSP] abonniert haben. Sie können [!UICONTROL On Demand] Inventar ein- und ausschließen.

  Sie können die Liste nach Quelle oder Feed anzeigen. Wenn Sie die Liste nach Feed anzeigen, können Sie nach Feed-Namen, Feed-Schlüssel oder einer ausgewählten Publisher-Region, einem Kategorie-Tag oder einem charakteristischen Tag suchen.

   * *[!UICONTROL Ensure Fixed or Floor Price for the bid]*: (Optional) Überschreibt den Bid-Price-Algorithmus, um mindestens die Festpreise und Mindestpreise für Angebote zu bieten.

So legen Sie die Inventar-Zielgruppenbestimmung fest:

* Um einen Inventartyp auszuschließen, deaktivieren Sie das Kontrollkästchen neben dem Namen.
* So wählen Sie einen Inventartyp aus:
   1. Aktivieren Sie das Kontrollkästchen neben dem Namen des Inventartyps.
   1. (Optional) Ändern Sie die Quellen, um Folgendes einzuschließen:
      1. Klicken Sie ![Bearbeiten](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] und [!UICONTROL On Demand] Inventar) Klicken Sie auf **[!UICONTROL View by Source]** oder **[!UICONTROL View by Feed]**, um zu ändern, wie die Quellen aufgeführt werden.
      1. Filtern Sie den Bestand nach Bedarf.
      1. Geben Sie die ein- und auszuschließenden Quellen an:
         * Für [!UICONTROL Public] oder [!UICONTROL On Demand]:
            * Um eine Quelle einzuschließen, klicken Sie **[!UICONTROL Include]** neben dem Quellnamen.
            * Um eine Quelle auszuschließen, klicken Sie **[!UICONTROL Exclude]** neben dem Quellnamen.
         * Für [!UICONTROL Private]:
            * Auf der Registerkarte [!UICONTROL Deals] :
               * Um den gesamten Bestand in ein Angebot aufzunehmen, klicken Sie **[!UICONTROL Include all]** neben dem Angebotsnamen.
               * Um eine einzelne Lagerbestandsquelle einzubeziehen, erweitern Sie den Abschlussnamen und klicken Sie dann auf das Kontrollkästchen neben dem Quellennamen.
            * Klicken Sie auf der Registerkarte [!UICONTROL Deal Lists] auf das Kontrollkästchen neben dem Namen der Angebotsliste.
   1. (Optional) Um eine CSV-Datei mit den Zielgruppenbestimmungsinformationen zum Download-Speicherort Ihres Browsers herunterzuladen, klicken Sie auf **[!UICONTROL Export]**.
   1. Klicken Sie auf **[!UICONTROL Save]**.

>[!TIP]
>
>Wenn Sie [!UICONTROL On Demand] Inventar abonniert haben, aber die Herausgeber oder Angebote für Target nicht finden können, überprüfen Sie den Status der Angebote. Weitere Informationen zu Status finden Sie unter [Über [!DNL On Demand] Premium-Inventar](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Video targeting]:** Zielbestand (aber nicht ausschließen) nach Inventarattributen. Wenn Sie mehrere Werte für dasselbe Videoattribut auswählen, kann jedes der ausgewählten Attribute als Ziel ausgewählt werden (z. B. \[Player-Größe = groß ODER Player-Größe = HD\]). Wenn mehrere Attribute ausgewählt werden, muss jedes der angegebenen Attribute vorhanden sein (z. B. \[Dauer = 30-60 min] UND \[Player-Größe = groß ODER Player-Größe = HD\]).

* **[!UICONTROL Player size]:** Zielinventar (aber nicht ausschließen) nach Player-Größe. Diese Einstellung gilt für Preroll-Platzierungen, standardmäßige mobile Preroll-Platzierungen und universelle Video-Platzierungen für Desktop- und Mobile-Umgebungen. Standardmäßig sind alle Größen ausgewählt. Um die Zielgruppen einzugrenzen, wählen Sie bestimmte Zielgrößen und/oder *Unbekannt* aus.

* **[!UICONTROL Playback mode]:** Zielinventar (aber nicht ausschließen) durch die Art und Weise, wie die Wiedergabe gestartet wird. Diese Einstellung gilt für Preroll-Platzierungen, standardmäßige mobile Preroll-Platzierungen und universelle Video-Platzierungen für Desktop- und Mobile-Umgebungen. Standardmäßig werden alle Modi als Ziel ausgewählt. Um die Zielgruppen einzugrenzen, wählen Sie bestimmte Zielmodi und/oder *Unbekannt* aus.

* **[!UICONTROL Skippability]:** Zielbestand (aber nicht ausschließen), je nachdem, ob er übersprungen werden kann oder nicht. Diese Einstellung gilt für alle VAST/VPAID-Platzierungen, einschließlich Preroll, Standard-Mobile-Preroll, Connected TV und Universal Video-Platzierungen. Standardmäßig sind alle Optionen ausgewählt. Um die Ziele einzugrenzen, wählen Sie bestimmte Ziele und/oder *Unbekannt* aus.

**[!UICONTROL Position targeting]:** Zielbestand (aber nicht ausschließen) nach Anzeigenposition. Diese Einstellung gilt für alle VAST/VPAID-Platzierungen, einschließlich Preroll, Standard-Mobile-Preroll, Connected TV und Universal Video-Platzierungen. Standardmäßig werden alle Positionen als Zielgruppen ausgewählt. Um die Zielgruppen einzugrenzen, wählen Sie bestimmte Zielpositionen und/oder *Unbekannt* aus.

## [!UICONTROL Site and App Targeting]

**[!UICONTROL Traffic type]:** Die Traffic-Typen an die Zielgruppe. Zu den Optionen gehören **[!UICONTROL Websites]** und **[!UICONTROL Apps]**.

**[!UICONTROL Tier]:** (Verfügbar, wenn **[!UICONTROL Paste list of targeted sites]** *[!UICONTROL Off]* ist) Die Qualität des Traffics auf das Ziel. Die Stufen 1 bis 3 sind markensicher und wurden vom DSP-Zuordnungsteam genehmigt.

* *[!UICONTROL Tier 1]:* Premium-Websites und -Anwendungen, die landesweit anerkannt sind.

* *[!UICONTROL Tier 2]:* Targeting von Tier 1 sowie von qualitativ hochwertigen Sites und Anwendungen, die weniger bekannt sind als Tier 1.

* *[!UICONTROL Tier 3]:* Targeting von Tiers 1-2 sowie legitimen und markensicheren Websites und Anwendungen, die auf eine Nischenzielgruppe zugeschnitten sind. Verwenden Sie Ebene 3 für Reichweiten- oder Daten-Targeting-Käufe.

* *[!UICONTROL All Sites or Apps]:* Targeting von Ebenen 1-3 und neuem Inventar, das nicht gefiltert oder kategorisiert wurde, was Sie für die Reichweite verwenden können.

>[!NOTE]
>
>Der Bestand ist spezifisch für die Werbeeinheiten in der Platzierung.

>[!TIP]
>
>Für Leistungskampagnen ist es am besten, *[!UICONTROL All Sites]* auszuwählen.

**[!UICONTROL Site or App Categories]:** (Optional; verfügbar, wenn **[!UICONTROL Paste list of targeted sites]** *[!UICONTROL Off]* ist) Websitekategorien innerhalb der ausgewählten Website-Ebenen, die als Ziele ein- oder ausgeschlossen werden sollen (aber nicht beide). Wählen Sie aus den vertikalen Site-Listen aus, die DSP basierend auf dem Betreff zugeordnet hat:

1. Klicken Sie ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die einzuschließenden oder auszuschließenden Site-Kategorien an:
   * So schließen Sie Site-Kategorien ein:
      1. Klicken Sie auf **[!UICONTROL Include categories]**.
      1. Aktivieren Sie das Kontrollkästchen neben jeder Kategorie, die Sie ansprechen möchten.
   * Ausschließen von Site-Kategorien:
      1. Klicken Sie auf **[!UICONTROL Exclude categories]**.
      1. Aktivieren Sie das Kontrollkästchen neben den einzelnen auszuschließenden Kategorien.
1. (Optional) Um eine CSV-Datei mit den Zielgruppenbestimmungsinformationen zum Download-Speicherort Ihres Browsers herunterzuladen, klicken Sie auf **[!UICONTROL Export]**.
1. Klicken Sie auf **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites or Apps]:** (Optional; verfügbar, wenn **[!UICONTROL Paste list of targeted sites]** *[!UICONTROL Off]* ist) Auszuschließende Sites/Apps und [URL-](/help/dsp/resources/lists-url-manage.md). Auf der Registerkarte [!UICONTROL Paste URL] können Sie nach Sites suchen und diese auswählen oder Domain-Namen eingeben oder einfügen. Auf der Registerkarte [!UICONTROL URL Lists] können Sie URL-Listen auswählen.

1. Klicken Sie ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die Sites an:
   * Auf der Registerkarte [!UICONTROL Paste URL] :
      * So suchen Sie nach einer Site:
         1. Klicken Sie auf **[!UICONTROL Search]**.
         1. Geben Sie einen Suchbegriff ein, wählen Sie eine Site-Ebene und/oder eine Site-Kategorie aus.
         1. Wählen Sie in den Suchergebnissen die auszuschließenden Websites aus:
            * Um ein einzelnes Gebiet auszuschließen, aktivieren Sie das entsprechende Kontrollkästchen.
            * (Wenn mehr als 50 Ergebnisse verfügbar sind) Um die ersten 50 Ergebnisse auszuschließen, klicken Sie auf **[!UICONTROL Exclude these 50]**. Um alle Suchergebnisse auszuschließen, klicken Sie auf **[!UICONTROL Exclude these \<*NN *\>]**.
      * Domain-Namen eingeben:
         1. Klicken Sie auf **[!UICONTROL Paste]**.
         1. Geben Sie einen oder mehrere Domain-Namen in separaten Zeilen ein.
         1. Klicken Sie auf **[!UICONTROL Exclude All]**.
   * Auf der Registerkarte [!UICONTROL URL Lists] :
      1. (Optional) Suchen Sie nach einer URL-Liste, indem Sie den Listennamen ganz oder teilweise in das Suchfeld eingeben.
      1. Aktivieren Sie das Kontrollkästchen neben jeder auszuschließenden URL-Liste.
1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Done]** .

>[!NOTE]
>
>* Zusätzlich zur DSP-Liste (Global Blockierte Site-Liste), die Sites umfasst, die als [ für Anzeigen gelten](/help/dsp/introduction/features/brand-safety-media-quality.md) werden auch Listen auf Konto- und Advertiser-Ebene angewendet.
>* Listen blockierter Sites setzen zielgerichtete Sites und Site-Listen immer außer Kraft. Wenn eine Platzierung dieselbe Zielgruppe für eine Anzeige sowohl ausschließt als auch enthält, wird die Zielgruppe ausgeschlossen.

**[!UICONTROL Language]:** (Optional) Eine einzelne Sprache zum Auswählen.

**[!UICONTROL Site or app list preview]:** (Schreibgeschützt) Alle für die Platzierung ausgewählten und blockierten Websites/Apps, einschließlich Websites/Apps auf Kontoebene, Advertiser-Ebene und globaler Listen blockierter DSP-Websites.

Optional können Sie die Liste der zielgerichteten und blockierten Websites als CSV-Datei (CSV) exportieren. Um die Liste zu exportieren, klicken Sie auf **[!UICONTROL Export full site list]** und öffnen oder speichern Sie die Datei dann entsprechend dem normalen Verfahren Ihres Browsers.

**[!UICONTROL Allow unscreened sites]:** (Nur Standardplatzierungen für Anzeigen) Aktiviert die Bereitstellung von Anzeigen auf nicht geprüften Sites. Wenn die Platzierung auf ein privates Inventar abzielt, kann diese Option Anzeigen auf blockierten Websites bereitstellen.

**[!UICONTROL Paste list of targeted sites]:** Ermöglicht das Targeting nur für bestimmte Sites. Wenn Sie diese Option aktivieren, sind die anderen Site-Targeting-Optionen deaktiviert.

**[!UICONTROL Sites or Apps]:** (verfügbar, wenn **[!UICONTROL Paste list of targeted sites]** ist *[!UICONTROL On]*) Zu adressierende Sites. Auf der Registerkarte [!UICONTROL Paste URL] können Sie nach Sites suchen und diese auswählen oder Domain-Namen eingeben oder einfügen. Auf der Registerkarte [!UICONTROL URL Lists] können Sie URL-Listen auswählen.

1. Klicken Sie ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die Sites an:
   * Auf der Registerkarte [!UICONTROL Paste URL] :
      * So suchen Sie nach einer Site:
         1. Klicken Sie auf **[!UICONTROL Search]**.
         1. Geben Sie einen Suchbegriff ein, wählen Sie eine Site-Ebene und/oder eine Site-Kategorie aus.
         1. Wählen Sie in den Suchergebnissen die einzuschließenden Websites aus:
            * Um eine einzelne Site einzubeziehen, aktivieren Sie das angrenzende Kontrollkästchen.
            * (Wenn mehr als 50 Ergebnisse verfügbar sind) Um die ersten 50 Ergebnisse einzubeziehen, klicken Sie auf **[!UICONTROL Include these 50]**. Um alle Suchergebnisse einzubeziehen, klicken Sie auf **[!UICONTROL Include these \<*NN *\>]**.
      * Domain-Namen eingeben:
         1. Klicken Sie auf **[!UICONTROL Paste]**.
         1. Geben Sie einen oder mehrere Domain-Namen in separaten Zeilen ein.
         1. Klicken Sie auf **[!UICONTROL Include All]**.
   * Auf der Registerkarte [!UICONTROL URL Lists] :
      1. (Optional) Suchen Sie nach einer URL-Liste, indem Sie den Listennamen ganz oder teilweise in das Suchfeld eingeben.
      1. Aktivieren Sie das Kontrollkästchen neben jeder einzuschließenden URL-Liste.
1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Done]** .

>[!NOTE]
>
>* Zusätzlich zur DSP-Liste (Global Blockierte Site-Liste), die Sites umfasst, die als [ für Anzeigen gelten](/help/dsp/introduction/features/brand-safety-media-quality.md) werden auch Listen auf Konto- und Advertiser-Ebene angewendet.
>* Listen blockierter Sites setzen zielgerichtete Sites und Site-Listen immer außer Kraft. Wenn eine Platzierung dieselbe Zielgruppe für eine Anzeige sowohl ausschließt als auch enthält, wird die Zielgruppe ausgeschlossen. Sie können entweder nach Sites suchen und diese auswählen oder Domain-Namen eingeben oder einfügen:

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Alle Zielgruppenziele für die Platzierung, einschließlich [Drittanbietersegmente, Erstanbietersegmente, Adobe-Segmente, benutzerdefinierte Segmente und gespeicherte Zielgruppen](/help/dsp/audiences/audience-settings.md). Außerdem wird die gesamte und aktive deduplizierte Zielgruppengröße für alle ausgewählten Segmente und gespeicherten Zielgruppen angezeigt. Sie können eine vorhandene Zielgruppe auswählen, eine Zielgruppe erstellen, die Sie später wiederverwenden können, oder bestimmte Zielgruppensegmente auswählen:

* Um eine vorhandene Audience auszuwählen, klicken Sie ![Auswählen](/help/dsp/assets/chevron-down.png) neben [!UICONTROL Included Audiences] und wählen Sie dann die Audience aus.
* Um eine Audience zu erstellen, klicken Sie ![Auswählen](/help/dsp/assets/chevron-down.png) neben [!UICONTROL Included Audiences] und wählen Sie dann **[!UICONTROL + Create Audience]** aus. Anweisungen finden Sie unter [Erstellen einer wiederverwendbaren Zielgruppe](/help/dsp/audiences/reusable-audience-create.md), beginnend mit Schritt 3.
* Um bestimmte Zielgruppensegmente auszuwählen, klicken Sie auf **[!UICONTROL Select segments for this placement only]**. Wählen Sie die Segmentlogik aus. Anweisungen finden Sie in Schritt 6 unter &quot;[ einer wiederverwendbaren Zielgruppe](/help/dsp/audiences/reusable-audience-create.md). Wenn Sie fertig sind, klicken Sie auf **Speichern**.

**[!UICONTROL Excluded Audiences]:** Alle Zielgruppen, die für die Platzierung ausgeschlossen werden sollen, einschließlich Zielgruppen mit [Drittanbietersegmenten, Erstanbietersegmenten, Adobe-Segmenten, benutzerdefinierten Segmenten und gespeicherten Zielgruppen](/help/dsp/audiences/audience-settings.md). Außerdem wird die gesamte und aktive deduplizierte Zielgruppengröße für alle ausgeschlossenen Zielgruppen angezeigt. Sie können eine vorhandene Zielgruppe auswählen oder eine neue Zielgruppe erstellen, die Sie später wiederverwenden können:

* Um eine vorhandene Audience auszuwählen, klicken Sie ![Auswählen](/help/dsp/assets/chevron-down.png) neben [!UICONTROL Excluded Audiences] und wählen Sie dann die Audience aus.

* Um eine Zielgruppe zu erstellen, klicken Sie ![Auswählen](/help/dsp/assets/chevron-down.png) neben [!UICONTROL Excluded Audiences] und wählen Sie dann **+ Zielgruppe erstellen aus**. Anweisungen finden Sie unter [Erstellen einer wiederverwendbaren Zielgruppe](/help/dsp/audiences/reusable-audience-create.md), beginnend mit Schritt 3.

**[!UICONTROL Targeting]:** Die Typen der anzuvisierenden Benutzer-IDs. Sie können diese Einstellung nicht ändern, nachdem die Platzierung live ist (d. h. nachdem der Flug begonnen hat).

Wenn Sie sowohl ältere als auch universelle IDs auswählen, erhalten universelle IDs Vorrang für Gebote.

* *[!UICONTROL Legacy IDs (Cookies, MAIDS, CTV)]*: (Standard) Targeting von Benutzern basierend auf ihren Cookies, IDs für mobile Werbung oder Connected TV-IDs (CTV). IDs werden basierend auf dem Browser-, In-App- oder CTV-Inventar ausgewählt.

* *[!UICONTROL Universal ID Beta]*: Targeting von IDs mit Fokus auf den Benutzerdatenschutz; Auswahl eines ID-Typs. Die verfügbaren Optionen werden durch die ausgewählten geografischen Ziele im Abschnitt [!UICONTROL Geo-Targeting] bestimmt. Verwenden Sie mit [[!DNL RampID] direkt in DSP importierten Segmenten](/help/dsp/audiences/sources/source-import-liveramp-segments.md), [Segmenten, für die DSP Ihre personenbezogenen Daten in universelle IDs konvertiert](/help/dsp/audiences/sources/source-about.md) oder [benutzerdefinierten Segmenten, die universelle IDs verfolgen](/help/dsp/audiences/custom-segment-create.md).

   * *[!UICONTROL ID5]*: Zielgruppen [!DNL ID5] IDs, die wahrscheinlich aus E-Mail-Adressen und anderen Signalen erstellt wurden.<!-- What countries/geos are these available for? Everywhere?--> ID5-IDs sind kostenlos verfügbar. **Hinweis:** Drittanbietersegmente aus [!DNL Eyeota] können ID5-IDs enthalten.

   * *[!UICONTROL RampID]*: Targeting [!DNL LiveRamp] [!DNL RampIDs] von Benutzern, die über ihre E-Mail-Adressen bei Ihrer Website angemeldet sind.<!-- Verify --> [!DNL RampIDs] sind für Benutzer in Nordamerika, Australien und Neuseeland verfügbar.

   * *[!UICONTROL Unified ID2.0]*: Targeting [!DNL Unified ID2.0] (UID2)-IDs von Benutzern, die über ihre E-Mail-Adressen bei Ihrer Website angemeldet sind.<!-- Verify -->[!DNL UID2 IDs] sind im Europäischen Wirtschaftsraum und in einigen weiteren Ländern nicht verfügbar. Siehe die [Liste der Länder, für die ein Verbot gilt](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

  **[!UICONTROL Terms of service]**: Die Nutzungsbedingungen für die Verwendung universeller IDs. Sie oder ein anderer Benutzer im DSP-Konto muss die Bedingungen nur einmal akzeptieren, bevor Sie Daten in einen neuen ID-Typ konvertieren können. Für Kunden mit verwalteten Service-Verträgen wird Ihr Adobe-Account-Team Ihre Zustimmung einholen und die Bedingungen im Namen Ihres Unternehmens akzeptieren. Um die Bedingungen zu lesen, klicken Sie auf **>**. Um die Bedingungen zu akzeptieren, scrollen Sie zum Ende der Bedingungen und klicken Sie auf **[!UICONTROL Accept]**.

**[!UICONTROL Cross Device Targeting]:** (Verfügbar, wenn die [Kampagne für personenbasiertes geräteübergreifendes Targeting konfiguriert ist](/help/dsp/campaign-management/campaigns/campaign-settings.md) nur für ältere IDs (nicht für universelle IDs), und Sie wählen mindestens ein Segment oder eine Audience aus. Ermöglicht die Erweiterung der Zielgruppenbestimmung auf alle bekannten Geräte einer Person (gemäß dem in den Kampagneneinstellungen angegebenen Gerätediagramm), auch auf Geräte, die nicht in den angegebenen Segmenten enthalten sind. Je nach dem für die Kampagne angegebenen Diagramm können Gebühren anfallen. Gerätediagrammdaten sind nur in Nordamerika verfügbar.

**[!UICONTROL Placement Cap]:** (Optional) Die Häufigkeit, mit der ein eindeutiges Gerät, eine universelle ID oder eine Person (je nach dem für die Kampagne angegebenen [!UICONTROL Cross Device Level] und der [!UICONTROL Targeting] der Platzierung) Anzeigen aus der Platzierung erhalten kann. Zu den Optionen gehören *[!UICONTROL Unlimited]* oder ein bestimmter Betrag pro Tag, Woche oder Monat.

>[!NOTE]
>
> Sie können Häufigkeitsbegrenzungen auf Kampagnen-, Paket- und Platzierungsebene festlegen. DSP berücksichtigt die strengste Häufigkeitsbegrenzung in der Kampagnenhierarchie.

**[!UICONTROL Secondary Cap]:** (Optional; verfügbar, wenn Sie eine numerische [!UICONTROL Placement Cap] einbeziehen) Eine zusätzliche Einschränkung innerhalb der Grenzen der primären Platzierungs-Begrenzung. Wählen Sie die Anzahl der Impressionen und den Zeitraum aus (z. B. 3 pro 12 Stunden).

**[!UICONTROL Day Parting]:** (Optional) Bestimmte Wochentage und Tageszeiten, an denen Anzeigen geschaltet werden können. So legen Sie DayParting-Intervalle fest:

1. Klicken Sie ![Bearbeiten](/help/dsp/assets/edit.png).
1. Wählen Sie die entsprechende Zeitzone aus.
1. Geben Sie die Intervalle an:
   * Um ein voreingestelltes Intervall auszuwählen, klicken Sie auf eine der Intervall-Schaltflächen. Zu den Optionen gehören *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]* oder *[!UICONTROL Prime]* (Primetime).
   * Um ein Intervall manuell auszuwählen, klicken Sie in eine Zelle und ziehen Sie optional, um das Intervall auszuwählen.
1. Klicken Sie auf **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Optional; für Werbetreibende verfügbar, die mit [!DNL Proximic by Comscore] Segmenten konfiguriert sind) Spezifische Segmentnamen oder IDs von [!DNL Proximic by Comscore], die als Ziele einbezogen werden sollen. Für diese Funktion können zusätzliche Gebühren anfallen. Wenden Sie sich an Ihr Adobe-Account-Team, um diese Funktion zu aktivieren und Themensegmente einzurichten.

So geben Sie die Themenzielgruppe an:

1. Klicken Sie ![Bearbeiten](/help/dsp/assets/edit.png).
1. Segmente angeben, die angesprochen werden sollen:
   1. Wählen Sie in der linken Spalte den Partner aus: (*[!UICONTROL Comscore]*.
   1. Geben Sie im Eingabefeld die Segmentnamen oder Segment-IDs ein.
1. (Optional) Um eine CSV-Datei mit den Themeninformationen zum Download-Speicherort Ihres Browsers herunterzuladen, klicken Sie auf **[!UICONTROL Export]**.
1. Klicken Sie auf **[!UICONTROL Save]**.

>[!TIP]
>
>* Themen-Targeting begrenzt den Bestand, auf dem die Platzierung Gebote abgeben kann. Verwenden Sie daher Themen-Targeting nur für einen kleinen Prozentsatz Ihres Gesamtkaufs.
>
>* Richten Sie eine beliebige negative Zielgruppenbestimmung innerhalb des Segments auf [!DNL Proximic by Comscore] ein.

**[!UICONTROL Device Targeting]:** (Optional) Spezifische Geräteinformationen, einschließlich Gerätetypen, Hersteller, Betriebssysteme, Browser und Konnektivitätstypen, die als Ziele ein- und ausgeschlossen werden sollen. Die Typen variieren je nach Platzierungstyp. So geben Sie das Geräte-Targeting an:

1. Klicken Sie ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die ein- und auszuschließenden Gerätedetails an:
   1. Wählen Sie in der linken Spalte die Kategorie aus.
   1. Zielgruppenbestimmung angeben:
      * Um einen Wert einzuschließen, klicken Sie **[!UICONTROL Include]** neben dem Wertnamen.
      * Um einen Wert auszuschließen, klicken Sie **[!UICONTROL Exclude]** neben dem Wertnamen.
1. (Optional) Um eine CSV-Datei mit Informationen zum Zielgruppenbestimmungsgerät in den Download-Speicherort Ihres Browsers herunterzuladen, klicken Sie auf **[!UICONTROL Export]**.
1. Klicken Sie auf **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Optional) Bestimmte Internet-Service-Provider (ISPs), die als Ziele ein- oder ausschließen (aber nicht beide) sollen. So geben Sie das ISP-Targeting an:

1. Klicken Sie ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die ein- oder auszuschließenden ISPs an:
   * So schließen Sie ISPs ein:
      1. Klicken Sie auf **[!UICONTROL Include ISPs]**.
      1. (Optional) Filtern Sie die Liste nach Keyword.
      1. Aktivieren Sie das Kontrollkästchen neben jedem zu kontaktierenden ISP.
   * So schließen Sie ISPs aus:
      1. Klicken Sie auf **[!UICONTROL Exclude ISPs]**.
      1. (Optional) Filtern Sie die Liste nach Keyword.
      1. Aktivieren Sie das Kontrollkästchen neben jedem auszuschließenden ISP.
1. (Optional) Um eine CSV-Datei mit den ISP-Zielgruppeninformationen zum Download-Speicherort Ihres Browsers herunterzuladen, klicken Sie auf **[!UICONTROL Export]**.
1. Klicken Sie auf **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Quality]

**[!UICONTROL DoubleVerify ABS segment ID]:** (Optional; nur [!DNL DoubleVerify] Kunden; verfügbar für Desktop-Pre-Roll, Standard- und Click-to-Play-Anzeige und nur native Anzeige- und Video-Platzierungen; nicht unterstützt für [Standardmäßige programmgesteuerte garantierte Platzierungen für Angebote](/help/dsp/inventory/programmatic-guaranteed-about.md)) Eine [!DNL DoubleVerify Authentic Brand Safety] Segment-ID, die mit dem [!DNL DoubleVerify]-Konto des Unternehmens verknüpft ist, das für die Platzierung verwendet werden soll. Durch die Angabe einer ID werden Impressionen nach dem Angebot anhand der benutzerdefinierten Markensicherheitsregeln blockiert, die für die angegebene Segment-ID konfiguriert sind. DSP stellt Ihrem Konto die Nutzung der Segment-ID in Rechnung.

Die ID muss mit „51“ beginnen und aus acht Ziffern bestehen. Wenn in den Einstellungen des Advertiser-Kontos eine Segment-ID angegeben ist, wird standardmäßig die ID auf Advertiser-Ebene eingegeben. Sie können die ID jedoch ändern, um ein anderes Segment zu verwenden, oder die ID löschen, um die Funktion zu deaktivieren.

**[!UICONTROL Contextual filtering]:** (gilt für Desktop- und mobile Web-Anzeigen, native und Video-Anzeigen) Typen von [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] und [!DNL Peer39] anzuwendenden kontextuellen Filtern. Die Standardeinstellungen auf Advertiser-Ebene sind für neue Platzierungen ausgewählt, Sie können jedoch die Einstellungen ändern:

<!-- Looks like we didn't rename this:
**[!UICONTROL Brand Safety categories]:** Types of [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], and [!DNL Peer39] brand safety category filters to apply. The advertiser-level defaults are selected for new placements, but you can change the settings:
-->

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Optional) Ein oder mehrere Arten von Inventarkontext, der standardmäßig blockiert werden soll. Es können zusätzliche Gebühren anfallen.

* [!UICONTROL Peer 39]:

   * **Target-Sites, die Folgendes sind:** (Optional) Mindestens ein Typ von Inventarattributen, die standardmäßig als Ziel ausgewählt werden sollen. Es können zusätzliche Gebühren anfallen.

* [!UICONTROL ComScore]:

   * **Sites blockieren, die Folgendes sind:** (Optional) Mindestens ein Typ von Inventarattributen, die standardmäßig blockiert werden sollen. Es können zusätzliche Gebühren anfallen.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Optional) Der Grad von Inhalten für Erwachsene, für die Anzeigen standardmäßig blockiert werden sollen: *[!UICONTROL Do Not Block]* (Standard), *[!UICONTROL Standard]* oder *[!UICONTROL Strict]*. Es können zusätzliche Gebühren anfallen.

   * **[!UICONTROL Alcohol Content]:** (Optional) Der Alkoholgehalt, für den Anzeigen standardmäßig blockiert werden sollen: *[!UICONTROL Do Not Block]* (Standard), *[!UICONTROL Standard]* oder *[!UICONTROL Strict]*. Es können zusätzliche Gebühren anfallen.

**[!UICONTROL Pre-bid fraud blocking]:** Arten von Websites, die aufgrund von betrügerischem Traffic und verdächtigen Aktivitäten blockiert werden sollen, die über [!DNL DoubleVerify], [!DNL Integral Ad Science] und [!DNL Peer39] gemessen werden. Die Standardeinstellungen auf Advertiser-Ebene sind für neue Platzierungen ausgewählt, Sie können jedoch die Einstellungen ändern:

* [!UICONTROL DoubleVerify]: (Gilt für Desktop- und mobile Web-Anzeigen, native Video- und Standard-TV-Anzeigen)

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** blockiert standardmäßig den gesamten zu 100 % ungültigen Traffic für neue Platzierungen, einschließlich Traffic auf entführten Geräten. Es können zusätzliche Gebühren anfallen.

   * **[!UICONTROL Also block sites with]:** (Optional) Eine zusätzliche Ebene von Betrug und ungültigem Traffic, die dazu führt, dass DSP Anzeigen standardmäßig blockiert: *[!UICONTROL None]* (die Standardeinstellung, die zusätzlichen Traffic nicht blockiert), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* oder *[!UICONTROL >25% Average Fraud/IVT levels]*. Es können zusätzliche Gebühren anfallen.

* [!UICONTROL Peer 39]: (Gilt für Desktop- und mobile Web-Anzeigen, native Anzeigen und Videoanzeigen)

   * **[!UICONTROL Block sites that are]:** (Optional) Eine oder mehrere Betrugsarten, die dazu führen, dass DSP Anzeigen standardmäßig blockiert: *[!UICONTROL Fraud]* (blockiert alle betrügerischen Websites), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* und/oder *[!UICONTROL Fraud: Zero Ads]*. Es können zusätzliche Gebühren anfallen.

* [!UICONTROL Integral Ad Science]: (Gilt für Desktop- und mobile Web-Anzeigen, native Anzeigen und Videoanzeigen)

   * **[!UICONTROL Block sites that are]:** (Optional) Ein Typ einer verdächtigen Website- oder App-Aktivität, der dazu führt, dass DSP Anzeigen standardmäßig blockiert: *[!UICONTROL None]* (der Standard, der Anzeigen nicht aufgrund verdächtiger Aktivitäten blockiert), *[!UICONTROL Suspicious Activity - High Risk]* oder *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Es können zusätzliche Gebühren anfallen.

**[!UICONTROL Pre-bid viewability]:** (Gilt für Desktop- und mobile Web-Anzeigen, native und Video-Anzeigen) Welche Pre-Bid-Sichtbarkeitsfilter nach [!DNL DoubleVerify] filtern und [!DNL Integral Ad Science] für die Platzierung beantragen. Die Standardeinstellungen auf Advertiser-Ebene sind für neue Platzierungen ausgewählt, Sie können jedoch die Einstellungen ändern. Es können zusätzliche Gebühren anfallen.

**[!UICONTROL Ads.txt filtering]:** (gilt für Desktop- und mobile Web-Anzeigen, native Video- und Audio-Anzeigen) Welche Ebene von [Ads.txt](https://iabtechlab.com/ads-txt-about/) Vorangebotfilterung ist zu verwenden, indem die Liste der autorisierten digitalen Verkäufer jedes Herausgebers angewendet wird. Der Standardwert auf Advertiser-Ebene wird für neue Platzierungen ausgewählt, Sie können jedoch die Einstellungen ändern:

* *[!UICONTROL Opt out of ads.txt (default)]*: Zu kaufen Inventar von allen Verkäufern.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Priorisierung des Kaufbestands bei den autorisierten Direktverkäufern und Wiederverkäufern einer Domain.
* *[!UICONTROL Ads.txt sellers only]*: Zum Kauf des Inventars nur von den autorisierten Direktverkäufern und Wiederverkäufern einer Domain.
* *[!UICONTROL Ads.txt sellers only]*: Um Inventar nur von den autorisierten Direktverkäufern einer Domain zu kaufen.

**[!UICONTROL Attention Targeting]:** (Gilt für Desktop- und mobile Web-Anzeige, Video und standardmäßig verbundene TV-Anzeigen) Zielt [!DNL Adelaide], Segmente basierend auf der angegebenen Website, dem Format und der Anzeigengröße vorab mit einem bestimmten Aufmerksamkeitsgrad (hoch, mittel oder niedrig) anzubieten. Die Segmente werden wöchentlich aktualisiert. **Hinweis** Bei der Verwendung [!DNL Adelaide] Zielgruppensegmente fallen für jede Impression, die mit [!DNL Adelaide] Zielgruppenbestimmung zugestellt wird, CPM-Gebühren an. Diese Gebühren sind von den Gebühren für die [Aufmerksamkeitsmessung“ ](/help/dsp/campaign-management/campaigns/campaign-settings.md). Für interaktive Pre-Roll-Platzierungen werden Ihnen nur VAST-Impressions berechnet.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] Platzierungen) Von [!DNL Roku] genehmigte Drittanbieter für Tracking sind [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Placed], [!DNL Oracle], [!DNL Polk] und [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (Optional) Ereignisverfolgungs-Pixel von Drittanbietern, die standardmäßig an alle neuen Anzeigen in der Platzierung angehängt werden sollen. So geben Sie Ereignispixel an:

1. Klicken Sie ![Bearbeiten](/help/dsp/assets/edit.png).
1. Führen Sie einen der folgenden Schritte aus:
   * Um ein vorhandenes Pixel auszuwählen, aktivieren Sie das Kontrollkästchen in der Pixelzeile.
   * So erstellen Sie ein Pixel:
      1. Klicken Sie auf **[!UICONTROL Create]**.
      1. Geben Sie die folgenden Informationen ein:
         * **[!UICONTROL Pixel name]:** Der Pixelname; die maximale Länge beträgt 500 Zeichen. Verwenden Sie einen Namen, der Ihnen die Identifizierung des Pixels erleichtert.
         * **[!UICONTROL Pixel event fires on]:** Das Ereignis, durch das das Pixel zum Auslösen Trigger wird. Die verfügbaren Ereignisse variieren je nach Anzeigentyp.
         * **[!UICONTROL Pixel type]:** Gibt an, ob das Pixel ein *[!UICONTROL IMG URL]* (Bilddatei mit 1 x 1 Pixel), *[!UICONTROL HTML]* oder *[!UICONTROL JavaScript URL]* ist.
         * **[!UICONTROL Pixel URL]:** Die URL des Pixelbilds.
      1. Klicken Sie auf **[!UICONTROL Create and attach]**.
   1. Klicken Sie auf **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (Optional) Konversionsverfolgungspixel, die standardmäßig an alle neuen Anzeigen in der Platzierung angehängt werden sollen. So legen Sie Konvertierungspixel fest:

1. Klicken Sie ![Bearbeiten](/help/dsp/assets/edit.png).
1. Führen Sie einen der folgenden Schritte aus:
   * Um ein vorhandenes Pixel auszuwählen, aktivieren Sie das Kontrollkästchen in der Pixelzeile.
   * So erstellen Sie ein Pixel:
      1. Klicken Sie auf **[!UICONTROL Create]**.
      1. Geben Sie die folgenden Informationen ein:
         * **[!UICONTROL Conversion pixel name]:** Der Pixelname; die maximale Länge beträgt 500 Zeichen. Verwenden Sie einen Namen, der Ihnen die Identifizierung des Pixels erleichtert.
         * **[!UICONTROL Conversion category]:** Der Konvertierungstyp.
         * **[!UICONTROL Impression conversion window]:** Die Anzahl der Tage nach Eintritt einer Anzeigenimpression, in denen die Impression einer Konversion zugeordnet werden kann. Der Standardwert ist 30 Tage.
         * **[!UICONTROL Click conversion window]:** Die Anzahl der Tage nach dem Klicken auf eine Anzeige, in denen der Klick einer Konversion zugeordnet werden kann. Der Standardwert ist 30 Tage.
         * **[!UICONTROL Notes]:** (Optional) Eine Beschreibung oder andere Informationen zum Pixel.
      1. Klicken Sie auf **[!UICONTROL Create and attach]**.
      1. Implementieren Sie das Konvertierungspixel auf den entsprechenden Web-Seiten:
         1. Navigieren Sie im Hauptmenü zu **[!UICONTROL Resources]** > **[!UICONTROL Conversion pixels]**.
         1. Klicken Sie in der Pixelzeile auf **[!UICONTROL edit]**.
         1. Kopieren Sie die Werte in die Felder [!UICONTROL HTML Tag] und [!UICONTROL Flash Tag] nach Bedarf, um sie dem Advertiser oder Website-Kontakt zur Verfügung zu stellen.

            Möglicherweise muss die IT-Abteilung oder andere Gruppe des Werbetreibenden die Tag-Bereitstellung planen oder darüber informiert werden.
   1. Klicken Sie auf **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Optional) Ein statischer Gebührensatz eines Drittanbieters, der als nicht fakturierbare Kosten pro 1000 Impressionen verfolgt werden soll. Der Standardwert auf Paketebene wird bei neuen Platzierungen automatisch angewendet, sofern zutreffend, es sei denn, Sie geben einen anderen Wert ein.

>[!NOTE]
>
>Fakturierbare Gebühren werden in der [!UICONTROL Net CPM] Metrik angezeigt.

>[!MORELIKETHIS]
>
>* [Über die Platzierungsverwaltung](placement-about.md)
>* [Platzierung erstellen](placement-create.md)
>* [Platzierungen bearbeiten](placement-edit.md)
>* [Angebotsmultiplikatoren für Platzierungen verwalten](placement-manage-bid-multipliers.md)
>* [Anzeigen des Änderungsprotokolls für eine Platzierung](placement-change-log.md)
>* [Tastaturbefehle](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Häufig gestellte Fragen zur Kampagnenverwaltung](/help/dsp/campaign-management/faq-campaign-management.md)
