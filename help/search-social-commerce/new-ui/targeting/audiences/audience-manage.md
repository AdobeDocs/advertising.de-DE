---
title: Verwalten von Audiences
description: Erfahren Sie mehr über die Zielgruppenbibliothek und darüber, wie Sie unterstützte Zielgruppen für Google Ads und Microsoft Advertising verwalten.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 7e7dcde9fb195e04025a1a8d89e792ff562b053f
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 0%
---
# Verwalten von Audiences

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising] Konten*

Eine Zielgruppe ist eine Benutzergruppe, die Sie als [Ziel](audience-targets-manage.md) oder [Ausschluss](audience-exclusions.md) für unterstützte Kampagnen und Anzeigengruppen im selben Werbenetzwerk verwenden können. Das Anzeigennetzwerk bestimmt, wie groß eine Zielgruppe sein muss, um anvisiert zu werden.

## Über die [!UICONTROL Library] {#audience-view-about}

Die Ansicht [!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Library] listet die Zielgruppen für den ausgewählten Advertiser auf. Um [!DNL Google Ads] und [!DNL Microsoft Advertising] Zielgruppen anzuzeigen, wählen Sie **[!UICONTROL All Other Network]** aus dem **[!UICONTROL Network]**.

Die Bibliothek umfasst [!DNL Google Ads] kundendatenbasierte, marktinterne und ähnliche Zielgruppen sowie [!DNL Microsoft Advertising] Remarketing, dynamisches Remarketing, benutzerdefiniert, Kundenabstimmung, marktinterne und ähnliche Zielgruppen.

Zum Anzeigen der Daten ist die Berechtigung [!UICONTROL View Audiences] erforderlich. Das Auswählen von Zeilen und das Löschen unterstützter Zielgruppen erfordert die Berechtigung [!UICONTROL Edit Audience Library] .

### Verfügbare Aktionen

<!--
Restricted to internal beta users:

* [Create a customer match audience from a customer data list](#audience-customer-list-create)

* [Create a Google Ads audience from Adobe audiences](#audience-adobe-create)

* [Create a Microsoft Advertising dynamic remarketing audience](#audience-dynamic-create)

* [Update a customer match audience using a customer data list](#audience-customer-list-edit)

* [Edit a dynamic remarketing audience](#audience-dynamic-edit)
-->

* [Löschen einer dynamischen Remarketing-Zielgruppe](#audience-delete)

* [Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren](#copy-to-clipboard)

## Zielgruppen-Datenquellen {#audience-data-sources}

Sie können Audiences verwenden, die auf den folgenden Datenquellen basieren:

* **Adobe-Zielgruppensegmente:** Werbetreibende mit angemeldeten Adobe Audience Manager- oder Adobe Analytics-Konten können [!DNL Google Ads] Zielgruppen für den Kundenabgleich basierend auf ihren bestehenden [!DNL Adobe] verwenden.

  * Für Werbetreibende mit [!DNL Analytics], die nicht auch über Audience Manager verfügen, verwenden die Zielgruppen Benutzer-IDs aus [!DNL Analytics] Segmenten, die mit Adobe CX Enterprise freigegeben wurden.

  * Für Werbetreibende mit Audience Manager-Konten verwenden die Zielgruppen Benutzer-IDs aus Audience Manager-Segmenten, die Search, Social und Commerce als Ziel haben. Dazu können [!DNL Analytics] in Adobe CX Enterprise veröffentlichte Segmente und Segmente gehören, die mit der Adobe CX Enterprise-Zielgruppenbibliothek erstellt wurden.

  Das [!DNL Google Ads]-Konto muss [für den Kundenabgleich infrage kommen](https://support.google.com/adspolicy/answer/6299717) und für [Benutzer-ID-Segmente“ &#x200B;](https://support.google.com/google-ads/answer/9199250). Das Advertiser-Konto in Search, Social und Commerce muss ebenfalls so konfiguriert sein, dass Zielgruppen für den Kundenabgleich erstellt werden können. Wenden Sie sich an Ihr Adobe-Accountteam , um die Funktion zu aktivieren.

  [!DNL Adobe] Segmentdaten und Cookie-Synchronisierungsdateien für kundendatenbasierte Zielgruppen werden täglich mit [!DNL Google Ads] synchronisiert.

* **Adobe Campaign-E-Mail-Listen:** Ihr Adobe-Accountteam kann Sie beim Einrichten eines Workflows unterstützen, um eine Zielgruppe für den [!DNL Google Ads]-Kundenabgleich aus einer E-Mail-Liste in [!DNL Campaign] zu erstellen und zu aktualisieren. Der Workflow wird in [!DNL Campaign] konfiguriert, nicht in der Zielgruppenbibliothek. Siehe [Erstellen einer Zielgruppe für den Kundenabgleich aus einer Adobe Campaign-E-Mail-Liste](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md)&quot;.

* **Kundendatenlisten:** Werbetreibende mit berechtigten [!DNL Google Ads]- oder [!DNL Microsoft Advertising]-Konten können Zielgruppen für den Kundenabgleich verwenden, die auf CSV-Dateien basieren, die primäre Kennungen aus ihren CRM-Systemen (Customer Relationship Management) enthalten.

* **Dynamische Remarketing-Listen:** Werbetreibende mit [!DNL Microsoft Advertising]-Konten können Zielgruppen verwenden, die auf Benutzenden basieren, die kürzlich mit ihren Produkten interagiert haben, z. B. Produkt-Viewer oder frühere Käufer. Für diese Zielgruppen ist das JavaScript-Konversions- und Zielgruppen-Tracking-Tag des Werbenetzwerks auf den entsprechenden Web-Seiten erforderlich.

  Dynamische Remarketing-Zielgruppen können mit Shopping-Kampagnen in den Such- und Zielgruppennetzwerken verwendet werden, um Benutzende mit Produktanzeigen erneut anzusprechen, und mit Suchkampagnen, um Benutzende mit Textanzeigen und dynamischen Suchanzeigen erneut anzusprechen.

  >[!NOTE]
  >
  >Angebotsmodifikatoren für dynamische Remarketing-Audience-Ziele werden in Portfolios mit der Einstellung [!UICONTROL Auto-optimize Bid Adjustment Values] nicht optimiert.

>[!NOTE]
>
>Search, Social und Commerce speichern keine Kundendaten, die Sie hochladen, oder Kundendaten aus [!DNL Adobe] Segmenten, die zum Erstellen oder Bearbeiten einer Zielgruppe verwendet werden.

<!--
Restricted to internal beta users: audience creation and library editing.

## Create a customer match audience from a customer data list {#audience-customer-list-create}

*[!DNL Google Ads] and [!DNL Microsoft Advertising] accounts that are eligible for customer match only*

For [!DNL Microsoft Advertising], the file can include email addresses. For [!DNL Google Ads], the file can include email addresses, mailing addresses, telephone numbers, user IDs, or mobile device IDs.

Creating and editing library audiences requires the [!UICONTROL Edit Audience Library] permission in addition to internal beta access.

1. Prepare a CSV file with the customer data in the required format.

   First and last names, email addresses, and telephone numbers must be hashed using SHA-256. Follow the network's formatting requirements for the selected identifier type. See the [Google Ads formatting guidelines](https://support.google.com/google-ads/answer/7476159) or the [Microsoft Advertising instructions for preparing customer match lists](https://help.ads.microsoft.com/#apex/ads/en/56921).

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. In **[!UICONTROL Data Source]**, select the customer-list option.

1. Enter the **[!UICONTROL Audience Name]** and select the **[!UICONTROL Data Upload Type]**:

   * ([!DNL Microsoft Advertising]) **[!UICONTROL Emails]**.

   * ([!DNL Google Ads]) **[!UICONTROL Emails, Phones, and/or Mailing Addresses]**, **[!UICONTROL User IDs]**, or **[!UICONTROL Mobile Device IDs]**.

     User ID lists are available only to eligible [!DNL Google Ads] advertisers in the U.S. who are opted in for user ID segments.

1. (Mobile device ID lists only) Select the **[!UICONTROL OS Type]** and enter the **[!UICONTROL App ID]**.

   For an Android app, use its package name in [!DNL Google Play], such as `com.example.game` from `https://play.google.com/store/apps/details?id=com.example.game`. For an iOS app, use its application ID from the [!DNL App Store], such as `id284882215`. Your development team can provide the ID.

1. In **[!UICONTROL Select File]**, select the CSV file from your device or network.

1. Select the check box to indicate that you agree with the [!DNL Adobe] and ad network privacy policies.

1. ([!DNL Google Ads]; optional) If you do business in the European Economic Area (EEA) or United Kingdom (UK) and have collected all required user consents, select the consent check box to send the consent status as **[!UICONTROL GRANTED]** for advertising and ad personalization.

   If you leave the check box unselected, the consent status is sent as **[!UICONTROL UNSPECIFIED]**. [!DNL Google Ads] ignores data for EEA and UK users with an unspecified consent status, which can cause data discrepancies and performance issues.

1. Click **[!UICONTROL Upload File]** and wait for the upload to finish.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available.

   Membership days specify how long a user's cookie stays in the audience. Use the length of time for which you expect the ad to remain relevant. Customer lists don't expire unless you enter a value.

1. Click **[!UICONTROL Review and Save]**.

1. Review the settings. To change a setting, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

The ad network may take up to 24 hours to process the file. See the [Google Ads documentation on customer match and its limitations](https://support.google.com/displayvideo/answer/9539301).

## Create Google Ads customer match audiences from Adobe audiences {#audience-adobe-create}

*Advertisers with an Adobe Advertising-Adobe Audience Manager or Adobe Advertising-Adobe Analytics integration only*

Each [!DNL Adobe] audience can be used for only one [!DNL Google Ads] audience. Each new audience has the same name as the original [!DNL Adobe] audience.

1. Complete the prerequisites:

   1. Ask an [!DNL Adobe] administrator or account manager to enable customer match audiences for the advertiser.

   1. Implement the [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html){target="_blank"} version 2.0 or higher.

   1. Deploy the following tag as high as possible on the advertiser's webpages from which the audience should be tracked:

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      Replace `Advertising_Cloud_UserID` with the advertiser's unique numeric user ID.

   1. Have an authorized user [configure synchronization with the advertiser's organization account in Adobe CX Enterprise](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu, and then click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select [!DNL Google Ads] and the account.

1. In **[!UICONTROL Data Source]**, select the Adobe audience option.

1. In **[!UICONTROL Adobe Audience]**, select one or more available segments. You can search the list.

   Segments already used for another [!DNL Google Ads] audience aren't available. If you select multiple segments, a separate audience is created for each segment.

1. Select the available customer list user ID option in **[!UICONTROL Audience Type]**.

1. Select the check box to indicate that you agree with the [!DNL Adobe] and ad network privacy policies.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available.

   Remarketing lists have a maximum duration of 540 days. Customer lists don't have a maximum duration; enter 10000 to indicate that the cookie never expires.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Create]**.

Search, Social, & Commerce automatically pushes a [!DNL Google] tracking URL back to each source segment so that [!DNL Google] can track the audience. [!DNL Google] may take up to 24 hours to process the audience.

>[!TIP]
>
>For real-time segmentation, use Audience Manager-created audiences. [!DNL Analytics] segments synced to Adobe CX Enterprise may have smaller populations because they're synced daily. Users who qualify for a segment may not be included until the next day.

## Create a Microsoft Advertising dynamic remarketing audience {#audience-dynamic-create}

You can create multiple dynamic remarketing audiences using the same tracking tag.

1. Implement the [Microsoft Advertising universal event tracking (UET) tag with the required product ID and page type parameters](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85) on the relevant webpages. Identify the tag's name.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu, and then click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select [!DNL Microsoft Advertising] and the account.

1. In **[!UICONTROL Data Source]**, select the dynamic remarketing list option.

1. Enter the **[!UICONTROL Audience Name]**.

1. In **[!UICONTROL Tag Name]**, select the UET tag on the webpages whose users comprise the audience.

1. In **[!UICONTROL Whom to add to your audience]**, select **[!UICONTROL General Visitors]**, **[!UICONTROL Product Searchers]**, **[!UICONTROL Product Viewers]**, **[!UICONTROL Past Buyers]**, or **[!UICONTROL Shopping Cart Abandoners]**.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available. For dynamic remarketing audiences, membership can range from 1-180 days.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Create]**.

Dynamic remarketing audiences are eligible for targeting once they include at least 300 users.

## Update a customer match audience using a customer data list {#audience-customer-list-edit}

You can update customer match audiences created from data files, but not [!DNL Google Ads] audiences created from [!DNL Adobe] audiences. You can add or delete members, or replace all existing members. You can't edit multiple library audiences at once.

1. Prepare a CSV file in the required format, using the same data type as the original list. For mobile device IDs, use the same app and operating system.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Select the check box next to one audience, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

1. In **[!UICONTROL Select Action]**, select:

   * **[!UICONTROL Add]:** Add members from the uploaded file who aren't already in the audience.

   * **[!UICONTROL Delete]:** Remove members in the uploaded file from the audience.

   * **[!UICONTROL Replace]:** Replace all existing audience members with the uploaded data.

1. In **[!UICONTROL Select File]**, select the CSV file, accept the privacy policies, and configure the applicable consent setting.

1. Click **[!UICONTROL Upload File]** and wait for the upload to finish.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Update]**.

The ad network may take a while to process audience updates.

## Edit a dynamic remarketing audience {#audience-dynamic-edit}

You can change a [!DNL Microsoft Advertising] dynamic remarketing audience's name, UET tag, and visitor type. You can't change its membership duration or edit multiple library audiences at once.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Select the check box next to one dynamic remarketing audience, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

1. Edit the **[!UICONTROL Audience Name]**, **[!UICONTROL Tag Name]**, or **[!UICONTROL Whom to add to your audience]**.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Update]**.
-->

## Löschen einer dynamischen Remarketing-Zielgruppe {#audience-delete}

Sie können [!DNL Microsoft Advertising] dynamische Remarketing-Zielgruppen einzeln löschen. Sie können keine anderen [!DNL Google Ads] oder [!DNL Microsoft Advertising] Zielgruppentypen aus der Bibliothek löschen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Targeting]>[!UICONTROL Audiences]**, und klicken Sie dann auf die Registerkarte **[!UICONTROL Library]** .

1. Wählen Sie im Menü **[!UICONTROL Network]** die Option **[!UICONTROL All Other Network]** aus.

1. Aktivieren Sie das Kontrollkästchen neben einer dynamischen Remarketing-Audience.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

## Alle Daten in ausgewählten Zeilen in die Zwischenablage kopieren {#copy-to-clipboard}

Kopieren Sie die sichtbaren Informationen in die ausgewählten Zeilen entsprechend den angewendeten Filtern und Spalten, die in der Ansicht sichtbar sind. Die Informationen werden als tabulatorgetrennte Werte (TSV) gespeichert.

1. Aktivieren Sie das Kontrollkästchen neben jeder Zeile, deren Daten Sie kopieren möchten.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Copy]**.

>[!MORELIKETHIS]
>
>* [Verwalten von Zielgruppenzielen für Kampagnen und Anzeigengruppen](audience-targets-manage.md)
>* [Verwalten von Zielgruppenausschlüssen für Kampagnen und Anzeigengruppen](audience-exclusions.md)
