---
title: (Neue Benutzeroberfläche) Verwalten von Benachrichtigungen
description: Erfahren Sie, wie Sie Search-, Social- und Commerce-Benachrichtigungen, einschließlich Push-Benachrichtigungen und die Web-Anwendung des Benachrichtigungszentrums, anzeigen, konfigurieren und verwalten.
feature: Search Notifications
source-git-commit: e36a2b66a8dc4c485c7139b44eaf375615826b2b
workflow-type: tm+mt
source-wordcount: '1711'
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Verwalten von Benachrichtigungen

*Beta-Funktion*

Sie können Ihre Benachrichtigungseinstellungen so konfigurieren, dass verschiedene Arten von Warnhinweisen abonniert oder abbestellt werden. Sie haben folgende Möglichkeiten, um Ihre Benachrichtigungen anzuzeigen:

* Im Bedienfeld [!UICONTROL Notifications] , das oben rechts unter ![Benachrichtigungen](/help/search-social-commerce/assets/notifications.png "Benachrichtigungen verfügbar "). Im Bedienfeld können Sie die Liste filtern, Ihre Benachrichtigungseinstellungen bearbeiten oder [!UICONTROL Notification Center] öffnen.

* Von [!UICONTROL Notification Center], das in einem separaten Fenster außerhalb von Search, Social und Commerce geöffnet wird. Um [!UICONTROL Notification Center] im [!UICONTROL Notifications] zu öffnen, klicken Sie auf **[!UICONTROL View All]**.

* Über eine [!UICONTROL Notification Center] Web-Anwendung, die [!UICONTROL Notification Center] in einem separaten Fenster außerhalb von Search, Social und Commerce geöffnet wird.

  Die Anwendung lädt schneller als die normale Browser-Version und wird automatisch aktualisiert. Sie können die Anwendung installieren und mit dem App Manager des Browsers verwalten.

* Von Push-Benachrichtigungen an Ihren Browser.

  Wenn Sie Push-Benachrichtigungen aktivieren, werden sie gemäß den Benachrichtigungskonventionen des Browsers angezeigt.

Sie können Ihre Benachrichtigungen anzeigen, Benachrichtigungen als gelesen oder ungelesen markieren und Benachrichtigungen löschen.

## Benachrichtigungstypen

* **[!UICONTROL Notices]**: Versionshinweise, Ausfallzeiten und andere Hinweise zum Änderungs-Management.

* **[!UICONTROL Recommendations]**: Es wurden Möglichkeiten identifiziert, die Leistung zu verbessern, Best Practices zu implementieren usw.

* **[!UICONTROL Warnings]**: Probleme, die Aufmerksamkeit erfordern, aber für Optimierung oder Management nicht entscheidend sind.

* **[!UICONTROL Issues]**: Kritische Probleme, die sofortige Aufmerksamkeit erfordern. Benachrichtigungen zu Fehlern bei der Kontoautorisierung sind enthalten.

## Benachrichtigungskategorien

<!-- Update info, and update links to files for new UI once they're available-->

* [!UICONTROL Campaign Management]

   * **[!UICONTROL Bulksheets]**: Benachrichtigungen, dass ein [Bulksheet-Vorgang](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) abgeschlossen wurde oder fehlgeschlagen ist.<!-- Update link once file for new UI available-->

   * **[!UICONTROL Manager Account Missing]**: Benachrichtigungen, dass in Search, Social und Commerce die Anmeldeinformationen für ein [Ad Network Manager-Konto](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md) fehlen, die für die korrekte Einrichtung kritischer Funktionen erforderlich sind.<!-- Moving to Campaign Management > Setup Errors at some point -->

   * **[!UICONTROL UI Actions]**: Benachrichtigungen, dass Ihre im Hintergrund ausgeführten Aufträge abgeschlossen wurden oder fehlgeschlagen sind. Zu den Vorgangstypen gehören [Bulksheet-Aufträge](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)<!-- Update link once file for new UI available--> Massenbearbeitungsaufträge innerhalb der Datentabelle oder über die Symbolleiste, Entitätszuweisungsaufträge oder andere Aktionen in der Benutzeroberfläche (z. B. Synchronisieren mit Werbenetzwerken, Einfügen von Zeilen oder Umbenennen von Entitäten). Die Zuordnung von Entitäten umfasst die Zuweisung oder Aufhebung [ Zuweisung eines ](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md)Kennzeichnungswerts“ zu einer Entität, die Zuweisung einer Kampagne zu einem Portfolio und [die Zuweisung oder Aufhebung der Zuweisung einer Angebotsbegrenzung zu einer Entität](/help/search-social-commerce/new-ui/goals/constraints-manage.md).

   * [!UICONTROL Data Upload]

      * **[!UICONTROL Direct File Upload]**: Benachrichtigungen, dass eine Kontodatendatei hochgeladen wurde oder ein Hochladen von Kontodaten fehlgeschlagen ist, über [manuelles Hochladen von Kontodaten](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md). <!-- Verify description-->

      * **[!UICONTROL File Upload to Cloud Storage]**: Benachrichtigungen, dass eine Kontodatendatei hochgeladen wurde oder ein Hochladen von Kontodaten fehlgeschlagen ist, über [Hochladen von Kontodaten in einen [!DNL Amazon] [!DNL S3]-Bucket](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/upload-account-data.md). <!-- Verify description-->

   * [!UICONTROL Network Errors]

      * **[!UICONTROL Account Auth Error]**: Benachrichtigungen, dass Search, Social und Commerce aufgrund ungültiger Anmeldeinformationen oder eines ungültigen oder abgelaufenen Autorisierungstokens nicht auf ein [Ad-](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)-Netzwerkkonto zugreifen konnten.

      * **[!UICONTROL Account Missing]**: Benachrichtigungen, dass in Search, Social und Commerce die Anmeldeinformationen für ein [Ad-Netzwerkkonto“ ](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md).

      * **[!UICONTROL Manager Account Auth Error]**: Benachrichtigungen, dass Search, Social und Commerce aufgrund ungültiger Anmeldeinformationen oder eines ungültigen oder abgelaufenen Autorisierungstokens nicht mit einem [Ad Network Manager-](/help/search-social-commerce/admin/manager-accounts.md) synchronisiert werden konnte.<!-- Update link once file for new UI available-->

* [!UICONTROL Insights & Reports]

   * **[!UICONTROL Advertising Insights]**: Benachrichtigungen, dass [an [!DNL Advertising Insight]](/help/search-social-commerce/advertising-insights/insight-about.md) abgeschlossen wurde oder fehlgeschlagen ist.

   * **[!UICONTROL Custom Alerts]**: Benachrichtigungen, dass [Warnhinweisinstanzen](/help/search-social-commerce/new-ui/alerts-manage.md) für eine Warnhinweisvorlage ausgelöst wurden.

   * **[!UICONTROL Spreadsheet Feeds]**: Benachrichtigungen, dass ein [Tabellenfeed](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md) abgeschlossen wurde oder fehlgeschlagen ist.

   * [!UICONTROL Reports]

      * **[!UICONTROL Grid Reports]**: Benachrichtigungen, dass ein Datenansichtsbericht aus einer bestimmten Ansicht (wie der Inhalt der Datentabelle in der [!UICONTROL Camapigns]) abgeschlossen wurde oder fehlgeschlagen ist.

      * **[!UICONTROL Reports]**: Benachrichtigungen, dass ein [benutzerdefinierter oder terminierter Bericht](/help/search-social-commerce/new-ui/reports/management/report-manage.md) abgeschlossen wurde oder fehlgeschlagen ist.

   * [!UICONTROL Portfolio Management]

      * **[!UICONTROL Intraday Optimization]**: Benachrichtigungen, wenn die Intraday-Optimierung deaktiviert ist.

      * **[!UICONTROL Simulation Report]**: Benachrichtigungen über [Simulationsaufträge](/help/search-social-commerce/new-ui/plan/simulations/simulation-about.md).

      * [!UICONTROL Objective & Conversion Configuration]

         * **[!UICONTROL Auto Assign Campaign Conversion Goal - Advertiser Level]**: Benachrichtigungen auf Advertiser-Ebene über die erfolgreiche und fehlgeschlagene automatische Zuweisung von Kampagnen-Konversionszielen.

         * **[!UICONTROL Auto Assign Campaign Conversion Goal - Portfolio Level]**: Benachrichtigungen auf Portfolioebene über die erfolgreiche und fehlgeschlagene automatische Zuweisung von Kampagnenkonversionszielen.

      * [!UICONTROL Portfolios]

         * **[!UICONTROL Portfolio Bulksheet Diagnostic Report]**: Benachrichtigungen über [Portfolio-Massenbearbeitungs-Aufträge über Bulksheets](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-bulksheets.md).

         * **[!UICONTROL Portfolio Settings]**: Benachrichtigungen über [Änderungen an Portfolioeinstellungen](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-settings.md).

<!--

In Campaign Management:

  * [!UICONTROL Setup Errors]

    * **[!UICONTROL Adobe Analytics Tracking Setup Error]**: Notifications that an account-level landing page suffix is incorrect due to missing or incorrect [AMO ID (`s_kwcid` parameter)](/help/integrations/analytics/ids.md).
  
    * **[!UICONTROL Manager Account Missing]**: Notifications that Search, Social, & Commerce is missing the credentials for an [ad network manager account](/help/search-social-commerce/admin/manager-accounts.md), which are required for the correct setup of critical functions.

-->

<!--
* [!UICONTROL Optimization]

  * **[!UICONTROL Accuracy]**: Notifications when a portfolio's model accuracy deviates [by how much?] from expectations.
-->


## Verfügbare Aktionen

* [Anzeigen von Benachrichtigungen](#notification-view)

* [Benachrichtigungseinstellungen bearbeiten](#notification-edit)

* [Markieren einer Benachrichtigung als gelesen oder ungelesen](#notification-mark-read-unread)

* [Löschen einer Benachrichtigung](#notification-delete)

* [Push-Benachrichtigungen aktivieren und deaktivieren](#notification-push-enable-disable)

* [Installieren und Deinstallieren der [!UICONTROL Notification Center]-Webanwendung](#notification-app-install-uninstall)

## Anzeigen von Benachrichtigungen {#notification-view}

Wenn Sie [abonnierte Benachrichtigungen](#notification-edit) über Fehler bei der Kontoauthentifizierung, ausgelöste benutzerdefinierte Warnhinweise und generierte [!UICONTROL Advertising Insights] erhalten, können Sie Ihre Benachrichtigungen entweder im [!UICONTROL Notifications] oder im [!UICONTROL Notification Center] einsehen.

### Anzeigen von Benachrichtigungen im [!UICONTROL Notifications]

1. Klicken Sie oben rechts auf einer beliebigen Seite auf ![Benachrichtigungen](/help/search-social-commerce/assets/notifications.png "Benachrichtigungen").

1. (Optional) Führen Sie einen der folgenden Schritte aus:

   * Um die Details einer Benachrichtigung anzuzeigen, klicken Sie auf den Namen der Benachrichtigung.

     In einigen Benachrichtigungen kann der [!UICONTROL Action Recommended] einen Link enthalten, der eine gefilterte Ansicht der betroffenen oder verantwortlichen Entitäten öffnet.

   * Um eine Benachrichtigung als *gelesen* oder *ungelesen* zu markieren, halten Sie den Cursor über dem Namen des Warnhinweises und klicken Sie auf ![Als gelesen markieren oder ](/help/search-social-commerce/assets/notifications-read-unread.png "Als gelesen oder ungelesen markieren").

     Benachrichtigungen, die als *gelesen* gekennzeichnet sind, haben einen helleren Text, bleiben aber verfügbar, bis Sie sie löschen.

     ![Lesen und ungelesene Benachrichtigungen](/help/search-social-commerce/assets/notifications-read-vs-unread.png "Lesen und ungelesene Benachrichtigungen")

   * Um Ihre Abonnementvoreinstellungen für den Benachrichtigungstyp zu ändern, klicken Sie auf ![Einstellungen](/help/search-social-commerce/assets/settings-nc.png "Einstellungen") neben der Benachrichtigung, ändern Sie Ihre Einstellungen und klicken Sie dann auf **[!UICONTROL Save]**.

   * Um eine Benachrichtigung zu löschen, klicken Sie ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen") neben der Benachrichtigung.

   * Um [!UICONTROL Notification Center] zu öffnen, klicken Sie auf **[!UICONTROL View All]**.

### Anzeigen von Benachrichtigungen in [!UICONTROL Notification Center]

1. Klicken Sie oben rechts auf einer beliebigen Seite auf ![Benachrichtigungen](/help/search-social-commerce/assets/notifications.png "Benachrichtigungen").

1. Klicken Sie auf **[!UICONTROL View All]**.

1. (Optional) Um Ihre Benachrichtigungen nach Typ zu filtern, klicken Sie auf *[!UICONTROL Notices], [!UICONTROL Recommendations], [!UICONTROL Warnings] oder[!UICONTROL Issues]*.

1. (Optional) Führen Sie einen der folgenden Schritte aus:

   * Um die Details einer Benachrichtigung anzuzeigen, klicken Sie auf den Namen der Benachrichtigung.

     In einigen Benachrichtigungen kann der [!UICONTROL Action Recommended] einen Link enthalten, der eine gefilterte Ansicht der betroffenen oder verantwortlichen Entitäten öffnet.

   * Um eine Benachrichtigung als *gelesen* oder *ungelesen* zu markieren, halten Sie den Cursor über dem Namen des Warnhinweises und klicken Sie auf ![Als gelesen markieren oder ](/help/search-social-commerce/assets/notifications-read-unread.png "Als gelesen oder ungelesen markieren").

     Benachrichtigungen, die als *gelesen* gekennzeichnet sind, haben einen helleren Text, bleiben aber verfügbar, bis Sie sie löschen.

   * Um Ihre Abonnementvoreinstellungen für den Benachrichtigungstyp zu ändern, klicken Sie auf ![Einstellungen](/help/search-social-commerce/assets/settings-nc.png "Einstellungen") neben der Benachrichtigung, ändern Sie Ihre Einstellungen und klicken Sie dann auf **[!UICONTROL Save]**.

   * Um eine Benachrichtigung zu löschen, klicken Sie ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen") neben der Benachrichtigung.

## Benachrichtigungseinstellungen bearbeiten {#notification-edit}

Optional können Sie E-Mail- und Web-Benachrichtigungen zu Fehlern bei der Kontoauthentifizierung, alle ausgelösten benutzerdefinierten Warnhinweise und den Abschluss der von Ihnen generierten [!UICONTROL Advertising Insights] abonnieren oder davon abmelden.

1. Öffnen Sie die Benachrichtigungseinstellungen auf eine der folgenden Arten:

   * Klicken Sie oben rechts auf einer beliebigen Seite auf ![Benachrichtigungen](/help/search-social-commerce/assets/notifications.png "Benachrichtigungen"), um den [!UICONTROL Notifications] zu öffnen. Klicken Sie oben rechts auf ![Einstellungen](/help/search-social-commerce/assets/settings-nc.png "Einstellungen").

   * Klicken Sie oben rechts auf einer beliebigen Seite auf ![Benachrichtigungen](/help/search-social-commerce/assets/notifications.png "Benachrichtigungen") klicken Sie auf **[!UICONTROL View All]**, um [!UICONTROL Notification Center] zu öffnen, und klicken Sie dann im linken Menü auf ![Einstellungen](/help/search-social-commerce/assets/settings-nc.png "Einstellungen").

1. Ändern Sie Ihre Einstellungen für jede der oben aufgeführten Benachrichtigungskategorien:

   * Um Benachrichtigungen zu abonnieren oder zu kündigen, bewegen Sie den Schieberegler in die Spalte [!UICONTROL Subscribe] :

      * Um das Abonnement aller Benachrichtigungstypen zu kündigen, bewegen Sie den Schieberegler nach links (deaktiviert).

      * Um einen oder mehrere Benachrichtigungstypen zu abonnieren, bewegen Sie den Schieberegler nach rechts (aktiviert).

   * (Wenn [!UICONTROL Subscribe] aktiviert ist) Um E-Mail-Benachrichtigungen zu abonnieren, aktivieren Sie das Kontrollkästchen in der Spalte **[!UICONTROL Email]** .

   * (Wenn [!UICONTROL Subscribe] deaktiviert ist) Um Web-Benachrichtigungen in Search, Social und Commerce sowie Push-Benachrichtigungen zu abonnieren, wenn sie für den Browser aktiviert sind, aktivieren Sie das Kontrollkästchen in der Spalte **[!UICONTROL Web]** .

     Web-Benachrichtigungen werden nur gesendet, wenn Sie [Push-Benachrichtigungen aktivieren](#notification-push-enable-disable) in Ihrem Browser aktivieren.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Markieren einer Benachrichtigung als gelesen oder ungelesen {#notification-mark-read-unread}

Wenn Sie eine Benachrichtigung als *gelesen* oder *ungelesen* markieren, ändert sich die Anzahl der ungelesenen Benachrichtigungen, die im [!UICONTROL Notifications] Link oben auf jeder Seite angezeigt werden (z. B. ![Benachrichtigungssymbol mit dem Zähler für ungelesene Benachrichtigungen](/help/search-social-commerce/assets/notifications-unread.png "Benachrichtigungssymbol mit dem Zähler für ungelesene Benachrichtigungen")).

Benachrichtigungen, die als *gelesen* gekennzeichnet sind, haben einen helleren Text, bleiben aber verfügbar, bis Sie sie löschen.

![Lesen und ungelesene Benachrichtigungen](/help/search-social-commerce/assets/notifications-read-vs-unread.png "Lesen und ungelesene Benachrichtigungen")

1. [Öffnen Sie den Benachrichtigungsbereich oder das Benachrichtigungszentrum](#notification-view).

1. Halten Sie den Cursor über den Namen des Warnhinweises und klicken Sie auf ![Als gelesen oder Ungelesen markieren](/help/search-social-commerce/assets/notifications-read-unread.png "Als gelesen oder Ungelesen markieren").

## Löschen einer Benachrichtigung {#notification-delete}

### Löschen einer Benachrichtigung im [!UICONTROL Notifications]

1. Klicken Sie oben rechts auf einer beliebigen Seite auf ![Benachrichtigungen](/help/search-social-commerce/assets/notifications.png "Benachrichtigungen").

1. Klicken Sie ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen") neben der Benachrichtigung.

### Löschen einer Benachrichtigung in [!UICONTROL Notification Center]

1. Klicken Sie oben rechts auf einer beliebigen Seite auf ![Benachrichtigungen](/help/search-social-commerce/assets/notifications.png "Benachrichtigungen").

1. Klicken Sie auf **[!UICONTROL View All]**.

1. (Optional) Um Ihre Benachrichtigungen nach Typ zu filtern, klicken Sie auf *[!UICONTROL Notices]*, *[!UICONTROL Recommendations]*, *[!UICONTROL Warnings]* oder *[!UICONTROL Issues]*.

1. Klicken Sie ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen") neben der Benachrichtigung.

## Push-Benachrichtigungen aktivieren und deaktivieren {#notification-push-enable-disable}

Sie können Benachrichtigungen in Search, Social und Commerce aktivieren, wo sie gemäß den Benachrichtigungskonventionen des Browsers angezeigt werden. Auf Geräten, die [!DNL Microsoft Windows] verwenden, werden Benachrichtigungen in der rechten unteren Ecke des Bildschirms (Taskleiste) angezeigt. Auf [!DNL Apple Mac] Geräten werden Benachrichtigungen im rechten Menü angezeigt.

Push-Benachrichtigungen sind in den folgenden Browsern verfügbar:

* [!DNL Google Chrome] 40 und höher

* [!DNL Microsoft Edge] 17 und höher

* [!DNL Mozilla Firefox] 44 und höher

Sie können Push-Benachrichtigungen gemäß dem Standardverfahren des Browsers deaktivieren.

### Push-Benachrichtigungen aktivieren

1. Klicken Sie oben rechts auf einer beliebigen Seite auf ![Benachrichtigungen](/help/search-social-commerce/assets/notifications.png "Benachrichtigungen").

1. Klicken Sie auf **[!UICONTROL View All]**.

1. Klicken Sie unten rechts auf ![Push-Benachrichtigungen aktivieren](/help/search-social-commerce/assets/notifications-push.png "Push-Benachrichtigungen aktivieren").

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Enable]**.

1. Konfigurieren Sie den Browser so, dass Benachrichtigungen von [!UICONTROL Notification Center] unter `https://alert-center-ui-na.efrontier.com` zugelassen werden.

   Die standardmäßigen Benachrichtigungseinstellungen variieren je nach Browser. Möglicherweise wird Ihnen entweder a) automatisch die Option zum Zulassen von Benachrichtigungen von [!UICONTROL Notification Center] angezeigt oder b) Sie müssen die Benachrichtigungseinstellungen manuell verwalten. In [!DNL Microsoft Edge] können Sie beispielsweise Benachrichtigungen von [!UICONTROL Notification Center] aus der Browser-Symbolleiste aus zulassen. Weitere Informationen finden Sie in den Anweisungen in der Browser-Hilfe.

   ![Verwalten von Benachrichtigungseinstellungen in Microsoft Edge](/help/search-social-commerce/assets/notifications-blocked-dialog.png "Verwalten von Benachrichtigungseinstellungen in Microsoft Edge")

1. Aktivieren Sie [Benachrichtigungseinstellungen](#notification-edit) die [!UICONTROL Web] Benachrichtigungen für die Warnhinweistypen, die gepusht werden sollen.

### Push-Benachrichtigungen deaktivieren

Entfernen Sie Benachrichtigungen aus `https://alert-center-ui-na.efrontier.com` im Benachrichtigungs-Manager des Browsers. In [!DNL Google Chrome] können Sie beispielsweise Benachrichtigungen von bestimmten Sites unter `chrome://settings/content/notifications` entfernen oder blockieren.

Weitere Informationen finden Sie in den Anweisungen in der Browser-Hilfe.

## Installieren und Deinstallieren der [!UICONTROL Notification Center]-Webanwendung {#notification-app-install-uninstall}

Sie können Benachrichtigungen außerhalb Ihres Browsers empfangen und verwalten, indem Sie eine [!UICONTROL Notification Center] Web-Anwendung installieren. Die Anwendung sieht genauso aus und verfügt über dieselben Funktionen, wie sie in Search, Social und Commerce [!UICONTROL Notification Center] sind. Die Anwendung ist für [!DNL Google Chrome] 40 und höher oder [!DNL Microsoft Edge] 17 und höher verfügbar.

Nachdem Sie die [!UICONTROL Notification Center] installiert haben, wird sie automatisch im Anwendungs-Manager des Browsers aktiviert und als separates Fenster geladen, dessen Layout dynamisch auf der Grundlage der Fenstergröße angeordnet wird. Sie können die Anwendung über den Anwendungs-Manager des Browsers öffnen und schließen oder an die Taskleiste oder das Dock des Betriebssystems anheften. Die Anwendung wird automatisch aktualisiert.

![Benachrichtigungszentrum-Symbol in Microsoft Windows-Taskleiste](/help/search-social-commerce/assets/windows-taskbar.png "Benachrichtigungszentrum-Symbol in Microsoft Windows-Taskleiste")

Sie können die Anwendung im Anwendungs-Manager des Browsers deaktivieren oder deinstallieren. Weitere Informationen zum Verwalten von Web-Anwendungen finden Sie in der Browser-Hilfe.

### Installieren der [!UICONTROL Notification Center]-Webanwendung für [!DNL Google Chrome]

1. Klicken Sie oben rechts auf einer beliebigen Seite auf ![Benachrichtigungen](/help/search-social-commerce/assets/notifications.png "Benachrichtigungen").

1. Klicken Sie auf **[!UICONTROL View All]**.

1. Klicken Sie unten rechts auf ![Benachrichtigungszentrum-Webanwendung installieren](/help/search-social-commerce/assets/notifications-install-app.png "Benachrichtigungszentrum-Webanwendung installieren").

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Add]**.

1. In der Install App? Nachricht, klicken Sie auf **[!UICONTROL Install]**.

### Installieren der [!UICONTROL Notification Center]-Webanwendung für [!DNL Microsoft Edge]

* Innerhalb von Search, Social und Commerce:

   1. Klicken Sie oben rechts auf einer beliebigen Seite auf ![Benachrichtigungen](/help/search-social-commerce/assets/notifications.png "Benachrichtigungen").

   1. Klicken Sie auf **[!UICONTROL View All]**.

   1. Klicken Sie unten rechts auf ![Benachrichtigungszentrum-Webanwendung installieren](/help/search-social-commerce/assets/notifications-install-app.png "Benachrichtigungszentrum-Webanwendung installieren").

   1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Add]**.

   1. Klicken Sie in der [!UICONTROL Install Notification Center] App-Nachricht auf **[!UICONTROL Install]**.

* Vom [!DNL Edge] Hauptmenü:

   1. Klicken Sie in der Browser-Symbolleiste auf **…** > **[!UICONTROL Apps]** > **[!UICONTROL Install Notification Center]**.

   1. Klicken Sie in der [!UICONTROL Install Notification Center] App-Nachricht auf **[!UICONTROL Install]**.

### Deinstallieren der [!UICONTROL Notification Center]-Webanwendung für [!DNL Google Chrome]

* Gehen Sie [!DNL Chrome] zu `chrome://apps`, klicken Sie mit der rechten Maustaste auf **[!UICONTROL notification-center]**, und klicken Sie dann auf **[!UICONTROL Remove from Chrome]**.

### Deinstallieren der [!UICONTROL Notification Center]-Webanwendung für [!DNL Microsoft Edge]

1. Klicken Sie in der [!DNL Edge] Browser-Symbolleiste auf **…** > **[!UICONTROL Apps]** > **[!UICONTROL Manage apps]**. Gehen Sie alternativ zu `edge://apps`.

1. Klicken Sie mit der rechten Maustaste auf **[!UICONTROL Notification Center]** und dann auf **[!UICONTROL Uninstall]**.
