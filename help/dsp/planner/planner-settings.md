---
title: Einstellungen für Pläne zur Anbindung an das Fernsehen
description: Siehe Beschreibungen der Einstellungen für vernetzte TV-Reichweitenpläne.
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 8574d76fd322cb1cbc6aaaf316e7ad2f961a9f6c
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Einstellungen für Pläne zur Anbindung an das Fernsehen

| Parameter | Beschreibung | Erforderlich? |
| --- | --- | --- |
| Name | Der Name, unter dem Ihr Plan identifiziert werden soll. | Ja |
| Advertiser | Der spezifische Advertiser im Konto, für das der Plan erstellt wird. | Ja |
| Medientyp | Die Art der Medien, die in den Plan aufgenommen werden sollen.<br><br>Derzeit nur [!UICONTROL Connected TV] ist verfügbar. | Ja |
| Datumsbereich | Beginn und Ende des Plans.<br><br>Das Startdatum darf nicht vor dem aktuellen Datum liegen. Der Datumsbereich darf nicht länger als 90 Tage sein. | Ja |
| Zieltyp | Der Typ des Ziels (z. B. [!UICONTROL Budget]) für den Plan zu berücksichtigen.<br><br>Derzeit nur [!UICONTROL Budget] ist verfügbar. | Ja |
| Zielwert | Der Zielwert für die Prognose. Verwenden Sie für genauere Prognoseergebnisse einen Wert > 5000 USD. | Ja |
| Max. Angebot | Der Höchstbetrag für 1000 Impressionen. Wenn die Variable [!UICONTROL Connected TV] Medientyp ausgewählt ist, geben Sie einen Wert von mindestens 10 USD ein. | Ja |
| Frequenzlimitierung | Die Häufigkeit, mit der einem einzelnen Haushalt Anzeigen bereitgestellt werden sollen.<br><br>Wenn Sie einen Plan implementieren und mehrere Platzierungen erstellen müssen, wenden Sie die Einstellung für die Frequenzbegrenzung auf Paketebene und nicht auf Platzierungsebene an, um eine ordnungsgemäße Bereitstellung sicherzustellen. | Ja |
| Geotargeting | Orte, die als Ziele ein- oder ausgeschlossen werden sollen. | Ja |
| Inventar-Targeting | Inventarquellen, die als Ziele ein- oder ausgeschlossen werden sollen. Wählen Sie mindestens einen Feed oder eine Quelle aus. | Ja |
| Zielgruppen-Targeting | Zielgruppen, die als Ziele ein- oder ausgeschlossen werden sollen. | Nein |
| Anzeigendauer | Die Dauer der Anzeigen, die für den Plan berücksichtigt werden sollen. | Nein |

>[!MORELIKETHIS]
>
>* [Über das DSP Planer-Tool](planner-about.md)
>* [Erstellen eines Anbindungsplans für TV-Geräte](planner-create.md)
>* [Connected TV-Reichweitenplan duplizieren](planner-duplicate.md)
>* [Bearbeiten eines Anbindungs-TV-Reichweitenplans](planner-edit.md)
>* [Connected TV-Reichweitenplan exportieren](planner-export.md)
>* [Vorhersage für einen vernetzten TV-Reichweitenplan regenerieren](planner-forecast.md)
>* [Archivieren eines Anbindungsplans für TV](planner-archive.md)
