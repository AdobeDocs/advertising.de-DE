---
title: Verwalten von Anzeigen-Netzwerkkonten
description: Erfahren Sie, wie Sie Kontodetails für ein Anzeigennetzwerkkonto einrichten und verwalten.
exl-id: fd8b38bd-24d0-488c-9e57-a516f5ae67ac
feature: Search Campaign Management
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '2086'
ht-degree: 0%

---

# Verwalten von Anzeigen-Netzwerkkonten

Im Folgenden finden Sie Anweisungen zum Erstellen und Bearbeiten von Kontodetails für Anzeigen und Netzwerke, und aktualisieren Sie die [!DNL oAuth] Token für ein Konto und Deaktivieren von Konten.

## Erstellen von Details zum Anzeigennetzkonto {#create-account}

*Nur für Adobe Account Manager,  Account Manager und Administratorbenutzer*

Um die Synchronisierung oder Verfolgung eines Kontos zu aktivieren, müssen Sie einen entsprechenden Kontodatensatz mit den Kontozugriffsberechtigungen und Tracking-Optionen sowie dem Status erstellen *active*. Weitere Informationen zu den für jedes Anzeigennetzwerk verfügbaren Funktionen finden Sie unter[Unterstützter Bestand](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

>[!NOTE]
>
>Um ein tatsächliches Konto im Werbenetzwerk zu erstellen, rufen Sie die Website des Werbenetzwerks auf.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Erstellen](/help/search-social-commerce/assets/add.png "Erstellen").

1. Geben Sie die [Kontoeinstellungen](#account-settings):

   1. Klicken Sie auf den Namen des Werbenetzwerks und dann auf **[!UICONTROL Next]**.

   1. Im **[!UICONTROL Account Details]** Geben Sie die Kontodetails ein.

      Für Werbenetzwerke, die den Anmelde-Autorisierungstyp verwenden:[!UICONTROL oAuth],&quot; erlauben Sie Search, Social und Commerce, auf das Konto mit der [OAuth-Autorisierungsprotokoll](https://oauth.net/2/):

      1. Geben Sie die **[!UICONTROL Login]** -Wert für das Konto, geben Sie optional das Kennwort ein und klicken Sie auf **[!UICONTROL Authenticate]**.

         Es empfiehlt sich, die -Anmeldung für den API-Zugriff auf das Konto zu verwenden. Geben Sie das Kennwort ein, wenn Sie es verschlüsseln und speichern möchten, damit das Adobe Account Team Token nach Bedarf aktualisieren kann.

      1. (Wenn Sie nicht im Konto des Werbetreibenden angemeldet sind) Melden Sie sich beim Anzeigenkonto des Werbetreibenden an. Es empfiehlt sich, die Anmeldeinformationen für den API-Zugriff auf das Konto zu verwenden.

      1. Klicken Sie im Bildschirm &quot;Berechtigungsanfrage/Zugriff&quot;auf die Schaltfläche , um die Berechtigung zu bestätigen.

      1. Kopieren Sie die Authentifizierungszeichenfolge im sich öffnenden Popup-Fenster und fügen Sie die Zeichenfolge in das **[!UICONTROL oAuth Token]** -Feld.

      1. Geben Sie die restlichen Kontodetails an.

   1. Klicks **[!UICONTROL Set Account Tracking]** und geben Sie die Tracking-Einstellungen ein.

1. Klicken **[!UICONTROL Post]**.

   Aktuelle Kosten- und Klickdaten für alle Kampagnen in dem Konto sind in Search, Social und Commerce in etwa 24 Stunden verfügbar. Je nach Werbenetzwerk sind die Daten standardmäßig für die letzten 5-10 Tage verfügbar. Bei Bedarf kann das Projekt-Launch-Team jedoch Daten für die letzten 60 Tage abrufen.

## Details zu Anzeigennetzkonten bearbeiten {#edit-account}

*Nur für Adobe Account Manager,  Account Manager und Administratorbenutzer*

Wenn sich die Kontoanmeldeinformationen ändern, möchten Sie die standardmäßigen Tracking-Parameter für ein Konto ändern oder die Aktivität für ein Konto aktivieren oder deaktivieren und dann die Kontodetails bearbeiten.

>[!NOTE]
>
>Um ein tatsächliches Konto im Werbenetzwerk zu bearbeiten, rufen Sie die Website des Werbenetzwerks auf.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Halten Sie den Cursor über den Kontonamen und klicken Sie auf ![Mehr](/help/search-social-commerce/assets/more-filters.png "Mehr")und wählen Sie **[!UICONTROL Edit]**.

1. Bearbeiten Sie die [Kontoeinstellungen](#account-settings):

   1. (Optional) Bearbeiten Sie die Kontodetails.

   1. (Optional) Klicken Sie auf **[!UICONTROL Set Account Tracking]** und bearbeiten Sie die Tracking-Einstellungen.

1. Klicken **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >Search, Social und Commerce müssen die neuen Kontodaten mit denen im Werbenetzwerk synchronisieren. Dies geschieht automatisch einmal täglich oder öfter, wenn Search, Social und Commerce Änderungen im Werbenetzwerk erkennt.

## Aktualisieren von oAuth-Zugriffstoken für Suchkonten {#refresh-oauth-tokens}

*Nur für Adobe Account Manager,  Account Manager und Administratorbenutzer*

Bei der Suche greifen Social und Commerce auf das Konto zu, das die [OAuth-Autorisierungsprotokoll](https://oauth.net/2/) und sich die Kontoanmeldeinformationen ändern oder wenn zusätzlicher Zugriff erforderlich ist, um neue Funktionen in Search, Social und Commerce zu unterstützen, müssen Sie ein neues Zugriffstoken für das Konto erhalten.

Ihr Adobe Account Team wird Sie darüber informieren, ob neue Funktionen ein neues Token erfordern.

1. (Wenn Sie in derselben Browser-Anwendung bei einem anderen Konto für dasselbe Werbenetzwerk angemeldet sind) Melden Sie sich von einem anderen Konto als dem des Werbetreibenden ab.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Halten Sie den Cursor über den Kontonamen und klicken Sie auf ![Mehr](/help/search-social-commerce/assets/more-filters.png "Mehr")und wählen Sie **[!UICONTROL Edit]**.

1. Neues Zugriffstoken abrufen:

   1. Klicken **[!UICONTROL Get oAuth Token]**.

   1. (Wenn Sie nicht im Konto des Werbetreibenden angemeldet sind) Melden Sie sich beim Anzeigenkonto des Werbetreibenden an. Es empfiehlt sich, die Anmeldeinformationen für den API-Zugriff auf das Konto zu verwenden.

   1. Klicken Sie im Bildschirm &quot;Berechtigungsanfrage/Zugriff&quot;auf die Schaltfläche , um die Berechtigung zu bestätigen.

   1. Kopieren Sie die Authentifizierungszeichenfolge im sich öffnenden Popup-Fenster und fügen Sie die Zeichenfolge in das **[!UICONTROL oAuth Token]** -Feld.

1. Klicken **[!UICONTROL Post]**.

## Anzeigen-Netzwerkkonten aktivieren oder deaktivieren {#enable-disable-account}

*Nur für Adobe Account Manager,  Account Manager und Administratorbenutzer*

Wenn Sie ein Anzeigennetzwerkkonto aktivieren, synchronisiert Search, Social und Commerce Kampagnendaten mit dem -Konto (sofern unterstützt) und überträgt automatisierte Angebote und/oder Kampagnenbudgets für Kampagnen in Portfolios. Wenn Sie ein Anzeigennetzwerkkonto deaktivieren, stoppt Search, Social und Commerce alle Aktivitäten auf dem Konto. Während der Kontoaktivität gesammelte Daten werden weiterhin gespeichert. Die Ansichten und Berichte der Kampagnenverwaltung enthalten jedoch keine Daten für den Zeitraum, in dem das Konto deaktiviert ist. Sie können das Konto später erneut aktivieren, um die Aktivität mit dem Konto wieder aufzunehmen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klicken Sie im Untermenü auf **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Führen Sie einen der folgenden Schritte aus:

   * (Um den Status für ein einzelnes Konto zu ändern) Halten Sie den Cursor über den Kontonamen, klicken Sie auf ![Mehr](/help/search-social-commerce/assets/more-filters.png "Mehr")und wählen Sie **[!UICONTROL Edit]**. Ändern Sie die **[!UICONTROL Status]** nach *Aktiviert* oder *Behinderte* und klicken Sie anschließend auf **[!UICONTROL Post]**.

   * (So ändern Sie den Status für ein oder mehrere Konten) Gehen Sie wie folgt vor:

      1. Aktivieren Sie das Kontrollkästchen neben jedem Konto.

         Tipps zur Auswahl mehrerer Zeilen finden Sie unter[Mehrere Zeilen auswählen](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Symbol &quot;Aktivieren&quot;](/help/search-social-commerce/assets/activate.png "Symbol &quot;Aktivieren&quot;") zur Aktivierung des Kontos oder ![Symbol Deaktivieren](/help/search-social-commerce/assets/disable.png "Symbol Deaktivieren") , um das Konto zu deaktivieren.

## Einstellungen für Anzeigen-Netzwerkkonten {#account-settings}

>[!NOTE]
>
>Nur Agenturkontoverwalter, [!DNL Adobe] -Kundenbetreuer und -administratoren können Kontoeinstellungen konfigurieren.

### Kontodetails

**[!UICONTROL SE Account ID]:** (Alle Konten außer [!DNL Naver] und [!DNL Yandex] Konten; nur bearbeitbar für neue Konten) Die vom Anzeigennetzwerk zugewiesene Konto-ID.

>[!NOTE]
>
>Die Ad Network Manager-Konten werden hier nicht unterstützt. So identifizieren Sie ein Managerkonto für [!DNL Microsoft Advertising] oder [!DNL Yandex]verwenden Sie das Feld Übergeordnete Konto-ID bzw. MCC-Konto . nach [Einrichten von Anmeldedaten für [!DNL Google Ads] Manager-Konto](/help/search-social-commerce/admin/manager-accounts.md), gehen Sie zu [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** Der Name, der für das Konto in Search, Social und Commerce angezeigt werden soll.

>[!NOTE]
>
>Wenn Sie über eine Integration von Search, Social, &amp; Commerce-Adobe Analytics verfügen und den Namen des Suchkontos ändern, benachrichtigen Sie das Adobe-Kontoteam, damit es die Zuordnung aktualisieren kann.

**[!UICONTROL Login Details]: \[Anmeldetyp\]** - ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] nur) Gibt an, ob Anmeldungen für das Konto mit folgenden Optionen autorisiert werden sollen:

* *[!UICONTROL oAuth]* (Standardeinstellung): Um die [[!DNL OAuth] Autorisierungsprotokoll](https://oauth.net/2/).

* *[!UICONTROL Password]:* Zum Verwenden des Kundenkennworts.

Für [!DNL Microsoft Advertising] nur Konten, [!DNL oAuth]-autorisierte Anmeldungen verwendet werden können.

**[!UICONTROL Login Details]: [!UICONTROL Login]:** (Alle Werbenetzwerke außer [!DNL Naver]) Der Anmeldename oder die ID, um den API-Zugriff auf das Konto zu aktivieren.

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** ([!DNL Microsoft Advertising] [!DNL oAuth]-aktiviert und alle anderen Netzwerke außer [!DNL Baidu], [!DNL Meta], und [!DNL Yandex]) Das Token des Kontos zur Autorisierung von Anmeldungen mithilfe der [[!DNL OAuth] Autorisierungsprotokoll](https://oauth.net/2/).

**[!UICONTROL Login Details]: [!UICONTROL Password]:** (Alle Werbenetzwerke außer [!DNL Naver]) Das Kennwort für das Konto. Für passwortaktivierte Konten unter [!DNL Baidu], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], und [!DNL Yandex], ist dieses Feld erforderlich. Für [!DNL oAuth]-aktivierte Konten ist dieses Feld optional. Verwenden Sie es, wenn Sie das Kennwort verschlüsseln und speichern möchten, damit der Kundenbetreuer Token nach Bedarf aktualisieren kann.

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** ([!DNL Baidu] und [!DNL Yandex] Nur Konten) Der Zugriffsschlüssel für das zu verwendende Entwicklerkonto.

**[!UICONTROL Currency]:** Die Abkürzung für die für das Konto verwendete Währung. Dieses Feld kann für neue [!DNL Naver] Konten. Bei allen anderen Suchnetzwerken wird der Wert automatisch mit der für das Konto im Werbenetzwerk konfigurierten Währung ausgefüllt, sobald Sie den Datensatz gespeichert haben.

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] und [!DNL Microsoft Advertising] Nur Konten; optional) Alle Parameter, die an das Ende der endgültigen URLs angehängt werden sollen, um Informationen zu verfolgen. Schließen Sie alle Parameter ein, die Ihr Unternehmen verfolgen muss.

Beispiel: `param1=value1&param2=value2`

Konten, die Adobe Advertising-Klick-Tracking verwenden, müssen die Klick-ID des Anzeigennetzwerks enthalten (`msclkid` für [!DNL Microsoft Advertising]; `gclid` für Google) im Suffix. Konten mit einer Adobe Analytics-Integration müssen den AMO-ID-Parameter verwenden (beginnend mit `s_kwcid`). Wenn das Konto über eine serverseitige AMO-ID-Implementierung verfügt, wird der Parameter automatisch hinzugefügt, wenn ein Benutzer auf eine Anzeige klickt. Andernfalls müssen Sie sie hier manuell hinzufügen. Siehe [erforderliche Suffix-Formate für [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) und [erforderliche Suffix-Formate für [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Dieses Feld wird nicht von der [!UICONTROL Auto Upload] Tracking-Einstellung.
>* Endgültige URL-Suffixe auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Verwenden Sie zur einfacheren Wartung nur das Suffix auf Kontoebene, es sei denn, es ist eine unterschiedliche Verfolgung für einzelne Kontokomponenten erforderlich. Verwenden Sie den Editor des Werbenetzwerks, um ein Suffix auf Anzeigengruppenebene oder niedriger zu konfigurieren.

**Zeitzone:** (Alle Werbenetzwerke außer [!DNL Baidu] und [!DNL Yahoo! Display Network]) Die Zeitzone des Advertisers. Dieses Feld kann bearbeitet werden und ist für neue [!DNL Naver] Konten. Bei allen anderen Suchnetzwerken wird der Wert automatisch mit der Zeitzone ausgefüllt, die für das Search-, Social- und Commerce-Konto des Advertisers konfiguriert ist, sobald Sie den Datensatz gespeichert haben.

**Status:** Der Kontostatus in Search, Social und Commerce:

* *Aktiviert:* Search, Social und Commerce synchronisiert Kampagnendaten mit dem -Konto (sofern unterstützt) und überträgt automatisierte Angebote und/oder Kampagnenbudgets für Kampagnen in Portfolios.
* *Deaktiviert:* Search, Social und Commerce stoppt alle Aktivitäten auf dem Konto. Während der Kontoaktivierung erfasste Daten werden weiterhin gespeichert. Die Ansichten und Berichte der Kampagnenverwaltung enthalten jedoch keine Daten für den Zeitraum, in dem das Konto angehalten wurde. Sie können das Konto später erneut aktivieren, um die Aktivität mit dem Konto wieder aufzunehmen.

**Tracking-Vorlage** - ([!DNL Google Ads], [!DNL Microsoft Advertising], und [!DNL Yahoo! Japan Ads] Nur Konten; optional) Die Standard-Tracking-Vorlage für das Konto, die alle Off-Landingpage-Umleitungen und Tracking-Parameter angibt und die finale URL/Landingpage in einen Parameter einbettet. Beispiel: `{lpurl}?source={network}&id=5` oder `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` , um eine Umleitung einzuschließen.

* So betten Sie die endgültige URL ein:

   * ([!DNL Google Ads] und [!DNL Microsoft Advertising] Nur) Eine Liste von Parametern zur Angabe der endgültigen URLs in Tracking-Vorlagen finden Sie im Abschnitt ([!DNL Microsoft Advertising] nur) [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799) oder ([!DNL Google Ads] nur) die Parameter &quot;Nur Tracking-Vorlage&quot; im Abschnitt &quot;Verfügbar&quot; [!DNL ValueTrack] Parameter&quot;im [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] nur) Verwenden Sie den Parameter . `!{lpurl}` um die Landingpage-URL anzugeben.

* Sie können optional URL-Parameter und alle für die Kampagne definierten benutzerdefinierten Parameter einbeziehen, getrennt durch kaufmännische Und-Zeichen (&amp;), z. B. `{lpurl}?matchtype={matchtype}&device={device}`.

* Sie können optional Umleitungen und Tracking von Drittanbietern hinzufügen.

* Wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload],&quot;Search, Social und Commerce beim Speichern des Datensatzes automatisch einen eigenen Umleitungs- und Trackingcode vorgibt.

>[!NOTE]
>
>* Für [!DNL Google Ads]vermeiden Sie die Verwendung von Makros, die nicht durch Klicks aus Quellen ersetzt werden, die das parallele Tracking ermöglichen. Wenn der Advertiser Makros verwenden muss, sollte das Adobe Account Team mit dem Support oder dem Implementierungsteam zusammenarbeiten, um sie hinzuzufügen.
>* Die Tracking-Vorlage auf der detailliertesten Ebene überschreibt die Werte auf allen höheren Ebenen. Wenn beispielsweise sowohl die Kontoeinstellungen als auch die Suchbegriffeinstellungen einen Wert enthalten, wird der Suchbegriffwert angewendet.
>* Wenn Sie eine Tracking-Vorlage auf Anzeigen-, Sitelink- oder Suchbegriffebene aktualisieren, werden die relevanten Anzeigen erneut zur Überprüfung eingereicht. Sie können Ihre Tracking-Vorlagen auf Konto-, Kampagnen- oder Anzeigengruppenebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.

**[!UICONTROL Master Account ID]:** ([!DNL Microsoft Advertising] Nur Konten) Die Kennung für ein Agentur-/Verwaltungskonto, das mit dem Konto verknüpft ist.

**[!UICONTROL MCC Account]:** ([!DNL Yandex] nur Konten; optional) Ein Agentur-/Verwaltungskonto, das mit dem Konto verknüpft ist. Um eine vorhandene Zuordnung zu entfernen, wählen Sie &quot;[!UICONTROL No MCC Account].&quot;

**[!UICONTROL Application ID]:** ([!DNL Yandex] Nur Konten) Das für das Konto zu verwendende Entwicklungstoken. Das gleiche Token wird für alle verwendet [!DNL Yandex] Konten.

**[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] Konten, bei denen die Einstellung Freigegebenes Konto deaktiviert ist; optional) Die numerische ID für die Kampagne, die zur Bezahlung aller Anzeigenkampagnen in dem Konto verwendet wird.

**[!UICONTROL Finance Token]:** ([!DNL Yandex] -Konten, bei denen die Einstellung Freigegebenes Konto deaktiviert ist; optional) Das Entwicklungstoken, das für finanzierungsbezogene API-Aufrufe verwendet wird, z. B. für die Neuzuweisung von Geld aus der Geldbörse zwischen den Kampagnen des Advertisers, sofern dies für die Portfoliooptimierung erforderlich ist.

### Kontoverfolgung

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

**[!UICONTROL Track Product Group]:** (Für [!UICONTROL EF Redirect] nur) Nicht implementiert

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **S_kwcid-Format** - (Bestehend [!DNL Google Ads] Konten für Advertiser mit einer Adobe Advertising-Adobe Analytics-Integration, für die die AMO-ID (s_kwcid) noch nicht migriert wurde.

Dieses Konto verwendet das ältere Format für den AMO-ID-Trackingcode, mit dem Adobe Advertising Daten über das Konto für Adobe Analytics freigeben können. Die [neuestes Format](/help/integrations/analytics/ids.md#amo-id-formats) enthält Parameter für die Kampagnen-ID und Anzeigengruppen-ID, die erforderlich sind, um eine genaue Berichterstellung auf Kampagnen- und Anzeigengruppenebene für [!DNL Google Ads] Kampagnen und Entwürfe sowie Experimente mit Höchstleistung in Analytics:

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

Wenn für dieses Konto Berichte auf Kampagnen- und Anzeigengruppenebene erstellt werden müssen, klicken Sie auf die Schaltfläche [!UICONTROL Edit] (Bleistift) und **[!UICONTROL Migrate to new s_kwcid format]** , um das neue Format zu ändern. Für Konten, die diese Kampagnentypen nicht enthalten, ist eine Migration in das neue Format optional, jedoch empfohlen.

Eine vollständige Anleitung finden Sie unter &quot;[Aktualisieren des AMO-ID-Trackingcodes für eine [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot;

**Report Suite-Namen** - (Nur für EF-Umleitung mit Token; Advertiser mit einer Adobe Advertising-Adobe Analytics-Integration; optional) Eine oder mehrere Analytics Report Suites, an die Search, Social und Commerce Daten aus dem Anzeigennetzwerk sendet, einschließlich Entitätsklassifizierungen und Klickdaten für das Konto. Diese Funktion ist nur für unterstützte Werbenetzwerke verfügbar.

Damit die Daten in den Report Suites angezeigt werden, muss entweder (a) die serverseitige AMO-ID-Funktion für das Konto oder (b) die Einstellung auf Advertiser-Ebene auf &quot;[!UICONTROL Enable tracking for SAINT feeds]&quot; muss aktiviert sein. Darüber hinaus muss das Analytics-Konto des Advertisers für den Empfang von Daten aus Search, Social und Commerce konfiguriert werden. Weitere Informationen erhalten Sie von Ihrem Adobe Account Manager.

>[!MORELIKETHIS]
>
>* [Über Werbenetzkonten](ad-network-account-about.md)
>* [Verwalten von Merchant-Center-Konten](merchant-account-manage.md)
>* [Aktualisieren Sie den s_kwcid-Trackingcode für eine [!DNL Google Ads] account](update-amo-id-google.md)
