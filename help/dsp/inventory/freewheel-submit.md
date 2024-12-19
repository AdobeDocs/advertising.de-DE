---
title: Senden einer Anzeige für einen PG-Deal an [!DNL FreeWheel]
description: Erfahren Sie, wie Sie eine Genehmigung für eine Anzeige für einen programmgesteuerten garantierten Deal mit einem Herausgeber in anfordern [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# Senden einer Anzeige für einen programmgesteuerten garantierten Abschluss an [!DNL Freewheel]

*Nur Konten mit der [!DNL FreeWheel] Programmatic Guaranteed-Berechtigung*

Sobald Sie [einen programmgesteuert garantierten Deal mit einem Publisher auf FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) akzeptieren, einschließlich der Auswahl einer Anzeige und der Erstellung der programmgesteuert garantierten Standardplatzierung, die für den Deal verwendet werden soll, müssen Sie die Anzeige zur Genehmigung an [!DNL Freewheel] senden.

>[!PREREQUISITES]
>
>Arbeiten Sie mit Ihrem Adobe-Konto-Team zusammen, um sicherzustellen, dass Ihr [!DNL DSP]-Konto über die Berechtigung zur Verwendung des [!DNL FreeWheel] programmgesteuert garantierten Workflows verfügt.

1. Kopieren Sie den Anzeigenschlüssel für die Anzeige, die mit dem [!DNL Freewheel] Deal verwendet wird:

   1. Klicken Sie auf den Namen der Kampagne.

   1. Klicken Sie im Untermenü auf **[!UICONTROL Ads]**.

   1. Klicken Sie neben dem Anzeigenamen auf **[!UICONTROL ...]** > **[!UICONTROL Edit]** .

   1. Kopieren Sie nach dem Öffnen der Anzeigeneinstellungen den alphanumerischen Anzeigenschlüssel in die URL, die in der Adressleiste des Browsers angezeigt wird.

      Bei der folgenden URL lautet der Anzeigenschlüssel beispielsweise `3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. Senden Sie die Anzeige an [!DNL Freewheel]:

   1. Führen Sie einen der folgenden Schritte aus:

      * Klicken Sie neben dem Anzeigenamen auf **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**.

      * Klicken Sie im Hauptmenü auf **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**. Klicken Sie in der Angebotszeile auf ![Optionsmenü](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**.

   1. Überprüfen Sie die Angebots-ID, geben Sie die in Schritt 1 kopierte **[!UICONTROL Ad Key]** ein und klicken Sie dann auf **[!UICONTROL Submit]**.

   Die Anzeige muss eingereicht und genehmigt werden, bevor sie ausgeführt wird.

1. [Überprüfen Sie den Status der Anzeigenübermittlung](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Überblick über die Einrichtung von garantierten programmgesteuerten Angeboten in [!DNL Freewheel]](freewheel-overview.md)
>* [Akzeptieren eines Angebots im Angebots-ID-Posteingang](deal-id-inbox-accept.md)
>* [Überprüfen Sie den Status der Anzeigen  [!DNL FreeWheel]  programmgesteuerte garantierte -Angebote](freewheel-check-status.md)
>* [Fehler-Codes für  [!DNL Freewheel] Anzeigenübermittlungen](freewheel-error-codes.md)
