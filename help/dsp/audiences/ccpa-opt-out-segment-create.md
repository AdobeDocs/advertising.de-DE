---
title: Erstellen und Implementieren eines CCPA-Opt-out vom Verkauf -Segments
description: Erfahren Sie, wie Sie ein Segment erstellen und implementieren, um Benutzer-IDs aus Verbraucher-Opt-out-Kaufanfragen zu verfolgen.
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
TQID: https://experienceleague.adobe.com/NYXgnUkEw4uSilL8LO8qlRPp5AVAjXeXNS0pVeIZl3Y
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: c193c532-b70e-4556-bde7-857186cbe140
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 0%

---

# Erstellen und Implementieren eines CCPA-Opt-out vom Verkauf -Segments

Sie können gemäß dem California Consumer Privacy Act (CCPA) ein Segment erstellen, um Benutzer-IDs aus Verbraucher-Opt-out-Kaufanfragen auf Ihrer Website zu verfolgen. Benutzende bleiben auf unbestimmte Zeit in CCPA-Opt-out-of-Sale-Segmenten.

Sobald das Segment-Pixel-Tag implementiert ist, beginnt Adobe Advertising mit der Erfassung eines Pools von IDs im Namen des Werbetreibenden.

>[!NOTE]
>
>* Informationen zur Kommunikation von CCPA-Opt-out-Anfragen an Adobe Advertising mithilfe der Adobe Experience Platform Privacy Service-API finden Sie unter [https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html).
>* Um Benutzende, die Web-Seiten für Zwecke besuchen, die nicht mit dem Tracking von CCPA-Opt-out-of-Sale-Ereignissen zusammenhängen, sowie Benutzende, die Anzeigen von Desktop-, Mobile- und CTV-Geräten ausgesetzt sind, zu verfolgen, erstellen Sie ein [benutzerdefiniertes Segment](/help/dsp/audiences/custom-segment-create.md).

1. Erstellen Sie das Segment:

   1. Klicken Sie im Hauptmenü auf **Zielgruppen > Segmente**.

   1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**.

   1. Eindeutige **[!UICONTROL Segment Name]** eingeben.

      Empfohlener Segmentname: &quot;*Ihr Advertiser-Name*> - CCPA-Opt-out vom Verkauf“ (z. B. „Acme - CCPA-Opt-out vom Verkauf„)

   1. Wählen Sie für die [!UICONTROL Segment Type] **[!UICONTROL CCPA Opt-out of sale]** aus.

   1. Klicken Sie auf **[!UICONTROL Save]**.

1. Kopieren Sie ein Pixel-Tag und implementieren Sie es, um das Segment zu verfolgen:

   1. Kehren Sie zu **[!UICONTROL Audiences]** > **[!UICONTROL Segments]** zurück.

   1. Halten Sie in der Segmentzeile den Cursor über das neue Segment und klicken Sie auf **[!UICONTROL Get pixel]**.

   1. Kopieren Sie das Bild-Pixel (beginnend mit `<img src="https://rtd-tm.everesttech.net"`), um Benutzer-IDs von Desktop- und Mobile-Besuchern auf einer Web-Seite zu erfassen.

   1. Stellen Sie dem Advertiser oder dem Kontakt auf der Website das Tag zur Bereitstellung bereit, indem Sie den Mechanismus verwenden, den das Unternehmen zur Verfolgung von CCPA-Opt-out-Kaufanfragen verwendet (z. B. mithilfe einer Einverständnisverwaltungsplattform).

      Möglicherweise muss die IT-Abteilung oder andere Gruppe des Werbetreibenden die Tag-Bereitstellung planen oder darüber informiert werden.

      Sobald das Pixel implementiert ist, beginnt Adobe Advertising mit der Erfassung eines Pools von IDs im Namen des Werbetreibenden.

      Obwohl die Auswahl und Logik der Implementierung Sache des Advertisers ist, finden Sie hier ein Beispiel dafür, wie ein Advertiser das Pixel auslösen könnte:

      1. Ein Verbraucher landet auf der Homepage des Werbetreibenden.
      1. Der Verbraucher findet und klickt auf die Schaltfläche „CCPA Opt-out vom Verkauf“ des Werbetreibenden.
      1. Dem Verbraucher wird eine Liste von Dienstleistern vorgelegt, mit denen der Werbetreibende zusammenarbeitet.
      1. Der Verbraucher aktiviert das Kontrollkästchen, um den Verkauf von Daten an Adobe Advertising abzuwählen.

         Durch diese Aktion wird das Pixel ausgelöst und die Cookie-ID des Verbrauchers innerhalb des angegebenen Segments &quot;[!UICONTROL CCPA Opt-out of sale]&quot; erfasst.

>[!MORELIKETHIS]
>
>* [Adobe Advertising-Unterstützung für den California Consumer Privacy Act: Unterstützung für Verbraucher-Opt-out vom Verkauf](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Über [!UICONTROL CCPA Opt-out-of-Sale] Segmente und Berichte](ccpa-opt-out-about.md)
>* [Abrufen von Opt-out-Verkaufsberichten von Kundinnen und Kunden](ccpa-opt-out-segment-report-retrieve.md)
>* [Erstellen und Implementieren eines benutzerdefinierten Segments](custom-segment-create.md)
>* [Über die Zielgruppenverwaltung](audience-about.md)
