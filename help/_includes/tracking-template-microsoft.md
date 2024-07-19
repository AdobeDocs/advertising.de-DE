---
source-git-commit: 38d6d70d03c12aab1a7caee6e589a2fdeaf78ad4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---
# Tracking-Vorlagenfeld für Microsoft Advertising-Entitäten

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Optional; nicht für alle Entitäten verfügbar) Die Tracking-Vorlage oder die Tracking-URL, die alle Off-Landingpage-Umleitungen und Tracking-Parameter angibt und außerdem die finale URL/Landingpage in einen Parameter einbettet. Beispiel: `{lpurl}?source={network}&id=5` oder `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` , um eine Umleitung einzuschließen.

Beim Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot;und &quot;[!UICONTROL Auto Upload]&quot;enthalten, präfixiert Search, Social und Commerce beim Speichern des Datensatzes automatisch seinen eigenen Umleitungs- und Trackingcode.

* Informationen zu unterstützten Parametern zum Einbetten der endgültigen URL finden Sie in der [[!DNL Microsoft Advertising] Dokumentation zu Parametern, die die endgültige URL angeben](https://help.ads.microsoft.com/#apex/3/en/56799).

* Sie können optional URL-Parameter und alle für die Kampagne definierten benutzerdefinierten Parameter einbeziehen, getrennt durch das kaufmännische Und-Zeichen (&amp;), z. B. {lpurl}?matchtype={matchtype}&amp;device={device}.

* Sie können optional Umleitungen und Tracking von Drittanbietern hinzufügen.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* Die Tracking-Vorlage auf der detailliertesten Ebene überschreibt die Werte auf allen höheren Ebenen. Wenn beispielsweise sowohl die Kontoeinstellungen als auch die Suchbegriffeinstellungen einen Wert enthalten, wird der Suchbegriffwert angewendet.
>* Sie können Ihre Tracking-Vorlagen auf jeder Ebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.
