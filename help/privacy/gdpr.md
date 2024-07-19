---
title: Adobe Advertising Unterstützung für die Datenschutz-Grundverordnung
description: Erfahren Sie mehr über die unterstützten Datenanforderungstypen, die erforderliche Einrichtung und Feldwerte sowie Beispiele für API-Zugriffsanfragen mit alten Produkt-IDs und zurückgegebenen Datenfeldern
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---

# Adobe Advertising Unterstützung für die Datenschutz-Grundverordnung

*Für [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; und Adobe Advertising DCO*

>[!IMPORTANT]
>
>Der Inhalt dieses Dokuments ist keine Rechtsberatung und soll keine Rechtsberatung ersetzen. Wenden Sie sich an Ihren Rechtsbeistand, um Ratschläge zur Datenschutz-Grundverordnung zu erhalten.

Die Datenschutz-Grundverordnung (DSGVO), ein Gesetz, das am 25. Mai 2018 in Kraft trat, gibt allen Personen (betroffenen Personen) innerhalb der Grenzen der Europäischen Union (EU) die Kontrolle über ihre personenbezogenen Daten und vereinfacht das Regelungsumfeld für internationale Geschäfte. Dieses Gesetz gilt für alle Unternehmen (Datenverantwortliche), die zum Zeitpunkt der Verarbeitung ihrer personenbezogenen Daten Waren oder Dienstleistungen anbieten, das Verhalten von Personen überwachen oder personenbezogene Daten von Personen innerhalb der Grenzen der EU erfassen, unabhängig vom Geschäftsort des Datenverantwortlichen.

Adobe Experience Cloud fungiert als Datenverarbeiter für alle personenbezogenen Daten, die es im Namen seiner Kunden empfängt und speichert. Als Datenverantwortlicher legen Sie fest, welche personenbezogenen Daten Adobe Experience Cloud in Ihrem Namen verarbeitet und speichert.

In diesem Dokument wird beschrieben, wie [!DNL Advertising Search, Social, & Commerce], Advertising Creative, Advertising DSP (Demand Side Platform) und [!DNL Advertising DCO] die DSGVO-Datenzugriffs- und Löschungsrechte der betroffenen Personen mithilfe der Adobe Experience Platform Privacy Service-API und der Privacy Service-Benutzeroberfläche unterstützen.

Weitere Informationen dazu, was die DSGVO für Ihr Unternehmen bedeutet, finden Sie unter [DSGVO und Ihr Unternehmen](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Unterstützte Datentypen für Adobe Advertising

Adobe Experience Platform bietet Unternehmen die Möglichkeit, die folgenden Aufgaben auszuführen:

* Greifen Sie auf die Daten auf Cookie-Ebene oder auf Geräte-ID-Ebene (für Anzeigen in mobilen Apps) eines Datensubjekts innerhalb von [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] oder [!DNL DCO] zu.
* Löschen Sie Daten auf Cookie-Ebene, die in [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] oder [!DNL DCO] für Datensubjekte gespeichert sind, die einen Browser verwenden, oder löschen Sie Daten auf ID-Ebene, die in [!DNL DSP] für Datensubjekte gespeichert sind, die Apps auf Mobilgeräten verwenden.
* Überprüfen Sie den Status einer oder aller vorhandenen Anforderungen.

## Erforderliche Einrichtung zum Senden von Anforderungen an Adobe Advertising

Um Anfragen zum Zugreifen auf und Löschen von Daten für Adobe Advertising zu stellen, müssen Sie:

1. Stellen Sie eine JavaScript-Bibliothek bereit, um Cookies Ihrer Datensubjekte abzurufen und zu entfernen. Dieselbe Bibliothek, `AdobePrivacy.js`, wird für alle Adobe Experience Cloud-Lösungen verwendet.

   >[!IMPORTANT]
   >
   >Anforderungen an einige Experience Cloud-Lösungen erfordern nicht die JavaScript-Bibliothek, aber Anforderungen an Adobe Advertising erfordern sie.

   Sie sollten die Bibliothek auf der Webseite bereitstellen, von der aus die betroffenen Personen Zugriffs- und Löschanfragen senden können, z. B. das Datenschutzportal Ihres Unternehmens. Die Bibliothek hilft Ihnen beim Abrufen von [!DNL Adobe] -Cookies (Namespace-ID: `gsurferID`), damit Sie diese Identitäten als Teil von Zugriffs- und Löschanfragen über die Adobe Experience Platform Privacy Service-API senden können.

   Wenn die betroffene Person die Löschung personenbezogener Daten verlangt, löscht die Bibliothek auch das Cookie der betroffenen Person aus dem Browser der betroffenen Person.

   >[!NOTE]
   >
   >Das Löschen personenbezogener Daten unterscheidet sich vom Opt-out-Verfahren, das die Zielgruppenbestimmung eines Endbenutzers mit Zielgruppensegmenten stoppt. Wenn ein Datensubjekt jedoch darum bittet, personenbezogene Daten aus [!DNL Creative], [!DNL DSP] oder [!DNL DCO] zu löschen, sendet die Bibliothek auch eine Anfrage an die Adobe Advertising, die betroffene Person vom Segment-Targeting abzumelden. Für Advertiser mit [!DNL Search, Social, & Commerce] empfehlen wir, den Datensubjekten einen Link zu [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html) bereitzustellen, der erklärt, wie sie das Zielgruppensegment-Targeting deaktivieren können.

1. Identifizieren Sie Ihre Experience Cloud-Organisations-ID und stellen Sie sicher, dass sie mit Ihren Adobe Advertising-Konten verknüpft ist.

   Eine Experience Cloud-Organisations-ID ist eine 24-stellige alphanumerische Zeichenfolge, die an &quot;@AdobeOrg&quot;angehängt wird. Den meisten Experience Cloud-Kunden wurde eine Organisations-ID zugewiesen. Wenn Ihr Marketing-Team oder Ihr interner Systemadministrator Ihre Organisations-ID nicht kennen oder nicht sicher ist, ob die ID bereitgestellt wurde, wenden Sie sich an die Adobe-Kundenunterstützung unter gdprsupport@adobe.com. [!DNL Adobe] Sie benötigen die Organisations-ID, um mithilfe des Namespace `imsOrgID` Anfragen an die Datenschutz-API zu senden.

   >[!IMPORTANT]
   >
   >Wenden Sie sich an den Adobe Advertising-Support-Mitarbeiter Ihres Unternehmens, um zu bestätigen, dass alle Adobe Advertising-Konten Ihres Unternehmens - einschließlich [!DNL DSP] Konten oder Advertiser, [!DNL Search, Social, & Commerce] Konten und [!DNL Creative] oder [!DNL DCO] Konten - mit Ihrer Experience Cloud-Organisations-ID verknüpft sind.

1. Verwenden Sie entweder die [Adobe Experience Platform Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (für automatisierte Anfragen) oder die [Privacy Service-Benutzeroberfläche](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=de) (für Ad-hoc-Anfragen), um Zugriffs- und Löschanfragen an Adobe Advertising im Namen der Datensubjekte zu senden und den Status vorhandener Anfragen zu überprüfen.

   Für Advertiser, die über eine mobile App verfügen, um mit Datensubjekten zu interagieren und Kampagnen mit DSP zu starten, müssen Sie die datenschutzbereiten Mobile SDKs für die Experience Cloud herunterladen. Die Mobile SDK ermöglichen es den Datenverantwortlichen, Opt-out-Status-Flags festzulegen, die Geräte-ID des Datensubjekts abzurufen (Namespace-ID: `deviceID`) und Anfragen an die Privacy Service-API zu senden. Für Ihre Mobile App ist die SDK-Version 4.15.0 oder höher erforderlich.

   Wenn Sie die Zugriffsanfrage eines Datensubjekts senden, gibt die Privacy Service-API die Informationen des Datensubjekts basierend auf dem angegebenen Cookie oder der angegebenen Geräte-ID zurück, die Sie dann an das Datensubjekt zurückgeben müssen.

   Wenn Sie die Löschanfrage eines Datensubjekts senden, werden die Cookie-ID oder Geräte-ID sowie alle mit dem Cookie verbundenen Kosten-, Klick- und Umsatzdaten vom Server gelöscht.

   >[!NOTE]
   >
   >Wenn Ihr Unternehmen über mehrere Experience Cloud-Organisations-IDs verfügt, müssen Sie für jede Datei separate API-Anfragen senden. Sie können jedoch eine API-Anfrage an mehrere Adobe Advertising-Unterlösungen ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] und [!DNL DCO]) mit einem Konto pro Unterlösung richten.

Alle diese Schritte sind zum Adobe Advertising erforderlich. Weitere Informationen zu diesen und anderen damit zusammenhängenden Aufgaben, die Sie mit dem Adobe Experience Platform Privacy Service ausführen müssen, sowie dazu, wo Sie die erforderlichen Elemente finden, finden Sie unter &quot;[Übersicht über Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)&quot;.

## Erforderliche Feldwerte in Adobe Advertising-JSON-Anforderungen

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*Ihre Experience Cloud-Organisations-ID*>

`"users":`

* `"key":` &lt;*gewöhnlich der Name des Datensubjekts*>

* `"action":` entweder `**access**` oder `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (was den Cookie-Speicherplatz von [!DNL adcloud] angibt)

   * `"value":` &lt;*der Cookie-ID-Wert des Datensubjekts, der von`AdobePrivacy.js`*> abgerufen wurde

* `"include": **adCloud**` (was das [!DNL Adobe] -Produkt ist, das für die Anfrage gilt)

* `"regulation": **gdpr**` (die Datenschutzverordnung, die für die Anfrage gilt)

## Beispiel einer Anfrage, die von einer betroffenen Person mit einer Adobe Advertising-Benutzer-ID gesendet wurde, die von `AdobePrivacy.js` abgerufen wurde

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
