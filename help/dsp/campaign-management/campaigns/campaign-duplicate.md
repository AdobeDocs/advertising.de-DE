---
title: Eine Kampagne duplizieren
description: Erfahren Sie, wie Sie eine Kampagne duplizieren.
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# Eine Kampagne duplizieren

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplizieren Sie eine Kampagne, um eine neue Kampagne mit ähnlichen Einstellungen zu erstellen. Sie können:

* Duplizieren Sie die Kampagne für den ursprünglichen Advertiser oder für einen anderen
* Optional Duplizieren Sie die Originalpakete und -platzierungen
* Ändern der Flugdaten der neuen Kampagne

Siehe[Nicht duplizierte Elemente](#campaign-not-duplicated)&quot; für eine Liste der Platzierungseinstellungen, die nicht dupliziert werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie neben dem Kampagnennamen auf **... >[!UICONTROL Duplicate]**.

1. Geben Sie die neuen Kampagneneinstellungen an:

   1. Geben Sie den neuen Kampagnennamen und das Endflugdatum ein.

   1. (Optional) Ändern Sie die Standardeinstellungen.

      Standardmäßig wird die neue Kampagne dem ursprünglichen Advertiser zugewiesen, hat einen Flugplan, der am aktuellen Tag beginnt, und enthält die ursprünglichen Pakete und Platzierungen.

1. Klicken **[!UICONTROL Submit]**.

## Nicht duplizierte Elemente {#campaign-not-duplicated}

Alle Einstellungen der ursprünglichen Platzierungen werden dupliziert, mit Ausnahme:

* Experimenteinstellungen
* (Wenn Sie die Flugdaten ändern) Benutzerdefinierte Anzeigenplanung
* (Wenn Sie keine Anzeigen anhängen) Benutzerdefinierte Anzeigengewichtung und -planung
* Standardplatzierungen für programmatisch garantierte (PG) Angebote und Platzierungen für [!UICONTROL Simple Ad Serving] Angebote
* (Wenn Sie Platzierungen in eine andere Kampagne kopieren):
   * Geo-Ziele
   * Ereignispixel
   * Anzeigen
   * Platzierungsebene [!DNL DoubleVerify Authentic Brand Safety] Segmente (die die Segmente auf Advertiser-Ebene überschreiben)

>[!MORELIKETHIS]
>
>* [Über Campaign Management](campaign-about.md)
>* [Erstellen einer Kampagne](campaign-create.md)
>* [Eine Kampagne bearbeiten](campaign-edit.md)
>* [Kampagneneinstellungen](campaign-settings.md)

