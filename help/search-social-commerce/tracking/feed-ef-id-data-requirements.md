---
title: Datenanforderungen für Daten-Feeds mit EF-IDs
description: Referenzieren Sie die Datenanforderungen für Daten-Feeds mithilfe von EF-IDs.
exl-id: 507ed42c-349f-4311-af61-8f7a27794162
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# Datenanforderungen für Daten-Feeds mit EF-IDs

Im Folgenden finden Sie die Header-Felder und die entsprechenden Datenfelder, die für jeden Feed-Dateityp erforderlich sind.

>[!NOTE]
>* Die Kopfzeilen können in beliebiger Reihenfolge vorliegen, solange die Daten in den nachfolgenden Zeilen derselben Reihenfolge entsprechen. Wenn Sie keine Kopfzeile einschließen, muss die Reihenfolge der Datenzeilen mit jeder Feed-Datei konsistent sein.
>* Jede Zeile der Feed-Datei muss Daten für eine Transaktion enthalten, und die Transaktion muss durch eine Adobe Advertising-generierte ef_id (Token) identifiziert werden.

| Header-Feld/Spaltenname | Typ | Beschreibung |
| ---- | ---- | ---- |
| EF ID | Zeichenfolge unter Berücksichtigung der Groß-/Kleinschreibung | Die ef_id (Token), die Sie beim Klick für die Transaktion erfasst haben und die aus der Surfer-ID, der Klickzeit und dem Netzwerktyp besteht. Ändern Sie den Wert nicht. |
| Transaktions-ID | Zeichenfolge unter Berücksichtigung der Groß-/Kleinschreibung | (Optional, aber empfohlen) Die vom Advertiser generierte Transaktions-ID. Es empfiehlt sich, dies für jede Transaktion einzuschließen, auch wenn die ef_id verwendet wird, um die Transaktion zum Zeitpunkt der Umleitung zu verfolgen. |
| Transaktionsdatum | DateTime | Das Datum der Transaktion. Das Format muss für jede Transaktion konsistent sein. |
| Client-spezifische Konversion | Zeichenfolge | Eine Konversion, die verfolgt wird (z. B. Transaktionstyp oder Betrag). Besprechen Sie die Konversionen, die mit dem Adobe Advertising-Implementierungsteam aufgenommen werden sollen, bevor Sie den Feed starten. |

## Beispiel

Die folgende Beispieldatei enthält Daten für zwei Konversionsmetriken (Produkt und Umsatz).

```
EF ID,Client Transaction ID, Transaction Date,Product,Revenue
TIl4VQqoEEQAAG8CU5EAAACY:20100217062449:s,04896325,2010-02-17,Coffee,15.00
SOl5PRKlPEILDG6CL3QYENOI:20100217065632:s,04896490,2010-02-17,Tea,42.00
TRl4BEtoTPMBEW4SU5ZUMEPIE:20100217065804:s,04896552,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Dateianforderungen für Konversions-Feed-Dateien](feed-file-requirements.md)
>* [Konversionsverfolgung mit einem EF-ID-Feed](/help/search-social-commerce/tracking/feed-efid.md)
