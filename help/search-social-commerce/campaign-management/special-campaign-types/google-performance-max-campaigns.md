---
title: Implementierung [!DNL Google Ads] Performance-Max-Kampagnen
description: Erfahren Sie mehr über den Workflow zur Einrichtung [!DNL Google Ads] Kampagnen mit maximaler Leistung.
exl-id: afad96b2-d4a6-41ee-ad84-38aa1306d73e
feature: Search Campaign Management
source-git-commit: ca9425333731ada692c68f08b20f070265eb3409
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Implementierung [!DNL Google Ads] Performance-Max-Kampagnen

In [!DNL Google Ads] Performance-Max-Kampagnen verwenden, richten Sie keine Anzeigengruppen, Anzeigen oder Suchbegriffe ein. Stattdessen geben Sie in den Kampagneneinstellungen eine oder mehrere Asset-Gruppen an, die Überschriften, Beschreibungen sowie hochgeladene Bilder, Logos und [!DNL YouTube videos]. [!DNL Google Ads] kombiniert die Assets automatisch, um Anzeigen basierend auf dem Kanal bereitzustellen (z. B. [!DNL YouTube], [!DNL Gmail]oder [!DNL Search]).

Sie können Ihre vorhandenen Performance-Max-Kampagnen mit Leistungsdaten im Tabellen- und Trend-Diagrammformat im [!DNL Campaigns] Ansicht; Daten sind nicht auf niedrigeren Ebenen verfügbar. Leistungsdaten auf Kampagnenebene sind auch in Berichten und in Adobe Analytics verfügbar (für Advertiser mit einer [Analytics-Integration](/help/integrations/analytics/overview.md). So zeigen Sie Leistungsdaten für Leistungsmax-Kampagnen in [!DNL Analytics], muss die Kampagne die [aktualisierter AMO-ID-Trackingcode](/help/search-social-commerce/tracking/amo-id-tracking-parameter.md) (verfolgt die Kampagnen-ID und Anzeigengruppen-ID).

>[!NOTE]
>
>* Sie müssen alle Bilddateien manuell hochladen. Links zu [!DNL Google Merchant Center] -Produkt-Feeds werden nicht unterstützt.
>* Es sind nur erforderliche Einstellungen verfügbar. Für optionale Einstellungen melden Sie sich bei der [!DNL Google Ads] Editor.
>* Unterstützung für die Auflistung von Gruppen ist nicht verfügbar. Um Daten für die Auflistung von Gruppen zu verwalten und anzuzeigen, melden Sie sich bei der [!DNL Google Ads] Editor.

## Schritte zum Einrichten [!DNL Google Ads] Performance-Max-Kampagnen

Sie können die Kampagnen zur Leistungsmax einzeln über die [!UICONTROL Campaigns] > [!UICONTROL Campaigns] anzeigen.

1. [Kampagne erstellen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) mit Kampagnentyp **[!UICONTROL Performance Max]**.

   Geben Sie die [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting], und [!UICONTROL URL Options]. Optional eingeben [!UICONTROL Negative Keywords], eingeben [!UICONTROL Negative Websites], und/oder überschreiben Sie die [!UICONTROL Campaign Tracking] Optionen.

1. Erstellen Sie Asset-Gruppen und laden Sie Assets für die Kampagne hoch:

   1. Klicken Sie unten in den Kampagneneinstellungen auf **[!UICONTROL Manage Asset Groups]**.

   1. Geben Sie die Einstellungen für die erste Asset-Gruppe an und laden Sie die Bilder, Logos und optionalen Videos für die Asset-Gruppe hoch.

      Siehe [Beschreibungen der Asset-Gruppeneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) um die Anforderungen und Spezifikationen zu verstehen.

   1. Fügen Sie nach Bedarf weitere Asset-Gruppen hinzu.

1. Klicken **[!UICONTROL Post]**.

1. (Optional) Fügen Sie die Kampagne zu einem hybriden Portfolio zur Optimierung hinzu.
