---
title: Anzeigen verwalten
description: Erfahren Sie, wie Sie Anzeigen erstellen und verwalten, einschließlich der verfügbaren Anzeigentypen.
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 730b474b83ae4df47c18f93adfec62b1dc9b8a16
workflow-type: tm+mt
source-wordcount: 1732
ht-degree: 0%

---

# Anzeigen verwalten

*Beta-Funktion*

Nur *[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising], [!DNL Yandex] und bestehende [!DNL Baidu] Konten*

Eine Anzeige gehört zu einer Anzeigengruppe und enthält den Inhalt, der Benutzenden angezeigt wird, z. B. die Überschrift, Beschreibung, das Bild oder andere kreative Elemente, je nach Anzeigennetzwerk und Anzeigentyp.

Sobald Sie [ein Anzeigennetzwerkkonto über eine API-Verbindung zugänglich machen](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) und Search, Social und Commerce die Kontodaten mit dem Anzeigennetzwerk synchronisiert haben, können Sie Anzeigen für einen [unterstützten Kampagnentyp“ ](/help/search-social-commerce/introduction/supported-inventory.md). Sie können auch den Status von Anzeigen bearbeiten und ändern.

Einzelheiten zu den für die einzelnen Werbenetzwerke verfügbaren Funktionen finden Sie unter &quot;[Unterstützte Inventarisierung](/help/search-social-commerce/introduction/supported-inventory.md).

## Über die [!UICONTROL Ads] {#ad-view-about}

Die Ansicht [!UICONTROL Manage] > [!UICONTROL Ads] listet alle Anzeigen in der gefilterten Ansicht für das ausgewählte Advertiser-Konto auf.

### Verfügbare Aktionen

* [Erstellen einer Anzeige](#ad-create)

* [Umbenennen einer Anzeige innerhalb der Zeile](#ad-rename)

* [Anzeigeneinstellungen bearbeiten](#ad-edit)

* [Ändern des Status einer Anzeige oder Löschen einer Anzeige](#ad-status)

* [Verwalten von Datenansichtsberichten aus der [!UICONTROL Ads]](#ad-reports)

## Verfügbare Anzeigentypen {#ad-types}

Sie können unterstützte Anzeigentypen für Anzeigengruppen in einem synchronisierten Anzeigennetzwerkkonto erstellen und verwalten:

* **Textanzeigen oder erweiterte Textanzeigen** für eine Anzeigengruppe in einer Kampagne, die auf das Suchnetzwerk abzielt. Textanzeigen können optionale Tracking-Parameter enthalten, die die Parameter auf Anzeigengruppen- oder Kampagnenebene überschreiben. Je nach Anzeigennetzwerk können Sie entweder erweiterte/erweiterte Textanzeigen oder Standardtextanzeigen erstellen.

* Geräteübergreifende, native **Zielgruppen-Anzeigen** für [!DNL Microsoft Advertising] Kampagnen auf der [!DNL Microsoft Audience Network]. Je nach den Kampagneneinstellungen stehen zwei Optionen für Zielgruppenanzeigen zur Verfügung:

  * Wenn die Kampagne mit einem Merchant Center-Store verknüpft ist, lassen Sie das Anzeigennetzwerk automatisch Feed-basierte Anzeigen für die Kampagne generieren, wobei die Produktinformationen des Stores verwendet werden. Sie müssen keine Feed-basierten Anzeigen für die Kampagne erstellen, sondern Anzeigengruppen mit Benutzer-Targeting.

  * Wenn die Kampagne nicht mit einem Merchant Center-Konto verknüpft ist, erstellen Sie bildbasierte Zielgruppenanzeigen mit dem responsiven Anzeigenformat , das mehrere Text- und Bild-Assets enthält. Das Anzeigennetzwerk stellt die Anzeigen mithilfe der effektivsten Kombinationen von Anzeigenelementen zusammen und zeigt sie auf Websites wie [!DNL MSN], [!DNL Outlook.com] und [!DNL Microsoft Edge] an.

* **Nur-Anruf-Anzeigen** für [!DNL Google Ads] Kampagnen im Suchnetzwerk. Reine Anrufanzeigen sind Textanzeigen, die eine Telefonnummer enthalten. Optional können Sie eine [!DNL Google Ads] Weiterleitungsnummer für erweiterte Anrufberichte verwenden.

  >[!NOTE]
  >
  >Sie können derzeit keine Anzeigen auf Anrufbasis erstellen oder bearbeiten. Sie können eine bestehende Anzeige auf der Basis eines reinen Aufrufs anzeigen, ihren Status ändern oder löschen.

* **Erweiterte dynamische Suchanzeigen** (jetzt in den Werbenetzwerken nur noch „dynamische Suchanzeigen“ genannt) für [!DNL Google Ads] und [!DNL Microsoft Advertising] dynamische Suchanzeigengruppen in Suchkampagnen. Dynamische Suchanzeigen verwenden Inhalte von Ihrer Website anstelle von Keywords, um zu entscheiden, wann Ihre Anzeigen angezeigt werden sollen. Das Anzeigennetzwerk generiert dynamisch die Überschrift, wählt die Landingpage-URL und die Anzeige-URL aus und generiert automatisch die endgültige URL.

  Weitere Informationen zu dynamischen Suchanzeigen finden Sie unter [[!DNL Google Ads] ](https://support.google.com/google-ads/answer/2471185) und [[!DNL Microsoft Advertising] Dokumentation](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **Multimedia-Anzeigen** für [!DNL Microsoft Advertising] Suchkampagnen. Multimedia-Anzeigen sind große Bildanzeigen, die an hervorgehobenen Positionen in der Haupt- und Seitenleiste angezeigt werden und pro Seite nur eine Multimedia-Anzeige angezeigt wird. Sie können mehrere Text- und Bild-Assets enthalten, z. B. responsive Anzeigen. Das Werbenetzwerk stellt die Anzeigen mithilfe der effektivsten Kombinationen von Anzeigenelementen zusammen. Multimedia-Anzeigen ersetzen nicht Ihre Text-Anzeigenplatzierungen.

* Promotion-Zeilen für **[!DNL Microsoft Advertising]Produkt (Shopping)-Anzeigen** im Shopping-Netzwerk. Shopping-Anzeigen verwenden Produkte in Ihrem vorhandenen [!DNL Microsoft Merchant Center]-Produkt-Feed anstelle von Keywords, um zu entscheiden, wie und wo Ihre Anzeigen angezeigt werden sollen. Die URLs für die Anzeigenkopie und die Landingpage werden automatisch aus Ihren Produktinformationen im Feed generiert. Sie können jedoch optional Promotion-Zeilen einrichten, die für die Anzeigengruppe enthalten sind.

  Weitere Informationen zu Produktanzeigen finden Sie in der Dokumentation zu [Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/51082).

* **Responsive Suchanzeigen** für [!DNL Google Ads] und [!DNL Microsoft Advertising] Kampagnen im Suchnetzwerk. Das Anzeigennetzwerk stellt textbasierte responsive Suchanzeigen dynamisch aus einer Reihe von Anzeigentiteln und -beschreibungen zusammen und begünstigt Kombinationen, die eine gute Leistung erzielen. Die Anzeige enthält bis zu drei Überschriften, zwei Beschreibungen und eine anpassbare URL aus den Feldern Basis-URL und optionaler Pfad1 und Pfad2. Sie können Anzeigentitel und Beschreibungen optional an bestimmte Positionen anheften.

  >[!NOTE]
  >
  >[!DNL Google Ads] stellt keine Daten über die als Anzeigen angezeigten Textkombinationen außerhalb der nativen Editoren bereit. Weitere Informationen zum Reporting für jede Textkombination finden Sie in der [Dokumentation zu Google Ads](https://support.google.com/google-ads/answer/7684791).

### Leistungsdaten auf Anzeigenebene

Daten auf Anzeigenebene sind für die meisten Anzeigentypen verfügbar.

Sie ist jedoch nicht für [!DNL Google Ads] dynamische Suchanzeige (DSA), die maximale Leistung, den intelligenten Einkauf und [!DNL YouTube] Kampagnen verfügbar. Rechnen Sie daher mit Abweichungen zwischen den gesamten Daten auf Anzeigenebene für eine Kampagne und den gesamten Daten für die Kampagne.

| Anzeigennetzwerk/Kampagne/Anzeigentyp | Datenverfügbarkeit |
|---|---|
| Dynamische Suchanzeige [!DNL Google Ads] (DSA) | Kampagne, Anzeigengruppe |
| Maximale [!DNL Google Ads] | Campaign |
| [!DNL Google Ads] Einkaufen, intelligentes Einkaufen | Kampagne, Anzeigengruppe |
| [!DNL Google Ads] [!DNL YouTube] | Kampagne, Anzeigengruppe |

## Erstellen einer Anzeige {#ad-create}

<!-- Verify that this note is still applicable -->

>[!NOTE]
>
>* Sie müssen keine Produktanzeigen für Shopping-Kampagnen erstellen. Das Werbenetzwerk erstellt sie automatisch. Für [!DNL Microsoft Advertising] Shopping-Kampagnen können Sie jedoch optional Promotion-Zeilen definieren, die in Anzeigen aufgenommen werden sollen.
>* Sie können keine [!DNL Google Ads] Anzeigen erstellen.

>[!TIP]
>
>Um eine große Anzahl von Anzeigen gleichzeitig zu erstellen, verwenden Sie [Kampagnen-Bulksheets](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Klicken Sie auf **[!UICONTROL Create Ads]**.

1. Wählen Sie im **[!UICONTROL Basic Settings]** Schritt das Netzwerk, das Konto, die Kampagne, die Anzeigengruppe und den Anzeigentyp aus.

   Weitere Informationen zu den verfügbaren Anzeigentypen finden Sie unter &quot;[Verfügbare Anzeigentypen](#ad-types).

1. Geben Sie die restlichen Einstellungen für eine [Baidu-Textanzeige](ad-settings-baidu-text.md), [Google Ads-erweiterte dynamische Suchanzeige](ad-settings-google-dsa.md) (in Google Ads nur als „dynamische Suchanzeige“ bezeichnet), [Google Ads-Responsive-Suchanzeige](ad-settings-google-rsa.md), [Microsoft Advertising-erweiterte dynamische Suchanzeige](ad-settings-microsoft-dsa.md), [Microsoft Advertising-Multimedia-Anzeige](ad-settings-microsoft-multimedia.md), [Microsoft Advertising-Produktanzeige](ad-settings-microsoft-product.md), [Microsoft-Responsive (Zielgruppe)-Anzeige](ad-settings-microsoft-responsive.md), [Advertising-Responsive-Suchanzeige](ad-settings-microsoft-rsa.md) oder [Yandex-](ad-settings-yandex-text.md)--Einstellungen an.

   >[!NOTE]
   >
   >(Kampagnen mit Adobe Advertising-Konversions-Tracking) Wenn die Konto- oder Kampagneneinstellungen das Tracking nur auf Keyword-Ebene angeben, generiert Search, Social und Commerce kein Tracking für Anzeigen.

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

1. Klicken Sie bei Bedarf auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten") **[!UICONTROL Edit]** und ändern Sie die Anzeigeneinstellungen.

1. Klicken Sie auf **[!UICONTROL Create]**.

1. <!-- Add link to where to generate this once available to users-->(Shopping-Anzeigen in Kampagnen mit Adobe Advertising-Konversions-Tracking; optional) Um Klicks auf die Anzeige zu verfolgen, fügen Sie manuell eine Tracking-URL zu den Konto-, Kampagnen- oder Produktgruppeneinstellungen hinzu.

## Umbenennen einer Anzeige {#ad-rename}

Schnelles Umbenennen einer Anzeige ohne Öffnen der vollständigen Anzeigeneinstellungen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Halten Sie den Cursor über der Anzeigenzeile und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Rename]**.

1. Bearbeiten Sie den Namen und klicken Sie dann auf **[!UICONTROL Apply]**.

## Anzeigeneinstellungen bearbeiten {#ad-edit}

>[!NOTE]
>
>* Die folgenden Anzeigentypen sind *veränderlich* was bedeutet, dass Sie die Anzeigenkopie oder das Bild ändern und dieselbe Anzeigen-ID beibehalten können: alle [!DNL Google Ads] Anzeigentypen mit Ausnahme von dynamischen Suchanzeigen und [!DNL Microsoft Advertising] erweiterten Textanzeigen.
>* Alle anderen unterstützten Anzeigen sind *nicht veränderlich* was bedeutet, dass eine Änderung der Anzeigenkopie oder des Bildes die vorhandene Anzeige löscht und eine neue erstellt. Die Leistung der neuen Anzeige kann einige Wochen lang schwanken, während Search, Social und Commerce genügend Daten für die Optimierung erfassen.
>* Der Inhalt einer Produktanzeige kann nicht bearbeitet werden, mit Ausnahme der Promotion-Zeile für [!DNL Microsoft Advertising] Produktanzeigen. Sie können jedoch eine Anzeige anhalten oder löschen.
>* Sie können [!DNL Google Ads] Anzeigen nicht bearbeiten, die nur für Anrufe bestimmt sind. Sie können jedoch eine pausieren oder löschen.
>* Sie können jeweils nur eine Anzeige bearbeiten.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Aktivieren Sie das Kontrollkästchen neben der Anzeige.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie im **[!UICONTROL Ad Details]** Schritt die Einstellungen [Baidu-Textanzeige](ad-settings-baidu-text.md), [Google Ads-erweiterte dynamische Suchanzeige](ad-settings-google-dsa.md) (jetzt in Google Ads nur „dynamische Suchanzeige“ genannt), [Google Ads-Responsive-Suchanzeige](ad-settings-google-rsa.md), [Microsoft Advertising-erweiterte dynamische Suchanzeige](ad-settings-microsoft-dsa.md), [Microsoft Advertising-Multimedia-Anzeige](ad-settings-microsoft-multimedia.md), [Microsoft Advertising-Produktanzeige](ad-settings-microsoft-product.md), [Microsoft-Responsive (Zielgruppe)-Anzeige](ad-settings-microsoft-responsive.md), [Advertising-Responsive-Suchanzeige](ad-settings-microsoft-rsa.md) oder [](ad-settings-yandex-text.md).

1. Klicken Sie auf **[!UICONTROL Review and Save]**.

1. Klicken Sie bei Bedarf auf ![Bearbeiten](/help/search-social-commerce/assets/edit-new.png "Bearbeiten") **[!UICONTROL Edit]** und ändern Sie die Anzeigeneinstellungen.

1. Klicken Sie auf **[!UICONTROL Update]**.

## Ändern des Status einer Anzeige {#ad-status}

Schnelles Ändern des Status einer Anzeige, ohne die vollständigen Anzeigeneinstellungen zu öffnen.

Sie können jede aktive Anzeige in einem unterstützten Werbenetzwerk anhalten, um die Angebotsabgabe darauf zu deaktivieren. Sie können die Gebotsabgabe später fortsetzen, indem Sie den Status wieder in Aktiv ändern.

Sie können auch alle aktiven oder pausierten Anzeigen löschen. Gelöschte Anzeigen werden aus dem Werbenetzwerk gelöscht. Sie sind weiterhin sichtbar, wenn Sie sie in den Datenfilter einbeziehen, können aber nicht geändert werden.

### Anzeigen aktivieren oder pausieren

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Aktivieren Sie das Kontrollkästchen für die Anzeigenzeile.

1. Ändern Sie in der Symbolleiste für Massenaktionen den Status:

   * Um eine pausierte Anzeige zu aktivieren, klicken Sie auf **[!UICONTROL Activate]**.

   * Um eine aktive Anzeige anzuhalten, klicken Sie auf **[!UICONTROL Pause]**.

### Löschen einer Anzeige

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Aktivieren Sie das Kontrollkästchen für die Anzeigenzeile.

1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Delete]**.

1. Klicken Sie in der Bestätigungsmeldung auf **[!UICONTROL Confirm]**.

## Verwalten von Datenansichtsberichten aus der [!UICONTROL Ads] {#ad-reports}

Erstellen Sie einen Bericht, der die Datenzeilen für eine oder mehrere Anzeigen in der [!UICONTROL Ads] enthält, und laden Sie dann den Bericht als Excel-Arbeitsblattdatei für Microsoft (XLXS-Format) herunter. Der Bericht enthält alle sichtbaren Spalten in der Ansicht.

Sie können jeden generierten Bericht löschen.

Siehe auch &quot;[(Ältere Benutzeroberfläche) Daten aus einer Kampagnen-Management-Ansicht herunterladen](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md) und &quot;[(Ältere Benutzeroberfläche) Löschen eines Leistungsdatenberichts oder einer Bulksheet-Datei aus dem [!UICONTROL Downloads] Menü](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)&quot;.

### Erstellen eines Berichts mit den gefilterten Datenzeilen

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Geben Sie die Anzeigen an, deren Daten Sie herunterladen möchten:

   * Um Daten für bestimmte Anzeigen herunterzuladen, aktivieren Sie die Kontrollkästchen neben den Anzeigen.

   * Um Daten für alle Anzeigen herunterzuladen, müssen Sie keine Kontrollkästchen aktivieren. Alle Anzeigen sind standardmäßig enthalten.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ")**[!UICONTROL Reports]**.

1. Geben Sie in den [!UICONTROL Grid Reports] einen eindeutigen Berichtsnamen ein, und klicken Sie dann auf **[!UICONTROL Generate]**.

   Standardmäßig heißt die Datei „ad_YYYMMDD_NNNN“, wobei „NNNN“ die sequenzielle Auftragsnummer ist (z. B. „ad_20250402_1326„).

   Die Datei wird der [!UICONTROL Recently Generated] hinzugefügt.

1. (Optional) Um die Datei nach Abschluss des Vorgangs herunterzuladen, klicken Sie ![Herunterladen](/help/search-social-commerce/assets/download.png "Herunterladen") neben dem Dateinamen.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

### Herunterladen eines abgeschlossenen Berichts

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ")**[!UICONTROL Reports]**.

1. Klicken Sie in der [!UICONTROL Recently Generated] im [!UICONTROL Grid Reports] auf ![Herunterladen](/help/search-social-commerce/assets/download.png "Herunterladen") neben dem Dateinamen.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

### Löschen eines abgeschlossenen Berichts

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ")**[!UICONTROL Reports]**.

1. Klicken Sie in der [!UICONTROL Recently Generated] im [!UICONTROL Grid Reports] auf ![Löschen](/help/search-social-commerce/assets/delete-new.png "Löschen") neben dem Dateinamen.

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] Einstellungen für Textanzeigen](ad-settings-baidu-text.md)
>* [[!DNL Google Ads] Erweiterte Einstellungen für dynamische Suchanzeigen](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] Einstellungen für responsive Suchanzeigen](ad-settings-google-rsa.md)
>* [[!DNL Microsoft Advertising] Erweiterte Einstellungen für dynamische Suchanzeigen](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising] Multimedia-Anzeigeneinstellungen](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] Einstellungen für Produktanzeigen](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising] Einstellungen für responsive Anzeigen (Zielgruppe)](ad-settings-microsoft-responsive.md)
>* [[!DNL Microsoft Advertising] Einstellungen für responsive Suchanzeigen](ad-settings-microsoft-rsa.md)
>* [[!DNL Yandex] Einstellungen für Textanzeigen](ad-settings-yandex-text.md)
