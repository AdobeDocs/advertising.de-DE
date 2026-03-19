---
title: Verwenden von Adobe Advertising-IDs zum Erstellen  [!DNL Marketing Channels]  Regeln
description: Erfahren Sie, wie Sie mit Adobe Advertising IDs Verarbeitungsregeln für  [!DNL Analytics Marketing Channels] erstellen.
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 0813a8bddc1ecf238f4a62c4fcefd8584f32e152
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# Verwenden von Adobe Advertising-IDs zum Erstellen [!DNL Marketing Channels] Verarbeitungsregeln

*Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

Sie können Adobe Advertising-IDs ([AMO-ID und EF-ID](../ids.md)) verwenden, um [!DNL Marketing Channels] Verarbeitungsregeln in Adobe Analytics zu konfigurieren. Verwenden Sie Adobe Advertising-IDs für Regeln, die speziell für Ihre Adobe Advertising-Kampagnen gelten. Die Reihenfolge, in der Sie die Regeln verarbeiten, bestimmt, ob alle möglichen Daten korrekt erfasst werden.

## Die AMO-ID in Verarbeitungsregeln

Die AMO-ID ist der primäre Trackingcode, mit dem Adobe Advertising-Daten in [!DNL Analytics] gemeldet werden. Die AMO-ID ist eine Verkettung dynamischer Werte, die von Adobe verwaltet werden, um innerhalb von [!DNL Analytics] ein granulares Reporting zu ermöglichen. Sie wird in einer [!DNL Analytics] [eVar- oder rVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)Dimension (AMO-ID) gespeichert. Die AMO-ID kann auf zwei Arten in [!DNL Analytics] festgelegt werden:

* Clickthrough-Tracking: Adobe Advertising legt den `s_kwcid` Abfragezeichenfolgenparameter in einem Link fest und [!DNL Analytics] den Parameter bei einem Clickthrough von der Landingpage-URL ab.

* View-Through-Tracking (nur [!DNL DSP]): Das [!DNL Last Event Service] erkennt ein View-Through auf der Server-Seite und sendet die AMO-ID an [!DNL Analytics]. In diesem Fall enthält die URL keinen `s_kwcid`.

Die dynamischen Werte in AMO-IDs geben den verfolgten Marketing-Kanal an:

* Das Präfix in der AMO-ID kann verwendet werden, um den Kanal der obersten Ebene in [!DNL Marketing Channels] zu identifizieren.

* Zeichensätze im Hauptteil der AMO-ID weisen auf einen spezifischeren Kampagnentyp hin.

* Das Suffix „vt“ ist für [!DNL DSP] View-Through-Traffic vorhanden und kann verwendet werden, um separate Click-Through- und View-Through-[!DNL DSP] zu erstellen.

Der Rest der AMO-ID kann ignoriert werden.

| [!UICONTROL AMO ID] | Kanal | Regellogik |
|--------|---------|--------------------|
| !ctv (Suffix) | [!UICONTROL DSP Connected TV ViewThrough] | Endet mit |
| !D! (Hauptteil) | [!UICONTROL Display Network] | Enthält |
| !G! (Hauptteil) | [!UICONTROL Google Search] | Enthält |
| !s! (Hauptteil) | [!UICONTROL Search Partner] | Enthält |
| !u! (Hauptteil) | [!UICONTROL Smart Shopping Campaign] | Enthält |
| !ytv! (Hauptteil) | [!UICONTROL YouTube Video Ad] | Enthält |
| !ja! (Hauptteil) | [!UICONTROL YouTube Search Ad] | Enthält |
| !VP! (Hauptteil) | [!UICONTROL Google Video Partners] | Enthält |
| !VT (Suffix) | [!UICONTROL DSP ViewThrough] | Endet mit |
| AL! (Präfix) | [!UICONTROL Paid Search] | Beginnt mit |
| AC! (Präfix) | [!UICONTROL DSP Display] | Beginnt mit |

## Die EF-ID in Verarbeitungsregeln

Die AMO EF ID (EF ID) ist der zweite Trackingcode, der in der [!DNL Analytics for Advertising]-Integration verwendet wird. Ihr Hauptzweck besteht darin, [!DNL Analytics] Ereignisdaten zu verfolgen und an Adobe Advertising zu übergeben. Jedes Mal, wenn ein Clickthrough oder eine Durchsicht erfolgt, wird eine eindeutige EF-ID generiert, auch wenn es sich um dieselbe Anzeige für denselben Besucher handelt. Die EF-ID wird in der Benutzeroberfläche für die [!DNL Analytics]-Berichterstellung nicht verwendet, da sie in der Regel die 500.000 eindeutigen Werte pro Variablenlimit in [!DNL Analytics] überschreitet, was sie für das Reporting unbrauchbar macht. Die Adobe Advertising-Metriken und -Metadaten werden nicht auf die EF-ID angewendet, sondern nur auf die AMO-ID. Die zusätzliche Granularität des Trackings ist für die Kampagnenoptimierung in Adobe Advertising erforderlich, sodass beide IDs erforderlich sind.

Obwohl die EF ID-Dimension nicht direkt im [!DNL Analytics]-Reporting verwendet wird, kann die EF ID beim Erstellen von Marketing-Kanälen nützlich sein. Das EF-ID-Suffix gibt den Kanal (Anzeige oder Suche) an und ob der Besuch durch einen Clickthrough oder einen View-Through gesteuert wurde. Das Trennzeichen in der EF-ID ist ein Doppelpunkt und nicht das Ausrufezeichen in der AMO-ID.

| EF-ID-Suffix | Kanal |
|-------|---------|
| :s | [!UICONTROL Paid Search Click-through] |
| :d | [!UICONTROL Display ClickThrough] |
| :i | [!UICONTROL Display ViewThrough] |

## Beispiele für Verarbeitungsregeln für Adobe Advertising

Der folgende Beispielregelsatz konzentriert sich auf die Regeln für die Werbekanäle (Paid Search, Display ClickThrough und Display ViewThrough). Die empfohlene Regel für die Erkennung von Paid Search (einschließlich der Interaktion dieser Regel mit der Logik des organischen Such-Marketing-Kanals) und eine optionale Aktualisierung der Regel für natürliche verweisende Domains werden ebenfalls demonstriert.

**Hinweis:** Anzeige kann je nach Werbekunden-Vorlieben als zwei Kanäle aufgeteilt oder zu einem einzigen Kanal zusammengeführt werden.

Im Beispiel-Screenshot sind weitere Kanäle enthalten, um die empfohlene Reihenfolge der Vorgänge der Werbekanäle im Vergleich zu anderen Kanälen in einer typischen Implementierung zu veranschaulichen.

>[!IMPORTANT]
>
>Informationen [&#x200B; Reihenfolge, in der Ihre Regeln verarbeitet werden sollen [!DNL Marketing Channels]  finden Sie unter „Reihenfolge der Vorgänge für &#x200B;](#rule-order)-Regeln“.

![Beispiel für einen Satz von Verarbeitungsregeln](/help/integrations/assets/a4adc-mc-rule-set-example.png)

### Paid Search-Regel

Es empfiehlt sich, für eine [!UICONTROL Paid Search] Regel zwei Bedingungen mit dem Operator „any“ einzuschließen:

* Kosten-/Klick-/Impressionsdaten enthalten die AMO-ID. Fügen Sie daher die AMO-ID hinzu. Die AMO-ID sollte mit „AL!“ beginnen. So ordnen Sie [!UICONTROL Paid Search] die Klick-/Kosten-/Impressionsdaten korrekt zu.<!-- Is this just called AMO ID there, not s_kwcid=XXX? What's the difference? -->

* Die URLs für [!UICONTROL Paid Search] Clickthroughs enthalten immer den `s_kwcid` Abfragezeichenfolgenparameter. Schließen Sie ihn also ein, um sicherzustellen, dass eine ordnungsgemäße Deduplizierung erfolgt, wenn der Besucher zur Landingpage zurückkehrt. „AL!“ einschließen vor der `s_kwcid`, Klicks-/Kosten-/Impressionsdaten korrekt [!UICONTROL Paid Search] zuzuordnen.

Setzen Sie den Kanalwert nicht auf die AMO-ID. Stattdessen sollte sie auf eine Domain wie „Verweisende Domain“, „Suchmaschine + Keyword“ oder „Seite“ festgelegt werden. (Dies ist für alle [!DNL Marketing Channels] relevant).

<!-- Explain that comment about relevancy -- do I need to repeat this for each rule example?  -->

![Beispiel einer Paid-Search-Regel](/help/integrations/assets/a4adc-mc-rule-paid-search.png "Beispiel einer Paid-Search-Regel")

### Natürliche Suchregel

Stellen Sie [!UICONTROL Natural Search] sicher, dass Ihre [[!UICONTROL Paid Search]-](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/t-paid-search-detection) die Abfragezeichenfolgenparameter `ef_id` und `s_kwcid` enthalten. (Normalerweise wird dies automatisch konfiguriert, wenn Advertising Search, Social und Commerce in [!DNL Analytics] integriert werden. Es sollte jedoch überprüft werden, ob ein [!DNL Analytics] die Logik nach der Konfiguration der Integration geändert hat.)

Legen Sie die Regel auf „Stimmt mit den Regeln der natürlichen Sucherkennung überein“ fest (dies ist in der Regel die Standardeinstellung für diesen Kanal).

![Beispiel einer natürlichen Suchregel](/help/integrations/assets/a4adc-mc-rule-natural-search.png "Beispiel einer natürlichen Suchregel")

### Clickthrough-Regel-#1 anzeigen

Erstellen Sie einen Display-ClickThrough-Marketing-Kanal, indem Sie nur Clickthroughs erfassen. Da die AMO-ID sowohl für Clickthroughs als auch für View-throughs identisch ist, verwendet diese Regel die EF ID-Variable und den `ef_id` Abfragezeichenfolgenparameter.

Manchmal werden Clickthroughs über die URL verfolgt (die Standardeinstellung). In anderen Fällen werden Clickthroughs über den Last Event Service auf der Server-Seite verfolgt, daher enthält die URL den `ef_id` nicht. Die Regel sucht daher nach Bedingungen, bei denen die EF-ID-Variable oder der `ef_id` Abfragezeichenfolgenparameter mit &quot;:d&quot; endet. Verwenden Sie den Operator &quot;`Any`&quot;, da diese Regel für jede Bedingung ausgelöst werden soll.

![Beispiel einer ClickThrough-Regel für das erste Display](/help/integrations/assets/a4adc-mc-rule-display-ct.png "Beispiel einer ClickThrough-Regel für das erste Display")

### Regel für natürliche Referrerdomänen

(Optional) Es empfiehlt sich, der [!UICONTROL Natural Referring Domains]-Standardregel die Bedingung „Ist erste Seite des Besuchs“ mit dem Operator „Beliebig“ hinzuzufügen. Diese Regel ist optional, kann jedoch verhindern, dass der Randfall „Natürliche Referrer“ festgelegt wird, wenn der Benutzer auf die Schaltfläche Zurück klickt, um zur Landingpage zurückzukehren.

![Beispiel einer Regel für natürliche verweisende Domains](/help/integrations/assets/a4adc-mc-rule-natural-referring-domains.png "Beispiel einer Regel für natürliche verweisende Domains")

### CTV-Durchsichtsregel anzeigen

Erstellen Sie eine Regel, bei der die AMO-ID auf [!DNL DSP] endet, um `"!ctv"` Durchsichten des verbundenen Fernsehens (CTV) zu verfolgen. Da der Besucher nicht auf die Anzeige geklickt hat, enthält das View-Through-Tracking nicht die `ef_id` oder `s_kwcid` in der URL, und die Regel erfordert nur eine Bedingung.

![Beispiel einer CTV ViewThrough-Regel für &#x200B;](/help/integrations/assets/a4adc-mc-rule-display-ctv-vt.png " AnzeigeBeispiel einer CTV ViewThrough-Regel für Anzeige")

### Durchsichtsregel anzeigen

Um einen ViewThrough-Kanal für das Display zu erstellen, erstellen Sie eine Regel, in der die EF-ID mit &quot;:i&quot; endet. Da der Besucher nicht auf die Anzeige geklickt hat, enthält das View-Through-Tracking nicht die `ef_id` oder `s_kwcid` in der URL, und die Regel erfordert nur eine Bedingung.

![Beispiel für eine ViewThrough-Regel für das Display](/help/integrations/assets/a4adc-mc-rule-display-vt.png "Beispiel für eine ViewThrough-Regel für das Display")

### Clickthrough-Regel-#2 anzeigen

Legen Sie für die zweite ClickThrough-Regel der Anzeige **„AMO-ID beginnt mit „AC!“**. Diese zweite Regel dient zur Erfassung der Klick-/Kosten-/Impressionsdaten für den Anzeigekanal, der direkt von Adobe Advertising in [!DNL Analytics] importiert wird. Diese Daten werden einer AMO-ID zugeordnet, enthalten jedoch keine URL mit der `ef_id` Abfragezeichenfolge. Daher sind diese Treffer nicht mit einer AMO-EF-ID verbunden, die von der ersten ClickThrough-Regel der Anzeige erfasst wird.

![Beispiel einer zweiten ClickThrough-Anzeigeregel](/help/integrations/assets/a4adc-mc-rule-display-ct2.png "Beispiel einer zweiten ClickThrough-Anzeigeregel")

## Reihenfolge der Vorgänge für [!DNL Marketing Channels] {#rule-order}

![Optimale Reihenfolge der Vorgänge für Adobe Advertising-bezogene Regeln](/help/integrations/assets/a4adc-mc-rule-order.png "Optimale Reihenfolge der Vorgänge für Adobe Advertising-bezogene Regeln")

* Stell [!UICONTROL Paid Search] *vorher* [!UICONTROL Natural Search]. Andernfalls können Paid-Search-Daten einer natürlichen Suche zugeordnet werden.

* Stellen Sie das **zuerst** [!UICONTROL Display ClickThrough] *vorher* [!UICONTROL Natural Referring Domains] und [!UICONTROL Natural Social].

* Wenn Sie [!UICONTROL CTV view-throughs] verwenden, legen Sie es *vor* [!UICONTROL Display ViewThroughs]. Andernfalls werden CTV-Durchsichten als Display-Durchsichten erfasst.

* Platzieren Sie [!UICONTROL Display ViewThroughs] *nachher* andere Kanäle, aber vor [!UICONTROL Internal] und [!UICONTROL Direct], da es möglich ist, dass eine Durchsicht und ein nicht [!DNL Advertising] Clickthrough im selben Landingevent auftreten können. So kann ein Besucher beispielsweise eine Adobe Advertising-Anzeige sehen, sich einen Eindruck verschaffen und dann über [!UICONTROL Natural Search] auf die Website gehen.

  Best Practice ist es, die anderen Kanäle (außer [!UICONTROL Internal] und [!UICONTROL Direct]) gegenüber den Viewthroughs zu priorisieren.

* Einige Werbetreibende entscheiden sich möglicherweise dafür, [!UICONTROL Display ViewThroughs] gegenüber [!UICONTROL Natural Referring Domains] zu priorisieren. Tauschen Sie dazu die Verarbeitungsreihenfolge der beiden Regeln aus.

* Die **zweite** [!UICONTROL Display ClickThrough] Regel dient dazu, die Klick-/Kosten-/Impressionsdaten zu erfassen, die direkt von Adobe Advertising in [!DNL Analytics] eingehen. Da diese Daten nur einer AMO ID zugeordnet werden, sind diese Treffer nicht mit einer AMO EF ID verbunden. Wenn Sie diese Regel nicht festlegen, fallen alle Klick-/Kosten-/Impressionsdaten unter den [!UICONTROL Direct]-Kanal, der der Standardkanal für alle Daten ist, die nicht mit einem [!DNL Marketing Channel] übereinstimmen. Diese Regel muss *hinter* der Durchsichtsregel kommen, da sie sonst alle Durchsichtsregeln aufnimmt.

<!-- WORDING!!!!  Check on this, and if it's necessary still with the other info about order:  If you include additional marketing channels, be sure to run your rules in order of specificity. For example, say you create a processing rule for [!DNL YouTube] video ad traffic tracked by Advertising Search, Social, & Commerce. The AMO ID for video traffic starts with with "AL!" and contain "!ytv!". If you run the rule for Paid Search (for which the AMO ID starts with "AL!") and then run the rule for video traffic, the YouTube video ad traffic would all fall under the Paid Search channel. -->

>[!MORELIKETHIS]
>
>* [Grundlagen von [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Warum Kanaldaten zwischen Adobe Advertising und variieren können [!DNL Marketing Channels]](mc-data-variances.md)
>* [Verwenden [!DNL Analytics Marketing Channels] mit Adobe Advertising-Daten](mc-ac-data.md)
>* [Video: Verwenden von  [!DNL Marketing Channels]  für Berichte in Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Adobe Advertising-IDs verwendet von [!DNL Analytics]](/help/integrations/analytics/ids.md)