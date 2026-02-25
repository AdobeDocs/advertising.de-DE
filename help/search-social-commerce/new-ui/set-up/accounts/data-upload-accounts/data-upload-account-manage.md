---
title: Konfigurieren von Ad-Network-Konten für den Datenupload
description: Erfahren Sie, wie Sie Kontodetails für ein Anzeigennetzwerkkonto einrichten und verwalten.
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 0%

---

# Verwalten von Anzeigen-Netzwerkkonten für Daten-Uploads

<!-- Edit all, including title and metadata -->

Im Folgenden finden Sie Anweisungen zum Verwalten von Kontodetails für Anzeigennetzwerkkonten, für die Sie die Kontodaten hochladen.

Einzelheiten zu den für die einzelnen Werbenetzwerke verfügbaren Funktionen finden Sie unter &quot;[Unterstützte Inventarisierung](/help/search-social-commerce/introduction/supported-inventory.md).

>[!NOTE]
>
>Anweisungen zum Verwalten von Kontodetails für ein Anzeigennetzwerkkonto, das mithilfe der API des Anzeigennetzwerks mit Search, Social und Commerce synchronisiert wird, finden Sie stattdessen unter [Verwalten von Anzeigennetzwerkkonten über eine API-Verbindung](../api-accounts/api-account-manage.md).

## Kontodetails erstellen {#create-account}

1. Klicken Sie auf **[!UICONTROL Create Account]**.

1. Klicken Sie auf den Namen des Werbenetzwerks und dann auf **[!UICONTROL Next]**.

1. Geben Sie die [Kontoeinstellungen](#account-settings) an:

   1. Bearbeiten Sie auf der Registerkarte **[!UICONTROL Account Details]** die Kontodetails.

   1. (Werbetreibende mit einer [[!DNL Adobe Analytics for Advertising]-Integration] (/help/integrations/analytics/overview.md) Klicken Sie auf die Registerkarte **[!UICONTROL Set up Adobe Analytics]** und bearbeiten Sie die [!DNL Analytics] Reporting-Suites, die für die Tracking- und Reporting-Kampagnenaktivität verwendet werden sollen.

   1. (Optional) Laden Sie auf der Registerkarte &quot;**[!UICONTROL Upload File]**&quot; Datendateien für das Konto hoch.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Kontodetails bearbeiten {#edit-account}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Wählen Sie das Konto auf eine der folgenden Arten aus:

   * Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]** .

   * Halten Sie den Cursor über den Kontonamen, klicken Sie auf **…** und dann auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie die [Kontoeinstellungen](#account-settings-upload):

   1. (Optional) Bearbeiten Sie auf der Registerkarte **[!UICONTROL Account Details]** die Kontodetails.

   1. (Optional, Werbetreibende mit einer [[!DNL Adobe Analytics for Advertising] Integration](/help/integrations/analytics/overview.md)) Klicken Sie auf die Registerkarte **[!UICONTROL Set up Adobe Analytics]** und bearbeiten Sie die [!DNL Analytics] Reporting-Suites, die für die Tracking- und Reporting-Kampagnenaktivität verwendet werden sollen.

   1. (Optional) Laden Sie auf der Registerkarte &quot;**[!UICONTROL Upload File]**&quot; Datendateien für das Konto hoch.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Klicken Sie auf **[!UICONTROL Save]**.

## Aktivieren oder Deaktivieren von Anzeigennetzwerkkonten {#enable-disable-account}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Führen Sie einen der folgenden Schritte aus:

   * (Aus der [!UICONTROL Accounts]):

      * (Um das Konto zu aktivieren) Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Activate]** .

      * (So deaktivieren Sie das Konto) Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Pause]** .

   * (Aus den Kontoeinstellungen):

      1. Wählen Sie das Konto auf eine der folgenden Arten aus:

         * Halten Sie den Cursor über den Kontonamen, klicken Sie auf **…** und dann auf **[!UICONTROL Edit]**.

         * Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]** .

      1. Deaktivieren Sie auf der Registerkarte **[!UICONTROL Account Details]** die Option **[!UICONTROL Account enabled]**.

      1. Klicken Sie auf **[!UICONTROL Save]**.

## Kontoeinstellungen {#account-settings-upload}

### Registerkarte [!UICONTROL Account Details]

**[!UICONTROL Account Name]:** Der Name, der für das Konto in Search, Social und Commerce angezeigt werden soll.

>[!NOTE]
>
>Wenn Sie eine Integration zwischen Search, Social und Commerce und Adobe Analytics haben und den Namen des Suchkontos ändern, benachrichtigen Sie Ihr Adobe-Accountteam, damit es die Zuordnung aktualisieren kann.

**[!UICONTROL Network Account ID]:** Die vom Werbenetzwerk zugewiesene Konto-ID. Diese ID wird nur für das Reporting verwendet. Search, Social und Commerce stellen keine direkte Verbindung mit dem Anzeigennetzwerkkonto her.

**[!UICONTROL Currency]:** (Schreibgeschützt für vorhandene Konten) Die Abkürzung für die für das Konto verwendete Währung.

**[!UICONTROL Time Zone]:** (Schreibgeschützt für vorhandene Konten) Die Zeitzone des Werbetreibenden.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Search, Social und Commerce ermöglichen den automatischen Datenabruf für einen bestimmten S3-Bucket.

## Registerkarte [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (Werbetreibende mit einer [[!DNL Adobe Analytics for Advertising] Integration](/help/integrations/analytics/overview.md); optional) Eine oder mehrere Analytics-Report Suites, an die Search, Social und Commerce Daten sendet, die Sie für das Werbenetzwerk hochladen, einschließlich Entitätsklassifizierungen und Klickdaten für das Konto.

Damit die Daten in den Report Suites angezeigt werden, muss entweder (a) die Server-seitige AMO-ID-Funktion für das Konto konfiguriert sein oder (b) die Einstellung auf Advertiser-Ebene auf &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; aktiviert sein. Darüber hinaus muss das [!DNL Analytics] des Werbetreibenden so konfiguriert sein, dass es Daten von Search, Social und Commerce empfängt. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

### Registerkarte [!UICONTROL Upload File]

(Optional) Laden Sie Datendateien für das Konto hoch.<!-- For instructions, see "[Upload offline account data for reporting and simulations](upload-account-data.md)." -->
