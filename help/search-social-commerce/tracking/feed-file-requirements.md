---
title: Dateianforderungen für Konversions-Feed-Dateien
description: Referenzieren Sie die Anforderungen an Konversions-Feed-Dateien.
exl-id: abc28394-3e00-447f-a04e-078fa9883a64
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '360'
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

Senden Sie die Datei über das SFTP-Übertragungsprotokoll über Port 22. Sie müssen Ihre Informationen zum öffentlichen Schlüssel bereitstellen.  Ihr Adobe-Konto-Team oder das Implementierungs-Team stellt Ihnen den Serverstandort zusammen mit den Anmeldeinformationen zur Verfügung, die für Ihr System zur Übertragung der Dateien erforderlich sind.

>[!TIP]
>
>Konversionsdaten-Feeds werden mehrmals täglich verarbeitet. Laden Sie den täglichen Feed so bald wie möglich nach Mitternacht (Ortszeit) um 12:00 Uhr hoch, damit Adobe Advertising Ihre Daten verarbeiten und in der Reporting-Benutzeroberfläche am frühen Morgen verfügbar machen kann.

>[!MORELIKETHIS]
>
>* [Datenanforderungen für Daten-Feeds mit EF-IDs](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
>* [Datenanforderungen für Daten-Feeds mit einer Transaktions-ID](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
