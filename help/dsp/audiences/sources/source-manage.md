---
title: Verwalten von Zielgruppenquellen zum Aktivieren von universellen ID-Zielgruppen
description: Erfahren Sie, wie Sie eine Quelle erstellen und verwalten, um Zielgruppen aus Ihrer Kundendatenplattform zu importieren und in Segmente mit universellen IDs zu konvertieren.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 02ed538a48a4ba0323f9b75938ee6b007c6e0fd7
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 0%

---

# Verwalten von Zielgruppenquellen zum Aktivieren von universellen ID-Zielgruppen

*Beta-Funktion*

Erstellen Sie eine Quelle in DSP für jede Erstanbieter-Zielgruppe in Ihrer Kundendatenplattform, die Sie in Segmente mit bestimmten universellen ID-Typen konvertieren möchten. Sie können die Segmente in das DSP Ihrer Organisation oder in ein Advertiser-Konto importieren. Datenentgelte werden auf der Grundlage der ausgewählten universellen ID-Typen angewendet. Nachdem Sie eine Quelle erstellt haben, sind zusätzliche Schritte erforderlich, um die Zielgruppen aus den einzelnen Kundendatenplattformen zu erfassen. Lesen Sie den Hinweis am Ende des Verfahrens, um eine Quelle zu erstellen.

Sie können später die universellen ID-Typen ändern, in die die Quellzielgruppe übersetzt wird, und ein Protokoll der Änderungen anzeigen.

Sie können auch eine Quelle löschen.

## Erstellen einer Audience Source

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Klicken Sie auf **[!UICONTROL Add Source]**.

1. Wählen Sie im Menü [!UICONTROL Select a Type] Ihre [Kundendatenplattform](source-about.md) aus:

   * *[!UICONTROL RT-CDP]*: Der [!DNL Adobe Real-Time Customer Data Platform].

   * *[!UICONTROL ActionIQ]*: Die [!DNL ActionIQ] Kundendatenplattform.

   * *[!UICONTROL Amperity]*: Die [!DNL Amperity] Kundendatenplattform.

   * *[!UICONTROL Optimizely]*: Die [!DNL Optimizely] Kundendatenplattform.

   * *[!UICONTROL Tealium CDP]*: (Nur konfigurierte Benutzer) Die [!DNL Tealium] Kundendatenplattform.

1. Geben Sie die [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* oder *[!UICONTROL Account]* an.

1. Geben Sie die restlichen [Quelleinstellungen](#source-settings) ein.

   Behalten Sie eine Kopie der generierten [!UICONTROL Source Key] bei. Du wirst den Wert später benötigen.

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!NOTE]
>
>Nachdem Sie eine Quelle für Ihre Kundendatenplattform erstellt haben, müssen Sie zusätzliche Schritte ausführen, um Ihre Zielgruppe zu importieren. Siehe den [Workflow für  [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md), <!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), --> den [Workflow für  [!DNL Amperity]](source-amperity.md), den [Workflow für  [!DNL Optimizely]](source-optimizely.md) und den [Workflow für  [!DNL Tealium]](source-tealium.md).

## Ändern der ID-Typen für eine Audience Source

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Halten Sie den Cursor über die Quellzeile und klicken Sie auf **[!UICONTROL Edit]**.

1. Ändern Sie die für die Quelle ausgewählten [IDs](#source-settings).

1. Klicken Sie auf **[!UICONTROL Save]**.

## Löschen von Audience Source

Durch Löschen einer Quelle werden die über die Quelle übersetzten Segmente entfernt.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Halten Sie den Cursor über die Quellzeile und klicken Sie auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

## Anzeigen des Änderungsprotokolls für eine Audience Source

Sie können Details zu Änderungen an einem Audience-Quelldatensatz anzeigen und optional Notizen zum Protokoll anhängen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Halten Sie den Cursor über die Quellzeile und klicken Sie auf **[!UICONTROL Change log]**.

1. (Optional) So fügen Sie dem Änderungsprotokoll einen Hinweis hinzu:

   1. Halten Sie den Cursor über die Quellzeile und klicken Sie auf **[!UICONTROL Add Notes]**.

   1. Geben Sie die Notiz ein und klicken Sie dann auf **[!UICONTROL Save]**.

      Die maximale Länge beträgt 256 Zeichen.

1. (Optional) Um das Protokoll in einem größeren Detailbildschirm zu öffnen, halten Sie den Cursor über die Quellzeile und klicken Sie auf **[!UICONTROL View Details]**.

## Audience Source-Einstellungen {#source-settings}

**[!UICONTROL Data Visibility Level]:** Gibt an, ob die Segmente für einen einzelnen Advertiser mit Zugriff auf das Konto (*[!UICONTROL Advertiser]*) oder für alle Advertiser mit Zugriff auf das Konto verfügbar sind *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Nur Sichtbarkeit auf Advertiser-Ebene) Der Advertiser, für den die Segmente verfügbar sind. Wählen Sie einen aus der Liste der Advertiser mit Zugriff auf das Konto aus.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] nur Quellen) Die Adobe Experience Cloud-Organisations-ID für das [!DNL Adobe Experience Platform]-Konto.

**[!UICONTROL Convert PII to the following IDs]:** Die ID-Typen, in die Sie Ihre personenbezogenen Daten (PII) konvertieren. Wenn Sie mehrere Typen auswählen, wird das generierte Segment mit Werten für jeden ausgewählten ID-Typ gefüllt (z. B. [!DNL RampID] und ein [!DNL Unified ID2.0] für jede E-Mail-Adresse). Die Datengebühren werden entsprechend angewendet.

Bei [!DNL RampID] und [!DNL Unified ID2.0] sucht der Anbieter jede E-Mail-Adresse, um zu sehen, ob bereits eine ID vorhanden ist, und übersetzt die Adresse in eine übereinstimmende ID, sofern verfügbar. Wenn für die Adresse keine ID vorhanden ist, wird eine neue ID erstellt.

>[!NOTE]
>
>Sie können nur einen ID-Typ in einer Platzierung als Ziel auswählen. Um die Leistung nach ID-Typ zu testen, erstellen Sie [eine separate Platzierung](/help/dsp/campaign-management/placements/placement-create.md) für jeden ID-Typ im Segment.

* *[!DNL RampID]:* So konvertieren Sie personenbezogene Daten in eine [!DNL RampID]. Sie können [!DNL RampIDs] für die Retargeting-Anmeldung und für die Messung [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) verwenden.

* *[!DNL Unified ID2.0](Beta):* So konvertieren Sie personenbezogene Daten in eine [einheitliche ID 2.0](https://unifiedid.com)-ID für Benutzer, die sich erneut anmelden.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** Die Nutzungsbedingungen für die Konvertierung von personenbezogenen Daten in universelle IDs. Sie oder ein anderer Benutzer im DSP müssen die Bedingungen einmal akzeptieren, bevor Sie Daten in einen neuen ID-Typ konvertieren können. Für Kunden mit verwalteten Serviceverträgen erhält Ihr Adobe Account Team Ihre Einwilligung und akzeptiert die Bedingungen im Namen Ihres Unternehmens. Um die Begriffe zu lesen, klicken Sie auf **>**. Um die Bedingungen zu akzeptieren, scrollen Sie zum unteren Rand der Bedingungen und klicken Sie auf **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Schreibgeschützt; automatisch generiert) Der Quellschlüssel, den Sie zum Erstellen einer Zielverbindung in der Kundendatenplattform verwenden können, um Zielgruppen an Advertising DSP zu senden. Sie können den Wert in die Zwischenablage kopieren, um ihn in die Zielverbindungseinstellungen oder in eine Datei einzufügen.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](source-about.md)
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Konvertieren von Benutzer-IDs aus  [!DNL Adobe Real-Time CDP] in universelle IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertieren von Benutzer-IDs aus  [!DNL Amperity] in universelle IDs](/help/dsp/audiences/sources/source-amperity.md)
>* [Konvertieren von Benutzer-IDs aus  [!DNL Optimizely] in universelle IDs](/help/dsp/audiences/sources/source-optimizely.md)
>* [Konvertieren von Benutzer-IDs aus  [!DNL Tealium] in universelle IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
