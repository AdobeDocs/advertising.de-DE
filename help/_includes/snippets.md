---
source-git-commit: 92bf7768be91e75f029e1577c7f4e7e790c5a934
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---
# Snippets

## Tracking-Vorlagenfeld für Google Ads-Entitäten {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

**[!UICONTROL Tracking Template]:** (Optional) Die Tracking-Vorlage oder die Tracking-URL, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die finale URL/Landingpage in einen [!DNL ValueTrack] -Parameter einbettet. Beispiel: `{lpurl}?source={network}&id=5` oder `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` , um eine Umleitung einzuschließen.

Beim Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot;und &quot;[!UICONTROL Auto Upload]&quot;enthalten, präfixiert Search, Social und Commerce beim Speichern des Datensatzes automatisch seinen eigenen Umleitungs- und Trackingcode.

* Informationen zu unterstützten Parametern zum Einbetten der endgültigen URL finden Sie in der [[!DNL Google Ads] Dokumentation für die unterstützten [!DNL ValueTrack] Formate](https://support.google.com/google-ads/answer/6305348). (Navigieren Sie zu den Parametern &quot;Nur Tracking-Vorlage&quot; im Abschnitt &quot;Verfügbare [!DNL ValueTrack] Parameter&quot;.)

* Sie können optional URL-Parameter und alle für die Kampagne definierten benutzerdefinierten Parameter einbeziehen, getrennt durch das kaufmännische Und-Zeichen (&amp;), z. B. {lpurl}?matchtype={matchtype}&amp;device={device}.

* Sie können optional Umleitungen und Tracking von Drittanbietern hinzufügen.

>[!NOTE]
>
>* Vermeiden Sie die Verwendung von Makros, die nicht durch Klicks aus Quellen ersetzt werden, die das parallele Tracking ermöglichen. Wenn der Advertiser Makros verwenden muss, sollte das Adobe Account-Team mit dem Support oder dem Implementierungsteam zusammenarbeiten, um sie hinzuzufügen.
>* Die Tracking-Vorlage auf der detailliertesten Ebene überschreibt die Werte auf allen höheren Ebenen. Wenn beispielsweise sowohl die Kontoeinstellungen als auch die Suchbegriffeinstellungen einen Wert enthalten, wird der Suchbegriffwert angewendet.
>* Wenn Sie eine Tracking-Vorlage auf Anzeigen-, Sitelink- oder Suchbegriffebene aktualisieren, werden die relevanten Anzeigen erneut zur Überprüfung eingereicht. Sie können Ihre Tracking-Vorlagen auf Konto-, Kampagnen- oder Anzeigengruppenebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.

## Tracking-Vorlagenfeld für [!DNL Microsoft Advertising] Entitäten {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Optional) Die Tracking-Vorlage oder die Tracking-URL, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die finale URL/Landingpage in einen Parameter einbettet. Beispiel: `{lpurl}?source={network}&id=5` oder `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` , um eine Umleitung einzuschließen.

Beim Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot;und &quot;[!UICONTROL Auto Upload]&quot;enthalten, präfixiert Search, Social und Commerce beim Speichern des Datensatzes automatisch seinen eigenen Umleitungs- und Trackingcode.

* Informationen zu unterstützten Parametern zum Einbetten der endgültigen URL finden Sie in der [[!DNL Microsoft Advertising] Dokumentation zu Parametern, die die endgültige URL angeben](https://help.ads.microsoft.com/#apex/3/en/56799).

* Sie können optional URL-Parameter und alle für die Kampagne definierten benutzerdefinierten Parameter einbeziehen, getrennt durch das kaufmännische Und-Zeichen (&amp;), z. B. {lpurl}?matchtype={matchtype}&amp;device={device}.

* Sie können optional Umleitungen und Tracking von Drittanbietern hinzufügen.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* Die Tracking-Vorlage auf der detailliertesten Ebene überschreibt die Werte auf allen höheren Ebenen. Wenn beispielsweise sowohl die Kontoeinstellungen als auch die Suchbegriffeinstellungen einen Wert enthalten, wird der Suchbegriffwert angewendet.
>* Sie können Ihre Tracking-Vorlagen auf jeder Ebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.

## Text und Vorlage - Hinweis zum Einfügen eines dynamischen Parameters {#inventory-feed-template-insert-dynamic-parameter}

Um einen Spaltennamen oder eine Modifikatorgruppe als dynamischen Parameter einzufügen, klicken Sie in das Eingabefeld und klicken Sie dann in der Spaltenliste auf einen Spaltennamen oder in der Modifikatorliste auf einen [Modifikatornamen](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) . Geben Sie zum Einfügen der Variablen [!DNL Param1] oder [!DNL Param2] den Wert `{param1:default text}` oder `{param2:default text}` ein, wobei &quot;Standardtext&quot;Text ist, der verwendet wird, wenn die Parameterspalte in der Feed-Datei für eine Anzeigenzeile leer ist.

## Text-Anzeigenvorlage - Hinweis zum Einfügen eines Anzeigenanpassers {#inventory-feed-template-insert-ad-customizer}

Verwenden Sie zum Einfügen eines Anzeigenanpassers die folgenden Formate, wobei `Default text` ein optionaler Wert ist, der eingefügt werden soll, wenn Ihre Feed-Datei keinen gültigen Wert enthält:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, z. B. `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, z. B. `{CUSTOMIZER.Discount:10%}`
