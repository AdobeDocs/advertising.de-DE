---
title: Verwalten von Einkaufsproduktgruppen
description: Erfahren Sie, wie Sie in Shopping-Kampagnen Shopping-Produktgruppen erstellen und verwalten.
exl-id: cf818b87-ee4b-4cf5-a4e8-0b9a7fc32182
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# Verwalten von Einkaufsproduktgruppen

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising] Shopping-Kampagnen*

In der Ansicht [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > Produktgruppen können Sie Produktgruppen erstellen und bearbeiten sowie Produktgruppen und deren untergeordnete Produktgruppen [!UICONTROL Product Groups].

## Erstellen einer &quot;[!UICONTROL All Products]&quot;-Produktgruppe

Bevor Sie Produktgruppen mit bestimmten Attributen erstellen können, müssen Sie zunächst eine allumfassende Produktgruppe namens &quot;[!UICONTROL All Products]&quot; erstellen. Jede Anzeigengruppe kann nur eine &quot;[!UICONTROL All Products]&quot;-Gruppe aufweisen.

>[!TIP]
>
>Um mehrere Kontokomponenten gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Wählen Sie das Werbenetzwerk, das Konto, die Kampagne und die Anzeigengruppe aus und klicken Sie dann auf **[!UICONTROL Continue]**.

1. Geben Sie die [[!DNL Google Ads] Produktgruppeneinstellungen](product-group-settings-google.md) oder [[!DNL Microsoft Advertising] Produktgruppeneinstellungen](product-group-settings-microsoft.md) an.

1. Klicken Sie auf **[!UICONTROL Post]**.

## Erstellen eines untergeordneten Produktgruppenknotens in einer vorhandenen Produktgruppe

Nachdem Sie mindestens eine vollständige &quot;[!UICONTROL All Products]&quot;-Gruppe für eine Anzeigengruppe erstellt haben, können Sie untergeordnete Produktgruppenknoten für Untergruppen von Produkten erstellen, die Sie ein- oder ausschließen möchten, wobei eine oder mehrere Produktgruppen auf jeder Ebene auf dasselbe Attribut abzielen (z. B. [!UICONTROL Brand]=Acme für eine Produktgruppe und [!UICONTROL Brand]=AcmePlus für eine andere auf derselben Ebene). Sie können bis zu sieben Ebenen von untergeordneten Produktgruppenknoten erstellen, ohne &quot;[!UICONTROL All Products]&quot; einzuschließen.

>[!NOTE]
>
>Es kann keine untergeordnete Produktgruppe für eine &quot;[!UICONTROL Everything Else]&quot; Produktgruppe erstellt werden.

>[!TIP]
>
>Um mehrere Kontokomponenten gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Optional) Um eine Produktgruppe und ihre untergeordneten Produktgruppenknoten in der Baumansicht anzuzeigen, halten Sie den Cursor über dem Namen der Produktgruppe, klicken Sie auf ![Menüsymbol](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menüsymbol") und wählen Sie dann **[!UICONTROL Tree View]** aus.

1. Halten Sie den Cursor über den Namen der Produktgruppe, klicken Sie auf ![Pfeil-Dropdown-Menü](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Pfeil-Dropdown-Menü") und wählen Sie dann **[!UICONTROL + Add Node]** aus.

1. Geben Sie die [[!DNL Google Ads] Produktgruppeneinstellungen](product-group-settings-google.md) oder [[!DNL Microsoft Advertising] Produktgruppeneinstellungen](product-group-settings-microsoft.md) einschließlich der Produktdimension und des -attributs an.

1. Klicken Sie auf **[!UICONTROL Post]**.

## Produktgruppen-Knoteneinstellungen bearbeiten

Sie können die Bid- und Tracking-Vorlage für Einzelproduktgruppenknoten (Produktgruppen ohne untergeordnete Produktgruppenknoten) bearbeiten, die für eine Anzeigengruppe enthalten sind. Sie können keine Informationen für ausgeschlossene Produktgruppen oder für eingeschlossene oder ausgeschlossene Unterteilungsknoten bearbeiten, bei denen es sich um Produktgruppen mit untergeordneten Produktgruppenknoten handelt.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Optional) Um eine Produktgruppe und ihre untergeordneten Produktgruppenknoten in der Baumansicht anzuzeigen, halten Sie den Cursor über dem Namen der Produktgruppe, klicken Sie auf ![Menüsymbol](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menüsymbol") und wählen Sie dann **[!UICONTROL Tree View]** aus.

1. Führen Sie einen der folgenden Schritte aus:

   1. (So bearbeiten Sie Einstellungen für einen einzelnen Produktgruppenknoten) Halten Sie den Cursor über dem Namen der Produktgruppe, klicken Sie auf ![Menüsymbol](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menüsymbol") und wählen Sie dann **[!UICONTROL + Edit Node]** aus.

   1. (So bearbeiten Sie Einstellungen für eine oder mehrere Anzeigengruppen:

      1. Aktivieren Sie das Kontrollkästchen neben jedem Knoten.

         Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

      1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

1. Bearbeiten Sie die [[!DNL Google Ads] Produktgruppeneinstellungen](product-group-settings-google.md) oder [[!DNL Microsoft Advertising] Produktgruppeneinstellungen](product-group-settings-microsoft.md).

   Bei mehreren Knoten werden Ihre Änderungen auf alle ausgewählten Knoten angewendet. Für das Feld [!UICONTROL Bid] haben Sie die Möglichkeit, vorhandene Werte in einen bestimmten Wert zu ändern oder den Betrag um einen bestimmten Prozentsatz oder Geldbetrag mit einer Grenze zu erhöhen oder zu verringern. Für das Feld [!UICONTROL Tracking Template] können Sie vorhandene Werte in einen angegebenen Wert ändern, eine vorhandene Zeichenfolge durch eine angegebene Zeichenfolge ersetzen, ein angegebenes Präfix an den Anfang jedes Werts hinzufügen oder ein Suffix an das Ende jedes Werts anhängen.

1. (Optional) Klicken Sie auf **[!UICONTROL Additional Details]** und geben Sie optional einen Projektnamen und eine Beschreibung ein.

1. Klicken Sie auf **[!UICONTROL Post]**.

## Produktgruppenknoten löschen

Sie können jede Produktgruppe löschen - mit Ausnahme der Gruppe „Alles andere“, wenn andere Produktgruppen auf derselben Ebene vorhanden sind -, mit der bestimmt wird, welche Produkte in Ihrem Merchant-Center-Konto in den Shopping-Anzeigen für die Anzeigengruppe enthalten sind. Beim Löschen einer Produktgruppe werden alle untergeordneten Produktgruppen gelöscht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]>[!UICONTROL Product Groups]**.

1. (Optional) Filtern Sie die Liste nach bestimmten Produktgruppen.

1. Führen Sie einen der folgenden Schritte aus:

   * Um eine Produktgruppe zu löschen, klicken Sie in die Spalte **[!UICONTROL Status]** und wählen Sie **[!UICONTROL Delete]** aus.

   * Gehen Sie wie folgt vor, um eine oder mehrere Produktgruppen zu löschen:

      1. Aktivieren Sie das Kontrollkästchen neben jeder Produktgruppe, die Sie löschen möchten.

         Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

      1. Klicken Sie in der Symbolleiste auf ![Mehr](/help/search-social-commerce/assets/more.png "Mehr") und wählen Sie **[!UICONTROL Delete]** aus.

      1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Über Shopping-Produktgruppen](product-group-about.md)
>* [[!DNL Google Ads] Produktgruppeneinstellungen](product-group-settings-google.md)
>* [[!DNL Microsoft Advertising] Produktgruppeneinstellungen](product-group-settings-microsoft.md)
