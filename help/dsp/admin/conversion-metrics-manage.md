---
title: Verwalten der Konversionsmetriken eines Advertisers in DSP.
description: Erfahren Sie, wie Sie die Konversionsmetriken verwenden können, die Adobe Advertising für einen DSP-Advertiser verfolgt.
feature: Conversions
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Konversionsmetriken eines Werbetreibenden verwalten

Die Konversionsmetriken eines Advertisers werden in Adobe Advertising verwendet:

* In Advertising DSP können Sie Konversionsmetriken in Kampagnenverwaltungsansichten, benutzerdefinierte Ziele und benutzerdefinierte Berichte einbeziehen. Sie können auch Konversionsmetriken eines Advertisers verwenden, um [benutzerdefinierte Ziele](/help/dsp/admin/custom-objectives-manage.md) zu erstellen, die zur Optimierung von Paketen verwendet werden.

* (Werbetreibende mit Advertising Search, Social und Commerce) In Search, Social und Commerce können Daten für Konversionsmetriken in Spalten in Kampagnen-, Portfolio- und Zielgruppen-Management-Ansichten und in Berichten angezeigt werden. Benutzer mit ausreichenden Zugriffsberechtigungen können Konversionsmetriken auch verwenden, um Ziele zu erstellen, die zur Optimierung von Portfolios verwendet werden.

<!--
The conversion metrics that Adobe Advertising tracks for an advertiser &mdash; including [conversion and site engagement metrics synced from Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md), [site events synced from Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md), and custom feeds &mdash; are used throughout Advertising DSP. You can include conversion metrics in campaign management views, custom objectives, and custom reports. You can also use conversion metrics to create [custom objectives](/help/dsp/admin/custom-objectives-manage.md), which are used to optimize packages.

By default, none of an advertiser's conversion metrics are available for campaign management views, custom objectives, and reports. They are available only when you specifically make them available. When you make a conversion metric available, you can either use the metric name exactly as it is spelled in the retrieved data or change the display name that's shown in column headings for readability.

From the list of visible metrics, each user with access to the advertiser's data can customize the metrics they see for campaign management views, objectives, and reports by including or omitting specific metrics. Users with sufficient access privileges can also optimize for specific metrics by associating them with DSP package-level custom goals.

-->

Zu den für DSP-Benutzende verfolgten Metriktypen gehören:

* Konversionsmetriken, die Adobe Advertising für einen Advertiser verfolgt.

* [Konversions- und Site-Interaktionsmetriken wurden aus Adobe Analytics synchronisiert](/help/integrations/analytics/analytics-data-in-advertising.md).

* [Site-Ereignisse, die mit Adobe Customer Journey Analytics synchronisiert ](/help/integrations/customer-journey-analytics/overview.md).

* Konversionen aus benutzerdefinierten Feeds.

Aus der Liste der verfügbaren Konversionsmetriken kann jeder Benutzer mit Zugriff auf die Daten des Werbetreibenden die Metriken anpassen, die für Verwaltungsansichten und Berichte verfügbar sind, einschließlich oder ohne Angabe bestimmter Metriken. Sie können entweder einen Metriknamen genau so verwenden, wie er in den abgerufenen Daten geschrieben ist, oder den Namen ändern, der in den Spaltenüberschriften angezeigt wird, um die Lesbarkeit zu verbessern.

>[!IMPORTANT]
>
>Standardmäßig ist keine der Konversionsmetriken eines Advertisers zur Aufnahme in Kampagnenverwaltungsansichten, benutzerdefinierte Ziele und benutzerdefinierte Berichte verfügbar. Um eine Konversionsmetrik verfügbar zu machen, müssen Sie sie explizit verfügbar machen.

>[!TIP]
>
>Sobald der Advertiser (oder das Werbenetzwerk) die Erfassung einer Konversionsmetrik beendet hat, [blenden Sie sie aus den Verwaltungsansichten und Berichten aus](#conversion-metrics-change-available) es sei denn, Sie möchten sie für die Anzeige historischer Daten verwenden.

## Anzeigen der für einen Advertiser verfolgten Konversionsmetriken

* Klicken Sie im Hauptmenü auf **[!UICONTROL Settings]>[!UICONTROL Conversions Beta]**.

Es werden alle für den Advertiser erfassten Konversionsmetriken und alle ihnen zugewiesenen Anzeigenamen aufgelistet. Jede Metrikzeile enthält die Quelle der Metrik.

## Anzeigenamen für eine Konversionsmetrik ändern

Wenn Sie beispielsweise Registrierungsdaten mithilfe einer Konversionsmetrik mit dem Namen *reg* erfassen, können Sie optional den Anzeigenamen ändern, damit er als „Registrierungen“ angezeigt wird.

Ein vorhandener Anzeigename kann nicht gelöscht werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Settings]>[!UICONTROL Conversions Beta]**.

1. Halten Sie den Cursor über der Zeile und klicken Sie auf **[!UICONTROL Edit Display Name]**.

1. Geben Sie den Namen ein, der angezeigt werden soll, und klicken Sie dann auf **[!UICONTROL Save]**.

   Anzeigenamen müssen eindeutig sein und dürfen die folgenden Sonderzeichen nicht enthalten: `\"<'>&`

## Ändern der Konversionsmetriken, die in Kampagnenverwaltungsansichten, benutzerdefinierten Zielen und benutzerdefinierten Berichten verfügbar sind {#change-the-conversion-metrics-available-in-ui}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Settings]>[!UICONTROL Conversions]**.

   Es werden alle Konversionsmetriken aufgelistet, die für den Advertiser erfasst wurden, sowie alle anderen Namen, die für die Anzeige angegeben wurden.

1. (Optional) Filtern Sie die Liste:

   1. Klicken Sie über der Liste auf ![Filter](/help/dsp/assets/filter.png "Filter").

   1. Geben Sie die Filter an und klicken Sie dann auf **[!DNL Apply]**.

      Sie können die Metriken nach der AMO-Client-ID, danach, ob die Metriken in der Benutzeroberfläche sichtbar oder ausgeblendet sind, und nach Datenquelle filtern.

1. Ändern der Konversionsmetriken, die für Verwaltungsansichten und -berichte verfügbar sind:

   * Um eine Metrik anzuzeigen, halten Sie den Cursor über der Zeile und klicken Sie auf **[!UICONTROL Show in UI and Reports]**.

   * Um eine Metrik auszublenden, halten Sie den Cursor über der Zeile und klicken Sie auf **[!UICONTROL Hide in UI and Reports]**.

>[!MORELIKETHIS]
>
>* [Kampagnendaten-Ansichten verwalten](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [Benutzerdefinierte Ziele verwalten](/help/dsp/admin/custom-objectives-manage.md)
