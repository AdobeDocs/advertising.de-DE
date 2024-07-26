---
title: Einstellungen für Pläne zur Anbindung an das Fernsehen
description: Siehe Beschreibungen der Einstellungen für vernetzte TV-Reichweitenpläne.
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 84cf49c9e366938479e9fea2ede55925f1cb3e51
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Einstellungen für Pläne zur Anbindung an das Fernsehen

| Parameter | Beschreibung | Erforderlich? |
| --- | --- | --- |
| [!UICONTROL Name] | Der Name, unter dem Ihr Plan identifiziert werden soll. | Ja |
| [!UICONTROL Advertiser] | Der spezifische Advertiser im Konto, für das der Plan erstellt wird. | Ja |
| [!UICONTROL Media Type] | Die Art der Medien, die in den Plan aufgenommen werden sollen.<br><br>Derzeit ist nur [!UICONTROL Connected TV] verfügbar. | Ja |
| [!UICONTROL Date Range] | Beginn und Ende des Plans.<br><br>Das Startdatum darf nicht vor dem aktuellen Datum liegen. Der Datumsbereich darf nicht länger als 90 Tage sein. | Ja |
| [!UICONTROL Goal Type] | Der Typ des Ziels (z. B. [!UICONTROL Budget]), das für den Plan berücksichtigt werden soll.<br><br>Derzeit ist nur [!UICONTROL Budget] verfügbar. | Ja |
| [!UICONTROL Goal Value] | Der Zielwert für die Prognose. Verwenden Sie für genauere Prognoseergebnisse einen Wert > 5000 USD. | Ja |
| [!UICONTROL Max Bid] | Der Höchstbetrag für 1000 Impressionen. Wenn der Medientyp [!UICONTROL Connected TV] ausgewählt ist, geben Sie einen Wert von mindestens 10 USD ein. | Ja |
| [!UICONTROL Frequency Cap] | Die Häufigkeit, mit der einem einzelnen Haushalt Anzeigen bereitgestellt werden sollen.<br><br>Wenn Sie einen Plan implementieren und mehrere Platzierungen erstellen müssen, wenden Sie die Einstellung für die Frequenzbegrenzung auf Paketebene und nicht auf Platzierungsebene an, um eine ordnungsgemäße Bereitstellung sicherzustellen. | Ja |
| [!UICONTROL Geo-Targeting] | Orte, die als Ziele ein- oder ausgeschlossen werden sollen. Zu den Optionen gehören:<ul><li>Länder, Städte, Bundesstaaten: Klicken Sie auf die Registerkarte &quot;**[!UICONTROL Country/State/City]**&quot;. Wählen Sie aus, ob es sich um ein Gebiet mit dem Status &quot;*Land*&quot;, &quot;*Bundesland*&quot;oder &quot;*Stadt*&quot; handelt. Erweitern Sie optional einen beliebigen Standort, um dessen Unterkomponenten anzuzeigen, und klicken Sie dann auf &quot;**[!UICONTROL Include]**&quot;oder &quot;**[!UICONTROL Exclude]**&quot;neben dem Standort.</li><li>Designierte Marktbereiche (DMAs) in den USA: Klicken Sie auf die Registerkarte &quot;**[!UICONTROL DMA]**&quot;. Erweitern Sie optional einen beliebigen Status, um dessen DMAs anzuzeigen, und klicken Sie dann neben dem Standort auf &quot;**[!UICONTROL Include]**&quot; oder &quot;**[!UICONTROL Exclude]**&quot;.</li><li>Postleitzahlen: Sie können:<ul><li>Klicken Sie auf die Registerkarte &quot;**[!UICONTROL Search postal code]**&quot;, wählen Sie das Land aus, geben Sie den vollständigen Namen des Ortes ein und drücken Sie die Taste &quot;**[Enter]**&quot;, klicken Sie auf den richtigen Stadtnamen, um alle Postleitzahlen für die Stadt anzuzeigen, klicken Sie auf die richtige Postleitzahl und klicken Sie dann auf &quot;**[!UICONTROL Include]**&quot;oder &quot;**[!UICONTROL Exclude]**&quot;.</li><li>Klicken Sie auf die Registerkarte &quot;**[!UICONTROL Paste postal code]**&quot;, wählen Sie das Land aus, geben Sie kommagetrennte Werte ein oder fügen Sie sie ein und klicken Sie auf &quot;**[!UICONTROL Include All]**&quot; oder &quot;**[!UICONTROL Exclude All]**&quot;.</li></ul></li></ul> | Ja |
| [!UICONTROL Inventory Targeting] | Inventarquellen, die als Ziele ein- oder ausgeschlossen werden sollen. Wählen Sie mindestens einen Feed oder eine Quelle aus. | Ja |
| [!UICONTROL Site/App Targeting] | Websites und Apps, die als Ziele ein- oder ausgeschlossen werden. Geben Sie eine URL pro Zeile ein und klicken Sie dann auf **[!UICONTROL Include All]** oder **[!UICONTROL Exclude All]**. | Nein |
| [!UICONTROL Audience Targeting] | Zielgruppen, die als Ziele ein- oder ausgeschlossen werden sollen. | Nein |
| [!UICONTROL Ad duration] | Die Dauer der Anzeigen, die für den Plan berücksichtigt werden sollen. | Nein |

>[!MORELIKETHIS]
>
>* [Über das DSP Planer-Tool](planner-about.md)
>* [Erstellen eines Anbindungs-TV-Reichweitenplans](planner-create.md)
>* [Duplizieren eines Anbindungs-TV-Reichweitenplans](planner-duplicate.md)
>* [Bearbeiten eines Anbindungs-TV-Reichweitenplans](planner-edit.md)
>* [Einen Plan für die Anbindung an den Fernsehempfang exportieren](planner-export.md)
>* [Vorhersage für einen vernetzten TV-Reichweitenplan regenerieren](planner-forecast.md)
>* [Archivieren eines Anbindungs-TV-Reichweiten-Plans](planner-archive.md)
