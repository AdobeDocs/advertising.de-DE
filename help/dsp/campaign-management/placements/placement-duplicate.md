---
title: Doppelte Platzierungen
description: Erfahren Sie, wie Sie eine oder mehrere Platzierungen duplizieren.
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
TQID: https://experienceleague.adobe.com/1QHdooPh2tr6pfbnRsPbe-P5o-lZLgX-NQIUNG2ulHM
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: fdc899fcc763a963e5878b2fcf313174b8f5a74b
workflow-type: tm+mt
source-wordcount: 445
ht-degree: 0%

---

# Doppelte Platzierungen

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplizieren Sie eine oder mehrere Platzierungen, um Platzierungen mit ähnlichen Einstellungen zu erstellen. Sie können:

* Erstellen mehrerer Duplikate von Platzierungen
* Duplizieren Sie Platzierungen innerhalb der ursprünglichen Werbetreibenden und Kampagnen oder innerhalb anderer
* (Für duplizierte Platzierungen innerhalb der ursprünglichen Kampagnen) Duplizieren Sie optional die ursprünglichen Anzeigen
* Status und Flugdatum der neuen Platzierungen ändern

Unter [Was nicht dupliziert wird](#placement-not-duplicated) finden Sie eine Liste der Platzierungseinstellungen, die nicht dupliziert werden.

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
* Mindestbudgets auf Platzierungsebene
* (Wenn Sie die Flugdaten ändern) Benutzerdefinierte Anzeigenplanung
* (Wenn Sie keine Anzeigen anhängen) Benutzerdefinierte Anzeigengewichtung und -planung
* Standardplatzierungen für programmgesteuert garantierte (PG) Angebote und Platzierungen für [!UICONTROL Simple Ad Serving] Angebote
* (Wenn Sie Platzierungen in eine andere Kampagne kopieren):
   * Geo-Ziele
   * Ereignispixel
   * Anzeigen
   * [!DNL DoubleVerify Authentic Brand Suitability] auf Platzierungsebene (die die Segmente auf Advertiser-Ebene überschreiben)

## Best Practices zum Konfigurieren der neuen Platzierungen

>[!TIP]
>
>* Verwenden Sie Bulksheets, [Änderungen an mehreren Kampagnenkomponenten gleichzeitig vorzunehmen](/help/dsp/campaign-management/campaign-components-review-edit.md).
>* Verwenden Sie Anzeigen-Tag[Blätter, um (mehrere Anzeigen von Drittanbietern hochzuladen](/help/dsp/campaign-management/ads/ad-create-multiple.md).

* Pausieren Sie die neuen Platzierungen, bis Sie bereit sind, sie zu aktivieren.

* Beachten Sie Folgendes und bearbeiten Sie die neuen Platzierungen nach Bedarf:

   * Verfügt das Konto über genügend Mittel, um die neuen Platzierungsbudgets aufzunehmen?

   * Benötigen die neuen Platzierungen ein anderes Budget als die vorherigen? Sind Mindestbudgets erforderlich?

   * Laden Sie Kreative, einschließlich aller erforderlichen benutzerdefinierten Anzeigengewichtungen und Zeitpläne, hoch und fügen Sie sie den Platzierungen hinzu.

   * Fügen Sie den Platzierungen und Anzeigen nach Bedarf Ereignis-Pixel hinzu.

   * Schließen Sie bei Bedarf geografische Ziele und [!DNL DoubleVerify Authentic Brand Suitability] auf Platzierungsebene in die Platzierungen ein.

   * Verwenden Sie für programmgesteuerte garantierte Angebote neue Angebots-IDs und erstellen Sie Standardplatzierungen.

   * Erstellen Sie bei Bedarf neue Platzierungen für [!UICONTROL Simple Ad Serving] Angebote.

>[!MORELIKETHIS]
>
>* [Über die Platzierungsverwaltung in Advertising DSP](placement-about.md)
>* [Platzierung erstellen](placement-create.md)
>* [Platzierungen bearbeiten](placement-edit.md)
>* [Anzeigen des Änderungsprotokolls für eine Platzierung](placement-change-log.md)
>* [Platzierungseinstellungen](placement-settings.md)
