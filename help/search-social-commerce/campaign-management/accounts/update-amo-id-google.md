---
title: Aktualisierung des Trackingcodes der AMO-ID (s_kwcid) für ein [!DNL Google Ads] Konto
description: Erfahren Sie, wie Sie zum neuesten AMO-ID-Trackingcode für ein [!DNL Google Ads] Konto wechseln.
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# AMO-ID-Trackingcode (s_kwcid) für ein [!DNL Google Ads]-Konto aktualisieren

*Advertiser nur mit Adobe Advertising-Adobe Analytics-Integration*

*[!DNL Google Ads]nur Konten*

Das veraltete Format (vor Oktober 2019) für den [AMO ID-Trackingcode](/help/integrations/analytics/ids.md#amo-id-formats) für vorhandene [!DNL Google Ads]-Konten unterstützt einige Funktionen in Analytics nicht, z. B. Berichte auf Kampagnen- und Anzeigengruppenebene für maximal [!DNL Google Ads] Kampagnen, Entwürfe und Experimentkampagnen und andere Anwendungsfälle, in denen dieselbe Kombination aus Anzeige+Keyword+Match in mehreren Kampagnen vorhanden ist.

Das aktuelle Format enthält Parameter für die Kampagnen-ID und Anzeigengruppen-ID:

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

Sie können das aktuelle Format für jedes oder alle Ihrer vorhandenen Konten einzeln ändern. Wenn Sie keine Kampagnen, Entwürfe und Experimente mit maximaler Leistung haben, ist eine Migration in das neue Format optional.

Alle neuen [!DNL Google Ads] -Konten verwenden automatisch das aktuelle AMO-ID-Format.

>[!NOTE]
>
>Nachdem Sie ein Konto migriert haben, werden alle Klick-, Kosten- und Impressionsdaten nach der Änderung korrekt gemeldet, aber alle Clickthroughs, die vor der Migration stattgefunden haben, werden weiterhin Konversionsdaten basierend auf dem alten AMO-ID-Format zugeordnet.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Halten Sie den Cursor über den Kontonamen, klicken Sie auf das Dropdown-Symbol ](/help/search-social-commerce/assets/arrow-dropdown-menu.png) mit dem Pfeil und wählen Sie dann **[!UICONTROL Edit]** aus.![

1. Klicken Sie auf **[!UICONTROL Set Account Tracking]**.

1. Starten Sie die Migration:

   1. Klicken Sie neben **[!UICONTROL S_KWCID FORMAT]** auf **[!UICONTROL LEGACY S_KWCID FORMAT]**.

   1. Klicken Sie auf **[!UICONTROL Migrate to new s_kwcid format]**.

   1. Aktivieren Sie in der Bestätigungsmeldung das Kontrollkästchen und klicken Sie auf **[!UICONTROL Continue]**.

   1. Klicken Sie in den Kontoeinstellungen auf **[!UICONTROL Post]**.

   Die Metadaten für die Kampagnen werden innerhalb weniger Tage in [!DNL Analytics] aktualisiert. Das Tracking wird unterbrechungsfrei fortgesetzt, sodass keine Daten verloren gehen. Die Berichterstellung spiegelt die neuen Trackingcodes jedoch möglicherweise erst wider, wenn [!DNL Analytics] alle Metadaten erhält.

   >[!NOTE]
   >
   >Alle Clickthroughs, die vor der Migration auftraten, melden weiterhin Konversionsdaten basierend auf dem alten Format.

1. Nachdem Sie mit der Migration begonnen haben, aktualisieren Sie die Einstellungen für das Suffix der Einstiegsseite (in einigen Werbenetzwerken als &quot;endgültiges URL-Suffix&quot;bezeichnet) nach Bedarf:

   * Wenn die Funktion &quot;[!UICONTROL Auto Upload]&quot; in den Tracking-Einstellungen aktiviert ist, aktualisiert Search, Social und Commerce automatisch den Trackingcode im Suffix der Landingpage für dieses Konto und seine Kampagnen. Du brauchst nichts zu tun.

   * Wenn die Funktion &quot;[!UICONTROL Auto Upload]&quot; nicht aktiviert ist und Sie die [serverseitige AMO-ID-Funktion](/help/integrations/analytics/ids.md#amo-id-formats) nicht verwenden, müssen Sie den AMO-ID-Parameter in den Einstellungen für das Suffix der Einstiegsseite manuell aktualisieren. Sie können die Suffixe auf Konto- und Kampagnenebene manuell in den Konto- und Kampagneneinstellungen ändern oder indem Sie Änderungen in ein Bulksheet hochladen. Verwenden Sie den Editor [!DNL Google Ads] , um ein Suffix auf Anzeigengruppenebene oder niedriger zu konfigurieren.

   * Wenn Sie die AMO-ID in die Einstellung Basis-URL für eine beliebige Kampagnenkomponente aufnehmen, verschieben Sie sie in die entsprechende Einstellung des Suffix der Einstiegsseite .

1. (Empfohlen) Überprüfen Sie die Daten für dieses Konto in [!DNL Analytics] , bevor Sie zusätzliche Konten migrieren.

>[!MORELIKETHIS]
>
>* [Verwalten von Anzeigen-Netzwerkkonten](ad-network-account-manage.md)
>* [Von  [!DNL Analytics]](/help/integrations/analytics/ids.md) verwendete Adobe Advertising-IDs
>* [Überblick über  [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
