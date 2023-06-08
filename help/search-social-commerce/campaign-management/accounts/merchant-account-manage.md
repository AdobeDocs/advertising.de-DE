---
title: Handelskonten verwalten
description: Erfahren Sie, wie Sie Kontodetails für ein Merchant Center-Konto einrichten und verwalten.
source-git-commit: a24b51405bef1e73ed57b1cb9d012bdfbda9cdec
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Handelskonten verwalten

*Nur für Adobe Account Manager,  Account Manager und Administrator-Benutzerrollen*

Search, Social und Commerce können täglich Produktdaten für die Google Merchant Center- oder Microsoft Merchant Center-Konten eines Advertisers herunterladen und anzeigen. Darüber hinaus können Search, Social und Commerce die Anzeigenerstellung anhand des Inhalts des Händlerkontos automatisieren. Um direkt mit Produktdaten in Search, Social und Commerce zu arbeiten, müssen Sie einen entsprechenden Kontodatensatz erstellen, der die Kontozugriffsberechtigungen und den Zugriff enthält *enabled*.

>[!NOTE]
>
>Sie können einen Handelskontodatensatz nicht entfernen. Sie können den Zugriff auf ein Konto deaktivieren, indem Sie den Kontotyp in *disabled*.

## Details zum Handelskonto erstellen {#create-merchant-account}

*Nur für Adobe Account Manager,  Account Manager und Administrator-Benutzerrollen*

Um Produktdaten anzuzeigen und Tracking-Vorlagen für ein Händlerkonto zu generieren und anhand der Daten Anzeigen zu erstellen, müssen Sie einen entsprechenden Kontodatensatz mit den Kontozugriffsdaten und dem Zugriff auf das Konto erstellen *enabled*.

>[!NOTE]
>
>Um ein Konto im Händlernetz zu erstellen, rufen Sie die Website des Netzwerks auf.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]**, der sich für [!UICONTROL Accounts] Registerkarte.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Create Account]**.

1. Geben Sie die [Kontoeinstellungen für Händler](#merchant-account-settings):

   1. Im [!UICONTROL Product Source] wählen Sie die Handelsmitte aus.

   1. (Erforderlich für [!DNL Google Ads] Konten; optional für [!DNL Microsoft Advertising] Konten) Suche, Social &amp; Commerce erlauben, auf das Konto zuzugreifen, das die [[!DNL OAuth] Autorisierungsprotokoll](https://oauth.net/2/):

      1. ([!DNL Microsoft Advertising] Nur Konten) Wählen Sie **[!UICONTROL oAuth]**.

      1. Klicken **[!UICONTROL Enable Connection]**.

      1. (Wenn Sie nicht im Konto des Werbetreibenden angemeldet sind) Melden Sie sich beim Konto des Werbetreibenden an. Die Best Practice ist, die Anmeldeinformationen für den API-Zugriff auf den Commerce-Center-Konto zu verwenden.

      1. Klicken Sie im Bildschirm &quot;Zugriffsanfrage/Berechtigung&quot;auf die Schaltfläche , um die Berechtigung zu bestätigen.

      1. Kopieren Sie die Authentifizierungszeichenfolge im sich öffnenden Popup-Fenster und fügen Sie die Zeichenfolge in das **[!UICONTROL oAuth Token]** -Feld.

      1. Geben Sie die anderen Kontoeinstellungen an.

1. Klicken **[!UICONTROL Save]**.

   Attributdaten für alle Produkte in dem Konto sind nach dem nächsten täglichen Synchronisierungsprozess in Search, Social und Commerce verfügbar (etwa 06:00 Uhr in der lokalen Zeitzone des Benutzers). Anschließend können Sie die Produktdaten verwenden, um die Anzeigenerstellung mithilfe von Inventar-Feeds zu automatisieren.

## Details zum Handelskonto bearbeiten {#edit-merchant-account}

*Nur für Adobe Account Manager,  Account Manager und Administrator-Benutzerrollen*

Wenn sich die Kontoanmeldeinformationen ändern oder Sie das Abrufen und Verwenden von Daten für ein Handelskonto einstellen möchten, bearbeiten Sie die Kontodetails.

>[!NOTE]
>
>Um ein tatsächliches Konto im Handelsnetzwerk zu bearbeiten, rufen Sie die Website des Netzwerks auf.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]**, der sich für [!UICONTROL Accounts] Registerkarte.

1. Klicken Sie neben dem Kontonamen auf ![Einstellungen anzeigen/bearbeiten](/help/search-social-commerce/assets/settings.png "Einstellungen anzeigen/bearbeiten").

1. Bearbeiten Sie die [Kontoeinstellungen für Händler](#merchant-account-settings).

1. Klicken **[!UICONTROL Save]**.

>[!NOTE]
>
>Search, Social und Commerce müssen die neuen Kontodaten mit denen im Händlernetzwerk synchronisieren. Dies geschieht automatisch einmal täglich um etwa 6:00 Uhr in der lokalen Zeitzone des Benutzers.

## Zugriff auf ein Händlerkonto deaktivieren {#disable-merchant-account}

*Nur für Adobe Account Manager,  Account Manager und Administrator-Benutzerrollen*

Wenn Sie ein Händlerkonto deaktivieren, melden sich Search, Social und Commerce nicht bei dem Konto an und rufen daher keine aktualisierten Produktdaten ab. Während der Aktivierung des Kontos erfasste Daten werden weiterhin gespeichert und vorhandene Anzeigen, die mithilfe von Produktdaten erstellt wurden, werden nicht gemäß der Feed-Vorlage und den Feed-Dateneinstellungen aktualisiert, angehalten oder gelöscht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** , der sich für [!UICONTROL Accounts] Registerkarte.

1. Klicken Sie neben dem Kontonamen auf ![Einstellungen anzeigen/bearbeiten](/help/search-social-commerce/assets/settings.png "Einstellungen anzeigen/bearbeiten").

1. Ändern Sie die [!UICONTROL EF Account Type] nach **[!UICONTROL Disabled]**.

1. Klicken **[!UICONTROL Save]**.

## Einstellungen für Merchant-Konten {#merchant-account-settings}

>[!NOTE]
>
>Nur Agenturkontoverwalter, [!DNL Adobe] -Kontomanager und Administrator-Benutzerrollen können die Einstellungen für das Händlerkonto konfigurieren.

**[!UICONTROL Product Source]:** Das Händlernetzwerk. Sie können den Wert für ein vorhandenes Konto nicht ändern.

**[!UICONTROL OAuth Token]:** ([!DNL Google Merchant Center] Nur Konten) Das Token des Kontos ermöglicht die Autorisierung von Anmeldungen mithilfe der [[!DNL OAuth] Autorisierungsprotokoll](https://oauth.net/2/).

**[!UICONTROL Auth Type]:** ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] nur) Gibt an, ob Anmeldungen für das Konto mit folgenden Optionen autorisiert werden sollen:

* *[!UICONTROL Client login]:* Um die Anmeldung des Kunden zu verwenden.

* *[!UICONTROL oAuth]* (Standardeinstellung): So verwenden Sie die [[!DNL OAuth] Autorisierungsprotokoll](https://oauth.net/2/).

**[!UICONTROL Access Key]:** ([!DNL Microsoft Merchant Center] nur) Der Zugriffsschlüssel für das zu verwendende Entwicklerkonto.

**[!UICONTROL Account Name]:** Der Name, der für das Konto in Search, Social und Commerce angezeigt wird.

**[!UICONTROL Login]:** Der Anmeldename oder die ID für das Konto.

**[!UICONTROL Password]:** Das Kennwort für das Konto.

**[!UICONTROL Confirm Password]:** Das Kennwort für das Konto.

**[!UICONTROL EF Account Type]:** Ob Search, Social und Commerce auf das Konto zugreifen:

* *[!UICONTROL Enabled]* (Standardeinstellung): Search, Social und Commerce können sich beim Konto anmelden, um Produktdaten abzurufen.

* *[!UICONTROL Disabled]:* Search, Social und Commerce melden sich nicht beim Konto an und rufen daher keine aktualisierten Produktdaten ab. Während der Aktivierung des Kontos erfasste Daten werden weiterhin gespeichert und vorhandene Anzeigen, die mithilfe von Produktdaten erstellt wurden, werden nicht gemäß der Feed-Vorlage und den Feed-Dateneinstellungen aktualisiert, angehalten oder gelöscht.

**[!UICONTROL Account ID]:** Die Konto-ID des Händlers. Wenn Sie nur ein Konto mit den angegebenen Anmeldeinformationen haben, ist dieser Wert optional.

**[!UICONTROL Time Zone]:** Die Zeitzone des Werbetreibenden. Verwenden Sie dieselbe Zeitzone, die für die Kontoinformationen des Advertisers für Suchen, Social und Commerce konfiguriert ist (die bei der Erstellung des Kontos festgelegt wird). Sie können den Wert für ein vorhandenes Konto nicht ändern.

>[!MORELIKETHIS]
>
>* [Über Werbenetzkonten](ad-network-account-about.md)
>* [Verwalten von Anzeigen-Netzwerkkonten](ad-network-account-manage.md)
