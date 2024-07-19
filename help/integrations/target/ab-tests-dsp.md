---
title: Konfigurieren von A/B-Tests für Adobe Advertising DSP-Anzeigen in Adobe Target
description: Erfahren Sie, wie Sie in [!DNL Target] einen A/B-Test für Ihre DSP-Anzeigen einrichten.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 7ffa5d3e9f1aae0f9d66d87c74807e491e818daa
workflow-type: tm+mt
source-wordcount: '1384'
ht-degree: 0%

---

# Konfigurieren von A/B-Tests in Adobe Target für Advertising DSP Ads

*Advertiser nur mit Advertising DSP*

Adobe Advertising und Adobe Target erleichtern es Marketern, personalisierte und vernetzte Erlebnisse über Paid Media und On-site-Nachrichten bereitzustellen. Durch die Freigabe von Signalen zwischen den Produkten können Sie:

* Verringern Sie die Site-Durchfallraten, indem Sie die Anzeigenbelichtung von Kunden aus DSP Kampagnen mit ihren Vor-Ort-Erlebnissen verknüpfen.

* Richten Sie A/B-Tests ein, indem Sie On-site-Erlebnisse mit Werbe-Messaging unter Verwendung von Adobe Audience Manager-Belichtungsdaten und Clickthrough-Feed-Zielgruppen [!DNL Target] spiegeln.

* Messen Sie die Wirkung von einheitlichem Messaging auf eine objektive Steigerung vor Ort mit einfachen Visualisierungen in Adobe Analytics für [!DNL Target].

In den folgenden Abschnitten finden Sie Anweisungen zu den Voraussetzungen und Anweisungen zum Einrichten des Clickthrough- und Viewthrough-Trackings, Implementieren der Signalfreigabe zwischen DSP und [!DNL Target], Einrichten einer A/B-Test-Aktivität und Einrichten von [!DNL Analytics] Analysis Workspace zur Anzeige der Testdaten.

Wenn Sie weitere Fragen haben, wenden Sie sich an adcloud_support@adobe.com.

## Voraussetzungen

Für dieses Anwendungsbeispiel sind die folgenden Produkte und Integrationen erforderlich:

* [!DNL Target]

* [[!DNL Analytics] für Advertising](/help/integrations/analytics/overview.md) integration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* Integration von [[!DNL Analytics] für  [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)

* Audience Manager (nur für Durchsichtstests erforderlich)

## Schritt 1: Einrichten des Clickthrough-Frameworks {#click-through-framework}

![Clickthrough-Framework](/help/integrations/assets/target-ct-framework.png)

Wenn Sie DSP Makros zu einer Clickthrough-URL hinzufügen (die URL, die angezeigt wird, wenn ein Benutzer auf eine Anzeige klickt und die Landingpage erreicht), erfasst DSP automatisch den Platzierungsschlüssel, indem er `${TM_PLACEMENT_ID}` in die Clickthrough-URL einbezieht. Dieses Makro erfasst den alphanumerischen Platzierungsschlüssel und nicht die numerische Platzierungs-ID.

![An die URL der Landingpage angehängte Clickthrough-URL](/help/integrations/assets/target-ct-url.jpg)

### (Nur DSP) Hinzufügen von DSP Makros zu Ihren Clickthrough-URLS

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Aktualisieren Sie im Flash-Gespräch oder in Google Campaign Manager 360 die Clickthrough-URL für jede Anzeige manuell, um die Makros einzuschließen, die zum Erfassen von AMO-ID-Variablen erforderlich sind. Die AMO-ID-Variablen werden verwendet, um Klickdaten an Adobe Analytics zu senden und Platzierungsschlüssel für A/B-Tests freizugeben. Anweisungen finden Sie auf den folgenden Seiten:

* [Anhängen von [!DNL Analytics for Advertising] Makros an  [!DNL Flashtalking] Anzeigen-Tags](/help/integrations/analytics/macros-flashtalking.md)

* [Anhängen von [!DNL Analytics for Advertising] Makros an  [!DNL Google Campaign Manager 360] Anzeigen-Tags](/help/integrations/analytics/macros-google-campaign-manager.md)

Wenden Sie sich an Ihr Adobe Account Team und die Advertising Solutions Group (aac-advertising-solutions-group@adobe.com), um den erforderlichen Platzierungsschlüssel abzurufen und die Einrichtung abzuschließen und sicherzustellen, dass jede Clickthrough-URL mit dem Platzierungsschlüssel ausgefüllt wird.

## Schritt 2: Einrichten des Durchsichts-Frameworks mit dem Audience Manager {#view-through-framework}

![Durchsichtsframework](/help/integrations/assets/targetr-vt-framework.png)

Durch Hinzufügen eines Audience Manager-Impressionsereignis-Pixels zu Ihren Anzeigen-Tags und Platzierungseinstellungen können Sie ein Testsegment erstellen, um weitere Ansichtsdurchsatztestmöglichkeiten zu erhalten.

1. Implementieren Sie ein Impressionsereignis-Pixel für Audience Manager in Ihre Anzeigen-Tags und DSP Platzierungseinstellungen.

   Anweisungen finden Sie unter &quot;[Erfassen von Medienbelichtungsdaten aus Advertising DSP-Kampagnen](/help/integrations/audience-manager/media-data-integration/collect.md)&quot;.

   Stellen Sie sicher, dass Sie [DSP Makros](/help/dsp/campaign-management/macros.md) hinzufügen, um alle Daten zu erfassen, für die das Impressionsereignis-Pixel zurückgegeben werden soll, einschließlich `${TM_PLACEMENT_ID_NUM}` für die numerische Platzierungs-ID.

   >[!NOTE]
   >
   >Klick-Tracking-URLs enthalten das Makro `${TM_PLACEMENT_ID}` für den alphanumerischen Platzierungsschlüssel anstelle von `${TM_PLACEMENT_ID_NUM}` für die numerische Platzierungs-ID.

1. Konfigurieren Sie ein Audience Manager-Segment aus DSP Impressionsdaten:

   1. Stellen Sie sicher, dass die Segmentdaten verfügbar sind:

      1. [Suchen Sie nach dem Signal](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) für das Schlüssel-Wert-Paar [3}, das bestimmt, auf welcher Ebene die Segmentbenutzer gruppiert werden.](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html)

         Verwenden Sie einen [unterstützten Schlüssel](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) mit einem Wert, der einem Makro entspricht, das Sie dem Impressionsereignis-Pixel des Audience Managers hinzugefügt haben.

         Um beispielsweise Benutzer für eine bestimmte Platzierung zu gruppieren, verwenden Sie den Schlüssel &quot;`d_placement`&quot;. Verwenden Sie für den Wert eine tatsächliche numerische Platzierungs-ID (z. B. 2501853), die vom DSP Makro `${TM_PLACEMENT_ID_NUM}` <!-- Explain where to find the placement ID, other than in a custom report. --> erfasst wird.

         Wenn in den Suchergebnissen die Benutzerzahlen für das Schlüssel-Wert-Paar angezeigt werden, was darauf hinweist, dass das Pixel korrekt platziert wurde und Daten fließen, fahren Sie mit dem nächsten Schritt fort.

   1. [Erstellen Sie eine regelbasierte Eigenschaft](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) für die Segmenterstellung in Audience Manager.

      * Benennen Sie die Eigenschaft so, dass sie in Testaktivitäten leicht identifiziert werden kann. Speichern Sie die Eigenschaft in dem Ordner, den Sie bevorzugen.

      * Wählen Sie `Ad Cloud` als **[!UICONTROL Data Source]** aus.

      * Verwenden Sie für den Eigenschaftsausdruck `d_event` als **[!UICONTROL Key]** und `imp` als **[!UICONTROL Value]**.

   1. [Richten Sie ein Testsegment](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) für die neue Eigenschaft in Audience Manager ein und wählen Sie `Ad Cloud` als **[!UICONTROL Data Source]** aus.

      Audience Manager teilt das Segment automatisch in eine Kontrollgruppe auf, die das standardmäßige Landingpage-Erlebnis erhält, und in eine Testgruppe, die ein personalisiertes Onsite-Erlebnis erhalten hat.

## Schritt 3: Einrichten einer A/B-Test-Aktivität in [!DNL Target] für DSP

In den folgenden Anweisungen werden Informationen zum DSP Anwendungsfall hervorgehoben.

1. [Melden Sie sich bei Adobe Target an](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Erstellen eines A/B-Tests](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. Geben Sie im Feld **[!UICONTROL Enter Activity URL]** die URL der Landingpage für den Test ein.

      >[!NOTE]
      >
      >Sie können mehrere URLs verwenden, um den Viewthrough-Site-Einstieg zu testen. Weitere Informationen finden Sie unter &quot;[Mehrseitige Aktivität](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html)&quot;. Sie können die wichtigsten Einträge einfach anhand der Seiten-URL identifizieren, indem Sie in Analytics einen [Site-Einstiegsbericht](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) erstellen.

   1. Geben Sie im Feld **[!UICONTROL Goal]** die Erfolgsmetrik für den Test ein.

      >[!NOTE]
      >
      >Stellen Sie sicher, dass [!DNL Analytics] als Datenquelle in [!DNL Target] aktiviert ist und dass die richtige Report Suite ausgewählt ist.

   1. Setzen Sie die **[!UICONTROL Priority]** auf `High` oder `999`, um Konflikte zu vermeiden, wenn Benutzer im Testsegment ein falsches On-site-Erlebnis erhalten.

   1. Wählen Sie in **[!UICONTROL Reporting Settings]** die **[!UICONTROL Company Name]** und **[!UICONTROL Report Suite]** aus, die mit Ihrem DSP verbunden sind.

      Weitere Tipps zur Berichterstellung finden Sie unter &quot;[Best Practices für die Berichterstellung und Fehlerbehebung](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html)&quot;.

   1. Geben Sie im Feld **[!UICONTROL Date Range]** das entsprechende Start- und Enddatum für den Test ein.

   1. Fügen Sie der Aktivität Zielgruppen hinzu:

      1. Wählen Sie das Segment [aus, das Sie zuvor in Audience Manager erstellt haben, um Durchsichtszielgruppen zu testen](#view-through-framework).

      1. Wählen Sie **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]** und geben Sie den DSP Platzierungsschlüssel in das Feld **[!UICONTROL Value]** ein, um die Abfragezeichenfolgenparameter Target für Clickthrough-Zielgruppen zu verwenden.

   1. Wählen Sie für den Wert &quot;**[!UICONTROL Traffic Allocation Method]**&quot;den Wert &quot;**[!UICONTROL Manual (Default)]**&quot;aus und teilen Sie die Zielgruppe 50/50 auf.

   1. Speichern Sie die Aktivität.

1. Verwenden Sie [Target Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html), um Designänderungen an der Landingpage-Vorlage für A/B-Tests vorzunehmen.

   * Erlebnis A: Nicht bearbeiten, da dies das standardmäßige/steuerbare Landingpage-Erlebnis ohne Personalisierung ist.

   * Erlebnis B: Verwenden Sie die [!DNL Target] -Benutzeroberfläche, um die Landingpage-Vorlage basierend auf den im Test enthaltenen Assets anzupassen (z. B. Überschriften, Kopie, Schaltflächenplatzierung und kreative Elemente).

   >[!NOTE]
   >
   >Wenden Sie sich beispielsweise in Anwendungsfällen für kreative Tests an Ihr Adobe-Account-Team.

## Schritt 4: Einrichten der [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) ist eine lösungsübergreifende Integration, die es Werbetreibenden ermöglicht, [!DNL Target] -Aktivitäten basierend auf [!DNL Analytics] Konversionsmetriken und Zielgruppensegmenten zu erstellen und die Ergebnisse dann mit [!DNL Analytics] als Berichtsquelle zu messen. Die gesamte Berichterstellung und Segmentierung für diese Aktivität basiert auf der [!DNL Analytics] -Datenerfassung.

Weitere Informationen zu [!DNL Analytics for Target], einschließlich eines Links zu Implementierungsanweisungen, finden Sie unter &quot;[Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Einrichten des [!DNL Analytics for Target]-Bedienfelds

Konfigurieren Sie in Analysis Workspace die [!DNL Analytics for Target panel], um Ihre [!DNL Target] -Aktivitäten und -Erlebnisse zu analysieren. Beachten Sie die folgenden wichtigen Hinweise und Informationen zu Ihren Berichten.

#### Metriken

* Erstellen Sie innerhalb des Arbeitsbereichs einen Bereich, der speziell für die Adobe Advertising-Kampagne, das Paket oder die Platzierung gilt, für die der Test ausgeführt wurde. Verwenden Sie Zusammenfassende Visualisierungen, um Adobe Advertising-Metriken im selben Bericht wie die [!DNL Target] Testleistung anzuzeigen.

* Priorisieren Sie die Verwendung von On-site-Metriken (z. B. Besuche und Konversionen), um die Leistung zu messen.

* Beachten Sie, dass aggregierte Medienmetriken von Adobe Advertising (wie Impressionen, Klicks und Kosten) nicht mit [!DNL Target] -Metriken abgeglichen werden können.

#### Dimensionen

Die folgenden Dimensionen beziehen sich auf [!DNL Analytics for Target]:

* **[!UICONTROL Target Activities]**: Name des A/B-Tests

* **[!UICONTROL Target Experiences]**: Namen der in der Aktivität verwendeten Landingpage-Erlebnisse

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]**: Der Aktivitäts- und Erlebnisname in derselben Zeile

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
* [Überblick über A/B-Tests](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Beschreibt A/B-Test-Aktivitäten, die Sie mit DSP Anzeigen verwenden können.
* [Erlebnisse und Angebote](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Erläutert [!DNL Target] Tools, mit denen der On-site-Inhalt bestimmt wird, für den DSP Testbenutzer verfügbar gemacht werden.
* [Signale, Eigenschaften und Segmente](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - Definiert einige der Audience Manager-Tools, die beim DSP Durchsichtstest helfen können.
* [Überblick über Analytics für Advertising](/help/integrations/analytics/overview.md) - Einführung in Analytics für Advertising, mit dem Sie Clickthrough- und Durchsichts-Site-Interaktionen in Ihren Analytics-Instanzen verfolgen können.

>[!MORELIKETHIS]
>
>* [Konfigurieren von A/B-Tests in Adobe Target für Advertising Search, Social und Commerce Ads](ab-tests-search.md)
