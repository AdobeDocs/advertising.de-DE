---
title: Verwalten von Einkaufsproduktgruppen
description: Erfahren Sie mehr über Shopping-Produktgruppen und das Erstellen, Bearbeiten und Löschen dieser Produktgruppen und verweisen Sie auf die Produktgruppeneinstellungen für Google Ads und Microsoft Advertising.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c074f430583e2d320eb4d47b4fc956c1822bd04a
workflow-type: tm+mt
source-wordcount: 2337
ht-degree: 0%

---


# Verwalten von Einkaufsproduktgruppen

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising] Shopping-Kampagnen*

Sie können Produktgruppen in der [!UICONTROL Product Groups] unter [!UICONTROL Assets] > [!UICONTROL Shopping] erstellen und verwalten.

Sie können Daten zu Produktgruppen in der [!UICONTROL Product Group Report][&#128279;](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md) .

## Was sind Produktgruppen?

In Shopping-Kampagnen bestimmen Ihre Produktgruppen - nicht Keywords - die Produkte in Ihrem Merchant-Center-Konto, für die Shopping-Anzeigen angezeigt werden. Jede Produktgruppe basiert auf einem einzelnen Produktattribut (z. B. Kategorie, Produkttyp, Marke, Bedingung, Produkt-ID oder benutzerdefinierte Beschriftungen) und verwendet dasselbe Angebot für alle übereinstimmenden Produkte. Sie können Angebote für die Produkte in jeder Gruppe ein- oder ausschließen.

Sie konfigurieren Produktgruppen auf Anzeigengruppenebene, um zu bestimmen, welche Produkte in Ihren Merchant-Center-Konten in den Shopping-Anzeigen für die Anzeigengruppe angezeigt werden. Auch wenn die Anzeigengruppe keine Anzeigenentitäten enthält, zeigt das Anzeigennetzwerk weiterhin Anzeigen für die Produkte an.

Wenn dasselbe Produkt in mehr als einer Kampagne enthalten ist, verwendet das Anzeigennetzwerk zunächst die Kampagnenpriorität, um zu bestimmen, welche Kampagne (und das zugehörige Angebot) für die Anzeigenauktion geeignet ist. Wenn alle Kampagnen dieselbe Priorität haben, ist die Kampagne mit dem höchsten Angebot geeignet.

Weitere Informationen zu [!DNL Google] Shopping-Kampagnen und Anzeigen finden Sie unter [Implementieren von  [!DNL Google Ads] -Shopping-](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)&quot; und in der Dokumentation zu [Google Ads](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&rd=1). Weitere Informationen zu [!DNL Microsoft] Shopping-Kampagnen finden Sie unter [Implementieren [!DNL Microsoft Advertising] Shopping-](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)&quot; und in der [[!DNL Microsoft Advertising] Dokumentation](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>In Kampagnen mit dem Typ „Performance Max“ wird keine [!DNL Google Ads] für Gruppen von Auflistungslisten unterstützt. Verwenden Sie zum Verwalten und Anzeigen von Daten für Auflistungsgruppen den [!DNL Google Ads].

### Produktgruppen-Hierarchie

Bevor Sie Produktgruppen mit bestimmten Attributen für eine Anzeigengruppe erstellen können, müssen Sie zunächst eine allumfassende Produktgruppe namens &quot;[!UICONTROL All Products]&quot; erstellen. Über diese übergeordnete Produktgruppe können Sie untergeordnete Produktgruppen für Produktuntergruppen erstellen, und Sie können untergeordnete Produktgruppen aus den untergeordneten Produktgruppen erstellen. Nachdem Sie die erste untergeordnete Produktgruppe für eine Anzeigengruppe erstellt haben, wird automatisch eine andere Produktgruppe mit dem Namen &quot;[!UICONTROL Everything Else]&quot; anhand des Standardangebots für die Anzeigengruppe erstellt. Wenn Sie weitere Produktgruppen hinzufügen, wird die Gruppe &quot;[!UICONTROL Everything Else]&quot; entsprechend angepasst, sodass sie alle Produkte umfasst, die nicht zu einer anderen Produktgruppe gehören.

Innerhalb einer Anzeigengruppe können Sie bis zu sieben Ebenen von Produktgruppen (ohne &quot;[!UICONTROL All Products]„) erstellen, um Angebote ein- oder auszuschließen, wobei eine oder mehrere Produktgruppen auf jeder Ebene auf dasselbe Attribut abzielen (z. B. [!UICONTROL Brand]=Acme für eine Produktgruppe und [!UICONTROL Brand]=AcmePlus für eine andere auf derselben Ebene). Übergeordnete Produktgruppen werden als Unterteilungen bezeichnet. Die unterste Ebene der Unterteilung wird als Einheit bezeichnet. Sie können Gebote und Tracking-Vorlagen auf Einheitenebene festlegen oder Gebote vollständig ausschließen. Der gesamte Satz aktiver Produktgruppen für eine Anzeigengruppe wird hierarchisch angewendet, um die geeigneten Produkte zu bestimmen. Wenn Sie beispielsweise [!UICONTROL All Products] in [!UICONTROL Brand]=AcmeBasic und [!UICONTROL Brand]=AcmePlus unterteilen und dann jede dieser Produktgruppen weiter in [!UICONTROL Condition]=New unterteilen und Gebote abgeben, können nur neue Produkte mit den Marken AcmeBasic und AcmePlus beworben oder von der Werbung ausgeschlossen werden.

![Beispiel eines Produktgruppensatzes](/help/search-social-commerce/assets/product-group-list-new.png "Beispiel eines Produktgruppensatzes")

![Beispiel für eine Produktgruppenhierarchie](/help/search-social-commerce/assets/product-group-tree-new.png "Beispiel-Produktgruppenhierarchie")

### Produktfilter {#product-filters}

<!-- I should be able to point to help in GGL and MS -->

Siehe auch die [!DNL Google Ads]-Hilfe [Verwalten einer Shopping-Kampagne mit &#x200B;](https://support.google.com/google-ads/answer/6275317)&quot; und die [!DNL Microsoft Advertising]-Hilfe [Verstehen und Verwenden von Produktgruppen](https://help.ads.microsoft.com/#apex/bae/en/56782).

| Einkaufsnetz | Produkt-Dimension | Attribute | Notizen |
|----|----|----|----|
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]: [!UICONTROL Category=]<br><br>Microsoft: [!UICONTROL Category 1=] zu [!UICONTROL Category 5=] | \[Die Kategorie-ID\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Brand=] | \[Die Marke\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Item ID=] | \[Die Element-ID\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Condition] | [!UICONTROL New], [!UICONTROL Used], [!UICONTROL Refurbished], [!UICONTROL Unknown] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!DNL Google Ads]: [!UICONTROL Product Type (1st level)=] zu [!UICONTROL Product Type (5th level)=]<br><br>[!DNL Microsoft]: [!UICONTROL Product Type=] | \[Der Produkttyp\] | — |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | [!UICONTROL Custom Label 0=] zu [!UICONTROL Custom Label 4=] | \[Das Attribut für die benutzerdefinierte Beschriftung\] | — |
| [!DNL Google Ads] | channel= | [!UICONTROL Local], [!UICONTROL Online] | Um Anzeigen nur für lokale Produkte oder Online-Produkte anzuzeigen.<br><br><b>Hinweis:</b> Um Anzeigen für lokale Produkte zu erstellen, muss die Option „Lokale Inventaranzeigen“ aktiviert sein und Sie müssen am lokalen Einkaufsprogramm mit [!DNL Google Merchant Center] teilnehmen. |
| [!DNL Google Ads] | [!UICONTROL ChannelExclusivity=] | [!UICONTROL SingleChannel], [!UICONTROL MultiChannel] | Gibt an, ob Anzeigen für Produkte angezeigt werden sollen, die nur für einen einzelnen Kanal verfügbar sind (entweder nur lokal oder nur online) oder für mehrere Kanäle verfügbar sind (sowohl lokal als auch online). |

## Die [!UICONTROL Product Groups]

Die [!UICONTROL Product Groups] Ansicht unter [!UICONTROL Assets] > [!UICONTROL Shopping] listet alle Produktgruppen in der gefilterten Ansicht für das ausgewählte Advertiser-Konto auf. Sie können auch Produktgruppen erstellen und verwalten.

### Verfügbare Aktionen <!-- Go through all -->

* [Erstellen einer &quot;[!UICONTROL All Products]&quot;-Produktgruppe](#product-group-create-all-products)

* [Erstellen eines untergeordneten Produktgruppenknotens in einer vorhandenen Produktgruppe](#node-add)

* Bearbeiten der Einstellungen für einen Produktgruppenknoten:

  * [Bearbeiten beliebiger Einstellungen](#node-edit)

  * [Nur die [!UICONTROL Tracking Template] bearbeiten](#node-edit-tracking-template)

  * [Nur die [!UICONTROL Max CPC] bearbeiten](#node-edit-maxcpc)

* [Löschen eines Produktgruppenknotens](#node-delete)

* [Einschränkungen zuweisen](#constraint-assign) zu Produktgruppen und [Einschränkungen entfernen](#constraint-unassign) aus Produktgruppen

* [Zuweisen von &#x200B;](#classification-values-assign) zu Produktgruppen und [Entfernen von &#x200B;](#classification-values-remove) aus Produktgruppen“

>[!NOTE]
>
>Sie können große Mengen an Produktgruppendaten (einschließlich Kennzeichnungen und Einschränkungszuweisungen) gleichzeitig erstellen und bearbeiten, indem Sie [Bulksheet-Dateien](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) hochladen und im Werbenetzwerk posten.

## Erstellen einer &quot;[!UICONTROL All Products]&quot;-Produktgruppe {#product-group-create-all-products}

Bevor Sie Produktgruppen mit bestimmten Attributen erstellen können, müssen Sie zunächst eine allumfassende Produktgruppe namens &quot;[!UICONTROL All Products]&quot; erstellen. Jede Anzeigengruppe kann nur eine &quot;[!UICONTROL All Products]&quot;-Gruppe aufweisen.

>[!TIP]
>
>Um mehrere Kontokomponenten gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL Create Product Group]**.

1. Wählen Sie das Werbenetzwerk, das Konto, die Kampagne und die Anzeigengruppe aus und klicken Sie dann auf **[!UICONTROL Continue]**.

1. Geben Sie die [Google Ads-](#google-ads-product-group-settings) oder [Microsoft Advertising-Produktgruppeneinstellungen](#microsoft-advertising-product-group-settings) an.

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

1. Klicken Sie bei Bedarf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten") und ändern Sie die [Google Ads-Produktgruppeneinstellungen &#x200B;](#google-ads-product-group-settings) [Microsoft Advertising-](#microsoft-advertising-product-group-settings).

1. Klicken Sie auf **[!UICONTROL Create]**.

## Erstellen eines untergeordneten Produktgruppenknotens in einer vorhandenen Produktgruppe {#product-group-create-child}

Nachdem Sie mindestens eine vollständige &quot;[!UICONTROL All Products]&quot;-Gruppe für eine Anzeigengruppe erstellt haben, können Sie untergeordnete Produktgruppenknoten für Untergruppen von Produkten erstellen, die Sie ein- oder ausschließen möchten, wobei eine oder mehrere Produktgruppen auf jeder Ebene auf dasselbe Attribut abzielen (z. B. [!UICONTROL Brand]=Acme für eine Produktgruppe und [!UICONTROL Brand]=AcmePlus für eine andere auf derselben Ebene). Sie können bis zu sieben Ebenen von untergeordneten Produktgruppenknoten erstellen, ohne &quot;[!UICONTROL All Products]&quot; einzuschließen.

>[!NOTE]
>
>Es kann keine untergeordnete Produktgruppe für eine &quot;[!UICONTROL Everything Else]&quot; Produktgruppe erstellt werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. (Optional) Um eine Produktgruppe und ihre untergeordneten Produktgruppenknoten in der Baumansicht anzuzeigen, halten Sie den Cursor über dem Namen der Produktgruppe und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Tree View]**.

1. Halten Sie den Cursor über den Namen der Produktgruppe und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL + Add Node]**.

1. Geben Sie die [Google Ads-](#google-ads-product-group-settings) oder [Microsoft Advertising-Produktgruppeneinstellungen](#microsoft-advertising-product-group-settings) an.

1. Klicken Sie auf **[!UICONTROL Center]**.

## Bearbeiten von Einstellungen für einen Produktgruppenknoten {#node-edit}

Sie können die Bid- und Tracking-Vorlage für Einzelproduktgruppenknoten (Produktgruppen ohne untergeordnete Produktgruppenknoten) bearbeiten, die für eine Anzeigengruppe enthalten sind. Sie können keine Informationen für ausgeschlossene Produktgruppen oder für eingeschlossene oder ausgeschlossene Unterteilungsknoten bearbeiten, bei denen es sich um Produktgruppen mit untergeordneten Produktgruppenknoten handelt.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. (Optional) Um eine Produktgruppe und ihre untergeordneten Produktgruppenknoten in der Baumansicht anzuzeigen, halten Sie den Cursor über dem Namen der Produktgruppe und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Tree View]**.

1. Halten Sie den Cursor über den Namen der Produktgruppe und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL + Edit Node]**.

1. Bearbeiten Sie die [Google Ads-](#google-ads-product-group-settings) oder [Microsoft Advertising-Produktgruppeneinstellungen](#microsoft-advertising-product-group-settings).

1. Klicken Sie auf **[!UICONTROL Update]**.

## Nur die [!UICONTROL Tracking Template] für einen Produktgruppenknoten bearbeiten {#node-edit-tracking-template}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Halten Sie den Cursor über den Namen der Produktgruppe und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Tree View]** , um die Produktgruppe und ihre untergeordneten Produktgruppenknoten in der Baumansicht anzuzeigen.

1. Klicken Sie in der Spalte **[!UICONTROL Tracking Template]** auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten").

1. Ändern Sie den **[!UICONTROL Tracking Template]** und klicken Sie dann auf **[!UICONTROL Save]**.

## Nur die [!UICONTROL Max CPC] für einen Produktgruppenknoten bearbeiten {#node-edit-maxcpc}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Halten Sie den Cursor über den Namen der Produktgruppe und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Tree View]** , um die Produktgruppe und ihre untergeordneten Produktgruppenknoten in der Baumansicht anzuzeigen.

1. Klicken Sie in der Spalte **[!UICONTROL Max CPC]** auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten").

1. Ändern Sie den **[!UICONTROL Max CPC]** und klicken Sie dann auf **[!UICONTROL Save]**.

## Löschen eines Produktgruppenknotens {#node-delete}

Sie können jede Produktgruppe löschen - mit Ausnahme der Gruppe „Alles andere“, wenn andere Produktgruppen auf derselben Ebene vorhanden sind -, mit der bestimmt wird, welche Produkte in Ihrem Merchant-Center-Konto in den Shopping-Anzeigen für die Anzeigengruppe enthalten sind. Beim Löschen einer Produktgruppe werden alle untergeordneten Produktgruppen gelöscht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Halten Sie den Cursor über den Namen der Produktgruppe und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Tree View]** , um die Produktgruppe und ihre untergeordneten Produktgruppenknoten in der Baumansicht anzuzeigen.

1. Klicken Sie in die Spalte **[!UICONTROL Status]** und wählen Sie **[!UICONTROL Delete]** aus.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

## Ausgewählten Produktgruppen eine Einschränkung zuweisen {#constraint-assign}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Produktgruppe, der Sie eine einzelne Begrenzung zuweisen.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Wählen Sie die Einschränkung aus.

1. Klicken Sie auf **[!UICONTROL Assign Now]**.

## Einschränkungen aus ausgewählten Produktgruppen entfernen {#constraint-unassign}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Produktgruppe, deren Zuweisung von Einschränkungen Sie aufheben möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Klicken Sie auf **[!UICONTROL Confirm]**.

## Zuweisen von Classification-Werten zu Produktgruppen {#classification-values-assign}

>[!NOTE]
>
>Beschriftungswerte werden von untergeordneten Entitäten übernommen. Geben Sie daher keine Werte für untergeordnete Entitäten ein, es sei denn, Sie möchten die übernommenen Werte überschreiben.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Produktgruppe, der Sie einen Kennzeichnungswert zuweisen.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**.

1. Gehen Sie für jeden zutreffenden Classification-Wert wie folgt vor:

   1. Geben Sie in der Spalte **[!UICONTROL Classifications]** die Klassifizierung an:

      * Um eine vorhandene Klassifizierung zu verwenden, klicken Sie auf den Klassifizierungsnamen, um sie zu erweitern.

      * Um eine Klassifizierung zu erstellen, klicken Sie in der Spaltenüberschrift auf [!UICONTROL +] . Geben Sie im Eingabefeld den Klassifizierungsnamen ein und klicken Sie dann auf ![Speichern](/help/search-social-commerce/assets/save-checkmark.png "Speichern"), um die Klassifizierung sofort zu speichern. Um die neue Klassifizierung zu verwenden, klicken Sie auf den Klassifizierungsnamen, um sie zu erweitern.

        Der Name muss aus [ASCII-Zeichen 32-126](https://www.asciitable.com/) bestehen und die maximale Länge beträgt 27 Einzelbyte-Zeichen.

   1. Geben Sie in der Spalte **[!UICONTROL Value Name]** den Wert für die ausgewählte Klassifizierung an:

      * Um einen vorhandenen Wert zu verwenden, wählen Sie den Wert aus.

      * Um einen Wert zu erstellen, klicken Sie in der Spaltenüberschrift auf [!UICONTROL +] . Geben Sie im Eingabefeld den Wert ein und klicken Sie dann auf ![Speichern](/help/search-social-commerce/assets/save-checkmark.png "Speichern"), um den Wert sofort zu speichern und standardmäßig auszuwählen.

        Die maximale Länge beträgt 100 Zeichen und kann ASCII- und Nicht-ASCII-Zeichen enthalten.

1. Klicken Sie auf **+[!UICONTROL Assign Now]**.

## Entfernen von Kennzeichnungswerten aus Produktgruppen {#classification-values-remove}

Das Entfernen eines Klassifizierungswerts entfernt die Verknüpfung mit der Kontokomponente und allen untergeordneten Komponenten. Berichtsdaten für den Classification-Wert sind für diese Komponenten nicht mehr verfügbar. Wenn Sie einen Klassifizierungswert entfernen, werden weder der Wert noch die Kontokomponenten gelöscht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Assets]>[!UICONTROL Shopping]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Produktgruppe, aus der Sie einen Titelwert entfernen möchten.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem Classification-Wert, der aus den ausgewählten Entitäten entfernt werden soll.

   Um alle zugewiesenen Werte auszuwählen, klicken Sie auf **[!UICONTROL Select All]**. Um die Auswahl aller zugewiesenen Werte aufzuheben, klicken Sie auf **[!UICONTROL Deselect All]**.

1. Klicken Sie auf **[!UICONTROL Unassign Selected]**.

## [!DNL Google Ads] Produktgruppeneinstellungen {#google-ads-product-group-settings}

### „Alle Produkte“-Produktgruppen

**[!UICONTROL Network]:** (Nur für neue Produktgruppen) Das Werbenetzwerk.

**[!UICONTROL Account]:** (Nur für neue Produktgruppen) Der Name des Anzeigen-Netzwerkkontos.

**[!UICONTROL Campaign]:** (Nur für neue Produktgruppen) Die Kampagne.

**[!UICONTROL Ad Group]:** (Nur neue Produktgruppen) Die Anzeigengruppe.

**[!UICONTROL Condition]** oder **[!UICONTROL Condition Type]:** (Schreibgeschützt) Alle Produkte

**[!UICONTROL Condition Value]:** (nur bestehende Produktgruppen)  

**[!UICONTROL Bid]** oder **[!UICONTROL Max CPC]:** (Nur Produktgruppen enthalten) Die maximalen Kosten pro Klick (CPC), was der höchste Betrag ist, der für einen Anzeigenklick bezahlt werden muss. Dieser Wert wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet und anstelle des Werts auf Anzeigengruppenebene.

{{$include /help/_includes/tracking-template-google.md}}

Diese Vorlage überschreibt Vorlagen auf höheren Ebenen und wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet. Für das Konto oder die Kampagne angegebene Anlagenparameter sind nicht enthalten. Für das Konto oder die Kampagne angegebene Anlagenparameter sind nicht enthalten.

### Alle anderen Produktgruppen

**[!UICONTROL Condition Type]** und **[!UICONTROL Condition Value]:** (Schreibgeschützt für bestehende Produktgruppen) Die Zielgruppendimensionen. Geben Sie für neue Produktgruppen die Dimension ein, nach der Produkte ausgewählt werden sollen, sowie das Attribut, das für die ausgewählte Informationskategorie qualifiziert ist (z. B. „Acme“ bei der Zielgruppenbestimmung nach Marke oder „Neu“ bei der Zielgruppenbestimmung nach Bedingung).

Nachdem Sie eine Produktgruppe für bestimmte Produktdimensionen (d. h. nicht für „Alle Produkte„) erstellt haben, erstellt Search, Social und Commerce automatisch eine Produktgruppe für „Alles andere“.

Eine Liste der verfügbaren Produktdimensionen finden Sie unter [Produktfilter](#product-filters). Die Liste der Dimensionen kann je nach [!UICONTROL Inventory Filter] der Kampagne begrenzt sein.

**[!UICONTROL Excluded]:** (optional für neue Produktgruppen; schreibgeschützt für bestehende Produktgruppen) Schließt Angebote für Anzeigen für übereinstimmende Produkte aus.

**[!UICONTROL Max CPC]:** (Nur für Produktgruppen) Die maximalen Kosten pro Klick (CPC), die den höchsten Betrag darstellen, der für einen Anzeigenklick bezahlt werden muss. Dieser Wert wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet und anstelle des Werts auf Anzeigengruppenebene.

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-google.md}}
-->

{{tracking-template-google}}

Diese Vorlage überschreibt Vorlagen auf höheren Ebenen und wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet.

## [!DNL Microsoft Advertising] Produktgruppeneinstellungen {#microsoft-advertising-product-group-settings}

### „Alle Produkte“-Produktgruppen

**[!UICONTROL Network]:** (Nur für neue Produktgruppen) Das Werbenetzwerk.

**[!UICONTROL Account]:** (Nur für neue Produktgruppen) Der Name des Anzeigen-Netzwerkkontos.

**[!UICONTROL Campaign]:** (Nur für neue Produktgruppen) Die Kampagne.

**[!UICONTROL Ad Group]:** (Nur neue Produktgruppen) Die Anzeigengruppe.

**[!UICONTROL Condition]** oder **[!UICONTROL Condition Type]:** (Schreibgeschützt) Alle Produkte

**[!UICONTROL Condition Value]:** (nur bestehende Produktgruppen)  

**[!UICONTROL Bid]** oder **[!UICONTROL Max CPC]:** (Nur Produktgruppen enthalten) Die maximalen Kosten pro Klick (CPC), was der höchste Betrag ist, der für einen Anzeigenklick bezahlt werden muss. Dieser Wert wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet und anstelle des Werts auf Anzeigengruppenebene.

**[!UICONTROL Base URL]:** (nur für neue Produktgruppen) Nicht verwendet<!-- Not sure this is supposed to be there; it's not showing for an existing product group: {{$include /help/_includes/base-url-keyword-ad-sitelink.md}} -->

{{$include /help/_includes/tracking-template-microsoft.md}}

Diese Vorlage überschreibt Vorlagen auf höheren Ebenen und wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet.

### Alle anderen Produktgruppen

**[!UICONTROL Condition Type]** und **[!UICONTROL Condition Value]:** (Schreibgeschützt für bestehende Produktgruppen) Die Zielgruppendimensionen. Geben Sie für neue Produktgruppen die Dimension ein, nach der Produkte ausgewählt werden sollen, sowie das Attribut, das für die ausgewählte Informationskategorie qualifiziert ist (z. B. „Acme“ bei der Zielgruppenbestimmung nach Marke oder „Neu“ bei der Zielgruppenbestimmung nach Bedingung).

Nachdem Sie eine Produktgruppe für bestimmte Produktdimensionen (d. h. nicht für „Alle Produkte„) erstellt haben, erstellt Search, Social und Commerce automatisch eine Produktgruppe für „Alles andere“.

Eine Liste der verfügbaren Produktdimensionen finden Sie unter [Produktfilter](#product-filters). Die Liste der Dimensionen kann je nach [!UICONTROL Inventory Filter] der Kampagne begrenzt sein.

**[!UICONTROL Excluded]:** (optional für neue Produktgruppen; schreibgeschützt für bestehende Produktgruppen) Schließt Angebote für Anzeigen für übereinstimmende Produkte aus.

**[!UICONTROL Max CPC]:** (Nur für Produktgruppen) Die maximalen Kosten pro Klick (CPC), die den höchsten Betrag darstellen, der für einen Anzeigenklick bezahlt werden muss. Dieser Wert wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet und anstelle des Werts auf Anzeigengruppenebene.

<!--
 ExL can't handle the same include twice in the same file, so using a snippet for the second occurrence.

{{$include /help/_includes/tracking-template-microsoft.md}}
-->

{{tracking-template-microsoft}}

Diese Vorlage überschreibt Vorlagen auf höheren Ebenen und wird nur für Einheiten ohne untergeordnete Produktgruppen verwendet.

>[!MORELIKETHIS]
>
>* [Implementieren [!DNL Google Ads] Shopping-Kampagnen](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [Implementieren [!DNL Microsoft Advertising] Shopping-Kampagnen](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
>* [Die [!UICONTROL Product Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/product-group-report.md)
