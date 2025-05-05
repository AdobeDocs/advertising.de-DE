---
title: Verwenden  [!DNL Marketing Channels]  Adobe Advertising-Daten
description: Erfahren Sie, wie Sie Adobe Advertising-Daten in  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# Verwenden von [!DNL Analytics Marketing Channels] mit Adobe Advertising-Daten

*Nur Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

Durch die Verwendung von Adobe Advertising- und [!DNL Analytics Marketing Channels]-Berichten erhalten Sie wertvolle Einblicke in die Beeinflussung der Website-Aktivität durch digitale Medien.

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

Die folgende Abbildung zeigt, wie Adobe Advertising und [!DNL Marketing Channels] die einzelnen Besuche verfolgen, aus denen die Journey eines Besuchers besteht. Adobe Advertising-Berichte in [!DNL Analytics] sind auf bezahlte Anzeige-, Such-, Social-Media- und Commerce-Kanalwerbung beschränkt, die über Adobe Advertising unter Verwendung der AMO-ID geschaltet wird. [!DNL Marketing Channels] verfolgt jedoch alle Kanäle, die in den [!DNL Marketing Channels]-Verarbeitungsregeln konfiguriert sind.

![Wie Adobe Advertising und [!DNL Marketing Channels] die einzelnen Besuche auf der Journey eines Besuchers verfolgen](/help/integrations/assets/a4adc-mc-sample-journey2.png)

Beim ersten Besuch ist der Benutzer über eine E-Mail-Kampagne auf die Website gelangt, hat zehn Seitenansichten ausgeführt und ist dann gegangen. Beim zweiten Besuch ist der Benutzer über eine Anzeige auf die Website gekommen, hat zehn Seitenansichten ausgeführt und ist dann gegangen. Beim dritten Besuch trat der Benutzer über die natürliche Suche auf die Website ein, führte fünf Seitenansichten aus, führte eine Konvertierung von 250 $ durch und links. Beachten Sie den Unterschied beim Tracking zwischen [!DNL Marketing Channels] und Adobe Advertising. Der einzige Kanal, den Adobe Advertising auf dieser Journey verfolgt, ist [!UICONTROL Display]. Adobe Advertising verfolgt den [!UICONTROL Display]-Kanalbesuch und ordnet die nachfolgenden Interaktionsdaten (z. B. Seitenansichten) und Konversionen wieder dem Einfluss dieser Anzeige zu. [!DNL Marketing Channels] hingegen bietet einen vollständigen Überblick über alle Kanäle.

Da die AMO-ID über den Journey des Besuchers gespeichert bleibt, können Sie anhand der AMO-ID-Daten sehen, wie sich das Adobe Advertising auf andere Marketing-Kanäle auswirkt. Die AMO-ID [bleibt standardmäßig 60 Tage erhalten](/help/integrations/analytics/overview.md) Sie können die Persistenz jedoch nach Bedarf konfigurieren.

## So kombinieren Sie Adobe Advertising- und Marketing-Kanaldaten zur Analyse der Medienleistung

Innerhalb von [!DNL Analytics] können Sie die Adobe Advertising-persistenten Paid-Advertising-Daten und die [!DNL Marketing Channels] umfassenden Besuchsdaten kombinieren, um Ihre Medienleistung besser zu analysieren, damit Sie die Kunden-Journey besser beeinflussen können.

Die folgende Analyse verwendet die Adobe Advertising-Daten, um verschiedene Versionen zu zeigen, wie sich eine Display-Anzeige auf die Website-Konversion auswirkt. Alle drei Spalten verwenden dieselbe Konversionsmetrik, aber jede Spalte erzählt eine andere Geschichte:

* In Spalte 1 werden die AMO-ID-Daten dargestellt, die auf der gesamten Journey des Besuchers persistent sind. In Spalte 1 ist angegeben, dass 641 Programmstarts entweder durch ein Durchsichts- oder ein Klickereignis mit einer Adobe Advertising-Anzeige verknüpft wurden. Diese Ansicht berücksichtigt keine andere [!DNL Marketing Channels].

* Im [!DNL Marketing Channels] Datensatz werden die 641 Anwendungsstarts jedoch anderen Marketing-Kanälen zugeordnet. Die letzten beiden Spalten nehmen die „641 Anwendungen beginnt“ und beschränken die Daten auf den [!UICONTROL Display Click-Through]- und [!UICONTROL Display View-Through]-Kanal, wobei die Konversionen angezeigt werden, die in einem Letztkontakt-Attributionsmodell auftreten.

![Beispiel dafür, wie sich eine Display-Anzeige auf die Website-Konversion auswirkt](/help/integrations/assets/a4adc-mc-display-impact.png)

Sie können diese Analyse noch einen Schritt weiterführen. Sie können die Adobe Advertising-Zeile nach Marketing-Kanal weiter aufschlüsseln, um zu sehen, wo die Adobe Advertising-Konversionen den 641 Startprogrammen zugeordnet sind. Sie wissen bereits, dass fünf dieser Konversionen einem Last-Touch-Display-Click-Through und 19 einem Last-Touch-Display-View-Through zugeordnet werden. So bleiben 617 Anwendungsstarts, die anderen Marketing-Kanälen zugeordnet werden. Sie können die Dimension Letztkontakt-Kanal per Drag-and-Drop auf den Zeileneintrag Advertising DSP ziehen, um die Kanalzuordnung für die übrigen gestarteten Programme anzuzeigen und die kanalübergreifende Wirkung des Anzeigekanals anzuzeigen.

![Hinzufügen der Dimension Letztkontakt-Kanal](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Jetzt können Sie sehen, wie die verbleibenden Anwendungsstarts zugeordnet werden. E-Mail wird für 357 Last Touch-Anwendungsstarts angerechnet, für die eine AMO-ID beibehalten wurde. Mit dieser Art von Analyse können Sie die Auswirkungen sehen, die Adobe Advertising-Display-Anzeigen auf allen Kanälen hatten. Mit nur einem Datensatz und einem Attributionsmodell wäre diese Art von Einblick nicht verfügbar.

![Beispiel für die kanalübergreifende Auswirkung der Anzeigekanäle](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

Sie können die Analyse weiter verbessern, indem Sie ein Stapeldiagramm verwenden, das auf „100 % gestapelt“ eingestellt ist, um Trenddaten im Zeitverlauf anzuzeigen. Diese Visualisierung erleichtert die Überwachung, welche Last-Touch-Marketing-Kanäle durch Ihre Display-Marketing-Kampagnen stärker betroffen sind.

![Beispiel für die trendmäßige kanalübergreifende Wirkung der Anzeigekanäle](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Grundlagen von [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Verwenden von Adobe Advertising-IDs zum Erstellen  [!DNL Marketing Channels]  Verarbeitungsregeln](mc-ids.md)
>* [Warum Kanaldaten zwischen Adobe Advertising und variieren können [!DNL Marketing Channels]](mc-data-variances.md)
>* [Video: Verwenden von  [!DNL Marketing Channels]  für das Adobe Advertising-Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=de)
>* [Überblick über [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
