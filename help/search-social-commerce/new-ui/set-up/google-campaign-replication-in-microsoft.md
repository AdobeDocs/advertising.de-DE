---
title: (Neue Benutzeroberfläche) Replizieren von Google Ads-Kampagnen in Microsoft Advertising
description: Erfahren Sie, wie Sie synchronisierte Kampagnen in einem Google Ads-Konto direkt in ein synchronisiertes Microsoft Advertising-Konto exportieren.
feature: Search Campaign Management
exl-id: d4f8e452-7b3d-4a1f-9c3e-6b8d2e5a4917
source-git-commit: 3f769f18ce006278b12a62f8d837d60affffda65
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Replizieren [!DNL Google Ads] Kampagnen in [!DNL Microsoft Advertising]

*Beta-Funktion*

Sie können synchronisierte Kampagnen in einem [!DNL Google Ads]-Konto direkt in ein synchronisiertes [!DNL Microsoft Advertising]-Konto als erweiterte CPC(eCPC)-Kampagnen exportieren. Die vorhandenen Angebote und Kampagnenbudgets werden skaliert. Vorhandenes Tracking für Suche, Social Media und Commerce wird nicht importiert.

Sie können die folgenden Kampagnentypen und ihre Kampagnenstruktur replizieren:

* [!DNL Google Ads] und Anzeigen von Kampagnen in [!DNL Microsoft Advertising] Kampagnen zum Suchen und Anzeigen.

* [!DNL Google Display Network] von Kampagnen, einschließlich Anzeigenbildern, in [!DNL Microsoft Advertising] Zielgruppenkampagnen im Microsoft Audience Network.

  Wenn Sie Shopping-Feed-basierte Display-Kampagnen replizieren möchten, replizieren Sie zunächst Ihre [!DNL Google Merchant Center] Produktangebote nach [!DNL Microsoft Merchant Center]. Wenn Sie die Kampagnen replizieren, wählen Sie in den Importoptionen den [!DNL Microsoft Merchant Center] Store aus, um den Store mit Ihren Feed-basierten Zielgruppenkampagnen zu verknüpfen.

* [!DNL Google Ads] von -Kampagnen mit dem Typ „Performance Max“, einschließlich lokaler Inventaranzeigen, in Kampagnen mit dem Typ „Performance Max“ [!DNL Microsoft Advertising].

Sie können die Kampagnen einmal, täglich, wöchentlich oder monatlich oder gemäß dem von [!DNL Microsoft Advertising] empfohlenen Zeitplan aktualisieren. Optional können Sie Benachrichtigungen bei jeder Ausführung eines Importvorgangs oder bei Fehlern oder Änderungen konfigurieren. Nachdem Sie Ihre Kampagnen in [!DNL Microsoft Advertising] importiert haben, können Sie den Status Ihres Importvorgangs überprüfen, alle Fehlerprotokolle ansehen, einen Importvorgang manuell ausführen und Ihren Importplan bearbeiten, anhalten, aktivieren oder löschen.

Nicht alle Kampagneninformationen werden repliziert, und Sie müssen möglicherweise einige Informationen zu Ihren [!DNL Microsoft Advertising] Kampagnen hinzufügen. Weitere Informationen dazu, welche Daten importiert werden, finden Sie [!DNL Microsoft Advertising] Hilfe unter &quot;[Was wird importiert? [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851){target="_blank"}. Da das Tracking nach Suche, Social und Commerce nicht importiert wird, sollten Sie auch Tracking in den Einstellungen [Konto](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [Kampagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [Anzeigengruppe](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) oder [Anzeige](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) hinzufügen.

## [!DNL Google Ads] Kampagnen replizieren

>[!NOTE]
>
>Wenn Sie Shopping-Feed-basierte Display-Kampagnen replizieren möchten, replizieren Sie zunächst [Ihre  [!DNL Google Merchant Center] -Angebote in [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870){target="_blank"}. Wenn Sie die Kampagnen replizieren, wählen Sie in den Importoptionen den [!DNL Microsoft Merchant Center] Store aus, um den Store mit Ihren Feed-basierten Zielgruppenkampagnen zu verknüpfen.

Siehe [Was wird aus - [!DNL Google Ads]  importiert](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500){target="_blank"}.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

1. Klicken Sie auf **[!UICONTROL Import Campaigns]**.

1. Geben Sie die [Importeinstellungen](#campaign-import-settings) an:

   1. Im **[!UICONTROL Select accounts]** Schritt:

      1. Geben Sie im Feld **[!UICONTROL Import Name]** einen Namen für den Importvorgang ein.

      1. Wählen Sie das Quell-[!DNL Google Ads] und das Ziel-[!DNL Microsoft Advertising] aus.

      1. Geben Sie Ihre **[!UICONTROL Credential ID]** ein. Wenden Sie sich an Ihr Adobe-Konto-Team, wenn Sie keine Berechtigungs-ID haben. Die automatische Generierung ist aufgrund von [!DNL Microsoft Advertising] nicht verfügbar.

      1. Klicken Sie auf **[!UICONTROL Next]**.

   1. Geben Sie im **[!UICONTROL Select campaigns & ad groups]** Schritt die zu importierenden Kampagnen und Anzeigengruppen an und klicken Sie auf **[!UICONTROL Next]**.

   1. Geben Sie im **[!UICONTROL Customize your import]** Schritt optional die Elementtypen, Angebots- und Budgeteinstellungen sowie andere zu importierende Optionen an und klicken Sie dann auf **[!UICONTROL Next]**.

   1. Geben Sie im **[!UICONTROL Set schedule]** Schritt an, wann der Importvorgang ausgeführt und wie Benachrichtigungen empfangen werden sollen.

1. Überprüfen Sie Ihre Auswahl in der Zusammenfassung und klicken Sie auf **[!UICONTROL Start Import]**.

1. (Optional) Fügen Sie Such-, Social- und Commerce-Tracking innerhalb der Einstellungen [Konto](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [Kampagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [Anzeigengruppe](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) oder [Anzeige](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) hinzu.

## Zeitplaneinstellungen für einen Kampagnen-Importauftrag bearbeiten

Siehe [Was wird aus - [!DNL Google Ads]  importiert](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500){target="_blank"}.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Jobs]** .

1. Klicken Sie auf den Namen des Importvorgangs, und klicken Sie dann auf **[!UICONTROL Edit]**.

1. Geben Sie im **[!UICONTROL Set schedule]** Schritt die [Zeitplaneinstellungen“ &#x200B;](#campaign-import-settings).

1. Klicken Sie auf **[!UICONTROL Save]**.

## Anzeigen von Campaign-Importvorgängen

Sie können alle Importaufträge auflisten, einschließlich des [!DNL Google Ads], des Zielgruppen-[!DNL Microsoft Advertising], der Importzeit oder des Importplans und des Benutzers, der den Auftrag erstellt hat. Wenn Sie einen Importvorgang mehrmals ausführen, auch während regelmäßig geplanter Importe, wird jedes Vorkommen als separater Vorgang aufgelistet.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

   Die Ansicht wird standardmäßig mit der Registerkarte **[!UICONTROL Jobs]** geöffnet.

## Ausführen eines Kampagnen-Importvorgangs

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Jobs]** .

1. Aktivieren Sie das Kontrollkästchen neben dem Importvorgang und klicken Sie dann auf **[!UICONTROL Run Now]**.

## Anzeigen von Protokollen für Campaign-Importvorgänge {#campaign-import-log}

Sie können alle abgeschlossenen oder fehlgeschlagenen Importvorgänge auflisten, einschließlich der Startzeit, des [!DNL Google Ads], des Zielgruppen-[!DNL Microsoft Advertising], des Benutzers, der den Auftrag erstellt hat, der Anzahl erfolgreicher und fehlgeschlagener Vorgänge und aller E-Mail-Adressen, die Benachrichtigungen für jeden Auftrag erhalten haben. Sie können weitere Details zu den Änderungen am [!DNL Microsoft Advertising]-Zielkonto anzeigen, die für jeden Auftrag aufgetreten sind, einschließlich der Anzahl der hinzugefügten, synchronisierten, gelöschten Elemente, die Fehler für jede Entitätsebene (z. B. Kampagne oder Keyword) im Konto verursacht haben.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Logs]** .

1. (Optional) Um Details zu einem Importvorgang anzuzeigen, klicken Sie auf den Wert in der Spalte [!UICONTROL Summary] .

## Einstellungen für Kampagnenimportaufträge {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Import Name]:** Ein Name zur Identifizierung des Importvorgangs.

**[!UICONTROL Source Google Ads account]:** Das synchronisierte [!DNL Google Ads], aus dem Kampagnendaten exportiert werden.

**[!UICONTROL Target Microsoft Ads account]:** Das synchronisierte [!DNL Microsoft Advertising], in das Kampagnendaten importiert werden.

**[!UICONTROL Credential ID]:** Eine ID, mit der [!DNL Microsoft Advertising] Ihre [!DNL Google Ads]-Anmeldeinformationen darstellt. Die automatische Generierung von [!DNL Microsoft Advertising]-Anmeldeinformationen für den Import ist aufgrund von [!DNL Microsoft Advertising] nicht verfügbar. Wenden Sie sich an Ihr Adobe-Account-Team. Es generiert die Anmeldeinformationen und gibt Ihnen die ID.

### [!UICONTROL Select campaigns & ad groups]

**\[Zu importierende Daten\]:** Zu importierende Daten:

* *[!UICONTROL Import all new and existing campaigns]:* Importieren von Daten für alle Kampagnen, die bereits vorhanden sind, und Kampagnen, die nicht in [!DNL Microsoft Advertising] vorhanden sind.

* *[!UICONTROL Import specific campaigns and adgroups]:* Um bestimmte Kampagnen und Anzeigengruppen auszuwählen.

   * Um eine Kampagne in ihre untergeordneten Anzeigengruppen zu erweitern, klicken Sie auf **[!UICONTROL >]** nach dem Kampagnennamen.

   * Um eine Kampagne oder eine Anzeigengruppe auszuwählen, wählen Sie das Element aus, sodass ein Häkchen angezeigt wird.

   * Um eine Kampagne oder eine Anzeigengruppe zu entfernen, heben Sie die Auswahl des Elements auf oder klicken Sie auf das Löschsymbol in der Spalte [!UICONTROL Selected] .

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Ermöglicht die Angabe von Importoptionen, Angeboten und Budgets sowie anderen Optionen.

**[!UICONTROL What to import]:** Definiert die zu importierenden Elemente. Optionen zum Importieren von Elementkategorien sind standardmäßig aktiviert, wobei alle Elementtypen ausgewählt sind. Um nur bestimmte Elementtypen einzubeziehen, klicken Sie auf **[!UICONTROL Show advanced options]** und ändern Sie die Elementtypen so, dass sie enthalten sind. Sie können optional auch eine UET-Tag-ID mit einer beliebigen Remarketing-Liste oder Zielgruppe verknüpfen, die noch nicht in [!DNL Microsoft Advertising] importiert wurde.

**[!UICONTROL Bids and budgets]:** Definiert, welche Gebot- und Budgeteinstellungen importiert, aktualisiert und angepasst werden sollen, einschließlich Optionen zum Erhöhen oder Verringern von Geboten und Budgets um einen bestimmten Prozentsatz für [!DNL Microsoft Advertising].

**[!UICONTROL Other options]:** Definiert, wie importierte Landingpage-URLs, Tracking-Vorlagen und andere Kampagnen-, Anzeigen- und Targeting-Optionen verarbeitet werden, einschließlich der Optionen zum Suchen und Ersetzen von Text und zum Einfügen von Suffixen.

### [!UICONTROL Set schedule]

**[!UICONTROL When]:** Wann die angegebenen Kampagnen importiert werden sollen: *Auto* (damit [!DNL Microsoft Advertising] einen Zeitplan festlegen können, um Ihre Kampagnen am besten zu optimieren), *[!UICONTROL Now]* (um den Auftrag auszuführen, wenn Sie die Auftragseinstellungen veröffentlichen), *[!UICONTROL Once]* zu einem bestimmten Zeitpunkt, *[!UICONTROL Daily]* zu einem bestimmten Zeitpunkt, *[!UICONTROL Weekly]* zu einem bestimmten Zeitpunkt oder *[!UICONTROL Monthly]* zu einem bestimmten Zeitpunkt.

**[!UICONTROL Receive email notifications]:** Ob und wann E-Mail-Benachrichtigungen über Importaufträge an die Adressen im [!UICONTROL Send reports to] Feld gesendet werden sollen: *[!UICONTROL No emails]*, *[!UICONTROL Only if there are changes or errors]* (Standard), *[!UICONTROL Only if there are errors]* oder *[!UICONTROL Every time this import runs]*.

**[!UICONTROL Send reports to]:** E-Mail-Adressen, um Benachrichtigungen über Importvorgänge zu erhalten. Trennen Sie mehrere Adressen durch Kommas (`,`).

>[!MORELIKETHIS]
>
>* [Verwalten von Anzeigennetzwerkkonten](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)
