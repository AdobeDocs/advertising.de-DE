---
title: Verwalten [!DNL Google Ads] dynamischen Suchziele
description: Erfahren Sie, wie Sie [!DNL Google Ads] dynamische Suchziele erstellen und verwalten.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: f907f445c70ce64368dfa7e77d4cd1900ecc7113
workflow-type: tm+mt
source-wordcount: '1504'
ht-degree: 0%
---
# Verwalten [!DNL Google Ads] dynamischen Suchziele

Nur *[!DNL Google Ads]Konten*

Sie können den Status dynamischer Suchziele für [!DNL Google Ads] Kampagnen, die das Suchnetzwerk verwenden, erstellen, bearbeiten und ändern.

## Was sind dynamische Suchziele?

Dynamische Suchziele definieren, ob das Anzeigennetzwerk alle Seiten oder eine Teilmenge der Seiten auf Ihrer Website verwendet, um Ihre dynamischen Suchanzeigen anzusprechen. Konfigurieren Sie dynamische Suchziele auf Anzeigengruppenebene; sie gelten für alle dynamischen Suchanzeigen in derselben Anzeigengruppe.

Abhängig von Ihren Kampagneneinstellungen können dynamische Suchziele erforderlich oder optional sein:

* Wenn Sie im Abschnitt &quot;[!UICONTROL DSA Options]&quot; der Kampagne keine Website-Domain und Sprache angeben, müssen Sie dynamische Suchziele erstellen.

* Optional können Sie dynamische Suchziele erstellen, wenn Sie eine Website-Domain und eine Sprache im Abschnitt &quot;[!UICONTROL DSA Options]&quot; der Kampagne angeben.

  [!DNL Google Ads] zeigt Ihre dynamischen Suchanzeigen automatisch basierend auf dem Inhalt einer Website an, die mit diesen Einstellungen festgelegt wurde.

Um die Leistung optimal zu verfolgen, konfigurieren Sie Ihre Kampagne mit einer Anzeigengruppe pro dynamischem Suchziel und schließen Sie eine Anzeigengruppe ein, die alle Kriterien berücksichtigt.

Weitere Informationen zu [!DNL Google Ads] dynamischen Suchanzeigen finden Sie unter https://support.google.com/google-ads/answer/2471185.

## Die [!UICONTROL Auto Targets] {#auto-target-view-about}

Die Ansicht [!UICONTROL Targeting] > [!UICONTROL Auto Targets] listet alle dynamischen Suchziele in der gefilterten Ansicht für das ausgewählte Advertiser-Konto auf. Sie können auch Ihre dynamischen Suchziele verwalten.

Zum Anzeigen der Daten ist die Berechtigung [!UICONTROL View Auto Targets] erforderlich. Das Erstellen von Zielen und das Bearbeiten ihrer Gebote oder ihres Status erfordert die Berechtigung [!UICONTROL Edit Auto Targets] .

### Verfügbare Aktionen

* [Erstellen einer dynamischen Suchzielgruppe](#auto-target-create)

* [Bearbeiten der Einstellungen für dynamische Suchziele](#auto-target-edit)

* [Ändern des Status von dynamischen Suchzielen oder Löschen von dynamischen Suchzielen](#auto-target-status)

* [Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren](#copy-to-clipboard)

* [Einschränkungen zuweisen](#constraint-assign) zu dynamischen Suchzielen und [Einschränkungen entfernen](#constraint-unassign) aus dynamischen Suchzielen

* [Kennzeichnungsklassifizierungen zuweisen](#classification-values-assign) zu dynamischen Suchzielen und [Kennzeichnungsklassifizierungen entfernen](#classification-values-remove) aus dynamischen Suchzielen

>[!NOTE]
>
>Sie können große Mengen an Zieldaten (einschließlich Kennzeichnungen und Einschränkungszuweisungen) gleichzeitig erstellen und bearbeiten, indem Sie [Bulksheet-Dateien](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) hochladen und im Werbenetzwerk posten.

## Erstellen eines [!DNL Google Ads] dynamischen Suchziels {#auto-target-create}

Sie können dynamische Suchziele erstellen, um Seiten in Ihren Websites zu definieren (d. h. die Domains, die in den Display-URLs Ihrer Anzeigen verwendet werden), deren Inhalt zum Targeting Ihrer dynamischen Suchanzeigen in derselben Anzeigengruppe verwendet wird.

Sie können alle indizierten Seiten als Ziel auswählen oder bis zu drei Kriterien angeben.

>[!NOTE]
>
>Um die Leistung optimal zu verfolgen, erstellen Sie eine Zielgruppe mit der Option [!UICONTROL All] für nur eine Anzeigengruppe pro Kampagne.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create Auto Target]**.

1. Wählen Sie **[!UICONTROL Basic Settings]** das Werbenetzwerk, das Konto, die Kampagne und die Anzeigengruppe aus.

1. Geben Sie die verbleibenden [Einstellungen für dynamische Suchziele](#auto-target-create-settings) an.

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

1. Überprüfen Sie die Einstellungen. Um Einstellungen zu ändern, klicken Sie auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten") **[!UICONTROL Edit]** im entsprechenden Abschnitt und ändern Sie die Einstellungen.

1. Klicken Sie auf **[!UICONTROL Create]**.

## Bearbeiten [!DNL Google Ads] Einstellungen für dynamische Suchziele {#auto-target-edit}

Sie können den Status oder das maximale Angebot für ein oder mehrere dynamische Suchziele bearbeiten. Die Kriterien für die Zielgruppe können nicht geändert werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder zu bearbeitenden Zeile.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie im Bedienfeld **[!UICONTROL Edit Auto Targets]** die [Status- und Bid-Einstellungen](#auto-target-edit-settings).

   Ihre Änderungen werden auf alle ausgewählten Ziele angewendet. Einstellungen, die Sie nicht ändern, behalten ihre vorhandenen Werte bei.

   Wenn die ausgewählten Ziele mehrere Währungen verwenden, ist die Angebotsbearbeitung deaktiviert. Sie können weiterhin ihren Status ändern.

1. Klicken Sie auf **[!UICONTROL Save]**.

Sie können das Angebot einer einzelnen Zielgruppe auch direkt in der Datentabelle bearbeiten, indem Sie auf den entsprechenden Bid-Wert klicken.

## Status von dynamischen Suchzielen ändern oder [!DNL Google Ads] löschen {#auto-target-status}

Sie können ein aktives dynamisches Suchziel anhalten, um es nicht mehr für dynamische Suchanzeigen in derselben Anzeigengruppe zu verwenden. Sie können die Verwendung der Zielgruppe später fortsetzen, indem Sie deren Status wieder in Aktiv ändern. Sie können auch dynamische Suchziele löschen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. (Optional) Filtern Sie die Liste, um bestimmte dynamische Suchziele einzuschließen.

1. Führen Sie einen der folgenden Schritte aus:

   * Um den Status einer Zielgruppe zu ändern, klicken Sie auf ihren Wert in der Spalte **[!UICONTROL Status]** und wählen Sie **[!UICONTROL Active]** oder **[!UICONTROL Paused]** aus.

   * Um den Status mehrerer Ziele zu ändern, aktivieren Sie das Kontrollkästchen neben den einzelnen Zielen, klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]**, wählen Sie die **[!UICONTROL Status]** im **[!UICONTROL Edit Auto Targets]** aus und klicken Sie dann auf **[!UICONTROL Save]**.

   * Um ein oder mehrere Ziele zu löschen, aktivieren Sie das Kontrollkästchen neben den einzelnen Zielen, klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL ...]>[!UICONTROL Delete]** und klicken Sie dann in der Bestätigungsmeldung auf **[!UICONTROL Confirm]** .

## Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren {#copy-to-clipboard}

Kopieren Sie die sichtbaren Informationen in die ausgewählten Zeilen entsprechend den angewendeten Filtern und Spalten, die in der Ansicht sichtbar sind. Die Informationen werden als tabulatorgetrennte Werte (TSV) gespeichert.

1. Aktivieren Sie das Kontrollkästchen neben jeder Zeile, deren Daten Sie kopieren möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Copy]**.

## Einschränkungszuweisungen für dynamische Suchziele verwalten {#constraints}

### Zuweisen einer Einschränkung zu dynamischen Suchzielen {#constraint-assign}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem dynamischen Suchziel, dem Sie eine einzelne Einschränkung zuweisen.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **+[!UICONTROL Assign]** > **[!UICONTROL Bid Constraint]**.

1. Wählen Sie die Einschränkung aus.

1. Klicken Sie auf **[!UICONTROL Assign Now]**.

### Entfernen von Einschränkungen aus ausgewählten dynamischen Suchzielen {#constraint-unassign}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder dynamischen Suchzielgruppe, deren Zuweisung von Einschränkungen Sie aufheben möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **-[!UICONTROL Unassign]** > **[!UICONTROL Bid Constraint]**.

1. Klicken Sie auf **[!UICONTROL Confirm]**.

## Verwalten von Klassifizierungswerten für dynamische Suchziele {#classification-values}

### Zuweisen von Klassifizierungswerten zu dynamischen Suchzielen {#classification-values-assign}

>[!NOTE]
>
>Beschriftungswerte werden von untergeordneten Entitäten übernommen. Geben Sie daher keine Werte für dynamische Suchziele ein, es sei denn, Sie möchten die übernommenen Werte überschreiben.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem Ziel der dynamischen Suche, dem Sie einen Titelwert zuweisen werden.

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

### Entfernen von Kennzeichnungswerten aus dynamischen Suchzielen {#classification-values-remove}

Das Entfernen eines Klassifizierungswerts entfernt die Verknüpfung mit der Kontokomponente und allen untergeordneten Komponenten. Berichtsdaten für den Classification-Wert sind für diese Komponenten nicht mehr verfügbar. Wenn Sie einen Klassifizierungswert entfernen, werden weder der Wert noch die Kontokomponenten gelöscht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Aktivieren Sie das Kontrollkästchen neben den einzelnen dynamischen Suchzielen, aus denen Sie einen Titelwert entfernen möchten.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem Classification-Wert, der aus den ausgewählten Entitäten entfernt werden soll.

   Um alle zugewiesenen Werte auszuwählen, klicken Sie auf **[!UICONTROL Select All]**. Um die Auswahl aller zugewiesenen Werte aufzuheben, klicken Sie auf **[!UICONTROL Deselect All]**.

1. Klicken Sie auf **[!UICONTROL Unassign Selected]**.

## Einstellungen für dynamische Suche [!DNL Google Ads] {#dynamic-search-target-settings}

### Bei der Erstellung verfügbare Einstellungen {#auto-target-create-settings}

#### [!UICONTROL Auto Target Details]

**Automatisches Targeting** Die indizierten Seiten, deren Inhalt zum Targeting der dynamischen Suchanzeigen in der Anzeigengruppe verwendet wird:

* *[!UICONTROL All]* (Standard): Targeting aller indizierten Seiten.

* *[!UICONTROL Specific]:* Targeting von Seiten, die bis zu drei Kriterien entsprechen. Wählen Sie ein Kriterium aus und geben Sie seinen Wert ein. Um ein weiteres Kriterium hinzuzufügen, klicken Sie auf **[!UICONTROL And]**. Die Kriterien sind mit UND kombiniert, sodass eine Seite allen angegebenen Kriterien entsprechen muss. Klicken Sie auf **[!UICONTROL Reset]** , um die Kriterien zu löschen.

  * *[!UICONTROL Category]:* Die [!DNL Google Ads] Inhaltskategorie der Seite entspricht dem angegebenen Wert. Geben Sie einen Wert ein.

  * *[!UICONTROL URL]:* Die URL der Seite enthält den angegebenen Wert, z. B. `shoes.example.com`. Geben Sie eine gültige URL ein.

  * *[!UICONTROL Page Title]:* Der Seitentitel enthält den angegebenen Text. Geben Sie einen Wert ein.

  * *[!UICONTROL Page Content]:* Der Seiteninhalt enthält den angegebenen Text. Geben Sie einen Wert ein.

Die Zielkriterien können nach der Erstellung der Zielgruppe nicht mehr geändert werden.

**[!UICONTROL Status]:** Der Status der Zielgruppe:

* *[!UICONTROL Active]* (Standard): Aktiviert die Gebotsabgabe.

* *[!UICONTROL Paused]:* Deaktiviert Gebote.

**[!UICONTROL Bid]:** Die maximalen Kosten pro Klick (CPC) für das Ziel. Dieser Wert überschreibt das Angebot auf Anzeigengruppenebene. Das Feld ist optional. Wenn Sie ein Gebot eingeben, beträgt der Mindestwert in der Kontowährung 0,01.

>[!NOTE]
>
>Wenn sich das Ziel in einem optimierten Portfolio befindet, wird das angegebene CPC-Angebot einen Tag lang angewendet. Anschließend platziert die Optimierungsfunktion Angebote gemäß ihren eigenen Berechnungen.

### Beim Bearbeiten verfügbare Einstellungen {#auto-target-edit-settings}

#### [!UICONTROL Auto Target Details]

**[!UICONTROL Status]:** Wählen Sie **[!UICONTROL Active]** oder **[!UICONTROL Paused]** aus.

#### [!UICONTROL Bid details]

Die Angebotsbearbeitung ist deaktiviert, wenn die ausgewählten Ziele mehrere Währungen verwenden.

**[!UICONTROL Bid adjustment]:** Ändern der Höchstgebote:

* *[!UICONTROL Set to]:* Ersetzen Sie jedes Angebot durch den Betrag in [!UICONTROL Set value].

* *[!UICONTROL Increase]:* Erhöhen Sie jedes Gebot um den Betrag oder Prozentsatz in [!UICONTROL Set value].

* *[!UICONTROL Decrease]:* jedes Gebot um den Betrag oder Prozentsatz in [!UICONTROL Set value].

**[!UICONTROL Modifier type]:** (Für [!UICONTROL Increase] und [!UICONTROL Decrease]) Wählen Sie **[!UICONTROL Currency]** oder **[!UICONTROL Percentage]**.

**[!UICONTROL Set value]:** Das neue Gebot oder der Betrag oder Prozentsatz, um den jedes Gebot geändert werden soll. Der Mindestwert ist 0,01.

**[!UICONTROL Max limit]:** (optional; für [!UICONTROL Increase] und [!UICONTROL Decrease]) Ein Limit in der Kontowährung. Bei einer Erhöhung ist dies das maximal resultierende Gebot. Bei einem Rückgang ist dies das Minimum des resultierenden Angebots. Wenn Sie eine Grenze eingeben, ist der Mindestwert 0,01.

>[!MORELIKETHIS]
>
>* [(Neue Benutzeroberfläche) Verwalten von Einschränkungen für Suchangebotseinheiten](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [(Neue Benutzeroberfläche) Verwalten von Kennzeichnungsklassifizierungen](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
