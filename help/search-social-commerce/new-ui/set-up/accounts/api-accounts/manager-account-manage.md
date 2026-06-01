---
title: (Neue Benutzeroberfläche) Verwalten der Anmeldeinformationen für Google Ads Manager-Konten
description: Erfahren Sie, wie Sie Anmeldeinformationen für Google Ads Manager-Konten in der neuen Benutzeroberfläche einrichten und verwalten.
feature: Search Admin
source-git-commit: bf1ca7f6133c19bb68dbe0395416dca8ef647464
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Verwalten von Anmeldeinformationen für [!DNL Google Ads] Manager-Konten

*Beta-Funktion*

Nur *[!DNL Google Ads]Konten*

Geben Sie Anmeldeinformationen für Ihre [!DNL Google Ads] Manager-Konten an, für die Search, Social und Commerce kontoübergreifende Konversionen hochladen sollen. Verwenden Sie diese Funktion, wenn Sie a) [!DNL Adobe] nachverfolgte, kontenübergreifende Konversionsmetriken in ein [!DNL Google Ads] Manager-Konto hochladen möchten oder b) Portfolioziele hochladen möchten, die kontoübergreifende Konversionen in [!DNL Google Ads] für die Hybridoptimierung enthalten.

Sie können Anmeldeinformationen für neue Manager-Kontoeinträge hinzufügen oder ein vorhandenes Manager-Konto erneut authentifizieren.

Nachdem Sie Anmeldeinformationen für ein Manager-Konto hinzugefügt haben, zeigen die Kontoeinstellungen die ID des zugehörigen Manager-Kontos als schreibgeschützt an. [!UICONTROL Notification Center] umfasst [Benachrichtigungen](/help/search-social-commerce/new-ui/notifications-manage.md) wenn die Anmeldeinformationen eines Manager-Kontos fehlen (die [!UICONTROL Manager Account Missing Error]) oder wenn ein Authentifizierungstoken für das Manager-Konto abläuft (die [!UICONTROL Manager Account Auth Error]).

## Anmeldeinformationen für ein neues Manager-Konto hinzufügen {#create-manager-account}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Klicken Sie auf **[!UICONTROL +]**.

1. Wählen Sie das Anzeigennetzwerk aus und klicken Sie dann auf **[!UICONTROL Next]**.

1. Geben Sie die [Manager-Kontoeinstellungen](#manager-account-settings) an.

1. Klicken Sie auf **[!UICONTROL Authenticate]** und melden Sie sich mit den Anmeldedaten für das Manager-Konto an.

   Search, Social und Commerce erfassen und speichern das Authentifizierungstoken automatisch.

1. Klicken Sie unter Suche, Social und Commerce auf **[!UICONTROL Save]**.

## Manager-Kontodetails bearbeiten {#edit-manager-account}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Wählen Sie das Konto auf eine der folgenden Arten aus:

   * Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]** .

   * Halten Sie den Cursor über den Kontonamen, klicken Sie auf **…** und klicken Sie dann auf (/help/search-social-commerce/assets/edit-new.png „Bearbeiten„).

1. Bearbeiten Sie die [Manager-Kontoeinstellungen](#manager-account-settings).

1. Klicken Sie auf **[!UICONTROL Re-Authenticate]** und melden Sie sich mit den Anmeldedaten für das Manager-Konto an.

   Search, Social und Commerce erfassen und speichern das Authentifizierungstoken automatisch.

1. Klicken Sie unter Suche, Social und Commerce auf **[!UICONTROL Save]**.

## Erneutes Authentifizieren eines Manager-Kontos {#reauthenticate-manager-account}

Authentifizieren Sie ein Manager-Konto erneut, wenn das OAuth-Token abläuft oder ungültig wird.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Manager Accounts]**.

1. Halten Sie den Cursor über den Kontonamen, klicken Sie auf **…** und dann auf **[!UICONTROL Reauthenticate]**.

1. Melden Sie sich mit den Anmeldedaten für das Manager-Konto an.

   Search, Social und Commerce erfassen und speichern das neue Authentifizierungstoken automatisch.

## Manager-Kontoeinstellungen {#manager-account-settings}

**[!UICONTROL Manager Account ID]:** Die eindeutige Konto-ID für das Manager-Konto im Werbenetzwerk.

**[!UICONTROL Mnaager Account Name]:** Der Name, der für das Manager-Konto in Search, Social und Commerce angezeigt werden soll.

**[!UICONTROL Login Email]:** Die E-Mail-Adresse, die mit der Anmeldung beim Manager-Konto verknüpft ist. Für Authentifizierung erforderlich.

**[!UICONTROL Password]:** (Optional) Das Kennwort für das Konto. Geben Sie das Passwort ein, wenn Sie es verschlüsseln und speichern möchten, damit der Account Manager Token nach Bedarf aktualisieren kann.

>[!MORELIKETHIS]
>
>* [Hochladen von Zielen in Werbenetzwerke aktivieren](/help/search-social-commerce/new-ui/goals/objectives/objective-upload-to-networks.md)
>* [Benachrichtigungen verwalten](/help/search-social-commerce/new-ui/notifications-manage.md)

<!--
I don't see this yet in new UI:
>* [Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
-->
