---
title: Verwalten von Google Ads Shared Callout-Erweiterungen
description: Erfahren Sie, wie Sie freigegebene Callout-Erweiterungen für Google Ads erstellen, bearbeiten und löschen.
feature: Search Campaign Management
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
source-git-commit: 10d7adc3b3ced812ee1281139a23a573df2beeef
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%
---
# Verwalten [!DNL Google Ads] freigegebenen Callout-Erweiterungen

Nur *[!DNL Google Ads]Konten*

Eine Callout-Erweiterung ist ein Text zu einem Produkt, einem Service oder einer Promotion, die bzw. den Ihre Site anbietet und der mit einer Textanzeige angezeigt wird. Das Werbenetzwerk kann 2-4 Hinweisen mit einer Anzeige anzeigen.

Sie erstellen freigegebenen Callout-Text und Einstellungen auf Kontoebene für ein [synchronisiertes Google Ads-Konto](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md). Hinweise in der Bibliothek werden erst dann für Anzeigen verwendet, wenn Sie sie mit einer unterstützten Kampagne oder Anzeigengruppe im Suchnetzwerk verknüpfen.

Damit Ihre Anzeigen für die Anzeige mit Hinweisen infrage kommen, müssen Sie pro Kampagne oder Anzeigengruppe mindestens zwei Hinweise zuweisen. Bei Hinweisen auf Anzeigengruppenebene werden Hinweisen auf Kampagnenebene überschrieben.

## Über die [!UICONTROL Callouts]- und [!UICONTROL Associations] {#callout-view-about}

In **[!UICONTROL Library]>[!UICONTROL Extensions]** listet die Registerkarte **[!UICONTROL Callouts]** Ihre freigegebenen Hinweise auf Kontoebene auf. Auf der Registerkarte **[!UICONTROL Associations]** werden die Verknüpfungen zwischen Erweiterungen und Kontoentitäten aufgelistet.

Zum Anzeigen dieser Registerkarten ist die Berechtigung [!UICONTROL View Extensions] erforderlich. Zum Erstellen, Bearbeiten und Löschen von Hinweisen sowie zum Erstellen oder Löschen von Verknüpfungen ist die Berechtigung [!UICONTROL Edit Extensions] erforderlich.

Die maximale Anzahl von Erweiterungen pro Konto finden Sie in der Dokumentation zu ](https://support.google.com/google-ads/answer/6372658) Ads für [Google.

### Verfügbare Aktionen

* [Erstellen eines freigegebenen Hinweises](#callout-create)

* [Einstellungen für freigegebene Callouts bearbeiten](#callout-edit)

* [Freigegebene Hinweise löschen](#callout-delete)

* [Verknüpfen von freigegebenen Hinweisen mit Kampagnen und Anzeigengruppen](ad-extension-association-manage.md#callout-associate)

* [Löschen von Erweiterungsverknüpfungen](ad-extension-association-manage.md#association-delete)

* [Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren](#copy-to-clipboard)

## Erstellen eines freigegebenen Hinweises {#callout-create}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Library]>[!UICONTROL Extensions]**, und klicken Sie dann auf die Registerkarte **[!UICONTROL Callouts]** .

1. Klicken Sie auf **[!UICONTROL Create Callout]**.

1. Wählen Sie in **[!UICONTROL Basic Settings]** [!DNL Google Ads] und das Konto aus.

1. Geben Sie die [Einstellungen für freigegebene ](#shared-callout-settings)&quot; ein.

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

1. Überprüfen Sie die Einstellungen. Um eine Einstellung zu ändern, klicken Sie im entsprechenden Abschnitt auf **[!UICONTROL Edit]**.

1. Klicken Sie auf **[!UICONTROL Create]**.

Nachdem Sie den Callout erstellt haben, [ Sie ihn mit einer Kampagne oder Anzeigengruppe ](ad-extension-association-manage.md#callout-associate).

## Einstellungen für freigegebene Callouts bearbeiten {#callout-edit}

Sie können jeweils nur einen freigegebenen Callout bearbeiten. Sie können das Startdatum nach der Erstellung nicht ändern.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Library]>[!UICONTROL Extensions]**, und klicken Sie dann auf die Registerkarte **[!UICONTROL Callouts]** .

1. Aktivieren Sie das Kontrollkästchen neben einem Callout.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie die [Einstellungen für freigegebene ](#shared-callout-settings)&quot;.

1. Klicken Sie auf **[!UICONTROL Review and Save]**, überprüfen Sie die Einstellungen, und klicken Sie dann auf **[!UICONTROL Update]**.

## Freigegebene Hinweise löschen {#callout-delete}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Library]>[!UICONTROL Extensions]**, und klicken Sie dann auf die Registerkarte **[!UICONTROL Callouts]** .

1. Aktivieren Sie das Kontrollkästchen neben den freigegebenen Hinweisen, die gelöscht werden sollen.

   Informationen zur Auswahl mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

Um eine Verknüpfung zu entfernen, ohne den freigegebenen Callout aus der Bibliothek zu löschen, [ Sie stattdessen die Verknüpfung ](ad-extension-association-manage.md#association-delete).

## Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren {#copy-to-clipboard}

Kopieren Sie die sichtbaren Informationen in die ausgewählten Zeilen entsprechend den angewendeten Filtern und Spalten, die in der Ansicht sichtbar sind. Die Informationen werden als tabulatorgetrennte Werte (TSV) gespeichert.

1. Aktivieren Sie das Kontrollkästchen neben jeder Zeile, deren Daten Sie kopieren möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Copy]**.

## Freigegebene Callout-Einstellungen {#shared-callout-settings}

Weitere Richtlinien und Gründe für die Ablehnung von Hinweisen finden Sie in den [Anforderungen an Hinweisen zu Google Ads](https://support.google.com/adspolicy/answer/1054212).

**[!UICONTROL Callout Text]:** Der anzuzeigende Text. Es kann bis zu 25 Einzelbyte- oder 12 Doppelbyte-Zeichen enthalten. Ausrufezeichen oder Satzzeichen dürfen nicht am Anfang des Textes stehen.

**[!UICONTROL Start Date]:** (Optional, nur Erstellung) Das erste Datum, an dem der Callout angezeigt werden kann. Der Standardwert ist der aktuelle Tag. Um ein Datum in der Zukunft anzugeben, geben Sie es im Format MM/TT/JJJJ ein oder verwenden Sie die Datumsauswahl. Das Startdatum ist für vorhandene Hinweise schreibgeschützt.

**[!UICONTROL End Date]:** (Optional) Das letzte Datum, an dem der Callout angezeigt werden kann. Standardmäßig kann der Callout unbegrenzt angezeigt werden. Um ein Enddatum festzulegen, geben Sie es im Format MM/TT/JJJJ ein oder verwenden Sie die Datumsauswahl.

**[!UICONTROL Mobile Preference]:** (Optional) Ermöglicht [!DNL Google Ads], zu versuchen, die Erweiterung für Benutzer von Mobilgeräten anzuzeigen, anstatt für Desktop- oder Tablet-Benutzer. Andernfalls kann die Erweiterung auf jedem Gerätetyp angezeigt werden. [!DNL Google Ads] garantiert nicht, dass die Erweiterung auf dem bevorzugten Gerätetyp angezeigt wird.

## Leistungsdaten für Hinweise {#callout-performance}

Search, Social und Commerce zugeordnet sind, die auf eine Anzeigenerweiterung und die daraus resultierenden Konversionen in das Keyword klicken, das mit der Anzeige verknüpft ist, in der die Erweiterung angezeigt wird. Kosten- und Klickdaten auf Erweiterungsebene sind in Search, Social und Commerce nicht verfügbar.

Sie können die Kosten für die Erweiterung anzeigen und in der [!DNL Google Ads] auf Daten klicken.

>[!MORELIKETHIS]
>
>* [Verwalten freigegebener Sitelink-Erweiterungen](sitelink-extension-manage.md)
>* [Verwalten von Anzeigenerweiterungsverknüpfungen](ad-extension-association-manage.md)
