---
title: Platzierungen verwalten
description: Erfahren Sie, wie Sie Google Ads-Platzierungen und negative Platzierungen erstellen und verwalten und Platzierungen Begrenzungen zuweisen.
feature: Search Optimization, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: d3e38179ae119f35c184bee398edaaf456fab563
workflow-type: tm+mt
source-wordcount: '1390'
ht-degree: 0%
---
# Platzierungen verwalten

*Beta-Funktion*

Nur *[!DNL Google Ads]Konten*

Platzierungen sind Orte im Display-Netzwerk, an denen Ihre Anzeigen erscheinen können. Die Platzierungseinstellungen umfassen das maximale Angebot und optionale Tracking-Parameter. Einstellungen auf Platzierungsebene setzen die Anzeigengruppen- oder Kampagneneinstellungen außer Kraft. Negative Platzierungen verhindern, dass Anzeigen auf bestimmten Sites angezeigt werden.

Sobald Sie [ein Anzeigennetzwerkkonto über eine API-Verbindung zugänglich machen](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md) und Search, Social und Commerce die Kontodaten mit dem Anzeigennetzwerk synchronisiert haben, können Sie Platzierungen für Anzeigengruppen in [unterstützten Kampagnentypen](/help/search-social-commerce/introduction/supported-inventory.md) erstellen, die auf das Anzeigennetzwerk abzielen. Sie können auch den Status von Platzierungen bearbeiten und ändern und negative Platzierungen erstellen und löschen.

>[!NOTE]
>
>[!DNL Google Ads] bietet keine Leistungsdaten auf Anzeigenebene für Platzierungen.

## Über die [!UICONTROL Placements] {#placement-view-about}

Die Ansicht [!UICONTROL Targeting] > [!UICONTROL Placements] enthält zwei Registerkarten für das ausgewählte Advertiser-Konto:

* Auf der Registerkarte [!UICONTROL Placements] werden alle Platzierungen mit Geboten in der gefilterten Ansicht aufgelistet.

* Auf der Registerkarte [!UICONTROL Negatives] werden alle negativen Platzierungen in der gefilterten Ansicht aufgelistet.

Zum Anzeigen der Seite ist die Berechtigung [!UICONTROL View Placements] erforderlich. Das Erstellen von Platzierungen oder negativen Platzierungen, das Bearbeiten von Platzierungen, das Ändern des Platzierungsstatus und das Löschen von Platzierungen oder negativen Platzierungen erfordert die Berechtigung [!UICONTROL Edit Placements] .

### Verfügbare Aktionen

* [Erstellen von Platzierungen](#placement-create)

* [Erstellen negativer Platzierungen](#placement-negative-create)

* [Platzierungseinstellungen bearbeiten](#placement-edit)

* [Status von Platzierungen und negativen Platzierungen ändern oder löschen](#placement-status)

* [Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren](#copy-to-clipboard)

* [Zuweisen von Einschränkungen zu Platzierungen und Aufheben der Zuweisung von Einschränkungen zu Platzierungen](#placement-constraints)

* [Zuweisen von Label-Klassifizierungen zu Platzierungen](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)

## Erstellen von Platzierungen {#placement-create}

>[!TIP]
>
>Um eine große Anzahl von Platzierungen gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Placements]** auf **[!UICONTROL Create Placement]**.

1. Wählen Sie im **[!UICONTROL Basic Settings]** Schritt das Netzwerk, das Konto, die Kampagne und die Anzeigengruppe aus.

1. Geben Sie die [Platzierungseinstellungen](#placement-create-settings) ein.

   Um mehrere Platzierungen zu erstellen, trennen Sie die Website-URLs durch Kommas.

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

1. Überprüfen Sie die Einstellungen. Um Einstellungen zu ändern, klicken Sie auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten") **[!UICONTROL Edit]** im entsprechenden Abschnitt und ändern Sie die Einstellungen.

1. Klicken Sie auf **[!UICONTROL Create]**.

## Erstellen negativer Platzierungen {#placement-negative-create}

Sie können negative Platzierungen für eine [!DNL Google Ads] Kampagne oder Anzeigengruppe erstellen, die auf das Anzeigennetzwerk ausgerichtet ist.

>[!NOTE]
>
>Sie können auch negative Platzierungen in den [Anzeigengruppeneinstellungen](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md) und [Kampagneneinstellungen](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md) erstellen und bearbeiten.

>[!TIP]
>
>Um eine große Anzahl negativer Platzierungen gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Negatives]** auf **[!UICONTROL Create Negative]** und dann entweder **[!UICONTROL Campaign Negative]** oder **[!UICONTROL Ad Group Negative]**.

1. Wählen Sie im **[!UICONTROL Basic Settings]** Schritt das Netzwerk, das Konto, die Kampagne und (bei negativen Platzierungen auf Anzeigengruppenebene) die Anzeigengruppe aus.

1. Geben Sie im **[!UICONTROL Manage Websites]** Schritt die negativen Website-URLs ein, z. B. `www.example.com` oder `example.com/shoes`.

   Trennen Sie mehrere URLs durch Kommas. Dieses Formular akzeptiert Website-URLs, keine Themen- oder Kategoriezeichenfolgen.

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

1. Überprüfen Sie die Einstellungen. Um Einstellungen zu ändern, klicken Sie auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten") **[!UICONTROL Edit]** im entsprechenden Abschnitt und ändern Sie die Einstellungen.

1. Klicken Sie auf **[!UICONTROL Create]**.

## Platzierungseinstellungen bearbeiten {#placement-edit}

Sie können den Status, das Angebot, die Basis-URL und die Tracking-Vorlage für eine oder mehrere Platzierungen bearbeiten. Sie können die Ziel-Website-URL nicht ändern und auch keine gelöschten Platzierungen bearbeiten.

>[!TIP]
>
>Um eine große Menge an Platzierungsdaten gleichzeitig zu bearbeiten, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Aktivieren Sie auf der Registerkarte **[!UICONTROL Placements]** das Kontrollkästchen neben jeder zu bearbeitenden Platzierung.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie im Bedienfeld **[!UICONTROL Edit Placements]** die [Platzierungseinstellungen](#placement-edit-settings).

   Bei mehreren Platzierungen werden Ihre Änderungen auf alle ausgewählten Platzierungen angewendet. Sie können Gebote auf einen bestimmten Wert setzen oder sie um einen bestimmten Prozentsatz oder Geldbetrag mit einer Grenze erhöhen oder verringern. Bei URLs können Sie den vorhandenen Wert ersetzen, Text suchen und ersetzen, ein Präfix hinzufügen oder ein Suffix anhängen.

   Die Angebotsbearbeitung ist deaktiviert, wenn die ausgewählten Platzierungen mehrere Währungen verwenden.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Status von Platzierungen und negativen Platzierungen ändern {#placement-status}

Sie können eine aktive, bidable Platzierung anhalten, um ein bidding dafür zu deaktivieren. Sie können die Gebotsabgabe später fortsetzen, indem Sie den Status wieder in Aktiv ändern.

Sie können auch aktive oder angehaltene Platzierungen oder negative Platzierungen löschen. Gelöschte Platzierungen werden aus dem Werbenetzwerk gelöscht. Sie sind weiterhin sichtbar, wenn Sie sie in den Datenfilter einbeziehen, können aber nicht geändert werden.

### Aktivieren oder Anhalten von Platzierungen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Filtern Sie auf der Registerkarte **[!UICONTROL Placements]** optional die Liste und aktivieren Sie dann das Kontrollkästchen neben jeder Platzierung, deren Status Sie ändern möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]**.

1. Ändern Sie im Abschnitt **[!UICONTROL Placement Details]** die **[!UICONTROL Status]**:

   * Um pausierte Platzierungen zu aktivieren, wählen Sie **[!UICONTROL Active]** aus.

   * Um aktive Platzierungen anzuhalten, wählen Sie **[!UICONTROL Paused]** aus.

1. Klicken Sie auf **[!UICONTROL Save]**.

### Platzierungen oder negative Platzierungen löschen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Filtern Sie auf der Registerkarte **[!UICONTROL Placements]** oder **[!UICONTROL Negatives]** optional die Liste und aktivieren Sie dann das Kontrollkästchen neben jeder zu löschenden Platzierung oder negativen Platzierung.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

## Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren {#copy-to-clipboard}

Kopieren Sie die sichtbaren Informationen in die ausgewählten Zeilen entsprechend den angewendeten Filtern und Spalten, die in der Ansicht sichtbar sind. Die Informationen werden als tabulatorgetrennte Werte (TSV) gespeichert.

1. Aktivieren Sie das Kontrollkästchen neben jeder Zeile, deren Daten Sie kopieren möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Copy]**.

## Einschränkungszuweisungen für Platzierungen verwalten {#placement-constraints}

Sie können Gebotsbeschränkungen für Kampagnen, Anzeigengruppen, Keywords, Platzierungen, Produktgruppen auf Einheitenebene und dynamische Suchziele zuweisen und entfernen. Jede Entität kann nur eine Einschränkung aufweisen.

Beschränkungen werden von untergeordneten Entitäten übernommen, sodass Sie untergeordneten Entitäten keine Beschränkungen zuweisen müssen, es sei denn, Sie möchten die übernommenen Werte überschreiben.

Wenn Sie die Zuweisung einer Einschränkung aufheben, wird die Verknüpfung mit den Kontokomponenten und allen untergeordneten Komponenten entfernt, und es sind keine Berichtsdaten für die Einschränkung mehr für diese Komponenten verfügbar. Beim Aufheben der Zuweisung einer Einschränkung werden die Einschränkung oder die Kontokomponenten selbst nicht gelöscht.

>[!NOTE]
>
>* Wenn Sie später ein Keyword oder die Anzeigenkopie für eine nicht veränderliche Anzeige bearbeiten und so ein neues Keyword oder eine neue Anzeige erstellen, wird die Begrenzung nicht der neuen Entität zugewiesen.
>* Aktive Einschränkungen beschränken die Gebotsabgabe nur für zugewiesene Gebotseinheiten in optimierten alten Portfolios auf Keyword-Ebene. Sie werden bei Gebotseinheiten ignoriert, die sich in aktiven Portfolios befinden, sich in hybriden Portfolios befinden oder nicht in Portfolios sind.

### Platzierungen eine Begrenzung zuweisen {#placement-constraint-assign}

Sie können einer oder mehreren Platzierungen eine einzelne Begrenzung zuweisen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Aktivieren Sie auf der Registerkarte **[!UICONTROL Placements]** das Kontrollkästchen neben jeder Platzierung, der Sie eine einzelne Begrenzung zuweisen.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Assign]>[!UICONTROL Bid Constraint]**.

1. Wählen Sie die Einschränkung aus.

1. Klicken Sie auf **[!UICONTROL Assign Now]**.

### Zuweisung von Einschränkungen zu Platzierungen aufheben {#placement-constraint-unassign}

Durch Aufheben der Zuweisung einer Einschränkung wird sie nicht gelöscht. Informationen zum Löschen einer Einschränkung, sodass sie für die zukünftige Verwendung nicht mehr verfügbar ist, finden Sie unter [Verwalten von Einschränkungen für Suchangebotseinheiten](/help/search-social-commerce/new-ui/goals/constraints-manage.md#constraint-change-status).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. Aktivieren Sie auf der Registerkarte **[!UICONTROL Placements]** das Kontrollkästchen neben jeder Platzierung, deren Zuweisung von Einschränkungen Sie aufheben möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Unassign]>[!UICONTROL Bid Constraint]**.

1. Klicken Sie auf **[!UICONTROL Confirm]**.

## Platzierungseinstellungen {#placement-settings}

### Einstellungen beim Erstellen von Platzierungen {#placement-create-settings}

#### [!UICONTROL Basic Settings]

**[!UICONTROL Network]:** Das Werbenetzwerk. Es wird nur [!DNL Google Ads] unterstützt.

**[!UICONTROL Account]:** Das Netzwerkkonto der Anzeige.

**[!UICONTROL Campaign]:** Die Kampagne.

**[!UICONTROL Ad Group]:** Die Anzeigengruppe.

#### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** Websites im Display-Netzwerk, auf denen Ihre Anzeige erscheinen kann. Geben Sie eine gültige Website-URL ein, z. B. `www.example.com`, `example.com` oder `example.com/shoes`. Trennen Sie mehrere URLs durch Kommas. Die URL darf kein Fragezeichen enthalten (`?`).

Um stattdessen Websites auszuschließen, wählen Sie [Erstellen negativer Platzierungen](#placement-negative-create) auf der Registerkarte [!UICONTROL Targeting] > [!UICONTROL Placements] > [!UICONTROL Negatives] oder verwenden Sie die Anzeigengruppen- und Kampagneneinstellungen.

**[!UICONTROL Status]:** Der Anzeigestatus der Platzierung: *[!UICONTROL Active]* (um Gebote zu aktivieren) oder *[!UICONTROL Paused]* (um Gebote zu deaktivieren).

#### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (Optional) Die maximalen Kosten pro Klick (CPC) oder Kosten pro Tausend sichtbarer Impressionen (vCPM) für die platzierungsbasierte Anzeige, abhängig von der Bid-Strategie der Kampagne. Dieser Wert überschreibt das Angebot auf Anzeigengruppenebene.

#### [!UICONTROL Tracking URLs]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/base-url-google-note.md}}

{{$include /help/_includes/tracking-template-google.md}}

>[!NOTE]
>
>Das Formular zur Erstellung der neuen Benutzeroberfläche erfordert, dass die Basis-URL und die Tracking-Vorlage, falls angegeben, mit `http://` oder `https://` beginnen.

### Einstellungen beim Bearbeiten von Platzierungen {#placement-edit-settings}

Das Bedienfeld [!UICONTROL Edit Placements] unterstützt die folgenden Einstellungen für eine oder mehrere ausgewählte Platzierungen. Die URL der Zielwebsite kann nicht geändert werden.

#### [!UICONTROL Placement Details]

**[!UICONTROL Status]:** *[!UICONTROL Active]* oder *[!UICONTROL Paused]*.

#### [!UICONTROL Bid Details]

**[!UICONTROL Bid adjustment]:** Ändern des Angebots:

* *[!UICONTROL Set to]:* Ersetzen Sie das vorhandene Angebot durch einen angegebenen Wert.

* *[!UICONTROL Increase]:* Erhöhen Sie das bestehende Angebot um einen bestimmten Betrag oder Prozentsatz.

* *[!UICONTROL Decrease]:* Verringert das bestehende Angebot um einen bestimmten Betrag oder Prozentsatz.

**[!UICONTROL Modifier type]:** (bei Erhöhungen oder Verringerungen) Ob die Anpassung *[!UICONTROL Currency]* oder *[!UICONTROL Percentage]* verwendet.

**[!UICONTROL Set value]:** Das neue Gebot oder der Anpassungsbetrag. Der Mindestwert ist 0,01.

**[!UICONTROL Max limit]:** (Bei Erhöhungen oder Verringerungen; optional) Die Obergrenze für das angepasste Gebot. Bei einer Erhöhung ist dies das Höchstgebot; bei einer Verringerung ist dies das Mindestgebot. Der Mindestgrenzwert ist 0,01.

Die Angebotsbearbeitung ist deaktiviert, wenn die ausgewählten Platzierungen mehrere Währungen verwenden.

#### [!UICONTROL Tracking Urls]

**[!UICONTROL Base Url]**, **[!UICONTROL Tracking Template]:** Wählen Sie für jedes Feld aus, wie der Wert geändert werden soll:

* *[!UICONTROL Set To]:* Ersetzen Sie den Wert. Geben Sie eine gültige Website-URL ein, die mit `http://` oder `https://` beginnt.

* *[!UICONTROL Find/Replace]:* Angegebenen Text im Wert ersetzen. Geben Sie den zu suchenden Text und den Ersatztext ein.

* *[!UICONTROL Add Suffix]:* Hängen Sie den Text an den Wert an. Geben Sie den Suffix-Text ein.

* *[!UICONTROL Add Prefix]:* Fügen Sie Text am Anfang des Werts hinzu. Geben Sie den Präfixtext ein.

>[!NOTE]
>
>Alle neuen Basis-URLs müssen gültige URLs sein, die mit `http://` oder `https://` beginnen.

>[!MORELIKETHIS]
>
>* [Einschränkungen für Suchangebotseinheiten verwalten](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Verwalten von Kennzeichnungsklassifizierungen](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
