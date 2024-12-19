---
title: Duplizieren einer Kampagne
description: Erfahren Sie, wie Sie eine Kampagne duplizieren.
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 4085c1b21c0fe84653978e449321868921841367
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Duplizieren einer Kampagne

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplizieren Sie eine Kampagne, um eine neue Kampagne mit ähnlichen Einstellungen zu erstellen. Sie können:

* Duplizieren Sie die Kampagne für den ursprünglichen Advertiser oder für einen anderen
* Optional können Sie die ursprünglichen Pakete und Platzierungen duplizieren
* Ändern der Flugdaten der neuen Kampagne

Unter [Was nicht dupliziert ist](#campaign-not-duplicated) finden Sie eine Liste der Platzierungseinstellungen, die nicht dupliziert werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie neben dem Kampagnennamen auf **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Geben Sie die neuen Kampagneneinstellungen an:

   1. Geben Sie den neuen Kampagnennamen und das Endflugdatum ein.

   1. (Optional) Ändern Sie die Standardeinstellungen.

      Standardmäßig ist die neue Kampagne dem ursprünglichen Werbetreibenden zugewiesen, hat einen Flugplan, der am aktuellen Tag beginnt und die ursprünglichen Pakete und Platzierungen enthält.

1. Klicken Sie auf **[!UICONTROL Submit]**.

## Was nicht dupliziert wird {#campaign-not-duplicated}

Alle Einstellungen aus den ursprünglichen Platzierungen werden dupliziert, mit Ausnahme von:

* Experimenteinstellungen
* (Wenn Sie die Flugdaten ändern) Benutzerdefinierte Anzeigenplanung
* (Wenn Sie keine Anzeigen anhängen) Benutzerdefinierte Anzeigengewichtung und -planung
* Standardplatzierungen für programmgesteuert garantierte (PG) Angebote und Platzierungen für [!UICONTROL Simple Ad Serving] Angebote
* (Wenn Sie Platzierungen in eine andere Kampagne kopieren):
   * Geo-Ziele
   * Ereignispixel
   * Anzeigen
   * [!DNL DoubleVerify Authentic Brand Safety] auf Platzierungsebene (die die Segmente auf Advertiser-Ebene überschreiben)

>[!MORELIKETHIS]
>
>* [Über Campaign Management](campaign-about.md)
>* [Erstellen einer Kampagne](campaign-create.md)
>* [Bearbeiten einer Kampagne](campaign-edit.md)
>* [Anzeigen des Änderungsprotokolls für eine Kampagne](campaign-change-log.md)
>* [Kampagneneinstellungen](campaign-settings.md)
