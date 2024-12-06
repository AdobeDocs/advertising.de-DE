---
title: Implementieren von [!DNL Microsoft Advertising] erweiterten Konvertierungen für Offline-Konvertierungen
description: Erfahren Sie mehr über den Workflow zum Einrichten von [!DNL Microsoft Advertising] erweiterten Konvertierungen für Offline-Konvertierungen.
feature: Search Campaign Management, Conversions
source-git-commit: 8f87e5bdab25aa527e72d7e9c75411267fe63780
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# Implementieren von [!DNL Microsoft Advertising] erweiterten Konvertierungen für Offline-Konvertierungen

*[!DNL Microsoft Advertising]nur Konten*

Mit [[!DNL Microsoft Advertising] erweiterten Konversionen](https://help.ads.microsoft.com/#apex/ads/en/60178) können Sie Benutzer mithilfe Ihrer Erstanbieter-Konversionsdaten Offline-Konversionen zuordnen. Verwenden Sie erweiterte Konversionen in Umgebungen, in denen Klick-IDs nicht verfügbar sind, z. B. zur Verfolgung von Telefon- oder E-Mail-Verkäufen, die aus Website-Leads resultieren.

In Search, Social und Commerce haben Sie folgende Möglichkeiten:

* Zeigen Sie Ihre vorhandenen erweiterten Konversionen für Offline-Konvertierungen an.

  Suchen, Social und Commerce synchronisiert Ihre vorhandenen erweiterten Konversionen täglich um 05:00 Uhr in der Zeitzone des Advertisers.

* Laden Sie Erstanbieter- und Offline-Konversionsdaten hoch, um sie Ihren vorhandenen erweiterten Konversionszielen zuzuordnen.

* Integrieren Sie Ihre erweiterten Konversionen als Metriken in Berichte und als gewichtete Metriken in Ziele zur Optimierung.

Führen Sie die folgenden Schritte aus, um diese Funktion zu verwenden.

1. Befolgen Sie alle Voraussetzungen in der [!DNL Microsoft Advertising] -Hilfe zu &quot;[Erweiterte Konvertierungen](https://help.ads.microsoft.com/#apex/ads/en/60178)&quot;.

1. [ Richten Sie ein erweitertes Konversionsziel innerhalb von  [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/60178) ein.

1. Laden Sie beliebig oft Erstanbieterdaten hoch, einschließlich Hash-E-Mail-Adressen oder Telefonnummern, um der Konversion für ein bestimmtes Konto zuzuordnen. Sie können diesen Schritt entweder innerhalb von [Suchen, Social und Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) oder innerhalb von [!DNL Microsoft Advertising] durchführen.

   * In Search, Social und Commerce können Sie eine Vorlage im Format [!DNL Microsoft Excel] herunterladen, Ihre Konversionsdaten eingeben, die Datei lokal speichern und dann die bearbeitete Datei hochladen.

     Alle hochgeladenen Daten werden in Echtzeit mit [!DNL Microsoft Advertising] synchronisiert.

   * Weitere Informationen zum Hochladen von Daten in [!DNL Microsoft Advertising] finden Sie im Abschnitt &quot;Einrichten von erweiterten Konvertierungen für Offline-Konvertierungen&quot;in der [!DNL Microsoft Advertising] -Hilfe zu &quot;[Erweiterte Konvertierungen](https://help.ads.microsoft.com/#apex/ads/en/60178)&quot;.

>[!MORELIKETHIS]
>
>* [Hochladen von Offline-Konversionsdaten für erweiterte Konvertierungen](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
