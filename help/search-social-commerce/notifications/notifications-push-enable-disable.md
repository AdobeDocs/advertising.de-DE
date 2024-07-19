---
title: Push-Benachrichtigungen über [!UICONTROL Notification Center] aktivieren und deaktivieren
description: Erfahren Sie, wie Sie Push-Benachrichtigungen über [!UICONTROL Notification Center] aktivieren und deaktivieren.
exl-id: f0e91e76-eb1e-4ff0-9a52-e9bc587552a2
feature: Search Notifications
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# Push-Benachrichtigungen über [!UICONTROL Notification Center] aktivieren und deaktivieren

*Beta-Funktion*

Sie können Benachrichtigungen in Search, Social und Commerce aktivieren, wenn sie gemäß den Benachrichtigungskonventionen des Browsers angezeigt werden. Auf Geräten, die [!DNL Microsoft Windows] verwenden, werden Benachrichtigungen unten rechts im Bildschirm (Systemablage) angezeigt. Auf [!DNL Apple Mac] -Geräten werden Benachrichtigungen im rechten Menü angezeigt.

Push-Benachrichtigungen sind in den folgenden Browsern verfügbar:

* [!DNL Google Chrome] 40 und höher

* [!DNL Microsoft Edge] 17 und höher

* [!DNL Mozilla Firefox] 44 und höher

Sie können Push-Benachrichtigungen entsprechend der üblichen Vorgehensweise des Browsers deaktivieren.

## Push-Benachrichtigungen aktivieren

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** > **[!UICONTROL Insights & Reports]** > **[!UICONTROL Notification Center Beta]**.

2. Klicken Sie unten rechts auf ![Push-Benachrichtigungen aktivieren](/help/search-social-commerce/assets/notifications-push.png "Push-Benachrichtigungen aktivieren").

3. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Enable]**.

4. Konfigurieren Sie den Browser so, dass Benachrichtigungen von [!UICONTROL Notification Center] bei `https://alert-center-ui-na.efrontier.com` zugelassen werden.

   Die standardmäßigen Benachrichtigungseinstellungen variieren je nach Browser. Sie können a) automatisch mit der Option angezeigt werden, Benachrichtigungen von [!UICONTROL Notification Center] zuzulassen oder b) die Benachrichtigungseinstellungen manuell verwalten. In [!DNL Microsoft Edge] können Sie beispielsweise Benachrichtigungen von [!UICONTROL Notification Center] aus der Browser-Symbolleiste zulassen. Siehe Anweisungen in der Hilfe des Browsers.

   ![Wo Sie Benachrichtigungseinstellungen in Microsoft Edge verwalten](/help/search-social-commerce/assets/notifications-blocked-dialog.png "wo Sie Benachrichtigungseinstellungen in Microsoft Edge verwalten")

5. Aktivieren Sie in den [Benachrichtigungseinstellungen](notification-edit.md) die [!UICONTROL Web] -Benachrichtigungen für die Warnhinweistypen, die gepusht werden sollen.

## Push-Benachrichtigungen deaktivieren

Entfernen Sie Benachrichtigungen aus `https://alert-center-ui-na.efrontier.com` im Benachrichtigungs-Manager des Browsers. In [!DNL Google Chrome] können Sie beispielsweise Benachrichtigungen von bestimmten Sites unter `chrome://settings/content/notifications` entfernen oder blockieren.

Siehe Anweisungen in der Hilfe des Browsers.

>[!MORELIKETHIS]
>
>* [Über Benachrichtigungen](/help/search-social-commerce/notifications/notification-about.md)
>* [Anzeigen Ihrer Benachrichtigungen](notification-view.md)
>* [Kennzeichnen einer Benachrichtigung als gelesen oder ungelesen](notification-mark-read-unread.md)
>* [Löschen einer Benachrichtigung](notification-delete.md)
>* [Bearbeiten der Benachrichtigungseinstellungen](notification-edit.md)
>* [Installieren und Deinstallieren der [!UICONTROL Notification Center] Webanwendung](notification-app-install-uninstall.md)
