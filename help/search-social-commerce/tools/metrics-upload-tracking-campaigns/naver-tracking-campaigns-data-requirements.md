---
title: Datenanforderungen für Traffic- und Konversionsmetriken für  [!DNL Naver] -Tracking-Konten
description: Verweisen Sie auf die Anforderungen für den Datenupload für  [!DNL Naver] -only-Konten.
exl-id: cc8ee5de-2bf2-48fd-9fa7-28421aed673f
feature: Search Tools
TQID: https://experienceleague.adobe.com/e4n2ab469CRIiEmqq5wd97pXSQZ9Dt-tehqJSp125GU
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 226
ht-degree: 0%

---

# Anforderungen an Metrikdaten für Nur-[!DNL Naver]-Tracking-Konten

Im Folgenden finden Sie die Datenanforderungen für [!DNL Naver] Traffic- und Konversionsmetriken für Nur-Tracking-Konten.

Datendateien müssen im TSV-, CSV- oder TXT-Format vorliegen.

Die folgenden Kopfzeilenfelder sind erforderlich und optional. Jede Datenzeile muss einen täglich aggregierten Wert für mindestens ein Metrikfeld enthalten.

| Header-Feld/Spaltenname | Typ | Beschreibung |
| ---- | ---- | ---- |
| Zeitraum | DateTime | Das Datum, für das die Daten gelten, im Format `YYYY.MM.DD.` (z. B. `2019.11.15.` mit einem Zeitraum nach dem Tag). |
| Campaign | Zeichenfolge unter Berücksichtigung der Groß-/Kleinschreibung | Der Kampagnenname. |
| Anzeigengruppe (als ein Wort) | Zeichenfolge unter Berücksichtigung der Groß-/Kleinschreibung | Der Name der Anzeigengruppe. |
| Schlüsselwort | Zeichenfolge unter Berücksichtigung der Groß-/Kleinschreibung | (Keyword Ads) Das Keyword, das die Anzeige generiert hat. |
| [metrisch] | Ganzzahl | (Optional) Die Anzahl der [unabhängig von der Metrik].</br><br>Standardmetriken umfassen Impressionen, Kosten und Klicks. Sie können beliebige zusätzliche Metriken vom Anzeigennetzwerk einbeziehen. Schließen Sie jede Metrik in einer separaten Spalte ein.<br><br><b>Hinweise:</b><ul><li>Die Spaltenüberschrift für Kosten muss „Kosten (KRW)“ lauten.</li><li>Um die Kosten (KRW) für Markenanzeigen einzubeziehen, teilen Sie die monatlichen Fixkosten auf Anzeigengruppenebene manuell nach Tag auf.</li><li>Entfernen Sie alle Kommas aus Standardmetrikwerten. Verwenden Sie beispielsweise 1000 anstelle von 1.000.</li><li>Verwenden Sie für Nullwerte 0.</li></ul> |

>[!MORELIKETHIS]
>
>* [Nur [!DNL Naver] Tracking-Konten implementieren](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Anhang - Erforderliche Bulksheet-Daten für  [!DNL Naver] Konten](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [Traffic- und Konversionsmetriken für  [!DNL Naver] -Tracking-Konten hochladen](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
