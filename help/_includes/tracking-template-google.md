---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---
# Tracking-Vorlagenfeld für Google Ads-Entitäten

<!-- Search CRUD and bulk edit of Google entity settings -->

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
