---
title: Hochladen von Offline-Konversionsdaten für erweiterte Konvertierungen
description: Erfahren Sie, wie Sie Erstanbieter- und Offline-Konversionsdaten hochladen können, um diese mit [!DNL Google Ads] erweiterten Konversionen für Leads zuzuordnen.
feature: Conversions
source-git-commit: c3cb1549adeb7b621c1b426c53da9bb09eddcbdc
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# Hochladen von Offline-Konversionsdaten für erweiterte Konvertierungen

*[!DNL Google Ads]nur Konten*

<!-- Tweak metadata title/description and heading -->

Sie können Ihre Erstanbieter-, Offline-Konversionsdaten - einschließlich Hash-E-Mail-Adressen und Telefonnummern - hochladen, um Ihre vorhandenen [[!DNL Google Ads] verbesserten Konversionen für Leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) zuzuordnen. Alle hochgeladenen Daten werden in Echtzeit mit [!DNL Google Ads] synchronisiert.

## Hochladen von Daten für [!DNL Google Ads] erweiterte Konversionen für Leads

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]** und dann auf die Registerkarte **[!UICONTROL Upload]**.

1. Wählen Sie das Werbenetzwerk und dann das Konto aus.

1. (Optional) Um eine Vorlage mit allen [erforderlichen Datenfeldern](#enhanced-conversions-leads-data) im [!DNL Microsoft Excel] -Format herunterzuladen, klicken Sie auf **[!UICONTROL View Template]** und laden Sie dann die Datei gemäß der üblichen Vorgehensweise Ihres Browsers herunter.

   Sie können die Datei bearbeiten, um Ihre Daten einzuschließen, Ihre Änderungen zu speichern und die Datei dann im nächsten Schritt hochzuladen.

1. Klicken Sie auf **[!UICONTROL Choose File]** und wählen Sie dann eine Datei aus, die Sie von Ihrem Gerät oder Netzwerk hochladen möchten.

## Erforderliche Daten für hochgeladene Dateien {#enhanced-conversions-leads-data}

### Daten über der Tabelle

`Parameters:TimeZone=insert_timezone`

Geben Sie die Zeitzone des Kontos entweder an dieser Stelle oder in der Spalte &quot;[!UICONTROL Conversion Time]&quot; für jede Zeile ein. Verwenden Sie entweder a) das [unterstützte Zeitzonen-ID-Format](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) oder b) den GMT-Versatz, wie durch + oder - angegeben, und die 4-stellige Zeitdifferenz (z. B. -0500 für New York).

### Tabellenspalten und -werte

| Spalte | Beschreibung |
| ------ | ----------- |
| E-Mail | Die E-Mail-Adresse des Benutzers, die mit dem SHA-256-Algorithmus gehasht werden muss. Jede Zeile muss entweder einen E-Mail-Wert oder einen Telefonnummernwert enthalten. |
| Telefonnummer | Die Telefonnummer des Benutzers, die mit dem SHA-256-Algorithmus gehasht werden muss. Sie muss einen Ländercode enthalten und kann Gedankenstriche und andere Symbole enthalten. Jede Zeile muss entweder einen E-Mail-Wert oder einen Telefonnummernwert enthalten. |
| Konversionsname | (Erforderlich) Der Name der Konvertierungsaktion. |
| Konvertierungszeit | (Erforderlich) Der Zeitpunkt, zu dem das Konversionsereignis in einem [unterstützten Zeitformat](https://support.google.com/google-ads/answer/7014069#prepare_data) aufgetreten ist. Wenn Sie die Zeitzonen-ID des Kontos nicht in die Zeile `Parameters:TimeZone=insert_timezone` oberhalb der Datentabelle einschließen, fügen Sie die Zeitzone für jede Zeile ein, indem Sie a) das unterstützte Zeitzonen-ID-Format [2} oder b) den GMT-Versatz verwenden, wie durch + oder - und die 4-stellige Zeitdifferenz (z. B. -0500 für New York) angegeben.](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) |
| Konversionswert | (Erforderlich) Der numerische Konversionswert. |
| Konversionswährung | Der Währungscode für das Konversionsereignis. |
| Anzeigenbenutzerdaten | (Gilt für Daten über Nutzer im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (UK)) Gibt an, ob die Zustimmung des Nutzers zum Senden von Benutzerdaten an [!DNL Google] zu Anzeigenpersonalisierungszwecken erteilt wurde. Die Werte können `Granted`, `Denied` oder \[null\] enthalten (was an [!DNL Google Ads] als `Unspecified` gesendet wird). **Hinweis:** [!DNL Google Ads] erzwingt derzeit keine Zustimmung für erweiterte Konversionen für Leads, kann dies aber in Zukunft tun. |
| Ad Personalization | (Gilt für Daten über Nutzer im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (UK)) Gibt an, ob die Zustimmung des Nutzers zur Übermittlung von Benutzerdaten zu Werbezwecken an [!DNL Google] erteilt wurde. Die Werte können `Granted`, `Denied` oder \[null\] enthalten (was an [!DNL Google Ads] als `Unspecified` gesendet wird). **Hinweis:** [!DNL Google Ads] erzwingt derzeit keine Zustimmung für erweiterte Konversionen für Leads, kann dies aber in Zukunft tun. |

>[!MORELIKETHIS]
>
>* [Erstellen Sie eine Konversionsaktion für eine [!DNL Google Ads] erweiterte Konversion für Leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Implementieren [!DNL Google Ads] verbesserter Konvertierungen für Leads](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [Laden Sie die von Search, Social und Commerce verfolgten Konversionsmetriken in [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md) hoch.
