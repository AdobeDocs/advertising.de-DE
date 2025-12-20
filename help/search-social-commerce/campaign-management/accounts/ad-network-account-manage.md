---
title: Verwalten von Anzeigennetzwerkkonten
description: Erfahren Sie, wie Sie Kontodetails für ein Anzeigennetzwerkkonto einrichten und verwalten.
exl-id: 4038d03b-63e2-4953-89df-37f7b5f68652
feature: Search Campaign Management
source-git-commit: 304b3589109fe9ddf4d2f0df84c7fa45aa3726d2
workflow-type: tm+mt
source-wordcount: '2078'
ht-degree: 0%

---

# Verwalten von Anzeigennetzwerkkonten

<!-- Probably need to change the page title. If I update the filename, get B. to create a redirect to the new URL. -->

Im Folgenden finden Sie Anweisungen zum Erstellen und Bearbeiten von Details zu Werbenetzwerkkonten, zum Aktualisieren des [!DNL oAuth]-Tokens für ein Konto und zum Deaktivieren von Konten.

<!-- Move out info about Naver?  Then change to the following:  Following are instructions for creating and editing account details for an ad network account that Search, Social, & Commerce will sync using the ad network's API; refreshing the [!DNL oAuth] token for an account; and disabling accounts. -->

<!-- Also update Description metadata to "Learn how to set up and manage account details for an ad network account synced via the ad network API." -->

Einzelheiten zu den für die einzelnen Werbenetzwerke verfügbaren Funktionen finden Sie unter &quot;[Unterstützte Inventarisierung](/help/search-social-commerce/introduction/supported-inventory.md).

## Erstellen und Netzwerkkonto-Details {#create-account}

*Nur Agenturkonto-Manager, Adobe-Konto-Manager und Admin-Benutzerrollen*

Um das Synchronisieren oder Tracking eines Kontos zu aktivieren, müssen Sie einen entsprechenden Kontodatensatz mit den Anmeldedaten für den Kontozugriff und den Tracking-Optionen und mit dem Status *aktiv“*.

>[!NOTE]
>
>* Für neue [!DNL Baidu]-Konten ist kein Support verfügbar.
>* Um ein tatsächliches Konto im Werbenetzwerk zu erstellen, gehen Sie zur Website des Werbenetzwerks.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Geben Sie die [Kontoeinstellungen](#account-settings) an:

   1. Klicken Sie auf den Namen des Werbenetzwerks und dann auf **[!UICONTROL Next]**.

   1. Geben Sie im Abschnitt **[!UICONTROL Account Details]** die Kontodetails ein.

      Lassen Sie für Werbenetzwerke, die den Anmeldeautorisierungstyp &quot;[!UICONTROL oAuth]&quot; verwenden, Search, Social und Commerce mithilfe des OAuth[Autorisierungsprotokolls Zugriff auf das Konto ](https://oauth.net/2/):

      1. Geben Sie den **[!UICONTROL Login]** für das Konto ein, geben Sie optional das Kennwort ein, und klicken Sie dann auf **[!UICONTROL Authenticate]**.

         Es empfiehlt sich, die Anmelde-API für den Zugriff auf das Konto zu verwenden. Geben Sie das Kennwort ein, wenn Sie es verschlüsseln und speichern möchten, damit das Adobe-Konto-Team Token nach Bedarf aktualisieren kann.

      1. (Wenn Sie nicht beim Konto des Werbetreibenden angemeldet sind) Melden Sie sich beim Werbekonto des Werbetreibenden an. Es empfiehlt sich, die Anmeldeinformationen für den API-Zugriff auf das Konto zu verwenden.

      1. Klicken Sie im Bildschirm Berechtigungsanfrage/Zugriff auf die Schaltfläche, um die Berechtigung zu bestätigen.

      1. Kopieren Sie die Authentifizierungszeichenfolge in das sich öffnende Popup-Fenster und fügen Sie die Zeichenfolge in das Feld **[!UICONTROL oAuth Token]** ein.

      1. Geben Sie die verbleibenden Kontodetails an.

   1. Klicken Sie auf **[!UICONTROL Set Account Tracking]** und geben Sie die Tracking-Einstellungen ein.

1. Klicken Sie auf **[!UICONTROL Post]**.

   Aktuelle Kosten- und Klickdaten für alle Kampagnen im Konto sind in Search, Social und Commerce in etwa 24 Stunden verfügbar. Standardmäßig sind die Daten je nach Anzeigennetzwerk für die letzten 5 bis 10 Tage verfügbar. Bei Bedarf kann das Projektstartteam jedoch Daten für bis zu den letzten 60 Tagen abrufen.

## Details zum Anzeigen-Netzwerkkonto bearbeiten {#edit-account}

*Nur Agenturkonto-Manager, Adobe-Konto-Manager und Admin-Benutzerrollen*

Wenn sich die Kontoanmeldeinformationen ändern, die standardmäßigen Tracking-Parameter eines Kontos geändert werden sollen oder die Aktivität eines Kontos aktiviert oder deaktiviert werden soll, bearbeiten Sie die Kontodetails.

>[!NOTE]
>
>Um ein tatsächliches Konto im Werbenetzwerk zu bearbeiten, gehen Sie auf die Website des Werbenetzwerks.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Halten Sie den Cursor über den Kontonamen, klicken Sie auf ![Mehr](/help/search-social-commerce/assets/more-filters.png "Mehr") und wählen Sie dann **[!UICONTROL Edit]** aus.

1. Bearbeiten Sie die [Kontoeinstellungen](#account-settings):

   1. (Optional) Bearbeiten Sie die Kontodetails.

   1. (Optional) Klicken Sie auf **[!UICONTROL Set Account Tracking]** und bearbeiten Sie die Tracking-Einstellungen.

1. Klicken Sie auf **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >Search, Social und Commerce müssen die neuen Kontodaten mit denen im Werbenetzwerk synchronisieren. Dies geschieht automatisch einmal täglich oder häufiger, wenn Search, Social und Commerce Änderungen im Werbenetzwerk erkennt.

## OAuth-Zugriffstoken für Suchkonten aktualisieren {#refresh-oauth-tokens}

*Nur Agenturkonto-Manager, Adobe-Konto-Manager und Admin-Benutzerrollen*

Wenn Search, Social und Commerce mit dem [OAuth-Autorisierungsprotokoll](https://oauth.net/2/) auf das Konto zugreift und sich die Kontoanmeldeinformationen ändern, oder wenn zusätzlicher Zugriff erforderlich ist, um neue Funktionen in Search, Social und Commerce zu unterstützen, müssen Sie ein neues Zugriffstoken für das Konto abrufen.

Ihr Adobe-Konto-Team wird Sie informieren, wenn neue Funktionen ein neues Token erfordern.

1. (Wenn Sie in einem anderen Konto für dasselbe Werbenetzwerk in derselben Browser-Anwendung angemeldet sind) Melden Sie sich von einem anderen Konto als dem des Werbetreibenden ab.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Halten Sie den Cursor über den Kontonamen, klicken Sie auf ![Mehr](/help/search-social-commerce/assets/more-filters.png "Mehr") und wählen Sie dann **[!UICONTROL Edit]** aus.

1. Abrufen eines neuen Zugriffs-Tokens:

   1. Klicken Sie auf **[!UICONTROL Get oAuth Token]**.

   1. (Wenn Sie nicht beim Konto des Werbetreibenden angemeldet sind) Melden Sie sich beim Werbekonto des Werbetreibenden an. Es empfiehlt sich, die Anmeldeinformationen für den API-Zugriff auf das Konto zu verwenden.

   1. Klicken Sie im Bildschirm Berechtigungsanfrage/Zugriff auf die Schaltfläche, um die Berechtigung zu bestätigen.

   1. Kopieren Sie die Authentifizierungszeichenfolge in das sich öffnende Popup-Fenster und fügen Sie die Zeichenfolge in das Feld **[!UICONTROL oAuth Token]** ein.

1. Klicken Sie auf **[!UICONTROL Post]**.

## Aktivieren oder Deaktivieren von Anzeigennetzwerkkonten {#enable-disable-account}

*Nur Agenturkonto-Manager, Adobe-Konto-Manager und Admin-Benutzerrollen*

Wenn Sie ein Anzeigennetzwerkkonto aktivieren, synchronisiert Search, Social und Commerce Kampagnendaten mit dem Konto (falls unterstützt) und pusht automatisierte Gebote und/oder Kampagnenbudgets für Kampagnen in Portfolios. Wenn Sie ein Anzeigennetzwerkkonto deaktivieren, stoppt Search, Social und Commerce alle Aktivitäten im Konto. Daten, die erfasst wurden, während das Konto aktiv war, werden weiterhin gespeichert, aber die Kampagnenverwaltungsansichten und -berichte enthalten keine Daten für den Zeitraum, in dem das Konto deaktiviert ist. Sie können das Konto später erneut aktivieren, um die Aktivität mit dem Konto fortzusetzen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Führen Sie einen der folgenden Schritte aus:

   * (Um den Status für ein einzelnes Konto zu ändern) Halten Sie den Cursor über den Kontonamen, klicken Sie auf ![Mehr](/help/search-social-commerce/assets/more-filters.png "Mehr") und wählen Sie dann **[!UICONTROL Edit]** aus. Ändern Sie die **[!UICONTROL Status]** in *Aktiviert* oder *Deaktiviert* und klicken Sie dann auf **[!UICONTROL Post]**.

   * (So ändern Sie den Status für ein oder mehrere Konten:

      1. Aktivieren Sie das Kontrollkästchen neben jedem Konto.

         Tipps zum Auswählen mehrerer Zeilen finden Sie unter [Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).

      1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Symbol aktivieren](/help/search-social-commerce/assets/activate.png "Symbol aktivieren"), um das Konto zu aktivieren, oder ![Symbol deaktivieren](/help/search-social-commerce/assets/disable.png "Symbol deaktivieren"), um das Konto zu deaktivieren.

## Einstellungen für Netzwerkkonto hinzufügen {#account-settings}

>[!NOTE]
>
>Nur Benutzerinnen und Benutzer von Agency Account Manager, [!DNL Adobe] Account Manager und Admins können Kontoeinstellungen konfigurieren.

### Kontodetails

**[!UICONTROL SE Account ID]:** (Alle Konten außer [!DNL Naver] und [!DNL Yandex] Konten; nur für neue Konten bearbeitbar) Die vom Werbenetzwerk zugewiesene Konto-ID.

>[!NOTE]
>
>Ad-Network-Manager-Konten werden hier nicht unterstützt. Um ein Manager-Konto für [!DNL Microsoft Advertising] oder [!DNL Yandex] zu identifizieren, verwenden Sie das Feld Master-Konto-ID bzw. MCC-Konto . Um [Anmeldeinformationen für ein [!DNL Google Ads] Manager-Konto einzurichten](/help/search-social-commerce/admin/manager-accounts.md), gehen Sie zu [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** Der Name, der für das Konto in Search, Social und Commerce angezeigt werden soll.

>[!NOTE]
>
>Wenn Sie eine Integration zwischen Search, Social und Commerce und Adobe Analytics haben und den Namen des Suchkontos ändern, bitten Sie Ihr Adobe-Accountteam, die Zuordnung zu aktualisieren.

**[!UICONTROL Login Details]: \[Login Type\]** - (nur [!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center]) Ob Anmeldungen am Konto autorisiert werden sollen mit:

* *[!UICONTROL oAuth]* (Standard): Zum Verwenden des [[!DNL OAuth] Autorisierungsprotokolls](https://oauth.net/2/).

* *[!UICONTROL Password]:* Das Kennwort des Clients verwenden.

Für [!DNL Microsoft Advertising]-Konten können nur [!DNL oAuth]-autorisierte Anmeldungen verwendet werden.

**[!UICONTROL Login Details]: [!UICONTROL Login]:** (Alle Werbenetzwerke außer [!DNL Naver]) Der Anmeldename oder die ID, um den API-Zugriff auf das Konto zu aktivieren.

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** ([!DNL Microsoft Advertising] [!DNL oAuth] und alle anderen Netzwerke außer [!DNL Meta] und [!DNL Yandex]) Das Token des Kontos, um Anmeldungen mithilfe des [[!DNL OAuth] Autorisierungsprotokolls](https://oauth.net/2/) zu autorisieren.

**[!UICONTROL Login Details]: [!UICONTROL Password]:** (Alle Werbenetzwerke außer [!DNL Naver]) Das Kennwort für das Konto. Für kennwortaktivierte Konten in [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] und [!DNL Yandex] ist dieses Feld erforderlich. Bei [!DNL oAuth]-aktivierten Konten ist dieses Feld optional. Verwenden Sie es, wenn Sie das Kennwort verschlüsseln und speichern möchten, damit der Konto-Manager Token nach Bedarf aktualisieren kann.

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** (nur [!DNL Yandex] Konten) Der Zugriffsschlüssel für das zu verwendende Entwicklerkonto.

**[!UICONTROL Currency]:** Die Abkürzung für die Währung, die für das Konto verwendet wird. Dieses Feld kann für neue [!DNL Naver] bearbeitet werden. Bei allen anderen Suchnetzwerken wird der Wert nach dem Speichern des Datensatzes automatisch mit der Währung ausgefüllt, die für das Konto im Werbenetzwerk konfiguriert wurde.

**[!UICONTROL Landing Page Suffix]** (Nur [!DNL Google Ads]- und [!DNL Microsoft Advertising]-Konten; optional) Alle Parameter, die an das Ende der endgültigen URLs angehängt werden sollen, um Informationen zu verfolgen; enthalten alle Parameter, die Ihr Unternehmen verfolgen muss.

Beispiel: `param1=value1&param2=value2`

Konten, die Adobe Advertising-Klick-Tracking verwenden, müssen die Klick-Kennung des Werbenetzwerks (`msclkid` für [!DNL Microsoft Advertising]; `gclid` für Google) im Suffix enthalten. Konten mit einer Adobe Analytics-Integration müssen den AMO ID-Parameter verwenden (beginnend mit `s_kwcid`). Wenn das Konto über eine serverseitige AMO ID-Implementierung verfügt, wird der Parameter automatisch hinzugefügt, wenn ein Benutzer auf eine Anzeige klickt. Andernfalls müssen Sie ihn hier manuell hinzufügen. Siehe die [erforderlichen Suffixformate für [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) und [erforderlichen Suffixformate für [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Dieses Feld wird von der Einstellung „Tracking [!UICONTROL Auto Upload]&quot; nicht aktualisiert.
>* Endgültige URL-Suffixe auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Zur einfacheren Wartung verwenden Sie nur das Suffix auf Kontoebene, es sei denn, eine andere Nachverfolgung für einzelne Kontokomponenten ist erforderlich. Um ein Suffix auf Anzeigengruppenebene oder darunter zu konfigurieren, verwenden Sie den Editor des Anzeigennetzwerks.

**Zeitzone:** (Alle Werbenetzwerke außer [!DNL Baidu] und [!DNL Yahoo! Display Network]) Die Zeitzone des Werbetreibenden. Dieses Feld kann bearbeitet werden und ist bei neuen [!DNL Naver] optional. Bei allen anderen Suchnetzwerken wird der Wert automatisch mit der Zeitzone ausgefüllt, die für das Konto „Suche“, „Social“ und &quot;Commerce&quot; des Werbetreibenden konfiguriert wurde, sobald der Datensatz gespeichert wird.

**Status:** Der Kontostatus in Search, Social und Commerce:

* *Aktiviert:* Search, Social und Commerce synchronisiert Kampagnendaten mit dem Konto (falls unterstützt) und sendet automatisierte Gebote und/oder Kampagnenbudgets für Kampagnen in Portfolios.
* *Deaktiviert:* Search, Social und Commerce stoppen alle Aktivitäten im Konto. Daten, die erfasst wurden, während das Konto aktiv war, werden weiterhin gespeichert, aber die Kampagnenverwaltungsansichten und -berichte enthalten keine Daten für den Zeitraum, in dem das Konto pausiert wurde. Sie können das Konto später erneut aktivieren, um die Aktivität mit dem Konto fortzusetzen.

**Tracking-Vorlage** - (Nur [!DNL Google Ads]-, [!DNL Microsoft Advertising]- und [!DNL Yahoo! Japan Ads]-Konten; optional) Die standardmäßige Tracking-Vorlage für das Konto, in der alle Weiterleitungen und Tracking-Parameter für Off-Landing-Domains angegeben und die endgültige/Landingpage-URL ebenfalls in einen Parameter eingebettet wird. Beispiel: `{lpurl}?source={network}&id=5` oder `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`, um eine Umleitung einzuschließen.

* Einbetten der endgültigen URL:

   * (Nur [!DNL Google Ads] und [!DNL Microsoft Advertising]) Eine Liste der Parameter zur Angabe der endgültigen URLs in Tracking-Vorlagen finden Sie in den Parametern (nur [!DNL Microsoft Advertising]) [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799) oder (nur [!DNL Google Ads]) den Parametern „Tracking-Vorlage nur“ im Abschnitt „Verfügbare [!DNL ValueTrack]&quot; in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348).

   * (Nur [!DNL Yahoo! Japan Ads]) Verwenden Sie den Parameter `!{lpurl}` , um die Landingpage-URL anzugeben.

* Sie können optional URL-Parameter und beliebige benutzerdefinierte Parameter einbeziehen, die für die Kampagne definiert wurden und durch kaufmännische Und-Zeichen (&amp;) getrennt sind, z. B. `{lpurl}?matchtype={matchtype}&device={device}`.

* Optional können Sie Umleitungen und Tracking von Drittanbietern hinzufügen.

* Wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; enthalten, stellt Search, Social und Commerce beim Speichern des Datensatzes automatisch seinem eigenen Umleitungs- und Trackingcode das Präfix voran.

>[!NOTE]
>
>* Vermeiden Sie [!DNL Google Ads] die Verwendung von Makros, die nicht durch Klicks aus Quellen ersetzt werden, die paralleles Tracking ermöglichen. Wenn der Werbetreibende Makros verwenden muss, sollte das Adobe-Account-Team mit dem Support oder dem Implementierungsteam zusammenarbeiten, um diese hinzuzufügen.
>* Die Tracking-Vorlage auf der detailliertesten Ebene überschreibt die Werte auf allen höheren Ebenen. Wenn beispielsweise sowohl die Kontoeinstellungen als auch die Keyword-Einstellungen einen Wert enthalten, wird der Keyword-Wert angewendet.
>* Wenn Sie eine Tracking-Vorlage auf Anzeigen-, Sitelink- oder Keyword-Ebene aktualisieren, werden die entsprechenden Anzeigen erneut zur Überprüfung eingereicht. Sie können Ihre Tracking-Vorlagen auf Konto-, Kampagnen- oder Anzeigengruppenebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.

**[!UICONTROL Master Account ID]:** (nur [!DNL Microsoft Advertising] Konten) Die ID für ein mit dem Konto verknüpftes Agentur-/Verwaltungskonto.

**[!UICONTROL MCC Account]:** (nur [!DNL Yandex] Konten; optional) Ein mit dem Konto verknüpftes Agentur-/Verwaltungskonto. Um eine vorhandene Verknüpfung zu entfernen, wählen Sie &quot;[!UICONTROL No MCC Account]&quot; aus.

**[!UICONTROL Application ID]:** (nur [!DNL Yandex] Konten) Das Entwickler-Token, das für das Konto verwendet werden soll. Dasselbe Token wird für alle [!DNL Yandex] Konten verwendet.

**[!UICONTROL Purse Campaign ID]:** (nur [!DNL Yandex] Konten mit deaktivierter Einstellung „Freigegebenes Konto“; optional) Die numerische ID für die Kampagne, mit der alle Anzeigenkampagnen im Konto bezahlt werden.

**[!UICONTROL Finance Token]:** (Nur [!DNL Yandex] Konten mit deaktivierter Einstellung „Freigegebenes Konto“; optional) Das Entwickler-Token, das für finanzbezogene API-Aufrufe verwendet wird, z. B. um Geld aus der Geldbörse zwischen den Kampagnen des Werbetreibenden neu zuzuweisen, wie es für die Portfoliooptimierung erforderlich ist.

### Account-Tracking

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (nur für [!UICONTROL EF Redirect]) Nicht implementiert

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **S_kwcid-Format:** (Bestehende [!DNL Google Ads]-Konten für Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration, für die die AMO-ID (s_kwcid) noch nicht migriert wurde)

Dieses Konto verwendet das veraltete Format für den AMO-ID-Trackingcode, mit dem Adobe Advertising Daten über das Konto mit Adobe Analytics teilen kann. Das [neueste Format](/help/integrations/analytics/ids.md#amo-id-formats) enthält Parameter für die Kampagnen-ID und die Anzeigengruppen-ID, die erforderlich sind, um für Kampagnen, Entwürfe und Experimente mit [!DNL Google Ads] in Analytics präzise Berichte auf Kampagnen- und Anzeigengruppenebene zu erstellen:

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

Wenn dieses Konto einen Bericht auf Kampagnen- und Anzeigengruppenebene erstellen muss, klicken Sie auf das [!UICONTROL Edit] (Stiftsymbol) und dann auf **[!UICONTROL Migrate to new s_kwcid format]**, um zum neuen Format zu wechseln. Für Konten, die diese Kampagnentypen nicht enthalten, ist die Migration zum neuen Format optional, wird aber empfohlen.

Vollständige Anweisungen finden Sie unter &quot;[Aktualisieren des AMO-ID-Trackingcodes für ein  [!DNL Google Ads] -Konto](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).

**Report Suite-Namen:** (Nur für EF-Umleitung mit Token; Werbetreibende mit einer Adobe Advertising-Adobe Analytics-Integration; optional) Eine oder mehrere Analytics-Report Suites, an die Search, Social und Commerce Daten senden, die sie aus dem Werbenetzwerk erfasst, einschließlich Entitätsklassifizierungen und Klickdaten für das Konto. Diese Funktion steht nur unterstützten Werbenetzwerken zur Verfügung.

Damit die Daten in den Report Suites angezeigt werden, muss entweder (a) die Server-seitige AMO-ID-Funktion für das Konto konfiguriert sein oder (b) die Einstellung auf Advertiser-Ebene auf &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; aktiviert sein. Darüber hinaus muss das Analytics-Konto des Werbetreibenden so konfiguriert sein, dass es Daten von Search, Social und Commerce empfängt. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

>[!MORELIKETHIS]
>
>* [Über Werbenetzwerkkonten](ad-network-account-about.md)
>* [Konten des Händlerzentrums verwalten](merchant-account-manage.md)
>* [Aktualisieren des s_kwcid-Trackingcodes für ein [!DNL Google Ads] Konto](update-amo-id-google.md)
