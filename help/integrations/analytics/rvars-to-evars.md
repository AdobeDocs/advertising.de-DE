---
title: Erfassen historischer Daten für AMO-IDs und EF-IDs zur Verwendung in Adobe Customer Journey Analytics
description: Erfahren Sie, wie Sie historische Daten für Ihre reservierten Variablen in Adobe Analytics zur zukünftigen Verwendung in Adobe Customer Journey Analytics erfassen
feature: Integration with Adobe Analytics
exl-id: 1f8fa139-f146-426b-b0c4-079f8e2de56c
source-git-commit: fa3065d12d5c8828eaaeaca52deeadfec7b0e318
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---

# Erfassen historischer Daten für AMO-IDs und EF-IDs zur Verwendung in Adobe Customer Journey Analytics

*Nur Werbetreibende mit [!DNL Analytics for Advertising] und Adobe Customer Journey Analytics*

Wenn Sie reservierte Variablen verwenden, um die [AMO-ID und EF-ID](ids.md) für Ihre [!DNL Analytics for Advertising]-Integration zu erfassen, können Sie sich auf eine zukünftige Integration zwischen Adobe Advertising und [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) vorbereiten, die die [!DNL analytics]-Lösung der nächsten Generation von Adobe ist, indem Sie Ihre reservierten Variablen für die AMO-ID und die EF-ID so bald wie möglich in [Standard [!DNL eVars]](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/evar) kopieren. Auf diese Weise können historische Daten für die AMO-IDs und EF-IDs erfasst werden, sobald Sie die Aufgabe abgeschlossen haben. Ihr Adobe-Konto-Team teilt Ihnen mit, ob Sie reservierte Variablen verwenden und diese Aufgabe abschließen müssen.

<!-- You can also do the same for any other reserved variables you use for your [!DNL Analytics for Advertising] implementation. -->

<!-- This will allow Adobe Experience Platform, which supplies data to Customer Journey Analytics, to begin collecting historical data for your [!DNL rVars] as soon as you complete the task. -->

## Warum muss ich historische Daten für Customer Journey Analytics erfassen?

Mit Customer Journey Analytics können Sie Daten aus Adobe Experience Platform mit Adobe Analytics Analysis Workspace synchronisieren. Derzeit sendet der [!DNL Analytics Data Connector] an Experience Platform keine Daten für reservierte Variablen von [!DNL Analytics] an Experience Platform. Daher sind Daten für AMO-IDs und EF-IDs, die von reservierten Variablen erfasst werden, derzeit nicht in Customer Journey Analytics verfügbar. <!-- Instead, XXXXXXXXXX what exactly? -->,<!-- Does the Analytics for Advertising implementation use the Analytics Data Connector in particular (why would it use anything?), and we're planning to implement the Web SDK to do it instead in the future? -->

Adobe Advertising plant mit Customer Journey Analytics eine zukünftige Implementierung. Sobald die Implementierung veröffentlicht wurde, müssen Sie für Ihre [!DNL Analytics for Advertising]-Integration weiterhin Clickthrough-Daten <!-- Add back if we implement this:  and (DSP users) view-through data --> Verwendung des [!DNL Analytics]-Trackings erfassen. Sie können Ihre Daten jedoch sowohl in 1\) [!DNL Analytics] <!-- (Analysis Workspace using data from [!DNL Analytics]) --> als auch in 2\) Customer Journey Analytics <!-- (Analysis Workspace using data from Experience Platform)--> anzeigen, wenn Ihr Unternehmen über beide Produkte verfügt. Wenn die Funktion veröffentlicht wird, beginnt Experience Platform mit der Erfassung von Daten für Ihre AMO-ID und EF-ID zur Verwendung in Customer Journey Analytics, aber es werden keine historischen Daten vor dem Veröffentlichungsdatum vorhanden sein.

Sie können jedoch <!-- [!DNL rVars] --> früher damit beginnen, Daten für Ihre AMO-IDs und EF-IDs zu erfassen, indem Sie eine einfache [[!DNL Analytics] Verarbeitungsregel](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/processing-rules) erstellen, um Ihre AMO-IDs und EF-IDs <!-- [!DNL rVars] --> jetzt in [!DNL eVars] zu kopieren. Sobald Sie die Verarbeitungsregel erstellt haben, beginnen Sie, Daten für Ihre AMO-IDs und EF-IDs zu sammeln, <!-- [!DNL rVars] --> sie neue Ereignisse verfolgen. Die historischen Daten sind dann in Customer Journey Analytics verfügbar, sobald die Implementierung verfügbar ist.

>[!NOTE]
>
>* Seit dem 28. Februar 2025 verfolgt dieser Prozess Clickthrough-Daten, jedoch keine Viewthrough-Daten.
>* Verarbeitungsregeln werden nur auf neue empfangene Daten angewendet. Sie arbeiten nicht rückwirkend an der Erfassung historischer Daten.

## Kopieren Sie Ihre reservierten Variablen für AMO-IDs und EF-IDs nach [!DNL eVars]

Dieser Schritt ist manuell und muss für jede Report Suite ausgeführt werden, die AMO-IDs und EF-IDs verfolgt, <!-- [!DNL rVars] --> Sie in Zukunft mit Adobe Advertising integrieren möchten.

1. [Erstellen Sie eine Verarbeitungsregel](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules) mit den folgenden Einstellungen:

   * Wählen Sie die Report Suite aus, für die Sie AMO-ID- und EF-ID-<!-- [!DNL rVar] -->-Daten zur Verwendung durch Customer Journey Analytics nach Experience Platform migrieren möchten.

   * Verwenden Sie für die [!UICONTROL Rule Title] einen beschreibenden Namen wie „AMO-ID und EF-ID in eVars kopieren“.

   * Fügen Sie im Abschnitt [!UICONTROL Always Execute] zwei Aktionen hinzu, um die neuen eVars zu erstellen:

      * Für die `AMO ID`:

         1. Wählen Sie **Wert von überschreiben**.
         1. *\&lt;die neue/nicht verwendete eVar\>*
         1. Wählen Sie **Abfragezeichenfolgen-Parameter** aus.
         1. `s_kwcid` eingeben.

        Beispiel: Wert von `rVar10` mit Abfragezeichenfolgen-Parameter `s_kwcid` überschreiben

      * Für die `EF ID`:

         1. Wählen Sie **Wert von überschreiben**.
         1. *\&lt;die neue/nicht verwendete eVar\>*
         1. Wählen Sie **Abfragezeichenfolgen-Parameter** aus.
         1. `ef_id` eingeben.

        Beispiel: Wert von `rVar11` mit Abfragezeichenfolgen-Parameter `ef_id` überschreiben

   * Verwenden Sie [!UICONTROL Reason for rule] einen beschreibenden Hinweis wie „Die AMO-ID und die EF-ID werden über den Adobe Analytics-Connector zu AEP transportiert.“

1. Validieren Sie die gespeicherte Verarbeitungsregel.

   Nachdem Sie die Verarbeitungsregel gespeichert haben, sollten die Daten für die `AMO ID` und die `AMO EF ID` <!-- the existing reserved variables --> mit den Daten für die beiden neuen eVars identisch sein, in die sie kopiert werden.

   Wenn beispielsweise die neue eVar-`eVar142` `amo.s_kwcid(Context Data)` zugeordnet wird, sollten die Daten für die `eVar142` und die `AMO ID` identisch sein.

Weitere Informationen zur Anwendung von Verarbeitungsregeln finden Sie unter &quot;[ der Funktionsweise von ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/processing-rules-about)&quot;.

>[!MORELIKETHIS]
>
>* [Überblick über [!DNL Analytics for Advertising]](overview.md)
