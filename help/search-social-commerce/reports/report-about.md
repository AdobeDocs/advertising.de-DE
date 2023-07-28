---
title: Über Berichte
description: Erfahren Sie mehr über Leistungsberichte, einschließlich der verschiedenen verfügbaren Berichtstypen und der Automatisierung von Berichten.
exl-id: a945b255-a9b0-42f4-85ea-44416c837fc0
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---

# Über Berichte

Mit Leistungsberichten können Sie die Leistung Ihrer Portfolios, Anzeigennetzwerke und Anzeigennetzwerkkontoentitäten auf beliebig detaillierter Ebene verfolgen und verwalten. Die meisten Berichte bieten einen umfassenden Einblick in den Beitrag der Anzeigen in den einzelnen Marketingkanälen zur Gesamtkonversionsrate.

Die Daten für einen Bericht werden bei jeder Ausführung des Berichts dynamisch kompiliert. Sie können optional einen neuen Bericht aus einem vorhandenen Bericht erstellen. Die verfügbaren Berichtsparameter variieren je nach Berichtstyp. Für die meisten Berichte haben Sie die Möglichkeit, eine Vorschau der ersten 50 Zeilen anzuzeigen, anstatt den gesamten Bericht zu generieren. Bei der Berichterstellung können Sie nach Abschluss eines Berichts eine Benachrichtigung mit Downloadlinks an eine oder mehrere E-Mail-Adressen senden. Die Empfänger können [die Benachrichtigungen in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md).

Alle abgeschlossenen Berichte sind im [!UICONTROL Latest Reports] Abschnitt [!UICONTROL Reports] anzeigen und Sie können sie entweder im Browserfenster im Tabellenformat anzeigen oder sie als Dateien öffnen oder herunterladen.

## Verfügbare Berichtskategorien

Die folgenden Berichtskategorien sind über die [!UICONTROL Reports] anzeigen. Möglicherweise haben Sie keinen Zugriff auf alle Berichte. Die verfügbaren Berichte und die von ihnen generierten Daten werden durch Ihre Rolle und die Konfiguration Ihres Kundenkontos bestimmt.

| Berichtskategorie | Beschreibung |
| ----| ---- |
| [!UICONTROL Basic Reports] | [Grundlegende Berichte](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md), die für alle Benutzer verfügbar sind, zeigen die tatsächlichen Kosten- und Klickdaten für Portfolios, Anzeigennetzwerkkonten, bestimmte Anzeigennetzwerkkonten, Kampagnen, Anzeigengruppen, Anzeigen, Suchbegriffe, Produktgruppen, Beschriftungsklassifizierungen und Beschriftungswerte, Gebotseinheiten-Einschränkungen und Netzwerkbeschränkungen an. Sie basieren auf Klicks, die von den entsprechenden Werbenetzwerken in Rechnung gestellt werden, und können optional Konversionsdaten oder andere von Ihnen erstellte Metriken enthalten. |
| [!UICONTROL Advanced Reports] | [Erweiterte Berichte](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) bieten zusätzliche Einblicke in Ihre Werbekonfiguration, sodass Sie feststellen können, wovon Sie durch eine Änderung Ihrer geografischen Zielbestimmungen oder Netzwerkeinstellungen profitieren würden. Sie können Ihnen auch dabei helfen, Konversionsdaten in den Kampagnen- und Portfoliomanagementansichten und -berichten anhand der internen Konversions-Tracking-Daten des Advertisers zu validieren. |
| [!UICONTROL Assist Reports] | [Hilfsberichte](/help/search-social-commerce/reports/management/assist/assist-report-about.md) bieten Einblicke in die Konversionspfade für alle Suchbegriffe und Anzeigen eines Advertisers. Sie verwenden Daten, die über den Adobe Advertising-Konversions-Tracking-Dienst erfasst werden und nur für Advertiser mit dem Dienst generiert werden können. |
| [!UICONTROL Specialty Reports] | [Spezifikationsberichte](/help/search-social-commerce/reports/management/specialty/specialty-report-about.md) aus Daten bestehen, die von den Werbenetzwerken (und nicht vom Adobe Advertising-Tracking) erfasst werden. |
| [!UICONTROL Model Accuracy Reports] | [Modellgenauigkeitsberichte](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md) die Genauigkeit der Kosten- und Umsatzmodelle angeben, die zur Optimierung von Angeboten verwendet werden. |

## Berichtsautomatisierung

Planen Sie die automatische Erstellung benutzerdefinierter Berichte auf eine oder beide der folgenden Arten:

* Sie können Berichte automatisch täglich oder an einem bestimmten Wochentag oder Monat erstellen, indem Sie [Berichtsvorlagen](/help/search-social-commerce/reports/automation/templates/template-about.md).

  Sie können optional [FTP-Bereitstellung grundlegender und erweiterter Berichte](/help/search-social-commerce/reports/automation/ftp-reports.md) , die eine Vorlage verwenden.

* Aktualisieren Sie Ihre benutzerdefinierten Tabellenvorlagen mit den täglichen Leistungsdaten, indem Sie [Tabellen-Feeds](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-about.md).

## Die Berichtsansichten

Die [!UICONTROL Reports] Ansichten unter [!UICONTROL Search] > [!UICONTROL Insights & Reports] > [!UICONTROL Reports] ermöglicht Ihnen die Erstellung und Verwaltung von Berichten, Vorlagen und Tabellen-Feeds. Die Ansicht enthält zwei Registerkarten:

* Die **[!UICONTROL Latest Reports]** enthält alle Berichte, die Ihnen in den letzten sieben Tagen zur Verfügung standen, mit Ausnahme der manuell gelöschten Berichte, wobei sich der neueste Bericht standardmäßig oben befindet. Zu den für jeden Bericht angezeigten Informationen gehören der Zeitplan, nach dem er ausgeführt wird (falls zutreffend), das Start- und Enddatum, für das Daten generiert wurden oder werden, sowie der Berichtsstatus (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]* oder *[!UICONTROL Error]*).

  Über die Links neben jedem Bericht können Sie den Bericht im Webbrowser anzeigen oder ihn als [!DNL Microsoft Excel] Arbeitsmappen (XLS) oder tabulatorgetrennte Werte (TSV). Einige Berichtstypen können auch als [!UICONTROL Excel] Arbeitsmappen mit einem separaten Arbeitsblatt für jede anwendbare Kampagne.

  Auf dieser Registerkarte können Sie auch einen neuen Bericht erstellen (der optional als Vorlage verwendet werden kann), einen neuen Bericht erstellen, der auf den Einstellungen für einen vorhandenen Bericht basiert, die für Sie verfügbaren laufenden Berichte abbrechen, indem Sie sie löschen und alle für Sie verfügbaren abgeschlossenen Berichte löschen. Berichte, die älter als sieben Tage sind, werden automatisch gelöscht.

* Die **[!UICONTROL Templates]** enthält alle gespeicherten grundlegenden und erweiterten Berichtvorlagen, die Ihnen zur Verfügung stehen, einschließlich Informationen zu den ihnen zugeordneten Zeitplänen. Die neueste Vorlage befindet sich standardmäßig ganz oben.

  Auf dieser Registerkarte erstellen Sie eine neue Vorlage, bearbeiten eine von Ihnen erstellte Vorlage (einschließlich Hinzufügen, Ändern oder Entfernen des Zeitplans), erstellen einen Bericht aus einer Vorlage und löschen alle für Sie verfügbaren Vorlagen.

## Verwendung von Berichten

| Zweck | Bericht |
| ---- | ---- |
| Leistungsüberwachung | <ul><li>[Die [!UICONTROL Portfolio Report]](/help/search-social-commerce/reports/management/basic-advanced/portfolio-report.md)</li><li>[Die [!UICONTROL Search Engine Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-report.md)</li><li>[Die [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[Die [!UICONTROL Campaign Report]](/help/search-social-commerce/reports/management/basic-advanced/campaign-report.md)</li><li>[Die [!UICONTROL Ad Group Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-group-report.md)</li><li>[Die [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Performance-Fehlerbehebung und Trend-Analyse | <ul><li>[Die [!UICONTROL Keyword Report]](/help/search-social-commerce/reports/management/basic-advanced/keyword-report.md)</li><li>[Die [!UICONTROL Ad Variation Report]](/help/search-social-commerce/reports/management/basic-advanced/ad-variation-report.md)</li><li>[Die [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)</li><li>[Die [!UICONTROL RSA Asset Report]](/help/search-social-commerce/reports/management/specialty/rsa-asset-report.md)</li><li>[Die [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/keyword-daily-impression-share-report.md) und [Die [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Jeder grundlegende Bericht, der zwei Zeitfenster mit dem[!UICONTROL Compare with]&quot;-Funktion</li></ul> |
| Ermitteln von Geschäftswachstumsmöglichkeiten | <ul><li>(Nur Advertiser mit Adobe Advertising-Konversions-Tracking) [Die [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Nur Advertiser mit Adobe Advertising-Konversions-Tracking) [Die [!UICONTROL Domain Referral Report]](/help/search-social-commerce/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Werbetreibende mit [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Benutzerdefinierte Berichte in Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Nur Advertiser mit Adobe Advertising-Konversions-Tracking) [Die [!UICONTROL Channel Assist Report]](/help/search-social-commerce/reports/management/assist/channel-assist-report.md)</li><li>(Werbetreibende mit [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Benutzerdefinierte Berichte in Adobe Analytics Analysis Workspace</li></ul> |

>[!MORELIKETHIS]
>
>* [Für Berichte verwendete Daten](data-used-for-reports.md)
>* [Erste Einrichtungsaufgaben für Berichte](initial-setup.md)
>* [Erstellen eines einfachen oder erweiterten Berichts](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [Modellexaktionsbericht generieren](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-generate.md)
>* [Einen Spezialbericht erstellen](/help/search-social-commerce/reports/management/specialty/specialty-report-generate.md)
>* [Hilfsbericht erstellen](/help/search-social-commerce/reports/management/assist/assist-report-generate.md)
