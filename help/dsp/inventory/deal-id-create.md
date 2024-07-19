---
title: Manuelles Erstellen von Details zur Angebots-ID
description: Erfahren Sie, wie Sie Details für eine Angebots-ID manuell eingeben.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Manuelles Erstellen von Details zur Angebots-ID

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]** und wählen Sie dann **[!UICONTROL Deal ID]** aus.

1. Geben Sie die [Deal-Einstellungen](deal-id-settings.md) ein:

   1. Geben Sie im Abschnitt [!UICONTROL Deal ID basics] die Details des Geschäfts und die Advertiser an, die auf den Deal zugreifen können. Für garantierte Angebote müssen Sie auch die geplanten Flugdaten und die geschätzte Anzahl der Impressionen angeben, und zwar ausschließlich zu Tracking-Zwecken.

      Sie können das Tempo der garantierten Angebote verfolgen, indem Sie die Ausgabespalte &quot;PG Impression Pacing&quot;in die Ansicht &quot;Inventar&quot;> &quot;Angebote&quot;einbeziehen.

   1. (Nur Administrator-Benutzer; optional) Bearbeiten Sie im Abschnitt [!UICONTROL Technical] die Standardeinstellungen nach Bedarf.

   1. Klicken Sie auf **[!UICONTROL Save]**.

1. (Nur garantierte Angebote) Wählen Sie die Anzeigen aus, die für das Angebot verwendet werden sollen (oder das 1x1-Pixel für publisher-verwaltete Anzeigen), und erstellen Sie eine standardmäßige, programmgarantierte Platzierung (PG).

   Standardmäßige PG-Platzierungen stellen sicher, dass Ihr Deal immer ein Angebot für jede Angebotsanforderung zurückgibt. Wenn Sie keine standardmäßige PG-Platzierung erstellen, platzieren Platzierungen, die auf den Deal abzielen, keine Angebote, es sei denn, sie sind korrekt eingerichtet. Sie sollten immer eine standardmäßige PG-Platzierung erstellen. In der Ansicht [!UICONTROL Placements] haben standardmäßige PG-Platzierungen den Spaltenwert &quot;[!UICONTROL PG Default]&quot;[!UICONTROL Sub-type].

   Sie können den Deal optional als Lagerbestandsziel in zusätzlichen Platzierungen verwenden, müssen sie jedoch korrekt einrichten, um Angebote zu platzieren.

   1. Wählen Sie in den Einstellungen für [!UICONTROL Ad & Campaign Selection] die Anzeigen aus, die für den Deal verwendet werden sollen:

      1. Wählen Sie den Advertiser, die Kampagne und den Anzeigentyp aus. Wählen Sie optional einen Anzeigenstatus zum Filtern der Anzeigen aus.

      1. Aktivieren Sie in der Liste der verfügbaren Anzeigen das Kontrollkästchen neben den einzelnen Anzeigen, die für das Geschäft verwendet werden sollen.

         Für jede von Publisher verwaltete Anzeige wird automatisch ein 1x1-Tracking-Pixel angewendet, nachdem ein Advertiser und eine Kampagne ausgewählt wurden.

      1. Klicken Sie auf **[!UICONTROL Apply]**.

   1. Im Bildschirm für die Platzierungseinstellungen:

      1. Geben Sie den Platzierungsnamen ein.

      1. (Optional) Bearbeiten Sie die [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md), einschließlich des Überschreibens des Standardangebots, das automatisch mit dem CPM-Wert aus dem Deal gefüllt wird, Ändern des Datumsbereichs oder Anhängen weiterer Anzeigen.

      Der Deal wird automatisch im Abschnitt Inventarziele angesprochen. Alle anderen Targeting-Optionen sind nicht verfügbar.

      1. Klicken Sie auf **[!UICONTROL Create placement]**.

Nachdem Sie den Deal erstellt haben, können Sie den Deal als Inventarziel für mehrere Platzierungen verwenden.

>[!NOTE]
>
> Sie müssen das Deal-Tag nicht zur Verifizierung an den Herausgeber senden.

>[!TIP]
>
>* In der Ansicht [!UICONTROL Inventory] > [!UICONTROL Deals] zeigt die Spalte [!UICONTROL Pacing & Budget] an, wie der Deal zum festgelegten Flugdatum und Impressionsziel gelangt.
>
>* Wenn der Versand zu kurz oder zu schnell verläuft, wenden Sie sich an Ihren Herausgeber, um die Menge anzupassen, die durch den Deal gesendet wird.

>[!MORELIKETHIS]
>
>* [Manuelle ID-Einstellungen für Geschäfte](deal-id-settings.md)
>* [Einrichten eines programmgesteuerten Garantierten Deals](programmatic-guaranteed-set-up.md)
>* [Senden einer Anzeige für einen programmgesteuerten garantierten Deal mit  [!DNL FreeWheel]](freewheel-submit.md)
>* [Über programmgesteuerte garantierte Deals](programmatic-guaranteed-about.md)
<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->
