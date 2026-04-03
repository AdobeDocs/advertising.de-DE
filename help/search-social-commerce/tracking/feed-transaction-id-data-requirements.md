---
title: Datenanforderungen für Daten-Feeds mit einer Transaktions-ID
description: Referenzieren Sie die Datenanforderungen für Daten-Feeds mithilfe einer Transaktions-ID.
exl-id: 055b1417-3185-4081-83f0-9f4798058c04
feature: Search Tracking
TQID: https://experienceleague.adobe.com/TONScPVaJyxsORRD-sOrYXwEzO9rsa6ERPUo8oSRono
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 295
ht-degree: 0%

---

# Datenanforderungen für Daten-Feeds mit einer Transaktions-ID

Im Folgenden finden Sie die Header-Felder und die entsprechenden Datenfelder, die für jeden Feed-Dateityp erforderlich sind.

>[!NOTE]
>* Die Kopfzeilen können in beliebiger Reihenfolge vorliegen, solange die Daten in den nachfolgenden Zeilen derselben Reihenfolge entsprechen. Wenn Sie keine Kopfzeile einschließen, muss die Reihenfolge der Datenzeilen mit jeder Feed-Datei konsistent sein.
>* Jede Zeile der Feed-Datei muss Daten für eine Transaktion enthalten, und die Transaktion muss durch eine Transaktions-ID identifiziert werden.

| Header-Feld/Spaltenname | Typ | Beschreibung |
| ---- | ---- | ---- |
| Transaktions-ID (ev_transid) | Zeichenfolge unter Berücksichtigung der Groß-/Kleinschreibung | Die vom Advertiser generierte Kennung, die mit der Transaktion verknüpft ist. Da das Adobe Advertising-Konversionsverfolgungs-Tag für die Online-Teile der Transaktion verwendet wird, muss dies mit der Transaktions-ID (ev_transid) übereinstimmen, die Adobe Advertising für den früheren Teil der Transaktion angegeben hat. Das bedeutet, dass das Konversions-Tag für den Online-Teil der Transaktion eine Konversionsmetrik für eine eindeutige Transaktions-ID enthalten muss.<br><br>**Hinweis:** Adobe Advertising verwendet die ID, um die alten Transaktionsdaten zu finden und entsprechend einem vereinbarten Einfügemodus zu aktualisieren (z. B. um die vorhandenen Daten zu ersetzen oder um sie mit den neuen Daten zu erweitern). |
| Transaktionsdatum | DateTime | Das Datum der Transaktion. Das Format muss für jede Transaktion konsistent sein. |
| Client-spezifische Konversion | Zeichenfolge | Eine Konversion, die verfolgt wird (z. B. Transaktionstyp oder Betrag). Besprechen Sie die Konversionen, die einbezogen werden sollen, mit dem Adobe Advertising-Implementierungsteam, bevor Sie den Feed starten. |

## Beispiel

Die folgende Beispieldatei enthält Daten für zwei Konversionsmetriken (Produkt und Umsatz).

```
Transaction ID,Transaction Date,Product,Revenue
12345,2010-02-17,Coffee,15.00
12346,2010-02-17,Tea,42.00
12347,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [Dateianforderungen für Konversions-Feed-Dateien](feed-file-requirements.md)
>* [Konversionsverfolgung mit einem Transaktions-ID-Feed](/help/search-social-commerce/tracking/feed-transaction-id.md)
