---
title: Händlerkonten verwalten
description: Erfahren Sie, wie Sie Kontodetails für ein Merchant Center-Konto einrichten und verwalten.
exl-id: 7d940e45-ea49-470b-98d0-0196593228cb
feature: Search Campaign Management
source-git-commit: cb65108fcc60c11b901e3b43c292ad5a94192b9f
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# Händlerkonten verwalten

*Nur Agenturkonto-Manager, Adobe-Konto-Manager und Admin-Benutzerrollen*

Search, Social und Commerce können Produktdaten jeden Tag für jedes Google Merchant Center- oder Microsoft Merchant Center-Konto eines Werbetreibenden herunterladen und anzeigen. Darüber hinaus können Search, Social und Commerce die Anzeigenerstellung basierend auf dem Inhalt des Händlerkontos automatisieren. Um direkt mit Produktdaten in Search, Social und Commerce zu arbeiten, müssen Sie einen entsprechenden Kontodatensatz erstellen, der die Anmeldeinformationen für den Kontozugriff enthält und mit *aktiviert*.

>[!NOTE]
>
>Ein Eintrag für ein Händlerkonto kann nicht entfernt werden. Sie können den Zugriff auf ein Konto deaktivieren, indem Sie den Kontotyp in &quot;*&quot;*.

## Details zum Händlerkonto erstellen {#create-merchant-account}

*Nur Agenturkonto-Manager, Adobe-Konto-Manager und Admin-Benutzerrollen*

Um Produktdaten anzuzeigen und Tracking-Vorlagen für ein Händlerkonto zu generieren sowie Anzeigen basierend auf den Daten zu erstellen, müssen Sie einen entsprechenden Kontodatensatz erstellen, der die Anmeldeinformationen für den Kontozugriff enthält und Zugriff auf das Konto *aktiviert*.

>[!NOTE]
>
>Um ein tatsächliches Konto im Händlernetzwerk zu erstellen, gehen Sie auf die Website des Netzwerks.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]**, um zur Registerkarte [!UICONTROL Accounts] zu gelangen.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Create Account]**.

1. Geben Sie die [Einstellungen für Händlerkonto](#merchant-account-settings) an:

   1. Wählen Sie im Menü [!UICONTROL Product Source] das Händlerzentrum aus.

   <!--

   1. ([!DNL Meta Ads] accounts only) Log in to the [!DNL Meta Ads] account.

   And are there additional steps just for Meta? If so, create a separate procedure for it.
   
   -->

   1. (Erforderlich für [!DNL Google Ads] Konten; optional für [!DNL Microsoft Advertising] Konten) Zulassen, dass Search, Social und Commerce mithilfe des [[!DNL OAuth] Autorisierungsprotokolls](https://oauth.net/2/) auf das Konto zugreifen:

      1. (Nur [!DNL Microsoft Advertising] Konten) **[!UICONTROL oAuth]** auswählen.

      1. Klicken Sie auf **[!UICONTROL Enable Connection]**.

      1. (Wenn Sie nicht beim Konto des Werbetreibenden angemeldet sind) Melden Sie sich beim Konto des Werbetreibenden an. Es empfiehlt sich, die Anmeldeinformationen für den Zugriff der Inhalts-API auf das Merchant Center-Konto zu verwenden.

      1. Klicken Sie im Bildschirm „Anfrage zum Zugriff/zur Berechtigung“ auf die Schaltfläche, um die Berechtigung zu bestätigen.

      1. Kopieren Sie die Authentifizierungszeichenfolge in das sich öffnende Popup-Fenster und fügen Sie die Zeichenfolge in das Feld **[!UICONTROL oAuth Token]** ein.

      1. Geben Sie die anderen Kontoeinstellungen an.

1. Klicken Sie auf **[!UICONTROL Save]**.

   Attributdaten für alle Produkte im Konto sind in Search, Social und Commerce nach dem nächsten täglichen Synchronisierungsprozess verfügbar (ca. 06:00 Uhr in der lokalen Zeitzone der Benutzerin oder des Benutzers). Anschließend können Sie die Produktdaten verwenden, um die Anzeigenerstellung mithilfe von Inventar-Feeds zu automatisieren.

## Details zum Händlerkonto bearbeiten {#edit-merchant-account}

*Nur Agenturkonto-Manager, Adobe-Konto-Manager und Admin-Benutzerrollen*

Wenn sich die Kontoanmeldeinformationen ändern oder Sie das Abrufen und Verwenden von Daten für ein Händlerkonto stoppen möchten, bearbeiten Sie die Kontodetails.

>[!NOTE]
>
>Um ein tatsächliches Konto im Händlernetzwerk zu bearbeiten, gehen Sie auf die Website des Netzwerks.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]**, um zur Registerkarte [!UICONTROL Accounts] zu gelangen.

1. Klicken Sie neben dem Kontonamen auf ![Einstellungen anzeigen/bearbeiten/](/help/search-social-commerce/assets/settings.png " anzeigen/bearbeiten").

1. Bearbeiten Sie die [Einstellungen des Händlerkontos](#merchant-account-settings).

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!NOTE]
>
>Search, Social und Commerce müssen die neuen Kontodaten mit denen im Händlernetzwerk synchronisieren. Dies geschieht automatisch einmal täglich um ca. 06:00 Uhr in der lokalen Zeitzone des Benutzers.

## Zugriff auf ein Händlerkonto deaktivieren {#disable-merchant-account}

*Nur Agenturkonto-Manager, Adobe-Konto-Manager und Admin-Benutzerrollen*

Wenn Sie ein Händlerkonto deaktivieren, meldet sich Search, Social und Commerce nicht beim Konto an und ruft daher keine aktualisierten Produktdaten ab. Daten, die während der Aktivierung des Kontos erfasst wurden, werden weiterhin gespeichert und vorhandene Anzeigen, die mit Produktdaten erstellt wurden, werden nicht gemäß den Einstellungen für Feed-Vorlagen und Feed-Daten aktualisiert, angehalten oder gelöscht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** , wodurch die Registerkarte [!UICONTROL Accounts] geöffnet wird.

1. Klicken Sie neben dem Kontonamen auf ![Einstellungen anzeigen/bearbeiten/](/help/search-social-commerce/assets/settings.png " anzeigen/bearbeiten").

1. Ändern Sie die [!UICONTROL EF Account Type] in **[!UICONTROL Disabled]**.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Einstellungen des Händlerkontos {#merchant-account-settings}

>[!NOTE]
>
>Nur die Benutzerrollen „Agenturkonto-Manager“, &quot;[!DNL Adobe]-Account-Manager“ und „Administrator“ können Einstellungen für Händlerkonten konfigurieren.

**[!UICONTROL Product Source]:** Das Händlernetzwerk. Sie können den Wert für ein vorhandenes Konto nicht ändern.

**[!UICONTROL OAuth Token]:** (nur [!DNL Google Merchant Center] Konten) Das Token des Kontos zum Autorisieren von Anmeldungen mit dem [[!DNL OAuth] Autorisierungsprotokoll](https://oauth.net/2/).

**[!UICONTROL Auth Type]:** (nur [!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center]) Ob die Anmeldung bei dem Konto autorisiert werden soll mit:

* *[!UICONTROL Client login]:* Um die Anmeldung des Clients zu verwenden.

* *[!UICONTROL oAuth]* (Standard): Zum Verwenden des [[!DNL OAuth] Autorisierungsprotokolls](https://oauth.net/2/).

**[!UICONTROL Access Key]:** (nur [!DNL Microsoft Merchant Center]) Der Zugriffsschlüssel für das zu verwendende Entwicklerkonto.

**[!UICONTROL Account Name]:** Der Name, der für das Konto in Search, Social und Commerce angezeigt wird.

**[!UICONTROL Login]:** Der Anmeldename oder die ID für das Konto.

**[!UICONTROL Password]:** Das Kennwort für das Konto.

**[!UICONTROL Confirm Password]:** Das Kennwort für das Konto.

**[!UICONTROL EF Account Type]:** Gibt an, ob Search, Social und Commerce auf das Konto zugreifen:

* *[!UICONTROL Enabled]* (Standard): Search, Social und Commerce können sich beim Konto anmelden, um Produktdaten abzurufen.

* *[!UICONTROL Disabled]:* Search, Social und Commerce melden sich nicht beim Konto an und rufen daher keine aktualisierten Produktdaten ab. Daten, die während der Aktivierung des Kontos erfasst wurden, werden weiterhin gespeichert und vorhandene Anzeigen, die mit Produktdaten erstellt wurden, werden nicht gemäß den Einstellungen für Feed-Vorlagen und Feed-Daten aktualisiert, angehalten oder gelöscht.

**[!UICONTROL Account ID]:** Die ID des Händlerkontos. Wenn Sie nur ein Konto mit den angegebenen Anmeldeinformationen haben, ist dieser Wert optional.

**[!UICONTROL Time Zone]:** Die Zeitzone des Werbetreibenden. Verwenden Sie dieselbe Zeitzone, die für die Kontoinformationen für Search, Social und Commerce des Advertisers konfiguriert wurde (die beim Erstellen des Kontos festgelegt wird). Sie können den Wert für ein vorhandenes Konto nicht ändern.

>[!MORELIKETHIS]
>
>* [Über Werbenetzwerkkonten](ad-network-account-about.md)
>* [Verwalten von Anzeigennetzwerkkonten](ad-network-account-manage.md)
