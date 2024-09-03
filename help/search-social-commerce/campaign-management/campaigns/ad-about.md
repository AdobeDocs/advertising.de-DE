---
title: Anzeigen verwalten
description: Erfahren Sie mehr über Anzeigen in Search, Social und Commerce, einschließlich der verfügbaren Anzeigentypen.
exl-id: 01bd211d-fe6b-4329-90e1-0e54d626c125
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# Über Anzeigen

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex] und vorhandene [!DNL Baidu] Konten nur*

Eine Anzeige kann auf einer Ziel-Website angezeigt werden (für Inhalte oder platzierungszielgerichtete Kampagnen), wenn ein Benutzer nach einem der Suchbegriffe in der Anzeigengruppe (für Suchkampagnen) oder nach Inhalten auf Ihrer Website (dynamische Suchanzeigen in [!DNL Google Ads] Suchkampagnen) sucht oder wenn ein Benutzer eine Suche durchführt, die für eines der Elemente in Ihrem [!DNL Google Merchant Center] - oder [!DNL Microsoft Merchant Center] -Produkt-Feed (Shopping-Anzeigen in [!DNL Google Ads] oder Produktanzeigen in [!DNL Microsoft Advertising] relevant ist) ist Kampagnen).

## Verfügbare Anzeigenarten

Sie können unterstützte Anzeigentypen für Anzeigengruppen innerhalb eines synchronen Anzeigennetzwerkkontos erstellen und verwalten:

* **Textanzeigen oder erweiterte Textanzeigen** für eine Anzeigengruppe in einer Kampagne, die auf das Suchnetzwerk ausgerichtet ist. Textanzeigen können optionale Tracking-Parameter enthalten, die die Parameter auf Anzeigengruppen- oder Kampagnenebene außer Kraft setzen. Je nach Werbenetzwerk können Sie entweder erweiterte/erweiterte Textanzeigen oder Standardtextanzeigen erstellen.

* Geräteübergreifende, native **Zielgruppenanzeigen** für [!DNL Microsoft Advertising] Kampagnen auf der [!DNL Microsoft Audience Network]. Basierend auf den Kampagneneinstellungen stehen Ihnen zwei Optionen für Zielgruppenanzeigen zur Verfügung:

   * Wenn die Kampagne mit einem Händler-Center-Store verknüpft ist, lassen Sie das Werbenetzwerk automatisch Anzeigen-Feed-basierte Anzeigen für die Kampagne generieren, wobei die Produktinformationen des Stores verwendet werden. Sie müssen keine Feed-basierten Anzeigen für die Kampagne erstellen, sondern Anzeigengruppen mit Benutzer-Targeting erstellen.

   * Wenn die Kampagne nicht mit einem Merchant Center-Konto verknüpft ist, erstellen Sie bildbasierte Zielgruppenanzeigen im responsiven Anzeigenformat, das mehrere Text- und Bild-Assets enthält. Das Werbenetzwerk stellt die Anzeigen anhand der effektivsten Kombinationen aus Anzeigenelementen zusammen und zeigt sie auf Sites wie [!DNL MSN], [!DNL Outlook.com] und [!DNL Microsoft Edge] an.

* **Schreibgeschützte Anzeigen** für [!DNL Google Ads] Kampagnen im Suchnetzwerk. Schreibgeschützte Anzeigen sind Textanzeigen mit einer Telefonnummer. Optional können Sie für erweiterte Aufrufberichte eine mit [!DNL Google Ads] zugewiesene Weiterleitungsnummer verwenden.

* **Dynamische Suchanzeigen erweitert** (jetzt auch &quot;dynamische Suchanzeigen&quot;in den Werbenetzwerken genannt) für dynamische Suchanzeigengruppen [!DNL Google Ads] und [!DNL Microsoft Advertising] in Suchkampagnen. Dynamische Suchanzeigen verwenden Inhalte von Ihrer Website anstelle von Keywords, um zu entscheiden, wann Ihre Anzeigen angezeigt werden. Das Werbenetzwerk generiert dynamisch die Überschrift, wählt die URL der Landingpage und die Anzeigen-URL aus und generiert automatisch die endgültige URL.

  Sie können die Seiten Ihrer Websites definieren, deren Inhalt für das Targeting Ihrer dynamischen Suchanzeigen verwendet wird, indem Sie spezifische dynamische Suchziele für die Anzeigengruppe einrichten. Für [!DNL Google Ads] können Sie dynamische Suchziele in Search, Social und Commerce erstellen. Für [!DNL Microsoft Advertising] müssen Sie diese in [!DNL Microsoft Advertising] erstellen. In [!DNL Google Ads]-Kampagnen können Sie optional eine Website-Domäne und -Sprache im Abschnitt &quot;[!DNL DSA Options]&quot;der Kampagne angeben, anstatt dynamische Suchziele zu erstellen.

  Wenn der Suchbegriff eines Benutzers genau mit einem Suchbegriff in einer Ihrer schlüsselwortbasierten Kampagnen übereinstimmt, wird anstelle einer dynamischen Suchanzeige eine Anzeige aus der schlüsselwortbasierten Kampagne angezeigt. Das Werbenetzwerk zeigt eine dynamische Suchanzeige anstelle einer zielgruppenorientierten Anzeige an, wenn der Suchbegriff des Benutzers eine weit gefasste Übereinstimmung oder Wortgruppe mit einem Ihrer Suchbegriffe ist und Ihre dynamische Suchanzeige einen höheren Anzeigenrang aufweist.

  Weitere Informationen zu dynamischen Suchanzeigen finden Sie in der [[!DNL Google Ads] Dokumentation](https://support.google.com/google-ads/answer/2471185) und der [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **Multimedia-Anzeigen** für [!DNL Microsoft Advertising] Suchkampagnen. Multimedia-Anzeigen sind große Bildanzeigen, die an auffälligen Festnetz- und Seitenleistenpositionen angezeigt werden und pro Seite nur eine Multimedia-Anzeige angezeigt wird. Sie können mehrere Text- und Bild-Assets enthalten, z. B. responsive Anzeigen, und das Werbenetzwerk stellt die Anzeigen anhand der effektivsten Kombinationen aus Anzeigenelementen zusammen. Multimedia-Anzeigen ersetzen Ihre Platzierungen für Textanzeigen nicht.

* Promotion-Linien für **[!DNL Microsoft Advertising]Produktanzeigen (Shopping)** im Warennetzwerk. Einkaufsanzeigen verwenden Produkte in Ihrem vorhandenen [!DNL Microsoft Merchant Center] -Produkt-Feed anstelle von Suchbegriffen, um zu entscheiden, wie und wo Ihre Anzeigen angezeigt werden. Die URLs für die Anzeigenkopie und die Landingpage werden automatisch aus Ihren Produktinformationen im Feed generiert. Sie können jedoch optional Promotionslinien einrichten, die für die Anzeigengruppe eingeschlossen werden.

  Sie können steuern, welche Produkte mit Ihren [!DNL Microsoft Advertising] -Shopping-Anzeigen angezeigt werden, indem Sie separate Produktgruppen für die Anzeigengruppe über die Ansicht [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] einrichten.

  Weitere Informationen zum Workflow für Produkt-/Shopping-Anzeigen finden Sie unter &quot;[Implementieren [!DNL Microsoft Advertising] Einkaufskampagnen](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)&quot;.  Weitere Informationen zu Produktanzeigen finden Sie in der Dokumentation zu [Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/51082).

* Responsive Suchanzeigen für [!DNL Google Ads] - und [!DNL Microsoft Advertising] -Kampagnen im Suchnetzwerk. Das Anzeigennetzwerk assembliert dynamisch textbasierte responsive Suchanzeigen aus einer Reihe von Anzeigentiteln und -beschreibungen, wobei bevorzugt Kombinationen gewählt werden, die eine gute Leistung erzielen. Die Anzeige enthält bis zu drei Überschriften, zwei Beschreibungen und eine anpassbare URL aus den Basis-URL- und optionalen Feldern path1 und path2. Sie können Anzeigentitel und -beschreibungen optional an bestimmte Positionen anheften.

>[!NOTE]
>
>[!DNL Google Ads] liefert keine Daten über die Textkombinationen, die als Anzeigen angezeigt wurden, außerhalb der nativen Editoren. Weitere Informationen zur Berichterstellung für die einzelnen Textkombinationen finden Sie in der Dokumentation zu [Google Ads](https://support.google.com/google-ads/answer/7684791) .

## Die Ansicht [!UICONTROL Ads]

Sie können den Status von Anzeigen in der Ansicht [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads] erstellen, bearbeiten und ändern.

## Leistungsdaten auf Anzeigenebene

Daten auf Anzeigenebene sind für die meisten Anzeigentypen verfügbar.

Es ist jedoch nicht für [!DNL Google Ads] dynamische Suchanzeige (DSA), Performance max, Smart Shopping und [!DNL YouTube] Kampagnen verfügbar. Erwarten Sie Diskrepanzen zwischen den Gesamtdaten der Anzeigenebene für eine Kampagne und den Gesamtdaten für die Kampagne.

| Werbenetzwerk/Kampagne/Werbetyp | Datenverfügbarkeit |
|---|---|
| [!DNL Google Ads] dynamische Suchanzeige (DSA) | Kampagne, Anzeigengruppe |
| [!DNL Google Ads] Performance max | Kampagne |
| [!DNL Google Ads] Einkaufen, Smart Shopping | Kampagne, Anzeigengruppe |
| [!DNL Google Ads] [!DNL YouTube] | Kampagne, Anzeigengruppe |

>[!MORELIKETHIS]
>
>* [Anzeigen verwalten](ad-manage.md)
