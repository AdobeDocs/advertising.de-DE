---
title: Warum Kanaldaten zwischen Adobe Advertising und  [!DNL Marketing Channels] variieren können
description: Erfahren Sie, warum Kanaldaten, die von der AMO-ID verfolgt werden, von Kanaldaten, die von verfolgt werden, abweichen  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Warum Kanaldaten zwischen Adobe Advertising und [!DNL Marketing Channels] variieren können

*Nur Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

Eine häufige Frage von Anwendern, die mehr über die Integration von Adobe Advertising- und [!DNL Marketing Channels]-Datensätzen erfahren, lautet: „Was verursacht die Varianz in den Daten zwischen der AMO-ID und der [!DNL Marketing Channels]?“ Oder, manchmal, „Warum sind die Daten beschädigt? Ich brauche alle Metriken, die in allen Berichten übereinstimmen.“ Glücklicherweise zeigen Diskrepanzen nicht an, dass die Daten „beschädigt“ sind, und Diskrepanzen werden erwartet und sogar gewünscht. Sehen wir uns an, warum die Integration auf diese Weise konzipiert wurde.

Die beiden Datensätze haben unterschiedliche primäre Anwendungsfälle:

* [!DNL Marketing Channels]: Der primäre Anwendungsfall für [!DNL Marketing Channels] besteht darin, Daten über mehrere Kanäle hinweg mit einem gemeinsamen Attributionsmodell zu vergleichen. Analysten können die Dimension [!UICONTROL Marketing Channel] verwenden, um mehr Einblicke in die Interaktion zwischen Kanälen zu erhalten. Diese Einblicke können dazu beitragen, Entscheidungen auf Makroebene darüber zu fördern, wie in jeden Kanal investiert werden soll, und können zu Einblicken darüber führen, wie Besucher aus jedem Kanal mit der Website interagieren.

  Die Dimension [!DNL Analytics] [!UICONTROL Marketing Channel] ist daher so konfiguriert, dass alle Kanäle erfasst und verfolgt werden. [!DNL Marketing Channels] kann auch so konfiguriert werden, dass die Viewthroughs und Clickthroughs von Advertising DSP erfasst werden, und zwar in Bezug auf die anderen Marketing-Kanäle.

* Adobe Advertising-AMO-ID: Der primäre Anwendungsfall für die Adobe Advertising-AMO-ID-Daten ist die Einspeisung der erweiterten [!DNL Adobe Sensei] Angebotsalgorithmen. Die Algorithmen treffen automatisch tausende von Bid-Entscheidungen auf Mikroebene, die täglich getroffen werden, um die Werbeausgaben zu maximieren und die Ziele der [!DNL DSP] Kampagne oder des [!DNL Search, Social, & Commerce] Portfolios zu erreichen. Je mehr Konversionsdaten die Algorithmen mit Kampagnen verbinden können, desto besser können die Algorithmen diese Angebotsentscheidungen treffen.

  Um diese Daten zu erfassen, übergibt die [!DNL Analytics for Advertising]-Integration rohe AMO-IDs, die als Clickthrough- und View-Through-Trackingcodes in der AMO-ID-Dimension von Adobe Analytics übersetzt werden können. Diese werden entweder als benutzerdefinierte Variable (eVar) oder als reservierte Variable (rVar) gespeichert. Clickthroughs für andere Kanäle sind in der AMO-ID-Dimension nicht festgelegt, sodass die AMO-ID-Dimension den Eintrag aus diesen anderen Kanälen nicht verfolgen kann. Dies hat zur Folge, dass die AMO-ID über [!DNL Marketing Channels] Einstiegspunkte bestehen bleibt.

Weitere Informationen zu möglichen Datenabweichungen zwischen Adobe Advertising-getrackten und [!DNL Analytics]-getrackten Daten finden Sie unter &quot;[Erwartete Datenabweichungen zwischen [!DNL Analytics]  und Adobe Advertising](../data-variances.md).

>[!MORELIKETHIS]
>
>* [Erwartete Datenabweichungen zwischen  [!DNL Analytics]  und Adobe Advertising](/help/integrations/analytics/data-variances.md)
>* [Grundlagen von [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Verwenden von Adobe Advertising-IDs zum Erstellen  [!DNL Marketing Channels]  Verarbeitungsregeln](mc-ids.md)
>* [Verwenden  [!DNL Analytics Marketing Channels]  Adobe Advertising-Daten](mc-ac-data.md)
>* [Video: Verwenden von  [!DNL Marketing Channels]  für das Adobe Advertising-Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
