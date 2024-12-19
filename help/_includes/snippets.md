---
source-git-commit: 92bf7768be91e75f029e1577c7f4e7e790c5a934
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---
# Snippets

## Feld „Tracking-Vorlage“ für Google Ads-Entitäten {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

**[!UICONTROL Tracking Template]:** (Optional) Die Tracking-Vorlage oder Tracking-URL, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und außerdem die endgültige Landingpage-URL in einen [!DNL ValueTrack] einbettet. Beispiel: `{lpurl}?source={network}&id=5` oder `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`, um eine Umleitung einzuschließen.

Beim Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; enthalten, stellt Search, Social und Commerce beim Speichern des Datensatzes automatisch einen eigenen Umleitungs- und Trackingcode als Präfix voran.

* Informationen zu den unterstützten Parametern zum Einbetten der endgültigen URL finden Sie unter [[!DNL Google Ads] Dokumentation für die unterstützten  [!DNL ValueTrack] -Formate](https://support.google.com/google-ads/answer/6305348). (Gehen Sie zu den Parametern „Nur Tracking-Vorlage“ im Abschnitt „Verfügbare [!DNL ValueTrack]&quot;.)

* Sie können optional URL-Parameter und beliebige benutzerdefinierte Parameter einbeziehen, die für die Kampagne definiert wurden und durch kaufmännische Und-Zeichen (&amp;) getrennt sind, z. B. {lpurl}?matchType={matchtype}&amp;device={device}.

* Optional können Sie Umleitungen und Tracking von Drittanbietern hinzufügen.

>[!NOTE]
>
>* Verwenden Sie keine Makros, da diese nicht durch Klicks aus Quellen ersetzt werden, die paralleles Tracking ermöglichen. Wenn der Werbetreibende Makros verwenden muss, sollte das Adobe-Account-Team den Support oder das Implementierungsteam kontaktieren, um diese hinzuzufügen.
>* Die Tracking-Vorlage auf der detailliertesten Ebene überschreibt die Werte auf allen höheren Ebenen. Wenn beispielsweise sowohl die Kontoeinstellungen als auch die Keyword-Einstellungen einen Wert enthalten, wird der Keyword-Wert angewendet.
>* Wenn Sie eine Tracking-Vorlage auf Anzeigen-, Sitelink- oder Keyword-Ebene aktualisieren, werden die entsprechenden Anzeigen erneut zur Überprüfung eingereicht. Sie können Ihre Tracking-Vorlagen auf Konto-, Kampagnen- oder Anzeigengruppenebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.

## Feld „Tracking-Vorlage“ für [!DNL Microsoft Advertising] Entitäten {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Optional) Die Tracking-Vorlage oder Tracking-URL, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und auch die endgültige/Landingpage-URL in einen Parameter einbettet. Beispiel: `{lpurl}?source={network}&id=5` oder `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`, um eine Umleitung einzuschließen.

Beim Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; enthalten, stellt Search, Social und Commerce beim Speichern des Datensatzes automatisch einen eigenen Umleitungs- und Trackingcode als Präfix voran.

* Informationen zu den unterstützten Parametern zum Einbetten der endgültigen URL finden Sie in der [[!DNL Microsoft Advertising] Dokumentation zu Parametern zur Angabe der endgültigen URL](https://help.ads.microsoft.com/#apex/3/en/56799).

* Sie können optional URL-Parameter und beliebige benutzerdefinierte Parameter einbeziehen, die für die Kampagne definiert wurden und durch kaufmännische Und-Zeichen (&amp;) getrennt sind, z. B. {lpurl}?matchType={matchtype}&amp;device={device}.

* Optional können Sie Umleitungen und Tracking von Drittanbietern hinzufügen.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* Die Tracking-Vorlage auf der detailliertesten Ebene überschreibt die Werte auf allen höheren Ebenen. Wenn beispielsweise sowohl die Kontoeinstellungen als auch die Keyword-Einstellungen einen Wert enthalten, wird der Keyword-Wert angewendet.
>* Sie können Ihre Tracking-Vorlagen auf jeder Ebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.

## Text und Vorlage - Hinweis zum Einfügen eines dynamischen Parameters {#inventory-feed-template-insert-dynamic-parameter}

Um einen Spaltennamen oder eine Modifikatorgruppe als dynamischen Parameter einzufügen, klicken Sie in das Eingabefeld, und klicken Sie dann auf einen Spaltennamen in der Spaltenliste oder auf einen [Modifikatornamen](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) in der Modifikatorliste. Um die Variable [!DNL Param1] oder [!DNL Param2] einzufügen, geben Sie den Wert `{param1:default text}` oder `{param2:default text}` ein, wobei „Standardtext“ Text ist, der verwendet wird, wenn die Parameterspalte in der Feed-Datei für eine Anzeigenzeile leer ist.

## Text-Anzeigenvorlage - Hinweis zum Einfügen eines Anzeigenanpassers {#inventory-feed-template-insert-ad-customizer}

Verwenden Sie zum Einfügen einer Anzeigenanpassung die folgenden Formate, wobei `Default text` ein optionaler Wert ist, der eingefügt wird, wenn Ihre Feed-Datei keinen gültigen Wert enthält:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, z. B. `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, z. B. `{CUSTOMIZER.Discount:10%}`
