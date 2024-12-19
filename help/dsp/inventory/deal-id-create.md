---
title: Details zur Angebots-ID manuell erstellen
description: Erfahren Sie, wie Sie Details für eine Angebots-ID manuell eingeben.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Details zur Angebots-ID manuell erstellen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]** und wählen Sie dann **[!UICONTROL Deal ID]** aus.

1. Geben Sie die [Abschlusseinstellungen](deal-id-settings.md) ein:

   1. Geben Sie im Abschnitt [!UICONTROL Deal ID basics] die Details des Angebots und die Werbetreibenden an, die auf das Angebot zugreifen können. Bei garantierten Angeboten müssen Sie auch die geplanten Flugdaten und die geschätzte Anzahl der Impressionen angeben, jedoch nur zu Tracking-Zwecken.

      Sie können das Tempo von garantierten Angeboten verfolgen, indem Sie die Ausgabespalte „PG-Impression-Geschwindigkeit“ in die Ansicht „Inventar“ > „Angebote“ aufnehmen.

   1. (Nur Administrator-Benutzer; optional) Bearbeiten Sie im Abschnitt [!UICONTROL Technical] die Standardeinstellungen nach Bedarf.

   1. Klicken Sie auf **[!UICONTROL Save]**.

1. (Nur garantierte Angebote) Wählen Sie die Anzeigen aus, die für das Angebot verwendet werden sollen (oder das 1x1-Pixel für vom Publisher verwaltete Anzeigen), und erstellen Sie eine standardmäßige programmgesteuert garantierte Platzierung (PG).

   Standardmäßige PG-Platzierungen stellen sicher, dass Ihr Abschluss für jede Angebotsanfrage immer ein Angebot zurückgibt. Wenn Sie keine standardmäßige PG-Platzierung erstellen, geben alle Platzierungen, die auf den Deal abzielen, keine Angebote aus, es sei denn, sie sind korrekt eingerichtet. Sie sollten immer eine standardmäßige PG-Platzierung erstellen. In der [!UICONTROL Placements] haben standardmäßige PG-Platzierungen den [!UICONTROL Sub-type] Spaltenwert &quot;[!UICONTROL PG Default]&quot;.

   Sie können das Angebot optional als Lagerziel in zusätzlichen Platzierungen verwenden, müssen es jedoch korrekt einrichten, um Angebote zu platzieren.

   1. Wählen Sie in den [!UICONTROL Ad & Campaign Selection] die Anzeigen aus, die für das Angebot verwendet werden sollen:

      1. Wählen Sie den Advertiser, die Kampagne und den Anzeigentyp aus. Wählen Sie optional einen Anzeigenstatus aus, nach dem die Anzeigen gefiltert werden sollen.

      1. Aktivieren Sie in der Liste der verfügbaren Anzeigen das Kontrollkästchen neben jeder Anzeige, die für das Angebot verwendet werden soll.

         Für jede vom Publisher verwaltete Anzeige wird automatisch ein 1 x 1 Tracking-Pixel angewendet, nachdem ein Advertiser und eine Kampagne ausgewählt wurden.

      1. Klicken Sie auf **[!UICONTROL Apply]**.

   1. Im Bildschirm mit den Platzierungseinstellungen :

      1. Geben Sie den Platzierungsnamen ein.

      1. (Optional) Bearbeiten Sie die [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md) einschließlich des Überschreibens des Standardangebots, das automatisch mit dem CPM-Wert aus dem Angebot gefüllt wird. Ändern Sie den Datumsbereich oder fügen Sie weitere Anzeigen hinzu.

      Der Abschluss wird automatisch im Abschnitt Inventarziele ausgewählt. Alle anderen Targeting-Optionen sind nicht anwendbar.

      1. Klicken Sie auf **[!UICONTROL Create placement]**.

Nachdem Sie den Abschluss erstellt haben, können Sie ihn als Lagerziel für mehrere Platzierungen verwenden.

>[!NOTE]
>
> Sie müssen das Angebots-Tag nicht zur Verifizierung an den Publisher senden.

>[!TIP]
>
>* In der Ansicht [!UICONTROL Inventory] > [!UICONTROL Deals] zeigt die Spalte [!UICONTROL Pacing & Budget] an, wie sich das Angebot am angegebenen Flugdatum und am angegebenen Impressionsziel entwickelt.
>
>* Wenn der Versand zu langsam oder zu schnell erfolgt, wenden Sie sich an Ihren Publisher, um anzupassen, wie viel Volumen er über den Abschluss sendet.

>[!MORELIKETHIS]
>
>* [Manuelle Deal ID-Einstellungen](deal-id-settings.md)
>* [Richten Sie einen programmgesteuerten garantierten Abschluss ein](programmatic-guaranteed-set-up.md)
>* [Senden einer Anzeige für einen programmgesteuerten garantierten Deal mit [!DNL FreeWheel]](freewheel-submit.md)
>* [Über programmgesteuerte garantierte -Angebote](programmatic-guaranteed-about.md)
<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->
