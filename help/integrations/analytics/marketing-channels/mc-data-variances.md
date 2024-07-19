---
title: Warum können Kanaldaten zwischen Adobe Advertising und [!DNL Marketing Channels] variieren?
description: Erfahren Sie, warum die von der AMO-ID verfolgten Kanaldaten von den von [!DNL Analytics Marketing Channels] verfolgten Kanaldaten variieren können.
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Warum können Kanaldaten zwischen Adobe Advertising und [!DNL Marketing Channels] variieren?

*Advertiser mit nur einer Adobe Advertising-Adobe Analytics-Integration*

Eine häufig gestellte Frage von Benutzern, die über die Integration der Adobe Advertising- und [!DNL Marketing Channels]-Datensätze lernen, lautet: &quot;Was verursacht die Datenabweichung zwischen der AMO-ID und [!DNL Marketing Channels]?&quot; Oder manchmal: &quot;Warum sind die Daten kaputt? Ich benötige, dass alle Metriken in allen Berichten übereinstimmen.&quot; Glücklicherweise zeigen Diskrepanzen nicht an, dass die Daten &quot;beschädigt&quot;sind, und Diskrepanzen werden erwartet und sogar gewünscht. Sehen wir uns an, warum die Integration auf diese Weise entworfen wurde.

Die beiden Datensätze weisen unterschiedliche Hauptanwendungsfälle auf:

* [!DNL Marketing Channels]: Der primäre Anwendungsfall von [!DNL Marketing Channels] besteht darin, Daten über mehrere Kanäle hinweg mit einem gemeinsamen Attributionsmodell zu vergleichen. Analysten können die Dimension [!UICONTROL Marketing Channel] verwenden, um bessere Einblicke in die Interaktion zwischen Kanälen zu erhalten. Diese Einblicke können dazu beitragen, Entscheidungen auf Makroebene darüber zu treffen, wie in die einzelnen Kanäle investiert werden soll, und können zu Einblicken darüber führen, wie Besucher aus den einzelnen Kanälen mit der Website interagieren.

  Die Dimension [!DNL Analytics] [!UICONTROL Marketing Channel] ist daher so konfiguriert, dass alle Kanäle erfasst und verfolgt werden. [!DNL Marketing Channels] kann auch so konfiguriert werden, dass Advertising DSP-Durchsichten und Clickthroughs erfasst werden. Dies geschieht in Bezug auf die anderen Marketingkanäle.

* Adobe Advertising AMO-ID: Der primäre Anwendungsfall der Adobe Advertising-AMO-ID-Daten besteht darin, die erweiterten [!DNL Adobe Sensei]-Angebotsalgorithmen zu speisen. Die Algorithmen treffen automatisch Tausende von Angebotsentscheidungen auf Mikroebene, die täglich getroffen werden, um die Werbeausgaben zu maximieren und die Ziele der [!DNL DSP]-Kampagne oder des [!DNL Search, Social, & Commerce]-Portfolios zu erreichen. Je mehr Konversionsdaten die Algorithmen mit Kampagnen verbinden können, desto besser können die Algorithmen diese Angebotsentscheidungen treffen.

  Um diese Daten zu erfassen, übergibt die [!DNL Analytics for Advertising] -Integration unbearbeitete AMO-IDs, die als Clickthrough- und Durchsichts-Trackingcodes in der AMO-ID-Dimension von Adobe Analytics übersetzt werden können. Diese werden entweder als benutzerspezifische Variable (eVar) oder als reservierte Variable (rVar) gespeichert. Clickthroughs für andere Kanäle werden nicht in der AMO-ID-Dimension festgelegt, sodass die AMO-ID-Dimension die Eingabe aus diesen anderen Kanälen nicht verfolgen kann. Das Ergebnis ist, dass die AMO-ID über [!DNL Marketing Channels] Einstiegspunkte beibehalten wird.

Weitere Informationen zu möglichen Datenabweichungen zwischen Adobe Advertising-verfolgten Daten und [!DNL Analytics]-verfolgten Daten finden Sie unter &quot;[Erwartete Datenabweichungen zwischen  [!DNL Analytics]  und Adobe Advertising](../data-variances.md)&quot;.

>[!MORELIKETHIS]
>
>* [Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising](/help/integrations/analytics/data-variances.md)
>* [Grundlagen von  [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Verwenden von Adobe Advertising-IDs zum Erstellen von [!DNL Marketing Channels] Verarbeitungsregeln](mc-ids.md)
>* [Verwenden von  [!DNL Analytics Marketing Channels] mit Adobe Advertising-Daten](mc-ac-data.md)
>* [Video: Verwendung von [!DNL Marketing Channels] für Adobe Advertising-Berichterstellung](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
