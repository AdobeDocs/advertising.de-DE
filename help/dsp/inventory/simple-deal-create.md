---
title: '[!UICONTROL Simple Ad Serving] Angebot erstellen'
description: Erfahren Sie, wie Sie ein Tracking-Pixel für ein [!UICONTROL Simple Ad Serving] Angebot erstellen.
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] Angebot erstellen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]** und wählen Sie dann **[!UICONTROL Simple Ad Serving]** aus.

1. Geben Sie die [Abschlusseinstellungen](simple-deal-settings.md) ein:

   1. Geben Sie im Abschnitt [!UICONTROL Select Ad Source] Informationen zum Herausgeber, zum Advertiser und zur Kampagne sowie zum Anzeigetyp an und klicken Sie dann auf **[!UICONTROL Next]**.

   1. Geben Sie im Abschnitt [!UICONTROL Select Ad(s)] eine Anzeige an, die als Proxy in DSP verwendet werden soll:

      1. Führen Sie einen der folgenden Schritte aus:

         * Wählen Sie für vorhandene Anzeigen die zu verwendenden Anzeigen aus.

         * Erstellen Sie für neue Anzeigen einen Proxy [Anzeige eines Drittanbieters](/help/dsp/campaign-management/ads/ad-create-multiple.md).

      >[!NOTE]
      > DSP bedient nicht die von Ihnen angegebenen Anzeigen. Der Herausgeber bedient die Anzeige.

      1. Klicken Sie auf **[!UICONTROL Next]**.

   1. Bearbeiten Sie in den Feed-Details die Feed-Details und klicken Sie dann auf **[!UICONTROL Next]**.

      DSP generiert automatisch eine Platzierung mit dem Namen „SAS-Platzierung - &lt;*Geschäftsname*>&quot; für die Anzeige. In der Platzierung wird das Angebot automatisch im Abschnitt [!UICONTROL Inventory Targets] angesprochen. Alle anderen Targeting-Optionen sind nicht anwendbar.

1. Senden Sie die Pixel für die Ereignisverfolgung zur Implementierung auf eine der folgenden Arten an den Herausgeber:

   * (Optional) Senden Sie auf dem [!UICONTROL Activate Tag with Publisher]-Bildschirm das Angebots-Tag an den Publisher.

     Wenn Sie die vorherigen Schritte abgeschlossen haben, generiert DSP eine E-Mail-Nachricht, die Sie an den Herausgeber senden können. Die Nachricht enthält die Details des Angebots, einen Link, über den die Angebots-Tag-Nummer abgerufen werden kann, und einen Autorisierungs-Code für den Link.

      1. Überprüfen Sie die Details des Angebots und führen Sie dann einen der folgenden Schritte aus:

         * Um die Informationen in eine E-Mail-Nachricht in einer E-Mail-Anwendung auf Ihrem Gerät einzufügen, klicken Sie auf **[!UICONTROL Email & Done]** und wählen Sie die E-Mail-Anwendung aus. Das Feld [!UICONTROL CC:] wird vorab mit einer [!DNL Adobe] Support-Adresse ausgefüllt. Sie können die Nachricht dann an den entsprechenden Kontakt für den Herausgeber senden.

         * Um die Informationen in die Zwischenablage zu kopieren, klicken Sie auf **[!UICONTROL Copy Email].** Sie können dann den Inhalt manuell in eine E-Mail-Nachricht einfügen und an den entsprechenden Kontakt für den Herausgeber senden. Sie müssen eine Kopie (CC:) zu `publisher-support-global@adobe.com` hinzufügen. Wenn Sie mit dem Kopieren der Nachricht fertig sind, klicken Sie auf **[!UICONTROL Email & Done]**.

      1. (Falls erforderlich) Wenden Sie sich an den Herausgeber, um festzustellen, ob das Tag die entsprechenden Makros enthält, damit das Tag mit dem Anzeigen-Server des Herausgebers zusammenarbeitet.

   * (Optional) Senden Sie die Pixel für die Ereignisverfolgung manuell an den Publisher:

      1. Klicken Sie in der Abschlusszeile in der [!UICONTROL Deals] auf ![Optionsmenü](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         Die Ereignispixel enthalten ein [!UICONTROL Clickthrough] und ein [!UICONTROL Impression]. Video- und Audioanzeigen enthalten auch Ereignispixel nach Quartil (von [!UICONTROL 25% Complete] bis [!UICONTROL 100% Complete]).

      1. Kopieren Sie die Pixel zur Ereignisverfolgung und stellen Sie sie Ihrem Publisher bereit.

>[!MORELIKETHIS]
>
>* [Über [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] Einstellungen](simple-deal-settings.md)
>* [Detailbericht für einen Abschluss anzeigen](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
