---
title: Grundlagen von [!DNL Marketing Channels]
description: Wichtige Informationen zu  [!DNL Analytics Marketing Channels] , die  [!DNL Analytics for Advertising]  verstehen sollten.
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
TQID: https://experienceleague.adobe.com/NJ4LPss-g-J06PuvdCaUktHPyP7MARdJK84-D8gnwAk
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: beb7a3c1-66ab-4786-b879-7621375b3c40
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 542
ht-degree: 0%

---

# Grundlagen der [!DNL Analytics Marketing Channels]

Auf dieser Seite werden wichtige Informationen zu [!DNL Analytics Marketing Channels] erläutert, die [!DNL Analytics for Advertising] Benutzer verstehen müssen.

Eine vollständige Dokumentation zu [!DNL Marketing Channels] finden Sie unter [Erste Schritte mit [!DNL Marketing Channels]](https://experienceleague.adobe.com/en/docs/analytics/components/marketing-channels/c-getting-started-mchannel).

## Übersicht über [!DNL Marketing Channels]

[!DNL Marketing Channels] sind eine wichtige Funktion von Adobe Analytics. [!DNL Marketing Channels] Berichte zeigen, wie Kunden über das Reporting-Fenster zu Ihrer Website gelangen und wie sich jeder Kanal auf den Umsatz oder das Verhalten vor Ort auswirkt.

Betrachten Sie das folgende Beispiel einer Cross-Visit-Journey. Jeder Besuch auf Ihrer Website wird durch den Marketing-Kanal angezeigt, über den der Besucher eingetreten ist. Der erste Besuch, auch als Erstkontakt-Kanal bezeichnet, ist E-Mail. Display on Visit Two ist ein teilnehmender Kanal und die natürliche Suche gilt als Letztkontakt-Kanal. Wenn Sie [!UICONTROL Last Touch Attribution] in [!UICONTROL Attribution IQ] verwenden, erhält Natural Search die volle Gutschrift für das Konversionsereignis von 250 $. Mithilfe des Experience Cloud ID-Service können Sie diese individuellen Besuche miteinander verknüpfen, um eine Journey durch einen einzelnen Besucher anzuzeigen.

![Beispiel einer besuchsübergreifenden Konversions-Journey in Marketing-Kanälen](/help/integrations/assets/a4adc-mc-sample-journey.png)

Mithilfe [!UICONTROL Marketing Channels] Verarbeitungsregeln können Sie Logiksätze erstellen, um die Kanäle zu bestimmen, die den Traffic steuern, und um jeden Kanal zu verfolgen, wenn Benutzer zu Ihrer Site kommen. Der [!UICONTROL Email]-Kanal wird beispielsweise durch einen eindeutigen Trackingcode angezeigt, der beim Klicken generiert wird und den Besuch bei der Protokollierung durch Adobe Analytics als von einer E-Mail-Marketing-Kampagne stammend kategorisiert.

## Verarbeitungsregeln und Festlegen der Marketing-Kanäle

Jedes Mal, wenn ein Benutzer auf eine Website kommt, erfolgt dies über eine URL, die er entweder angeklickt oder direkt in die Adressleiste eingegeben hat. Wenn der Besucher die Website betritt, verfolgt [!DNL Analytics] Informationen, anhand derer ermittelt werden kann, über welchen Kanal der Besuch erfolgte.

Häufig hängen Marketer Abfragezeichenfolgen-Parameter-Trackingcodes an Kanal-URLs an, um die Auswirkungen des Kanals auf ihre Site zu verfolgen. Sie können [!DNL Marketing Channels] Verarbeitungsregeln konfigurieren, um auf bestimmte Tracking-Parameter und -Werte zu warten und so den Kanal ohne zusätzliche Tracking-Funktionen zu bestimmen. Wenn beispielsweise alle E-Mail-Kampagnen-URLs dem Format `www.adobe.com?cid=email…` entsprechen (wobei die URL den Abfragezeichenfolgenparameter und den Wert `cid=email` enthält), können Sie eine Regel erstellen, die auf diesen Trackingcode wartet und den Besuch im [!UICONTROL Email]-Kanal zusammenfasst.

Andere Kanäle haben keine verfolgbaren URL-Pfade und benötigen weitere Logik zur Identifizierung. Ein wichtiger Kanal zum Nachverfolgen ist zum Beispiel [!UICONTROL Earned Social], bei dem ein Benutzer auf einen Link klickt, den ein anderer Benutzer organisch in einem sozialen Netzwerk freigegeben hat. Der Marketing-Experte hat jedoch keine Möglichkeit, einen Trackingcode für Abfragezeichenfolgen-Parameter an die freigegebene URL anzuhängen. In diesem Fall können Sie eine Verarbeitungsregel erstellen, die auf die verweisende Domain von Social Media wartet, die von Interesse sind, und das Fehlen bezahlter Trackingcodes, um den Kanal zu bestimmen. Die Besuche, die diese Anforderungen erfüllen, werden dann im Bericht Marketing-Kanäle als „Social-Media-verdient“ erfasst.

Adobe empfiehlt, mit Ihrem [!DNL Analytics]-Team zusammenzuarbeiten, um einen umfassenden Satz von [!DNL Marketing Channels]-Verarbeitungsregeln zu erstellen, mit denen alle relevanten Kanäle verfolgt werden. Auf diese Weise können Sie leistungsstarke Attributionsberichte erstellen.

Informationen dazu, wie Adobe Advertising zu den Signalen beitragen kann, die zum Erstellen benutzerdefinierter Marketing-Kanäle erforderlich sind, finden Sie unter [Verwenden von Adobe Advertising-IDs zum Erstellen  [!DNL Marketing Channels]  Verarbeitungsregeln](mc-ids.md).

>[!MORELIKETHIS]
>
>* [Verwenden von Adobe Advertising-IDs zum Erstellen  [!DNL Marketing Channels]  Verarbeitungsregeln](mc-ids.md)
>* [Warum Kanaldaten zwischen Adobe Advertising und variieren können [!DNL Marketing Channels]](mc-data-variances.md)
>* [Verwenden [!DNL Analytics Marketing Channels] mit Adobe Advertising-Daten](mc-ac-data.md)
>* [Video: Verwenden von  [!DNL Marketing Channels]  für Berichte in Adobe Advertising](https://experienceleague.adobe.com/en/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc)
>* [Überblick über [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
