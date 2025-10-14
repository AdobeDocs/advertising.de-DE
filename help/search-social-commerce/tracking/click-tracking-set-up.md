---
title: Einrichten von Cookie-basiertem Klick-Tracking
description: Erfahren Sie, wie Sie Klick-Tracking-Tags einrichten und validieren.
exl-id: 3f2b09bc-9794-41d1-89fc-0d239bad2fb1
feature: Search Tracking
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Einrichten von Cookie-basiertem Klick-Tracking

Für Search, Social und Commerce müssen die folgenden Elemente konfiguriert und validiert werden, um Klicks zu verfolgen.

1. (Adobe-Konto-Team) Richten Sie den Advertiser als Pixel-Kunde ein.

1. [Geben Sie die richtigen Tracking-Optionen für die einzelnen Konten und Kampagnen des Werbenetzwerks des Werbetreibenden an](#set-up-click-tracking-options).

1. Generieren [&#x200B; bei Bedarf Tracking-URLs und laden Sie sie &#x200B;](#generate-upload-tracking-urls) einige Kampagnenelemente hoch.

1. [Validieren Sie das Format einiger Klick-Tracking-URLs und testen Sie sie, um sicherzustellen, dass die richtige Landingpage geöffnet wird](#validate-tracking-urls).

## Einrichten von Tracking-Optionen für Werbenetzwerkkonten und -kampagnen {#set-up-click-tracking-options}

*Nur Agenturkonto-Manager, [!DNL Adobe]-Account-Manager und Admin-Benutzerrollen*

1. Gehen Sie für jedes Anzeigennetzwerkkonto wie folgt vor:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]>[!UICONTROL Accounts]**.

   1. Halten Sie den Cursor über den Kontonamen, klicken Sie auf ![Menüsymbol](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menüsymbol") und wählen Sie dann **[!UICONTROL Edit]** aus.

   1. Klicken Sie auf **[!UICONTROL Set Account Tracking]**.

   1. Wählen Sie als [!UICONTROL Tracking Type] die Option **[!UICONTROL EF Redirect]** aus.

   1. (Damit Search, Social und Commerce Daten mit Adobe Analytics austauschen oder Konversionen verfolgen können, die in [!DNL Apple Safari] auftreten) Wählen Sie die [!UICONTROL Redirect Type] Option **[!UICONTROL Token]**.

   1. (Optional) Aktivieren Sie die Option &quot;**[!UICONTROL Auto Upload]**&quot;, um neue Tracking-URLs automatisch in das Werbenetzwerk hochzuladen, wenn Search, Social und Commerce das nächste Mal damit synchronisiert werden. Dieser Wert wird als Standard für alle Kampagnen im Konto übernommen, kann jedoch auf Kampagnenebene überschrieben werden.

1. Gehen Sie für jede Kampagne wie folgt vor:

   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klicken Sie in den Untermenüs auf **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

   1. Halten Sie den Cursor über den Kampagnennamen, klicken Sie auf ![Menüsymbol](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Menüsymbol") und wählen Sie dann **[!UICONTROL Edit]**.

   1. Klicken Sie auf **[!UICONTROL Set Campaign Tracking]**. Wählen Sie dann die zu **[!UICONTROL Override Account Tracking]** Option aus.

   1. Wählen Sie als [!UICONTROL Tracking Type] die Option **[!UICONTROL EF Redirect]** aus.

   1. (Damit Search, Social und Commerce Daten mit Adobe Analytics austauschen oder Konversionen verfolgen können, die in [!DNL Apple Safari] auftreten) Wählen Sie die [!UICONTROL Redirect Type] Option **[!UICONTROL Token]**.

   1. (Optional) Aktivieren Sie die Option &quot;**[!UICONTROL Auto Upload]**&quot;, um neue Tracking-URLs automatisch in das Werbenetzwerk hochzuladen, wenn Search, Social und Commerce das nächste Mal damit synchronisiert werden. Dieser Wert wird als Standard für alle Kampagnen im Konto übernommen, kann jedoch auf Kampagnenebene überschrieben werden.

## Tracking-URLs generieren und hochladen {#generate-upload-tracking-urls}

Siehe &quot;[&#x200B; und Generieren von Klick-Tracking-URLs](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)&quot;.

### Testen des Formats von Klick-Tracking-URLs {#validate-tracking-urls}

Überprüfen Sie, ob die richtige Landingpage für die Klick-Tracking-URL geöffnet wird.

1. Nachahmen eines Anzeigenklicks, indem Traffic an die Staging-Umgebung des Werbetreibenden gesendet wird:

   1. Fügen Sie in einem Texteditor eine Klick-Tracking-URL ein, ändern Sie die Landingpage-URL so, dass sie in der Staging-Umgebung des Werbetreibenden auf dieselbe Seite verweist, und fügen Sie dann die neue URL in die Adressleiste Ihres Browsers ein, und drücken Sie die **[!DNL Enter]**.

   1. Suchen Sie nach dem Cookie in den gespeicherten Cookies Ihres Browsers.

   1. Schließen Sie eine Transaktion auf der Staging-Site ab und überprüfen Sie, ob die Erfolgsseite das richtige Pixel auslöst. Die tatsächlich vom Pixel verfolgten Parameter variieren je nach Advertiser und Tracking-URL. Im folgenden Beispiel möchte der Werbetreibende die Anzahl der neuen Anwendungen und die Höhe des neuen Umsatzes verfolgen:

      Für einen neuen Endbenutzer (mit einem neuen Cookie) sollte das folgende Pixel ausgelöst werden:

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      Wenn das Cookie nicht neu ist, sollte das folgende Pixel ausgelöst werden:

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. Wiederholen Sie den Vorgang für mehrere Klick-Tracking-URLs in der Domain.

1. Wiederholen Sie Schritt 1 für jede Domain und verwenden Sie entsprechend eine andere Landingpage.

1. Bestätigen Sie bei Bedarf, dass Search, Social und Commerce die Pixel für die während des Tests generierten Transaktions-IDs (`ev_transid`) sehen können.

>[!MORELIKETHIS]
>
>* [Wann und wie Sie Klick-Tracking-URLs generieren](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
