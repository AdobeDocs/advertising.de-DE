---
title: Konversionsmetriken aus Adobe Analytics [!DNL eVars] und Props erstellen
description: Konfigurieren Sie benutzerdefinierte Erfolgsereignismetriken mit Daten der Ebenen [!DNL eVar] und [!DNL prop].
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
source-git-commit: db815958b039508b005f4be60561ddc4656da86e
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---

# Konversionsmetriken aus Adobe Analytics erstellen [!DNL eVars] und [!DNL props]

*Advertiser mit nur einer Adobe Advertising-Adobe Analytics-Integration*

Sie können Erfolgsereignismetriken verwenden, um DSP- und Such-, Social- und Commerce-Kampagnen auf der Grundlage von Adobe Analytics-Site-Daten zu optimieren, die am besten zu den Zielen Ihrer Marke passen. Sie können benutzerdefinierte Erfolgsereignismetriken basierend auf Ihren vorhandenen [[!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) und [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) konfigurieren, indem Sie Daten der Ebenen [!DNL eVar] und [!DNL prop] in ein Ereignis umwandeln. Andere [!DNL Analytics] -Metriken, einschließlich standardmäßiger, benutzerdefinierter und reservierter Konversionsmetriken und Traffic-Metriken, sind automatisch in DSP und Suche, Social und Commerce verfügbar.

![Nutzungsbeispiel](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Nutzungsbeispiel")

Die meisten der folgenden Aufgaben müssen von einem [!DNL Analytics] -Administrator oder einem anderen Benutzer ausgeführt werden. Wenn Sie Hilfe benötigen, wenden Sie sich an (DSP-Benutzer) das DSP technische Supportteam unter `adcloud_support@adobe.com` oder (Benutzer von Search, Social und Commerce) Ihr Adobe-Account-Team.

1. Erstellen Sie in [!DNL Analytics] [ein Platzhalter-Erfolgsereignis](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-event).

   Verwenden Sie die folgenden zusätzlichen Parameter:

   **Typ:** `Counter`

   **Polarität:** entweder `Up is Good` oder `Up is Bad`

   **Sichtbarkeit:** `Visible Everywhere`

   **Eindeutige Ereignisaufzeichnung:** `Always Record Event`

   **Beitrag:** `Enabled`

   Sie müssen das neue Ereignis nicht auf der Website Ihrer Marke implementieren, da es bereits erfasste vorhandene Daten verwendet.

1. Erstellen und validieren Sie eine Verarbeitungsregel in [!DNL Analytics]:

   >[!NOTE]
   >
   >Nur [!DNL Analytics] -Kontoadministratoren können Verarbeitungsregeln erstellen, es sei denn, sie haben Nicht-Administratoren Zugriff auf diese Regeln gewährt.

   1. [Erstellen Sie eine Verarbeitungsregel](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en) mit der folgenden Konfiguration:

      * Geben Sie für die Bedingung, die erfüllt sein muss, den erforderlichen [!DNL eVars] oder den erforderlichen [!DNL props] an.

        Sie können bei Bedarf zusätzliche Granularitätsstufen konfigurieren, um sicherzustellen, dass die Ereignisse mit der höchsten Genauigkeit erstellt werden.

        >[!TIP]
        >
        >Es empfiehlt sich, nur einen [!DNL eVar] oder einen [!DNL prop] zu verwenden.

      * Wählen Sie für die Aktion **Ereignis festlegen** und dann das Platzhalterereignis aus.

   1. Erstellen Sie in [!DNL Analytics] [!DNL Analysis Workspace] [ein Projekt](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) und ziehen Sie das neue Ereignis in eine Freiformtabelle, um sicherzustellen, dass Daten für die Metrik [!DNL eVar] oder [!DNL prop] gefüllt werden.

1. Wenden Sie sich an Ihr Adobe-Account-Team, um die neue Metrik mit Adobe Advertising zu synchronisieren.

Nachdem die Metrik verfügbar ist, können Sie sie verwenden, um ein Ziel zu erstellen, das Sie dann einem Search-, Social- und Commerce-Portfolio zuweisen oder als [benutzerdefiniertes Ziel](/help/dsp/optimization/custom-goal.md) für ein DSP-Package verwenden können.

Weitere Informationen finden Sie im Kapitel &quot;Optimierungshandbuch&quot;unter &quot;Ziele&quot;, das in Search, Social und Commerce verfügbar ist.

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Daten in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Anzeigen der für einen Advertiser verfolgten Konversionsmetriken](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
