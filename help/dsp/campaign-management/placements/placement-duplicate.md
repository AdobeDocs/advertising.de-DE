---
title: Duplizieren von Platzierungen
description: Erfahren Sie, wie Sie eine oder mehrere Platzierungen duplizieren.
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# Duplizieren von Platzierungen

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplizieren Sie eine oder mehrere Platzierungen, um Platzierungen mit ähnlichen Einstellungen zu erstellen. Sie können:

* Mehrere Duplikate von Platzierungen erstellen
* Duplizieren Sie Platzierungen innerhalb der ursprünglichen Advertiser und Kampagnen oder in verschiedenen Kampagnen.
* (Für duplizierte Platzierungen in den ursprünglichen Kampagnen) Optional Duplizieren Sie die ursprünglichen Anzeigen.
* Status und Flugdaten der neuen Platzierungen ändern

Eine Liste der nicht duplizierten Platzierungseinstellungen finden Sie unter &quot;[Was ist nicht dupliziert](#placement-not-duplicated)&quot;.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Placements]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Um eine Platzierung zu duplizieren, klicken Sie auf **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** neben dem Paketnamen.

   * Duplizieren mehrerer Platzierungen:

      1. Aktivieren Sie das Kontrollkästchen neben jeder Platzierung, die dupliziert werden soll.

      1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Duplicate]**.

1. Geben Sie die neuen Platzierungseinstellungen an:

   1. (Einzelplatzierungen) Geben Sie den neuen Platzierungsnamen ein.

   1. Wählen Sie im Menü **[!UICONTROL Choose Package (Required)]** entweder das übergeordnete Paket oder **[!UICONTROL No package]* aus.

   1. (Optional) Ändern Sie die Standardeinstellungen.

   Die Einstellungen gelten für alle ausgewählten Platzierungen.

   Standardmäßig beziehen sich die neuen Platzierungen auf den ursprünglichen Anzeigentyp, werden den ursprünglichen Advertisern und Kampagnen zugewiesen, haben Flugpläne, die am aktuellen Tag beginnen, werden angehalten und enthalten nicht die ursprünglichen Anzeigen.

   Wenn Sie mehrere Platzierungen erstellen, werden die neuen Platzierungsnamen entsprechend der Konvention &lt;*original_placement_name #N*> mit einer Zahl angehängt, z. B. &quot;My Placement #2&quot;.

1. Klicken Sie auf **[!UICONTROL Submit]**.

## Nicht duplizierte Elemente {#placement-not-duplicated}

Alle Einstellungen der ursprünglichen Platzierungen werden dupliziert, mit Ausnahme:

* Experimenteinstellungen
* (Wenn Sie die Flugdaten ändern) Benutzerdefinierte Anzeigenplanung
* (Wenn Sie keine Anzeigen anhängen) Benutzerdefinierte Anzeigengewichtung und -planung
* Standardplatzierungen für programmgarantierte (PG) Angebote und Platzierungen für [!UICONTROL Simple Ad Serving] Angebote
* (Wenn Sie Platzierungen in eine andere Kampagne kopieren):
   * Geo-Ziele
   * Ereignispixel
   * Anzeigen
   * Segmente auf Platzierungsebene [!DNL DoubleVerify Authentic Brand Safety] (die die Segmente auf Advertiser-Ebene überschreiben)

>[!MORELIKETHIS]
>
>* [Über die Platzierungsverwaltung](placement-about.md)
>* [Erstellen einer Platzierung](placement-create.md)
>* [Platzierungen bearbeiten](placement-edit.md)
>* [Anzeigen des Änderungsprotokolls für eine Platzierung](placement-change-log.md)
>* [Platzierungseinstellungen](placement-settings.md)
