---
title: Verwalten [!DNL Google Ads] dynamischer Suchziele
description: Erfahren Sie, wie Sie dynamische  [!DNL Google Ads]  erstellen und verwalten.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: c074f430583e2d320eb4d47b4fc956c1822bd04a
workflow-type: tm+mt
source-wordcount: 702
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

## Die [!UICONTROL Auto Targets]

Die Ansicht [!UICONTROL Target] > [!UICONTROL Auto Targets] listet alle dynamischen Suchziele in der gefilterten Ansicht für das ausgewählte Advertiser-Konto auf. Sie können auch Ihre dynamischen Suchziele verwalten.

### Verfügbare Aktionen

<!--
* Create a dynamic search target

* Edit the settings for a dynamic search target

* Change the status of dynamic search targets
-->

* [Einschränkungen zuweisen](#constraint-assign) zu dynamischen Suchzielen und [Einschränkungen entfernen](#constraint-unassign) aus dynamischen Suchzielen

* [Kennzeichnungsklassifizierungen zuweisen](#classification-values-assign) zu dynamischen Suchzielen und [Kennzeichnungsklassifizierungen entfernen](#classification-values-remove) aus dynamischen Suchzielen

>[!NOTE]
>
>Sie können große Mengen an Zieldaten (einschließlich Kennzeichnungen und Einschränkungszuweisungen) gleichzeitig erstellen und bearbeiten, indem Sie [Bulksheet-Dateien](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) hochladen und im Werbenetzwerk posten.

<!--
Not available yet:

## Create a [!DNL Google Ads] dynamic search target

You can create dynamic search targets to define pages in your websites (that is, the domains used in your ads' display URLs) whose content is used to target your dynamic search ads in the same ad group.

You can target all criteria or up to three individual criteria.

>[!NOTE]
>
>To best track performance, create an "[!UICONTROL All Targets]" target for only one ad group per campaign.

>[!TIP]
>
>To create many account components at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. In the toolbar above the data table, click ![Create](/help/search-social-commerce/assets/add.png "Create").

1. Select the ad network, the account, the campaign, and the ad group, and then click **[!UICONTROL Continue]**.

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

1. Click **[!UICONTROL Post]**.

## Edit [!DNL Google Ads] dynamic search target settings

You can edit the status or maximum bid for a [!DNL Google Ads] dynamic search target. You can't change the criteria that are targeted.

>[!TIP]
>
>To edit large amounts of data at once, use [campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. Select the check box next to each row to edit.

   For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."

1. In the toolbar above the data table, click ![Edit](/help/search-social-commerce/assets/edit.png "Edit").

1. Specify the [dynamic search target settings](#dynamic-search-target-settings).

   For multiple targets, your changes are applied to all of the selected targets. For the [!UICONTROL Bid field], you have options to change existing values to a specified value or to either increase or decrease the amount by a specified percentage or monetary amount, with a limit.

1. Save the data:

   * (Single targets) Click **[!UICONTROL Post]**.
   
   * (Multiple ad groups) Click **[!UICONTROL Post Now]**.

## Change the status of [!DNL Google Ads] dynamic search targets

You can pause any active dynamic search target in a supported campaign type to stop using them for dynamic search ads in the same ad group. You can later use them as targets by changing the ad status back to active.

You can also delete any dynamic target.

1. In the main menu, click **[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]**. In the submenus, click **[!UICONTROL Live] > [!UICONTROL Auto Targets]**.

1. (Optional) Filter the list to include specific dynamic targets.

1. Do either of the following:
   
   * To change the status of one dynamic target, click in the **[!UICONTROL Status]** column and change the status.
   
   * To delete one or more dynamic targets, do the following:
   
     1.  Select the check box next to each dynamic target you want to delete.
     
        For tips on selecting multiple rows, see "[Select multiple rows](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)."
     
     1. In the toolbar, click ![More](/help/search-social-commerce/assets/more.png "More") and select **[!UICONTROL Delete]**.
     
     1. In the confirmation message, click **[!UICONTROL Delete]**.

## [!DNL Google Ads] dynamic search target settings {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** (Required when you don't specify a website domain and language in the campaign's [!UICONTROL DSA Options] section; read-only for existing targets) Dynamic search targets for the ad group:

* *[!UICONTROL All Targets]* (the default): Targets all indexed pages.

* *\[Specific Targets\]:* Targets up to three criteria for the indexed pages. When you select this, you must specify the criteria by specifying information categories and specific values for which to target ads (for example, "URL contains shoes.example.com"). To specify more than one criteria, click **[!UICONTROL + And]**. Target criteria include:

  * *[!UICONTROL Category]:* To show ads for indexed pages with a specific [!DNL Google Ads] content category.

  * *[!UICONTROL URL]:* To show ads for indexed pages with a specific URL, where the value may be included anywhere within the URL.

  * *[!UICONTROL Page Title]:* To show ads for indexed pages with specific text in the page title.

  * *[!UICONTROL Page Content]:* To show ads for indexed pages with specific content.

**Status:** The status of the target settings:

* *[!UICONTROL Active]* (the default): Enables bidding.

* *[!UICONTROL Paused]:* Disables bidding.

* *[!UICONTROL Deleted]* (existing targets only): Deletes the target settings.

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** The maximum cost per click (CPC) for an ad or cost per 1000 impressions (CPM) for an ad, as applicable for the ad network and campaign pricing model. This value overrides the ad group-level value.

>[!NOTE]
>
>If the target is in an optimized portfolio, then the specified CPC bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations.

-->

## Weisen Sie ausgewählten dynamischen Suchzielen in der neuen [!UICONTROL Auto Targets] eine Einschränkung zu {#constraint-assign}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Target]>[!UICONTROL Auto Targets]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem dynamischen Suchziel, dem Sie eine einzelne Einschränkung zuweisen.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Wählen Sie die Einschränkung aus.

1. Klicken Sie auf **[!UICONTROL Assign Now]**.

## Entfernen von Einschränkungen aus ausgewählten dynamischen Suchzielen aus der neuen [!UICONTROL Auto Targets] {#constraint-unassign}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Auto Targets]**.

1. Aktivieren Sie das Kontrollkästchen neben jeder dynamischen Suchzielgruppe, deren Zuweisung von Einschränkungen Sie aufheben möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Klicken Sie auf **[!UICONTROL Confirm]**.

## Zuweisen von Klassifizierungswerten zu dynamischen Suchzielen {#classification-values-assign}

>[!NOTE]
>
>Beschriftungswerte werden von untergeordneten Entitäten übernommen. Geben Sie daher keine Werte für untergeordnete Entitäten ein, es sei denn, Sie möchten die übernommenen Werte überschreiben.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Target]>[!UICONTROL Auto Targets]**.

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

## Entfernen von Kennzeichnungswerten aus dynamischen Suchzielen {#classification-values-remove}

Das Entfernen eines Klassifizierungswerts entfernt die Verknüpfung mit der Kontokomponente und allen untergeordneten Komponenten. Berichtsdaten für den Classification-Wert sind für diese Komponenten nicht mehr verfügbar. Wenn Sie einen Klassifizierungswert entfernen, werden weder der Wert noch die Kontokomponenten gelöscht.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Target]>[!UICONTROL Auto Targets]**.

1. Aktivieren Sie das Kontrollkästchen neben den einzelnen dynamischen Suchzielen, aus denen Sie einen Titelwert entfernen möchten.

   Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Aktivieren Sie das Kontrollkästchen neben jedem Classification-Wert, der aus den ausgewählten Entitäten entfernt werden soll.

   Um alle zugewiesenen Werte auszuwählen, klicken Sie auf **[!UICONTROL Select All]**. Um die Auswahl aller zugewiesenen Werte aufzuheben, klicken Sie auf **[!UICONTROL Deselect All]**.

1. Klicken Sie auf **[!UICONTROL Unassign Selected]**.

>[!MORELIKETHIS]
>
>* [(Neue Benutzeroberfläche) Verwalten von Einschränkungen für Suchangebotseinheiten](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [(Neue Benutzeroberfläche) Verwalten von Kennzeichnungsklassifizierungen](/help/search-social-commerce/new-ui/reports/label-classifications-manage.md)
