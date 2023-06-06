---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---
# Tracking-Vorlagenfeld für Microsoft Advertising-Entitäten

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Optional) Die Tracking-Vorlage oder Tracking-URL, die alle Off-Landing-Domain-Umleitungen und Tracking-Parameter angibt und die finale/Landingpage-URL in einen Parameter einbettet. Beispiel: `{lpurl}?source={network}&id=5` oder `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` , um eine Umleitung einzuschließen.

Für das Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload],&quot;&quot;Search, Social und Commerce setzt beim Speichern des Datensatzes automatisch einen eigenen Umleitungs- und Trackingcode voran.

* Informationen zu unterstützten Parametern zum Einbetten der endgültigen URL finden Sie in der [[!DNL Microsoft Advertising] Dokumentation zu Parametern zur Angabe der endgültigen URL](https://help.ads.microsoft.com/#apex/3/en/56799).

* Sie können optional URL-Parameter und alle für die Kampagne definierten benutzerdefinierten Parameter einbeziehen, getrennt durch das kaufmännische Und-Zeichen (&amp;), z. B. {lpurl}?matchtype={matchtype}&amp;device={device}.

* Sie können optional Umleitungen und Tracking von Drittanbietern hinzufügen.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* Die Tracking-Vorlage auf der detailliertesten Ebene überschreibt die Werte auf allen höheren Ebenen. Wenn beispielsweise sowohl die Kontoeinstellungen als auch die Suchbegriffeinstellungen einen Wert enthalten, wird der Suchbegriffwert angewendet.
>* Sie können Ihre Tracking-Vorlagen auf jeder Ebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.

