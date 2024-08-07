---
title: Audience Source-Einstellungen
description: Erfahren Sie mehr über die Einstellungen für Zielgruppenquellen.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Audience Source-Einstellungen

*Beta-Funktion*

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
>* [Verwalten von Zielgruppenquellen zum Aktivieren von universellen ID-Zielgruppen](source-manage.md)
>* [Über Erstanbieter-Zielgruppenquellen](source-about.md)
>* [ Manuelles Importieren authentifizierter Segmente aus  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Adobe Advertising DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)
