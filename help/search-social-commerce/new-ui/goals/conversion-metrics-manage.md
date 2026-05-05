---
title: Konversionsmetriken eines Werbetreibenden verwalten
description: Erfahren Sie, wie Sie die Konversionsmetriken verwenden können, die Adobe Advertising für einen Advertiser verfolgt.
feature: Conversions
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 0%

---

# Konversionsmetriken eines Werbetreibenden verwalten

Die Metriken [Konversion](/help/search-social-commerce/glossary.md#c-d) eines Advertisers werden in Adobe Advertising verwendet:

* In Search, Social und Commerce können Daten für Konversionsmetriken in Spalten in Kampagnen-, Portfolio- und Zielgruppen-Management-Ansichten und in Berichten angezeigt werden. Benutzer mit ausreichenden Zugriffsberechtigungen können Konversionsmetriken auch verwenden, um Ziele zu erstellen, die zur Optimierung von Portfolios verwendet werden.

* (Werbetreibende mit Advertising DSP) In DSP können Sie Konversionsmetriken in Kampagnenverwaltungsansichten, benutzerdefinierte Ziele und benutzerdefinierte Berichte aufnehmen. Sie können Konversionsmetriken auch verwenden, um [benutzerdefinierte Ziele](/help/dsp/admin/custom-objectives-manage.md) zu erstellen, die zur Optimierung von Paketen verwendet werden.

Zu den verfügbaren Metriken gehören:

* Konversionsmetriken, die Adobe Advertising für einen Advertiser verfolgt.

* [Konversions- und Site-Interaktionsmetriken wurden aus Adobe Analytics synchronisiert](/help/integrations/analytics/analytics-data-in-advertising.md).

* [Site-Ereignisse, die mit Adobe Customer Journey Analytics synchronisiert ](/help/integrations/customer-journey-analytics/overview.md).

* Konversionen, die von [!DNL Google Ads] verfolgt werden, und Konversionen, die von [!DNL Microsoft Advertising] universellen Ereignisverfolgungstags verfolgt werden.

* ([ Sie eine bestimmte Kombination aus  [!DNL Google Analytics] , Eigenschaft und Ansicht als Datenquelle konfiguriert haben](/help/search-social-commerce/admin/data-sources/data-source-about.md) für Search, Social und Commerce) Konversionen von [!DNL Google Analytics] verfolgt.

* Konversionen aus benutzerdefinierten Feeds.

Aus der Liste der verfügbaren Konversionsmetriken kann jeder Benutzer mit Zugriff auf die Daten des Werbetreibenden die Metriken anpassen, die für Verwaltungsansichten und Berichte verfügbar sind, einschließlich oder ohne Angabe bestimmter Metriken. Sie können entweder einen Metriknamen genau so verwenden, wie er in den abgerufenen Daten geschrieben ist, oder den Namen ändern, der in den Spaltenüberschriften angezeigt wird, um die Lesbarkeit zu verbessern.

>[!IMPORTANT]
>
>Standardmäßig sind keine der Konversionsmetriken eines Advertisers - mit Ausnahme der Konversionen, die von [!DNL Google Ads], [!DNL Google Analytics] und [!DNL Microsoft Advertising] universellen Ereignisverfolgungs-Tags verfolgt werden - zur Aufnahme in Kampagnen- und Portfolioverwaltungsansichten, -ziele und -berichte verfügbar. Um eine Konversionsmetrik verfügbar zu machen, müssen Sie sie explizit verfügbar machen.
>
>Neue Konversionen, die von [!DNL Google Ads], [!DNL Google Analytics] und [!DNL Microsoft Advertising] universellen Ereignis-Tracking-Tags verfolgt werden, sind immer automatisch verfügbar.

>[!TIP]
>
>Sobald der Advertiser (oder das Werbenetzwerk) die Erfassung einer Konversionsmetrik beendet hat, [blenden Sie sie aus den Verwaltungsansichten und Berichten aus](#conversion-metrics-change-available) es sei denn, Sie möchten sie für die Anzeige historischer Daten verwenden.

## Anzeigen der für einen Advertiser verfolgten Konversionsmetriken

* Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

Es werden alle für den Advertiser erfassten Konversionsmetriken und alle ihnen zugewiesenen Anzeigenamen aufgelistet. Jede Metrikzeile enthält die Quelle der Metrik.

## Anzeigenamen für eine Konversionsmetrik ändern

Wenn Sie beispielsweise Registrierungsdaten mithilfe einer Konversionsmetrik mit dem Namen *reg* erfassen, können Sie optional den Anzeigenamen ändern, damit er als „Registrierungen“ angezeigt wird.

Ein vorhandener Anzeigename kann nicht gelöscht werden.

>[!NOTE]
>
>Bei [Metriken von [!DNL Google Analytics]](/help/search-social-commerce/admin/data-sources/data-source-about.md) werden alle manuellen Änderungen am Anzeigenamen überschrieben, wenn Sie die Integration aktualisieren oder erneut authentifizieren. Ebenso werden alle Namensänderungen in [!DNL Google Analytics] ignoriert, es sei denn, Sie [ die Integration ](/help/search-social-commerce/admin/data-sources/data-source-edit.md) oder [erneut ](/help/search-social-commerce/admin/data-sources/data-source-reauthenticate.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Filtern Sie die Liste [über die Symbolleiste](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) oder aus einer [Spaltenüberschrift](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Halten Sie in der Spalte **[!UICONTROL Conversion Display Name]** für die Metrik den Cursor über den Metriknamen und klicken Sie auf **…** > **[!UICONTROL Rename]**.

1. Geben Sie den Namen ein, der angezeigt werden soll, und klicken Sie dann auf **[!UICONTROL Apply]**.

   Anzeigenamen müssen eindeutig sein und dürfen die folgenden Sonderzeichen nicht enthalten: `\"<'>&`

## Ändern der Konversionsmetriken, die in Verwaltungsansichten, Zielen und Berichten verfügbar sind {#conversion-metrics-change-available}

>[!NOTE]
>
>Wenn Sie eine Konversionsmetrik ausblenden, die zuvor verfügbar war, wird sie aus allen abgeleiteten Metriken entfernt, die die Konversionsmetrik enthalten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

   Es werden alle Konversionsmetriken aufgelistet, die für den Advertiser erfasst wurden, sowie alle anderen Namen, die für die Anzeige angegeben wurden.

1. (Optional) Filtern Sie die Liste [aus der Symbolleiste](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) oder aus einer [Spaltenüberschrift](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

1. Ändern der Konversionsmetriken, die für Verwaltungsansichten und -berichte verfügbar sind:

   * Um eine einzelne Metrik ein- oder auszublenden, klicken Sie in der Spalte **[!UICONTROL Visibility]** auf den Umschalter, um die Einstellung zu ändern.

   * Gehen Sie wie folgt vor, um mehrere Metriken ein- oder auszublenden:

      1. Aktivieren Sie das Kontrollkästchen neben jeder Konversionsmetrik.

         Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

      1. Klicken Sie in der Symbolleiste für Massenaktionen auf ![Sichtbarkeit](/help/search-social-commerce/assets/visible.png "Sichtbarkeit"), um die Metriken anzuzeigen oder ![Sichtbarkeit von](/help/search-social-commerce/assets/visibility-off.png "Sichtbarkeit von") auszublenden.

      1. (Um Metriken auszublenden) Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]** , um die Metriken auszublenden und sie auch aus allen abgeleiteten Metriken zu entfernen, die die Metriken enthalten.

<!--
>[!MORELIKETHIS]
>
>* 
-->
