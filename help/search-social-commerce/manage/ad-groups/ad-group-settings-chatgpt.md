---
title: Einstellungen für Anzeigengruppen [!DNL ChatGPT]
description: Verweisen Sie auf die Einstellungen für [!DNL ChatGPT] Anzeigengruppen.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
source-git-commit: 487af67f7215bf4a070af5e813649288141b0ed4
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%
---
# Einstellungen für Anzeigengruppen [!DNL ChatGPT]

*Anzeigen in [!DNL ChatGPT] sind eine Pilotfunktion von[!DNL OpenAI]*

## Registerkarte [!UICONTROL Basic Settings]

*Nur neue Anzeigengruppen*

**[!UICONTROL Network]:** Das Werbenetzwerk.

**[!UICONTROL Account]:** Das Netzwerkkonto der Anzeige.

**[!UICONTROL Campaign]:** Die Kampagne. Sie können die Kampagne nach dem Erstellen der Anzeigengruppe nicht mehr ändern.

## Registerkarte [!UICONTROL Ad Group Details]

**[!UICONTROL Ad Group name]:** Ein Anzeigengruppenname, der innerhalb der Kampagne eindeutig ist und mindestens drei Zeichen enthält.

**[!UICONTROL Status]:** Der Anzeigestatus der Anzeigengruppe: *[!UICONTROL Active]* oder *[!UICONTROL Paused]*. Der Standardwert für neue Anzeigengruppen ist *[!UICONTROL Active]*.

**[!UICONTROL Bid strategy]:** (Kampagnen mit dem Ziel [!UICONTROL Clicks] oder [!UICONTROL Conversions]) Gebot für Anzeigen in der Anzeigengruppe:

* *[!UICONTROL Autobid]:* (Standard für neue Anzeigengruppen) passt [!DNL OpenAI] Angebote automatisch an, um die meisten Klicks oder Konversionen je nach Kampagnenziel aus Ihrem Budget zu erhalten. Sie geben keinen Gebotsbetrag ein. Diese Option ist sowohl für das tägliche Kampagnenbudget als auch für das Kampagnenbudget über die gesamte Lebensdauer verfügbar.

* *[!UICONTROL Target CPC]:* (Kampagnen mit dem Ziel [!UICONTROL Clicks]) Bietet ein durchschnittliches Kosten-pro-Klick-Ziel. Geben Sie das Ziel in das Feld [!UICONTROL Target CPC] ein.

* *[!UICONTROL Target CPA]:* (Kampagnen mit dem Ziel [!UICONTROL Conversions]) Bietet ein Ziel für die durchschnittlichen Kosten pro Konversion an. Geben Sie das Ziel in das Feld [!UICONTROL Target CPA] ein.

* *[!UICONTROL Manual: Max bid]:* (Nur vorhandene manuelle Bid-Anzeigengruppen) Behält das vorhandene Höchstgebot als schreibgeschützten Betrag bei. Sie können diese Strategie beibehalten oder zu [!UICONTROL Autobid] oder der Zielstrategie für das Kampagnenziel wechseln. Diese Option ist nicht für neue Anzeigengruppen verfügbar oder beim Bearbeiten von Anzeigengruppen, die bereits automatische Gebote oder Target-Gebote verwenden.

Bestehende manuell gebotene Anzeigengruppen werden nicht automatisch in eine andere Strategie geändert. Die Bearbeitung nur eines Zielbetrags oder einer nicht damit verbundenen Einstellung ändert nichts an einer bestehenden Ziel-Gebotsstrategie.

**[!UICONTROL Target CPC]:** (Anzeigengruppen mit der Bid-Strategie [!UICONTROL Target CPC]; erforderlich) Die durchschnittlichen Kosten pro Klick, die Sie erreichen möchten, in der Währung des Kontos. Geben Sie einen positiven Betrag ein. Dies ist ein Ziel mit durchschnittlichen Kosten, kein Maximalgebot.

**[!UICONTROL Target CPA]:** (Anzeigengruppen mit der Bid-Strategie [!UICONTROL Target CPA]; erforderlich) Die durchschnittlichen Kosten pro Konversion, die Sie erreichen möchten, in der Währung des Kontos. Geben Sie einen positiven Betrag ein. Dies ist ein Ziel mit durchschnittlichen Kosten, kein Maximalgebot.

**[!UICONTROL Maximum CPC bid]:** (Kampagnen mit dem Ziel-[!UICONTROL Clicks]; vorhandene Anzeigengruppen, die manuell gebeten werden; schreibgeschützt) Der vorhandene Höchstbetrag, den Sie für jeden Klick zahlen werden.

**[!UICONTROL Conversion-optimized bid cap]:** (Kampagnen mit dem Ziel-[!UICONTROL Conversions]; vorhandene Anzeigengruppen, die manuell gebeten werden; schreibgeschützt) Der vorhandene Höchstbetrag, den Sie für eine Konversion bieten möchten. [!DNL OpenAI] verwendet die prognostizierte Konversionsrate, um diesen Wert in ein Impression-Auktionsgebot umzuwandeln.

**[!UICONTROL Maximum CPM bid]:** (Kampagnen mit dem Ziel-[!UICONTROL Reach]) Der maximale Betrag, den Sie für eintausend Impressionen zahlen werden, in der Währung des Kontos. Geben Sie einen Wert zwischen 0,01 und 5000 ein. Reach-Kampagnen verfügen nicht über die [!UICONTROL Bid strategy] Optionen.

**[!UICONTROL Context hints (optional)]:** Beschreibung der Konversationen, Themen oder Schlüsselwörter, für die Ihre Produkte oder Dienstleistungen relevant sein können. Trennen Sie Hinweise durch Kommas oder Zeilenumbrüche. Ihre Hinweise können als Leitfaden für den Abgleich verwendet werden, sind aber keine exakt übereinstimmenden Zielgruppenbestimmungsregeln. Siehe [[!DNL ChatGPT Ads] Hilfe zum Schreiben effektiver Kontexthinweise](https://help.openai.com/en/articles/20001211-create-ad-groups-for-chatgpt#writing-effective-context-hints).

**[!UICONTROL Landing Page Suffix]:** (Optional) Alle Parameter, die an das Ende der Landingpage-URLs angehängt werden sollen, um Informationen zu verfolgen. Beispiel: `param1=value1&param2=value2`.

>[!MORELIKETHIS]
>
>* [Anzeigengruppen verwalten](ad-group-manage.md)
