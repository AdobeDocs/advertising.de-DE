---
title: Verfügbar [!DNL Google Analytics] Metriken
description: Verweisen Sie auf [!DNL Google Analytics] Metriken, die für Datenquellen verfügbar sind.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Anhang - Verfügbar [!DNL Google Analytics] Metriken

Die folgenden Metriken sind verfügbar, mit Ausnahme der aufgeführten Ausnahmen, wenn sie in der Implementierung des Kunden in [!DNL Google Analytics].

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
| Interne Suche | — | Den Anzeigenamen aller Metriken aus der internen Suche wird der Wert &quot;InternalSearch:&quot;vorangestellt. &quot; |
| Ereignisverfolgung | — | — |
| E-Commerce | — | — |
| Social-Interaktionen | — | — |
| Ausnahmen | — | — |
| Benutzerdefinierte Variablen oder Spalten | ga:calcMetric_* | Berechnete Metriken werden immer ausgeschlossen. |

>[!MORELIKETHIS]
>
>* [Über die Synchronisierung [!DNL Google Analytics] Konversionsmetriken](data-source-about.md)
>* [Voraussetzungen für die Konfiguration einer [!DNL Google Analytics] Datenquelle](data-source-prerequisites.md)
>* [Konfigurieren Sie eine [!DNL Google Analytics] als Datenquelle anzeigen](data-source-configure.md)
>* [Bearbeiten von [!DNL Google Analytics] Datenquelle](data-source-edit.md)
>* [Synchronisierung einer Datenquelle anhalten](data-source-pause.md)
>* [Erneutes Authentifizieren eines [!DNL Google Analytics] Datenquelle](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] Datenquelleneinstellungen](data-source-settings.md)

