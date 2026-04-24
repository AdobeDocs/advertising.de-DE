---
title: Konfigurieren von A/B-Tests für Adobe Advertising DSP Ads in Adobe Target
description: Erfahren Sie, wie Sie einen A/B-Test in  [!DNL Target]  für Ihre DSP-Anzeigen einrichten.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
TQID: https://experienceleague.adobe.com/xETpACcZbZqfFjS58mS-k-kXhm0BT79W0aHz2bdKDGs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1645
ht-degree: 0%

---

# Konfigurieren von A/B-Tests in Adobe Target für Advertising DSP Ads

*Nur Werbetreibende mit Advertising DSP*

Adobe Advertising und Adobe Target erleichtern es Marketing-Experten, ein personalisiertes und vernetztes Erlebnis über bezahlte Medien und Vor-Ort-Messaging hinweg bereitzustellen. Durch die gemeinsame Nutzung von Signalen zwischen den Produkten haben Sie folgende Möglichkeiten:

* Decrease site fall-through rates by linking customers’ ad exposure from DSP campaigns to their on-site experiences.

* Establish A/B testing by mirroring on-site experiences with advertising messaging using Adobe Audience Manager exposure data and click-to-feed [!DNL Target] audiences.

* Measure the impact of unified messaging on an on-site objective lift with simple visualizations in Adobe Analytics for [!DNL Target].

See the following sections for the prerequisites and for instructions to set up click-through and view-through tracking, implement signal sharing between DSP and [!DNL Target] and set up an A/B test activity, and set up [!DNL Analytics] Analysis Workspace to view the test data.

If you have additional questions, contact your Adobe Account Team.

## Voraussetzungen

This use case requires the following products and integrations:

* [!DNL Target]

* [[!DNL Analytics] for Advertising](/help/integrations/analytics/overview.md) integration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)-Integration

* Audience Manager (required for view-through testing only)

## Step 1: Set up the Click-through Framework {#click-through-framework}

![Click-through framework](/help/integrations/assets/target-ct-framework.png)

When you add DSP macros to a click-through URL (the URL displayed when a user clicks an ad and reaches the landing page), DSP automatically captures the placement key by including `${TM_PLACEMENT_ID}` in the click-through URL. This macro captures the alphanumeric placement key and not the numeric placement ID.

![Click-through URL appended to the landing page URL](/help/integrations/assets/target-ct-url.jpg)

### (DSP only) Add DSP macros to your click-through URLs

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Within [!DNL Flashtalking] or Google Campaign Manager 360, manually update the click-through URL for each ad to include the macros required to capture AMO ID variables. The AMO ID variables are used to send click data to Adobe Analytics and to share placement keys for A/B testing. See the following pages for instructions:

* [Append [!DNL Analytics for Advertising] macros to [!DNL Flashtalking] ad tags](/help/integrations/analytics/macros-flashtalking.md). **Hinweis:** Dieses Verfahren ist nicht erforderlich, wenn Ihr Unternehmen eine direkte Partnerschaft mit [!DNL Flashtalking] unterhält und Sie in der Dokumentation zum [!DNL Flashtalking]-Support unter [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros) Datenweiterleitungs-Makros zum Tracking der `s_kwcid`- und `ef_id` verwenden.

* [Append [!DNL Analytics for Advertising] macros to [!DNL Google Campaign Manager 360] ad tags](/help/integrations/analytics/macros-google-campaign-manager.md)

Contact your Adobe Account Team to retrieve the required placement key and finalize the setup, and to make sure that each click-through URL is populated with the placement key.

## Step 2: Set up the view-through framework using Audience Manager {#view-through-framework}

![View-through framework](/help/integrations/assets/targetr-vt-framework.png)

By adding an Audience Manager impression event pixel in your ad tags and placement settings, you can create a test segment for additional view-through testing opportunities.

1. Implement an Audience Manager impression event pixel in your ad tags and DSP placement settings.

   For instructions, see &quot;[Collect media exposure data from Advertising DSP campaigns](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   Make sure you add [DSP macros](/help/dsp/campaign-management/macros.md) to capture all data you want the impression event pixel to pass back, including `${TM_PLACEMENT_ID_NUM}` for the numeric placement ID.

   >[!NOTE]
   >
   >Click-tracking URLs include the `${TM_PLACEMENT_ID}` macro for the alphanumeric placement key, instead of `${TM_PLACEMENT_ID_NUM}` for the numeric placement ID.

1. Configure an Audience Manager segment from the DSP impression data:

   1. Verify that segment data is available:

      1. [Search for the signal](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) for the [key-value pair](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html) that determines at what level the segment users are grouped.

         Use a [supported key](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) with a value that corresponds to a macro that you added to the Audience Manager impression event pixel.

         For example, to group users for a particular placement, use the `d_placement` key. For the value, use an actual numeric placement ID (such as 2501853) that&#39;s captured by the DSP macro `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

         If the search results show user counts for the key-value pair, which indicates that the pixel was placed correctly and data is flowing, then continue to the next step.

   1. [Create a rule-based trait](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) for segment creation in Audience Manager.

      * Name the trait so that it’s easily identifiable within test activities. Store the trait in whichever folder you prefer.

      * Select `Ad Cloud` as the **[!UICONTROL Data Source]**.

      * For the trait expression, use `d_event` as the **[!UICONTROL Key]** and `imp` as the **[!UICONTROL Value]**.

   1. [Set up a test segment](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) for the new trait in Audience Manager, selecting `Ad Cloud` as the **[!UICONTROL Data Source]**.

      Audience Manager automatically splits the segment into a control group that receives the standard landing page experience and a test group that received a personalized onsite experience.

## Step 3: Set up an A/B test activity in [!DNL Target] for DSP

The following instructions highlight information pertaining to the DSP use case.

1. [Bei Adobe Target anmelden](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Erstellen eines A/B-Tests](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. Geben Sie im Feld **[!UICONTROL Enter Activity URL]** die Landingpage-URL für den Test ein.

      >[!NOTE]
      >
      >You can use multiple URLs to test view-through site entry. For more information, see &quot;[Multipage Activity](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; Sie können die wichtigsten Einträge anhand der Seiten-URL leicht identifizieren, indem Sie einen [Site-Einstiegsbericht) &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/integrations/adobe-advertising-dsp/create-advertising-cloud-site-entry-reports) Analytics erstellen.

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

1. Verwenden Sie [Target Visual Experience &#x200B;](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html)), um Design-Änderungen an der Vorlage für die A/B-Test-Landingpage vorzunehmen.

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

* **[!UICONTROL Target Activities]**: Name of the A/B Test

* **[!UICONTROL Target Experiences]**: Names of landing page experiences used within the activity

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**: The activity name and experience name in the same row

### Fehlerbehebung bei Analytics für [!DNL Target] Daten

Wenn Sie in Analysis Workspace bemerken, dass die Daten zu Aktivitäten und Erlebnissen nur minimal sind oder nicht ausgefüllt werden, gehen Sie wie folgt vor:

* Stellen Sie sicher, dass dieselbe [!UICONTROL Supplemental Data ID] (SDID) sowohl für [!DNL Target] als auch für [!DNL Analytics] verwendet wird. Sie können die SDID-Werte überprüfen, indem Sie die [Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) auf der Landingpage verwenden, zu der die Kampagne Benutzer führt.

  [Zusätzliche Daten-ID-Werte (SDID) in Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Überprüfen Sie auf derselben Landingpage, ob a) der in der Adobe Debugger unter [!UICONTROL Solutions] > [!UICONTROL Target] angezeigte [!UICONTROL Hostname] mit b) der in [!DNL Target] für die Aktivität angezeigten [!UICONTROL Tracking Server] übereinstimmt (unter [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] muss bei Aufrufen von [!DNL Target] an den Datenerfassungs-Server von [!DNL Modstats] für Analytics ein [!DNL Analytics]-Tracking-Server gesendet werden.<!-- just "to Analytics?"-->

  [Hostnamenwert in Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

  [Wert des Tracking-Servers in Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Weitere Informationen

* [Integrate Target with Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Explains how to set up [!DNL Target] reporting in Analysis Workspace.
* [A/B Test Overview](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Describes A/B test activities, which you can use with DSP ads.
* [Experiences and offers](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Explains [!DNL Target] tools to determine the on-site content to which DSP test users are exposed.
* [Signals, Traits, and Segments](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - Defines some of the Audience Manager tools that can help with DSP view-through testing.
* [Overview of [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) - Introduces [!DNL Analytics for Advertising], which allows you to track click-through and view-through site interactions in your Analytics instances.

>[!MORELIKETHIS]
>
>* [Configure A/B tests in Adobe Target for Advertising Search, Social, &amp; Commerce ads](ab-tests-search.md)
