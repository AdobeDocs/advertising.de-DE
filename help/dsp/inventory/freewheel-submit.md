---
title: Senden einer Anzeige für ein PG-Deal an [!DNL FreeWheel]
description: Erfahren Sie, wie Sie eine Genehmigung für eine Anzeige für ein programmgesteuertes garantiertes Geschäft mit einem Herausgeber anfordern können in [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Senden Sie eine Anzeige für einen programmgesteuerten garantierten Deal an [!DNL Freewheel]

*Konten mit der [!DNL FreeWheel] Nur programmatische Garantieberechtigungen*

Einmal [akzeptieren programmgesteuertes garantiertes Geschäft mit einem Herausgeber auf FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), einschließlich der Auswahl einer Anzeige und der Erstellung der programmgarantierten Standardplatzierung, die für das Angebot verwendet werden soll, müssen Sie die Anzeige an senden [!DNL Freewheel] zur Genehmigung.

>[!PREREQUISITES]
>
>Arbeiten Sie mit Ihrem Adobe-Kundenbetreuungsteam zusammen, um sicherzustellen, dass Ihre [!DNL DSP] -Konto über die Berechtigung zum Verwenden der [!DNL FreeWheel] programmgesteuerter garantierter Workflow.

1. Kopieren Sie den Anzeigenschlüssel für die mit der [!DNL Freewheel] handeln:

   1. Klicken Sie auf den Namen der Kampagne.

   1. Klicken Sie im Untermenü auf **[!UICONTROL Ads]**.

   1. Klicken  **[!UICONTROL ...]** > **[!UICONTROL Edit]** neben dem Anzeigennamen.

   1. Kopieren Sie nach dem Öffnen der Anzeigeneinstellungen den alphanumerischen Anzeigenschlüssel in die URL, die in der Adressleiste des Browsers angezeigt wird.

      In der folgenden URL lautet beispielsweise der Anzeigenschlüssel `3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. Senden Sie die Anzeige an [!DNL Freewheel]:

   1. Führen Sie einen der folgenden Schritte aus:

      * Klicken Sie neben dem Anzeigennamen auf  **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**.

      * Klicken Sie im Hauptmenü auf **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**. Klicken Sie in der Zeile &quot;Deal&quot;auf ![Optionen, Menü](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**.
   1. Überprüfen Sie die Deal-ID, geben Sie die **[!UICONTROL Ad Key]** Sie haben in Schritt 1 kopiert und klicken dann auf **[!UICONTROL Submit]**.

   Die Anzeige muss vor der Ausführung gesendet und genehmigt werden.

1. [Überprüfen des Status der Anzeigenübermittlung](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Übersicht über die Einrichtung von programmatischen Garantievereinbarungen in [!DNL Freewheel]](freewheel-overview.md)
>* [Akzeptieren eines Angebots im Deal-ID-Posteingang](deal-id-inbox-accept.md)
>* [Überprüfen des Status von Anzeigen auf [!DNL FreeWheel] Gesicherte programmatische Vereinbarungen](freewheel-check-status.md)
>* [Fehlercodes für [!DNL Freewheel] Anzeigenübermittlungen](freewheel-error-codes.md)

