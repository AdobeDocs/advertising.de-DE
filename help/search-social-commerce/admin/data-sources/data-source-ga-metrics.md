---
title: Verfügbare [!DNL Google Analytics] Metriken
description: Referenzieren Sie die für Datenquellen verfügbaren [!DNL Google Analytics] Metriken.
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Anhang - Verfügbare [!DNL Google Analytics] Metriken

Die folgenden Metriken mit Ausnahme der aufgeführten Ausnahmen sind verfügbar, wenn sie in der Implementierung des Kunden in [!DNL Google Analytics] aktiviert sind.

<!-- Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| Kategorie | Ausgeschlossen | Kommentare |
| ---- | ---- | ---- |
| \[Alle\] | Metriken mit dem Datentyp &quot;PERCENT&quot; | Metriken, die in Prozent angezeigt werden, sind immer ausgeschlossen. |
| Benutzer | ga:1dayUsers, ga:7dayUsers, ga:14dayUsers, ga:28dayUsers, ga:sessionsPerUser | — |
| Sitzung | ga:uniqueDimensionCombinations | — |
| Zielkonversionen | — | — |
| Seitenverfolgung | ga:eingehenden, ga:timeOnPage, ga:exit | — |
| Interne Suche | — | Den Anzeigenamen aller Metriken aus der internen Suche wird der Wert &quot;InternalSearch: &quot; vorangestellt. |
| Ereignisverfolgung | — | — |
| E-Commerce | — | — |
| Social-Interaktionen | — | — |
| Ausnahmen | — | — |
| Benutzerdefinierte Variablen oder Spalten | ga:calcMetric_* | Berechnete Metriken werden immer ausgeschlossen. |

>[!MORELIKETHIS]
>
>* [Über die Synchronisierung von [!DNL Google Analytics] Konversionsmetriken](data-source-about.md)
>* [Voraussetzungen für die Konfiguration einer  [!DNL Google Analytics] Datenquelle](data-source-prerequisites.md)
>* [Konfigurieren einer [!DNL Google Analytics] Ansicht als Datenquelle](data-source-configure.md)
>* [Bearbeiten einer [!DNL Google Analytics] Datenquelle](data-source-edit.md)
>* [Synchronisierung einer Datenquelle anhalten](data-source-pause.md)
>* [Erneutes Authentifizieren einer  [!DNL Google Analytics] Datenquelle](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] Datenquelleneinstellungen](data-source-settings.md)
