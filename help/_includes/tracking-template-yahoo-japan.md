---
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---
# Feld „Tracking-Vorlage“ für [!DNL LY Ads] Entitäten

<!-- Search CRUD and bulk edit of LY Ads entity settings -->

**[!UICONTROL Tracking Template]:** (Optional) Die Tracking-Vorlage oder Tracking-URL, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und auch die endgültige/Landingpage-URL in einen Parameter einbettet. Verwenden Sie den `!{lpurl}`, um die Landingpage-URL anzugeben. Beispiel: `{lpurl}?source={network}&id=5` oder `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`, um eine Umleitung einzuschließen.

Optional können Sie Umleitungen und Tracking von Drittanbietern hinzufügen.

Bei Adobe Advertising-Konversionsverfolgung, die angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; enthalten, stellt Search, Social und Commerce beim Speichern des Datensatzes automatisch einen eigenen Umleitungs- und Trackingcode voran.

>[!NOTE]
>
>* Die Tracking-Vorlage auf der detailliertesten Ebene überschreibt die Werte auf allen höheren Ebenen. Wenn beispielsweise sowohl die Kontoeinstellungen als auch die Keyword-Einstellungen einen Wert enthalten, wird der Keyword-Wert angewendet.
>* Sie können Ihre Tracking-Vorlagen auf jeder Ebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.
