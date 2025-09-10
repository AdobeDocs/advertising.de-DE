---
title: Adobe Advertising-IDs verwendet von [!DNL Analytics]
description: Adobe Advertising-IDs verwendet von [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 1a0a111e25efd7d0f38c2d18f4b57b9428ec4ed7
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 0%

---

# Von [!DNL Analytics] verwendete Adobe Advertising-IDs

*Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

*Gilt für Advertising DSP und[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising verwendet zwei IDs zur Leistungsüberwachung auf der Site: die *EF ID* und die *AMO ID*.

Wenn eine Ad-Impression auftritt, erstellt Adobe Advertising die AMO ID- und EF ID-Werte und speichert sie. Wenn ein Besucher, der eine Anzeige gesehen hat, die Website betritt, ohne auf eine Anzeige zu klicken, ruft [!DNL Analytics] diese Werte von Adobe Advertising über den [!DNL Analytics for Advertising] JavaScript-Code auf. Für View-Through-Traffic generiert [!DNL Analytics] eine zusätzliche ID (`SDID`), mit der die EF-ID und die AMO-ID [!DNL Analytics] zugeordnet werden. Für Clickthrough-Traffic werden diese IDs mithilfe der Abfragezeichenfolgen-Parameter `ef_id` und `s_kwcid` (für die AMO-ID) in die Landingpage-URL aufgenommen.

Adobe Advertising unterscheidet anhand der folgenden Kriterien zwischen einem Clickthrough- oder einem View-Through-Eintrag auf der Website:

* Ein Viewthrough-Eintrag wird erfasst, wenn ein Benutzer die Website besucht, nachdem er eine Anzeige angesehen, aber nicht darauf geklickt hat. [!DNL Analytics] zeichnet eine Durchsicht auf, wenn zwei Bedingungen erfüllt sind:

   * Der Besucher hat keine Clickthroughs für eine [!DNL DSP] oder [!DNL Search, Social, & Commerce] Anzeige während des [Click-Lookback-Fensters](/help/integrations/analytics/prerequisites.md#lookback-a4adc).

   * Der Besucher hat mindestens eine [!DNL DSP] Anzeige während des Impression[Lookback-Fensters gesehen](/help/integrations/analytics/prerequisites.md#lookback-a4adc). Der letzte Impression wird als Durchsicht weitergegeben.

* Ein Clickthrough-Eintrag wird erfasst, wenn ein Site-Besucher auf eine Anzeige klickt, bevor er die Site betritt. [!DNL Analytics] erfasst einen Clickthrough, wenn eine der folgenden Bedingungen auftritt:

   * Die URL enthält eine EF-ID und eine AMO-ID, die von Adobe Advertising zur Landingpage-URL hinzugefügt wurden.

   * Die URL enthält keine Trackingcodes, aber der Adobe Advertising JavaScript-Code erkennt innerhalb der letzten zwei Minuten einen Klick.

![Ansichtsbasierte [!DNL Analytics]-Integration von Adobe Advertising](/help/integrations/assets/a4adc-view-through-process.png)

*Abbildung 1: Ansichtsbasierte [!DNL Analytics] von Adobe Advertising*

![Adobe Advertising-Klick-URL-basierte [!DNL Analytics]-Integration](/help/integrations/assets/a4adc-click-through-process.png)

*Abbildung 2: URL-basierte [!DNL Analytics]-Integration für Adobe Advertising*

<!-- ## Adobe Advertising EF IDs -->

{{$include /help/_includes/ef-id.md}}

### Die EF-ID Dimension in [!DNL Analytics]

In [!DNL Analytics] Berichten können Sie EF ID-Daten finden, indem Sie nach der Dimension &quot;[!UICONTROL EF ID]&quot; suchen und die [!UICONTROL EF ID Instance] verwenden.

EF-IDs unterliegen dem Limit von 500.000 eindeutigen Kennungen in Analysis Workspace. Sobald der 500k-Wert erreicht ist, werden alle neuen Trackingcodes unter dem einzeiligen Titel &quot;[!UICONTROL Low Traffic]&quot; gemeldet. Aufgrund der Möglichkeit fehlender Berichterstellungstreue werden die EF-IDs nicht klassifiziert und sollten nicht für Segmente oder Berichte in [!DNL Analytics] verwendet werden.

<!-- ## Adobe Advertising AMO IDs {#amo-id} -->

{{$include /help/_includes/amo-id.md}}

### Möglichkeiten zur Implementierung der AMO-ID {#amo-id-implement}

Der Parameter wird den Tracking-URLs auf eine der folgenden Arten hinzugefügt:

* (Empfohlen) Wenn die Server-seitige Einfügefunktion implementiert ist.

   * DSP-Kunden: Der Pixel-Server hängt den Parameter s_kwcid automatisch an die Suffixe Ihrer Landingpage an, wenn ein Endbenutzer eine Display-Anzeige mit dem Adobe Advertising-Pixel aufruft.

   * Kunden aus den Bereichen Suche, Social Media und Commerce:

      * Bei [!DNL Google Ads]- und [!DNL Microsoft Advertising]-Konten mit aktivierter [!UICONTROL Auto Upload] für das Konto oder die Kampagne fügt der Pixel-Server den Parameter s_kwcid automatisch an die Suffixe der Landingpage an, wenn ein Endbenutzer bzw. eine Endbenutzerin auf eine Anzeige mit dem Pixel &quot;Adobe Advertising&quot; klickt.

      * Für andere Werbenetzwerke oder [!DNL Google Ads]- und [!DNL Microsoft Advertising]-Konten mit deaktivierter [!UICONTROL Auto Upload]-Einstellung fügen Sie den Parameter manuell zu Ihren [Anlagenparametern auf Kontoebene](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} hinzu, die ihn an Ihre Basis-URLs anhängen.

* Wenn die Server-seitige Einfügefunktion nicht implementiert ist:

   * DSP-Kunden: Der [JavaScript](javascript.md)Code zeichnet automatisch Clickthroughs und Viewthroughs auf. Wenn ein Browser keine Cookies von Drittanbietern unterstützt, können Sie weiterhin Klick-basierte Konversionen für die folgenden Anzeigentypen verfolgen:

      * Fügen Sie für [!DNL Flashtalking]-Anzeigen-Tags manuell zusätzliche Makros pro &quot;[Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](/help/integrations/analytics/macros-flashtalking.md) ein. **Hinweis:** Dieses Verfahren ist nicht erforderlich, wenn Ihr Unternehmen eine direkte Partnerschaft mit [!DNL Flashtalking] unterhält und Sie in der Dokumentation zum `s_kwcid`-Support unter `ef_id`https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros[!DNL Flashtalking] Datenweiterleitungs-Makros zum Tracking der [- und ](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros) verwenden.

      * Fügen Sie für [!DNL Google Campaign Manager 360]-Anzeigen-Tags manuell zusätzliche Makros pro &quot;[Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md) ein.

   * Kunden aus den Bereichen Suche, Social Media und Commerce:

      * Fügen Sie für ([!DNL Google Ads] und [!DNL Microsoft Advertising]) Anzeigen manuell den AMO-ID-Parameter zu Ihren Landingpage-Suffixen hinzu, idealerweise auf [Kontoebene](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} es sei denn, es ist ein anderes Tracking für einzelne Kontokomponenten erforderlich.

      * Für Anzeigen in allen anderen Werbenetzwerken fügen Sie den AMO-ID-Parameter manuell zu Ihren [Append-Parametern auf Kontoebene](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} hinzu, die ihn an Ihre Basis-URLs anhängen.

Wenden Sie sich an Ihr Adobe-Accountteam, um die Server-seitige Einfügefunktion zu implementieren oder die beste Option für Ihr Unternehmen zu ermitteln.

### AMO ID Dimension in [!DNL Analytics]

In Analytics-Berichten können Sie AMO-ID-Daten finden, indem Sie nach der [!UICONTROL AMO ID] Dimension suchen und die [!UICONTROL AMO ID Instances] Metrik verwenden. Die Dimension [!UICONTROL AMO ID] enthält alle erfassten AMO-ID-Werte, während die Metrik [!UICONTROL AMO ID Instances] angibt, wie oft ein AMO-ID-Wert von der Site erfasst wurde. Wenn beispielsweise viermal auf dieselbe Suchanzeige geklickt wurde, Analytics jedoch sieben Site-Einträge nachverfolgt hat, wären [!UICONTROL AMO ID Instances] sieben (7) und [!UICONTROL Clicks] vier (4).

Für Reporting- oder Auditing-Vorgänge innerhalb von [!DNL Analytics] ist die Best Practice, die AMO-ID zusammen mit der entsprechenden -Instanz zu verwenden. Weitere Informationen finden Sie unter &quot;[-Through-Datenvalidierung für [!DNL Analytics for Advertising]](data-variances.md#data-validation) in „Erwartete Datenvarianzen zwischen [!DNL Analytics] und Adobe Advertising&quot;.

## Über Analytics Classifications

[!DNL Analytics] ist eine [Klassifizierung](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html?lang=de) ein Metadatenelement für einen bestimmten Trackingcode, z. B. Konto, Kampagne oder Anzeige. Adobe Advertising kategorisiert Adobe Advertising-Rohdaten mithilfe von Klassifizierungen, sodass Sie die Daten beim Generieren von Berichten auf unterschiedliche Weise anzeigen können (z. B. nach Anzeigentyp oder Kampagne). Klassifizierungen bilden die Grundlage des Adobe Advertising-Reportings in [!DNL Analytics] und können mit den AMO-Metriken wie [!UICONTROL Adobe Advertising Cost], [!UICONTROL Adobe Advertising Impressions] und [!UICONTROL AMO Clicks] sowie mit benutzerdefinierten und standardmäßigen Onsite-Ereignissen wie [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] und [!UICONTROL Revenue] verwendet werden.

>[!MORELIKETHIS]
>
>* [Überblick über [!DNL Analytics for Advertising]](overview.md)
>* [Erwartete Datenabweichungen zwischen  [!DNL Analytics]  und Adobe Advertising](data-variances.md)
