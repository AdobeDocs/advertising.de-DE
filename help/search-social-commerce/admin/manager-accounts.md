---
title: Verwalten von Anmeldeinformationen für Ad-Netzwerk-Manager-Konten
description: Erfahren Sie, wie Sie Anmeldedaten für Ihre [!DNL Google Ads] Manager-Konten.
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
source-git-commit: 4cf04fc7ea22e50b5f56cd278ad9a1aac724edf7
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---

# Verwalten von Anmeldeinformationen für Ad-Netzwerk-Manager-Konten

*[!DNL Google Ads]Nur Konten*

Geben Sie die Anmeldeinformationen für Ihre [!DNL Google Ads] Manager-Konten, in die Sie kontoübergreifende Konversionen von Search, Social und Commerce hochladen möchten. Verwenden Sie diese Funktion, wenn Sie einen) Upload durchführen möchten. [!DNL Adobe]-verfolgte, kontenübergreifende Konversionsmetriken in eine [!DNL Google Ads] Manager-Konto oder b) Hochladen von Portfoliozielen, die kontoübergreifende Konversionen in [!DNL Google Ads] zur Hybridoptimierung.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

Sie können Anmeldeinformationen für neue Manager-Kontodatensätze hinzufügen oder ein vorhandenes Manager-Konto erneut authentifizieren.

Nachdem Sie Anmeldeinformationen für ein Manager-Konto hinzugefügt haben, wird in den Kontoeinstellungen die zugehörige Manager-Konto-ID als schreibgeschützt angezeigt. Darüber hinaus ist ein optionales[!UICONTROL Manager Account for Cross-Account Conversions]&quot; in der Spalte [!UICONTROL Campaigns] > [!UICONTROL Accounts] -Ansicht zeigt die Manager-Konto-ID für jedes untergeordnete Konto an und zeigt einen Fehler an, wenn das Managerkonto nicht authentifiziert ist. [!UICONTROL Notification Center] enthält Benachrichtigungen, wenn die Anmeldeinformationen eines Managerkontos fehlen ([die [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) oder wenn ein Authentifizierungstoken für ein Manager-Konto abläuft ([die [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## Hinzufügen von Anmeldeinformationen für ein neues Manager-Konto

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Auswählen **[!UICONTROL Create new manager account]**.

1. Geben Sie Anmeldedaten für das Manager-Konto ein.

   Die **[!UICONTROL Manager Account ID]** und **[!UICONTROL Login Email]** sind erforderlich. Search, Social und Commerce erfassen und speichern automatisch das Konto-Token, das zur Authentifizierung verwendet werden soll.

   Sie können optional eine **[!UICONTROL MCC Account Name]** zur Identifizierung in Search, Social &amp; Commerce und dem Konto **[!UICONTROL Password]**. Geben Sie das Kennwort ein, wenn Sie es verschlüsseln möchten, und speichern Sie es, damit der Kundenbetreuer Token nach Bedarf aktualisieren kann.

1. Klicks **[!UICONTROL Authenticate]**.

1. Klicks **[!UICONTROL Save]**.

## So authentifizieren Sie ein vorhandenes Managerkonto erneut

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Auswählen **[!UICONTROL Reauthenticate existing manager account]**.

1. Wählen Sie das Konto Manager aus.

1. Geben Sie Anmeldedaten für das Manager-Konto ein.

   Die **[!UICONTROL Manager Account ID]** und **Anmelde-E-Mail** sind erforderlich. Search, Social und Commerce erfassen und speichern automatisch das Konto-Token, das zur Authentifizierung verwendet werden soll.

   Sie können optional eine **[!UICONTROL MCC Account Name]** zur Identifizierung in Search, Social &amp; Commerce und dem Konto **[!UICONTROL Password]**. Geben Sie das Kennwort ein, wenn Sie es verschlüsseln möchten, und speichern Sie es, damit der Kundenbetreuer Token nach Bedarf aktualisieren kann.

1. Klicks **[!UICONTROL Authenticate]**.

1. Klicks **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Aktivieren des Hochladens von Zielen in Werbenetzwerke](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [Hochladen von Konversionsmetriken in [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [Benachrichtigungseinstellungen bearbeiten](/help/search-social-commerce/notifications/notification-edit.md)
