---
title: Implementieren von [!DNL Google Ads] erweiterten Konvertierungen für Leads
description: Erfahren Sie mehr über den Workflow zum Einrichten von  [!DNL Google Ads] erweiterten Konvertierungen für Leads.
feature: Search Campaign Management, Conversions
exl-id: b708c9f2-2962-45d9-8780-4e96ef2ae8f7
source-git-commit: 56161ece4ba9c01cddb86e16796150c391f1a811
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# Implementieren von [!DNL Google Ads] erweiterten Konversionen für Leads

*[!DNL Google Ads]nur Konten*

Mit [[!DNL Google Ads] erweiterten Konversionen für Leads](https://support.google.com/google-ads/answer/9888656) können Sie Benutzer mithilfe Ihrer Erstanbieter-Konversionsdaten Offline-Konversionen zuordnen. Verwenden Sie erweiterte Konversionen für Leads in Umgebungen, in denen Klick-IDs nicht verfügbar sind, z. B. zur Verfolgung von Telefon- oder E-Mail-Verkäufen, die aus Website-Leads resultieren.

In Search, Social und Commerce haben Sie folgende Möglichkeiten:

* Zeigen Sie Ihre vorhandenen erweiterten Konversionen für Leads an.

  Suchen, Social und Commerce synchronisiert Ihre vorhandenen erweiterten Konversionen für Leads täglich um 05:00 Uhr in der Zeitzone des Advertisers.

* Erstellen Sie erweiterte Konversionen für Leads.

* Laden Sie Erstanbieter- und Offline-Konversionsdaten hoch, um sie Ihren erweiterten Konversionen für Leads zuzuordnen.

* Schließen Sie Ihre erweiterten Konversionen für Leads als Metriken in Berichten und als gewichtete Metriken in Ziele zur Optimierung ein.

Führen Sie die folgenden Schritte aus, um diese Funktion zu verwenden. Die Schritte zum Erstellen von Konversions-Tracking-Tags und zum Erstellen von Konversionsaktionen können optional rückgängig gemacht werden.

1. Aktivieren Sie in [!DNL Google Ads] die Option für erweiterte Konvertierungen für Leads:

   1. Öffnen Sie die Konvertierungseinstellungen des Kontos.

   1. Wählen Sie die Option für erweiterte Konvertierungen für Leads aus und akzeptieren Sie die Dienstbedingungen.

   1. Wählen Sie aus, ob zum Erstellen des Konversions-Tags ein [!DNL Google] -Tag oder [!DNL Google Tag Manager] verwendet werden soll.


1. Konfigurieren und implementieren Sie ein [!DNL Google] -Tag für die Konvertierungsaktion.

   Anweisungen finden Sie in der [!DNL Google Ads]-Hilfe zum Erstellen von Tags für erweiterte Konvertierungen für Leads [mit einem  [!DNL Google] Tag](https://support.google.com/google-ads/answer/11021502) oder [mit  [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11347292).

1. Erstellen Sie eine Konversionsaktion für die erweiterte Konversion von Leads in [Search, Social und Commerce](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) oder [Google Ads](https://support.google.com/google-ads/answer/12216226).

   Wählen Sie für den Konversionstyp **die Option *Konvertierung importieren* oder den Wert *Importieren* aus.**

1. Laden Sie beliebig oft Erstanbieterdaten hoch, einschließlich Hash-E-Mail-Adressen oder Telefonnummern, um der Konversion für ein bestimmtes Konto zuzuordnen. Sie können diesen Schritt entweder in [Suche, Social und Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) oder mit [!DNL Google Data Manager] durchführen.

   * In Search, Social und Commerce können Sie eine Vorlage im Format [!DNL Microsoft Excel] herunterladen, Ihre Konversionsdaten eingeben, die Datei lokal speichern und dann die bearbeitete Datei hochladen. Die Vorlage enthält Spalten, die angeben, ob die Zustimmung des Benutzers zum Hochladen von Daten zu Werbezwecken und zur Anzeigenpersonalisierung an [!DNL Google] erteilt wurde.

     Alle hochgeladenen Daten werden in Echtzeit mit [!DNL Google Ads] synchronisiert.

   * Weitere Informationen zum Hochladen von Daten mit [!DNL Google Data Manager] finden Sie unter &quot;[Über den Daten-Manager](https://support.google.com/google-ads/answer/14639041)&quot;.

>[!MORELIKETHIS]
>
>* [Erstellen Sie eine Konversionsaktion für eine [!DNL Google Ads] erweiterte Konversion für Leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Hochladen von Offline-Konversionsdaten für erweiterte Konvertierungen](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
