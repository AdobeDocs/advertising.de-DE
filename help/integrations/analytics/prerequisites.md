---
title: Voraussetzungen und wichtige Informationen für die Implementierung [!DNL Analytics for Advertising]
description: Voraussetzungen und wichtige Informationen für die Implementierung [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 8481227a8ccb1f1e6e715e34e14732967110c168
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# Voraussetzungen und wichtige Informationen für die Implementierung [!DNL Analytics for Advertising]

*Werbetreibende mit Advertising DSP und[!DNL Advertising Search, Social, & Commerce]*

Lesen Sie die folgenden Informationen, bevor Sie Adobe Advertising mit Adobe Analytics integrieren.

## Anforderungen für das Reporting von Adobe Advertising-Daten in [!DNL Analytics]

* einer der folgenden Schritte:
   * Adobe Experience Platform-Web-SDK: `alloy.js`
   * Experience Cloud Identity Dienst: `visitorAPI.js` Version 2.0 oder höher
* Jede Version von Adobe Analytics (einschließlich [!DNL Prime], [!DNL Premium], oder [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` Version 2.1 oder höher
* (Werbung DSP Kunden) Ein [Werbe-DSP JavaScript-Snippet](javascript.md) , das auf Ihren Webseiten zur Nachverfolgung von Ansicht-Through-Besuchen eingesetzt wird.

>[!TIP]
>
>Verwenden Sie zur Verbesserung der Daten Treue die neueste Version jedes Bibliothek.

## Voraussetzungen für die Freigabe von Analytics-Segmenten in Adobe Advertising

* Experience Cloud Identity Service: `visitorAPI.js` Version 2.1 oder höher
* Adobe Analytics: `appMeasurement.js` Version 1.8 oder höher

## Anforderungen an die Berichterstellung [!DNL Analytics] Daten in Adobe Advertising

Geben Sie dem Adobe Advertising-Implementierungs-Team Folgendes:

* Die [!DNL Analytics] Report Suite-ID, die für das Reporting über bezahlte Medienaktivitäten und für den Feed der Website-Aktivität für die Optimierung und Berichterstellung in Adobe Advertising verwendet wird
* Die Experience Cloud-Organisations-ID (Organisations-ID) des Unternehmens.

Beide IDs finden Sie auf der [Registerkarte „Zusammenfassung“ von Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Zusammenfassungsbildschirm von Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Daten in Adobe Advertising {#lookback-a4adc}

Weil [!DNL Analytics] -Daten werden zum Reporting und zur Optimierung an Adobe Advertising gesendet. Die Daten unterliegen den Attributionsregeln, einschließlich der Impression- und Klick-Lookback-Fenster, die für den Advertiser in Adobe Advertising konfiguriert sind.

![Einstellungen des Lookback-Fensters auf Advertiser-Ebene in Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising - Click-Lookback-Fenster für die Attribution: Die Anzahl der Tage nach dem ersten Klick, in denen der Klick einer Konversion zugeordnet werden kann. Standardmäßig beträgt dieser Wert 60 Tage, der Höchstwert 90 Tage
* Impression-Lookback-Fenster der Adobe Advertising-Attribution: Die Anzahl der Tage nach dem Auftreten einer Ad-Impression, in denen die Impression einer Konversion zugeordnet werden kann. Standardmäßig ist dieser Wert 14 Tage, der Höchstwert 30 Tage

  >[!NOTE]
  >
  > Das Impression-Lookback-Fenster ist spezifisch für Adobe Advertising, nicht [!DNL Analytics for Advertising], Reporting.

Der [!DNL Analytics for Advertising] JavaScript verwendet diese Einstellungen, um zu bestimmen, wie weit ein Ansicht-Through-Eintrag oder ein Clickthrough-Eintrag für die Site als gültig betrachtet werden soll. Weitere Informationen zur Bestimmung von Durchsichten und Clickthroughs finden Sie unter &quot;[Adobe Advertising - Von Analytics verwendete IDs](ids.md).“

## Adobe Systems Werbung Daten in [!DNL Analytics]

[!DNL Analytics] Legt Adobe Systems Werbe-IDs (AMO IDs) innerhalb der Analytics Treffer fest, vorbehaltlich der [!DNL eVar] Persistenzeinstellung der Advertiser, die sowohl für Clickthroughs als auch für Ansicht Throughs gilt. Die Persistenzeinstellung wird im Adobe Systems Werbe-Backend konfiguriert und kann von Ihrem Adobe Systems Account Team geändert werden.

* [!DNL Analytics for Advertising][!DNL eVar] Gültigkeit: standardmäßig 60 Tage für AMO-IDs

>[!NOTE]
>
>Um Daten für eine andere Zeitrahmen zu Segment, können [Sie innerhalb Analysis Workspace benutzerdefinierte Segmente](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) mit unterschiedlichen Lookback-Fenstern einrichten.

## Unterstützte Anzeigenumgebungen

* Suche
* Anzeige
* Video
* Online-Video
* Connected TV
* Nativ

Wenden Sie sich an Ihr Adobe-Konto-Team , um die neuesten unterstützten Anzeigenumgebungen in den einzelnen Kanälen zu erhalten.

## Wichtige Informationen vor der Implementierung

* Das Implementierungs-Team von Adobe Advertising richtet die Integration ein.

* Für diese Integration werden keine zusätzlichen Kosten in Rechnung gestellt. Auch führen Server-Aufrufe nicht zu zusätzlichen Kosten [!DNL Analytics] oder Adobe Advertising-Gebühren.

* [!DNL Analytics for Advertising] ist Adserver-agnostisch: Ein Ansicht-Through- oder Click-Through kann von jedem Adserver aus erfolgen, und die richtigen IDs werden beim Betreten der Site generiert.

* Die Integration übergibt nur [!DNL Analytics] standardmäßige und benutzerdefinierte Ereignisse an Adobe Systems Advertising zur Gebot Optimierung nachfolgender bezahlte Medien und Werbemaßnahmen. Segmente, berechnete Metriken und [!DNL eVars] Adobe Systems Werbung werden nicht zur Gebot Optimierung übergeben[!DNL Analytics].

* Adobe Systems Advertising erstellt persistente IDs [!DNL Analytics] , die auf der letzten Anzeige basieren, auf die geklickt oder angezeigt wurde, bevor der User die Website betritt, basierend auf den [in Adobe Systems Advertising konfigurierten Click- und Ansicht-Through-Lookback-Fenstern](#lookback-a4adc) . Wenn ein Site-Besucher beide Arten von Site-Einstiegsinteraktionen in seinem Profil aufweist und der Klick innerhalb des Lookback-Zeitraums erfolgt, überschreibt die Clickthrough-ID des Besucher die Ansicht-Through-ID für Site-Berichte.

* [!DNL Analytics for Advertising] Konversion Tracking in Adobe Analytics verwendet ein konfigurierbares Tracking Lookback-Fenster (standardmäßig 60 Tage). Adobe Systems Werbeberichte spiegeln Site-Umrechnungen und Interaktion bis zum Ende dieses Tracking Lookback-Fensters wider.

* Alle Anzeigentypen werden unterstützt. Es werden jedoch nicht alle Anzeigenumgebungen unterstützt.

* [!DNL Analytics] Konversionen werden derzeit verfolgt und nur einem Besucher auf demselben Gerät zugeordnet.

* [!DNL Analytics for Advertising] unterstützt keine In-App-View-Through-Konversionen.

* Das View-Through-Tracking wird für Werbetreibende, die eine serverseitige Weiterleitungsimplementierung von verwenden, nicht unterstützt [!DNL Analytics].

### Ergänzende ID

Sobald der Experience Cloud Identity Service für eine Site implementiert ist, werden Treffer, die Daten aus dem [!DNL Analytics] oder Adobe Advertising eine zusätzliche ID enthalten.

Beispiel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Für eine präzise Datenintegration werden alle von einem [!DNL Analytics for Advertising] Die Aktivität zur Bereitstellung von Inhalten oder zur Aufzeichnung der Zielmetrik muss über eine entsprechende verfügen [!DNL Analytics] Treffer mit derselben zusätzlichen ID.

Bei der Fehlerbehebung in [!DNL Analytics]Stellen Sie sicher, dass die zusätzliche ID für vorhanden ist [!DNL Analytics] Treffer. In der [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html)wird diese ID auf der Registerkarte Adobe Advertising wie folgt angezeigt: `sdid` Parameter.

>[!NOTE]
>
> Diese Implementierung funktioniert ähnlich wie die [!DNL Analytics for Target] Integration.

>[!MORELIKETHIS]
>
>* [Überblick über [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript-Code für Analytics für Advertising](/help/integrations/analytics/javascript.md)
