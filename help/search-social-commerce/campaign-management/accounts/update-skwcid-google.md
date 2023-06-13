---
title: "Aktualisieren Sie den s\_kwcid-Trackingcode für eine [!DNL Google Ads] account"
description: Erfahren Sie, wie Sie zum neuesten s\_kwcid-Trackingcode für eine [!DNL Google Ads] -Konto.
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# Aktualisieren Sie den s\_kwcid-Trackingcode für eine [!DNL Google Ads] account

*Advertiser mit nur einer Adobe-Advertising-Adobe Analytics-Integration*

*[!DNL Google Ads]Nur Konten*

Das alte Format für den s\_kwcid-Trackingcode für vorhandene [!DNL Google Ads] -Konten unterstützen einige Funktionen in Analytics nicht, z. B. Berichte auf Kampagnen- und Anzeigengruppenebene für [!DNL Google Ads] Kampagnen, Entwürfe und Experimente sowie andere Anwendungsfälle, in denen dieselbe Kombination aus Anzeige- und Suchbegriff- und Übereinstimmungstyp in mehreren Kampagnen vorhanden ist.

Das neueste Format enthält Parameter für die Kampagnen-ID und Anzeigengruppen-ID:

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

Sie können das neue Format für jedes oder alle Ihrer vorhandenen Konten einzeln ändern. Wenn Sie keine Kampagnen, Entwürfe und Experimente mit maximaler Leistung haben, ist eine Migration in das neue Format optional.

Alle neuen [!DNL Google Ads] -Konten verwenden automatisch das neue s\_kwcid -Format.

>[!NOTE]
>
>Nachdem Sie ein Konto migriert haben, werden alle Klick-, Kosten- und Impressionsdaten nach der Änderung korrekt gemeldet, aber alle Clickthroughs, die vor der Migration stattgefunden haben, werden weiterhin Konversionsdaten basierend auf dem alten s\_kwcid-Format zugeordnet.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.
1. Halten Sie den Cursor über den Kontonamen und klicken Sie auf ![PfeilDropdown-Symbol](/help/search-social-commerce/assets/arrow-dropdown-menu.png)und wählen Sie **[!UICONTROL Edit]**.
1. Klicken **[!UICONTROL Set Account Tracking]**.
1. Starten Sie die Migration:

   1. Weiter zu **[!UICONTROL S_KWCID FORMAT]** klicken **[!UICONTROL LEGACY S_KWCID FORMAT]**.
   1. Klicken **[!UICONTROL Migrate to new s_kwcid format]**.
   1. Aktivieren Sie in der Bestätigungsmeldung das Kontrollkästchen und klicken Sie auf **[!UICONTROL Continue]**.
   1. Klicken Sie in den Kontoeinstellungen auf **[!UICONTROL Post]**.

   Die Metadaten für die Kampagnen werden in Analytics innerhalb weniger Tage aktualisiert. Das Tracking wird unterbrechungsfrei fortgesetzt, sodass keine Daten verloren gehen. Die Berichterstellung spiegelt die neuen Trackingcodes jedoch möglicherweise erst wider, wenn Analytics alle Metadaten erhält.

   >[!NOTE]
   >
   >Alle Clickthroughs, die vor der Migration aufgetreten sind, melden weiterhin Konversionsdaten basierend auf dem alten Format.

1. Nachdem Sie mit der Migration begonnen haben, aktualisieren Sie die Einstellungen für das Suffix der Einstiegsseite (in einigen Werbenetzwerken als &quot;endgültiges URL-Suffix&quot;bezeichnet) nach Bedarf:

   * Wenn die [!UICONTROL Auto Upload]&quot;-Funktion in den Tracking-Einstellungen aktiviert ist, aktualisiert Search, Social und Commerce den Trackingcode im Suffix der Einstiegsseite für dieses Konto und seine Kampagnen automatisch. Du brauchst nichts zu tun.
   * Wenn die [!UICONTROL Auto Upload]&quot;-Funktion nicht aktiviert ist und Sie nicht die serverseitige s-kwcid verwenden, müssen Sie den Parameter s\_kwcid in den Einstellungen für das Suffix der Einstiegsseite manuell aktualisieren. Sie können die Suffixe auf Konto- und Kampagnenebene manuell in den Konto- und Kampagneneinstellungen ändern oder indem Sie Änderungen in ein Bulksheet hochladen. Um ein Suffix auf Anzeigengruppenebene oder niedriger zu konfigurieren, verwenden Sie die [!DNL Google Ads] Editor.
   * Wenn Sie die s\_kwcid in die Basis-URL-Einstellung für eine beliebige Kampagnenkomponente aufnehmen, verschieben Sie sie in die entsprechende Einstellung für das Suffix der Einstiegsseite.

1. (Empfohlen) Überprüfen Sie die Daten für dieses Konto in Analytics, bevor Sie zusätzliche Konten migrieren.

>[!MORELIKETHIS]
>
>* [Verwalten von Anzeigen-Netzwerkkonten](ad-network-account-manage.md)
>* [Der Tracking-Parameter s_kwcid](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md)
>* [Übersicht über [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
