---
title: Einrichten des Cookie-basierten Klick-Trackings
description: Erfahren Sie, wie Sie Klick-Tracking-Tags einrichten und validieren.
exl-id: 3f2b09bc-9794-41d1-89fc-0d239bad2fb1
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Einrichten des Cookie-basierten Klick-Trackings

Damit Sie Klicks in Search, Social und Commerce verfolgen können, müssen die folgenden Elemente konfiguriert und validiert werden.

1. (Adobe Account Team) Richten Sie den Advertiser als Pixelkunde ein.

1. [Legen Sie die richtigen Tracking-Optionen für die Anzeigennetzwerkkonten und -kampagnen des Advertisers fest](#set-up-click-tracking-options).

1. Falls erforderlich, generieren Sie Tracking-URLs und laden Sie sie](#generate-upload-tracking-urls) für einige Kampagnenelemente hoch.[

1. [Validieren Sie das Format einiger Klick-Tracking-URLs und testen Sie sie, um zu überprüfen, ob die richtige Landingpage geöffnet wird.](#validate-tracking-urls)

## Tracking-Optionen für Anzeigennetzwerkkonten und -kampagnen einrichten {#set-up-click-tracking-options}

*Nur Agentur-Kundenbetreuer, [!DNL Adobe] -Kundenbetreuer und Administrator-Benutzerrollen*

1. Gehen Sie für jedes Anzeigennetzwerkkonto wie folgt vor:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]>[!UICONTROL Accounts]**.

   1. Halten Sie den Cursor über den Kontonamen, klicken Sie auf das Symbol ![Menü-Symbol](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menü-Symbol") und wählen Sie dann **[!UICONTROL Edit]** aus.

   1. Klicken Sie auf **[!UICONTROL Set Account Tracking]**.

   1. Wählen Sie für die Einstellung &quot;[!UICONTROL Tracking Type]&quot;den Wert &quot;**[!UICONTROL EF Redirect]**&quot;.

   1. (Damit Search, Social und Commerce Daten mit Adobe Analytics austauschen oder Konversionen verfolgen können, die in [!DNL Apple Safari] auftreten) Wählen Sie die Option [!UICONTROL Redirect Type] aus. **[!UICONTROL Token]**

   1. (Optional) Aktivieren Sie die Option &quot;**[!UICONTROL Auto Upload]**&quot;, um beim nächsten Synchronisieren von Search, Social und Commerce automatisch neue Tracking-URLs in das Werbenetzwerk hochzuladen. Dieser Wert wird als Standard für alle Kampagnen im Konto übernommen, kann jedoch auf Kampagnenebene überschrieben werden.

1. Gehen Sie für jede Kampagne wie folgt vor:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

   1. Halten Sie den Cursor über den Kampagnennamen, klicken Sie auf das Symbol ![Menü-Symbol](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menü-Symbol") und wählen Sie dann **[!UICONTROL Edit]** aus.

   1. Klicken Sie auf **[!UICONTROL Set Campaign Tracking]**. Wählen Sie dann die Option &quot;**[!UICONTROL Override Account Tracking]**&quot;.

   1. Wählen Sie für die Einstellung &quot;[!UICONTROL Tracking Type]&quot;den Wert &quot;**[!UICONTROL EF Redirect]**&quot;.

   1. (Damit Search, Social und Commerce Daten mit Adobe Analytics austauschen oder Konversionen verfolgen können, die in [!DNL Apple Safari] auftreten) Wählen Sie die Option [!UICONTROL Redirect Type] aus. **[!UICONTROL Token]**

   1. (Optional) Aktivieren Sie die Option &quot;**[!UICONTROL Auto Upload]**&quot;, um beim nächsten Synchronisieren von Search, Social und Commerce automatisch neue Tracking-URLs in das Werbenetzwerk hochzuladen. Dieser Wert wird als Standard für alle Kampagnen im Konto übernommen, kann jedoch auf Kampagnenebene überschrieben werden.

## Tracking-URLs generieren und hochladen {#generate-upload-tracking-urls}

Siehe &quot;[Wann und wie Klick-Tracking-URLs generiert werden](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)&quot;.

### Testen des Formats von Klick-Tracking-URLs {#validate-tracking-urls}

Überprüfen Sie, ob die richtige Landingpage für die Klick-Tracking-URL geöffnet wird.

1. Sie können einen Anzeigenklick imitieren, indem Sie Traffic an die Staging-Umgebung des Advertisers senden:

   1. Fügen Sie in einem Texteditor eine Klick-Tracking-URL ein, ändern Sie die URL der Landingpage so, dass sie innerhalb der Staging-Umgebung des Advertisers auf dieselbe Seite verweist, fügen Sie dann die neue URL in die Adressleiste Ihres Browsers ein und drücken Sie die Taste **[!DNL Enter]** .

   1. Suchen Sie in den gespeicherten Cookies Ihres Browsers nach dem Cookie.

   1. Schließen Sie eine Transaktion auf der Staging-Site ab und überprüfen Sie, ob die Erfolgsseite das richtige Pixel auslöst. Die tatsächlichen Parameter, die vom Pixel verfolgt werden, variieren je nach Advertiser und Tracking-URL. Im folgenden Beispiel möchte der Werbetreibende die Anzahl neuer Anwendungen und den Umfang des neuen Umsatzes verfolgen:

      Für einen neuen Endbenutzer (mit einem neuen Cookie) sollte das folgende Pixel ausgelöst werden:

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      Wenn das Cookie nicht frisch ist, sollte das folgende Pixel ausgelöst werden:

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. Wiederholen Sie diesen Vorgang für mehrere Klick-Tracking-URLs in der Domäne.

1. Wiederholen Sie Schritt 1 für jede Domäne und verwenden Sie entsprechend eine andere Landingpage.

1. Bestätigen Sie bei Bedarf, dass in Search, Social und Commerce die Pixel für die während des Tests generierten Transaktions-IDs (`ev_transid`) angezeigt werden.

>[!MORELIKETHIS]
>
>* [Wann und wie Klick-Tracking-URLs generiert werden](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
