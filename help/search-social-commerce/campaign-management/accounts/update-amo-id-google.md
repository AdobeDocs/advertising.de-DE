---
title: Aktualisieren des AMO-ID-Trackingcodes (s_kwcid) für ein  [!DNL Google Ads] -Konto
description: Erfahren Sie, wie Sie zum neuesten AMO ID-Trackingcode für ein - [!DNL Google Ads]  wechseln.
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: edb46265c6977a1e2c1b352f41fedcfc3a9e3bbf
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# Aktualisieren des AMO-ID-Trackingcodes (s_kwcid) für ein [!DNL Google Ads] Konto

*Werbetreibende nur mit einer Adobe Advertising-Adobe Analytics-Integration*

Nur *[!DNL Google Ads]Konten*

Das veraltete Format (vor Oktober 2019) für den [AMO ID-Trackingcode](/help/integrations/analytics/ids.md#amo-id-formats) für bestehende [!DNL Google Ads]-Konten unterstützt einige Funktionen in Analytics nicht, z. B. das Reporting auf Kampagnen- und Anzeigengruppenebene für [!DNL Google Ads] Kampagnen des Typs „Performance Max“, Entwürfe und Experimente und andere Anwendungsfälle, in denen dieselbe Kombination aus Anzeigen, Keyword und Übereinstimmungstyp in mehreren Kampagnen vorhanden ist.

Das aktuelle Format enthält Parameter für die Kampagnen-ID und die Anzeigengruppen-ID:

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

Für ein vorhandenes Konto, das das alte Format verwendet, können Sie das aktuelle Format ändern. Wenn Sie keine Kampagnen des Typs „Performance Max“ oder Kampagnen des Typs „Entwürfe und Experimente“ haben, ist die Migration in das neue Format optional.

Alle neuen [!DNL Google Ads]-Konten verwenden automatisch das aktuelle AMO-ID-Format.

>[!NOTE]
>
>Diese Option ist nur für Konten verfügbar, die nicht das aktuelle Format verwenden.
>
>Nach der Migration eines Kontos werden alle Klick-, Kosten- und Impressionsdaten nach der Änderung korrekt gemeldet, aber alle Clickthroughs, die vor der Migration stattfanden, werden weiterhin Konversionsdaten auf der Grundlage des alten AMO ID-Formats zugeordnet.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Halten Sie den Cursor über den Kontonamen, klicken Sie auf ![Pfeil-Dropdown-](/help/search-social-commerce/assets/arrow-dropdown-menu.png), und wählen Sie dann **[!UICONTROL Edit]** aus.

1. Klicken Sie auf **[!UICONTROL Set Account Tracking]**.

1. Starten Sie die Migration:

   1. Klicken Sie neben **[!UICONTROL S_KWCID FORMAT]** in den [!UICONTROL Account Tracking] auf **[!UICONTROL LEGACY S_KWCID FORMAT]**.

   1. Klicken Sie auf **[!UICONTROL Migrate to new s_kwcid format]**.

   1. Aktivieren Sie in der Bestätigungsmeldung das Kontrollkästchen, und klicken Sie dann auf **[!UICONTROL Continue]**.

   1. Klicken Sie in den Kontoeinstellungen auf **[!UICONTROL Post]**.

   Metadaten für die Kampagnen werden in [!DNL Analytics] innerhalb weniger Tage aktualisiert. Das Tracking wird unterbrechungsfrei fortgesetzt, sodass keine Daten verloren gehen. Die neuen Trackingcodes werden jedoch in den Berichten möglicherweise erst widergespiegelt, wenn [!DNL Analytics] alle Metadaten empfangen.

   >[!NOTE]
   >
   >Alle Clickthroughs, die vor der Migration auftraten, melden weiterhin Konversionsdaten, die auf dem alten Format basieren.

1. Aktualisieren Sie nach Beginn der Migration die Einstellungen für das Landingpage-Suffix (in einigen Werbenetzwerken als „endgültiges URL-Suffix“ bezeichnet) nach Bedarf:

   * Wenn die Funktion &quot;[!UICONTROL Auto Upload]&quot; in den Tracking-Einstellungen aktiviert ist, aktualisiert Search, Social und Commerce automatisch den Tracking-Code im Suffix der Landingpage für dieses Konto und dessen Kampagnen. Du brauchst nichts zu tun.

   * Wenn die Funktion &quot;[!UICONTROL Auto Upload]&quot; nicht aktiviert ist und Sie die [Server-seitige AMO ID-Funktion](/help/integrations/analytics/ids.md#amo-id-formats) nicht verwenden, müssen Sie den AMO ID-Parameter in den Suffix-Einstellungen für die Landingpage manuell aktualisieren. Suffixe auf Konto- und Kampagnenebene können manuell in den [Kontoeinstellungen](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) und [Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) oder durch [Hochladen von Änderungen in einer Bulksheet) ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md). Um ein Suffix auf Anzeigengruppenebene oder darunter zu konfigurieren, verwenden Sie den [!DNL Google Ads].

   * Wenn Sie die AMO-ID in die Einstellung der Basis-URL für eine beliebige Kampagnenkomponente aufnehmen, verschieben Sie sie in die entsprechende Einstellung für das Landingpage-Suffix .

1. (Empfohlen) Überprüfen Sie die Daten für dieses Konto in [!DNL Analytics], bevor Sie zusätzliche Konten migrieren.

>[!MORELIKETHIS]
>
>* [Verwalten von Anzeigennetzwerkkonten](ad-network-account-manage.md)
>* [Adobe Advertising-IDs verwendet von [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Überblick über [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html?lang=de){target="_blank"}
