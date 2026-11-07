---
title: (Neue Benutzeroberfläche) Verwalten von Anzeigennetzwerkkonten
description: Erfahren Sie, wie Sie Kontodetails in der neuen Benutzeroberfläche für ein über die Werbenetzwerk-API synchronisiertes Werbenetzwerk einrichten und verwalten.
feature: Search Campaign Management
exl-id: a50b2943-7568-401c-be5b-ff6f62629488
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
source-git-commit: b568da9300e9adb8d189811c3c8b52516dfcef6f
workflow-type: tm+mt
source-wordcount: '3141'
ht-degree: 0%
---
# (Neue Benutzeroberfläche) Verwalten von Anzeigennetzwerkkonten über eine API-Verbindung

In diesen Anweisungen wird beschrieben, wie Sie Anzeigennetzwerkkonten verwalten, die über APIs nach, sozialen und Commerce-Synchronisationen suchen, einschließlich Authentifizierung, Verbindungsaktualisierung und Statusprüfungen.

Zum Erstellen, Bearbeiten oder erneuten Authentifizieren von Konten benötigen Sie die Berechtigung zum Bearbeiten von Konten.

Einzelheiten zu den für die einzelnen Werbenetzwerke verfügbaren Funktionen finden Sie unter &quot;[Unterstützte Inventarisierung](/help/search-social-commerce/introduction/supported-inventory.md).

## Über die [!UICONTROL Accounts] {#account-view-about}

Die Ansicht [!UICONTROL Manage] > [!UICONTROL Accounts] listet alle Werbenetzwerkkonten in der gefilterten Ansicht für das ausgewählte Advertiser-Konto auf. Klicken Sie auf einen Kontonamen, um die für dieses Konto gefilterte [!UICONTROL Campaigns] zu öffnen.

### Kontoauthentifizierung und Zugriffsstatus {#authentication-status}

Details zur Authentifizierung und zum Zugriff variieren je nach Anzeigennetzwerk und den für das Konto verfügbaren Informationen. Einem aktivierten oder erfolgreich authentifizierten Konto können weiterhin Berechtigungen fehlen.

Die folgenden Spalten zeigen Details zum Kontostatus, zur Authentifizierung und zum Zugriff:

* **[!UICONTROL Status]:** Der Betriebsstatus des Kontos, der von der Authentifizierung und den Berechtigungen getrennt ist. Ein aktiviertes Konto kann Daten mit dem Werbenetzwerk synchronisieren und unterstützte Kontoverwaltungs- und Optimierungsfunktionen verwenden. Ein deaktiviertes Konto stoppt Aktivitäten in Search, Social und Commerce. Die Kontostatusanzeige verwendet eine grüne Anzeige für **[!UICONTROL Enabled]**, eine rote Anzeige für **[!UICONTROL Disabled]** und eine gelbe Anzeige für **[!UICONTROL Pending]**. Sie können [Konten aktivieren oder deaktivieren](#enable-disable-account) über die Ansicht oder die Kontoeinstellungen.

* **[!UICONTROL Authenticated]:** Ob das Konto authentifiziert ist:

  * **[!UICONTROL Yes]:** Das Konto ist authentifiziert.

  * **[!UICONTROL No]:** Das Konto ist nicht authentifiziert. Wenn ein Authentifizierungsfehler verfügbar ist, halten Sie den Cursor über das rote Warnsymbol, um den Fehler anzuzeigen.

  * **[!UICONTROL Not Applicable]: Die**-Authentifizierung wird nicht angewendet, da Sie Daten für das Konto hochladen, anstatt eine Verbindung über eine API herzustellen.

  * **[!UICONTROL Expiring in N days]**, **[!UICONTROL Expiring today]** oder **[!UICONTROL Expired]:** Eine Token-Ablaufwarnung ersetzt **[!UICONTROL Yes]**, wenn Ablaufinformationen verfügbar sind und das Token in 14 Tagen oder weniger abläuft oder bereits abgelaufen ist. Klicken Sie auf das Warnsymbol, um die Zugriffsdetails des Kontos anzuzeigen und sich [&#x200B; authentifizieren](#reauthenticate).

* **[!UICONTROL Manager Account for Cross-Account Conversions]:** (nur [!DNL Google Ads] Konten) Die ID des zugehörigen Manager-Kontos, das für kontoübergreifende Konversions-Uploads verwendet wird. Wenn für das Manager-Konto ein Fehler verfügbar ist, wird neben der ID ein Warnsymbol angezeigt. Um den Fehler anzuzeigen, halten Sie den Cursor über dem Symbol. Die Anmeldeinformationen des Manager-Kontos sind getrennt von den Anmeldeinformationen des Anzeigennetzwerkkontos. Um Anmeldeinformationen für das Manager-Konto hinzuzufügen oder zu aktualisieren, verwenden Sie **[!UICONTROL Setup]** > **[!UICONTROL Manager Accounts]**. Siehe &quot;[Verwalten von Manager-](/help/search-social-commerce/new-ui/set-up/manager-account-manage.md)&quot;.

* **[!UICONTROL Access Level]:** Die angezeigte Zugriffsebene des Kontos, z. B. **[!UICONTROL Full]**, **[!UICONTROL Limited]** oder **[!UICONTROL None]**, oder **[!UICONTROL Not Applicable]**, wenn kein Wert für die Zugriffsebene verfügbar ist.

  Wenn Berechtigungen fehlen, klicken Sie auf das Warnsymbol, um die Zugriffsdetails des Kontos anzuzeigen. Im Abschnitt **[!UICONTROL Access]** werden Berechtigungen als **[!UICONTROL Granted]** oder **[!UICONTROL Missing]** aufgelistet. Wenn Details zur Auswirkung verfügbar sind, werden im Abschnitt **[!UICONTROL Not working]** die betroffenen Funktionen aufgelistet. Um [erneut zu authentifizieren](#reauthenticate) und Berechtigungen zu aktualisieren, klicken Sie auf **[!UICONTROL Update Access]**.

### Verfügbare Aktionen

Die verfügbaren Aktionen hängen von Ihren Berechtigungen und dem Kontotyp ab.

* [Erstellen und Netzwerkkonto-Details](#create-account)

* [Details zum Anzeigen-Netzwerkkonto bearbeiten](#edit-account)

* [Erneutes Authentifizieren eines Werbenetzwerkkontos](#reauthenticate)

* [Aktivieren oder Deaktivieren von Anzeigennetzwerkkonten](#enable-disable-account)

* [Kontodaten mit dem Werbenetzwerk synchronisieren](sync-api-accounts.md)

* [Anzeigen eines Leistungsdiagramms in der [!UICONTROL Accounts]](#account-performance-graph)

* [Verwalten von Datenansichtsberichten aus der [!UICONTROL Accounts]](#account-reports)

## Erstellen und Netzwerkkonto-Details {#create-account}

Um die Synchronisierung eines Kontos zu aktivieren, müssen Sie einen entsprechenden Kontodatensatz mit den Anmeldedaten für den Kontozugriff und den Tracking-Optionen sowie mit dem Status *Aktiviert“*.

>[!NOTE]
>
>Um ein tatsächliches Konto im Werbenetzwerk zu erstellen, gehen Sie zur Website des Werbenetzwerks.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Klicken Sie auf **[!UICONTROL Create Account]**.

1. Klicken Sie auf den Namen des Werbenetzwerks, um die Kontoeinrichtung zu öffnen.

1. (Alle Werbenetzwerke außer [!DNL ChatGPT Ads] und [!DNL Yandex]) Vervollständigen Sie auf der Registerkarte **[!UICONTROL Authenticate]** die Anmeldung im Popup-Fenster mit den Anmeldedaten des Werbetreibenden und gewähren Sie dem angeforderten Konto Zugriff.

   Der Setup-Bildschirm wird automatisch aktualisiert und zeigt **[!UICONTROL Authentication Successful]** an, wenn die Authentifizierung erfolgreich war. Wenn Sie das Anmeldefenster erneut öffnen müssen, klicken Sie auf **[!UICONTROL Open login again]**. Wenn Ihr Browser das Fenster blockiert, bearbeiten Sie Ihre Browser-Einstellungen, um Popups für die Site zuzulassen.

   [!DNL Meta Ads] werden fehlende Berechtigungen und ihre Auswirkungen durch einen Warnhinweis identifiziert. Eine erfolgreiche Authentifizierung bedeutet nicht unbedingt, dass alle angeforderten Berechtigungen gewährt wurden.

   Zum Fortfahren auf **[!UICONTROL Next]** klicken.

1. Geben Sie die [Kontoeinstellungen](#account-settings-api) auf jeder verfügbaren Registerkarte an. Wählen Sie bei Konten, die in einem Popup authentifiziert werden sollen, auf der Registerkarte **[!UICONTROL Select Accounts]** das zu synchronisierende Konto aus **[!UICONTROL Linked Ad Accounts]**.

1. Klicken Sie auf **[!UICONTROL Save]**.

   Die aktuellen Kosten- und Klickdaten für alle Kampagnen im Konto werden stündlich in Search, Social und Commerce aktualisiert. Standardmäßig sind die Daten je nach Anzeigennetzwerk für die letzten 5 bis 10 Tage verfügbar. Bei Bedarf kann das Projektstartteam jedoch Daten für bis zu den letzten 60 Tagen abrufen.

## Details zum Anzeigen-Netzwerkkonto bearbeiten {#edit-account}

Um Aktivitäten für ein Konto zu aktivieren oder zu deaktivieren, die standardmäßigen Tracking-Parameter eines Kontos zu ändern oder die für Tracking und Reporting zu verwendenden [!DNL Analytics] Report Suites zu ändern, bearbeiten Sie die Kontodetails. Um die Verbindung zu aktualisieren oder die Berechtigungen zu aktualisieren, können [&#x200B; das Konto &#x200B;](#reauthenticate) den Kontoeinstellungen oder der [!UICONTROL Accounts] erneut authentifizieren.

>[!NOTE]
>
>Um ein tatsächliches Konto im Werbenetzwerk zu bearbeiten, gehen Sie auf die Website des Werbenetzwerks.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Wählen Sie das Konto auf eine der folgenden Arten aus:

   * Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]** .

   * Halten Sie den Cursor über den Kontonamen, klicken Sie auf **…** und dann auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie die [Kontoeinstellungen](#account-settings-api) auf den verfügbaren Registerkarten.

1. Klicken Sie auf **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Search, Social und Commerce müssen die neuen Kontodaten mit denen im Werbenetzwerk synchronisieren. Dies geschieht automatisch einmal täglich oder häufiger, wenn Search, Social und Commerce Änderungen im Werbenetzwerk erkennt.

## Erneutes Authentifizieren eines Werbenetzwerkkontos {#reauthenticate}

*Für Konten, die Popup-Authentifizierung verwenden; nicht anwendbar auf [!DNL ChatGPT Ads] oder [!DNL Yandex] Konten*

Um die Anzeigennetzwerkverbindung zu aktualisieren oder die Berechtigungen für das Konto zu aktualisieren, müssen Sie das Konto erneut authentifizieren.

1. (Wenn Sie in einem anderen Konto für dasselbe Werbenetzwerk in derselben Browser-Anwendung angemeldet sind) Melden Sie sich von einem anderen Konto als dem des Werbetreibenden ab.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Öffnen Sie die Authentifizierung auf eine der folgenden Arten:

   * (Wenn der **[!UICONTROL Authenticated]** des Kontos **[!UICONTROL No]** ist) Halten Sie den Cursor über den Kontonamen, klicken Sie auf **…** und klicken Sie dann auf **[!UICONTROL Re authenticate]**, falls verfügbar.

   * (Wenn eine Token-Ablaufwarnung angezeigt wird) Klicken Sie auf das Warnsymbol in der Spalte &quot;**[!UICONTROL Authenticated]**&quot; und dann auf **[!UICONTROL Reauthenticate]**.

   * (Wenn Berechtigungen fehlen) Klicken Sie auf das Warnsymbol in der Spalte **[!UICONTROL Access Level]** und dann auf **[!UICONTROL Update Access]**.

   * (In den Kontoeinstellungen) Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]**, oder halten Sie den Cursor über dem Kontonamen, klicken Sie auf **…** und klicken Sie dann auf **[!UICONTROL Edit]**. Klicken Sie auf der Registerkarte **[!UICONTROL Account Details]** in **[!UICONTROL Account Authentication]** auf **[!UICONTROL Re authenticate]**.

1. Schließen Sie die Anmeldung im Popup-Fenster mit den Anmeldedaten des Werbetreibenden ab und gewähren Sie dem angeforderten Konto Zugriff.

   Das neue Zugriffstoken wird automatisch gespeichert, wenn die erneute Authentifizierung erfolgreich ist. Wenn Sie auch andere Kontoeinstellungen ändern, klicken Sie auf **[!UICONTROL Save]** , um diese Änderungen zu speichern.

   [!DNL Meta Ads] werden in einer Informationsmeldung alle Berechtigungen identifiziert, die nach erfolgreicher erneuter Authentifizierung noch fehlen. Um die betroffenen Funktionen zu identifizieren, überprüfen Sie die [Zugriffsdetails](#authentication-status).

## Aktivieren oder Deaktivieren von Anzeigennetzwerkkonten {#enable-disable-account}

Wenn Sie ein Anzeigennetzwerkkonto aktivieren, synchronisiert Search, Social und Commerce Kampagnendaten mit dem Konto (falls unterstützt) und pusht automatisierte Gebote und/oder Kampagnenbudgets für Kampagnen in Portfolios. Wenn Sie ein Anzeigennetzwerkkonto deaktivieren, stoppt Search, Social und Commerce alle Aktivitäten im Konto. Daten, die erfasst wurden, während das Konto aktiv war, werden weiterhin gespeichert, aber die Kampagnenverwaltungsansichten und -berichte enthalten keine Daten für den Zeitraum, in dem das Konto deaktiviert ist. Sie können das Konto später erneut aktivieren, um die Aktivität mit dem Konto fortzusetzen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Führen Sie einen der folgenden Schritte aus:

   * (Aus der [!UICONTROL Accounts]):

     * (Um das Konto zu aktivieren) Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Enable]** .

     * (So deaktivieren Sie das Konto) Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Disable]** .

   * (Aus den Kontoeinstellungen):

     1. Wählen Sie das Konto auf eine der folgenden Arten aus:

        * Halten Sie den Cursor über den Kontonamen, klicken Sie auf **…** und dann auf **[!UICONTROL Edit]**.

        * Aktivieren Sie das Kontrollkästchen neben dem Kontonamen und klicken Sie dann in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]** .

     1. Aktivieren Sie auf der Registerkarte **[!UICONTROL Account Details]** die Option **[!UICONTROL Account Enabled]** , um das Konto zu aktivieren, oder deaktivieren Sie sie, um das Konto zu deaktivieren.

     1. Klicken Sie auf **[!UICONTROL Save]**.

## Anzeigen eines Leistungsdiagramms in der [!UICONTROL Accounts] {#account-performance-graph}

Öffnen und konfigurieren Sie ein Leistungsdiagramm mit bis zu drei Metriken insgesamt für alle Konten in der gefilterten Ansicht für den angegebenen Datumsbereich und die angegebene Währung.

### Anzeigen eines Leistungsdiagramms

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Geben Sie den Datumsbereich an und wenden Sie alle Filter auf die Konten an, deren Leistung Sie anzeigen möchten.

1. Klicken Sie über der Datentabelle auf ![Diagramme](/help/search-social-commerce/assets/charts.png "Diagramme").

1. (Optional) Verwenden Sie **[!UICONTROL Currency]** und **[!UICONTROL Metrics]**, um die Währung und bis zu drei Metriken anzugeben, die in das Diagramm aufgenommen werden sollen.

### Ausblenden eines sichtbaren Leistungsdiagramms

* Klicken Sie über der Datentabelle auf ![Diagramme](/help/search-social-commerce/assets/charts.png "Diagramme").

## Verwalten von Datenansichtsberichten aus der [!UICONTROL Accounts] {#account-reports}

Erstellen Sie einen Bericht, der die Datenzeilen für ein oder mehrere Konten in der [!UICONTROL Accounts] enthält, und laden Sie dann den Bericht als Excel-Arbeitsblattdatei für Microsoft (XLSX-Format) herunter. Der Bericht enthält die sichtbaren Spalten in der Ansicht für den angegebenen Datumsbereich.

Sie können abgeschlossene Berichte und Berichte löschen, die nicht generiert werden konnten.

### Erstellen eines Berichts mit den gefilterten Datenzeilen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Geben Sie den Datumsbereich an und wenden Sie alle Filter auf die Daten an, die Sie herunterladen möchten.

1. Geben Sie die Konten an, deren Daten Sie herunterladen möchten:

   * Um Daten für bestimmte Konten herunterzuladen, aktivieren Sie die Kontrollkästchen neben den Konten.

   * Wenn Sie Daten für alle Konten in der gefilterten Ansicht herunterladen möchten, lassen Sie alle Kontrollkästchen deaktiviert.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ")**[!UICONTROL Reports]**.

1. Behalten Sie im Dialogfeld [!UICONTROL Grid Reports] die **[!UICONTROL Report Name]** bei, oder geben Sie einen anderen Namen ein, und klicken Sie dann auf **[!UICONTROL Generate]**.

   Der Bericht wird der **[!UICONTROL Recently Generated]** hinzugefügt.

1. (Optional) Um die Datei nach Abschluss des Vorgangs herunterzuladen, klicken Sie ![Herunterladen](/help/search-social-commerce/assets/download.png "Herunterladen") neben dem Dateinamen.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

### Herunterladen eines abgeschlossenen Berichts

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ")**[!UICONTROL Reports]**.

1. Klicken Sie in der **[!UICONTROL Recently Generated]** im [!UICONTROL Grid Reports] auf ![Herunterladen](/help/search-social-commerce/assets/download.png "Herunterladen") neben dem Dateinamen.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

### Löschen eines Berichts

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ")**[!UICONTROL Reports]**.

1. Klicken Sie in der **[!UICONTROL Recently Generated]** im [!UICONTROL Grid Reports] auf ![Löschen](/help/search-social-commerce/assets/delete-new.png "Löschen") neben dem Namen eines abgeschlossenen Berichts oder eines Berichts, der nicht generiert werden konnte.

1. Bestätigen Sie den Löschvorgang.

## Einstellungen für Netzwerkkonto hinzufügen {#account-settings-api}

Die Kontoeinstellungen variieren je nach Anzeigennetzwerk. Möglicherweise werden nicht alle Einstellungen unten angezeigt.

### Registerkarte [!UICONTROL Authenticate]

(Sichtbar, während Sie ein Konto erstellen, das die Popup-Authentifizierung verwendet) Stellen Sie mithilfe der Anmeldeinformationen des Werbetreibenden eine Verbindung zum Werbenetzwerk her. Auf der Registerkarte wird der Verbindungsstatus angezeigt und es werden **[!UICONTROL Open login again]** zum erneuten Öffnen des Anmelde-Popup angezeigt.

### Registerkarte [!UICONTROL Select Accounts]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** Der Name, der für das Konto in Search, Social und Commerce angezeigt werden soll.

>[!NOTE]
>
>Wenn Sie eine Integration zwischen Search, Social und Commerce und Adobe Analytics haben und den Namen des Suchkontos ändern, bitten Sie Ihr Adobe-Accountteam, die Zuordnung zu aktualisieren.

**[!UICONTROL Linked Ad Accounts]:** (sichtbar, während Sie ein Konto erstellen, das die Popup-Authentifizierung verwendet) Das zu synchronisierende Netzwerkkonto der Anzeige. Wählen Sie aus den Werbekonten aus, die mit Ihrer Netzwerkanmeldung verknüpft sind.

**[Anmeldedetails]:** (nur [!DNL Yandex] Konten) Die zu verwendenden Kontoanmeldeinformationen:

* **[!UICONTROL Login]:** Der Anmeldename oder die ID, um den API-Zugriff auf das Konto zu aktivieren.

* **[!UICONTROL Password]:** Das Kennwort für das Konto.

* **[!UICONTROL Access Key]:** Der Zugriffsschlüssel für das zu verwendende Entwicklerkonto.

* **[!UICONTROL Application ID]:** Das für das Konto zu verwendende Entwickler-Token. Dasselbe Token wird für alle [!DNL Yandex] Konten verwendet.

* **[!UICONTROL Purse Campaign ID]:** (nur [!DNL Yandex] Konten mit deaktivierter Einstellung „Freigegebenes Konto“; optional) Die numerische ID für die Kampagne, mit der alle Anzeigenkampagnen im Konto bezahlt werden.

* **[!UICONTROL Finance Token]:** (Nur [!DNL Yandex] Konten mit der Einstellung „Freigegebenes Konto“ deaktiviert; optional) Das Entwickler-Token für finanzbezogene API-Aufrufe, z. B. die Umverteilung von Geld zwischen Advertiser-Kampagnen zur Portfoliooptimierung.

**[!UICONTROL Currency]:** (Schreibgeschützt) Die Abkürzung für die für das Konto verwendete Währung. Dieser Wert wird nach dem Speichern des Datensatzes automatisch mit der Währung ausgefüllt, die für das Konto im Werbenetzwerk konfiguriert wurde.

**[!UICONTROL Time Zone]:** Die Zeitzone des Werbetreibenden. Dieser Wert wird nach dem Speichern des Datensatzes automatisch mit der Zeitzone ausgefüllt, die für das Konto „Suche“, „Social“ und &quot;Commerce&quot; des Werbetreibenden konfiguriert ist.

**[!UICONTROL Login]:** (Schreibgeschützt) Das Benutzerkonto, das zum Anmelden bei dem Konto verwendet wird.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Search, Social und Commerce synchronisiert Kampagnendaten mit dem Konto (falls unterstützt) und pusht automatisierte Gebote und/oder Kampagnenbudgets für Kampagnen in Portfolios.

**[!UICONTROL Account Authentication]> [!UICONTROL Re authenticate]:** (sichtbar, während Sie ein Konto bearbeiten, das die Popup-Authentifizierung verwendet) Aktualisiert die Verbindung oder aktualisiert die Kontoberechtigungen. Das neue Zugriffstoken wird automatisch gespeichert, wenn die erneute Authentifizierung erfolgreich ist.

## Registerkarte [!UICONTROL Setup Tracking]

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]:** Gibt an, ob das Tracking mit dem Konversionsverfolgungs-Service von Adobe Advertising aktiviert werden soll. Diese Methode generiert eindeutige Klick-Tracking-IDs und leitet Benutzer zu Tracking-Zwecken an den Adobe Advertising-Server weiter, bevor sie an die Landingpage des Clients gesendet werden. Diese Methode verfügt über standardmäßige Tracking-Optionen, die Sie optional anpassen können, und Sie können auch Parameter angeben, die an jede URL angehängt werden sollen.

Um diese Funktion zu aktivieren, aktivieren Sie **[Tracking aktivieren]**.

>[!NOTE]
>
>* Wenn Sie diese Einstellung ändern, müssen Sie die Tracking-URLs für das Konto neu generieren.
>* Tracking-Optionen auf Kampagnenebene setzen Einstellungen auf Kontoebene außer Kraft.

**[!UICONTROL Tracking Type]:** (Wenn das Tracking in Search, Social und Commerce aktiviert ist) Die Methode der Weiterleitung von Endbenutzenden an die endgültige URL oder Ziel-URL. Die ausgewählte Option gilt für alle Gebotseinheiten im Konto oder in der Kampagne. Die Standardeinstellung auf Kontoebene wird von den Tracking-Einstellungen des Advertisers übernommen, und die Standardeinstellung auf Kampagnenebene wird von den Kontoeinstellungen übernommen.

* *[!UICONTROL Standard]:*, um den Endbenutzer an die angegebene URL weiterzuleiten.

* *[!UICONTROL Token]:* Um den Endbenutzer zur URL umzuleiten und auch die ID für Suche, Social und Commerce für den Klick (`ef_id`) als Abfragezeichenfolgenparameter aufzuzeichnen, der als Token verwendet wird. Wählen Sie diese Option aus, wenn Sie Offline-Transaktionen melden, Search, Social und Commerce Daten mit Adobe Analytics austauschen sollen oder alle Konversionen verfolgen möchten, die in [!DNL Apple Safari] Browsern auftreten.

>[!NOTE]
>
>* Wenn Sie von [!UICONTROL Standard] zu [!UICONTROL Token] oder umgekehrt wechseln, müssen Sie die Tracking-URLs für das Konto neu generieren.
>* Die Einstellung auf Kontoebene kann auf Kampagnenebene außer Kraft gesetzt werden.

**[!UICONTROL Auto Update]:** (Wenn das Tracking in Search, Social und Commerce aktiviert ist) Standardisiert Ihre Tracking-URLs für die Kompatibilität zwischen Browsern und Servern. Search, Social und Commerce laden bei der nächsten Synchronisierung automatisch Folgendes in das Werbenetzwerk hoch: (a) Tracking-Parameter für Suche, Social und Commerce für Tracking-Vorlagen und dieselben Parameter, die an die endgültigen URLs angehängt werden, oder (b) neue Ziel-URLs, die in den Tracking-Code für Search, Social und Commerce eingebettet sind. Für Werbetreibende mit einer [Adobe Advertising-Adobe Analytics-Integration](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) und einer serverseitigen AMO-ID-Konfiguration (s_kwcid) enthält der Upload auch [AMO-ID-Parameter](/help/integrations/analytics/ids.md#amo-id) für Ihre [!DNL Google Ads]- und [!DNL Microsoft Advertising]. Die Standardeinstellung auf Kontoebene wird von den Tracking-Einstellungen des Advertisers übernommen. Die Einstellung auf Kontoebene kann auf Kampagnenebene außer Kraft gesetzt werden.

Tracking-URLs werden täglich nur für Entitäten aktualisiert, die nicht synchronisiert sind (d. h. neue hinzugefügte Entitäten und vorhandene Entitäten, deren Eigenschaften sich geändert haben). Wenn Sie diese Einstellung für einen vorhandenen Advertiser/ein vorhandenes Konto/eine vorhandene Kampagne von „Deaktiviert“ in „Aktiviert“ ändern, werden die Tracking-URLs daher nicht für vorhandene Entitäten aktualisiert, die bereits synchronisiert sind. Um den URLs vorhandener, synchronisierter Entitäten Tracking hinzuzufügen, wenden Sie sich an Ihr Adobe-Accountteam und fordern Sie einen einmaligen, manuellen Synchronisierungsprozess an. Zukünftige Änderungen werden durch den automatischen Upload-Prozess verarbeitet.

**[!UICONTROL URL Encoding]:** (Wenn das Tracking in Search, Social und Commerce aktiviert ist, nur Konten mit Ziel-URLs) Kodiert die Basis-URL in der Browser-Adressleiste des Endbenutzers (z. B. `%3D` anstelle von `=`):

**[!UICONTROL Tracking Level]:** (Wenn das Tracking nach Search, Social und Commerce aktiviert ist, auf Konto- und Kampagnenebene verfügbar; nicht anwendbar auf Werbenetzwerke, die für das parallele Tracking aktiviert sind) Die Ebene, auf der Klicks und Umsatz verfolgt werden sollen, indem eine Umleitung hinzugefügt und Parameter an die entsprechenden URLs angehängt werden:

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

**Konto-Tracking-URL**: (Nur [!DNL Google Ads]-, [!DNL LY Ads]- und [!DNL Microsoft Advertising]-Konten; optional) Die standardmäßige Tracking-Vorlage für das Konto, in der alle Umleitungen und Tracking-Parameter für Off-Landing-Domains angegeben und die endgültige/Landingpage-URL ebenfalls in einen Parameter eingebettet wird. Beispiel: `{lpurl}?source={network}&id=5` oder `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`, um eine Umleitung einzuschließen.

* Einbetten der endgültigen URL:

  * (Nur [!DNL Google Ads] und [!DNL Microsoft Advertising]) Eine Liste der Parameter zur Angabe der endgültigen URLs in Tracking-Vorlagen finden Sie in den Parametern (nur [!DNL Microsoft Advertising]) [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/3/en/56799) oder (nur [!DNL Google Ads]) den Parametern „Tracking-Vorlage nur“ im Abschnitt „Verfügbare [!DNL ValueTrack]&quot; in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/6305348).

  * (Nur [!DNL LY Ads]) Verwenden Sie den Parameter `!{lpurl}` , um die Landingpage-URL anzugeben.

* Sie können optional URL-Parameter und beliebige benutzerdefinierte Parameter einbeziehen, die für die Kampagne definiert wurden und durch kaufmännische Und-Zeichen (&amp;) getrennt sind, z. B. `{lpurl}?matchtype={matchtype}&device={device}`.

* Optional können Sie Umleitungen und Tracking von Drittanbietern hinzufügen.

* Wenn die Kampagneneinstellungen &quot;[!UICONTROL EF Redirect]&quot; und &quot;[!UICONTROL Auto Upload]&quot; enthalten, stellt Search, Social und Commerce beim Speichern des Datensatzes automatisch seinem eigenen Umleitungs- und Trackingcode das Präfix voran.

>[!NOTE]
>
>* Vermeiden Sie [!DNL Google Ads] die Verwendung von Makros, die nicht durch Klicks aus Quellen ersetzt werden, die paralleles Tracking ermöglichen. Wenn der Werbetreibende Makros verwenden muss, fügt das Adobe Account Team diese dem Kunden-Support oder dem Implementierungsteam hinzu.
>* Die Tracking-Vorlage auf der detailliertesten Ebene überschreibt die Werte auf allen höheren Ebenen. Wenn beispielsweise sowohl die Kontoeinstellungen als auch die Keyword-Einstellungen einen Wert enthalten, wird der Keyword-Wert angewendet.
>* Wenn Sie eine Tracking-Vorlage auf Anzeigen-, Sitelink- oder Keyword-Ebene aktualisieren, werden die entsprechenden Anzeigen erneut zur Überprüfung eingereicht. Sie können Ihre Tracking-Vorlagen auf Konto-, Kampagnen- oder Anzeigengruppenebene aktualisieren, ohne Ihre Anzeigen erneut zur Genehmigung einzureichen.

## Registerkarte [!UICONTROL Set up Adobe Analytics]

Diese Einstellungen sind für Werbetreibende mit einer -[[!DNL Adobe Analytics for Advertising]  verfügbar](/help/integrations/analytics/overview.md).

**[!UICONTROL Adobe Analytics Report Suite]:** (Optional) Eine oder mehrere Analytics Report Suites, an die Search, Social und Commerce Daten sendet, die über das Werbenetzwerk erfasst werden, einschließlich Entitätsklassifizierungen und Klickdaten für das Konto. Diese Funktion steht nur unterstützten Werbenetzwerken zur Verfügung.<!-- What are the repercussions of changing the suites? Timing of updated data? -->

Damit die Daten in den Report Suites angezeigt werden, muss entweder (a) die Server-seitige AMO-ID-Funktion für das Konto konfiguriert sein oder (b) die Einstellung auf Advertiser-Ebene auf &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; aktiviert sein. Darüber hinaus muss das [!DNL Analytics] des Werbetreibenden so konfiguriert sein, dass es Daten von Search, Social und Commerce empfängt. Weitere Informationen erhalten Sie von Ihrem Adobe Account Team.

**[!UICONTROL Adobe Analytics Conversion Reporting]: [!UICONTROL Enable conversion reporting in Adobe Analytics]:** ([!DNL Meta Ads] Konten; optional) Fügt den [AMO ID (s_kwcid)-Tracking-Parameter &#x200B;](/help/search-social-commerce/tracking/amo-id-tracking-parameter.md) allen Anzeigen in der Kampagne an. Der Parameter ermöglicht es Adobe Analytics, Konversionen mit Meta Ads-Kampagnen in der angegebenen Report Suite sowie mit den Entitätsklassifizierungen und Klickdaten zu verknüpfen.

>[!MORELIKETHIS]
>
>* [Über Werbenetzwerkkonten](../ad-network-account-about.md)
>* [Konten des Händlerzentrums verwalten](/help/search-social-commerce/new-ui/set-up/manager-account-manage.md)
>* [Aktualisieren des s_kwcid-Trackingcodes für ein [!DNL Google Ads] Konto](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
