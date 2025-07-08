---
title: Benutzerdefinierte Metrikeinstellungen
description: Referenzieren Sie die Einstellungen für benutzerdefinierte Metriken, die anhand von Standardmetriken berechnet werden.
exl-id: b9e8434d-5ea2-47cd-9d63-705a6337c34c
feature: Search Common Tasks, Search Custom Metrics
source-git-commit: a89a6513dfe468b98513b2d47c086a3107e63d47
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# Benutzerdefinierte Metrikeinstellungen

Benutzerdefinierte Metrikeinstellungen unterscheiden sich geringfügig in verschiedenen Teilen der Benutzeroberfläche.

## Benutzerdefinierte Metrikeinstellungen in den meisten Verwaltungsansichten

| Parameter/Bereich | Beschreibung |
|----|----|
| Name der benutzerdefinierten Metrik | Der Name der Metrik, der als Spaltenname angezeigt wird. <b>Tipp</b> Verwenden Sie einen aussagekräftigen Metriknamen, beachten Sie jedoch, dass längere Namen die Spalte breiter machen. |
| Metrik einfügen | Die mathematische Formel, die zur Berechnung der neuen Metrik verwendet wird (z. B[Kosten]/[Registrierungen]:<ul><li>Um eine Metrik aus der Liste der Traffic- und Umsatzmetriken einzufügen, platzieren Sie den Cursor an der Stelle, an der Sie die Metrik einfügen möchten, und wählen Sie dann die Metrik entweder aus der Liste aus oder geben Sie sie manuell ein und schließen sie in Klammern ein (z. B. `[CPC]`).</li><li>Um einen Operator einzufügen, platzieren Sie den Cursor an die Stelle, an der Sie den Operator einfügen möchten, und klicken Sie dann entweder auf die Schaltfläche oder geben Sie das Symbol manuell ein. Die verfügbaren mathematischen Operatoren: `+ - * / ( ) ()`</li></ul><b>Hinweis</b> Die Berechnung komplexer benutzerdefinierter Metriken dauert länger und die Erstellung von Berichten und Ansichten, die diese enthalten - insbesondere wenn sie separate Spalten für Clickthrough- und View-Through-Konversionen enthalten - dauert länger. |
| Format | Darstellung der Daten für diese Metrik: *[!UICONTROL Currency]* (ein monetärer Wert), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* oder *[!UICONTROL Percentage]* (ein Prozentsatz mit zwei Dezimalpunkten).<br><br><b>Achtung:</b> Wenn Sie eine abgeleitete Metrik im Format [!UICONTROL Number w/out Decimal Points] erstellen (in dem die Daten als Ganzzahlen angezeigt werden) und sie in eine Ansicht oder einen Bericht aufnehmen, der bzw. der eine Attributionsregel für die gewichtete Konversion verwendet ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] oder [!UICONTROL Even Distribution]), wird die Ausgabe in Ganzzahlen und nicht in Dezimalzahlen angezeigt. Daher können einzelne Datenfelder falsch sein, obwohl die Gesamtwerte korrekt sind. Wenn beispielsweise eine Reihenfolge gleichmäßig auf drei Ereignisse aufgeteilt wird, wird jedem der drei Ereignisse eine Reihenfolge (statt 0,33 Reihenfolge) zugeordnet. Um das Problem zu vermeiden, verwenden Sie das Metrikformat [!UICONTROL Number to 2 Decimal Points]. |

## Benutzerdefinierte Metrikeinstellungen in Berichten und Berichtsvorlagen sowie in den veralteten [!UICONTROL Portfolios]

| Parameter/Bereich | Beschreibung |
|----|----|
| Name der benutzerdefinierten Metrik | Der Name der Metrik, der als Spaltenname angezeigt wird. <b>Tipp</b> Verwenden Sie einen aussagekräftigen Metriknamen, beachten Sie jedoch, dass längere Namen die Spalte breiter machen. |
| Format | Darstellung der Daten für diese Metrik: *[!UICONTROL Currency]* (ein monetärer Wert), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* oder *[!UICONTROL Percentage]* (ein Prozentsatz mit zwei Dezimalpunkten).<br><br><b>Achtung:</b> Wenn Sie eine abgeleitete Metrik im Format [!UICONTROL Number w/out Decimal Points] erstellen (in dem die Daten als Ganzzahlen angezeigt werden) und sie in eine Ansicht oder einen Bericht aufnehmen, der bzw. der eine Attributionsregel für die gewichtete Konversion verwendet ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] oder [!UICONTROL Even Distribution]), wird die Ausgabe in Ganzzahlen und nicht in Dezimalzahlen angezeigt. Daher können einzelne Datenfelder falsch sein, obwohl die Gesamtwerte korrekt sind. Wenn beispielsweise eine Reihenfolge gleichmäßig auf drei Ereignisse aufgeteilt wird, wird jedem der drei Ereignisse eine Reihenfolge (statt 0,33 Reihenfolge) zugeordnet. Um das Problem zu vermeiden, verwenden Sie das Metrikformat [!UICONTROL Number to 2 Decimal Points]. |
| Metrik einfügen | Eine Liste der vorhandenen Metriken, aus denen Sie eine Formel erstellen können.<br><br>Um eine Metrik in das Formeleingabefeld einzufügen, platzieren Sie den Cursor an die Stelle, an der Sie die Metrik einfügen möchten. Wählen Sie dann die Metrik aus der Liste aus oder geben Sie sie manuell ein und schließen Sie sie in Klammern ein (z. B. `[CPC]`). |
| Operator einfügen | Die verfügbaren mathematischen Operatoren: `+ - x / ( )`<br><br>Um einen Operator in das Formeleingabefeld einzufügen, platzieren Sie den Cursor an der gewünschten Stelle, und klicken Sie dann entweder auf die Schaltfläche oder geben Sie das Symbol manuell ein. |
| [Formeleingabefeld für die Metrik] | Die mathematische Formel, mit der die neue Metrik basierend auf einer oder mehreren vorhandenen Eigenschaften oder Standardmetriken (z. B. `[Cost]/[Registrations]`) berechnet wird. Sie kann eine beliebige Kombination von Metriken und Operatoren enthalten.<br><br><b>Hinweis</b> Die Berechnung komplexer benutzerdefinierter Metriken dauert länger und die Erstellung von Berichten und Ansichten, die diese enthalten - insbesondere wenn sie separate Spalten für Clickthrough- und View-Through-Konversionen enthalten - dauert länger. |

>[!MORELIKETHIS]
>
>* [Über benutzerdefinierte Metriken](custom-metric-about.md)
>* [Erstellen einer benutzerdefinierten Metrik](custom-metric-create.md)
>* [Bearbeiten einer benutzerdefinierten Metrik](custom-metric-edit.md)
>* [Löschen einer benutzerdefinierten Metrik](custom-metric-delete.md)
