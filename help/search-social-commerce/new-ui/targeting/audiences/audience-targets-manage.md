---
title: Verwalten von Zielgruppenzielen für Kampagnen und Anzeigengruppen
description: Erfahren Sie, wie Sie Zielgruppenziele und ihre Angebotsanpassungen für Google Ads und Microsoft Advertising verwalten.
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
source-git-commit: 7e7dcde9fb195e04025a1a8d89e792ff562b053f
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 0%
---
# Verwalten von Zielgruppenzielen für Kampagnen und Anzeigengruppen

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising] Konten*

[!DNL Google Ads] Kampagnen und Anzeigengruppen sowie [!DNL Microsoft Advertising] Anzeigengruppen können bestimmte [&#x200B; (Zielgruppen](audience-manage.md) aus demselben Anzeigennetzwerk ansprechen. Das Anzeigennetzwerk bestimmt, wie groß eine Zielgruppe sein muss, um anvisiert zu werden.

Eine Audience-Zielgruppe verknüpft eine bestehende Audience mit einer Kampagne oder Anzeigengruppe. Sie können die Angebotsanpassung und den Status vorhandener Ziele bearbeiten.

>[!NOTE]
>
>[Zielgruppenausschlüsse](audience-exclusions.md) setzen Ziele immer außer Kraft.

## Über die [!UICONTROL Targets] {#audience-targets-view-about}

Die Ansicht [!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Targets] listet die Zielgruppenziele in der gefilterten Ansicht für den ausgewählten Advertiser auf.

Zum Anzeigen der Daten ist die Berechtigung [!UICONTROL View Audiences] erforderlich. Das Bearbeiten, Ändern des Status und Löschen von Zielen erfordert die Berechtigung [!UICONTROL Edit Audience Targets] .

### Verfügbare Aktionen

<!--
Restricted to internal beta users:

* [Configure audience targets](#audience-targets-create)
-->

* [Bearbeiten der Zielgruppen-Bid-Anpassungen und des Status](#audience-targets-edit)

* [Ändern des Status von Audience-Zielen oder Löschen von Audience-Zielen](#audience-targets-status)

* [Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience target creation.

## Configure audience targets {#audience-targets-create}

Creating targets requires the [!UICONTROL Edit Audience Targets] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Targets]** tab.

1. Click **[!UICONTROL Create Target]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups to target:

   * Select each applicable campaign or ad group for inclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

   You can't configure a target for both a parent campaign and a child ad group that automatically uses the target.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

1. (Optional) [Set a bid adjustment](#audience-targets-edit) for the new targets.
-->

## Bearbeiten der Zielgruppen-Bid-Anpassungen und des Status {#audience-targets-edit}

Sie können jeweils ein oder mehrere Zielgruppenziele bearbeiten. Ihre Änderungen gelten für alle ausgewählten Ziele.

>[!NOTE]
>
>Search, Social und Commerce optimieren den Angebotsmodifikator automatisch, wenn die übergeordnete Kampagne die CPC-Angebotsstrategie verwendet und sich in einem Portfolio befindet, das so konfiguriert ist, dass die Angebotsanpassungswerte für Zielgruppenziele automatisch optimiert werden. Angebotsmodifikatoren für [!DNL Microsoft Advertising] dynamische Remarketing-Audience-Ziele werden nicht optimiert.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Audiences]**, und klicken Sie dann auf die Registerkarte **[!UICONTROL Targets]** .

1. Aktivieren Sie das Kontrollkästchen neben jeder zu bearbeitenden Zielgruppe.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]**.

1. **[!UICONTROL Bid Modifier]**, **[!UICONTROL Status]** oder beides bearbeiten. Siehe [Bearbeiten von Einstellungen](#audience-targets-edit-settings).

   Lassen Sie ein Feld unverändert, um den vorhandenen Wert beizubehalten.

1. (Optional) Erweitern Sie **[!UICONTROL ADDITIONAL DETAILS]** und geben Sie eine **[!UICONTROL Project Name]** und einen **[!UICONTROL Description]** ein.

1. Klicken Sie auf **[!UICONTROL Save]**.

Sie können die Bid-Anpassung eines einzelnen Ziels auch direkt in der Datentabelle bearbeiten, indem Sie in der Spalte **[!UICONTROL Bid Adjustment]** auf seinen Wert klicken.

## Ändern des Status von Audience-Zielen oder Löschen von Audience-Zielen {#audience-targets-status}

Sie können ein aktives Audience-Ziel anhalten, um die Gebotsabgabe für dieses Ziel zu deaktivieren, und später die Gebotsabgabe durch Aktivierung fortsetzen. Sie können auch aktive oder pausierte Ziele löschen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Audiences]**, und klicken Sie dann auf die Registerkarte **[!UICONTROL Targets]** .

1. (Optional) Filtern Sie die Liste, um bestimmte Zielgruppenziele einzuschließen.

1. Aktivieren Sie das Kontrollkästchen neben jeder Zielgruppe, deren Status Sie ändern möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf eine der folgenden Optionen:

   * **[!UICONTROL Activate]**, um die ausgewählten Ziele zu aktivieren.

   * Ausgewählte Ziele **[!UICONTROL Pause]** angehalten werden.

   * **[!UICONTROL Delete]** die ausgewählten Ziele gelöscht werden.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

## Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren {#copy-to-clipboard}

Kopieren Sie die sichtbaren Informationen in die ausgewählten Zeilen entsprechend den angewendeten Filtern und Spalten, die in der Ansicht sichtbar sind. Die Informationen werden als tabulatorgetrennte Werte (TSV) gespeichert.

1. Aktivieren Sie das Kontrollkästchen neben jeder Zeile, deren Daten Sie kopieren möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Copy]**.

## Bearbeiten von Audience Target-Einstellungen {#audience-targets-edit-settings}

**[!UICONTROL Bid Modifier]:** Ändern der Zielgruppen-Angebotsanpassung:

* *[!UICONTROL Set To]:* Ersetzen Sie die bestehende Angebotsanpassung durch den angegebenen Prozentsatz.

* *[!UICONTROL Increase]:* Erhöhen Sie den vorhandenen Wert um den angegebenen Prozentsatz.

* *[!UICONTROL Decrease]:* Verringern Sie den vorhandenen Wert um den angegebenen Prozentsatz.

Geben Sie für [!UICONTROL Increase] und [!UICONTROL Decrease] einen nicht negativen Wert ein.

Bei einem festgelegten Wert wird das Gebot bei 0 % nicht angepasst. Andere unterstützte Werte liegen zwischen -90 % und 900 %. Wenn beispielsweise das Gebot auf Keyword-Ebene 1 USD und die Anpassung der Zielgruppengebote 50 % beträgt, erhöht sich das Gebot für diese Zielgruppe auf 1,50 USD.

**[!UICONTROL Status]:** Wählen Sie **[!UICONTROL Active]** aus, um die Gebotsabgabe zu aktivieren, oder **[!UICONTROL Paused]** , um die Gebotsabgabe für die Zielgruppe zu deaktivieren.

>[!MORELIKETHIS]
>
>* [Verwalten von Zielgruppen](audience-manage.md)
>* [Verwalten von Zielgruppenausschlüssen für Kampagnen und Anzeigengruppen](audience-exclusions.md)
