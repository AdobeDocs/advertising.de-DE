---
title: Hochladen von Offline-Konversionsdaten für erweiterte Konversionen
description: Erfahren Sie, wie Sie First-Party- und Offline-Konversionsdaten hochladen, um sie Leads  [!DNL Google Ads]  erweiterten Konversionen  [!DNL Microsoft Advertising] .
feature: Conversions
source-git-commit: 88a45014064220a2bec6aa6080a2a1f53d24b9bb
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# Hochladen von Offline-Konversionsdaten für erweiterte Konversionen

<!-- Renamed file to start with "conversions-"-->

<!-- Update to add procedure in new UI -->

Nur *[!DNL Google Ads]und [!DNL Microsoft Advertising] Konten*

Sie können Ihre Erstanbieter-Offline-Konversionsdaten - einschließlich gehashter E-Mail-Adressen und Telefonnummern - hochladen, um sie Ihren vorhandenen [[!DNL Google Ads] erweiterten Konversionen für Leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) und [[!DNL Microsoft Advertising] erweiterten Konversionen](https://help.ads.microsoft.com/#apex/ads/en/60178) zuzuordnen. Alle hochgeladenen Daten werden in Echtzeit mit dem Werbenetzwerk synchronisiert.

## (Neue Benutzeroberfläche) Hochladen von Daten für erweiterte Konversionen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Set up Conversion]**.

1. Geben Sie die Einstellungen für den Datenupload an:

   1. Auf der Registerkarte [!UICONTROL Basic Details] :

      1. Wählen Sie die [!UICONTROL Setup Method] *[!UICONTROL Data Upload]* aus.

      1. Wählen Sie die [!UICONTROL Platform] aus: *[!UICONTROL Google]* oder *[!UICONTROL Microsoft]*.

      1. Klicken Sie auf **[!UICONTROL Next]**.

   1. Auf der Registerkarte [!UICONTROL Configure] :

      1. (Optional) Um eine Vorlage mit allen [erforderlichen Datenfeldern](#enhanced-conversions-leads-data) im [!DNL Microsoft Excel]-Format herunterzuladen, klicken Sie auf **[!UICONTROL Download Template]** und laden Sie dann die Datei entsprechend dem normalen Verfahren Ihres Browsers herunter.

         Sie können die Datei bearbeiten, um Ihre Daten einzubeziehen und Ihre Änderungen zu speichern, und die Datei dann in das angegebene Anzeigennetzwerkkonto hochladen.

      1. Wählen Sie das Netzwerkkonto aus, in das die Daten hochgeladen werden sollen.

      1. Führen Sie im Feld [!UICONTROL Upload Conversion File] einen der folgenden Schritte aus:

         * Ziehen Sie eine Datei in das Feld.

         * Klicken Sie auf **[!UICONTROL Browse File]** und wählen Sie dann eine Datei aus, die von Ihrem Gerät oder Netzwerk hochgeladen werden soll.

   1. Klicken Sie auf **[!UICONTROL Review and Save]** , um die Einstellungen zu überprüfen.

   1. Klicken Sie auf **[!UICONTROL Upload]**.

## (Alte Benutzeroberfläche) Hochladen von Daten für erweiterte Konversionen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**, und klicken Sie dann auf die Registerkarte **[!UICONTROL Upload]**.

1. Wählen Sie das Werbenetzwerk und dann das Konto aus.

1. (Optional) Um eine Vorlage mit allen [erforderlichen Datenfeldern](#enhanced-conversions-leads-data) im [!DNL Microsoft Excel]-Format herunterzuladen, klicken Sie auf **[!UICONTROL View Template]** und laden Sie dann die Datei entsprechend dem normalen Verfahren Ihres Browsers herunter.

   Sie können die Datei bearbeiten, um Ihre Daten einzubeziehen und Ihre Änderungen zu speichern, und die Datei dann im nächsten Schritt hochladen.

1. Klicken Sie auf **[!UICONTROL Choose File]** und wählen Sie dann eine Datei aus, die von Ihrem Gerät oder Netzwerk hochgeladen werden soll.

## Erforderliche Daten für hochgeladene Dateien {#enhanced-conversions-leads-data}

### Daten über der Tabelle

`Parameters:TimeZone=insert_timezone`

Geben Sie die Zeitzone des Kontos entweder an diesem Speicherort oder in der Spalte &quot;[!UICONTROL Conversion Time]&quot; für jede Zeile ein. Verwenden Sie entweder a\) ([!DNL [!DNL Google Ads] only]) das [unterstützte Zeitzonen-ID-Format](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) oder b\) den GMT-Offset, wie durch + oder - angegeben, und die 4-stellige Zeitdifferenz (z. B. -0500 für New York, +0100 für Berlin oder +0000 für Greenwich Mean Time).

### Tabellenspalten und Werte für [!DNL Google Ads]

| Spalte | Beschreibung |
| ------ | ----------- |
| [!UICONTROL Email] | Die E-Mail-Adresse des Benutzers, die mit dem SHA-256-Algorithmus gehasht werden muss. Jede Zeile muss entweder einen [!UICONTROL Email] oder einen [!UICONTROL Phone Number] enthalten. |
| [!UICONTROL Phone Number] | Die Telefonnummer des Benutzers, die mit dem SHA-256-Algorithmus gehasht werden muss. Sie muss einen Ländercode enthalten und darf Bindestriche und andere Symbole enthalten. Jede Zeile muss entweder einen [!UICONTROL Email] oder einen [!UICONTROL Phone Number] enthalten. |
| [!UICONTROL Conversion Name] | (Erforderlich) Der Name der Konvertierungsaktion. |
| [!UICONTROL Conversion Time] | (Erforderlich) Der Zeitpunkt, zu dem das Konversionsereignis in einem (unterstützten [) &#x200B;](https://support.google.com/google-ads/answer/7014069#prepare_data) aufgetreten ist. Wenn Sie die Zeitzonen-ID des Kontos nicht in die `Parameters:TimeZone=insert_timezone` Zeile über der Datentabelle aufnehmen, schließen Sie die Zeitzone für jede Zeile entweder mit a\) dem [unterstützten Zeitzonen-ID-Format](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) oder b\) dem GMT-Offset, wie durch + oder - angegeben, und der 4-stelligen Zeitdifferenz (z. B. -0500 für New York, +0100 für Berlin oder +0000 für Greenwich Mean Time) ein. |
| [!UICONTROL Conversion Value] | (Erforderlich) Der numerische Konvertierungswert. |
| [!UICONTROL Conversion Currency] | Der Währungscode für das Konversionsereignis. |
| [!UICONTROL Ad User Data] | (Gilt für Daten von Benutzern im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (Vereinigtes Königreich)) Gibt an, ob die Benutzerzustimmung für die Übermittlung von Benutzerdaten an [!DNL Google] zu Zwecken der Anzeigenpersonalisierung erteilt wurde. Werte können `Granted`, `Denied` oder \[null\] (der als `Unspecified` an [!DNL Google Ads] gesendet wird) sein. **Hinweis:** [!DNL Google Ads] erzwingt derzeit keine Zustimmung zu erweiterten Konversionen für Leads, kann dies aber in Zukunft tun. |
| [!UICONTROL Ad Personalization] | (Gilt für Daten, die sich auf Benutzer im Europäischen Wirtschaftsraum (EWR) oder im Vereinigten Königreich (Vereinigtes Königreich) beziehen) Gibt an, ob die Benutzerzustimmung für die Übermittlung von Benutzerdaten an [!DNL Google] zu Werbezwecken erteilt wurde. Werte können `Granted`, `Denied` oder \[null\] (der als `Unspecified` an [!DNL Google Ads] gesendet wird) sein. **Hinweis:** [!DNL Google Ads] erzwingt derzeit keine Zustimmung zu erweiterten Konversionen für Leads, kann dies aber in Zukunft tun. |

### Tabellenspalten und Werte für [!DNL Microsoft Advertising]

Weitere Anweisungen zum Formatieren und Hashen der Daten finden Sie in der [!DNL Microsoft Ads]-Dokumentation unter [Erweiterte Konvertierungen](https://help.ads.microsoft.com/#apex/ads/60178).

| Spalte | Beschreibung |
| ------ | ----------- |
| [!UICONTROL Email] | Die E-Mail-Adresse des Benutzers, die mit dem SHA-256-Algorithmus gehasht werden muss. Jede Zeile muss entweder einen [!UICONTROL Email] oder einen [!UICONTROL Phone Number] enthalten. |
| [!UICONTROL Phone Number] | Die Telefonnummer des Benutzers, die mit dem SHA-256-Algorithmus gehasht werden muss. Sie muss einen Ländercode enthalten und darf Bindestriche und andere Symbole enthalten. Bei erweiterten Offline-Konvertierungen muss jede Zeile entweder einen [!UICONTROL Email] oder einen [!UICONTROL Phone Number] enthalten. |
| [!UICONTROL Conversion Name] | (Erforderlich) Der Name der Konvertierungsaktion. |
| [!UICONTROL Conversion Time] | (Erforderlich) Der Zeitpunkt, zu dem das Konversionsereignis aufgetreten ist. Wenn Sie die Zeitzonen-ID des Kontos nicht in der `Parameters:TimeZone=insert_timezone` Zeile über der Datentabelle angeben, schließen Sie die Zeitzone für jede Zeile mit dem GMT-Offset ein, wie durch + oder - angegeben, und die 4-stellige Zeitdifferenz (z. B. -0500 für New York, +0100 für Berlin oder +0000 für Greenwich Mean Time). Eine Liste der Zeitzonen für verschiedene Städte finden Sie unter [https://learn.microsoft.com/en-us/advertising/guides/time-zones](https://learn.microsoft.com/en-us/advertising/guides/time-zones). Achten Sie jedoch darauf, dass Sie das hier angegebene Format anstelle des Formats in der Zeitzonenliste verwenden. |
| [!UICONTROL Conversion Value] | (Erforderlich) Der numerische Konvertierungswert. |
| [!UICONTROL Conversion Currency] | Der Währungscode für das Konversionsereignis. |

>[!MORELIKETHIS]
>
>* [Implementieren [!DNL Google Ads] verbesserter Konversionen für Leads](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [Implementieren  [!DNL Microsoft Advertising]  erweiterten Offline-Konversionen](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* [Erstellen einer Konversionsaktion für eine  [!DNL Google Ads]  Konversion für Leads](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Konversionsmetriken für Suche, Social Media und Commerce-Tracking hochladen nach [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
