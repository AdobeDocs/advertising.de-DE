---
title: Adobe Advertising-Unterstützung für den California Consumer Privacy Act &#58; Consumer Opt-Out-of-Sale-Support
description: Erfahren Sie mehr über die Unterstützung für die Erfassung von Opt-out-Anfragen von Verbrauchern.
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%

---

# Adobe Advertising-Unterstützung für den California Consumer Privacy Act: Consumer Opt-out of Sale Support

*Für Adobe Advertising-Demand Side Platform (DSP)*

>[!IMPORTANT]
>
>Der Inhalt dieses Dokuments ist keine Rechtsberatung und soll keine Rechtsberatung ersetzen. Wenden Sie sich an Ihren Rechtsbeistand, um Ratschläge zum California Consumer Privacy Act zu erhalten.

Der California Consumer Privacy Act (CCPA) ist das neue kalifornische Datenschutzgesetz, das am 1. Januar 2020 in Kraft tritt. Der CCPA gibt in Kalifornien ansässigen Personen neue Rechte in Bezug auf ihre personenbezogenen Daten und verpflichtet bestimmte in Kalifornien tätige Unternehmen zur Einhaltung von Datenschutzvorschriften. Der CCPA bietet Verbrauchern das Recht, auf ihre Daten zuzugreifen und sie zu löschen sowie bestimmte Aktivitäten, die als &quot;Verkauf&quot;personenbezogener Daten an Dritte gelten, abzuwählen.

Als Unternehmen legen Sie fest, welche personenbezogenen Daten Adobe Experience Cloud in Ihrem Namen verarbeitet und speichert.

Als Ihr Dienstleister unterstützt Adobe Advertising Ihr Unternehmen bei der Erfüllung seiner CCPA-Verpflichtungen, die für die Verwendung von Adobe Advertising-Produkten und -Dienstleistungen gelten, einschließlich der Verwaltung von Verbraucheranfragen für den Zugriff auf und die Löschung personenbezogener Daten und der Verwaltung von Verbraucheranfragen, die den Verkauf personenbezogener Daten deaktivieren.

In diesem Dokument wird beschrieben, wie Adobe Advertising Demand Side Platform (DSP) als Dienstleister das Verbraucherrecht unterstützt, sich vom &quot;Verkauf&quot;von &quot;personenbezogenen Daten&quot;abzumelden, da jeder Begriff vom CCPA definiert wird. Er enthält Informationen dazu, wie Sie Adobe Advertising Opt-out-Kaufanfragen mitteilen und Berichte zu den Opt-out-Kaufanfragen Ihres Unternehmens abrufen können.

Informationen dazu, wie [!DNL Advertising Search, Social, & Commerce], Advertising Creative und [!DNL Advertising DCO] die Zugriffs- und Löschungsrechte von Verbrauchern für personenbezogene Daten unterstützen, finden Sie unter [Adobe Advertising-Unterstützung für den California Consumer Privacy Act: Consumer Data Access and Delete Support](/help/privacy/ccpa/ccpa-access-delete.md).

Weitere Informationen zu den Adobe-Datenschutzdiensten für CCPA finden Sie im [Datenschutzzentrum für Adobe](https://www.adobe.com/privacy/ccpa.html).

## Übermittlung von Opt-out-Anfragen von Verbrauchern an Adobe Advertising

Sie können Verbraucher-Opt-out-Anfragen für den Verkauf über eine der folgenden Methoden kommunizieren:

* ein in Advertising DSP erstelltes CCPA-Opt-out-Kaufsegment
* Adobe Experience Platform Privacy Service-API

### Methode 1: Kommunikation von CCPA-Opt-out-of-Sale-Anfragen mithilfe eines [!UICONTROL CCPA Opt-Out-of-Sale]-Segments in Advertising DSP

>[!NOTE]
>
>Benutzer bleiben unbegrenzt in CCPA-Opt-out-Segmenten.

1. Melden Sie sich unter [https://advertising.adobe.com/](https://advertising.adobe.com/) beim Konto des Advertisers in Advertising DSP an.
1. [Erstellen Sie ein CCPA-Opt-out-of-Sale-Segment und implementieren Sie das Segmentpixel, um die Opt-out-Anfragen zu erfassen.](/help/dsp/audiences/ccpa-opt-out-segment-create.md)

### Methode 2: Kommunikation von CCPA-Opt-out-of-Sale-Anfragen mithilfe der Adobe Experience Platform Privacy Service-API

*Advertiser haben nur eine Adobe Experience Cloud-Organisations-ID zugewiesen*

1. Stellen Sie eine JavaScript-Bibliothek bereit, um die Cookies Ihrer Kunden abzurufen. Dieselbe Bibliothek, `AdobePrivacy.js`, wird für alle Adobe Experience Cloud-Lösungen verwendet.

   >[!IMPORTANT]
   >
   >Für Anforderungen an einige Adobe Experience Cloud-Lösungen ist keine JavaScript-Bibliothek erforderlich, für Anfragen zum Adobe Advertising ist dies jedoch erforderlich.

   Sie sollten die -Bibliothek auf der Webseite bereitstellen, von der aus Ihre Kunden Opt-out-Kaufanfragen senden können, z. B. das Datenschutzportal Ihres Unternehmens. Die Bibliothek hilft Ihnen beim Abrufen von Adobe-Cookies (Namespace-ID: `gsurferID`), damit Sie diese Identitäten als Teil von Opt-out-Kaufanfragen über die Adobe Experience Platform Privacy Service-API senden können.

1. Identifizieren Sie Ihre Experience Cloud-Organisations-ID und stellen Sie sicher, dass sie mit Ihren Adobe Advertising-Konten verknüpft ist.

   Eine Experience Cloud-Organisations-ID ist eine 24-stellige alphanumerische Zeichenfolge, die an &quot;@AdobeOrg&quot;angehängt wird. Den meisten Experience Cloud-Kunden wurde eine Organisations-ID zugewiesen. Wenn Ihr Marketingteam oder Ihr Adobe-Systemadministrator Ihre Organisations-ID nicht kennen oder nicht sicher ist, ob die ID bereitgestellt wurde, wenden Sie sich an Ihr Adobe-Account-Team. Sie benötigen die Organisations-ID, um mithilfe des Namespace `imsOrgID` Anfragen an die Datenschutz-API zu senden.

   >[!IMPORTANT]
   >
   >Wenden Sie sich an den Adobe Advertising-Support-Mitarbeiter Ihres Unternehmens, um zu bestätigen, dass alle Adobe Advertising-Konten Ihres Unternehmens - einschließlich [!DNL DSP] Konten oder Advertiser, [!DNL Search, Social, & Commerce] Konten und [!DNL Creative] oder [!DNL DCO] Konten - mit Ihrer Experience Cloud-Organisations-ID verknüpft sind.

1. Verwenden Sie die Adobe Experience Platform Privacy Service-API, um [Opt-out-of-Sale-Anfragen](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) an Adobe Advertising im Namen von Verbrauchern zu senden und den Status vorhandener Anfragen zu überprüfen.

   Im folgenden Anhang finden Sie ein Beispiel für eine Opt-out-Kaufanfrage.

   >[!NOTE]
   >
   >Wenn Ihr Unternehmen über mehrere Experience Cloud-Organisations-IDs verfügt, müssen Sie für jede Datei separate API-Anfragen senden. Sie können jedoch eine API-Anfrage an mehrere Adobe Advertising-Unterlösungen ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] und [!DNL DCO]) mit einem Konto pro Unterlösung richten.

Alle diese Schritte sind erforderlich, um Unterstützung von Adobe Advertising zu erhalten. Weitere Informationen zu diesen und anderen damit zusammenhängenden Aufgaben, die Sie mit dem Adobe Experience Platform Privacy Service ausführen müssen, sowie dazu, wo Sie die erforderlichen Elemente finden, finden Sie unter [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Abrufen von Berichten von Verbrauchern, die Opt-out-Kaufanfragen eingereicht haben

Adobe Advertising generiert monatliche Berichte über IDs, die Kunden für Opt-out-Kaufanfragen für das Konto eingereicht haben. Jeder Bericht ist als tabulatorgetrennte Textdatei verfügbar, die in das GZIP-Format komprimiert ist. Die Daten konsolidieren Anforderungen, die mithilfe von CCPA-Opt-out-Kaufsegmenten erfasst wurden, die in Advertising DSP erstellt wurden, sowie alle über die Privacy Service-API durchgeführten Übermittlungen. In CCPA-Opt-out-Verkaufssegmenten erfasste Benutzer-IDs werden nach Segment und Advertiser identifiziert. Die Berichte werden am ersten eines jeden Monats für den Vormonat erstellt. Beispielsweise ist die monatliche Benutzerliste für Juni am 1. Juli verfügbar.

Sie können Links zu den monatlichen Berichten abrufen, die in den letzten drei Monaten erstellt wurden, entweder aus Advertising DSP oder mithilfe von Advertising DSP [!DNL Trafficking API]. Jeder Link ist sieben Tage lang gültig, wird jedoch jedes Mal aktualisiert, wenn ein Kunde versucht, ihn abzurufen.

### Methode 1: Abruf von Kundenabmeldeberichten innerhalb von Advertising DSP

1. Melden Sie sich unter [https://advertising.adobe.com/](https://advertising.adobe.com/) beim Konto des Advertisers in Advertising DSP an.
1. [Rufen Sie die Berichte ab](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Methode 2: Abrufen von Berichten zur Kundenabmeldung mit der Advertising DSP [!DNL Trafficking API]

Diese Funktion steht Unternehmen zur Verfügung, die den [!DNL Trafficking API] verwenden. Weitere Informationen finden Sie in der Dokumentation für den [!DNL Trafficking API] .<!-- Add link to API doc once it's published. -->

Wenn Ihr Unternehmen nicht die [!DNL Trafficking API] verwendet, aber an weiteren Informationen interessiert ist, wenden Sie sich an Ihr Adobe-Account-Team.

## Anhang: Beispiel [!UICONTROL CCPA Opt-Out-of-Sale] Anforderung für Privacy Service-API-Benutzer

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "adCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["adCloud"],
    "regulation": "ccpa"
}'
```

wobei:

* `"namespace": "adCloud"` gibt den Cookie-Bereich `adCloud` an und der entsprechende Wert ist die Cookie-ID des Kunden, wie von `AdobePrivacy.js` abgerufen.
* `"include": ["adCloud"]` gibt an, dass die Anforderung auf Adobe Advertising angewendet wird
