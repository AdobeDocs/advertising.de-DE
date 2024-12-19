---
title: Optionale Tracking-Parameter für Klick-Tracking-URLs
description: Erfahren Sie mehr über die optionalen Tracking-Parameter für Suche, Social und Commerce und fügen Sie netzwerkspezifische Tracking-Parameter hinzu, die Sie Ihren Klick-Tracking-URLs hinzufügen können.
exl-id: df53bb8c-63ad-47f9-af44-57bd4bd58d71
feature: Search Tracking
source-git-commit: f633f2af545f034b08b378653b4b967710402a03
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# Optionale Tracking-Parameter für Klick-Tracking-URLs

Nur *[!DNL Google Ads]-, [!DNL Microsoft Advertising]-, [!DNL Yahoo! Japan]- und [!DNL Yandex] Konten*

Anstatt nur die standardmäßigen Tracking-Parameter für eine endgültige URL oder Ziel-URL zu verwenden, können Sie weitere Parameter hinzufügen, um bestimmte Daten für ein Werbenetzwerkkonto zu verfolgen. Sie können in den Konto- oder Kampagneneinstellungen eine beliebige Kombination der folgenden Parameter hinzufügen:

* Sie können jede beliebige statische Textzeichenfolge als Parameter in den Basis-URLs für das Konto/die Kampagne anhängen.

* Sie können netzwerkspezifische Adobe Advertising- und Anzeigenparameter in den Basis-URLs für das Konto/die Kampagne anhängen, um weitere Daten zu verfolgen:

   * Adobe Advertising-Parameter sind semistatisch. Adobe Advertising fügt beim Hochladen der Basis-URL in das Werbenetzwerk einen Datenwert ein. Wenn Sie beispielsweise `campaign={ef_campaign}` an die Basis-URL anhängen, ersetzt Adobe Advertising `{ef_campaign}` beim Hochladen der URL durch den tatsächlichen Kampagnennamen (z. B. „Zurück zur Schule - Kampagne„).

     **Hinweis:** Sobald die Werte eingefügt wurden, bleiben sie statisch. Wenn Sie ein Keyword oder eine Anzeige in eine andere Anzeigengruppe verschieben oder die Anzeigengruppe in eine andere Kampagne verschieben, wird der {ef_adgroup}- oder {ef_campaign}-Parameter nicht automatisch aktualisiert, sodass Sie manuell eine neue Ziel-URL oder Basis-URL (endgültige) generieren müssen.

   * Anzeigennetzwerkspezifische Parameter sind dynamisch und die Suchmaschine fügt einen Datenwert ein, wenn der Benutzer auf eine Anzeige klickt. Wenn Sie beispielsweise `{param1}` an die Basis-URL anhängen, ersetzt das Anzeigennetzwerk sie durch den tatsächlichen {param1}, wenn ein Endbenutzer auf die Anzeige klickt.

>[!NOTE]
>
>* Trennen Sie mehrere Parameter durch Kommas oder `&`.
>* Bei den folgenden Parametern wird nicht zwischen Groß- und Kleinschreibung unterschieden.
>* Sonderzeichen in den angehängten Parametern werden in der generierten Ziel-URL oder Basis-URL (final) wie folgt ersetzt:
>  * `=` wird durch `%3D` ersetzt
>  * `?` wird durch `%26` ersetzt
>  * Ein leeres Leerzeichen wird durch `%2B` ersetzt
>  Wenn Sie beispielsweise den Parameter `campaign={ef_campaign}` an die Basis-URL http://www.example.com für ein Keyword anhängen, wird die Basis-URL für dieses Keyword als `http://www.example.com/campaign%3D{ef_campaign}` generiert.

## Statische Tracking-Parameter für Suche, Social und Commerce

Sie können die folgenden Parameter für Konten in jedem Anzeigennetzwerk verwenden und sie bei Bedarf mit Parametern für ein bestimmtes Anzeigennetzwerk kombinieren. Einige dieser Parameter duplizieren die Parameter, die automatisch für bestimmte Werbenetzwerke hinzugefügt werden, wenn die Tracking-Methode des Kontos &quot;[!UICONTROL EF Direct]&quot; lautet.

Alle der folgenden Parameter müssen als Schlüssel-Wert-Paar angegeben werden. Sie können mehrere Parameter für ein Wertepaar einbeziehen. Um beispielsweise den Kampagnennamen einzufügen, verwenden Sie `<your_parameter_name>={ef_campaign}`, z. B. `campaign={ef_campaign}`. Um den Übereinstimmungstyp mit den angegebenen Namen des Übereinstimmungstyps einzufügen, verwenden Sie `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`, z. B. `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. Die nicht zutreffenden Übereinstimmungstypen werden nicht in der resultierenden URL angezeigt.

| Parameter | Beschreibung |
| ---- | ---- |
| <code>{custom_code}</code> | So fügen Sie Daten aus der Spalte „Benutzerdefinierter URL-Parameter“ in eine hochgeladene Bulksheet-Datei in die Tracking-URL ein. {custom_code} können nur am Ende des Werts von einem oder mehreren Schlüssel-Wert-Paaren in der Tracking-URL verwendet werden. Beispiele: <code>a={custom_code}</code>; <code>a={ef_campaignid}{custom_code}</code>; <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>Hinweis:</b> Um den benutzerdefinierten Wert aus der Bulksheet-Datei in die Tracking-URL einzufügen, laden Sie die Bulksheet-Datei mit der Option „Tracking-URLs generieren“ hoch. Weitere Informationen zur Verwendung von Bulksheet-Dateien finden Sie unter &quot;[ zur Verwaltung von Kampagnendaten mithilfe von Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md). |
| <code>{ef_uniqueid}</code> | So fügen Sie die vom Adobe Advertising erstellte eindeutige ID ein. Wird automatisch hinzugefügt, wenn die Tracking-Methode „EF Redirect“ lautet. |
| <code>{ef_userid}</code> | So fügen Sie die eindeutige Benutzer-ID ein, die Adobe Advertising dem Advertiser zuweist. |
| <code>{ef_sid}</code> | So fügen Sie die numerische ID ein, die Search, Social und Commerce dem Anzeigennetzwerk zuweist: <i>[!UICONTROL 3]</i> für [!DNL Google Ads], <i>[!UICONTROL 10]</i> für [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> für [!DNL Meta], <i>[!UICONTROL 86]</i> für [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> für [!DNL Naver], <i>[!UICONTROL 88]</i> für [!DNL Baidu], <i>[!UICONTROL 90]</i> für [!DNL Yandex], <i>[!UICONTROL 94]</i> für [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> für [!DNL Yahoo Native] (nicht mehr unterstützt) oder <i>[!UICONTROL 106]</i> für [!DNL Pinterest] (nicht mehr unterstützt). |
| <code>{ef_searchengine}</code> | So fügen Sie den Anzeigennetzwerknamen ein. |
| <code>{ef_campaign}</code> | So fügen Sie den Kampagnennamen ein. |
| <code>{ef_campaignid}</code> | Um die Kampagnen-ID einzufügen. <b>Hinweis:</b> Die ID für eine neue Kampagne wird erst erstellt, wenn die Kampagne im Werbenetzwerk gepostet wurde. Wenn das Konto die Optionen &quot;[!UICONTROL EF Redirect]&quot; und „AutoUpload“ verwendet, fügt Adobe Advertising die Kampagnen-ID am nächsten Tag automatisch in die entsprechenden Ziel-URLs oder endgültigen URLs ein. Wenn das Konto nicht die Optionen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; verwendet und Sie die Kampagnen-ID in die entsprechenden Ziel-URLs oder endgültigen URLs einfügen möchten, müssen Sie die Kampagne erstellen, eine Bulksheet-Datei für die neue Kampagne herunterladen und die Option zum Generieren von Tracking-URLs verwenden und die Datei dann im Werbenetzwerk posten. |
| <code>{ef_adgroup}</code> | So fügen Sie den Anzeigengruppennamen ein. |
| <code>{ef_adgroupid}</code> | So fügen Sie die Anzeigengruppen-ID ein. <b>Hinweis:</b> Die ID für eine neue Anzeigengruppe wird erst erstellt, wenn die Anzeigengruppe im Anzeigennetzwerk veröffentlicht wurde. Wenn das Konto die Optionen &quot;[!UICONTROL EF Redirect]&quot; und „AutoUpload“ verwendet, fügt Adobe Advertising die Anzeigengruppen-ID am nächsten Tag automatisch in die entsprechenden Ziel-URLs oder endgültigen URLs ein. Wenn das Konto nicht die Optionen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; verwendet und Sie die Anzeigengruppen-ID in die entsprechenden Ziel-URLs oder endgültigen URLs einfügen möchten, müssen Sie die Anzeigengruppe erstellen, eine Bulksheet-Datei für die neue Anzeigengruppe herunterladen und die Option zum Generieren von Tracking-URLs verwenden und die Datei dann im Anzeigennetzwerk posten. |
| <code>{ef_keyword}</code> | Um das Keyword einzufügen. |
| <code>{ef_keywordid}</code> | So fügen Sie die Keyword-ID ein. <b>Hinweis:</b> Die ID für ein neues Keyword wird erst erstellt, wenn das Keyword im Anzeigennetzwerk veröffentlicht wird. Wenn das Konto die Optionen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; verwendet, fügt Adobe Advertising am nächsten Tag automatisch die Keyword-ID in die entsprechenden Ziel-URLs oder endgültigen URLs ein. Wenn das Konto nicht die Optionen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; verwendet und Sie die Keyword-ID in die relevanten Ziel-URLs oder endgültigen URLs einfügen möchten, müssen Sie das Keyword erstellen, eine Bulksheet-Datei für das neue Keyword herunterladen und die Option zum Generieren von Tracking-URLs verwenden und dann die Datei im Anzeigennetzwerk posten. |
| <code>{ef_matchtype}</code> | Um den Übereinstimmungstyp des Keywords als „Grob“, „Exakt“ oder „Phrase“ einzufügen. Automatisch für [!DNL Google Ads] und [!DNL Microsoft Advertising] mit der Tracking-Methode &quot;[!UICONTROL EF Redirect]&quot; enthalten. |
| <code>{ef_adid}</code> | So fügen Sie die Werbe-ID ein. <b>Hinweis:</b> Die ID für eine neue Anzeige wird erst erstellt, wenn die Anzeige im Werbenetzwerk gepostet wurde. Wenn das Konto die Optionen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; verwendet, fügt Adobe Advertising die Werbe-ID am nächsten Tag automatisch in die entsprechenden Ziel-URLs oder endgültigen URLs ein. Wenn das Konto nicht die Optionen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; verwendet und Sie die Anzeigen-ID in die entsprechenden Ziel-URLs oder endgültigen URLs einfügen möchten, müssen Sie die Anzeige erstellen, eine Bulksheet-Datei für die neue Anzeige herunterladen und die Option zum Generieren von Tracking-URLs verwenden und die Datei dann im Anzeigennetzwerk posten. |

## Dynamische Tracking-Parameter [!DNL Google Ads]

Siehe [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## Dynamische Tracking-Parameter [!DNL Microsoft Advertising]

Siehe [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## Yahoo! Dynamische Tracking-Parameter für Japan Ads

Siehe [https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US).

## Dynamische Tracking-Parameter [!DNL Yandex]

Siehe [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [Über Klick-Tracking-URL-Formate für den Adobe Advertising-Konversionsverfolgungs-Service](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
