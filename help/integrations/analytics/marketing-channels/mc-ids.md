---
title: Verwenden von Adobe Advertising-IDs zum Erstellen  [!DNL Marketing Channels]  Regeln
description: Erfahren Sie, wie Sie Adobe Advertising-IDs verwenden, um Verarbeitungsregeln für zu erstellen [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 96a0add168c7fb7a6d80cf1b81ef4b315fbba89f
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Verwenden von Adobe Advertising-IDs zum Erstellen [!DNL Marketing Channels] Verarbeitungsregeln

*Nur Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

Sie können Adobe Advertising-IDs ([AMO-ID und EF-ID](../ids.md)) verwenden, um [!DNL Marketing Channels] Verarbeitungsregeln in Adobe Analytics zu konfigurieren. Verwenden Sie Adobe Advertising-IDs für Regeln, die speziell für Ihre Adobe Advertising-Kampagnen gelten.

## Die AMO-ID in Verarbeitungsregeln

Die AMO-ID ist der primäre Trackingcode, mit dem Adobe Advertising-Daten in [!DNL Analytics] gemeldet werden. Die AMO-ID ist eine Verkettung dynamischer Werte, die von Adobe verwaltet werden, um innerhalb von [!DNL Analytics] ein granulares Reporting zu ermöglichen. Er wird in einer [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) oder rVar-Dimension (AMO-ID) gespeichert. Die AMO-ID kann auf zwei Arten in [!DNL Analytics] festgelegt werden:

* Clickthrough-Tracking: Adobe Advertising legt den Parameter der `s_kwcid` Abfragezeichenfolge in einem Link fest und [!DNL Analytics] nimmt den Parameter bei einem Clickthrough von der Landingpage-URL auf.
* View-Through-Tracking (nur [!DNL DSP]): Der Last Event Service erkennt eine View-Through auf der Server-Seite und sendet die AMO-ID an [!DNL Analytics]. In diesem Fall enthält die URL keinen `s_kwcid`.

Die dynamischen Werte in AMO-IDs geben den verfolgten Marketing-Kanal an:

* Das Präfix in der AMO-ID kann verwendet werden, um den Kanal der obersten Ebene in [!DNL Marketing Channels] zu identifizieren.

* Zeichensätze im Hauptteil der AMO-ID weisen auf einen spezifischeren Kampagnentyp hin.

* Das Suffix „vt“ ist für [!DNL DSP] View-Through-Traffic vorhanden und kann verwendet werden, um separate Click-Through- und View-Through-[!DNL DSP] zu erstellen.

Der Rest der AMO-ID kann ignoriert werden.

| [!UICONTROL AMO ID] | Kanal | Regellogik |
|--------|---------|--------------------|
| !ctv (Suffix) | [!UICONTROL DSP Connected TV View-through] | Endet mit |
| !D! (Hauptteil) | [!UICONTROL Display Network] | CONTAINS |
| !G! (Hauptteil) | [!UICONTROL Google Search] | CONTAINS |
| !s! (Hauptteil) | [!UICONTROL Search Partner] | CONTAINS |
| !u! (Hauptteil) | [!UICONTROL Smart Shopping Campaign] | CONTAINS |
| !ytv! (Hauptteil) | [!UICONTROL YouTube Video Ad] | CONTAINS |
| !ja! (Hauptteil) | [!UICONTROL YouTube Search Ad] | CONTAINS |
| !VP! (Hauptteil) | [!UICONTROL Google Video Partners] | CONTAINS |
| !VT (Suffix) | [!UICONTROL DSP View-through] | Endet mit |
| AL! (Präfix) | [!UICONTROL Paid Search] | Beginnt mit |
| AC! (Präfix) | [!UICONTROL DSP] | Beginnt mit |

### Beispiele für Verarbeitungsregeln, die die AMO-ID verwenden

Die [!DNL Marketing Channels] Verarbeitungsregel für den [!UICONTROL Paid Search]-Kanal könnte wie folgt aussehen:

![Beispiel einer [!UICONTROL Paid Search] Regel](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

Die [!DNL Marketing Channels] Verarbeitungsregel für den [!UICONTROL YouTube Video Ads]-Kanal könnte wie folgt aussehen:

![Beispiel einer [!UICONTROL YouTube Video Ads] Regel](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Achten Sie darauf, Ihre Regeln in der Reihenfolge ihrer Spezifität auszuführen. Wenn die beiden oben genannten Regeln nacheinander ausgeführt werden, würde der gesamte [!DNL YouTube] Video-Werbe-Traffic unter den [!UICONTROL Paid Search]-Kanal fallen, da die AMO-ID beide mit „AL!“ beginnen würde. und &quot;!ytv!“ enthalten.

## Die EF-ID in Verarbeitungsregeln

Die AMO EF ID (EF ID) ist der zweite Trackingcode, der in der [!DNL Analytics for Advertising]-Integration verwendet wird. Ihr Hauptzweck besteht darin, [!DNL Analytics] Ereignisdaten zu verfolgen und an Adobe Advertising weiterzugeben. Jedes Mal, wenn ein Clickthrough oder eine Durchsicht erfolgt, wird eine eindeutige EF-ID generiert, auch wenn es sich um dieselbe Anzeige für denselben Besucher handelt. Die EF-ID wird in der Benutzeroberfläche für die [!DNL Analytics]-Berichterstellung nicht verwendet, da sie in der Regel die 500.000 eindeutigen Werte pro Variablenlimit in [!DNL Analytics] überschreitet, was sie für das Reporting unbrauchbar macht. Die Adobe Advertising-Metriken und Metadaten werden nicht auf die EF-ID angewendet, sondern nur auf die AMO-ID. Die zusätzliche Granularität des Trackings ist für die Kampagnenoptimierung in Adobe Advertising erforderlich, sodass beide IDs erforderlich sind.

Obwohl die EF ID-Dimension nicht direkt im [!DNL Analytics]-Reporting verwendet wird, kann die EF ID beim Erstellen von Marketing-Kanälen nützlich sein. Das EF-ID-Suffix gibt den Kanal (Anzeige oder Suche) an und ob der Besuch durch einen Clickthrough oder einen View-Through gesteuert wurde. Das Trennzeichen in der EF-ID ist ein Doppelpunkt und nicht das Ausrufezeichen in der AMO-ID.

| EF-ID-Suffix | Kanal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Beispiele für Verarbeitungsregeln, die die EF-ID verwenden

#### Clickthrough-Regel anzeigen

Erstellen Sie einen Display-Clickthrough-Marketing-Kanal, indem Sie nur Clickthroughs erfassen. Da die AMO-ID sowohl für Clickthroughs als auch für View-throughs identisch ist, verwendet diese Regel die EF ID-Variable und den `ef_id` Abfragezeichenfolgenparameter.

Manchmal werden Clickthroughs über die URL verfolgt (die Standardeinstellung). In anderen Fällen werden Clickthroughs über den Last Event Service auf der Server-Seite verfolgt, daher enthält die URL den `ef_id` nicht. Die Regel sucht daher nach Bedingungen, bei denen die EF-ID-Variable oder der `ef_id` Abfragezeichenfolgenparameter mit &quot;:d“ endet. Verwenden Sie den Operator &quot;`Any`&quot;, da diese Regel für jede Bedingung ausgelöst werden soll.

![Beispiel einer Clickthrough-Regel für die Anzeige](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Durchsichtsregel anzeigen

Um einen Viewthrough-Kanal für die Anzeige zu erstellen, erstellen Sie eine Regel, in der die EF-ID mit &quot;:i“ endet. Da der Besucher nicht auf die Anzeige geklickt hat, enthält das View-Through-Tracking nicht die `ef_id` oder `s_kwcid` in der URL, sodass für die Regel nur eine Bedingung erforderlich ist.

![Beispiel für eine Durchsichtsregel für die Anzeige](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Grundlagen von [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Warum Kanaldaten zwischen Adobe Advertising und variieren können [!DNL Marketing Channels]](mc-data-variances.md)
>* [Verwenden  [!DNL Analytics Marketing Channels]  Adobe Advertising-Daten](mc-ac-data.md)
>* [Video: Verwenden von  [!DNL Marketing Channels]  für das Adobe Advertising-Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Adobe Advertising-IDs verwendet von [!DNL Analytics]](/help/integrations/analytics/ids.md)
