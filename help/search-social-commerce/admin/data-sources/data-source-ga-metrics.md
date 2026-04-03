---
title: Available [!DNL Google Analytics] metrics
description: Referenzieren Sie die  [!DNL Google Analytics]  Metriken, die für Datenquellen verfügbar sind.
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
TQID: https://experienceleague.adobe.com/hRYeNcQu4uUTCAHXcF9zaZfQm-mw6kDlqvs2AxZhED8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
subfeature_v2: id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 131
ht-degree: 0%

---

# Anhang - Verfügbare [!DNL Google Analytics]

Die folgenden Metriken, mit Ausnahme der angegebenen Ausschlüsse, sind verfügbar, wenn sie in der Implementierung des Kunden in [!DNL Google Analytics] aktiviert sind.

<!--
 Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| Kategorie | Ausgeschlossen | Kommentare |
| ---- | ---- | ---- |
| \[Alle\] | Metriken mit dem Datentyp „PERCENT“ | Metriken, die als Prozentsatz angezeigt werden, sind immer ausgeschlossen. |
| Benutzer | GA:1dayUsers, GA:7dayUsers, GA:14dayUsers, GA:28dayUsers, GA:sessionsPerUser | — |
| Sitzung | allgemein verfügbar:uniqueDimensionCombinations | — |
| Zielkonversionen | — | — |
| Seiten-Tracking | GA:entrances, GA:timeOnPage, GA:exits | — |
| Interne Suche | — | Den Anzeigenamen aller Metriken aus der internen Suche wird der Wert „InternalSearch: &quot; vorangestellt. |
| Ereignisverfolgung | — | — |
| E-Commerce | — | — |
| Soziale Interaktionen | — | — |
| Ausnahmen | — | — |
| Benutzerdefinierte Variablen oder Spalten | GA :calcMetric_* | Berechnete Metriken sind immer ausgeschlossen. |

>[!MORELIKETHIS]
>
>* [Über Synchronisierungs [!DNL Google Analytics] Konversionsmetriken](data-source-about.md)
>* [Voraussetzungen für die Konfiguration  [!DNL Google Analytics]  Datenquelle](data-source-prerequisites.md)
>* [Konfigurieren einer  [!DNL Google Analytics] -Ansicht als Datenquelle](data-source-configure.md)
>* [Datenquelle  [!DNL Google Analytics] bearbeiten](data-source-edit.md)
>* [Synchronisierung einer Datenquelle anhalten](data-source-pause.md)
>* [Erneutes Authentifizieren  [!DNL Google Analytics]  Datenquelle](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] Datenquelleneinstellungen](data-source-settings.md)
