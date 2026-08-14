---
title: Fehlerbehebung bei Adobe Advertising-Daten in Customer Journey Analytics
description: Erfahren Sie, wie Sie Probleme mit Adobe Advertising-Daten in Customer Journey Analytics beheben.
feature: Integration with Adobe Customer Journey Analytics
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 3745130aae22ffa2e34c5c23276ed6d05ccdab93
workflow-type: tm+mt
source-wordcount: 3018
ht-degree: 0%

---

# Fehlerbehebung bei Adobe Advertising-Daten in Customer Journey Analytics

Im Folgenden finden Sie mögliche Probleme, deren mögliche Ursachen und Lösungen.

## Liste aller potenziellen Symptome

| Symptom | Weitere Informationen |
| ------- | ---------------- |
| Auf der Registerkarte „Netzwerk“ des Browsers sind keine Legierungsaufrufe sichtbar | Siehe Abschnitt &quot;[&#x200B; und Setup-Probleme](#issues-installation-setup)&quot; > &quot;[WebSDK-Erweiterung wird nicht initialisiert](#websdk-extension-doesn't-initialize)&quot; |
| Konsolenfehler: Legierung ist nicht definiert | Siehe &quot;[&#x200B; und Setup-Probleme](#issues-installation-setup)&quot; > &quot;[WebSDK-Erweiterung wird nicht initialisiert](#websdk-extension-doesn't-initialize)&quot; |
| Keine Interaktionen oder Sammelanfragen an edge.adobedc.net | Siehe &quot;[&#x200B; und Setup-Probleme](#issues-installation-setup)&quot; > &quot;[WebSDK-Erweiterung wird nicht initialisiert](#websdk-extension-doesn't-initialize)&quot; |
| Anfragen erreichen den Edge, geben aber 400 oder 500 Fehler zurück | Siehe Abschnitt &quot;[&#x200B; und Setup-Probleme](#issues-installation-setup)&quot; > &quot;[Datenstrom nicht konfiguriert oder falsch konfiguriert](#datastream-not-configured-or-misconfigured)&quot; |
| In Adobe Analytics- oder Adobe Advertising-Berichten werden keine Daten angezeigt | Siehe Abschnitt &quot;[&#x200B; und Setup-Probleme](#issues-installation-setup)&quot; > &quot;[Datenstrom nicht konfiguriert oder falsch konfiguriert](#datastream-not-configured-or-misconfigured)&quot; |
| Fehler in der Netzwerkantwort: „Datenstrom nicht gefunden“ | Siehe Abschnitt &quot;[&#x200B; und Setup-Probleme](#issues-installation-setup)&quot; > &quot;[Datenstrom nicht konfiguriert oder falsch konfiguriert](#datastream-not-configured-or-misconfigured)&quot; |
| Die Besucher-ID ändert sich zwischen den Seiten | Siehe Abschnitt &quot;[&#x200B; und Setup-Probleme](#issues-installation-setup)&quot; > &quot;[Identitäts- und ECID-Probleme](#identity-and-ecid-issues)&quot; |
| Advertising-Zielgruppensegmente stimmen nicht überein | Siehe Abschnitt &quot;[&#x200B; und Setup-Probleme](#issues-installation-setup)&quot; > &quot;[Identitäts- und ECID-Probleme](#identity-and-ecid-issues)&quot; |
| Der Debugger zeigt an, dass die Regelbedingungen nicht erfüllt sind | Siehe Abschnitt &quot;[&#x200B; und Setup-Probleme](#issues-installation-setup)&quot; > &quot;[Regeln oder Ereignisse werden nicht ausgelöst](#rules-or-events-aren't-firing)&quot; |
| Die [!UICONTROL Send Event] Aktion wird nie ausgeführt | Siehe Abschnitt &quot;[&#x200B; und Setup-Probleme](#issues-installation-setup)&quot; > &quot;[Regeln oder Ereignisse werden nicht ausgelöst](#rules-or-events-aren't-firing)&quot; |
| In [!DNL Tags] vorgenommene Änderungen werden nicht auf der Live-Site angezeigt | Siehe Abschnitt &quot;[&#x200B; und Setup-Probleme](#issues-installation-setup)&quot; > &quot;[Probleme beim Erstellen und Veröffentlichen von Bibliotheken](#library-build-and-publishing-issues)&quot; |
| Eine Aktualisierung der Erweiterung wurde angewendet, aber das alte Verhalten bleibt bestehen | Siehe Abschnitt &quot;[&#x200B; und Setup-Probleme](#issues-installation-setup)&quot; > &quot;[Probleme beim Erstellen und Veröffentlichen von Bibliotheken](#library-build-and-publishing-issues)&quot; |
| Der `alloy()` send-Ereignisaufruf ist erfolgreich (mit einer Antwort von 200), aber in den Berichten fehlen Adobe Advertising-Konversionsdaten | Siehe Abschnitt &quot;[&#x200B; und Setup-Probleme](#issues-installation-setup)&quot; > &quot;[Schemavalidierungsprobleme für Advertising-Felder](#schema-validation-for-advertising-fields)&quot; |
| Die XDM-Payload im Debugger zeigt kein `_experience.adcloud` Objekt an | Siehe Abschnitt &quot;[&#x200B; und Setup-Probleme](#issues-installation-setup)&quot; > &quot;[Schemavalidierungsprobleme für Advertising-Felder](#schema-validation-for-advertising-fields)&quot; |
| Für die Web-Seite werden keine Viewthrough- oder Clickthrough-Konversionen aufgezeichnet | Siehe Abschnitt &quot;[Setup-Probleme mit der Advertising-Erweiterung](#advertising-extension-setup-issues)&quot; |
| `_experience.adcloud` fehlt in der Experience-Datenmodell (XDM)-Payload für Clickthroughs | Siehe Abschnitt &quot;[Setup-Probleme mit der Advertising-Erweiterung](#advertising-extension-setup-issues)&quot; |
| Konvertierungen werden in einem Debugger-Tool bestätigt, werden jedoch nicht in Adobe Advertising-Berichten angezeigt | Siehe Abschnitt &quot;[Setup-Probleme mit der Advertising-Erweiterung](#advertising-extension-setup-issues)&quot; |

## Probleme mit der Installation und Einrichtung {#issues-installation-setup}

### WebSDK-Erweiterung initialisiert nicht. {#websdk-extension-doesn-initialize}

Symptome:

* Auf der Registerkarte „Netzwerk“ des Browsers sind keine Legierungsaufrufe sichtbar
* Konsolenfehler: Legierung ist nicht definiert
* Keine Interaktionen oder Sammelanfragen an edge.adobedc.net

+++ Bibliothek nicht veröffentlicht oder im Entwurfsstatus

Wechseln Sie zu [Veröffentlichungsablauf](https://experienceleague.adobe.com/de/docs/experience-platform/tags/publish/publishing-flow) und stellen Sie sicher, dass sich die Bibliothek, die die WebSDK-Erweiterung enthält, im Status Genehmigt/Veröffentlicht befindet.

+++

+++ Fehlende oder falsche Umgebung beim Einbettungs-Code

Stellen Sie sicher, dass der [!DNL Tags] Einbettungs-Code auf der Web-Seite auf die richtige Umgebung (Entwicklung/Staging/Produktion) verweist. Suchen Sie im `<head>`-Tag nach der Umgebung für das `//assets.adobedtm.com/...`-Skript-Tag.

+++

+++ Asynchrone vs. synchrone Last - Konflikt

Stellen Sie sicher, dass pro Web-Seite nur ein [!DNL Tags] Einbettungs-Code vorhanden ist. Doppelte Einbettungs-Codes verursachen Wettbewerbsbedingungen.

+++

+++ Sperrung von Content Security Policy (CSP)

Fügen Sie `edge.adobedc.net` und `assets.adobedtm.com` zu Ihren CSP-`connect-src` und `script-src` hinzu.

+++

### Datenstrom nicht oder falsch konfiguriert {#datastream-not-configured-or-misconfigured}

Symptome:

* Anfragen erreichen den Edge, geben aber 400 oder 500 Fehler zurück
* In Adobe Analytics- oder Adobe Advertising-Berichten werden keine Daten angezeigt<!-- It's not useful to organize this info by cause, not symptom -->
* Fehler in der Netzwerkantwort: „Datenstrom nicht gefunden“

+++ Die Datenstrom-ID für die Tag-Eigenschaft fehlt oder ist falsch

1. Öffnen Sie in [!DNL Tags] die [Datenstromkonfigurationseinstellungen](https://experienceleague.adobe.com/de/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams) für Ihre Tag-Eigenschaft.
1. Vergewissern Sie sich, dass das Feld [!UICONTROL Datastream] auf den richtigen Datenstrom für jede Umgebung (Entwicklung, Staging und Produktion) sowie auf das richtige Schema und den richtigen Datensatz verweist.

   Jede Umgebung sollte über einen eigenen Datenstrom verfügen, es sei denn, Sie geben explizit einen Datenstrom für alle drei Umgebungen frei.

+++

+++ Datenstrom-Services sind für die Tag-Eigenschaft nicht aktiviert

[Öffnen Sie die Datenstromeinstellungen](https://experienceleague.adobe.com/de/docs/experience-platform/datastreams/configure) und stellen Sie sicher, dass die folgenden Services aktiviert sind:

* Adobe Advertising (für Konvertierung/Zielgruppensynchronisierung)
* Adobe Experience Platform (für die Profilaufnahme)

+++

+++ Sandbox stimmt nicht überein

Stellen Sie sicher, dass der Datenstrom zur selben Adobe Experience Platform-Sandbox wie Ihr Schema und Ihr Datensatz gehört. Ein häufiger Fehler besteht darin, einen Datenstrom in der Produktions-Sandbox zu erstellen, aber Schemas auf die Entwicklungs-Sandbox zu verweisen.

+++

### Identitäts- und ECID-Probleme {#identity-and-ecid-issues}

Symptome:

* Die Besucher-ID ändert sich zwischen den Seiten
* Advertising-Zielgruppensegmente stimmen nicht überein

+++ Third-Party-Cookies werden blockiert

Migrieren Sie zur Erstanbieter-CNAME-Datenerfassung, indem Sie eine Erstanbieter-Domain in der Edge-Konfiguration des Datenstroms konfigurieren.

+++

+++ `idMigrationEnabled` ist auf `false` gesetzt, während ein Legacy-`s_ecid` vorhanden ist

Legen Sie in der WebSDK-Basiskonfiguration `idMigrationEnabled: true` fest, um die vorhandene ECID aus den `s_ecid` oder `AMCV_` Cookies zu migrieren.

+++

### Regeln oder Ereignisse werden nicht ausgelöst {#rules-or-events-arent-fire}

Symptome:

* Der Debugger zeigt an, dass die Regelbedingungen nicht erfüllt sind
* Die [!UICONTROL Send Event] Aktion wird nie ausgeführt

Überprüfen Sie Folgendes:

* Die Regel wird gespeichert und in den aktiven Bibliotheks-Build eingeschlossen.
* Der Ereignistyp entspricht dem tatsächlichen Seitenverhalten (z. B. [!UICONTROL Library Loaded] vs. [!UICONTROL DOM Ready] vs. [!UICONTROL Window Loaded]).
* Die Bedingungen der Regel sind nicht zu restriktiv. Testen Sie , indem Sie Bedingungen vorübergehend entfernen, um das Problem zu isolieren.
* Die Regelreihenfolge ist korrekt. Wenn mehrere Regeln dasselbe Ereignis gemeinsam haben, überprüfen Sie die Regelreihenfolge.
* Keine JavaScript-Fehler weiter oben auf der Seite stoppen die Ausführung. Überprüfen Sie die Browser-Konsole auf nicht erfasste Ausnahmen.

### Probleme beim Erstellen und Veröffentlichen von Bibliotheken {#library-build-and-publishing-issues}

Symptome:

* In [!DNL Tags] vorgenommene Änderungen werden nicht auf der Live-Site angezeigt
* Eine Aktualisierung der Erweiterung wurde angewendet, aber das alte Verhalten bleibt bestehen

+++ Änderungen wurden keiner Bibliothek hinzugefügt

Bestätigen Sie [!UICONTROL Publishing Flow], dass Ihre Änderungen zu einer Bibliothek in der Entwicklungsumgebung hinzugefügt wurden. Gehen Sie zu [!UICONTROL Libraries], öffnen Sie die Arbeitsbibliothek, wählen Sie **Alle geänderten Ressourcen hinzufügen** und klicken Sie dann auf **Speichern und erstellen**.

+++

+++ Der Browser speichert eine alte Bibliothek im Cache

Führen Sie eine harte Aktualisierung durch (Strg+Umschalt+R oder Befehl+Umschalt+R) oder öffnen Sie die Seite in einem inkognito/privaten Fenster. Löschen Sie den Browser-Cache vollständig, wenn das Problem weiterhin besteht.

+++

+++ Der Einbettungs-Code ist für die falsche Umgebung

Bestätigen Sie, dass der Einbettungs-Code auf der Seite der Produktions-Einbettungs-Code ist, wenn Sie das Produktionsverhalten testen.

+++

+++ Der Bibliotheks-Build ist im Hintergrund fehlgeschlagen

Wechseln Sie zu [!UICONTROL Publishing Flow] und überprüfen Sie, ob die Bibliothek einen [!UICONTROL Build Failed] Status aufweist. Öffnen Sie die Bibliothek und überprüfen Sie das Build-Protokoll. Häufige Ursachen sind ungültige Regelkonfigurationen oder Konflikte mit Erweiterungsversionen.

+++

### Probleme bei der Schemavalidierung für Advertising-Felder {#schema-validation-for-advertising-fields}

Symptome:

* Der `alloy()` send-Ereignisaufruf ist erfolgreich (mit einer Antwort von 200), aber in den Berichten fehlen Adobe Advertising-Konversionsdaten
* Die XDM-Payload im Debugger zeigt kein `_experience.adcloud` Objekt an

#### Schritt 1: Überprüfen Sie, ob die [!UICONTROL Advertising] Feldergruppe zum Schema hinzugefügt wird

1. Navigieren Sie zu Adobe Experience Platform > [!UICONTROL Data Management] > [!UICONTROL Schemas].
1. Öffnen Sie das von Ihrem Datenstrom verwendete Schema.
1. Bestätigen Sie im [!UICONTROL Field Groups], dass **Adobe Advertising Cloud ExperienceEvent Full Extension** aufgeführt ist.
1. Wenn sie fehlt, wählen Sie **Hinzufügen**, suchen Sie nach **Adobe Advertising Cloud**, wählen Sie **Adobe Advertising Cloud ExperienceEvent Full Extension** aus und klicken Sie dann auf **Speichern**.

>[!NOTE]
>Das erneute Veröffentlichen Ihrer [!DNL Tags]-Bibliothek ist nicht nur für Schemaänderungen erforderlich, sondern Sie müssen das XDM-Datenelement in [!DNL Tags] neu zuordnen, wenn neue Felder hinzugefügt wurden.

#### Schritt 2: Überprüfen Sie, ob die erforderlichen Adobe Advertising-Felder im Schema unter `_experience.adcloud.conversionDetails` vorhanden sind.

| Feldpfad | Typ | Beschreibung |
| ----- | --- | --- |
| `_experience.adcloud.conversionDetails.trackingCode` | Zeichenfolge | Ordnet die Konvertierung dem Ursprungs- und dem Klick zu. Befüllt aus dem `s_kwcid` Abfrageparameter in der Landingpage-URL. |
| `_experience.adcloud.conversionDetails.trackingIdentity` | Zeichenfolge | Speichert die eindeutige Identität und andere Details für das verfolgte Durchsichts- oder Clickthrough-Konversionsereignis. Befüllt aus dem `ef_id` Abfrageparameter in der Landingpage-URL. |

Wenn eines der Felder fehlt, stellen Sie sicher, dass die Feldergruppe **Adobe Advertising Cloud ExperienceEvent Full Extension** im Schema gespeichert wurde, und aktualisieren Sie dann den Schema-Editor.

#### Schritt 3: Bestätigen Sie, dass die Landingpage-URL Abfrageparameter enthält

Bei einem Anzeigen-Clickthrough muss die Landingpage-URL beide Abfrageparameter enthalten, z. B.:

`https://www.example.com/landing-page?s_kwcid=AL!12345!3!abc123&ef_id=abc123xyz:G:s`

| Fehlender Parameter | Wahrscheinliche Ursache |
| ----- | --- |
| `s_kwcid` | Das automatische Tagging ist in den Einstellungen für die Adobe Advertising-Suche oder die DSP-Kampagne nicht aktiviert. |
| `ef_id` | Die Landingpage-URL verwendet keine von Adobe Advertising getrackte Umleitung, oder das Anhängen der EF-ID ist in den Kampagneneinstellungen nicht aktiviert. |

#### Schritt 4: Ausgehende XDM-Payload validieren

Öffnen Sie den AEP Debugger oder die Registerkarte [!UICONTROL Network] im Browser, filtern Sie nach `edge.adobedc.net` und überprüfen Sie den Textkörper der Interaktionsanfrage. Eine gültige Clickthrough-Payload sieht etwa wie folgt aus:

```json
{
  "events": [{
    "xdm": {
      "eventType": "advertising.clicks",
      "_experience": {
        "adcloud": {
          "conversionDetails": {
            "trackingCode": "AL!12345!3!abc123",
            "trackingIdentity": "abc123xyz:G:s"
          }
        }
      }
    }
  }]
}
```

Wenn `trackingCode` oder `trackingIdentity` leer sind oder fehlen:

* Der Abfrageparameter war zum Zeitpunkt der Regelauslösung nicht auf der Seite vorhanden. Überprüfen Sie die URL und den Ereigniszeitpunkt der Regel.
* Die Feldergruppe fehlt im Schema. Gehen Sie wie oben beschrieben vor.

## Setup-Probleme bei [!UICONTROL Advertising]-Erweiterungen {#advertising-extension-setup-issues}

Symptome:

* Für die Web-Seite werden keine Viewthrough- oder Clickthrough-Konversionen aufgezeichnet.

  So überprüfen Sie, ob Konvertierungen aufgezeichnet wurden:

  1. Öffnen Sie die Web-Seite, wobei `ef_id=test&s_kwcid=test` an die URL angehängt wird.
  1. Öffnen Sie das Code-Inspektions-Tool Ihres Browsers (häufig als [!DNL Inspect] bezeichnet), öffnen Sie die Registerkarte [!DNL Network] und suchen Sie nach einem Interaktionsaufruf für event_type=„advertising.enrichment_ct“ aus Adobe Experience Platform.
  1. Öffnen Sie in der Datenerfassungsschnittstelle [Schemadefinition](https://experienceleague.adobe.com/de/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas) für die Website-Daten, die Sie erfassen möchten, und bestätigen Sie, dass `xdm->_experience->adcloud->conversionDetails->trackingCode` und `trackingIdentities` `ef_id` und `s_kwcid` enthalten.

* `_experience.adcloud` fehlt in der Experience-Datenmodell (XDM)-Payload für Clickthroughs.

* Konvertierungen werden in einem Debugger-Tool bestätigt, werden jedoch nicht in Adobe Advertising-Berichten angezeigt

+++ Der `Adobe Advertising`-Service ist für den Datenstrom nicht aktiviert

1. Öffnen Sie in [!DNL Tags] die [Datenstromkonfigurationseinstellungen](https://experienceleague.adobe.com/de/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams) für Ihre Tag-Eigenschaft.
1. Aktivieren Sie die folgenden Dienste und speichern Sie die Einstellungen:
   * Adobe Advertising (für Konvertierung/Zielgruppensynchronisierung)
   * Adobe Experience Platform (für die Profilaufnahme)

+++

+++ Die `Adobe Advertising`-Komponente ist für die [!UICONTROL WebSDK] nicht aktiviert

Die `Adobe Advertising` innerhalb der WebSDK-Erweiterung ist standardmäßig deaktiviert und muss explizit aktiviert werden, damit das Tracking für Adobe Advertising-Clickthroughs oder -Viewthroughs funktioniert, unabhängig davon, wie das XDM-Schema oder die Regeln konfiguriert sind.

1. Öffnen Sie in [!DNL Tags] die [Build-Optionen für die Eigenschaft in den Konfigurationseinstellungen von Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/de/docs/experience-platform/tags/extensions/client/web-sdk/configure/custom-build-components).
1. Aktivieren Sie die Komponente **Advertising** und speichern Sie die Einstellungen.
1. Bibliothek neu erstellen und erneut veröffentlichen.

+++

+++ Es werden nur Clickthrough-Konversionen aufgezeichnet. Durchsichtskonversionen werden nie angezeigt

Dies ist das erwartete Standardverhalten. Sobald die `Adobe Advertising` aktiviert ist, wird das Clickthrough-Tracking automatisch über die `s_kwcid` und `ef_id` URL-Abfrageparameter aktiviert. Das View-Through-Tracking ist standardmäßig deaktiviert und erfordert eine zusätzliche Konfiguration — siehe nächstes Element.

+++

+++ View-Through-Tracking ist nicht aktiviert oder konfiguriert

1. Aktivieren des Adobe Advertising-Service für den Datenstrom:
   1. Gehen Sie in Adobe Experience Platform zu [!UICONTROL Data Collection] > [!UICONTROL Datastreams] und öffnen Sie den von Ihrer [!DNL Tags]-Eigenschaft verwendeten Datenstrom.
   1. Wählen Sie **Service hinzufügen**, wählen Sie **Adobe Advertising** und **Adobe Experience Platform** aus und klicken Sie dann auf **Speichern**.
1. Konfigurieren von Advertisern in Adobe Advertising DSP:
   1. Navigieren Sie in [!DNL Tags] zu [!UICONTROL Extensions] > [!UICONTROL Installed] > **Adobe Experience Platform Web SDK** > [!UICONTROL Configure].
   1. Wählen Sie im Abschnitt [!UICONTROL Advertiser] einen Advertiser aus der Dropdown-Liste aus und aktivieren Sie ihn. Um mehrere Advertiser zu konfigurieren, wählen Sie **Advertiser hinzufügen** aus.
1. Stellen Sie sicher, dass durchsichtige Konvertierungspixel ausgelöst werden:
   1. Bestätigen Sie in AEP Debugger, dass der Interaktionsaufruf `stitchId` unter dem Feld `xdm.query` enthält.
   1. Bestätigen Sie auf der Registerkarte Browser-[!UICONTROL Network] , dass ein Ereignis vom Typ `advertising.enrichment` ausgelöst wird, das `stitchId` unter `xdm.query` enthält.

View-Through-Konversionen werden nur alle 30 Minuten ausgelöst, unabhängig von der Anzahl der Besuche. Wenn kein Interaktionsaufruf angezeigt wird, löschen Sie den Browser-Cache und versuchen Sie es erneut.

+++

+++ (Wenn nach dem Aufruf „Viewthrough-Interaktion“ keine Viewthrough-Ereignisse in Experience Platform ausgelöst werden) Der Advertiser wurde manuell eingegeben anstatt im Dropdown-Menü ausgewählt wurde

Wählen Sie den Advertiser aus dem Dropdown-Menü [!UICONTROL Advertiser] erneut aus, anstatt ihn manuell einzugeben.

+++

+++ (Wenn in Experience Platform nach dem Aufruf „Viewthrough-Interaktion“ keine Durchsichtsereignisse ausgelöst werden) wird mit dem Aufruf „Durchsichts-Interaktion“ keine Advertiser-ID gesendet

Vergewissern Sie sich, dass ein Advertiser im Abschnitt [!UICONTROL Advertiser] der WebSDK-Erweiterungskonfiguration konfiguriert und aktiviert ist, und erstellen Sie dann die Bibliothek neu und veröffentlichen Sie sie erneut.

+++

Bevor Sie ein Support-Ticket für Probleme bei der Einrichtung [!UICONTROL Advertising] Erweiterung öffnen, überprüfen Sie Folgendes:

* Die Services **Adobe Advertising** und **Adobe Experience Platform** werden zum Datenstrom hinzugefügt.
* Die Komponente **Adobe Advertising** ist in der WebSDK-Erweiterungskonfiguration aktiviert.
* Die Bibliothek wurde nach der Aktivierung der Komponente neu erstellt und erneut veröffentlicht.
* Für das Clickthrough-Tracking enthält die Landingpage-URL `s_kwcid` und `ef_id` für den Anzeigenklick.
* Für das View-Through-Tracking wird in Adobe Advertising DSP ein Advertiser mit der richtigen Advertiser-ID konfiguriert.
* Die WebSDK-Erweiterung ist Version 2.36.0 oder höher.

## Validierungs- und Debugging-Tools

### Adobe Experience Platform Debugger

Installieren Sie die [!DNL Adobe Experience Platform Debugger]-Erweiterung für [!DNL Chrome]. Er bietet:

* Eine Echtzeitansicht aller WebSDK-`alloy()`
* Datenstrom-ID und Umgebungsprüfung
* XDM-Payload-Überprüfung
* Edge Network-Anfrage- und -Antwortdetails

Schlüsselprüfungen im Debugger:

| Tabulator | Was zu überprüfen ist |
| ----- | --- |
| [!UICONTROL Summary] | Bestätigt, dass das WebSDK erkannt wird und die installierte Version anzeigt. |
| [!UICONTROL AEP Web SDK] | Zeigt jedes ausgelöste Ereignis, die vollständige XDM-Payload und die Edge-Antwort. |
| [!UICONTROL Adobe Advertising] | Bestätigt die AMO-ID-Erfassung und den XDM-Interaktionsaufruf mit dem `advertising.enrichment` Ereignistyp. |

### Browser-Registerkarte „Netzwerk“

Filtern Sie nach `edge.adobedc.net`, um unformatierte Edge-Anfragen zu überprüfen:

* Anfrage-URL: `https://[org-id].data.adobedc.net/ee/v2/interact`
* Methode: `POST`
* Status: `200` (fehlerfrei), `400` (fehlerhafte Payload) oder `500` (Server- oder Datenstromfehler)

Payload der Anfrage überprüfen auf:

* Die richtige `dataStreamId`
* Das Vorhandensein eines `xdm` mit den erwarteten Feldern
* Ein `identityMap` mit ausgefüllter ECID

### Konsolenvalidierung

Überprüfen Sie die installierte WebSDK-Version:

```js
window.alloy.version
```

Manuelles Trigger eines Testereignisses:

```js
alloy("sendEvent", {
  xdm: {
    eventType: "web.webpagedetails.pageViews",
    web: {
      webPageDetails: { name: "Test Page", URL: window.location.href }
    }
  }
}).then(result => console.log("Edge response:", result))
  .catch(err => console.error("Send event error:", err));
```

## Checkliste für die Schnellreferenz

Überprüfen Sie Folgendes, bevor Sie ein Support-Ticket öffnen:

* Die WebSDK-Erweiterung verwendet die neueste Version.
* Die Bibliothek wird veröffentlicht und der Einbettungs-Code ist für die Umgebung korrekt.
* Die Datenstrom-ID ist für Entwicklung, Staging und Produktion korrekt festgelegt.
* Alle erforderlichen Datenstrom-Services sind aktiviert.
* Die [!UICONTROL Advertising]-Komponente wird in der WebSDK-Erweiterungskonfiguration aktiviert und eine DSP Advertiser-ID wird konfiguriert.
* Das XDM-Schema umfasst die [!UICONTROL Advertising] Feldergruppe .
* Die [!UICONTROL Send Event]-Regel enthält eine Identitätszuordnung und wird für das richtige Ereignis ausgelöst.
* Keine CSP- oder Browser-Datenschutzeinstellungen blockieren Edge-Anfragen.
* Der AEP Debugger bestätigt, dass Ereignisse den Edge erreichen.
* Keine JavaScript-Fehler in der Browser-Konsole stoppen die Ausführung.
* Die **Adobe Advertising Cloud ExperienceEvent Full Extension**-Feldergruppe wird dem Schema hinzugefügt.
* `_experience.adcloud.conversionDetails.trackingCode` ist im Schema vorhanden.
* `_experience.adcloud.conversionDetails.trackingIdentity` ist im Schema vorhanden.
* Die Landingpage-URL enthält sowohl `s_kwcid` als auch `ef_id` Clickthrough.
* Der AEP Debugger bestätigt, dass `conversionDetails` in die ausgehende Payload eingefügt wird.

## Eskalationszeitpunkt

Eskalieren Sie an Ihr Adobe-Account-Team oder Ihr Engineering-Team, wenn:

* Edge-Anfragen geben nach der Validierung des Datenstroms persistente `500` zurück.
* [!UICONTROL Advertising] Konvertierungen werden im Debugger bestätigt, aber nach 24-48 Stunden nicht mehr in Berichten angezeigt.
* Eine WebSDK-Versionsaktualisierung führt eine Regression ein, die in der vorherigen Version nicht vorhanden war. Schließen Sie die spezifischen Versionsnummern in das Support-Ticket ein.

## Probleme beim Reporting

### Zusammenfassende Berichte

+++ In Customer Journey Analytics sind keine zusammenfassenden Berichtsdaten für Advertising DSP oder Advertising Search, Social und Commerce verfügbar.

Überprüfen Sie Folgendes:

* Customer Journey Analytics Workspace verweist auf die richtige Datenansicht.

* Der Feed von Adobe Advertising an Customer Journey Analytics ist aktiviert. Wenden Sie sich an Ihr Adobe-Accountteam.

* Ihre Adobe Advertising-Dimension/Ihr Klassifizierungs-/Lookup-Datensatz und Ihr Zusammenfassungsdatensatz sind in Ihrer Customer Journey Analytics-Verbindung enthalten.

* Ihre Adobe Advertising-Dimensionen und Zusammenfassungsmetriken sind in Ihrer Customer Journey Analytics-Datenansicht enthalten.

Wenn Sie alle oben genannten Einstellungen überprüfen, aber immer noch keine Zusammenfassungsdaten sehen, öffnen Sie ein Support-Ticket für Ihr Unternehmen unter [https://experienceleague.adobe.com/home?lang=de#support](https://experienceleague.adobe.com/home?lang=de&support-tab=home#support).

+++

+++ Zusammenfassende Berichtsdaten sind in Customer Journey Analytics für Advertiser 1 verfügbar, nicht jedoch für Advertiser 2.

Überprüfen Sie Folgendes:

* Der Feed von Adobe Advertising an Customer Journey Analytics ist für Advertiser 2 aktiviert. Wenden Sie sich an Ihr Adobe-Accountteam.

* Die Einstellung &quot;[!UICONTROL Backfill all existing data]&quot; ist für Ihre drei Datensätze (Dimension/Klassifizierung/Suche, Zusammenfassung und Ereignismetriken) in Ihrer Customer Journey Analytics-Verbindung aktiviert.

Wenn Sie alle oben genannten Bedingungen überprüfen, aber immer noch keine Zusammenfassungsdaten sehen, öffnen Sie ein Support-Ticket für Ihr Unternehmen unter [https://experienceleague.adobe.com/home?lang=de#support](https://experienceleague.adobe.com/home?lang=de&support-tab=home#support).

+++

+++ (Benutzer von Search, Social und Commerce) Zusammenfassende Berichtsdaten sind in Customer Journey Analytics für ein [!DNL Google Ads]-, [!DNL Meta Ads]- oder [!DNL Microsoft Advertising]-Konto verfügbar, jedoch nicht für ein anderes.

Stellen Sie sicher, dass der Feed von Adobe Advertising an Customer Journey Analytics für das spezifische Werbenetzwerkkonto aktiviert ist. Wenden Sie sich an Ihr Adobe-Accountteam.

Wenn der Feed für ein Konto aktiviert ist, aber immer noch keine Zusammenfassungsdaten angezeigt werden, öffnen Sie ein Support-Ticket für Ihr Unternehmen unter [https://experienceleague.adobe.com/home?lang=de#support](https://experienceleague.adobe.com/home?lang=de&support-tab=home#support). Fügen Sie die [!UICONTROL Account ID] für das Anzeigennetzwerkkonto ein.

+++

+++ Die Daten des Zusammenfassungsberichts in Customer Journey Analytics Workspace unterscheiden sich von den Daten in Advertising DSP oder Advertising Search, Social und Commerce oder für einige Kampagnen- und Kampagnenentitäten fehlen Zusammenfassungsdaten.

Überprüfen Sie Folgendes:

* Sie verwenden dieselben Datumsbereiche sowohl in [!DNL Workspace] als auch im Adobe Advertising-Bericht.

* Alle Filter und Segmente, die in [!DNL Workspace] und im Adobe Advertising-Bericht angewendet werden, verursachen keine Datenunterschiede.

* Der [!UICONTROL Time Zone] für Ihre Customer Journey Analytics-Datenansicht entspricht dem [[!UICONTROL Default Timezone] für Ihr Advertising DSP-Konto](/help/dsp/admin/user-own-profile-edit.md).

* Die Einstellung &quot;[!UICONTROL Backfill all existing data]&quot; ist für Ihre drei Datensätze (Dimension/Klassifizierung/Suche, Zusammenfassung und Ereignismetriken) in Ihrer Customer Journey Analytics-Verbindung aktiviert.

Wenn Sie sich einer Datendiskrepanz sicher sind, öffnen Sie ein Support-Ticket für Ihr Unternehmen unter [https://experienceleague.adobe.com/home?lang=de#support](https://experienceleague.adobe.com/home?lang=de&support-tab=home#support). Fügen Sie die [!UICONTROL Account ID] für das Anzeigennetzwerkkonto ein. Um Beweise für die Diskrepanz zu zeigen, fügen Sie Screenshots und Tabellen hinzu. Ihr Adobe-Konto-Team kann den Daten-Feed bei Bedarf nachträglich korrigieren, um die Diskrepanz zu beheben.

+++

### Reporting auf Ereignisebene

+++ Konversionsdaten (z. B. `Page Views`) sind für eine Reporting-Dimension (z. B. `Campaign`) in CJA Customer Journey Analytics Workspace nicht verfügbar.

Überprüfen Sie Folgendes, beginnend mit den Elementen mit den geringsten Überprüfungsbarrieren:

* Sie verwenden die richtige Datenansicht.

* Die entsprechenden Konversionsmetriken sind Web-/Online-Ereignisse, die Adobe Advertising Dimensionen zuordnen kann.

* Adobe Advertising verfolgt Clickthroughs und Viewthroughs auf der entsprechenden Site. <!-- Link to validation instructions in the user guide -->

* In der Customer Journey Analytics-Verbindung für den Klassifizierungsdatensatz sind die Werte für die [!DNL Key]- und [!DNL Matching Key] korrekt: [!DNL Key]: `Tracking Code` (_customername.adLens2.trackingCode), [!DNL Matching Key]: `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode)

* Der [!DNL Adobe Advertising]-Service wird dem Adobe Experience Platform-Datenstrom hinzugefügt, das zugeordnete Schema für den Datenstrom wird `XDM ExperienceEvent Schema` und die Feldergruppe `Adobe Advertising Cloud ExperienceEvent Full Extension` wird dem `XDM ExperienceEvent` hinzugefügt.

* Die Adobe Advertising-Einstellungen werden in der WebSDK-Erweiterung korrekt konfiguriert und veröffentlicht.

Wenn Sie alle oben genannten Einstellungen überprüfen, aber immer noch keine Konversionsdaten sehen, öffnen Sie ein Support-Ticket für Ihr Unternehmen unter [https://experienceleague.adobe.com/home?lang=de#support](https://experienceleague.adobe.com/home?lang=de&support-tab=home#support). Fügen Sie die [!UICONTROL Account ID] für das Anzeigennetzwerkkonto ein.

+++

<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

>[!MORELIKETHIS]
>
>* [Übersicht](overview.md)
>* [Adobe Advertising-IDs verwendet von [!DNL Customer Journey Analytics]](ids.md)
>* [Voraussetzungen](prerequisites.md)
>* [Einrichten von Datenerfassung, Datenübertragung und Reporting](set-up.md)
>* [Adobe Advertising-Metriken und -Dimensionen in Customer Journey Analytics](advertising-data-in-cja.md)
>* (Adobe Analytics-Benutzer) [Erfassen historischer Daten für AMO-IDs und EF-IDs zur Verwendung in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
