---
title: Anzeigengruppen verwalten
description: Erfahren Sie, wie Sie Anzeigengruppen erstellen und verwalten.
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: fc836f17b53a3708bf881dc62a437d391709a050
workflow-type: tm+mt
source-wordcount: 1676
ht-degree: 0%

---

# Anzeigengruppen verwalten

<!-- Go through all -->

*Beta-Funktion*

Eine Anzeigengruppe enthält eine Reihe von Anzeigen und die zugehörigen Keywords. Eine Anzeigengruppe in einer Kampagne, die auf das Display-Netzwerk abzielt, kann auch Platzierungen enthalten, d. h. Positionen im Display-Netzwerk, in denen Ihre Anzeigen erscheinen können. Die Einstellungen der Anzeigengruppen, die für alle Komponenten der Anzeigengruppe gelten, variieren je nach Anzeigennetzwerk.

Sobald Sie [ein Anzeigennetzwerkkonto über eine API-Verbindung zugänglich machen](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) und Search, Social und Commerce die Kontodaten mit dem Anzeigennetzwerk synchronisiert haben, können Sie Anzeigengruppen für einen [unterstützten Kampagnentyp“ ](/help/search-social-commerce/introduction/supported-inventory.md). Sie können auch den Status von Anzeigengruppen bearbeiten und ändern.

Einzelheiten zu den für die einzelnen Werbenetzwerke verfügbaren Funktionen finden Sie unter &quot;[Unterstützte Inventarisierung](/help/search-social-commerce/introduction/supported-inventory.md).

## Über die [!UICONTROL Ad Groups] {#ad-group-view-about}

Die Ansicht [!UICONTROL Manage] > [!UICONTROL Ad Groups] listet alle Anzeigengruppen in der gefilterten Ansicht für das ausgewählte Advertiser-Konto auf.

### Verfügbare Aktionen

* [Erstellen einer Anzeigengruppe](#ad-group-create)

* [Eine Anzeigengruppe innerhalb der Zeile umbenennen](#ad-group-rename)

* [Anzeigengruppeneinstellungen bearbeiten](#ad-group-edit)

* [Ändern des Status einer Anzeigengruppe innerhalb der Zeile oder Löschen dieser Gruppe](#ad-group-status)

* [Anzeigen eines Leistungsdiagramms in der [!UICONTROL Ad Groups]](#ad-group-performance-graph)

* [Weisen Sie Anzeigengruppen Angebotsbegrenzungen zu und heben Sie die Zuweisung von Begrenzungen zu Anzeigengruppen auf](#ad-group-constraints)

* [Zuweisen von Kennzeichnungsklassifizierungen zu Anzeigengruppen und Entfernen von Kennzeichnungsklassifizierungen aus Anzeigengruppen](#ad-group-classifications)

* [Verwalten von Datenansichtsberichten aus der [!UICONTROL Ad Groups]](#ad-group-reports)

## Erstellen einer Anzeigengruppe {#ad-group-create}

>[!TIP]
>
>Um eine große Anzahl von Anzeigengruppen gleichzeitig zu erstellen, verwenden Sie<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [Campaign-Bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Klicken Sie auf **[!UICONTROL Create Ad Group]**.

1. Geben Sie die [Baidu](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-ly.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-microsoft.md) oder [Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-yandex.md) Anzeigengruppeneinstellungen an.

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

1. Klicken Sie bei Bedarf auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten") **[!UICONTROL Edit]** und ändern Sie die Einstellungen der Anzeigengruppe.

1. Klicken Sie auf **[!UICONTROL Create]**.

Später können Sie die Gebote auf Anzeigengruppenebene überschreiben, indem Sie Gebote für einzelne Keywords oder Platzierungen in der Anzeigengruppe festlegen.

## Eine Anzeigengruppe umbenennen {#ad-group-rename}

Schnelles Umbenennen einer Anzeigengruppe, ohne die vollständigen Anzeigengruppeneinstellungen zu öffnen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Halten Sie den Cursor über der Anzeigengruppenzeile und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Rename]**.

1. Bearbeiten Sie den Namen und klicken Sie dann auf **[!UICONTROL Apply]**.

## Anzeigengruppeneinstellungen bearbeiten {#ad-group-edit}

Sie können Einstellungen für einzelne Anzeigengruppen bearbeiten. Sie können auch einige Felder für mehrere Anzeigengruppen gleichzeitig bearbeiten, einschließlich einiger Anzeigengruppendetails, Budgetoptionen und URL-Optionen, die für alle ausgewählten Anzeigengruppen gelten.

>[!TIP]
>
>Sie können Daten mit auch stapelweise bearbeiten<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [Campaign-Bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Halten Sie den Cursor über den Entitätsnamen und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Edit]**.

   * Aktivieren Sie das Kontrollkästchen neben der Anzeigengruppe. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie die [Baidu](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-ly.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-microsoft.md) oder [Yandex](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-yandex.md) Anzeigengruppeneinstellungen.

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

1. Klicken Sie bei Bedarf auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten") **[!UICONTROL Edit]** und ändern Sie die Einstellungen der Anzeigengruppe.

1. Klicken Sie auf **[!UICONTROL Update]**.

## Ändern des Status einer Anzeigengruppe {#ad-group-status}

Schnelles Ändern des Status einer Anzeigengruppe, ohne die vollständigen Anzeigengruppeneinstellungen zu öffnen.

Sie können jede aktive Anzeigengruppe in einem unterstützten Anzeigennetzwerk anhalten, um die Angebotsabgabe darauf zu deaktivieren. Sie können die Gebotsabgabe später fortsetzen, indem Sie den Status wieder in Aktiv ändern.

Sie können auch alle aktiven oder pausierten Anzeigengruppen löschen. Gelöschte Anzeigengruppen werden aus dem Anzeigennetzwerk gelöscht. Sie sind weiterhin sichtbar, wenn Sie sie in den Datenfilter einbeziehen, können aber nicht geändert werden.

### Anzeigengruppe aktivieren oder anhalten

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Halten Sie den Cursor über der Anzeigengruppenzeile und klicken Sie ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten") neben der [!UICONTROL Status].

1. Status ändern:

   * Um eine pausierte Anzeigengruppe zu aktivieren, klicken Sie auf **[!UICONTROL Active]**.

   * Um eine aktive Anzeigengruppe anzuhalten, wählen Sie **[!UICONTROL Paused]** aus.

### Eine Anzeigengruppe löschen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Halten Sie den Cursor über der Anzeigengruppenzeile und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Delete]**.

   * Halten Sie den Cursor über der Anzeigengruppenzeile und klicken Sie ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten") neben der [!UICONTROL Status]. Wählen Sie **[!UICONTROL Deleted]** aus.

## Angebotseinschränkungszuweisungen für Anzeigengruppen verwalten {#ad-group-constraints}

Jede Entität kann nur eine Einschränkung aufweisen. Beschränkungen werden von untergeordneten Entitäten übernommen, sodass Sie untergeordneten Entitäten keine Beschränkungen zuweisen müssen, es sei denn, Sie möchten die übernommenen Werte überschreiben.

Wenn Sie die Zuweisung einer Einschränkung aufheben, wird die Verknüpfung mit den Kontokomponenten und allen untergeordneten Komponenten entfernt, und es sind keine Berichtsdaten für die Einschränkung mehr für diese Komponenten verfügbar. Durch Aufheben der Zuweisung einer Beschränkung werden weder die Beschränkung noch die Kontokomponenten selbst gelöscht.

### Weisen Sie ausgewählten Anzeigengruppen in der neuen [!UICONTROL Ad Groups] eine Angebotsbegrenzung zu

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Anzeigengruppe, der Sie eine einzelne Einschränkung zuweisen.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Wählen Sie die Einschränkung aus.

1. Klicken Sie auf **[!UICONTROL Assign Now]**.

### Weisen Sie ausgewählten Suchangebotseinheiten aus den veralteten [!UICONTROL Campaigns] eine Angebotsbegrenzung zu

1. Wählen Sie in **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** die Ansicht Kontomomponente aus.

1. Aktivieren Sie das Kontrollkästchen neben jeder relevanten Zeile.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL More]** und anschließend auf **[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Wählen Sie die entsprechende Einschränkung aus.

1. (Optional) Geben Sie zusätzliche Details ein:

   1. Klicken Sie neben [!UICONTROL Additional Details] auf **[!UICONTROL Open]** , um die Details zu erweitern.

   1. Geben Sie eine optionale **[!UICONTROL Project Name]** und/oder eine optionale **[!UICONTROL Description]** ein.

1. Klicken Sie auf **[!UICONTROL Save]**.

### Entfernen von Angebotsbegrenzungen aus ausgewählten Anzeigengruppen aus der neuen [!UICONTROL Ad Groups]

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Anzeigengruppe, deren Zuweisung von Einschränkungen Sie aufheben möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Klicken Sie auf **[!UICONTROL Confirm]**.

### Entfernen Sie Angebotsbegrenzungen aus den Suchangebotseinheiten aus den alten [!UICONTROL Campaigns]

>[!NOTE]
>
>Informationen zum Löschen einer Einschränkung, sodass sie für die zukünftige Verwendung nicht mehr verfügbar ist, finden Sie unter „Löschen von Einschränkungen für Suchangebotseinheiten“ im Kapitel „Optimierungshandbuch“ zu „Bid-Einschränkungen“, das in Search, Social und Commerce verfügbar ist.

1. Wählen Sie in **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** die Ansicht Kontomomponente aus.

1. Aktivieren Sie das Kontrollkästchen neben jeder Komponente, von der Sie die Einschränkung entfernen möchten.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL More]** und anschließend auf **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Wählen Sie im Bestätigungsdialogfeld **[!UICONTROL Yes, Unassign]** aus.

## Zuweisen von Kennzeichnungsklassifizierungen zu Anzeigengruppen {#ad-group-classifications}

>[!NOTE]
>
>Beschriftungswerte werden von untergeordneten Entitäten übernommen. Geben Sie daher keine Werte für untergeordnete Entitäten ein, es sei denn, Sie möchten die übernommenen Werte überschreiben.

### Zuweisen von Klassifizierungswerten zu Anzeigengruppen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Anzeigengruppe, der Sie einen Titelwert zuweisen.

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

### Entfernen von Kennzeichnungswerten aus Anzeigengruppen

Das Entfernen eines Klassifizierungswerts entfernt die Verknüpfung mit der Kontokomponente und allen untergeordneten Komponenten. Berichtsdaten für den Classification-Wert sind für diese Komponenten nicht mehr verfügbar. Wenn Sie einen Klassifizierungswert entfernen, werden weder der Wert noch die Kontokomponenten gelöscht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Anzeigengruppe, aus der Sie einen Titelwert entfernen möchten.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem Classification-Wert, der aus den ausgewählten Entitäten entfernt werden soll.

   Um alle zugewiesenen Werte auszuwählen, klicken Sie auf **[!UICONTROL Select All]**. Um die Auswahl aller zugewiesenen Werte aufzuheben, klicken Sie auf **[!UICONTROL Deselect All]**.

1. Klicken Sie auf **[!UICONTROL Unassign Selected]**.

## Anzeigen eines Leistungsdiagramms in der [!UICONTROL Ad Groups] {#ad-group-performance-graph}

Öffnen und konfigurieren Sie ein Leistungsdiagramm mit bis zu drei Metriken insgesamt für alle Anzeigengruppen in der Ansicht für den angegebenen Datumsbereich.

### Anzeigen eines Leistungsdiagramms

1. Klicken Sie über der Datentabelle auf ![Diagramme](/help/search-social-commerce/assets/charts.png "Diagramme").

1. (Optional) Geben Sie die Währung und bis zu drei Metriken an, die in das Diagramm aufgenommen werden sollen.

### Ausblenden eines sichtbaren Leistungsdiagramms

* Klicken Sie über der Datentabelle auf ![Diagramme](/help/search-social-commerce/assets/charts.png "Diagramme").

## Verwalten von Datenansichtsberichten aus der [!UICONTROL Ad Groups] {#ad-group-reports}

Erstellen Sie einen Bericht, der die Datenzeilen für eine oder mehrere Anzeigengruppen in der [!UICONTROL Ad Groups] enthält, und laden Sie dann den Bericht als Excel-Arbeitsblattdatei für Microsoft (XLXS-Format) herunter. Der Bericht enthält alle sichtbaren Spalten in der Ansicht.

Sie können jeden generierten Bericht löschen.

Siehe auch &quot;>* [(veraltete Benutzeroberfläche) Daten aus einer Kampagnen-Management-Ansicht herunterladen](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md) und &quot;[(veraltete Benutzeroberfläche) Löschen eines Leistungsdatenberichts oder einer Bulksheet-Datei aus dem [!UICONTROL Downloads] Menü](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)&quot;.

### Erstellen eines Berichts mit den gefilterten Datenzeilen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Geben Sie die Anzeigengruppen an, deren Daten Sie herunterladen möchten:

   * Um Daten für bestimmte Anzeigengruppen herunterzuladen, aktivieren Sie die Kontrollkästchen neben den Anzeigengruppen.

   * Um Daten für alle Anzeigengruppen herunterzuladen, müssen Sie keine Kontrollkästchen aktivieren. Alle Anzeigengruppen sind standardmäßig enthalten.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ")**[!UICONTROL Reports]**.

1. Geben Sie in den [!UICONTROL Grid Reports] einen eindeutigen Berichtsnamen ein, und klicken Sie dann auf **[!UICONTROL Generate]**.

   Standardmäßig heißt die Datei „ad group_YYYYMMDD_NNNN“, wobei „NNNN“ die sequenzielle Auftragsnummer ist (z. B. „ad group_20250402_1326„).

   Die Datei wird der [!UICONTROL Recently Generated] hinzugefügt.

1. (Optional) Um die Datei nach Abschluss des Vorgangs herunterzuladen, klicken Sie ![Herunterladen](/help/search-social-commerce/assets/download.png "Herunterladen") neben dem Dateinamen.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

### Herunterladen eines abgeschlossenen Berichts

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ")**[!UICONTROL Reports]**.

1. Klicken Sie in der [!UICONTROL Recently Generated] im [!UICONTROL Grid Reports] auf ![Herunterladen](/help/search-social-commerce/assets/download.png "Herunterladen") neben dem Dateinamen.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

### Löschen eines abgeschlossenen Berichts

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ad Groups]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ")**[!UICONTROL Reports]**.

1. Klicken Sie in der [!UICONTROL Recently Generated] im [!UICONTROL Grid Reports] auf ![Löschen](/help/search-social-commerce/assets/delete-new.png "Löschen") neben dem Dateinamen.

>[!MORELIKETHIS]
>
>* [Einschränkungen für Suchangebotseinheiten verwalten](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Einschränkungszuweisungen für Kampagnen verwalten](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [Verwalten von Einschränkungszuweisungen für Schlüsselwörter](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [Einschränkungszuweisungen für Platzierungen verwalten](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [ (veraltete Benutzeroberfläche) Herunterladen von Daten aus einer Kampagnen-Management-Ansicht](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [(Alte Benutzeroberfläche) Löschen eines Leistungsdatenberichts oder einer Bulksheet-Datei aus dem [!UICONTROL Downloads] Menü](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [[!DNL Baidu] Anzeigengruppeneinstellungen](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-baidu.md)
>* [[!DNL Google Ads] Anzeigengruppeneinstellungen](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-google.md)
>* [[!DNL LY Ads] Anzeigengruppeneinstellungen](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-ly.md)
>* [[!DNL Microsoft Advertising] Anzeigengruppeneinstellungen](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-microsoft.md)
>* [[!DNL Yandex] Anzeigengruppeneinstellungen](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-yandex.md)
