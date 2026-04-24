---
title: Adobe Advertising-Unterstützung für den California Consumer Privacy Act &#58; Unterstützung für den Zugriff auf und die Löschung von Verbraucherdaten
description: Erfahren Sie mehr über die unterstützten Datenanfragetypen, die erforderliche Einrichtung und die Feldwerte und Beispiele für API-Zugriffsanfragen mit älteren Produkt-IDs und zurückgegebenen Datenfeldern.
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
TQID: https://experienceleague.adobe.com/g7Klc5k3qEPYDKIbTmsQcnklUPVvbN6qqhXaHCHvn3A
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1111
ht-degree: 0%

---

# Adobe Advertising-Unterstützung für den California Consumer Privacy Act: Unterstützung für den Zugriff auf und die Löschung von Verbraucherdaten

*Für [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; und Adobe Advertising DCO*

>[!IMPORTANT]
>
>Der Inhalt dieses Dokuments ist keine Rechtsberatung und soll die Rechtsberatung nicht ersetzen. Wenden Sie sich an Ihren Rechtsbeistand, um sich über den California Consumer Privacy Act zu informieren.

Der California Consumer Privacy Act (CCPA) ist das neue kalifornische Datenschutzgesetz, das am 1. Januar 2020 in Kraft tritt. Der CCPA gewährt Personen mit Wohnsitz in Kalifornien neue Rechte in Bezug auf ihre personenbezogenen Daten und erlegt bestimmten Unternehmen, die in Kalifornien Geschäfte tätigen, Datenschutzverpflichtungen auf. Der CCPA bietet Verbrauchern das Recht, auf ihre personenbezogenen Daten zuzugreifen und sie zu löschen sowie das Recht, bestimmte Aktivitäten abzuwählen, die als „Verkauf“ personenbezogener Daten an Dritte gelten.

Als Unternehmen legen Sie fest, welche personenbezogenen Daten Adobe CX Enterprise in Ihrem Namen verarbeitet und speichert.

Als Ihr Dienstleister unterstützt Adobe Advertising Ihr Unternehmen bei der Erfüllung seiner CCPA-Verpflichtungen, die für die Verwendung von Adobe Advertising-Produkten und -Services gelten. Dazu gehört auch die Verwaltung von Anfragen zum Zugriff auf und zur Löschung personenbezogener Daten sowie die Verwaltung von Anfragen zum Opt-out vom Verkauf personenbezogener Daten.

In diesem Dokument wird beschrieben, wie [!DNL Advertising Search, Social, & Commerce], Advertising Creative, Advertising DSP (Demand Side Platform) und [!DNL Advertising DCO] - als Dienstleister - die Rechte der Verbraucher auf den Zugriff auf und die Löschung personenbezogener Daten mithilfe der Adobe-[!DNL Experience Platform Privacy Service API] und -[!DNL Privacy Service UI] unterstützen.

Informationen dazu, wie Advertising DSP das Verbraucherrecht auf Opt-out vom Verkauf personenbezogener Daten unterstützt, finden Sie unter [Adobe Advertising-Support für den California Consumer Privacy Act: Verbraucher-Opt-out vom Verkauf](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

Weitere Informationen zu den Adobe Privacy Services für CCPA finden Sie im [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Unterstützte Datenanfragetypen für Adobe Advertising

Adobe Experience Platform bietet Unternehmen die Möglichkeit, die folgenden Aufgaben auszuführen:

* Greifen Sie auf Daten auf Cookie-Ebene oder Geräte-ID-Ebene eines Verbrauchers (für Anzeigen in Mobile Apps) in [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] oder [!DNL DCO] zu.
* Löschen von Daten auf Cookie-Ebene, die in [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] oder [!DNL DCO] gespeichert sind, für Verbraucher, die einen Browser verwenden, oder Löschen von Daten auf ID-Ebene, die in [!DNL DSP] gespeichert sind, für Verbraucher, die Apps auf Mobilgeräten verwenden.
* Überprüfen Sie den Status einer oder aller vorhandenen Anfragen.

## Erforderliche Einrichtung zum Senden von Anfragen an Adobe Advertising

Um Anfragen zum Zugreifen auf und Löschen von personenbezogenen Daten von Verbrauchenden aus Adobe Advertising zu stellen, müssen Sie:

1. Stellen Sie eine JavaScript-Bibliothek bereit, um die Cookies Ihrer Kundinnen und Kunden abzurufen und zu entfernen. Dieselbe Bibliothek `AdobePrivacy.js` wird für alle Adobe CX Enterprise-Lösungen verwendet.

   >[!IMPORTANT]
   >
   >Für Anfragen an einige CX Enterprise-Lösungen ist keine JavaScript-Bibliothek erforderlich, für Anfragen an Adobe Advertising ist sie jedoch erforderlich.

   Stellen Sie die Bibliothek auf der Web-Seite bereit, über die Ihre Kunden Zugriffs- und Löschanfragen senden können, z. B. das Datenschutzportal Ihres Unternehmens. Mit der -Bibliothek können Sie Adobe-Cookies abrufen (Namespace-ID: `gsurferID`), damit Sie diese Identitäten als Teil von Zugriffs- und Löschanfragen über die [!DNL Adobe Experience Platform Privacy Service API] senden können.

   Wenn der Kunde die Löschung personenbezogener Daten verlangt, löscht die Bibliothek auch das Cookie des Kunden aus dem Browser des Kunden.

   >[!NOTE]
   >
   >Das Löschen personenbezogener Daten unterscheidet sich vom Opt-out, das die Zielgruppenbestimmung eines Endbenutzers mit Zielgruppensegmenten stoppt. Wenn ein Verbraucher jedoch darum bittet, personenbezogene Daten aus [!DNL Creative], [!DNL DSP] oder [!DNL DCO] zu löschen, sendet die Bibliothek auch eine Anfrage an Adobe Advertising, um den Kunden vom Segment-Targeting abzumelden. Für Werbetreibende mit [!DNL Search, Social, & Commerce] empfehlen wir, Ihren Kunden einen Link zu [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse) bereitzustellen, in dem erläutert wird, wie Sie das Targeting von Zielgruppensegmenten deaktivieren können.

1. Identifizieren Sie Ihre CX Enterprise-Organisations-ID und stellen Sie sicher, dass sie mit Ihren Adobe Advertising-Konten verknüpft ist.

   Eine CX Enterprise-Organisations-ID ist eine 24-stellige alphanumerische Zeichenfolge, an die &quot;@AdobeOrg“ angehängt wird. Den meisten CX Enterprise-Kunden wurde eine Organisations-ID zugewiesen. Wenn Ihr Marketing-Team oder der interne [!DNL Adobe]-Systemadministrator Ihre Organisations-ID nicht kennt oder nicht sicher ist, ob sie bereitgestellt wurde, wenden Sie sich an Ihr Adobe-Account-Team. Sie benötigen die Organisations-ID, um Anfragen an die Datenschutz-API unter Verwendung des `imsOrgID` Namespace zu senden.

   >[!IMPORTANT]
   >
   >Wenden Sie sich an den Adobe Advertising-Support-Mitarbeiter Ihres Unternehmens, um zu bestätigen, dass alle Adobe Advertising-Konten Ihres Unternehmens - einschließlich [!DNL DSP]-Konten oder Werbekunden, [!DNL Search, Social, & Commerce]-Konten sowie [!DNL Creative]- oder [!DNL DCO]-Konten - mit Ihrer CX Enterprise-Organisations-ID verknüpft sind.

1. Verwenden Sie entweder die [Adobe Experience Platform Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (für automatisierte Anfragen) oder die [Privacy Service-Benutzeroberfläche](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=de) (für Ad-hoc-Anfragen), um Anfragen zum Zugriff auf und Löschen personenbezogener Daten an Adobe Advertising im Namen von Verbrauchern zu senden und den Status vorhandener Anfragen zu überprüfen.

   Für Werbetreibende, die über eine Mobile App verfügen, um mit Kunden zu interagieren und Kampagnen mit [!DNL DSP] zu starten, müssen Sie die datenschutzfähigen Mobile SDKs für CX Enterprise herunterladen. Mit den Mobile SDKs können Unternehmen Status-Flags zum Opt-out festlegen, die Geräte-ID des Verbrauchers abrufen (Namespace-ID: `deviceID`) und Anfragen an die Privacy Service-API senden. Für Ihre Mobile App ist die SDK-Version 4.15.0 oder höher erforderlich.

   Wenn Sie eine Privatkunden betreffende Zugriffsanfrage senden, gibt die Privacy Service-API die Verbraucherinformationen auf Grundlage des angegebenen Cookies oder der angegebenen Geräte-ID zurück, die Sie dann an den Privatkunden zurückgeben müssen.

   Wenn Sie eine Privatkunden betreffende Löschanfrage stellen, werden die Cookie-ID oder Geräte-ID sowie alle mit dem Cookie verbundenen Kosten-, Klick- und Umsatzdaten vom Server gelöscht.

   >[!NOTE]
   >
   >Wenn Ihr Unternehmen über mehrere CX Enterprise-Organisations-IDs verfügt, müssen Sie jeweils separate API-Anfragen senden. Sie können jedoch eine API-Anfrage an mehrere Adobe Advertising-Unterlösungen ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] und [!DNL DCO]) mit einem Konto pro Unterlösung senden.

Alle Schritte sind erforderlich, um Unterstützung von Adobe Advertising zu erhalten. Weitere Informationen zu diesen und anderen damit verbundenen Aufgaben, die Sie mit dem Adobe Experience Platform Privacy Service ausführen müssen, und wo Sie die erforderlichen Elemente finden, finden Sie unter [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Erforderliche Feldwerte in Adobe Advertising-JSON-Anfragen

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` *Ihre CX Enterprise-Organisations-ID*>

„Benutzer“:

* `"key":` *In der Regel der Name des Kunden*>

* `"action":` entweder `**access**` oder `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (gibt den [[!DNL AdCloud] Cookie-Bereich](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix) an)

   * `"value":` *Der Cookie-ID-Wert des tatsächlichen Kunden, wie er von`AdobePrivacy.js`* abgerufen wurde>

* `"include": **adCloud**` (d. h. das [[!DNL Adobe] Produkt](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix) das für die Anfrage gilt)

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

Im Folgenden finden Sie ein Beispiel für eine Antwort zum Zugriff auf personenbezogene Daten für Adobe Advertising.

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
                    "segmentName":"eXelate Australia Demographic - Jobs & Education - Job Seekers",
                    "segmentID":"2213789",
                    "serviceProvider":"exelate"
                }
            ]
        }
    }
}
```
