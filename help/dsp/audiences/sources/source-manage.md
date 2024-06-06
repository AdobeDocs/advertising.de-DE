---
title: Verwalten von Zielgruppenquellen zum Aktivieren von universellen ID-Zielgruppen
description: Erfahren Sie, wie Sie eine Quelle erstellen und verwalten, um Zielgruppen aus Ihrer Kundendatenplattform zu importieren und in Segmente mit universellen IDs zu konvertieren.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 9411089703ce0b9502c1c2522cce999c3a5fafbf
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 0%

---

# Verwalten von Zielgruppenquellen zum Aktivieren von universellen ID-Zielgruppen

*Beta-Funktion*

Erstellen Sie eine Quelle in DSP für jede Erstanbieter-Zielgruppe in Ihrer Kundendatenplattform, die Sie in Segmente mit bestimmten universellen ID-Typen konvertieren möchten. Sie können die Segmente in das DSP Ihrer Organisation oder in ein Advertiser-Konto importieren. Datenentgelte werden auf der Grundlage der ausgewählten universellen ID-Typen angewendet. Nachdem Sie eine Quelle erstellt haben, sind zusätzliche Schritte erforderlich, um die Zielgruppen aus den einzelnen Kundendatenplattformen zu erfassen. Lesen Sie den Hinweis am Ende des Verfahrens, um eine Quelle zu erstellen.

Sie können später die universellen ID-Typen ändern, in die die Quellzielgruppe übersetzt wird, und ein Protokoll der Änderungen anzeigen.

Sie können auch eine Quelle löschen.

## Erstellen einer Zielgruppenquelle

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Klicks **[!UICONTROL Add Source]**.

1. Im [!UICONTROL Select a Type] wählen Sie Ihre Kundendatenplattform aus:

   * *[!UICONTROL RT-CDP]*: [Die [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*: Die [[!DNL ActionIQ] Kundendatenplattform](source-about.md).

   * *[!UICONTROL Tealium CDP]*: (Nur konfigurierte Benutzer) Die [[!DNL Tealium] Kundendatenplattform](source-about.md).

1. Geben Sie die [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* oder *[!UICONTROL Account]*.

1. Den Rest eingeben [Quelleinstellungen](#source-settings).

   Eine Kopie der [!UICONTROL Source Key] wird generiert. Du wirst den Wert später benötigen.

1. Klicks **[!UICONTROL Save]**.

>[!NOTE]
>
>Nachdem Sie eine Quelle für Ihre Kundendatenplattform erstellt haben, müssen Sie weitere Schritte ausführen. Siehe [Workflow zum Import von Audiences aus [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> und [Workflow zum Import von Audiences aus [!DNL Tealium]](source-tealium.md).

## Ändern der ID-Typen für eine Zielgruppenquelle

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Halten Sie den Cursor über die Quellzeile und klicken Sie auf **[!UICONTROL Edit]**.

1. Ändern Sie die [Für die Quelle ausgewählte IDs](#source-settings).

1. Klicks **[!UICONTROL Save]**.

## Eine Zielgruppenquelle löschen

Durch Löschen einer Quelle werden die über die Quelle übersetzten Segmente entfernt.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Halten Sie den Cursor über die Quellzeile und klicken Sie auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsnachricht auf **[!UICONTROL Delete]**.

## Anzeigen des Änderungsprotokolls für eine Zielgruppenquelle

Sie können Details zu Änderungen an einem Audience-Quelldatensatz anzeigen und optional Notizen zum Protokoll anhängen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Halten Sie den Cursor über die Quellzeile und klicken Sie auf **[!UICONTROL Change log]**.

1. (Optional) So fügen Sie dem Änderungsprotokoll einen Hinweis hinzu:

   1. Halten Sie den Cursor über die Quellzeile und klicken Sie auf **[!UICONTROL Add Notes]**.

   1. Geben Sie die Notiz ein und klicken Sie dann auf **[!UICONTROL Save]**.

      Die maximale Länge beträgt 256 Zeichen.

1. (Optional) Um das Protokoll in einem größeren Detailbildschirm zu öffnen, halten Sie den Cursor über die Quellzeile und klicken Sie auf **[!UICONTROL View Details]**.

## Einstellungen der Zielgruppenquelle {#source-settings}

**[!UICONTROL Data Visibility Level]:** Gibt an, ob die Segmente für einen einzelnen Advertiser mit Zugriff auf das Konto verfügbar sind (*[!UICONTROL Advertiser]*) oder für alle Advertiser mit Zugriff auf das Konto *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Nur Sichtbarkeit auf Advertiser-Ebene) Der Advertiser, für den die Segmente verfügbar sind. Wählen Sie einen aus der Liste der Advertiser mit Zugriff auf das Konto aus.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] Nur -Quellen) Die Adobe Experience Cloud-Organisations-ID für die [!DNL Adobe Experience Platform] -Konto.

**[!UICONTROL Convert PII to the following IDs]:** Die ID-Typen, in die Sie Ihre personenbezogenen Daten (PII) konvertieren. Wenn Sie mehrere Typen auswählen, wird das generierte Segment mit Werten für jeden ausgewählten ID-Typ aufgefüllt (z. B. eine [!DNL RampID] und [!DNL Unified ID2.0] für jede E-Mail-Adresse). Die Datengebühren werden entsprechend angewendet.

Für [!DNL RampID] und [!DNL Unified ID2.0]sucht der Anbieter jede E-Mail-Adresse, um zu sehen, ob bereits eine ID vorhanden ist, und übersetzt die Adresse in eine passende ID, sofern verfügbar. Wenn für die Adresse keine ID vorhanden ist, wird eine neue ID erstellt.

>[!NOTE]
>
>Sie können nur einen ID-Typ in einer Platzierung als Ziel auswählen. So testen Sie die Leistung nach ID-Typ: [Erstellen einer separaten Platzierung](/help/dsp/campaign-management/placements/placement-create.md) für jeden ID-Typ im Segment.

* *[!DNL RampID]:* So konvertieren Sie PII in eine [!DNL RampID]. Sie können [!DNL RampIDs] für Benutzer, die sich erneut anmelden, und für [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) Messung.

* *[!DNL Unified ID2.0](Beta):* So konvertieren Sie PII in eine [Unified ID 2.0](https://unifiedid.com) ID für Benutzer, die sich erneut anmelden.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** Die Vertragsbedingungen für die Konvertierung von personenbezogenen Daten in universelle IDs. Sie oder ein anderer Benutzer im DSP müssen die Bedingungen einmal akzeptieren, bevor Sie Daten in einen neuen ID-Typ konvertieren können. Für Kunden mit verwalteten Serviceverträgen erhält Ihr Adobe Account Team Ihre Einwilligung und akzeptiert die Bedingungen im Namen Ihres Unternehmens. Um die Begriffe zu lesen, klicken Sie auf **>**. Um die Bedingungen zu akzeptieren, scrollen Sie zum unteren Rand der Bedingungen und klicken Sie auf **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Schreibgeschützt; automatisch generiert) Der Quellschlüssel, mit dem Sie eine Zielverbindung in der Kundendatenplattform erstellen können, um Zielgruppen an Advertising DSP zu leiten. Sie können den Wert in die Zwischenablage kopieren, um ihn in die Zielverbindungseinstellungen oder in eine Datei einzufügen.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](source-about.md)
>* [Manuelles Importieren authentifizierter Segmente aus [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Adobe Advertising DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
