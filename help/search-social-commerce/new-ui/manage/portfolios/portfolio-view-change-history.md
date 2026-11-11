---
title: (Neue Benutzeroberfläche) Anzeigen des Änderungsverlaufs und des Änderungsverlaufs eines Portfolios
description: Erfahren Sie, wie Sie in Adobe Advertising Search, Social und Commerce Portfolioänderungen und den Bid-Änderungsverlauf anzeigen, Datumsbereiche ändern, Portfolioänderungen filtern und Verlaufsberichte generieren, herunterladen und löschen können.
feature: Search Portfolios, Search Optimization
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
source-git-commit: e7e0221adbb72127a9e6d2354b6a235b233a4a76
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%
---
# (Neue Benutzeroberfläche) Anzeigen des Änderungsverlaufs und des Änderungsverlaufs eines Portfolios

*Beta-Funktion*

Sie können ein Protokoll der Änderungen anzeigen, die während eines beliebigen Datumsbereichs am Portfolio vorgenommen wurden. Zu den protokollierten Aktionen gehören die Portfolioerstellung, alle Änderungen an den Portfolioeinstellungen, alle Kampagnen, die dem Portfolio zugewiesen sind oder deren Zuweisung aufgehoben wurde, alle Einschränkungen, die auf die Gebotseinheiten im Portfolio angewendet bzw. von ihnen entfernt wurden, alle Einschränkungen für die Gebotseinheiten im Portfolio, die abgelaufen sind, und andere Aktionen, die das Portfolio betreffen.

Das Dialogfeld [!UICONTROL Change History] enthält eine Registerkarte [!UICONTROL Portfolio Change History] für Portfolioänderungen und eine Registerkarte [!UICONTROL Portfolio Bid Change History] für den Angebotsverlauf. Standardmäßig werden auf beiden Registerkarten die letzten 180 Tage angezeigt, die gestern endeten.

Sie können Portfolioänderungen nach Kategorie filtern und den Datumsbereich für jede Registerkarte ändern. Sie können die Daten auch in eine Tabellendatei herunterladen.

## Anzeigen des Änderungsverlaufs eines Portfolios {#portfolio-change-history}

Zu den Informationen für jede Änderung gehören [!UICONTROL Change Date], [!UICONTROL Changed By], [!UICONTROL Change Type] und [!UICONTROL Description]. Die Änderungen werden von neu nach alt aufgelistet.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Halten Sie den Cursor über der Portfoliozeile und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Change History]**.

1. Rufen Sie im Dialogfeld [!UICONTROL Change History] die Registerkarte **[!UICONTROL Portfolio Change History]** auf.

1. (Optional) Ändern Sie die angezeigten Informationen:

   * Klicken Sie ![Kalender](/help/search-social-commerce/assets/calendar-new.png "Kalender"), um den Datumsbereich für den Bericht zu ändern.

   * Klicken Sie ![Filter](/help/search-social-commerce/assets/filter-new.png "Filter"), um die Daten nach Kategorie zu filtern: [!UICONTROL All], [!UICONTROL Objective], [!UICONTROL Campaign], [!UICONTROL Target], [!UICONTROL Constraints], [!UICONTROL Optimization Levers] oder [!UICONTROL Others].

## Anzeigen des Änderungsverlaufs von Angeboten eines Portfolios {#portfolio-bid-change-history}

1. [Öffnen Sie den Änderungsverlauf des Portfolios](#portfolio-change-history).

1. Klicken Sie auf die Registerkarte **[!UICONTROL Portfolio Bid Change History]** .

1. (Optional) Klicken Sie auf ![Kalender](/help/search-social-commerce/assets/calendar-new.png "Kalender"), um den Datumsbereich zu ändern.

1. (Optional) Klicken Sie auf die Spaltenüberschrift Datum , um die Liste nach Datum in auf- oder absteigender Reihenfolge zu sortieren.

Um den Verlauf für eine einzelne Gebotseinheit anzuzeigen, [ Sie die Details der Gebotseinheit in den Leistungsdetails des Portfolios](portfolio-details.md#bid-unit-history). Sie können auch [Angebotseinheitenverlauf über die [!UICONTROL Keywords] öffnen](/help/search-social-commerce/new-ui/manage/keywords/keyword-manage.md#bid-unit-history) wenn die Spalte [!UICONTROL Bid Unit ID] verfügbar ist.

## Verwalten von Berichten für Portfolioänderungsverläufe

Sie können zusätzliche Informationen zum Änderungsverlauf für ein Portfolio in eine Datei [!DNL Microsoft Excel] Arbeitsmappen-Format (XLSX-Datei) herunterladen. Der Bericht enthält die numerische Änderungs-ID, die alten und neuen Werte, den Änderungstyp (z. B. „hinzugefügt“ oder „geändert„), den Aktionstyp (z. B. „Budget“ oder &quot;Portfolio-Name„) und gegebenenfalls den Untertyp, die Zeit und den Benutzernamen.

Über die Registerkarte [!UICONTROL Portfolio Bid Change History] können Sie auch Berichte erstellen, herunterladen und löschen. Die Berichtseinstellungen haben den Titel [!UICONTROL Portfolio History] für Portfolioänderungen und [!UICONTROL Portfolio Bid History] für den Angebotsverlauf.

### Erstellen eines Berichts mit den gefilterten Datenzeilen

1. [Öffnen Sie den Änderungsverlauf des Portfolios](#portfolio-change-history) und klicken Sie dann auf die Registerkarte, deren Daten Sie herunterladen möchten.

1. Klicken Sie oben rechts auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ").

1. Akzeptieren Sie in den [!UICONTROL Portfolio History]- oder [!UICONTROL Portfolio Bid History] den Standardnamen des Berichts, oder geben Sie einen eindeutigen Berichtsnamen ein, und klicken Sie dann auf **[!UICONTROL Generate]**.

   Standardmäßig enthält der Berichtsname den Verlaufstyp sowie das Datum und die Uhrzeit `YYYYMMDD_HHmm` Format, z. B. „portfolioChangeHistory_20260402_1326“. Wenn der Name bereits vorhanden ist, wird ein numerisches Suffix hinzugefügt.

   Die Datei wird der [!UICONTROL Recently Generated] hinzugefügt.

1. (Optional) Um die Datei nach Abschluss des Vorgangs herunterzuladen, klicken Sie ![Herunterladen](/help/search-social-commerce/assets/download.png "Herunterladen") neben dem Dateinamen.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

### Herunterladen eines abgeschlossenen Berichts

1. [Öffnen Sie den Änderungsverlauf des Portfolios und ](#portfolio-change-history) Sie dann auf die Registerkarte, von der aus Sie den Bericht generiert haben.

1. Klicken Sie oben rechts auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ").

1. Klicken Sie in der [!UICONTROL Recently Generated] in den [!UICONTROL Portfolio History]- oder [!UICONTROL Portfolio Bid History] auf ![Download](/help/search-social-commerce/assets/download.png "Download") neben dem Dateinamen.

   Die Datei wird nach dem üblichen Verfahren Ihres Browsers heruntergeladen.

### Löschen eines abgeschlossenen Berichts

1. [Öffnen Sie den Änderungsverlauf des Portfolios und ](#portfolio-change-history) Sie dann auf die Registerkarte, von der aus Sie den Bericht generiert haben.

1. Klicken Sie oben rechts auf ![Bericht herunterladen](/help/search-social-commerce/assets/download.png "Bericht ").

1. Klicken Sie in der [!UICONTROL Recently Generated] in den [!UICONTROL Portfolio History]- oder [!UICONTROL Portfolio Bid History] auf ![Löschen](/help/search-social-commerce/assets/delete-new.png "Löschen") neben dem Dateinamen.

>[!MORELIKETHIS]
>
>* [Erstellen eines Portfolios](portfolio-create.md)
>* [(Neue Benutzeroberfläche) Bearbeiten eines Portfolios](portfolio-edit.md)
>* [(Neue Benutzeroberfläche) Anzeigen von Details zur Portfolioleistung](portfolio-details.md)
>* [(Neue Benutzeroberfläche) Herunterladen von Daten in der [!UICONTROL Portfolios] Ansicht](portfolio-view-report.md)
>* [Über Portfolios](portfolio-about.md)
