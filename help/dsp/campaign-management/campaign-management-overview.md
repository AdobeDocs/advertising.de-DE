---
title: Überblick über die Kampagnenverwaltung in Advertising DSP
description: Erfahren Sie mehr über die Hierarchie und Komponenten der Kampagnenverwaltung.
feature: DSP Packages, DSP Placements, DSP Ads
exl-id: 8eb7b4a5-4a31-4637-858f-202392dfac98
TQID: https://experienceleague.adobe.com/w7j86H42OR371vewJM--ep2YUn70XJpMWJQNT92r2CY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
  - id: d9510790-d834-436d-8423-8d69cd50464a
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 335
ht-degree: 0%

---

# Überblick über die Kampagnenverwaltung in Advertising DSP

DSP-Kampagnen haben die folgende Hierarchie:

* Campaign
   * Package(s)
      * Platzierung/en
         * Anzeige(n)
<!--
 Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package includes placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[Kampagnen](/help/dsp/campaign-management/campaigns/campaign-about.md) sind das übergeordnete Framework der Flugeinstellungen. Jede Kampagne wird mit einem Advertiser, Start- und Enddaten, einem Gesamtbudget, einer geräteübergreifenden Targeting-Option und einer standardmäßigen Häufigkeitsbegrenzung sowie Berichtsoptionen für Sichtbarkeit, Betrug, Markensicherheit und Zielgruppenüberprüfung konfiguriert. Alle Einstellungen auf Kampagnenebene gelten automatisch für jedes Paket und jede Platzierung innerhalb der Kampagne.

## [!UICONTROL Packages]

Jede Kampagne kann ein oder mehrere [Pakete](/help/dsp/campaign-management/packages/package-about.md) enthalten, von denen jede eine Reihe von Platzierungen enthält.

Verwenden Sie Pakete, um Platzierungen für die Bereitstellung nach einem festgelegten Budget, einem Leistungsziel und einer benutzerdefinierten Schrittmacherstrategie zu gruppieren. DSP optimiert Pakete, indem Budgets auf die Platzierungen verschoben werden, die im Paket am besten abschneiden. Sie können Pakete nach Platzierungsformat, Inventartyp, Datenanbieter, Rolle oder anderen unterscheidbaren Merkmalen organisieren.

Pakete sind optional, werden aber empfohlen.

## [!UICONTROL Placements]

Eine [Platzierung](/help/dsp/campaign-management/placements/placement-about.md) speichert Zielgruppenbestimmungsparameter für eine oder mehrere Anzeigen desselben Anzeigentyps. Sie können eine Platzierung für eine einzelne Kampagne oder ein einzelnes Paket erstellen und ihr dann Anzeigen zuweisen.

## [!UICONTROL Ads]

[Anzeigen](/help/dsp/campaign-management/ads/ad-about.md) enthalten Kreativ-Assets und Tracking-URLs. Sie können Anzeigen-Tags von Drittanbietern einzeln oder stapelweise mithilfe von Partner-Tag-Blättern oder der Bulk-Tag-Vorlage hochladen. Sie können auch manuell native Display-Anzeigen erstellen, die von DSP bereitgestellt werden.

Sobald Ihre Anzeigen eingerichtet sind, müssen Sie jede Anzeige an eine Platzierung anhängen, um mit der Ausführung der Anzeige zu beginnen. Sie können eine einzelne Anzeige an eine oder mehrere Platzierungen anhängen.

Alle aktiven, genehmigten Anzeigen in einer aktiven Platzierung in einer aktiven Kampagne können basierend auf den Zielgruppenbestimmungsparametern für die Platzierung ausgeführt werden.

>[!MORELIKETHIS]
>
>* [Über die Kampagnenverwaltung in Advertising DSP](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Über die Paketverwaltung in Advertising DSP](/help/dsp/campaign-management/packages/package-about.md)
>* [Über die Platzierungsverwaltung in Advertising DSP](/help/dsp/campaign-management/placements/placement-about.md)
>* [Über die Anzeigenverwaltung in Advertising DSP](/help/dsp/campaign-management/ads/ad-about.md)
>* [Checkliste zum Kampagnenstart](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Best Practices für die Einrichtung von Leistungskampagnen](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Typen von Leistungsberichten in Kampagnenverwaltungsansichten](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Kampagnendaten-Ansichten verwalten](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Video: DSP-Kontostruktur und Benutzeroberfläche](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html?lang=de)
