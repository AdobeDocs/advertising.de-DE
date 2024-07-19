---
title: Überblick über [!DNL Analytics for Advertising]
description: Überblick über [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: a0a3bb1e74ffc687118d0336a03dcc6164b67226
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 0%

---

# Überblick über [!DNL Analytics for Advertising]

*Advertiser mit Advertising DSP und[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] integriert Adobe Analytics und Adobe Advertising, um die Funktionen der einzelnen Produkte zu erweitern und zu erweitern.

Die Integration ermöglicht es Advertisern, Clickthrough- und Durchsichts-Site-Interaktionen in ihren [!DNL Analytics]-Instanzen zu verfolgen, sodass Marken sehen können, wie ihre Werbeausgaben zu Site-Interaktionen und wichtigen Geschäftszielen führen.

Darüber hinaus kann Adobe Advertising auf die umfangreichen Erstanbieterdaten zugreifen, die [!DNL Analytics] mithilfe von [!DNL Analytics] -Tags erfasst, die sich bereits auf der Site befinden. Dies ermöglicht ein robusteres Journey-Management, Erstanbieter-Remarketing und die Berichterstellung für gebührenpflichtige Medien-Sites. Adobe Advertising kann die [!DNL Analytics] -Daten weiter für die Ausgaben- und Angebotsoptimierung verwenden.

Bei ordnungsgemäßer Verwendung verwischt [!DNL Analytics for Advertising] die Linien zwischen zwei herkömmlichen Journey-Rollen: Anzeigen--Management (das Senden von Benutzern über Anzeigen zur Site) und Verstehen der Site-Interaktion über Webanalysen.

Primäre Vorteile:

* Senden Sie [!DNL Analytics] -Segmente direkt an Adobe Advertising, um Erstanbieter-Site-Remarketing zu ermöglichen.
* Verwenden Sie [!DNL Analytics] benutzerspezifische und standardmäßige Ereignisse als Konversionssignale zur Optimierung der Paid-Media-Werbung.
* Nutzen Sie die Vorteile von [!DNL Analytics] Analysis Workspace, um Einstiegspunkte und Besuchsverhalten auf der Site besser zu verstehen.
* Schaffen Sie eine engere Zusammenarbeit zwischen Webanalysten und Paid-Media-Teams.
* Verwenden Sie persistente Adobe Advertising-Durchsichts- und Clickthrough-IDs in [!DNL Analytics], um die Site-Interaktion zu verstehen.
* Erweitern Sie herkömmliche Berichte zu gebührenpflichtigen Medien in Analysis Workspace mit benutzerdefinierten Metriken, benutzerdefinierten Dimensionen und Site-Aktivitäten, die beim Exportieren von Daten oder Pixeln in Werbeserver oder andere DSP nicht erreichbar sind.
* Nutzen Sie den [!DNL Analytics] -Code, der bereits auf Ihrer Website zur Verfolgung und Optimierung innerhalb von Adobe Advertising verfügbar ist.

>[!TIP]
>
> Sehen Sie sich eine [Videoeinführung zu  [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html#analytics) an.

## Verwenden von Analytics für Berichte zu gebührenpflichtigen Medien

[!DNL Analytics for Advertising] verbessert die Berichterstellung und Einblicke, wie Ihre Werbung das Site-Verhalten beeinflusst, indem Sie Folgendes tun können:

* Verwenden Sie persistente Adobe Advertising-Durchsichts- und Clickthrough-IDs in [!DNL Analytics], um die Site-Interaktion zu verstehen.
* Nutzen Sie Analysis Workspace, um Einstiegspunkte auf der Site und das Besuchsverhalten besser zu verstehen. Sie können auf Paid-Media-Dimensions- und Ereignisdaten zugreifen, zu denen Adobe Advertising-Kampagnenentitätsnamen (bis hin zu Platzierungen und Anzeigen) und die zugehörigen Metriken wie Klicks, Impressionen und Kosten gehören.

Um [!DNL Analytics] als Reporting-Tool für gebührenpflichtige Medien zu verwenden, benötigt Ihr Unternehmen eine Experience Cloud-Anmeldung mit Zugriff auf Analysis Workspace. Ihr Adobe Advertising-Team hilft Ihnen bei der Zuordnung Ihrer Adobe Advertising-Daten zu einzelnen Report Suites in Analysis Workspace. Sie können Adobe Advertising-Daten an eine beliebige Report Suite senden. Beachten Sie jedoch die Report Suites, die Adobe Advertising zugeordnet wurden, und jene, die dies nicht getan haben. Abhängig von der Report Suite kann dies die gemeldeten Daten ändern.

[Adobe Advertising-IDs innerhalb von  [!DNL Analytics]](ids.md) funktionieren wie andere [!DNL eVars] mit einem benutzerdefinierten, beständigen Ablauf. Standardmäßig ist das Attributions-Lookback-Fenster während der Adobe Advertising-Implementierung auf 60 Tage eingestellt. Wenden Sie sich an Ihr Adobe-Account-Team, um diese Einstellung zu ändern.

Adobe Advertising-Dimensionen werden mit dem Suffix &quot;(AMO-ID)&quot;angehängt (z. B. &quot;Anzeigentyp (AMO-ID)&quot;). Eine Liste der verfügbaren Dimensionen finden Sie unter &quot;[Adobe Advertising-Metriken in Analysis Workspace](advertising-metrics-in-analytics.md)&quot;.

>[!NOTE]
>
> Beachten Sie bei der Anzeige von Adobe Advertising-Daten (oder beliebigen Datensätzen) in [!DNL Analytics], dass Metriken und Berichte auf den in [!DNL Analytics] festgelegten Regeln basieren. Die Daten können sich von denen in anderen Berichterstellungssystemen unterscheiden, z. B. in Berichten zu Anzeigenservern, [!DNL DSP] Berichten oder Suchmaschinenberichten. Um die Datenunterschiede in [!DNL Analytics] zu verstehen, müssen Sie wissen, wann [!DNL eVar] -Daten ablaufen, was einen Besuch definiert, was als Letztkontakt-Attribution im Vergleich zur gesamten persistenten Attribution betrachtet wird und andere Faktoren. Weitere Informationen finden Sie unter [Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising](data-variances.md).

## Verwenden von Analytics zum Power Adobe Advertising-Kampagnen und -Portfolios

Ohne zusätzliche Pixel zu benötigen, ermöglicht [!DNL Analytics for Advertising] eine bessere Optimierung und einfachere Zielgruppensegmentierung, indem zwei Hauptsignale an Adobe Advertising gesendet werden:

* Als Angebotssignale zu verwendende Konversionsmetriken:
   * Standardmetriken wie [!UICONTROL Revenue] und [!UICONTROL Cart Views].
   * Site-Interaktionsmetriken, z. B. Seitenansichts- und Besuchsmetriken.
   * benutzerspezifische Umsatzmetriken.
   * reservierte Umsatzmetriken.
* In [!DNL Analytics] erstellte und auf Experience Cloud veröffentlichte Segmente.

  Sie können [!DNL Analytics]-Segmente für Erstanbieter-Site-Retargeting in [!DNL DSP] und Paid-Search-Anzeigen verwenden.

  ([!DNL Search, Social, & Commerce] only) Advertiser mit [!DNL Analytics], aber nicht Audience Manager können auch Google-Website-Tag-basierte Zielgruppen (Remarketing-Listen) und Kundenabgleichzielgruppen (Kundenlisten) aus [!DNL Analytics] Segmenten erstellen, die für Experience Cloud freigegeben sind.

### Site-Konversionsmetriken als Angebotssignale

Sie können Standardereignisse und benutzerspezifische Ereignisse von [!DNL Analytics] verwenden, um gewichtete Ziele in Adobe Advertising zu erstellen. Ziele informieren über Angebotsentscheidungen für Ihre [!DNL DSP]-Pakete und Suchportfolios.

>[!NOTE]
>
> Sie können berechnete Metriken von [!DNL Analytics] nicht Adobe Advertising zuordnen.

Ihr Adobe Advertising-Team hilft Ihnen dabei, die für die Leistung von Paid Media relevanten Ereignisse zu identifizieren und der Adobe Advertising zuzuordnen, wo sie unter [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions] aufgeführt sind.

Eine Liste der verfügbaren Metriken finden Sie unter &quot;[Analytics-Metriken in Adobe Advertising](analytics-data-in-advertising.md)&quot;.

### Analytics-Segmente für Site-Retargeting

Adobe Advertising kann [!DNL Analytics] -Segmente für Remarketing-Zwecke für Advertising DSP- und [!DNL Search, Social, & Commerce]-Anzeigen erfassen, indem die native Experience Cloud-Zielgruppenintegration zwischen [!DNL Analytics] und Experience Cloud verwendet wird.

Um auf die [!DNL Analytics] -Segmente zuzugreifen, muss ein Advertiser-Konto den [Experience Cloud ID-Dienst](https://experienceleague.adobe.com/docs/id-service/using/home.html) aktivieren. Wenn der ID-Dienst aktiviert ist, werden alle Experience Cloud-Segmente (einschließlich in [!DNL Analytics] erstellte und auf Experience Cloud veröffentlichte Segmente, in Adobe Audience Manager erstellte Experience Cloud-Segmente, mit [!DNL People core service] erstellte Segmente und in Adobe Experience Platform erstellte Segmente, die per Audience Manager an Adobe Advertising gesendet werden) innerhalb von Adobe Advertising verfügbar, sobald sie verarbeitet werden.

[!DNL Analytics] -Segmente sind innerhalb von 24 Stunden verfügbar und werden täglich aktualisiert.

Weitere Informationen zum Experience Cloud-Zielgruppendienst finden Sie unter [Experience Cloud-Zielgruppen](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Beispiele zur Verwendung der Integration {#integration-examples}

### Verwenden von Adobe Advertising-Daten in Analysis Workspace

Informationen dazu, wie Sie mit Ihren Adobe Advertising-Daten visuelle Berichte in Analysis Workspace erstellen können, finden Sie im Video &quot;[Einführung in Workspace und Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html)&quot;.

#### Verwenden von Connected TV-Durchsichtskonversionen in Berichten

*Nur Advertising DSP-Benutzer*

Sie können die Volltrichter-Effektivität Ihrer verbundenen TV-Kampagnen (CTV) messen, indem Sie die Anzeige auf CTV-Geräten mit Konversionen vor Ort verknüpfen. Der neue [!UICONTROL Landing Type] -Filter &quot;[!UICONTROL View-through (CTV)]&quot; teilt Konversionen für die Werte [!UICONTROL Click Through], [!UICONTROL View Through] und [!UICONTROL View Through (CTV)] in separate Zeilen auf.

Um Ihre CTV-Durchsichts-Konversionsmetriken anzuzeigen, verwenden Sie entweder die Platzierungsansicht oder die Marketingkanal-Ansicht in Analysis Workspace.

Verwenden der Platzierungsansicht:

1. Schließen Sie CTV-Ausgaben-Platzierungen in die Berichtsansicht ein.

1. Schließen Sie die gewünschten Metriken ein, z. B. &quot;Impressionen&quot;, &quot;Klicks&quot; usw.

1. Wenden Sie die folgenden Filter an:

   Anzeigenplattform: `Advertising Cloud DSP`

   Landingpage: `View-Through (CTV)`

Verwenden der Marketingkanal-Ansicht:

1. Schließen Sie die Dimension &quot;`Marketing Channel`&quot;ein.

1. Schließen Sie die gewünschten Metriken ein, z. B. &quot;Impressionen&quot;, &quot;Klicks&quot; usw.

1. Wenden Sie die folgenden Filter an:

   Anzeigenplattform: `Advertising Cloud DSP`

   Landingpage: `View-Through (CTV)`

### Erstellen von Adobe Advertising-Dashboards

Informationen dazu, wie Sie Ihre Adobe Advertising-Daten anhand Ihrer Ziele in Analysis Workspace verfolgen können, finden Sie im Video &quot;[Erstellen von Adobe Advertising-Dashboards mit Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html)&quot;.

### Verwenden der Adobe Advertising-ID für die Site-Einstiegsanalyse

Informationen zum Erstellen eines Site-Einstiegsberichts zur Überwachung von Wochentag, Tageszeit, Browser und geografischen Einflüssen finden Sie im Video &quot;[Erstellen von Einstiegsberichten für Adobe Advertising-Sites](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html)&quot;.

## Initiieren einer [!DNL Analytics for Advertising]-Implementierung

Wenden Sie sich an Ihr Adobe Account-Team, das die für den Start erforderliche Erstkonfiguration abschließt und Ihnen bei der Planung Ihrer Implementierung und Datennutzung entsprechend den Anforderungen Ihres Unternehmens hilft.

>[!MORELIKETHIS]
>
>* [Video: Einführung in [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html)
>* [Voraussetzungen und wichtige Informationen für die Implementierung [!DNL Analytics for Advertising]](prerequisites.md)
>* [Von Analytics verwendete Adobe Advertising-IDs](ids.md)
>* [JavaScript-Code für Analytics für Advertising](/help/integrations/analytics/javascript.md)
>* [Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising](data-variances.md)
>* [Adobe Advertising-Metriken in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Daten in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
