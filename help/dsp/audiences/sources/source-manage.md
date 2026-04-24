---
title: Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen
description: Erfahren Sie, wie Sie eine Quelle erstellen und verwalten, um Zielgruppen aus Ihrer Kundendatenplattform zu importieren und sie in Segmente mit universellen IDs zu konvertieren.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
TQID: https://experienceleague.adobe.com/us8NC8BEngb240MAW8hEo-DHGoW7MRDWvu0HedMsnFs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: 761
ht-degree: 0%

---

# Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen

*Beta-Funktion*

Erstellen Sie in DSP eine Quelle für jede Erstanbieter-Zielgruppe in Ihrer Kundendatenplattform, die Sie in Segmente mit angegebenen universellen ID-Typen konvertieren möchten. Sie können die Segmente in das DSP-Konto Ihres Unternehmens oder in ein Advertiser-Konto importieren. Datengebühren werden basierend auf den ausgewählten universellen ID-Typen erhoben. Nachdem Sie eine Quelle erstellt haben, sind zusätzliche Schritte erforderlich, um die Zielgruppen aus jeder Kundendatenplattform aufzunehmen. Siehe den Hinweis am Ende des Vorgangs zum Erstellen einer Quelle.

Sie können später die universellen ID-Typen ändern, in die die Quell-Audience übersetzt wird, und ein Protokoll der Änderungen anzeigen.

Sie können auch eine Quelle löschen.

## Erstellen einer Zielgruppenquelle

<!--
 Not sure about this

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

## Ändern der ID-Typen für eine Zielgruppenquelle

<!-- 
Clarify this:

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses that you shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we don't delete any historical IDs of that type from the segments shared through the source.

-->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Halten Sie den Cursor über der Quellzeile und klicken Sie auf **[!UICONTROL Edit]**.

1. Ändern Sie die [IDs, die für die Quelle ausgewählt wurden](#source-settings).

1. Klicken Sie auf **[!UICONTROL Save]**.

## Löschen einer Zielgruppenquelle

Durch das Löschen einer Quelle werden die übersetzten Segmente aus der Quelle entfernt.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Halten Sie den Cursor über der Quellzeile und klicken Sie auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

## Anzeigen des Änderungsprotokolls für eine Zielgruppenquelle

Sie können Details zu Änderungen an einem Zielgruppen-Quelldatensatz anzeigen und optional Notizen an das Protokoll anhängen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Halten Sie den Cursor über der Quellzeile und klicken Sie auf **[!UICONTROL Change log]**.

1. (Optional) So fügen Sie dem Änderungsprotokoll einen Hinweis hinzu:

   1. Halten Sie den Cursor über der Quellzeile und klicken Sie auf **[!UICONTROL Add Notes]**.

   1. Geben Sie die Anmerkung ein, und klicken Sie dann auf **[!UICONTROL Save]**.

      Die maximale Länge beträgt 256 Zeichen.

1. (Optional) Um das Protokoll in einem größeren Detailbildschirm zu öffnen, halten Sie den Cursor über der Quellzeile und klicken Sie auf **[!UICONTROL View Details]**.

## Einstellungen der Zielgruppenquelle {#source-settings}

**[!UICONTROL Data Visibility Level]:** Ob die Segmente einem einzelnen Advertiser mit Zugriff auf das Konto (*[!UICONTROL Advertiser]*) oder allen Advertisern mit Zugriff auf das *[!UICONTROL Account]* zur Verfügung stehen.

**[!UICONTROL Advertiser]:** (Nur Sichtbarkeit auf Advertiser-Ebene) Der Advertiser, für den die Segmente verfügbar sind. Select one from the list of advertisers with access to the account.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] sources only) The Adobe CX Enterprise organization ID for the [!DNL Adobe Experience Platform] account.

**[!UICONTROL Convert PII to the following IDs]:** The ID types to which you&#39;ll convert your personally identifiable information (PII). If you select multiple types, the generated segment is populated with values for each selected ID type (such as a [!DNL RampID] and a [!DNL Unified ID2.0] for each email address). Data charges are applied accordingly.

For [!DNL RampID] and [!DNL Unified ID2.0], the vendor looks up each email address to see if an ID already exists and translates the address to a matching ID when available. If an ID doesn&#39;t exist for the address, then it creates a new ID.

>[!NOTE]
>
>You can target only one type of ID in a single placement. To test performance by ID type, [create a separate placement](/help/dsp/campaign-management/placements/placement-create.md) for each ID type in the segment.

* *[!DNL RampID]:* To convert PII to a [!DNL RampID]. You can use [!DNL RampIDs] for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

* *[!DNL Unified ID2.0] (Beta):* To convert PII to a [Unified ID 2.0](https://unifiedid.com) ID for retargeting logging-in users.

<!--
 Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** The terms of service agreement for converting PII to universal IDs. You or another user in the DSP account must accept the terms once before you can convert data to a new ID type. For customers with managed service contracts, your Adobe Account Team gets your consent and accepts the terms on your organization&#39;s behalf. To read the terms, click **>**. To accept the terms, scroll to the bottom of the terms and click **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Read-only; generated automatically) The source key that you can use to create a destination connection in the customer data platform to push audiences to Advertising DSP. You can copy the value to your clipboard to paste into the destination connection settings or into a file.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](source-about.md)
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Convert user IDs from [!DNL Adobe Real-Time CDP] to universal IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convert user IDs from [!DNL Amperity] to universal IDs](/help/dsp/audiences/sources/source-amperity.md)
>* [Convert user IDs from [!DNL Optimizely] to universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
>* [Convert user IDs from [!DNL Tealium] to universal IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Über die Zielgruppenverwaltung](/help/dsp/audiences/audience-about.md)
