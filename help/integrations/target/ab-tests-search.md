---
title: Konfigurieren von A/B-Tests für Adobe Advertising-Suche, Social Media und Commerce Ads in Adobe Target
description: Erfahren Sie, wie Sie in Search, Social und Commerce einen A/B [!DNL Target] Test für Ihre  [!DNL Google Ads] und [!DNL Microsoft Advertising] Anzeigen einrichten.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Konfigurieren von A/B-Tests in Adobe Target für Advertising Search, Social und Commerce Ads

*Nur Werbetreibende mit Advertising Search, Social und Commerce*

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising] Konten*

Adobe Advertising und Adobe Target erleichtern die Einrichtung von A/B-Tests für Landingpage-Erlebnisse für die digitale Werbung, [!DNL Google Ads] und [!DNL Microsoft Advertising] zu:

* Verbessern Sie Konversionsraten (CVR) und Akquisitionseffizienzmaßnahmen (wie CPA, CPL und CAC).

* Liefern Sie ein personalisierteres Landingpage-Erlebnis, das für die Anzeige relevant ist (z. B. Abgleich des Bild-/Videosignals, der kreativen Kopie, des Keywords oder anderer Werbesignale mit der Landingpage).

Sie können auch die Berichtsdimensionen der nativen Integration [[!DNL Analytics] für Advertising](/help/integrations/analytics/overview.md) und [[!DNL Analytics] für [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=de), die in Adobe Analytics integriert sind, kombinieren, um Ihre Testdaten mit [!DNL Analytics] Metriken und Erfolgsereignissen zu messen und zu visualisieren.

In den folgenden Abschnitten finden Sie die Voraussetzungen, Anweisungen zum Einrichten von A/B-Tests in [!DNL Target] für Clickthrough-Traffic von Anzeigen in Search, Social und Commerce sowie Tipps zum Messen und Visualisieren Ihrer Tests in [!DNL Analytics].

## Voraussetzungen

### Erforderliche Produkte

* Suche, Social und Commerce
* [!DNL Target]

### Empfohlene Produkte und Integrationen

* [!DNL Analytics]

* [[!DNL Analytics] Integration mit Advertising](/help/integrations/analytics/overview.md)<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=de)-Integration

## Schritt 1: Erstellen einer A/B-Test -Aktivität in [!DNL Target] für Search, Social und Commerce

In den folgenden Anweisungen werden Informationen zum Anwendungsfall „Suche“, „Social“ und &quot;Commerce&quot; hervorgehoben.

1. [Melden Sie sich bei Adobe Target an](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html?lang=de).

1. [Erstellen eines A/B-Tests](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=de):

   1. Geben Sie im Feld **[!UICONTROL Enter Activity URL]** die Landingpage-URL für den Test ein.

   1. Geben Sie im Feld **[!UICONTROL Goal]** die Erfolgsmetrik für den Test ein.

      >[!NOTE]
      >
      >Stellen Sie sicher, dass [!DNL Analytics] als Datenquelle in [!DNL Target] aktiviert ist und dass die richtige Report Suite ausgewählt ist.

   1. Legen Sie die **[!UICONTROL Priority]** auf `High` oder `999` fest, um Konflikte zu vermeiden, wenn Benutzende im Testsegment ein falsches Onsite-Erlebnis erhalten.


   1. Wählen Sie in **[!UICONTROL Reporting Settings]** die **[!UICONTROL Company Name]** und **[!UICONTROL Report Suite]** aus, die mit Ihrem Search-, Social- und Commerce-Konto verbunden sind.

      Weitere Tipps zum Reporting finden Sie unter [Best Practices für das Reporting und Fehlerbehebung](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html?lang=de).

   1. Geben Sie im Feld **[!UICONTROL Date Range]** das entsprechende Start- und Enddatum für den Test ein.

   1. Wählen Sie **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]** aus. Geben Sie im Feld **[!UICONTROL Value]** die [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID] oder [!UICONTROL Network Ad ID] für die entsprechende Anzeigennetzwerkentität in Search, Social und Commerce ein. Auf diese Weise können Sie die [!DNL Target] Abfragezeichenfolgenparameter für Clickthrough-Zielgruppen für die Entität verwenden.

      Sie können die ID suchen, indem Sie [die entsprechende ID-Spalte zur Entitätsansicht hinzufügen](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] Spalte in der [!UICONTROL Accounts] Ansicht](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] Spalte in der [!UICONTROL Accounts] Ansicht")

      Wenden Sie sich an Ihr Adobe-Account-Team, wenn Sie Hilfe benötigen.

   1. Wählen Sie für die **[!UICONTROL Traffic Allocation Method]** die Option **[!UICONTROL Manual (Default)]** aus und teilen Sie die Zielgruppe 50/50 auf.

   1. Speichern Sie die Aktivität.

1. Verwenden Sie [Target Visual Experience ](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=de)), um Design-Änderungen an der Vorlage für die A/B-Test-Landingpage vorzunehmen.

   * Erlebnis A: Nicht bearbeiten, da es sich um das standardmäßige Landingpage-Erlebnis ohne Personalisierung handelt.

   * Erlebnis B: Verwenden Sie die [!DNL Target]-Benutzeroberfläche, um die Landingpage-Vorlage auf der Grundlage der im Test enthaltenen Assets anzupassen (z. B. Überschriften, Kopie, Schaltflächenplatzierung und Kreative).

   >[!NOTE]
   >
   >Wenden Sie sich beispielsweise an Ihr Adobe-Account-Team, wenn Sie kreative Testfälle benötigen.

## Schritt 2: Einrichten der [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics]

[!DNL Analytics for Target] (A4T) ist eine lösungsübergreifende Integration, die es Advertisern ermöglicht, [!DNL Target] Aktivitäten basierend auf [!DNL Analytics] Konversionsmetriken und Zielgruppensegmenten zu erstellen und die Ergebnisse dann mithilfe von [!DNL Analytics] als Berichtsquelle zu messen. Die gesamte Berichterstellung und Segmentierung für diese Aktivität basiert auf [!DNL Analytics] Datenerfassung.

Weitere Informationen zu [!DNL Analytics for Target], einschließlich eines Links zu Implementierungsanweisungen, finden Sie unter &quot;[Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=de).

### Einrichten des [!DNL Analytics for Target]

Konfigurieren Sie in Analysis Workspace die [!DNL Analytics for Target panel], um Ihre [!DNL Target] Aktivitäten und Erlebnisse zu analysieren. Beachten Sie die folgenden wichtigen Hinweise und Informationen zu Ihren Berichten.

#### Metriken

* Erstellen Sie innerhalb des Arbeitsbereichs ein Bedienfeld, das für das Adobe Advertising-Konto, die Kampagne oder die Anzeigengruppe <!-- only applicable entities? -->, für die der Test ausgeführt wurde. Verwenden Sie Visualisierungen in der Zusammenfassung, um Adobe Advertising-Metriken im selben Bericht wie die [!DNL Target] anzuzeigen.

* Priorisieren Sie die Verwendung von Onsite-Metriken (z. B. Besuche und Konversionen), um die Leistung zu messen.

* Verstehen Sie, dass aggregierte Medienmetriken vom Adobe Advertising (wie Impressionen, Klicks und Kosten) nicht mit [!DNL Target] Metriken abgeglichen werden können.

#### Dimensionen

Die folgenden Dimensionen beziehen sich auf [!DNL Analytics for Target]:

* **Target-**: Name des A/B-Tests

* **Target-Erlebnisse**: Namen der Landingpage-Erlebnisse, die in der Aktivität verwendet werden

* **Target-** > **Erlebnis**: Der Aktivitätsname und der Erlebnisname in derselben Zeile

### Fehlerbehebung bei Analytics für [!DNL Target]

Wenn Sie in Analysis Workspace bemerken, dass die Daten zu Aktivitäten und Erlebnissen nur minimal sind oder nicht ausgefüllt werden, gehen Sie wie folgt vor:

* Stellen Sie sicher, dass dieselbe [!UICONTROL Supplemental Data ID] (SDID) sowohl für [!DNL Target] als auch für [!DNL Analytics] verwendet wird. Sie können die SDID-Werte mit dem [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html?lang=de) auf der Landingpage überprüfen, zu der die Kampagne Benutzer führt.

[Zusätzliche Daten-ID-Werte (SDID) im Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Überprüfen Sie auf derselben Landingpage, ob a) der im Adobe Debugger unter [!UICONTROL Solutions] > [!UICONTROL Target] angezeigte [!UICONTROL Hostname] mit b) dem [!UICONTROL Tracking Server] übereinstimmt, der in [!DNL Target] für die Aktivität angezeigt wird (unter [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] muss bei Aufrufen von [!DNL Target] an den Datenerfassungs-Server von [!DNL Modstats] für Analytics ein [!DNL Analytics]-Tracking-Server gesendet werden.<!-- just "to Analytics?"-->

[Hostnamenwert im Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Wert des Tracking-Servers in Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Weitere Informationen

* [Target mit Analytics integrieren](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html?lang=de) - Beschreibt das Einrichten von [!DNL Target] in Analysis Workspace.
* [A/B-Test - Übersicht](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html?lang=de) Beschreibt A/B-Test-Aktivitäten, die Sie mit Anzeigen in Search, Social und Commerce verwenden können.
* [Überblick über Analytics für Advertising](/help/integrations/analytics/overview.md) - Einführung in Analytics für Advertising, mit dem Sie Site-Interaktionen mit Clickthrough und View-Through in Ihren Analytics-Instanzen verfolgen können.

>[!MORELIKETHIS]
>
>* [Konfigurieren von A/B-Tests in Adobe Target für Advertising DSP Ads](ab-tests-dsp.md)
