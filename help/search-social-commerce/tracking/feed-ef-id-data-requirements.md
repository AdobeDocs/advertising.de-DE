---
title: Datenanforderungen für Daten-Feeds mit EF IDs
description: Referenzieren Sie die Datenanforderungen für Daten-Feeds mit EF IDs.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Datenanforderungen für Daten-Feeds mit EF IDs

Im Folgenden finden Sie die Kopfzeilenfelder und entsprechenden Datenfelder, die für jeden Feed-Dateityp erforderlich sind.

>[!NOTE]
>* Die Header können in beliebiger Reihenfolge angeordnet werden, solange die Daten in den nachfolgenden Zeilen der gleichen Reihenfolge entsprechen. Wenn Sie keine Kopfzeile angeben, muss die Reihenfolge der Datenzeilen mit den einzelnen Feed-Dateien übereinstimmen.
>* Jede Zeile der Feed-Datei muss Daten für eine Transaktion enthalten und die Transaktion muss durch eine von der Adobe Advertising-generierte ef_id (Token) identifiziert werden.


| Header Field/Column Name | Typ | Beschreibung |
| ---- | ---- | ---- |
| EF ID | Zeichenfolge, bei der zwischen Groß- und Kleinschreibung unterschieden wird | Die ef_id (Token), die Sie beim Klick für die Transaktion erfasst haben, bestehend aus der Surfer-ID, der Klickzeit und dem Netzwerktyp. Ändern Sie den Wert nicht. |
| Transaktions-ID | Zeichenfolge, bei der zwischen Groß- und Kleinschreibung unterschieden wird | (Optional, jedoch empfohlen) Die vom Advertiser generierte Transaktions-ID. Es empfiehlt sich, dies für jede Transaktion einzubeziehen, auch wenn die ef_id zum Tracking der Transaktion zum Zeitpunkt der Umleitung verwendet wird. |
| Transaktionsdatum | DateTime | Das Datum der Transaktion. Das Format muss für jede Transaktion konsistent sein. |
| Client-spezifische Konversion | Zeichenfolge | Eine Konversion, die verfolgt wird (z. B. der Transaktionstyp oder der Betrag). Beschreiben Sie die Konversionen, die im Implementierungsteam von Adobe Advertising enthalten sein sollen, bevor Sie den Feed starten. |

## Beispiel

Die folgende Beispieldatei enthält Daten zu zwei Transaktionseigenschaften (Produkt und Umsatz).

```
EF ID,Client Transaction ID, Transaction Date,Product,Revenue
TIl4VQqoEEQAAG8CU5EAAACY:20100217062449:s,04896325,2010-02-17,Coffee,15.00
SOl5PRKlPEILDG6CL3QYENOI:20100217065632:s,04896490,2010-02-17,Tea,42.00
TRl4BEtoTPMBEW4SU5ZUMEPIE:20100217065804:s,04896552,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Dateianforderungen für Konversions-Feed-Dateien](feed-file-requirements.md)
>* [Konversions-Tracking mit einem EF ID-Feed](/help/search-social-commerce/tracking/feed-efid.md)

