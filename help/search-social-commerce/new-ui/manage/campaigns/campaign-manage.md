---
title: Verwalten von Kampagnen
description: Erfahren Sie, wie Sie Anzeigenkampagnen erstellen und verwalten.
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: fc836f17b53a3708bf881dc62a437d391709a050
workflow-type: tm+mt
source-wordcount: 2285
ht-degree: 0%

---

# Verwalten von Kampagnen

*Beta-Funktion*

Eine Kampagne ist die Hauptkomponente eines Anzeigennetzwerkkontos. Bei den meisten Kampagnentypen besteht sie aus einer Reihe von Anzeigengruppen oder Anzeigengruppen. Die Kampagneneinstellungen umfassen Kampagnenbudgetparameter, Anzeigenziele und optionale Tracking-Parameter für alle Anzeigen in der Kampagne. Tracking-Parameter auf Kampagnenebene überschreiben die Parameter auf Kontoebene, können jedoch auf niedrigerer Ebene überschrieben werden.

Sobald Sie [ein Anzeigennetzwerkkonto über eine API-Verbindung zugänglich machen](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) und Search, Social und Commerce die Kontodaten mit dem Anzeigennetzwerk synchronisiert haben, können Sie neue Kampagnen mit [unterstützten Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md) erstellen. Sie können auch den Status von Kampagnen bearbeiten und ändern.

Einzelheiten zu den für die einzelnen Werbenetzwerke verfügbaren Funktionen finden Sie unter &quot;[Unterstützte Inventarisierung](/help/search-social-commerce/introduction/supported-inventory.md).

## Über die [!UICONTROL Campaigns] {#campaign-view-about}

Die Ansicht [!UICONTROL Manage] > [!UICONTROL Campaigns] listet alle Kampagnen in der gefilterten Ansicht für das ausgewählte Advertiser-Konto auf. Sie können eine Liste der Anzeigengruppen in der Kampagne öffnen, indem Sie auf den Kampagnennamen klicken.

Während Sie Kampagnendaten in den [!UICONTROL Campaigns] hinzufügen und bearbeiten, übertragen Search, Social und Commerce die Datenänderungen sofort an das Werbenetzwerk. Search, Social und Commerce ruft außerdem die Daten zur Kampagnenstruktur ab und klickt täglich oder öfter auf Daten, wenn neue Kampagnen erkannt werden. Für alle synchronisierten Werbenetzwerke können Sie bei Bedarf auch Konten synchronisieren.

Search, Social und Commerce rufen Leistungsdaten stündlich von synchronisierten [!DNL Google Ads]- und [!DNL Microsoft Advertising]-Konten und täglich von anderen synchronisierten Anzeigennetzwerkkonten ab.

### Verfügbare Aktionen

* [Erstellen einer Kampagne](#campaign-create)

* [Umbenennen einer Kampagne innerhalb der Zeile](#campaign-rename)

* [Kampagneneinstellungen bearbeiten](#campaign-edit)

* [Ändern des Status einer Kampagne in der Zeile oder Löschen einer Kampagne](#campaign-status)

* [Zuweisen von Kampagnen zu einem Portfolio und Entfernen von Kampagnen aus einem Portfolio](#campaign-portfolio)

* [Anzeigen eines Leistungsdiagramms in der [!UICONTROL Campaigns]](#campaign-performance-graph)

* [Zuweisen von Angebotsbeschränkungen zu Kampagnen und Aufheben der Zuweisung von Beschränkungen zu Kampagnen](#campaign-constraints)

* [Zielgruppeneinschränkungen Kampagnen zuweisen und die Zuweisung von Zielgruppeneinschränkungen zu Kampagnen aufheben](#campaign-target-constraints)

* [Zuweisen von Label-Klassifizierungen zu Kampagnen und Entfernen von Label-Klassifizierungen aus Kampagnen](#campaign-classifications)

* [Verwalten von Datenansichtsberichten aus der [!UICONTROL Campaigns]](#campaign-reports)

## Erstellen einer Kampagne {#campaign-create}

>[!NOTE]
>
>* Bevor Sie eine Kampagne erstellen[ implementieren Sie Konversionsverfolgungstags ](/help/search-social-commerce/tracking/conversion-tracking-about.md) den Web-Seiten des Werbetreibenden.
>* Um eine große Anzahl von Kampagnen gleichzeitig zu erstellen, verwenden Sie<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [Campaign-Bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Klicken Sie auf **[!UICONTROL Create Campaign]**.

1. Geben Sie die Kampagneneinstellungen [Baidu](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md), [Microsoft Advertising](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md) oder [Yandex](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md) an.

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

1. Klicken Sie bei Bedarf auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten") **[!UICONTROL Edit]** und ändern Sie die Kampagneneinstellungen.

1. Klicken Sie auf **[!UICONTROL Create]**.

Je nach Anzeigennetzwerk, in dem die Kampagne erstellt wurde, müssen Sie möglicherweise verknüpfte Anzeigengruppen und Anzeigen erstellen, bevor die Kampagne an das Anzeigennetzwerk gepusht wird.

## Umbenennen einer Kampagne {#campaign-rename}

Schnelles Umbenennen einer Kampagne, ohne die vollständigen Kampagneneinstellungen zu öffnen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Halten Sie den Cursor über der Kampagnenzeile und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Rename]**.

1. Bearbeiten Sie den Namen und klicken Sie dann auf **[!UICONTROL Apply]**.

## Kampagneneinstellungen bearbeiten {#campaign-edit}

Sie können Einstellungen für einzelne Kampagnen bearbeiten. Sie können auch einige Felder für mehrere Kampagnen gleichzeitig bearbeiten, einschließlich einiger Kampagnendetails, Budgetoptionen und URL-Optionen, die für alle ausgewählten Kampagnen gelten.

>[!TIP]
>
>Sie können Daten mit auch stapelweise bearbeiten<!-- Not available in new UI as of 7/21: the [copy and paste feature](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) or--> [Campaign-Bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Halten Sie den Cursor über den Entitätsnamen und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Edit]**.

   * Aktivieren Sie das Kontrollkästchen neben der Kampagne. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie die [Baidu](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md), [LY Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md), <!-- [Meta Ads](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-meta.md), --> Kampagneneinstellungen für {](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md)}Microsoft Advertising[ oder ](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md)Yandex“.[

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

1. Klicken Sie bei Bedarf auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten") **[!UICONTROL Edit]** und ändern Sie die Kampagneneinstellungen.

1. Klicken Sie auf **[!UICONTROL Update]**.

Je nach Anzeigennetzwerk, in dem die Kampagne erstellt wurde, muss die Kampagne möglicherweise Anzeigengruppen und Anzeigen enthalten, bevor sie an das Anzeigennetzwerk gesendet wird.

## Ändern des Status einer Kampagne {#campaign-status}

Schnelles Ändern des Status einer Kampagne, ohne die vollständigen Kampagneneinstellungen zu öffnen.

Sie können jede aktive Kampagne in einem unterstützten Werbenetzwerk anhalten, um die Angebotsabgabe dafür zu deaktivieren. Sie können die Gebotsabgabe später fortsetzen, indem Sie den Status wieder in Aktiv ändern.

Sie können auch jede aktive oder angehaltene Kampagne löschen. Gelöschte Kampagnen werden aus dem Werbenetzwerk gelöscht. Sie sind weiterhin sichtbar, wenn Sie sie in den Datenfilter einbeziehen, können aber nicht geändert werden.

### Aktivieren oder Anhalten einer Kampagne

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Halten Sie den Cursor über die Kampagnenzeile und klicken Sie ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten") neben der Spalte [!UICONTROL Status].

1. Status ändern:

   * Um eine pausierte Kampagne zu aktivieren, wählen Sie **[!UICONTROL Active]** aus.

   * Um eine aktive Kampagne anzuhalten, wählen Sie **[!UICONTROL Paused]** aus.

### Löschen einer Kampagne

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Halten Sie den Cursor über der Kampagnenzeile und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Delete]**.

   * Halten Sie den Cursor über die Kampagnenzeile und klicken Sie ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten") neben der Spalte [!UICONTROL Status]. Wählen Sie **[!UICONTROL Deleted]** aus.

## Zuweisen von Kampagnen zu einem Portfolio {#campaign-portfolio}

Durch die Zuweisung einer Kampagne zu einem optimierten Portfolio können Search, Social und Commerce Gebote, Kampagnenbudgets und Bid-Strategie-Ziele für Keywords und Anzeigen in der Kampagne optimieren. Sie können einem Portfolio Kampagnen in der [!UICONTROL Campaigns]-Ansicht zuweisen, wenn Sie das Portfolio erstellen, oder indem Sie die Einstellungen eines Portfolios bearbeiten.

Nicht alle Kampagnentypen und Werbenetzwerke können optimiert werden. Sehen Sie sich eine Liste der [unterstützten Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md) an, die Sie in ein Portfolio aufnehmen können. Überprüfen Sie außerdem die [Optimierungsunterstützung für jede Kampagnenangebotstrategie](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md#optimization-by-bid-strategy).

>[!NOTE]
>
>Jede Kampagne kann nur einem Portfolio zugewiesen werden. Wenn Sie eine Kampagne, die bereits mit einem anderen Portfolio verknüpft ist, einem neuen Portfolio zuweisen, wird diese aus dem ursprünglichen Portfolio entfernt.

### Zuweisen von Kampagnen zu einem vorhandenen Portfolio über die [!UICONTROL Campaigns]

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Kampagne, die Sie einem einzelnen Portfolio zuweisen möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **+[!UICONTROL Assign]** > **[!UICONTROL Existing Portfolio]** .

1. Portfolio auswählen.

1. Klicken Sie auf **[!UICONTROL Assign Now]**.

### Zuweisen von Kampagnen zu einem neuen Portfolio über die [!UICONTROL Campaigns]

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Kampagne, für die Sie das neue Portfolio erstellen möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **+[!UICONTROL Assign]** > **[!UICONTROL New Portfolio]**.

1. Geben Sie auf dem Bildschirm [!UICONTROL Create Portfolio] die Portfolioeinstellungen an.

   Die zuvor ausgewählten Kampagnen sind der Kampagne bereits zugewiesen. Optional können Sie die Kampagnenliste für das Portfolio bearbeiten.

   Weitere Informationen zu den Portfolioeinstellungen finden Sie im Optimierungshandbuch , das bei Search, Social und Commerce verfügbar ist.

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

### Ändern von Kampagnenzuweisungen für ein Portfolio in der [!UICONTROL Portfolios]

Wenn Sie eine Kampagne aus einem Portfolio entfernen, können Search, Social und Commerce die Gebote, Kampagnenbudgets und Bid-Strategieziele für diese Kampagne nicht optimieren.

Die Aktion wird im Änderungsverlauf des Portfolios protokolliert.

Weitere Informationen zur Optimierung finden Sie im Optimierungshandbuch , das bei Search, Social und Commerce verfügbar ist.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Aktivieren Sie das Kontrollkästchen neben dem Portfolio.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]**.

1. Gehen Sie in den Portfolioeinstellungen zum Abschnitt [!UICONTROL Assign Campaigns] und ändern Sie die Kampagnenzuweisungen.

   Weitere Informationen zu den Portfolioeinstellungen finden Sie im Optimierungshandbuch , das bei Search, Social und Commerce verfügbar ist.

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

1. Überprüfen Sie die Einstellungen, nehmen Sie ggf. Änderungen vor und klicken Sie dann auf **[!UICONTROL Save]**.

## Zuweisungen von Angebotsbegrenzungen für Kampagnen verwalten {#campaign-constraints}

Jede Entität kann nur eine Einschränkung aufweisen. Beschränkungen werden von untergeordneten Entitäten übernommen, sodass Sie untergeordneten Entitäten keine Beschränkungen zuweisen müssen, es sei denn, Sie möchten die übernommenen Werte überschreiben.

Wenn Sie die Zuweisung einer Einschränkung aufheben, wird die Verknüpfung mit den Kontokomponenten und allen untergeordneten Komponenten entfernt, und es sind keine Berichtsdaten für die Einschränkung mehr für diese Komponenten verfügbar. Durch Aufheben der Zuweisung einer Beschränkung werden weder die Beschränkung noch die Kontokomponenten selbst gelöscht.

>[!NOTE]
>
>Aktive Einschränkungen beschränken die Gebotsabgabe nur für zugewiesene Gebotseinheiten in optimierten alten Portfolios auf Keyword-Ebene. Sie werden bei Gebotseinheiten ignoriert, die sich in aktiven Portfolios befinden, sich in hybriden Portfolios befinden oder nicht in Portfolios sind.

### Weisen Sie ausgewählten Kampagnen in der neuen [!UICONTROL Campaigns] eine Angebotsbegrenzung zu

Eine einzelne Einschränkung kann einer oder mehreren Kampagnen zugewiesen werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Kampagne, der Sie eine einzelne Einschränkung zuweisen.

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

### Entfernen von Angebotsbegrenzungen aus ausgewählten Kampagnen aus der neuen [!UICONTROL Campaigns]

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Kampagne, deren Zuweisung von Einschränkungen Sie aufheben möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Klicken Sie auf **[!UICONTROL Confirm]**.

### Entfernen Sie Angebotsbegrenzungen aus den Suchangebotseinheiten aus den alten [!UICONTROL Campaigns]

>[!NOTE]
>
>Informationen zum Löschen einer Einschränkung, sodass sie für die zukünftige Verwendung nicht mehr verfügbar ist, finden Sie unter „Löschen von Einschränkungen für Suchangebotseinheiten“ im Kapitel „Optimierungshandbuch“ zu „Bid-Einschränkungen“, das in Search, Social und Commerce verfügbar ist.<!-- verify convention for referencing Optimization Guide here -->

1. Wählen Sie in **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** die Ansicht Kontomomponente aus.

1. Aktivieren Sie das Kontrollkästchen neben jeder Komponente, von der Sie die Einschränkung entfernen möchten.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste über der Datentabelle auf **[!UICONTROL More]** und anschließend auf **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Wählen Sie im Bestätigungsdialogfeld **[!UICONTROL Yes, Unassign]** aus.

## Zielgruppen-Einschränkungszuweisungen für Kampagnen verwalten {#campaign-target-constraints}

### Weisen Sie ausgewählten Kampagnen in der neuen [!UICONTROL Campaigns] eine Zielgruppeneinschränkung zu

Sie können einer oder mehreren Kampagnen eine einzelne Zielgruppeneinschränkung zuweisen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Kampagne, der Sie eine einzelne Zielgruppeneinschränkung zuweisen.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **+[!UICONTROL Assign]** > **[!UICONTROL Target Constraint]**.

1. Wählen Sie die Einschränkung aus.

1. Klicken Sie auf **[!UICONTROL Assign Now]**.

### Entfernen von Zielgruppeneinschränkungen aus ausgewählten Kampagnen aus der neuen [!UICONTROL Campaigns]

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Kampagne, deren Zuweisung einer Zielgruppenbeschränkung Sie aufheben möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **-[!UICONTROL Unassign]** > **[!UICONTROL Target Constraint]**.

1. Klicken Sie auf **[!UICONTROL Confirm]**.

## Zuweisen von Kennzeichnungsklassifizierungen zu Kampagnen {#campaign-classifications}

>[!NOTE]
>
>Beschriftungswerte werden von untergeordneten Entitäten übernommen. Geben Sie daher keine Werte für untergeordnete Entitäten ein, es sei denn, Sie möchten die übernommenen Werte überschreiben.

### Zuweisen von Classification-Werten zu Kampagnen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Kampagne, der Sie einen Kennzeichnungswert zuweisen.

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

### Entfernen von Kennzeichnungswerten aus Kampagnen

Das Entfernen eines Klassifizierungswerts entfernt die Verknüpfung mit der Kontokomponente und allen untergeordneten Komponenten. Berichtsdaten für den Classification-Wert sind für diese Komponenten nicht mehr verfügbar. Wenn Sie einen Klassifizierungswert entfernen, werden weder der Wert noch die Kontokomponenten gelöscht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder Kampagne, aus der Sie einen Titelwert entfernen möchten.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem Classification-Wert, der aus den ausgewählten Entitäten entfernt werden soll.

   Um alle zugewiesenen Werte auszuwählen, klicken Sie auf **[!UICONTROL Select All]**. Um die Auswahl aller zugewiesenen Werte aufzuheben, klicken Sie auf **[!UICONTROL Deselect All]**.

1. Klicken Sie auf **[!UICONTROL Unassign Selected]**.

## Anzeigen eines Leistungsdiagramms in der [!UICONTROL Campaigns] {#campaign-performance-graph}

Öffnen und konfigurieren Sie ein Leistungsdiagramm mit bis zu drei Metriken insgesamt für alle Kampagnen in der Ansicht für den angegebenen Datumsbereich.

### Anzeigen eines Leistungsdiagramms

1. Klicken Sie über der Datentabelle auf ![Diagramme](/help/search-social-commerce/assets/charts.png "Diagramme").

1. (Optional) Geben Sie die Währung und bis zu drei Metriken an, die in das Diagramm aufgenommen werden sollen.

### Ausblenden eines sichtbaren Leistungsdiagramms

* Klicken Sie über der Datentabelle auf ![Diagramme](/help/search-social-commerce/assets/charts.png "Diagramme").

## Verwalten von Datenansichtsberichten aus der [!UICONTROL Campaigns] {#campaign-reports}

<!-- Wording??????  Filtered data reports? -->

Erstellen Sie einen Bericht, der die Datenzeilen für eine oder mehrere Kampagnen in der [!UICONTROL Campaigns] enthält, und laden Sie dann den Bericht als Excel-Arbeitsblattdatei für Microsoft (XLXS-Format) herunter. Der Bericht enthält alle sichtbaren Spalten in der Ansicht.

Sie können jeden generierten Bericht löschen.

Siehe auch &quot;>* [(veraltete Benutzeroberfläche) Daten aus einer Kampagnen-Management-Ansicht herunterladen](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md) und &quot;[(veraltete Benutzeroberfläche) Löschen eines Leistungsdatenberichts oder einer Bulksheet-Datei aus dem [!UICONTROL Downloads] Menü](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)&quot;.

### Erstellen eines Berichts mit den gefilterten Datenzeilen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Geben Sie die Kampagnen an, deren Daten Sie herunterladen möchten:

   * Um Daten für bestimmte Kampagnen herunterzuladen, aktivieren Sie die Kontrollkästchen neben den Kampagnen.

   * Um Daten für alle Kampagnen herunterzuladen, müssen Sie keine Kontrollkästchen aktivieren. Alle Kampagnen sind standardmäßig enthalten.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ")**[!UICONTROL Reports]**.

1. Geben Sie in den [!UICONTROL Grid Reports] einen eindeutigen Berichtsnamen ein, und klicken Sie dann auf **[!UICONTROL Generate]**.

   Standardmäßig heißt die Datei „campaign_YYYYMMDD_NNNN“, wobei „NNNN“ die sequenzielle Auftragsnummer ist (z. B. „campaign_20250402_1326„).

   Die Datei wird der [!UICONTROL Recently Generated] hinzugefügt.

1. (Optional) Um die Datei nach Abschluss des Vorgangs herunterzuladen, klicken Sie ![Herunterladen](/help/search-social-commerce/assets/download.png "Herunterladen") neben dem Dateinamen.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

### Herunterladen eines abgeschlossenen Berichts

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ")**[!UICONTROL Reports]**.

1. Klicken Sie in der [!UICONTROL Recently Generated] im [!UICONTROL Grid Reports] auf ![Herunterladen](/help/search-social-commerce/assets/download.png "Herunterladen") neben dem Dateinamen.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

### Löschen eines abgeschlossenen Berichts

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ")**[!UICONTROL Reports]**.

1. Klicken Sie in der [!UICONTROL Recently Generated] im [!UICONTROL Grid Reports] auf ![Löschen](/help/search-social-commerce/assets/delete-new.png "Löschen") neben dem Dateinamen.

>[!MORELIKETHIS]
>
>* [Einschränkungen für Suchangebotseinheiten verwalten](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Einschränkungszuweisungen für Anzeigengruppen verwalten](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [Verwalten von Einschränkungszuweisungen für Schlüsselwörter](/help/search-social-commerce/new-ui/target/keywords/keyword-constraint-assignments-manage.md)
>* [Einschränkungszuweisungen für Platzierungen verwalten](/help/search-social-commerce/new-ui/target/placements/placement-constraint-assignments-manage.md)
>* [ (veraltete Benutzeroberfläche) Herunterladen von Daten aus einer Kampagnen-Management-Ansicht](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)
>* [(Alte Benutzeroberfläche) Löschen eines Leistungsdatenberichts oder einer Bulksheet-Datei aus dem [!UICONTROL Downloads] Menü](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
>* [[!DNL Baidu] Kampagneneinstellungen](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-baidu.md)
>* [[!DNL Google Ads] Kampagneneinstellungen](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-google.md)
>* [[!DNL LY Ads] Kampagneneinstellungen](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-ly.md)
>* [[!DNL Microsoft Advertising] Kampagneneinstellungen](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-microsoft.md)
>* [[!DNL Yandex] Kampagneneinstellungen](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-yandex.md)

<!-- >* [[!DNL Meta Ads] campaign settings](/help/search-social-commerce/new-ui/manage/campaigns/campaign-settings-meta.md) -->

