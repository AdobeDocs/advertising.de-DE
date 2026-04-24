---
title: Adobe Advertising-Unterstützung für den California Consumer Privacy Act &#58; Support zum Verbraucher-Opt-out vom Verkauf
description: Erfahren Sie mehr über die Unterstützung bei der Erfassung von Kaufabmeldungsanfragen von Kundinnen und Kunden.
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
TQID: https://experienceleague.adobe.com/16JkyKVsVoBIGKEbhEIH7HWZ-H-XkjBad7yq9-NhY3s
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1101
ht-degree: 0%

---

# Adobe Advertising-Unterstützung für den California Consumer Privacy Act: Unterstützung für Verbraucher-Opt-out vom Verkauf

*Für Adobe Advertising Demand Side Platform (DSP)*

>[!IMPORTANT]
>
>Der Inhalt dieses Dokuments ist keine Rechtsberatung und soll die Rechtsberatung nicht ersetzen. Wenden Sie sich an Ihren Rechtsbeistand, um sich über den California Consumer Privacy Act zu informieren.

Der California Consumer Privacy Act (CCPA) ist das neue kalifornische Datenschutzgesetz, das am 1. Januar 2020 in Kraft tritt. Der CCPA gewährt Personen mit Wohnsitz in Kalifornien neue Rechte in Bezug auf ihre personenbezogenen Daten und erlegt bestimmten Unternehmen, die in Kalifornien Geschäfte tätigen, Datenschutzverpflichtungen auf. Der CCPA bietet Verbrauchern das Recht, auf ihre Daten zuzugreifen und sie zu löschen sowie das Recht, sich gegen bestimmte Aktivitäten zu entscheiden, die als „Verkauf“ personenbezogener Daten an Dritte gelten.

Als Unternehmen legen Sie fest, welche personenbezogenen Daten Adobe CX Enterprise in Ihrem Namen verarbeitet und speichert.

Als Ihr Dienstleister unterstützt Adobe Advertising Ihr Unternehmen bei der Erfüllung seiner CCPA-Verpflichtungen, die für die Verwendung von Adobe Advertising-Produkten und -Services gelten. Dazu gehören die Verwaltung von Verbraucheranfragen zum Zugriff und zur Löschung personenbezogener Daten sowie die Verwaltung von Verbraucheranfragen zum Opt-out vom Verkauf personenbezogener Daten.

In diesem Dokument wird beschrieben, wie Adobe Advertising Demand Side Platform (DSP) als Dienstleister das Verbraucherrecht unterstützt, vom „Verkauf“ „personenbezogener Daten“ abzutreten, wie jeder Begriff vom CCPA definiert ist. Sie enthält Informationen darüber, wie Sie Adobe Advertising Opt-out-Anfragen mitteilen und wie Sie Berichte über die Opt-out-Anfragen Ihres Unternehmens abrufen können.

Informationen dazu, wie [!DNL Advertising Search, Social, & Commerce], Advertising Creative und [!DNL Advertising DCO] die Zugriffs- und Löschrechte für personenbezogene Daten von Verbrauchern unterstützen, finden Sie unter [Adobe Advertising-Unterstützung für den California Consumer Privacy Act: Unterstützung beim Zugriff auf und Löschen von Verbraucherdaten](/help/privacy/ccpa/ccpa-access-delete.md).

Weitere Informationen zu den Adobe Privacy Services für CCPA finden Sie im [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Mitteilung von Kaufabmeldeanfragen an Adobe Advertising

Sie können Anfragen zum Ausstieg aus dem Verkauf von Produkten an Verbraucher übermitteln, indem Sie eine der folgenden Möglichkeiten verwenden:

* ein in Advertising DSP erstelltes CCPA-Opt-out vom Verkauf
* die Adobe Experience Platform Privacy Service-API

### Methode 1: Kommunizieren von CCPA-Opt-out-Anfragen mithilfe eines [!UICONTROL CCPA Opt-Out-of-Sale] Segments in Advertising DSP

>[!NOTE]
>
>Benutzende bleiben auf unbestimmte Zeit in CCPA-Opt-out-of-Sale-Segmenten.

1. Melden Sie sich beim Konto des Werbetreibenden in Advertising DSP unter [https://advertising.adobe.com/](https://advertising.adobe.com/) an.

1. [Erstellen Sie ein CCPA-Opt-out vom Verkauf -Segment und implementieren Sie das Segmentpixel, um die Opt-out-Anfragen zu erfassen](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Methode 2: Kommunizieren von CCPA-Opt-out-Anfragen mithilfe der Adobe Experience Platform Privacy Service-API

*Werbetreibende haben nur eine Adobe CX Enterprise-Organisations-ID zugewiesen*

1. Stellen Sie eine JavaScript-Bibliothek bereit, um die Cookies Ihrer Kundinnen und Kunden abzurufen. Dieselbe Bibliothek `AdobePrivacy.js` wird für alle Adobe CX Enterprise-Lösungen verwendet.

   >[!IMPORTANT]
   >
   >Für Anfragen an einige Adobe CX Enterprise-Lösungen ist keine JavaScript-Bibliothek erforderlich, für Anfragen an Adobe Advertising ist sie jedoch erforderlich.

   Sie sollten die Bibliothek auf der Web-Seite bereitstellen, über die Ihre Kunden Opt-out-Kaufanfragen senden können, z. B. das Datenschutzportal Ihres Unternehmens. Mit der -Bibliothek können Sie Adobe-Cookies abrufen (Namespace-ID: `gsurferID`), damit Sie diese Identitäten als Teil von Opt-out-Kaufanfragen über die Adobe Experience Platform Privacy Service-API senden können.

1. Identifizieren Sie Ihre CX Enterprise-Organisations-ID und stellen Sie sicher, dass sie mit Ihren Adobe Advertising-Konten verknüpft ist.

   Eine CX Enterprise-Organisations-ID ist eine 24-stellige alphanumerische Zeichenfolge, an die &quot;@AdobeOrg“ angehängt wird. Den meisten CX Enterprise-Kunden wurde eine Organisations-ID zugewiesen. Wenn Ihr Marketing-Team oder der interne Adobe-Systemadministrator Ihre Organisations-ID nicht kennt oder nicht sicher ist, ob sie bereitgestellt wurde, wenden Sie sich an Ihr Adobe-Accountteam. Sie benötigen die Organisations-ID, um Anfragen an die Datenschutz-API unter Verwendung des `imsOrgID` Namespace zu senden.

   >[!IMPORTANT]
   >
   >Wenden Sie sich an den Adobe Advertising-Support-Mitarbeiter Ihres Unternehmens, um zu bestätigen, dass alle Adobe Advertising-Konten Ihres Unternehmens - einschließlich [!DNL DSP]-Konten oder Werbekunden, [!DNL Search, Social, & Commerce]-Konten sowie [!DNL Creative]- oder [!DNL DCO]-Konten - mit Ihrer CX Enterprise-Organisations-ID verknüpft sind.

1. Verwenden Sie die Adobe Experience Platform Privacy Service [API, um im Namen von Verbrauchern Opt-out-Kaufanfragen an Adobe Advertising &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html?lang=de) senden und den Status vorhandener Anfragen zu überprüfen.

   Ein Beispiel für eine Opt-out-Anfrage finden Sie im Anhang unten.

   >[!NOTE]
   >
   >Wenn Ihr Unternehmen über mehrere CX Enterprise-Organisations-IDs verfügt, müssen Sie jeweils separate API-Anfragen senden. Sie können jedoch eine API-Anfrage an mehrere Adobe Advertising-Unterlösungen ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] und [!DNL DCO]) mit einem Konto pro Unterlösung senden.

Alle diese Schritte sind erforderlich, um Unterstützung von Adobe Advertising zu erhalten. Weitere Informationen zu diesen und anderen damit verbundenen Aufgaben, die Sie mit dem Adobe Experience Platform Privacy Service ausführen müssen, und wo Sie die erforderlichen Elemente finden, finden Sie unter [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=de](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=de).

## Abrufen von Berichten von Verbrauchern, die Opt-out-Kaufanfragen eingereicht haben

Adobe Advertising generiert monatliche Berichte zu IDs, die Kunden für Opt-out-Kaufanfragen für das Konto gesendet haben. Jeder Bericht ist als tabulatorgetrennte Textdatei verfügbar, die im GZIP-Format komprimiert ist. Die Daten konsolidieren Anfragen, die mithilfe von in Advertising DSP erstellten CCPA-Opt-out-of-Sale-Segmenten erfasst wurden, sowie alle Übermittlungen, die über die Privacy Service-API erfolgen. In CCPA-Opt-out-of-Sale-Segmenten erfasste Benutzer-IDs werden nach Segment und Advertiser identifiziert. Berichte werden am ersten eines jeden Monats für den vorherigen Monat generiert. Beispielsweise ist die monatliche Benutzerliste für Juni am 1. Juli verfügbar.

Sie können Links zu den Monatsberichten abrufen, die in den letzten drei Monaten erstellt wurden, entweder aus Advertising DSP oder mithilfe der Advertising DSP-[!DNL Trafficking API]. Jeder Link ist sieben Tage lang gültig, wird jedoch jedes Mal aktualisiert, wenn ein Kunde versucht, einen abzurufen.

### Methode 1: Abrufen von Berichten zum Verbraucher-Opt-out vom Verkauf in Advertising DSP

1. Melden Sie sich beim Konto des Werbetreibenden in Advertising DSP unter [https://advertising.adobe.com/](https://advertising.adobe.com/) an.

1. [Berichte abrufen](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Methode 2: Abrufen von Opt-out-Verkaufsberichten von Verbrauchern mithilfe der Advertising DSP-[!DNL Trafficking API]

Diese Funktion steht Organisationen zur Verfügung, die die [!DNL Trafficking API] verwenden. Weitere Informationen finden Sie in der Dokumentation für die [!DNL Trafficking API].<!-- Add link to API doc once it's published. -->

Wenn Ihr Unternehmen die [!DNL Trafficking API] nicht verwendet, aber an weiteren Informationen interessiert ist, wenden Sie sich an Ihr Adobe Account Team.

## Anhang: Beispielanfrage [!UICONTROL CCPA Opt-Out-of-Sale] Privacy Service-API-Benutzende

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
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["adCloud"],
    "regulation": "ccpa"
}'
```

Dabei gilt gemäß den [Privacy Service-API-Spezifikationen](https://experienceleague.adobe.com/de/docs/experience-platform/privacy/api/appendix):

* `"namespace": "AdCloud"` gibt den `AdCloud` Cookie-Bereich an. Der entsprechende Wert ist die Cookie-ID des Kunden, wie sie von `AdobePrivacy.js` abgerufen wurde
* `"include": ["adCloud"]` gibt an, dass die Anfrage für das Produkt Adobe Advertising gilt
