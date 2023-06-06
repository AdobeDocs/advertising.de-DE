---
title: Ändern der in Verwaltungsansichten und -berichten verfügbaren Transaktionseigenschaften
description: Erfahren Sie, wie Sie Transaktionseigenschaften in Ihren Verwaltungsansichten und -berichten verfügbar machen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# Ändern der in Verwaltungsansichten und -berichten verfügbaren Transaktionseigenschaften

Wenn Adobe Advertising eine [Transaktionseigenschaft](/help/search-social-commerce/glossary.md#s-t) für einen Advertiser zunächst aus Portfoliozielen, Berichten und Managementansichten ausgeschlossen. Um eine Eigenschaft sichtbar zu machen, müssen Sie sie explizit verfügbar machen und dann optional den standardmäßigen Anzeigenamen ändern, d. h. den angezeigten Namen. Die einzige Ausnahme ist, dass Konversionen verfolgt werden durch [!DNL Google Ads], [!DNL Google Analytics]und [!DNL Microsoft® Advertising] universelle Ereignis-Tracking-Tags sind automatisch verfügbar und sichtbar.

Auf ähnliche Weise können Sie eine Eigenschaft aus Portfoliozielen, Berichten und Managementansichten ausblenden. Wenn Sie eine Eigenschaft ausblenden, die zuvor sichtbar war, wird sie aus allen abgeleiteten Metriken entfernt, die die Eigenschaft enthalten.

Aus der Liste der verfügbaren Eigenschaften kann jeder Benutzer mit Zugriff auf die Daten des Advertisers die Eigenschaften anpassen, die er für Verwaltungsansichten und Berichte sieht, einschließlich oder Nichtberücksichtigung bestimmter Eigenschaften nach Wahl.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.

   Alle Transaktionseigenschaften, die für den Advertiser gesammelt wurden, sowie alle anderen Namen, die für die Anzeige angegeben wurden, werden aufgelistet.

1. (Optional) Filtern Sie die Liste:

   * Um nach einem bestimmten Eigenschaftsnamen oder Anzeigenamen zu suchen, klicken Sie auf ![Suche](/help/search-social-commerce/assets/search.png "Suche"), geben Sie das Wort oder die Zeichenfolge in das Eingabefeld ein und drücken Sie dann die **[!DNL Enter]** Schlüssel.

      Sie können nach Zeichenfolgen suchen, die an einer beliebigen Stelle im Satz vorkommen (z. B. im ersten oder in den letzten drei Buchstaben), und die Suchbegriffe werden nicht [Groß-/Kleinschreibung beachten](/help/search-social-commerce/glossary.md#c-d).

   * Um in Verwaltungsansichten und Berichten nach Eigenschaften zu suchen, klicken Sie auf ![Filter](/help/search-social-commerce/assets/filter.png "Filter")und wählen Sie den Filter aus **[!UICONTROL Show in UI and Reports]**. Wählen Sie anschließend **[!UICONTROL Show]** (um die verfügbaren Eigenschaften anzuzeigen, die in Berichte und Verwaltungsansichten aufgenommen werden können) oder **[!UICONTROL Hide]** (um die Eigenschaften anzuzeigen, die in Berichten und Verwaltungsansichten nicht verfügbar sind).

1. Ändern Sie die für Verwaltungsansichten und Berichte verfügbaren Eigenschaften:

   * Um eine einzelne Eigenschaft ein- oder auszublenden, klicken Sie auf den Schalter im **[!UICONTROL Show in UI and Reports]** -Spalte, um die Einstellung zu ändern.

   * Gehen Sie wie folgt vor, um mehrere Eigenschaften ein- oder auszublenden:

      1. Aktivieren Sie das Kontrollkästchen neben jeder Eigenschaft.

         Tipps zur Auswahl mehrerer Zeilen finden Sie unter[Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Anzeigen](/help/search-social-commerce/assets/show.png "Anzeigen") zum Anzeigen der Eigenschaften oder ![Ausblenden](/help/search-social-commerce/assets/hide.png "Ausblenden") um die Eigenschaften auszublenden.

      1. (Um Eigenschaften auszublenden) Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Yes]** um die Eigenschaften auszublenden, einschließlich des Entfernens aus allen abgeleiteten Metriken, die die Eigenschaften enthalten.

1. (Optional) [Ändern des Namens, der in Spaltenüberschriften angezeigt wird](transaction-property-edit-display-name.md) für eine der Eigenschaften.

   Der standardmäßige Anzeigename für jede sichtbare Eigenschaft ist der Eigenschaftsname, wie er in den abgerufenen Daten geschrieben ist.

>[!NOTE]
>
>Wenn Adobe Advertising Daten für neue Eigenschaften erfasst, dann die neuen Eigenschaften — mit Ausnahme der Konversionen, die von verfolgt werden [!DNL Google Ads], [!DNL Google Analytics]und [!DNL Microsoft® Advertising] universelle Ereignis-Tracking-Tags - werden automatisch von Management-Ansichten und -Berichten ausgeschlossen, bis Sie sie einschließen. Neue Konversionen verfolgt von [!DNL Google Ads], [!DNL Google Analytics]und [!DNL Microsoft® Advertising] universelle Ereignis-Tracking-Tags sind immer automatisch verfügbar.

>[!MORELIKETHIS]
* [Über die Verwaltung der Transaktionseigenschaften eines Advertisers](transaction-property-about.md)
* [Anzeigen der für einen Advertiser verfolgten Transaktionseigenschaften](transaction-property-view-tracked.md)
* [Anzeigenamen für eine Transaktionseigenschaft ändern](transaction-property-edit-display-name.md)

