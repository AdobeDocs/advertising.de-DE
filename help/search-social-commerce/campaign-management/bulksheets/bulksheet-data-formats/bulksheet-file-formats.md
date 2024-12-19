---
title: Unterstützte Bulksheet-Dateiformate
description: Verweisen Sie auf die allgemeinen Dateianforderungen für Bulksheets.
exl-id: f3daf036-8f0c-4c75-9c76-2734abd850ec
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Unterstützte Bulksheet-Dateiformate

## Dateiformate

Sie können Bulksheet-Dateien für unterstützte Werbenetzwerke in einem der folgenden Formate herunterladen, hochladen und posten:

* CSV (kommagetrennte Werte)
* TSV (tabulatorgetrennte Werte)
* TXT (Unicode-Text), durch Kommas oder Tabulatoren getrennt
* ZIP (komprimiert) mit einer Datei im CSV-, TSV- oder TXT-Format, getrennt durch Kommas oder Tabulatoren

Wenn Sie eine Bulksheet erstellen/herunterladen, wird sie im angegebenen Dateiformat erstellt, wobei alle relevanten Daten in der Datei enthalten sind. Verwenden Sie die folgenden Informationen, um Daten in der Datei zu bearbeiten oder manuell eine eigene Bulksheet zu erstellen.

## Grundlegende Inhalte eines Bulksheets

Der erste Datensatz (die erste Zeile) einer Bulksheet-Datei enthält eine Reihe spezifischer Spaltennamen, die zusammen als &quot;<i>&quot; bezeichnet </i>. Die Spaltennamen in der Kopfzeile haben eine bestimmte Reihenfolge und entsprechen den einzelnen Feldern in den nachfolgenden Datensätzen. Die in der Kopfzeile erforderlichen Spaltennamen variieren je nach Anzeigennetzwerk.

Jeder nachfolgende Datensatz (Zeile) enthält Daten mit Feldern, die Werte (oder keine Werte) für jede Spalte in der Kopfzeile enthalten.

## Maximale Dateigröße

Bulksheet-Dateien können bis zu 2,5 GB groß sein, was etwa 2,5 Millionen Zeilen entspricht.

>[!NOTE]
>
>Wenn Sie eine Bulksheet für mehrere Kampagnen generieren und die kombinierten Daten aus mehr als 500.000 Zeilen bestehen, werden die Daten nach Kampagne in zwei oder mehr Dateien mit den Namen `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv` usw. aufgeteilt.

## Formatierungsanforderungen für verschiedene Dateitypen

Durch Tabulatoren und Kommas getrennte Datenfelder erfordern eine unterschiedliche Formatierung.

### Durch Tabulatoren getrennte TSV-Dateien und TXT-Dateien

Datenfelder in TSV-Dateien und durch Tabulatoren getrennte TXT-Dateien müssen wie folgt formatiert sein:

* Die Felder in jedem Datensatz werden durch Tabulatorzeichen getrennt. Wenn Sie keinen Wert für ein Feld angeben möchten, verwenden Sie nur das Tabulatorzeichen.

  Beispiel: `Cruises<TAB>5000<TAB>Caribbean<TAB><TAB><TAB>`

* Felder dürfen keine eingebetteten Tabulatorzeichen enthalten.

### CSV-Dateien und durch Kommas getrennte TXT-Dateien

Datenfelder in CSV-Dateien und durch Kommas getrennte TXT-Dateien müssen wie folgt formatiert sein:

* Die Felder in einem Datensatz werden durch Kommas getrennt. Wenn Sie keinen Wert für ein Feld angeben möchten, verwenden Sie nur das Komma.

  Beispiel: `Cruises,5000,Caribbean,,,`

* Jedes Feld kann optional in doppelte Anführungszeichen (`""`) eingeschlossen werden.

  Beispiel: `"Cruises","5000","Caribbean",`

* Felder mit eingebetteten Kommas müssen in doppelte Anführungszeichen (`""`) gesetzt werden.

  Beispiel: `Cruises,5000,Caribbean,"Luxurious, spacious cabins",`

* Felder mit eingebetteten doppelten Anführungszeichen müssen in doppelte Anführungszeichen (`""`) eingeschlossen werden.

  Beispiel: `Cruises,5000,Caribbean,"Customers say ""We wish we could stay forever."",`

* Felder mit vorangestellten oder nachfolgenden Leerzeichen müssen in doppelte Anführungszeichen (`""`) gesetzt werden.

  Beispiel: `Cruises,5000,Caribbean,"  Come see what we mean.  ",`

>[!MORELIKETHIS]
>
>* [Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets](../bulksheet-about.md)
>* [Vorgänge, die Sie in Bulksheets ausführen können](bulksheet-operations.md)
>* [Anhang - Bulksheet-Fehler](../bulksheet-errors.md)
>* [Bulksheet-Datei herunterladen/erstellen](../bulksheet-download.md)
