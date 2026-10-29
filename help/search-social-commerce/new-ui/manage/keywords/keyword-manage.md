---
title: Schlüsselwörter verwalten
description: Erfahren Sie, wie Sie angebotfähige und negative Keywords erstellen und verwalten und Keywords Einschränkungen zuweisen.
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
source-git-commit: d3e38179ae119f35c184bee398edaaf456fab563
workflow-type: tm+mt
source-wordcount: '1282'
ht-degree: 0%
---
# Schlüsselwörter verwalten

*Beta-Funktion*

Nur *[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising], [!DNL Yandex] und bestehende [!DNL Baidu] Konten*

Ein Keyword ist ein Wort oder eine Phrase, das bzw. die mit einer Anzeige verbunden ist. Die Einstellungen für Keywords umfassen den Typ der Keyword-Übereinstimmung, die maximalen Gebote, die verwendet werden sollen, wenn Ihre Anzeige durch das Keyword ausgelöst wird, und (für einige Anzeigennetzwerke) optionale Tracking-Parameter. Einstellungen auf Keyword-Ebene setzen die Anzeigengruppen- oder Kampagneneinstellungen außer Kraft. Negative Keywords verhindern, dass Anzeigen für übereinstimmende Suchen angezeigt werden.

Sobald Sie [ein Anzeigennetzwerkkonto über eine API-Verbindung zugänglich machen](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md) und Search, Social und Commerce die Kontodaten mit dem Anzeigennetzwerk synchronisiert haben, können Sie in &quot;[ Kampagnentypen“ Schlüsselwörter für Suchanzeigengruppen ](/help/search-social-commerce/introduction/supported-inventory.md). Sie können auch den Status von Keywords bearbeiten und ändern und negative Keywords erstellen und löschen.

Einzelheiten zu den für die einzelnen Werbenetzwerke verfügbaren Funktionen finden Sie unter &quot;[Unterstützte Inventarisierung](/help/search-social-commerce/introduction/supported-inventory.md).

## Über die [!UICONTROL Keywords] {#keyword-view-about}

Die Ansicht [!UICONTROL Manage] > [!UICONTROL Keywords] enthält zwei Registerkarten für das ausgewählte Advertiser-Konto:

* Auf der Registerkarte [!UICONTROL Keywords] werden alle bidable-Schlüsselwörter in der gefilterten Ansicht aufgelistet.

* Die Registerkarte [!UICONTROL Negatives] listet alle negativen Keywords in der gefilterten Ansicht auf.

### Verfügbare Aktionen

* [Schlüsselwörter erstellen](#keyword-create)

* [Negative Keywords erstellen](#keyword-negative-create)

* [Keyword-Einstellungen bearbeiten](#keyword-edit)

* [Status von Keywords und negativen Keywords ändern oder löschen](#keyword-status)

* [Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren](#copy-to-clipboard)

* [Zuweisen von Einschränkungen zu Keywords und Aufheben der Zuweisung von Einschränkungen zu Keywords](#keyword-constraints)

* [Zuweisen von ](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md) zu Schlüsselwörtern

## Schlüsselwörter erstellen {#keyword-create}

>[!TIP]
>
>Um eine große Anzahl von Keywords gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Keywords]** auf **[!UICONTROL Create Keywords]**.

1. Wählen Sie im **[!UICONTROL Basic Settings]** Schritt das Netzwerk, das Konto, die Kampagne und die Anzeigengruppe aus.

1. Geben Sie die [[!DNL Baidu] Keyword-Einstellungen](keyword-settings-baidu.md), [[!DNL Google Ads] Keyword-Einstellungen](keyword-settings-google.md), [[!DNL LY Ads] Keyword-Einstellungen](keyword-settings-yahoo-japan.md), [[!DNL Microsoft Advertising] Keyword-Einstellungen](keyword-settings-microsoft.md) oder [[!DNL Yandex] Keyword-Einstellungen](keyword-settings-yandex.md) ein.

   Sie können bis zu 2000 Keywords in einem Vorgang eingeben oder einfügen. Trennen Sie mehrere Keywords durch Kommas oder geben Sie sie in separaten Zeilen ein.

   >[!NOTE]
   >
   >Wenn in den Konto- oder Kampagneneinstellungen das Tracking nur auf Anzeigenebene festgelegt ist, generiert Search, Social und Commerce kein Tracking für Keywords.

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

1. Überprüfen Sie die Einstellungen. Um Einstellungen zu ändern, klicken Sie auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten") **[!UICONTROL Edit]** im entsprechenden Abschnitt und ändern Sie die Einstellungen.

1. Klicken Sie auf **[!UICONTROL Create]**.

## Keyword-Einstellungen bearbeiten {#keyword-edit}

Wenn Sie den Schlüsselworttext oder Übereinstimmungstyp ändern, können Sie das vorhandene Schlüsselwort löschen und je nach Anzeigennetzwerk ein neues erstellen. Einzelheiten finden Sie in den Keyword-Einstellungen für Ihr Werbenetzwerk.

>[!TIP]
>
>Um eine große Menge an Keyword-Daten gleichzeitig zu bearbeiten, einschließlich Keywords in verschiedenen Werbenetzwerken, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Aktivieren Sie auf der Registerkarte **[!UICONTROL Keywords]** das Kontrollkästchen neben den einzelnen Keywords, die bearbeitet werden sollen.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie die [[!DNL Baidu] Keyword-Einstellungen](keyword-settings-baidu.md), [[!DNL Google Ads] Keyword-Einstellungen](keyword-settings-google.md), [[!DNL LY Ads] Keyword-Einstellungen](keyword-settings-yahoo-japan.md), [[!DNL Microsoft Advertising] Keyword-Einstellungen](keyword-settings-microsoft.md) oder [[!DNL Yandex] Keyword-Einstellungen](keyword-settings-yandex.md).

   Bei mehreren Keywords können Sie nur die Felder bearbeiten, die für alle ausgewählten Keywords gelten, und Ihre Änderungen werden auf alle ausgewählten Keywords angewendet. Bei einigen alphanumerischen Feldern können Sie vorhandene Werte in einen angegebenen Wert ändern, eine vorhandene Zeichenfolge durch eine angegebene Zeichenfolge ersetzen, ein Präfix hinzufügen oder ein Suffix anhängen. Für einige Währungsfelder können Sie vorhandene Werte in einen bestimmten Wert ändern oder den Betrag um einen bestimmten Prozentsatz oder Geldbetrag mit einer Begrenzung erhöhen oder verringern.

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

1. Überprüfen Sie die Einstellungen. Um Einstellungen zu ändern, klicken Sie auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten") **[!UICONTROL Edit]** im entsprechenden Abschnitt und ändern Sie die Einstellungen.

1. Klicken Sie auf **[!UICONTROL Update]**.

## Negative Keywords erstellen {#keyword-negative-create}

Nur *[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising] und vorhandene [!DNL Baidu] Konten*

Sie können negative Keywords für eine Suchanzeigengruppe oder Kampagne erstellen, die auf die Suche oder das Display/native Netzwerk abzielt.

>[!NOTE]
>
>Sie können auch negative Keywords in den [Anzeigengruppeneinstellungen](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md) und [Kampagneneinstellungen](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md) erstellen und bearbeiten.

>[!TIP]
>
>Um eine große Anzahl negativer Keywords gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Negatives]** auf **[!UICONTROL Create Negatives]** und dann entweder **[!UICONTROL Campaign Negative Keyword]** oder **[!UICONTROL Ad Group Negative Keyword]**.

1. Wählen Sie das Netzwerk, das Konto, die Kampagne und (bei negativen Keywords auf Anzeigengruppenebene) die Anzeigengruppe aus.

1. Negative Keywords eingeben. Verwenden Sie die folgende Syntax ohne Minuszeichen (`-`):

   * Negative weit gefasste Übereinstimmung: `keyword` (von [!DNL Microsoft Advertising] nicht unterstützt)

   * Negative Übereinstimmung der Phrasen: `"keyword"`

   * Negative exakte Übereinstimmung: `[keyword]`

   Trennen Sie mehrere Werte durch Kommas oder geben Sie sie in separate Zeilen ein. Sie können bis zu 2000 negative Keywords in einem Vorgang eingeben oder einfügen. Es gelten die folgenden Anforderungen und Einschränkungen:

   * Maximale Zeichenlängen: [!DNL Baidu]: 30 Einzelbyte oder 15 Doppelbyte; [!DNL Microsoft Advertising]: 100 Einzelbyte oder 50 Doppelbyte; [!DNL Google Ads] und [!DNL LY Ads]: 80 Einzelbyte oder 40 Doppelbyte.

   * [!DNL Baidu] ist nur ein Übereinstimmungstyp pro Keyword pro Anzeigengruppe zulässig. Beispielsweise kann Anzeigengruppe 1 nicht sowohl `"keyword"` als auch `[keyword]` enthalten.

   * [!DNL Google Ads]: Jedes Keyword darf aus höchstens 10 Wörtern bestehen und nur Buchstaben, Ziffern und die folgenden Sonderzeichen enthalten: `# $ & _ - " [ ] ' + . / :`

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

1. Überprüfen Sie die Einstellungen. Um Einstellungen zu ändern, klicken Sie auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten") **[!UICONTROL Edit]** im entsprechenden Abschnitt und ändern Sie die Einstellungen.

1. Klicken Sie auf **[!UICONTROL Create]**.

## Status von Keywords und negativen Keywords ändern {#keyword-status}

Sie können ein aktives, bidable Suchbegriff anhalten, um das bidding dafür zu deaktivieren. Sie können die Gebotsabgabe später fortsetzen, indem Sie den Status wieder in Aktiv ändern.

Sie können auch aktive oder angehaltene Suchbegriffe oder negative Suchbegriffe löschen. Gelöschte Keywords werden aus dem Werbenetzwerk gelöscht. Sie sind weiterhin sichtbar, wenn Sie sie in den Datenfilter einbeziehen, können aber nicht geändert werden.

### Schlüsselwörter aktivieren oder anhalten

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Filtern Sie auf der Registerkarte **[!UICONTROL Keywords]** optional die Liste und aktivieren Sie dann das Kontrollkästchen neben jedem Keyword, dessen Status Sie ändern möchten.

1. Ändern Sie in der Symbolleiste für Massenaktionen den Status:

   * Um pausierte Keywords zu aktivieren, klicken Sie auf **[!UICONTROL Activate]**.

   * Um die aktiven Keywords anzuhalten, klicken Sie auf **[!UICONTROL Pause]**.

### Löschen von Keywords oder negativen Keywords

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Filtern Sie auf der Registerkarte **[!UICONTROL Keywords]** oder **[!UICONTROL Negatives]** optional die Liste und aktivieren Sie dann das Kontrollkästchen neben den einzelnen Keywords oder negativen Keywords, die gelöscht werden sollen.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

## Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren {#copy-to-clipboard}

Kopieren Sie die sichtbaren Informationen in die ausgewählten Zeilen entsprechend den angewendeten Filtern und Spalten, die in der Ansicht sichtbar sind. Die Informationen werden als tabulatorgetrennte Werte (TSV) gespeichert.

1. Aktivieren Sie das Kontrollkästchen neben jeder Zeile, deren Daten Sie kopieren möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Copy]**.

## Einschränkungszuweisungen für Schlüsselwörter verwalten {#keyword-constraints}

Sie können Gebotsbeschränkungen für Kampagnen, Anzeigengruppen, Keywords, Platzierungen, Produktgruppen auf Einheitenebene und dynamische Suchziele zuweisen und entfernen. Jede Entität kann nur eine Einschränkung aufweisen.

Beschränkungen werden von untergeordneten Entitäten übernommen, sodass Sie untergeordneten Entitäten keine Beschränkungen zuweisen müssen, es sei denn, Sie möchten die übernommenen Werte überschreiben.

Wenn Sie die Zuweisung einer Einschränkung aufheben, wird die Verknüpfung mit den Kontokomponenten und allen untergeordneten Komponenten entfernt, und es sind keine Berichtsdaten für die Einschränkung mehr für diese Komponenten verfügbar. Beim Aufheben der Zuweisung einer Einschränkung werden die Einschränkung oder die Kontokomponenten selbst nicht gelöscht.

>[!NOTE]
>
>* Wenn Sie später ein Keyword oder die Anzeigenkopie für eine nicht veränderliche Anzeige bearbeiten und so ein neues Keyword oder eine neue Anzeige erstellen, wird die Begrenzung nicht der neuen Entität zugewiesen.
>* Aktive Einschränkungen beschränken die Gebotsabgabe nur für zugewiesene Gebotseinheiten in optimierten alten Portfolios auf Keyword-Ebene. Sie werden bei Gebotseinheiten ignoriert, die sich in aktiven Portfolios befinden, sich in hybriden Portfolios befinden oder nicht in Portfolios sind.

### Zuweisen einer Einschränkung zu Schlüsselwörtern {#keyword-constraint-assign}

Sie können einem oder mehreren Keywords eine einzelne Einschränkung zuweisen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Aktivieren Sie auf der Registerkarte **[!UICONTROL Keywords]** das Kontrollkästchen neben jedem Keyword, dem Sie eine einzelne Einschränkung zuweisen möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Wählen Sie die Einschränkung aus.

1. Klicken Sie auf **[!UICONTROL Assign Now]**.

### Zuweisung von Einschränkungen zu Schlüsselwörtern aufheben {#keyword-constraint-unassign}

Durch Aufheben der Zuweisung einer Einschränkung wird sie nicht gelöscht. Informationen zum Löschen einer Einschränkung, sodass sie für die zukünftige Verwendung nicht mehr verfügbar ist, finden Sie unter „Löschen von Einschränkungen für Suchangebotseinheiten“ im Kapitel „Optimierungshandbuch“ zu „Bid-Einschränkungen“, das in Search, Social und Commerce verfügbar ist.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. Aktivieren Sie auf der Registerkarte **[!UICONTROL Keywords]** das Kontrollkästchen neben jedem Keyword, dessen Zuweisung Sie aufheben möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Klicken Sie auf **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] Keyword-Einstellungen](keyword-settings-baidu.md)
>* [[!DNL Google Ads] Keyword-Einstellungen](keyword-settings-google.md)
>* [[!DNL LY Ads] Keyword-Einstellungen](keyword-settings-yahoo-japan.md)
>* [[!DNL Microsoft Advertising] Keyword-Einstellungen](keyword-settings-microsoft.md)
>* [[!DNL Yandex] Keyword-Einstellungen](keyword-settings-yandex.md)
>* [Einschränkungen für Suchangebotseinheiten verwalten](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Verwalten von Kennzeichnungsklassifizierungen](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
