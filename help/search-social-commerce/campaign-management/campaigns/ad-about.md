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

Nur *[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex] und bestehende [!DNL Baidu] Konten*

Eine Anzeige kann auf einer Ziel-Website angezeigt werden (für Kampagnen, die auf Inhalte oder Platzierungen abzielen); wenn ein Benutzer nach einem der Keywords in der Anzeigengruppe (für Suchkampagnen) oder nach Inhalten auf Ihrer Website sucht (dynamische Suchanzeigen in [!DNL Google Ads] Kampagnen, die nur auf die Suche ausgerichtet sind); oder wenn ein Benutzer eine Suche durchführt, die für eines der Elemente in Ihrem [!DNL Google Merchant Center] oder [!DNL Microsoft Merchant Center] Produkt-Feed relevant ist (Shopping-Anzeigen in [!DNL Google Ads] oder Produktanzeigen in [!DNL Microsoft Advertising] Kampagnen).

## Verfügbare Anzeigentypen

Sie können unterstützte Anzeigentypen für Anzeigengruppen in einem synchronisierten Anzeigennetzwerkkonto erstellen und verwalten:

* **Textanzeigen oder erweiterte Textanzeigen** für eine Anzeigengruppe in einer Kampagne, die auf das Suchnetzwerk abzielt. Textanzeigen können optionale Tracking-Parameter enthalten, die die Parameter auf Anzeigengruppen- oder Kampagnenebene überschreiben. Je nach Anzeigennetzwerk können Sie entweder erweiterte/erweiterte Textanzeigen oder Standardtextanzeigen erstellen.

* Geräteübergreifende, native **Zielgruppen-Anzeigen** für [!DNL Microsoft Advertising] Kampagnen auf der [!DNL Microsoft Audience Network]. Je nach den Kampagneneinstellungen stehen zwei Optionen für Zielgruppenanzeigen zur Verfügung:

   * Wenn die Kampagne mit einem Merchant Center-Store verknüpft ist, lassen Sie das Anzeigennetzwerk automatisch Anzeigen-Feed-basierte Anzeigen für die Kampagne generieren, wobei die Produktinformationen des Stores verwendet werden. Sie müssen keine Feed-basierten Anzeigen für die Kampagne erstellen, sondern Anzeigengruppen mit Benutzer-Targeting.

   * Wenn die Kampagne nicht mit einem Merchant Center-Konto verknüpft ist, erstellen Sie bildbasierte Zielgruppenanzeigen mit dem responsiven Anzeigenformat , das mehrere Text- und Bild-Assets enthält. Das Anzeigennetzwerk stellt die Anzeigen mithilfe der effektivsten Kombinationen von Anzeigenelementen zusammen und zeigt sie auf Websites wie [!DNL MSN], [!DNL Outlook.com] und [!DNL Microsoft Edge] an.

* **Nur-Anruf-Anzeigen** für [!DNL Google Ads] Kampagnen im Suchnetzwerk. Reine Anrufanzeigen sind Textanzeigen, die eine Telefonnummer enthalten. Optional können Sie eine [!DNL Google Ads] Weiterleitungsnummer für erweiterte Anrufberichte verwenden.

* **Erweiterte dynamische Suchanzeigen** (jetzt in den Werbenetzwerken nur noch „dynamische Suchanzeigen“ genannt) für [!DNL Google Ads] und [!DNL Microsoft Advertising] dynamische Suchanzeigengruppen in Suchkampagnen. Dynamische Suchanzeigen verwenden Inhalte von Ihrer Website anstelle von Keywords, um zu entscheiden, wann Ihre Anzeigen angezeigt werden sollen. Das Anzeigennetzwerk generiert dynamisch die Überschrift, wählt die Landingpage-URL und die Anzeige-URL aus und generiert automatisch die endgültige URL.

  Sie können die Seiten in Ihren Websites definieren, deren Inhalt für das Targeting Ihrer dynamischen Suchanzeigen verwendet wird, indem Sie bestimmte dynamische Suchziele für die Anzeigengruppe einrichten. Sie können [!DNL Google Ads] dynamische Suchziele in Search, Social und Commerce erstellen. Sie müssen sie [!DNL Microsoft Advertising] in [!DNL Microsoft Advertising] erstellen. In [!DNL Google Ads] Kampagnen können Sie optional eine Website-Domain und eine Sprache im Abschnitt &quot;[!DNL DSA Options]&quot; der Kampagne angeben, anstatt oder zusätzlich zu der Erstellung dynamischer Suchziele.

  Wenn der Suchbegriff eines Benutzers genau mit einem Keyword in einer Ihrer schlüsselwortbasierten Kampagnen übereinstimmt, wird anstelle einer dynamischen Suchanzeige eine Anzeige aus der schlüsselwortbasierten Kampagne angezeigt. Das Anzeigennetzwerk zeigt eine dynamische Suchanzeige anstelle einer auf ein Keyword ausgerichteten Anzeige an, wenn der Suchbegriff des Benutzers eine breite Übereinstimmung oder Phrase mit einem Ihrer Keywords aufweist und Ihre dynamische Suchanzeige einen höheren Anzeigenrang hat.

  Weitere Informationen zu dynamischen Suchanzeigen finden Sie unter [[!DNL Google Ads] &#x200B;](https://support.google.com/google-ads/answer/2471185) und [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **Multimedia-Anzeigen** für [!DNL Microsoft Advertising] Suchkampagnen. Multimedia-Anzeigen sind große Bildanzeigen, die an hervorgehobenen Positionen in der Haupt- und Seitenleiste angezeigt werden und pro Seite nur eine Multimedia-Anzeige angezeigt wird. Sie können mehrere Text- und Bild-Assets enthalten, z. B. responsive Anzeigen. Das Werbenetzwerk stellt die Anzeigen mithilfe der effektivsten Kombinationen von Anzeigenelementen zusammen. Multimedia-Anzeigen ersetzen nicht Ihre Text-Anzeigenplatzierungen.

* Promotion-Zeilen für **[!DNL Microsoft Advertising]Produkt (Shopping)-Anzeigen** im Shopping-Netzwerk. Shopping-Anzeigen verwenden Produkte in Ihrem vorhandenen [!DNL Microsoft Merchant Center]-Produkt-Feed anstelle von Keywords, um zu entscheiden, wie und wo Ihre Anzeigen angezeigt werden sollen. Die URLs für die Anzeigenkopie und die Landingpage werden automatisch aus Ihren Produktinformationen im Feed generiert. Sie können jedoch optional Promotion-Zeilen einrichten, die für die Anzeigengruppe enthalten sind.

  Sie können steuern, welche Produkte mit Ihren [!DNL Microsoft Advertising] Shopping-Anzeigen angezeigt werden, indem Sie separate Produktgruppen für die Anzeigengruppe einrichten, und zwar über die Ansicht [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] .

  Weitere Informationen zum Workflow für Produkt-/Shopping-Anzeigen finden Sie unter [Implementieren [!DNL Microsoft Advertising] Shopping-Kampagnen](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md).  Weitere Informationen zu Produktanzeigen finden Sie in der Dokumentation zu [Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/51082).

* Responsive Suchanzeigen für [!DNL Google Ads] und [!DNL Microsoft Advertising] Kampagnen im Suchnetzwerk. Das Anzeigennetzwerk stellt textbasierte responsive Suchanzeigen dynamisch aus einer Reihe von Anzeigentiteln und -beschreibungen zusammen und begünstigt Kombinationen, die eine gute Leistung erzielen. Die Anzeige enthält bis zu drei Überschriften, zwei Beschreibungen und eine anpassbare URL aus den Feldern Basis-URL und optionaler Pfad1 und Pfad2. Sie können Anzeigentitel und Beschreibungen optional an bestimmte Positionen anheften.

>[!NOTE]
>
>[!DNL Google Ads] stellen keine Daten über die Textkombinationen bereit, die als Anzeigen angezeigt wurden, außerhalb der nativen Editoren. Weitere Informationen zum Reporting für jede Textkombination finden Sie in der [Dokumentation zu Google Ads](https://support.google.com/google-ads/answer/7684791).

## Die [!UICONTROL Ads]

Sie können den Status von Anzeigen in der Ansicht [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads] erstellen, bearbeiten und ändern.

## Leistungsdaten auf Anzeigenebene

Daten auf Anzeigenebene sind für die meisten Anzeigentypen verfügbar.

Sie ist jedoch nicht für [!DNL Google Ads] dynamische Suchanzeige (DSA), die maximale Leistung, den intelligenten Einkauf und [!DNL YouTube] Kampagnen verfügbar. Rechnen Sie daher mit Abweichungen zwischen den gesamten Daten auf Anzeigenebene für eine Kampagne und den gesamten Daten für die Kampagne.

| Anzeigennetzwerk/Kampagne/Anzeigentyp | Datenverfügbarkeit |
|---|---|
| Dynamische Suchanzeige [!DNL Google Ads] (DSA) | Kampagne, Anzeigengruppe |
| Maximale [!DNL Google Ads] | Campaign |
| [!DNL Google Ads] Einkaufen, intelligentes Einkaufen | Kampagne, Anzeigengruppe |
| [!DNL Google Ads] [!DNL YouTube] | Kampagne, Anzeigengruppe |

>[!MORELIKETHIS]
>
>* [Anzeigen verwalten](ad-manage.md)
