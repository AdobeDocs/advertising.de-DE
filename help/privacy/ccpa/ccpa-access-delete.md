---
title: Adobe Advertising-Unterstützung für den California Consumer Privacy Act &#58; Unterstützung für Datenzugriff und -löschung von Verbrauchern
description: Erfahren Sie mehr über die unterstützten Datenanfragetypen, die erforderliche Einrichtung und die Feldwerte und Beispiele für API-Zugriffsanfragen mit älteren Produkt-IDs und zurückgegebenen Datenfeldern.
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Adobe Advertising-Unterstützung für den California Consumer Privacy Act: Unterstützung für den Zugriff auf und die Löschung von Verbraucherdaten

*Für [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; und Adobe Advertising DCO*

>[!IMPORTANT]
>
>Der Inhalt dieses Dokuments ist keine Rechtsberatung und soll die Rechtsberatung nicht ersetzen. Wenden Sie sich an Ihren Rechtsbeistand, um sich über den California Consumer Privacy Act zu informieren.

Der California Consumer Privacy Act (CCPA) ist das neue kalifornische Datenschutzgesetz, das am 1. Januar 2020 in Kraft tritt. Der CCPA gewährt Personen mit Wohnsitz in Kalifornien neue Rechte in Bezug auf ihre personenbezogenen Daten und erlegt bestimmten Unternehmen, die in Kalifornien Geschäfte tätigen, Datenschutzverpflichtungen auf. Der CCPA bietet Verbrauchern das Recht, auf ihre personenbezogenen Daten zuzugreifen und sie zu löschen sowie das Recht, bestimmte Aktivitäten abzuwählen, die als „Verkauf“ personenbezogener Daten an Dritte gelten.

Als Unternehmen legen Sie fest, welche personenbezogenen Daten Adobe Experience Cloud in Ihrem Namen verarbeitet und speichert.

Als Ihr Dienstleister unterstützt Adobe Advertising Ihr Unternehmen bei der Erfüllung seiner CCPA-Verpflichtungen, die für die Verwendung von Adobe Advertising-Produkten und -Services gelten, einschließlich der Verwaltung von Anfragen zum Zugriff auf und zur Löschung personenbezogener Daten und der Verwaltung von Anfragen zum Opt-out vom Verkauf personenbezogener Daten.

In diesem Dokument wird beschrieben, wie [!DNL Advertising Search, Social, & Commerce], Advertising Creative, Advertising DSP (Demand Side Platform) und [!DNL Advertising DCO] - als Dienstleister - die Rechte der Verbraucher auf Zugang zu personenbezogenen Daten und deren Löschung mithilfe der Adobe-[!DNL Experience Platform Privacy Service API] und -[!DNL Privacy Service UI] unterstützen.

Informationen dazu, wie Advertising DSP das Verbraucherrecht auf Opt-out vom Verkauf personenbezogener Daten unterstützt, finden Sie unter [Adobe Advertising-Unterstützung für den California Consumer Privacy Act: Verbraucher-Opt-out-Unterstützung](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

Weitere Informationen zu den Adobe Privacy Services für CCPA finden Sie im [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Unterstützte Datenanfragetypen für Adobe Advertising

Adobe Experience Platform bietet Unternehmen die Möglichkeit, die folgenden Aufgaben auszuführen:

* Greifen Sie auf Daten auf Cookie-Ebene oder Geräte-ID-Ebene eines Verbrauchers (für Anzeigen in Mobile Apps) in [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] oder [!DNL DCO] zu.
* Löschen von Daten auf Cookie-Ebene, die in [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] oder [!DNL DCO] gespeichert sind, für Verbraucher, die einen Browser verwenden, oder Löschen von Daten auf ID-Ebene, die in [!DNL DSP] gespeichert sind, für Verbraucher, die Apps auf Mobilgeräten verwenden.
* Überprüfen Sie den Status einer oder aller vorhandenen Anfragen.

## Erforderliches Setup zum Senden von Anfragen für Adobe Advertising

Um Anfragen zum Zugreifen auf und Löschen von personenbezogenen Daten von Verbrauchern von Adobe Advertising zu stellen, ist Folgendes erforderlich:

1. Stellen Sie eine JavaScript-Bibliothek bereit, um die Cookies Ihrer Kundinnen und Kunden abzurufen und zu entfernen. Dieselbe Bibliothek `AdobePrivacy.js` wird für alle Adobe Experience Cloud-Lösungen verwendet.

   >[!IMPORTANT]
   >
   >Anfragen an einige Experience Cloud-Lösungen erfordern nicht die JavaScript-Bibliothek, Anfragen an Adobe Advertising erfordern sie jedoch.

   Stellen Sie die Bibliothek auf der Web-Seite bereit, über die Ihre Kunden Zugriffs- und Löschanfragen senden können, z. B. das Datenschutzportal Ihres Unternehmens. Mit der -Bibliothek können Sie Adobe-Cookies abrufen (Namespace-ID: `gsurferID`), damit Sie diese Identitäten als Teil von Zugriffs- und Löschanfragen über die [!DNL Adobe Experience Platform Privacy Service API] senden können.

   Wenn der Kunde die Löschung personenbezogener Daten verlangt, löscht die Bibliothek auch das Cookie des Kunden aus dem Browser des Kunden.

   >[!NOTE]
   >
   >Das Löschen personenbezogener Daten unterscheidet sich vom Opt-out, das die Zielgruppenbestimmung eines Endbenutzers mit Zielgruppensegmenten stoppt. Wenn ein Verbraucher jedoch darum bittet, personenbezogene Daten aus [!DNL Creative], [!DNL DSP] oder [!DNL DCO] zu löschen, sendet die Bibliothek auch eine Anfrage an Adobe Advertising, um den Kunden vom Segment-Targeting abzumelden. Für Werbetreibende mit [!DNL Search, Social, & Commerce] empfehlen wir, Ihren Kunden einen Link zu [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse) bereitzustellen, in dem erläutert wird, wie Sie das Targeting von Zielgruppensegmenten deaktivieren können.

1. Identifizieren Sie Ihre Experience Cloud-Organisations-ID und stellen Sie sicher, dass sie mit Ihren Adobe Advertising-Konten verknüpft ist.

   Eine Experience Cloud-Organisations-ID ist eine 24-stellige alphanumerische Zeichenfolge, die an &quot;@AdobeOrg“ angehängt wird. Den meisten Experience Cloud-Kunden wurde eine Organisations-ID zugewiesen. Wenn Ihr Marketing-Team oder Ihr interner [!DNL Adobe]-Systemadministrator Ihre Organisations-ID nicht kennt oder nicht sicher ist, ob sie bereitgestellt wurde, wenden Sie sich an Ihr Adobe-Account-Team. Sie benötigen die Organisations-ID, um Anfragen an die Datenschutz-API unter Verwendung des `imsOrgID` Namespace zu senden.

   >[!IMPORTANT]
   >
   >Wenden Sie sich an den Adobe Advertising-Beauftragten Ihres Unternehmens, um zu bestätigen, dass alle Adobe Advertising-Konten Ihres Unternehmens - einschließlich [!DNL DSP]-Konten oder Werbekunden, [!DNL Search, Social, & Commerce]-Konten und [!DNL Creative]- oder [!DNL DCO]-Konten - mit Ihrer Experience Cloud-Organisations-ID verknüpft sind.

1. Verwenden Sie entweder die [Adobe Experience Platform Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (für automatisierte Anfragen) oder die [Privacy Service-Benutzeroberfläche](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=de) (für Ad-hoc-Anfragen), um Anfragen zum Zugriff auf und Löschen personenbezogener Daten im Namen von Verbrauchern an Adobe Advertising zu senden und den Status bestehender Anfragen zu überprüfen.

   Für Werbetreibende, die über eine Mobile App verfügen, um mit Kunden zu interagieren und Kampagnen mit [!DNL DSP] zu starten, müssen Sie die datenschutzfähigen Mobile SDKs zum Experience Cloud herunterladen. Mit den Mobile SDKs können Unternehmen Status-Flags zum Opt-out festlegen, die Geräte-ID des Verbrauchers abrufen (Namespace-ID: `deviceID`) und Anfragen an die Privacy Service-API senden. Für Ihre Mobile App ist die SDK-Version 4.15.0 oder höher erforderlich.

   Wenn Sie eine Privatkunden betreffende Zugriffsanfrage senden, gibt die Privacy Service-API die Verbraucherinformationen auf Grundlage des angegebenen Cookies oder der angegebenen Geräte-ID zurück, die Sie dann an den Privatkunden zurückgeben müssen.

   Wenn Sie eine Privatkunden betreffende Löschanfrage stellen, werden die Cookie-ID oder Geräte-ID sowie alle mit dem Cookie verbundenen Kosten-, Klick- und Umsatzdaten vom Server gelöscht.

   >[!NOTE]
   >
   >Wenn Ihr Unternehmen über mehrere Experience Cloud-Organisations-IDs verfügt, müssen Sie jeweils separate API-Anfragen senden. Sie können jedoch eine API-Anfrage an mehrere Adobe Advertising-Unterlösungen ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] und [!DNL DCO]) mit einem Konto pro Unterlösung senden.

Alle diese Schritte sind erforderlich, um Unterstützung von Adobe Advertising zu erhalten. Weitere Informationen zu diesen und anderen damit verbundenen Aufgaben, die Sie mit dem Adobe Experience Platform Privacy Service ausführen müssen, und wo Sie die erforderlichen Elemente finden, finden Sie unter [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Erforderliche Feldwerte beim Adobe Advertising von JSON-Anfragen

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*Ihre Experience Cloud-Organisations-ID*>

„Benutzer“:

* `"key":` &lt;*normalerweise der Name des Kunden*>

* `"action":` entweder `**access**` oder `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (gibt den [!DNL adCloud] Cookie-Bereich an)

   * `"value":` &lt;*der Wert der Cookie-ID des tatsächlichen Kunden, wie von`AdobePrivacy.js`* abgerufen>

* `"include": **adCloud**` (dies ist das [!DNL Adobe] Produkt, das für die Anfrage gilt)

* `"regulation": **ccpa**` (dies ist die Datenschutzverordnung, die für die Anfrage gilt)

## Beispiel einer von einem Verbraucher mit einer Adobe Advertising-Benutzer-ID gesendeten Anfrage, die von AdobePrivacy.js abgerufen wurde

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
    "regulation":"ccpa"
}
```

## Datenfelder, die für Zugriffsanfragen zurückgegeben werden

Im Folgenden finden Sie ein Beispiel für eine Antwort zum Zugriff auf personenbezogene Daten beim Adobe Advertising.

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
