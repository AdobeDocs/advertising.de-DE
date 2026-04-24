---
title: Neue Funktionen
description: Learn about updates to integrations between Adobe Advertising and other products and services in Adobe CX Enterprise (formerly Adobe Experience Cloud).
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: e5874077-d2a8-43bb-ad4e-55547442c8a4
TQID: https://experienceleague.adobe.com/6-dzP-cjgKB5-HBvIpy8iU3B8FEbWAfP8r5UEad23Ok
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
  - id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2:
  - id: d1e2786d-1070-4f97-93d7-f5b95de25b2b
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: 870
ht-degree: 0%

---

# Neue Funktionen

The following features are new or recently changed.

| Date | Feature | Beschreibung | For More Information |
| ---- | ------- | ----------- | -------------------- |
| 8 September 2025 | Integration with Customer Journey Analytics | (Beta feature) Advertisers with Customer Journey Analytics but not [!DNL Analytics for Advertising] can now natively exchange data between Adobe Advertising and Customer Journey Analytics using the [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html). | See &quot;[Overview of the integration between Adobe Advertising with Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md).&quot; |
| &#x200B;26. März 2025 | [!DNL Adobe Analytics for Advertising] | (Advertisers with Search, Social, &amp; Commerce; [!DNL Microsoft Advertising] accounts; and [!DNL Adobe Analytics for Advertising]) For accounts with the [!UICONTROL Auto Upload] tracking option, the format of the AMO ID parameter in the landing page suffixes for all campaign types was updated to the latest format. Zuvor wurden Performance Max-Kampagnen für die meisten Konten in das neue Format migriert.<br><br>Bei Konten ohne die [!UICONTROL Auto Upload]-Tracking-Option, die noch nicht in das neue Format migriert wurden, müssen Sie jedoch jedes Landingpage-Suffix manuell aktualisieren, um das neue AMO-ID-Format aufzunehmen.<br><br>Aktuelles Format: `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}` | Siehe &quot;[Überblick über [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) und die [AMO ID-Formate](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items). |
| 13 November 2024 | [!DNL Analytics for Advertising] | (Advertisers with [!DNL Analytics for Advertising] and Adobe Customer Journey Analytics) If you use reserved variables to capture your AMO IDs and EF IDs, then you can prepare for a future integration between Adobe Advertising and Adobe Customer Journey Analytics by copying your reserved variables for the AMO ID and the EF ID into standard [!DNL eVars] as soon as possible. This will allow the collection of historical data for the AMO IDs and EF IDs as soon as you complete the task, and the historical data will be available for future use. Ihr Adobe-Konto-Team teilt Ihnen mit, ob Sie reservierte Variablen verwenden und diese Aufgabe abschließen müssen. | Siehe &quot;[Erfassen historischer Daten für AMO-IDs und EF-IDs zur Verwendung in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)&quot;. |
| Erschienen am 29. Oktober 2024 | [!DNL Adobe Analytics for Advertising] | (Werbetreibende mit Kampagnen mit [!DNL Adobe Analytics for Advertising] und [!DNL Microsoft Advertising] Performance Max) Daten auf Asset-Gruppenebene für Ihre Kampagnen mit dem Typ Performance Max sind jetzt in Adobe Analytics verfügbar, wenn Sie einen neuen AMO ID ([!DNL s_kwcid])-Parameter in die Tracking-URLs für Ihre Kampagnen mit dem Typ Performance Max implementieren, die keine Anzeigen und Keywords enthalten. Das Tracking für die meisten Konten mit Performance Max-Kampagnen wurde bereits in das neue Format migriert. Bei Konten mit Performance Max-Kampagnen ohne die [!UICONTROL Auto Upload]-Tracking-Option, die noch nicht in das neue Format migriert wurden, müssen Sie jedoch jedes Landingpage-Suffix manuell aktualisieren, um das neue AMO-ID-Format aufzunehmen.<br><br>Adobe Analytics-Daten für Ihre Performance Max-Kampagnen sind auch in Search, Social und Commerce verfügbar. | Siehe das neue [AMO ID-Format](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items) und [wann und wie Sie den -Parameter zu Ihren Tracking-URLs hinzufügen](/help/integrations/analytics/ids.md). |
| &#x200B;16. Dezember 2023 | Hilfe | In einem neuen Dokument wird erläutert, wie Sie A/B-Tests in [!DNL Target] für Clickthrough-Traffic von Anzeigen in Search, Social und Commerce einrichten und wie Sie Ihre Tests in [!DNL Analytics] messen und visualisieren können. | Siehe &quot;[&#x200B; von A/B-Tests in Adobe Target für Search-, Social- und Commerce-Anzeigen](/help/integrations/target/ab-tests-search.md)&quot;. |
| &#x200B;8. August 2023 | [!DNL Analytics for Advertising] | Einige [!DNL Analytics] Erfolgsereignismetriken, einschließlich standardmäßiger, benutzerdefinierter und reservierter Konversionsmetriken und Traffic-Metriken, sind automatisch in DSP und in Search, Social und Commerce verfügbar. Jetzt können Sie auch Ihre eigenen Erfolgsmetriken basierend auf Ihren vorhandenen [!DNL Analytics]-[!DNL eVars] und -[!DNL props] konfigurieren, indem Sie Daten auf [!DNL eVar]- und [!DNL prop] Ebene in ein benutzerdefiniertes Erfolgsereignis kanalisieren. | Siehe &quot;[&#x200B; von Konversionsmetriken aus Adobe Analytics erstellen [!DNL eVars] und [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)&quot;. |
| &#x200B;13. Juli 2023 | Berichterstellung | (DSP-Benutzer mit [!DNL Analytics for Advertising]) View-Through-Konversionen für CTV-Platzierungen (Connected TV) sind jetzt in den in Adobe Analytics verfügbaren Konversionsdaten enthalten. | Siehe den Abschnitt „Beispiele für die Verwendung der Integration“ in &quot;[&#x200B; von [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md#integration-examples)&quot;. |
| &#x200B;1. November 2022 | Hilfe | In einem neuen Dokument wird erläutert, wie Sie Clickthrough- und View-Through-Signalfreigabe zwischen Advertising DSP und Adobe Target implementieren, eine A/B-Testaktivität in [!DNL Target] für Ihre DSP-Anzeigen einrichten und Adobe Analytics Analysis Workspace einrichten, um die Testdaten anzuzeigen. | Siehe &quot;[&#x200B; von A/B-Tests in Adobe Target für Advertising DSP Ads](/help/integrations/target/ab-tests-dsp.md)&quot;. |
| &#x200B;17. August 2022 | Hilfe | A new chapter explains all ways in which Adobe Advertising is integrated with Adobe Audience Manager. | See the chapter on &quot;Integration with Adobe Audience Manager,&quot; including an overview of &quot;[Adobe Advertising Integrations with Adobe Audience Manager](/help/integrations/audience-manager/overview.md).&quot; |
| 27 April 2021 | [!DNL Analytics for Advertising] | Learn why and how to add [!DNL Analytics for Advertising] macros to your [!DNL Google Campaign Manager 360] ad tags to send click data to Adobe Analytics. | See &quot;[Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md).&quot; |
| 19 April 2021 | [!DNL Analytics for Advertising] | Learn why and how to append macros to your [!DNL Flashtalking] ad tags to send click data to Adobe Analytics. | See &quot;[Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](/help/integrations/analytics/macros-flashtalking.md).&quot; |
| 27 October 2021 | [!DNL Analytics for Advertising] | If your organization wants to switch from using the legacy Adobe Analytics `visitorAPI.js` library to the [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) library (`alloy.js`) for data collection, you must make some changes to enable ID stitching. | See &quot;[Using the [!DNL Last Event Service] JavaScript Library with Adobe Experience Platform [!DNL Web SDK]](/help/integrations/analytics/web-sdk.md).&quot; |
| 26 May 2021 | Hilfe | The chapter &quot;[!DNL Analytics for Advertising]&quot; now includes a subchapter on &quot;Working in [!DNL Analytics Marketing Channels].&quot; | See: &quot;[Fundamentals of [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-overview.md)," "[Using Adobe Advertising IDs to create [!DNL Marketing Channels] processing rules](/help/integrations/analytics/marketing-channels/mc-ids.md),&quot; &quot;[Using [!DNL Analytics Marketing Channels] with Adobe Advertising data](/help/integrations/analytics/marketing-channels/mc-ac-data.md),&quot; and &quot;[Why channel data can vary between Adobe Advertising and [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md).&quot; |
| 26 May 2021 | Hilfe | A link to all video tutorials about [!DNL Analytics for Advertising] was added. | See: &quot;[Video tutorials about Adobe Advertising integrations](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/overview.html).&quot; |

{style="table-layout:auto"}

<!--
 At some point, just make this an overview page instead?

Adobe Advertising is integrated with the following Adobe CX Enterprise products:

* [Adobe Analytics](/help/integrations/analytics/overview.md)

* Adobe Audience Manager

* Adobe Campaign (Adobe Advertising Search only)

 -->
