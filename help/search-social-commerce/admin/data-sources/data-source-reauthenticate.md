---
title: Erneutes Authentifizieren eines [!DNL Google Analytics] Datenquelle
description: Erfahren Sie, wie Sie eine [!DNL Google Analytics] Datenquelle, wenn Sie das zugehörige Kennwort ändern oder das Zertifikat abläuft.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# Erneutes Authentifizieren eines [!DNL Google Analytics] Datenquelle

*Agentenadministratoren, Agenturkontomanager, Adobe Account Manager und nur Administratoren*

Wenn Sie das Kennwort für das E-Mail-Konto ändern, das für eine Datenquelle verwendet wird, oder wenn die Variable [!DNL OAuth] Zertifikat für das Konto abläuft, werden alle offenen Verbindungen zum E-Mail-Konto geschlossen und Sie müssen sich erneut authentifizieren, um die Synchronisierung der Daten fortzusetzen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Aktivieren Sie das Kontrollkästchen neben der Datenquelle, die Sie erneut authentifizieren möchten.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

1. Bearbeiten Sie die [Datenquelleneinstellungen](data-source-settings.md):

   1. Im [!UICONTROL Connect to Google Analytics] führen Sie die folgenden Schritte aus.

      1. (Bei Bedarf) Geben Sie eine neue E-Mail-Adresse ein, die für den Zugriff auf Daten aus dieser Datenquelle verwendet werden soll. Die E-Mail-Adresse muss bei einem [!DNL Google] und über &quot;Lesen und Analysieren&quot;-Berechtigungen für die [!DNL Google Analytics] -Konto. Siehe [Anweisungen zum Zuweisen von Benutzerberechtigungen in [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >So stellen Sie sicher, dass nur bestimmte [!DNL Google Analytics] -Eigenschaften und -Ansichten in Search, Social und Commerce verfügbar sind, melden Sie sich mit einer E-Mail-Adresse an, die nur Zugriff auf diese Eigenschaften und Ansichten hat.
   1. Aktivieren Sie das Kontrollkästchen, um Search, Social und Commerce zu autorisieren, auf Metriken für das Konto zuzugreifen.

   1. Klicken **[!UICONTROL Re-Authenticate]**.


1. Klicken **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Über die Synchronisierung [!DNL Google Analytics] Konversionsmetriken](data-source-about.md)
>* [Voraussetzungen für die Konfiguration einer [!DNL Google Analytics] Datenquelle](data-source-prerequisites.md)
>* [Konfigurieren Sie eine [!DNL Google Analytics] als Datenquelle anzeigen](data-source-configure.md)
>* [Bearbeiten von [!DNL Google Analytics] Datenquelle](data-source-edit.md)
>* [Synchronisierung einer Datenquelle anhalten](data-source-pause.md)
>* [[!DNL Google Analytics] Datenquelleneinstellungen](data-source-settings.md)
>* [Anhang - Verfügbar [!DNL Google Analytics] Metriken](data-source-ga-metrics.md)

