---
title: Verwalten von Zielgruppenzielen für Kampagnen und Anzeigengruppen
description: Erfahren Sie, wie Sie Audience-Ziele für Ihre - [!DNL Google Ads] -Kampagnen  [!DNL Microsoft Advertising]  Anzeigengruppen konfigurieren und verwalten.
exl-id: 9a496d15-082d-44e1-a0a3-71356e24b932
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# Verwalten von Zielgruppenzielen für Ihre [!DNL Google Ads] und [!DNL Microsoft Advertising] Kampagnen und Anzeigengruppen

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising]*

[!DNL Google Ads] Kampagnen und Anzeigengruppen sowie [!DNL Microsoft Advertising] Anzeigengruppen können bestimmte Zielgruppen aus demselben Anzeigennetzwerk ansprechen. Das Anzeigennetzwerk bestimmt, wie groß eine Zielgruppe sein muss, um anvisiert zu werden.

>[!NOTE]
>
>Ausnahmen überschreiben immer Einschlüsse/Ziele.

Sie können Zielgruppenziele konfigurieren, die Angebotsmodifikatoren für Zielgruppenziele bearbeiten und den Status von Zielgruppenzielen ändern.

## Zielgruppenziele konfigurieren

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Wählen Sie das Anzeigennetzwerk und den Kontonamen aus und klicken Sie dann auf **[!UICONTROL Continue]**.

1. Konfigurieren Sie die Audience-Ziele für bestimmte Kampagnen und Anzeigengruppen:

   1. Wählen Sie die entsprechenden Zielgruppen für das angegebene Werbenetzwerk aus.

      Sie können optional nach Zielgruppen suchen, die eine bestimmte Textzeichenfolge mit mindestens drei Zeichen enthalten. Klicken Sie für jede passende Zielgruppe auf **[!UICONTROL Include]** , um sie auszuwählen.

      [!DNL Google Ads] Zielgruppen für den Kundenabgleich sind nur für Such- und Shopping-Kampagnen verfügbar.

   1. Geben Sie die Ziele an:

      1. (Optional) Um eine Kampagne und ihre untergeordneten Anzeigengruppen zu erweitern, klicken Sie auf den Namen der Kampagne.

      1. (Optional) Um eine Kampagnenliste oder Anzeigengruppenliste nach einer im Namen enthaltenen Textzeichenfolge zu filtern, klicken Sie auf ![Filter](/help/search-social-commerce/assets/filter.png "Filter") , geben Sie die Textzeichenfolge entweder ein oder fügen Sie sie in das Eingabefeld ein und drücken Sie dann die **[!UICONTROL Enter]**.

      1. Geben Sie jede Kampagne und jedes Anzeigengruppenziel für das angegebene Anzeigennetzwerk an, indem Sie auf den angrenzenden leeren Kreis klicken, sodass ein blaues Häkchen (![Auswählen](/help/search-social-commerce/assets/include.png "Auswählen")) angezeigt wird.

      Sie können keine Zielgruppe sowohl für eine übergeordnete Kampagne als auch für eine untergeordnete Anzeigengruppe konfigurieren (die die Zielgruppe automatisch verwendet).

1. Klicken Sie auf **[!UICONTROL Post]**.

1. (Optional) Legen Sie in der [!UICONTROL Targets] eine Angebotsanpassung für das Ziel auf eine der folgenden Arten fest:

   * Klicken Sie in die Spalte **[!UICONTROL Bid Adjustment]** und geben Sie einen Wert ein.

   * Aktivieren Sie das Kontrollkästchen neben der Zielzeile. Klicken Sie in der Symbolleiste auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten"), geben Sie den Angebotsmodifikator ein und klicken Sie dann auf **[!UICONTROL Post]**.

   Werte können Folgendes beinhalten:

   * *0%:* Gebote für diese Zielgruppe nicht anpassen.

   * /[*Andere Werte von -90% bis 900%*/]: Erhöhen oder Verringern des Angebots für Anzeigen für diese Zielgruppe. Wenn beispielsweise das Gebot auf Keyword-Ebene 1 USD beträgt und die Gebotsanpassung für ein bestimmtes Zielgruppenziel 50 % beträgt, erhöht sich das Gebot für diese Zielgruppe auf 1,50 USD.

## Bearbeiten des Angebotsmodifikators für Zielgruppenziele

Sie können den Angebotsmodifikator und den Status von Zielgruppenzielen für alle Zielgruppentypen mit Ausnahme der marktinternen Zielgruppen ändern.

>[!NOTE]
>
>Search, Social und Commerce optimieren den Angebotsmodifikator automatisch, wenn die übergeordnete Kampagne die CPC-Angebotsstrategie verwendet und sich in einem Portfolio befindet, das so konfiguriert ist, dass die Angebotsanpassungswerte für Zielgruppenziele automatisch optimiert werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Um einen Angebotsmodifikator für eine Zielgruppe zu bearbeiten, klicken Sie in die Spalte **[!UICONTROL Bid Adjustment]** und bearbeiten Sie die Angebotsanpassung.

   * Gehen Sie wie folgt vor, um einen Angebotsmodifikator für eine oder mehrere Zielgruppen zu bearbeiten:

      1. Aktivieren Sie das Kontrollkästchen neben jeder zu bearbeitenden Zielgruppe.

         Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

      1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

      1. Bearbeiten Sie die **[!UICONTROL Bid Modifier]**- und/oder **[!UICONTROL Status]**.

         Für das Feld [!UICONTROL Bid Modifier] haben Sie die Möglichkeit, vorhandene Werte in einen bestimmten Wert zu ändern oder den Betrag um einen bestimmten Prozentsatz oder Geldbetrag mit einer Grenze zu erhöhen oder zu verringern.

         Bei einem festgelegten Wert kann der Wert Folgendes enthalten:

         * *0%:* Gebote für diese Zielgruppe nicht anpassen.

         * /[*Andere Werte von -90% bis 900%*/]: Erhöhen oder Verringern des Angebots für Anzeigen für diese Zielgruppe. Wenn beispielsweise das Gebot auf Keyword-Ebene 1 USD beträgt und die Gebotsanpassung für ein bestimmtes Zielgruppenziel 50 % beträgt, erhöht sich das Gebot für diese Zielgruppe auf 1,50 USD.

         Bei mehreren Zielen werden Ihre Änderungen auf alle ausgewählten Ziele angewendet.

      1. (Optional) Klicken Sie auf **[!UICONTROL Additional Details]** und geben Sie optional einen Projektnamen und eine Beschreibung ein.

      1. Klicken Sie auf **[!UICONTROL Post]**.

## Ändern des Status von Audience-Zielen

Sie können eine aktive Zielgruppe anhalten, um die Angebotsabgabe dafür zu deaktivieren. Sie können die Gebotsabgabe später fortsetzen, indem Sie den Status wieder in Aktiv ändern.

Sie können auch eine aktive oder angehaltene Audience-Suche löschen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. (Optional) Filtern Sie die Liste, um bestimmte Zielgruppenziele einzuschließen.

1. Aktivieren Sie das Kontrollkästchen neben jeder Zielgruppe, deren Status Sie ändern möchten.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste auf die Schaltfläche Status :

   * Um die Zeilen zu aktivieren, klicken Sie auf ![Aktivieren](/help/search-social-commerce/assets/activate.png "Aktivieren").

   * Um die Zeilen anzuhalten, klicken Sie auf ![Pause](/help/search-social-commerce/assets/pause.png "Pause").

   * Um die Zeilen zu löschen, klicken Sie auf ![Mehr Aktionen](/help/search-social-commerce/assets/more.png "Mehr Aktionen") und wählen Sie **[!UICONTROL Delete]** aus. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Info über Zielgruppen](audience-about.md)
>* [Verwalten von Zielgruppenausschlüssen für Kampagnen und Anzeigengruppen](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
