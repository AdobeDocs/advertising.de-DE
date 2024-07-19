---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---
# Feld für Tracking-Vorlage für Yahoo! Japan Ads-Entitäten

<!-- Search CRUD and bulk edit of Yahoo! Japan Ads entity settings -->

**[!UICONTROL Tracking Template]:** (Optional) Die Tracking-Vorlage oder die Tracking-URL, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die finale URL/Landingpage in einen Parameter einbettet. Verwenden Sie den Parameter `!{lpurl}`, um die URL der Landingpage anzugeben. Beispiel: `{lpurl}?source={network}&id=5` oder `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` , um eine Umleitung einzuschließen.

Sie können optional Umleitungen und Tracking von Drittanbietern hinzufügen.

Beim Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot;und &quot;[!UICONTROL Auto Upload]&quot;enthalten, präfixiert Search, Social und Commerce beim Speichern des Datensatzes automatisch seinen eigenen Umleitungs- und Trackingcode.

>[!NOTE]
>
>* Die Tracking-Vorlage auf der detailliertesten Ebene überschreibt die Werte auf allen höheren Ebenen. Wenn beispielsweise sowohl die Kontoeinstellungen als auch die Suchbegriffeinstellungen einen Wert enthalten, wird der Suchbegriffwert angewendet.
>* Sie können Ihre Tracking-Vorlagen auf jeder Ebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.
