---
title: '[!UICONTROL Simple Ad Serving] Abschlusseinstellungen'
description: Erfahren Sie mehr über die verfügbaren Einstellungen für [!UICONTROL Simple Ad Serving].
feature: DSP Simple Ad Serving
exl-id: 20e23182-d3d0-457f-a821-0ad4770a138d
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] Abschlusseinstellungen

## Neue [!UICONTROL Simple Ad Serving]

### [!UICONTROL Select Ad Source]

| Parameter | Beschreibung |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | Der Medientyp für dieses Angebot: *[!UICONTROL Video],* *[!UICONTROL Display],* oder *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | Der Name des Herausgebers, der dieses Inventar verkauft. Suchen Sie nach einem Herausgeber, indem Sie mindestens die ersten beiden Zeichen des Namens eingeben. Um einen Herausgeber hinzuzufügen, der nicht aufgeführt ist, wenden Sie sich an Ihr Adobe-Account-Team. |
| **[!UICONTROL Advertiser]** | Ein einzelner Advertiser im Konto, der auf dieses Angebot zugreifen kann. Wählen Sie auch die Kampagne und (optional) das Paket aus, in dem das Angebot verfügbar ist. |
| **[!UICONTROL Media Quality Assessment?]** | (Einige Benutzer) Ermöglicht die Ausführung der Anzeige auf einer anderen DSP zur Überprüfung durch Dritte. <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | Die einzige Option ist *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | (Nur neue Angebote) Ob:<ul><li>*[!UICONTROL Create New]:* Um eine Anzeige für diesen Deal zu erstellen.</li><li>*[!UICONTROL Select Ads]:* Um eine vorhandene Anzeige für dieses Angebot zu verwenden.</li></ul> |
| **[!UICONTROL Ad Type]** | Der Anzeigentyp für diesen Deal. Wenn Sie Anzeigen für das Angebot erstellen möchten, geben Sie die Anzeigengröße oder -dauer wie angefordert an. Die verfügbaren Optionen variieren je nach Medientyp. |

{style="table-layout:auto"}

### [!UICONTROL Select Ad(s)]

(Wenn Sie vorhandene Anzeigen verwenden) Die Anzeigen, die in das Angebot aufgenommen werden sollen. Aktivieren Sie das Kontrollkästchen neben jeder einzuschließenden Anzeige.

### [!UICONTROL Select & Upload [Media Type]]

(Nur neue Anzeigen) Screens zum Erstellen einer neuen [Drittanbieteranzeige](/help/dsp/campaign-management/ads/ad-create-multiple.md).

### [!UICONTROL Feed Details]

| Parameter | Beschreibung |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | Die Kosten pro 1000 Impressionen (CPM), wie sie auf der Tarifkarte für Ihren Vertrag angegeben sind. Wenden Sie sich für diesen Wert an Ihr Adobe-Account-Team. <br><br>Geben Sie auch die Währung für den Abschluss an. Alle Benutzer können entweder USD oder, falls das SSP zusätzliche Währungen unterstützt, die Währung für das DSP-Konto auswählen. |
| **[!UICONTROL Third Party Billed Fees]** | (Optional) Eine statische Drittanbietergebühr, die als nicht fakturierbare Kosten erfasst werden soll, und die Währung für den Abschluss.<br><br>Alle Benutzer können USD oder, falls das SSP zusätzliche Währungen unterstützt, die Währung für das DSP-Konto auswählen. **HINWEIS** Fakturierbare Gebühren werden in der [!UICONTROL Net CPM] Metrik angezeigt. |
| **[!UICONTROL Third Party Fee Description]** | (Optional) Eine Beschreibung der Gebühren für Dritte. |
| **[!UICONTROL Flight Dates]** | Das Start- und Enddatum für Traffic, der dieses Angebot verwendet. Die Flugdaten müssen in den Kampagnenflugdaten enthalten sein. Die Anzeigen-Tags geben eine Antwort nur während des angegebenen Flugs zurück.<br><br> Best Practice ist es, eine separate einfache Anzeigenbereitstellungskampagne mit einer einjährigen Dauer zu erstellen und darin Tracking-Pixel zu erstellen. |
| **[!UICONTROL Impressions]** | (Optional) Die geschätzte Anzahl der Impressionen, die Sie mit diesem Angebot ausführen möchten. Dieser Wert wird nur zu Tracking-Zwecken verwendet und um anzugeben, wann die Versandziele erreicht werden. Der Publisher steuert den tatsächlichen Anzeigenversand. Es empfiehlt sich, eine hohe Anzahl von Impressions einzugeben, um das Tag in DSP aktiv zu halten, damit es bei Bedarf erneuert oder erweitert werden kann. |
| **[!UICONTROL Deal Name]** | Der Angebotsname. Geben Sie einen Namen ein oder wählen Sie *[!UICONTROL Auto Generate Deal Name]* aus, damit DSP einen Namen basierend auf den Abschlussdetails generieren kann.<br><br>Beispiel für einen automatisch generierten Namen: `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | (Schreibgeschützt) Die Anzeigen, die Teil des Angebots sind. Um eine Anzeige zu bearbeiten, klicken Sie auf den Anzeigenamen. Um eine Anzeige aus dem Angebot zu entfernen, klicken Sie auf **[!UICONTROL X]** neben dem Anzeigenamen. |

{style="table-layout:auto"}

<!-- 
## Existing Simple Ad Serving Deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [Über [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [Erstellen eines [!UICONTROL Simple Ad Serving] Angebots](simple-deal-create.md)
>* [Bearbeiten [!UICONTROL Simple Ad Serving] Angebotseinstellungen](simple-deal-edit.md)
>* [Detailbericht für einen Abschluss anzeigen](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
