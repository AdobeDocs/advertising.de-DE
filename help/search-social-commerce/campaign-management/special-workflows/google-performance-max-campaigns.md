---
title: Implementieren  [!DNL Google Ads]  Kampagnen mit maximaler Leistung
description: Erfahren Sie mehr über den Workflow zum Einrichten  [!DNL Google Ads]  Kampagnen mit maximaler Leistung.
exl-id: 4208774c-e4dd-499d-987e-933fe073c04f
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Implementieren [!DNL Google Ads] Kampagnen mit maximaler Leistung

In [!DNL Google Ads] Kampagnen mit dem Typ „Performance Max“ richten Sie keine Anzeigengruppen, Anzeigen oder Schlüsselwörter ein. Stattdessen geben Sie in den Kampagneneinstellungen eine oder mehrere Asset-Gruppen an, zu denen Überschriften, Beschreibungen und hochgeladene Bilder, Logos und [!DNL YouTube videos] gehören. [!DNL Google Ads] kombiniert die Assets automatisch, um Anzeigen basierend auf dem Kanal bereitzustellen (z. B. [!DNL YouTube], [!DNL Gmail] oder [!DNL Search]).

Sie können Ihre bestehenden Performance Max-Kampagnen mit Leistungsdaten im Tabellen- und Trenddiagramm-Format in der [!DNL Campaigns] Ansicht anzeigen. Daten sind nicht auf niedrigeren Ebenen verfügbar. Leistungsdaten auf Kampagnenebene sind auch in Berichten und in Adobe Analytics (für Werbetreibende mit einer [Analytics-Integration) &#x200B;](/help/integrations/analytics/overview.md). Um Leistungsdaten für Kampagnen mit dem Status „Performance Max“ in [!DNL Analytics] anzuzeigen, muss die Kampagne den [upgegradeten AMO-ID-Trackingcode](/help/integrations/analytics/ids.md#amo-id-formats) verwenden, mit dem die Kampagnen-ID und die Anzeigengruppen-ID verfolgt werden.

>[!NOTE]
>
>* Sie müssen alle Bilddateien manuell hochladen. Links zu [!DNL Google Merchant Center] Produkt-Feeds werden nicht unterstützt.
>* Es sind nur erforderliche Einstellungen verfügbar. Für optionale Einstellungen melden Sie sich beim [!DNL Google Ads] an.
>* Die Auflistung von Gruppen wird nicht unterstützt. Um Daten für die Auflistung von Gruppen zu verwalten und anzuzeigen, melden Sie sich beim [!DNL Google Ads] an.

## Schritte zum Einrichten [!DNL Google Ads] Kampagnen mit maximaler Leistung

Sie können Performance Max-Kampagnen individuell über die Ansicht [!UICONTROL Campaigns] > [!UICONTROL Campaigns] einrichten.

1. [Erstellen einer Kampagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) mit Kampagnentyp **[!UICONTROL Performance Max]**.

   Geben Sie [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting] und [!UICONTROL URL Options] an. Geben Sie optional [!UICONTROL Negative Keywords] ein, geben Sie [!UICONTROL Negative Websites] ein und/oder überschreiben Sie die [!UICONTROL Campaign Tracking].

1. Asset-Gruppen erstellen und Assets für die Kampagne hochladen:

   1. Klicken Sie unten in den Kampagneneinstellungen auf **[!UICONTROL Manage Asset Groups]**.

   1. Legen Sie die Einstellungen für die erste Asset-Gruppe fest und laden Sie die Bilder, Logos und optionalen Videos für die Asset-Gruppe hoch.

      Unter [Beschreibungen der Asset-Gruppeneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) finden Sie weitere Informationen zu den Anforderungen und Spezifikationen.

   1. Fügen Sie bei Bedarf weitere Asset-Gruppen hinzu.

1. Klicken Sie auf **[!UICONTROL Post]**.

1. (Optional) Fügen Sie die Kampagne zur Optimierung einem hybriden Portfolio hinzu.
