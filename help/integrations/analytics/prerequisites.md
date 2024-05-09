---
title: Voraussetzungen und Schlüsselinformationen für die Implementierung [!DNL Analytics for Advertising]
description: Voraussetzungen und Schlüsselinformationen für die Implementierung [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# Voraussetzungen und Schlüsselinformationen für die Implementierung [!DNL Analytics for Advertising]

*Advertiser mit Advertising DSP und[!DNL Advertising Search, Social, & Commerce]*

Lesen Sie die folgenden Informationen, bevor Sie Adobe Advertising in Adobe Analytics integrieren.

## Anforderungen für die Berichterstellung für Adobe Advertising-Daten in [!DNL Analytics]

* Eine der folgenden Optionen:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience Cloud Identity Service: `visitorAPI.js` Version 2.0 oder höher
* Jede Version von Adobe Analytics (einschließlich [!DNL Prime], [!DNL Premium]oder [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` Version 2.1 oder höher
* (Kunden von Advertising DSP) Eine [Advertising DSP JavaScript-Snippet](javascript.md) bereitgestellt, um Durchsichtsbesuche zu verfolgen.

>[!TIP]
>
>Verwenden Sie zur Verbesserung der Datenintegrität die neueste Version jeder Bibliothek.

## Voraussetzungen für die Freigabe von Analytics-Segmenten mit Adobe Advertising

* Experience Cloud Identity Service: `visitorAPI.js` Version 2.1 oder höher
* Adobe Analytics: `appMeasurement.js` Version 1.8 oder höher

## Berichterstattungsanforderungen [!DNL Analytics] Daten in Adobe Advertising

Stellen Sie dem Adobe Advertising-Implementierungsteam Folgendes zur Verfügung:

* Die [!DNL Analytics] Report Suite-ID, die für die Berichterstellung über Paid-Media-Aktivitäten und für die Bereitstellung von Site-Aktivitäten zur Optimierung und Berichterstellung in Adobe Advertising verwendet wird
* Die Experience Cloud-Organisations-ID (Organisations-ID) des Unternehmens.

Sie finden beide IDs auf der [Registerkarte &quot;Zusammenfassung&quot;des Adobe Experience Cloud Debuggers](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Bildschirm &quot;Experience Cloud Debugger Summary&quot;](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Daten in Adobe Advertising {#lookback-a4adc}

weil [!DNL Analytics] -Daten zur Berichterstellung und Optimierung an Adobe Advertising gesendet werden, unterliegen die Daten den Attributionsregeln, einschließlich der Impression- und Klick-Lookback-Fenster, die für den Advertiser in Adobe Advertising konfiguriert sind.

![Lookback-Fenstereinstellungen auf Advertiser-Ebene in Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising Attributions-Klick-Lookback-Fenster: Die Anzahl der Tage nach dem ersten Klick, in denen der Klick einer Konversion zugeordnet werden kann. Standardmäßig beträgt dieser Wert 60 Tage, der Höchstwert 90 Tage.
* Adobe Advertising Attributions-Impression-Lookback-Fenster: Die Anzahl der Tage, nach denen eine Ad-Impression auftritt und in denen die Impression einer Konversion zugeordnet werden kann. Standardmäßig beträgt dieser Wert 14 Tage, die maximale Dauer beträgt 30 Tage.

  >[!NOTE]
  >
  > Das Impression-Lookback-Fenster ist spezifisch für Adobe Advertising, nicht [!DNL Analytics for Advertising], Reporting.

Die [!DNL Analytics for Advertising] JavaScript verwendet diese Einstellungen, um zu bestimmen, wie weit ein Durchsichtseintrag oder Clickthrough-Eintrag für die Site als gültig zurückbetrachtet werden soll. Weitere Informationen zur Bestimmung von Durchsichten und Clickthroughs finden Sie unter[Von Analytics verwendete Adobe Advertising-IDs](ids.md).&quot;

## Adobe Advertising-Daten in [!DNL Analytics]

[!DNL Analytics] legt Adobe Advertising-IDs (AMO-IDs) innerhalb des Analytics-Treffers fest, abhängig von der [!DNL eVar] Persistenzeinstellung, die sowohl für Clickthroughs als auch für Durchsichten gilt. Die Persistenzeinstellung wird auf dem Adobe Advertising-Backend konfiguriert und Ihr Adobe-Account-Team kann sie ändern.

* [!DNL Analytics for Advertising] [!DNL eVar] Gültigkeit: Standardmäßig 60 Tage für AMO-IDs

>[!NOTE]
>
>Um Daten für einen anderen Zeitrahmen zu segmentieren, können Sie [Einrichten benutzerdefinierter Segmente](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) mit verschiedenen Lookback-Fenstern in Analysis Workspace.

## Unterstützte Anzeigenumgebungen

* Suche
* Anzeige
* Video
* Online-Video
* Nativ

Wenden Sie sich an Ihr Adobe Account-Team, um die neuesten unterstützten Anzeigenumgebungen in den einzelnen Kanälen zu erhalten.

## Was Sie vor der Implementierung wissen sollten

* Das Adobe Advertising-Implementierungsteam richtet die Integration ein.

* Für diese Integration werden keine zusätzlichen Kosten in Rechnung gestellt, auch keine Server-Aufrufe führen zu zusätzlichen [!DNL Analytics] oder Adobe Advertising-Gebühren.

* [!DNL Analytics for Advertising] ist serverunabhängig: Ein Durchsichts- oder Clickthrough-Vorgang kann von jedem Anzeigen-Server aus erfolgen, und die richtigen IDs werden bei der Site-Eingabe generiert.

* Die Integration übergibt nur [!DNL Analytics] Standardereignisse und benutzerspezifische Ereignisse an die Adobe Advertising zur Angebotsoptimierung nachfolgender Paid-Media- und Werbemaßnahmen. Es ist nicht vorbei [!DNL Analytics] Segmente, berechnete Metriken und [!DNL eVars] auf Adobe Advertising zur Angebotsoptimierung.

* Adobe Advertising erstellt persistente IDs in [!DNL Analytics] basierend auf der letzten Anzeige, auf die geklickt oder angezeigt wurde, bevor der Benutzer die Site aufruft, basierend auf der [Klick- und Viewthrough-Lookback-Fenster](#lookback-a4adc) konfiguriert in Adobe Advertising. Wenn ein Site-Besucher innerhalb seines Profils über beide Arten von Site-Einstiegsinteraktionen verfügt und sich der Klick innerhalb des Lookback-Zeitraums befindet, setzt die Clickthrough-ID des Besuchers die Durchsichts-ID für die Site-Berichterstellung außer Kraft.

* [!DNL Analytics for Advertising] Das Konversions-Tracking in Adobe Analytics verwendet ein konfigurierbares Tracking-Lookback-Fenster (standardmäßig 60 Tage). Adobe Advertising-Berichte spiegeln Site-Konversionen und Interaktionen am Ende dieses Tracking-Lookback-Fensters wider.

* Alle Anzeigentypen werden unterstützt. Es werden jedoch nicht alle Anzeigenumgebungen unterstützt.

  Beispielsweise werden Anzeigen mit angeschlossenem TV (CTV) nicht verfolgt, da in CTV keine Klicks auftreten und auf demselben Gerät keine Konversionen stattfinden können. Wenn die Anzeige jedoch in einer Desktop-Umgebung angezeigt wird, können einige Viewthrough-Site-Einstiegsdaten verfolgt werden.

* [!DNL Analytics] Konversionen werden derzeit verfolgt und nur einem Besucher auf demselben Gerät zugeordnet.

* [!DNL Analytics for Advertising] unterstützt keine In-App-Durchsichtskonvertierungen.

* Advertiser, die eine serverseitige Weiterleitungsimplementierung von [!DNL Analytics].

### Zusätzliche ID

Sobald der Experience Cloud Identity-Dienst für eine Site implementiert wurde, werden Treffer mit Daten aus [!DNL Analytics] oder Adobe Advertising eine zusätzliche ID enthält.

Beispiel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Für eine genaue Datenintegration werden alle Adobe Advertising-Aufrufe verwendet, die von einer [!DNL Analytics for Advertising] -Aktivität, um Inhalte bereitzustellen oder die Zielmetrik aufzuzeichnen, muss über eine entsprechende [!DNL Analytics] Treffer, der dieselbe zusätzliche ID aufweist.

Fehlerbehebung in [!DNL Analytics]müssen Sie sicherstellen, dass die zusätzliche ID für [!DNL Analytics] Treffer. Im [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html), können Sie diese ID auf der Registerkarte Adobe Advertising als `sdid` -Parameter.

>[!NOTE]
>
> Diese Implementierung funktioniert ähnlich wie die [!DNL Analytics for Target] Integration.

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript-Code für Analytics für Werbung](/help/integrations/analytics/javascript.md)
