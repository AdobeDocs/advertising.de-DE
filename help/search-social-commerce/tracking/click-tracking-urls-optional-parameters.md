---
title: Optionale Tracking-Parameter für Klick-Tracking-URLs
description: Erfahren Sie mehr über optionale Tracking-Parameter für Suche, Social und Commerce sowie über netzwerkspezifische Tracking-Parameter für Anzeigen, die Sie zu Ihren Klick-Tracking-URLs hinzufügen können.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 0%

---

# Optionale Tracking-Parameter für Klick-Tracking-URLs

*Google Ads, Microsoft Advertising und Yahoo! Nur Japan*

Statt nur die Standard-Tracking-Parameter für eine endgültige URL oder Ziel-URL zu verwenden, können Sie weitere Parameter hinzufügen, um bestimmte Daten für ein Anzeigennetzwerkkonto zu verfolgen. Sie können eine beliebige Kombination der folgenden Parameter in den Kontoeinstellungen oder den Kampagneneinstellungen hinzufügen:

* Sie können jede statische Textzeichenfolge als Parameter in den Basis-URLs für das Konto/die Kampagne anhängen.

* Sie können Adobe Advertising- und Anzeigen-Netzwerkparameter an die Basis-URLs für das Konto/die Kampagne anhängen, um weitere Daten zu verfolgen:

   * Adobe Advertising-Parameter sind halbstatisch. Adobe Advertising fügt einen Datenwert ein, wenn die Basis-URL in das Werbenetzwerk hochgeladen wird. Wenn Sie beispielsweise `campaign={ef_campaign}` zur Basis-URL ersetzt Adobe Advertising `{ef_campaign}` mit dem tatsächlichen Kampagnennamen (z. B. &quot;Back-to-School-Campaign&quot;) beim Hochladen der URL.

      **Hinweis:** Nach dem Einfügen bleiben die Werte statisch. Wenn Sie einen Suchbegriff oder eine Anzeige in eine andere Anzeigengruppe verschieben oder die Anzeigengruppe in eine andere Kampagne verschieben, wird der Parameter {ef_adgroup} oder {ef_campaign} nicht automatisch aktualisiert. Daher müssen Sie manuell eine neue Ziel-URL oder Basis-URL (endgültig) generieren.

   * Netzwerkspezifische Anzeigenparameter sind dynamisch. Die Suchmaschine fügt einen Datenwert ein, wenn der Benutzer auf eine Anzeige klickt. Wenn Sie beispielsweise `{param1}` zur Basis-URL hinzufügen, ersetzt das Werbenetzwerk sie durch den tatsächlichen {param1} -Wert, wenn ein Endbenutzer auf die Anzeige klickt.

>[!NOTE]
>
>* Trennen Sie mehrere Parameter durch Kommas oder Und-Zeichen (`&`).
>* Bei den folgenden Parametern wird nicht zwischen Groß- und Kleinschreibung unterschieden.
>* Sonderzeichen in den angehängten Parametern werden in der generierten Ziel-URL oder Basis-URLl wie folgt ersetzt:
>  * `=` ersetzt durch `%3D`
>  * `?` ersetzt durch `%26`
>  * Ein leeres Leerzeichen wird durch `%2B`

   >  Wenn Sie beispielsweise den Parameter anhängen `campaign={ef_campaign}` zur Basis-URL http://www.example.com für einen Suchbegriff hinzu, wird die Basis-URL für diesen Suchbegriff als `http://www.example.com/campaign%3D{ef_campaign}`.


## statische Tracking-Parameter für Suche, Social und Commerce

Sie können die folgenden Parameter für Konten in jedem Werbenetzwerk verwenden und sie nach Bedarf mit Parametern für ein bestimmtes Werbenetzwerk kombinieren. Einige dieser Parameter duplizieren die Parameter, die automatisch für bestimmte Werbenetzwerke hinzugefügt werden, wenn die Tracking-Methode des Kontos lautet.[!UICONTROL EF Direct].&quot;

Alle folgenden Parameter müssen als Schlüssel-Wert-Paar angegeben werden. können Sie mehrere Parameter für ein Wertpaar einbeziehen. Verwenden Sie beispielsweise zum Einfügen des Kampagnennamens `<your_parameter_name>={ef_campaign}`, z. B. `campaign={ef_campaign}`. Verwenden Sie zum Einfügen des Übereinstimmungstyps mit den angegebenen Übereinstimmungstypnamen die `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`, z. B. `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. Die nicht zutreffenden Übereinstimmungstypen werden nicht in der resultierenden URL angezeigt.

| Parameter | Beschreibung |
| ---- | ---- |
| {custom_code}</code> | So fügen Sie Daten aus der Spalte &quot;Benutzerdefinierter URL-Parameter&quot;in eine hochgeladene Bulksheet-Datei in die Tracking-URL ein. {custom_code} darf nur am Ende des Werts eines oder mehrerer Schlüssel-Wert-Paare in der Tracking-URL verwendet werden. Beispiele: a={custom_code}</code>; a={ef_campaignid}{custom_code}</code>; a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>Hinweis:</b> Um den benutzerdefinierten Wert aus der Bulksheet-Datei in die Tracking-URL einzufügen, laden Sie die Bulksheet-Datei mit der Option &quot;Tracking-URLs generieren&quot;hoch. Weitere Informationen zur Verwendung von Bulksheet-Dateien finden Sie unter[Verwalten von Kampagnendaten mithilfe von Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot; |
| {ef_uniqueid}</code> | So fügen Sie die eindeutige ID ein, die von Adobe Advertising erstellt wurde. Wird automatisch hinzugefügt, wenn die Tracking-Methode &quot;EF-Umleitung&quot;lautet. |
| {ef_userid}</code> | Fügen Sie die eindeutige Benutzer-ID ein, die Adobe Advertising dem Advertiser zuweist. |
| {ef_sid}</code> | So fügen Sie die numerische ID ein, die Search, Social und Commerce dem Werbenetzwerk zuweist: <i>[!UICONTROL 3]</i> für [!DNL Google Ads], <i>[!UICONTROL 10]</i> für [!DNL Microsoft® Advertising], <i>[!UICONTROL 45]</i> für [!DNL Meta], <i>[!UICONTROL 86]</i> für [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> für [!DNL Naver], <i>[!UICONTROL 88]</i> für [!DNL Baidu], <i>[!UICONTROL 90]</i> für [!DNL Yandex], <i>[!UICONTROL 94]</i> für [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> für [!DNL Yahoo Native] (veraltet) oder <i>[!UICONTROL 106]</i> für [!DNL Pinterest] (nicht mehr unterstützt). |
| {ef_searchengine}</code> | So fügen Sie den Namen des Werbenetzwerks ein. |
| {ef_campaign}</code> | Fügen Sie den Kampagnennamen ein. |
| {ef_campaignid}</code> | Fügen Sie die Kampagnen-ID ein. <b>Hinweis:</b> Die Kennung für eine neue Kampagne wird erst erstellt, nachdem die Kampagne im Werbenetzwerk veröffentlicht wurde. Wenn das Konto die Optionen &quot;EF Redirect&quot;und &quot;AutoUpload&quot;verwendet, fügt Adobe Advertising die Kampagnen-ID am nächsten Tag automatisch in die entsprechenden Ziel-URLs oder endgültigen URLs ein. Wenn das Konto nicht die Optionen &quot;EF Redirect&quot;und &quot;Auto Upload&quot;verwendet und Sie die Kampagnen-ID in die entsprechenden Ziel-URLs oder endgültigen URLs einfügen möchten, müssen Sie die Kampagne erstellen. Laden Sie eine Bulksheet-Datei für die neue Kampagne herunter, verwenden Sie die Option &quot;Tracking-URLs generieren&quot;, und posten Sie dann die Datei im Werbenetzwerk. |
| {ef_adgroup}</code> | So fügen Sie den Anzeigengruppennamen ein. |
| {ef_adgroupid}</code> | So fügen Sie die Anzeigengruppen-ID ein. <b>Hinweis:</b> Die ID für eine neue Anzeigengruppe wird erst erstellt, wenn die Anzeigengruppe im Werbenetzwerk veröffentlicht wurde. Wenn das Konto die Optionen &quot;EF Redirect&quot;und &quot;AutoUpload&quot;verwendet, fügt Adobe Advertising die Anzeigengruppen-ID am nächsten Tag automatisch in die entsprechenden Ziel-URLs oder endgültigen URLs ein. Wenn das Konto nicht die Optionen &quot;EF Redirect&quot;und &quot;Auto Upload&quot;verwendet und Sie die Anzeigengruppen-ID in die relevanten Ziel-URLs oder endgültigen URLs einfügen möchten, müssen Sie die Anzeigengruppe erstellen. Laden Sie eine Bulksheet-Datei für die neue Anzeigengruppe herunter, verwenden Sie die Option &quot;Tracking-URLs generieren&quot;, und posten Sie dann die Datei im Werbenetzwerk. |
| {ef_keyword}</code> | So fügen Sie den Suchbegriff ein. |
| {ef_keywordid}</code> | So fügen Sie die Keyword-ID ein. <b>Hinweis:</b> Die ID für einen neuen Suchbegriff wird erst erstellt, nachdem der Suchbegriff im Werbenetzwerk veröffentlicht wurde. Wenn das Konto die Optionen &quot;EF Redirect&quot;und &quot;Auto Upload&quot;verwendet, fügt Adobe Advertising die Suchbegriff-ID am nächsten Tag automatisch in die entsprechenden Ziel-URLs oder endgültigen URLs ein. Wenn das Konto nicht die Optionen &quot;EF Redirect&quot;und &quot;Auto Upload&quot;verwendet und Sie die Suchbegriff-ID in die entsprechenden Ziel-URLs oder endgültigen URLs einfügen möchten, müssen Sie den Suchbegriff erstellen. Laden Sie eine Bulksheet-Datei für den neuen Suchbegriff herunter, verwenden Sie die Option &quot;Tracking-URLs generieren&quot;, und posten Sie dann die Datei im Werbenetzwerk. |
| {ef_matchtype}</code> | So fügen Sie den Suchbegriff-Übereinstimmungstyp als &quot;Weit gefasst&quot;, &quot;Exakt&quot;oder &quot;Satz&quot;ein. Wird automatisch für Google Ads und Microsoft Advertising mit der Tracking-Methode &quot;EF Redirect&quot;integriert. |
| {ef_adid}</code> | So fügen Sie die Anzeigen-ID ein. <b>Hinweis:</b> Die ID für eine neue Anzeige wird erst erstellt, nachdem die Anzeige im Werbenetzwerk veröffentlicht wurde. Wenn das Konto die Optionen &quot;EF Redirect&quot;und &quot;Auto Upload&quot;verwendet, fügt Adobe Advertising die Anzeigen-ID am nächsten Tag automatisch in die entsprechenden Ziel-URLs oder endgültigen URLs ein. Wenn das Konto nicht die Optionen &quot;EF Redirect&quot;und &quot;Auto Upload&quot;verwendet und Sie die Anzeigen-ID in die relevanten Ziel-URLs oder endgültigen URLs einfügen möchten, müssen Sie die Anzeige erstellen. Laden Sie eine Bulksheet-Datei für die neue Anzeige herunter, verwenden Sie die Option &quot;Tracking-URLs generieren&quot;, und posten Sie dann die Datei im Werbenetzwerk. |

## Dynamische Tracking-Parameter für Google Ads

Siehe [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## Dynamische Tracking-Parameter für Microsoft Advertising

Siehe [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## Native Yahoo-Parameter für dynamisches Tracking

Siehe [https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters](https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters).

## Yahoo! Dynamische Tracking-Parameter für Japan Ads

Siehe [https://help.marketing.yahoo.co.jp/en/?p=115](https://help.marketing.yahoo.co.jp/en/?p=115).

## Dynamische Tracking-Parameter von Yandex

Siehe [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [Über Klick-Tracking-URL-Formate für den Adobe Advertising-Konversions-Tracking-Dienst](/help/search-social-commerce/tracking/formats-click-tracking-about.md)

