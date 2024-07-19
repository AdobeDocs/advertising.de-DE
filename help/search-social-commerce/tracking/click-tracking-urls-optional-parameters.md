---
title: Optionale Tracking-Parameter für Klick-Tracking-URLs
description: Erfahren Sie mehr über optionale Tracking-Parameter für Search, Social und Commerce sowie über netzwerkspezifische Tracking-Parameter für Anzeigen, die Sie zu Ihren Klick-Tracking-URLs hinzufügen können.
exl-id: df53bb8c-63ad-47f9-af44-57bd4bd58d71
feature: Search Tracking
source-git-commit: f633f2af545f034b08b378653b4b967710402a03
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# Optionale Tracking-Parameter für Klick-Tracking-URLs

Nur die Konten *[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan] und [!DNL Yandex]*

Statt nur die Standard-Tracking-Parameter für eine endgültige URL oder Ziel-URL zu verwenden, können Sie weitere Parameter hinzufügen, um bestimmte Daten für ein Anzeigennetzwerkkonto zu verfolgen. Sie können eine beliebige Kombination der folgenden Parameter in den Kontoeinstellungen oder den Kampagneneinstellungen hinzufügen:

* Sie können jede statische Textzeichenfolge als Parameter in den Basis-URLs für das Konto/die Kampagne anhängen.

* Sie können netzwerkspezifische Adobe Advertising- und Anzeigenparameter an die Basis-URLs für das Konto/die Kampagne anhängen, um weitere Daten zu verfolgen:

   * Adobe Advertising-Parameter sind halbstatisch. Adobe Advertising fügt einen Datenwert ein, wenn die Basis-URL in das Werbenetzwerk hochgeladen wird. Wenn Sie beispielsweise `campaign={ef_campaign}` an die Basis-URL anhängen, ersetzt Adobe Advertising `{ef_campaign}` beim Hochladen der URL durch den tatsächlichen Kampagnennamen (z. B. &quot;Back-to-School-Campaign&quot;).

     **Hinweis:** Sobald die Werte eingefügt wurden, bleiben sie statisch. Wenn Sie einen Suchbegriff oder eine Anzeige in eine andere Anzeigengruppe verschieben oder die Anzeigengruppe in eine andere Kampagne verschieben, wird der Parameter {ef_adgroup} oder {ef_campaign} nicht automatisch aktualisiert. Daher müssen Sie manuell eine neue Ziel-URL oder eine Basis-URL (endgültige) generieren.

   * Netzwerkspezifische Anzeigenparameter sind dynamisch. Die Suchmaschine fügt einen Datenwert ein, wenn der Benutzer auf eine Anzeige klickt. Wenn Sie beispielsweise `{param1}` an die Basis-URL anhängen, ersetzt das Werbenetzwerk diese durch den tatsächlichen {param1} -Wert, wenn ein Endbenutzer auf die Anzeige klickt.

>[!NOTE]
>
>* Trennen Sie mehrere Parameter durch Kommas oder Und-Zeichen (`&`).
>* Bei den folgenden Parametern wird nicht zwischen Groß- und Kleinschreibung unterschieden.
>* Sonderzeichen in den angehängten Parametern werden in der generierten Ziel-URL oder Basis-URLl wie folgt ersetzt:
>  * `=` wird durch `%3D` ersetzt
>  * `?` wird durch `%26` ersetzt
>  * Ein leeres Leerzeichen wird durch `%2B` ersetzt.
>  Wenn Sie beispielsweise den Parameter `campaign={ef_campaign}` an die Basis-URL http://www.example.com für einen Suchbegriff anhängen, wird die Basis-URL für diesen Suchbegriff als `http://www.example.com/campaign%3D{ef_campaign}` generiert.

## statische Tracking-Parameter für Suche, Social und Commerce

Sie können die folgenden Parameter für Konten in jedem Werbenetzwerk verwenden und sie nach Bedarf mit Parametern für ein bestimmtes Werbenetzwerk kombinieren. Einige dieser Parameter duplizieren die Parameter, die automatisch für bestimmte Werbenetzwerke hinzugefügt werden, wenn die Tracking-Methode des Kontos &quot;[!UICONTROL EF Direct]&quot; lautet.

Alle folgenden Parameter müssen als Schlüssel-Wert-Paar angegeben werden. Sie können mehrere Parameter für ein Wertpaar einbeziehen. Verwenden Sie beispielsweise `<your_parameter_name>={ef_campaign}`, z. B. `campaign={ef_campaign}`, um den Kampagnennamen einzufügen. Um den Übereinstimmungstyp mit den angegebenen Übereinstimmungstypnamen einzufügen, verwenden Sie `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`, z. B. `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. Die nicht zutreffenden Übereinstimmungstypen werden nicht in der resultierenden URL angezeigt.

| Parameter | Beschreibung |
| ---- | ---- |
| <code>{custom_code}</code> | So fügen Sie Daten aus der Spalte &quot;Benutzerdefinierter URL-Parameter&quot;in eine hochgeladene Bulksheet-Datei in die Tracking-URL ein. {custom_code} darf nur am Ende des Werts eines oder mehrerer Schlüssel-Wert-Paare in der Tracking-URL verwendet werden. Beispiele: <code>a={custom_code}</code>; <code>a={ef_campaignid}{custom_code}</code>; <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>Hinweis:</b> Um den benutzerdefinierten Wert aus der Bulksheet-Datei in die Tracking-URL einzufügen, laden Sie die Bulksheet-Datei mit der Option &quot;Tracking-URLs generieren&quot;hoch. Weitere Informationen zur Verwendung von Bulksheet-Dateien finden Sie unter &quot;[Über die Verwaltung von Kampagnendaten mit Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)&quot;. |
| <code>{ef_uniqueid}</code> | So fügen Sie die von Adobe Advertising erstellte eindeutige ID ein. Wird automatisch hinzugefügt, wenn die Tracking-Methode &quot;EF-Umleitung&quot;lautet. |
| <code>{ef_userid}</code> | Fügen Sie die eindeutige Benutzer-ID ein, die Adobe Advertising dem Advertiser zuweist. |
| <code>{ef_sid}</code> | Fügen Sie die numerische ID ein, die Search, Social und Commerce dem Werbenetzwerk zuweist: <i>[!UICONTROL 3]</i> für [!DNL Google Ads], <i>[!UICONTROL 10]</i> für [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> für [!DNL Meta], <i>[!UICONTROL 86]</i> für [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> für [!DNL Naver], <i>[!UICONTROL 88]</i> für [!DNL Baidu], <i>[!UICONTROL 90]</i> für [!DNL Yandex], <i>[!UICONTROL 94]</i> für [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i>} für [!DNL Yahoo Native] (veraltet) oder <i>[!UICONTROL 106]</i> für [!DNL Pinterest] (veraltet). |
| <code>{ef_searchengine}</code> | So fügen Sie den Namen des Werbenetzwerks ein. |
| <code>{ef_campaign}</code> | Fügen Sie den Kampagnennamen ein. |
| <code>{ef_campaignid}</code> | Fügen Sie die Kampagnen-ID ein. <b>Hinweis:</b> Die Kennung für eine neue Kampagne wird erst erstellt, nachdem die Kampagne im Werbenetzwerk veröffentlicht wurde. Wenn das Konto die Optionen &quot;[!UICONTROL EF Redirect]&quot;und &quot;AutoUpload&quot;verwendet, fügt Adobe Advertising die Kampagnen-ID am nächsten Tag automatisch in die entsprechenden Ziel-URLs oder endgültigen URLs ein. Wenn das Konto nicht die Optionen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; verwendet und Sie die Kampagnen-ID in die entsprechenden Ziel-URLs oder endgültigen URLs einfügen möchten, müssen Sie die Kampagne erstellen, eine Bulksheet-Datei für die neue Kampagne herunterladen, mit der Option &quot;Tracking-URLs generieren&quot;und die Datei dann im Werbenetzwerk veröffentlichen. |
| <code>{ef_adgroup}</code> | So fügen Sie den Anzeigengruppennamen ein. |
| <code>{ef_adgroupid}</code> | So fügen Sie die Anzeigengruppen-ID ein. <b>Hinweis:</b> Die ID für eine neue Anzeigengruppe wird erst erstellt, nachdem die Anzeigengruppe im Anzeigennetzwerk veröffentlicht wurde. Wenn das Konto die Optionen &quot;[!UICONTROL EF Redirect]&quot;und &quot;AutoUpload&quot;verwendet, fügt Adobe Advertising die Anzeigengruppen-ID am nächsten Tag automatisch in die entsprechenden Ziel-URLs oder endgültigen URLs ein. Wenn das Konto nicht die Optionen[!UICONTROL EF Redirect] und [!UICONTROL Auto Upload] verwendet und Sie die Anzeigengruppen-ID in die entsprechenden Ziel-URLs oder endgültigen URLs einfügen möchten, müssen Sie die Anzeigengruppe erstellen, eine Bulksheet-Datei für die neue Anzeigengruppe herunterladen und die Option &quot;Tracking-URLs generieren&quot;verwenden und die Datei dann im Werbenetzwerk veröffentlichen. |
| <code>{ef_keyword}</code> | So fügen Sie den Suchbegriff ein. |
| <code>{ef_keywordid}</code> | So fügen Sie die Keyword-ID ein. <b>Hinweis:</b> Die ID für einen neuen Suchbegriff wird erst erstellt, nachdem der Suchbegriff im Werbenetzwerk veröffentlicht wurde. Wenn das Konto die Optionen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; verwendet, fügt Adobe Advertising am nächsten Tag automatisch die Suchbegriff-ID in die entsprechenden Ziel-URLs oder endgültigen URLs ein. Wenn das Konto nicht die Optionen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; verwendet und Sie die Suchbegriff-ID in die entsprechenden Ziel-URLs oder endgültigen URLs einfügen möchten, müssen Sie den Suchbegriff erstellen, eine Bulksheet-Datei für den neuen Suchbegriff herunterladen, mit der Option &quot;Tracking-URLs generieren&quot;und die Datei dann im Werbenetzwerk veröffentlichen. |
| <code>{ef_matchtype}</code> | So fügen Sie den Suchbegriff-Übereinstimmungstyp als &quot;Weit gefasst&quot;, &quot;Exakt&quot;oder &quot;Satz&quot;ein. Wird automatisch für [!DNL Google Ads] und [!DNL Microsoft Advertising] mit der Tracking-Methode &quot;[!UICONTROL EF Redirect]&quot; eingeschlossen. |
| <code>{ef_adid}</code> | So fügen Sie die Anzeigen-ID ein. <b>Hinweis:</b> Die ID für eine neue Anzeige wird erst erstellt, nachdem die Anzeige im Werbenetzwerk veröffentlicht wurde. Wenn das Konto die Optionen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; verwendet, fügt Adobe Advertising die Anzeigen-ID am nächsten Tag automatisch in die entsprechenden Ziel-URLs oder endgültigen URLs ein. Wenn das Konto nicht die Optionen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; verwendet und Sie die Anzeigen-ID in die entsprechenden Ziel-URLs oder endgültigen URLs einfügen möchten, müssen Sie die Anzeige erstellen, eine Bulksheet-Datei für die neue Anzeige herunterladen und die Option &quot;Tracking-URLs generieren&quot;verwenden und die Datei dann im Werbenetzwerk veröffentlichen. |

## [!DNL Google Ads] dynamische Tracking-Parameter

Siehe [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## [!DNL Microsoft Advertising] dynamische Tracking-Parameter

Siehe [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## Yahoo! Dynamische Tracking-Parameter für Japan Ads

Siehe [https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US).

## [!DNL Yandex] dynamische Tracking-Parameter

Siehe [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [Über Klick-Tracking-URL-Formate für den Adobe Advertising-Konversions-Tracking-Dienst](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
