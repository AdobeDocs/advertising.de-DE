---
title: Konversionsmetriken aus Adobe Analytics-eVars und -Props erstellen
description: Konfigurieren Sie benutzerdefinierte Erfolgsereignismetriken mithilfe von Daten auf eVar- und Eigenschaftenebene.
feature: Integration with Adobe Analytics, Conversions
source-git-commit: d4f439ad23fc386bc85d95cc1291ec668ecf1cd2
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Konversionsmetriken aus Adobe Analytics-eVars und -Props erstellen

*Werbetreibende, die nur über eine Adobe Advertising-Adobe Analytics-Integration verfügen*

Sie können Erfolgsereignismetriken verwenden, um DSP- und Such-, Social- und Commerce-Kampagnen auf der Grundlage von Adobe Analytics-Site-Daten zu optimieren, die am besten zu den Zielen Ihrer Marke passen. Sie können benutzerdefinierte Erfolgsereignismetriken basierend auf Ihren vorhandenen [!DNL Analytics] [eVars](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) und [props](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) durch Trichtern von Daten auf eVar- und Prop-Ebene in ein Ereignis. Sonstiges [!DNL Analytics] Metriken, einschließlich standardmäßiger, benutzerdefinierter und reservierter Konversionsmetriken und Traffic-Metriken, sind automatisch in DSP und Suche, Social und Commerce verfügbar.

![Nutzungsbeispiel](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Nutzungsbeispiel")

Die meisten der folgenden Aufgaben müssen von einem [!DNL Analytics] Administrator oder anderer Benutzer. Wenn Sie Hilfe benötigen, wenden Sie sich an (DSP Benutzer) das DSP technische Support-Team unter `adcloud_support@adobe.com` oder (Benutzer von Search, Social und Commerce) Ihrem Adobe Account Team.

1. In [!DNL Analytics], [ein Platzhalter-Erfolgsereignis erstellen](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-events/success-event.html?lang=en).

   Verwenden Sie die folgenden zusätzlichen Parameter:

   **Typ:** `Counter`

   **Polarität:**  entweder `Up is Good` oder `Up is Bad`

   **Sichtbarkeit:** `Visible Everywhere`

   **Eindeutige Ereignisaufzeichnung:** `Always Record Event`

   **Beitrag:** `Enabled`

   Sie müssen das neue Ereignis nicht auf der Website Ihrer Marke implementieren, da es bereits erfasste vorhandene Daten verwendet.

1. Erstellen Sie eine Verarbeitungsregel in [!DNL Analytics]:

   >[!NOTE]
   >
   >Nur [!DNL Analytics] -Kontoadministratoren können Verarbeitungsregeln erstellen, es sei denn, sie haben Nicht-Administratoren Zugriff auf diese Regeln gewährt.

   1. [Erstellen einer Verarbeitungsregel](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en), unter Verwendung der folgenden Konfiguration:

      * Geben Sie für die zu erfüllende Bedingung die erforderlichen eVars oder Eigenschaften an.

        Sie können bei Bedarf zusätzliche Granularitätsstufen konfigurieren, um sicherzustellen, dass die Ereignisse mit der höchsten Genauigkeit erstellt werden.

        >[!TIP]
        >
        >Es empfiehlt sich, nur eine eVar oder Eigenschaft zu verwenden.

      * Wählen Sie für die Aktion **Ereignis festlegen** und wählen Sie das Platzhalterereignis aus.

   1. In [!DNL Analytics] [!DNL Analysis Workspace], [Erstellen eines Projekts](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) und ziehen Sie das neue Ereignis in eine Freiformtabelle, um sicherzustellen, dass Daten für die eVar- oder Eigenschaftsmetrik gefüllt werden.

1. Wenden Sie sich an Ihr Adobe Account Team, um die neue Metrik mit Adobe Advertising zu synchronisieren.

Sobald die Metrik verfügbar ist, können Sie sie verwenden, um ein Ziel zu erstellen, das Sie dann einem Search-, Social- und Commerce-Portfolio zuweisen oder als [benutzerdefiniertes Ziel](/help/dsp/optimization/custom-goal-about.md) für ein DSP Paket.

Weitere Informationen zum Erstellen von Zielen finden Sie im Kapitel &quot;Optimierungshandbuch&quot;unter &quot;Ziele&quot;, das in &quot;Suche&quot;, &quot;Social&quot;und &quot;Commerce&quot;verfügbar ist.

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Daten in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
<!--
>* [](/help/search-social-commerce/admin/conversion-metrics/ ????????)
-->