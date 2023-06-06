---
title: Die für Berichte verwendeten Daten
description: Erfahren Sie mehr über die verschiedenen Datentypen, die in Datenansichten und benutzerdefinierten Berichten verfügbar sind.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Die für Berichte verwendeten Daten

Search, Social und Commerce umfasst einen umfassenden Satz von Leistungsberichten, die auf Klick- und Konversionsdaten basieren. Sie können grundlegende Leistungsdaten für die verschiedenen Komponenten eines Portfolios oder Anzeigenkontos über die [!UICONTROL Portfolios] und [!UICONTROL Campaigns] und durch die Erstellung verschiedener grundlegender und erweiterter Berichte.

Werbetreibende, die den Adobe Advertising Conversion-Tracking-Dienst verwenden, können auch die Anzahl der Klicks für einen geografischen Standort oder Domänennamen einer verweisenden Website identifizieren, wie Anzeigen in den einzelnen Kanälen und die verschiedenen Ereignisse, die zu einer Konversion führen, zur Gesamtkonversionsrate und zur Verteilung der Konversionen für eine einzige Website beitragen. [Transaktionseigenschaft](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) nach Marketing-Kanal. Die verfügbaren Berichte variieren je nach Benutzerkontotyp. Das Adobe Account Team hat Zugriff auf alle Berichte.

Die meisten Berichte können so angepasst werden, dass nur die Informationen angezeigt werden, die Sie sehen möchten. Die folgenden Standardmetriken sind in den meisten Berichten verfügbar und werden auf Anzeigenebene berechnet:

* **Standardmäßige Leistungsmetriken:**

   * **[!UICONTROL Impressions]:** Die Gesamtanzahl der Anzeigenplatzierungen.

   * **[!UICONTROL Clicks]:** Die Gesamtzahl der Klicks auf einen Link in der Anzeige.

   * **[!UICONTROL Cost]:** Die Gesamtkosten der Anzeige. Die Kosten für Pay-per-Click-Werbung (PPC) entsprechen immer der Anzahl der Klicks multipliziert mit den Kosten pro Klick.

   * **[!UICONTROL Cost per Click]:** Die durchschnittlichen Kosten für einen Klick für eine Anzeige, die den Kosten der Anzeige dividiert durch die Gesamtanzahl der Klicks für die Anzeige entspricht. Wenn Sie beispielsweise 100 USD für eine Anzeigenimpression ausgeben und die Anzeige 10 Klicks generiert, betragen die Kosten pro Klick 100 USD/10=10 USD pro Klick.

   * **[!UICONTROL Average Position]:** (Falls zutreffend) Die durchschnittliche Position einer Anzeige, die platziert wurde, gewichtet mit der Anzahl der Impressionen.

   * **[!UICONTROL Estimated Clicks]:** (Nur in erweiterte Berichte für Advertiser mit dem Adobe Advertising Conversion-Tracking-Dienst enthalten) Die Gesamtanzahl der geschätzten Klicks für einen Ort oder Domänennamen einer verweisenden Website. Dies kann Daten für Werbenetzwerke umfassen, für die ein Werber kein Werbekonto hat.

* **Konversionsmetriken:** Die Gesamtzahl der Konversionen für die einzelnen Konversionen der [Transaktionseigenschaften](/help/search-social-commerce/glossary.md#s-t)oder Transaktionsdaten, die für einen Konversionstyp verfolgt werden. Dazu können Konversions- und Site-Interaktionsmetriken, jedoch keine berechneten Metriken und erweiterte berechnete Metriken gehören, die aus Adobe Analytics synchronisiert werden.

   Dies kann auch Folgendes umfassen: [[!DNL Google Ads]-verfolgte Konversionen](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) und [[!DNL Google Analytics]-verfolgte Konversionen](/help/search-social-commerce/admin/data-sources/data-source-about.md) die für das Advertiser-Konto synchronisiert werden.

* **Benutzerdefinierte Metriken:** Ihre eigenen Metriken, die Sie durch die Erstellung von Formeln auf der Grundlage vorhandener Metriken ableiten (z. B. Kosten pro Bestellung).

## Datenverfügbarkeit

Beim Generieren von Berichten können Sie festlegen, wie Konversionsdaten in einer Reihe von Ereignissen zugeordnet werden, die zu einer Konversion führen. Beispielsweise können Sie die gesamte Konversion dem letzten Ereignis zuordnen oder das letzte Ereignis stärker gewichten als die anderen. Standardmäßig werden Konversionen dem letzten Ereignis zugeordnet.

Je nach der für den Bericht festgelegten Attributionsregel stehen für die folgenden Daten Daten für die einzelnen Berichtstypen zur Verfügung.

| Berichtsgruppe | Bericht | Daten, für die Daten verfügbar sind |
|---|---|---|
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | Ab dem 15. Mai 2021.<br><br><b>Ausnahme:</b> Die Daten zu den Bekanntheitsmetriken stehen ab dem 8. September 2022 zur Verfügung. |
|  | Alle anderen [!UICONTROL Basic Reports] | Die letzten 36 Monate.<br><br><b>Ausnahme:</b> Die Daten zu den Bekanntheitsmetriken stehen ab dem 8. September 2022 zur Verfügung. |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | Die letzten 45 Tage. |
|  | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | Die beiden vorherigen (2) Monate plus der aktuelle Monat. |
| [!UICONTROL Assist Reports] | Alle | Die letzten 18 Monate. |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | Das Vorjahr. |
|  | [!UICONTROL RSA Assets Report] | Ab 10. August 2022. |
|  | Alle anderen [!UICONTROL Specialty Reports] | Die beiden vorherigen (2) Monate. |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | Die letzten 18 Monate. |
| [!UICONTROL Change History Report] | — | Die letzten 31 Tage. |

>[!MORELIKETHIS]
>
>* [Über Berichte](report-about.md)
>* [Erste Einrichtungsaufgaben für Berichte](initial-setup.md)

