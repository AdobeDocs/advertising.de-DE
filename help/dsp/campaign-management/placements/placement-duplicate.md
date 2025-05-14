---
title: Duplizieren von Platzierungen
description: Erfahren Sie, wie Sie eine oder mehrere Platzierungen duplizieren.
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
source-git-commit: 1fe0d3c026cac52104d54b571fd9c2202cc2384b
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Duplizieren von Platzierungen

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplizieren Sie eine oder mehrere Platzierungen, um Platzierungen mit ähnlichen Einstellungen zu erstellen. Sie können:

* Erstellen mehrerer Duplikate von Platzierungen
* Duplizieren Sie Platzierungen innerhalb der ursprünglichen Werbetreibenden und Kampagnen oder innerhalb anderer
* (Für duplizierte Platzierungen innerhalb der ursprünglichen Kampagnen) Duplizieren Sie optional die ursprünglichen Anzeigen
* Status und Flugdatum der neuen Platzierungen ändern

Unter [Was nicht dupliziert ist](#placement-not-duplicated) finden Sie eine Liste der Platzierungseinstellungen, die nicht dupliziert werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Placements]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Um eine Platzierung zu duplizieren, klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** neben dem Paketnamen.

   * Duplizieren mehrerer Platzierungen:

      1. Aktivieren Sie das Kontrollkästchen neben jeder zu duplizierenden Platzierung.

      1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Duplicate]**.

1. Geben Sie die neuen Platzierungseinstellungen an:

   1. (Einzelne Platzierungen) Geben Sie den neuen Platzierungsnamen ein.

   1. Wählen Sie im Menü **[!UICONTROL Choose Package (Required)]** entweder das übergeordnete Paket oder **[!UICONTROL No package]* aus.

   1. (Optional) Ändern Sie die Standardeinstellungen.

   Die Einstellungen gelten für alle ausgewählten Platzierungen.

   Standardmäßig beziehen sich die neuen Platzierungen auf den ursprünglichen Anzeigentyp, werden den ursprünglichen Werbetreibenden und Kampagnen zugewiesen, haben Flugpläne, die am aktuellen Tag beginnen, sind angehalten und enthalten nicht die ursprünglichen Anzeigen.

   Wenn Sie mehrere Platzierungen erstellen, werden die neuen Platzierungsnamen mit einer Nummer gemäß der Konvention &lt;*original_placement_name #N*> angehängt, z. B. „Meine Platzierung #2“.

1. Klicken Sie auf **[!UICONTROL Submit]**.

## Was nicht dupliziert wird {#placement-not-duplicated}

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

## Best Practices zum Konfigurieren der neuen Platzierungen

>[!TIP]
>
>* Verwenden Sie Bulksheets, [Änderungen an mehreren Kampagnenkomponenten gleichzeitig vorzunehmen](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Verwenden Sie Anzeigen-Tag[Blätter, um (mehrere Anzeigen von Drittanbietern hochzuladen](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Pausieren Sie die neuen Platzierungen, bis Sie bereit sind, sie zu aktivieren.

* Beachten Sie Folgendes und bearbeiten Sie die neuen Platzierungen nach Bedarf:

   * Verfügt das Konto über genügend Mittel, um die neuen Platzierungsbudgets aufzunehmen?

   * Benötigen die neuen Platzierungen ein anderes Budget als die vorherigen?

   * Laden Sie Kreative, einschließlich aller erforderlichen benutzerdefinierten Anzeigengewichtungen und Zeitpläne, hoch und fügen Sie sie den Platzierungen hinzu.

   * Fügen Sie den Platzierungen und Anzeigen nach Bedarf Ereignis-Pixel hinzu.

   * Schließen Sie bei Bedarf geografische Ziele und [!DNL DoubleVerify Authentic Brand Safety] auf Platzierungsebene in die Platzierungen ein.

   * Verwenden Sie für programmgesteuerte garantierte Angebote neue Angebots-IDs und erstellen Sie Standardplatzierungen.

   * Erstellen Sie bei Bedarf neue Platzierungen für [!UICONTROL Simple Ad Serving] Angebote.

>[!MORELIKETHIS]
>
>* [Über die Platzierungsverwaltung](placement-about.md)
>* [Platzierung erstellen](placement-create.md)
>* [Platzierungen bearbeiten](placement-edit.md)
>* [Anzeigen des Änderungsprotokolls für eine Platzierung](placement-change-log.md)
>* [Platzierungseinstellungen](placement-settings.md)
