---
title: Implementieren von [!DNL Google Ads] Leistungsmax-Kampagnen
description: Erfahren Sie mehr über den Workflow zum Einrichten von Kampagnen mit der höchsten Leistung. [!DNL Google Ads]
exl-id: 4208774c-e4dd-499d-987e-933fe073c04f
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Implementieren von [!DNL Google Ads] Leistungsmax-Kampagnen

In den Kampagnen zur maximalen Performance von [!DNL Google Ads] richten Sie keine Anzeigengruppen, Anzeigen oder Suchbegriffe ein. Stattdessen geben Sie in den Kampagneneinstellungen eine oder mehrere Asset-Gruppen an, die Überschriften, Beschreibungen sowie hochgeladene Bilder, Logos und [!DNL YouTube videos] enthalten. [!DNL Google Ads] kombiniert die Assets automatisch, um Anzeigen basierend auf dem Kanal bereitzustellen (wie [!DNL YouTube], [!DNL Gmail] oder [!DNL Search]).

Sie können Ihre vorhandenen Performance-Max-Kampagnen mit Leistungsdaten im Tabellen- und Trend-Diagrammformat in der Ansicht [!DNL Campaigns] anzeigen. Daten sind nicht auf niedrigeren Ebenen verfügbar. Leistungsdaten auf Kampagnenebene stehen auch in Berichten und in Adobe Analytics zur Verfügung (für Advertiser mit einer [Analytics-Integration](/help/integrations/analytics/overview.md)). Um Leistungsdaten für Leistungsmax-Kampagnen in [!DNL Analytics] anzuzeigen, muss die Kampagne den [aktualisierten AMO-ID-Trackingcode](/help/integrations/analytics/ids.md#amo-id-formats) verwenden (der die Kampagnen-ID und Anzeigengruppen-ID verfolgt).

>[!NOTE]
>
>* Sie müssen alle Bilddateien manuell hochladen. Links zu [!DNL Google Merchant Center] -Produkt-Feeds werden nicht unterstützt.
>* Es sind nur erforderliche Einstellungen verfügbar. Für optionale Einstellungen melden Sie sich beim [!DNL Google Ads]-Editor an.
>* Unterstützung für die Auflistung von Gruppen ist nicht verfügbar. Um Daten für die Auflistung von Gruppen zu verwalten und anzuzeigen, melden Sie sich beim [!DNL Google Ads]-Editor an.

## Schritte zum Einrichten von [!DNL Google Ads] Leistungsmax-Kampagnen

Über die Ansicht [!UICONTROL Campaigns] > [!UICONTROL Campaigns] können Sie die Leistungsmax-Kampagnen einzeln einrichten.

1. [Erstellen Sie eine Kampagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) mit dem Kampagnentyp **[!UICONTROL Performance Max]**.

   Geben Sie die Werte [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting] und [!UICONTROL URL Options] an. Geben Sie optional [!UICONTROL Negative Keywords] ein, geben Sie [!UICONTROL Negative Websites] ein und/oder überschreiben Sie die [!UICONTROL Campaign Tracking] Optionen.

1. Erstellen Sie Asset-Gruppen und laden Sie Assets für die Kampagne hoch:

   1. Klicken Sie unten in den Kampagneneinstellungen auf **[!UICONTROL Manage Asset Groups]**.

   1. Geben Sie die Einstellungen für die erste Asset-Gruppe an und laden Sie die Bilder, Logos und optionalen Videos für die Asset-Gruppe hoch.

      Unter [Beschreibungen der Asset-Gruppeneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) finden Sie Informationen zu den Anforderungen und Spezifikationen.

   1. Fügen Sie nach Bedarf weitere Asset-Gruppen hinzu.

1. Klicken Sie auf **[!UICONTROL Post]**.

1. (Optional) Fügen Sie die Kampagne zu einem hybriden Portfolio zur Optimierung hinzu.
