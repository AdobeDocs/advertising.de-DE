---
title: (Neue Benutzeroberfläche) Berichtsvorlagen verwalten
description: Erfahren Sie, wie Sie wiederverwendbare Berichtsvorlagen für terminierte und On-Demand-Berichte erstellen, anzeigen, bearbeiten und löschen.
feature: Search Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
source-git-commit: eb12699872b7c89240f5340cd3b0a251c9c08366
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%
---
# (Neue Benutzeroberfläche) Berichtsvorlagen verwalten

Berichtsvorlagen sind vordefinierte Berichtslayouts, die Sie bei der Erstellung der meisten Berichte wiederverwenden können. Die Verwendung von Vorlagen spart Ihnen Zeit, wenn Sie nicht standardmäßige Parameter verwenden, Varianten desselben Berichts ausführen oder denselben Bericht nach einem regulären Zeitplan ausführen möchten. Gespeicherte Vorlagen sind auf der Registerkarte **[!UICONTROL Templates]** unter **[!UICONTROL Reports]>[!UICONTROL Reports]** verfügbar.

Sie können bis zu 100 Vorlagen gleichzeitig verwalten.

Zum Anzeigen der Daten ist die Berechtigung [!UICONTROL View Scheduled Reports] erforderlich. Zum Erstellen, Duplizieren, Bearbeiten, Ausführen und Löschen von Vorlagen sowie zum Kopieren von Zeilendaten ist die Berechtigung [!UICONTROL Edit Scheduled Reports] erforderlich. Sie können nur von Ihnen erstellte Vorlagen bearbeiten.

## Verfügbare Aktionen

* [Erstellen einer Berichtsvorlage](#template-create) als neue Vorlage oder basierend auf einer vorhandenen Vorlage.

* [Anzeigen der Einstellungen einer Berichtsvorlage ohne Änderung des Originals](#template-view).

* [Bearbeiten einer Berichtsvorlage](#template-edit) einschließlich ihres Zeitplans.

* [Bei Bedarf Berichte für angegebene Vorlagen ](#template-run).

* [Löschen von Berichtsvorlagen](#template-delete).

* [Kopieren Sie alle Daten in ausgewählten Zeilen in die Zwischenablage](#copy-to-clipboard).

## Erstellen einer Berichtsvorlage {#template-create}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Führen Sie einen der folgenden Schritte aus:

   * Um eine neue Vorlage zu erstellen, klicken Sie auf **[!UICONTROL Create Template]**. Wählen Sie im Bedienfeld **[!UICONTROL Create a New Template]** die Berichtskategorie und den Berichtstyp aus und klicken Sie dann auf **[!UICONTROL Proceed]**.

   * Um eine Vorlage basierend auf einer vorhandenen Vorlage zu erstellen, halten Sie den Cursor über der Vorlagenzeile und klicken Sie entweder ![Vorlageneinstellungen](/help/search-social-commerce/assets/settings-new.png "Vorlageneinstellungen") **[!UICONTROL Template Settings]** oder **[!UICONTROL ...]>[!UICONTROL Duplicate]**.

1. Geben Sie einen eindeutigen **[!UICONTROL Report Name]** für die Vorlage ein und stellen Sie sicher, dass **[!UICONTROL Save as Template]** aktiviert ist.

   Die Einstellung ist standardmäßig aktiviert, wenn Sie mit **[!UICONTROL Create Template]** beginnen. Wenn Sie sie deaktivieren, ändert sich die endgültige Aktion in **[!UICONTROL Run Report]**, wodurch ein Bericht generiert wird, anstatt eine Vorlage zu speichern.

1. Konfigurieren Sie die Berichteinstellungen für [einfache und erweiterte Berichte](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md), [unterstützende Berichte](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md), [Modellgenauigkeitsberichte](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md) oder [Spezialberichte](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md).

   Klicken Sie auf **[!UICONTROL Next]** , um zwischen den Einstellungsabschnitten zu wechseln.

1. (Optional) Um Berichte automatisch zu generieren, konfigurieren Sie die **[!UICONTROL Frequency]**- und Versandeinstellungen in **[!UICONTROL Scheduling]**.

1. Klicken Sie auf **[!UICONTROL Create]**.

Sie können eine Vorlage auch speichern, während Sie [Bericht auf der Registerkarte Letzte Berichte erstellen](/help/search-social-commerce/new-ui/reports/management/report-manage.md) indem Sie **[!UICONTROL Save as Template]** vor dem Senden der Berichteinstellungen aktivieren.

## Einstellungen einer Berichtsvorlage anzeigen {#template-view}

Um Einstellungen zu überprüfen, ohne die ursprüngliche Vorlage zu ändern, öffnen Sie ein Duplikat. Dies erfordert die Berechtigung [!UICONTROL Edit Scheduled Reports] . Das Öffnen des Duplikats speichert keine neue Vorlage.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Halten Sie den Cursor über der Vorlagenzeile und klicken Sie auf ![Vorlageneinstellungen](/help/search-social-commerce/assets/settings-new.png "Vorlageneinstellungen") **[!UICONTROL Template Settings]**.

1. Überprüfen Sie die Berichteinstellungen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Cancel]** . Wenn Sie dazu aufgefordert werden, die Einrichtung zu verwerfen, klicken Sie auf **[!UICONTROL Discard]**.

Um stattdessen eine Kopie zu speichern, folgen Sie dem [Verfahren zur Vorlagenerstellung](#template-create).

## Bearbeiten einer Berichtsvorlage {#template-edit}

Sie können die Einstellungen und den Zeitplan jeder Vorlage ändern, die Sie erstellt haben. Die Änderungen gelten für Berichte, die in Zukunft aus der Vorlage generiert werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Aktivieren Sie das Kontrollkästchen neben einer von Ihnen erstellten Vorlage.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]**.

   [!UICONTROL Edit] ist nicht verfügbar, wenn mehrere Vorlagen ausgewählt sind oder die ausgewählte Vorlage von einem anderen Benutzer erstellt wurde.

1. Ändern Sie die Berichteinstellungen. Um einen Zeitplan hinzuzufügen, zu ändern oder zu entfernen, bearbeiten Sie **[!UICONTROL Frequency]** in **[!UICONTROL Scheduling]**.

   Wählen Sie eine tägliche, wöchentliche oder monatliche Häufigkeit für geplante Berichte aus. Um einen wiederkehrenden Zeitplan zu entfernen, klicken Sie auf **[!UICONTROL Now]**.

   **[!UICONTROL Save as Template]** und **[!UICONTROL Type]** sind beim Bearbeiten einer vorhandenen Vorlage schreibgeschützt. Sie müssen [!UICONTROL Save as Template] nicht erneut aktivieren.

1. Klicken Sie auf **[!UICONTROL Save]**.

## On-Demand-Berichte für angegebene Vorlagen ausführen {#template-run}

Sie können jederzeit Berichte für eine oder mehrere Vorlagen ausführen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Führen Sie einen der folgenden Schritte aus:

   * (So führen Sie eine einzelne Vorlage aus):

     1. Öffnen Sie das Menü der Vorlagenzeile und wählen Sie **[!UICONTROL Run]** aus.

     1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

   * (So führen Sie eine oder mehrere Vorlagen aus):

     1. Aktivieren Sie das Kontrollkästchen neben jeder Vorlage, die Sie ausführen möchten.

     1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Run]**.

     1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

Sie können eine Vorlage auch beim Bearbeiten ausführen, indem Sie auf **[!UICONTROL Run Report]** und dann auf **[!UICONTROL Confirm]** klicken. Speichern Sie zuerst alle Änderungen. Mit dieser Aktion wird die gespeicherte Vorlage ausgeführt.

## Löschen von Berichtsvorlagen {#template-delete}

Sie können jede Berichtsvorlage löschen, die Ihnen zur Verfügung steht. Wenn Sie eine Vorlage löschen, die einen Zeitplan enthält, wird dieser Bericht in Zukunft nicht mehr generiert.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Reports]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Führen Sie einen der folgenden Schritte aus:

   * (So löschen Sie eine einzelne Vorlage):

     1. Öffnen Sie das Menü der Vorlagenzeile und wählen Sie **[!UICONTROL Delete]** aus.

     1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

   * (So löschen Sie eine oder mehrere Vorlagen):

     1. Aktivieren Sie das Kontrollkästchen neben jeder Vorlage, die Sie löschen möchten.

     1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Delete]**.

     1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

## Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren {#copy-to-clipboard}

Kopieren Sie die sichtbaren Informationen in die ausgewählten Zeilen entsprechend den angewendeten Filtern und Spalten, die in der Ansicht sichtbar sind. Die Informationen werden als tabulatorgetrennte Werte (TSV) gespeichert.

1. Aktivieren Sie das Kontrollkästchen neben jeder Zeile, deren Daten Sie kopieren möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Copy]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.
