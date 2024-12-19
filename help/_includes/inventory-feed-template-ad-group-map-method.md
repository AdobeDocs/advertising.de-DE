---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---
# Text-Anzeigenvorlage - Zuordnungsmethode der Anzeigengruppe

**[!UICONTROL Map Method]:** (Wenn [!UICONTROL Map Only] für Anzeigengruppen aktiviert ist; alle Anzeigennetzwerke außer [!DNL Yandex]) Die Methode, mit der neue Schlüsselwörter und Anzeigen vorhandenen Anzeigengruppen zugeordnet werden:

* *[!UICONTROL Contains Anywhere]:* Fügt Daten zu einer bestehenden Anzeigengruppe hinzu, deren Name die angegebene Zeichenfolge enthält, sofern diese vorhanden ist.

* *[!UICONTROL Contains Exactly]:* Fügt Daten zu einer bestehenden Anzeigengruppe hinzu, deren Name die angegebene Zeichenfolge enthält, sofern diese vorhanden ist.

* *[!UICONTROL Exactly Matches]* (Standard): Fügt Daten zu einer vorhandenen Anzeigengruppe mit demselben Namen hinzu, sofern vorhanden.

Wenn keine Übereinstimmung gefunden wird, werden alle Daten für die Anzeigengruppe ignoriert. Wenn die Anzeigengruppendaten im Feed keine Kampagnendaten enthalten, wird die Anzeigengruppe einer Anzeigengruppe mit demselben Namen in einer beliebigen Kampagne zugeordnet, sofern vorhanden. Wenn mehrere Anzeigengruppenübereinstimmungen gefunden werden, werden die Schlüsselwörter und Anzeigen allen zugeordnet.
