---
title: Erfassen historischer Daten für AMO-IDs und EF-IDs zur Verwendung in Adobe Customer Journey Analytics
description: Erfahren Sie, wie Sie historische Daten für Ihre reservierten Variablen in Adobe Analytics für die zukünftige Verwendung in Adobe Customer Journey Analytics erfassen.
feature: Integration with Adobe Analytics
source-git-commit: 4cd58fd995b3df9fb7837077108207ce910157c1
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# Erfassen historischer Daten für AMO-IDs und EF-IDs zur Verwendung in Adobe Customer Journey Analytics

*Advertiser mit [!DNL Analytics for Advertising] und nur Adobe Customer Journey Analytics*

Wenn Sie reservierte Variablen verwenden, um die [AMO-ID und die EF ID](ids.md) für Ihre [!DNL Analytics for Advertising] -Integration zu erfassen, können Sie sich auf eine zukünftige Integration zwischen Adobe Advertising und [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) vorbereiten, der Adobe-Lösung der nächsten Generation von [!DNL analytics], indem Sie Ihre reservierten Variablen für die AMO-ID und die EF-ID so bald wie möglich in [standard [!DNL eVars]](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/evar) kopieren. Dadurch können historische Daten für die AMO-IDs und EF-IDs erfasst werden, sobald Sie die Aufgabe abgeschlossen haben. Ihr Adobe Account-Team teilt Ihnen mit, ob Sie reservierte Variablen verwenden und diese Aufgabe abschließen müssen.

<!-- You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation. -->

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## Warum muss ich historische Daten zum Customer Journey Analytics erfassen?

Mit Customer Journey Analytics können Sie Daten von Adobe Experience Platform mit Adobe Analytics Analysis Workspace synchronisieren. Derzeit sendet der [!DNL Analytics Data Connector]-Experience Platform keine Daten für reservierte Variablen von [!DNL Analytics] an Experience Platform. Daher sind derzeit keine Daten für AMO-IDs und EF-IDs verfügbar, die von reservierten Variablen erfasst werden. <!-- Instead, XXXXXXXXXX what exactly? -->.<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

Adobe Advertising plant eine zukünftige Implementierung mit Customer Journey Analytics. Sobald die Implementierung veröffentlicht ist, müssen Sie bei Ihrer [!DNL Analytics for Advertising]-Integration weiterhin Clickthrough-Daten und (DSP Benutzer) Durchsichtsdaten mithilfe des [!DNL Analytics]-Trackings erfassen. Sie können Ihre Daten jedoch sowohl in der 1\) [!DNL Analytics] <!-- (Analysis Workspace using data from [!DNL Analytics]) -->- als auch in der 2\)-Customer Journey Analytics <!-- (Analysis Workspace using data from Experience Platform)--> anzeigen, wenn Ihr Unternehmen über beide Produkte verfügt. Wenn die Funktion veröffentlicht wird, beginnt Experience Platform mit der Erfassung von Daten für Ihre AMO-ID und EF-ID zur Verwendung in Customer Journey Analytics. Es sind jedoch keine historischen Daten vor dem Veröffentlichungsdatum vorhanden.

Sie können jedoch früher mit der Datenerfassung für Ihre AMO-IDs und EF-IDs <!-- [!DNL rVars] --> beginnen, indem Sie eine einfache [[!DNL Analytics] Verarbeitungsregel](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules) erstellen, um Ihre AMO-IDs und EF-IDs <!-- [!DNL rVars] --> jetzt in [!DNL eVars] zu kopieren. Sobald Sie die Verarbeitungsregel erstellt haben, beginnen Sie mit der Generierung von Daten für Ihre AMO-IDs und EF-IDs <!-- [!DNL rVars] -->, sobald diese neue Ereignisse verfolgen. Sobald die Implementierung verfügbar ist, stehen die historischen Daten in Customer Journey Analytics zur Verfügung.

>[!NOTE]
>
>Verarbeitungsregeln werden nur auf neue Daten angewendet, die empfangen werden. Sie arbeiten nicht rückwirkend, um vergangene Daten zu sammeln.

## Kopieren Sie Ihre reservierten Variablen für AMO-IDs und EF-IDs in [!DNL eVars]

Dieser Schritt ist manuell und muss für jede Report Suite durchgeführt werden, die AMO-IDs und EF-IDs <!-- [!DNL rVars] --> verfolgt, die Sie in Zukunft mit Adobe Advertising integrieren werden.

1. [Erstellen Sie eine Verarbeitungsregel ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules) mit den folgenden Einstellungen:

   * Wählen Sie die Report Suite aus, für die Sie AMO-ID- und EF ID <!-- [!DNL rVar] -->-Daten zur Verwendung durch Customer Journey Analytics auf Experience Platform migrieren möchten.

   * Verwenden Sie für den [!UICONTROL Rule Title] einen beschreibenden Namen, z. B. &quot;Kopieren Sie die AMO-ID und die EF ID in eVars&quot;.

   * Fügen Sie im Abschnitt [!UICONTROL Always Execute] zwei Aktionen hinzu, um die neuen eVars zu erstellen:

      * Für den `AMO ID`: ```Overwrite value of <new/unused eVar> with amo.s_kwcid(Context Data)```

      * Für den `EF ID`: ```Overwrite value of <new/unused eVar> With amo.ef_id(Context Data)```

   * Verwenden Sie für den Wert &quot;[!UICONTROL Reason for rule]&quot;einen beschreibenden Hinweis, z. B. &quot;AMO-ID und EF-ID werden über Adobe Analytics Connector zu AEP übertragen&quot;.

1. Validieren Sie die gespeicherte Verarbeitungsregel.

   Nachdem Sie die Verarbeitungsregel gespeichert haben, sollten die Daten für die `AMO ID` und die `AMO EF ID` <!-- the existing reserved variables --> mit den Daten für die beiden neuen eVars übereinstimmen, in die sie kopiert werden.

   Wenn beispielsweise die neue eVar `eVar142` `amo.s_kwcid(Context Data)` zugeordnet ist, sollten die Daten für `eVar142` und `AMO ID` identisch sein.

Weitere Informationen zur Anwendung von Verarbeitungsregeln finden Sie unter &quot;[Funktionsweise von Verarbeitungsregeln](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about)&quot;.

>[!MORELIKETHIS]
>
>* [Überblick über  [!DNL Analytics for Advertising]](overview.md)
