---
title: Importieren von Adobe Audience Manager-Segmenten für Anzeigen-Targeting
description: Erfahren Sie, wie Sie Ihre [!DNL Adobe] Zielgruppen in Advertising DSP importieren und mit Adobe Audience Manager suchen
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: e6635abdb34444bc40d833a3c6a5eaf07f9f1789
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Importieren von Adobe Audience Manager-Segmenten für Anzeigen-Targeting

Advertising DSP und [!DNL Advertising Search, Social, & Commerce] können jeweils Metadaten, Hierarchiedaten und eindeutige Zielgruppendaten für alle [!DNL Adobe] Zielgruppen eines Advertisers oder einer Agentur<!-- segments or audiences? Standardize terms per AAM's docs --> abrufen, einschließlich:

* Adobe Audience Manager-Segmente

* Adobe Analytics-Segmente, die in Adobe Experience Cloud veröffentlicht werden

* Segmente, die mit dem Adobe Experience Cloud [!DNL Audience Library] erstellt wurden

* Segmente, die in Adobe Experience Platform erstellt und über Audience Manager an Adobe Advertising gesendet werden

Um auf [!DNL Adobe] Zielgruppen in DSP oder [!DNL Creative] zuzugreifen, müssen Sie die Zielgruppen in DSP importieren. Um auf [!DNL Adobe] Zielgruppen in [!DNL Search, Social, & Commerce] zuzugreifen, müssen Sie die Zielgruppen in [!DNL Search, Social, & Commerce] importieren.

## Voraussetzungen

* Der Advertiser muss [die  [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview) Version 2.0 oder höher implementieren. Der [!DNL Identity Service] bietet eine universelle, beständige ID, mit der Ihre Besucher lösungsübergreifend in Experience Cloud identifiziert werden.

  Die Implementierung umfasst das Hinzufügen des [!DNL Identity service] -Codes zu jeder Webseite auf den Sites des Advertisers.

* Das Unternehmen muss für Experience Cloud-Services ](https://experienceleague.adobe.com/en/docs/core-services/interface/services/overview) mit [aktiviertem Experience Cloud [!DNL Organization ID] (früher [!DNL IMS org ID]) ausgestattet sein.

  Mit dem [!UICONTROL Organization ID] können Unternehmen mit mehreren Adobe Experience Cloud-Produkten Daten für einige der Produkte freigeben.

* (Advertiser mit [!DNL Analytics]) Der Advertiser muss [2}mit `appMeasurement.js`](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview) Version 1.6.4 oder höher implementieren. [!DNL Analytics] 

* Die Website-Besucher des Advertisers enthalten keine hohen Benutzerzahlen mit [!DNL Apple Safari].

* (Wird empfohlen, wenn der Werbetreibende sowohl Audience Manager als auch [!DNL Analytics] verwendet) Um Aufrufe auf jede Webseite zu reduzieren, entfernen Sie den vorhandenen Audience Manager- [!DNL Data Integration Library]-Code für die Datenerfassung und aktivieren Sie stattdessen die serverseitige Weiterleitung für jede [!DNL Analytics] Report Suite. Weitere Informationen finden Sie unter &quot;[Übersicht über die serverseitige Weiterleitung](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf)&quot;.

* (Empfohlen) Für höhere Übereinstimmungsraten senden Sie nur Erstanbieter-Website-Daten an Adobe Advertising. Wenn der Advertiser Drittanbieterdaten oder Offline-Daten aus einem Customer Relationship Management-System bündelt, kann die Datenleckage die Übereinstimmungsraten reduzieren.

## Importieren von Audience Manager-Zielgruppen in DSP

### Schritte zum Importieren von Zielgruppen in DSP

Die [!DNL Adobe] -Konto- und Datenoperationsteams führen die folgenden Schritte aus.

1. Das Adobe Account Team sollte die Einstellung &quot;[!UICONTROL Adobe Analytics Cloud]&quot; auf Advertiser-Ebene konfigurieren.

1. Das Adobe Account-Team sollte eine Anfrage an das Dateneinsatzteam senden, um die Audience Manager-Segmente des Unternehmens mithilfe der nativen Advertising DSP-API-Integration zu importieren.

### Welche Veränderungen führen zu Audience Manager?

Die API automatisch:

* Erstellt zwei DSP Ziele in Audience Manager:

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* Ordnet die beiden Ziele allen Segmenten des Audience Managers zu, sodass Audience Manager die Segmente für das DSP Advertiser-Konto freigeben können, das mit dem für den Audience Manager verwendeten Experience Cloud [!DNL Organization ID] verknüpft ist.

  Das Unternehmen kann optional nicht benötigte Segmente aus den Zielen in Audience Manager entfernen.

* Fügt das folgende Pixel zur Cookie-Synchronisierung zum Audience Manager-Container des Unternehmens hinzu, um die Reichweite von Kundenkampagnen zu verbessern:

   * Adobe AdCloud: 411 (Dieses Pixel kommt standardmäßig und automatisch als Teil von [!DNL Identity Service] Version 2.0. Organisationen mit [!DNL Identity Service] -Versionen unter 2.0 sollten dieses Pixel ihrem Audience Manager-Container hinzufügen.

## Importieren von Audience Manager-Zielgruppen in [!DNL Search, Social, & Commerce]

### Schritte zum Importieren von Zielgruppen in [!DNL Search, Social, & Commerce]

Die Mitarbeiter von [!DNL Adobe] führen die meisten oder alle der folgenden Schritte aus.

1. Das Adobe Account-Team sollte eine Anfrage an das Dateneinsatzteam senden, um eine Integration zwischen [!DNL Search, Social, & Commerce] und Audience Manager einzurichten. Schließen Sie die Namen der Audience Manager-Segmente ein, die Sie in [!DNL Search, Social, & Commerce] exportieren möchten.

1. Konfigurieren Sie in Audience Manager Ziele für [!DNL Search, Social, & Commerce]:

   1. Erstellen Sie zwei neue Ziele: `[!UICONTROL Adobe Media Optimizer (HTTP)]` und `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] ist ein früherer Name für [!DNL Search, Social, & Commerce].

   1. Geben Sie die Segmente für die einzelnen Ziele an.

      Mit der Option [!UICONTROL Automatically map all current and future segments] werden alle Segmente täglich zugeordnet und synchronisiert.

      Mit der Option [!UICONTROL Manually map segments] können Sie die Segmente manuell zuordnen, um sie mit dem Batch-Ziel zu synchronisieren (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Es müssen keine Segmente manuell dem HTTP-Ziel zugeordnet werden.

1. Innerhalb von [!DNL Search, Social, & Commerce] sollte entweder das Implementierungsteam von [!DNL Search, Social, & Commerce] oder ein Benutzer mit der Rolle &quot;Client-Manager mit direktem Zugriff&quot;den Import von [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup] starten.

   Die Experience Cloud [!DNL Organization ID] ([!DNL IMS org ID]) des Unternehmens ist erforderlich. Die Kennung muss mit der für das Audience Manager-Konto des Unternehmens verwendeten identisch sein.

### Welche Veränderungen führen zu Audience Manager?

Zwei [!DNL Search, Social, & Commerce] -Ziele stehen dem Unternehmen in Audience Manager zur Verfügung:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## Datensynchronisation

Der erste Import dauert etwa 24 Stunden. Nach dem ersten Import werden die Daten in Echtzeit mit einer Verzögerung von einer bis zwei Sekunden synchronisiert.

Segmentzugehörigkeitsdaten werden erst gesendet, nachdem eines der folgenden Ereignisse eintritt:

* (Advertiser mit DSP):

   * Das Segment wird in einer Adobe Advertising-Display-Anzeige als Ziel ausgewählt.

   * Das Segment wird den Batch- und Echtzeitzielen [!DNL Adobe AdCloud Cross-Channel] in der Audience Manager-Benutzeroberfläche hinzugefügt.

* (Advertiser mit [!DNL Search, Social, & Commerce]):

   * Das Segment wird in einer Adobe Advertising-Suchanzeige als Ziel ausgewählt.

   * Das Segment wird den Batch- und HTTP-Zielen für [!DNL Adobe Media Optimizer] in der Audience Manager-Benutzeroberfläche hinzugefügt.

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### DSP Synchronisieren der Daten

DSP synchronisiert die Daten automatisch mit &quot;[!DNL Adobe Experience Cloud Identity (ECID) Service]&quot;. Während der Synchronisierung ruft [!DNL ECID Service] die Adobe Advertising bei [!DNL cm.everesttech.net] auf. Da Adobe Advertising eine vertrauenswürdige Domäne ist, erfolgt die ID-Synchronisierung von übergeordneten Seiten aus statt innerhalb der iFrames für die Zielveröffentlichung, wie dies bei den meisten Aktivierungspartnern von Drittanbietern der Fall ist. Audience Manager identifiziert Unique Users anhand von Geräte-IDs. Dazu wird [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam) verwendet, die auch als [!DNL Device ID] bezeichnet werden.

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### So synchronisieren Search, Social und Commerce die Daten

Die Daten werden in Search, Social und Commerce automatisch mit dem Wert [!DNL Adobe Experience Cloud Identity (ECID) Service] synchronisiert. Während der Synchronisierung ruft [!DNL ECID Service] die Adobe Advertising unter [!DNL cm.everesttech.net] auf, eine vertrauenswürdige Domäne, die zu Adobe Advertising gehört. Audience Manager identifiziert Unique Users anhand von Geräte-IDs. Dazu wird [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam) verwendet, die auch als [!DNL Device ID] bezeichnet werden.

## Suchen nach synchronisierten Segmenten

### In DSP

DSP organisiert die Segmentnamen nach der Audience Manager-Taxonomie und umfasst die entsprechenden Segmentzugehörigkeitszahlen in:

* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): Auf der Registerkarte [!UICONTROL Adobe Segments] des Bereichs [!UICONTROL Audience Targeting].

* In [Zielgruppeneinstellungen](/help/dsp/audiences/audience-settings.md): Auf der Registerkarte [!UICONTROL Adobe Segments] .

### In Advertising Creative

In [!DNL Creative] sind die Segmente in den Erlebniseinstellungen für Zielknoten verfügbar.

### In [!DNL Advertising Search, Social, & Commerce]

In [!DNL Search, Social, & Commerce] sind die Segmente verfügbar, wenn Sie eine [!DNL Google] -Zielgruppe mit dem [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; aus [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library] erstellen.

Für jede von Ihnen erstellte [!DNL Google] Zielgruppe stellt [!DNL Google] die Zielgruppengröße bereit.

>[!MORELIKETHIS]
>
>* [Adobe Advertising-Integrationen mit Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
