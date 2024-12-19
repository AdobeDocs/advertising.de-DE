---
title: Einstellungen für Connected TV Reach-Pläne
description: Siehe Beschreibungen der Einstellungen für vernetzte TV-Reichweitenpläne.
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 5d8d981f08eaea2b0a0bc553ab06bd47f1e88ac9
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Einstellungen für Connected TV Reach-Pläne

<!-- Move out of table for consistency at some point. -->

| Parameter | Beschreibung | Erforderlich? |
| --- | --- | --- |
| [!UICONTROL Name] | Der Name zur Identifizierung Ihres Plans. | Ja |
| [!UICONTROL Advertiser] | Der spezifische Advertiser in dem Konto, für das der Plan erstellt wird. | Ja |
| [!UICONTROL Media Type] | Der Medientyp, der in den Plan aufgenommen werden soll.<br><br>Derzeit ist nur [!UICONTROL Connected TV] verfügbar. | Ja |
| [!UICONTROL Date Range] | Das Start- und Enddatum für den Plan.<br><br>Das Startdatum darf nicht vor dem aktuellen Datum liegen. Der Datumsbereich darf nicht länger als 90 Tage sein. | Ja |
| [!UICONTROL Goal Type] | Die Art des Ziels (z. B. [!UICONTROL Budget]), die für den Plan berücksichtigt werden soll.<br><br>Derzeit ist nur [!UICONTROL Budget] verfügbar. | Ja |
| [!UICONTROL Goal Value] | Der Zielwert für die Prognose. Für genauere Prognoseergebnisse verwenden Sie einen Wert > 5000 USD. | Ja |
| [!UICONTROL Max Bid] | Der maximale Betrag, der für 1000 Impressionen zu zahlen ist. Wenn der [!UICONTROL Connected TV] Medientyp ausgewählt ist, geben Sie einen Wert von mindestens 10 USD ein. | Ja |
| [!UICONTROL Frequency Cap] | Die Häufigkeit, mit der einem bestimmten Haushalt Anzeigen bereitgestellt werden sollen.<br><br>Wenn Sie einen Plan implementieren und mehrere Platzierungen erstellen müssen, wenden Sie die Einstellung für die Häufigkeitsbegrenzung auf Paketebene an, nicht auf der Platzierungsebene, um eine ordnungsgemäße Bereitstellung sicherzustellen. | Ja |
| [!UICONTROL Geo-Targeting] | Ein- oder Ausschlussorte als Zielgruppen. Zu den Optionen gehören:<ul><li>Länder, Städte, Bundesstaaten: Klicken Sie auf die Registerkarte **[!UICONTROL Country/State/City]**. Wählen Sie aus, ob das Gebiet ein *Land*, *Bundesland* oder *Stadt* ist. Erweitern Sie optional einen Speicherort, um dessen Unterkomponenten anzuzeigen, und klicken Sie dann auf **[!UICONTROL Include]** oder **[!UICONTROL Exclude]** neben dem Speicherort.</li><li>Ausgewiesene Marktgebiete (DMAs) in den Vereinigten Staaten: Klicken Sie auf die Registerkarte &quot;**[!UICONTROL DMA]**&quot;. Erweitern Sie optional einen beliebigen Status, um die DMAs anzuzeigen, und klicken Sie dann neben dem Speicherort auf **[!UICONTROL Include]** oder **[!UICONTROL Exclude]**.</li><li>Postleitzahlen: Sie haben folgende Möglichkeiten:<ul><li>Klicken Sie auf die Registerkarte **[!UICONTROL Search postal code]**, wählen Sie das Land aus, geben Sie den vollständigen Stadtnamen oder die darin enthaltenen Buchstaben ein und drücken Sie dann die **[Eingabetaste]**, klicken Sie auf den richtigen Stadtnamen, um alle Postleitzahlen für die Stadt anzuzeigen, klicken Sie auf die richtige Postleitzahl und klicken Sie dann auf **[!UICONTROL Include]** oder **[!UICONTROL Exclude]**.</li><li>Klicken Sie auf die Registerkarte **[!UICONTROL Paste postal code]**, wählen Sie das Land aus, geben Sie durch Komma getrennte Werte ein oder fügen Sie sie ein und klicken Sie dann auf **[!UICONTROL Include All]** oder **[!UICONTROL Exclude All]**.</li></ul></li></ul> | Ja |
| [!UICONTROL Inventory Targeting] | Inventarquellen, die als Ziele ein- oder ausgeschlossen werden sollen. Wählen Sie mindestens einen Feed oder eine Quelle aus. | Ja |
| [!UICONTROL Site/App Targeting] | Websites und Apps, die als Ziele ein- oder ausgeschlossen werden sollen. Geben Sie eine URL pro Zeile ein, und klicken Sie dann auf **[!UICONTROL Include All]** oder **[!UICONTROL Exclude All]**. | Nein |
| [!UICONTROL Audience Targeting] | Zielgruppen, die als Ziele ein- oder ausgeschlossen werden sollen. | Nein |
| [!UICONTROL Ad duration] | Die Dauer der für den Plan zu berücksichtigenden Anzeigen. | Nein |

>[!MORELIKETHIS]
>
>* [Über das DSP-Planer-Tool](planner-about.md)
>* [Erstellen eines Plans für die Reichweite von vernetzten Fernsehgeräten](planner-create.md)
>* [Duplizieren Sie einen Plan für die Reichweite eines verbundenen Fernsehers](planner-duplicate.md)
>* [Bearbeiten eines Connected TV-Reach-Plans](planner-edit.md)
>* [Exportieren eines Connected TV Reach Plans](planner-export.md)
>* [Regenerieren Sie die Prognose für einen Connected TV Reach Plan](planner-forecast.md)
>* [Archivieren eines Connected TV Reach Plans](planner-archive.md)
