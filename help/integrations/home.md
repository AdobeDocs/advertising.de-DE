---
title: Neue Funktionen
description: Erfahren Sie mehr über Aktualisierungen der Integrationen zwischen Adobe Advertising und anderen Produkten und Services in Adobe Experience Cloud.
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: e5874077-d2a8-43bb-ad4e-55547442c8a4
source-git-commit: ae93aff0056e58fd4427620d2eab76330a73039c
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# Neue Funktionen

Die folgenden Funktionen sind neu oder wurden kürzlich geändert.

| Datum | Funktion | Beschreibung | Für weitere Informationen |
| ---- | ------- | ----------- | -------------------- |
| &#x200B;26. März 2025 | [!DNL Adobe Analytics for Advertising] | (Werbetreibende mit Search, Social und Commerce; [!DNL Microsoft Advertising] Konten; und [!DNL Adobe Analytics for Advertising]) Für Konten mit der Option &quot;[!UICONTROL Auto Upload]-Tracking“ wurde das Format des AMO-ID-Parameters in den Suffixen der Landingpage für alle Kampagnentypen auf das neueste Format aktualisiert. Zuvor wurden Performance Max-Kampagnen für die meisten Konten in das neue Format migriert.<br><br>Bei Konten ohne die [!UICONTROL Auto Upload]-Tracking-Option, die noch nicht in das neue Format migriert wurden, müssen Sie jedoch jedes Landingpage-Suffix manuell aktualisieren, um das neue AMO-ID-Format aufzunehmen.<br><br>Aktuelles Format: `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}` | Siehe &quot;[Überblick über [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) und die [AMO ID-Formate](/help/integrations/analytics/ids.md#amo-id-formats). |
| &#x200B;13. November 2024 | [!DNL Analytics for Advertising] | (Advertisers mit [!DNL Analytics for Advertising] und Adobe Customer Journey Analytics) Wenn Sie reservierte Variablen verwenden, um Ihre AMO-IDs und EF-IDs zu erfassen, können Sie sich auf eine zukünftige Integration zwischen Adobe Advertising und Adobe Customer Journey Analytics vorbereiten, indem Sie Ihre reservierten Variablen für die AMO-ID und die EF-ID so bald wie möglich in [!DNL eVars] kopieren. Auf diese Weise können historische Daten für die AMO-IDs und EF-IDs erfasst werden, sobald Sie die Aufgabe abgeschlossen haben. Die historischen Daten stehen dann für die zukünftige Verwendung zur Verfügung. Ihr Adobe-Konto-Team teilt Ihnen mit, ob Sie reservierte Variablen verwenden und diese Aufgabe abschließen müssen. | Siehe &quot;[Erfassen historischer Daten für AMO-IDs und EF-IDs zur Verwendung in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md)&quot;. |
| Erschienen am 29. Oktober 2024 | [!DNL Adobe Analytics for Advertising] | (Werbetreibende mit Kampagnen mit [!DNL Adobe Analytics for Advertising] und [!DNL Microsoft Advertising] Performance Max) Daten auf Asset-Gruppenebene für Ihre Kampagnen mit dem Typ Performance Max sind jetzt in Adobe Analytics verfügbar, wenn Sie einen neuen AMO ID ([!DNL s_kwcid])-Parameter in die Tracking-URLs für Ihre Kampagnen mit dem Typ Performance Max implementieren, die keine Anzeigen und Keywords enthalten. Das Tracking für die meisten Konten mit Performance Max-Kampagnen wurde bereits in das neue Format migriert. Bei Konten mit Performance Max-Kampagnen ohne die [!UICONTROL Auto Upload]-Tracking-Option, die noch nicht in das neue Format migriert wurden, müssen Sie jedoch jedes Landingpage-Suffix manuell aktualisieren, um das neue AMO-ID-Format aufzunehmen.<br><br>Adobe Analytics-Daten für Ihre Performance Max-Kampagnen sind auch in Search, Social und Commerce verfügbar. | Siehe das neue [AMO ID-Format](/help/integrations/analytics/ids.md#amo-id-formats) und [wann und wie Sie den -Parameter zu Ihren Tracking-URLs hinzufügen](/help/integrations/analytics/ids.md#amo-id-implement). |
| &#x200B;16. Dezember 2023 | Hilfe | In einem neuen Dokument wird erläutert, wie Sie A/B-Tests in [!DNL Target] für Clickthrough-Traffic von Anzeigen in Search, Social und Commerce einrichten und wie Sie Ihre Tests in [!DNL Analytics] messen und visualisieren können. | Siehe &quot;[ von A/B-Tests in Adobe Target für Search, Social und Commerce Ads](/help/integrations/target/ab-tests-search.md)&quot;. |
| &#x200B;8. August 2023 | [!DNL Analytics for Advertising] | Einige [!DNL Analytics] Erfolgsereignismetriken, einschließlich standardmäßiger, benutzerdefinierter und reservierter Konversionsmetriken und Traffic-Metriken, sind automatisch in DSP und in Search, Social und Commerce verfügbar. Jetzt können Sie auch Ihre eigenen Erfolgsmetriken basierend auf Ihren vorhandenen [!DNL Analytics]-[!DNL eVars] und -[!DNL props] konfigurieren, indem Sie Daten auf [!DNL eVar]- und [!DNL prop] Ebene in ein benutzerdefiniertes Erfolgsereignis kanalisieren. | Siehe &quot;[ von Konversionsmetriken aus Adobe Analytics erstellen [!DNL eVars] und [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)&quot;. |
| &#x200B;13. Juli 2023 | Berichterstellung | (DSP-Benutzer mit [!DNL Analytics for Advertising]) View-Through-Konversionen für CTV-Platzierungen (Connected TV) sind jetzt in den in Adobe Analytics verfügbaren Konversionsdaten enthalten. | Siehe den Abschnitt „Beispiele für die Verwendung der Integration“ in &quot;[ von [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md#integration-examples)&quot;. |
| &#x200B;1. November 2022 | Hilfe | In einem neuen Dokument wird erläutert, wie Sie Clickthrough- und View-Through-Signalfreigabe zwischen Advertising DSP und Adobe Target implementieren, eine A/B-Testaktivität in [!DNL Target] für Ihre DSP-Anzeigen einrichten und Adobe Analytics Analysis Workspace einrichten, um die Testdaten anzuzeigen. | Siehe &quot;[ von A/B-Tests in Adobe Target für Advertising DSP Ads](/help/integrations/target/ab-tests-dsp.md)&quot;. |
| &#x200B;17. August 2022 | Hilfe | In einem neuen Kapitel werden alle Möglichkeiten erläutert, wie Adobe Advertising mit Adobe Audience Manager integriert wird. | Siehe das Kapitel „Integration mit Adobe Audience Manager&quot;, einschließlich einer Übersicht über &quot;[Adobe Advertising-Integrationen mit Adobe Audience Manager](/help/integrations/audience-manager/overview.md)&quot;. |
| &#x200B;27. April 2021 | [!DNL Analytics for Advertising] | Erfahren Sie, warum und wie Sie Ihren [!DNL Analytics for Advertising]-Anzeigen-Tags [!DNL Google Campaign Manager 360]-Makros hinzufügen, um Klickdaten an Adobe Analytics zu senden. | Siehe &quot;[append [!DNL Analytics for Advertising] macros to [!DNL Google Campaign Manager 360] ad tags](/help/integrations/analytics/macros-google-campaign-manager.md)&quot; |
| &#x200B;19. April 2021 | [!DNL Analytics for Advertising] | Erfahren Sie, warum und wie Sie Makros an Ihre [!DNL Flashtalking]-Anzeigen-Tags anhängen, um Klickdaten an Adobe Analytics zu senden. | Siehe &quot;[append [!DNL Analytics for Advertising] macros to [!DNL Flashtalking] ad tags](/help/integrations/analytics/macros-flashtalking.md)&quot; |
| &#x200B;27. Oktober 2021 | [!DNL Analytics for Advertising] | Wenn Ihr Unternehmen für die Datenerfassung von der Verwendung der veralteten Adobe Analytics `visitorAPI.js`-Bibliothek auf die [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=de)-Bibliothek (`alloy.js`) wechseln möchte, müssen Sie einige Änderungen vornehmen, um die ID-Zuordnung zu aktivieren. | Siehe &quot;[Verwenden der  [!DNL Last Event Service] JavaScript-Bibliothek mit Adobe Experience Platform [!DNL Web SDK]](/help/integrations/analytics/web-sdk.md)&quot;. |
| &#x200B;26. Mai 2021 | Hilfe | Das Kapitel &quot;[!DNL Analytics for Advertising]&quot; enthält jetzt ein Unterkapitel „Arbeiten in [!DNL Analytics Marketing Channels]&quot;. | Siehe: [Grundlagen von Marketing-Kanälen](/help/integrations/analytics/marketing-channels/mc-overview.md), [Verwenden von Adobe Advertising-IDs zum Erstellen  [!DNL Analytics Marketing Channels]  Verarbeitungsregeln](/help/integrations/analytics/marketing-channels/mc-ids.md), [Verwenden von  [!DNL Analytics Marketing Channels]  mit Adobe Advertising-Daten](/help/integrations/analytics/marketing-channels/mc-ac-data.md) und [Warum Kanaldaten zwischen Adobe Advertising und  [!DNL Analytics Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md) variieren können.“ |
| &#x200B;26. Mai 2021 | Hilfe | Es wurde ein Link zu allen Video-Tutorials zu [!DNL Analytics for Advertising] hinzugefügt. | Siehe: [Video-Tutorials zu Adobe Advertising-Integrationen](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/overview.html?lang=de). |

{style="table-layout:auto"}

<!-- At some point, just make this an overview page instead?

Adobe Advertising is integrated with the following Adobe Experience Cloud products:

* [Adobe Analytics](/help/integrations/analytics/overview.md)

* Adobe Audience Manager

* Adobe Campaign (Adobe Advertising Search only)

 -->
