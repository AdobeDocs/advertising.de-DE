---
title: Verwenden von [!DNL Marketing Channels] mit Adobe Advertising-Daten
description: Erfahren Sie, wie Sie Adobe Advertising-Daten in [!DNL Analytics Marketing Channels] verwenden.
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# Verwenden von [!DNL Analytics Marketing Channels] mit Adobe Advertising-Daten

*Advertiser mit nur einer Adobe Advertising-Adobe Analytics-Integration*

Durch die Verwendung von Adobe Advertising- und [!DNL Analytics Marketing Channels] -Berichten erhalten Sie wertvolle Einblicke in die Beeinflussung der Site-Aktivität durch Ihre digitalen Medien.

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

Die folgende Abbildung zeigt, wie Adobe Advertising und [!DNL Marketing Channels] die einzelnen Besuche verfolgen, aus denen die Journey eines Besuchers besteht. Adobe Advertising-Berichte in [!DNL Analytics] sind auf Paid-Display-, Such-, Social- und Commerce-Kanal-Werbung beschränkt, die über Adobe Advertising unter Verwendung der AMO-ID weitergeleitet wird. [!DNL Marketing Channels] verfolgt jedoch alle in den [!DNL Marketing Channels] Verarbeitungsregeln konfigurierten Kanäle.

![So verfolgen Adobe Advertising und [!DNL Marketing Channels] die einzelnen Besuche auf der Journey eines Besuchers](/help/integrations/assets/a4adc-mc-sample-journey2.png)

Beim ersten Besuch kam der Benutzer über eine E-Mail-Kampagne auf die Website, führte zehn Seitenansichten durch und verließ dann die Website. Beim zweiten Besuch kam der Benutzer über eine Display-Anzeige auf die Site, führte zehn Seitenansichten aus und verließ dann die Site. Beim dritten Besuch kam der Benutzer über die natürliche Suche auf die Site, führte fünf Seitenansichten aus, führte eine Konversion von 250 USD und die linke Seite aus. Beachten Sie den Unterschied beim Tracking zwischen [!DNL Marketing Channels] und Adobe Advertising. Der einzige Kanal, den Adobe Advertising in diesem Journey verfolgt, ist [!UICONTROL Display]. Adobe Advertising verfolgt den Kanalbesuch von [!UICONTROL Display] und ordnet die nachfolgenden Interaktionsdaten (wie Seitenansichten) und Konversionen dem Einfluss dieser Werbung zu. [!DNL Marketing Channels] hingegen bietet einen vollständigen Überblick über alle Kanäle.

Da die AMO-ID über die Journey des Besuchers beibehalten wird, können Sie die AMO-ID-Daten verwenden, um zu sehen, wie Adobe Advertising andere Marketingkanäle beeinflusst. Die AMO-ID [ bleibt standardmäßig 60 Tage lang bestehen. Sie können die Persistenz jedoch nach Bedarf konfigurieren.](/help/integrations/analytics/overview.md)

## Kombinieren von Adobe Advertising- und Marketingkanaldaten zur Analyse der Medienleistung

Innerhalb von [!DNL Analytics] können Sie die Adobe Advertising, die Paid-Advertising-Daten beibehält, mit den umfassenden Besuchsdaten von [!DNL Marketing Channels] kombinieren, um Ihre Medienleistung besser zu analysieren und so die Journey des Kunden besser beeinflussen zu können.

Die folgende Analyse verwendet die Adobe Advertising-Daten, um verschiedene Versionen davon anzuzeigen, wie sich eine Display-Werbung auf die Site-Konversion auswirkt. Alle drei Spalten verwenden dieselben Konversionsmetriken, aber jede Spalte erzählt eine andere Geschichte:

* Spalte 1 betrachtet die AMO-ID-Daten, die über die Journey des Besuchers hinweg persistent sind. Spalte 1 zeigt an, dass 641 App-Starts zu einem Zeitpunkt entweder durch eine Durchsicht oder ein Clickthrough-Ereignis mit einer Adobe Advertising-Anzeige verknüpft wurden. Diese Ansicht berücksichtigt keine andere [!DNL Marketing Channels] -Attribution.

* Im Datensatz [!DNL Marketing Channels] werden die 641 Anwendungsstarts jedoch anderen Marketing-Kanälen zugeordnet. Die letzten beiden Spalten nehmen die 641 &quot;Anwendungsstarts&quot;und beschränken die Daten auf die Kanäle [!UICONTROL Display Click-Through] und [!UICONTROL Display View-Through], wobei die Konversionen angezeigt werden, die in einem Letztkontakt-Attributionsmodell auftreten.

![Beispiel, wie eine Display-Anzeige sich auf die Site-Konversion auswirkt](/help/integrations/assets/a4adc-mc-display-impact.png)

Sie können diese Analyse einen Schritt weiter ausführen. Sie können die Adobe Advertising-Zeile weiter nach Marketingkanälen aufschlüsseln, um zu sehen, wo die Adobe Advertising-Konversionen den 641 Anwendungen Starts zugeordnet werden. Sie wissen bereits, dass fünf dieser Konversionen einem Last Touch-Display-Clickthrough und 19 einem Last Touch-Display-Clickthrough zugeordnet werden. Dadurch bleiben 617 Anwendungsstarts weiterhin anderen Marketingkanälen zugeordnet. Sie können die Dimension &quot;Letztkontakt Kanal&quot;per Drag-and-Drop auf das Zeilenelement &quot;Advertising DSP&quot;ziehen, um die Kanalzuordnung für den Rest der &quot;Anwendungsstarts&quot;anzuzeigen und die kanalübergreifende Auswirkung des Anzeigekanals anzuzeigen.

![Hinzufügen der Dimension &quot;Letztkontakt Kanal&quot;](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Jetzt können Sie sehen, wie die verbleibenden Anwendungsstarts zugeordnet werden. E-Mail wird 357 Last Touch-Anwendungen Starts zugeschrieben, für die eine AMO-ID beibehalten wurde. Mithilfe dieser Analyseart können Sie die Wirkung von Adobe Advertising-Display-Anzeigen auf alle Kanäle erkennen. Bei nur einem Datensatz und Attributionsmodell ist dieser Insight-Typ nicht verfügbar.

![Beispiel für die kanalübergreifende Auswirkung der Anzeigenkanäle](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

Sie können die Analyse weiter verbessern, indem Sie ein Stack-Diagramm verwenden, das auf &quot;100 % gestapelt&quot;festgelegt ist, um Trend-Daten über einen bestimmten Zeitraum anzuzeigen. Diese Visualisierung erleichtert die Überwachung der von Ihren Display-Marketing-Kampagnen am stärksten betroffenen Letztkontakt-Marketing-Kanäle.

![Beispiel für die kanalübergreifende Trendwirkung der Anzeigenkanäle](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Grundlagen von  [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Verwenden von Adobe Advertising-IDs zum Erstellen von [!DNL Marketing Channels] Verarbeitungsregeln](mc-ids.md)
>* [Warum Kanaldaten zwischen Adobe Advertising und  [!DNL Marketing Channels]](mc-data-variances.md) variieren können
>* [Video: Verwendung von [!DNL Marketing Channels] für Adobe Advertising-Berichterstellung](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Überblick über  [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
