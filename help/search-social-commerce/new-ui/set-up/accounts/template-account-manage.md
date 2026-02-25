---
title: (Neue Benutzeroberfläche) Verwalten  [!DNL Naver]  Konten nur für das Tracking
description: Erfahren Sie, wie Sie Kontodetails in der neuen Benutzeroberfläche für ein -Konto einrichten  [!DNL Naver]  verwalten.
feature: Search Campaign Management
source-git-commit: 0de2a01905727314ca6c0792c5efaf6450548293
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Verwalten [!DNL Naver] Konten nur für das Tracking

*Beta-Funktion*

Im Folgenden finden Sie Anweisungen für die Verwaltung [[!DNL Naver] Konten](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md) zum Nachverfolgen, Erstellen von Berichten und Visualisieren der Leistung für die Anzeigen, die Sie direkt über das Werbenetzwerk kaufen. Search, Social und Commerce synchronisieren keine Daten mit dem Werbenetzwerk, bieten keine automatisierten Gebote und bieten keine Optimierungs- oder Simulationstypen.

Weitere Informationen zu den verfügbaren Funktionen finden Sie unter &quot;[Unterstütztes Inventar](/help/search-social-commerce/introduction/supported-inventory.md).

## Erstellen und Netzwerkkonto-Details {#create-account}

Um das Tracking eines Kontos zu aktivieren, müssen Sie einen entsprechenden Kontodatensatz mit den Anmeldedaten für den Kontozugriff und mit dem Status *aktiviert* erstellen.

>[!NOTE]
>
>Um ein tatsächliches Konto im Werbenetzwerk zu erstellen, gehen Sie zur Website des Werbenetzwerks.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Klicken Sie auf **[!UICONTROL Create Account]**.

1. Klicken Sie auf den Namen des Werbenetzwerks und dann auf **[!UICONTROL Next]**.

1. Geben Sie die [Kontoeinstellungen](#account-settings-naver) an:

   1. Geben Sie auf der Registerkarte **[!UICONTROL Enter Account Details]** die allgemeinen Kontoeinstellungen an.

   1. (Werbetreibende mit einer [[!DNL Adobe Analytics for Advertising] Integration](/help/integrations/analytics/overview.md)) Klicken Sie auf die Registerkarte **[!UICONTROL Set up Adobe Analytics]** und wählen Sie alle Reporting-Suites aus, [!DNL Analytics] für die Tracking- und Reporting-Kampagnenaktivität verwendet werden sollen.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Details zum Anzeigen-Netzwerkkonto bearbeiten {#edit-account}

Um den Kontonamen zu ändern, den Kontostatus zu ändern oder die [!DNL Analytics] Report Suites zu ändern, die für Tracking und Reporting verwendet werden sollen, bearbeiten Sie die Kontodetails.

>[!NOTE]
>
>Um ein tatsächliches Konto im Werbenetzwerk zu bearbeiten, gehen Sie auf die Website des Werbenetzwerks.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Wählen Sie das Konto auf eine der folgenden Arten aus:

   * Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]** .

   * Halten Sie den Cursor über den Kontonamen, klicken Sie auf **…** und dann auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie die [Kontoeinstellungen](#account-settings-api):

   1. (Optional) Bearbeiten Sie auf der Registerkarte **[!UICONTROL Account Details]** die Kontodetails.

   1. (Optional, Werbetreibende mit einer [[!DNL Adobe Analytics for Advertising] Integration](/help/integrations/analytics/overview.md)) Klicken Sie auf die Registerkarte **[!UICONTROL Set up Adobe Analytics]** und bearbeiten Sie die [!DNL Analytics] Reporting-Suites, die für die Tracking- und Reporting-Kampagnenaktivität verwendet werden sollen.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Klicken Sie auf **[!UICONTROL Save]**.

<!-- What does this do?

## Enable or disable ad network accounts {#enable-disable-account}

When you enable an ad network account, Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios. When you disable an ad network account, Search, Social, & Commerce stops all activity on the account. Data collected while the account was active is still stored, but the campaign management views and reports don't include data for the time period in which the account is disabled. You can later re-enable the account to resume activity with the account.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Do either of the following:

   * (From the [!UICONTROL Accounts] view):

     * (To enable the account) Select the check box next to the account name, and then click **[!UICONTROL Activate]** in the bulk actions toolbar.

     * (To disable the account) Select the check box next to the account name, and then click **[!UICONTROL Pause]** in the bulk actions toolbar.

   * (From the account settings):
   
     1. Select the account in either of the following ways:
     
        * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.
        
        * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.
        
     1. On the **[!UICONTROL Account Details]** tab, turn off **[!UICONTROL Account enabled]**.

     1. Click **[!UICONTROL Save]**.

-->

## Einstellungen für Netzwerkkonto hinzufügen {#account-settings-api}

### Registerkarte [!UICONTROL Account Details]

#### [!UICONTROL Enter Account Details]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** Der Name, der für das Konto in Search, Social und Commerce angezeigt werden soll.

>[!NOTE]
>
>Wenn Sie eine Integration zwischen Search, Social und Commerce und Adobe Analytics haben und den Namen des Suchkontos ändern, bitten Sie Ihr Adobe-Accountteam, die Zuordnung zu aktualisieren.

**[!UICONTROL Network Account ID]:** Die vom Werbenetzwerk zugewiesene Konto-ID.

**[!UICONTROL Currency]:** Die Abkürzung für die Währung, die für das Konto verwendet wird.

**[!UICONTROL Time Zone]:** Die Zeitzone des Werbetreibenden.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Search, Social und Commerce synchronisiert Kampagnendaten mit dem Konto (falls unterstützt) und pusht automatisierte Gebote und/oder Kampagnenbudgets für Kampagnen in Portfolios.

## Registerkarte [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (Werbetreibende mit einer [[!DNL Adobe Analytics for Advertising] Integration](/help/integrations/analytics/overview.md); optional) Eine oder mehrere Analytics-Report Suites, an die Search, Social und Commerce Daten sendet, die Sie für das Werbenetzwerk hochladen, einschließlich Entitätsklassifizierungen und Klickdaten für das Konto.

Damit die Daten in den Report Suites angezeigt werden, muss entweder (a) die Server-seitige AMO-ID-Funktion für das Konto konfiguriert sein oder (b) die Einstellung auf Advertiser-Ebene auf &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; aktiviert sein. Darüber hinaus muss das [!DNL Analytics] des Werbetreibenden so konfiguriert sein, dass es Daten von Search, Social und Commerce empfängt. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

>[!MORELIKETHIS]
>
>* [Nur [!DNL Naver] Tracking-Konten implementieren](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Über Werbenetzwerkkonten](/help/search-social-commerce/new-ui/set-up/accounts/ad-network-account-about.md)
