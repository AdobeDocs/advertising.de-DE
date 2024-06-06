---
title: Veröffentlichen von aus Feeds generierten Kampagnendaten in Werbenetzwerke
description: Erfahren Sie, wie Sie Daten veröffentlichen, die aus Bestandsdaten-Feeds in Werbenetzwerke generiert wurden.
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: 2cf15dbab3dc00ec88a41e4f7d8b5b3646b843e8
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Veröffentlichen von aus Feeds generierten Kampagnendaten in Werbenetzwerke

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (Nur Aktionen löschen) und [!DNL Yandex] Nur Konten*

Sie können Kampagnendaten, die aus einem Feed generiert wurden, veröffentlichen, während Sie die Daten über die zugehörigen Vorlagen oder als separaten Prozess propagieren. Sobald Sie Daten posten, werden alle vorhandenen propagierten Daten aus der [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] Listen.

Für eine erfolgreiche Veröffentlichung müssen alle Anzeigengruppen Kampagnen zugewiesen werden, alle Suchbegriffe und Anzeigen müssen Anzeigengruppen zugewiesen werden und alle erforderlichen Informationen müssen ohne Längenverletzungen enthalten sein.

* Wenn Sie die Option für &quot;[!UICONTROL Propagate and Preview],&quot; then [die generierte Bulksheet-Datei posten](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (mit dem Namen &quot;`<feed file name>_<template name>`&quot;) aus dem [!UICONTROL Bulksheets] anzeigen.

  Wenn Sie zuvor [Landingpages validieren](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md), können Sie dies tun, bevor Sie die Datei posten.

* Wenn Sie die Option für &quot;[!UICONTROL Propagate only],&quot;können Sie die generierten Daten für Komponenten mit der [[!UICONTROL New] status](propagated-data-status.md) innerhalb einer Kampagnenhierarchie aus der [!UICONTROL Templates] Registerkarte.

  >[!NOTE]
  >
  >Aktive oder gelöschte Komponenten können neue Unterkomponenten enthalten und die Unterkomponenten können veröffentlicht werden, wenn die Daten gültig sind.

  >[!TIP]
  >
  >Wenn Sie Ihre Landingpages zuvor nicht validiert haben und dies tun möchten, dann [Daten propagieren und sie in der Vorschau anzeigen](feed-data-propagate.md) aus dem [!UICONTROL Bulksheets] anzeigen, anstatt sie in das Werbenetzwerk zu posten. Sie können dann [Validieren der URLs](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) bevor Sie die Datei manuell in das Werbenetzwerk posten.

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, der sich für [!UICONTROL Templates] Registerkarte.

   1. Aktivieren Sie das Kontrollkästchen neben der Vorlage.

   1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Post]**.

   1. Geben Sie in den Beitragseinstellungen Informationen in die Felder ein oder wählen Sie sie aus und klicken Sie auf **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** Welche Kontokomponenten werden veröffentlicht?

      * **[!UICONTROL Scheduling]:** Wann sollte die Datei veröffentlicht werden?

         * *[!UICONTROL Post to search engine now]* (Standard): Erstellt eine Bulk-Sheet-Datei aus den propagierten Feed-Daten und beginnt sofort mit der Veröffentlichung.

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* Erstellt eine Bulksheet-Datei und veröffentlicht sie später. Geben Sie Folgendes an:

            * **[!UICONTROL Start Time]:** Ein zukünftiges Datum und eine Uhrzeit, zu der die Bulksheet-Datei im Werbenetzwerk veröffentlicht werden soll. Standardmäßig wird die Datei am nächsten Tag um 00:00 Uhr (12:00 Uhr) gesendet. **Hinweis:** Bei großen Dateien, die eine längere Verarbeitung erfordern, stehen die veröffentlichten Daten nicht sofort in den Kampagnenverwaltungsansichten oder im Anzeigen-Manager des Netzwerks zur Verfügung.

            * **[!UICONTROL End Time]:** Ein zukünftiges Datum und eine Uhrzeit, zu der die veröffentlichten Anzeigen basierend auf der Variablen [Feeddateneinstellung](feed-settings-manage.md#feed-data-settings) für &quot;[!UICONTROL When the Scheduled End Date is reached].&quot; Standardmäßig beträgt die Endzeit 30 Tage vor dem heutigen Tag 00:00 Uhr (12:00 Uhr). Auswählen **[!UICONTROL None]** um die Daten unbegrenzt aktiv zu halten (oder bis Sie neue Daten für die Vorlage propagieren) oder ein Datum und eine Uhrzeit anzugeben.

              Um ein Datum anzugeben, verwenden Sie das Format TT/MM/JJJJ oder D/M/JJJJ oder klicken Sie auf ![Kalender](/help/search-social-commerce/assets/calendar.png "Kalender") , um den Kalender zu öffnen, und [Datum auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Um eine Zeit zu ändern, geben Sie die Zeit im 24-Stunden-Format HH/MM oder H/M ein oder wählen Sie eine Zeit (in Intervallen von 30 Minuten) aus der Liste aus.

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** Erstellt eine Bulk-Sheet-Datei, die über das [!UICONTROL Search] > [!UICONTROL Bulksheets] anzeigen. Sie können die Datei optional von dort aus posten.

           Wenn die resultierende Bulksheet-Datei größer als 2 MB ist, weist die Datei das ZIP-Format auf. Sie müssen die Datei nicht entpacken, um sie zu posten.

      * **[!UICONTROL Generate Tracking URLs]:** Ob Tracking-URLs für Suchbegriffe und Anzeigenvarianten in die Bulksheet-Datei aufgenommen werden sollen: *[!UICONTROL Yes]* (Standardeinstellung) oder *[!UICONTROL No]*.

        Wenn Sie *[!UICONTROL Yes]* und dann werden die URLs aus den Basis-URLs für die Suchbegriffe und Anzeigen entsprechend der Variablen [!UICONTROL Tracking Methods] Parameter in [Kontoeinstellungen](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) oder, wenn Sie Daten vorhandenen Kampagnen zuordnen, dem [!UICONTROL Tracking Methods] Parameter in den vorhandenen [Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

        Wenn Tracking-URLs für die relevanten Elemente vorhanden sind, werden sie nur dann neu generiert, wenn neue benötigt werden (z. B. wenn sich der Keyword-Übereinstimmungstyp, der kreative Text oder die Tracking-Parameter des Kontos geändert haben).

      * **[!UICONTROL Bulksheet Name]:** Der Name der Bulksheet-Datei, die aus den propagierten Feed-Daten erstellt werden soll. Standardmäßig erhält die Datei den Namen `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. Sie können die Datei beliebig umbenennen, sie muss jedoch mit einer der folgenden Dateierweiterungen enden: `.tsv` (für tabulatorgetrennte Werte), `.txt` (für ASCII-Text), `.csv` (bei kommagetrennten Werten) oder `.zip` (für eine komprimierte TSV-Datei). Verwenden Sie für Daten, die internationale Zeichen enthalten, das Format TSV oder TXT.

        Die veröffentlichte Datei ist im [!UICONTROL Bulksheets] 30 Tage lang anzeigen, unabhängig davon, ob Sie sie im Werbenetzwerk posten oder nicht.

Die &quot;[!UICONTROL Last Prop. Status]&quot; zeigt den Auftragsstatus für die entsprechenden Vorlagen an.

Wenn das Bulksheet erstellt wird, wird es im [!UICONTROL Bulksheets] anzeigen. Wenn die Datei gepostet wird, wird eine E-Mail-Benachrichtigung mit einem Link zur Datei gesendet. Wenn jedoch alle oder einige der Daten nicht veröffentlicht werden können, wird eine Fehlerdatei im [!UICONTROL Bulksheets] angezeigt und eine E-Mail-Benachrichtigung mit einem Link zur Fehlerdatei gesendet.

>[!NOTE]
>
>* Unabhängig von der ausgewählten Planungsoption werden die angegebenen Daten aus dem [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], und [!UICONTROL Ads] Listen.
>* Die Verarbeitung großer Datenmengen dauert länger. Sie können den Fortschritt der Datei während des Prozesses verfolgen.
>* Alle veröffentlichten Daten unterliegen dem redaktionellen Prozess des Netzwerks.
>* Bevor eine Bulksheet-Datei veröffentlicht wird, können Sie [Abbrechen der Veröffentlichung](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](inventory-feeds-about.md)
>* [Aus Feeds generierte Daten anzeigen](propagated-data-view.md)
>* [Aus Feeds generierte Daten bearbeiten](propagated-data-edit.md)
>* [Beenden eines Veröffentlichungsauftrags für Inventar-Feed-Daten](stop-job.md)
>* [Status der aus Feeds generierten Daten](propagated-data-status.md)
