---
title: Syntax für die Logik von Zielgruppensegmenten
description: Referenzieren Sie die Syntax, die Sie zum Definieren der Logik für Zielgruppensegmente verwenden können.
feature: DSP Audiences
exl-id: fb73f35f-1f65-463b-b93c-90804a8d19a9
TQID: 'https://experienceleague.adobe.com/FPci9npdKrFxwge6tw41Fhx4XAC9VqYFc-RZhLhILLo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: b4dc2b3d-fdb5-55cd-9190-f1076d8563e4
    internal-label: DSP Audiences
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
    internal-label: Audiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%
---
# Syntax für die Logik von Zielgruppensegmenten

Beim Erstellen wiederverwendbarer Zielgruppen können Sie die Segmentlogik manuell mithilfe alphanumerischer Segment-IDs (Schlüssel) und der folgenden Syntax definieren:

* (a) um eine Gruppe anzugeben
* `||` für [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp;&amp; für [!DNL AND]
* ! für [!DNL NOT] (ausschließen)

>[!NOTE]
>
>* Alle angegebenen Segmentgruppen sind enthalten, es sei denn, ihnen wird ! (ohne sie).
>* Sie können [die Segment-ID für eine Zielgruppe finden](reusable-audience-clipboard.md) unter [!UICONTROL Audiences] > [!UICONTROL All audiences].

Beispielsweise die folgende Logik:

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

meint (im Klartext)

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>In Platzierungseinstellungen können Sie gespeicherte Zielgruppen entweder als Zielgruppen verwenden, die explizit ausgewählt werden sollen, oder als separate Zielgruppen, die vom Targeting ausgeschlossen werden sollen. Stellen Sie sicher, dass Ihre Segmentlogik den Zweck der Verwendung der Zielgruppe widerspiegelt.

>[!MORELIKETHIS]
>
>* [Kopieren Sie den Segmentschlüssel für eine wiederverwendbare Zielgruppe in die Zwischenablage](reusable-audience-clipboard.md)
>* [Über die Zielgruppenverwaltung](audience-about.md)
>* [Erstellen einer wiederverwendbaren Zielgruppe](reusable-audience-create.md)
>* [Zielgruppeneinstellungen](audience-settings.md)
>* [Verfügbare Datenanbieter von Drittanbietern](third-party-data-providers.md)
