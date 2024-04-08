---
title: Erstellen von Konversionsmetriken aus Adobe Analytics [!DNL eVars] und Props
description: Konfigurieren von benutzerdefinierten Erfolgsereignismetriken mithilfe von [!DNL eVar]- und [!DNL prop]Daten auf untergeordneter Ebene.
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
source-git-commit: a0d5bc1791f5d05e2cbdeab58e1943f4d494b53f
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Erstellen von Konversionsmetriken aus Adobe Analytics [!DNL eVars] und [!DNL props]

*Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration*

Sie können Erfolgsereignismetriken verwenden, um DSP-Pakete und Such-, Social- und Commerce-Kampagnen zu optimieren, die auf Adobe Analytics-Site-Daten basieren und am besten den Zielen Ihrer Marke entsprechen. Sie können benutzerdefinierte Erfolgsereignismetriken basierend auf Ihren vorhandenen [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) und [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) durch Trichter [!DNL eVar]- und [!DNL prop]Daten auf untergeordneter Ebene in ein Ereignis umwandeln. Sonstige [!DNL Analytics] Metriken, einschließlich standardmäßiger, benutzerdefinierter und reservierter Konversionsmetriken und Traffic-Metriken, sind automatisch in DSP und Search, Social und Commerce verfügbar.

![Anwendungsbeispiel](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Anwendungsbeispiel")

Die meisten der folgenden Aufgaben müssen von einem [!DNL Analytics] Administrator oder anderer Benutzer. Wenn Sie Hilfe benötigen, wenden Sie sich unter (DSP-Benutzer) an das technische Supportteam von DSP unter `adcloud_support@adobe.com` oder (Benutzer von Search, Social und Commerce) Ihr Adobe-Konto-Team.

1. in [!DNL Analytics], [Erstellen eines Platzhalter-Erfolgsereignisses](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-events/success-event.html?lang=en).

   Verwenden Sie die folgenden zusätzlichen Parameter:

   **Typ:** `Counter`

   **Polarität:**  entweder `Up is Good` oder `Up is Bad`

   **Sichtbarkeit:** `Visible Everywhere`

   **Eindeutige Ereignisaufzeichnung:** `Always Record Event`

   **Teilnahme:** `Enabled`

   Sie müssen das neue Ereignis nicht auf der Website Ihrer Marke implementieren, da es vorhandene Daten verwendet, die bereits erfasst wurden.

1. Erstellen und Validieren einer Verarbeitungsregel in [!DNL Analytics]:

   >[!NOTE]
   >
   >Nur [!DNL Analytics] Kontoadministratoren können Verarbeitungsregeln erstellen, es sei denn, sie haben Nicht-Administratoren die Berechtigung erteilt.

   1. [Erstellen einer Verarbeitungsregel](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en), wobei die folgende Konfiguration verwendet wird:

      * Geben Sie für die Bedingung, die erfüllt werden muss, die erforderliche an [!DNL eVars] oder [!DNL props].

        Sie können bei Bedarf zusätzliche Granularitätsstufen konfigurieren, um sicherzustellen, dass die genauesten Ereignisse erstellt werden.

        >[!TIP]
        >
        >Es empfiehlt sich, nur eine zu verwenden [!DNL eVar] oder [!DNL prop].

      * Wählen Sie für die Aktion **Ereignis festlegen** und das Platzhalterereignis auswählen.

   1. in [!DNL Analytics] [!DNL Analysis Workspace], [Erstellen eines Projekts](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) und ziehen Sie das neue Ereignis in eine Freiformtabelle, um sicherzustellen, dass die Daten für das [!DNL eVar] oder [!DNL prop] Metrik.

1. Wenden Sie sich an Ihr Adobe-Konto-Team, um die neue Metrik mit Adobe Advertising zu synchronisieren.

Nachdem die Metrik verfügbar ist, können Sie sie zum Erstellen eines Ziels verwenden, das Sie dann einem Search-, Social- und Commerce-Portfolio zuweisen oder als [Benutzerdefiniertes Ziel](/help/dsp/optimization/custom-goal.md) für ein DSP-Paket.

Weitere Informationen zum Erstellen von Zielen finden Sie im Kapitel „Optimierungshandbuch“ zu „Ziele„, das von Search, Social und Commerce aus verfügbar ist.

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Daten auf Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Anzeigen der für einen Advertiser nachverfolgten Konversionsmetriken](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
