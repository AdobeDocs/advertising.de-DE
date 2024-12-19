---
title: Verwalten [!DNL Google Ads] dynamischer Suchziele
description: Erfahren Sie, wie Sie dynamische  [!DNL Google Ads]  erstellen und verwalten.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Verwalten [!DNL Google Ads] dynamischen Suchziele

Nur *[!DNL Google Ads]Konten*

Sie können den Status dynamischer Suchziele für Kampagnen, die das Suchnetzwerk verwenden, erstellen, bearbeiten und ändern.

>[!NOTE]
>
>Sie können große Mengen an Zieldaten gleichzeitig erstellen und bearbeiten, indem Sie [Bulksheet-Dateien](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) hochladen und im Anzeigennetzwerk posten.

## Erstellen eines [!DNL Google Ads] dynamischen Suchziels

Sie können dynamische Suchziele erstellen, um Seiten in Ihren Websites zu definieren (d. h. die Domains, die in den Display-URLs Ihrer Anzeigen verwendet werden), deren Inhalt zum Targeting Ihrer dynamischen Suchanzeigen in derselben Anzeigengruppe verwendet wird.

Sie können alle Kriterien oder bis zu drei einzelne Kriterien auswählen.

>[!NOTE]
>
>Um die Leistung bestmöglich zu verfolgen, erstellen Sie ein &quot;[!UICONTROL All Targets]&quot;-Ziel für nur eine Anzeigengruppe pro Kampagne.

>[!TIP]
>
>Um mehrere Kontokomponenten gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Wählen Sie das Werbenetzwerk, das Konto, die Kampagne und die Anzeigengruppe aus und klicken Sie dann auf **[!UICONTROL Continue]**.

1. Geben Sie die [Einstellungen für dynamische Suche](#dynamic-search-target-settings) an.

1. Klicken Sie auf **[!UICONTROL Post]**.

## Bearbeiten [!DNL Google Ads] Einstellungen für dynamische Suchziele

Sie können den Status oder das maximale Angebot für eine [!DNL Google Ads] dynamische Suchzielgruppe bearbeiten. Die Kriterien für die Zielgruppe können nicht geändert werden.

>[!TIP]
>
>Um große Datenmengen gleichzeitig zu bearbeiten, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder zu bearbeitenden Zeile.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

1. Geben Sie die [Einstellungen für dynamische Suche](#dynamic-search-target-settings) an.

   Bei mehreren Zielen werden Ihre Änderungen auf alle ausgewählten Ziele angewendet. Für die [!UICONTROL Bid field] haben Sie die Möglichkeit, vorhandene Werte in einen bestimmten Wert zu ändern oder den Betrag um einen bestimmten Prozentsatz oder Geldbetrag mit einer Grenze zu erhöhen oder zu verringern.

1. Speichern Sie die Daten:

   * (Einzelne Ziele) Klicken Sie auf **[!UICONTROL Post]**.

   * (Mehrere Anzeigengruppen) Klicken Sie auf **[!UICONTROL Post Now]**.

## Ändern des Status [!DNL Google Ads] dynamischen Suchziele

Sie können jedes aktive dynamische Suchziel in einem unterstützten Kampagnentyp anhalten, um seine Verwendung für dynamische Suchanzeigen in derselben Anzeigengruppe zu beenden. Sie können sie später als Ziele verwenden, indem Sie den Anzeigenstatus wieder in „Aktiv“ ändern.

Sie können auch jede beliebige dynamische Zielgruppe löschen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. (Optional) Filtern Sie die Liste, um bestimmte dynamische Ziele einzuschließen.

1. Führen Sie einen der folgenden Schritte aus:

   * Um den Status einer dynamischen Zielgruppe zu ändern, klicken Sie in die Spalte **[!UICONTROL Status]** und ändern Sie den Status.

   * Gehen Sie wie folgt vor, um ein oder mehrere dynamische Ziele zu löschen:

      1. Aktivieren Sie das Kontrollkästchen neben jeder dynamischen Zielgruppe, die Sie löschen möchten.

     Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

      1. Klicken Sie in der Symbolleiste auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr") und wählen Sie **[!UICONTROL Delete]** aus.

      1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

## Einstellungen für dynamische Suche [!DNL Google Ads] {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (erforderlich, wenn Sie im [!UICONTROL DSA Options] der Kampagne keine Website-Domain und Sprache angeben; schreibgeschützt für vorhandene Ziele) Dynamische Suchziele für die Anzeigengruppe:

* *[!UICONTROL All Targets]* (Standard): Targeting aller indizierten Seiten.

* *\[Spezifische Ziele\]:* Gibt bis zu drei Kriterien für die indizierten Seiten an. Bei Auswahl dieser Option müssen Sie die Kriterien angeben, indem Sie Informationskategorien und bestimmte Werte angeben, für die Anzeigen ausgewählt werden sollen (z. B. „URL enthält shoes.example.com„). Um mehr als ein Kriterium anzugeben, klicken Sie auf **[!UICONTROL + And]**. Zu den Zielkriterien gehören:

   * *[!UICONTROL Category]:* Anzeigen für indizierte Seiten mit einer bestimmten [!DNL Google Ads] Inhaltskategorie anzuzeigen.

   * *[!UICONTROL URL]:* Anzeigen für indizierte Seiten mit einer bestimmten URL anzeigen, wobei der Wert an einer beliebigen Stelle in der URL enthalten sein kann.

   * *[!UICONTROL Page Title]:* Anzeigen für indizierte Seiten mit bestimmtem Text im Seitentitel anzeigen.

   * *[!UICONTROL Page Content]:* Anzeigen für indizierte Seiten mit bestimmtem Inhalt anzuzeigen.

**Status** Der Status der Zieleinstellungen:

* *[!UICONTROL Active]* (Standard): Aktiviert die Gebotsabgabe.

* *[!UICONTROL Paused]:* Deaktiviert Gebote.

* *[!UICONTROL Deleted]* (nur vorhandene Ziele): Löscht die Zieleinstellungen.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** Die Maximalkosten pro Klick (CPC) für eine Anzeige oder Kosten pro 1000 Impressionen (CPM) für eine Anzeige, wie für das Anzeigennetzwerk- und Kampagnenpreismodell zutreffend. Dieser Wert überschreibt den Wert auf Anzeigengruppenebene.

>[!NOTE]
>
>Wenn sich das Ziel in einem optimierten Portfolio befindet, wird das angegebene CPC-Angebot einen Tag lang angewendet. Anschließend platziert die Optimierungsfunktion Angebote gemäß ihren eigenen Berechnungen.

>[!MORELIKETHIS]
>
>* [Über [!DNL Google Ads] dynamische Suchziele](dynamic-search-target-about.md)
