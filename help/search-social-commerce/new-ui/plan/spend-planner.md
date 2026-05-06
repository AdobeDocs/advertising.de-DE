---
title: Verwenden der [!UICONTROL Spend Planner]
description: Erfahren Sie, wie Sie Empfehlungen für Portfoliobudgets generieren, herunterladen und anwenden können, um eine optimale Verteilung der Ausgaben über Ihre Portfolios zu erreichen.
feature: Search Optimization, Search Portfolios
exl-id: 966b8968-68b6-4385-9efb-e639a6729362
TQID: https://experienceleague.adobe.com/8BAQij06MRhxYoCoFNjhHsgC4o38lQnj9vpmTzYyqGg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: c3664a71f39c9a45fad739fdf4805c9862c69915
workflow-type: tm+mt
source-wordcount: 801
ht-degree: 0%

---

# Verwenden der [!UICONTROL Spend Planner]

Die [!UICONTROL Spend Planner] (in der alten Benutzeroberfläche als &quot;[!UICONTROL Spend Recommendation Tool]&quot; bezeichnet) identifiziert die optimale Ausgabenverteilung über optimierte und aktive Portfolios mit demselben Ziel und derselben Währung, sodass Sie den Umsatz maximieren oder Ziele für das Portfolio-Set anstreben können.

Wenn Sie einen Bericht mit Ausgabenempfehlungen für Portfolios mit täglichen Budgets anzeigen, können Sie die Budgets für jedes der Portfolios in die empfohlenen Budgets ändern.

## Daten im [!UICONTROL Spend Planner]

Für Portfolios mit dem Ziel [!UICONTROL Maximize Clicks] enthält der Bericht Ausgabenempfehlungen und Klickprognosen. Für alle anderen Ziele enthält der Bericht Ausgabenempfehlungen und Einnahmenprojektionen.

Die Berichte über Ausgabenempfehlungen enthalten die folgenden Daten:

* Ein Streudiagramm zeigt den prognostizierten maximalen Umsatz oder die Klicks, die mit einer bestimmten Gesamtkosten für das Portfolio erzielt werden können, die festgelegt werden, wenn die einzelnen Ausgabenziele optimal festgelegt werden. Die prognostizierten Kosten für jeden Umsatzpunkt oder Klickpunkt sind enthalten.

* Zwei Ringdiagramme, die die Ausgaben und den erwarteten Umsatz anzeigen, oder Klick-Verteilung nach Portfolio für 1\) die aktuellen Ausgabenziele und 2\) die vorgeschlagenen Ausgabenziele.

* Ein Balkendiagramm für jedes der Portfolios, das die empfohlenen täglichen Ausgaben (Kosten) und die prognostizierte Umsatzverteilung oder Klick-Verteilung anzeigt, wenn Sie das aktuelle Ziel für die gesamten täglichen Ausgaben für alle ausgewählten Portfolios oder für ein vorgeschlagenes Ziel für die Gesamtausgaben beibehalten. Sie können optional die empfohlenen Ausgabenziele auf die ausgewählten Portfolios anwenden, was sich auf die Gebote im nächsten Angebotsausführungszyklus auswirkt.

## Verfügbare Aktionen

* Generieren eines [!UICONTROL Spend Planner] Berichts über die [neue Benutzeroberfläche](#spend-recommendations-generate) oder [veraltete Benutzeroberfläche](#spend-recommendations-generate-legacy)

* [Wenden Sie Ausgabenempfehlungen &#x200B;](#spend-recommendations-apply) die entsprechenden Portfolios an.

* [Öffnen oder Speichern von Berichtsdaten zu Ausgabenempfehlungen in einer Datei](#spend-recommendations-download)

## (Neue Benutzeroberfläche) Erstellen eines [!UICONTROL Spend Planner] Berichts {#spend-recommendations-generate}

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken Sie im Hauptmenü auf **[!UICONTROL Plan]>[!UICONTROL Spend Planner]**.

   * Klicken Sie im Hauptmenü auf **[!UICONTROL Plan]>[!UICONTROL Simulations]**. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Ausgabenplaner](/help/search-social-commerce/assets/spend-planner-icon.png "Ausgabenplaner").

   Das [!UICONTROL Spend Recommendation]-Tool wird in der Benutzeroberfläche der veralteten Version geöffnet.

1. Zeigen Sie Daten unter Verwendung der aktuellen, kombinierten Budgets für die ausgewählten Portfolios an:

   1. Wählen Sie das Ziel des Portfolios aus.

   1. Währung auswählen.

   1. (Optional) Wählen Sie eine Portfolio-Ausgabenstrategie aus, um die Portfolioliste weiter zu filtern.

   1. Aktivieren Sie das Kontrollkästchen neben jedem einzuschließenden Portfolio. Um alle Portfolios auszuwählen, aktivieren Sie das Kontrollkästchen neben [!UICONTROL Portfolios].

      Es werden nur optimierte und aktive Portfolios mit den ausgewählten Parametern aufgelistet.

   1. Klicken Sie auf **[!UICONTROL Update]**.

   1. (Optional) Halten Sie den Cursor über den Punkt, um die Kosten und den Umsatz für einen beliebigen Punkt im Diagramm anzuzeigen.

1. (Optional) Um das empfohlene Ziel für die täglichen Ausgaben und den erwarteten Umsatz für jedes der Portfolios unter Verwendung eines anderen Ziels für die Gesamtausgaben anzuzeigen, geben Sie ein vorgeschlagenes Ziel für die täglichen Ausgaben für alle Portfolios im Feld [!UICONTROL Total Spend Target] ein. Drücken Sie dann die **Eingabetaste**.

   Das Tool für Ausgabenempfehlungen verwendet Daten aus wöchentlichen Simulationen, sodass die insgesamt empfohlenen Ausgaben am ehesten dem von Ihnen vorgeschlagenen Ausgabenziel mit dem idealen Ausgabenmix entsprechen.

<!--

New UI; validate post-Update steps once I get it to generate a report:

## Generate a spend recommendation report {#spend-recommendations-generate}

1. In the main menu, click **[!UICONTROL Plan] > [!UICONTROL Spend Planner]**.

1. View data using the current, combined budgets for the selected portfolios:

   1. Click **[!UICONTROL Select Objective]**.

   1. Select the portfolio objective.

   1. Select the currency.

   1. (Optional) Select a portfolio spend strategy to further filter the portfolios list.

   1. Select the check box next to each portfolio to include.

      Only optimized and active portfolios with the selected parameters are listed.

   1. Click **[!UICONTROL Update]**.

   1. (Optional) To see the cost and revenue for any point on the chart, hold the cursor over the point.

1. (Optional) To download the proposed allocation and expected revenue per portfolio, click ![Download](/help/search-social-commerce/assets/download-spend-recommendation.png "Download") next to [!UICONTROL Portfolio Allocation] in the right column.

   Open or save the file according to your browser's normal procedure. For more information, see your browser's online help.

1. (Optional) To view the recommended daily spend and expected revenue for each of the portfolios using a different total spend target, enter a proposed total daily spend target across all portfolios in the [!UICONTROL Total Spend Target] field. Then press the **Enter** key.

   The spend recommendation tool uses data from weekly simulations, so the total recommended spend is the closest match to your proposed spend target with the ideal spend mix.

-->

## (Alte Benutzeroberfläche) Generieren eines [!UICONTROL Spend Recommendation] Berichts über die Ansicht [!UICONTROL Optimization] > [!UICONTROL Spend Recommendation] {#spend-recommendations-generate-legacy}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Optimization] >[!UICONTROL Spend Recommendation]**.

1. Zeigen Sie Daten unter Verwendung der aktuellen, kombinierten Budgets für die ausgewählten Portfolios an:

   1. Wählen Sie das Ziel des Portfolios aus.

   1. Währung auswählen.

   1. (Optional) Wählen Sie eine Portfolio-Ausgabenstrategie aus, um die Portfolioliste weiter zu filtern.

   1. Aktivieren Sie das Kontrollkästchen neben jedem einzuschließenden Portfolio. Um alle Portfolios auszuwählen, aktivieren Sie das Kontrollkästchen neben [!UICONTROL Portfolios].

      Es werden nur optimierte und aktive Portfolios mit den ausgewählten Parametern aufgelistet.

   1. Klicken Sie auf **[!UICONTROL Update]**.

   1. (Optional) Halten Sie den Cursor über den Punkt, um die Kosten und den Umsatz für einen beliebigen Punkt im Diagramm anzuzeigen.

1. (Optional) Um die empfohlenen täglichen Ausgaben und die prognostizierten Einnahmen für jedes der Portfolios unter Verwendung eines neuen Gesamtausgabenziels anzuzeigen, geben Sie ein vorgeschlagenes Ziel für die gesamten täglichen Ausgaben für alle Portfolios im Feld [!UICONTROL Total Spend Target] ein. Drücken Sie dann die **Eingabetaste**.

   Das Tool für Ausgabenempfehlungen verwendet Daten aus wöchentlichen Simulationen, sodass die insgesamt empfohlenen Ausgaben am ehesten dem von Ihnen vorgeschlagenen Ausgabenziel mit dem idealen Ausgabenmix entsprechen.

<!--
## (New UI) Apply spend recommendations {#spend-recommendations-apply}

*Portfolios with daily budgets only*

>[!NOTE]
>
>* If the applied changes will increase or decrease the spend target of any portfolio by more than 20%, you must approve the change.
>* When the spend target for a portfolio changes by more than 20%, Search, Social, & Commerce takes up to 3-4 days to adjust its models and achieve the new target.

1. [Generate a spend recommendation report](#spend-recommendations-generate) for one or more portfolios with daily budgets.

1. Select the check box next to each portfolio for which you want to apply the recommended spend target. To select all portfolios, select the check box next to **[!UICONTROL Select All Recommendations]**.

1. Click **[!UICONTROL Apply Selected Recommendations]**.

1. (If any of the budgets will change by more than 20%) In the confirmation message, click **[!UICONTROL Confirm]** to approve the changes.

-->

## &#x200B;<!--(Legacy UI) -->Ausgabenempfehlungen anwenden {#spend-recommendations-apply-legacy}

*Portfolios nur mit Tagesbudgets*

>[!NOTE]
>
>* Wenn die angewendeten Änderungen das Ausgabenziel eines Portfolios um mehr als 20 % erhöhen oder senken, müssen Sie die Änderung genehmigen.
>* Wenn sich das Ausgabenziel für ein Portfolio um mehr als 20 % ändert, dauert Search, Social und Commerce bis zu 3-4 Tage, um die Modelle anzupassen und das neue Ziel zu erreichen.

1. [Bericht mit Ausgabenempfehlungen generieren](#spend-recommendations-generate-legacy) für ein oder mehrere Portfolios mit täglichen Budgets.

1. Aktivieren Sie das Kontrollkästchen neben jedem Portfolio, für das Sie das empfohlene Ausgabenziel anwenden möchten. Um alle Portfolios auszuwählen, aktivieren Sie das Kontrollkästchen neben **[!UICONTROL Select All Recommendations]**.

1. Klicken Sie auf **[!UICONTROL Apply Selected Recommendations]**.

1. (Wenn sich eines der Budgets um mehr als 20 % ändert) Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Yes]** , um die Änderungen zu genehmigen.

<!--

## (New UI) Open or save data as a [!DNL Microsoft Excel] workbook file {#spend-recommendations-download}

You can open or save data from either a) the line chart showing cost points and the expected revenue for each cost and b) the donut charts of the current and proposed media mix. [This seems to be identical to the Portfolio Allocation report -- how should these be different?]

1. [Generate a spend recommendation report](#spend-recommendations-generate) for selected portfolios.

1. Above the report, click ![Download](/help/search-social-commerce/assets/download-spend-recommendation.png "Download").

   Open or save the file according to your browser's normal procedure. For more information, see your browser's online help.

-->

<!--(Legacy UI) -->

## Öffnen oder Speichern von Daten als [!DNL Microsoft Excel] Arbeitsmappendatei {#spend-recommendations-download-legacy}

1. Erstellen Sie einen Bericht mit Ausgabenempfehlungen für ausgewählte Portfolios.

1. Klicken Sie oben rechts im Bericht auf ![Download](/help/search-social-commerce/assets/download-spend-recommendation.png "Download").

   Öffnen oder speichern Sie die Datei entsprechend dem normalen Verfahren Ihres Browsers. Weitere Informationen finden Sie in der Online-Hilfe Ihres Browsers.
