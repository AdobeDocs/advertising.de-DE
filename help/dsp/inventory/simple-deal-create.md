---
title: Erstellen eines [!UICONTROL Simple Ad Serving]-Angebots
description: Erfahren Sie, wie Sie ein Tracking-Pixel für einen [!UICONTROL Simple Ad Serving] -Deal erstellen.
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Erstellen eines [!UICONTROL Simple Ad Serving]-Angebots

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]** und wählen Sie dann **[!UICONTROL Simple Ad Serving]** aus.

1. Geben Sie die [Deal-Einstellungen](simple-deal-settings.md) ein:

   1. Geben Sie im Abschnitt &quot;[!UICONTROL Select Ad Source]&quot;Informationen zum Publisher, Advertiser, Kampagne und Anzeigentyp an und klicken Sie auf &quot;**[!UICONTROL Next]**&quot;.

   1. Geben Sie im Abschnitt [!UICONTROL Select Ad(s)] eine Anzeige an, die als Proxy in DSP verwendet werden soll:

      1. Führen Sie einen der folgenden Schritte aus:

         * Wählen Sie für vorhandene Anzeigen die zu verwendenden Anzeigen aus.

         * Erstellen Sie für neue Anzeigen einen Proxy [Drittanbieteranzeige](/help/dsp/campaign-management/ads/ad-create-multiple.md).

      >[!NOTE]
      > DSP bedient nicht die von Ihnen angegebenen Anzeigen. Der Herausgeber stellt die Anzeige bereit.

      1. Klicken Sie auf **[!UICONTROL Next]**.

   1. Bearbeiten Sie in den Feed-Details die Feed-Details und klicken Sie auf **[!UICONTROL Next]**.

      DSP generiert für die Anzeige automatisch eine Platzierung mit dem Namen &quot;SAS Placement - &lt;*Vorlagenname*>&quot;. In der Platzierung wird der Deal automatisch im Abschnitt &quot;[!UICONTROL Inventory Targets]&quot; angesprochen. Alle anderen Targeting-Optionen sind nicht verfügbar.

1. Senden Sie die Ereignisverfolgungspixel zur Implementierung an den Herausgeber auf eine der folgenden Arten:

   * (Optional) Senden Sie im Bildschirm &quot;[!UICONTROL Activate Tag with Publisher]&quot;das Deal-Tag an den Herausgeber.

     Wenn Sie die vorherigen Schritte abgeschlossen haben, generiert DSP eine E-Mail-Nachricht, die Sie an den Herausgeber senden können. Die Nachricht enthält die Details des Deals, einen Link, aus dem das Deal-Tag abgerufen werden soll, und einen Autorisierungscode für den Link.

      1. Überprüfen Sie die Details des Deals und führen Sie dann einen der folgenden Schritte aus:

         * Um die Informationen in eine E-Mail-Nachricht in eine E-Mail-Anwendung auf Ihrem Gerät einzufügen, klicken Sie auf **[!UICONTROL Email & Done]** und wählen Sie die E-Mail-Anwendung aus. Das Feld &quot;[!UICONTROL CC:]&quot; wird vorab mit der Support-Adresse &quot;[!DNL Adobe]&quot; ausgefüllt. Sie können die Nachricht dann an den entsprechenden Kontakt für den Herausgeber senden.

         * Um die Informationen in die Zwischenablage zu kopieren, klicken Sie auf **[!UICONTROL Copy Email].** Sie können den Inhalt dann manuell in eine E-Mail-Nachricht einfügen und an den entsprechenden Kontakt für den Herausgeber senden. Sie müssen eine Kopie (CC:) in `publisher-support-global@adobe.com` einfügen. Wenn Sie mit dem Kopieren der Nachricht fertig sind, klicken Sie auf **[!UICONTROL Email & Done]**.

      1. (Falls erforderlich) Nehmen Sie mit dem Herausgeber Kontakt auf, um zu sehen, ob das Tag die entsprechenden Makros enthält, damit das Tag mit dem Anzeigenserver des Herausgebers funktioniert.

   * (Optional) Senden Sie die Pixel für die Ereignisverfolgung manuell an den Herausgeber:

      1. Klicken Sie in der Zeile &quot;deal&quot;in der Ansicht [!UICONTROL Deals] auf ![Menü &quot;Optionen&quot;](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         Die Ereignispixel enthalten ein [!UICONTROL Clickthrough] Pixel und ein [!UICONTROL Impression] Pixel. Video- und Audioanzeigen enthalten auch Ereignispixel nach Quartil, die abgeschlossen sind (von [!UICONTROL 25% Complete] bis [!UICONTROL 100% Complete]).

      1. Kopieren Sie die Pixel für die Ereignisverfolgung und stellen Sie sie Ihrem Herausgeber bereit.

>[!MORELIKETHIS]
>
>* [Info [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] Einstellungen](simple-deal-settings.md)
>* [Detaillierten Bericht für einen Deal anzeigen](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
