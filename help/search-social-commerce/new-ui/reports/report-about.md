---
title: (Neue Benutzeroberfläche) Informationen zu terminierten Berichten
description: Erfahren Sie mehr über geplante Leistungsberichte, einschließlich der verschiedenen verfügbaren Berichtstypen und der Automatisierung von Berichten.
feature: Search Reports
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: e246c273-d720-4ece-b29b-7aaba7d50169
  - id: c916feea-e212-4773-b673-4daed287b8a3
  - id: adcb1be7-7ed0-464d-a8d4-c905c9d47742
  - id: ff99aaef-142d-4c93-a88c-011e979e3843
  - id: fa0141e5-dc99-4fbd-9c0e-40aff66de606
  - id: b36a77b1-3c8f-4e1c-8b0b-6e0ba3fb2664
source-git-commit: bd4246ec79684167254a153d2f3d0b917a493096
workflow-type: tm+mt
source-wordcount: 857
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Informationen zu terminierten Berichten

Mit terminierten Leistungsberichten können Sie die Leistung Ihrer Portfolios, Werbenetzwerke und Anzeigennetzwerkkontoentitäten auf einer gewünschten granularen Ebene verfolgen und verwalten. Die meisten Berichte bieten vollständige Einblicke in den Beitrag, den die Anzeigen in den einzelnen Marketing-Kanälen zur Gesamtkonversionsrate leisten.

Die Daten für einen Bericht werden bei jeder Ausführung des Berichts dynamisch kompiliert. Optional können Sie einen neuen Bericht aus einem vorhandenen Bericht generieren. Die verfügbaren Berichtsparameter variieren je nach Berichtstyp. Bei den meisten Berichten haben Sie die Möglichkeit, die ersten 50 Zeilen in der Vorschau anzuzeigen, anstatt den gesamten Bericht zu generieren. Wenn Sie einen Bericht generieren, können Sie nach Abschluss eines Berichts eine Benachrichtigung mit Download-Links an eine oder mehrere E-Mail-Adressen senden und die Empfänger können [die Benachrichtigungen in [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md) verwalten.

Alle abgeschlossenen Berichte sind im Abschnitt [!UICONTROL Latest Reports] der [!UICONTROL Reports] verfügbar, und Sie können sie entweder im Tabellenformat im Browserfenster anzeigen oder als Dateien öffnen oder herunterladen.

## Verfügbare Berichtskategorien

Die folgenden Berichtskategorien sind in der [!UICONTROL Scheduled Reports] verfügbar. Möglicherweise haben Sie nicht auf alle Berichte Zugriff. Die verfügbaren Berichte und die von ihnen generierten Daten werden durch Ihre Rolle und die Konfiguration Ihres Kundenkontos bestimmt.

| Berichtskategorie | Beschreibung |
| ----| ---- |
| [!UICONTROL Basic Reports] | [Standardberichte](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md) die allen Benutzern zur Verfügung stehen, zeigen die Ist-Kosten- und Klickdaten für Portfolios, Werbenetzwerkkonten, spezifische Werbenetzwerkkonten, Kampagnen, Anzeigengruppen, Anzeigen, Schlüsselwörter, Produktgruppen, Kennzeichnungsklassifizierungen und Kennzeichnungswerte, Einschränkungen der Gebotseinheiten und Netzwerkeinschränkungen an. Sie basieren auf Klicks, die von den entsprechenden Werbenetzwerken in Rechnung gestellt werden, und können optional Konversionsdaten oder andere von Ihnen erstellte Metriken enthalten. |
| [!UICONTROL Advanced Reports] | [Erweiterte Berichte](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md) bieten zusätzliche insight in Ihrer Werbekonfiguration, sodass Sie erkennen können, wo Sie von einer Änderung Ihrer geografischen Zielgruppenbestimmungs- oder Netzwerkeinstellungen profitieren würden. Sie können auch dabei helfen, Konversionsdaten in den Ansichten und Berichten der Kampagnen- und Portfolioverwaltung mit den internen Konversionsverfolgungsdaten des Werbetreibenden zu vergleichen. |
| [!UICONTROL Assist Reports] | [Assist-Berichte](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-about.md) bieten Einblicke in die Konversionspfade für alle Keywords und Anzeigen eines Advertisers. Sie verwenden Daten, die über den Konversionsverfolgungs-Service von Adobe Advertising erfasst werden, und können nur für Werbetreibende mit dem Service erzeugt werden. |
| [!UICONTROL Specialty Reports] | [Spezialberichte](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-about.md) bestehen aus Daten, die von den Werbenetzwerken (und nicht vom Adobe Advertising-Tracking) erfasst werden. |
| [!UICONTROL Model Accuracy Reports] | [Modellgenauigkeitsberichte](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-about.md) geben die Genauigkeit der Kosten- und Umsatzmodelle an, die zur Optimierung von Angeboten, Kampagnenbudgets und Bid-Strategie-Zielen für ein Portfolio verwendet werden. |

## Berichtsautomatisierung

Sie können benutzerdefinierte Berichte so planen, dass sie automatisch auf eine oder beide der folgenden Arten generiert werden:

* Erstellt mithilfe von „Berichtsvorlagen“ automatisch Berichte täglich oder an einem bestimmten Wochentag [&#x200B; Monat](/help/search-social-commerce/new-ui/reports/report-templates-manage.md).

  Optional können Sie die [FTP-Bereitstellung von einfachen und erweiterten Berichten](/help/search-social-commerce/new-ui/reports/ftp-reports.md) die eine Vorlage verwenden, einrichten.

* Aktualisieren Sie Ihre benutzerdefinierten Tabellenvorlagen mit täglichen Leistungsdaten mithilfe von [Tabellenfeeds](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md).

## Die [!UICONTROL Scheduled Reports]

Mit der Ansicht [!UICONTROL Reports] > [!UICONTROL Scheduled Reports] können Sie Berichte, Vorlagen und Tabellen-Feeds erstellen und verwalten. Die Ansicht enthält zwei Registerkarten:

* Auf der Registerkarte **[!UICONTROL Latest Reports]** werden alle Berichte aufgelistet, die in den letzten sieben Tagen angefordert wurden, mit Ausnahme der manuell gelöschten Berichte. Der neueste Bericht befindet sich standardmäßig oben. Zu den für jeden Bericht angezeigten Informationen gehören der Zeitplan, nach dem er ausgeführt wird (falls zutreffend), das Start- und Enddatum, für das Daten generiert wurden oder werden werden, und der Berichtsstatus (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]* oder *[!UICONTROL Error]*).

  Über Links neben den einzelnen Berichten können Sie den Bericht im Webbrowser anzeigen, öffnen oder als [!DNL Microsoft Excel] Arbeitsmappe (XLS) oder TSV-Datei (tabulatorgetrennte Werte) speichern. Einige Berichtstypen können auch als [!UICONTROL Excel] Arbeitsmappen mit einem separaten Arbeitsblatt für jede entsprechende Kampagne gespeichert werden.

  Auf dieser Registerkarte können Sie auch einen neuen Bericht erstellen (der optional als Vorlage verwendet werden kann), einen neuen Bericht auf der Grundlage der Einstellungen für einen vorhandenen Bericht erstellen, die Ihnen zur Verfügung stehenden Berichte in Bearbeitung abbrechen, indem Sie sie löschen, und alle abgeschlossenen Berichte löschen, die Ihnen zur Verfügung stehen. Berichte, die älter als sieben Tage sind, werden automatisch gelöscht.

* Auf der Registerkarte **[!UICONTROL Templates]** werden alle gespeicherten einfachen und erweiterten Berichtsvorlagen aufgelistet, die Ihnen zur Verfügung stehen, einschließlich Informationen zu Zeitplänen, die mit ihnen verknüpft sind. Die neueste Vorlage befindet sich standardmäßig oben.

  Auf dieser Registerkarte können Sie eine neue Vorlage erstellen, eine von Ihnen erstellte Vorlage bearbeiten (einschließlich Hinzufügen, Ändern oder Entfernen der Vorlage), einen Bericht aus einer Vorlage erstellen und alle verfügbaren Vorlagen löschen.

## Verwendung von Berichten

| Zweck | Bericht |
| ---- | ---- |
| Leistungsüberwachung | <ul><li>[Die [!UICONTROL Portfolio Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/portfolio-report.md)</li><li>[Die [!UICONTROL Search Engine Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-report.md)</li><li>[Die [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[Die [!UICONTROL Campaign Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/campaign-report.md)</li><li>[Die [!UICONTROL Ad Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-group-report.md)</li><li>[Die [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/new-ui/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Fehlerbehebung und Trendanalyse der Leistung | <ul><li>[Die [!UICONTROL Keyword Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/keyword-report.md)</li><li>[Die [!UICONTROL Ad Variation Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-variation-report.md)</li><li>[Die [!UICONTROL Transaction Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)</li><li>[Die [!UICONTROL RSA Asset Report]](/help/search-social-commerce/new-ui/reports/management/specialty/rsa-asset-report.md)</li><li>[Die [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/keyword-daily-impression-share-report.md) und [Die [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Ein einfacher Bericht, der zwei Zeitfenster mithilfe der Funktion &quot;[!UICONTROL Compare with]&quot; vergleicht</li></ul> |
| Identifizieren von Wachstumschancen für Unternehmen | <ul><li>(Nur Werbetreibende mit Adobe Advertising-Konversions-Tracking) [Die [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Nur Werbetreibende mit Adobe Advertising-Konversions-Tracking) [Die [!UICONTROL Domain Referral Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Werbetreibende mit [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Benutzerdefinierte Berichte in Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Nur Werbetreibende mit Adobe Advertising-Konversions-Tracking) [Die [!UICONTROL Channel Assist Report]](/help/search-social-commerce/new-ui/reports/management/assist/channel-assist-report.md)</li><li>(Werbetreibende mit [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Benutzerdefinierte Berichte in Adobe Analytics Analysis Workspace</li></ul> |

>[!MORELIKETHIS]
>
>* [Die anfänglichen Einrichtungsaufgaben für Berichte](initial-setup.md)
>* [Die für Berichte verwendeten Daten](data-used-for-reports.md)
>* [Terminierte Berichte verwalten](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
