---
title: Unterstützte Massendateiformate
description: Referenzieren Sie die allgemeinen Dateianforderungen für Bulksheets.
exl-id: f3daf036-8f0c-4c75-9c76-2734abd850ec
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Unterstützte Massendateiformate

## Dateiformate

Sie können Bulksheet-Dateien für unterstützte Werbenetzwerke in einem der folgenden Formate herunterladen, hochladen und posten:

* CSV (kommagetrennte Werte)
* TSV (tabulatorgetrennte Werte)
* TXT (Unicode-Text), durch Kommas oder Tabulatoren getrennt
* ZIP (komprimiert), die eine Datei im CSV-Format, im TSV-Format oder im TXT-Format enthält, getrennt durch Kommas oder Tabulatoren

Wenn Sie ein Bulksheet erstellen/herunterladen, wird es im angegebenen Dateiformat mit allen relevanten Daten erstellt, die in der Datei enthalten sind. Verwenden Sie die folgenden Informationen, um Daten in der Datei zu bearbeiten oder manuell ein eigenes Bulksheet zu erstellen.

## Grundlegender Inhalt eines Bulksheets

Der erste Datensatz (Zeile) einer Bulksheet-Datei enthält eine Reihe spezifischer Spaltennamen, die zusammen als <i>header</i> bezeichnet werden. Die Spaltennamen in der Kopfzeile sind in einer angegebenen Reihenfolge und entsprechen jedem der Felder in den nachfolgenden Datensätzen. Die in der Kopfzeile erforderlichen Spaltennamen variieren je nach Anzeigennetzwerk.

Jeder nachfolgende Datensatz (Zeile) enthält Daten, wobei Felder Werte (oder keine Werte) für jede Spalte in der Kopfzeile enthalten.

## Maximale Dateigröße

Bulksheet-Dateien können bis zu 2,5 GB groß sein, was etwa 2,5 Millionen Zeilen entspricht.

>[!NOTE]
>
>Wenn Sie ein Bulksheet für mehrere Kampagnen generieren und die kombinierten Daten aus mehr als 500.000 Zeilen bestehen, werden die Daten nach Kampagne in zwei oder mehr Dateien mit den Namen `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv` usw. aufgeteilt.

## Formatierungsanforderungen für verschiedene Dateitypen

Datenfelder, die durch Tabulatoren und Kommas getrennt sind, müssen unterschiedlich formatiert sein.

### TSV-Dateien und TXT-Dateien mit Tabulatoren getrennt

Datenfelder in TSV-Dateien und TXT-Dateien, die durch Tabulatoren getrennt sind, müssen wie folgt formatiert sein:

* Die Felder in jedem Datensatz werden durch Tabulatorzeichen getrennt. Wenn Sie einen Wert für ein Feld weglassen möchten, verwenden Sie nur das Tabulatorzeichen.

  Beispiel: `Cruises<TAB>5000<TAB>Caribbean<TAB><TAB><TAB>`

* Felder dürfen keine eingebetteten Tabulatorzeichen enthalten.

### CSV-Dateien und TXT-Dateien mit Kommas als Trennzeichen

Datenfelder in CSV-Dateien und TXT-Dateien, die durch Kommas getrennt sind, müssen wie folgt formatiert sein:

* Die Felder in einem Datensatz werden durch Kommas getrennt. Wenn Sie einen Wert für ein Feld weglassen möchten, verwenden Sie nur das Komma.

  Beispiel: `Cruises,5000,Caribbean,,,`

* Jedes Feld kann optional in doppelte Anführungszeichen (`""`) gesetzt werden.

  Beispiel: `"Cruises","5000","Caribbean",`

* Felder mit eingebetteten Kommas müssen in doppelte Anführungszeichen (`""`) gesetzt werden.

  Beispiel: `Cruises,5000,Caribbean,"Luxurious, spacious cabins",`

* Felder mit eingebetteten doppelten Anführungszeichen müssen in doppelte Anführungszeichen (`""`) gesetzt werden.

  Beispiel: `Cruises,5000,Caribbean,"Customers say ""We wish we could stay forever."",`

* Felder mit vorangestellten oder nachfolgenden Leerzeichen müssen in doppelte Anführungszeichen (`""`) gesetzt werden.

  Beispiel: `Cruises,5000,Caribbean,"  Come see what we mean.  ",`

>[!MORELIKETHIS]
>
>* [Über die Verwaltung von Kampagnendaten mithilfe von Bulksheets](../bulksheet-about.md)
>* [Vorgänge, die Sie in Bulksheets ausführen können](bulksheet-operations.md)
>* [Anhang - Bulksheet-Fehler](../bulksheet-errors.md)
>* [Herunterladen/Erstellen einer Bulksheet-Datei](../bulksheet-download.md)
