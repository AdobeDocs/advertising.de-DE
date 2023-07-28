---
title: Anzeigen verwalten
description: Erfahren Sie mehr über Anzeigen in Search, Social und Commerce, einschließlich der verfügbaren Anzeigentypen.
exl-id: 92ae631a-c35a-40ec-9d40-ebce13e3311b
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '895'
ht-degree: 0%

---

# Über Anzeigen

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads], und [!DNL Yandex] Nur Konten*

Eine Anzeige kann auf einer Ziel-Website angezeigt werden (für Inhalte oder platzierungszielgerichtete Kampagnen); wenn ein Benutzer nach einem der Suchbegriffe in der Anzeigengruppe (für Suchkampagnen) oder nach Inhalten auf Ihrer Website (dynamische Suchanzeigen in [!DNL Google Ads] Suchkampagnen); oder wenn ein Benutzer eine Suche durchführt, die für eines der Elemente in Ihrer [!DNL Google Merchant Center] oder [!DNL Microsoft® Merchant Center] Produkt-Feed (Shopping-Anzeigen in [!DNL Google Ads] oder Produktanzeigen in [!DNL Microsoft® Advertising] Kampagnen).

## Verfügbare Anzeigenarten

Sie können unterstützte Anzeigentypen für Anzeigengruppen innerhalb eines synchronen Anzeigennetzwerkkontos erstellen und verwalten:

* **Textanzeigen oder erweiterte Textanzeigen** für eine Anzeigengruppe in einer Kampagne, die auf das Suchnetzwerk ausgerichtet ist. Textanzeigen können optionale Tracking-Parameter enthalten, die die Parameter auf Anzeigengruppen- oder Kampagnenebene außer Kraft setzen. Je nach Werbenetzwerk können Sie entweder erweiterte/erweiterte Textanzeigen oder Standardtextanzeigen erstellen.

* Geräteübergreifend, nativ **Zielgruppenanzeigen** für [!DNL Microsoft® Advertising] Kampagnen auf [!DNL Microsoft® Audience Network]. Basierend auf den Kampagneneinstellungen stehen Ihnen zwei Optionen für Zielgruppenanzeigen zur Verfügung:

   * Wenn die Kampagne mit einem Händler-Center-Store verknüpft ist, lassen Sie das Werbenetzwerk automatisch Anzeigen-Feed-basierte Anzeigen für die Kampagne generieren, wobei die Produktinformationen des Stores verwendet werden. Sie müssen keine Feed-basierten Anzeigen für die Kampagne erstellen, sondern Anzeigengruppen mit Benutzer-Targeting erstellen.

   * Wenn die Kampagne nicht mit einem Merchant Center-Konto verknüpft ist, erstellen Sie bildbasierte Zielgruppenanzeigen im responsiven Anzeigenformat, das mehrere Text- und Bild-Assets enthält. Das Werbenetzwerk stellt die Anzeigen anhand der effektivsten Kombinationen aus Anzeigenelementen zusammen und zeigt sie auf Sites wie [!DNL MSN], [!DNL Outlook.com], und [!DNL Microsoft® Edge].

* **Schreibgeschützte Anzeigen** für [!DNL Google Ads] Kampagnen im Suchnetzwerk. Schreibgeschützte Anzeigen sind Textanzeigen mit einer Telefonnummer. Optional können Sie eine [!DNL Google Ads]-zugewiesene Weiterleitungsnummer für erweiterte Anrufberichte.

* **Erweiterte dynamische Suchanzeigen** (jetzt auch &quot;dynamische Suchanzeigen&quot;in Werbenetzwerken genannt) für [!DNL Google Ads] und [!DNL Microsoft® Advertising] dynamische Suchanzeigengruppen in Suchkampagnen. Dynamische Suchanzeigen verwenden Inhalte von Ihrer Website anstelle von Keywords, um zu entscheiden, wann Ihre Anzeigen angezeigt werden. Das Werbenetzwerk generiert dynamisch die Überschrift, wählt die URL der Landingpage und die Anzeigen-URL aus und generiert automatisch die endgültige URL.

  Sie können die Seiten Ihrer Websites definieren, deren Inhalt für das Targeting Ihrer dynamischen Suchanzeigen verwendet wird, indem Sie spezifische dynamische Suchziele für die Anzeigengruppe einrichten. Für [!DNL Google Ads]können Sie dynamische Suchziele in Search, Social und Commerce erstellen. [!DNL Microsoft® Advertising], müssen Sie sie in [!DNL Microsoft® Advertising]. In [!DNL Google Ads] Kampagnen können Sie optional eine Website-Domäne und -Sprache in der Kampagnen-[!DNL DSA Options]&quot;, anstatt dynamischer Suchziele zu erstellen.

  Wenn der Suchbegriff eines Benutzers genau mit einem Suchbegriff in einer Ihrer schlüsselwortbasierten Kampagnen übereinstimmt, wird anstelle einer dynamischen Suchanzeige eine Anzeige aus der schlüsselwortbasierten Kampagne angezeigt. Das Werbenetzwerk zeigt eine dynamische Suchanzeige anstelle einer zielgruppenorientierten Anzeige an, wenn der Suchbegriff des Benutzers eine weit gefasste Übereinstimmung oder Wortgruppe mit einem Ihrer Suchbegriffe ist und Ihre dynamische Suchanzeige einen höheren Anzeigenrang aufweist.

  Weitere Informationen zu dynamischen Suchanzeigen finden Sie in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/2471185) und [[!DNL Microsoft® Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **Multimedia-Anzeigen** für [!DNL Microsoft® Advertising] Suchkampagnen. Multimedia-Anzeigen sind große Bildanzeigen, die an auffälligen Festnetz- und Seitenleistenpositionen angezeigt werden und pro Seite nur eine Multimedia-Anzeige angezeigt wird. Sie können mehrere Text- und Bild-Assets enthalten, z. B. responsive Anzeigen, und das Werbenetzwerk stellt die Anzeigen anhand der effektivsten Kombinationen aus Anzeigenelementen zusammen. Multimedia-Anzeigen ersetzen Ihre Platzierungen für Textanzeigen nicht.

* Werbeplänen für **[!DNL Microsoft® Advertising]Produktanzeigen (Shopping-Anzeigen)** im Warennetzwerk. Shopping-Anzeigen verwenden Produkte in Ihren vorhandenen [!DNL Microsoft® Merchant Center] Produkt-Feed anstelle von Keywords verwenden, um zu entscheiden, wie und wo Ihre Anzeigen angezeigt werden. Die URLs für die Anzeigenkopie und die Landingpage werden automatisch aus Ihren Produktinformationen im Feed generiert. Sie können jedoch optional Promotionslinien einrichten, die für die Anzeigengruppe eingeschlossen werden.

  Sie können steuern, welche Produkte mit Ihrer [!DNL Microsoft® Advertising] Einkaufen-Anzeigen, indem Sie separate Produktgruppen für die Anzeigengruppe einrichten, über die [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] anzeigen.

  Weitere Informationen zum Workflow für Produkt-/Einkaufsanzeigen finden Sie unter &quot;[Implementierung [!DNL Microsoft® Advertising] Warenkorb](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md).&quot;  Weitere Informationen zu Produktanzeigen finden Sie unter [Microsoft® Advertising-Dokumentation](https://help.ads.microsoft.com/#apex/3/en/51082).

* Responsive Suchanzeigen für [!DNL Google Ads] und [!DNL Microsoft® Advertising] Kampagnen im Suchnetzwerk. Das Anzeigennetzwerk assembliert dynamisch textbasierte responsive Suchanzeigen aus einer Reihe von Anzeigentiteln und -beschreibungen, wobei bevorzugt Kombinationen gewählt werden, die eine gute Leistung erzielen. Die Anzeige enthält bis zu drei Überschriften, zwei Beschreibungen und eine anpassbare URL aus den Basis-URL- und optionalen Feldern path1 und path2. Sie können Anzeigentitel und -beschreibungen optional an bestimmte Positionen anheften.

>[!NOTE]
>
>[!DNL Google Ads] stellen außerhalb der nativen Editoren keine Daten zu den Textkombinationen bereit, die als Anzeigen angezeigt wurden. Weitere Informationen zur Berichterstellung für die einzelnen Textkombinationen finden Sie unter [Dokumentation zu Google Ads](https://support.google.com/google-ads/answer/7684791).

## Die [!UICONTROL Ads] Ansicht

Sie können den Status von Anzeigen erstellen, bearbeiten und ändern über die [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads] anzeigen.

## Leistungsdaten auf Anzeigenebene

Daten auf Anzeigenebene sind für die meisten Anzeigentypen verfügbar.

Es ist jedoch nicht verfügbar für [!DNL Google Ads] dynamische Suchanzeige (DSA), Leistungsmax, intelligentes Einkaufen und [!DNL YouTube] Kampagnen. Erwarten Sie Diskrepanzen zwischen den Gesamtdaten der Anzeigenebene für eine Kampagne und den Gesamtdaten für die Kampagne.

| Werbenetzwerk/Kampagne/Werbetyp | Datenverfügbarkeit |
|---|---|
| [!DNL Google Ads] dynamische Suchanzeige (DSA) | Kampagne, Anzeigengruppe |
| [!DNL Google Ads] Performance max | Kampagne |
| [!DNL Google Ads] Einkaufen, Smart Shopping | Kampagne, Anzeigengruppe |
| [!DNL Google Ads] [!DNL YouTube] | Kampagne, Anzeigengruppe |

>[!MORELIKETHIS]
>
>* [Anzeigen verwalten](ad-manage.md)
