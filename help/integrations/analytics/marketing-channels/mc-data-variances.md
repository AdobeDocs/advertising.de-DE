---
title: Warum Kanaldaten zwischen Adobe Advertising und [!DNL Marketing Channels] variieren können
description: Erfahren Sie, warum Kanaldaten, die von der AMO-ID verfolgt werden, von Kanaldaten, die von [!DNL Analytics Marketing Channels] verfolgt werden, abweichen können.
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
TQID: 'https://experienceleague.adobe.com/zzYKrbiwvW9Ysf7baDfKGsETmSvYbXDY7-lIygorXH8'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: f2860a4b-f905-4545-bead-1bbc92564592
    internal-label: Advertising integrations
subfeature_v2:
  - id: cfd751d4-ee56-4323-8fd1-dc174b031709
    internal-label: Analytics integration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: dba482e5-29a8-4127-afa2-c4b913512ef8
    internal-label: Data and analytics
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%
---
# Warum Kanaldaten zwischen Adobe Advertising und [!DNL Marketing Channels] variieren können

*Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

Eine häufige Frage von Benutzenden, die mehr über die Integration der Adobe Advertising- und [!DNL Marketing Channels]-Datensätze erfahren, lautet: „Was verursacht die Datenabweichung zwischen der AMO-ID und der [!DNL Marketing Channels]?“ Oder, manchmal, „Warum sind die Daten beschädigt? Ich brauche alle Metriken, die in allen Berichten übereinstimmen.“ Glücklicherweise zeigen Diskrepanzen nicht an, dass die Daten „beschädigt“ sind, und Diskrepanzen werden erwartet und sogar gewünscht. Sehen wir uns an, warum die Integration so konzipiert wurde.

Die beiden Datensätze haben unterschiedliche primäre Anwendungsfälle:

* [!DNL Marketing Channels]: Der primäre Anwendungsfall für [!DNL Marketing Channels] besteht darin, Daten über mehrere Kanäle hinweg mit einem gemeinsamen Attributionsmodell zu vergleichen. Analysten können die Dimension [!UICONTROL Marketing Channel] verwenden, um mehr Einblicke in die Interaktion zwischen Kanälen zu erhalten. Diese insight kann Entscheidungen auf Makroebene über Investitionen in die einzelnen Kanäle anregen und zu Einblicken in die Interaktion der Besucher der einzelnen Kanäle mit der Website führen.

  Die Dimension [!DNL Analytics] [!UICONTROL Marketing Channel] ist daher so konfiguriert, dass alle Kanäle erfasst und verfolgt werden. [!DNL Marketing Channels] kann auch so konfiguriert werden, dass die Viewthroughs und Clickthroughs von Advertising DSP erfasst werden, und zwar in Bezug auf die anderen Marketing-Kanäle.

* Adobe Advertising-AMO-ID: Der Hauptanwendungsfall der Adobe Advertising-AMO-ID-Daten ist die Einspeisung der erweiterten [!DNL Adobe AI] Angebotsalgorithmen. Die Algorithmen treffen automatisch tausende von Bid-Entscheidungen auf Mikroebene, die täglich getroffen werden, um die Werbeausgaben zu maximieren und die Ziele der [!DNL DSP] Kampagne oder des [!DNL Search, Social, & Commerce] Portfolios zu erreichen. Je mehr Konversionsdaten die Algorithmen mit Kampagnen verbinden können, desto besser können die Algorithmen diese Angebotsentscheidungen treffen.

  Um diese Daten zu erfassen, übergibt die [!DNL Analytics for Advertising]-Integration rohe AMO-IDs, die als Clickthrough- und View-Through-Trackingcodes in der AMO-ID-Dimension von Adobe Analytics übersetzt werden können. Diese werden entweder als benutzerdefinierte Variable (eVar) oder als reservierte Variable (rVar) gespeichert. Clickthroughs für andere Kanäle sind in der AMO-ID-Dimension nicht festgelegt, sodass die AMO-ID-Dimension den Eintrag aus diesen anderen Kanälen nicht verfolgen kann. Dies hat zur Folge, dass die AMO-ID über [!DNL Marketing Channels] Einstiegspunkte bestehen bleibt.

Weitere Informationen zu möglichen Datenabweichungen zwischen von Adobe Advertising verfolgten Daten und [!DNL Analytics] verfolgten Daten finden Sie unter [Erwartete Datenabweichungen zwischen  [!DNL Analytics]  und Adobe Advertising](../data-variances.md).

>[!MORELIKETHIS]
>
>* [Erwartete Datenabweichungen zwischen  [!DNL Analytics]  und Adobe Advertising](/help/integrations/analytics/data-variances.md)
>* [Grundlagen von [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Verwenden von Adobe Advertising-IDs zum Erstellen  [!DNL Marketing Channels]  Verarbeitungsregeln](mc-ids.md)
>* [Verwenden [!DNL Analytics Marketing Channels] mit Adobe Advertising-Daten](mc-ac-data.md)
>* [Video: Verwenden von  [!DNL Marketing Channels]  für Berichte in Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
