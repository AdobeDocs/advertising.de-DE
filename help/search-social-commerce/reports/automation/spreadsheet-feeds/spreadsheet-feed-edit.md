---
title: Bearbeiten der Feed-Einstellungen für Tabellenberichte
description: Erfahren Sie, wie Sie die Einstellungen für Tabellenfeeds bearbeiten.
exl-id: 8ca36006-4038-404b-aaf9-66dc3e9ddcf6
feature: Search Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# Bearbeiten der Feed-Einstellungen für Tabellenberichte

*Nur für grundlegende Berichte und Berichte zur Modellgenauigkeit*

Sie können ändern, welche Berichtsvorlage, [!DNL Microsoft Excel] Vorlage und andere Parameter für einen Tabellenfeed verwendet werden.

>[!NOTE]
>
> Wenn Sie die Spalten in der Berichtsvorlage bearbeiten oder eine neue oder aktualisierte Berichtsvorlage verwenden, müssen Sie die Vorlage [!DNL Excel] entsprechend aktualisieren und erneut hochladen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Spreadsheet Feeds]**.

1. (Optional) Um die Berichtsvorlage oder die für den Tabellenfeed verwendete [!DNL Excel] Vorlage zu aktualisieren:

   * (Optional) Um eine andere oder aktualisierte Berichtsvorlage für den Feed zu verwenden, erstellen Sie [eine neue [!DNL Excel] Vorlage für die Berichtsvorlage](spreadsheet-feed-create-excel-template.md).

     Sie müssen im nächsten Schritt sowohl die Berichtsvorlage als auch die neue [!DNL Excel] -Datei hochladen.

   * (Optional) Um der Vorlage [!DNL Excel] einfach benutzerdefinierte Spalten hinzuzufügen, fügen Sie die Spalten rechts von den Spalten aus der Berichtsvorlage ein und speichern Sie die Datei dann als [!DNL Excel]-Tabelle im XLSX-Format. Sie müssen die neue [!DNL Excel]-Datei im nächsten Schritt hochladen.

1. Ändern Sie die Einstellungen des Tabellenfeeds:

   * Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

   * Klicken Sie neben dem Namen des Tabellenfeeds auf die Schaltfläche ![Einstellungen anzeigen/bearbeiten](/help/search-social-commerce/assets/settings.png "Schaltfläche &quot;Einstellungen anzeigen/bearbeiten&quot;").

   * Ändern Sie im Dialogfeld [!UICONTROL Edit Spreadsheet Feed] die Einstellungen für den [Tabellenfeed ](spreadsheet-feed-settings.md).

   * Klicken Sie auf **[!UICONTROL Submit]**.

   * (Optional) Sobald die [!UICONTROL Update Status] des Feeds den Wert *[!UICONTROL Finished]* hat, klicken Sie neben dem Feed auf **[!UICONTROL XLSX]** und öffnen oder speichern Sie dann die Datei gemäß der üblichen Vorgehensweise Ihres Browsers.

     >[!NOTE]
     >
     > Wenn die mit dem Feed verknüpfte Berichtsvorlage später gelöscht wird, wird der Feed ebenfalls gelöscht.

     Tabellen-Feeds werden automatisch um 08:00 Uhr in der Zeitzone des Werbetreibenden aktualisiert. Wenn die Berichtsvorlage Adressen für E-Mail-Empfänger enthält, erhalten diese Adressen Benachrichtigungen, wenn die Tabelle aktualisiert wird.

>[!MORELIKETHIS]
>
>* [Über Tabellenbericht-Feeds](spreadsheet-feed-about.md)
>* [Erstellen eines Tabellenbericht-Feeds](spreadsheet-feed-create.md)
>* [Erstellen einer [!DNL Excel] Vorlage für einen Tabellenbericht-Feed](spreadsheet-feed-create-excel-template.md)
>* [Bearbeiten Sie die Einstellungen des Tabellenbericht-Feeds](spreadsheet-feed-edit.md)
>* [Einstellungen für den Spreadsheet-Bericht](spreadsheet-feed-settings.md)
>* [Anzeigen oder Speichern einer Tabellenbericht-Feed-Datei](spreadsheet-feed-view-or-save.md)
>* [Manuelles Aktualisieren von Tabellenbericht-Feeds](spreadsheet-feed-refresh.md)
