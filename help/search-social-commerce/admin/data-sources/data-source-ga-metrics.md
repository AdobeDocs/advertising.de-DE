---
title: Available [!DNL Google Analytics] metrics
description: Referenzieren Sie die  [!DNL Google Analytics]  Metriken, die für Datenquellen verfügbar sind.
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Anhang - Verfügbare [!DNL Google Analytics]

Die folgenden Metriken, mit Ausnahme der angegebenen Ausschlüsse, sind verfügbar, wenn sie in der Implementierung des Kunden in [!DNL Google Analytics] aktiviert sind.

<!-- Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| Kategorie | Ausgeschlossen | Kommentare |
| ---- | ---- | ---- |
| \[Alle\] | Metriken mit dem Datentyp „PERCENT“ | Metriken, die als Prozentsatz angezeigt werden, sind immer ausgeschlossen. |
| Benutzer | ga:1dayBenutzer, ga:7dayBenutzer, ga:14dayBenutzer, ga:28dayBenutzer, ga:sessionsPerBenutzer | — |
| Sitzung | ga:uniqueDimensionCombinations | — |
| Zielkonversionen | — | — |
| Seiten-Tracking | ga:eintritte, ga:timeOnPage, ga:exits | — |
| Interne Suche | — | Den Anzeigenamen aller Metriken aus der internen Suche wird der Wert „InternalSearch: &quot; vorangestellt. |
| Ereignisverfolgung | — | — |
| E-Commerce | — | — |
| Soziale Interaktionen | — | — |
| Ausnahmen | — | — |
| Benutzerdefinierte Variablen oder Spalten | ga:calcMetric_* | Berechnete Metriken sind immer ausgeschlossen. |

>[!MORELIKETHIS]
>
>* [Über Synchronisierungs [!DNL Google Analytics] Konversionsmetriken](data-source-about.md)
>* [Voraussetzungen für die Konfiguration  [!DNL Google Analytics]  Datenquelle](data-source-prerequisites.md)
>* [Konfigurieren einer  [!DNL Google Analytics] -Ansicht als Datenquelle](data-source-configure.md)
>* [Datenquelle  [!DNL Google Analytics] bearbeiten](data-source-edit.md)
>* [Synchronisierung einer Datenquelle anhalten](data-source-pause.md)
>* [Erneutes Authentifizieren  [!DNL Google Analytics]  Datenquelle](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] Datenquelleneinstellungen](data-source-settings.md)
