---
title: Überblick über Campaign Management in Advertising DSP
description: Erfahren Sie mehr über die Kampagnenverwaltungshierarchie und -komponenten.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Überblick über Campaign Management in Advertising DSP

DSP Kampagnen weisen die folgende Hierarchie auf:

* Kampagne
   * Paket(e)
      * Platzierung(en)
         * Anzeige(en)
<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Kampagnen](/help/dsp/campaign-management/campaigns/campaign-about.md) sind das übergreifende Framework der Flugeinstellungen. Jede Kampagne wird mit einem Advertiser, Start- und Enddaten, einem Gesamtbudget, einer geräteübergreifenden Targeting-Option und einer standardmäßigen Frequenzbegrenzung sowie Berichtsoptionen für Sichtbarkeit, Betrug, Markensicherheit und Zielgruppenüberprüfung konfiguriert. Alle Einstellungen auf Kampagnenebene gelten automatisch für jedes Paket und jede Platzierung innerhalb der Kampagne.

## [!UICONTROL Packages]

Jede Kampagne kann ein oder mehrere [Pakete](/help/dsp/campaign-management/packages/package-about.md) enthalten, die jeweils eine Reihe von Platzierungen enthalten.

Verwenden Sie Pakete, um Platzierungen für die Bereitstellung in einem festgelegten Budget, Leistungsziel und einer benutzerdefinierten Schrittstrategie zu gruppieren. DSP optimiert Pakete, indem Budgets auf die leistungsstärksten Platzierungen im Paket umgestellt werden. Sie können Pakete nach Platzierungsformat, Inventartyp, Datenanbieter, Persona oder anderen unterscheidbaren Eigenschaften organisieren.

Pakete sind optional, werden jedoch empfohlen.

## [!UICONTROL Placements]

Eine [placement](/help/dsp/campaign-management/placements/placement-about.md) speichert Targeting-Parameter für eine oder mehrere Anzeigen desselben Anzeigentyps. Sie können eine Platzierung für eine einzelne Kampagne oder ein einzelnes Paket erstellen und ihr dann Anzeigen zuweisen.

## [!UICONTROL Ads]

[Anzeigen](/help/dsp/campaign-management/ads/ad-about.md) enthalten Kreativ-Assets und Tracking-URLs. Sie können Werbe-Tags von Drittanbietern einzeln oder in großen Mengen hochladen, indem Sie Partner-Tag-Tabellen oder die Bulk-Tag-Vorlage verwenden. Sie können auch manuell native Display-Anzeigen für DSP erstellen.

Sobald Ihre Anzeigen eingerichtet sind, müssen Sie jede Anzeige an eine Platzierung anhängen, um die Anzeige auszuführen. Sie können eine einzelne Anzeige an eine oder mehrere Platzierungen anhängen.

Alle aktiven, genehmigten Anzeigen in einer aktiven Platzierung in einer aktiven Kampagne können auf der Grundlage der Platzierungs-Targeting-Parameter ausgeführt werden.

>[!MORELIKETHIS]
>
>* [Info zu Campaign Management](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Über die Paketverwaltung](/help/dsp/campaign-management/packages/package-about.md)
>* [Über die Platzierungsverwaltung](/help/dsp/campaign-management/placements/placement-about.md)
>* [Über die Anzeigenverwaltung](/help/dsp/campaign-management/ads/ad-about.md)
>* [Checkliste für den Kampagnenstart](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Best Practices zum Einrichten von Leistungskampagnen](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Typen von Leistungsberichten in Campaign Management-Ansichten](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Verwalten der Datenansichten Ihrer Kampagne](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Video: DSP Kontostruktur und Benutzeroberfläche](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
