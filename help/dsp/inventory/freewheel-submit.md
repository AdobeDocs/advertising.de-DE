---
title: Senden einer Anzeige für ein PG-Geschäft an  [!DNL FreeWheel]
description: Erfahren Sie, wie Sie eine Genehmigung für eine Anzeige für ein programmgesteuertes garantiertes Geschäft mit einem Herausgeber für  [!DNL Freewheel] anfordern.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# Senden einer Anzeige für einen programmgesteuerten garantierten Deal an [!DNL Freewheel]

*Nur Konten mit der Berechtigung [!DNL FreeWheel] Programmgarantiert*

Sobald Sie [ein programmgesteuertes garantiertes Angebot für einen Herausgeber auf FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) akzeptiert haben, einschließlich der Auswahl einer Anzeige und der Erstellung der programmgarantierten Standardplatzierung, die für das Geschäft verwendet werden soll, müssen Sie die Anzeige zur Genehmigung an [!DNL Freewheel] senden.

>[!PREREQUISITES]
>
>Arbeiten Sie mit Ihrem Adobe Account-Team zusammen, um sicherzustellen, dass Ihr [!DNL DSP]-Konto berechtigt ist, den programmgarantierten Workflow [!DNL FreeWheel] zu verwenden.

1. Kopieren Sie den Anzeigenschlüssel für die Anzeige, die mit dem [!DNL Freewheel] -Deal verwendet wird:

   1. Klicken Sie auf den Namen der Kampagne.

   1. Klicken Sie im Untermenü auf **[!UICONTROL Ads]**.

   1. Klicken Sie neben dem Anzeigennamen auf **[!UICONTROL ...]** > **[!UICONTROL Edit]** .

   1. Sobald die Anzeigeneinstellungen geöffnet sind, kopieren Sie den alphanumerischen Anzeigenschlüssel in die URL, die in der Adressleiste des Browsers angezeigt wird.

      In der folgenden URL ist der Anzeigenschlüssel beispielsweise `3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. Senden Sie die Anzeige an [!DNL Freewheel]:

   1. Führen Sie einen der folgenden Schritte aus:

      * Klicken Sie neben dem Anzeigennamen auf **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**.

      * Klicken Sie im Hauptmenü auf **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**. Klicken Sie in der Zeile &quot;Deal&quot;auf ![Menü &quot;Optionen&quot;](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**.

   1. Überprüfen Sie die Deal-ID, geben Sie die **[!UICONTROL Ad Key]** ein, die Sie in Schritt 1 kopiert haben, und klicken Sie dann auf **[!UICONTROL Submit]**.

   Die Anzeige muss gesendet und genehmigt werden, bevor sie ausgeführt wird.

1. [Überprüfen Sie den Status der Anzeigenübermittlung](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Übersicht über die Einrichtung programmgesteuerter garantierter Deals in  [!DNL Freewheel]](freewheel-overview.md)
>* [Akzeptieren eines Angebots im Posteingang der Angebots-ID](deal-id-inbox-accept.md)
>* [Überprüfen Sie den Status der Anzeigen für  [!DNL FreeWheel] programmgesteuerte garantierte Angebote](freewheel-check-status.md)
>* [Fehlercodes für [!DNL Freewheel] Anzeigenübermittlungen](freewheel-error-codes.md)
