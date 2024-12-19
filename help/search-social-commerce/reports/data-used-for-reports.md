---
title: Die für Berichte verwendeten Daten
description: Erfahren Sie mehr über die verschiedenen Datentypen, die in Datenansichten und benutzerdefinierten Berichten verfügbar sind.
exl-id: ba808b21-4421-4de5-9293-a20ec67cc81c
feature: Search Reports
source-git-commit: f357d9a9ec0f8b38fbc43726265521e6fd77c7d0
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# Die für Berichte verwendeten Daten

Search, Social und Commerce enthalten einen umfassenden Satz von Leistungsberichten, die auf Klick- und Konversionsdaten basieren. Sie können grundlegende Leistungsdaten für die verschiedenen Komponenten eines Portfolios oder Werbekontos in den [!UICONTROL Portfolios]- und [!UICONTROL Campaigns] sowie durch Generieren verschiedener grundlegender und erweiterter Berichte anzeigen.

Werbetreibende, die den Adobe Advertising-Konversionsverfolgungs-Service verwenden, können auch die Anzahl der Klicks für einen geografischen Standort oder Domain-Namen einer verweisenden Website identifizieren sowie feststellen, wie Anzeigen in jedem Kanal und die verschiedenen Ereignisse, die zu einer Konversion führen, zur Gesamtkonversionsrate beitragen und wie die Konversionen für eine einzelne [Konversionsmetrik](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) nach Marketing-Kanal verteilt werden. Die verfügbaren Berichte variieren je nach Benutzerkontotyp. Das Adobe Account Team hat Zugriff auf alle Berichte.

Die meisten Berichte können so angepasst werden, dass nur die Informationen angezeigt werden, die Sie sehen möchten. Die folgenden Standardmetriken sind in den meisten Berichten verfügbar und werden auf Anzeigenebene berechnet:

* **Standardleistungsmetriken:**

   * **[!UICONTROL Impressions]:** Die Gesamtzahl der Male, wie oft die Anzeige platziert wurde.

   * **[!UICONTROL Clicks]:** Die Gesamtzahl der Klicks auf einen Link in der Anzeige.

   * **[!UICONTROL Cost]:** Die Gesamtkosten der Anzeige. Die Kosten für PPC-Werbung sind immer die Anzahl der Klicks multipliziert mit den Kosten pro Klick.

   * **[!UICONTROL Cost per Click]:** Die durchschnittlichen Kosten für einen Klick für eine Anzeige, die sich aus den Kosten der Anzeige dividiert durch die Gesamtzahl der Klicks für die Anzeige ergeben. Wenn Sie beispielsweise 100 USD für eine Anzeigenimpression ausgeben und die Anzeige 10 Klicks generiert, liegen die Kosten pro Klick bei 100 USD/10=10 USD pro Klick.

   * **[!UICONTROL Average Position]:** (falls zutreffend) Die durchschnittliche Position einer platzierten Anzeige, gewichtet durch die Anzahl der Impressionen.

   * **[!UICONTROL Estimated Clicks]:** (nur in erweiterten Berichten für Werbetreibende mit dem Adobe Advertising-Konversionsverfolgungs-Service enthalten) Die Gesamtzahl der geschätzten Klicks für einen Stadt- oder Domain-Namen einer verweisenden Website. Dies kann Daten für Werbenetzwerke enthalten, für die ein Advertiser kein Werbekonto hat.

* **Konversionsmetriken:** Die Gesamtzahl der Konversionen für jede der Konversionsmetriken des Advertisers oder der Transaktionsdaten, die in Richtung einer Konversionsmetrik verfolgt werden. Dies kann Konversions- und Site-Interaktionsmetriken umfassen, jedoch keine berechneten Metriken und erweiterten berechneten Metriken, die mit Adobe Analytics synchronisiert werden.

  Dies kann auch [[!DNL Google Ads]-getrackte ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) und [[!DNL Google Analytics]-getrackte Konversionen ](/help/search-social-commerce/admin/data-sources/data-source-about.md), die für das Advertiser-Konto synchronisiert werden.

* **Benutzerdefinierte Metriken:** Eigene Metriken, die Sie durch die Erstellung von Formeln ableiten, die auf vorhandenen Metriken basieren (z. B. die Kosten pro Bestellung).

## Datenverfügbarkeit

Beim Generieren von Berichten können Sie auswählen, wie Konversionsdaten in einer Reihe von Ereignissen zugeordnet werden sollen, die zu einer Konversion führen. Sie können beispielsweise festlegen, dass die gesamte Konversion dem letzten Ereignis oder dem letzten Ereignis mehr als den anderen zugewiesen wird. Standardmäßig werden Konversionen dem letzten Ereignis zugeordnet.

Je nach der für den Bericht angegebenen Attributionsregel stehen Daten für jeden Berichtstyp für die folgenden Daten zur Verfügung.

| Berichtsgruppe | Bericht | Verfügbare Daten |
| --- | --- | --- |
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | Beginn: 15. Mai 2021.<br><br><b>Ausnahme: </b> Daten zu Bekanntheitsmetriken sind ab dem 8. September 2022 verfügbar. |
| | Alle anderen [!UICONTROL Basic Reports] | Die letzten 36 Monate.<br><br><b>Ausnahme: </b> Daten zu Bekanntheitsmetriken sind ab dem 8. September 2022 verfügbar. |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | Die letzten 45 Tage. |
| | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | Die vorherigen zwei (2) Monate plus der aktuelle Monat. |
| [!UICONTROL Assist Reports] | Alle | Die letzten 18 Monate. |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | Das Vorjahr. |
| | [!UICONTROL Google Asset Group Performance Report] | Keine Einschränkungen |
| | [!UICONTROL MSA Ad Extension by Ad Report], [!UICONTROL MSA Ad Extension by Keyword Report], [!UICONTROL MSA Ad Extension Detail Report], [!UICONTROL MSA Network Impression Share Report], [!UICONTROL MSA Network Performance Report] | Die letzten 180 Tage. |
| | [!UICONTROL RSA Assets Report] | Beginn: 10. August 2022. |
| | Alle anderen [!UICONTROL Specialty Reports] | Die letzten zwei (2) Monate. |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | Die letzten 18 Monate. |
| [!UICONTROL Change History Report] | — | Die letzten 31 Tage. |

>[!MORELIKETHIS]
>
>* [Über Berichte](report-about.md)
>* [Ersteinstellungsaufgaben für Berichte](initial-setup.md)
