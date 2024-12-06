---
title: Hochladen von Offline-Konversionsdaten für erweiterte Konvertierungen
description: Erfahren Sie, wie Sie Erstanbieter- und Offline-Konversionsdaten hochladen können, um diese mit [!DNL Google Ads] erweiterten Konversionen für Leads und [!DNL Microsoft Advertising] erweiterten Konversionen zuzuordnen.
feature: Conversions
exl-id: 5c5dfbb8-3b17-4973-8012-fc7f0e97e33b
source-git-commit: eb7320fdddce4895a689c32ec6fb1e44cb8f2705
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# Hochladen von Offline-Konversionsdaten für erweiterte Konvertierungen

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising] Konten*

Sie können Ihre Erstanbieter-, Offline-Konversionsdaten - einschließlich Hash-E-Mail-Adressen und Telefonnummern - hochladen, um Ihre vorhandenen [[!DNL Google Ads] erweiterten Konversionen für Leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) und [[!DNL Microsoft Advertising] erweiterten Konversionen](https://help.ads.microsoft.com/#apex/ads/en/60178) zuzuordnen. Alle hochgeladenen Daten werden in Echtzeit mit dem Werbenetzwerk synchronisiert.

## Hochladen von Daten für erweiterte Konvertierungen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]** und dann auf die Registerkarte **[!UICONTROL Upload]**.

1. Wählen Sie das Werbenetzwerk und dann das Konto aus.

1. (Optional) Um eine Vorlage mit allen [erforderlichen Datenfeldern](#enhanced-conversions-leads-data) im [!DNL Microsoft Excel] -Format herunterzuladen, klicken Sie auf **[!UICONTROL View Template]** und laden Sie dann die Datei gemäß der üblichen Vorgehensweise Ihres Browsers herunter.

   Sie können die Datei bearbeiten, um Ihre Daten einzuschließen, Ihre Änderungen zu speichern und die Datei dann im nächsten Schritt hochzuladen.

1. Klicken Sie auf **[!UICONTROL Choose File]** und wählen Sie dann eine Datei aus, die Sie von Ihrem Gerät oder Netzwerk hochladen möchten.

## Erforderliche Daten für hochgeladene Dateien {#enhanced-conversions-leads-data}

### Daten über der Tabelle

`Parameters:TimeZone=insert_timezone`

Geben Sie die Zeitzone des Kontos entweder an dieser Stelle oder in der Spalte &quot;[!UICONTROL Conversion Time]&quot; für jede Zeile ein. Verwenden Sie entweder a\) ([!DNL Google Ads only]) das [unterstützte Zeitzonen-ID-Format](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) oder b\) den GMT-Versatz, wie durch + oder - angegeben, und die 4-stellige Zeitdifferenz (z. B. -0500 für New York, +0100 für Berlin oder +000 für Greenwich Mean Time).

### Tabellenspalten und -werte für [!DNL Google Ads]

| Spalte | Beschreibung |
| ------ | ----------- |
| E-Mail | Die E-Mail-Adresse des Benutzers, die mit dem SHA-256-Algorithmus gehasht werden muss. Jede Zeile muss entweder einen E-Mail-Wert oder einen Telefonnummernwert enthalten. |
| Telefonnummer | Die Telefonnummer des Benutzers, die mit dem SHA-256-Algorithmus gehasht werden muss. Sie muss einen Ländercode enthalten und kann Gedankenstriche und andere Symbole enthalten. Jede Zeile muss entweder einen E-Mail-Wert oder einen Telefonnummernwert enthalten. |
| Konversionsname | (Erforderlich) Der Name der Konvertierungsaktion. |
| Konvertierungszeit | (Erforderlich) Der Zeitpunkt, zu dem das Konversionsereignis in einem [unterstützten Zeitformat](https://support.google.com/google-ads/answer/7014069#prepare_data) aufgetreten ist. Wenn Sie die Zeitzonen-ID des Kontos nicht in die Zeile &quot;`Parameters:TimeZone=insert_timezone`&quot;oberhalb der Datentabelle einschließen, fügen Sie die Zeitzone für jede Zeile ein, indem Sie a\) das Format [unterstützte Zeitzonen-ID-Format](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) oder b\) den GMT-Versatz verwenden, wie durch &quot;+&quot;oder - und die vierstellige Zeitdifferenz (z. B. -0500 für New York, +010 für Berlin angegeben. 0000 für Greenwich Mean Time). |
| Konversionswert | (Erforderlich) Der numerische Konversionswert. |
| Konversionswährung | Der Währungscode für das Konversionsereignis. |
| Anzeigenbenutzerdaten | (Gilt für Daten über Nutzer im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (UK)) Gibt an, ob die Zustimmung des Nutzers zum Senden von Benutzerdaten an [!DNL Google] zu Anzeigenpersonalisierungszwecken erteilt wurde. Die Werte können `Granted`, `Denied` oder \[null\] enthalten (was an [!DNL Google Ads] als `Unspecified` gesendet wird). **Hinweis:** [!DNL Google Ads] erzwingt derzeit keine Zustimmung für erweiterte Konversionen für Leads, kann dies aber in Zukunft tun. |
| Ad Personalization | (Gilt für Daten über Nutzer im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (UK)) Gibt an, ob die Zustimmung des Nutzers zur Übermittlung von Benutzerdaten zu Werbezwecken an [!DNL Google] erteilt wurde. Die Werte können `Granted`, `Denied` oder \[null\] enthalten (was an [!DNL Google Ads] als `Unspecified` gesendet wird). **Hinweis:** [!DNL Google Ads] erzwingt derzeit keine Zustimmung für erweiterte Konversionen für Leads, kann dies aber in Zukunft tun. |

### Tabellenspalten und -werte für [!DNL Microsoft Advertising]

Weitere Anweisungen zur Verwendung der Vorlage finden Sie unter [https://help.ads.microsoft.com/#apex/3/56852](https://help.ads.microsoft.com/#apex/3/56852).

| Spalte | Beschreibung |
| ------ | ----------- |
| Konversionsname | (Erforderlich) Der Name des Konversionsziels. |
| Konvertierungszeit | (Erforderlich) Der Zeitpunkt, zu dem das Konversionsereignis eingetreten ist. Wenn Sie die Zeitzonen-ID des Kontos nicht in die Zeile `Parameters:TimeZone=insert_timezone` oberhalb der Datentabelle einschließen, fügen Sie die Zeitzone für jede Zeile mit dem GMT-Versatz ein, wie durch + oder - angegeben, und die vierstellige Zeitdifferenz (z. B. -0500 für New York, +0100 für Berlin oder +000 für Greenwich Mean Time). Eine Liste der Zeitzonen für verschiedene Städte finden Sie unter [https://learn.microsoft.com/en-us/advertising/guides/time-zones](https://learn.microsoft.com/en-us/advertising/guides/time-zones). Achten Sie jedoch darauf, das hier angegebene Format anstelle des Formats in der Zeitzonenliste zu verwenden. |
| Konversionswert | (Erforderlich) Der numerische Konversionswert. |
| Konversionswährung | Der Währungscode für das Konversionsereignis. |
| Microsoft-Klick-ID | Die zugehörige eindeutige [!DNL Microsoft] Klick-ID (MSCLKID). Dieses Feld kann für erweiterte Offline-Konvertierungen leer sein. |
| Hash-E-Mail-Adresse | Die E-Mail-Adresse des Benutzers, die mit dem SHA-256-Algorithmus gehasht werden muss. Für erweiterte Offline-Konvertierungen muss jede Zeile entweder einen Hash-Wert für die E-Mail-Adresse oder einen Hash-Wert für die Telefonnummer enthalten. |
| Hash-Telefonnummer | Die Telefonnummer des Benutzers, die mit dem SHA-256-Algorithmus gehasht werden muss. Sie muss einen Ländercode enthalten und kann Gedankenstriche und andere Symbole enthalten. Für erweiterte Offline-Konvertierungen muss jede Zeile entweder einen Hash-Wert für die E-Mail-Adresse oder einen Hash-Wert für die Telefonnummer enthalten. |

>[!MORELIKETHIS]
>
>* [Implementieren [!DNL Google Ads] verbesserter Konvertierungen für Leads](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [Implementieren [!DNL Microsoft Advertising] verbesserter Offline-Konvertierungen](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* ([!DNL Google Ads only])[Erstellen Sie eine Konversionsaktion für eine [!DNL Google Ads] erweiterte Konversion für Leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Laden Sie die von Search, Social und Commerce verfolgten Konversionsmetriken in [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md) hoch.
