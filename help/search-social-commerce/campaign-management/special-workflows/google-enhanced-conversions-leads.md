---
title: Implementieren  [!DNL Google Ads]  erweiterten Konversionen für Leads
description: Erfahren Sie mehr über den Workflow zum Einrichten/ [!DNL Google Ads]  von Konversionen für Leads.
feature: Search Campaign Management, Conversions
exl-id: b708c9f2-2962-45d9-8780-4e96ef2ae8f7
source-git-commit: e0b1a65e3eddc41bed73817dabb6e38b1ef881b5
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# Implementieren [!DNL Google Ads] erweiterten Konvertierungen für Leads

Nur *[!DNL Google Ads]Konten*

[[!DNL Google Ads] Verbesserte Konversionen für Leads](https://support.google.com/google-ads/answer/9888656) ermöglichen es Ihnen, Benutzer mithilfe Ihrer First-Party-Konversionsdaten Offline-Konversionen zuzuordnen. Verwenden Sie erweiterte Konversionen für Leads in Umgebungen, in denen keine Klick-IDs verfügbar sind, z. B. um Telefon- oder E-Mail-Verkäufe zu verfolgen, die aus Website-Leads resultieren.

Innerhalb von Search, Social und Commerce können Sie:

* Zeigen Sie Ihre vorhandenen erweiterten Konversionen für Leads an.

  Search, Social und Commerce synchronisieren Ihre vorhandenen erweiterten Konversionen für Leads täglich um 05:00 Uhr in der Zeitzone des Werbetreibenden.

* Erstellen Sie erweiterte Konversionen für Leads.

* Laden Sie Offline-Konversionsdaten von Erstanbietern hoch, um sie Ihren erweiterten Konversionen für Leads zuzuordnen.

* Nehmen Sie Ihre erweiterten Konversionen für Leads als Metriken in Berichte und als gewichtete Metriken in Ziele zur Optimierung auf.

Um diese Funktion zu verwenden, führen Sie die folgenden Schritte aus. Die Schritte zum Erstellen von Konversionsverfolgungs-Tags und zum Erstellen von Konversionsaktionen können optional rückgängig gemacht werden.

1. Opt-in innerhalb von [!DNL Google Ads] für erweiterte Konversionen für Leads:

   1. Öffnen Sie die Konvertierungseinstellungen des Kontos.

   1. Wählen Sie die Option Erweiterte Konvertierungen für Leads aus und akzeptieren Sie die Nutzungsbedingungen.

   1. Wählen Sie aus, ob ein [!DNL Google]-Tag oder [!DNL Google Tag Manager] zum Erstellen des Konvertierungs-Tags verwendet werden soll.

1. Konfigurieren und implementieren Sie ein Tag zum Tracking der Konversionsaktion.

   Anweisungen finden Sie in der [!DNL Google Ads] Hilfe zum Erstellen von Tags für erweiterte Konversionen für Leads [mit einem  [!DNL Google] -Tag](https://support.google.com/google-ads/answer/11021502) oder [mit [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11347292).

1. Erstellen Sie eine Konversionsaktion für die erweiterte Konversion für Leads innerhalb von [Search, Social, &amp; Commerce](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) oder [Google Ads](https://support.google.com/google-ads/answer/12216226).

   Wenn Sie die Konversionsaktion in Search, Social und Commerce erstellen, geben Sie den **Konversionstyp** als *Konversion importieren* oder *Import.* an

1. Laden Sie so oft wie nötig First-Party-Daten, einschließlich Hash-E-Mail-Adressen oder Telefonnummern, hoch, um sie der Konversion für ein bestimmtes Konto zuzuordnen. Sie können diesen Schritt entweder in [Suche, Social und Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) oder mithilfe von [!DNL Google Data Manager] durchführen.

   * In Search, Social und Commerce können Sie eine Vorlage im [!DNL Microsoft Excel]-Format herunterladen, Ihre Konvertierungsdaten eingeben, die Datei lokal speichern und dann die bearbeitete Datei hochladen. Die Vorlage enthält Spalten, in denen angegeben wird, ob das Einverständnis des Benutzers zum Hochladen von Daten in [!DNL Google] zu Werbezwecken und zur Personalisierung von Anzeigen erteilt wurde.

     Alle hochgeladenen Daten werden in Echtzeit mit [!DNL Google Ads] synchronisiert.

   * Weitere Informationen zum Hochladen von Daten mit [!DNL Google Data Manager] finden Sie unter &quot;[&#x200B; zum Daten-Manager](https://support.google.com/google-ads/answer/14639041).

>[!MORELIKETHIS]
>
>* [Erstellen einer Konversionsaktion für eine  [!DNL Google Ads]  Konversion für Leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Hochladen von Offline-Konversionsdaten für erweiterte Konversionen](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
