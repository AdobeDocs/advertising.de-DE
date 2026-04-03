---
title: '[!DNL Google Analytics] Datenquelleneinstellungen'
description: Referenzieren Sie die erforderlichen Einstellungen für  [!DNL Google Analytics]  Datenquellen.
role: User, Admin
exl-id: 78422c2c-ed58-410e-8996-882759ed5556
feature: Search Data Sources
TQID: https://experienceleague.adobe.com/EvCJTrEFxRU87kUlKCZ-rN3jtNVjSkVGmrHCNsPMElw
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 799
ht-degree: 0%

---

# [!DNL Google Analytics] Datenquelleneinstellungen

| Abschnitt | Parameter | Beschreibung |
| ---- | ---- | ---- |
| [!UICONTROL Connect to Google Analytics] | [!UICONTROL Google Analytics Account ID] | Die ID des [!DNL Google Analytics] Kontos, von dem Daten abgerufen werden. Alle API-Nutzungen zum Abrufen von Daten werden dem angegebenen Konto in Rechnung gestellt. Das Konto muss der angegebenen E-Mail-Adresse die Berechtigung „Lesen und Analysieren“ erteilen.<br><br>Um Ihre ID zu finden, melden Sie sich bei [!DNL Google Analytics] an. Klicken Sie oben links auf **[!DNL All accounts]** , um eine Liste Ihrer Konten zu öffnen. Die ID für jedes Konto befindet sich unter dem Kontonamen. |
| | [!UICONTROL Google Analytics Login] | Geben Sie die Anmelde-/E-Mail-Adresse an, die für den Zugriff auf Daten für diese Datenquelle verwendet werden soll. Die Anmeldung muss bei einem [!DNL Google]-Konto registriert sein und über die Berechtigung „Lesen und Analysieren“ für das [!DNL Google Analytics]-Konto verfügen. Siehe [Anweisungen zum Zuweisen von Benutzerberechtigungen in [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).<br><br><b>Hinweis:</b> Wenn Sie das Passwort für dieses Anmeldekonto ändern, werden alle offenen Verbindungen zum Konto geschlossen. Um mit der Synchronisierung von Daten fortzufahren, kehren Sie zu dieser Seite zurück und [erneut authentifizieren](data-source-reauthenticate.md). |
| [!UICONTROL Account Details] | [!UICONTROL Google Analytics Account Name] | (Schreibgeschützt; nur verbundene Konten) Der Kontoname. |
| | [!UICONTROL Google Analytics Property] | Die Eigenschaft (Website, Mobile App oder Gerät), von der Daten für das [!DNL Google Analytics] erfasst werden sollen.<br><br> Um Metriken für mehrere Eigenschaften zu integrieren, richten Sie für jede Eigenschaft eine separate Datenquelle ein. |
| | [!UICONTROL Google Analytics View] | Die Ansicht, die den Datensatz enthält, auf den Sie zugreifen möchten. Wenn die Eigenschaft über mehrere Ansichten verfügt, sollten Sie die ungefilterte Ansicht auf der höchsten Ebene abrufen, die alle Daten enthält.<br><br>Um Metriken für mehrere Ansichten für dieselbe Eigenschaft zu integrieren, richten Sie für jede Ansicht eine separate Datenquelle ein. Stellen Sie sicher, dass sich die Daten in den Ansichten nicht überschneiden. |
| | [!UICONTROL Google Analytics Dimension] | Die [!DNL Google Analytics] benutzerdefinierte Dimension, die mit dem Wert des Adobe Advertising-Abfragezeichenfolgenparameters „ef_id“ aufgefüllt wird. Wenn die richtige Dimension nicht aufgeführt ist, wenden Sie sich an Ihr [!DNL Google Analytics] Implementierungsteam.<br><br>Die „ef_id“ wird als Primärschlüssel verwendet, um Daten von [!DNL Google Analytics] an Adobe Advertising zu übergeben. |
| [!UICONTROL Import Metrics] | [!UICONTROL Available Metrics] | Alle verfügbaren Metriken für die angegebene [!DNL Google Analytics]-Eigenschaft und -Ansicht, die nicht für die Datenquelle importiert werden, sortiert nach Kategorie. Die Liste enthält den importierten Anzeigenamen und den Backend-Namen (beginnend mit „ga„). für jede Metrik. Mit der Schaltfläche [!UICONTROL Refresh] wird die Liste mit allen neuen Metriken in [!DNL Google Analytics] aktualisiert.<br><br>Um eine verfügbare Metrik zu importieren, ziehen Sie sie in den [!UICONTROL Selected Metrics].<br><br>Siehe &quot;[Available [!DNL Google Analytics] Metrics in Advertising Cloud](data-source-ga-metrics.md).“ |
| | Selected Metrics | Alle Metriken für die angegebene [!DNL Google Analytics]-Eigenschaft und -Ansicht, die für die Datenquelle importiert werden, und der Validierungsstatus für jede Metrik. Die Liste enthält für jede Metrik den importierten Anzeigenamen und den Back-End-Namen (beginnend mit &quot;`ga.`„). Jede Datenquelle kann vier standardmäßige Traffic-Metriken enthalten, die Sie nicht entfernen können ([!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces] und [!UICONTROL Session Duration]), sowie bis zu 16 zusätzliche gültige Metriken oder Metriken ohne Daten. Sie können die Metrikliste jederzeit bearbeiten.<br><br>Um eine Metrik zu importieren, wählen Sie sie im [!UICONTROL Available Metrics] aus und ziehen Sie sie hierher.<br><br><b>Achtung:</b> [!DNL Google Analytics] ermöglicht bis zu 10 Metriken in einem einzigen Daten-Feed. Jede Ihrer Datenquellen in Search, Social und Commerce kann bis zu zwei Feeds mit insgesamt 20 Metriken enthalten. Bei Verwendung eines zweiten Feeds verdoppelt sich jedoch Ihre API-Aufrufe an [!DNL Google Analytics]. Wenn Sie viele Metriken haben, wählen Sie nur die Metriken aus, die Sie in Zielen zur Optimierung verwenden möchten. Sie können Ihre Kontingente für dieses Projekt in [der [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas) anzeigen. Weitere Informationen finden Sie [Kontingente und Aufrufbeschränkungen für API-Anfragen an [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).<br><br><b>Hinweise:</b><br><ul><li>Der Anzeigename wird als Anzeigename für eine Metrik in die Ansicht [!UICONTROL Admin] > [!UICONTROL Transactions Properties] importiert und mit &quot;<code>_ga:&lt;metric_tag konfiguriert im Feld Metrik-Tag>&quot; angehängt</code>&quot; (wie „Seitenansichten_ga:UK„). Sie können optional den Anzeigenamen Ihrer benutzerdefinierten Ziele und Metriken bearbeiten, aber die Anzeigenamen für alle gängigen Metriken werden jeden Tag mit den Anzeigenamen in [!DNL Google Analytics] überschrieben, an die die angegebenen Tags angehängt werden.</li><li>Seitenansichten, Sitzungen, Absprungrate (berechnet als Absprünge/Sitzungen) und Sitzungsdauer werden automatisch in die Portfolio-Angebotsalgorithmen einbezogen. Sie können einem Portfolioziel manuell jede andere Metrik hinzufügen.</li><li>Wenn Sie eine Metrik aus der Datenquelle entfernen, speichert Adobe Advertising die historischen Daten gemäß der normalen [Datenspeicherungsrichtlinie](/help/search-social-commerce/reports/data-used-for-reports.md).</li></ul> |
| Metrik-Tag | Metrik-Tag | Ein Tag, das an jede ausgewählte [!DNL Google Analytics] in Adobe Advertising angehängt werden soll, gefolgt von &quot;<code>_ga:</code>&quot; (wie „Seitenansichten_Tag:&lt;metric_tag>„). Das Tag kann aus 2-5 alphanumerischen Zeichen bestehen und muss für den Advertiser eindeutig sein.<br><br>Dieses Tag hilft Ihnen, die Datenquelle für jede Metrik zu identifizieren. Dieses Tag ist besonders wichtig, wenn Sie mehrere Datenquellen einrichten, da jede Datenquelle einige der gleichen Metriknamen enthält (einschließlich [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces] und [!UICONTROL Session Duration] und möglicherweise andere Metriken). Durch das Anhängen verschiedener Metrik-Tags werden doppelte Metriknamen verhindert.<br><br>Wenn Sie beispielsweise separate Integrationen für Ihre UK-Eigenschaft und Ihre JP-Eigenschaft einrichten, können Sie „UK“ und „JP“ als Metrik-Tags verwenden. Die [!UICONTROL Pageviews] Metriken für die beiden Eigenschaften werden dann in Adobe Advertising als „Pageviews_ga:UK und „Pageviews_ga“ :JP. |

>[!MORELIKETHIS]
>
>* [Über Synchronisierungs [!DNL Google Analytics] Konversionsmetriken](data-source-about.md)
>* [Voraussetzungen für die Konfiguration  [!DNL Google Analytics]  Datenquelle](data-source-prerequisites.md)
>* [Konfigurieren einer  [!DNL Google Analytics] -Ansicht als Datenquelle](data-source-configure.md)
>* [Datenquelle  [!DNL Google Analytics] bearbeiten](data-source-edit.md)
>* [Synchronisierung einer Datenquelle anhalten](data-source-pause.md)
>* [Erneutes Authentifizieren  [!DNL Google Analytics]  Datenquelle](data-source-reauthenticate.md)
>* [Anhang - Verfügbare  [!DNL Google Analytics] Metriken](data-source-ga-metrics.md)
