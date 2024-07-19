---
title: Benutzerdefinierte Metrikeinstellungen
description: Referenzieren Sie die Einstellungen für benutzerdefinierte Metriken, die aus Standardmetriken berechnet werden.
exl-id: b9e8434d-5ea2-47cd-9d63-705a6337c34c
feature: Search Common Tasks, Search Custom Metrics
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---

# Benutzerdefinierte Metrikeinstellungen

Die Einstellungen für benutzerdefinierte Metriken unterscheiden sich in verschiedenen Teilen der Benutzeroberfläche geringfügig.

## Benutzerdefinierte Metrikeinstellungen in Kampagnenverwaltungsansichten

| Parameter/Abschnitt | Beschreibung |
|----|----|
| Name der benutzerdefinierten Metrik | Der Name der Metrik, der als Spaltenname angezeigt wird. <b>Tipp:</b> Verwenden Sie einen aussagekräftigen Metriknamen, beachten Sie jedoch, dass die Spalte durch längere Namen breiter wird. |
| Metrik einfügen | Die mathematische Formel zur Berechnung der neuen Metrik (z. B. [Kosten]/[Registrierungen]:<ul><li>Um eine Metrik aus der Liste der Traffic- und Umsatzmetriken einzufügen, platzieren Sie den Cursor an die Stelle, an der Sie die Metrik einfügen möchten. Wählen Sie dann die Metrik aus der Liste aus oder geben Sie sie manuell ein und fügen Sie sie in eckige Klammern ein (z. B. `[CPC]`).</li><li>Um einen Operator einzufügen, platzieren Sie den Cursor an die Stelle, an der der Operator eingefügt werden soll, und klicken Sie dann auf die Schaltfläche oder geben Sie das Symbol manuell ein. Die verfügbaren mathematischen Operatoren: `+ - * / ( ) ()`</li></ul><b>Hinweis: </b> Die Berechnung komplexer benutzerdefinierter Metriken dauert länger, und die Erstellung von Berichten und Ansichten, die sie enthalten - insbesondere wenn sie separate Spalten für Clickthrough- und Durchsichtskonversionen enthalten - dauert länger. |
| Format | Darstellung der Daten für diese Metrik: *[!UICONTROL Currency]* (ein Geldwert), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* oder *[!UICONTROL Percentage]* (ein Prozentsatz mit zwei Dezimalstellen).<br><br><b>Vorsicht:</b> Wenn Sie eine abgeleitete Metrik im Format [!UICONTROL Number w/out Decimal Points] erstellen (das Daten als Ganzzahlen anzeigt) und sie in eine Ansicht oder einen Bericht einfügen, der eine gewichtete Konversionszuordnungsregel ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] oder [!UICONTROL Even Distribution]) verwendet, wird die Ausgabe in Ganzzahlen und nicht in Dezimalzahlen angezeigt. Infolgedessen können einzelne Datenfelder falsch sein, auch wenn die Summen korrekt sind. Wenn eine Bestellung beispielsweise gleichmäßig zwischen drei Ereignissen aufgeteilt ist, wird jedem der drei Ereignisse eine Bestellung (statt einer Reihenfolge von 0,33) zugeordnet. Um das Problem zu vermeiden, verwenden Sie das Metrikformat [!UICONTROL Number to 2 Decimal Points]. |

## Benutzerdefinierte Metrikeinstellungen in Berichten und Berichtsvorlagen sowie in den [!UICONTROL Portfolios] Ansichten

| Parameter/Abschnitt | Beschreibung |
|----|----|
| Name der benutzerdefinierten Metrik | Der Name der Metrik, der als Spaltenname angezeigt wird. <b>Tipp:</b> Verwenden Sie einen aussagekräftigen Metriknamen, beachten Sie jedoch, dass die Spalte durch längere Namen breiter wird. |
| Format | Darstellung der Daten für diese Metrik: *[!UICONTROL Currency]* (ein Geldwert), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* oder *[!UICONTROL Percentage]* (ein Prozentsatz mit zwei Dezimalstellen).<br><br><b>Vorsicht:</b> Wenn Sie eine abgeleitete Metrik im Format [!UICONTROL Number w/out Decimal Points] erstellen (das Daten als Ganzzahlen anzeigt) und sie in eine Ansicht oder einen Bericht einfügen, der eine gewichtete Konversionszuordnungsregel ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] oder [!UICONTROL Even Distribution]) verwendet, wird die Ausgabe in Ganzzahlen und nicht in Dezimalzahlen angezeigt. Infolgedessen können einzelne Datenfelder falsch sein, auch wenn die Summen korrekt sind. Wenn eine Bestellung beispielsweise gleichmäßig zwischen drei Ereignissen aufgeteilt ist, wird jedem der drei Ereignisse eine Bestellung (statt einer Reihenfolge von 0,33) zugeordnet. Um das Problem zu vermeiden, verwenden Sie das Metrikformat [!UICONTROL Number to 2 Decimal Points]. |
| Metrik einfügen | Eine Liste vorhandener Metriken, aus denen Sie eine Formel erstellen können.<br><br>Um eine Metrik in das Formeleingabefeld einzufügen, platzieren Sie den Cursor an die Stelle, an der Sie die Metrik einfügen möchten. Wählen Sie dann die Metrik aus der Liste aus oder geben Sie sie manuell ein und fügen Sie sie in eckige Klammern ein (z. B. `[CPC]`). |
| Operator einfügen | Verfügbare mathematische Operatoren: `+ - x / ( )`<br><br>Um einen Operator in das Formeleingabefeld einzufügen, platzieren Sie den Cursor an die Stelle, an der der Operator eingefügt werden soll, und klicken Sie dann auf die Schaltfläche oder geben Sie das Symbol manuell ein. |
| [Formeleingabefeld für die Metrik] | Die mathematische Formel zur Berechnung der neuen Metrik basierend auf einer oder mehreren vorhandenen Eigenschaften oder Standardmetriken (z. B. `[Cost]/[Registrations]`. Sie kann eine beliebige Kombination von Metriken und Operatoren enthalten.<br><br><b>Hinweis: </b> Die Berechnung komplexer benutzerdefinierter Metriken dauert länger, und die Erstellung von Berichten und Ansichten, die sie enthalten - insbesondere wenn sie separate Spalten für Clickthrough- und Durchsichtskonversionen enthalten - dauert länger. |

>[!MORELIKETHIS]
>
>* [Über benutzerdefinierte Metriken](custom-metric-about.md)
>* [Benutzerdefinierte Metrik erstellen](custom-metric-create.md)
>* [Benutzerdefinierte Metrik bearbeiten](custom-metric-edit.md)
>* [Löschen einer benutzerdefinierten Metrik](custom-metric-delete.md)
