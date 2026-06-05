---
title: Konversionsmetriken eines Werbetreibenden verwalten
description: Erfahren Sie, wie Sie die Konversionsmetriken verwenden können, die Adobe Advertising für einen Advertiser verfolgt.
feature: Conversions
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
subfeature_v2:
  - id: d068b149-b9d1-421c-9033-a51495366ddc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: b9388f691c8e804cece8d9f1eeb1bdc4f352dd11
workflow-type: tm+mt
source-wordcount: 932
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Verwalten der Konversionsmetriken eines Werbetreibenden

*Beta-Funktion*

Die Metriken [Konversion](/help/search-social-commerce/glossary.md#c-d) eines Advertisers werden in Adobe Advertising verwendet:

* In Search, Social und Commerce können Daten für Konversionsmetriken in Spalten in Kampagnen-, Portfolio- und Zielgruppen-Management-Ansichten und in Berichten angezeigt werden. Benutzer mit ausreichenden Zugriffsberechtigungen können Konversionsmetriken auch verwenden, um Ziele zu erstellen, die zur Optimierung von Portfolios verwendet werden.

* (Werbetreibende mit Advertising DSP) In DSP können Sie Konversionsmetriken in Kampagnenverwaltungsansichten, benutzerdefinierte Ziele und benutzerdefinierte Berichte aufnehmen. Sie können Konversionsmetriken auch verwenden, um [benutzerdefinierte Ziele](/help/dsp/admin/custom-objectives-manage.md) zu erstellen, die zur Optimierung von Paketen verwendet werden.

Zu den verfügbaren Metriken gehören:

* Konversionsmetriken, die Adobe Advertising für einen Advertiser verfolgt.

* [Konversions- und Site-Interaktionsmetriken wurden aus Adobe Analytics synchronisiert](/help/integrations/analytics/analytics-data-in-advertising.md).

* [Site-Ereignisse, die mit Adobe Customer Journey Analytics synchronisiert &#x200B;](/help/integrations/customer-journey-analytics/overview.md).

* Konversionen, die von [!DNL Google Ads] verfolgt werden, und Konversionen, die von [!DNL Microsoft Advertising] universellen Ereignisverfolgungstags verfolgt werden.

* ([&#x200B; Sie eine bestimmte Kombination aus  [!DNL Google Analytics] , Eigenschaft und Ansicht als Datenquelle konfiguriert haben](/help/search-social-commerce/admin/data-sources/data-source-about.md) für Search, Social und Commerce) Konversionen von [!DNL Google Analytics] verfolgt.

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
>Bei [Metriken von [!DNL Google Analytics]](/help/search-social-commerce/admin/data-sources/data-source-about.md) werden alle manuellen Änderungen am Anzeigenamen überschrieben, wenn Sie die Integration aktualisieren oder erneut authentifizieren. Ebenso werden alle Namensänderungen in [!DNL Google Analytics] ignoriert, es sei denn, Sie [&#x200B; die Integration &#x200B;](/help/search-social-commerce/admin/data-sources/data-source-edit.md) oder [erneut &#x200B;](/help/search-social-commerce/admin/data-sources/data-source-reauthenticate.md).

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

## Verwalten der Konversionssichtbarkeit und der Quellberichte

Sie können die folgenden Informationen zu Ihren verfolgten Konversionen herunterladen: den Namen der synchronisierten Metrik, den Anzeigenamen für die Metrik in den Verwaltungsansichten und -berichten für Suche, Social Media und Commerce, ob die Metrik in Verwaltungsansichten und -berichten sichtbar ist, die Konversions-ID und die Metrikquelle. Laden Sie die Daten in eine Datei [!DNL Microsoft Excel] Arbeitsmappen-Format (XLSX-Datei) herunter.

### Erstellen eines Berichts mit den gefilterten Datenzeilen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Geben Sie die Konversionen an, deren Daten Sie herunterladen möchten:

   * Um Daten für bestimmte Zeilen herunterzuladen, aktivieren Sie die Kontrollkästchen neben den Zeilen.

   * Um Daten für alle Zeilen herunterzuladen, müssen Sie keine Kontrollkästchen aktivieren. Alle Zeilen sind standardmäßig eingeschlossen.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ")**[!UICONTROL Reports]**.

1. Geben Sie in den [!UICONTROL Grid Reports] einen eindeutigen Berichtsnamen ein, und klicken Sie dann auf **[!UICONTROL Generate]**.

   Standardmäßig trägt die Datei den Namen „conversionReport_YYYYMMDD_NNNN“, wobei „NNNN“ die sequenzielle Auftragsnummer ist (z. B. „conversionsReport_20260402_1326).

   Die Datei wird der [!UICONTROL Recently Generated] hinzugefügt.

1. (Optional) Um die Datei nach Abschluss des Vorgangs herunterzuladen, klicken Sie ![Herunterladen](/help/search-social-commerce/assets/download.png "Herunterladen") neben dem Dateinamen.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

### Herunterladen eines abgeschlossenen Berichts

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ")**[!UICONTROL Reports]**.

1. Klicken Sie in der [!UICONTROL Recently Generated] im [!UICONTROL Grid Reports] auf ![Herunterladen](/help/search-social-commerce/assets/download.png "Herunterladen") neben dem Dateinamen.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

### Löschen eines abgeschlossenen Berichts

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Herunterladen](/help/search-social-commerce/assets/download.png "Herunterladen") **[!UICONTROL Reports]**.

1. Klicken Sie in der [!UICONTROL Recently Generated] im [!UICONTROL Grid Reports] auf ![Löschen](/help/search-social-commerce/assets/delete-new.png "Löschen") neben dem Dateinamen.

<!--
>[!MORELIKETHIS]
>
>* 
-->
