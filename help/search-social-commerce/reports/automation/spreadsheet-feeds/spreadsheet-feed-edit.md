---
title: Bearbeiten von Tabellenbericht-Feed-Einstellungen
description: Erfahren Sie, wie Sie die Einstellungen für Tabellen-Feeds bearbeiten.
exl-id: 8ca36006-4038-404b-aaf9-66dc3e9ddcf6
feature: Search Reports
TQID: https://experienceleague.adobe.com/xsq7qkYTc5p7Q4Q-LKHeCX7-W8DRW80ET6ylOWocYG0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 317
ht-degree: 0%

---

# Bearbeiten von Tabellenbericht-Feed-Einstellungen

*Nur für Basisberichte und Berichte zur Modellgenauigkeit*

Sie können ändern, welche Berichtsvorlage, [!DNL Microsoft Excel] Vorlage und andere Parameter für einen Tabellenfeed verwendet werden.

>[!NOTE]
>
> Wenn Sie die Spalten in der Berichtsvorlage bearbeiten oder eine neue oder aktualisierte Berichtsvorlage verwenden, müssen Sie die [!DNL Excel] entsprechend aktualisieren und erneut hochladen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Spreadsheet Feeds]**.

1. (Optional) So aktualisieren Sie die Berichtsvorlage oder die [!DNL Excel], die für den Tabellen-Feed verwendet wird:

   * (Optional) Um eine andere oder aktualisierte Berichtsvorlage für den Feed zu verwenden, [erstellen Sie eine neue  [!DNL Excel]  für die Berichtsvorlage](spreadsheet-feed-create-excel-template.md).

     Sie müssen im nächsten Schritt sowohl die Berichtsvorlage als auch die neue [!DNL Excel] hochladen.

   * (Optional) Um der [!DNL Excel]-Vorlage einfach benutzerdefinierte Spalten hinzuzufügen, fügen Sie die Spalten rechts neben den Spalten aus der Berichtsvorlage ein und speichern Sie dann die Datei als [!DNL Excel] Kalkulationstabelle im .XLSX-Format. Sie müssen im nächsten Schritt die neue [!DNL Excel]-Datei hochladen.

1. Ändern der Einstellungen für den Tabellenvorschub:

   * Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

   * Klicken Sie neben dem Namen des Tabellenvorschubs auf die Schaltfläche ![Einstellungen anzeigen/bearbeiten](/help/search-social-commerce/assets/settings.png "Einstellungen anzeigen/bearbeiten").

   * Ändern Sie im Dialogfeld [!UICONTROL Edit Spreadsheet Feed] die [Tabellenvorschub](spreadsheet-feed-settings.md).

   * Klicken Sie auf **[!UICONTROL Submit]**.

   * (Optional) Klicken Sie nach der [!UICONTROL Update Status] des Feed-*[!UICONTROL Finished]* auf **[!UICONTROL XLSX]** neben dem Feed und öffnen oder speichern Sie die Datei dann entsprechend dem normalen Verfahren Ihres Browsers.

     >[!NOTE]
     >
     > Wenn die mit dem Feed verknüpfte Berichtsvorlage später gelöscht wird, wird der Feed ebenfalls gelöscht.

     Tabellen-Feeds werden täglich um 08 :00 in der Zeitzone des Werbetreibenden automatisch aktualisiert. Wenn die Berichtsvorlage Adressen für E-Mail-Empfänger enthält, erhalten diese Adressen beim Aktualisieren der Tabelle Benachrichtigungen.

>[!MORELIKETHIS]
>
>* [Über Tabellenbericht-Feeds](spreadsheet-feed-about.md)
>* [Erstellen eines Tabellenbericht-Feeds](spreadsheet-feed-create.md)
>* [Erstellen einer  [!DNL Excel]  für einen Tabellenbericht-Feed](spreadsheet-feed-create-excel-template.md)
>* [Bearbeiten von Tabellenbericht-Feed-Einstellungen](spreadsheet-feed-edit.md)
>* [Einstellungen für Tabellenbericht-Feeds](spreadsheet-feed-settings.md)
>* [Anzeigen oder Speichern einer Tabellenbericht-Feed-Datei](spreadsheet-feed-view-or-save.md)
>* [Tabellenbericht-Feeds manuell aktualisieren](spreadsheet-feed-refresh.md)
