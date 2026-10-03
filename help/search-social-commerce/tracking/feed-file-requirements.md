---
title: Dateianforderungen für Konversions-Feed-Dateien
description: Referenzieren Sie die Anforderungen an Konversions-Feed-Dateien.
exl-id: abc28394-3e00-447f-a04e-078fa9883a64
feature: Search Tracking
TQID: 'https://experienceleague.adobe.com/y5kEsTB71WWQE6RGYdsIq0GFuZI037tRbRQTwuOP8aM'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 2206c6aa-b5c2-51b3-88e0-706d57048fe4
    internal-label: Search Tracking
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%
---
# Dateianforderungen für Konversions-Feed-Dateien

Im Folgenden finden Sie die Anforderungen an das Dateiformat, die erforderlichen und optionalen Datenfelder, den Dateinamen und das Dateiübertragungsprotokoll für Feed-Dateien.

## Dateiformat

Die Datendatei muss im Textformat (TXT), als kommagetrennte Werte (CSV) oder als tabulatorgetrennte Werte (TSV) vorliegen. Die Datei kann aus einer Kopfzeile und Datenzeilen bestehen, deren Werte durch Tabulatoren, Kommas oder ein anderes Zeichen (aber keine Leerzeichen) getrennt sind:

* **Kopfzeile:** (Optional) Die erste Zeile der Datei ist eine Kopfzeile, die die erforderlichen Feldnamen (oder Spaltennamen) in einer bestimmten Reihenfolge angibt, getrennt durch Registerkarten oder Kommas. Die erforderlichen Spaltennamen enthalten die Konversionsmetriken, die von Adobe Advertising als Konversionen verfolgt werden.

* **Datenzeilen:** Jede nachfolgende Zeile enthält Datenfelder in der gleichen Reihenfolge wie die Kopfzeile und getrennt durch Tabulatoren oder Kommas. Wenn der erste Datensatz keine Kopfzeile ist, muss jede Datenzeile alle möglichen Felder in einer bestimmten Reihenfolge enthalten. Die Werte aller IDs und Konversionsmetriken müssen alphanumerisch sein.

  Wenn mehrere Klicks auf eine oder mehrere Anzeigen zu einer Transaktion führen, müssen Sie die Klick-ID und die Tracking-ID bestimmen, denen die Transaktion zugeordnet werden soll. Da für jede Transaktion eine eindeutige ID gemeldet wird, können Sie einzelne Transaktionen aktualisieren.

## Dateibenennungskonvention

Der Dateiname muss das Datum enthalten und konsistent sein. Wenn Sie beispielsweise das Format JJJJMMTT.txt verwenden, muss eine am 15. Mai 2011 gesendete Datei den Namen 20110515.txt haben.

## Dateiübertragungsprotokoll

Senden Sie die Datei über das SFTP-Übertragungsprotokoll über Port 22. Sie müssen Ihre Informationen zum öffentlichen Schlüssel bereitstellen.  Ihr Adobe-Konto-Team oder das Implementierungs-Team stellt Ihnen den Serverstandort zusammen mit den Anmeldeinformationen zur Verfügung, die Ihr System zur Übertragung der Dateien benötigt.

>[!TIP]
>
>Konversionsdaten-Feeds werden mehrmals täglich verarbeitet. Laden Sie den täglichen Feed so bald wie möglich nach Mitternacht (Ortszeit) um 12:00 Uhr hoch, damit Adobe Advertising Ihre Daten verarbeiten und in der Reporting-Benutzeroberfläche am frühen Morgen verfügbar machen kann.

>[!MORELIKETHIS]
>
>* [Datenanforderungen für Daten-Feeds mit EF-IDs](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
>* [Datenanforderungen für Daten-Feeds mit einer Transaktions-ID](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
