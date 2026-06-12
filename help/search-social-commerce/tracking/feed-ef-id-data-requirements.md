---
title: Datenanforderungen für Daten-Feeds mit EF-IDs
description: Referenzieren Sie die Datenanforderungen für Daten-Feeds mithilfe von EF-IDs.
exl-id: 507ed42c-349f-4311-af61-8f7a27794162
feature: Search Tracking
TQID: https://experienceleague.adobe.com/p66X8xVlx-JwKjGgXxonJRRu78Q8F4109VkaIVtUbwU
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 261
ht-degree: 0%

---

# Datenanforderungen für Daten-Feeds mit EF-IDs

Im Folgenden finden Sie die Header-Felder und die entsprechenden Datenfelder, die für jeden Feed-Dateityp erforderlich sind.

>[!NOTE]
>* Die Kopfzeilen können in beliebiger Reihenfolge vorliegen, solange die Daten in den nachfolgenden Zeilen derselben Reihenfolge entsprechen. Wenn Sie keine Kopfzeile einschließen, muss die Reihenfolge der Datenzeilen mit jeder Feed-Datei konsistent sein.
>* Jede Zeile der Feed-Datei muss Daten für eine Transaktion enthalten, und die Transaktion muss durch eine von Adobe Advertising generierte ef_id (Token) identifiziert werden.

| Header-Feld/Spaltenname | Typ | Beschreibung |
| ---- | ---- | ---- |
| EF ID | Zeichenfolge unter Berücksichtigung der Groß-/Kleinschreibung | Die ef_id (Token), die Sie beim Klick für die Transaktion erfasst haben und die aus der Surfer-ID, der Klickzeit und dem Netzwerktyp besteht. Ändern Sie den Wert nicht. |
| Transaktions-ID | Zeichenfolge unter Berücksichtigung der Groß-/Kleinschreibung | (Optional, aber empfohlen) Die vom Advertiser generierte Transaktions-ID. Es empfiehlt sich, dies für jede Transaktion einzuschließen, auch wenn die ef_id verwendet wird, um die Transaktion zum Zeitpunkt der Umleitung zu verfolgen. |
| Transaktionsdatum | DateTime | Das Datum der Transaktion. Das Format muss für jede Transaktion konsistent sein. |
| Client-spezifische Konversion | Zeichenfolge | Eine Konversion, die verfolgt wird (z. B. Transaktionstyp oder Betrag). Besprechen Sie die Konversionen, die einbezogen werden sollen, mit dem Adobe Advertising-Implementierungsteam, bevor Sie den Feed starten. |

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
