---
title: Erstellen und Implementieren eines CCPA-Ausschluss-Verkaufssegments
description: Erfahren Sie, wie Sie ein Segment erstellen und implementieren, um Benutzer-IDs aus Opt-out-Kaufanfragen von Verbrauchern zu verfolgen.
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# Erstellen und Implementieren eines CCPA-Ausschluss-Verkaufssegments

Sie können ein Segment erstellen, um Benutzer-IDs aus Opt-out-Kaufanfragen von Verbrauchern auf Ihrer Website gemäß dem California Consumer Privacy Act (CCPA) zu verfolgen. Benutzer bleiben unbegrenzt in CCPA-Opt-out-Segmenten.

Sobald das Segment-Pixel-Tag implementiert ist, beginnt Adobe Advertising, einen Pool von IDs im Namen des Advertisers zu sammeln.

>[!NOTE]
>
>* Informationen zur Kommunikation von CCPA-Opt-out-of-Sale-Anfragen an Adobe Advertising mithilfe der Adobe Experience Platform Privacy Service-API finden Sie unter [https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html).
>* Um Benutzer zu verfolgen, die Webseiten zu Zwecken besuchen, die nicht mit dem Tracking von CCPA-Opt-out-Kaufereignissen in Verbindung stehen, sowie Benutzer, die Anzeigen von Desktop-, Mobil- und CTV-Geräten ausgesetzt sind, erstellen Sie eine [benutzerspezifisches Segment](/help/dsp/audiences/custom-segment-create.md).

1. Erstellen Sie das Segment:

   1. Klicken Sie im Hauptmenü auf **Zielgruppen > Segmente**.

   1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**.

   1. Eindeutige Eingabe **[!UICONTROL Segment Name]**.

      Empfohlener Segmentname: &quot;&lt;*Ihr Advertiser-Name*> - CCPA Opt-out of Sale (zum Beispiel &quot;Acme - CCPA Opt-out of Sale&quot;)

   1. Für [!UICONTROL Segment Type]auswählen **[!UICONTROL CCPA Opt-out of sale]**.

   1. Klicks **[!UICONTROL Save]**.

1. Kopieren Sie ein Pixel-Tag und implementieren Sie es, um das Segment zu verfolgen:

   1. Zurück zu **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Halten Sie in der Segmentzeile den Cursor über das neue Segment und klicken Sie auf **[!UICONTROL Get pixel]**.

   1. Kopieren Sie das Bildpixel (beginnend mit `<img src="https://rtd-tm.everesttech.net"`), um Benutzer-IDs von Desktop- und mobilen Besuchern einer Webseite zu erfassen.

   1. Stellen Sie das Tag dem Advertiser oder Website-Kontakt für die Bereitstellung zur Verfügung. Verwenden Sie dazu den Mechanismus, den das Unternehmen verwendet, um CCPA-Opt-out-Anfragen für den Verkauf zu verfolgen (z. B. die Verwendung einer Consent Management Platform).

      Möglicherweise muss die IT-Abteilung des Werbetreibenden oder eine andere Gruppe die Tag-Bereitstellung planen oder darüber informiert werden.

      Sobald das Pixel implementiert ist, beginnt Adobe Advertising, einen Pool von IDs im Namen des Werbetreibenden zu sammeln.

      Obwohl die Wahl und Logik der Implementierung dem Advertiser obliegt, hier ein Beispiel dafür, wie ein Advertiser das Pixel auslösen kann:

      1. Ein Verbraucher landet auf der Homepage des Werbetreibenden.
      1. Der Verbraucher findet die Schaltfläche &quot;CCPA-Opt-out vom Verkauf&quot;des Werbetreibenden und klickt darauf.
      1. Dem Verbraucher wird eine Liste der Dienstleister angezeigt, mit denen der Werber arbeitet.
      1. Der Verbraucher prüft das Kontrollkästchen, um den Verkauf von Daten an Adobe Advertising abzuwählen.

         Diese Aktion Trigger das Pixel, das ausgelöst und die Cookie-ID des Verbrauchers innerhalb der angegebenen &quot;[!UICONTROL CCPA Opt-out of sale]&quot;.

>[!MORELIKETHIS]
>
>* [Adobe Advertising-Unterstützung für den California Consumer Privacy Act: Unterstützung für Verbraucher-Opt-out](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Info [!UICONTROL CCPA Opt-out-of-Sale] Segmente und Berichte](ccpa-opt-out-about.md)
>* [Abrufen von Opt-out-Berichten für Verbraucher](ccpa-opt-out-segment-report-retrieve.md)
>* [Erstellen und Implementieren eines benutzerdefinierten Segments](custom-segment-create.md)
>* [Über Zielgruppen-Management](audience-about.md)
