---
title: Verwenden von Adobe Advertising-IDs zum Erstellen von [!DNL Marketing Channels] Regeln
description: Erfahren Sie, wie Sie mit Adobe Advertising-IDs Verarbeitungsregeln für [!DNL Analytics Marketing Channels] erstellen.
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Verwenden von Adobe Advertising-IDs zum Erstellen von [!DNL Marketing Channels] Verarbeitungsregeln

*Advertiser mit nur einer Adobe Advertising-Adobe Analytics-Integration*

Sie können Adobe Advertising-IDs ([AMO-ID und EF ID](../ids.md)) verwenden, um [!DNL Marketing Channels] Verarbeitungsregeln in Adobe Analytics zu konfigurieren. Verwenden Sie Adobe Advertising-IDs für Adobe Advertising-Kampagnen-spezifische Regeln.

## AMO-ID in Verarbeitungsregeln

Die AMO-ID ist der primäre Trackingcode, mit dem Adobe Advertising-Daten innerhalb von [!DNL Analytics] gemeldet werden. Die AMO-ID ist eine Verkettung von dynamischen Werten, die von Adobe verwaltet werden, um detaillierte Berichte innerhalb von [!DNL Analytics] bereitzustellen. Er wird in einer [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) - oder rVar -Dimension (AMO-ID) gespeichert. Die AMO-ID kann auf zwei Arten in [!DNL Analytics] festgelegt werden:

* Clickthrough-Tracking: Adobe Advertising legt den Abfragezeichenfolgenparameter `s_kwcid` in einem Link fest und [!DNL Analytics] übernimmt den Parameter aus der Landingpage-URL, wenn ein Clickthrough erfolgt.
* Durchsichtsverfolgung ([!DNL DSP] Nur): Der letzte Ereignisdienst erkennt eine Durchsicht auf dem Server und sendet die AMO-ID an [!DNL Analytics]. In diesem Fall enthält die URL keinen Parameter `s_kwcid` .

Die dynamischen Werte innerhalb von AMO-IDs geben den verfolgten Marketing-Kanal an:

* Das Präfix in der AMO-ID kann verwendet werden, um den Kanal der obersten Ebene innerhalb von [!DNL Marketing Channels] zu identifizieren.

* Zeichensätze im Hauptteil der AMO-ID weisen auf einen spezifischeren Kampagnentyp hin.

* Das Suffix &quot;vt&quot;ist für [!DNL DSP] Durchsichts-Traffic vorhanden und kann zum Erstellen separater Clickthrough- und Durchsichtskanäle [!DNL DSP] verwendet werden.

Der Rest der AMO-ID kann ignoriert werden.

| [!UICONTROL AMO ID] | Kanal | Regellogik |
|--------|---------|--------------------|
| AL! (Präfix) | [!UICONTROL Paid Search] | Beginnt mit |
| AC! (Präfix) | [!UICONTROL DSP] | Beginnt mit |
| !g! (Hauptteil) | [!UICONTROL Google Search] | Enthält |
| !s! (Hauptteil) | [!UICONTROL Search Partner] | Enthält |
| !d! (Hauptteil) | [!UICONTROL Display Network] | Enthält |
| !u! (Hauptteil) | [!UICONTROL Smart Shopping Campaign] | Enthält |
| !ytv! (Hauptteil) | [!UICONTROL YouTube Video Ad] | Enthält |
| !yts! (Hauptteil) | [!UICONTROL YouTube Search Ad] | Enthält |
| !vp! (Hauptteil) | [!UICONTROL Google Video Partners] | Enthält |
| !vt (Suffix) | [!UICONTROL DSP View-through] | Endet in |

### Beispiele für Verarbeitungsregeln, die die AMO-ID verwenden

Die [!DNL Marketing Channels]-Verarbeitungsregel für den Kanal [!UICONTROL Paid Search] könnte wie folgt aussehen:

![Beispiel einer [!UICONTROL Paid Search] Regel](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

Die [!DNL Marketing Channels]-Verarbeitungsregel für den Kanal [!UICONTROL YouTube Video Ads] könnte wie folgt aussehen:

![Beispiel einer [!UICONTROL YouTube Video Ads] Regel](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Stellen Sie sicher, dass Sie Ihre Regeln in der richtigen Reihenfolge ausführen. Wenn die beiden oben genannten Regeln in der richtigen Reihenfolge ausgeführt werden, würde der [!DNL YouTube]-Videoanzeigen-Traffic alle unter den [!UICONTROL Paid Search] -Kanal fallen, da die AMO-ID beide mit &quot;AL!&quot;beginnt. und enthalten &quot;!ytv!&quot;.

## Die EF ID in den Verarbeitungsregeln

Die AMO EF ID (EF ID) ist der zweite Trackingcode, der in der [!DNL Analytics for Advertising] -Integration verwendet wird. Ihr Hauptzweck besteht darin, [!DNL Analytics] -Ereignisdaten zu verfolgen und an Adobe Advertising weiterzugeben. Jedes Mal, wenn ein Clickthrough oder eine Durchsicht erfolgt, wird eine eindeutige EF-ID generiert, auch wenn es sich um genau dieselbe Anzeige für denselben Besucher handelt. Die EF ID wird in der Berichterstellungsbenutzeroberfläche von [!DNL Analytics] nicht verwendet, da sie normalerweise die 500.000 individuellen Werte pro Variablenbegrenzung in [!DNL Analytics] überschreitet, wodurch sie für Berichte unbrauchbar wird. Die Adobe Advertising-Metriken und Metadaten werden nicht auf die EF ID angewendet, sondern nur auf die AMO-ID. Die zusätzliche Granularität des Trackings ist für die Kampagnenoptimierung im Adobe Advertising erforderlich, sodass beide IDs erforderlich sind.

Obwohl die EF ID-Dimension nicht direkt in [!DNL Analytics] -Berichten verwendet wird, kann die EF ID bei der Erstellung von Marketing-Kanälen hilfreich sein. Das EF ID-Suffix zeigt den Kanal (Anzeige oder Suche) an und ob der Besuch durch einen Clickthrough oder eine Durchsicht gesteuert wurde. Das Trennzeichen in der EF ID ist ein Doppelpunkt und nicht der Ausrufezeichen in der AMO-ID.

| EF ID Suffix | Kanal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Beispiele für Verarbeitungsregeln, die die EF ID verwenden

#### Clickthrough-Regel anzeigen

Erstellen Sie einen Display-Clickthrough-Marketing-Kanal, indem Sie nur Clickthroughs erfassen. Da die AMO-ID für Clickthroughs und Durchsichten gleich ist, verwendet diese Regel die EF ID-Variable und den `ef_id`-Abfragezeichenfolgenparameter.

Manchmal werden Clickthroughs über die URL verfolgt (Standard). In anderen Fällen werden Clickthroughs über den letzten Ereignisdienst auf der Serverseite verfolgt, weshalb die URL nicht den Parameter `ef_id` enthält. Die Regel sucht daher nach Bedingungen, in denen die EF ID-Variable oder der `ef_id`-Abfragezeichenfolgenparameter mit &quot;:d&quot;endet. Verwenden Sie den Operator &quot;`Any`&quot;, da diese Regel für beide Bedingungen ausgelöst werden soll.

![Beispiel einer Anzeige-Clickthrough-Regel](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Durchsichtsregel anzeigen

Um einen Durchsichtskanal für die Anzeige zu erstellen, erstellen Sie eine Regel, in der die EF-ID mit &quot;:i&quot;endet. Da der Besucher nicht auf die Anzeige geklickt hat, enthält das Durchsichts-Tracking nicht die `ef_id` oder `s_kwcid` in der URL, sodass die Regel nur eine Bedingung erfordert.

![Beispiel einer Durchsichtsregel für die Anzeige](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Grundlagen von  [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Warum Kanaldaten zwischen Adobe Advertising und  [!DNL Marketing Channels]](mc-data-variances.md) variieren können
>* [Verwenden von  [!DNL Analytics Marketing Channels] mit Adobe Advertising-Daten](mc-ac-data.md)
>* [Video: Verwendung von [!DNL Marketing Channels] für Adobe Advertising-Berichterstellung](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Von  [!DNL Analytics]](/help/integrations/analytics/ids.md) verwendete Adobe Advertising-IDs
