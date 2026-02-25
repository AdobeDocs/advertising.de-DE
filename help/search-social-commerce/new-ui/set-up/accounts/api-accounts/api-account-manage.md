---
title: (Neue Benutzeroberfläche) Verwalten von Anzeigennetzwerkkonten
description: Erfahren Sie, wie Sie Kontodetails in der neuen Benutzeroberfläche für ein über die Werbenetzwerk-API synchronisiertes Werbenetzwerk einrichten und verwalten.
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '2129'
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Verwalten von Anzeigennetzwerkkonten über eine API-Verbindung

<!-- Besides just logging into an account, do you have to make any other choices once you're logged in (such as to give speciic permissions to SSC?  And what about oAuth tokens -- do we still use them? -->

*Beta-Funktion*

<!-- Move out info about Naver into a separate page -->

Im Folgenden finden Sie Anweisungen zum Verwalten von Anzeigennetzwerkkonten, die über die API des Anzeigennetzwerks mit Search, Social und Commerce synchronisiert werden.

<!-- Move out info about Naver into a separate page -->

Einzelheiten zu den für die einzelnen Werbenetzwerke verfügbaren Funktionen finden Sie unter &quot;[Unterstützte Inventarisierung](/help/search-social-commerce/introduction/supported-inventory.md).

## Erstellen und Netzwerkkonto-Details {#create-account}

Um die Synchronisierung eines Kontos zu aktivieren, müssen Sie einen entsprechenden Kontodatensatz mit den Anmeldedaten für den Kontozugriff und den Tracking-Optionen sowie mit dem Status *Aktiviert“*.

>[!NOTE]
>
>Um ein tatsächliches Konto im Werbenetzwerk zu erstellen, gehen Sie zur Website des Werbenetzwerks.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Klicken Sie auf **[!UICONTROL Create Account]**.

1. Klicken Sie auf den Namen des Werbenetzwerks und dann auf **[!UICONTROL Next]**.

1. (Alle Werbenetzwerke außer [!DNL Yandex]) Melden Sie sich mit den Anmeldeinformationen des Werbetreibenden beim Werbenetzwerk an. Wählen Sie die Option „Konto-Tracking für dieses Konto“ aus. Klicken Sie dann oben rechts auf **[!UICONTROL Next]**.

1. Geben Sie die [Kontoeinstellungen](#account-settings-api) an:

   1. Geben Sie auf der Registerkarte **[!UICONTROL Select Accounts]** die allgemeinen Kontoeinstellungen an. Geben Sie für [!DNL Yandex] Konten die Kontoanmeldeinformationen an.

   1. Klicken Sie auf die Registerkarte **[!UICONTROL Setup Tracking]** und geben Sie die Tracking-Einstellungen ein.

   1. (Werbetreibende mit einer [[!DNL Adobe Analytics for Advertising] Integration](/help/integrations/analytics/overview.md)) Klicken Sie auf die Registerkarte **[!UICONTROL Set up Adobe Analytics]** und wählen Sie alle Reporting-Suites aus, [!DNL Analytics] für die Tracking- und Reporting-Kampagnenaktivität verwendet werden sollen.

1. Klicken Sie auf **[!UICONTROL Save]**.

   Die aktuellen Kosten- und Klickdaten für alle Kampagnen im Konto werden stündlich in Search, Social und Commerce aktualisiert. Standardmäßig sind die Daten je nach Anzeigennetzwerk für die letzten 5 bis 10 Tage verfügbar. Bei Bedarf kann das Projektstartteam jedoch Daten für bis zu den letzten 60 Tagen abrufen.

## Details zum Anzeigen-Netzwerkkonto bearbeiten {#edit-account}

Um die Kontoeinstellungen erneut zu authentifizieren, um die Verbindung zu aktualisieren oder Berechtigungen zu aktualisieren, aktivieren oder deaktivieren Sie die Aktivität in einem Konto, ändern Sie die standardmäßigen Tracking-Parameter in einem Konto oder ändern Sie die [!DNL Analytics] Report Suites, die für Tracking und Reporting verwendet werden sollen, und bearbeiten Sie dann die Kontodetails.

>[!NOTE]
>
>Um ein tatsächliches Konto im Werbenetzwerk zu bearbeiten, gehen Sie auf die Website des Werbenetzwerks.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Wählen Sie das Konto auf eine der folgenden Arten aus:

   * Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]** .

   * Halten Sie den Cursor über den Kontonamen, klicken Sie auf **…** und dann auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie die [Kontoeinstellungen](#account-settings-api):

   1. (Optional) Bearbeiten Sie auf der Registerkarte **[!UICONTROL Account Details]** die Kontodetails.

   1. (Optional) Klicken Sie auf die Registerkarte **[!UICONTROL Setup Tracking]** und bearbeiten Sie die Tracking-Einstellungen.

   1. (Optional, Werbetreibende mit einer [[!DNL Adobe Analytics for Advertising] Integration](/help/integrations/analytics/overview.md)) Klicken Sie auf die Registerkarte **[!UICONTROL Set up Adobe Analytics]** und bearbeiten Sie die [!DNL Analytics] Reporting-Suites, die für die Tracking- und Reporting-Kampagnenaktivität verwendet werden sollen.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Klicken Sie auf **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Search, Social und Commerce müssen die neuen Kontodaten mit denen im Werbenetzwerk synchronisieren. Dies geschieht automatisch einmal täglich oder häufiger, wenn Search, Social und Commerce Änderungen im Werbenetzwerk erkennt.

## Erneutes Authentifizieren eines Werbenetzwerkkontos {#reauthenticate}

Um die Anzeigennetzwerkverbindung zu aktualisieren oder die Berechtigungen für das Konto zu aktualisieren, müssen Sie das Konto erneut authentifizieren.

1. (Wenn Sie in einem anderen Konto für dasselbe Werbenetzwerk in derselben Browser-Anwendung angemeldet sind) Melden Sie sich von einem anderen Konto als dem des Werbetreibenden ab.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

<!-- For Bing and Yandex, the right-click menu includes "Re authenticate." Clarify why just those types -->

1. Wählen Sie das Konto auf eine der folgenden Arten aus:

   * Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]** .

   * Halten Sie den Cursor über den Kontonamen, klicken Sie auf **…** und dann auf **[!UICONTROL Edit]**.

1. Klicken Sie auf der Registerkarte **[!UICONTROL Account Details]** auf **[!UICONTROL Re authenticate]** und melden Sie sich mit den Anmeldeinformationen des Werbetreibenden beim Werbenetzwerk an.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Aktivieren oder Deaktivieren von Anzeigennetzwerkkonten {#enable-disable-account}

Wenn Sie ein Anzeigennetzwerkkonto aktivieren, synchronisiert Search, Social und Commerce Kampagnendaten mit dem Konto (falls unterstützt) und pusht automatisierte Gebote und/oder Kampagnenbudgets für Kampagnen in Portfolios. Wenn Sie ein Anzeigennetzwerkkonto deaktivieren, stoppt Search, Social und Commerce alle Aktivitäten im Konto. Daten, die erfasst wurden, während das Konto aktiv war, werden weiterhin gespeichert, aber die Kampagnenverwaltungsansichten und -berichte enthalten keine Daten für den Zeitraum, in dem das Konto deaktiviert ist. Sie können das Konto später erneut aktivieren, um die Aktivität mit dem Konto fortzusetzen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Führen Sie einen der folgenden Schritte aus:

   * (Aus der [!UICONTROL Accounts]):

      * (Um das Konto zu aktivieren) Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Activate]** .

      * (So deaktivieren Sie das Konto) Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Pause]** .

   * (Aus den Kontoeinstellungen):

      1. Wählen Sie das Konto auf eine der folgenden Arten aus:

         * Halten Sie den Cursor über den Kontonamen, klicken Sie auf **…** und dann auf **[!UICONTROL Edit]**.

         * Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]** .

      1. Deaktivieren Sie auf der Registerkarte **[!UICONTROL Account Details]** die Option **[!UICONTROL Account enabled]**.

      1. Klicken Sie auf **[!UICONTROL Save]**.

## Einstellungen für Netzwerkkonto hinzufügen {#account-settings-api}

Die Kontoeinstellungen variieren je nach Anzeigennetzwerk. Möglicherweise werden nicht alle Einstellungen unten angezeigt.

<!-- When you're creating new accounts only; not sure that you'll have anything to do here once you've authenticated

### Authenticate tab

-->

### Registerkarte [!UICONTROL Select Accounts]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** Der Name, der für das Konto in Search, Social und Commerce angezeigt werden soll.

>[!NOTE]
>
>Wenn Sie eine Integration zwischen Search, Social und Commerce und Adobe Analytics haben und den Namen des Suchkontos ändern, bitten Sie Ihr Adobe-Accountteam, die Zuordnung zu aktualisieren.

**[!DNL [Ad Network] Accounts]:** (sichtbar, während Sie ein Konto erstellen) Das zu synchronisierende Ad-Netzwerk-Konto.

**[Anmeldedetails]:** (nur Yandex-Konten) Die zu verwendenden Kontoanmeldeinformationen:

* **[!UICONTROL Login]:** Der Anmeldename oder die ID, um den API-Zugriff auf das Konto zu aktivieren.

* **[!UICONTROL Password]:** Das Kennwort für das Konto.

* **[!UICONTROL Access Key]:** Der Zugriffsschlüssel für das zu verwendende Entwicklerkonto.

* **[!UICONTROL Application ID]:** Das für das Konto zu verwendende Entwickler-Token. Dasselbe Token wird für alle [!DNL Yandex] Konten verwendet.

* **[!UICONTROL Purse Campaign ID]:** (nur [!DNL Yandex] Konten mit deaktivierter Einstellung „Freigegebenes Konto“; optional) Die numerische ID für die Kampagne, mit der alle Anzeigenkampagnen im Konto bezahlt werden.

* **[!UICONTROL Finance Token]:** (Nur [!DNL Yandex] Konten mit deaktivierter Einstellung „Freigegebenes Konto“; optional) Das Entwickler-Token, das für finanzbezogene API-Aufrufe verwendet wird, z. B. um Geld aus der Geldbörse zwischen den Kampagnen des Werbetreibenden neu zuzuweisen, wie es für die Portfoliooptimierung erforderlich ist.

**[!UICONTROL Network Account ID]:** (Alle Werbenetzwerke außer [!DNL Yandex] Die vom Werbenetzwerk zugewiesene Konto-ID.

>[!NOTE]
>
>Ad-Network-Manager-Konten werden hier nicht unterstützt. Um ein Manager-Konto für [!DNL Microsoft Advertising] zu identifizieren, verwenden Sie das Feld Master-Konto-ID bzw. MCC-Konto . Um [Anmeldeinformationen für ein [!DNL Google Ads] Manager-Konto einzurichten](/help/search-social-commerce/admin/manager-accounts.md), gehen Sie zu [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Currency]:** (Schreibgeschützt) Die Abkürzung für die für das Konto verwendete Währung. Dieser Wert wird nach dem Speichern des Datensatzes automatisch mit der Währung ausgefüllt, die für das Konto im Werbenetzwerk konfiguriert wurde.

**[!UICONTROL Time Zone]:** Die Zeitzone des Werbetreibenden. Dieser Wert wird nach dem Speichern des Datensatzes automatisch mit der Zeitzone ausgefüllt, die für das Konto „Suche“, „Social“ und &quot;Commerce&quot; des Werbetreibenden konfiguriert ist.

**[!UICONTROL Login]:** (Schreibgeschützt) Das Benutzerkonto, das zum Anmelden bei dem Konto verwendet wird.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Search, Social und Commerce synchronisiert Kampagnendaten mit dem Konto (falls unterstützt) und pusht automatisierte Gebote und/oder Kampagnenbudgets für Kampagnen in Portfolios.

## Registerkarte [!UICONTROL Setup Tracking]

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]:** Gibt an, ob das Tracking mit dem Konversionsverfolgungs-Service von Adobe Advertising aktiviert werden soll. Diese Methode generiert eindeutige Klick-Tracking-IDs und leitet Benutzer zu Tracking-Zwecken an den Adobe Advertising-Server weiter, bevor sie an die Landingpage des Clients gesendet werden. Diese Methode verfügt über standardmäßige Tracking-Optionen, die Sie optional anpassen können, und Sie können auch Parameter angeben, die an jede URL angehängt werden sollen.

Um diese Funktion zu aktivieren, aktivieren Sie **[Tracking aktivieren]**.

>[!NOTE]
>
>* Wenn Sie diese Einstellung ändern, müssen Sie die Tracking-URLs für das Konto neu generieren.
>* Tracking-Optionen auf Kampagnenebene setzen Einstellungen auf Kontoebene außer Kraft.

**[!UICONTROL Tracking Type]:** (Wenn das Tracking in Search, Social und Commerce aktiviert ist) Die Methode der Weiterleitung von Endbenutzenden an die endgültige URL oder Ziel-URL. Die ausgewählte Option gilt für alle Gebotseinheiten im Konto oder in der Kampagne. Die Standardeinstellung auf Kontoebene wird von den Tracking-Einstellungen des Advertisers übernommen, und die Standardeinstellung auf Kampagnenebene wird von den Kontoeinstellungen übernommen.

* *[!UICONTROL Standard]:* Um den Endbenutzer einfach zur angegebenen URL umzuleiten.

* *[!UICONTROL Token]:* Um den Endbenutzer zur URL umzuleiten und auch die ID für Suche, Social und Commerce für den Klick (`ef_id`) als Abfragezeichenfolgenparameter aufzuzeichnen, der als Token verwendet wird. Wählen Sie diese Option aus, wenn Sie Offline-Transaktionen melden, Search, Social und Commerce Daten mit Adobe Analytics austauschen sollen oder alle Konversionen verfolgen möchten, die in [!DNL Apple Safari] Browsern auftreten.

>[!NOTE]
>
>* Wenn Sie von [!UICONTROL Standard] zu [!UICONTROL Token] oder umgekehrt wechseln, müssen Sie die Tracking-URLs für das Konto neu generieren.
>* Die Einstellung auf Kontoebene kann auf Kampagnenebene außer Kraft gesetzt werden.

**[!UICONTROL Auto Update]:** (Wenn das Tracking in Search, Social und Commerce aktiviert ist) Standardisiert Ihre Tracking-URLs für die Kompatibilität zwischen Browsern und Servern. Search, Social und Commerce laden bei der nächsten Synchronisierung automatisch Folgendes in das Werbenetzwerk hoch: (a) Tracking-Parameter für Suche, Social und Commerce für Tracking-Vorlagen und dieselben Parameter, die an die endgültigen URLs angehängt werden, oder (b) neue Ziel-URLs, die in den Tracking-Code für Search, Social und Commerce eingebettet sind. Für Werbetreibende mit einer [Adobe Advertising-Adobe Analytics-Integration](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=de) und einer serverseitigen AMO-ID-Konfiguration (s_kwcid) enthält der Upload auch [AMO-ID-Parameter](/help/integrations/analytics/ids.md#amo-id) für Ihre [!DNL Google Ads]- und [!DNL Microsoft Advertising]. Die Standardeinstellung auf Kontoebene wird von den Tracking-Einstellungen des Advertisers übernommen. Die Einstellung auf Kontoebene kann auf Kampagnenebene außer Kraft gesetzt werden.

Tracking-URLs werden täglich nur für Entitäten aktualisiert, die nicht synchronisiert sind (d. h. neue hinzugefügte Entitäten und vorhandene Entitäten, deren Eigenschaften sich geändert haben). Wenn Sie diese Einstellung für einen vorhandenen Advertiser/ein vorhandenes Konto/eine vorhandene Kampagne von „Deaktiviert“ in „Aktiviert“ ändern, werden die Tracking-URLs daher nicht für vorhandene Entitäten aktualisiert, die bereits synchronisiert sind. Um den URLs vorhandener, synchronisierter Entitäten Tracking hinzuzufügen, wenden Sie sich an Ihr Adobe-Accountteam und fordern Sie einen einmaligen, manuellen Synchronisierungsprozess an. Der automatische Upload-Prozess handhabt zukünftige Änderungen.

**[!UICONTROL URL Encoding]:** (Wenn das Tracking in Search, Social und Commerce aktiviert ist, nur Konten mit Ziel-URLs) Kodiert die Basis-URL in der Browser-Adressleiste des Endbenutzers (z. B. `%3D` anstelle von `=`):

**[!UICONTROL Tracking Level]:** (Wenn das Tracking nach Search, Social und Commerce aktiviert ist, auf Konto- und Kampagnenebene verfügbar ist, nicht auf Werbenetzwerke anwendbar, die für das parallele Tracking aktiviert sind) Die Ebene, auf der Klicks und Umsatz verfolgt werden sollen, indem eine Umleitung hinzugefügt wird (falls relevant) und Parameter an die entsprechenden URLs angehängt werden:

* *[!UICONTROL Keyword]:* Zum Nachverfolgen von Daten nur auf Keyword-Ebene. Nicht verfügbar für [!DNL Yandex].

* *[!UICONTROL Ad]:* Zum Nachverfolgen von Daten nur auf Anzeigenebene. Nicht verfügbar für [!DNL Naver].

* *[!UICONTROL Keyword and Ad]:* Zum Nachverfolgen von Daten sowohl auf Keyword- als auch auf Anzeigenebene. Nicht verfügbar für [!DNL Naver] und [!DNL Yandex].

**[!UICONTROL Landing Page Suffix]** (Nur [!DNL Google Ads]- und [!DNL Microsoft Advertising]-Konten; optional) Alle Parameter, die an das Ende der endgültigen URLs angehängt werden sollen, um Informationen zu verfolgen; enthalten alle Parameter, die Ihr Unternehmen verfolgen muss.

Beispiel: `param1=value1&param2=value2`

Konten, die Adobe Advertising-Klick-Tracking verwenden, müssen die Klick-Kennung des Werbenetzwerks (`msclkid` für [!DNL Microsoft Advertising]; `gclid` für Google) im Suffix enthalten. Konten mit einer Adobe Analytics-Integration müssen den AMO ID-Parameter verwenden (beginnend mit `s_kwcid`). Wenn das Konto über eine serverseitige AMO ID-Implementierung verfügt, wird der Parameter automatisch hinzugefügt, wenn ein Benutzer auf eine Anzeige klickt. Andernfalls müssen Sie ihn hier manuell hinzufügen. Siehe die [erforderlichen Suffixformate für [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) und [erforderlichen Suffixformate für [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Dieses Feld wird von der Einstellung „Tracking [!UICONTROL Auto Update]&quot; nicht aktualisiert.
>* Endgültige URL-Suffixe auf niedrigeren Ebenen überschreiben das Suffix auf Kontoebene. Zur einfacheren Wartung verwenden Sie nur das Suffix auf Kontoebene, es sei denn, eine andere Nachverfolgung für einzelne Kontokomponenten ist erforderlich. Um ein Suffix auf Anzeigengruppenebene oder darunter zu konfigurieren, verwenden Sie den Editor des Anzeigennetzwerks.

**Konto-Tracking-URL**: (Nur [!DNL Google Ads]-, [!DNL Microsoft Advertising]- und [!DNL Yahoo! Japan Ads]-Konten; optional) Die standardmäßige Tracking-Vorlage für das Konto, in der alle Umleitungen und Tracking-Parameter für Off-Landing-Domains angegeben und die endgültige/Landingpage-URL ebenfalls in einen Parameter eingebettet wird. Beispiel: `{lpurl}?source={network}&id=5` oder `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`, um eine Umleitung einzuschließen.

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

## Registerkarte [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (Werbetreibende mit einer [[!DNL Adobe Analytics for Advertising] Integration](/help/integrations/analytics/overview.md); optional) Eine oder mehrere Analytics-Report Suites, an die Search, Social und Commerce Daten sendet, die über das Werbenetzwerk erfasst werden, einschließlich Entitätsklassifizierungen und Klickdaten für das Konto. Diese Funktion steht nur unterstützten Werbenetzwerken zur Verfügung.

Damit die Daten in den Report Suites angezeigt werden, muss entweder (a) die Server-seitige AMO-ID-Funktion für das Konto konfiguriert sein oder (b) die Einstellung auf Advertiser-Ebene auf &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; aktiviert sein. Darüber hinaus muss das [!DNL Analytics] des Werbetreibenden so konfiguriert sein, dass es Daten von Search, Social und Commerce empfängt. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

>[!MORELIKETHIS]
>
>* [Über Werbenetzwerkkonten](../ad-network-account-about.md)
>* [Konten des Händlerzentrums verwalten](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
>* [Aktualisieren des s_kwcid-Trackingcodes für ein [!DNL Google Ads] Konto](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
