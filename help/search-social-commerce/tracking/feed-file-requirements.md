---
title: Dateianforderungen für Konversions-Feed-Dateien
description: Verweisen Sie auf die Anforderungen für Konversions-Feed-Dateien.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---

# Dateianforderungen für Konversions-Feed-Dateien

Im Folgenden finden Sie die Anforderungen an das Dateiformat, die erforderlichen und optionalen Datenfelder, den Dateinamen und das Dateiübertragungsprotokoll für Feed-Dateien.

## Dateiformat

Die Datendatei muss im Format &quot;Flattext&quot;(TXT), &quot;Komma-getrennte Werte&quot;(CSV) oder &quot;Tabulator-getrennte Werte&quot;(TSV) vorliegen. Die Datei kann aus einer Kopfzeile und Datenzeilen mit Werten bestehen, die durch Tabulatoren, Kommas oder ein anderes Zeichen (ohne Leerzeichen) getrennt sind:

* **Kopfzeile:** (Optional) Die erste Zeile der Datei ist eine Kopfzeile, die die erforderlichen Feldnamen (oder Spaltennamen) in einer bestimmten Reihenfolge angibt, getrennt durch Registerkarten oder Kommas. Die erforderlichen Spaltennamen enthalten die Transaktionseigenschaften, die Adobe Advertising als Konversionen verfolgt.

* **Datenzeilen:** Jede nachfolgende Zeile enthält Datenfelder in derselben Reihenfolge wie die Kopfzeile und durch Tabulatoren oder Kommas getrennt. Wenn der erste Datensatz keine Kopfzeile ist, muss jede Datenzeile alle möglichen Felder in einer angegebenen Reihenfolge enthalten. Die Werte aller IDs und Transaktionseigenschaften müssen alphanumerisch sein.

   Wenn mehrere Klicks auf eine oder mehrere Anzeigen zu einer Transaktion führen, müssen Sie die Klick-ID und die Tracking-ID bestimmen, der die Transaktion zugeordnet werden soll. Da für jede Transaktion eine eindeutige ID gemeldet wird, können Sie einzelne Transaktionen aktualisieren.

## Dateibenennungskonvention

Der Dateiname muss das Datum enthalten und konsistent sein. Wenn Sie beispielsweise das Format JJJJMMTT.txt verwenden, muss eine am 15. Mai 2011 gesendete Datei den Namen 20110515.txt haben.

## File Transfer Protocol

Senden Sie die Datei über das SFTP-Übertragungsprotokoll mit Port 22. Sie müssen Ihre Informationen zu öffentlichen Schlüsseln angeben.  Ihr Adobe Account-Team oder das Implementierungsteam stellt Ihnen den Serverstandort zusammen mit den Anmeldeinformationen bereit, die Sie benötigen, damit Ihr System die  übertragen kann.

>[!TIP]
>
>Konversionsdaten-Feeds werden mehrmals täglich verarbeitet. Laden Sie den täglichen Feed so bald wie möglich nach 12:00 Uhr Ortszeit hoch, damit Adobe Advertising Ihre Daten verarbeiten und in der Reporting-Benutzeroberfläche am frühen Morgen verfügbar machen kann.

>[!MORELIKETHIS]
>
>* [Datenanforderungen für Daten-Feeds mit EF IDs](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
>* [Datenanforderungen für Daten-Feeds mit einer Transaktions-ID](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)

