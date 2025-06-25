---
title: Überblick über [!DNL Analytics for Advertising]
description: Überblick über [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Übersicht über [!DNL Analytics for Advertising]

*Werbetreibende mit Advertising DSP und[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] integriert Adobe Analytics und Adobe Advertising, um die Funktionen der einzelnen Produkte zu erweitern und zu verbessern.

Die Integration ermöglicht es Werbetreibenden, Clickthrough- und View-Through-Site-Interaktionen in ihren [!DNL Analytics] Instanzen zu verfolgen, sodass Marken sehen können, wie ihre Werbeausgaben zu Website-Interaktion und wichtigen Geschäftszielen führen.

Darüber hinaus kann Adobe Advertising auf die umfangreichen First-Party-Daten zugreifen, die [!DNL Analytics] mithilfe von bereits auf der Site befindlichen [!DNL Analytics]-Tags erfasst. Dies ermöglicht eine robustere Journey-Verwaltung, First-Party-Remarketing und Paid-Media-Site-Reporting. Adobe Advertising kann die [!DNL Analytics] Daten weiterhin zur Ausgaben- und Angebotsoptimierung verwenden.

Bei richtiger Anwendung verwischt [!DNL Analytics for Advertising] die Grenzen zwischen zwei herkömmlichen Rollen: Advertising Journey-Management (der Vorgang, Benutzende über Anzeigen zur Website zu senden) und das Verständnis dieser Website-Interaktion durch Web-Analysen.

Primäre Vorteile:

* Senden Sie [!DNL Analytics] Segmente direkt an Adobe Advertising für das Remarketing von Erstanbieter-Sites.
* Verwenden Sie [!DNL Analytics] benutzerspezifischen und standardmäßigen Ereignisse als Konversionssignale zur Optimierung der Paid-Media-Werbung.
* Nutzen Sie [!DNL Analytics] Analysis Workspace, um Site-Einstiegspunkte und das Besuchsverhalten besser zu verstehen.
* Ermöglichen Sie eine engere Zusammenarbeit zwischen Web-Analysten und Paid-Media-Teams.
* Verwenden Sie persistente Viewthrough- und Clickthrough-IDs von Adobe Advertising in [!DNL Analytics], um die Website-Interaktion zu verstehen.
* Verbessern Sie herkömmliche Paid-Media-Berichte in Analysis Workspace mit benutzerdefinierten Metriken, benutzerdefinierten Dimensionen und der Site-Aktivität, die beim Exportieren von Daten oder Pixeln in Werbeserver oder andere DSPs nicht erreicht werden können.
* Nutzen Sie [!DNL Analytics] Code, der sich bereits auf Ihrer Website befindet, für das Tracking und die Optimierung in Adobe Advertising.

>[!TIP]
>
> Sehen Sie sich ein [Video Einführung in an [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## Verwenden von Analytics für Paid Media-Berichte

[!DNL Analytics for Advertising] verbessert die Berichterstellung und die insight dazu, wie Ihre Werbung das Verhalten auf Ihrer Site beeinflusst, indem sie Folgendes ermöglicht:

* Verwenden Sie persistente Viewthrough- und Clickthrough-IDs von Adobe Advertising in [!DNL Analytics], um die Website-Interaktion zu verstehen.
* Nutzen Sie Analysis Workspace, um Site-Einstiegspunkte und das Besuchsverhalten besser zu verstehen. Sie können auf Paid-Media-Dimensions- und -Ereignisdaten zugreifen, darunter Adobe Advertising-Kampagnenentitätsnamen (bis hin zu Platzierungen und Anzeigen) und die zugehörigen Metriken wie Klicks, Impressionen und Kosten.

Um [!DNL Analytics] als Reporting-Tool für bezahlte Medien verwenden zu können, benötigt Ihr Unternehmen eine Experience Cloud-Anmeldung mit Zugriff auf Analysis Workspace. Ihr Adobe Advertising-Team hilft Ihnen bei der Zuordnung Ihrer Adobe Advertising-Daten zu einzelnen Report Suites in Analysis Workspace. Sie können Adobe Advertising-Daten an beliebige Report Suites senden, sollten jedoch die Report Suites kennen, die Adobe Advertising zugeordnet wurden, und die, die dies nicht getan haben. Je nach Report Suite kann dies die gemeldeten Daten ändern.

[Adobe Advertising-IDs innerhalb von [!DNL Analytics]](ids.md) funktionieren wie andere [!DNL eVars] mit einer benutzerdefinierten, dauerhaften Gültigkeit. Standardmäßig ist das Attributions-Lookback-Fenster während der Adobe Advertising-Implementierung auf 60 Tage festgelegt. Um diese Einstellung zu ändern, wenden Sie sich an Ihr Adobe Account Team.

Adobe Advertising-Dimensionen werden mit dem Suffix „(AMO ID)“ angehängt (z. B. „Ad Type (AMO ID)„). Unter &quot;[Adobe Advertising-Metriken in Analysis Workspace](advertising-metrics-in-analytics.md)&quot; finden Sie eine Liste der verfügbaren Dimensionen.

>[!NOTE]
>
> Wenn Sie Adobe Advertising-Daten (oder beliebige Datensätze) in [!DNL Analytics] anzeigen, beachten Sie, dass Metriken und Berichte auf den in [!DNL Analytics] festgelegten Regeln basieren. Die Daten können sich von denen in anderen Berichtssystemen unterscheiden, z. B. Anzeigen-Server-Berichte, [!DNL DSP]-Berichte oder Suchmaschinenberichte. Um die Datenunterschiede in [!DNL Analytics] zu verstehen, müssen Sie wissen, wann [!DNL eVar] Daten ablaufen, was einen Besuch definiert, was als Letztkontakt-Attribution im Vergleich zur Gesamtzahl der persistenten Attributionen gilt und andere Faktoren. Weitere Informationen finden Sie unter [Erwartete Datenabweichungen zwischen  [!DNL Analytics]  und Adobe Advertising](data-variances.md).

## Verwenden von Analytics zur Unterstützung von Adobe Advertising-Kampagnen und -Portfolios

Ohne zusätzliche Pixel ermöglicht [!DNL Analytics for Advertising] eine bessere Optimierung und einfachere Zielgruppensegmentierung, indem zwei Hauptsignale an Adobe Advertising gesendet werden:

* Konversionsmetriken zur Verwendung als Bid-Signale:
   * Standardmetriken wie [!UICONTROL Revenue] und [!UICONTROL Cart Views].
   * Site-Interaktionsmetriken wie Seitenansichts- und Besuchsmetriken.
   * Benutzerdefinierte Umsatzmetriken.
   * Reservierte Umsatzmetriken.
* In [!DNL Analytics] erstellte und in Experience Cloud veröffentlichte Segmente

  Sie können [!DNL Analytics] Segmente für das Retargeting von Erstanbieter-Websites in [!DNL DSP]- und Paid-Search-Anzeigen verwenden.

  (Nur [!DNL Search, Social, & Commerce]) Werbetreibende mit [!DNL Analytics], aber nicht mit Audience Manager können auch tagbasierte Zielgruppen für die Google-Website (Remarketing-Listen) und Zielgruppen für den Kundenabgleich (Kundenlisten) aus [!DNL Analytics] Segmenten erstellen, die mit Experience Cloud freigegeben werden.

### Site-Konversionsmetriken als Bid-Signale

Sie können Ihre Standardereignisse und benutzerspezifischen Ereignisse aus [!DNL Analytics] verwenden, um gewichtete Ziele in Adobe Advertising zu erstellen. Ziele bestimmen die Angebotsentscheidungen für Ihre [!DNL DSP]-Pakete und die Portfolios für Search, Social und Commerce.

Für [!DNL Google Ads]- und [!DNL Google Microsoft Advertising]-Kampagnen in den Hybridportfolios von Search, Social und Commerce können Sie die Ziele - einschließlich aller [!DNL Analytics] Ereignisse in den Zielen - optional direkt in die Werbenetzwerke hochladen, wo sie als Konversionsaktionen für benutzerdefinierte Konversionsziele auf Konto- und Kampagnenebene zur Verfügung stehen.

>[!NOTE]
>
> Sie können keine berechneten Metriken von [!DNL Analytics] in Adobe Advertising zuordnen.

Ihr Adobe Advertising-Team hilft Ihnen, die Ereignisse, die für die Paid-Media-Leistung relevant sind, zu identifizieren und in Adobe Advertising zuzuordnen, wo sie unter [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Conversions] aufgeführt sind.

Eine Liste der verfügbaren [ finden Sie unter &quot;](analytics-data-in-advertising.md) in Adobe Advertising&quot;.

### Analytics-Segmente für Site-Retargeting

Adobe Advertising kann mithilfe der nativen Integration von Experience Cloud Audiences zwischen [!DNL Analytics] und Experience Cloud [!DNL Analytics] Segmente für Remarketing-Zwecke für Advertising DSP- und [!DNL Search, Social, & Commerce]-Anzeigen aufnehmen.

Um auf die [!DNL Analytics] Segmente zugreifen zu können, muss ein Advertiser-Konto den [Experience Cloud ID-Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) aktivieren. Wenn der ID-Service aktiviert ist, werden alle Experience Cloud-Segmente (einschließlich der in [!DNL Analytics] erstellten und in Experience Cloud veröffentlichten Segmente, der in Adobe Audience Manager erstellten Segmente, der mit dem [!DNL People core service] in Experience Cloud erstellten Segmente und der in Adobe Experience Platform erstellten und über Audience Manager an Adobe Advertising gesendeten Segmente) innerhalb von Adobe Advertising verfügbar, sobald sie verarbeitet werden.

[!DNL Analytics] Segmente sind innerhalb von 24 Stunden verfügbar und werden täglich aktualisiert.

Weitere Informationen zum Experience Cloud-Zielgruppen-Service finden Sie unter [Experience Cloud-Zielgruppen](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Beispiele für die Verwendung der Integration {#integration-examples}

### Verwenden von Adobe Advertising-Daten in Analysis Workspace

Informationen dazu, wie Sie Ihre Adobe Advertising-Daten zum Erstellen visueller Berichte in Analysis Workspace verwenden können, finden Sie im Video [Einführung in Workspace und Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).

#### Verwenden von Connected TV-View-Through-Konversionen in Berichten

*Nur Advertising DSP-Benutzer*

Sie können die volle Trichtereffektivität Ihrer CTV-Kampagnen (Connected TV) messen, indem Sie die Anzeigenexposition auf CTV-Geräten mit Konversionen vor Ort verknüpfen. Der neue [!UICONTROL Landing Type] &quot;[!UICONTROL View-through (CTV)]&quot; unterteilt Konversionen in separate Zeilen für [!UICONTROL Click Through]-, [!UICONTROL View Through]- und [!UICONTROL View Through (CTV)].

Um Ihre CTV-View-Through-Konversionsmetriken anzuzeigen, verwenden Sie entweder die Platzierungs- oder die Marketing-Kanal-Ansicht in Analysis Workspace.

Verwenden der Platzierungsansicht:

1. CTV-Ausgabenplatzierungen in die Berichtsansicht einschließen.

1. Schließen Sie die gewünschten Metriken wie „Impressionen“, „Klicks“ usw. ein.

1. Wenden Sie die folgenden Filter an:

   Anzeigenplattform: `Advertising Cloud DSP`

   Landingpage: `View-Through (CTV)`

Verwenden der Marketing-Kanal-Ansicht:

1. `Marketing Channel` einschließen.

1. Schließen Sie die gewünschten Metriken wie „Impressionen“, „Klicks“ usw. ein.

1. Wenden Sie die folgenden Filter an:

   Anzeigenplattform: `Advertising Cloud DSP`

   Landingpage: `View-Through (CTV)`

### Erstellen von Adobe Advertising-Dashboards

Informationen dazu, wie Sie Ihre Adobe Advertising-Daten im Vergleich zu Ihren Zielen in Analysis Workspace verfolgen können, finden Sie im Video [Erstellen von Adobe Advertising-Dashboards mit Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html).

### Verwenden der Adobe Advertising-ID für Site Entry Analysis

Wie Sie einen Adobe Advertising-Site-Einstiegsbericht erstellen können, um Wochentag, Tageszeit, Browser und geografische Einflüsse zu überwachen, erfahren Sie im Video &quot;[Erstellen von Adobe Advertising Site Entry Reports](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html)&quot;.

## So starten Sie eine [!DNL Analytics for Advertising] Implementierung

Wenden Sie sich an Ihr Adobe-Kundenbetreuerteam, das die für den Einstieg erforderliche Erstkonfiguration durchführt und Sie bei der Planung Ihrer Implementierung und Datennutzung entsprechend den Anforderungen Ihres Unternehmens unterstützt.

>[!MORELIKETHIS]
>
>* [Video: Einführung in [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Voraussetzungen und wichtige Informationen für die Implementierung [!DNL Analytics for Advertising]](prerequisites.md)
>* [Von Analytics verwendete Adobe Advertising-IDs](ids.md)
>* [JavaScript-Code für Analytics für Advertising](/help/integrations/analytics/javascript.md)
>* [Erwartete Datenabweichungen zwischen  [!DNL Analytics]  und Adobe Advertising](data-variances.md)
>* [Adobe Advertising-Metriken in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Daten in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
