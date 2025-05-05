---
title: Grundlagen von [!DNL Marketing Channels]
description: Wichtige Informationen zu  [!DNL Analytics Marketing Channels] , die  [!DNL Analytics for Advertising]  verstehen sollten.
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: 29b49e8fa54580d7cdd62f9a10fd2616def4694b
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# Grundlagen der [!DNL Analytics Marketing Channels]

Auf dieser Seite werden wichtige Informationen zu [!DNL Analytics Marketing Channels] erläutert, die [!DNL Analytics for Advertising] Benutzer verstehen müssen.

Eine vollständige Dokumentation zu [!DNL Marketing Channels] finden Sie unter [Erste Schritte mit [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html?lang=de).

## Übersicht über [!DNL Marketing Channels]

[!DNL Marketing Channels] sind eine wichtige Funktion von Adobe Analytics. [!DNL Marketing Channels] Berichte zeigen, wie Kunden über das Reporting-Fenster zu Ihrer Website gelangen und wie sich jeder Kanal auf den Umsatz oder das Verhalten vor Ort auswirkt.

Betrachten Sie das folgende Beispiel einer Cross-Visit-Journey. Jeder Besuch auf Ihrer Website wird durch den Marketing-Kanal angezeigt, über den der Besucher eingetreten ist. Der erste Besuch, auch als Erstkontakt-Kanal bezeichnet, ist E-Mail. Display on Visit Two ist ein teilnehmender Kanal und die natürliche Suche gilt als Letztkontakt-Kanal. Wenn Sie [!UICONTROL Last Touch Attribution] in [!UICONTROL Attribution IQ] verwenden, wird Natural Search das Konversionsereignis im Wert von 250 $ vollständig gutgeschrieben. Mithilfe des Experience Cloud-ID-Service können Sie diese individuellen Besuche zusammenführen, um eine Journey durch einen einzelnen Besucher anzuzeigen.

![Beispiel einer besuchsübergreifenden Konversions-Journey in Marketing-Kanälen](/help/integrations/assets/a4adc-mc-sample-journey.png)

Mithilfe [!UICONTROL Marketing Channels] Verarbeitungsregeln können Sie Logiksätze erstellen, um die Kanäle zu bestimmen, die den Traffic steuern, und um jeden Kanal zu verfolgen, wenn Benutzer zu Ihrer Site gelangen. Beispielsweise würde der [!UICONTROL Email] Kanal durch einen eindeutigen Trackingcode angezeigt, der beim Klicken generiert wird und den Besuch bei der Protokollierung durch Adobe Analytics als von einer E-Mail-Marketing-Kampagne stammend kategorisiert.

## Verarbeitungsregeln und Festlegen der Marketing-Kanäle

Jedes Mal, wenn ein Benutzer auf eine Website kommt, erfolgt dies über eine URL, die er entweder angeklickt oder direkt in die Adressleiste eingegeben hat. Wenn der Besucher die Website betritt, verfolgt [!DNL Analytics] Informationen, anhand derer ermittelt werden kann, über welchen Kanal der Besuch erfolgte.

Häufig hängen Marketer Abfragezeichenfolgen-Parameter-Trackingcodes an Kanal-URLs an, um die Auswirkungen des Kanals auf ihre Site zu verfolgen. Sie können [!DNL Marketing Channels] Verarbeitungsregeln konfigurieren, um auf bestimmte Tracking-Parameter und -Werte zu warten und so den Kanal ohne zusätzliche Tracking-Funktionen zu bestimmen. Wenn beispielsweise alle E-Mail-Kampagnen-URLs dem Format `www.adobe.com?cid=email…` entsprechen (wobei die URL den Abfragezeichenfolgenparameter und den Wert `cid=email` enthält), können Sie eine Regel erstellen, die auf diesen Trackingcode wartet und den Besuch im [!UICONTROL Email]-Kanal zusammenfasst.

Andere Kanäle haben keine verfolgbaren URL-Pfade und benötigen weitere Logik zur Identifizierung. Ein wichtiger Kanal zum Nachverfolgen ist zum Beispiel [!UICONTROL Earned Social], bei dem ein Benutzer auf einen Link klickt, den ein anderer Benutzer organisch in einem sozialen Netzwerk freigegeben hat. Der Marketing-Experte hat jedoch keine Möglichkeit, einen Trackingcode für Abfragezeichenfolgen-Parameter an die freigegebene URL anzuhängen. In diesem Fall können Sie eine Verarbeitungsregel erstellen, die auf die verweisende Domain von Social Media wartet, die von Interesse sind, und das Fehlen bezahlter Trackingcodes, um den Kanal zu bestimmen. Die Besuche, die diese Anforderungen erfüllen, werden dann im Bericht Marketing-Kanäle als „Social-Media-verdient“ erfasst.

Adobe empfiehlt, mit Ihrem Analytics-Team zusammenzuarbeiten, um einen umfassenden Satz an [!DNL Marketing Channels] Verarbeitungsregeln zu erstellen, mit denen alle Kanäle verfolgt werden, die für Ihr Unternehmen relevant sind. Auf diese Weise können Sie leistungsstarke Attributionsberichte erstellen.

Informationen dazu, wie Adobe Advertising zu den Signalen beitragen kann, die zum Erstellen benutzerdefinierter Marketing-Kanäle erforderlich sind, finden Sie unter &quot;[Verwenden von Advertising-IDs zum Erstellen  [!DNL Marketing Channels]  Regeln](mc-ids.md)&quot;.

>[!MORELIKETHIS]
>
>* [Verwenden von Adobe Advertising-IDs zum Erstellen  [!DNL Marketing Channels]  Verarbeitungsregeln](mc-ids.md)
>* [Warum Kanaldaten zwischen Adobe Advertising und variieren können [!DNL Marketing Channels]](mc-data-variances.md)
>* [Verwenden  [!DNL Analytics Marketing Channels]  Adobe Advertising-Daten](mc-ac-data.md)
>* [Video: Verwenden von  [!DNL Marketing Channels]  für das Adobe Advertising-Reporting](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=de)
>* [Überblick über [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
