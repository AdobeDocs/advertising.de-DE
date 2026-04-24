---
title: JavaScript-Code für [!DNL Analytics for Advertising]
description: JavaScript-Code für [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
TQID: https://experienceleague.adobe.com/g9onwe1IQl1kbyQ82W2KmODPGUAReKiotxy65yCZcNY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 941
ht-degree: 0%

---

# JavaScript-Code für [!DNL Analytics for Advertising]

*Nur Werbetreibende mit Advertising DSP*

Bei Advertising DSP verfolgt die [!DNL Analytics for Advertising]-Integration Site-Interaktionen mit Ansichts- und Clickthrough. Clickthrough-Besuche werden vom Standard-Adobe Analytics-Code auf Ihren Web-Seiten verfolgt; der [!DNL Analytics] erfasst die AMO-ID- und EF-ID-Parameter in der Landingpage-URL und verfolgt sie in ihren jeweiligen reservierten [!DNL eVars]. Sie können Viewthrough-Besuche verfolgen, indem Sie ein JavaScript-Snippet auf Ihren Web-Seiten bereitstellen.

Bei der ersten Seitenansicht eines Besuchs auf der Website prüft der Adobe Advertising JavaScript-Code, ob der Besucher eine Anzeige bereits gesehen oder darauf geklickt hat. Wenn der/die Benutzende die Website zuvor über einen Clickthrough betreten hat oder keine Anzeige gesehen hat, wird der/die Besuchende ignoriert. Wenn der Besucher eine Anzeige gesehen hat und während des in Adobe Advertising festgelegten [Klick-Lookback-Fensters](/help/integrations/analytics/prerequisites.md#lookback-a4adc) nicht über einen Clickthrough auf die Website zugegriffen hat, verwendet der Adobe Advertising-JavaScript-Code entweder a) den [Experience Cloud ID-Service](https://experienceleague.adobe.com/docs/id-service/using/home.html), um eine zusätzliche ID zu generieren (`SDID`), oder b) die Adobe Experience Platform-[!DNL Web SDK]-`generateRandomID`-Methode, um eine `[!DNL StitchID]` zu generieren. Beide IDs werden verwendet, um Daten aus Adobe Advertising mit dem Adobe Analytics-Treffer des Besuchers zusammenzufügen. Adobe Analytics fragt dann in Adobe Advertising die AMO-ID und die EF-ID ab, die mit der Anzeigenbelichtung verbunden sind. Die AMO-ID und die EF-IDs werden dann in den entsprechenden [!DNL eVars] ausgefüllt. Diese Werte bleiben für einen bestimmten Zeitraum erhalten (standardmäßig 60 Tage).

[!DNL Analytics] sendet stündlich Traffic-Metriken (z. B. Seitenansichten, Besuche und Besuchszeit) sowie alle [!DNL Analytics] benutzerdefinierten oder Standardereignisse an Adobe Advertising. Dabei wird die EF-ID als Schlüssel verwendet. Diese [!DNL Analytics] Metriken laufen dann durch das Adobe Advertising-Attributionssystem, um die Konversionen mit dem Klick- und Belichtungsverlauf zu verbinden.

>[!NOTE]
>
>Die Adobe Advertising JavaScript-Tracking-Logik findet auf der Adobe-Seite statt und hat daher praktisch keine Auswirkungen auf die Seitenladezeit.
>
>Dagegen erfolgt die Logik für die [!DNL Analytics] des [!DNL DCM] Data Connectors (mithilfe von [!DNL Google Campaign Manager 360]) für Advertising DSP Client-seitig. Client-seitiges Stitching verlangsamt das Laden der Seite und erhöht das Risiko von Datenverlust. Dies tritt auf, weil der [!DNL Analytics] JavaScript einen Ping-[!DNL DoubleClick] durchführen muss und darauf warten muss, dass [!DNL DoubleClick] die Daten des letzten Klicks/der letzten Impression an [!DNL Analytics] zurückgibt. Wenn Ihr [!DNL DSP]-Team den [!DNL DCM] Data Connector einrichtet, müssen Sie angeben, wie lange Sie die Seite verzögern möchten.

<!--
## Deploying the JavaScript code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The standard code

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

### Additional code to import first-party segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5's technical team will provide a unique tag for your organization to implement on your webpages.
-->

## Bereitstellen des JavaScript-Codes

Die JavaScript-Bibliothek besteht aus zwei Zeilen, die es [!DNL Analytics] und Adobe Advertising ermöglichen, miteinander zu kommunizieren. If the [!DNL Analytics for Advertising] integration was completed during the Adobe Advertising implementation, then you should have already received this code with instructions on how to deploy it.

### The code

#### Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### Where to place the code

The [!DNL Analytics for Advertising] JavaScript function must come after the Experience Cloud ID Service but before your Analytics App Measurement code. This ensures that the supplemental ID (`SDID`) or `[!DNL StitchID]` is included in your Analytics call.

![Code placement](/help/integrations/assets/a4adc-code-placement.png)

### Validating code deployment

You can perform validation using any packet sniffer type of tool (such as [!DNL Charles], [!DNL Fiddler], or [!DNL Chrome Developer Tools]) by comparing the values of the four IDs between the request going to Adobe Advertising and the request going to [!DNL Analytics], as outlined below.

#### How to confirm the code with [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Open [!DNL Chrome Developer Tools] and click the **Network** tab.

1. Load a website page that contains the [!DNL Analytics for Advertising] JavaScript.

1. Filter the [!UICONTROL Network] tab by `last` and review two rows:

   ![Filtering on last](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * The first row is the call to the JavaScript library and is titled `last-event-tag-latest.min.js`.
   * The second row is the call sending the request to Adobe Advertising. It begins as follows: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     If you don&#39;t see the call to Adobe Advertising, then it might not be the first page view of your visit. For testing purposes, you can remove the cookie so that the next call is the first page view for the corresponding visit:

   1. On the Application tab, find the `adcloud` cookie, and verify that the cookie contains `_les_v` (last visit) with a value of `y` and a UTC epoch timestamp that expires in 30 minutes.
      1. Delete the `adcloud` cookie and refresh the page.

1. (Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code) Filter on `/b/ss` to see the Analytics hit.

   ![Filtering on `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code) Filter on `/interact` to verify that the request payload to the Edge Network contains `advertisingStitchID`.

   ![Filtern nach `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Vergleichen Sie die ID-Werte zwischen den beiden Treffern. Alle Werte sollten in Abfragezeichenfolgenparametern angegeben werden, mit Ausnahme der Report Suite-ID im Analytics-Treffer, bei der es sich um den URL-Pfad unmittelbar nach der `/b/ss/` handelt.

   | ID | Analytics-Parameter | Edge Network | Adobe Advertising-Parameter |
   | --- | --- | --- | --- |
   | Experience Cloud IMS Org | `mcorgid` |  | `_les_imsOrgid` |
   | Zusatzdaten-ID | sdid |  | `_les_sdid` |
   | Zuordnungs-ID | stitchId | `advertisingStitchID` unter der `_adcloud` |  |
   | Analytics Report Suite | Der Wert nach `/b/ss/` | | `_les_rsid` |
   | Experience Cloud-Besucher-ID | Mitte |  | `_les_mid` |

   Wenn die ID-Werte übereinstimmen, wird die JavaScript-Implementierung bestätigt. Adobe Advertising sendet dem [!DNL Analytics] alle Clickthrough- oder View-Through-Tracking-Details, sofern vorhanden.

#### Bestätigen des Codes mit [!DNL Adobe Experience Platform Debugger]

1. Öffnen Sie [die [!DNL Adobe Experience Platform Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) auf Ihrer Homepage.
1. Wechseln Sie zur Registerkarte [!UICONTROL Network] .
1. Klicken Sie in der [!UICONTROL Solutions Filter]-Symbolleiste auf [!UICONTROL Adobe Advertising] und [!UICONTROL Analytics] Sie.
1. Suchen Sie in der [!UICONTROL Request URL - Hostname] Parameterzeile nach `lasteventf-tm.everesttech.net`.
1. Überprüfen Sie in der [!UICONTROL Request - Parameters] Zeile die generierten Signale, ähnlich wie in Schritt 3 unter &quot;[ zum Bestätigen des Codes mit [!DNL Chrome Developer Tools]](#validate-js-chrome).
   * (Implementierungen, die den `visitorAPI.js`-Code des Experience Cloud Identity Services verwenden) Stellen Sie sicher, dass der `Sdid` mit dem `Supplemental Data ID` im Adobe Analytics-Filter übereinstimmt.
   * (Implementierungen, die den Experience Platform-[!DNL Web SDK] verwenden `alloy.js`Code) Stellen Sie sicher, dass der Wert des `advertisingStitchID`-Parameters mit dem an Experience Platform Edge Network gesendeten `Sdid` übereinstimmt.
   * Wenn der Code nicht generiert wird, überprüfen Sie, ob das Adobe Advertising-Cookie auf der Registerkarte &quot;[!UICONTROL Application]&quot; entfernt wurde. Aktualisieren Sie die Seite nach dem Entfernen und wiederholen Sie den Vorgang.

   ![Auditing [!DNL Analytics for Advertising] JavaScript-Codes in [!DNL Platform Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Überblick über [!DNL Analytics for Advertising]](overview.md)
>* [Voraussetzungen und wichtige Informationen für die Implementierung [!DNL Analytics for Advertising]](prerequisites.md)
