---
title: Importieren von Adobe Audience Manager-Segmenten für Anzeigen-Targeting
description: Erfahren Sie, wie Sie Ihre [!DNL Adobe] Zielgruppen in Advertising DSP und Suche mit Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: e6635abdb34444bc40d833a3c6a5eaf07f9f1789
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Importieren von Adobe Audience Manager-Segmenten für Anzeigen-Targeting

Advertising DSP und [!DNL Advertising Search, Social, & Commerce] kann jedes Mal Metadaten, Hierarchiedaten und eindeutige Zielgruppendaten für alle Daten eines Advertisers oder einer Agentur abrufen [!DNL Adobe] Zielgruppen<!-- segments or audiences? Standardize terms per AAM's docs -->, einschließlich:

* Adobe Audience Manager-Segmente

* Adobe Analytics-Segmente, die in Adobe Experience Cloud veröffentlicht werden

* Segmente, die mit der Adobe Experience Cloud erstellt wurden [!DNL Audience Library]

* Segmente, die in Adobe Experience Platform erstellt und über Audience Manager an Adobe Advertising gesendet werden

Zugriff [!DNL Adobe] Zielgruppen in DSP oder [!DNL Creative], müssen Sie die Zielgruppen in DSP importieren. Zugriff [!DNL Adobe] Zielgruppen in [!DNL Search, Social, & Commerce], müssen Sie die Zielgruppen in [!DNL Search, Social, & Commerce].

## Voraussetzungen

* Der Werbetreibende muss [die [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview) Version 2.0 oder höher. Die [!DNL Identity Service] bietet eine universelle, beständige ID, mit der Ihre Besucher lösungsübergreifend in Experience Cloud identifiziert werden.

  Die Implementierung umfasst das Hinzufügen der [!DNL Identity service] Code für jede Webseite auf den Websites des Werbetreibenden.

* Die Organisation muss [aktiviert für Experience Cloud-Dienste](https://experienceleague.adobe.com/en/docs/core-services/interface/services/overview) und über eine Experience Cloud verfügen [!DNL Organization ID] (zuvor [!DNL IMS org ID]).

  Die [!UICONTROL Organization ID] ermöglicht Unternehmen mit mehreren Adobe Experience Cloud-Produkten die gemeinsame Nutzung von Daten für einige der Produkte.

* (Werbetreibende mit [!DNL Analytics]) Der Advertiser muss [implementieren [!DNL Analytics] using `appMeasurement.js`](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview) Version 1.6.4 oder höher.

* Die Website-Besucher des Advertisers enthalten keine große Menge an [!DNL Apple Safari] Benutzer.

* (Wird empfohlen, wenn der Advertiser sowohl Audience Manager als auch [!DNL Analytics]) Um die Aufrufe auf jeder Webseite zu reduzieren, entfernen Sie vorhandenen Audience Manager [!DNL Data Integration Library] Code für die Datenerfassung und Aktivierung der serverseitigen Weiterleitung für jede [!DNL Analytics] Report Suite . Weitere Informationen finden Sie unter &quot;[Übersicht über die serverseitige Weiterleitung](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* (Empfohlen) Für höhere Übereinstimmungsraten senden Sie nur Erstanbieter-Website-Daten an Adobe Advertising. Wenn der Advertiser Drittanbieterdaten oder Offline-Daten aus einem Customer Relationship Management-System bündelt, kann die Datenleckage die Übereinstimmungsraten reduzieren.

## Importieren von Audience Manager-Zielgruppen in DSP

### Schritte zum Importieren von Zielgruppen in DSP

Die [!DNL Adobe] Teams für Konto- und Datenoperationen führen die folgenden Schritte aus.

1. Das Adobe Account Team sollte die Einstellung auf Advertiser-Ebene konfigurieren &quot;[!UICONTROL Adobe Analytics Cloud].&quot;

1. Das Adobe Account-Team sollte eine Anfrage an das Dateneinsatzteam senden, um die Audience Manager-Segmente des Unternehmens mithilfe der nativen Advertising DSP-API-Integration zu importieren.

### Welche Veränderungen führen zu Audience Manager?

Die API automatisch:

* Erstellt zwei DSP Ziele in Audience Manager:

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* Ordnet die beiden Ziele allen Audience Manager-Segmenten zu, sodass Audience Manager die Segmente für das DSP Advertiser-Konto freigeben können, das mit demselben Experience Cloud verknüpft ist [!DNL Organization ID] verwendet für Audience Manager.

  Das Unternehmen kann optional nicht benötigte Segmente aus den Zielen in Audience Manager entfernen.

* Fügt das folgende Pixel zur Cookie-Synchronisierung zum Audience Manager-Container des Unternehmens hinzu, um die Reichweite von Kundenkampagnen zu verbessern:

   * Adobe AdCloud: 411 (Dieses Pixel kommt standardmäßig und automatisch als Teil von [!DNL Identity Service] Version 2.0. Organisationen mit [!DNL Identity Service] -Versionen unter 2.0 sollten dieses Pixel ihrem Audience Manager-Container hinzufügen.

## Importieren von Audience Manager-Zielgruppen in [!DNL Search, Social, & Commerce]

### Schritte zum Importieren von Zielgruppen in [!DNL Search, Social, & Commerce]

[!DNL Adobe] Personal führt die meisten oder alle der folgenden Schritte aus.

1. Das Adobe Account-Team sollte eine Anfrage an das Dateneinsatzteam senden, um eine Integration zwischen [!DNL Search, Social, & Commerce] und Audience Manager. Beziehen Sie die Namen der Audience Manager-Segmente ein, in die Sie exportieren möchten [!DNL Search, Social, & Commerce].

1. Konfigurieren Sie in Audience Manager Ziele für [!DNL Search, Social, & Commerce]:

   1. Erstellen Sie zwei neue Ziele: `[!UICONTROL Adobe Media Optimizer (HTTP)]` und `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] ist der frühere Name für [!DNL Search, Social, & Commerce].

   1. Geben Sie die Segmente für die einzelnen Ziele an.

      Mit dem [!UICONTROL Automatically map all current and future segments] festgelegt ist, werden alle Segmente täglich zugeordnet und synchronisiert.

      Die [!UICONTROL Manually map segments] -Option können Sie die Segmente manuell der Synchronisierung mit dem Batch-Ziel zuordnen (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Es müssen keine Segmente manuell dem HTTP-Ziel zugeordnet werden.

1. Within [!DNL Search, Social, & Commerce], entweder [!DNL Search, Social, & Commerce] Implementierungs-Team oder ein Benutzer mit der Rolle &quot;Client-Manager mit direktem Zugriff&quot;sollte den Import von [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Experience Cloud der Organisation [!DNL Organization ID] ([!DNL IMS org ID]) ist erforderlich. Die Kennung muss mit der für das Audience Manager-Konto des Unternehmens verwendeten identisch sein.

### Welche Veränderungen führen zu Audience Manager?

Zwei [!DNL Search, Social, & Commerce] Ziele stehen der Organisation in Audience Manager zur Verfügung:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## Datensynchronisation

Der erste Import dauert etwa 24 Stunden. Nach dem ersten Import werden die Daten in Echtzeit mit einer Verzögerung von einer bis zwei Sekunden synchronisiert.

Segmentzugehörigkeitsdaten werden erst gesendet, nachdem eines der folgenden Ereignisse eintritt:

* (Advertiser mit DSP):

   * Das Segment wird in einer Adobe Advertising-Display-Anzeige als Ziel ausgewählt.

   * Das Segment wird zum [!DNL Adobe AdCloud Cross-Channel] Batch- und Echtzeit-Ziele in der Audience Manager-Benutzeroberfläche.

* (Werbetreibende mit [!DNL Search, Social, & Commerce]):

   * Das Segment wird in einer Adobe Advertising-Suchanzeige als Ziel ausgewählt.

   * Das Segment wird zum [!DNL Adobe Media Optimizer] Batch- und HTTP-Ziele in der Audience Manager-Benutzeroberfläche.

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### DSP Synchronisieren der Daten

DSP synchronisiert die Daten automatisch mit der [!DNL Adobe Experience Cloud Identity (ECID) Service]. Während der Synchronisierung wird die Variable [!DNL ECID Service] ruft Adobe Advertising auf unter [!DNL cm.everesttech.net]. Da Adobe Advertising eine vertrauenswürdige Domäne ist, erfolgt die ID-Synchronisierung von übergeordneten Seiten aus statt innerhalb der iFrames für die Zielveröffentlichung, wie dies bei den meisten Aktivierungspartnern von Drittanbietern der Fall ist. Audience Manager identifiziert Unique Users anhand von Geräte-IDs mithilfe der [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), auch als [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### So synchronisieren Search, Social und Commerce die Daten

Suchen, Social und Commerce synchronisieren die Daten automatisch mit der [!DNL Adobe Experience Cloud Identity (ECID) Service]. Während der Synchronisierung wird die Variable [!DNL ECID Service] ruft Adobe Advertising auf unter [!DNL cm.everesttech.net], eine vertrauenswürdige Domäne, die zu Adobe Advertising gehört. Audience Manager identifiziert Unique Users anhand von Geräte-IDs mithilfe der [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), auch als [!DNL Device ID].

## Suchen nach synchronisierten Segmenten

### In DSP

DSP organisiert die Segmentnamen nach der Audience Manager-Taxonomie und umfasst die entsprechenden Segmentzugehörigkeitszahlen in:

* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): Im [!UICONTROL Adobe Segments] des [!UICONTROL Audience Targeting] Abschnitt.

* In [Zielgruppeneinstellungen](/help/dsp/audiences/audience-settings.md): Im [!UICONTROL Adobe Segments] Registerkarte.

### In Advertising Creative

In [!DNL Creative], sind die Segmente in den Erlebniseinstellungen für Zielknoten verfügbar.

### In [!DNL Advertising Search, Social, & Commerce]

In [!DNL Search, Social, & Commerce], sind die Segmente verfügbar, wenn Sie eine [!DNL Google] Zielgruppe, die [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; von [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Für jeden [!DNL Google] von Ihnen erstellte Zielgruppen, [!DNL Google] stellt die Zielgruppengröße bereit.

>[!MORELIKETHIS]
>
>* [Adobe Advertising-Integrationen mit Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
