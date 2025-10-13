---
title: Verwalten des Retargeting von Pixeln
description: Erfahren Sie, wie Sie Retargeting-Pixel erstellen und implementieren, die als Ziele für Anzeigenerlebnisse verwendet werden sollen.
feature: Creative Pixels
exl-id: dcd13c5a-315d-4380-99f9-6dbab3e1e1be
source-git-commit: ed3bf0200d3d3b31ef80c790c4e702914459c521
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 0%

---

# Verwalten des Retargeting von Pixeln

<!-- Note to self: These aren't segments -- we don't create a pool of users. -->

Sie können ein Retargeting-Pixel erstellen, um Besucher der Landingpages oder Konversionsseiten eines Advertisers mithilfe von Benutzer-Cookies oder universellen IDs zu identifizieren. Das Pixel verfolgt das jüngste Ereignis, das der Besucher auf einer Seite durchführt, und erfasst bestimmte Attribute, die die Seite für diese Besucher verfolgt. Generieren Sie nach dem Erstellen des Pixels ein Pixel-Tag, das Sie in die entsprechenden Web-Seiten einfügen können, um Besucher zu verfolgen.<!-- Note to self: surfer id=cookie or universal ID -->

Sie können dann das Pixel als Ziel für jedes kreative Element innerhalb eines Anzeigenerlebnisses verwenden, um Anzeigen nur Benutzern mit bestimmten Attributen anzuzeigen, die zuvor die mit dem Pixel verknüpften Web-Seiten besucht haben. Sie können beispielsweise Besucherinnen und Besucher, die rote Schuhe in Größe 10 betrachten, ansprechen, wenn die Web-Seiten diese Attributwerte verfolgen.<!-- better example? Make sure they match attribute examples below --> Die Zielgruppen auf Erlebnisebene werden in Verbindung mit den Zielgruppenbestimmungsoptionen Ihrer DSP angewendet. Das hierarchische Zielgruppenbestimmungsverhalten kann je nach DSP variieren.

Retargeting-Profile werden 180 Tage lang gespeichert.

Beispiel-Pixel:

```
<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--Insert ID5_PARTNER_ID--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--"></script>
```

>[!NOTE]
>
> * [!DNL Creative] unterstützt universelle IDs nur für Advertising DSP.
>* Sie können auch Ihre Erstanbieter-Zielgruppen aus Adobe Audience Manager und Adobe Analytics als [kreative Ziele für Ihre Erlebnisse“ &#x200B;](/help/creative/experiences/experience-settings-targeting.md).
>* Wenn Sie ein Erlebnis als Anzeige in einer Advertising DSP-Platzierung verwenden, können Sie die Platzierung auf alle Zielgruppen ausrichten, die Ihnen in DSP zur Verfügung stehen. Sie können auch [benutzerdefinierte Zielgruppensegment-Tags erstellen](/help/dsp/audiences/custom-segment-create.md) um alle Besucher bestimmter Landingpages zu verfolgen und diese Segmente dann als kreative Ziele für eine Platzierung zu verwenden. Advertising DSP wendet Targeting auf Anzeigenebene zusätzlich zum Targeting auf (nicht anstelle des Targeting auf Platzierungsebene an.
>* Website-Besuchende, die sich gegen das Tracking für das Anzeigen-Targeting entschieden haben, erhalten keine Anzeigen mit personalisierten kreativen Inhalten, die auf dem Zielgruppensegment oder dem Retargeting-Profil basieren.

## Erstellen eines Retargeting-Pixels

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Creative]** und wählen Sie dann > **[!UICONTROL Retargeting Pixel]** aus.

1. Geben Sie die [Einstellungen für Retargeting](#retargeting-pixel-settings) an.

1. Klicken Sie auf **[!UICONTROL Save]**.

1. [Pixel-Tag generieren](#retargeting-pixel-generate), das dem Advertiser oder Website-Kontakt bereitgestellt wird.

   Das Pixel-Tag für das Retargeting muss die letzte Aktion auf der Seite sein.<!-- verify here and below -->

   Möglicherweise muss die IT-Abteilung oder andere Gruppe des Werbetreibenden die Tag-Bereitstellung planen oder darüber informiert werden.

## Retargeting-Pixel bearbeiten

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Halten Sie den Cursor über den Pixelnamen und klicken Sie auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie die [Einstellungen für Retargeting-Pixel](#retargeting-pixel-settings).

1. Klicken Sie auf **[!UICONTROL Save]**.

1. [Pixel-Tag generieren](#retargeting-pixel-generate), das dem Advertiser oder Website-Kontakt bereitgestellt wird, damit er das ursprüngliche Tag ersetzen kann.

   Das Pixel-Tag für das Retargeting muss die letzte Aktion auf der Landingpage sein.

   Möglicherweise muss die IT-Abteilung oder andere Gruppe des Werbetreibenden die Tag-Bereitstellung planen oder darüber informiert werden.

## Tag für ein Retargeting-Pixel generieren {#retargeting-pixel-generate}

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Halten Sie den Cursor über den Pixelnamen und klicken Sie auf **[!UICONTROL Generate Tag]**.

1. Klicken Sie auf **[!UICONTROL Copy to Clipboard]** , um das Tag in die Zwischenablage Ihres Computers zu kopieren, von der aus Sie den Text in eine zu speichernde Datei einfügen können.

1. Geben Sie im Pixel-Tag einen Wert für jedes Attribut sowohl im `<img src>`- als auch im `<script src>`-Abschnitt an, indem Sie jedes &quot;`Insert <attribute>`&quot; durch einen Wert ersetzen. Geben Sie eine ID5-Partner-ID an, wenn das Tag eine universelle ID erfasst.

   Wenn Sie zusätzliche Attribute manuell hinzufügen, schließen Sie die URL-Codierung ein.

   Wenn Sie beispielsweise die Attribute „category“, „color“ und „size“ einbeziehen und universelle IDs der Kategorie „id5“ erfassen, enthält das Pixel-Tag die folgenden Parameter: `&ut1=--Insert category--&ut2=--Insert color--&ut3=--Insert size--` und `&id5pid=--Insert ID5_PARTNER_ID--`. Um Benutzer anzusprechen, die rote Sandalen in Größe 10 auswählen, ändern Sie die Parameter sowohl im Bild-Tag als auch im Skript-Tag in `&ut1=sandals&ut2=red&ut3=10` und geben Sie außerdem Ihre ID5-Partner-ID im Skript-Tag ein, z. B. `&id5pid=0123456789`.

   `<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--0123456789--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--"></script>`

1. Geben Sie dem Advertiser oder Website-Kontakt das ausgefüllte Pixel-Tag zusammen mit einer Liste der relevanten Landingpages, in die es eingefügt werden soll, an.

   Das Pixel-Tag für das Retargeting muss die letzte Aktion auf der Landingpage sein.

   Möglicherweise muss die IT-Abteilung oder andere Gruppe des Werbetreibenden die Tag-Bereitstellung planen oder darüber informiert werden.

## Löschen eines Retargeting-Pixels

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Halten Sie den Cursor über den Pixelnamen und klicken Sie auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Delete]**.

## Pixel-Einstellungen für das Retargeting {#retargeting-pixel-settings}

**[!UICONTROL Pixel Name]:** Der Name des Pixels. **Hinweis:** Das Pixel-Tag enthält die Pixel-ID (`pxId=<ID>`), nicht den Pixelnamen.

**[!UICONTROL Advertiser]:** (Schreibgeschützt für vorhandene Pixel) Der Advertiser, für den das Pixel verfolgt wird.

**[!UICONTROL Attribute 1]:** Ein Attribut, das in das Pixel-Tag aufgenommen werden soll, z. B. „SKU“, „Kategorie“, „Größe“ oder andere Attribute der Seite oder des Produkts, die auf der Seite angezeigt werden. Geben Sie einen Wert für das -Attribut im Pixel-Tag an, bevor Sie es in die entsprechenden Web-Seiten einfügen.

Wenn Sie Anzeigen-Erlebnisse für Benutzende festlegen, die dem Pixel ausgesetzt sind, geben die Targeting-Einstellungen die Attributwerte an, die vorhanden sein müssen, um die Kreativen anzuzeigen.

**[!UICONTROL Attribute 2]**, **[!UICONTROL Attribute 3]**, **[!UICONTROL Attribute 4]**, **[!UICONTROL Attribute 5]:** (Optional) Zusätzliche Attribute, die in das Pixel-Tag aufgenommen werden sollen. Geben Sie für jedes zusätzliche Attribut im Pixel-Tag einen Wert an, bevor Sie es in die entsprechenden Web-Seiten einfügen.

Wenn Sie Anzeigen-Erlebnisse für Benutzende festlegen, die dem Pixel ausgesetzt sind, geben die Targeting-Einstellungen die Attributwerte an, die vorhanden sein müssen, um die Kreativen anzuzeigen.

**[!UICONTROL Advanced]** > **[!UICONTROL Universal IDs]:** (Nur neue Pixel; optional) Typen universeller IDs für das nachzuverfolgende Pixel-Tag:

* *[!UICONTROL ID5]:* Das Pixel-Tag verfolgt [!DNL ID5] IDs. Für Impressionen, die an universelle IDs gesendet werden, fallen keine Gebühren an.

* *[!UICONTROL Ramp ID]:* Das Pixel-Tag verfolgt [!DNL Ramp IDs]. Für Impressionen, die an universelle IDs gesendet werden, fallen keine Gebühren an.

Um diese Funktion verwenden zu können, müssen Sie bzw. ein anderer Benutzer im DSP-Konto die Nutzungsbedingungen für die einmalige Verwendung universeller IDs akzeptieren, bevor Sie universelle IDs für einen neuen ID-Typ verwenden können. Für Kunden mit verwalteten Service-Verträgen wird Ihr Adobe-Account-Team Ihre Zustimmung einholen und die Bedingungen im Namen Ihres Unternehmens akzeptieren. Um die Bedingungen zu lesen, klicken Sie auf **[!UICONTROL Terms of Service]**. Um die Bedingungen zu akzeptieren, scrollen Sie zum Ende der Bedingungen und klicken Sie auf **[!UICONTROL Accept]**.

>[!MORELIKETHIS]
>
>* [Einstellungen für zielgerichtete Anzeigenerlebnisse](/help/creative/experiences/experience-settings-targeting.md)
>* [Über Anzeigen-Erlebnisse](/help/creative/experiences/experience-about.md)
