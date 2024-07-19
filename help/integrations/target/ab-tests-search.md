---
title: Konfigurieren von A/B-Tests für Adobe Advertising-Suchen-, Social- und Commerce-Anzeigen in Adobe Target
description: Erfahren Sie, wie Sie in [!DNL Target] einen A/B-Test für Ihre [!DNL Google Ads] und [!DNL Microsoft Advertising] Anzeigen in Search, Social und Commerce einrichten.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Konfigurieren von A/B-Tests in Adobe Target für Advertising Search-, Social- und Commerce-Anzeigen

*Advertiser mit Advertising Search, Social &amp; Commerce only*

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising] Konten*

Mit Adobe Advertising und Adobe Target können Sie mühelos A/B-Tests für das Erlebnis von Landingpages für den Traffic digitaler Werbung [!DNL Google Ads] und [!DNL Microsoft Advertising] einrichten, um:

* Verbesserung der Konversionsraten (CVR) und der Akquise-Effizienz (z. B. CPA, CPL und CAC).

* Bereitstellung eines personalisierteren Landingpage-Erlebnisses, das für die Anzeige relevant ist (z. B. Abgleich von Bild/Video-Kreativelement, Kopie, Keyword oder anderem Werbesignal mit der Landingpage).

Sie können auch die nativen Dimensionen für die Integrationsberichte [[!DNL Analytics] für Advertising](/help/integrations/analytics/overview.md) und [[!DNL Analytics] für  [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) kombinieren, die in Adobe Analytics integriert sind, um Ihre Testdaten mit [!DNL Analytics] -Metriken und Erfolgsereignissen zu messen und zu visualisieren.

In den folgenden Abschnitten finden Sie die Voraussetzungen, Anweisungen zum Einrichten von A/B-Tests in [!DNL Target] für Clickthrough-Traffic von Anzeigen in Search, Social und Commerce sowie Tipps zum Messen und Visualisieren Ihrer Tests in [!DNL Analytics].

## Voraussetzungen

### Erforderliche Produkte

* Suchen, Social und Commerce
* [!DNL Target]

### Empfohlene Produkte und Integrationen

* [!DNL Analytics]

* [[!DNL Analytics] für Advertising](/help/integrations/analytics/overview.md) integration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* Integration von [[!DNL Analytics] für  [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)

## Schritt 1: Erstellen einer A/B-Test-Aktivität in [!DNL Target] für Suche, Social und Commerce

In den folgenden Anweisungen werden Informationen zum Anwendungsfall &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;hervorgehoben.

1. [Melden Sie sich bei Adobe Target an](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Erstellen eines A/B-Tests](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. Geben Sie im Feld **[!UICONTROL Enter Activity URL]** die URL der Landingpage für den Test ein.

   1. Geben Sie im Feld **[!UICONTROL Goal]** die Erfolgsmetrik für den Test ein.

      >[!NOTE]
      >
      >Stellen Sie sicher, dass [!DNL Analytics] als Datenquelle in [!DNL Target] aktiviert ist und dass die richtige Report Suite ausgewählt ist.

   1. Setzen Sie die **[!UICONTROL Priority]** auf `High` oder `999`, um Konflikte zu vermeiden, wenn Benutzer im Testsegment ein falsches On-site-Erlebnis erhalten.


   1. Wählen Sie in **[!UICONTROL Reporting Settings]** die **[!UICONTROL Company Name]** und **[!UICONTROL Report Suite]** aus, die mit Ihrem Suchkonto, Social- und Commerce-Konto verbunden sind.

      Weitere Tipps zur Berichterstellung finden Sie unter &quot;[Best Practices für die Berichterstellung und Fehlerbehebung](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html)&quot;.

   1. Geben Sie im Feld **[!UICONTROL Date Range]** das entsprechende Start- und Enddatum für den Test ein.

   1. Wählen Sie **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]** aus. Geben Sie im Feld **[!UICONTROL Value]** die [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID] oder [!UICONTROL Network Ad ID] für die entsprechende Anzeigennetzwerkentität in Search, Social und Commerce ein. Auf diese Weise können Sie die [!DNL Target] Abfragezeichenfolgenparameter für Clickthrough-Zielgruppen für die Entität verwenden.

      Sie können die ID finden, indem Sie [die entsprechende ID-Spalte zur Entitätsansicht hinzufügen](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] Spalte in der Spalte [!UICONTROL Accounts] view](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] in der [!UICONTROL Accounts] view")

      Wenden Sie sich an Ihr Adobe-Account-Team, wenn Sie Hilfe benötigen.

   1. Wählen Sie für den Wert &quot;**[!UICONTROL Traffic Allocation Method]**&quot;den Wert &quot;**[!UICONTROL Manual (Default)]**&quot;aus und teilen Sie die Zielgruppe 50/50 auf.

   1. Speichern Sie die Aktivität.

1. Verwenden Sie [Target Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html), um Designänderungen an der Landingpage-Vorlage für A/B-Tests vorzunehmen.

   * Erlebnis A: Nicht bearbeiten, da dies das standardmäßige/steuerbare Landingpage-Erlebnis ohne Personalisierung ist.

   * Erlebnis B: Verwenden Sie die [!DNL Target] -Benutzeroberfläche, um die Landingpage-Vorlage basierend auf den im Test enthaltenen Assets anzupassen (z. B. Überschriften, Kopie, Schaltflächenplatzierung und kreative Elemente).

   >[!NOTE]
   >
   >Wenden Sie sich beispielsweise in Anwendungsfällen für kreative Tests an Ihr Adobe-Account-Team.

## Schritt 2: Einrichten der [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics]

[!DNL Analytics for Target] (A4T) ist eine lösungsübergreifende Integration, die es Werbetreibenden ermöglicht, [!DNL Target] -Aktivitäten basierend auf [!DNL Analytics] Konversionsmetriken und Zielgruppensegmenten zu erstellen und die Ergebnisse dann mit [!DNL Analytics] als Berichtsquelle zu messen. Die gesamte Berichterstellung und Segmentierung für diese Aktivität basiert auf der [!DNL Analytics] -Datenerfassung.

Weitere Informationen zu [!DNL Analytics for Target], einschließlich eines Links zu Implementierungsanweisungen, finden Sie unter &quot;[Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Einrichten des [!DNL Analytics for Target]-Bedienfelds

Konfigurieren Sie in Analysis Workspace die [!DNL Analytics for Target panel], um Ihre [!DNL Target] -Aktivitäten und -Erlebnisse zu analysieren. Beachten Sie die folgenden wichtigen Hinweise und Informationen zu Ihren Berichten.

#### Metriken

* Erstellen Sie einen Bereich innerhalb des Arbeitsbereichs, der spezifisch für das Adobe Advertising-Konto, die Kampagne oder die Anzeigengruppe<!-- only applicable entities? --> ist, für das bzw. die der Test ausgeführt wurde. Verwenden Sie Zusammenfassende Visualisierungen, um Adobe Advertising-Metriken im selben Bericht wie die [!DNL Target] Testleistung anzuzeigen.

* Priorisieren Sie die Verwendung von On-site-Metriken (z. B. Besuche und Konversionen), um die Leistung zu messen.

* Beachten Sie, dass aggregierte Medienmetriken von Adobe Advertising (wie Impressionen, Klicks und Kosten) nicht mit [!DNL Target] -Metriken abgeglichen werden können.

#### Dimensionen

Die folgenden Dimensionen beziehen sich auf [!DNL Analytics for Target]:

* **Target Activities**: Name des A/B-Tests

* **Target-Erlebnisse**: Namen der in der Aktivität verwendeten Landingpage-Erlebnisse

* **Target-Aktivität** > **Erlebnis**: Der Aktivitäts- und Erlebnisname in derselben Zeile

### Fehlerbehebung bei Analytics für [!DNL Target]-Daten

Wenn Sie in Analysis Workspace feststellen, dass die Daten zu Aktivitäten und Erlebnissen minimal sind oder nicht ausgefüllt werden, führen Sie die folgenden Schritte aus:

* Stellen Sie sicher, dass sowohl für [!DNL Target] als auch für [!DNL Analytics] dieselbe [!UICONTROL Supplemental Data ID] (SDID) verwendet wird. Sie können die SDID-Werte mithilfe des [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) auf der Landingpage überprüfen, zu der die Benutzer durch die Kampagne geleitet werden.

[Zusätzliche Daten-ID-Werte (SDID) in Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Vergewissern Sie sich auf derselben Landingpage, dass a) das im Adobe Debugger unter [!UICONTROL Solutions] > [!UICONTROL Target] angezeigte [!UICONTROL Hostname] mit dem in [!DNL Target] für die Aktivität angezeigten [!UICONTROL Tracking Server] übereinstimmt (unter [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] erfordert, dass ein [!DNL Analytics]-Tracking-Server in Aufrufen von [!DNL Target] an den [!DNL Modstats]-Datenerfassungsserver für Analytics gesendet wird.<!-- just "to Analytics?"-->

[Hostnamenwert in Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Tracking-Server-Wert in Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Weitere Informationen

* [Target in Analytics integrieren](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Erklärt, wie Sie die [!DNL Target] -Berichterstellung in Analysis Workspace einrichten.
* [Überblick über A/B-Tests](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Beschreibt A/B-Test-Aktivitäten, die Sie mit Anzeigen in Search, Social und Commerce verwenden können.
* [Überblick über Analytics für Advertising](/help/integrations/analytics/overview.md) - Einführung in Analytics für Advertising, mit dem Sie Clickthrough- und Durchsichts-Site-Interaktionen in Ihren Analytics-Instanzen verfolgen können.

>[!MORELIKETHIS]
>
>* [Konfigurieren von A/B-Tests in Adobe Target für Advertising DSP Ads](ab-tests-dsp.md)
