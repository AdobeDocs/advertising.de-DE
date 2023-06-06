---
title: Datenanforderungen für Traffic- und Konversionsmetriken für [!DNL Naver] Nur-Tracking-Konten
description: Verweisen Sie auf die Anforderungen zum Hochladen von Daten für [!DNL Naver] reine Tracking-Konten.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# Anforderungen an Metrikdaten für [!DNL Naver] Nur-Tracking-Konten

Im Folgenden finden Sie die Datenanforderungen für [!DNL Naver] Traffic- und Konversionsmetriken für reine Tracking-Konten.

Datendateien müssen im TSV-, CSV- oder TXT-Format vorliegen.

Die folgenden Header-Felder sind erforderlich und optional. Jede Datenzeile muss einen täglich aggregierten Wert für mindestens ein Metrikfeld enthalten.

| Header Field/Column Name | Typ | Beschreibung |
| ---- | ---- | ---- |
| Zeitraum | DateTime | Das Datum, für das die Daten gelten, im Format `YYYY.MM.DD.` (z. B. `2019.11.15.`, wobei ein Zeitraum nach dem Tag beginnt). |
| Kampagne | Zeichenfolge, bei der zwischen Groß- und Kleinschreibung unterschieden wird | Der Kampagnenname. |
| Gruppe hinzufügen (als ein Wort) | Zeichenfolge, bei der zwischen Groß- und Kleinschreibung unterschieden wird | Der Anzeigengruppenname. |
| Schlüsselwort | Zeichenfolge, bei der zwischen Groß- und Kleinschreibung unterschieden wird | (Suchbegriffanzeigen) Der Suchbegriff, der die Anzeige generiert hat. |
| [Metrik] | Ganzzahl | (Optional) Die Anzahl der [was immer die Metrik misst].</br><br>Zu den Standardmetriken gehören Impressionen, Kosten und Klicks. Sie können beliebige zusätzliche Metriken aus dem Werbenetzwerk einbeziehen. Schließen Sie jede Metrik in eine separate Spalte ein.<br><br><b>Hinweise:</b><ul><li>Die Spaltenüberschrift für Kosten muss &quot;Kosten (KRW)&quot;lauten.</li><li>Um Kosten (KRW) für Markenanzeigen einzubeziehen, teilen Sie die monatlichen Fixkosten manuell nach Tag auf Anzeigengruppenebene.</li><li>Entfernen Sie alle Kommas aus den Standardmetrikwerten. Verwenden Sie beispielsweise 1000 anstelle von 1.000.</li><li>Verwenden Sie für Null-Werte 0.</li></ul> |

>[!MORELIKETHIS]
>
>* [Implementierung [!DNL Naver] Nur-Tracking-Konten](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Anhang - Erforderliche Bulksheet-Daten für [!DNL Naver] Konten](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [Hochladen von Traffic- und Konversionsmetriken für [!DNL Naver] Nur-Tracking-Konten](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)

