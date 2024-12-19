---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---
# Feld „Tracking-Vorlage“ für Google Ads-Entitäten

<!-- Search CRUD and bulk edit of Google entity settings -->

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
