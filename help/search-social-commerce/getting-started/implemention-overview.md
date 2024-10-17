---
title: Übersicht über die Implementierung von Search, Social und Commerce
description: Lernen
exl-id: c99dc029-81e4-4416-89b1-7cf8d66658b2
feature: Search Getting Started
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 0%

---

# Übersicht über die Implementierung von Search, Social und Commerce

[!DNL Adobe] oder eine ihrer Partneragenturen arbeitet mit jedem Advertiser zusammen, um seine Online-Werbeportfolios zu starten und alle zusätzlichen Werbekampagnen zu verfolgen. Nach dem ersten Start stellen zusätzliche laufende Aufgaben sicher, dass die Ziele des Werbetreibenden auch weiterhin erreicht werden.

Im Folgenden finden Sie den allgemeinen Workflow zur Implementierung und Verwendung von Search, Social und Commerce.

## Erster Start

[!DNL Adobe] und/oder Ihre Agentur arbeiten mit Ihnen wie folgt zusammen:

1. Bewerten Sie Ihre allgemeinen Geschäftsziele und entwickeln Sie Strategien zu ihrer Erreichung:

   1. Ermitteln Sie Ihr Geschäftsmodell und Ihre Marketing-Ziele.

   1. Ermitteln der Konversions-Tracking-Anforderungen

   1. Analysieren Sie Ihre bestehenden Online-Anzeigenkontostrukturen.

   1. Identifizieren Sie Metriken zur Portfoliooptimierung und -berichterstellung.

1. (Administrator- oder Account Manager-Benutzer) Einrichten von Administratorkonten:

   1. Richten Sie das Konto des Werbetreibenden ein. Wenn eine Agentur die Daten des Werbetreibenden verwaltet, muss das Konto des Werbetreibenden mit dem Agenturkonto verknüpft werden.

   1. (Bei Bedarf) Erstellen Sie Benutzerkonten für den Advertiser, um seine Kampagnendaten anzuzeigen und zu verwalten und Berichte zu erstellen.

   Weitere Informationen zum Einrichten von Konten finden Sie im Hilfekapitel unter &quot;Admin&quot;.

1. Synchronisieren oder erstellen Sie Kampagnen für jedes Ihrer Anzeigennetzwerkkonten:

   * Synchronisieren Sie mit dem Konto, indem Sie a) einen entsprechenden Kontodatensatz in Search, Social und Commerce erstellen, der die Kontozugriffsberechtigungen und Tracking-Optionen enthält, und b) den Kontostatus auf aktiviert setzen.

   * Wenn die Konten noch keine Kampagnendaten enthalten, fügen Sie Kampagnen, Anzeigengruppen, Suchbegriffe, Anzeigen und Platzierungen aus Search, Social und Commerce oder aus dem Werbenetzwerk hinzu.

     Weitere Informationen zum Einrichten von Suchkampagnen finden Sie im Hilfekapitel zu &quot;Campaign Management&quot;.

1. Richten Sie das Tracking für alle Anzeigen ein, für die Adobe Advertising Konversionen verfolgen soll:

   1. (Falls erforderlich) Richten Sie Klick-Tracking für Anzeigen und optional für Suchbegriffe, [!DNL Google Ads] Platzierungen und [!DNL Google Ads] Erweiterungen ein, indem Sie Klick-Tracking-URLs generieren und hochladen.

      Klick-Tracking-URLs für Advertiser mit dem Adobe Advertising-pixelbasierten Konversions-Tracking-Dienst enthalten eine Umleitung zu [!DNL Adobe] -Servern.

   1. Einrichten des Konversions-Trackings. Abhängig von der Implementierung kann dies das Hinzufügen von Konversions-Tracking-Tags zu den entsprechenden Webseiten und/oder das Einrichten eines täglichen Feed-Drops für Konversionsdaten umfassen, die Sie mit Ihrer eigenen Methode erfasst haben.

      Weitere Informationen zum Einrichten des Trackings finden Sie im Hilfekapitel unter &quot;Tracking&quot;.

1. Richten Sie Integrationen mit zusätzlichen Produkten ein:

   1. (Werbetreibende mit Adobe Analytics und/oder Adobe Audience Manager) Richten Sie Integrationen zwischen den verschiedenen Konten ein, damit Adobe Advertising Daten mit ihnen austauschen kann.

      Siehe Handbuch zu &quot;[Integrationen mit Experience Cloud](/help/integrations/home.md)&quot;.

   1. (Advertiser mit [!DNL Google Analytics]) Synchronisieren Sie Konversionsmetriken für eine [!DNL Google Analytics] -Konto-, Eigenschaften- und Ansichtskombination zur Optimierung und Berichterstellung.

      Weitere Informationen finden Sie im Hilfeunterkapitel &quot;Admin&quot;> &quot;[Konfigurieren von Data Sources](/help/search-social-commerce/admin/data-sources/data-source-about.md)&quot;.

1. Richten Sie Portfolios ein und starten Sie sie:

   1. Richten Sie mit den entsprechenden Kampagnen Portfolios ein, die zur Erreichung Ihrer Ziele und Geschäftsziele konfiguriert sind. Das Implementierungsteam sammelt und validiert dann Klick- und Umsatzdaten für mindestens 14 Tage und validiert die Portfolioeinstellungen.

      >[!NOTE]
      >
      >In Search, Social und Commerce werden weiterhin Daten für Kampagnen verfolgt und berichtet, die nicht Portfolios zugewiesen sind, sie werden jedoch nicht optimiert.

   1. Sobald genügend Daten verfügbar sind, um eine Grundlinie zu erstellen, kann das Team das Portfolio starten, sodass Search, Social und Commerce die Angebote und/oder Budgets für das Portfolio basierend auf dem Optimierungstyp optimieren können.

   Weitere Informationen zum Einrichten und Starten von Portfolios finden Sie in der Hilfe zu &quot;Optimierung&quot;, die über das Menü [!UICONTROL Help] (![Hilfe-Menü](/help/search-social-commerce/assets/help-main-menu.png "Hilfe-Menü")) oben rechts auf jeder Seite in Search, Social und Commerce verfügbar ist.

1. Überwachen Sie die Leistung Ihrer Portfolios:

   1. Erstellen Sie Werbeeinblicke, die visuelle, umsetzbare Daten über Ihre optimierten und aktiven Portfolios darstellen.

   1. Richten Sie benutzerdefinierte Berichte zur Leistungsüberwachung ein und automatisieren Sie sie möglicherweise.

   Weitere Informationen zum Ausführen von Werbeeinsichten und zum Einrichten von Berichten finden Sie im Hilfekapitel zu &quot;Insights &amp; Reports&quot;.

1. (Optional) Konfigurieren Sie Ihre [Leistungsdatenansichten](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) so, dass die Daten angezeigt werden, die Sie sehen möchten.

## Laufende Aufgaben

Nach dem ersten Start sind die folgenden laufenden Aufgaben erforderlich. Abhängig von Ihren Einsatzbedingungen führt entweder [!DNL Adobe], eine Affiliate-Agentur oder der Advertiser die folgenden Aufgaben aus:

* Überwachen und analysieren Sie weiterhin die Leistung der einzelnen Portfolios, indem Sie Warnhinweise, Leistungsdaten für jedes Portfolio und seine Komponentenkampagnen, anpassbare Berichte und (einige Rollen) Simulationen anzeigen.

* Passen Sie bei Bedarf die verschiedenen Strategien und Einstellungen, die Sie zur Verwaltung des Portfolio-Sets verwenden, auf Grundlage der tatsächlichen und prognostizierten Leistung und Wachstumsmöglichkeiten des Portfolios an:

   * Passen Sie die Portfoliobudgets, -ziele und andere Einstellungen an.

   * Passen Sie die Konto-/Kampagnenstrukturen an, um Änderungen in der Marketingstrategie Rechnung zu tragen.

   * Hinzufügen/Anhalten/Löschen von Kampagnenkomponenten Dazu können die Erweiterung von Suchbegriffssätzen auf der Grundlage der Suchbegriffanalyse sowie das Testen von Werbeanzeigen und Landingpages gehören.

   * Aktualisieren Sie geografische und Site-Targeting-Strategien auf der Grundlage erweiterter Leistungsberichte.

   * (Optional) Fügen Sie Angebotsbegrenzungen zu einzelnen Suchbegriffen oder zu allen Suchbegriffen in einer Anzeigengruppe, Kampagne oder einem Portfolio hinzu.

   * Hinzufügen neuer Portfolios.

Anweisungen zum Überwachen von Portfolios und Anpassen der Portfoliostrategien finden Sie im Hilfeunterkapitel &quot;Optimierung&quot;> &quot;Verwalten von Portfolios&quot;> &quot;Leistungsüberwachung und -verwaltung&quot;, das über das Menü [!UICONTROL Help] (![Hilfemenü](/help/search-social-commerce/assets/help-main-menu.png "Hilfe-Menü")) oben rechts auf jeder Seite in Search, Social und Commerce verfügbar ist.
