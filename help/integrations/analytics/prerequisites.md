---
title: Voraussetzungen und wichtige Informationen für die Implementierung [!DNL Analytics for Advertising]
description: Voraussetzungen und wichtige Informationen für die Implementierung [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
TQID: https://experienceleague.adobe.com/ZUROuxkhySqUbUOInKkdhgvmqJth3P-9-fVDHojrn34
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 834
ht-degree: 0%

---

# Voraussetzungen und wichtige Informationen für die Implementierung von [!DNL Analytics for Advertising]

*Werbetreibende mit Advertising DSP und[!DNL Advertising Search, Social, & Commerce]*

Lesen Sie die folgenden Informationen, bevor Sie Adobe Advertising mit Adobe Analytics integrieren.

## Anforderungen für das Reporting von Adobe Advertising-Daten in [!DNL Analytics]

* einer der folgenden Schritte:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience Cloud Identity Service: `visitorAPI.js` Version 2.0 oder höher
* Jede Version von Adobe Analytics (einschließlich [!DNL Prime], [!DNL Premium] oder [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` Version 2.1 oder höher
* (Advertising DSP-Kunden) Ein [Advertising DSP JavaScript-Snippet](javascript.md) das auf Ihren Web-Seiten bereitgestellt wird, um Durchsichtsbesuche zu verfolgen.

>[!TIP]
>
>Verwenden Sie zum Verbessern der Datengenauigkeit die neueste Version jeder Bibliothek.

## Voraussetzungen für die Freigabe von Analytics-Segmenten mit Adobe Advertising

* Experience Cloud Identity Service: `visitorAPI.js` Version 2.1 oder höher
* Adobe Analytics: `appMeasurement.js` Version 1.8 oder höher

## Anforderungen für das Reporting [!DNL Analytics] Daten in Adobe Advertising

Stellen Sie dem Adobe Advertising-Implementierungsteam Folgendes bereit:

* Die [!DNL Analytics] Report Suite-ID, die für das Reporting über Paid-Media-Aktivitäten und für den Feed der Site-Aktivität für die Optimierung und Berichterstellung in Adobe Advertising verwendet werden soll
* Die CX Enterprise-Organisations-ID (Organisations-ID) des Unternehmens.

Beide IDs finden Sie auf der Registerkarte [Zusammenfassung“ der Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Zusammenfassungsbildschirm des Experience Platform-Debuggers](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Data in Adobe Advertising {#lookback-a4adc}

Because [!DNL Analytics] data is sent to Adobe Advertising for reporting and optimization, the data is subject to the attribution rules, including the impression and click lookback windows, that are configured for the advertiser in Adobe Advertising.

![advertiser-level lookback window settings in Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising attribution click lookback window: The number of days after the first click occurs in which the click can be attributed to a conversion. By default, this value is 60 days; the maximum is 90 days
* Adobe Advertising attribution impression lookback window: The number of days after an ad impression occurs in which the impression can be attributed to a conversion. By default, this value is 14 days; the maximum is 30 days

  >[!NOTE]
  >
  > The impression lookback window is specific to Adobe Advertising, not [!DNL Analytics for Advertising], reporting.

The [!DNL Analytics for Advertising] JavaScript uses these settings to determine how far back to consider a view-through entry or click-through entry to the site as valid. For more information about how view-throughs and click-throughs are determined, see &quot;[Adobe Advertising IDs used by Analytics](ids.md).&quot;

## Adobe Advertising data in [!DNL Analytics]

[!DNL Analytics] sets Adobe Advertising IDs (AMO IDs) within the Analytics hit, subject to the advertiser&#39;s [!DNL eVar] persistence setting, which applies to both click-throughs and view-throughs. The persistence setting is configured on the Adobe Advertising back end, and your Adobe Account Team can change it.

* [!DNL Analytics for Advertising] [!DNL eVar] expiration: 60 days by default for AMO IDs

>[!NOTE]
>
>To segment data for a different timeframe, you can [set up custom segments](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) with different lookback windows within Analysis Workspace.

## Supported ad environments

* Search
* Display
* Video
* Online Video
* Connected TV
* Native

Contact your Adobe Account Team for the latest supported ad environments in each channel.

## Things to know before you implement

* The Adobe Advertising implementation team sets up the integration.

* No additional costs are billed for this integration, nor do server calls result in additional [!DNL Analytics] or Adobe Advertising fees.

* [!DNL Analytics for Advertising] ist Server-unabhängig von Anzeigen: Ein Viewthrough oder ein Clickthrough kann von jedem Anzeigen-Server aus auftreten, und die richtigen IDs werden bei der Site-Eingabe generiert.

* Die Integration übergibt nur [!DNL Analytics] Standard- und benutzerspezifische Ereignisse an Adobe Advertising zur Angebotsoptimierung für nachfolgende Paid-Media- und Werbemaßnahmen. Er übergibt keine [!DNL Analytics] Segmente, berechneten Metriken und [!DNL eVars] zur Angebotsoptimierung an Adobe Advertising.

* Adobe Advertising erstellt persistente IDs innerhalb von [!DNL Analytics] basierend auf der zuletzt angeklickten oder angezeigten Anzeige, bevor der Benutzer die Website betritt, basierend auf den in Adobe Advertising konfigurierten [Click and View-Through](#lookback-a4adc)Lookback-Fenstern. Wenn ein Site-Besucher in seinem Profil beide Arten von Site-Einstiegsinteraktionen hat und sich der Klick innerhalb der Lookback-Periode befindet, überschreibt die Clickthrough-ID des Besuchers die View-Through-ID für das Site-Reporting.

* [!DNL Analytics for Advertising] Konversionsverfolgung in Adobe Analytics verwendet ein konfigurierbares Tracking-Lookback-Fenster (standardmäßig 60 Tage). Adobe Advertising-Berichte spiegeln Website-Konversionen und die Interaktion am Ende dieses Tracking-Lookback-Fensters wider.

* Alle Anzeigentypen werden unterstützt. <!--Clarify what this might include. It used to include CTV, but not anymore: However, not all ad environments are supported. -->

* [!DNL Analytics] Konversionen werden derzeit verfolgt und nur einem Besucher auf demselben Gerät zugeordnet.

* [!DNL Analytics for Advertising] unterstützt keine In-App-View-Through-Konversionen.

* Das View-Through-Tracking wird für Werbetreibende, die eine serverseitige Weiterleitungsimplementierung von [!DNL Analytics] verwenden, nicht unterstützt.

### Ergänzende ID

Sobald der Experience Cloud Identity Service für eine Site implementiert ist, enthalten Treffer, die Daten aus [!DNL Analytics] oder Adobe Advertising enthalten, eine zusätzliche ID.

Beispiel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Für eine präzise Datenintegration müssen alle Adobe Advertising-Aufrufe, die von einer [!DNL Analytics for Advertising]-Aktivität zum Bereitstellen von Inhalten oder Aufzeichnen der Zielmetrik verwendet werden, über einen entsprechenden [!DNL Analytics]-Treffer verfügen, der dieselbe zusätzliche ID aufweist.

Stellen Sie bei der Fehlerbehebung in [!DNL Analytics] sicher, dass die zusätzliche ID für [!DNL Analytics] Treffer vorhanden ist. In der [Adobe Experience Platform Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) wird diese ID auf der Registerkarte &quot;Adobe Advertising&quot; als `sdid` angezeigt.

>[!NOTE]
>
> Diese Implementierung funktioniert ähnlich wie die [!DNL Analytics for Target].

>[!MORELIKETHIS]
>
>* [Überblick über [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript-Code für Analytics für Advertising](/help/integrations/analytics/javascript.md)
