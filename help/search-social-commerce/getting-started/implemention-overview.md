---
title: Übersicht über die Implementierung von Search, Social und Commerce
description: Erfahren Sie mehr über den allgemeinen Workflow zum Starten und Verwalten eines Portfolios.
exl-id: c99dc029-81e4-4416-89b1-7cf8d66658b2
feature: Search Getting Started
source-git-commit: 9c7f3d2aec0952b38d2fd3097d0b3499d33bf3b8
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# Übersicht über die Implementierung von Search, Social und Commerce

[!DNL Adobe] oder eine seiner Partneragenturen arbeitet mit jedem Advertiser zusammen, um seine Online-Werbeportfolios zu starten und alle zusätzlichen Werbekampagnen zu verfolgen. Nach dem ersten Start stellen zusätzliche laufende Aufgaben sicher, dass die Ziele des Werbetreibenden weiterhin erfüllt werden.

Im Folgenden finden Sie den allgemeinen Workflow für die Implementierung und Verwendung von Search, Social und Commerce.

## Ursprünglicher Start

[!DNL Adobe] und/oder Ihre Agentur, die mit Ihnen zusammenarbeitet, führen folgende Schritte durch:

1. Bewerten Sie Ihre allgemeinen Geschäftsziele und entwickeln Sie Strategien, um diese zu erreichen:

   1. Identifizieren Sie Ihr Geschäftsmodell und Ihre Marketing-Ziele.

   1. Ermitteln der Anforderungen an das Konversionstracking

   1. Analysieren Sie Ihre vorhandenen Online-Anzeigenkontenstrukturen.

   1. Identifizieren Sie Metriken für die Portfoliooptimierung und das Reporting.

1. (Administrator- oder Account Manager-Benutzer) Einrichten von Administratorkonten:

   1. Richten Sie das Konto des Werbetreibenden ein. Wenn eine Agentur die Daten des Werbetreibenden verwaltet, muss das Konto des Werbetreibenden mit dem Agenturkonto verknüpft sein.

   1. (Falls erforderlich) Erstellen Sie Benutzerkonten für den Advertiser, um seine Kampagnendaten anzuzeigen und zu verwalten und Berichte zu generieren.

   Weitere Informationen zum Einrichten von Konten finden Sie im Hilfekapitel zu „Admin“.

1. Synchronisieren mit oder erstellen Sie Kampagnen für jedes Ihrer Werbenetzwerkkonten:

   * Synchronisieren Sie mit dem Konto, indem Sie a) einen entsprechenden Kontodatensatz in Search, Social und Commerce erstellen, der die Kontozugriffs-Anmeldeinformationen und Tracking-Optionen enthält, und b) den Kontostatus auf „Aktiviert“ setzen.

   * Wenn die Konten noch keine Kampagnendaten enthalten, fügen Sie Kampagnen, Anzeigengruppen, Keywords, Anzeigen und Platzierungen aus Search, Social und Commerce oder aus dem Anzeigennetzwerk hinzu.

     Weitere Informationen zum Einrichten von Suchkampagnen finden Sie im Hilfekapitel zu „Kampagnen-Management“.

1. Richten Sie das Tracking für alle Anzeigen ein, für die Adobe Advertising Konversionen verfolgen soll:

   1. Richten Sie (falls erforderlich) Klick-Tracking für Anzeigen und optional für Schlüsselwörter, [!DNL Google Ads] Platzierungen und [!DNL Google Ads] ein, indem Sie Klick-Tracking-URLs generieren und hochladen.

      Klick-Tracking-URLs für Werbetreibende mit dem pixelbasierten Konversionsverfolgungs-Service von Adobe Advertising enthalten eine Umleitung zu [!DNL Adobe].

   1. Konversionsverfolgung einrichten. Je nach Implementierung kann dies das Hinzufügen von Konversionsverfolgungs-Tags zu den entsprechenden Web-Seiten und/oder das Einrichten eines täglichen Feed-Abrufs für Konversionsdaten beinhalten, den Sie mit Ihrer eigenen Methode erfasst haben.

      Einzelheiten zum Einrichten des Trackings finden Sie im Hilfekapitel zu „Tracking“.

1. Einrichten von Integrationen mit zusätzlichen Produkten:

   1. (Werbetreibende mit Adobe Analytics und/oder Adobe Audience Manager) Richten Sie Integrationen zwischen den verschiedenen Konten ein, damit Adobe Advertising Daten mit ihnen austauschen kann.

      Weitere Informationen finden Sie im Handbuch [Integrationen mit Experience Cloud](/help/integrations/home.md).

   1. (Advertiser mit [!DNL Google Analytics]) Synchronisieren Sie Konversionsmetriken für ein [!DNL Google Analytics] Konto, eine Eigenschaft und eine Ansichtskombination, um Optimierungen und Berichte zu ermöglichen.

      Siehe Hilfekapitel „Admin“ > &quot;[Konfigurieren von Datenquellen](/help/search-social-commerce/admin/data-sources/data-source-about.md).“

1. Portfolios einrichten und starten:

   1. Richten Sie Portfolios ein, die so konfiguriert sind, dass sie Ihre Ziele und Geschäftsziele erfüllen, und nutzen Sie dazu die entsprechenden Kampagnen. Das Implementierungs-Team sammelt und validiert dann Klick- und Umsatzdaten für mindestens 14 Tage und validiert die Portfolioeinstellungen.

      >[!NOTE]
      >
      >Search, Social und Commerce verfolgen und melden weiterhin Daten für Kampagnen, die keinen Portfolios zugewiesen sind, bieten jedoch keine Optimierung für sie.

   1. Wenn genügend Daten zur Erstellung einer Baseline verfügbar sind, kann das Team das Portfolio starten, sodass Search, Social und Commerce Angebote und/oder Budgets für das Portfolio basierend auf dem Optimierungstyp optimieren können.

   Weitere Informationen zum Einrichten und Starten von Portfolios finden Sie in der Hilfe zu „Optimierung“, die über das [!UICONTROL Help]-Menü (![Hilfemenü](/help/search-social-commerce/assets/help-main-menu.png "Hilfemenü")) oben rechts auf jeder Seite in Search, Social und Commerce verfügbar ist.

1. Überwachen der Leistung Ihrer Portfolios:

   1. Generieren Sie Werbeeinblicke, d. h. visuelle, verwertbare Daten zu Ihren optimierten und aktiven Portfolios.

   1. Richten Sie benutzerdefinierte Berichte zur Leistungsüberwachung ein und automatisieren Sie sie potenziell.

   Weitere Informationen zum Ausführen von Advertising Insights und zum Einrichten von Berichten finden Sie im Hilfekapitel zu „Insights &amp; Reports“.

1. (Optional) Konfigurieren Sie Ihre [Leistungsdatenansichten](/help/search-social-commerce/common-tasks/data-views/data-views-about.md) so, dass die Daten angezeigt werden, die Sie sehen möchten.

## Laufende Aufgaben

Nach dem ersten Launch sind die folgenden laufenden Aufgaben erforderlich. Abhängig von Ihren Interaktionsbedingungen führt entweder [!DNL Adobe], eine Affiliate-Agentur oder der Werbetreibende die folgenden Aufgaben aus:

* Überwachen und analysieren Sie weiterhin die Leistung der einzelnen Portfolios, indem Sie Warnhinweise, Leistungsdaten für jedes Portfolio und seine Komponentenkampagnen, anpassbare Berichte und (einige) Rollensimulationen anzeigen.

* Passen Sie die verschiedenen Strategien und Einstellungen, die Sie zur Verwaltung des Portfoliosatzes verwenden, bei Bedarf an, basierend auf der tatsächlichen und prognostizierten Leistung des Portfolios und den Wachstumschancen:

   * Passen Sie die Portfoliobudgets, Ziele und andere Einstellungen an.

   * Anpassen der Konto-/Kampagnenstrukturen, um Änderungen an der Marketing-Strategie zu berücksichtigen.

   * Hinzufügen/Anhalten/Löschen von Kampagnenkomponenten. Dies kann die Erweiterung von Keyword-Sätzen auf der Grundlage einer Suchbegriffanalyse sowie das Testen und Kopieren von und Landingpages umfassen.

   * Aktualisieren Sie die geografischen und Site-Targeting-Strategien auf der Grundlage erweiterter Leistungsberichte.

   * (Optional) Fügen Sie Gebotsbeschränkungen zu einzelnen Suchbegriffen oder zu allen Keywords in einer Anzeigengruppe, Kampagne oder einem Portfolio hinzu.

   * Neue Portfolios hinzufügen.

Anweisungen zum Überwachen von Portfolios und zum Anpassen der Portfoliostrategien finden Sie im Hilfekapitel „Optimierung“ > „Portfolios verwalten“ > „Überwachung und Verwaltung der Performance“, das über das [!UICONTROL Help]-Menü (![Hilfemenü](/help/search-social-commerce/assets/help-main-menu.png "Hilfemenü")) oben rechts auf jeder Seite von Search, Social und Commerce verfügbar ist.
