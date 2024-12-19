---
title: Adobe Advertising-Unterstützung für die Datenschutz-Grundverordnung
description: Erfahren Sie mehr über die unterstützten Datenanfragetypen, die erforderliche Einrichtung und die Feldwerte und Beispiele für API-Zugriffsanfragen mit älteren Produkt-IDs und zurückgegebenen Datenfeldern
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---

# Adobe Advertising-Unterstützung für die Datenschutz-Grundverordnung

*Für [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; und Adobe Advertising DCO*

>[!IMPORTANT]
>
>Der Inhalt dieses Dokuments ist keine Rechtsberatung und soll die Rechtsberatung nicht ersetzen. Beraten Sie sich bei Fragen zur Datenschutz-Grundverordnung mit Ihrem Rechtsbeistand.

Die Datenschutz-Grundverordnung (DSGVO), ein Gesetz, das am 25. Mai 2018 in Kraft ist, gibt allen Personen (betroffenen Personen) innerhalb der Grenzen der Europäischen Union (EU) die Kontrolle über ihre personenbezogenen Daten und vereinfacht das rechtliche Umfeld für internationale Unternehmen. Dieses Gesetz gilt für alle Unternehmen (Datenverantwortliche), die zum Zeitpunkt der Verarbeitung personenbezogener Daten innerhalb der EU Waren oder Dienstleistungen anbieten, um das Verhalten von Personen zu überwachen oder personenbezogene Daten von ihnen zu sammeln, unabhängig vom Unternehmensstandort des Datenverantwortlichen.

Adobe Experience Cloud fungiert als Auftragsverarbeiter für personenbezogene Daten, die es im Namen seiner Kunden erhält und speichert. Als Datenverantwortlicher bestimmen Sie die personenbezogenen Daten, die Adobe Experience Cloud in Ihrem Auftrag verarbeitet und speichert.

In diesem Dokument wird beschrieben, wie [!DNL Advertising Search, Social, & Commerce], Advertising Creative, Advertising DSP (Demand Side Platform) und [!DNL Advertising DCO] die DSGVO-Rechte der betroffenen Personen zum Datenzugriff und zur Löschung über die Adobe Experience Platform Privacy Service-API und die Privacy Service-Benutzeroberfläche unterstützen.

Weitere Informationen dazu, was die DSGVO für Ihr Unternehmen bedeutet, finden Sie unter [DSGVO und Ihr Unternehmen](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Unterstützte Datenanfragetypen für Adobe Advertising

Adobe Experience Platform bietet Unternehmen die Möglichkeit, die folgenden Aufgaben auszuführen:

* Greifen Sie auf Daten auf Cookie-Ebene oder Geräte-ID-Ebene einer betroffenen Person (für Anzeigen in Mobile Apps) in [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] oder [!DNL DCO] zu.
* Löschen von Daten auf Cookie-Ebene, die in [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] oder [!DNL DCO] gespeichert sind, für betroffene Personen mithilfe eines Browsers oder Löschen von Daten auf ID-Ebene, die in [!DNL DSP] gespeichert sind, für betroffene Personen, die Mobile Apps auf Mobilgeräten verwenden.
* Überprüfen Sie den Status einer oder aller vorhandenen Anfragen.

## Erforderliches Setup zum Senden von Anfragen für Adobe Advertising

Um Anfragen zum Zugreifen auf und Löschen von Daten für Adobe Advertising zu stellen, ist Folgendes erforderlich:

1. Stellen Sie eine JavaScript-Bibliothek bereit, um Ihre Cookies von betroffenen Personen abzurufen und zu entfernen. Dieselbe Bibliothek `AdobePrivacy.js` wird für alle Adobe Experience Cloud-Lösungen verwendet.

   >[!IMPORTANT]
   >
   >Anfragen an einige Experience Cloud-Lösungen erfordern nicht die JavaScript-Bibliothek, Anfragen an Adobe Advertising erfordern sie jedoch.

   Stellen Sie die Bibliothek auf der Webseite bereit, von der aus Ihre betroffenen Personen Zugriffs- und Löschanfragen senden können, z. B. das Datenschutzportal Ihres Unternehmens. Mit der -Bibliothek können Sie [!DNL Adobe]-Cookies abrufen (Namespace-ID: `gsurferID`), damit Sie diese Identitäten als Teil von Zugriffs- und Löschanfragen über die Adobe Experience Platform Privacy Service-API übermitteln können.

   Wenn die betroffene Person die Löschung personenbezogener Daten verlangt, löscht die Bibliothek auch das Cookie der betroffenen Person aus dem Browser der betroffenen Person.

   >[!NOTE]
   >
   >Das Löschen personenbezogener Daten unterscheidet sich vom Opt-out, das die Zielgruppenbestimmung eines Endbenutzers mit Zielgruppensegmenten stoppt. Wenn eine betroffene Person jedoch darum bittet, personenbezogene Daten aus [!DNL Creative], [!DNL DSP] oder [!DNL DCO] zu löschen, sendet die Bibliothek auch eine Anfrage an Adobe Advertising, um die betroffene Person vom Segment-Targeting auszuschließen. Für Werbetreibende mit [!DNL Search, Social, & Commerce] empfehlen wir, den betroffenen Personen einen Link zu [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html) bereitzustellen, in dem erläutert wird, wie Sie das Targeting von Zielgruppensegmenten deaktivieren können.

1. Identifizieren Sie Ihre Experience Cloud-Organisations-ID und stellen Sie sicher, dass sie mit Ihren Adobe Advertising-Konten verknüpft ist.

   Eine Experience Cloud-Organisations-ID ist eine 24-stellige alphanumerische Zeichenfolge, die an &quot;@AdobeOrg“ angehängt wird. Den meisten Experience Cloud-Kunden wurde eine Organisations-ID zugewiesen. Wenn Ihr Marketing-Team oder Ihr interner [!DNL Adobe]-Systemadministrator Ihre Organisations-ID nicht kennt oder nicht sicher ist, ob sie bereitgestellt wurde, wenden Sie sich unter gdprsupport@adobe.com an die Adobe-Kundenunterstützung. Sie benötigen die Organisations-ID, um Anfragen an die Datenschutz-API unter Verwendung des `imsOrgID` Namespace zu senden.

   >[!IMPORTANT]
   >
   >Wenden Sie sich an den Adobe Advertising-Beauftragten Ihres Unternehmens, um zu bestätigen, dass alle Adobe Advertising-Konten Ihres Unternehmens - einschließlich [!DNL DSP]-Konten oder Werbekunden, [!DNL Search, Social, & Commerce]-Konten und [!DNL Creative]- oder [!DNL DCO]-Konten - mit Ihrer Experience Cloud-Organisations-ID verknüpft sind.

1. Verwenden Sie entweder die [Adobe Experience Platform Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (für automatisierte Anfragen) oder die [Privacy Service-Benutzeroberfläche](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=de) (für Ad-hoc-Anfragen), um im Namen der betroffenen Personen Zugriffs- und Löschanfragen an Adobe Advertising zu senden und den Status bestehender Anfragen zu überprüfen.

   Für Werbetreibende, die über eine mobile App verfügen, um mit betroffenen Personen zu interagieren und Kampagnen mit DSP zu starten, müssen Sie die datenschutzfähigen Mobile SDKs zum Experience Cloud herunterladen. Mit den Mobile SDKs können Datenverantwortliche Status-Flags zum Opt-out festlegen, die Geräte-ID der betroffenen Person abrufen (Namespace-ID: `deviceID`) und Anfragen an die Privacy Service-API senden. Für Ihre Mobile App ist die SDK-Version 4.15.0 oder höher erforderlich.

   Wenn Sie die Zugriffsanfrage einer betroffenen Person senden, gibt die Privacy Service-API die Informationen der betroffenen Person basierend auf dem angegebenen Cookie oder der Geräte-ID zurück, die Sie dann an die betroffene Person zurückgeben müssen.

   Wenn Sie die Löschanfrage einer betroffenen Person senden, werden die Cookie-ID oder Geräte-ID sowie alle mit dem Cookie verbundenen Kosten-, Klick- und Umsatzdaten vom Server gelöscht.

   >[!NOTE]
   >
   >Wenn Ihr Unternehmen über mehrere Experience Cloud-Organisations-IDs verfügt, müssen Sie jeweils separate API-Anfragen senden. Sie können jedoch eine API-Anfrage an mehrere Adobe Advertising-Unterlösungen ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] und [!DNL DCO]) mit einem Konto pro Unterlösung senden.

Alle diese Schritte sind für das Adobe Advertising erforderlich. Weitere Informationen zu diesen und anderen damit verbundenen Aufgaben, die Sie mit dem Adobe Experience Platform Privacy Service ausführen müssen, und wo Sie die erforderlichen Elemente finden, finden Sie unter &quot;[Übersicht über den Privacy Service ](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)&quot;.

## Erforderliche Feldwerte beim Adobe Advertising von JSON-Anfragen

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*Ihre Experience Cloud-Organisations-ID*>

`"users":`

* `"key":` &lt;*normalerweise der Name der betroffenen Person*>

* `"action":` entweder `**access**` oder `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (gibt den [!DNL adcloud] Cookie-Bereich an)

   * `"value":` &lt;*Der Wert der Cookie-ID der betroffenen Person, wie von`AdobePrivacy.js`* abgerufen>

* `"include": **adCloud**` (dies ist das [!DNL Adobe] Produkt, das für die Anfrage gilt)

* `"regulation": **gdpr**` (dies ist die Datenschutzverordnung, die für die Anfrage gilt)

## Beispiel einer von einer betroffenen Person mit einer Adobe Advertising-Benutzer-ID gesendeten Anfrage, die von `AdobePrivacy.js` abgerufen wurde

```
{
"companyContexts":[
    {
        "namespace":"imsOrgID",
        "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
 "userIDs":[
      { 
        "namespace":"411",
        "value":"Wqersioejr-wdg",
        "type":"namespaceId",
        "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"gdpr"
}
```

## Datenfelder, die für Zugriffsanfragen zurückgegeben werden

Im Folgenden finden Sie ein Beispiel für eine Zugriffsantwort für Adobe Advertising.

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
