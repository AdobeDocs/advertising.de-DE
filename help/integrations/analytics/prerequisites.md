---
title: Voraussetzungen und wichtige Informationen für die Implementierung [!DNL Analytics for Advertising]
description: Voraussetzungen und wichtige Informationen für die Implementierung [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 1559c2cb83e32d90f4b2fe959d07c4e588d9becf
workflow-type: tm+mt
source-wordcount: '795'
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

* Die [!DNL Analytics] Report Suite-ID, die für das Reporting über Paid-Media-Aktivitäten und für den Feed der Site-Aktivität für die Optimierung und Berichterstellung im Adobe Advertising verwendet wird
* Die Experience Cloud-Organisations-ID (Organisations-ID) des Unternehmens.

Beide IDs finden Sie auf der Registerkarte [Zusammenfassung“ des Adobe Experience Cloud Debuggers](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=de).

![Bildschirm mit der Experience Cloud Debugger-Zusammenfassung](/help/integrations/assets/a4adc-debugger-summary.png)

## Daten in Adobe Advertising [!DNL Analytics] {#lookback-a4adc}

Da [!DNL Analytics] Daten zum Reporting und zur Optimierung an Adobe Advertising gesendet werden, unterliegen die Daten den Attributionsregeln, einschließlich der Impression- und Klick-Lookback-Fenster, die für den Advertiser in Adobe Advertising konfiguriert sind.

![Einstellungen des Lookback-Fensters auf Advertiser-Ebene in Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising-Attribution Klick-Lookback-Fenster : Die Anzahl der Tage nach dem ersten Klick, in denen der Klick einer Konversion zugeordnet werden kann. Standardmäßig beträgt dieser Wert 60 Tage, der Höchstwert 90 Tage
* Adobe Advertising Attribution Impression Lookback-Fenster: Die Anzahl der Tage nach dem Auftreten einer Anzeigenimpression, in denen die Impression einer Konversion zugeordnet werden kann. Standardmäßig ist dieser Wert 14 Tage, der Höchstwert 30 Tage

  >[!NOTE]
  >
  > Das Impression-Lookback-Fenster ist spezifisch für das Adobe Advertising, nicht für das [!DNL Analytics for Advertising], Reporting.

Die [!DNL Analytics for Advertising] JavaScript verwendet diese Einstellungen, um zu bestimmen, wie weit ein Viewthrough-Eintrag oder ein Clickthrough-Eintrag zur Website zurückreicht, um ihn als gültig zu betrachten. Weitere Informationen zum Bestimmen von Viewthroughs und Clickthroughs finden Sie unter [Adobe Advertising-IDs, die von Analytics verwendet werden](ids.md).

## Adobe Advertising-Daten in [!DNL Analytics]

[!DNL Analytics] legt Adobe Advertising-IDs (AMO-IDs) im Analytics-Treffer fest, abhängig von der [!DNL eVar] Persistenzeinstellung des Advertisers, die sowohl für Clickthroughs als auch für View-Throughs gilt. Die Persistenzeinstellung wird im Adobe Advertising-Backend konfiguriert und kann von Ihrem Adobe-Account-Team geändert werden.

* Ablauf der [!DNL Analytics for Advertising]-[!DNL eVar]: Standardmäßig 60 Tage für AMO-IDs

>[!NOTE]
>
>Um Daten für einen anderen Zeitrahmen zu segmentieren, können Sie [benutzerdefinierte Segmente einrichten](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=de) mit verschiedenen Lookback-Fenstern in Analysis Workspace.

## Unterstützte Anzeigenumgebungen

* Suche
* Anzeige
* Video
* Online-Video
* Connected TV
* Nativ

Wenden Sie sich an Ihr Adobe-Account-Team , um die neuesten unterstützten Anzeigenumgebungen für jeden Kanal zu erhalten.

## Wichtige Informationen vor der Implementierung

* Das Adobe Advertising-Implementierungsteam richtet die Integration ein.

* Für diese Integration werden keine zusätzlichen Kosten in Rechnung gestellt, und auch die Server-Aufrufe verursachen keine zusätzlichen [!DNL Analytics]- oder Adobe Advertising-Gebühren.

* [!DNL Analytics for Advertising] ist Server-unabhängig von Anzeigen: Ein Viewthrough oder ein Clickthrough kann von jedem Anzeigen-Server aus auftreten, und die richtigen IDs werden bei der Site-Eingabe generiert.

* Die Integration übergibt nur [!DNL Analytics] Standard- und benutzerspezifische Ereignisse an Adobe Advertising zur Angebotsoptimierung für nachfolgende Paid-Media- und Werbemaßnahmen. Er übergibt keine [!DNL Analytics] Segmente, berechneten Metriken und [!DNL eVars] zur Angebotsoptimierung an Adobe Advertising.

* Adobe Advertising erstellt persistente IDs innerhalb von [!DNL Analytics] basierend auf der zuletzt angeklickten oder angezeigten Anzeige, bevor der Benutzer die Website betritt, basierend auf den [Click- und View-Through-Lookback-Fenstern](#lookback-a4adc) die in Adobe Advertising konfiguriert sind. Wenn ein Site-Besucher in seinem Profil beide Arten von Site-Einstiegsinteraktionen hat und sich der Klick innerhalb der Lookback-Periode befindet, überschreibt die Clickthrough-ID des Besuchers die View-Through-ID für das Site-Reporting.

* [!DNL Analytics for Advertising] Konversionsverfolgung in Adobe Analytics verwendet ein konfigurierbares Tracking-Lookback-Fenster (standardmäßig 60 Tage). Adobe Advertising-Berichte spiegeln Website-Konversionen und die Interaktion am Ende dieses Tracking-Lookback-Fensters wider.

* Alle Anzeigentypen werden unterstützt. <!--Clarify what this might include. It used to include CTV, but not anymore: However, not all ad environments are supported. -->

* [!DNL Analytics] Konversionen werden derzeit verfolgt und nur einem Besucher auf demselben Gerät zugeordnet.

* [!DNL Analytics for Advertising] unterstützt keine In-App-View-Through-Konversionen.

* Das View-Through-Tracking wird für Werbetreibende, die eine serverseitige Weiterleitungsimplementierung von [!DNL Analytics] verwenden, nicht unterstützt.

### Ergänzende ID

Sobald der Experience Cloud Identity Service für eine Site implementiert ist, enthalten Treffer, die Daten von [!DNL Analytics] oder Adobe Advertising enthalten, eine zusätzliche ID.

Beispiel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Für eine präzise Datenintegration müssen alle Adobe Advertising-Aufrufe, die von einer [!DNL Analytics for Advertising]-Aktivität zum Bereitstellen von Inhalten oder Aufzeichnen der Zielmetrik verwendet werden, einen entsprechenden [!DNL Analytics]-Treffer mit derselben zusätzlichen ID aufweisen.

Stellen Sie bei der Fehlerbehebung in [!DNL Analytics] sicher, dass die zusätzliche ID für [!DNL Analytics] Treffer vorhanden ist. Im [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=de) wird diese ID auf der Registerkarte &quot;Adobe Advertising&quot; als `sdid` angezeigt.

>[!NOTE]
>
> Diese Implementierung funktioniert ähnlich wie die [!DNL Analytics for Target].

>[!MORELIKETHIS]
>
>* [Überblick über [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript-Code für Analytics für Advertising](/help/integrations/analytics/javascript.md)
