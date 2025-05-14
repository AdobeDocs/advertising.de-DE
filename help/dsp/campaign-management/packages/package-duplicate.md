---
title: Duplizieren eines Pakets
description: Erfahren Sie, wie Sie ein Paket duplizieren.
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 860761bf65dd6ea35abbb3b04863d78c6461fe0f
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Duplizieren eines Pakets

Duplizieren Sie ein Paket, um ein Paket mit ähnlichen Einstellungen zu erstellen. Sie können:

* Duplizieren Sie das Paket innerhalb des ursprünglichen Werbetreibenden und der ursprünglichen Kampagne oder innerhalb anderer

* Optional können Sie die Platzierungen innerhalb des Pakets duplizieren

* (Für duplizierte Pakete innerhalb der ursprünglichen Kampagnen) Duplizieren Sie optional die Original-Anzeigen und Ereignispixel auf Platzierungsebene

* Ändern der Flugdaten des neuen Pakets

Unter [Was nicht dupliziert ist](#package-not-duplicated) finden Sie eine Liste der Platzierungseinstellungen, die nicht dupliziert werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne, um die [!UICONTROL Packages] zu öffnen.

1. Klicken Sie neben dem Paketnamen auf **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Geben Sie die neuen Paketeinstellungen an:

   1. Geben Sie den neuen Paketnamen ein.

   1. (Optional) Ändern Sie die Standardeinstellungen.

      Standardmäßig:

      * Das neue Paket wird dem ursprünglichen Advertiser und der ursprünglichen Kampagne zugewiesen.

      * Das neue Paket ist ab dem aktuellen Tag aktiv.<!-- and the flight continues for NN  days. -->

      * Platzierungen innerhalb des ursprünglichen Pakets werden in das neue Paket kopiert.

      * Die Ereignispixel auf Anzeigen- und Platzierungsebene werden nicht in das neue Paket kopiert.

1. Klicken Sie auf **[!UICONTROL Submit]**.

## Was nicht dupliziert wird {#package-not-duplicated}

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

## Best Practices für die Konfiguration des neuen Pakets

>[!TIP]
>
>* Verwenden Sie Bulksheets, [Änderungen an mehreren Kampagnenkomponenten gleichzeitig vorzunehmen](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Verwenden Sie Anzeigen-Tag[Blätter, um (mehrere Anzeigen von Drittanbietern hochzuladen](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Pausieren Sie das neue Paket, bis Sie es aktivieren können.

* Beachten Sie Folgendes und bearbeiten Sie das neue Paket nach Bedarf:

   * Verfügt das Konto über genügend Mittel, um das neue Budgetpaket aufzunehmen?

   * Benötigt das neue Paket ein anderes Budget als das vorherige?

   * Sind Mindestbudgets für eine der Platzierungen erforderlich?

   * Laden Sie Kreative, einschließlich aller erforderlichen benutzerdefinierten Anzeigengewichtungen und Zeitpläne, hoch und fügen Sie sie den Platzierungen hinzu.

   * Fügen Sie den Platzierungen und Anzeigen nach Bedarf Ereignis-Pixel hinzu.

   * Schließen Sie bei Bedarf geografische Ziele und [!DNL DoubleVerify Authentic Brand Safety] auf Platzierungsebene in Platzierungen ein.

   * Verwenden Sie für programmgesteuerte garantierte Angebote neue Angebots-IDs und erstellen Sie Standardplatzierungen.

   * Erstellen Sie bei Bedarf neue Platzierungen für [!UICONTROL Simple Ad Serving] Angebote.

* Verwenden Sie bei Paketen, die benutzerdefinierte Optimierungsziele verwenden, die [[!UICONTROL Linked Package for Optimization Learnings Carryover] -Einstellung](/help/dsp/campaign-management/packages/package-settings.md) damit jedes Paket die historischen Daten der vorherigen Kampagne als Eingabe für die Optimierung des Pakets verwendet.

>[!MORELIKETHIS]
>
>* [Über die Paketverwaltung](package-about.md)
>* [Erstellen eines Pakets](package-create.md)
>* [Bearbeiten eines Pakets](package-edit.md)
>* [Anzeigen des Änderungsprotokolls für ein Paket](package-change-log.md)
>* [Paketeinstellungen](package-settings.md)
