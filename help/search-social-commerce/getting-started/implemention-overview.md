---
title: Übersicht über die Implementierung von Search, Social und Commerce
description: Erfahren Sie mehr über den allgemeinen Workflow zum Starten und Verwalten eines Portfolios.
exl-id: c99dc029-81e4-4416-89b1-7cf8d66658b2
feature: Search Getting Started
TQID: 'https://experienceleague.adobe.com/AFMTue1YGuFjAJF04HTHEimfd2JC8ZxSkYCRDu8wDFY'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 54967645-9f46-5896-8af7-b943b426aadf
    internal-label: Search Getting Started
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '886'
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

   Arbeiten Sie mit Ihrem Administrator zusammen, um den Zugriff mithilfe von Adobe Admin Console und den entsprechenden Produktprofilen zu konfigurieren. Siehe &quot;[Benutzerverwaltung für Suche, Social und Commerce](/help/search-social-commerce/user-administration.md)&quot;

1. Synchronisieren mit oder erstellen Sie Kampagnen für jedes Ihrer Werbenetzwerkkonten:

   * Für Konten mit API-Verbindung [&#x200B; Sie &#x200B;](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md#create-account)Kontodetails erstellen) unter [!UICONTROL Manage] > [!UICONTROL Accounts] die netzwerkspezifische Authentifizierung, konfigurieren Sie Tracking-Optionen und aktivieren Sie das Konto.

   * Befolgen Sie bei Konten ohne API-Unterstützung je [&#x200B; den Workflow &#x200B;](/help/search-social-commerce/manage/accounts/data-upload-accounts/data-upload-account-manage.md)Datenupload[&#x200B; oder &#x200B;](/help/search-social-commerce/manage/accounts/template-account-manage.md)Nur-Tracking-Konto“. Diese Konten werden nicht mit dem Anzeigennetzwerk synchronisiert und unterstützen keine Portfoliooptimierung.

   * Wenn die Konten noch keine Kampagnendaten enthalten, fügen Sie Kampagnen, Anzeigengruppen, Keywords, Anzeigen und Platzierungen aus Search, Social und Commerce oder aus dem Anzeigennetzwerk hinzu.

     Eine detaillierte Checkliste zur Einrichtung finden Sie unter [Einrichten von Werbenetzwerkkonten und -kampagnen](campaign-implementation-overview.md). Verwenden Sie für unterstützte Kampagnentypen [!UICONTROL Manage] > [!UICONTROL Campaigns] , um [Kampagnen zu erstellen und zu verwalten](/help/search-social-commerce/manage/campaigns/campaign-manage.md).

1. Richten Sie das Tracking für alle Anzeigen ein, für die Adobe Advertising Konversionen verfolgen soll:

   1. (Falls erforderlich) [Richten Sie das Klick-Tracking &#x200B;](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) Anzeigen und optional für Keywords, [!DNL Google Ads] Platzierungen und [!DNL Google Ads] Erweiterungen ein, indem Sie Klick-Tracking-URLs generieren und hochladen.

      Klick-Tracking-URLs für Werbetreibende mit dem pixelbasierten Konversionsverfolgungs-Service von Adobe Advertising enthalten eine Umleitung zu [!DNL Adobe].

   1. [Konversionsverfolgung einrichten](/help/search-social-commerce/tracking/conversion-tracking-about.md). Je nach Implementierung kann dies das Hinzufügen von Konversionsverfolgungs-Tags zu den entsprechenden Web-Seiten und/oder das Einrichten eines täglichen Feed-Abrufs für Konversionsdaten beinhalten, den Sie mit Ihrer eigenen Methode erfasst haben. Sie können [Konversionsverfolgungstags für Adobe Advertising generieren](/help/search-social-commerce/goals/conversions/conversion-tag-generate.md) unter [!UICONTROL Goals] > [!UICONTROL Conversions].

      Weitere Informationen finden Sie unter &quot;[&#x200B; zum Tracking für Search, Social und Commerce](/help/search-social-commerce/tracking/tracking-about.md).

1. Einrichten von Integrationen mit zusätzlichen Produkten:

   1. (Werbetreibende mit Adobe Analytics und/oder Adobe Audience Manager) Richten Sie Integrationen zwischen den verschiedenen Konten ein, damit Adobe Advertising Daten mit ihnen austauschen kann.

      Weitere Informationen finden Sie im Handbuch [Integrationen mit CX Enterprise](/help/integrations/home.md).

   1. (Advertiser mit [!DNL Google Analytics]) Synchronisieren Sie Konversionsmetriken für ein [!DNL Google Analytics] Konto, eine Eigenschaft und eine Ansichtskombination, um Optimierungen und Berichte zu ermöglichen.

      Diese Konfiguration verwendet die alte Benutzeroberfläche. Siehe &quot;[Über Synchronisierungs [!DNL Google Analytics] Konversionsmetriken](/help/search-social-commerce/legacy-ui/admin/data-sources/data-source-about.md)&quot; und, falls erforderlich, [zur alten Benutzeroberfläche wechseln](ui-switch.md).

1. (Optional) Portfolios einrichten und starten:

   1. Überprüfen Sie unter [!UICONTROL Goals] > [!UICONTROL Conversions] [&#x200B; die Konversionsmetriken und machen Sie die erforderlichen Metriken &#x200B;](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#conversion-metrics-change-available). Wählen Sie unter [!UICONTROL Goals] > [!UICONTROL Objectives] [Ziel erstellen oder auswählen](/help/search-social-commerce/goals/objectives/objective-about.md) aus.

   1. Erstellen Sie unter [!UICONTROL Manage] > [!UICONTROL Portfolios] [Portfolios](/help/search-social-commerce/manage/portfolios/portfolio-create.md) die so konfiguriert sind, dass sie Ihre Ziele und Geschäftsziele erfüllen, mit den entsprechenden [geeigneten Kampagnen](/help/search-social-commerce/manage/campaigns/campaign-manage.md#campaign-portfolio). [Aktivieren Sie die Portfolios](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) um Daten zu sammeln und zu modellieren. Das Implementierungs-Team sammelt und validiert dann Klick- und Umsatzdaten für mindestens 14 Tage und validiert die Portfolioeinstellungen.

      >[!NOTE]
      >
      >Search, Social und Commerce verfolgen und melden weiterhin Daten für Kampagnen, die keinen Portfolios zugewiesen sind, bieten jedoch keine Optimierung für sie.

   1. Sobald genügend Daten zur Erstellung einer Baseline verfügbar sind, kann das Team [den Portfoliostatus in „optimiert“ ändern](/help/search-social-commerce/manage/portfolios/portfolio-change-status.md) sodass Search, Social und Commerce die Gebote, Budgets und/oder Gebotsstrategieziele für das Portfolio basierend auf dem Portfoliotyp und den Kampagnen-Gebotsstrategien optimieren können.

   Siehe &quot;[&#x200B; zu Portfolios](/help/search-social-commerce/manage/portfolios/portfolio-about.md) für Optimierungsunterstützung und Portfoliostatus.

1. Überwachen der Leistung Ihrer Portfolios:

   1. Verwenden Sie [!UICONTROL Dashboard] > [!UICONTROL Overview] , um [Portfoliotrends](/help/search-social-commerce/dashboard/dashboard-overview.md) zu überprüfen und [Details zur Portfolioleistung anzuzeigen](/help/search-social-commerce/manage/portfolios/portfolio-details.md), um die Ergebnisse und Modellgenauigkeit zu untersuchen.

   1. [Einrichten benutzerdefinierter Warnhinweise](/help/search-social-commerce/common-tasks/alerts-manage.md) und [Erstellen benutzerdefinierter Berichte](/help/search-social-commerce/reports/management/report-manage.md) für die Leistungsüberwachung. Automatisieren Sie bei Bedarf das Reporting mithilfe [Berichtsvorlagen](/help/search-social-commerce/reports/report-templates-manage.md) und [Tabellen-Feeds](/help/search-social-commerce/reports/spreadsheet-feeds-manage.md).

   Weitere Informationen finden Sie unter [Überwachen der Kampagnen- und Portfolioleistung](/help/search-social-commerce/manage/manage-about.md#monitor-performance).

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

Anweisungen zur Überwachung von Kampagnen und Portfolios und zur Anpassung ihrer Einstellungen finden Sie unter [Über die Verwaltung von Kampagnen und &#x200B;](/help/search-social-commerce/manage/manage-about.md)&quot; und [Portfoliodetails bearbeiten](/help/search-social-commerce/manage/portfolios/portfolio-edit.md).
