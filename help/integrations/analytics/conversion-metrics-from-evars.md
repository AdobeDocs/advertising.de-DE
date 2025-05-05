---
title: Erstellen von Konversionsmetriken aus Adobe Analytics  [!DNL eVars]  Props
description: Konfigurieren Sie benutzerdefinierte Erfolgsereignismetriken mithilfe von  [!DNL eVar]- und  [!DNL prop].
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
source-git-commit: 91e8435ff00feca804dfa2f4c323f88ee31813ab
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Erstellen von Konversionsmetriken aus Adobe Analytics [!DNL eVars] und [!DNL props]

*Nur Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

Sie können Erfolgsereignismetriken verwenden, um DSP-Pakete und Such-, Social- und Commerce-Kampagnen auf der Grundlage von Adobe Analytics-Site-Daten zu optimieren, die den Zielen Ihrer Marke am besten entsprechen. Sie können benutzerdefinierte Erfolgsereignismetriken basierend auf Ihren vorhandenen [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=de) und [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html?lang=de) konfigurieren, indem Sie Daten auf [!DNL eVar]- und [!DNL prop] Ebene in ein Ereignis einleiten. Andere [!DNL Analytics], einschließlich standardmäßiger, benutzerdefinierter und reservierter Konversionsmetriken und Traffic-Metriken, sind automatisch in DSP und Search, Social und Commerce verfügbar.

![Nutzungsbeispiel](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Nutzungsbeispiel")

Die meisten der folgenden Aufgaben müssen von einem [!DNL Analytics] oder einem anderen Benutzer durchgeführt werden. Wenn Sie Hilfe benötigen, wenden Sie sich unter (DSP-Benutzer) an das technische Support-Team von DSP unter `adcloud_support@adobe.com` oder (Benutzer von Search, Social und Commerce) an Ihr Adobe-Account-Team.

1. Erstellen Sie [!DNL Analytics] [ein Platzhalter-Erfolgsereignis](https://experienceleague.adobe.com/de/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-event).

   Verwenden Sie die folgenden zusätzlichen Parameter:

   **type:** `Counter`

   **Polarität:** entweder `Up is Good` oder `Up is Bad`

   **Sichtbarkeit:** `Visible Everywhere`

   **Eindeutige Ereignisaufzeichnung:** `Always Record Event`

   **Teilnahme:** `Enabled`

   Sie müssen das neue Ereignis nicht auf der Website Ihrer Marke implementieren, da es vorhandene Daten verwendet, die bereits erfasst wurden.

1. Erstellen und validieren Sie eine Verarbeitungsregel in [!DNL Analytics]:

   >[!NOTE]
   >
   >Nur [!DNL Analytics]-Konto-Administratoren können Verarbeitungsregeln erstellen, es sei denn, sie haben Nicht-Administratoren die Berechtigung erteilt.

   1. [Erstellen Sie eine Verarbeitungsregel](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=de) mithilfe der folgenden Konfiguration:

      * Geben Sie für die Bedingung, die erfüllt werden muss, die erforderliche [!DNL eVars] oder [!DNL props] an.

        Sie können bei Bedarf zusätzliche Granularitätsstufen konfigurieren, um sicherzustellen, dass die genauesten Ereignisse erstellt werden.

        >[!TIP]
        >
        >Es empfiehlt sich, nur eine [!DNL eVar] oder [!DNL prop] zu verwenden.

      * Wählen Sie für die Aktion **Ereignis festlegen** und wählen Sie das Platzhalterereignis aus.

   1. Erstellen Sie in [!DNL Analytics] [!DNL Analysis Workspace] [ein Projekt](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html?lang=de) und ziehen Sie das neue Ereignis in eine Freiformtabelle, um sicherzustellen, dass die Daten für die [!DNL eVar] oder [!DNL prop] Metrik gefüllt werden.

1. Wenden Sie sich an Ihr Adobe-Konto-Team , um die neue Metrik mit Adobe Advertising zu synchronisieren.

Nachdem die Metrik verfügbar ist, können Sie sie zum Erstellen eines Ziels verwenden, das Sie dann einem Search-, Social- und Commerce-Portfolio zuweisen oder als [benutzerdefiniertes Ziel](/help/dsp/optimization/custom-goal.md) für ein DSP-Paket verwenden können.

Weitere Informationen zum Erstellen von Zielen finden Sie im Kapitel „Optimierungshandbuch“ zu „Zielen“, das in Search, Social und Commerce verfügbar ist

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Daten in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Anzeigen der für einen Advertiser verfolgten Konversionsmetriken](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
