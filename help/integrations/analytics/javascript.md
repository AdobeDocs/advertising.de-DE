---
title: JavaScript-Code für  [!DNL Analytics for Advertising]
description: JavaScript-Code für  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 5d07300ab49b96daf392cb51f8936fa4c0cd20ce
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# JavaScript-Code für [!DNL Analytics for Advertising]

*Advertiser nur mit Advertising DSP*

Bei Advertising DSP verfolgt die [!DNL Analytics for Advertising] -Integration Durchsichts- und Clickthrough-Site-Interaktionen. Clickthrough-Besuche werden anhand des standardmäßigen Adobe Analytics-Codes auf Ihren Webseiten verfolgt. Der [!DNL Analytics]-Code erfasst die AMO-ID- und EF-ID-Parameter in der URL der Landingpage und verfolgt sie in ihrem jeweils reservierten [!DNL eVars]. Sie können Durchsichtsbesuche verfolgen, indem Sie ein JavaScript-Snippet in Ihren Webseiten bereitstellen.

Beim ersten Seitenaufruf eines Site-Besuchs prüft der Adobe Advertising JavaScript-Code, ob der Besucher zuvor eine Anzeige gesehen oder angeklickt hat. Wenn der Benutzer zuvor über einen Clickthrough auf die Site gelangt ist oder noch keine Anzeige gesehen hat, wird der Besucher ignoriert. Wenn der Besucher eine Anzeige gesehen hat und nicht über einen Clickthrough während des innerhalb von Adobe Advertising festgelegten [Klick-Lookback-Fensters](/help/integrations/analytics/prerequisites.md#lookback-a4adc) auf die Site gelangt ist, verwendet der Adobe Advertising JavaScript-Code a) den [Experience Cloud ID-Dienst](https://experienceleague.adobe.com/docs/id-service/using/home.html), um eine zusätzliche ID (`SDID`) zu generieren, oder b) verwendet die Adobe Experience Platform [!DNL Web SDK] `generateRandomID` -Methode, um einen `[!DNL StitchID]` zu generieren. Jede ID wird verwendet, um Daten von Adobe Advertising dem Adobe Analytics-Treffer des Besuchers zuzuordnen. Adobe Analytics fragt dann Adobe Advertising nach der AMO-ID und der EF-ID ab, die mit der Anzeigenbelichtung verknüpft sind. Die AMO-ID und EF-IDs werden dann in ihre jeweiligen [!DNL eVars] eingetragen. Diese Werte bleiben für einen bestimmten Zeitraum bestehen (standardmäßig 60 Tage).

[!DNL Analytics] sendet Site-Traffic-Metriken (z. B. Seitenansichten, Besuche und Besuchszeit) und alle [!DNL Analytics] benutzerspezifischen oder standardmäßigen Ereignisse stündlich an die Adobe Advertising, wobei die EF-ID als Schlüssel verwendet wird. Diese [!DNL Analytics] -Metriken werden dann über das Adobe Advertising-Attributionssystem ausgeführt, um die Konversionen mit dem Klick- und Belichtungsverlauf zu verbinden.

>[!NOTE]
>
>Die Adobe Advertising JavaScript-Tracking-Logik findet auf der Adobe-Seite statt und hat daher praktisch keine Auswirkungen auf die Seitenladezeit.
>
>Im Gegensatz dazu tritt die Logik für den [!DNL DCM]-Data Connector zu [!DNL Analytics] (unter Verwendung von [!DNL Google Campaign Manager 360]) für Advertising DSP clientseitig auf. Die clientseitige Zuordnung verlangsamt das Laden der Seite und erhöht das Risiko eines Datenverlusts. Dies geschieht, weil der [!DNL Analytics] JavaScript [!DNL DoubleClick] pingen und warten muss, bis [!DNL DoubleClick] die letzten Klick-/Impressionsdaten an [!DNL Analytics] zurückgibt. Wenn Ihr [!DNL DSP]-Team den [!DNL DCM]-Data Connector eingerichtet hat, müssen Sie angeben, wie lange Sie die Seite verzögern möchten.

<!--
## Deploying the JavaScript Code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The Standard Code

The standard JavaScript library consists of two lines that allow [!DNL Analytics] and Adobe Advertising to communicate with each other. If the [!DNL Analytics for Advertising] integration was completed during the Adobe Advertising implementation, then you should have already received this code with instructions on how to deploy it.

#### Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code

### Additional Code to Import First-Party Segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5’s technical team will provide a unique tag for your organization to implement on your webpages.
-->

## Bereitstellen des JavaScript-Codes

Die JavaScript-Bibliothek besteht aus zwei Zeilen, die es [!DNL Analytics] und Adobe Advertising ermöglichen, miteinander zu kommunizieren. Wenn die [!DNL Analytics for Advertising] -Integration während der Adobe Advertising-Implementierung abgeschlossen wurde, sollten Sie diesen Code bereits mit Anweisungen zur Bereitstellung erhalten haben.

### Der Code

#### Implementierungen, die den Code des Experience Cloud Identity Service `visitorAPI.js` verwenden

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementierungen, die den Experience Platform [!DNL Web SDK] `alloy.js`code verwenden

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### Speicherort des Codes

Die Funktion &quot;[!DNL Analytics for Advertising] JavaScript&quot;muss nach dem Experience Cloud ID-Dienst, jedoch vor Ihrem Analytics-App-Measurement-Code stehen. Dadurch wird sichergestellt, dass die zusätzliche ID (`SDID`) oder `[!DNL StitchID]` in Ihrem Analytics-Aufruf enthalten ist.

![Codeplatzierung](/help/integrations/assets/a4adc-code-placement.png)

### Validieren der Codebereitstellung

Sie können eine Validierung mit einem beliebigen Paket-Sniffer-Typ von Tool durchführen (z. B. [!DNL Charles], [!DNL Fiddler] oder [!DNL Chrome Developer Tools]), indem Sie die Werte der vier IDs zwischen der Anfrage an Adobe Advertising und der Anfrage an [!DNL Analytics] vergleichen, wie unten beschrieben.

#### So bestätigen Sie den Code mit [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Öffnen Sie [!DNL Chrome Developer Tools] und klicken Sie auf die Registerkarte **Netzwerk** .

1. Laden Sie eine Website-Seite mit dem JavaScript &quot;[!DNL Analytics for Advertising]&quot;.

1. Filtern Sie die Registerkarte [!UICONTROL Network] nach `last` und überprüfen Sie zwei Zeilen:

   ![Filtern beim letzten](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * Die erste Zeile ist der Aufruf der JavaScript-Bibliothek mit dem Titel `last-event-tag-latest.min.js`.
   * Die zweite Zeile ist der Aufruf, der die Anfrage an Adobe Advertising sendet. Er beginnt wie folgt: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     Wenn Sie den Aufruf zum Adobe Advertising nicht sehen, ist dies möglicherweise nicht der erste Seitenaufruf Ihres Besuchs. Zu Testzwecken können Sie das Cookie entfernen, sodass der nächste Aufruf der erste Seitenaufruf für den entsprechenden Besuch ist:

   1. Suchen Sie auf der Registerkarte &quot;Anwendung&quot;das Cookie &quot;`adcloud`&quot;und stellen Sie sicher, dass das Cookie &quot;`_les_v`&quot;(letzter Besuch) mit dem Wert &quot;`y`&quot;und einem Zeitstempel für die UTC-Epoche enthält, der nach 30 Minuten abläuft.
      1. Löschen Sie das Cookie `adcloud` und aktualisieren Sie die Seite.

1. (Implementierungen, die den Code des Experience Cloud Identity Service `visitorAPI.js` verwenden) Filtern Sie nach `/b/ss`, um den Analytics-Treffer anzuzeigen.

   ![Filtern auf `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementierungen, die den Experience Platform [!DNL Web SDK] `alloy.js`code verwenden) Filtern Sie nach `/interact`, um sicherzustellen, dass die Anfrage-Payload zum Edge Network `advertisingStitchID` enthält.

   ![Filtern auf `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Vergleichen Sie die ID-Werte zwischen den beiden Treffern. Alle Werte sollten in Abfragezeichenfolgenparametern enthalten sein, mit Ausnahme der Report Suite-ID im Analytics-Treffer, der der URL-Pfad unmittelbar nach `/b/ss/` ist.

   | ID | Analytics-Parameter | Edge Network | Adobe Advertising-Parameter |
   | --- | --- | --- | --- |
   | Experience Cloud IMS-Organisation | `mcorgid` |  | `_les_imsOrgid` |
   | Zusätzliche Daten-ID | sdid |  | `_les_sdid` |
   | Zuordnungs-ID | stitchId | `advertisingStitchID` unter der Eigenschaft `_adcloud` |  |
   | Analytics Report Suite | Der Wert nach `/b/ss/` | | `_les_rsid` |
   | Experience Cloud-Besucher-ID | mid |  | `_les_mid` |

   Wenn die ID-Werte übereinstimmen, wird die JavaScript-Implementierung bestätigt. Adobe Advertising sendet dem [!DNL Analytics] -Server alle Clickthrough- oder Durchsichts-Tracking-Details, sofern vorhanden.

#### So bestätigen Sie den Code mit [!DNL Adobe Experience Cloud Debugger]

1. Öffnen Sie die [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) auf Ihrer Homepage.
1. Navigieren Sie zur Registerkarte [!UICONTROL Network] .
1. Klicken Sie in der Symbolleiste [!UICONTROL Solutions Filter] auf [!UICONTROL Adobe Advertising] und [!UICONTROL Analytics].
1. Suchen Sie in der Parameterzeile [!UICONTROL Request URL - Hostname] nach `lasteventf-tm.everesttech.net`.
1. Prüfen Sie in der Zeile [!UICONTROL Request - Parameters] die erzeugten Signale, ähnlich wie in Schritt 3 unter &quot;[So bestätigen Sie den Code mit  [!DNL Chrome Developer Tools]](#validate-js-chrome)&quot;.
   * (Implementierungen, die den Code des Experience Cloud Identity Service `visitorAPI.js` verwenden) Stellen Sie sicher, dass der Parameter `Sdid` mit dem Parameter `Supplemental Data ID` im Adobe Analytics-Filter übereinstimmt.
   * (Implementierungen, die den Experience Platform [!DNL Web SDK] `alloy.js`code verwenden) Stellen Sie sicher, dass der Wert des Parameters `advertisingStitchID` mit dem an das Experience Platform-Edge Network gesendeten `Sdid` übereinstimmt.
   * Wenn der Code nicht generiert wird, überprüfen Sie, ob das Adobe Advertising-Cookie auf der Registerkarte [!UICONTROL Application] entfernt wurde. Nachdem sie entfernt wurde, aktualisieren Sie die Seite und wiederholen Sie den Vorgang.

   ![Auditing [!DNL Analytics for Advertising] JavaScript-Code in [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Überblick über  [!DNL Analytics for Advertising]](overview.md)
>* [Voraussetzungen und wichtige Informationen für die Implementierung [!DNL Analytics for Advertising]](prerequisites.md)
