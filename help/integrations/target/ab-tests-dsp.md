---
title: Konfigurieren von A/B-Tests für Adobe Advertising DSP Ads in Adobe Target
description: Erfahren Sie, wie Sie einen A/B-Test in  [!DNL Target]  für Ihre DSP-Anzeigen einrichten.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 0%

---

# Konfigurieren von A/B-Tests in Adobe Target für Advertising DSP Ads

*Nur Werbetreibende mit Advertising DSP*

Adobe Advertising und Adobe Target erleichtern es Marketing-Experten, ein personalisiertes und vernetztes Erlebnis über bezahlte Medien und Vor-Ort-Messaging hinweg bereitzustellen. Durch die gemeinsame Nutzung von Signalen zwischen den Produkten haben Sie folgende Möglichkeiten:

* Verringern Sie die Fallthrough-Raten von Websites, indem Sie die Anzeigenexposition von Kundinnen und Kunden aus DSP-Kampagnen mit ihren Onsite-Erlebnissen verknüpfen.

* Etablieren von A/B-Tests durch Spiegelung der Erlebnisse auf der Site mit Werbebotschaften mithilfe von Adobe Audience Manager-Belichtungsdaten und „Click-to-Feed“-[!DNL Target].

* Messen der Wirkung von Unified Messaging auf die objektive Steigerung der Kundenzufriedenheit vor Ort mit einfachen Visualisierungen in Adobe Analytics for [!DNL Target].

In den folgenden Abschnitten finden Sie die Voraussetzungen und Anweisungen zum Einrichten von Clickthrough- und View-Through-Tracking, zum Implementieren der Signalfreigabe zwischen DSP und [!DNL Target] und zum Einrichten einer A/B-Testaktivität sowie zum Einrichten [!DNL Analytics] Analysis Workspace zum Anzeigen der Testdaten.

Bei weiteren Fragen wenden Sie sich bitte an adcloud_support@adobe.com.

## Voraussetzungen

Für diesen Anwendungsfall sind die folgenden Produkte und Integrationen erforderlich:

* [!DNL Target]

* [[!DNL Analytics] Integration mit Advertising](/help/integrations/analytics/overview.md)<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)-Integration

* Audience Manager (nur für Durchsichtstests erforderlich)

## Schritt 1: Einrichten des Clickthrough-Frameworks {#click-through-framework}

![Clickthrough-Framework](/help/integrations/assets/target-ct-framework.png)

Wenn Sie DSP-Makros zu einer Clickthrough-URL hinzufügen (die URL, die angezeigt wird, wenn ein(e) Benutzende(r) auf eine Anzeige klickt und die Landingpage erreicht), erfasst DSP automatisch den Platzierungsschlüssel, indem `${TM_PLACEMENT_ID}` in die Clickthrough-URL aufgenommen wird. Dieses Makro erfasst den alphanumerischen Platzierungsschlüssel und nicht die numerische Platzierungs-ID.

![Click-Through-URL, die an die Landingpage-URL angehängt ist](/help/integrations/assets/target-ct-url.jpg)

### (Nur DSP) Hinzufügen von DSP-Makros zu Ihren Clickthrough-URLs

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Aktualisieren Sie in [!DNL Flashtalking] oder Google Campaign Manager 360 die Clickthrough-URL für jede Anzeige manuell, um die Makros einzuschließen, die zur Erfassung von AMO ID-Variablen erforderlich sind. Die AMO ID-Variablen werden verwendet, um Klickdaten an Adobe Analytics zu senden und Platzierungsschlüssel für A/B-Tests freizugeben. Anweisungen finden Sie auf den folgenden Seiten:

* [Append [!DNL Analytics for Advertising] Macros to. [!DNL Flashtalking]  Tags](/help/integrations/analytics/macros-flashtalking.md). **Hinweis:** Dieses Verfahren ist nicht erforderlich, wenn Ihr Unternehmen eine direkte Partnerschaft mit [!DNL Flashtalking] unterhält und Sie in der Dokumentation zum [!DNL Flashtalking]-Support unter [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros) Datenweiterleitungs-Makros zum Tracking der `s_kwcid`- und `ef_id` verwenden.

* [Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md)

Wenden Sie sich an Ihr Adobe-Account-Team und die Advertising Solutions Group (aac-advertising-solutions-group@adobe.com), um den erforderlichen Platzierungsschlüssel abzurufen und die Einrichtung abzuschließen, und um sicherzustellen, dass jede Clickthrough-URL mit dem Platzierungsschlüssel ausgefüllt ist.

## Schritt 2: Einrichten des View-Through-Frameworks mithilfe von Audience Manager {#view-through-framework}

![Durchsichts-Framework](/help/integrations/assets/targetr-vt-framework.png)

Durch Hinzufügen eines Audience Manager-Impression-Ereignis-Pixels zu Ihren Anzeigen-Tags und Platzierungseinstellungen können Sie ein Testsegment für zusätzliche Gelegenheiten zum Durchschauen erstellen.

1. Implementieren Sie ein Audience Manager Impression Event-Pixel in Ihren Anzeigentags und DSP-Platzierungseinstellungen.

   Anweisungen finden Sie unter &quot;[ von Medienexpositionsdaten aus Advertising DSP-Kampagnen ](/help/integrations/audience-manager/media-data-integration/collect.md)&quot;.

   Stellen Sie sicher, dass Sie [DSP](/help/dsp/campaign-management/macros.md)Makros hinzufügen, um alle Daten zu erfassen, die das Impression-Ereignispixel zurückgeben soll, einschließlich `${TM_PLACEMENT_ID_NUM}` für die numerische Platzierungs-ID.

   >[!NOTE]
   >
   >Klick-Tracking-URLs enthalten das `${TM_PLACEMENT_ID}`-Makro für den alphanumerischen Platzierungsschlüssel anstelle der numerischen Platzierungs-ID `${TM_PLACEMENT_ID_NUM}`.

1. Konfigurieren Sie ein Audience Manager-Segment aus den DSP-Impressionsdaten:

   1. Überprüfen Sie, ob Segmentdaten verfügbar sind:

      1. [Nach dem Signal suchen](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) nach dem [Schlüssel-Wert-Paar](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html), das bestimmt, auf welcher Ebene die Segmentbenutzer gruppiert werden.

         Verwenden Sie einen [unterstützten Schlüssel](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) mit einem Wert, der einem Makro entspricht, das Sie dem Audience Manager Impression Event-Pixel hinzugefügt haben.

         Um beispielsweise Benutzer für eine bestimmte Platzierung zu gruppieren, verwenden Sie den `d_placement` . Verwenden Sie für den Wert eine tatsächliche numerische Platzierungs-ID (z. B. 2501853), die vom DSP-`${TM_PLACEMENT_ID_NUM}` erfasst wird. <!-- Explain where to find the placement ID, other than in a custom report. -->

         Wenn die Suchergebnisse Benutzerzahlen für das Schlüssel-Wert-Paar zeigen, was anzeigt, dass das Pixel korrekt platziert wurde und Daten fließen, fahren Sie mit dem nächsten Schritt fort.

   1. [Erstellen einer regelbasierten Eigenschaft](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) für die Segmenterstellung in Audience Manager.

      * Benennen Sie die Eigenschaft, damit sie in Testaktivitäten leicht identifiziert werden kann. Speichern Sie die Eigenschaft in einem beliebigen Ordner.

      * Wählen Sie `Ad Cloud` als **[!UICONTROL Data Source]** aus.

      * Verwenden Sie für den Eigenschaftsausdruck `d_event` als **[!UICONTROL Key]** und `imp` als **[!UICONTROL Value]**.

   1. [Testsegment einrichten](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) Wählen Sie für die neue Eigenschaft in Audience Manager `Ad Cloud` als **[!UICONTROL Data Source]** aus.

      Audience Manager teilt das Segment automatisch in eine Kontrollgruppe auf, die das standardmäßige Landingpage-Erlebnis erhält, und in eine Testgruppe, die ein personalisiertes Onsite-Erlebnis erhalten hat.

## Schritt 3: Einrichten einer A/B-Test -Aktivität in [!DNL Target] für DSP

In den folgenden Anweisungen werden Informationen zum DSP-Anwendungsfall hervorgehoben.

1. [Bei Adobe Target anmelden](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Erstellen eines A/B-Tests](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. Geben Sie im Feld **[!UICONTROL Enter Activity URL]** die Landingpage-URL für den Test ein.

      >[!NOTE]
      >
      >Sie können mehrere URLs verwenden, um die Viewthrough-Site-Eingabe zu testen. Weitere Informationen finden Sie unter &quot;[Mehrseitige Aktivität](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html). Sie können die wichtigsten Einträge anhand der Seiten-URL leicht identifizieren, indem Sie einen [Site-Einstiegsbericht) ](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/integrations/adobe-advertising-dsp/create-advertising-cloud-site-entry-reports) Analytics erstellen.

   1. Geben Sie im Feld **[!UICONTROL Goal]** die Erfolgsmetrik für den Test ein.

      >[!NOTE]
      >
      >Stellen Sie sicher, dass [!DNL Analytics] als Datenquelle in [!DNL Target] aktiviert ist und dass die richtige Report Suite ausgewählt ist.

   1. Legen Sie die **[!UICONTROL Priority]** auf `High` oder `999` fest, um Konflikte zu vermeiden, wenn Benutzende im Testsegment ein falsches Onsite-Erlebnis erhalten.

   1. Wählen Sie in **[!UICONTROL Reporting Settings]** die **[!UICONTROL Company Name]** und **[!UICONTROL Report Suite]** aus, die mit Ihrem DSP-Konto verbunden sind.

      Weitere Tipps zum Reporting finden Sie unter [Best Practices für das Reporting und Fehlerbehebung](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).

   1. Geben Sie im Feld **[!UICONTROL Date Range]** das entsprechende Start- und Enddatum für den Test ein.

   1. Zielgruppen zur Aktivität hinzufügen:

      1. Wählen Sie das [Segment“ aus, das Sie zuvor in Audience Manager erstellt haben, um Durchsichts-Zielgruppen zu testen](#view-through-framework).

      1. Wählen Sie **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]** aus und geben Sie den DSP-Platzierungsschlüssel in das Feld **[!UICONTROL Value]** ein, um die Target-Abfragezeichenfolgenparameter für Clickthrough-Zielgruppen zu verwenden.

   1. Wählen Sie für die **[!UICONTROL Traffic Allocation Method]** die Option **[!UICONTROL Manual (Default)]** aus und teilen Sie die Zielgruppe 50/50 auf.

   1. Speichern Sie die Aktivität.

1. Verwenden Sie [Target Visual Experience ](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)), um Design-Änderungen an der Vorlage für die A/B-Test-Landingpage vorzunehmen.

   * Erlebnis A: Nicht bearbeiten, da es sich um das standardmäßige Landingpage-Erlebnis ohne Personalisierung handelt.

   * Erlebnis B: Verwenden Sie die [!DNL Target]-Benutzeroberfläche, um die Landingpage-Vorlage auf der Grundlage der im Test enthaltenen Assets anzupassen (z. B. Überschriften, Kopie, Schaltflächenplatzierung und Kreative).

   >[!NOTE]
   >
   >Wenden Sie sich beispielsweise an Ihr Adobe-Account-Team, wenn Sie kreative Testfälle benötigen.

## Schritt 4: Einrichten der [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) ist eine lösungsübergreifende Integration, die es Advertisern ermöglicht, [!DNL Target] Aktivitäten basierend auf [!DNL Analytics] Konversionsmetriken und Zielgruppensegmenten zu erstellen und die Ergebnisse dann mithilfe von [!DNL Analytics] als Berichtsquelle zu messen. Die gesamte Berichterstellung und Segmentierung für diese Aktivität basiert auf [!DNL Analytics] Datenerfassung.

Weitere Informationen zu [!DNL Analytics for Target], einschließlich eines Links zu Implementierungsanweisungen, finden Sie unter &quot;[Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html).

### Einrichten des [!DNL Analytics for Target]

Konfigurieren Sie in Analysis Workspace die [!DNL Analytics for Target panel], um Ihre [!DNL Target] Aktivitäten und Erlebnisse zu analysieren. Beachten Sie die folgenden wichtigen Hinweise und Informationen zu Ihren Berichten.

#### Metriken

* Erstellen Sie im Arbeitsbereich ein Bedienfeld, das speziell für die Adobe Advertising-Kampagne, das -Paket oder die Platzierung gilt, für die der Test ausgeführt wurde. Verwenden Sie zusammenfassende Visualisierungen, um Adobe Advertising-Metriken im selben Bericht wie die [!DNL Target] anzuzeigen.

* Priorisieren Sie die Verwendung von Onsite-Metriken (z. B. Besuche und Konversionen), um die Leistung zu messen.

* Verstehen Sie, dass aggregierte Medienmetriken aus Adobe Advertising (wie Impressionen, Klicks und Kosten) nicht mit [!DNL Target] Metriken abgeglichen werden können.

#### Dimensionen

Die folgenden Dimensionen beziehen sich auf [!DNL Analytics for Target]:

* **[!UICONTROL Target Activities]**: Name des A/B-Tests

* **[!UICONTROL Target Experiences]**: Namen der Landingpage-Erlebnisse, die in der Aktivität verwendet werden

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**: Der Aktivitätsname und der Erlebnisname in derselben Zeile

### Fehlerbehebung bei Analytics für [!DNL Target]

Wenn Sie in Analysis Workspace bemerken, dass die Daten zu Aktivitäten und Erlebnissen nur minimal sind oder nicht ausgefüllt werden, gehen Sie wie folgt vor:

* Stellen Sie sicher, dass dieselbe [!UICONTROL Supplemental Data ID] (SDID) sowohl für [!DNL Target] als auch für [!DNL Analytics] verwendet wird. Sie können die SDID-Werte mit dem [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) auf der Landingpage überprüfen, zu der die Kampagne Benutzer führt.

[Zusätzliche Daten-ID-Werte (SDID) in Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Überprüfen Sie auf derselben Landingpage, ob a) der in der Adobe Debugger unter [!UICONTROL Solutions] > [!UICONTROL Target] angezeigte [!UICONTROL Hostname] mit b) der in [!DNL Target] für die Aktivität angezeigten [!UICONTROL Tracking Server] übereinstimmt (unter [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] muss bei Aufrufen von [!DNL Target] an den Datenerfassungs-Server von [!DNL Modstats] für Analytics ein [!DNL Analytics]-Tracking-Server gesendet werden.<!-- just "to Analytics?"-->

[Hostnamenwert in Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Wert des Tracking-Servers in Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Weitere Informationen

* [Target mit Analytics integrieren](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Beschreibt das Einrichten von [!DNL Target] in Analysis Workspace.
* [A/B-Test - Übersicht](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) Beschreibt A/B-Test -Aktivitäten, die Sie mit DSP Ads verwenden können.
* [Erlebnisse und Angebote](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Erläutert [!DNL Target] Tools zur Bestimmung der Inhalte auf der Site, mit denen DSP-Testbenutzer konfrontiert werden.
* [Signale, Eigenschaften und Segmente](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - Definiert einige der Audience Manager-Tools, die beim Durchsichtstest in DSP helfen können.
* [Überblick über Analytics für Advertising](/help/integrations/analytics/overview.md) - Einführung in Analytics für Advertising, mit dem Sie Site-Interaktionen mit Clickthrough und View-Through in Ihren Analytics-Instanzen verfolgen können.

>[!MORELIKETHIS]
>
>* [Konfigurieren von A/B-Tests in Adobe Target für Advertising Search, Social und Commerce Ads](ab-tests-search.md)
