---
title: Verwalten von Anmeldeinformationen für Ad-Netzwerk-Manager-Konten
description: Erfahren Sie, wie Sie Anmeldedaten für Ihre [!DNL Google Ads] Manager-Konten bereitstellen.
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# Verwalten von Anmeldeinformationen für Ad-Netzwerk-Manager-Konten

*[!DNL Google Ads]nur Konten*

Geben Sie die Anmeldedaten für Ihre [!DNL Google Ads] Manager-Konten ein, in die Search, Social und Commerce kontoübergreifende Konversionen hochladen sollen. Verwenden Sie diese Funktion, wenn Sie a) [!DNL Adobe]-getrackte, kontenübergreifende Konversionsmetriken in ein [!DNL Google Ads] Manager-Konto hochladen oder b) Portfolioziele hochladen möchten, die kontoübergreifende Konversionen zur Hybridoptimierung in [!DNL Google Ads] enthalten.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

Sie können Anmeldeinformationen für neue Manager-Kontodatensätze hinzufügen oder ein vorhandenes Manager-Konto erneut authentifizieren.

Nachdem Sie Anmeldeinformationen für ein Manager-Konto hinzugefügt haben, wird in den Kontoeinstellungen die zugehörige Manager-Konto-ID als schreibgeschützt angezeigt. Darüber hinaus zeigt eine optionale Spalte &quot;[!UICONTROL Manager Account for Cross-Account Conversions]&quot; in der Ansicht &quot;[!UICONTROL Campaigns] > [!UICONTROL Accounts]&quot;die Manager-Konto-ID für jedes untergeordnete Konto an und zeigt einen Fehler an, wenn das Managerkonto nicht authentifiziert ist. [!UICONTROL Notification Center] enthält Benachrichtigungen, wenn die Anmeldeinformationen eines Managerkontos fehlen ([der [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) oder wenn ein Authentifizierungstoken für ein Managerkonto abläuft ([der [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## Hinzufügen von Anmeldeinformationen für ein neues Manager-Konto

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Wählen Sie **[!UICONTROL Create new manager account]** aus.

1. Geben Sie Anmeldedaten für das Manager-Konto ein.

   Die **[!UICONTROL Manager Account ID]** und **[!UICONTROL Login Email]** sind erforderlich. Search, Social und Commerce erfassen und speichern automatisch das Konto-Token, das zur Authentifizierung verwendet werden soll.

   Sie können optional ein &quot;**[!UICONTROL MCC Account Name]**&quot;zur Identifikation in Search, Social und Commerce und dem Konto &quot;**[!UICONTROL Password]**&quot;hinzufügen. Geben Sie das Kennwort ein, wenn Sie es verschlüsseln möchten, und speichern Sie es, damit der Kundenbetreuer Token nach Bedarf aktualisieren kann.

1. Klicken Sie auf **[!UICONTROL Authenticate]**.

1. Klicken Sie auf **[!UICONTROL Save]**.

## So authentifizieren Sie ein vorhandenes Managerkonto erneut

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Wählen Sie **[!UICONTROL Reauthenticate existing manager account]** aus.

1. Wählen Sie das Konto Manager aus.

1. Geben Sie Anmeldedaten für das Manager-Konto ein.

   Die **[!UICONTROL Manager Account ID]** und die **Anmelde-E-Mail** sind erforderlich. Search, Social und Commerce erfassen und speichern automatisch das Konto-Token, das zur Authentifizierung verwendet werden soll.

   Sie können optional ein &quot;**[!UICONTROL MCC Account Name]**&quot;zur Identifikation in Search, Social und Commerce und dem Konto &quot;**[!UICONTROL Password]**&quot;hinzufügen. Geben Sie das Kennwort ein, wenn Sie es verschlüsseln möchten, und speichern Sie es, damit der Kundenbetreuer Token nach Bedarf aktualisieren kann.

1. Klicken Sie auf **[!UICONTROL Authenticate]**.

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Aktivieren des Hochladens von Zielen in Anzeigennetzwerke](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [Laden Sie die von Search, Social und Commerce verfolgten Konversionsmetriken in [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md) hoch.
>* [Bearbeiten der Benachrichtigungseinstellungen](/help/search-social-commerce/notifications/notification-edit.md)
