---
title: Ändern der in Verwaltungsansichten und Berichten verfügbaren Konversionsmetriken
description: Erfahren Sie, wie Sie Konversionsmetriken in Ihren Management-Ansichten und -Berichten verfügbar machen.
feature: Conversions
exl-id: de3d288a-5fec-4479-92cf-7754390e21bb
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Ändern der in Verwaltungsansichten und Berichten verfügbaren Konversionsmetriken

Wenn Adobe Advertising eine [Konversionsmetrik](/help/search-social-commerce/glossary.md#c-d) für einen Advertiser verfolgt, wird sie zunächst aus Portfoliozielen, Berichten und Verwaltungsansichten ausgeschlossen. Um eine Konversionsmetrik sichtbar zu machen, müssen Sie sie explizit verfügbar machen und dann optional den standardmäßigen Anzeigenamen ändern, der den angezeigten Namen darstellt. Die einzige Ausnahme besteht darin, dass Konversionen, die von den universellen Ereignis-Tracking-Tags [!DNL Google Ads], [!DNL Google Analytics] und [!DNL Microsoft Advertising] verfolgt werden, automatisch verfügbar und sichtbar sind.

Auf ähnliche Weise können Sie eine Konversionsmetrik aus Portfoliozielen, Berichten und Managementansichten ausblenden. Wenn Sie eine Konversionsmetrik ausblenden, die zuvor sichtbar war, wird sie aus allen abgeleiteten Metriken entfernt, die die Konversionsmetrik enthalten.

Aus der Liste der verfügbaren Konversionsmetriken kann jeder Benutzer mit Zugriff auf die Daten des Advertisers die Metriken anpassen, die er für Verwaltungsansichten und Berichte sieht, einschließlich oder Nichtberücksichtigung bestimmter Metriken bei seiner Auswahl.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   Alle Konversionsmetriken, die für den Advertiser erfasst wurden, sowie alle anderen Namen, die für die Anzeige angegeben wurden, werden aufgelistet.

1. (Optional) Filtern Sie die Liste:

   * Um nach einem bestimmten Metriknamen oder Anzeigenamen zu suchen, klicken Sie auf ![Suchen](/help/search-social-commerce/assets/search.png "Suchen") , geben Sie das Wort oder die Zeichenfolge in das Eingabefeld ein und drücken Sie dann die Taste **[!DNL Enter]**.

     Sie können nach Zeichenfolgen suchen, die an einer beliebigen Stelle im Satz vorkommen (z. B. im ersten oder in den letzten drei Buchstaben), und bei den Suchbegriffen wird nicht zwischen [Groß- und Kleinschreibung unterschieden](/help/search-social-commerce/glossary.md#c-d).

   * Um nach Konversionsmetriken nach ihrer Verfügbarkeit in Verwaltungsansichten und Berichten zu suchen, klicken Sie auf ![Filter](/help/search-social-commerce/assets/filter.png "Filter") und wählen Sie den Filter **[!UICONTROL Show in UI and Reports]** aus. Wählen Sie dann entweder &quot;**[!UICONTROL Show]**&quot;(um die Konversionsmetriken anzuzeigen, die in Berichte und Verwaltungsansichten aufgenommen werden können) oder &quot;**[!UICONTROL Hide]**&quot;(um die Konversionsmetriken anzuzeigen, die in Berichten und Verwaltungsansichten nicht verfügbar sind).

1. Ändern Sie die für Verwaltungsansichten und Berichte verfügbaren Konversionsmetriken:

   * Um eine einzelne Metrik ein- oder auszublenden, klicken Sie auf den Schalter in der Spalte **[!UICONTROL Show in UI and Reports]** , um die Einstellung zu ändern.

   * Gehen Sie wie folgt vor, um mehrere Metriken ein- oder auszublenden:

      1. Aktivieren Sie das Kontrollkästchen neben den einzelnen Konversionsmetriken.

         Tipps zum Auswählen mehrerer Zeilen finden Sie unter &quot;[Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Anzeigen](/help/search-social-commerce/assets/show.png "Anzeigen") , um die Metriken anzuzeigen, oder auf ![Ausblenden](/help/search-social-commerce/assets/hide.png "Ausblenden") , um die Metriken auszublenden.

      1. (Um Metriken auszublenden) Klicken Sie in der Bestätigungsmeldung auf &quot;**[!UICONTROL Yes]**&quot;, um die Metriken auszublenden. So können Sie sie auch aus allen abgeleiteten Metriken entfernen, die die Metriken enthalten.

1. (Optional) [Ändern Sie den Namen, der in Spaltenüberschriften angezeigt wird](conversion-metric-edit-display-name.md) für eine der Konversionsmetriken.

   Der standardmäßige Anzeigename für jede sichtbare Konversionsmetrik ist der Metrikname, wie er in den abgerufenen Daten geschrieben ist.

>[!NOTE]
>
>Wenn Adobe Advertising Daten für neue Konversionsmetriken erfasst, werden die neuen Metriken - mit Ausnahme der Konversionen, die von den Verfolgungstags [!DNL Google Ads], [!DNL Google Analytics] und [!DNL Microsoft Advertising] für universelle Ereignisse verfolgt werden - automatisch aus Verwaltungsansichten und Berichten ausgeschlossen, bis Sie sie einbeziehen. Neue Konversionen, die von den universellen Ereignisverfolgungstags [!DNL Google Ads], [!DNL Google Analytics] und [!DNL Microsoft Advertising] verfolgt werden, sind immer automatisch verfügbar.

>[!MORELIKETHIS]
>
>* [Über die Verwaltung der Konversionsmetriken eines Advertisers](conversion-metric-about.md)
>* [Anzeigen der für einen Advertiser verfolgten Konversionsmetriken](conversion-metric-view-tracked.md)
>* [Anzeigenamen für eine Konversionsmetrik ändern](conversion-metric-edit-display-name.md)
