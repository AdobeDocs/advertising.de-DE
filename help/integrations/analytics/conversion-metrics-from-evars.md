---
title: Erstellen von Konversionsmetriken aus Adobe Analytics  [!DNL eVars]  Props
description: Konfigurieren Sie benutzerdefinierte Erfolgsereignismetriken mithilfe von  [!DNL eVar]- und  [!DNL prop].
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
TQID: https://experienceleague.adobe.com/DRwNcYJ4-tv6CWhaIHc-qZ-xNsM8sSqoSNkG8AaYI2c
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
  - id: f2860a4b-f905-4545-bead-1bbc92564592
subfeature_v2:
  - id: cfd751d4-ee56-4323-8fd1-dc174b031709
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 0%

---

# Erstellen von Konversionsmetriken aus Adobe Analytics [!DNL eVars] und [!DNL props]

*Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

Sie können Erfolgsereignismetriken verwenden, um DSP-Pakete und Such-, Social- und Commerce-Kampagnen auf der Grundlage von Adobe Analytics-Site-Daten zu optimieren, die den Zielen Ihrer Marke am besten entsprechen. Sie können benutzerdefinierte Erfolgsereignismetriken basierend auf Ihren vorhandenen [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=de) und [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html?lang=de) konfigurieren, indem Sie Daten auf [!DNL eVar]- und [!DNL prop] Ebene in ein Ereignis einleiten. Andere [!DNL Analytics], einschließlich standardmäßiger, benutzerdefinierter und reservierter Konversionsmetriken und Traffic-Metriken, sind automatisch in DSP und Search, Social und Commerce verfügbar.

![Nutzungsbeispiel](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Nutzungsbeispiel")

Die meisten der folgenden Aufgaben müssen von einem [!DNL Analytics] oder einem anderen Benutzer durchgeführt werden. Wenn Sie Hilfe benötigen, wenden Sie sich an Ihr Adobe Account Team.

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
