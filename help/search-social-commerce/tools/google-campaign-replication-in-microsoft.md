---
title: Replikation [!DNL Google Ads] Kampagnen in [!DNL Microsoft® Advertising]
description: Erfahren Sie, wie Sie Ihre synchronisierten Kampagnen in eine [!DNL Google Ads] direkt in einer synchronisierten [!DNL Microsoft® Advertising] -Konto.
exl-id: e7714d3d-4a8e-44ef-a3a7-e5198c091660
feature: Search Tools
source-git-commit: 877333330df84ff5c8bd7ee1bfc837de492877fb
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 0%

---

# Replikation [!DNL Google Ads] Kampagnen in [!DNL Microsoft® Advertising]

Sie können Ihre synchronisierten Kampagnen in eine [!DNL Google Ads] direkt in einer synchronisierten [!DNL Microsoft® Advertising] als erweiterte CPC (eCPC)-Kampagnen. Die vorhandenen Angebote und Kampagnenbudgets werden skaliert. Vorhandenes Tracking von Suchen, Social und Commerce wird nicht importiert.

Sie können die folgenden Kampagnentypen und deren Kampagnenstruktur replizieren:

* [!DNL Google Ads] Kampagnen suchen und anzeigen in [!DNL Microsoft® Advertising] Kampagnen durchsuchen und anzeigen.

* [!DNL Google Display Network] Kampagnen, einschließlich Anzeigenbilder, in [!DNL Microsoft® Advertising] Zielgruppenkampagnen im Microsoft® Zielgruppen-Netzwerk.

  Wenn Sie Shopping-Feed-basierte Display-Kampagnen replizieren möchten, replizieren Sie zunächst Ihre [!DNL Google Merchant Center] Produktangebote an [!DNL Microsoft® Merchant Center]. Wählen Sie bei der Replikation der Kampagnen die [!DNL Microsoft® Merchant Center] in den Importoptionen speichern, um den Speicher mit Ihren Feed-basierten Zielgruppenkampagnen zu verknüpfen.

* [!DNL Google Ads] Leistungsmax-Kampagnen, einschließlich lokaler Inventaranzeigen in [!DNL Microsoft® Advertising] Kampagnen mit maximaler Leistung.

Sie können die Kampagnen einmalig, wöchentlich oder monatlich oder je nach [!DNL Microsoft® Advertising]wird empfohlen. Sie können optional Benachrichtigungen bei jeder Ausführung eines Importvorgangs oder bei Fehlern oder Änderungen konfigurieren. Importieren Sie Ihre Kampagnen in [!DNL Microsoft® Advertising]können Sie den Status Ihres Importvorgangs überprüfen, alle Fehlerprotokolle überprüfen, einen Importauftrag manuell ausführen und Ihren Importplan bearbeiten, anhalten, aktivieren oder löschen.

Nicht alle Kampagneninformationen werden repliziert, und Sie müssen möglicherweise einige Informationen zu Ihrem [!DNL Microsoft® Advertising] Kampagnen. Weitere Informationen dazu, welche Daten importiert werden, finden Sie unter [!DNL Microsoft® Advertising] Hilfe zu &quot;[Was importiert wird von [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851).&quot; Da das Tracking von Suche, Social und Commerce nicht importiert wird, sollten Sie auch das Tracking innerhalb der [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [Kampagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [Anzeigengruppe](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)oder [Anzeige](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) -Einstellungen.

## Replikation [!DNL Google Ads] Kampagnen

>[!NOTE]
>
>Wenn Sie Shopping-Feed-basierte Display-Kampagnen replizieren möchten, müssen Sie zuerst [replizieren Sie Ihre [!DNL Google Merchant Center] Produktangebote in [!DNL Microsoft® Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). Wählen Sie bei der Replikation der Kampagnen die [!DNL Microsoft® Merchant Center] in den Importoptionen speichern, um den Speicher mit Ihren Feed-basierten Zielgruppenkampagnen zu verknüpfen.

Siehe [Was wird importiert von [!DNL Google Ads] Kampagnen](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Klicken Sie im Hauptmenü &quot;Suchen&quot;, &quot;Social&quot;und &quot;Commerce&quot;auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Klicken **[!UICONTROL +Import]**.

1. Geben Sie die [Importeinstellungen](#campaign-import-settings):

   1. Im **[!UICONTROL Select accounts]** Abschnitt:

      1. Wählen Sie die Quell- und Zielkonten aus.

      1. Klicken **[!UICONTROL Get Credential Id from MSA]**.

      1. Bei Ziel anmelden [!DNL Microsoft Advertising] -Konto, kopieren Sie die angezeigte Berechtigungs-ID und fügen Sie den Wert in die **[!UICONTROL Credential ID]** -Feld.

   1. Im **[!UICONTROL Select campaigns & ad groups]** die zu importierenden Kampagnen und Anzeigengruppen.

   1. Im **[!UICONTROL Customize your import]** angeben, geben Sie die zu importierenden Elementtypen an.

   1. Im **[!UICONTROL Set schedule]** angeben, wann der Importauftrag ausgeführt werden soll.

1. Klicken **[!UICONTROL Post]**.

1. (Optional) Fügen Sie das Tracking für Suche, Social und Commerce innerhalb der [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [Kampagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [Anzeigengruppe](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)oder [Anzeige](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) -Einstellungen.

## Planeinstellungen für einen Kampagnenimportauftrag bearbeiten

Siehe [Was wird importiert von [!DNL Google Ads] Kampagnen](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben dem Importauftrag und klicken Sie auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

1. Im **[!UICONTROL Set schedule]** -Abschnitt, geben Sie die [Zeitplaneinstellungen](#campaign-import-settings).

1. Klicken **[!UICONTROL Post]**.

## Anzeigen von Kampagnenimportaufträgen

Sie können alle Importvorgänge einschließlich der Quelle auflisten [!DNL Google Ads] Konto, Zielgruppe [!DNL Microsoft® Advertising] -Konto, die Importzeit oder den Zeitplan sowie den Benutzer, der den Auftrag erstellt hat. Wenn Sie einen Importauftrag mehrmals ausführen, auch während regelmäßig geplanter Importe, wird jedes Vorkommen als separater Auftrag aufgeführt.

* Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

     Standardmäßig öffnet sich die Ansicht im [!UICONTROL List of Import Jobs] Registerkarte.

   * Aus dem [[!UICONTROL Import Logs] tab](#campaign-import-log), klicken Sie auf die **[!UICONTROL List of Import Jobs]** Registerkarte.

## Kampagnenimportauftrag ausführen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben dem Importauftrag.

1. Klicks ![Jetzt ausführen](/help/search-social-commerce/assets/run.png "Jetzt ausführen").

## Anzeigen von Protokollen für Kampagnenimportaufträge {#campaign-import-log}

Sie können alle abgeschlossenen oder fehlgeschlagenen Importvorgänge auflisten, einschließlich der Startzeit, der Quelle [!DNL Google Ads] Konto, Zielgruppe [!DNL Microsoft® Advertising] -Konto, der Benutzer, der den Auftrag erstellt hat, die Anzahl erfolgreicher und fehlgeschlagener Vorgänge sowie alle E-Mail-Adressen, an die Benachrichtigungen zu den einzelnen Aufträgen gesendet wurden. Sie können weitere Details zu den Änderungen am Ziel anzeigen [!DNL Microsoft® Advertising] -Konto, das für jeden Auftrag aufgetreten ist, einschließlich der Anzahl der hinzugefügten, synchronisierten, gelöschten Elemente und der Fehler für jede Entitätsebene (z. B. Kampagne oder Keyword) im Konto.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Klicken Sie auf **[!UICONTROL Import Logs]** Registerkarte.

1. (Optional) Um Details zu einem Importauftrag anzuzeigen, klicken Sie auf den Wert im [!UICONTROL Summary] Spalte.

## Einstellungen für den Campaign-Import-Auftrag {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** Die synchronisierten [!DNL Google Ads] Konto, aus dem die Kampagnendaten exportiert werden.

**[!UICONTROL Credential ID]:** Eine ID, die [!DNL Microsoft® Advertising] verwendet, um Ihre [!DNL Google Ads] Anmeldedaten.

Automatische Generierung von [!DNL Microsoft® Advertising] Die Anmeldeinformationen für den Import sind aufgrund von [!DNL Microsoft® Advertising] Einschränkungen. Wenden Sie sich an Ihr Adobe Account-Team, das die Anmeldeinformationen generiert und Ihnen die Kennung gibt.

**[!UICONTROL Target Microsoft® Ads account]:** Die synchronisierten [!DNL Microsoft® Advertising] Konto, in das die Kampagnendaten importiert werden.

### [!UICONTROL Select campaigns & ad groups]

**\[Zu importierende Daten\]:** Geben Sie die zu importierenden Daten an:

* *[!UICONTROL Import all new and existing campaigns]:* So importieren Sie Daten für alle bereits vorhandenen Kampagnen und Kampagnen, die in nicht vorhanden sind [!DNL Microsoft® Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* So wählen Sie bestimmte Kampagnen und Anzeigengruppen aus.

   * Um eine Kampagne in ihre untergeordneten Anzeigengruppen zu erweitern, klicken Sie auf **[!UICONTROL >]** nach dem Kampagnennamen.

   * Um eine Kampagne oder Anzeigengruppe auszuwählen, wählen Sie das Element aus, damit ein Häkchen angezeigt wird.

   * So entfernen Sie eine Kampagne oder Anzeigengruppe:

      * Im [!UICONTROL Campaigns] oder [!UICONTROL Adgroups] deaktivieren Sie die Auswahl der Kampagne oder Anzeigengruppe, damit das Häkchen verschwindet.

      * Im [!UICONTROL Selected] Spalte, klicken ![Löschen](/help/search-social-commerce/assets/delete.png "Löschen").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Ermöglicht die Angabe des Importvorgangs, der Angebote und Budgets sowie anderer Optionen.

**[!UICONTROL What to import]:** Definiert die zu importierenden Elemente. Optionen zum Importieren von Elementkategorien sind standardmäßig ausgewählt, wobei alle Elementtypen ausgewählt sind. Um nur bestimmte Elementtypen einzuschließen, klicken Sie auf **[!UICONTROL Show advanced options]** und ändern Sie die einzuschließenden Elementtypen.

**[!UICONTROL Bids and budgets]:** Definiert, welche Gebots- und Budgeteinstellungen importiert, aktualisiert und angepasst werden sollen.

**[!UICONTROL Other options]:** Definiert, wie importierte Landingpage-URLs, Tracking-Vorlagen und andere Kampagnen-, Anzeigen- und Targeting-Optionen verarbeitet werden.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** Der Name des Importvorgangs.

**[!UICONTROL When]:** Wann werden die angegebenen Kampagnen importiert? *Auto* (zu lassen [!DNL Microsoft® Advertising] Festlegung eines Zeitplans zur bestmöglichen Optimierung Ihrer Kampagnen), *[!UICONTROL Now]* (zum Ausführen des Auftrags beim Posten der Auftragseinstellungen), *[!UICONTROL Once]* zu einem bestimmten Zeitpunkt, *[!UICONTROL Daily]* zu einem bestimmten Zeitpunkt, *[!UICONTROL Weekly]* zu einem bestimmten Zeitpunkt oder *[!UICONTROL Monthly]* zu einem bestimmten Zeitpunkt.

**[!UICONTROL Receive email notifications]:** Wenn und wann E-Mail-Benachrichtigungen über Importvorgänge an die E-Mail-Adressen im Feld Berichte senden an gesendet werden sollen.

**[!UICONTROL Send reports to]:** E-Mail-Adressen , um Benachrichtigungen zu Importvorgängen zu erhalten. Trennen Sie mehrere Adressen durch Kommas (`,`).
