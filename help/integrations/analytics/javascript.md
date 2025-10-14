---
title: JavaScript-Code für [!DNL Analytics for Advertising]
description: JavaScript-Code für [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 5d07300ab49b96daf392cb51f8936fa4c0cd20ce
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# JavaScript-Code für [!DNL Analytics for Advertising]

*Nur Werbetreibende mit Advertising DSP*

Bei Advertising DSP verfolgt die [!DNL Analytics for Advertising]-Integration Site-Interaktionen mit Ansichts- und Clickthrough. Clickthrough-Besuche werden vom Standard-Adobe Analytics-Code auf Ihren Web-Seiten verfolgt; der [!DNL Analytics] erfasst die AMO-ID- und EF-ID-Parameter in der Landingpage-URL und verfolgt sie in ihren jeweiligen reservierten [!DNL eVars]. Sie können Viewthrough-Besuche verfolgen, indem Sie ein JavaScript-Snippet auf Ihren Web-Seiten bereitstellen.

Bei der ersten Seitenansicht eines Besuchs auf der Website prüft der Adobe Advertising-JavaScript-Code, ob der Besucher eine Anzeige bereits gesehen oder darauf geklickt hat. Wenn der/die Benutzende die Website zuvor über einen Clickthrough betreten hat oder keine Anzeige gesehen hat, wird der/die Besuchende ignoriert. Wenn der Besucher eine Anzeige gesehen hat und während des in Adobe Advertising festgelegten [Klick-Lookback-Fensters](/help/integrations/analytics/prerequisites.md#lookback-a4adc) nicht über einen Clickthrough auf die Website zugegriffen hat, verwendet der Adobe Advertising-JavaScript-Code entweder a) den [Experience Cloud-ID-Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=de), um eine zusätzliche ID zu generieren (`SDID` [!DNL Web SDK]), oder b) verwendet die Adobe Experience Platform-`generateRandomID`-Methode, um eine `[!DNL StitchID]` zu generieren. Beide ID werden verwendet, um Daten vom Adobe Advertising mit dem Adobe Analytics-Treffer des Besuchers zu verknüpfen. Adobe Analytics fragt dann Adobe Advertising nach der AMO-ID und der EF-ID ab, die mit der Anzeigenbelichtung verbunden sind. Die AMO-ID und die EF-IDs werden dann in den entsprechenden [!DNL eVars] ausgefüllt. Diese Werte bleiben für einen bestimmten Zeitraum erhalten (standardmäßig 60 Tage).

[!DNL Analytics] sendet Website-Traffic-Metriken (z. B. Seitenansichten, Besuche und Besuchszeit) sowie alle [!DNL Analytics] benutzerdefinierten oder Standardereignisse stündlich an Adobe Advertising. Dabei wird die EF-ID als Schlüssel verwendet. Diese [!DNL Analytics] Metriken laufen dann durch das Adobe Advertising-Attributionssystem, um die Konversionen mit dem Klick- und Belichtungsverlauf zu verbinden.

>[!NOTE]
>
>Die Adobe Advertising-JavaScript-Trackinglogik erfolgt auf der Adobe-Seite und hat somit praktisch keinen Einfluss auf die Seitenladezeit.
>
>Dagegen erfolgt die Logik für die [!DNL Analytics] des [!DNL DCM] Data Connectors (mithilfe von [!DNL Google Campaign Manager 360]) für Advertising DSP Client-seitig. Client-seitiges Stitching verlangsamt das Laden der Seite und erhöht das Risiko von Datenverlust. Dies tritt auf, weil der [!DNL Analytics] JavaScript einen Ping-[!DNL DoubleClick] durchführen muss und darauf warten muss, dass [!DNL DoubleClick] die Daten des letzten Klicks/der letzten Impression an [!DNL Analytics] zurückgibt. Wenn Ihr [!DNL DSP]-Team den [!DNL DCM] Data Connector einrichtet, müssen Sie angeben, wie lange Sie die Seite verzögern möchten.

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

Die JavaScript-Bibliothek besteht aus zwei Zeilen, die es [!DNL Analytics] und Adobe Advertising ermöglichen, miteinander zu kommunizieren. Wenn die [!DNL Analytics for Advertising]-Integration während der Adobe Advertising-Implementierung abgeschlossen wurde, sollten Sie diesen Code bereits mit Anweisungen zur Bereitstellung erhalten haben.

### Der Code

#### Implementierungen, die den Experience Cloud Identity Service-`visitorAPI.js` verwenden

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementierungen, die den Experience Platform-[!DNL Web SDK] verwenden `alloy.js`code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### Wo der Code platziert werden soll

Die [!DNL Analytics for Advertising] JavaScript-Funktion muss hinter dem Experience Cloud-ID-Service, aber vor dem Messcode Ihrer Analytics-App stehen. Dadurch wird sichergestellt, dass die zusätzliche ID (`SDID`) oder `[!DNL StitchID]` in Ihrem Analytics-Aufruf enthalten ist.

![Code-Platzierung](/help/integrations/assets/a4adc-code-placement.png)

### Validieren der Code-Bereitstellung

Sie können die Validierung mit einem beliebigen Tool vom Typ „Paket-Sniffer“ (z. B. [!DNL Charles], [!DNL Fiddler] oder [!DNL Chrome Developer Tools]) durchführen, indem Sie die Werte der vier IDs zwischen der Anfrage, die an den Adobe Advertising gesendet wird, und der Anfrage, die an den [!DNL Analytics] gesendet wird, vergleichen, wie unten beschrieben.

#### Bestätigen des Codes mit [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Öffnen Sie [!DNL Chrome Developer Tools] und klicken Sie auf die **Netzwerk**.

1. Laden Sie eine Webseite, die die [!DNL Analytics for Advertising] JavaScript enthält.

1. Filtern Sie die Registerkarte [!UICONTROL Network] nach `last` und überprüfen Sie zwei Zeilen:

   ![Filtern am letzten](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * Die erste Zeile ist der Aufruf der JavaScript-Bibliothek und heißt `last-event-tag-latest.min.js`.
   * Die zweite Zeile ist der Aufruf zum Senden der Anfrage an Adobe Advertising. Sie beginnt wie folgt: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     Wenn Sie den Aufruf von Adobe Advertising nicht sehen, ist dies möglicherweise nicht die erste Seitenansicht Ihres Besuchs. Zu Testzwecken können Sie das Cookie entfernen, sodass der nächste Aufruf die erste Seitenansicht für den entsprechenden Besuch ist:

   1. Suchen Sie auf der Registerkarte Anwendung das `adcloud`-Cookie und stellen Sie sicher, dass das Cookie `_les_v` (letzten Besuch) mit dem Wert `y` und einem UTC-Epochenzeitstempel enthält, der in 30 Minuten abläuft.
      1. Löschen Sie das `adcloud`-Cookie und aktualisieren Sie die Seite.

1. (Implementierungen, die den Experience Cloud Identity Service-`visitorAPI.js` verwenden) Filtern Sie nach `/b/ss`, um den Analytics-Treffer anzuzeigen.

   ![Filtern nach `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementierungen, die den Experience Platform-Code verwenden[!DNL Web SDK] `alloy.js` Filtern nach `/interact`, um zu überprüfen, ob die Payload der Anfrage an das Edge Network `advertisingStitchID` enthält.

   ![Filtern nach `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Vergleichen Sie die ID-Werte zwischen den beiden Treffern. Alle Werte sollten in Abfragezeichenfolgenparametern angegeben werden, mit Ausnahme der Report Suite-ID im Analytics-Treffer, bei der es sich um den URL-Pfad unmittelbar nach der `/b/ss/` handelt.

   | ID | Analytics-Parameter | Edge Network | Adobe Advertising-Parameter |
   | --- | --- | --- | --- |
   | Experience Cloud IMS Org | `mcorgid` |  | `_les_imsOrgid` |
   | Zusatzdaten-ID | sdid |  | `_les_sdid` |
   | Zuordnungs-ID | stitchId | `advertisingStitchID` unter der `_adcloud` |  |
   | Analytics Report Suite | Der Wert nach `/b/ss/` | | `_les_rsid` |
   | Experience Cloud-Besucher-ID | Mitte |  | `_les_mid` |

   Wenn die ID-Werte übereinstimmen, wird die JavaScript-Implementierung bestätigt. Adobe Advertising sendet dem [!DNL Analytics] alle Clickthrough- oder View-Through-Tracking-Details, falls vorhanden.

#### Bestätigen des Codes mit [!DNL Adobe Experience Cloud Debugger]

1. Öffnen Sie die [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=de) auf Ihrer Homepage.
1. Wechseln Sie zur Registerkarte [!UICONTROL Network] .
1. Klicken Sie in der [!UICONTROL Solutions Filter]-Symbolleiste auf [!UICONTROL Adobe Advertising] und [!UICONTROL Analytics] Sie.
1. Suchen Sie in der [!UICONTROL Request URL - Hostname] Parameterzeile nach `lasteventf-tm.everesttech.net`.
1. Überprüfen Sie in der [!UICONTROL Request - Parameters] Zeile die generierten Signale, ähnlich wie in Schritt 3 unter &quot;[&#x200B; zum Bestätigen des Codes mit [!DNL Chrome Developer Tools]](#validate-js-chrome).
   * (Implementierungen, die den Experience Cloud Identity Service-`visitorAPI.js` verwenden) Stellen Sie sicher, dass der `Sdid` mit dem `Supplemental Data ID` im Adobe Analytics-Filter übereinstimmt.
   * (Implementierungen, die den Experience Platform-Code [!DNL Web SDK]`alloy.js`) Stellen Sie sicher, dass der Wert des `advertisingStitchID`-Parameters mit dem an das Experience Platform-Edge Network gesendeten `Sdid` übereinstimmt.
   * Wenn der Code nicht generiert wird, überprüfen Sie, ob das Adobe Advertising-Cookie auf der Registerkarte &quot;[!UICONTROL Application]&quot; entfernt wurde. Aktualisieren Sie die Seite nach dem Entfernen und wiederholen Sie den Vorgang.

   ![Auditing [!DNL Analytics for Advertising] JavaScript-Codes in [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Überblick über [!DNL Analytics for Advertising]](overview.md)
>* [Voraussetzungen und wichtige Informationen für die Implementierung [!DNL Analytics for Advertising]](prerequisites.md)
