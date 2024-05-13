---
title: Konfigurieren von A/B-Tests für Adobe Advertising-Suchen-, Social- und Commerce-Anzeigen in Adobe Target
description: Erfahren Sie, wie Sie einen A/B-Test einrichten in [!DNL Target] für Ihre [!DNL Google Ads] und [!DNL Microsoft Advertising] Anzeigen in Search, Social und Commerce.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Konfigurieren von A/B-Tests in Adobe Target für Advertising Search-, Social- und Commerce-Anzeigen

*Advertiser mit Advertising Search, Social und Commerce*

*[!DNL Google Ads]und [!DNL Microsoft Advertising] Nur Konten*

Adobe Advertising und Adobe Target vereinfachen die Einrichtung von A/B-Tests für Landingpage-Erlebnisse für den Traffic digitaler Werbung [!DNL Google Ads] und [!DNL Microsoft Advertising] an:

* Verbesserung der Konversionsraten (CVR) und der Akquise-Effizienz (z. B. CPA, CPL und CAC).

* Bereitstellung eines personalisierteren Landingpage-Erlebnisses, das für die Anzeige relevant ist (z. B. Abgleich von Bild/Video-Kreativelement, Kopie, Keyword oder anderem Werbesignal mit der Landingpage).

Sie können auch die nativen [[!DNL Analytics] für Werbung](/help/integrations/analytics/overview.md) und [[!DNL Analytics] für [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) Integrationsberichterstellungsdimensionen, die in Adobe Analytics integriert sind, um Ihre Testdaten zu messen und zu visualisieren mit [!DNL Analytics] Metriken und Erfolgsereignisse.

In den folgenden Abschnitten finden Sie die Voraussetzungen und Anweisungen zum Einrichten von A/B-Tests in [!DNL Target] für Clickthrough-Traffic von Anzeigen in Search, Social und Commerce sowie Tipps zur Messung und Visualisierung Ihrer Tests in [!DNL Analytics].

## Voraussetzungen

### Erforderliche Produkte

* Suchen, Social und Commerce
* [!DNL Target]

### Empfohlene Produkte und Integrationen

* [!DNL Analytics]

* [[!DNL Analytics] für Werbung](/help/integrations/analytics/overview.md) Integration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] für [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) Integration

## Schritt 1: Erstellen einer A/B-Test-Aktivität in [!DNL Target] für Search, Social und Commerce

In den folgenden Anweisungen werden Informationen zum Anwendungsfall &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;hervorgehoben.

1. [Bei Adobe Target anmelden](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Erstellen eines A/B-Tests](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. Im **[!UICONTROL Enter Activity URL]** Geben Sie die Landingpage-URL für den Test ein.

   1. Im **[!UICONTROL Goal]** geben Sie die Erfolgsmetrik für den Test ein.

      >[!NOTE]
      >
      >Stellen Sie sicher, dass [!DNL Analytics] als Datenquelle in [!DNL Target]und dass die richtige Report Suite ausgewählt ist.

   1. Legen Sie die **[!UICONTROL Priority]** nach `High` oder `999` um Konflikte zu vermeiden, wenn Benutzer im Testsegment ein falsches On-site-Erlebnis erhalten.


   1. Within **[!UICONTROL Reporting Settings]**, wählen Sie die **[!UICONTROL Company Name]** und **[!UICONTROL Report Suite]** mit Ihrem Search-, Social- und Commerce-Konto verknüpft ist.

      Weitere Tipps zur Berichterstellung finden Sie unter[Best Practices und Fehlerbehebung für die Berichterstellung](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. Im **[!UICONTROL Date Range]** geben Sie das entsprechende Start- und Enddatum für den Test ein.

   1. Auswählen **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. Im **[!UICONTROL Value]** und geben Sie die [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID]oder [!UICONTROL Network Ad ID] für die entsprechende Anzeigennetzwerkentität in Search, Social und Commerce. Auf diese Weise können Sie die [!DNL Target] Abfragezeichenfolgenparameter für Clickthrough-Zielgruppen für die Entität.

      Sie können die Kennung nach [Hinzufügen der entsprechenden ID-Spalte zur Entitätsansicht](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] in der [!UICONTROL Accounts] Ansicht](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] in der [!UICONTROL Accounts] Ansicht")

      Wenden Sie sich an Ihr Adobe-Account-Team, wenn Sie Hilfe benötigen.

   1. Für **[!UICONTROL Traffic Allocation Method]** auswählen **[!UICONTROL Manual (Default)]** und teilen Sie die Zielgruppe 50/50 auf.

   1. Speichern Sie die Aktivität.

1. Verwendung [Target Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) , um Designänderungen an der Landingpage-Vorlage für A/B-Tests vorzunehmen.

   * Erlebnis A: Nicht bearbeiten, da dies das standardmäßige/steuerbare Landingpage-Erlebnis ohne Personalisierung ist.

   * Erlebnis B: Verwenden Sie die [!DNL Target] -Benutzeroberfläche, um die Landingpage-Vorlage auf der Grundlage der im Test enthaltenen Assets anzupassen (z. B. Überschriften, Kopien, Schaltflächenplatzierung und Kreativinhalte).

   >[!NOTE]
   >
   >Wenden Sie sich beispielsweise in Anwendungsfällen für kreative Tests an Ihr Adobe-Account-Team.

## Schritt 2: Einrichten der [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics]

[!DNL Analytics for Target] (A4T) ist eine lösungsübergreifende Integration, mit der Advertiser Inhalte erstellen können. [!DNL Target] Aktivitäten, die auf [!DNL Analytics] Konversionsmetriken und Zielgruppensegmente verwenden und dann die Ergebnisse mit [!DNL Analytics] als Berichtsquelle. Alle Berichte und Segmentierungen für diese Aktivität basieren auf [!DNL Analytics] Datenerfassung.

Weitere Informationen finden Sie unter [!DNL Analytics for Target], einschließlich eines Links zu Implementierungsanweisungen, siehe[Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Richten Sie die [!DNL Analytics for Target] Bedienfeld

Konfigurieren Sie in Analysis Workspace die [!DNL Analytics for Target panel] , um Ihre [!DNL Target] Aktivitäten und Erlebnisse. Beachten Sie die folgenden wichtigen Hinweise und Informationen zu Ihren Berichten.

#### Metriken

* Erstellen Sie innerhalb des Arbeitsbereichs einen spezifischen Bereich für das Adobe Advertising-Konto, die Kampagne oder die Anzeigengruppe.<!-- only applicable entities? --> für die der Test ausgeführt wurde. Verwenden Sie Zusammenfassungsvisualisierungen, um Adobe Advertising-Metriken im selben Bericht wie die [!DNL Target] Testleistung.

* Priorisieren Sie die Verwendung von On-site-Metriken (z. B. Besuche und Konversionen), um die Leistung zu messen.

* Sie müssen wissen, dass aggregierte Medienmetriken von Adobe Advertising (wie Impressionen, Klicks und Kosten) nicht mit [!DNL Target] Metriken.

#### Dimensionen

Die folgenden Dimensionen beziehen sich auf [!DNL Analytics for Target]:

* **Target Activities**: Name des A/B-Tests

* **Target-Erlebnisse**: Namen der in der Aktivität verwendeten Landingpage-Erlebnisse

* **Target-Aktivität** > **Erlebnis**: Der Aktivitäts- und Erlebnisname in derselben Zeile

### Fehlerbehebung in Analytics für [!DNL Target] Daten

Wenn Sie in Analysis Workspace feststellen, dass die Daten zu Aktivitäten und Erlebnissen minimal sind oder nicht ausgefüllt werden, führen Sie die folgenden Schritte aus:

* Stellen Sie sicher, dass [!UICONTROL Supplemental Data ID] (SDID) wird für beide [!DNL Target] und [!DNL Analytics]. Sie können die SDID-Werte mithilfe der [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) auf der Landingpage, zu der die Kampagne Benutzer steuert.

[Zusätzliche Daten-ID-Werte (SDID) in Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Überprüfen Sie auf derselben Landingpage, ob a) die Variable [!UICONTROL Hostname] im Adobe Debugger unter [!UICONTROL Solutions] > [!UICONTROL Target] entspricht b) [!UICONTROL Tracking Server] angezeigt in [!DNL Target] für die Aktivität (unter [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] erfordert [!DNL Analytics] Tracking-Server, der bei Aufrufen von [!DNL Target] der [!DNL Modstats] Datenerfassungsserver für Analytics.<!-- just "to Analytics?"-->

[Hostnamenwert in Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Tracking-Server-Wert in Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Weitere Informationen

* [Integration von Target in Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Erläutert die Einrichtung [!DNL Target] Reporting in Analysis Workspace.
* [Überblick über A/B-Tests](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Beschreibt A/B-Test-Aktivitäten, die Sie mit Anzeigen in Search, Social und Commerce verwenden können.
* [Übersicht über Analytics für Werbung](/help/integrations/analytics/overview.md) - Einführung in Analytics for Advertising, mit dem Sie Clickthrough- und Durchsichts-Site-Interaktionen in Ihren Analytics-Instanzen verfolgen können.

>[!MORELIKETHIS]
>
>* [Konfigurieren von A/B-Tests in Adobe Target für Anzeigen DSP](ab-tests-dsp.md)
