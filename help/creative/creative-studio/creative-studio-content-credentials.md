---
title: C2PA-Metadaten in Creative Studio
description: Erfahren Sie, wie C2PA-Metadaten automatisch an Inhalte angehängt werden, die mit generativer KI in Creative Studio generiert oder bearbeitet werden.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d335c890ccc3ff8b2d391881660a71d10fcba53a
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 2%

---

# C2PA-Metadaten in [!UICONTROL Creative Studio]

[!UICONTROL Creative Studio] fügt automatisch C2PA-Metadaten an Inhalte an, die mit generativer KI generiert oder bearbeitet werden, sodass der Ursprung Ihres Anzeigeninhalts als dauerhafte, unsichtbare Metadaten aufgezeichnet wird. Die Metadaten entsprechen dem Standard der [Coalition for Content Provenance and Authenticity](https://c2pa.org/) (C2PA).

## Inhaltstypen und ihr Umfang {#cc-content-types}

| Content-Typ | Unterstützt? | KI-Service, der den Inhalt generiert | Modell, das die Berechtigung generiert |
| --- | --- | --- | --- |
| Bilder | Ja. C2PA-Metadaten werden angehängt, wenn Bilder mit generativer KI generiert oder bearbeitet werden. Diese werden durch Zuschneiden und Ändern der Größe, die vom KI-Assistenten ausgeführt werden, beibehalten. | [!DNL Adobe Firefly C2PA] | [!DNL Gemini Flash] |

## Aktionen, die C2PA-Metadaten anhängen

In der folgenden Tabelle wird basierend auf der im [!UICONTROL Creative Studio]-KI-Assistenten durchgeführten Bildaktion zusammengefasst, wann C2PA-Metadaten angehängt werden.

| Aktion | Beschreibung | C2PA-Metadaten angehängt? | Anwendungsbeispiel |
| --- | --- | --- | --- |
| **Bild erstellen** | Erstellen eines neuen Bildes mithilfe einer Textaufforderung | Immer, da das Bild durch generative KI generiert wird. | Sie verwenden eine Textaufforderung, um ein neues Hintergrundbild oder Logo für eine Anzeigenvorlage zu generieren.<br><br>Sie verwenden eine Textaufforderung, um das Standardbild in einem Anzeigenkonzept durch ein hochgeladenes Asset aus Ihrer Bibliothek zu ersetzen.<br><br>Sie verwenden eine Textaufforderung, um Varianten eines Hintergrundbilds in einer Anzeigenvorlage zu generieren. |

## Was passiert, wenn Inhalte verschoben werden? {#cc-content-moves}

Die vollständige Provenienzkette bleibt erhalten, wenn ein Benutzer eine Bilddatei herunterlädt oder sie zur Bereitstellung in einer Anzeige versendet wird.

## Was beinhalten die C2PA-Metadaten?

Für jede GenAI-Generierung oder -Änderung sind in den C2PA-Metadaten Folgendes enthalten. Wenn ein Asset mehrmals geändert wird, wird jeder Vorgang in den C2PA-Metadaten angezeigt.

* Name und Versionsinformationen des verwendeten KI-Systems ([!DNL Adobe Firefly C2PA])
* Verwendetes KI-Modell ([!DNL Gemini Flash])
* Nutzung: Ob sie mit GenAI generiert oder bearbeitet wurde
* Zeit und Datum der Inhaltserstellung und/oder -änderung mit generativen KI-Tools
* Eindeutige Kennung (die zur Unterscheidung jeder Verwendung der generativen KI verwendet werden kann)

## Wie kann ich C2PA-Metadaten für ein Bild anzeigen?

So zeigen Sie den vollständigen Asset-Verlauf für ein Bild an:

* Öffnen Sie die Bilddatei in einem Tool zur Überprüfung der Content-Authentizität, z. B. https://contentauthenticity.adobe.com/inspect oder https://verify.contentauthenticity.org/.

* Anzeigen der Bildmetadaten.

* Zeigen Sie den Bild-Code mit dem Code-Inspektions-Tool Ihres Browsers (häufig als [!DNL Inspect] bezeichnet) an.

![Beispiel für C2PA-Metadaten für ein Bild](/help/creative/assets/cs-content-credentials-example.png "C2PA-Metadaten für ein Bild")

## Zusätzliche Ressourcen

* [Benutzerrichtlinien für [!DNL Adobe] generative KI](https://www.adobe.com/de/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

>[!MORELIKETHIS]
>
>* [Über Creative Studio](/help/creative/creative-studio/creative-studio-about.md)
