---
title: Erstellen einer Zielgruppenquelle zur Aktivierung von universellen ID-Zielgruppen
description: Erfahren Sie, wie Sie eine Quelle erstellen, um Zielgruppen aus Ihrer Kundendatenplattform zu importieren und in Segmente mit universellen IDs zu konvertieren.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 16a796e02150b00c77c825d7f54c6e390c85214a
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Erstellen einer Zielgruppenquelle zur Aktivierung von universellen ID-Zielgruppen

*Beta-Funktion*

Erstellen Sie eine Quelle in DSP für jede Erstanbieter-Zielgruppe in Ihrer Kundendatenplattform, die Sie in Segmente mit bestimmten universellen ID-Typen konvertieren möchten. Sie können die Segmente in das DSP Ihrer Organisation oder in ein Advertiser-Konto importieren. Datenentgelte werden auf der Grundlage der ausgewählten universellen ID-Typen angewendet.

Es sind zusätzliche Schritte erforderlich, um die Zielgruppen aus den einzelnen Kundendatenplattformen zu erfassen. Siehe Hinweis am Ende des Verfahrens.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Klicks **[!UICONTROL Add Source]**.

1. Im [!UICONTROL Select a Type] wählen Sie Ihre Kundendatenplattform aus:

   * *[!UICONTROL RT-CDP]*: [Die [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*: Die [[!DNL ActionIQ] Kundendatenplattform](source-about.md).

   * *[!UICONTROL Tealium CDP]*: (Nur konfigurierte Benutzer) Die [[!DNL Tealium] Kundendatenplattform](source-about.md).

1. Geben Sie die [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* oder *[!UICONTROL Account]*.

1. Den Rest eingeben [Quelleinstellungen](source-settings.md).

   Eine Kopie der [!UICONTROL Source Key] wird generiert. Du wirst den Wert später benötigen.

1. Klicks **[!UICONTROL Save]**.

>[!NOTE]
>
>Nachdem Sie eine Quelle für Ihre Kundendatenplattform erstellt haben, müssen Sie weitere Schritte ausführen. Siehe [Workflow zum Import von Audiences aus [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> und [Workflow zum Import von Audiences aus [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [Einstellungen der Zielgruppenquelle](source-settings.md)
>* [Über Erstanbieter-Zielgruppenquellen](source-about.md)
>* [Adobe Advertising Cloud DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
