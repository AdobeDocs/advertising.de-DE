---
title: Überblick über Campaign Management in Advertising DSP
description: Erfahren Sie mehr über die Hierarchie und Komponenten der Kampagnenverwaltung.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Überblick über Campaign Management in Advertising DSP

DSP-Kampagnen haben die folgende Hierarchie:

* Campaign
   * Package(s)
      * Platzierung/en
         * Anzeige(n)
<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Kampagnen](/help/dsp/campaign-management/campaigns/campaign-about.md) sind das übergeordnete Framework der Flugeinstellungen. Jede Kampagne wird mit einem Advertiser, Start- und Enddaten, einem Gesamtbudget, einer geräteübergreifenden Targeting-Option und einer standardmäßigen Häufigkeitsbegrenzung sowie Berichtsoptionen für Sichtbarkeit, Betrug, Markensicherheit und Zielgruppenüberprüfung konfiguriert. Alle Einstellungen auf Kampagnenebene gelten automatisch für jedes Paket und jede Platzierung innerhalb der Kampagne.

## [!UICONTROL Packages]

Jede Kampagne kann ein oder mehrere [Pakete](/help/dsp/campaign-management/packages/package-about.md) enthalten, von denen jede eine Reihe von Platzierungen enthält.

Verwenden Sie Pakete, um Platzierungen für die Bereitstellung nach einem festgelegten Budget, einem Leistungsziel und einer benutzerdefinierten Schrittmacherstrategie zu gruppieren. DSP optimiert Pakete durch Umschichtung der Budgets auf die leistungsstärksten Platzierungen im Paket. Sie können Pakete nach Platzierungsformat, Inventartyp, Datenanbieter, Rolle oder anderen unterscheidbaren Merkmalen organisieren.

Pakete sind optional, werden aber empfohlen.

## [!UICONTROL Placements]

Eine [Platzierung](/help/dsp/campaign-management/placements/placement-about.md) speichert Zielgruppenbestimmungsparameter für eine oder mehrere Anzeigen desselben Anzeigentyps. Sie können eine Platzierung für eine einzelne Kampagne oder ein einzelnes Paket erstellen und ihr dann Anzeigen zuweisen.

## [!UICONTROL Ads]

[Anzeigen](/help/dsp/campaign-management/ads/ad-about.md) enthalten Kreativ-Assets und Tracking-URLs. Sie können Anzeigen-Tags von Drittanbietern einzeln oder stapelweise mithilfe von Partner-Tag-Blättern oder der Bulk-Tag-Vorlage hochladen. Sie können auch manuell native Display-Anzeigen für die Bereitstellung von DSP erstellen.

Sobald Ihre Anzeigen eingerichtet sind, müssen Sie jede Anzeige an eine Platzierung anhängen, um mit der Ausführung der Anzeige zu beginnen. Sie können eine einzelne Anzeige an eine oder mehrere Platzierungen anhängen.

Alle aktiven, genehmigten Anzeigen in einer aktiven Platzierung in einer aktiven Kampagne können basierend auf den Zielgruppenbestimmungsparametern für die Platzierung ausgeführt werden.

>[!MORELIKETHIS]
>
>* [Über Campaign Management](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Über die Paketverwaltung](/help/dsp/campaign-management/packages/package-about.md)
>* [Über die Platzierungsverwaltung](/help/dsp/campaign-management/placements/placement-about.md)
>* [Über die Anzeigenverwaltung](/help/dsp/campaign-management/ads/ad-about.md)
>* [Checkliste für den Kampagnenstart](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Best Practices zum Einrichten von Leistungskampagnen](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Typen von Leistungsberichten in Campaign Management-Ansichten](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Campaign-Datenansichten verwalten](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Video: DSP-Kontostruktur und Benutzeroberfläche](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
