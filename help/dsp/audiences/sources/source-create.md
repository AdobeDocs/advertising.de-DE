---
title: Erstellen einer Zielgruppenquelle zum Aktivieren von Erstanbieterzielgruppen
description: Erfahren Sie, wie Sie eine Quelle erstellen, um Zielgruppen in Ihr Konto oder ein Advertiser-Konto zu importieren.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# Erstellen einer Zielgruppenquelle zum Aktivieren von Erstanbieterzielgruppen

<!-- Will this remain for admin users/Adobe Account Team users only? -->

Erstellen Sie eine Quelle in DSP, um Erstanbieter-Zielgruppen in Ihr DSP-Konto oder ein Advertiser-Konto zu importieren.

Weitere Schritte zur Aufnahme von Segmenten von bestimmten Kundendatenplattformen finden Sie unter [Zielgruppenspezifische Aktivierungs-Workflows](source-about.md)

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Klicks **[!UICONTROL Add Source]**.

1. Im [!UICONTROL Select a Type] wählen Sie den Quelltyp aus.

   * *[!UICONTROL RT-CDP]*: [Die [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   <!-- * *[!UICONTROL ActionIQ]*: The [[!DNL ActionIQ] customer data platform](source-about.md). -->

   * *[!UICONTROL Tealium CDP]*: Die [[!DNL Tealium] Kundendatenplattform](source-about.md).

1. Geben Sie die [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* oder *[!UICONTROL Account]*.

1. Den Rest eingeben [Quelleinstellungen](source-settings.md).

   Eine Kopie der [!UICONTROL Source Key] wird generiert. Du wirst den Wert später benötigen.

1. Klicks **[!UICONTROL Save]**.

>[!NOTE]
>
>Nachdem Sie eine Quelle für Ihre Kundendatenplattform erstellt haben, müssen Sie weitere Schritte ausführen. Siehe [Aktivierungs-Workflow für [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> und [Aktivierungs-Workflow für [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [Einstellungen der Zielgruppenquelle](source-settings.md)
>* [Informationen zum Aktivieren authentifizierter Segmente aus Zielgruppen-Quellen](source-about.md)
>* [Authentifizierte Segmente von universellen ID-Partnern aktivieren](source-universal-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
