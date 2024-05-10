---
title: Aktualisierung des Trackingcodes der AMO-ID (s_kwcid) für eine [!DNL Google Ads] account
description: Erfahren Sie, wie Sie zum neuesten AMO-ID-Trackingcode für eine [!DNL Google Ads] -Konto.
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Aktualisierung des Trackingcodes der AMO-ID (s_kwcid) für eine [!DNL Google Ads] account

*Advertiser nur mit Adobe Advertising-Adobe Analytics-Integration*

*[!DNL Google Ads]Nur Konten*

Das ältere (vor Oktober 2019) Format für [AMO-ID-Trackingcode](/help/integrations/analytics/ids.md#amo-id-formats) für bestehende [!DNL Google Ads] -Konten unterstützen einige Funktionen in Analytics nicht, z. B. Berichte auf Kampagnen- und Anzeigengruppenebene für [!DNL Google Ads] Kampagnen, Entwürfe und Experimente sowie andere Anwendungsfälle, in denen dieselbe Kombination aus Anzeige- und Suchbegriff- und Übereinstimmungstyp in mehreren Kampagnen vorhanden ist.

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

1. Halten Sie den Cursor über den Kontonamen und klicken Sie auf ![PfeilDropdown-Symbol](/help/search-social-commerce/assets/arrow-dropdown-menu.png)und wählen Sie **[!UICONTROL Edit]**.

1. Klicks **[!UICONTROL Set Account Tracking]**.

1. Starten Sie die Migration:

   1. Weiter zu **[!UICONTROL S_KWCID FORMAT]** klicken **[!UICONTROL LEGACY S_KWCID FORMAT]**.

   1. Klicks **[!UICONTROL Migrate to new s_kwcid format]**.

   1. Aktivieren Sie in der Bestätigungsmeldung das Kontrollkästchen und klicken Sie auf **[!UICONTROL Continue]**.

   1. Klicken Sie in den Kontoeinstellungen auf **[!UICONTROL Post]**.

   Die Metadaten für die Kampagnen werden in [!DNL Analytics] innerhalb weniger Tage. Das Tracking wird unterbrechungsfrei fortgesetzt, sodass keine Daten verloren gehen. Die Berichterstellung spiegelt die neuen Trackingcodes jedoch möglicherweise erst wider, wenn [!DNL Analytics] empfängt alle Metadaten.

   >[!NOTE]
   >
   >Alle Clickthroughs, die vor der Migration auftraten, melden weiterhin Konversionsdaten basierend auf dem alten Format.

1. Nachdem Sie mit der Migration begonnen haben, aktualisieren Sie die Einstellungen für das Suffix der Einstiegsseite (in einigen Werbenetzwerken als &quot;endgültiges URL-Suffix&quot;bezeichnet) nach Bedarf:

   * Wenn die Variable [!UICONTROL Auto Upload]&quot;-Funktion in den Tracking-Einstellungen aktiviert ist, aktualisiert Search, Social und Commerce den Trackingcode im Suffix der Einstiegsseite für dieses Konto und seine Kampagnen automatisch. Du brauchst nichts zu tun.

   * Wenn die Variable [!UICONTROL Auto Upload]&quot;nicht aktiviert ist und Sie die [serverseitige AMO-ID-Funktion](/help/integrations/analytics/ids.md#amo-id-formats)festgelegt ist, müssen Sie den AMO-ID-Parameter in den Einstellungen für das Suffix der Einstiegsseite manuell aktualisieren. Sie können die Suffixe auf Konto- und Kampagnenebene manuell in den Konto- und Kampagneneinstellungen ändern oder indem Sie Änderungen in ein Bulksheet hochladen. Um ein Suffix auf Anzeigengruppenebene oder niedriger zu konfigurieren, verwenden Sie die [!DNL Google Ads] Editor.

   * Wenn Sie die AMO-ID in die Einstellung Basis-URL für eine beliebige Kampagnenkomponente aufnehmen, verschieben Sie sie in die entsprechende Einstellung des Suffix der Einstiegsseite .

1. (Empfohlen) Überprüfen Sie die Daten für dieses Konto in [!DNL Analytics] bevor Sie zusätzliche Konten migrieren.

>[!MORELIKETHIS]
>
>* [Verwalten von Anzeigen-Netzwerkkonten](ad-network-account-manage.md)
>* [Von verwendete Adobe Advertising-IDs [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Übersicht über [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
