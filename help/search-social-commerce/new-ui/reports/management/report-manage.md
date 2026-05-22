---
title: Terminierte Berichte verwalten
description: Erfahren Sie, wie Sie terminierte Berichte verwalten.
feature: Search Reports, Search Basic Reports, Search Advanced Reports, Search Assist Reports, Search Model Accuracy Reports, Search Specialty Reports
source-git-commit: bfca434eacf52ec7236804c54b7740442aa12961
workflow-type: tm+mt
source-wordcount: '1571'
ht-degree: 0%

---

# Terminierte Berichte verwalten

Leistungsberichte ermöglichen es Ihnen, die Leistung Ihrer Portfolios, Werbenetzwerke und Anzeigennetzwerkkontoentitäten auf einer gewünschten granularen Ebene zu verfolgen und zu verwalten. Die meisten Berichte bieten vollständige Einblicke in den Beitrag, den die Anzeigen in den einzelnen Marketing-Kanälen zur Gesamtkonversionsrate leisten.

Die Daten für einen Bericht werden bei jeder Ausführung des Berichts dynamisch kompiliert. Optional können Sie einen neuen Bericht aus einem vorhandenen Bericht generieren. Die verfügbaren Berichtsparameter variieren je nach Berichtstyp. Bei den meisten Berichten haben Sie die Möglichkeit, die ersten 50 Zeilen in der Vorschau anzuzeigen, anstatt den gesamten Bericht zu generieren. Wenn Sie einen Bericht generieren, können Sie nach Abschluss eines Berichts eine Benachrichtigung mit Download-Links an eine oder mehrere E-Mail-Adressen senden und die Empfänger können [die Benachrichtigungen in [!UICONTROL Notification Center]](/help/search-social-commerce/notifications/notification-about.md) verwalten.

Alle abgeschlossenen Berichte sind im Abschnitt [!UICONTROL Latest Reports] der [!UICONTROL Reports] verfügbar, und Sie können sie entweder im Tabellenformat im Browserfenster anzeigen oder als Dateien öffnen oder herunterladen.

## Verfügbare Berichtskategorien

Die folgenden Berichtskategorien sind in der [!UICONTROL Reports] verfügbar. Möglicherweise haben Sie nicht auf alle Berichte Zugriff. Die verfügbaren Berichte und die von ihnen generierten Daten werden durch Ihre Rolle und die Konfiguration Ihres Kundenkontos bestimmt.

| Berichtskategorie | Beschreibung |
| ----| ---- |
| [!UICONTROL Basic Reports] | [Standardberichte](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md) die allen Benutzern zur Verfügung stehen, zeigen die Ist-Kosten- und Klickdaten für Portfolios, Werbenetzwerkkonten, spezifische Werbenetzwerkkonten, Kampagnen, Anzeigengruppen, Anzeigen, Schlüsselwörter, Produktgruppen, Kennzeichnungsklassifizierungen und Kennzeichnungswerte, Einschränkungen der Gebotseinheiten und Netzwerkeinschränkungen an. Sie basieren auf Klicks, die von den entsprechenden Werbenetzwerken in Rechnung gestellt werden, und können optional Konversionsdaten oder andere von Ihnen erstellte Metriken enthalten. |
| [!UICONTROL Advanced Reports] | [Erweiterte Berichte](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md) bieten zusätzliche insight in Ihrer Werbekonfiguration, sodass Sie erkennen können, wo Sie von einer Änderung Ihrer geografischen Zielgruppenbestimmungs- oder Netzwerkeinstellungen profitieren würden. Sie können auch dabei helfen, Konversionsdaten in den Ansichten und Berichten der Kampagnen- und Portfolioverwaltung mit den internen Konversionsverfolgungsdaten des Werbetreibenden zu vergleichen. |
| [!UICONTROL Assist Reports] | [Assist-Berichte](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-about.md) bieten Einblicke in die Konversionspfade für alle Keywords und Anzeigen eines Advertisers. Sie verwenden Daten, die über den Konversionsverfolgungs-Service von Adobe Advertising erfasst werden, und können nur für Werbetreibende mit dem Service erzeugt werden. |
| [!UICONTROL Specialty Reports] | [Spezialberichte](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-about.md) bestehen aus Daten, die von den Werbenetzwerken (und nicht vom Adobe Advertising-Tracking) erfasst werden. |
| [!UICONTROL Model Accuracy Reports] | [Modellgenauigkeitsberichte](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-about.md) geben die Genauigkeit der Kosten- und Umsatzmodelle an, die zur Optimierung von Angeboten, Kampagnenbudgets und Bid-Strategie-Zielen für ein Portfolio verwendet werden. |

## Berichtsautomatisierung

Sie können benutzerdefinierte Berichte so planen, dass sie automatisch auf eine oder beide der folgenden Arten generiert werden:

* Erstellt mithilfe von „Berichtsvorlagen“ automatisch Berichte täglich oder an einem bestimmten Wochentag [&#x200B; Monat](/help/search-social-commerce/reports/automation/templates/template-about.md).

  Optional können Sie die [FTP-Bereitstellung von einfachen und erweiterten Berichten](/help/search-social-commerce/new-ui/reports/ftp-reports.md) die eine Vorlage verwenden, einrichten.

* Aktualisieren Sie Ihre benutzerdefinierten Tabellenvorlagen mit täglichen Leistungsdaten mithilfe von [Tabellenfeeds](/help/search-social-commerce/new-ui/reports/spreadsheet-feeds-manage.md).

## Die [!UICONTROL Scheduled Reports]

Mit [!UICONTROL Reports] > [!UICONTROL Scheduled Reports] können Sie Berichte und Berichtsvorlagen erstellen und verwalten:

* Auf der Registerkarte **[!UICONTROL Latest Reports]** werden alle Berichte aufgelistet, <!-- Doesn't seem to be true: that were requested in the last seven days --> Ihnen zur Verfügung stehen, mit Ausnahme der manuell gelöschten Berichte. Der neueste Bericht befindet sich standardmäßig oben. Zu den für jeden Bericht angezeigten Informationen gehören der Zeitplan, nach dem er ausgeführt wird (falls zutreffend), das Start- und Enddatum, für das Daten generiert wurden oder werden werden, der Ersteller des Berichts und der Berichtsstatus (*[!UICONTROL Finished]*, *[!UICONTROL In Progress]* oder *[!UICONTROL Error]*).

  Über Links neben den einzelnen Berichten können Sie den Bericht als [!DNL Microsoft Excel]-Arbeitsmappe (XLS), als TSV-Datei (Tabulatorgetrennte Werte) oder als CSV-Datei (kommagetrennte Werte) öffnen oder speichern. Einige Berichtstypen können auch als [!UICONTROL Excel] mit einem separaten Arbeitsblatt für jede entsprechende Kampagne gespeichert werden.

  Auf dieser Registerkarte können Sie auch einen neuen Bericht erstellen (der optional als Vorlage verwendet werden kann), einen neuen Bericht basierend auf den Einstellungen für einen vorhandenen Bericht erstellen oder eine Berichtsvorlage verwenden, die Ihnen zur Verfügung stehenden Berichte abbrechen, indem Sie sie löschen, und alle abgeschlossenen Berichte löschen, die Ihnen zur Verfügung stehen.

* Auf der Registerkarte **[!UICONTROL Templates]** werden alle gespeicherten einfachen und erweiterten Berichtsvorlagen aufgelistet, die Ihnen zur Verfügung stehen, einschließlich Informationen zu Zeitplänen, die mit ihnen verknüpft sind. Die neueste Vorlage befindet sich standardmäßig oben.

  Auf dieser Registerkarte können Sie eine neue Vorlage erstellen, eine von Ihnen erstellte Vorlage bearbeiten (einschließlich Hinzufügen, Ändern oder Entfernen der Vorlage), einen Bericht aus einer Vorlage erstellen und alle verfügbaren Vorlagen löschen.

## Verwendung von Berichten

| Zweck | Bericht |
| ---- | ---- |
| Leistungsüberwachung | <ul><li>[Die [!UICONTROL Portfolio Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/portfolio-report.md)</li><li>[Die [!UICONTROL Search Engine Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-report.md)</li><li>[Die [!UICONTROL Search Engine Account Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/search-engine-account-report.md)</li><li>[Die [!UICONTROL Campaign Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/campaign-report.md)</li><li>[Die [!UICONTROL Ad Group Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-group-report.md)</li><li>[Die [!UICONTROL Forecast Accuracy Report]](/help/search-social-commerce/new-ui/reports/management/model-accuracy/forecast-accuracy-report.md)</li></ul> |
| Fehlerbehebung und Trendanalyse der Leistung | <ul><li>[Die [!UICONTROL Keyword Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/keyword-report.md)</li><li>[Die [!UICONTROL Ad Variation Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/ad-variation-report.md)</li><li>[Die [!UICONTROL Transaction Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)</li><li>[Die [!UICONTROL RSA Asset Report]](/help/search-social-commerce/new-ui/reports/management/specialty/rsa-asset-report.md)</li><li>[Die [!UICONTROL Keyword Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/keyword-daily-impression-share-report.md) und [Die [!UICONTROL Campaign Daily Impression Share Report]](/help/search-social-commerce/new-ui/reports/management/specialty/campaign-daily-impression-share-report.md)</li><li>Ein einfacher Bericht, der zwei Zeitfenster mithilfe der Funktion &quot;[!UICONTROL Compare with]&quot; vergleicht</li></ul> |
| Identifizieren von Wachstumschancen für Unternehmen | <ul><li>(Nur Werbetreibende mit Adobe Advertising-Konversions-Tracking) [Die [!UICONTROL Geo Distribution Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/geo-distribution-report.md)</li><li>(Nur Werbetreibende mit Adobe Advertising-Konversions-Tracking) [Die [!UICONTROL Domain Referral Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/domain-referral-report.md)</li><li>(Werbetreibende mit [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Benutzerdefinierte Berichte in Adobe Analytics Analysis Workspace</li></ul> |
| Analytics | <ul><li>(Nur Werbetreibende mit Adobe Advertising-Konversions-Tracking) [Die [!UICONTROL Channel Assist Report]](/help/search-social-commerce/new-ui/reports/management/assist/channel-assist-report.md)</li><li>(Werbetreibende mit [Adobe [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)) Benutzerdefinierte Berichte in Adobe Analytics Analysis Workspace</li></ul> |

## Erstellen von Berichten

### Erstellen eines neuen Berichts

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**.

1. Klicken Sie auf **[!UICONTROL Create Report]**, klicken Sie im linken Bereich auf die Kategorie Bericht und wählen Sie dann den Berichtstyp aus.<!-- Add link to list of report categories and report types --> Klicken Sie auf **[!UICONTROL Proceed]**.

1. (Optional) Ändern Sie im [!UICONTROL Create Report] die standardmäßigen Berichteinstellungen für [Basis- und erweiterte Berichte](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md), [Assist-Berichte](/help/search-social-commerce/new-ui/reports/management/assist/assist-report-settings.md), [Modellgenauigkeitsberichte](/help/search-social-commerce/new-ui/reports/management/model-accuracy/model-accuracy-report-settings.md) und [Spezialberichte](/help/search-social-commerce/new-ui/reports/management/specialty/specialty-report-settings.md):

   1. (Optional) Geben Sie einen benutzerdefinierten Namen für den Bericht und für die Vorlage ein (wenn Sie den Bericht als Vorlage speichern).

   1. (Optional) Um die Berichtseinstellungen als Vorlage zu speichern, aktivieren Sie die **[!UICONTROL Save as template]**.

   1. (Optional) Wählen Sie innerhalb derselben Berichtskategorie einen anderen **[!UICONTROL Type]** aus.

   1. (Optional) Wählen Sie auf der Registerkarte **[!UICONTROL Basic Settings]** eine vorhandene Berichtsvorlage aus, um die standardmäßigen Grundeinstellungen für den Bericht zu verwenden oder zu ändern.

   1. (Optional) Klicken Sie auf die Registerkarte **[!UICONTROL Columns]** und ändern Sie die Standardspalten im Bericht, einschließlich der Spaltenreihenfolge.

      Standardmäßig werden alle monetären Daten in Berichten im Format für US-Dollar angezeigt (z. B. 1.000,00). Um den Wert im richtigen Währungsformat (aber ohne Währungssymbole im CSV- und TSV-Format) anzuzeigen, fügen Sie dem Bericht die Spalte &quot;[!UICONTROL Currency]&quot; hinzu. Wenn der Bericht Daten für Konten mit unterschiedlichen Währungen enthält, sind alle &quot;[!UICONTROL Total]&quot; Geldwerte die Summe aller Zahlen in der Spalte, unabhängig von der Währung.

   1. (Einige Berichtstypen, optional) Klicken Sie auf die Registerkarte **[!UICONTROL Filters & Attribution]** oder **[!UICONTROL Filters]** und fügen Sie Datenfilter hinzu, beschränken Sie (einige Berichtstypen) die Berichtsergebnisse auf bestimmte Beschriftungsklassifizierungen und ändern Sie die standardmäßigen Attributionsregeln und Konversionszuordnungseinstellungen.

   1. (Optional) Klicken Sie auf die Registerkarte **[!UICONTROL Scheduling]** und ändern Sie die standardmäßigen Zeitplan- und Versandoptionen.

1. Klicken Sie auf **[!UICONTROL Create]**.

Wenn Sie keinen Berichtszeitplan angegeben haben, wird der Bericht sofort ausgeführt. Andernfalls wird er gemäß dem angegebenen Zeitplan ausgeführt. Der Berichtsname wird der [[!UICONTROL Latest Reports] hinzugefügt](/help/search-social-commerce/reports/report-about.md). Wenn Sie den Bericht als Vorlage gespeichert haben, wird er auch der [[!UICONTROL Templates] hinzugefügt](/help/search-social-commerce/reports/report-about.md). Nach Fertigstellung des Berichts kann die Datei geöffnet oder gespeichert werden. Vorlagen sind sofort verfügbar.

Wenn Sie E-Mail-Adressen zur Benachrichtigung eingegeben haben, erhält jeder Empfänger eine Benachrichtigung, wenn der Berichtsvorgang abgeschlossen wurde oder fehlschlägt, basierend auf den [konfigurierten Benachrichtigungseinstellungen](/help/search-social-commerce/notifications/notification-edit.md) für Berichte.

### Erstellen eines Berichts aus einem vorhandenen Bericht

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**. Daraufhin wird die Registerkarte **[!UICONTROL Latest Reports]** geöffnet.

1. Führen Sie einen der folgenden Schritte aus:

   * Halten Sie den Cursor über die Berichtszeile und klicken Sie auf **…** > **[!UICONTROL Duplicate]**.

   * Aktivieren Sie das Kontrollkästchen neben dem Bericht. Klicken Sie in der Symbolleiste für Massenaktionen auf [Duplizieren](/help/search-social-commerce/assets/duplicate.png "Duplikat").

1. Bearbeiten Sie bei Bedarf die Berichteinstellungen.

1. Klicken Sie auf **[!UICONTROL Create]**.

### Erstellen eines Berichts aus einer vorhandenen Vorlage

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Templates]** .

1. Führen Sie einen der folgenden Schritte aus:

   * Halten Sie den Cursor über der Vorlagenzeile und klicken Sie auf **…** > **[!UICONTROL Duplicate]**.

   * Aktivieren Sie das Kontrollkästchen neben der vorhandenen Vorlage. Klicken Sie in der Symbolleiste für Massenaktionen auf [Duplizieren](/help/search-social-commerce/assets/duplicate.png) **[!UICONTROL Duplicate]**.

1. (Optional) Benennen Sie die Vorlage um und bearbeiten Sie bei Bedarf die Berichteinstellungen.

   Klicken Sie auf **[!UICONTROL Next]** , um zwischen den Einstellungsabschnitten zu wechseln.

1. Aktivieren Sie die **[!UICONTROL Save as Template]**.

1. Klicken Sie auf **[!UICONTROL Create]**.

## Vorschau oder Speichern eines Berichts

Sie können einen Bericht im Webbrowser in der Vorschau anzeigen oder die Berichtsdaten als [!DNL Microsoft Excel] Arbeitsmappe, als TSV-Datei (Tabulatorgetrennte Werte), CSV-Datei (Kommagetrennte Werte) oder (bei einigen Berichtstypen) als Arbeitsmappe mit [!DNL Microsoft Excel] Registerkarten öffnen oder speichern.

>[!NOTE]
>
>Mitglieder des Adobe Account Teams und einige Admin-Benutzer können Berichte anzeigen, die von Advertiser- und Agenturbenutzenden erstellt wurden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**. Daraufhin wird die Registerkarte **[!UICONTROL Latest Reports]** geöffnet.

1. Führen Sie einen der folgenden Schritte aus:

   * (Um einen Bericht im Webbrowser anzuzeigen) Führen Sie einen der folgenden Schritte aus:

      * Halten Sie den Cursor über der Vorlagenzeile und klicken Sie auf **…** > **[!UICONTROL Preview]**.

      * Aktivieren Sie das Kontrollkästchen neben der vorhandenen Vorlage. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Preview]**.

   * (So öffnen oder speichern Sie die Berichtsdaten in einer Datei) Klicken Sie in der Spalte [!UICONTROL Export] neben dem Berichtsnamen auf den Namen eines Formats und öffnen oder speichern Sie die Datei dann entsprechend dem normalen Verfahren Ihres Browsers:

      * **[!UICONTROL XLS]:** Für eine [!DNL Excel] Arbeitsmappe mit einem einzelnen Arbeitsblatt (XLSX-Format). Der Bericht enthält ein Arbeitsblatt, das oben mit den Parametern beschriftet ist, wobei für jede Komponente eine Zeile angezeigt wird, wenn Daten für die Komponente verfügbar sind. Zeilen ohne Daten werden weggelassen.

        Standardberichte enthalten einen Gesamtwert für jede numerische Spalte.

      * **[!UICONTROL TSV]:** Für eine TSV-Datei. Der Bericht enthält die Parameter und eine Zeile für jede gemeldete Komponente.

      * **[!UICONTROL CSV]:** Für eine CSV-Datei. Der Bericht enthält die Parameter und eine Zeile für jede gemeldete Komponente.

## Berichte löschen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Reports]>[!UICONTROL Scheduled Reports]**. Daraufhin wird die Registerkarte **[!UICONTROL Latest Reports]** geöffnet.

1. Führen Sie einen der folgenden Schritte aus:

   * (So löschen Sie einen einzelnen Bericht):

      1. Halten Sie den Cursor über die Berichtszeile und klicken Sie auf **…** > **[!UICONTROL Run]**.

      1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

   * (So löschen Sie einen oder mehrere Berichte):

      1. Aktivieren Sie das Kontrollkästchen neben jedem Bericht, den Sie löschen möchten.

      1. Klicken Sie in der Symbolleiste für Massenaktionen auf [Löschen](/help/search-social-commerce/assets/delete-new.png "Löschen") **[!UICONTROL Delete]**.

      1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

<!--

>[!MORELIKETHIS]
>
>* [About basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [Basic and advanced report settings](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [Report columns for basic and advanced reports](/help/search-social-commerce/new-ui/reports/management/basic-advanced/basic-advanced-report-columns.md)

-->
