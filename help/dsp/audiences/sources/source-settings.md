---
title: Einstellungen für Audience Source
description: Erfahren Sie mehr über die Einstellungen für Zielgruppenquellen.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Einstellungen für Audience Source

*Beta-Funktion*

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
>* [Verwalten von Zielgruppenquellen zum Aktivieren universeller ID-Zielgruppen](source-manage.md)
>* [Über Erstanbieter-Zielgruppenquellen](source-about.md)
>* [Importieren Sie authentifizierte Segmente manuell aus [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Adobe Advertising DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=de)
>* [Über die Zielgruppenverwaltung](/help/dsp/audiences/audience-about.md)
