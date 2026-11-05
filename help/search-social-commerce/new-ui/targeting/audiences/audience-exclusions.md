---
title: Verwalten von Zielgruppenausschlüssen für Kampagnen und Anzeigengruppen
description: Erfahren Sie mehr über Google Ads und Microsoft Advertising-Zielgruppenausschlüsse, einschließlich der Löschung von Google Ads-Ausschlüssen.
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
source-wordcount: '269'
ht-degree: 0%
---
# Verwalten von Zielgruppenausschlüssen für Kampagnen und Anzeigengruppen

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising] Konten*

Ein Zielgruppenausschluss verhindert, dass Anzeigen in einer Kampagne oder Anzeigengruppe Benutzern in einer bestimmten [Zielgruppe“ angezeigt &#x200B;](audience-manage.md).

Bei [!DNL Google Ads]-Konten können Sie jeden Zielgruppentyp ausschließen. Bei [!DNL Microsoft Advertising]-Konten können Sie nur dynamische Remarketing-Audiences ausschließen.

>[!NOTE]
>
>Ausschlüsse überschreiben immer [Zielgruppenziele](audience-targets-manage.md).

## Über die [!UICONTROL Exclusions] {#audience-exclusions-view-about}

Die Ansicht [!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Exclusions] listet die Zielgruppenausschlüsse in der gefilterten Ansicht für den ausgewählten Advertiser auf.

Zum Anzeigen der Daten ist die Berechtigung [!UICONTROL View Audiences] erforderlich. Das Auswählen von Zeilen und das Löschen unterstützter Ausschlüsse erfordert die Berechtigung [!UICONTROL Edit Audience Exclusions] .

### Verfügbare Aktionen

<!--
Restricted to internal beta users:

* [Configure audience exclusions](#audience-exclusions-create)
-->

* [Zielgruppenausschlüsse löschen](#audience-exclusions-delete)

* [Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren](#copy-to-clipboard)

<!--
Restricted to internal beta users: audience exclusion creation.

## Configure audience exclusions {#audience-exclusions-create}

Creating exclusions requires the [!UICONTROL Edit Audience Exclusions] permission in addition to internal beta access.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Exclusions]** tab.

1. Click **[!UICONTROL Create Exclusion]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. Select one or more audiences from the account. You can search the list.

   [!DNL Google Ads] customer match audiences are available only for search and shopping campaigns.

1. Select the campaigns or ad groups from which to exclude the audiences:

   * Select each applicable campaign or ad group for exclusion.

   * To view a campaign's ad groups, expand the campaign.

   * Use the list's search controls to find specific campaigns or ad groups.

1. Click **[!UICONTROL Review and Save]**.

1. Review the selections. To make changes, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.
-->

## Zielgruppenausschlüsse löschen {#audience-exclusions-delete}

Nur *[!DNL Google Ads]Ausschlüsse*

Sie können einen oder mehrere [!DNL Google Ads] Zielgruppenausschlüsse löschen. Das Löschen [!DNL Microsoft Advertising] Ausschlüsse wird in dieser Ansicht nicht unterstützt.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Audiences]**, und klicken Sie dann auf die Registerkarte **[!UICONTROL Exclusions]** .

1. (Optional) Filtern Sie die Liste, um bestimmte Zielgruppenausschlüsse einzuschließen.

1. Aktivieren Sie das Kontrollkästchen neben jedem zu löschenden [!DNL Google Ads]. Schließen Sie keine Ausschlüsse aus einem anderen Werbenetzwerk in die Auswahl ein.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

## Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren {#copy-to-clipboard}

Kopieren Sie die sichtbaren Informationen in die ausgewählten Zeilen entsprechend den angewendeten Filtern und Spalten, die in der Ansicht sichtbar sind. Die Informationen werden als tabulatorgetrennte Werte (TSV) gespeichert.

1. Aktivieren Sie das Kontrollkästchen neben jeder Zeile, deren Daten Sie kopieren möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Copy]**.

>[!MORELIKETHIS]
>
>* [Verwalten von Zielgruppen](audience-manage.md)
>* [Verwalten von Zielgruppenzielen für Kampagnen und Anzeigengruppen](audience-targets-manage.md)
