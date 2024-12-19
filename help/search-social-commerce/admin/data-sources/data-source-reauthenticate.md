---
title: Erneutes Authentifizieren  [!DNL Google Analytics]  Datenquelle
description: Erfahren Sie, wie Sie eine Datenquelle  [!DNL Google Analytics]  erneut authentifizieren, wenn Sie das zugehörige Kennwort ändern oder das Zertifikat abläuft.
role: User, Admin
exl-id: 624f0f0e-3f2f-45b1-b3dc-c1b107b4736f
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# [!DNL Google Analytics] Datenquelle erneut authentifizieren

*Agenturadministratoren, Agenturkonto-Manager, Adobe-Kontomanager und nur Administratoren*

Wenn Sie das Kennwort für das E-Mail-Konto ändern, das für eine Datenquelle verwendet wird, oder wenn das [!DNL OAuth] für das Konto abläuft, werden alle offenen Verbindungen zum E-Mail-Konto geschlossen und Sie müssen sich erneut authentifizieren, um die Synchronisierung von Daten fortzusetzen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Aktivieren Sie das Kontrollkästchen neben der Datenquelle, die Sie erneut authentifizieren möchten.

1. Klicken Sie in der Symbolleiste über der Datentabelle auf ![Bearbeiten](/help/search-social-commerce/assets/edit.png "Bearbeiten").

1. Bearbeiten Sie die [Datenquelleneinstellungen](data-source-settings.md):

   1. Gehen Sie im Abschnitt [!UICONTROL Connect to Google Analytics] wie folgt vor.

      1. (Falls erforderlich) Geben Sie eine neue E-Mail-Adresse ein, die verwendet werden soll, um auf Daten für diese Datenquelle zuzugreifen. Die E-Mail-Adresse muss bei einem [!DNL Google]-Konto registriert sein und über die Berechtigung zum Lesen und Analysieren für das [!DNL Google Analytics]-Konto verfügen. Siehe [Anweisungen zum Zuweisen von Benutzerberechtigungen in [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Um sicherzustellen, dass in Search, Social und Commerce nur bestimmte [!DNL Google Analytics] und Ansichten verfügbar sind, melden Sie sich mit einer E-Mail-Adresse an, die nur Zugriff auf diese Eigenschaften und Ansichten hat.

   1. Aktivieren Sie das Kontrollkästchen, um Search, Social und Commerce zum Zugriff auf Metriken für das Konto zu autorisieren.

   1. Klicken Sie auf **[!UICONTROL Re-Authenticate]**.

1. Klicken Sie auf **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Über Synchronisierungs [!DNL Google Analytics] Konversionsmetriken](data-source-about.md)
>* [Voraussetzungen für die Konfiguration  [!DNL Google Analytics]  Datenquelle](data-source-prerequisites.md)
>* [Konfigurieren einer  [!DNL Google Analytics] -Ansicht als Datenquelle](data-source-configure.md)
>* [Datenquelle  [!DNL Google Analytics] bearbeiten](data-source-edit.md)
>* [Synchronisierung einer Datenquelle anhalten](data-source-pause.md)
>* [[!DNL Google Analytics] Datenquelleneinstellungen](data-source-settings.md)
>* [Anhang - Verfügbare  [!DNL Google Analytics] Metriken](data-source-ga-metrics.md)
