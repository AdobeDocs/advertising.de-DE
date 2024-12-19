---
source-git-commit: 38d6d70d03c12aab1a7caee6e589a2fdeaf78ad4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---
# Feld „Tracking-Vorlage“ für Microsoft Advertising-Entitäten

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Optional, nicht für alle Entitäten verfügbar) Die Tracking-Vorlage oder Tracking-URL, die alle Weiterleitungs- und Tracking-Parameter für Off-Landing-Domains angibt und außerdem die endgültige/Landingpage-URL in einen Parameter einbettet. Beispiel: `{lpurl}?source={network}&id=5` oder `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`, um eine Umleitung einzuschließen.

Beim Adobe Advertising-Konversions-Tracking, das angewendet wird, wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; enthalten, stellt Search, Social und Commerce beim Speichern des Datensatzes automatisch einen eigenen Umleitungs- und Trackingcode als Präfix voran.

* Informationen zu den unterstützten Parametern zum Einbetten der endgültigen URL finden Sie in der [[!DNL Microsoft Advertising] Dokumentation zu Parametern zur Angabe der endgültigen URL](https://help.ads.microsoft.com/#apex/3/en/56799).

* Sie können optional URL-Parameter und beliebige benutzerdefinierte Parameter einbeziehen, die für die Kampagne definiert wurden und durch kaufmännische Und-Zeichen (&amp;) getrennt sind, z. B. {lpurl}?matchType={matchtype}&amp;device={device}.

* Optional können Sie Umleitungen und Tracking von Drittanbietern hinzufügen.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* Die Tracking-Vorlage auf der detailliertesten Ebene überschreibt die Werte auf allen höheren Ebenen. Wenn beispielsweise sowohl die Kontoeinstellungen als auch die Keyword-Einstellungen einen Wert enthalten, wird der Keyword-Wert angewendet.
>* Sie können Ihre Tracking-Vorlagen auf jeder Ebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.
