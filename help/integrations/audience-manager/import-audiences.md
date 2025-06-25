---
title: Adobe Audience Manager-Segmente für das Anzeigen-Targeting importieren
description: Erfahren Sie, wie Sie Ihre Zielgruppen  [!DNL Adobe]  Advertising DSP importieren und mit Adobe Audience Manager suchen
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Adobe Audience Manager-Segmente für das Anzeigen-Targeting importieren

Advertising DSP und [!DNL Advertising Search, Social, & Commerce] können jeweils Metadaten, Hierarchiedaten und eindeutige Zielgruppendaten für alle [!DNL Adobe] Zielgruppen eines Werbetreibenden oder einer Agentur abrufen<!-- segments or audiences? Standardize terms per AAM's docs --> darunter:

* Adobe Audience Manager-Segmente

* Adobe Analytics-Segmente, die in Adobe Experience Cloud veröffentlicht werden

* Segmente, die mit dem Adobe Experience Cloud-[!DNL Audience Library] erstellt werden

* Segmente, die in Adobe Experience Platform erstellt und über Audience Manager an Adobe Advertising gesendet werden

Um auf [!DNL Adobe] Zielgruppen in DSP oder [!DNL Creative] zuzugreifen, müssen Sie die Zielgruppen in DSP importieren. Um auf [!DNL Adobe] Zielgruppen in [!DNL Search, Social, & Commerce] zuzugreifen, müssen Sie die Zielgruppen in [!DNL Search, Social, & Commerce] importieren.

## Voraussetzungen

* Der Werbetreibende muss [die [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/de/docs/id-service/using/intro/overview) Version 2.0 oder höher implementieren. Die [!DNL Identity Service] bietet eine universelle, beständige ID zum Identifizieren Ihrer Besucher über alle Experience Cloud-Lösungen hinweg.

  Die Implementierung umfasst das Hinzufügen des [!DNL Identity service]-Codes zu jeder Web-Seite auf den Sites des Werbetreibenden.

* Die Organisation muss [für Experience Cloud-Services aktiviert](https://experienceleague.adobe.com/de/docs/core-services/interface/services/overview) und über eine Experience Cloud-[!DNL Organization ID] (früher als [!DNL IMS org ID] bezeichnet) verfügen.

  Mit der [!UICONTROL Organization ID] können Unternehmen mit mehreren Adobe Experience Cloud-Produkten Daten zwischen einigen der Produkte austauschen.

* (Advertiser mit [!DNL Analytics]) Der Advertiser muss [implementieren [!DNL Analytics] mit `appMeasurement.js`](https://experienceleague.adobe.com/de/docs/analytics/implementation/js/overview) Version 1.6.4 oder höher.

* Die Website-Besucher des Werbetreibenden umfassen nicht viele [!DNL Apple Safari].

* (Empfohlen, wenn der Advertiser sowohl Audience Manager als auch [!DNL Analytics] verwendet) Um die Aufrufe an die einzelnen Web-Seiten zu reduzieren, entfernen Sie den vorhandenen Audience Manager-[!DNL Data Integration Library]-Code für die Datenerfassung und aktivieren Sie stattdessen die Server-seitige Weiterleitung für jede [!DNL Analytics] Report Suite. Weitere Informationen finden Sie unter &quot;[Übersicht über die Server-seitige Weiterleitung](https://experienceleague.adobe.com/de/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* (Empfohlen) Senden Sie bei höheren Übereinstimmungsraten nur First-Party-Website-Daten an Adobe Advertising. Wenn der Werbetreibende Daten von Drittanbietern oder Offline-Daten aus einem CRM-System (Customer Relationship Management) bündelt, kann Datenlecks die Übereinstimmungsraten verringern.

## Audience Manager-Zielgruppen in DSP importieren

### Schritte zum Importieren von Zielgruppen in DSP

Die Teams für [!DNL Adobe]-Konto- und Datenoperationen führen die folgenden Schritte aus.

1. Das Adobe-Konto-Team sollte die Einstellung auf Advertiser-Ebene &quot;[!UICONTROL Adobe Analytics Cloud]&quot; konfigurieren.

1. Das Adobe-Konto-Team sollte eine Anfrage an das Datenübertragungs-Team senden, um die Audience Manager-Segmente des Unternehmens mithilfe der nativen Advertising DSP-API-Integration zu importieren.

### Welche Änderungen führen zu Audience Manager?

Die -API automatisch:

* Erstellt zwei DSP-Ziele in Audience Manager:

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* Ordnet die beiden Ziele allen Audience Manager-Segmenten zu, sodass Audience Manager die Segmente mit dem DSP Advertiser-Konto teilen kann, das mit demselben Experience Cloud-[!DNL Organization ID] verknüpft ist, das für Audience Manager verwendet wird.

  Optional kann das Unternehmen nicht benötigte Segmente aus den Zielen in Audience Manager entfernen.

* Fügt das folgende Exchange-Cookie-Synchronisierungs-Pixel zum Audience Manager-Container des Unternehmens hinzu, um die Reichweite von Kundenkampagnen zu verbessern:

   * Adobe AdCloud: 411 (Dieses Pixel wird standardmäßig und automatisch als Teil [!DNL Identity Service] Version 2.0 bereitgestellt. Unternehmen mit [!DNL Identity Service] Versionen unter 2.0 sollten dieses Pixel ihrem Audience Manager-Container hinzufügen.

## Audience Manager-Zielgruppen nach [!DNL Search, Social, & Commerce] importieren

### Schritte zum Importieren von Zielgruppen in [!DNL Search, Social, & Commerce]

[!DNL Adobe] Personal führt die meisten oder alle der folgenden Schritte aus.

1. Das Adobe-Konto-Team sollte eine Anfrage an das Datenverwaltungsteam richten, um eine Integration zwischen [!DNL Search, Social, & Commerce] und Audience Manager einzurichten. Schließen Sie die Namen der Audience Manager-Segmente ein, die Sie nach [!DNL Search, Social, & Commerce] exportieren möchten.

1. Konfigurieren Sie in Audience Manager Ziele für [!DNL Search, Social, & Commerce]:

   1. Erstellen Sie zwei neue Ziele: `[!UICONTROL Adobe Media Optimizer (HTTP)]` und `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] ist ein früherer Name für [!DNL Search, Social, & Commerce].

   1. Geben Sie die Segmente für jedes der Ziele an.

      Mit der Option [!UICONTROL Automatically map all current and future segments] werden alle Segmente täglich zugeordnet und synchronisiert.

      Mit der Option [!UICONTROL Manually map segments] können Sie die Segmente manuell zuordnen, um sie mit dem Batch-Ziel (`[!UICONTROL Adobe Media Optimizer Batch Destination]`) zu synchronisieren. Dem HTTP-Ziel müssen keine Segmente manuell zugeordnet werden.

1. In [!DNL Search, Social, & Commerce] sollte entweder das [!DNL Search, Social, & Commerce] Implementierungs-Team oder ein Benutzer mit der Rolle „Direktzugriff-Client-Manager“ den Import von [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup] initiieren.

   Die Experience Cloud-[!DNL Organization ID] ([!DNL IMS org ID]) des Unternehmens ist erforderlich. Die ID muss mit der ID übereinstimmen, die für das Audience Manager-Konto des Unternehmens verwendet wird.

### Welche Änderungen führen zu Audience Manager?

In Audience Manager werden zwei [!DNL Search, Social, & Commerce] Ziele für das Unternehmen verfügbar:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## Datensynchronisation

Der erste Import dauert etwa 24 Stunden. Nach dem ersten Import werden die Daten in Echtzeit mit einer Verzögerung von ein bis zwei Sekunden synchronisiert.

Daten zur Segmentzugehörigkeit werden erst gesendet, nachdem eines der folgenden Ereignisse eintritt:

* (Werbetreibende mit DSP):

   * Das Segment wird in einer Adobe Advertising-Display-Anzeige angesprochen.

   * Das Segment wird den [!DNL Adobe AdCloud Cross-Channel] Batch- und Echtzeit-Zielen in der Benutzeroberfläche von Audience Manager hinzugefügt.

* (Werbetreibende mit [!DNL Search, Social, & Commerce]):

   * Das Segment wird in einer Adobe Advertising-Suchanzeige angesprochen.

   * Das Segment wird den [!DNL Adobe Media Optimizer] Batch- und HTTP-Zielen in der Benutzeroberfläche von Audience Manager hinzugefügt.

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### So synchronisiert DSP die Daten

DSP synchronisiert die Daten automatisch mithilfe der [!DNL Adobe Experience Cloud Identity (ECID) Service]. Während der Synchronisierung ruft die [!DNL ECID Service] Adobe Advertising unter [!DNL cm.everesttech.net] auf. Da es sich bei Adobe Advertising um eine vertrauenswürdige Domain handelt, erfolgt die ID-Synchronisierung von übergeordneten Seiten aus statt innerhalb der Ziel-Publishing-iFrames, wie bei den meisten Aktivierungspartnern von Drittanbietern. Audience Manager identifiziert eindeutige Benutzer anhand von Geräte-IDs mithilfe der [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/de/docs/audience-manager/user-guide/reference/ids-in-aam), auch als [!DNL Device ID] bezeichnet.

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### So synchronisieren Search, Social und Commerce die Daten

Search, Social und Commerce synchronisieren die Daten automatisch mithilfe der [!DNL Adobe Experience Cloud Identity (ECID) Service]. Bei der Synchronisierung ruft der [!DNL ECID Service] Adobe Advertising unter [!DNL cm.everesttech.net] auf. Dies ist eine vertrauenswürdige Domain, die zu Adobe Advertising gehört. Audience Manager identifiziert eindeutige Benutzer anhand von Geräte-IDs mithilfe der [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/de/docs/audience-manager/user-guide/reference/ids-in-aam), auch als [!DNL Device ID] bezeichnet.

## Wo Sie Ihre synchronisierten Segmente finden

### In DSP

DSP ordnet die Segmentnamen nach der Audience Manager-Taxonomie an und enthält die entsprechende Anzahl der Segmentzugehörigkeiten in:

* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): Auf der Registerkarte &quot;[!UICONTROL Adobe Segments]&quot; im Abschnitt [!UICONTROL Audience Targeting].

* In [Zielgruppeneinstellungen](/help/dsp/audiences/audience-settings.md): auf der Registerkarte [!UICONTROL Adobe Segments].

### In Advertising Creative

In [!DNL Creative] sind die Segmente in den Erlebniseinstellungen für Zielknoten verfügbar.

### in [!DNL Advertising Search, Social, & Commerce]

In [!DNL Search, Social, & Commerce] sind die Segmente verfügbar, wenn Sie eine [!DNL Google] Zielgruppe mithilfe der [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; unter [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library] erstellen.

Für jede [!DNL Google] Zielgruppe, die Sie erstellen, gibt [!DNL Google] die Zielgruppengröße an.

>[!MORELIKETHIS]
>
>* [Adobe Advertising-Integrationen mit Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
