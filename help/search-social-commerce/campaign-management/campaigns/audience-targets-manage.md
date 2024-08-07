---
title: Verwalten von Zielgruppenzielen für Kampagnen und Anzeigengruppen
description: Erfahren Sie, wie Sie Zielgruppenziele für Ihre [!DNL Google Ads] und [!DNL Microsoft Advertising] Kampagnen und Anzeigengruppen konfigurieren und verwalten.
exl-id: 9a496d15-082d-44e1-a0a3-71356e24b932
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# Zielgruppenziele für Ihre [!DNL Google Ads] - und [!DNL Microsoft Advertising] -Kampagnen und Anzeigengruppen verwalten

*[!DNL Google Ads]und [!DNL Microsoft Advertising] nur*

[!DNL Google Ads] Kampagnen und Anzeigengruppen sowie [!DNL Microsoft Advertising] Anzeigengruppen können bestimmte Zielgruppen aus demselben Werbenetzwerk ansprechen. Das Werbenetzwerk bestimmt, wie groß eine Zielgruppe sein muss, damit sie als Zielgruppe ausgewählt werden kann.

>[!NOTE]
>
>Ausnahmen überschreiben immer Einschlüsse/Ziele.

Sie können Zielgruppenziele konfigurieren, die Angebotsmodifikatoren für Zielgruppenziele bearbeiten und den Status von Zielgruppenzielen ändern.

## Konfigurieren von Zielgruppenzielen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen") .

1. Wählen Sie das Werbenetzwerk und den Kontonamen aus und klicken Sie auf **[!UICONTROL Continue]**.

1. Konfigurieren Sie Zielgruppenziele für bestimmte Kampagnen und Anzeigengruppen:

   1. Wählen Sie die entsprechenden Zielgruppen für das angegebene Werbenetzwerk aus.

      Sie können optional nach Zielgruppen suchen, die eine bestimmte Textzeichenfolge mit mindestens drei Zeichen enthalten. Klicken Sie für jede passende Zielgruppe auf **[!UICONTROL Include]** , um sie auszuwählen.

      [!DNL Google Ads] Zielgruppen für Kundenabgleich sind nur für Such- und Einkaufskampagnen verfügbar.

   1. Geben Sie die Ziele an:

      1. (Optional) Klicken Sie auf den Kampagnennamen, um die untergeordneten Anzeigengruppen einer Kampagne zu erweitern.

      1. (Optional) Um eine Kampagnenliste oder Anzeigengruppenliste nach einer im Namen enthaltenen Textzeichenfolge zu filtern, klicken Sie auf ![Filter](/help/search-social-commerce/assets/filter.png "Filter") , geben Sie die Textzeichenfolge ein oder fügen Sie sie in das Eingabefeld ein und drücken Sie dann die Taste **[!UICONTROL Enter]**.

      1. Geben Sie die einzelnen Kampagnen- und Anzeigengruppenziele für das angegebene Anzeigennetzwerk an, indem Sie auf den angrenzenden leeren Kreis klicken, damit ein blaues Häkchen (![Auswählen](/help/search-social-commerce/assets/include.png "Auswählen")) angezeigt wird.

      Es ist nicht möglich, eine Zielgruppe sowohl für eine übergeordnete Kampagne als auch für eine untergeordnete Anzeigengruppe zu konfigurieren (die automatisch das Ziel verwendet).

1. Klicken Sie auf **[!UICONTROL Post]**.

1. (Optional) Legen Sie eine Angebotsanpassung für das Ziel auf eine der folgenden Arten in der [!UICONTROL Targets]-Ansicht fest:

   * Klicken Sie in die Spalte **[!UICONTROL Bid Adjustment]** und geben Sie einen Wert ein.

   * Aktivieren Sie das Kontrollkästchen neben der Zielzeile. Klicken Sie in der Symbolleiste auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten") , geben Sie den Angebotsmodifikator ein und klicken Sie dann auf **[!UICONTROL Post]**.

   Die Werte können Folgendes umfassen:

   * *0%:* So passen Sie keine Angebote für Anzeigen für diese Zielgruppe an.

   * /[*Andere Werte von -90 % bis 900 %*/]: Um das Angebot für Anzeigen für diese Zielgruppe zu erhöhen oder zu verringern. Wenn das Angebot auf Suchbegriffebene beispielsweise 1 USD und die Angebotsanpassung für ein bestimmtes Zielgruppen-Ziel 50 % beträgt, erhöht sich das Angebot für diese Zielgruppe auf 1,50 USD.

## Bearbeiten des Angebotsmodifikators für Zielgruppenziele

Sie können den Angebotsmodifikator und den Status von Zielgruppenzielen für alle Zielgruppentypen ändern, mit Ausnahme von In-Market-Zielgruppen.

>[!NOTE]
>
>Search, Social und Commerce optimieren den Angebotsmodifikator automatisch, wenn die übergeordnete Kampagne die CPC-Angebotsstrategie verwendet und sich in einem Portfolio befindet, das zur automatischen Optimierung der Angebotsanpassung für Zielgruppen konfiguriert ist.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Um einen Angebotsmodifikator für eine Zielgruppe zu bearbeiten, klicken Sie in die Spalte **[!UICONTROL Bid Adjustment]** und bearbeiten Sie die Angebotsanpassung.

   * Gehen Sie wie folgt vor, um einen Angebotsmodifikator für eine weitere Zielgruppe zu bearbeiten:

      1. Aktivieren Sie das Kontrollkästchen neben den zu bearbeitenden Zielgruppen.

         Tipps zum Auswählen mehrerer Zeilen finden Sie unter &quot;[Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

      1. Bearbeiten Sie die Felder **[!UICONTROL Bid Modifier]** und/oder **[!UICONTROL Status]**.

         Für das Feld [!UICONTROL Bid Modifier] haben Sie die Möglichkeit, die vorhandenen Werte in einen bestimmten Wert zu ändern oder den Betrag um einen bestimmten Prozentsatz oder Geldbetrag mit einer Begrenzung zu erhöhen oder zu verringern.

         Für einen festgelegten Wert kann der Wert Folgendes umfassen:

         * *0%:* So passen Sie keine Angebote für Anzeigen für diese Zielgruppe an.

         * /[*Andere Werte von -90 % bis 900 %*/]: Um das Angebot für Anzeigen für diese Zielgruppe zu erhöhen oder zu verringern. Wenn das Angebot auf Suchbegriffebene beispielsweise 1 USD und die Angebotsanpassung für ein bestimmtes Zielgruppen-Ziel 50 % beträgt, erhöht sich das Angebot für diese Zielgruppe auf 1,50 USD.

         Bei mehreren Zielgruppen werden Ihre Änderungen auf alle ausgewählten Zielgruppen angewendet.

      1. (Optional) Klicken Sie auf **[!UICONTROL Additional Details]** und geben Sie optional einen Projektnamen und eine Beschreibung ein.

      1. Klicken Sie auf **[!UICONTROL Post]**.

## Ändern des Status von Zielgruppenzielen

Sie können ein aktives Zielgruppen-Ziel anhalten, um die Gebote darauf zu deaktivieren. Sie können das Angebot später fortsetzen, indem Sie den Status zurück in &quot;aktiv&quot;ändern.

Sie können auch ein aktives oder angehaltenes Suchtzielgruppen-Ziel löschen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. (Optional) Filtern Sie die Liste, um bestimmte Zielgruppen einzuschließen.

1. Aktivieren Sie das Kontrollkästchen neben allen Zielgruppen, deren Status Sie ändern möchten.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter &quot;[Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. Klicken Sie in der Symbolleiste auf die Statusschaltfläche:

   * Klicken Sie zum Aktivieren der Zeilen auf ![Aktivieren](/help/search-social-commerce/assets/activate.png "Aktivieren").

   * Um die Zeilen anzuhalten, klicken Sie auf ![Pause](/help/search-social-commerce/assets/pause.png "Pause").

   * Klicken Sie zum Löschen der Zeilen auf ![Mehr Aktionen](/help/search-social-commerce/assets/more.png "Mehr Aktionen") und wählen Sie **[!UICONTROL Delete]** aus. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Über Zielgruppen](audience-about.md)
>* [Verwalten von Zielgruppenausschlüssen für Kampagnen und Anzeigengruppen](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
