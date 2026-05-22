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
source-git-commit: 14a4d5b0bbe27697668b4a1a8eb3a7f74a18cc04
workflow-type: tm+mt
source-wordcount: 881
ht-degree: 0%

---

# Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen

Erstellen Sie in DSP eine Quelle für jede Erstanbieter-Zielgruppe in Ihrer Kundendatenplattform, die Sie importieren oder in Segmente mit angegebenen universellen ID-Typen konvertieren möchten. Sie können die Segmente in das DSP-Konto Ihres Unternehmens oder in ein Advertiser-Konto importieren. Wenn Sie Zielgruppen in universelle IDs konvertieren, werden basierend auf den ausgewählten universellen ID-Typen Gebühren erhoben. Nachdem Sie eine Quelle erstellt haben, sind zusätzliche Schritte erforderlich, um die Quell-Zielgruppen von jeder Kundendatenplattform zu streamen. Siehe den Hinweis am Ende des Vorgangs zum Erstellen einer Quelle.

Für alle Kundendatenplattformen außer [!DNL AdFixus] können Sie später die universellen ID-Typen ändern, in die die Quellzielgruppe übersetzt wird, und ein Protokoll der Änderungen anzeigen.

Sie können auch eine Quelle löschen.

## Erstellen einer Zielgruppenquelle

Sie können für jede Kombination aus universeller ID-Partner-ID und -Konto oder einzelnen Advertisern eine Quelle erstellen. Sie können beispielsweise eine [!UICONTROL RT-CDP] für das Konto, eine [!UICONTROL RT-CDP] für Advertiser 1 und eine [!UICONTROL RT-CDP] für Advertiser 2 haben.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Klicken Sie auf **[!UICONTROL Add Source]**.

1. Wählen Sie im Menü [!UICONTROL Select a Type] Ihre [Kundendatenplattform](source-about.md):

   * *[!UICONTROL RT-CDP]*: Die [!DNL Adobe Real-Time CDP].

   * *[!UICONTROL AdFixus ID]*: Die [!DNL AdFixus] Kundendatenplattform. Gilt nur für Inserenten in Australien.

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
>Nachdem Sie eine Quelle für Ihre Kundendatenplattform erstellt haben, müssen Sie zusätzliche Schritte ausführen, um Ihre Audience zu importieren:
>* Wenden Sie sich für [!DNL ActionIQ] an Ihr Adobe-Account-Team.
>* Informationen zu anderen Quelltypen finden <!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), --> unter [Workflow für [!DNL AdFixus]](source-adfixus.md), the [workflow for [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md), [Workflow für [!DNL Amperity]](source-amperity.md), [Workflow für [!DNL Optimizely]](source-optimizely.md) und [Workflow für [!DNL Tealium]](source-tealium.md).

## Ändern der ID-Typen für eine Zielgruppenquelle

*Verfügbar für alle unterstützten Kundendatenplattformen mit Ausnahme von[!DNL AdFixus]*

<!-- 
Clarify this:

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses that you shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we don't delete any historical IDs of that type from the segments shared through the source.

-->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Halten Sie den Cursor über der Quellzeile und klicken Sie auf **[!UICONTROL Edit]**.

1. Ändern Sie die [IDs, die für die Quelle ausgewählt wurden](#source-settings).

1. Klicken Sie auf **[!UICONTROL Save]**.

## Löschen einer Zielgruppenquelle

Durch das Löschen einer Quelle werden die über die Quelle importierten Segmente entfernt, einschließlich aller übersetzten IDs.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

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

**[!UICONTROL Advertiser]:** (Nur Sichtbarkeit auf Advertiser-Ebene) Der Advertiser, für den die Segmente verfügbar sind. Wählen Sie einen aus der Liste der Advertiser mit Zugriff auf das Konto aus.

**[!UICONTROL Enter IMS Org Id]:** (nur [!DNL Real-Time CDP]) Die Adobe CX Enterprise-Organisations-ID für das [!DNL Adobe Experience Platform].

**[!UICONTROL Convert PII to the following IDs]:** (für alle unterstützten Kundendatenplattformen außer [!DNL AdFixus] verfügbar) Die ID-Typen, in die Sie Ihre personenbezogenen Daten (PII) konvertieren. Wenn Sie mehrere Typen auswählen, wird das generierte Segment mit Werten für jeden ausgewählten ID-Typ gefüllt (z. B. eine [!DNL RampID] und eine [!DNL Unified ID2.0] für jede E-Mail-Adresse). Die Datengebühren werden entsprechend berechnet.

Für [!DNL RampID] und [!DNL Unified ID2.0] sucht der Anbieter nach jeder E-Mail-Adresse, um festzustellen, ob bereits eine ID vorhanden ist, und übersetzt die Adresse in eine entsprechende ID, sofern verfügbar. Wenn für die Adresse keine ID vorhanden ist, wird eine neue ID erstellt.

>[!NOTE]
>
>Sie können nur einen ID-Typ in einer Platzierung auswählen. Um die Leistung nach ID-Typ zu testen[&#x200B; erstellen Sie für &#x200B;](/help/dsp/campaign-management/placements/placement-create.md) ID-Typ im Segment eine separate Platzierung.

* *[!DNL RampID]:* Konvertieren von personenbezogenen Daten in ein [!DNL RampID]. Sie können [!DNL RampIDs] für die Retargeting-Zielgruppenbestimmung der angemeldeten Benutzer und für [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) Messung verwenden.

* *[!DNL Unified ID2.0]:* Konvertieren von personenbezogenen Daten in eine [Unified ID 2.0](https://unifiedid.com)-ID für die erneute Zielgruppenbestimmung der angemeldeten Benutzer.

<!--
 Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** Die Nutzungsbedingungen für die Konvertierung von personenbezogenen Daten in universelle IDs. Sie oder ein anderer Benutzer im DSP-Konto müssen die Bedingungen akzeptieren, bevor Sie IDs importieren, Daten in einen neuen ID-Typ konvertieren oder einen ID-Typ als Ziel festlegen können. Für Kunden mit verwalteten Service-Verträgen erhält Ihr Adobe-Konto-Team Ihr Einverständnis und akzeptiert die Bedingungen im Namen Ihres Unternehmens. Um die Bedingungen zu lesen, klicken Sie auf **>**. Um die Bedingungen zu akzeptieren, scrollen Sie zum Ende der Bedingungen und klicken Sie auf **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Schreibgeschützt; wird automatisch generiert) Der Quellschlüssel, mit dem Sie eine Zielverbindung in der Kundendatenplattform erstellen können, um Zielgruppen an Advertising DSP zu senden. Sie können den Wert in die Zwischenablage kopieren, um ihn in die Zielverbindungseinstellungen oder in eine Datei einzufügen. Geben Sie den Wert für das Team frei, das die Zielgruppen an DSP streamt.

>[!MORELIKETHIS]
>
>* [Über Erstanbieter-Zielgruppenquellen](source-about.md)
>* [Unterstützung für die Aktivierung universeller IDs](/help/dsp/audiences/universal-ids.md)
>* [Konvertieren von Benutzer-IDs  [!DNL Adobe Real-Time CDP]  universelle IDs](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Konvertieren von Benutzer-IDs  [!DNL Amperity]  universelle IDs](/help/dsp/audiences/sources/source-amperity.md)
>* [Konvertieren von Benutzer-IDs  [!DNL Optimizely]  universelle IDs](/help/dsp/audiences/sources/source-optimizely.md)
>* [Konvertieren von Benutzer-IDs  [!DNL Tealium]  universelle IDs](/help/dsp/audiences/sources/source-tealium.md)
>* [Importieren von First-Party-Segmenten aus [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)
>* [Über die Zielgruppenverwaltung](/help/dsp/audiences/audience-about.md)
