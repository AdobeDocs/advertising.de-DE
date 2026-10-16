---
title: Erstellen einer Anzeigenvorlage aus einem Bild mithilfe von KI
description: Erfahren Sie, wie Sie mit KI in Creative Studio ein vorhandenes statisches Anzeigen-Anzeigenbild in eine bearbeitbare Anzeigenvorlage konvertieren können.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: adc2fdc93f06b5459c19b08306d1e30ce00e7028
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%
---
# Erstellen einer Anzeigenvorlage aus einem Bild mithilfe von KI

*Beta-Funktion*

Verwenden Sie KI in [!UICONTROL Creative Studio] , um ein vorhandenes statisches Display-Anzeigenbild in eine bearbeitbare Display-Anzeigenvorlage zu konvertieren. Überprüfen Sie die generierte Vorlage, fordern Sie Änderungen in natürlicher Sprache an, und öffnen Sie den Vorlageneditor, um manuelle Änderungen vorzunehmen und die Vorlage zu speichern.

## Bevor Sie beginnen

Sie benötigen eine vorhandene statische Bildanzeige in einer Creative-Bibliothek. Dieser Workflow wählt Anzeigen aus Ihren Bibliotheken aus und lädt kein neues Bild direkt in den Erstellungsdialog hoch.

## Erstellen und Überprüfen der Vorlage {#template-generate}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative Studio]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. (Optional) Wählen Sie oben auf der Seite einen Advertiser aus der Advertiser-Liste aus, um die Bibliotheken dieses Advertisers anzuzeigen.

1. Klicken Sie im **[!UICONTROL Use AI to Generate a New Display Ad Template]** auf **[!UICONTROL Generate]**.

1. Wählen Sie im Dialogfeld **[!UICONTROL Generate New Ad Template]** die Option **[!UICONTROL Generate from Existing Standard Ad Image]** aus, falls sie nicht bereits ausgewählt ist.

1. Wählen Sie in der Liste **[!UICONTROL Ad Library]** die Bibliothek aus, die die Bildanzeige enthält.

1. Halten Sie den Cursor über die Bild-Anzeigenkarte und klicken Sie auf **[!UICONTROL Use this Standard Ad]**.

   Die Generierung beginnt automatisch mit der Breite und Höhe der ausgewählten Anzeige.

1. Warten Sie, bis die Generierung abgeschlossen ist, und überprüfen Sie dann die Vorlagenvorschau und das Bedienfeld &quot;**[!UICONTROL Layers]**&quot;, falls verfügbar.

   Überprüfen Sie den Text, die Bilder und das Layout, bevor Sie die Vorlage verwenden. Die hier angezeigten Ebenen werden überprüft. Nehmen Sie manuelle Änderungen im Vorlageneditor vor.

1. (Optional) Anfordern von Änderungen an der generierten Vorlage:

   1. Beschreiben Sie im Feld **[!UICONTROL Ask the AI for any changes]** die gewünschten Änderungen. Geben Sie beispielsweise `Change the headline to "Limited Time Offer" and the button text to "Shop Now"` ein.

   1. Klicken Sie auf **[!UICONTROL Regenerate]**.

   1. Überprüfen Sie die aktualisierte Vorschau. Wiederholen Sie dies nach Bedarf.

1. Wenn Sie bereit zum Fortfahren sind, klicken Sie auf **[!UICONTROL Use this Ad Template]**.

   Die generierte Vorlage wird im Anzeigevorlageneditor geöffnet.

## Vorlage bearbeiten und speichern {#template-save}

1. Überprüfen Sie im Vorlageneditor die generierten Elemente und nehmen Sie die verbleibenden Änderungen mithilfe der Steuerelemente [Vorlageneditor) ](creative-studio-manage-templates.md#template-controls).

1. Klicken Sie auf **[!UICONTROL Save]**.

1. Geben Sie im Dialogfeld &quot;**[!UICONTROL Update Template]**&quot; die **[!UICONTROL Template name]** ein, aktualisieren Sie sie, wählen Sie die **[!UICONTROL Advertiser]** aus und fügen Sie optional Tags hinzu.

1. Klicken Sie auf **[!UICONTROL Update]** , um die Vorlage zu speichern und zur **[!UICONTROL Templates]** zurückzukehren.

   Um stattdessen eine separate Kopie zu speichern, klicken Sie auf **[!UICONTROL Save As New]**.

Anschließend können Sie die Vorlage verwenden, um [Anzeigenvarianten zu generieren](creative-studio-manage-templates.md#ad-variations-generate).

## Wenn Sie keine Vorlage generieren können {#troubleshooting}

* **Es werden keine Bibliotheken oder Bildanzeigen aufgelistet:** Überprüfen Sie den ausgewählten Advertiser und die **[!UICONTROL Ad Library]**. Wenn die Bibliothek keine Standard-Anzeigenbilder enthält, wählen Sie eine andere Bibliothek aus, die eine vorhandene statische Bildanzeige enthält.

* **Die Generierung schlägt fehl oder das Bild kann nicht konvertiert werden:** Sie die angezeigte Nachricht, klicken Sie auf &quot;**[!UICONTROL Back to library]**&quot; und wählen Sie eine Bildanzeige aus, um es erneut zu versuchen.

>[!MORELIKETHIS]
>
>* [Verwalten von Anzeigenvorlagen in Creative Studio](creative-studio-manage-templates.md)
>* [Verwalten von Standardanzeigen in Creative Studio](creative-studio-manage-standard-ads.md)