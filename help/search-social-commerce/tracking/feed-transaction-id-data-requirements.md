---
title: Datenanforderungen für Daten-Feeds mit einer Transaktions-ID
description: Verweisen Sie mithilfe einer Transaktions-ID auf die Datenanforderungen für Daten-Feeds.
exl-id: 055b1417-3185-4081-83f0-9f4798058c04
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Datenanforderungen für Daten-Feeds mit einer Transaktions-ID

Im Folgenden finden Sie die Kopfzeilenfelder und entsprechenden Datenfelder, die für jeden Feed-Dateityp erforderlich sind.

>[!NOTE]
>* Die Header können in beliebiger Reihenfolge angeordnet werden, solange die Daten in den nachfolgenden Zeilen der gleichen Reihenfolge entsprechen. Wenn Sie keine Kopfzeile angeben, muss die Reihenfolge der Datenzeilen mit den einzelnen Feed-Dateien übereinstimmen.
>* Jede Zeile der Feed-Datei muss Daten für eine Transaktion enthalten und die Transaktion muss durch eine Transaktions-ID identifiziert werden.

| Header Field/Column Name | Typ | Beschreibung |
| ---- | ---- | ---- |
| Transaktions-ID (ev_transid) | Groß-/Kleinschreibung beachten | Die vom Advertiser generierte Kennung, die mit der Transaktion verknüpft ist. Da das Adobe Advertising-Konversions-Tracking-Tag für die Online-Teile der Transaktion verwendet wird, muss dies mit der Transaktions-ID (ev_transid) übereinstimmen, die Adobe Advertising für den früheren Teil der Transaktion bereitgestellt hat. Das bedeutet, dass das Konversions-Tag für den Online-Teil der Transaktion eine Konversionsmetrik für eine eindeutige Transaktions-ID enthalten muss.<br><br>**Hinweis:** Adobe Advertising verwendet die ID, um die alten Transaktionsdaten zu lokalisieren und gemäß einem vereinbarten Einfügemodus zu aktualisieren (z. B. um die vorhandenen Daten zu ersetzen oder sie durch die neuen Daten zu ergänzen). |
| Transaktionsdatum | DateTime | Das Datum der Transaktion. Das Format muss für jede Transaktion konsistent sein. |
| Client-spezifische Konversion | Zeichenfolge | Eine verfolgte Konversion (z. B. der Transaktionstyp oder der Betrag). Beschreiben Sie die Konversionen, die in das Adobe Advertising-Implementierungsteam eingeschlossen werden sollen, bevor Sie den Feed starten. |

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
>* [Konversions-Tracking mit einem Transaktions-ID-Feed](/help/search-social-commerce/tracking/feed-transaction-id.md)
