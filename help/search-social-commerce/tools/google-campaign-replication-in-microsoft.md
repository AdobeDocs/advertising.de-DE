---
title: Replizieren von [!DNL Google Ads] Kampagnen in [!DNL Microsoft Advertising]
description: Erfahren Sie, wie Sie Ihre synchronisierten Kampagnen direkt in ein [!DNL Google Ads] Konto in ein synchronisiertes [!DNL Microsoft Advertising] Konto exportieren.
exl-id: e7714d3d-4a8e-44ef-a3a7-e5198c091660
feature: Search Tools
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# Replizieren von [!DNL Google Ads] Kampagnen in [!DNL Microsoft Advertising]

Sie können Ihre synchronisierten Kampagnen in ein [!DNL Google Ads] -Konto direkt in ein synchronisiertes [!DNL Microsoft Advertising] -Konto als erweiterte CPC-Kampagnen (eCPC) exportieren. Die vorhandenen Angebote und Kampagnenbudgets werden skaliert. Vorhandenes Tracking von Suchen, Social und Commerce wird nicht importiert.

Sie können die folgenden Kampagnentypen und deren Kampagnenstruktur replizieren:

* [!DNL Google Ads] Suchkampagnen durchsuchen und in [!DNL Microsoft Advertising] Such- und Display-Kampagnen anzeigen.

* [!DNL Google Display Network] Kampagnen, einschließlich Anzeigenbilder, in [!DNL Microsoft Advertising] Zielgruppenkampagnen im Microsoft Audience Network.

  Wenn Sie Shopping-Feed-basierte Display-Kampagnen replizieren möchten, replizieren Sie zunächst Ihre [!DNL Google Merchant Center] -Produktangebote in [!DNL Microsoft Merchant Center]. Wenn Sie die Kampagnen replizieren, wählen Sie in den Importoptionen den Store [!DNL Microsoft Merchant Center] aus, um den Store mit Ihren Feed-basierten Zielgruppenkampagnen zu verknüpfen.

* [!DNL Google Ads] Leistungsmax-Kampagnen, einschließlich lokaler Lagerbestandsanzeigen, in [!DNL Microsoft Advertising] Leistungsmax-Kampagnen.

Sie können festlegen, dass die Kampagnen einmal, wöchentlich, monatlich oder gemäß dem von [!DNL Microsoft Advertising] empfohlenen Zeitplan aktualisiert werden. Sie können optional Benachrichtigungen bei jeder Ausführung eines Importvorgangs oder bei Fehlern oder Änderungen konfigurieren. Nachdem Sie Ihre Kampagnen in [!DNL Microsoft Advertising] importiert haben, können Sie den Status Ihres Importvorgangs überprüfen, alle Fehlerprotokolle überprüfen, einen Importauftrag manuell ausführen und Ihren Importplan bearbeiten, anhalten, aktivieren oder löschen.

Nicht alle Kampagneninformationen werden repliziert, und möglicherweise müssen Sie Ihren [!DNL Microsoft Advertising] -Kampagnen einige Informationen hinzufügen. Weitere Informationen dazu, welche Daten importiert werden, finden Sie in der [!DNL Microsoft Advertising] Hilfe zu &quot;[Was importiert wird von  [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851)&quot;. Da das Tracking von Suche, Social und Commerce nicht importiert wird, sollten Sie auch das Tracking in den Einstellungen [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) oder [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) hinzufügen.

## Replizieren von [!DNL Google Ads] Kampagnen

>[!NOTE]
>
>Wenn Sie auf Einkaufs-Feed basierende Display-Kampagnen replizieren möchten, replizieren Sie zunächst Ihre [!DNL Google Merchant Center] Produktangebote in  [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). [ Wenn Sie die Kampagnen replizieren, wählen Sie in den Importoptionen den Store [!DNL Microsoft Merchant Center] aus, um den Store mit Ihren Feed-basierten Zielgruppenkampagnen zu verknüpfen.

Siehe [Was wird aus  [!DNL Google Ads] Kampagnen](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500) importiert?

1. Klicken Sie im Hauptmenü von Search, Social und Commerce auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Klicken Sie auf **[!UICONTROL +Import]**.

1. Geben Sie die [Importeinstellungen](#campaign-import-settings) an:

   1. Im Abschnitt **[!UICONTROL Select accounts]** :

      1. Wählen Sie die Quell- und Zielkonten aus.

      1. Klicken Sie auf **[!UICONTROL Get Credential Id from MSA]**.

      1. Melden Sie sich beim Ziel-Konto [!DNL Microsoft Advertising] an, kopieren Sie die angezeigte Berechtigungs-ID und fügen Sie den Wert in das Feld **[!UICONTROL Credential ID]** ein.

   1. Geben Sie im Abschnitt **[!UICONTROL Select campaigns & ad groups]** die zu importierenden Kampagnen und Anzeigengruppen an.

   1. Geben Sie im Abschnitt **[!UICONTROL Customize your import]** die zu importierenden Elementtypen an.

   1. Geben Sie im Abschnitt **[!UICONTROL Set schedule]** an, wann der Importauftrag ausgeführt werden soll.

1. Klicken Sie auf **[!UICONTROL Post]**.

1. (Optional) Fügen Sie das Tracking von Suche, Social und Commerce in den Einstellungen [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) oder [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) hinzu.

## Planeinstellungen für einen Kampagnenimportauftrag bearbeiten

Siehe [Was wird aus  [!DNL Google Ads] Kampagnen](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500) importiert?

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben dem Importauftrag und klicken Sie auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

1. Geben Sie im Abschnitt **[!UICONTROL Set schedule]** die [Zeitplaneinstellungen](#campaign-import-settings) an.

1. Klicken Sie auf **[!UICONTROL Post]**.

## Anzeigen von Kampagnenimportaufträgen

Sie können alle Importvorgänge auflisten, einschließlich des Quell- [!DNL Google Ads]-Kontos, des Zielkontos [!DNL Microsoft Advertising], der Importzeit oder des Zeitplans sowie des Benutzers, der den Auftrag erstellt hat. Wenn Sie einen Importauftrag mehrmals ausführen, auch während regelmäßig geplanter Importe, wird jedes Vorkommen als separater Auftrag aufgeführt.

* Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

     Standardmäßig wird die Ansicht auf der Registerkarte [!UICONTROL List of Import Jobs] geöffnet.

   * Klicken Sie auf der Registerkarte [[!UICONTROL Import Logs] ](#campaign-import-log) auf die Registerkarte **[!UICONTROL List of Import Jobs]** .

## Kampagnenimportauftrag ausführen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben dem Importauftrag.

1. Klicken Sie auf ![Jetzt ausführen](/help/search-social-commerce/assets/run.png "Jetzt ausführen").

## Anzeigen von Protokollen für Kampagnenimportaufträge {#campaign-import-log}

Sie können alle abgeschlossenen oder fehlgeschlagenen Importvorgänge auflisten, einschließlich der Startzeit, des Quell-[!DNL Google Ads]-Kontos, des Ziel-1}-Kontos, des Benutzers, der den Auftrag erstellt hat, der Anzahl erfolgreicher und fehlgeschlagener Vorgänge sowie aller E-Mail-Adressen, an die Benachrichtigungen für jeden Auftrag gesendet wurden. [!DNL Microsoft Advertising] Sie können weitere Details zu den Änderungen am Zielkonto [!DNL Microsoft Advertising] anzeigen, die für jeden Auftrag aufgetreten sind, einschließlich der Anzahl der hinzugefügten, synchronisierten, gelöschten Elemente und der Fehler für jede Entitätsebene (z. B. Kampagne oder Keyword) im Konto.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Import Logs]** .

1. (Optional) Um Details zu einem Importauftrag anzuzeigen, klicken Sie auf den Wert in der Spalte [!UICONTROL Summary] .

## Einstellungen für den Campaign-Import-Auftrag {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** Das synchronisierte [!DNL Google Ads] Konto, aus dem Kampagnendaten exportiert werden.

**[!UICONTROL Credential ID]:** Eine ID, die [!DNL Microsoft Advertising] verwendet, um Ihre [!DNL Google Ads]-Anmeldeinformationen darzustellen.

Die automatische Generierung von [!DNL Microsoft Advertising] -Anmeldeinformationen für den Import ist aufgrund von [!DNL Microsoft Advertising] -Beschränkungen nicht verfügbar. Wenden Sie sich an Ihr Adobe Account-Team, das die Anmeldeinformationen generiert und Ihnen die Kennung gibt.

**[!UICONTROL Target Microsoft Ads account]:** Das synchronisierte [!DNL Microsoft Advertising] Konto, in das Kampagnendaten importiert werden.

### [!UICONTROL Select campaigns & ad groups]

**\[Zu importierende Daten\]:** Geben Sie die zu importierenden Daten an:

* *[!UICONTROL Import all new and existing campaigns]:* Importieren von Daten für alle bereits vorhandenen Kampagnen und Kampagnen, die nicht in [!DNL Microsoft Advertising] vorhanden sind.

* *[!UICONTROL Import specific campaigns and adgroups]:* So wählen Sie bestimmte Kampagnen und Anzeigengruppen aus.

   * Um eine Kampagne in ihre untergeordneten Anzeigengruppen zu erweitern, klicken Sie hinter dem Kampagnennamen auf **[!UICONTROL >]** .

   * Um eine Kampagne oder Anzeigengruppe auszuwählen, wählen Sie das Element aus, damit ein Häkchen angezeigt wird.

   * So entfernen Sie eine Kampagne oder Anzeigengruppe:

      * Heben Sie in der Spalte [!UICONTROL Campaigns] oder [!UICONTROL Adgroups] die Auswahl der Kampagne oder Anzeigengruppe auf, damit das Häkchen verschwindet.

      * Klicken Sie in der Spalte [!UICONTROL Selected] auf ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Ermöglicht Ihnen die Angabe, was importiert werden soll, Angebote und Budgets sowie andere Optionen.

**[!UICONTROL What to import]:** Definiert die zu importierenden Elemente. Optionen zum Importieren von Elementkategorien sind standardmäßig ausgewählt, wobei alle Elementtypen ausgewählt sind. Um nur bestimmte Elementtypen einzuschließen, klicken Sie auf **[!UICONTROL Show advanced options]** und ändern Sie die Elementtypen, die einbezogen werden sollen.

**[!UICONTROL Bids and budgets]:** Definiert, welche Gebots- und Budgeteinstellungen importiert, aktualisiert und angepasst werden sollen.

**[!UICONTROL Other options]:** Definiert, wie importierte Landingpage-URLs, Tracking-Vorlagen und andere Kampagnen-, Anzeigen- und Targeting-Optionen verarbeitet werden.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** Der Name des Importvorgangs.

**[!UICONTROL When]:** Wann die angegebenen Kampagnen importiert werden sollen: *Auto* (damit [!DNL Microsoft Advertising] einen Zeitplan für die bestmögliche Optimierung Ihrer Kampagnen festlegt), *[!UICONTROL Now]* (um den Auftrag beim Posten der Auftragseinstellungen auszuführen), *[!UICONTROL Once]* zu einer bestimmten Zeit, *[!UICONTROL Daily]* zu einer bestimmten Zeit, *[!UICONTROL Weekly]* zu einer bestimmten Zeit oder *[!UICONTROL Monthly]* zu einer bestimmten Zeit.

**[!UICONTROL Receive email notifications]:** Wenn und wann E-Mail-Benachrichtigungen über Importvorgänge an die E-Mail-Adressen im Feld Berichte senden an gesendet werden sollen.

**[!UICONTROL Send reports to]:** E-Mail-Adressen, an die Benachrichtigungen zu Importvorgängen gesendet werden. Trennen Sie mehrere Adressen durch Kommas (`,`).
