---
title: Verwalten von Anmeldeinformationen für Ad Network Manager-Konten
description: Erfahren Sie, wie Sie Anmeldeinformationen für Ihre  [!DNL Google Ads] -Manager-Konten bereitstellen.
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# Verwalten von Anmeldeinformationen für Ad Network Manager-Konten

Nur *[!DNL Google Ads]Konten*

Geben Sie die Anmeldeinformationen für Ihre [!DNL Google Ads] Manager-Konten an, für die Search, Social und Commerce kontoübergreifende Konversionen hochladen sollen. Verwenden Sie diese Funktion, wenn Sie a) [!DNL Adobe] nachverfolgte, kontenübergreifende Konversionsmetriken in ein [!DNL Google Ads] Manager-Konto hochladen möchten oder b) Portfolioziele hochladen möchten, die kontoübergreifende Konversionen in [!DNL Google Ads] für die Hybridoptimierung enthalten.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

Sie können Anmeldeinformationen für neue Manager-Kontoeinträge hinzufügen oder ein vorhandenes Manager-Konto erneut authentifizieren.

Nachdem Sie Anmeldeinformationen für ein Manager-Konto hinzugefügt haben, zeigen die Kontoeinstellungen die ID des zugehörigen Manager-Kontos als schreibgeschützt an. Darüber hinaus zeigt eine optionale Spalte &quot;[!UICONTROL Manager Account for Cross-Account Conversions]&quot; in der Ansicht [!UICONTROL Campaigns] > [!UICONTROL Accounts] die Manager-Konto-ID für jedes untergeordnete Konto an und zeigt einen Fehler an, wenn das Manager-Konto nicht authentifiziert ist. [!UICONTROL Notification Center] umfasst Benachrichtigungen, wenn die Anmeldeinformationen eines Manager-Kontos fehlen ([die [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) oder wenn ein Authentifizierungstoken für das Manager-Konto abläuft ([die [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## So fügen Sie Anmeldeinformationen für ein neues Manager-Konto hinzu

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Wählen Sie **[!UICONTROL Create new manager account]** aus.

1. Geben Sie die Anmeldeinformationen für das Manager-Konto ein.

   **[!UICONTROL Manager Account ID]** und **[!UICONTROL Login Email]** sind erforderlich. Search, Social und Commerce erfasst und speichert automatisch das Konto-Token, das für die Authentifizierung verwendet werden soll.

   Sie können optional eine **[!UICONTROL MCC Account Name]** zur Identifizierung in Search, Social und Commerce und die **[!UICONTROL Password]** einschließen. Geben Sie das Passwort ein, wenn Sie es verschlüsseln und speichern möchten, damit der Account Manager Token nach Bedarf aktualisieren kann.

1. Klicken Sie auf **[!UICONTROL Authenticate]**.

1. Klicken Sie auf **[!UICONTROL Save]**.

## So authentifizieren Sie ein vorhandenes Manager-Konto erneut

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Wählen Sie **[!UICONTROL Reauthenticate existing manager account]** aus.

1. Wählen Sie das Manager-Konto aus.

1. Geben Sie die Anmeldeinformationen für das Manager-Konto ein.

   Die **[!UICONTROL Manager Account ID]** und **Anmelde-E-**) sind erforderlich. Search, Social und Commerce erfasst und speichert automatisch das Konto-Token, das für die Authentifizierung verwendet werden soll.

   Sie können optional eine **[!UICONTROL MCC Account Name]** zur Identifizierung in Search, Social und Commerce und die **[!UICONTROL Password]** einschließen. Geben Sie das Passwort ein, wenn Sie es verschlüsseln und speichern möchten, damit der Account Manager Token nach Bedarf aktualisieren kann.

1. Klicken Sie auf **[!UICONTROL Authenticate]**.

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Hochladen von Zielen in Werbenetzwerke aktivieren](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [Konversionsmetriken für Suche, Social Media und Commerce-Tracking hochladen nach [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [Benachrichtigungseinstellungen bearbeiten](/help/search-social-commerce/notifications/notification-edit.md)
