---
title: Voraussetzungen und wichtige Informationen für die Implementierung von [!DNL Analytics for Advertising]
description: Voraussetzungen und wichtige Informationen für die Implementierung von [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 1559c2cb83e32d90f4b2fe959d07c4e588d9becf
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Voraussetzungen und Schlüsselinformationen für die Implementierung von [!DNL Analytics for Advertising]

*Advertiser mit Advertising DSP und[!DNL Advertising Search, Social, & Commerce]*

Lesen Sie die folgenden Informationen, bevor Sie Adobe Advertising in Adobe Analytics integrieren.

## Anforderungen für die Berichterstellung für Adobe Advertising-Daten in [!DNL Analytics]

* Eine der folgenden Optionen:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience Cloud Identity Service: `visitorAPI.js` Version 2.0 oder höher
* Jede Version von Adobe Analytics (einschließlich [!DNL Prime], [!DNL Premium] oder [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` Version 2.1 oder höher
* (Advertising DSP-Kunden) Ein [Advertising DSP JavaScript-Snippet](javascript.md), das auf Ihren Webseiten bereitgestellt wird, um Durchsichtsbesuche zu verfolgen.

>[!TIP]
>
>Verwenden Sie zur Verbesserung der Datenintegrität die neueste Version jeder Bibliothek.

## Voraussetzungen für die Freigabe von Analytics-Segmenten mit Adobe Advertising

* Experience Cloud Identity Service: `visitorAPI.js` Version 2.1 oder höher
* Adobe Analytics: `appMeasurement.js` Version 1.8 oder höher

## Anforderungen für die Berichterstellung von [!DNL Analytics] Daten in Adobe Advertising

Stellen Sie dem Adobe Advertising-Implementierungsteam Folgendes zur Verfügung:

* Die [!DNL Analytics] Report Suite-ID, die für die Berichterstellung über Paid-Media-Aktivitäten und für die Bereitstellung von Site-Aktivitäten zur Optimierung und Berichterstellung in Adobe Advertising verwendet wird
* Die Experience Cloud-Organisations-ID (Organisations-ID) des Unternehmens.

Sie finden beide IDs auf der Registerkarte [Zusammenfassung des Adobe Experience Cloud Debuggers](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Bildschirm &quot;Experience Cloud Debugger-Zusammenfassung&quot;](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Daten in Adobe Advertising {#lookback-a4adc}

Da [!DNL Analytics] -Daten zur Berichterstellung und Optimierung an Adobe Advertising gesendet werden, unterliegen die Daten den Attributionsregeln, einschließlich der Impression- und Klick-Lookback-Fenster, die für den Advertiser in Adobe Advertising konfiguriert sind.

![Lookback-Fenstereinstellungen auf Advertiser-Ebene in Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising Attributions-Klick-Lookback-Fenster: Die Anzahl der Tage nach dem ersten Klick, in denen der Klick einer Konversion zugeordnet werden kann. Standardmäßig beträgt dieser Wert 60 Tage, der Höchstwert 90 Tage.
* Adobe Advertising Attributions-Impression-Lookback-Fenster: Die Anzahl der Tage, nach denen eine Ad-Impression auftritt und in denen die Impression einer Konversion zugeordnet werden kann. Standardmäßig beträgt dieser Wert 14 Tage, die maximale Dauer beträgt 30 Tage.

  >[!NOTE]
  >
  > Das Impression-Lookback-Fenster ist spezifisch für Adobe Advertising, nicht für die Berichterstellung mit [!DNL Analytics for Advertising].

Der [!DNL Analytics for Advertising] -JavaScript verwendet diese Einstellungen, um zu bestimmen, wie weit ein Viewthrough-Eintrag oder Clickthrough-Eintrag für die Site als gültig zurückbetrachtet werden soll. Weitere Informationen dazu, wie Durchsichten und Clickthroughs ermittelt werden, finden Sie unter &quot;[Von Analytics verwendete Adobe Advertising-IDs](ids.md)&quot;.

## Adobe Advertising Data in [!DNL Analytics]

[!DNL Analytics] legt Adobe Advertising-IDs (AMO-IDs) im Analytics-Treffer fest, vorbehaltlich der Persistenzeinstellung [!DNL eVar] des Advertisers, die sowohl für Clickthroughs als auch für Durchsichten gilt. Die Persistenzeinstellung wird auf dem Adobe Advertising-Backend konfiguriert und Ihr Adobe-Account-Team kann sie ändern.

* [!DNL Analytics for Advertising] [!DNL eVar] Ablauf: Standardmäßig 60 Tage für AMO-IDs

>[!NOTE]
>
>Um Daten für einen anderen Zeitrahmen zu segmentieren, können Sie [benutzerdefinierte Segmente](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) mit verschiedenen Lookback-Fenstern in Analysis Workspace einrichten.

## Unterstützte Anzeigenumgebungen

* Suche
* Anzeige
* Video
* Online-Video
* Angeschlossener Fernseher
* Nativ

Wenden Sie sich an Ihr Adobe Account-Team, um die neuesten unterstützten Anzeigenumgebungen in den einzelnen Kanälen zu erhalten.

## Was Sie vor der Implementierung wissen sollten

* Das Adobe Advertising-Implementierungsteam richtet die Integration ein.

* Für diese Integration werden keine zusätzlichen Kosten in Rechnung gestellt, auch keine Server-Aufrufe führen zu zusätzlichen [!DNL Analytics]- oder Adobe Advertising-Gebühren.

* [!DNL Analytics for Advertising] ist anzeigenserverunabhängig: Ein Durchsichts- oder Clickthrough-Vorgang kann von jedem Anzeigen-Server aus erfolgen, und die richtigen IDs werden bei der Site-Eingabe generiert.

* Bei der Integration werden nur [!DNL Analytics] standardmäßige und benutzerdefinierte Ereignisse an Adobe Advertising übergeben, um die Angebotsoptimierung nachfolgender gebührenpflichtiger Medien und Werbemaßnahmen zu ermöglichen. Zur Angebotsoptimierung werden keine [!DNL Analytics] -Segmente, berechneten Metriken und [!DNL eVars] an Adobe Advertising übergeben.

* Adobe Advertising erstellt persistente IDs innerhalb von [!DNL Analytics] basierend auf der letzten Anzeige, die angeklickt oder angezeigt wurde, bevor der Benutzer die Site aufruft, basierend auf den in Adobe Advertising konfigurierten [Klick- und Durchsichts-Lookback-Fenstern](#lookback-a4adc). Wenn ein Site-Besucher innerhalb seines Profils über beide Arten von Site-Einstiegsinteraktionen verfügt und sich der Klick innerhalb des Lookback-Zeitraums befindet, setzt die Clickthrough-ID des Besuchers die Durchsichts-ID für die Site-Berichterstellung außer Kraft.

* Das Konversions-Tracking von [!DNL Analytics for Advertising] in Adobe Analytics verwendet ein konfigurierbares Tracking-Lookback-Fenster (standardmäßig 60 Tage). Adobe Advertising-Berichte spiegeln Site-Konversionen und Interaktionen am Ende dieses Tracking-Lookback-Fensters wider.

* Alle Anzeigentypen werden unterstützt. <!--Clarify what this might include. It used to include CTV, but not anymore: However, not all ad environments are supported. -->

* [!DNL Analytics] -Konversionen werden derzeit verfolgt und nur einem Besucher auf demselben Gerät zugeordnet.

* [!DNL Analytics for Advertising] unterstützt keine In-App-Durchsichtskonvertierungen.

* Das Durchsichtstracking wird für Advertiser, die eine serverseitige Weiterleitungsimplementierung von [!DNL Analytics] verwenden, nicht unterstützt.

### Zusätzliche ID

Sobald der Experience Cloud Identity-Dienst für eine Site implementiert ist, enthalten Treffer, die Daten von [!DNL Analytics] oder Adobe Advertising enthalten, eine zusätzliche ID.

Beispiel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Für eine genaue Datenintegration müssen alle Adobe Advertising-Aufrufe, die von einer [!DNL Analytics for Advertising] -Aktivität zur Bereitstellung von Inhalten oder zur Aufzeichnung der Zielmetrik verwendet werden, einen entsprechenden [!DNL Analytics] -Treffer aufweisen, der dieselbe zusätzliche ID aufweist.

Stellen Sie bei der Fehlerbehebung in [!DNL Analytics] sicher, dass die zusätzliche ID für [!DNL Analytics] -Treffer vorhanden ist. Im [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) können Sie diese ID auf der Registerkarte &quot;Adobe Advertising&quot;als den Parameter `sdid` sehen.

>[!NOTE]
>
> Diese Implementierung funktioniert ähnlich wie die [!DNL Analytics for Target] -Integration.

>[!MORELIKETHIS]
>
>* [Überblick über  [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript-Code für Analytics für Advertising](/help/integrations/analytics/javascript.md)
