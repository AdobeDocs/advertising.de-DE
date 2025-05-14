---
title: Duplizieren einer Kampagne
description: Erfahren Sie, wie Sie eine Kampagne duplizieren.
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 860761bf65dd6ea35abbb3b04863d78c6461fe0f
workflow-type: tm+mt
source-wordcount: '377'
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
* Mindestbudgets auf Platzierungsebene
* (Wenn Sie die Flugdaten ändern) Benutzerdefinierte Anzeigenplanung
* (Wenn Sie keine Anzeigen anhängen) Benutzerdefinierte Anzeigengewichtung und -planung
* Standardplatzierungen für programmgesteuert garantierte (PG) Angebote und Platzierungen für [!UICONTROL Simple Ad Serving] Angebote
* (Wenn Sie Platzierungen in eine andere Kampagne kopieren):
   * Geo-Ziele
   * Ereignispixel
   * Anzeigen
   * [!DNL DoubleVerify Authentic Brand Safety] auf Platzierungsebene (die die Segmente auf Advertiser-Ebene überschreiben)

## Best Practices für die Konfiguration der neuen Kampagne

>[!TIP]
>
>* Verwenden Sie Bulksheets, [Änderungen an mehreren Kampagnenkomponenten gleichzeitig vorzunehmen](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Verwenden Sie Anzeigen-Tag[Blätter, um (mehrere Anzeigen von Drittanbietern hochzuladen](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Pausieren Sie die neue Kampagne, bis Sie sie aktivieren können.

* Beachten Sie Folgendes und bearbeiten Sie die neue Kampagne nach Bedarf:

   * Verfügt das Konto über genügend Mittel für das neue Kampagnenbudget?

   * Benötigt die neue Kampagne ein anderes Budget als die vorherige Kampagne?

   * Sind Mindestbudgets für eine der Platzierungen erforderlich?

   * Laden Sie Kreative, einschließlich aller erforderlichen benutzerdefinierten Anzeigengewichtungen und Zeitpläne, hoch und fügen Sie sie den Platzierungen hinzu.

   * Fügen Sie den Platzierungen und Anzeigen nach Bedarf Ereignis-Pixel hinzu.

   * Schließen Sie bei Bedarf geografische Ziele und [!DNL DoubleVerify Authentic Brand Safety] auf Platzierungsebene in Platzierungen ein.

   * Verwenden Sie für programmgesteuerte garantierte Angebote neue Angebots-IDs und erstellen Sie Standardplatzierungen.

   * Erstellen Sie bei Bedarf neue Platzierungen für [!UICONTROL Simple Ad Serving] Angebote.

* Verwenden Sie für Leistungskampagnen (d. h. Kampagnen mit Paketen, die benutzerdefinierte Optimierungsziele verwenden) die [[!UICONTROL Linked Package for Optimization Learnings Carryover] -Einstellung, ](/help/dsp/campaign-management/packages/package-settings.md) jedes Paket die historischen Daten der vorherigen Kampagne als Eingabe für die Optimierung des Pakets verwendet.

>[!MORELIKETHIS]
>
>* [Über die Kampagnenverwaltung](campaign-about.md)
>* [Erstellen einer Kampagne](campaign-create.md)
>* [Bearbeiten einer Kampagne](campaign-edit.md)
>* [Anzeigen des Änderungsprotokolls für eine Kampagne](campaign-change-log.md)
>* [Kampagneneinstellungen](campaign-settings.md)
