---
title: Verwalten von Einkaufsproduktgruppen
description: Erfahren Sie, wie Sie Einkaufsproduktgruppen in Einkaufskampagnen erstellen und verwalten.
exl-id: cf818b87-ee4b-4cf5-a4e8-0b9a7fc32182
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Verwalten von Einkaufsproduktgruppen

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising] Shopping-Kampagnen*

Sie können in der Ansicht [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] Produktgruppen erstellen und bearbeiten sowie Produktgruppen und deren untergeordnete Produktgruppen löschen.

## Erstellen einer &quot;[!UICONTROL All Products]&quot;-Produktgruppe

Bevor Sie Produktgruppen mit bestimmten Attributen erstellen können, müssen Sie zunächst eine umfassende Produktgruppe mit dem Namen &quot;[!UICONTROL All Products]&quot;erstellen. Jede Anzeigengruppe kann nur eine &quot;[!UICONTROL All Products]&quot;-Gruppe aufweisen.

>[!TIP]
>
>Um mehrere Kontokomponenten gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen") .

1. Wählen Sie das Werbenetzwerk, das Konto, die Kampagne und die Anzeigengruppe aus und klicken Sie auf **[!UICONTROL Continue]**.

1. Geben Sie die [[!DNL Google Ads] Produktgruppeneinstellungen](product-group-settings-google.md) oder die [[!DNL Microsoft Advertising] Produktgruppeneinstellungen](product-group-settings-microsoft.md) an.

1. Klicken Sie auf **[!UICONTROL Post]**.

## Erstellen eines untergeordneten Produktgruppenknotens in einer vorhandenen Produktgruppe

Nachdem Sie mindestens eine All-Include-Gruppe &quot;[!UICONTROL All Products]&quot; für eine Anzeigengruppe erstellt haben, können Sie untergeordnete Produktgruppenknoten für Teilmengen von Produkten erstellen, die ein- oder ausgeschlossen werden sollen, wobei mindestens eine Produktgruppe auf jeder Ebene dasselbe Attribut angibt (z. B. [!UICONTROL Brand]=Acme für eine Produktgruppe und [!UICONTROL Brand]=AcmePlus für eine andere auf derselben Ebene). Sie können bis zu sieben Ebenen untergeordneter Produktgruppenknoten erstellen, darunter &quot;[!UICONTROL All Products]&quot;.

>[!NOTE]
>
>Sie können keine untergeordnete Produktgruppe für eine &quot;[!UICONTROL Everything Else]&quot;-Produktgruppe erstellen.

>[!TIP]
>
>Um mehrere Kontokomponenten gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Optional) Um eine Produktgruppe und ihre untergeordneten Produktgruppenknoten in der Baumansicht anzuzeigen, halten Sie den Cursor über den Namen der Produktgruppe, klicken Sie auf das Symbol ](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menü-Symbol") und wählen Sie dann **[!UICONTROL Tree View]** aus.![

1. Halten Sie den Cursor über den Namen der Produktgruppe, klicken Sie auf ![Dropdown-Menü &quot;Pfeil&quot;](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Dropdown-Menü &quot;Pfeil&quot;") und wählen Sie dann **[!UICONTROL + Add Node]** aus.

1. Geben Sie die [[!DNL Google Ads] Produktgruppeneinstellungen](product-group-settings-google.md) oder die [[!DNL Microsoft Advertising] Produktgruppeneinstellungen](product-group-settings-microsoft.md) an, einschließlich der Produktdimension und des Attributs.

1. Klicken Sie auf **[!UICONTROL Post]**.

## Bearbeiten der Knoteneinstellungen für Produktgruppen

Sie können die Angebots- und Tracking-Vorlage für Produktgruppenknoten (Produktgruppen ohne untergeordnete Produktgruppenknoten) bearbeiten, die für eine Anzeigengruppe enthalten sind. Sie können keine Informationen für ausgeschlossene Produktgruppen oder für eingeschlossene oder ausgeschlossene Unterteilungsknoten bearbeiten, bei denen es sich um Produktgruppen mit untergeordneten Produktgruppenknoten handelt.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Optional) Um eine Produktgruppe und ihre untergeordneten Produktgruppenknoten in der Baumansicht anzuzeigen, halten Sie den Cursor über den Namen der Produktgruppe, klicken Sie auf das Symbol ](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menü-Symbol") und wählen Sie dann **[!UICONTROL Tree View]** aus.![

1. Führen Sie einen der folgenden Schritte aus:

   1. (Um Einstellungen für einen einzelnen Produktgruppenknoten zu bearbeiten) Halten Sie den Cursor über den Namen der Produktgruppe, klicken Sie auf das Symbol ![Menü-Symbol](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menü-Symbol") und wählen Sie dann **[!UICONTROL + Edit Node]** aus.

   1. (So bearbeiten Sie Einstellungen für eine oder mehrere Anzeigengruppen) Gehen Sie wie folgt vor:

      1. Aktivieren Sie das Kontrollkästchen neben den einzelnen Knoten.

         Tipps zum Auswählen mehrerer Zeilen finden Sie unter &quot;[Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

1. Bearbeiten Sie die [[!DNL Google Ads] Produktgruppeneinstellungen](product-group-settings-google.md) oder die [[!DNL Microsoft Advertising] Produktgruppeneinstellungen](product-group-settings-microsoft.md).

   Bei mehreren Knoten werden Ihre Änderungen auf alle ausgewählten Knoten angewendet. Für das Feld [!UICONTROL Bid] haben Sie die Möglichkeit, die vorhandenen Werte in einen bestimmten Wert zu ändern oder den Betrag um einen bestimmten Prozentsatz oder Geldbetrag mit einer Begrenzung zu erhöhen oder zu verringern. Für das Feld [!UICONTROL Tracking Template] können Sie vorhandene Werte in einen angegebenen Wert ändern, eine vorhandene Zeichenfolge durch eine angegebene Zeichenfolge ersetzen, am Anfang jedes Werts ein angegebenes Präfix hinzufügen oder ein Suffix an das Ende jedes Werts anhängen.

1. (Optional) Klicken Sie auf **[!UICONTROL Additional Details]** und geben Sie optional einen Projektnamen und eine Beschreibung ein.

1. Klicken Sie auf **[!UICONTROL Post]**.

## Produktgruppenknoten löschen

Sie können jede Produktgruppe löschen - mit Ausnahme der Gruppe &quot;Alles andere&quot;, wenn andere Produktgruppen auf derselben Ebene vorhanden sind -, die verwendet wird, um zu bestimmen, welche Produkte in Ihrem Händlercenter-Konto in den Shopping-Anzeigen für die Anzeigengruppe enthalten sind. Durch Löschen einer Produktgruppe werden alle untergeordneten Produktgruppen gelöscht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Optional) Filtern Sie die Liste, um bestimmte Produktgruppen einzuschließen.

1. Führen Sie einen der folgenden Schritte aus:

   * Um eine Produktgruppe zu löschen, klicken Sie in die Spalte **[!UICONTROL Status]** und wählen Sie **[!UICONTROL Delete]** aus.

   * Gehen Sie wie folgt vor, um eine oder mehrere Produktgruppen zu löschen:

      1. Aktivieren Sie das Kontrollkästchen neben jeder Produktgruppe, die Sie löschen möchten.

         Tipps zum Auswählen mehrerer Zeilen finden Sie unter &quot;[Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Klicken Sie in der Symbolleiste auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr") und wählen Sie **[!UICONTROL Delete]** aus.

      1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Über Einkaufsproduktgruppen](product-group-about.md)
>* [[!DNL Google Ads] Produktgruppeneinstellungen](product-group-settings-google.md)
>* [[!DNL Microsoft Advertising] Produktgruppeneinstellungen](product-group-settings-microsoft.md)
