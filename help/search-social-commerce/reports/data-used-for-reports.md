---
title: Die für Berichte verwendeten Daten
description: Erfahren Sie mehr über die verschiedenen Datentypen, die in Datenansichten und benutzerdefinierten Berichten verfügbar sind.
exl-id: ba808b21-4421-4de5-9293-a20ec67cc81c
feature: Search Reports
source-git-commit: 840c7f6295b73a784725c301a78ae89c827fd45e
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# Die für Berichte verwendeten Daten

Search, Social und Commerce umfasst einen umfassenden Satz von Leistungsberichten, die auf Klick- und Konversionsdaten basieren. Sie können grundlegende Leistungsdaten für die verschiedenen Komponenten eines Portfolios oder Anzeigenkontos aus den Ansichten [!UICONTROL Portfolios] und [!UICONTROL Campaigns] anzeigen sowie verschiedene einfache und erweiterte Berichte generieren.

Werbetreibende, die den Adobe Advertising-Konversions-Tracking-Dienst verwenden, können auch die Anzahl der Klicks für einen geografischen Standort oder Domänennamen einer verweisenden Website identifizieren, wie Anzeigen in den einzelnen Kanälen und die verschiedenen Ereignisse, die zu einer Konversion führen, zur Gesamtkonversionsrate beitragen und die Verteilung der Konversionen für eine einzelne [Konversionsmetrik](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) nach Marketingkanälen. Die verfügbaren Berichte variieren je nach Benutzerkontotyp. Das Adobe Account Team hat Zugriff auf alle Berichte.

Die meisten Berichte können so angepasst werden, dass nur die Informationen angezeigt werden, die Sie sehen möchten. Die folgenden Standardmetriken sind in den meisten Berichten verfügbar und werden auf Anzeigenebene berechnet:

* **Standardmäßige Leistungsmetriken:**

   * **[!UICONTROL Impressions]:** Die Gesamtanzahl der Anzeigenplatzierungen.

   * **[!UICONTROL Clicks]:** Die Gesamtzahl der Klicks auf einen Link in der Anzeige.

   * **[!UICONTROL Cost]:** Die Gesamtkosten der Anzeige. Die Kosten für Pay-per-Click-Werbung (PPC) entsprechen immer der Anzahl der Klicks multipliziert mit den Kosten pro Klick.

   * **[!UICONTROL Cost per Click]:** Die durchschnittlichen Kosten für einen Klick für eine Anzeige, die den Kosten der Anzeige dividiert durch die Gesamtanzahl der Klicks für die Anzeige entspricht. Wenn Sie beispielsweise 100 USD für eine Anzeigenimpression ausgeben und die Anzeige 10 Klicks generiert, betragen die Kosten pro Klick 100 USD/10=10 USD pro Klick.

   * **[!UICONTROL Average Position]:** (Falls zutreffend) Die durchschnittliche Position einer Anzeige, die platziert wurde, gewichtet mit der Anzahl der Impressionen.

   * **[!UICONTROL Estimated Clicks]:** (In erweiterte Berichte für Advertiser mit dem Adobe Advertising-Konversions-Tracking-Dienst eingeschlossen) Die Gesamtanzahl der geschätzten Klicks für einen Ort oder Domänennamen einer verweisenden Website. Dies kann Daten für Werbenetzwerke umfassen, für die ein Werber kein Werbekonto hat.

* **Konversionsmetriken:** Die Gesamtzahl der Konversionen für jede der Konversionsmetriken des Advertisers oder der Transaktionsdaten, die zu einer Konversionsmetrik verfolgt wurden. Dazu können Konversions- und Site-Interaktionsmetriken, jedoch keine berechneten Metriken und erweiterte berechnete Metriken gehören, die aus Adobe Analytics synchronisiert werden.

  Dies kann auch [[!DNL Google Ads]-verfolgte Konversionen](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) und [[!DNL Google Analytics]-verfolgte Konversionen](/help/search-social-commerce/admin/data-sources/data-source-about.md) umfassen, die für das Advertiser-Konto synchronisiert werden.

* **Benutzerdefinierte Metriken:** Ihre eigenen Metriken, die Sie durch die Erstellung von Formeln auf der Grundlage vorhandener Metriken ableiten (z. B. Kosten pro Bestellung).

## Datenverfügbarkeit

Beim Generieren von Berichten können Sie festlegen, wie Konversionsdaten in einer Reihe von Ereignissen zugeordnet werden, die zu einer Konversion führen. Beispielsweise können Sie die gesamte Konversion dem letzten Ereignis zuordnen oder das letzte Ereignis stärker gewichten als die anderen. Standardmäßig werden Konversionen dem letzten Ereignis zugeordnet.

Je nach der für den Bericht festgelegten Attributionsregel stehen für die folgenden Daten Daten für die einzelnen Berichtstypen zur Verfügung.

| Berichtsgruppe | Bericht | Daten, für die Daten verfügbar sind |
|---|---|---|
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | Ab dem 15. Mai 2021.<br><br><b>Ausnahme:</b> Die Daten der Bekanntheitsmetriken sind ab dem 8. September 2022 verfügbar. |
| | Alle anderen [!UICONTROL Basic Reports] | Die letzten 36 Monate.<br><br><b>Ausnahme:</b> Die Daten der Bekanntheitsmetriken sind ab dem 8. September 2022 verfügbar. |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | Die letzten 45 Tage. |
| | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | Die beiden vorherigen (2) Monate plus der aktuelle Monat. |
| [!UICONTROL Assist Reports] | Alle | Die letzten 18 Monate. |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | Das Vorjahr. |
| | [!UICONTROL RSA Assets Report] | Ab 10. August 2022. |
| | [!UICONTROL MSA Ad Extension by Ad Report], [!UICONTROL MSA Ad Extension by Keyword Report], [!UICONTROL MSA Ad Extension Detail Report], [!UICONTROL MSA Network Impression Share Report], [!UICONTROL MSA Network Performance Report] | Die letzten 180 Tage. |
| | Alle anderen [!UICONTROL Specialty Reports] | Die beiden vorherigen (2) Monate. |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | Die letzten 18 Monate. |
| [!UICONTROL Change History Report] | — | Die letzten 31 Tage. |

>[!MORELIKETHIS]
>
>* [Über Berichte](report-about.md)
>* [Erste Einrichtungsaufgaben für Berichte](initial-setup.md)
