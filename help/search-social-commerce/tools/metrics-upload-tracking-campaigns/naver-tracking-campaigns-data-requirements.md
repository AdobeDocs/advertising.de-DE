---
title: Datenanforderungen für Traffic- und Konversionsmetriken für "Nur-Tracking"-Konten [!DNL Naver]
description: Verweisen Sie auf die Anforderungen zum Hochladen von Daten für reine [!DNL Naver] Tracking-Konten.
exl-id: cc8ee5de-2bf2-48fd-9fa7-28421aed673f
feature: Search Tools
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Metrikdatenanforderungen für reine [!DNL Naver]-Tracking-Konten

Im Folgenden finden Sie die Datenanforderungen für [!DNL Naver] Traffic- und Konversionsmetriken für reine Tracking-Konten.

Datendateien müssen im TSV-, CSV- oder TXT-Format vorliegen.

Die folgenden Header-Felder sind erforderlich und optional. Jede Datenzeile muss einen täglich aggregierten Wert für mindestens ein Metrikfeld enthalten.

| Header Field/Column Name | Typ | Beschreibung |
| ---- | ---- | ---- |
| Zeitraum | DateTime | Das Datum, für das die Daten gelten, im Format `YYYY.MM.DD.` (z. B. `2019.11.15.` mit einem Punkt nach dem Tag). |
| Kampagne | Groß-/Kleinschreibung beachten | Der Kampagnenname. |
| Gruppe hinzufügen (als ein Wort) | Groß-/Kleinschreibung beachten | Der Anzeigengruppenname. |
| Schlüsselwort | Groß-/Kleinschreibung beachten | (Suchbegriffanzeigen) Der Suchbegriff, der die Anzeige generiert hat. |
| [Metrik] | Ganzzahl | (Optional) Die Anzahl der [für die Metrik, die ] misst.</br><br>Standardmetriken umfassen Impressionen, Kosten und Klicks. Sie können beliebige zusätzliche Metriken aus dem Werbenetzwerk einbeziehen. Schließen Sie jede Metrik in eine separate Spalte ein.<br><br><b>Notizen:</b><ul><li>Die Spaltenüberschrift für Kosten muss &quot;Kosten (KRW)&quot;lauten.</li><li>Um Kosten (KRW) für Markenanzeigen einzubeziehen, teilen Sie die monatlichen Fixkosten manuell nach Tag auf Anzeigengruppenebene.</li><li>Entfernen Sie alle Kommas aus den Standardmetrikwerten. Verwenden Sie beispielsweise 1000 anstelle von 1.000.</li><li>Verwenden Sie für Null-Werte 0.</li></ul> |

>[!MORELIKETHIS]
>
>* [Implementieren von [!DNL Naver] Nur-Tracking-Konten](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Anhang - Erforderliche Bulksheet-Daten für  [!DNL Naver] Konten](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [Hochladen von Traffic- und Konversionsmetriken für  [!DNL Naver] Nur-Tracking-Konten](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
