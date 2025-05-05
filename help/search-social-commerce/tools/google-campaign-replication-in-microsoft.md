---
title: Replizieren  [!DNL Google Ads]  Kampagnen in [!DNL Microsoft Advertising]
description: Erfahren Sie, wie Sie synchronisierte Kampagnen in einem - [!DNL Google Ads]  direkt in ein synchronisiertes - [!DNL Microsoft Advertising]  exportieren.
exl-id: e7714d3d-4a8e-44ef-a3a7-e5198c091660
feature: Search Tools
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# Replizieren [!DNL Google Ads] Kampagnen in [!DNL Microsoft Advertising]

Sie können synchronisierte Kampagnen in einem [!DNL Google Ads]-Konto direkt in ein synchronisiertes [!DNL Microsoft Advertising]-Konto als erweiterte CPC(eCPC)-Kampagnen exportieren. Die vorhandenen Angebote und Kampagnenbudgets werden skaliert. Vorhandenes Tracking für Suche, Social Media und Commerce wird nicht importiert.

Sie können die folgenden Kampagnentypen und ihre Kampagnenstruktur replizieren:

* [!DNL Google Ads] und Anzeigen von Kampagnen in [!DNL Microsoft Advertising] Kampagnen zum Suchen und Anzeigen.

* [!DNL Google Display Network] von Kampagnen, einschließlich Anzeigenbildern, in [!DNL Microsoft Advertising] Zielgruppenkampagnen im Microsoft Audience Network.

  Wenn Sie Shopping-Feed-basierte Display-Kampagnen replizieren möchten, replizieren Sie zunächst Ihre [!DNL Google Merchant Center] Produktangebote nach [!DNL Microsoft Merchant Center]. Wenn Sie die Kampagnen replizieren, wählen Sie in den Importoptionen den [!DNL Microsoft Merchant Center] Store aus, um den Store mit Ihren Feed-basierten Zielgruppenkampagnen zu verknüpfen.

* [!DNL Google Ads] von -Kampagnen mit dem Typ „Performance Max“, einschließlich lokaler Inventaranzeigen, in Kampagnen mit dem Typ „Performance Max“ [!DNL Microsoft Advertising].

Sie können die Kampagnen einmal, täglich, wöchentlich oder monatlich oder gemäß dem von [!DNL Microsoft Advertising] empfohlenen Zeitplan aktualisieren. Optional können Sie Benachrichtigungen bei jeder Ausführung eines Importvorgangs oder bei Fehlern oder Änderungen konfigurieren. Nachdem Sie Ihre Kampagnen in [!DNL Microsoft Advertising] importiert haben, können Sie den Status Ihres Importvorgangs überprüfen, alle Fehlerprotokolle ansehen, einen Importvorgang manuell ausführen und Ihren Importplan bearbeiten, anhalten, aktivieren oder löschen.

Nicht alle Kampagneninformationen werden repliziert, und Sie müssen möglicherweise einige Informationen zu Ihren [!DNL Microsoft Advertising] Kampagnen hinzufügen. Weitere Informationen dazu, welche Daten importiert werden, finden Sie [!DNL Microsoft Advertising] Hilfe unter &quot;[Was wird importiert? [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851). Da das Tracking nach Suche, Social und Commerce nicht importiert wird, sollten Sie auch Tracking in den Einstellungen [Konto](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [Kampagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [Anzeigengruppe](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) oder [Anzeige](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) hinzufügen.

## [!DNL Google Ads] Kampagnen replizieren

>[!NOTE]
>
>Wenn Sie Shopping-Feed-basierte Display-Kampagnen replizieren möchten, replizieren Sie zunächst [Ihre  [!DNL Google Merchant Center] -Angebote in [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). Wenn Sie die Kampagnen replizieren, wählen Sie in den Importoptionen den [!DNL Microsoft Merchant Center] Store aus, um den Store mit Ihren Feed-basierten Zielgruppenkampagnen zu verknüpfen.

Siehe [Was wird aus - [!DNL Google Ads]  importiert](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Klicken Sie im Hauptmenü von Search, Social und Commerce auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Klicken Sie auf **[!UICONTROL +Import]**.

1. Geben Sie die [Importeinstellungen](#campaign-import-settings) an:

   1. Im **[!UICONTROL Select accounts]** Abschnitt:

      1. Quell- und Zielkonten auswählen.

      1. Klicken Sie auf **[!UICONTROL Get Credential Id from MSA]**.

      1. Melden Sie sich beim Ziel-[!DNL Microsoft Advertising] an, kopieren Sie die angezeigte Berechtigungs-ID und fügen Sie den Wert in das Feld **[!UICONTROL Credential ID]** ein.

   1. Geben Sie im Abschnitt **[!UICONTROL Select campaigns & ad groups]** die zu importierenden Kampagnen und Anzeigengruppen an.

   1. Geben Sie im Abschnitt **[!UICONTROL Customize your import]** die zu importierenden Elementtypen an.

   1. Geben Sie im Abschnitt **[!UICONTROL Set schedule]** an, wann der Importvorgang ausgeführt werden soll.

1. Klicken Sie auf **[!UICONTROL Post]**.

1. (Optional) Fügen Sie Such-, Social- und Commerce-Tracking innerhalb der Einstellungen [Konto](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [Kampagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [Anzeigengruppe](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) oder [Anzeige](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) hinzu.

## Zeitplaneinstellungen für einen Kampagnen-Importauftrag bearbeiten

Siehe [Was wird aus - [!DNL Google Ads]  importiert](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben dem Importauftrag und klicken Sie dann auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

1. Geben Sie im Abschnitt **[!UICONTROL Set schedule]** die [Zeitplaneinstellungen](#campaign-import-settings) an.

1. Klicken Sie auf **[!UICONTROL Post]**.

## Anzeigen von Campaign-Importvorgängen

Sie können alle Importaufträge auflisten, einschließlich des [!DNL Google Ads], des Zielgruppen-[!DNL Microsoft Advertising], der Importzeit oder des Importplans und des Benutzers, der den Auftrag erstellt hat. Wenn Sie einen Importvorgang mehrmals ausführen, auch während regelmäßig geplanter Importe, wird jedes Vorkommen als separater Vorgang aufgelistet.

* Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

     Standardmäßig wird die Ansicht auf der Registerkarte [!UICONTROL List of Import Jobs] geöffnet.

   * Klicken Sie auf der [&#128279;](#campaign-import-log) [!UICONTROL Import Logs] auf die Registerkarte **[!UICONTROL List of Import Jobs]** .

## Ausführen eines Kampagnen-Importvorgangs

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben dem Importauftrag.

1. Klicken Sie ![Jetzt ausführen](/help/search-social-commerce/assets/run.png "Jetzt ausführen").

## Anzeigen von Protokollen für Campaign-Importvorgänge {#campaign-import-log}

Sie können alle abgeschlossenen oder fehlgeschlagenen Importvorgänge auflisten, einschließlich der Startzeit, des [!DNL Google Ads], des Zielgruppen-[!DNL Microsoft Advertising], des Benutzers, der den Auftrag erstellt hat, der Anzahl erfolgreicher und fehlgeschlagener Vorgänge und aller E-Mail-Adressen, die Benachrichtigungen für jeden Auftrag erhalten haben. Sie können weitere Details zu den Änderungen am [!DNL Microsoft Advertising]-Zielkonto anzeigen, die für jeden Auftrag aufgetreten sind, einschließlich der Anzahl der hinzugefügten, synchronisierten, gelöschten Elemente, die Fehler für jede Entitätsebene (z. B. Kampagne oder Keyword) im Konto verursacht haben.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Import Logs]** .

1. (Optional) Um Details zu einem Importvorgang anzuzeigen, klicken Sie auf den Wert in der Spalte [!UICONTROL Summary] .

## Einstellungen für Kampagnenimportaufträge {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** Das synchronisierte [!DNL Google Ads], aus dem Kampagnendaten exportiert werden.

**[!UICONTROL Credential ID]:** Eine ID, mit der [!DNL Microsoft Advertising] Ihre [!DNL Google Ads]-Anmeldeinformationen darstellt.

Die automatische Generierung von [!DNL Microsoft Advertising]-Anmeldeinformationen für den Import ist aufgrund von [!DNL Microsoft Advertising] nicht verfügbar. Wenden Sie sich an Ihr Adobe-Account-Team. Es generiert die Anmeldeinformationen und gibt Ihnen die ID.

**[!UICONTROL Target Microsoft Ads account]:** Das synchronisierte [!DNL Microsoft Advertising], in das Kampagnendaten importiert werden.

### [!UICONTROL Select campaigns & ad groups]

**\[Zu importierende Daten\]:** Geben Sie die zu importierenden Daten an:

* *[!UICONTROL Import all new and existing campaigns]:* Importieren von Daten für alle Kampagnen, die bereits vorhanden sind, und Kampagnen, die nicht in [!DNL Microsoft Advertising] vorhanden sind.

* *[!UICONTROL Import specific campaigns and adgroups]:* Um bestimmte Kampagnen und Anzeigengruppen auszuwählen.

   * Um eine Kampagne in ihre untergeordneten Anzeigengruppen zu erweitern, klicken Sie auf **[!UICONTROL >]** nach dem Kampagnennamen.

   * Um eine Kampagne oder eine Anzeigengruppe auszuwählen, wählen Sie das Element aus, sodass ein Häkchen angezeigt wird.

   * So entfernen Sie eine Kampagne oder Anzeigengruppe:

      * Heben Sie in der Spalte [!UICONTROL Campaigns] oder [!UICONTROL Adgroups] die Auswahl der Kampagne oder Anzeigengruppe auf, sodass das Häkchen ausgeblendet wird.

      * Klicken Sie in der Spalte [!UICONTROL Selected] auf ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Ermöglicht die Angabe von Importoptionen, Angeboten und Budgets sowie anderen Optionen.

**[!UICONTROL What to import]:** Definiert die zu importierenden Elemente. Optionen zum Importieren von Elementkategorien sind standardmäßig ausgewählt, wobei alle Elementtypen ausgewählt sind. Um nur bestimmte Elementtypen einzubeziehen, klicken Sie auf **[!UICONTROL Show advanced options]** und ändern Sie die Elementtypen so, dass sie enthalten sind.

**[!UICONTROL Bids and budgets]:** Definiert, welche Angebots- und Budgeteinstellungen importiert, aktualisiert und angepasst werden sollen.

**[!UICONTROL Other options]:** Definiert, wie importierte Landingpage-URLs, Tracking-Vorlagen und andere Kampagnen-, Anzeigen- und Targeting-Optionen verarbeitet werden.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** Der Name des Importvorgangs.

**[!UICONTROL When]:** Wann die angegebenen Kampagnen importiert werden sollen: *Auto* (damit [!DNL Microsoft Advertising] einen Zeitplan festlegen können, um Ihre Kampagnen am besten zu optimieren), *[!UICONTROL Now]* (um den Auftrag auszuführen, wenn Sie die Auftragseinstellungen veröffentlichen), *[!UICONTROL Once]* zu einem bestimmten Zeitpunkt, *[!UICONTROL Daily]* zu einem bestimmten Zeitpunkt, *[!UICONTROL Weekly]* zu einem bestimmten Zeitpunkt oder *[!UICONTROL Monthly]* zu einem bestimmten Zeitpunkt.

**[!UICONTROL Receive email notifications]:** Ob und wann E-Mail-Benachrichtigungen über Importvorgänge an die E-Mail-Adressen im Feld Berichte senden an gesendet werden sollen.

**[!UICONTROL Send reports to]:** E-Mail-Adressen, um Benachrichtigungen über Importvorgänge zu erhalten. Trennen Sie mehrere Adressen durch Kommas (`,`).
