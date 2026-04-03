---
title: Implementieren  [!DNL Microsoft Advertising]  erweiterten Konversionen für Offline-Konversionen
description: Erfahren Sie mehr über den Workflow zum Einrichten  [!DNL Microsoft Advertising]  erweiterten Konvertierungen für Offline-Konvertierungen.
feature: Search Campaign Management, Conversions
exl-id: 44937db7-9e80-4a5d-85c7-5bd5febc3b96
TQID: https://experienceleague.adobe.com/GLFczqDqV8HE5hUZt8ORAlQMNy4OqQTtMdaHoYoN10U
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 0%

---

# Implementieren [!DNL Microsoft Advertising] erweiterten Konvertierungen für Offline-Konvertierungen

Nur *[!DNL Microsoft Advertising]Konten*

[[!DNL Microsoft Advertising] Erweiterte Konversionen](https://help.ads.microsoft.com/#apex/ads/en/60178) ermöglichen es Ihnen, Benutzer mithilfe Ihrer First-Party-Konversionsdaten Offline-Konversionen zuzuordnen. Verwenden Sie erweiterte Konversionen in Umgebungen, in denen keine Klick-IDs verfügbar sind, z. B. zum Nachverfolgen von Telefon- oder E-Mail-Verkäufen, die aus Website-Leads resultieren.

Innerhalb von Search, Social und Commerce können Sie:

* Anzeigen vorhandener erweiterter Konversionen für Offline-Konversionen

  Search, Social und Commerce synchronisieren Ihre vorhandenen erweiterten Konversionen täglich um 05 :00 in der Zeitzone des Werbetreibenden.

* Laden Sie Offline-Konversionsdaten von Erstanbietern hoch, um sie Ihren vorhandenen erweiterten Konversionszielen zuzuordnen.

* Nehmen Sie Ihre erweiterten Konversionen als Metriken in Berichte und als gewichtete Metriken in Ziele zur Optimierung auf.

Um diese Funktion zu verwenden, führen Sie die folgenden Schritte aus.

1. Befolgen Sie alle Voraussetzungen in der [!DNL Microsoft Advertising]-Hilfe unter &quot;[ Konversionen](https://help.ads.microsoft.com/#apex/ads/en/60178).

1. [Richten Sie in ein erweitertes Konversionsziel  [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/60178).

1. Laden Sie so oft wie nötig First-Party-Daten, einschließlich Hash-E-Mail-Adressen oder Telefonnummern, hoch, um sie der Konversion für ein bestimmtes Konto zuzuordnen. Sie können diesen Schritt entweder in [Suche, Social und Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) oder in [!DNL Microsoft Advertising] ausführen.

   * In Search, Social und Commerce können Sie eine Vorlage im [!DNL Microsoft Excel]-Format herunterladen, Ihre Konvertierungsdaten eingeben, die Datei lokal speichern und dann die bearbeitete Datei hochladen.

     Alle hochgeladenen Daten werden in Echtzeit mit [!DNL Microsoft Advertising] synchronisiert.

   * Weitere Informationen zum Hochladen von Daten in [!DNL Microsoft Advertising] finden Sie im Abschnitt „Einrichten erweiterter Konvertierungen für Offline-Konvertierungen“ in der [!DNL Microsoft Advertising]-Hilfe zu &quot;[Erweiterte Konvertierungen](https://help.ads.microsoft.com/#apex/ads/en/60178).

>[!MORELIKETHIS]
>
>* [Hochladen von Offline-Konversionsdaten für erweiterte Konversionen](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
