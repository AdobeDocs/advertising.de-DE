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

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (nur Aktionen löschen) und [!DNL Yandex] Konten nur*

Sie können Kampagnendaten, die aus einem Feed generiert wurden, veröffentlichen, während Sie die Daten über die zugehörigen Vorlagen oder als separaten Prozess propagieren. Sobald Sie Daten posten, werden alle vorhandenen propagierten Daten aus den Listen [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads] entfernt.

Für eine erfolgreiche Veröffentlichung müssen alle Anzeigengruppen Kampagnen zugewiesen werden, alle Suchbegriffe und Anzeigen müssen Anzeigengruppen zugewiesen werden und alle erforderlichen Informationen müssen ohne Längenverletzungen enthalten sein.

* Wenn Sie die Option für &quot;[!UICONTROL Propagate and Preview]&quot; verwendet haben, posten Sie [die generierte Bulksheet-Datei](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (mit dem Namen &quot;`<feed file name>_<template name>`&quot;) aus der [!UICONTROL Bulksheets]-Ansicht.

  Wenn Sie Ihre Landingpages bisher nicht [ validiert haben, können Sie dies tun, bevor Sie die Datei veröffentlichen.](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md)

* Wenn Sie die Option für &quot;[!UICONTROL Propagate only]&quot; verwendet haben, können Sie die generierten Daten für Komponenten mit dem [[!UICONTROL New] Status](propagated-data-status.md) in einer Kampagnen-Hierarchieansicht auf der Registerkarte [!UICONTROL Templates] posten.

  >[!NOTE]
  >
  >Aktive oder gelöschte Komponenten können neue Unterkomponenten enthalten und die Unterkomponenten können veröffentlicht werden, wenn die Daten gültig sind.

  >[!TIP]
  >
  >Wenn Sie Ihre Landingpages zuvor nicht validiert haben und dies tun möchten, propagieren Sie [Daten und zeigen Sie sie in der [!UICONTROL Bulksheets] -Ansicht in der Vorschau an, anstatt sie in das Werbenetzwerk zu posten. ](feed-data-propagate.md) Anschließend können Sie [ die URLs validieren](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md), bevor Sie die Datei manuell in das Werbenetzwerk posten.

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, wodurch die Registerkarte [!UICONTROL Templates] geöffnet wird.

   1. Aktivieren Sie das Kontrollkästchen neben der Vorlage.

   1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Post]**.

   1. Geben Sie in den Beitragseinstellungen Informationen in die Felder ein oder wählen Sie sie aus und klicken Sie auf **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** Welche Kontokomponenten werden veröffentlicht.

      * **[!UICONTROL Scheduling]:** Wann die Datei gepostet werden soll:

         * *[!UICONTROL Post to search engine now]* (Standard): Erstellt eine Bulk-Sheet-Datei aus den propagierten Feed-Daten und beginnt sofort mit der Veröffentlichung.

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* Erstellt eine Bulksheet-Datei und veröffentlicht sie später. Geben Sie Folgendes an:

            * **[!UICONTROL Start Time]:** Ein zukünftiges Datum und eine zukünftige Uhrzeit, zu der die Bulksheet-Datei im Werbenetzwerk veröffentlicht werden soll. Standardmäßig wird die Datei am nächsten Tag um 00:00 Uhr (12:00 Uhr) gesendet. **Hinweis:** Bei großen Dateien, die länger verarbeitet werden müssen, stehen die veröffentlichten Daten nicht sofort in den Ansichten der Kampagnenverwaltung oder im Anzeigen-Manager des Netzwerks zur Verfügung.

            * **[!UICONTROL End Time]:** Ein zukünftiges Datum und eine zukünftige Uhrzeit, zu der die veröffentlichten Anzeigen basierend auf der [Feed-Dateneinstellung](feed-settings-manage.md#feed-data-settings) für &quot;[!UICONTROL When the Scheduled End Date is reached]&quot; angehalten oder gelöscht werden können. Standardmäßig beträgt die Endzeit 30 Tage vor dem heutigen Tag 00:00 Uhr (12:00 Uhr). Wählen Sie &quot;**[!UICONTROL None]**&quot;, um die Daten unbegrenzt aktiv zu halten (oder bis Sie neue Daten für die Vorlage propagieren), oder geben Sie ein Datum und eine Uhrzeit an.

              Um ein Datum anzugeben, verwenden Sie das Format TT/MM/JJJJ oder D/M/JJJJ oder klicken Sie auf ![Kalender](/help/search-social-commerce/assets/calendar.png "Kalender") , um den Kalender zu öffnen, und [wählen Sie ein Datum aus](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Um eine Zeit zu ändern, geben Sie die Zeit im 24-Stunden-Format HH/MM oder H/M ein oder wählen Sie eine Zeit (in Intervallen von 30 Minuten) aus der Liste aus.

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** Erstellt eine Bulk-Sheet-Datei, die in der Ansicht [!UICONTROL Search] > [!UICONTROL Bulksheets] verfügbar ist. Sie können die Datei optional von dort aus posten.

           Wenn die resultierende Bulksheet-Datei größer als 2 MB ist, weist die Datei das ZIP-Format auf. Sie müssen die Datei nicht entpacken, um sie zu posten.

      * **[!UICONTROL Generate Tracking URLs]:** Ob Tracking-URLs für Suchbegriffe und Anzeigenvarianten in die Bulksheet-Datei aufgenommen werden sollen: *[!UICONTROL Yes]* (Standard) oder *[!UICONTROL No]*.

        Wenn Sie &quot;*[!UICONTROL Yes]*&quot;auswählen, werden die URLs aus den Basis-URLs für die Suchbegriffe und Anzeigen gemäß den [!UICONTROL Tracking Methods] -Parametern in den [Kontoeinstellungen](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) oder, wenn Sie Daten vorhandenen Kampagnen zuordnen, den [!UICONTROL Tracking Methods] -Parametern in den vorhandenen [Kampagneneinstellungen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) generiert.

        Wenn Tracking-URLs für die relevanten Elemente vorhanden sind, werden sie nur dann neu generiert, wenn neue benötigt werden (z. B. wenn sich der Keyword-Übereinstimmungstyp, der kreative Text oder die Tracking-Parameter des Kontos geändert haben).

      * **[!UICONTROL Bulksheet Name]:** Der Name der Bulksheet-Datei, die aus den propagierten Feed-Daten erstellt werden soll. Standardmäßig erhält die Datei den Namen `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. Sie können die Datei nach Belieben umbenennen, sie muss jedoch mit einer der folgenden Dateierweiterungen enden: `.tsv` (für tabulatorgetrennte Werte), `.txt` (für ASCII-Text), `.csv` (für kommagetrennte Werte) oder `.zip` (für eine komprimierte TSV-Datei). Verwenden Sie für Daten, die internationale Zeichen enthalten, das Format TSV oder TXT.

        Die veröffentlichte Datei ist 30 Tage lang in der Ansicht [!UICONTROL Bulksheets] verfügbar, unabhängig davon, ob Sie sie im Werbenetzwerk posten oder nicht.

Die Spalte &quot;[!UICONTROL Last Prop. Status]&quot; zeigt den Auftragsstatus für die entsprechenden Vorlagen an.

Wenn das Bulksheet erstellt wird, wird es in der Ansicht &quot;[!UICONTROL Bulksheets]&quot;aufgeführt. Wenn die Datei gepostet wird, wird eine E-Mail-Benachrichtigung mit einem Link zur Datei gesendet. Wenn jedoch alle oder einige der Daten nicht veröffentlicht werden können, wird in der Ansicht &quot;[!UICONTROL Bulksheets]&quot;eine Fehlerdatei aufgelistet und eine E-Mail-Benachrichtigung mit einem Link zur Fehlerdatei gesendet.

>[!NOTE]
>
>* Unabhängig von der ausgewählten Planungsoption werden die angegebenen Daten aus den Listen [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] und [!UICONTROL Ads] entfernt.
>* Die Verarbeitung großer Datenmengen dauert länger. Sie können den Fortschritt der Datei während des Prozesses verfolgen.
>* Alle veröffentlichten Daten unterliegen dem redaktionellen Prozess des Netzwerks.
>* Bevor eine Bulksheet-Datei veröffentlicht wird, können Sie den Beitrag [abbrechen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [Über Inventar-Feeds](inventory-feeds-about.md)
>* [Aus Feeds generierte Daten anzeigen](propagated-data-view.md)
>* [Aus Feeds generierte Daten bearbeiten](propagated-data-edit.md)
>* [Beenden eines Veröffentlichungsauftrags für Inventar-Feed-Daten](stop-job.md)
>* [Status der aus Feeds generierten Daten](propagated-data-status.md)
