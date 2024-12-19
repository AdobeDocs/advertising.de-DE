---
title: Ändern der Konversionsmetriken, die in Verwaltungsansichten und -berichten verfügbar sind
description: Erfahren Sie, wie Sie Konversionsmetriken in Ihren Verwaltungsansichten und -berichten verfügbar machen.
feature: Conversions
exl-id: de3d288a-5fec-4479-92cf-7754390e21bb
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Ändern der Konversionsmetriken, die in Verwaltungsansichten und -berichten verfügbar sind

Wenn Adobe Advertising für einen Advertiser eine [Konversions](/help/search-social-commerce/glossary.md#c-d)-Metrik nachverfolgt, ist sie zunächst von Portfoliozielen, Berichten und Verwaltungsansichten ausgeschlossen. Um eine Konversionsmetrik sichtbar zu machen, müssen Sie sie explizit verfügbar machen und dann optional den standardmäßigen Anzeigenamen ändern, d. h. den angezeigten Namen. Die einzige Ausnahme besteht darin, dass Konversionen, die von [!DNL Google Ads], [!DNL Google Analytics] und [!DNL Microsoft Advertising] universellen Ereignisverfolgungs-Tags verfolgt werden, automatisch verfügbar und sichtbar sind.

Ebenso können Sie eine Konversionsmetrik aus Portfoliozielen, Berichten und Verwaltungsansichten ausblenden. Wenn Sie eine Konversionsmetrik ausblenden, die zuvor sichtbar war, wird sie aus allen abgeleiteten Metriken entfernt, die die Konversionsmetrik enthalten.

Aus der Liste der verfügbaren Konversionsmetriken kann jeder Benutzer mit Zugriff auf die Daten des Werbetreibenden die Metriken anpassen, die er für Verwaltungsansichten und -berichte ansieht, einschließlich oder ohne Angabe bestimmter Metriken je nach Wahl.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   Es werden alle Konversionsmetriken aufgelistet, die für den Advertiser erfasst wurden, sowie alle anderen Namen, die für die Anzeige angegeben wurden.

1. (Optional) Filtern Sie die Liste:

   * Um nach einem bestimmten Metriknamen oder Anzeigenamen zu suchen, klicken Sie auf ![Suchen](/help/search-social-commerce/assets/search.png "Suchen"), geben Sie das Wort oder die Zeichenfolge in das Eingabefeld ein und drücken Sie dann die **[!DNL Enter]**.

     Sie können nach Zeichenfolgen suchen, die an einer beliebigen Stelle innerhalb des Satzes erscheinen (z. B. der erste Buchstabe oder die letzten drei Buchstaben), wobei bei den Suchbegriffen nicht zwischen Groß- [ Kleinschreibung unterschieden ](/help/search-social-commerce/glossary.md#c-d).

   * Um nach Konversionsmetriken anhand ihrer Verfügbarkeit in Verwaltungsansichten und Berichten zu suchen, klicken Sie auf ![Filter](/help/search-social-commerce/assets/filter.png "Filter") und wählen Sie die **[!UICONTROL Show in UI and Reports]** aus. Wählen Sie dann entweder **[!UICONTROL Show]** (um die verfügbaren Konversionsmetriken anzuzeigen, die in Berichte und Verwaltungsansichten aufgenommen werden können) oder **[!UICONTROL Hide]** (um die Konversionsmetriken anzuzeigen, die nicht in Berichten und Verwaltungsansichten verfügbar sind).

1. Ändern der Konversionsmetriken, die für Verwaltungsansichten und -berichte verfügbar sind:

   * Um eine einzelne Metrik ein- oder auszublenden, klicken Sie in der Spalte **[!UICONTROL Show in UI and Reports]** auf den Umschalter, um die Einstellung zu ändern.

   * Gehen Sie wie folgt vor, um mehrere Metriken ein- oder auszublenden:

      1. Aktivieren Sie das Kontrollkästchen neben jeder Konversionsmetrik.

         Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

      1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Anzeigen](/help/search-social-commerce/assets/show.png "Anzeigen") um die Metriken anzuzeigen oder ![Ausblenden](/help/search-social-commerce/assets/hide.png "Ausblenden"), um die Metriken auszublenden.

      1. (Um Metriken auszublenden) Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Yes]** , um die Metriken auszublenden und sie auch aus allen abgeleiteten Metriken zu entfernen, die die Metriken enthalten.

1. (Optional) [Ändern Sie den Namen, der in den Spaltenüberschriften angezeigt wird](conversion-metric-edit-display-name.md) für eine der Konversionsmetriken.

   Der standardmäßige Anzeigename für jede sichtbare Konversionsmetrik ist der Metrikname, wie er in den abgerufenen Daten geschrieben ist.

>[!NOTE]
>
>Wenn Adobe Advertising Daten für neue Konversionsmetriken erfasst, werden die neuen Metriken - mit Ausnahme der Konversionen, die von [!DNL Google Ads], [!DNL Google Analytics] und [!DNL Microsoft Advertising] universellen Ereignisverfolgungs-Tags verfolgt werden - automatisch aus den Verwaltungsansichten und -berichten ausgeschlossen, bis Sie sie einbeziehen. Neue Konversionen, die von [!DNL Google Ads], [!DNL Google Analytics] und [!DNL Microsoft Advertising] universellen Ereignis-Tracking-Tags verfolgt werden, sind immer automatisch verfügbar.

>[!MORELIKETHIS]
>
>* [Über die Verwaltung der Konversionsmetriken eines Werbetreibenden](conversion-metric-about.md)
>* [Anzeigen der für einen Advertiser verfolgten Konversionsmetriken](conversion-metric-view-tracked.md)
>* [Ändern des Anzeigenamens für eine Konversionsmetrik](conversion-metric-edit-display-name.md)
