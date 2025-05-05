---
title: Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen
description: Erfahren Sie, wie Sie eine Quelle erstellen und verwalten, um Zielgruppen aus Ihrer Kundendatenplattform zu importieren und sie in Segmente mit universellen IDs zu konvertieren.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: e9ce180e302f619c85a3d6db813c83903e437d04
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 0%

---

# Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen

*Beta-Funktion*

Erstellen Sie in DSP eine Quelle für jede Erstanbieter-Zielgruppe in Ihrer Kundendatenplattform, die Sie in Segmente mit angegebenen universellen ID-Typen konvertieren möchten. Sie können die Segmente in das DSP-Konto Ihres Unternehmens oder in ein Advertiser-Konto importieren. Datengebühren werden basierend auf den ausgewählten universellen ID-Typen erhoben. Nachdem Sie eine Quelle erstellt haben, sind zusätzliche Schritte erforderlich, um die Zielgruppen aus jeder Kundendatenplattform aufzunehmen. Siehe den Hinweis am Ende des Vorgangs zum Erstellen einer Quelle.

Sie können später die universellen ID-Typen ändern, in die die Quell-Audience übersetzt wird, und ein Protokoll der Änderungen anzeigen.

Sie können auch eine Quelle löschen.

## Erstellen einer Zielgruppen-Source

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Klicken Sie auf **[!UICONTROL Add Source]**.

1. Wählen Sie im Menü [!UICONTROL Select a Type] Ihre [Kundendatenplattform](source-about.md):

   * *[!UICONTROL RT-CDP]*: Die [!DNL Adobe Real-Time CDP].

   * *[!UICONTROL ActionIQ]*: Die [!DNL ActionIQ] Kundendatenplattform.

   * *[!UICONTROL Amperity]*: Die [!DNL Amperity] Kundendatenplattform.

   * *[!UICONTROL Optimizely]*: Die [!DNL Optimizely] Kundendatenplattform.

   * *[!UICONTROL Tealium CDP]*: (Nur konfigurierte Benutzer) Die [!DNL Tealium] Kundendatenplattform.

1. Geben Sie die [!UICONTROL Data Visibility Level] an: *[!UICONTROL Advertiser]* oder *[!UICONTROL Account]*.

1. Geben Sie die verbleibenden [Quelleinstellungen](#source-settings) ein.

   Eine Kopie des generierten [!UICONTROL Source Key] beibehalten. Sie benötigen den Wert später.

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!NOTE]
>
>Nachdem Sie eine Quelle für Ihre Kundendatenplattform erstellt haben, müssen Sie zusätzliche Schritte ausführen, um Ihre Audience zu importieren. Siehe [Workflow für [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md), <!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), --> der [Workflow für [!DNL Amperity]](source-amperity.md), [Workflow für [!DNL Optimizely]](source-optimizely.md) und [Workflow für [!DNL Tealium]](source-tealium.md).

## Ändern der ID-Typen für eine Zielgruppen-Source

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Halten Sie den Cursor über der Quellzeile und klicken Sie auf **[!UICONTROL Edit]**.

1. Ändern Sie die [IDs, die für die Quelle ausgewählt wurden](#source-settings).

1. Klicken Sie auf **[!UICONTROL Save]**.

## Löschen einer Zielgruppen-Source

Durch das Löschen einer Quelle werden die übersetzten Segmente aus der Quelle entfernt.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Halten Sie den Cursor über der Quellzeile und klicken Sie auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

## Anzeigen des Änderungsprotokolls für eine Zielgruppen-Source

Sie können Details zu Änderungen an einem Zielgruppen-Quelldatensatz anzeigen und optional Notizen an das Protokoll anhängen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Halten Sie den Cursor über der Quellzeile und klicken Sie auf **[!UICONTROL Change log]**.

1. (Optional) So fügen Sie dem Änderungsprotokoll einen Hinweis hinzu:

   1. Halten Sie den Cursor über der Quellzeile und klicken Sie auf **[!UICONTROL Add Notes]**.

   1. Geben Sie die Anmerkung ein, und klicken Sie dann auf **[!UICONTROL Save]**.

      Die maximale Länge beträgt 256 Zeichen.

1. (Optional) Um das Protokoll in einem größeren Detailbildschirm zu öffnen, halten Sie den Cursor über der Quellzeile und klicken Sie auf **[!UICONTROL View Details]**.

## Einstellungen für Audience Source {#source-settings}

**[!UICONTROL Data Visibility Level]:** Ob die Segmente einem einzelnen Advertiser mit Zugriff auf das Konto (*[!UICONTROL Advertiser]*) oder allen Advertisern mit Zugriff auf das *[!UICONTROL Account]* zur Verfügung stehen.

**[!UICONTROL Advertiser]:** (Nur Sichtbarkeit auf Advertiser-Ebene) Der Advertiser, für den die Segmente verfügbar sind. Wählen Sie einen aus der Liste der Advertiser mit Zugriff auf das Konto aus.

**[!UICONTROL Enter IMS Org Id]:** (nur [!DNL Real-Time CDP]) Die Adobe Experience Cloud-Organisations-ID für das [!DNL Adobe Experience Platform].

**[!UICONTROL Convert PII to the following IDs]:** Die ID-Typen, in die Sie Ihre personenbezogenen Daten (PII) konvertieren. Wenn Sie mehrere Typen auswählen, wird das generierte Segment mit Werten für jeden ausgewählten ID-Typ gefüllt (z. B. eine [!DNL RampID] und eine [!DNL Unified ID2.0] für jede E-Mail-Adresse). Die Datengebühren werden entsprechend berechnet.

Für [!DNL RampID] und [!DNL Unified ID2.0] sucht der Anbieter nach jeder E-Mail-Adresse, um festzustellen, ob bereits eine ID vorhanden ist, und übersetzt die Adresse in eine entsprechende ID, sofern verfügbar. Wenn für die Adresse keine ID vorhanden ist, wird eine neue ID erstellt.

>[!NOTE]
>
>Sie können nur einen ID-Typ in einer Platzierung auswählen. Um die Leistung nach ID-Typ zu testen[ erstellen Sie für ](/help/dsp/campaign-management/placements/placement-create.md) ID-Typ im Segment eine separate Platzierung.

* *[!DNL RampID]:* Konvertieren von personenbezogenen Daten in ein [!DNL RampID]. Sie können [!DNL RampIDs] für die Retargeting-Zielgruppenbestimmung der angemeldeten Benutzer und für [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) Messung verwenden.

* *[!DNL Unified ID2.0] (Beta):* Konvertieren von personenbezogenen Daten in eine [Unified ID 2.0](https://unifiedid.com)-ID für die erneute Zielgruppenbestimmung von angemeldeten Benutzenden.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** Die Nutzungsbedingungen für die Konvertierung von personenbezogenen Daten in universelle IDs. Sie oder ein anderer Benutzer im DSP-Konto muss die Bedingungen nur einmal akzeptieren, bevor Sie Daten in einen neuen ID-Typ konvertieren können. Für Kunden mit verwalteten Service-Verträgen wird Ihr Adobe-Account-Team Ihre Zustimmung einholen und die Bedingungen im Namen Ihres Unternehmens akzeptieren. Um die Bedingungen zu lesen, klicken Sie auf **>**. Um die Bedingungen zu akzeptieren, scrollen Sie zum Ende der Bedingungen und klicken Sie auf **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Schreibgeschützt; wird automatisch generiert) Der Quellschlüssel, den Sie zum Erstellen einer Zielverbindung in der Kundendatenplattform verwenden können, um Zielgruppen an Advertising DSP zu senden. Sie können den Wert in die Zwischenablage kopieren, um ihn in die Zielverbindungseinstellungen oder in eine Datei einzufügen.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](source-about.md)
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Konvertieren von Benutzer-IDs  [!DNL Adobe Real-Time CDP]  universelle IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertieren von Benutzer-IDs  [!DNL Amperity]  universelle IDs](/help/dsp/audiences/sources/source-amperity.md)
>* [Konvertieren von Benutzer-IDs  [!DNL Optimizely]  universelle IDs](/help/dsp/audiences/sources/source-optimizely.md)
>* [Konvertieren von Benutzer-IDs  [!DNL Tealium]  universelle IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Über die Zielgruppenverwaltung](/help/dsp/audiences/audience-about.md)
