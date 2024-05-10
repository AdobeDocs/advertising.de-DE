---
title: Übersicht über [!DNL Analytics for Advertising]
description: Übersicht über [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---

# Übersicht über [!DNL Analytics for Advertising]

*Advertiser mit Advertising DSP und[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] integriert Adobe Analytics und Adobe Advertising, um die Funktionen der einzelnen Produkte zu erweitern und zu erweitern.

Die Integration ermöglicht es Advertisern, Clickthrough- und Durchsichts-Site-Interaktionen in ihren [!DNL Analytics] Instanzen, sodass Marken sehen können, wie ihre Werbeausgaben zu Site-Interaktionen und kritischen Geschäftszielen führen.

Darüber hinaus kann Adobe Advertising auf die umfangreichen Erstanbieterdaten zugreifen, die [!DNL Analytics] erfasst mithilfe von [!DNL Analytics] Tags bereits auf der Site. Dies ermöglicht ein robusteres Journey-Management, Erstanbieter-Remarketing und die Berichterstellung für gebührenpflichtige Medien-Sites. Adobe Advertising kann die [!DNL Analytics] Daten zur Ausgaben- und Angebotsoptimierung.

bei ordnungsgemäßer Arbeit, [!DNL Analytics for Advertising] die Linien zwischen zwei herkömmlichen Journey-Rollen verwischt: das Anzeigen--Management (die Aktion, mit der Benutzer durch Werbung auf die Site geleitet werden) und das Verständnis dieser Site-Interaktion durch Webanalysen.

Primäre Vorteile:

* Senden [!DNL Analytics] Segmente direkt auf Adobe Advertising für Erstanbieter-Site-Remarketing.
* Verwendung [!DNL Analytics] benutzerspezifische und standardmäßige Ereignisse als Konversionssignale zur Optimierung der Paid-Media-Werbung.
* Nutzen Sie die Vorteile [!DNL Analytics] Analysis Workspace , um Einstiegspunkte und Besuchsverhalten der Site besser zu verstehen.
* Schaffen Sie eine engere Zusammenarbeit zwischen Webanalysten und Paid-Media-Teams.
* Verwenden persistenter Adobe Advertising-Durchsichts- und Clickthrough-IDs in [!DNL Analytics] , um die Site-Interaktion zu verstehen.
* Erweitern Sie herkömmliche Berichte zu gebührenpflichtigen Medien in Analysis Workspace mit benutzerdefinierten Metriken, benutzerdefinierten Dimensionen und Site-Aktivitäten, die beim Exportieren von Daten oder Pixeln in Werbeserver oder andere DSP nicht erreichbar sind.
* Nutzen Sie die Vorteile [!DNL Analytics] Code, der bereits auf Ihrer Website zur Verfolgung und Optimierung innerhalb von Adobe Advertising verfügbar ist.

>[!TIP]
>
> Sehen Sie sich eine [Videoeinführung in [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics).

## Verwenden von Analytics für Berichte zu gebührenpflichtigen Medien

[!DNL Analytics for Advertising] verbessert die Berichterstellung und Einblicke, wie Ihre Werbung das Site-Verhalten fördert, indem Sie:

* Verwenden persistenter Adobe Advertising-Durchsichts- und Clickthrough-IDs in [!DNL Analytics] , um die Site-Interaktion zu verstehen.
* Nutzen Sie Analysis Workspace, um Einstiegspunkte auf der Site und das Besuchsverhalten besser zu verstehen. Sie können auf Paid-Media-Dimensions- und Ereignisdaten zugreifen, zu denen Adobe Advertising-Kampagnenentitätsnamen (bis hin zu Platzierungen und Anzeigen) und die zugehörigen Metriken wie Klicks, Impressionen und Kosten gehören.

Verwendung [!DNL Analytics] als Reporting-Tool für gebührenpflichtige Medien benötigt Ihr Unternehmen eine Experience Cloud-Anmeldung mit Zugriff auf Analysis Workspace. Ihr Adobe Advertising-Team hilft Ihnen bei der Zuordnung Ihrer Adobe Advertising-Daten zu einzelnen Report Suites in Analysis Workspace. Sie können Adobe Advertising-Daten an eine beliebige Report Suite senden. Beachten Sie jedoch die Report Suites, die Adobe Advertising zugeordnet wurden, und jene, die dies nicht getan haben. Abhängig von der Report Suite kann dies die gemeldeten Daten ändern.

[Adobe Advertising-IDs in [!DNL Analytics]](ids.md) funktioniert wie andere [!DNL eVars], mit einer benutzerdefinierten, beständigen Gültigkeit. Standardmäßig ist das Attributions-Lookback-Fenster während der Adobe Advertising-Implementierung auf 60 Tage eingestellt. Wenden Sie sich an Ihr Adobe-Account-Team, um diese Einstellung zu ändern.

Adobe Advertising-Dimensionen werden mit dem Suffix &quot;(AMO-ID)&quot;angehängt (z. B. &quot;Anzeigentyp (AMO-ID)&quot;). Siehe &quot;[Adobe Advertising von Metriken in Analysis Workspace](advertising-metrics-in-analytics.md)&quot; für eine Liste der verfügbaren Dimensionen.

>[!NOTE]
>
> Wenn Sie Adobe Advertising-Daten (oder einen beliebigen Datensatz) in [!DNL Analytics]Beachten Sie, dass Metriken und Berichte auf den Regeln basieren, die in [!DNL Analytics]. Die Daten können sich von denen in anderen Berichterstattungssystemen unterscheiden, z. B. in Berichten für Werbeserver, [!DNL DSP] Berichte oder Suchmaschinenberichte. So verstehen Sie die Datenunterschiede in [!DNL Analytics], müssen Sie wissen, wann [!DNL eVar] Daten laufen ab, was einen Besuch definiert, was als Letztkontakt-Attribution im Vergleich zur persistenten Gesamtattribution betrachtet wird und andere Faktoren. Weitere Informationen finden Sie unter [Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising](data-variances.md).

## Verwenden von Analytics zum Power Adobe Advertising-Kampagnen und -Portfolios

Ohne zusätzliche Pixel zu benötigen, [!DNL Analytics for Advertising] ermöglicht eine bessere Optimierung und einfachere Zielgruppensegmentierung, indem zwei Hauptsignale an Adobe Advertising gesendet werden:

* Als Angebotssignale zu verwendende Konversionsmetriken:
   * Standardmetriken, z. B. [!UICONTROL Revenue] und [!UICONTROL Cart Views].
   * Site-Interaktionsmetriken, z. B. Seitenansichts- und Besuchsmetriken.
   * benutzerspezifische Umsatzmetriken.
   * reservierte Umsatzmetriken.
* In erstellte Segmente [!DNL Analytics] und auf Experience Cloud veröffentlicht.

  Sie können [!DNL Analytics] Segmente für Erstanbieter-Site-Retargeting in [!DNL DSP] und Paid Search-Werbung.

  ([!DNL Search, Social, & Commerce] Nur Advertiser mit [!DNL Analytics] Audience Manager können jedoch auch nicht aus Google-Website-Tag-basierte Zielgruppen (Remarketing-Listen) und Zielgruppen für die Kundenübereinstimmung (Kundenlisten) aus erstellen. [!DNL Analytics] Segmente, die für Experience Cloud freigegeben sind.

### Site-Konversionsmetriken als Angebotssignale

Sie können Ihre Standardereignisse und benutzerspezifischen Ereignisse aus [!DNL Analytics] um gewichtete Ziele in der Adobe Advertising zu erstellen. Ziele informieren über Angebotsentscheidungen für Ihre [!DNL DSP] Packages und Suchportfolios.

>[!NOTE]
>
> Berechnete Metriken können nicht zugeordnet werden aus [!DNL Analytics] in Adobe Advertising.

Ihr Adobe Advertising-Team hilft Ihnen dabei, die für die Leistung von Paid Media relevanten Ereignisse zu identifizieren und der Adobe Advertising zuzuordnen, wo sie aufgeführt sind in [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions].

Siehe &quot;[Analytics-Metriken im Adobe Advertising](analytics-data-in-advertising.md)für eine Liste der verfügbaren Metriken.

### Analytics-Segmente für Site-Retargeting

Adobe Advertising can ingest [!DNL Analytics] Segmente für Remarketing-Zwecke für Advertising DSP und [!DNL Search, Social, & Commerce] Anzeigen, die die native Experience Cloud-Zielgruppenintegration zwischen [!DNL Analytics] und Experience Cloud.

So greifen Sie auf die [!DNL Analytics] Segmente, muss ein Advertiser-Konto über die [Experience Cloud ID-Dienst](https://experienceleague.adobe.com/docs/id-service/using/home.html) aktiviert. Wenn der ID-Dienst aktiviert ist, werden alle Experience Cloud-Segmente (einschließlich der in [!DNL Analytics] und auf Experience Cloud veröffentlicht werden, in Adobe Audience Manager erstellte Segmente, Segmente, die in Experience Cloud mithilfe der [!DNL People core service], und Segmente, die in Adobe Experience Platform erstellt und über den Audience Manager an Adobe Advertising gesendet wurden) in Adobe Advertising verfügbar werden, sobald sie verarbeitet werden.

[!DNL Analytics] -Segmente sind innerhalb von 24 Stunden verfügbar und werden täglich aktualisiert.

Weitere Informationen zum Experience Cloud-Zielgruppendienst finden Sie unter [Experience Cloud Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Beispiele zur Verwendung der Integration {#integration-examples}

### Verwenden von Adobe Advertising-Daten in Analysis Workspace

Informationen dazu, wie Sie mit Ihren Adobe Advertising-Daten visuelle Berichte in Analysis Workspace erstellen können, finden Sie im Video &quot;[Einführung in Workspace und Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

#### Verwenden von Connected TV-Durchsichtskonversionen in Berichten

*Nur Advertising DSP Benutzer*

Sie können die Volltrichter-Effektivität Ihrer verbundenen TV-Kampagnen (CTV) messen, indem Sie die Anzeige auf CTV-Geräten mit Konversionen vor Ort verknüpfen. Die neue [!UICONTROL Landing Type] filter &quot;[!UICONTROL View-through (CTV)]&quot; teilt Konversionen in separate Zeilen für [!UICONTROL Click Through], [!UICONTROL View Through], und [!UICONTROL View Through (CTV)] -Werte.

Um Ihre CTV-Durchsichts-Konversionsmetriken anzuzeigen, verwenden Sie entweder die Platzierungsansicht oder die Marketingkanal-Ansicht in Analysis Workspace.

Verwenden der Platzierungsansicht:

1. Schließen Sie CTV-Ausgaben-Platzierungen in die Berichtsansicht ein.

1. Schließen Sie die gewünschten Metriken ein, z. B. &quot;Impressionen&quot;, &quot;Klicks&quot; usw.

1. Wenden Sie die folgenden Filter an:

   Anzeigenplattform: `Advertising Cloud DSP`

   Landingpage: `View-Through (CTV)`

Verwenden der Marketingkanal-Ansicht:

1. Dimension einschließen `Marketing Channel`.

1. Schließen Sie die gewünschten Metriken ein, z. B. &quot;Impressionen&quot;, &quot;Klicks&quot; usw.

1. Wenden Sie die folgenden Filter an:

   Anzeigenplattform: `Advertising Cloud DSP`

   Landingpage: `View-Through (CTV)`

### Erstellen von Adobe Advertising-Dashboards

Informationen dazu, wie Sie Ihre Adobe Advertising-Daten anhand Ihrer Ziele in Analysis Workspace verfolgen können, finden Sie im Video &quot;[Erstellen von Adobe Advertising-Dashboards mit Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Verwenden der Adobe Advertising-ID für die Site-Einstiegsanalyse

Wie Sie einen Site-Einstiegsbericht erstellen können, um Wochentage, Tageszeit, Browser und geografische Einflüsse zu überwachen, erfahren Sie im Video .[Erstellen von Adobe Advertising Site-Einstiegsberichten](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [Video: Einführung in [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Voraussetzungen und Schlüsselinformationen für die Implementierung [!DNL Analytics for Advertising]](prerequisites.md)
>* [Von Analytics verwendete Adobe Advertising-IDs](ids.md)
>* [JavaScript-Code für Analytics für Werbung](/help/integrations/analytics/javascript.md)
>* [Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising](data-variances.md)
>* [Adobe Advertising von Metriken in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Daten in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
