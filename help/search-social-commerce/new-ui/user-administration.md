---
title: (Neue Benutzeroberfläche) Benutzerverwaltung
description: Erfahren Sie, wie Sie den Benutzerzugriff verwalten.
feature: Search Introduction
source-git-commit: c198b5ea2f8ef125b1a5d25616158d57950ce3b0
workflow-type: tm+mt
source-wordcount: '975'
ht-degree: 0%

---

# (Neue Benutzeroberfläche) Benutzerverwaltung für Suche, Social und Commerce

Einige Benutzende können den Zugriff auf die neue Benutzeroberfläche für Suche, Social und Commerce mithilfe von [Adobe Admin Console](https://helpx.adobe.com/de/enterprise/using/admin-console.html) verwalten. Dies ist der zentrale Speicherort für die Verwaltung aller Adobe-Berechtigungen und die Benutzerverwaltung. Benutzer werden entweder als Endbenutzer oder als Administratoren kategorisiert. Ihr Adobe-Konto-Team benachrichtigt Sie, wenn Sie Administrator sind. Wenn Sie Administrator sind, finden Sie in den folgenden Abschnitten Informationen zu Ihren Berechtigungen und Workflows für die Benutzerverwaltung.

## Typen von Admins

Admin Console bietet mehrere Arten von Administratoren. Für Search, Social und Commerce sind die folgenden Administratortypen und -berechtigungen erforderlich. Sie können zusätzliche Typen hinzufügen, wenn Sie Benutzerverwaltungsaufgaben delegieren möchten.

**Systemadministrator** Superuser, der alle Produkte für die Organisation verwaltet, einschließlich aller Client-Instanzen für die Organisation. (Client-Instanzen sind mit alten Advertiser-Konten identisch, mit einer oder mehreren Instanzen pro Organisations-ID). Ein Systemadministrator bzw. eine Systemadministratorin kann alle administrativen Aufgaben in Admin Console für das Unternehmen ausführen und administrative Funktionen für jedes Produkt des Unternehmens an andere Benutzende delegieren.

**Produktadministrator** Verwaltet den Zugriff auf ein bestimmtes [!DNL Adobe] (z. B. Suche, Social Media und Commerce) und die Benutzerberechtigungen für dieses Produkt. Produktadministrierende können Produktprofile für das Produkt erstellen, Benutzende und Benutzergruppen für das Produkt erstellen (aber nicht entfernen), Benutzende und Benutzergruppen zu Produktprofilen hinzufügen oder entfernen und andere Produktadministrierende zum Produkt hinzufügen oder daraus entfernen.

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## Standardproduktprofile

Produktprofile, die Rollen ähnlich sind, geben Benutzern die Berechtigung mit bestimmten Services für ein bestimmtes Produkt.

Die neue Benutzeroberfläche für Search, Social und Commerce verfügt über die folgenden Standardproduktprofile, die verschiedene Untergruppen von Funktionen und Services bereitstellen. Sie können die Produktberechtigungen für die Standardproduktprofile nicht bearbeiten oder die Standardproduktprofile löschen. Produktadministrierende, Produktprofiladministrierende und Systemadministrierende können jedoch bei Bedarf zusätzliche Produktprofile mit verschiedenen Untergruppen verfügbarer Berechtigungen erstellen und verwalten.

* **[!UICONTROL Basic Optimization]:** Dieses Profil bietet die folgenden Funktionen:

   * [!UICONTROL Objectives]: Vollständiger Zugriff

   * [!UICONTROL Simulations]: Vollständiger Zugriff

   * [!UICONTROL Portfolio Groups]: Vollständiger Zugriff

   * [!UICONTROL Portfolios]: Erstellen/Bearbeiten des Zugriffs auf Portfolioeinstellungen für [!UICONTROL Objectives], [!UICONTROL Campaigns] und [!UICONTROL Management]; Nur-Lese-Zugriff auf die verbleibenden Portfolioeinstellungen.

   * [!UICONTROL Campaigns]: Nur-Lese-Zugriff auf Kampagneneinstellungen (Funktionen zum Erstellen, Bearbeiten oder Löschen sind nicht verfügbar); Vollständiger Zugriff auf Einschränkungs- und Portfoliozuweisungen

   * [!UICONTROL Ad Groups]: Nur-Lese-Zugriff auf Anzeigengruppeneinstellungen (es sind keine Funktionen zum Erstellen, Bearbeiten oder Löschen verfügbar); Vollständiger Zugriff auf Einschränkungs- und Portfoliozuweisungen

  Diese Zugriffsebene wird für Benutzende bevorzugt, die noch lernen, Search, Social und Commerce zu verwenden.

* **[!UICONTROL Expert Optimization]:** Dieses Profil bietet die folgenden Funktionen:

   * [!UICONTROL Objectives]: Vollständiger Zugriff

   * [!UICONTROL Simulations]: Vollständiger Zugriff

   * [!UICONTROL Portfolio Groups]: Vollständiger Zugriff

   * [!UICONTROL Portfolios]: Vollständiger Zugriff

   * [!UICONTROL Campaigns]: Nur-Lese-Zugriff auf die Kampagnenliste (es sind noch keine Funktionen zum Erstellen, Bearbeiten oder Löschen von Kampagnen verfügbar); Vollständiger Zugriff auf Begrenzungs- und Portfoliozuweisungen

   * [!UICONTROL Ad Groups]: Nur-Lese-Zugriff auf die Anzeigengruppenliste (es sind noch keine Funktionen zum Erstellen, Bearbeiten oder Löschen von Kampagnen verfügbar); Vollständiger Zugriff auf Einschränkungs- und Portfoliozuweisungen

  Diese Zugriffsebene wird für erfahrene Benutzer von Search, Social und Commerce empfohlen.

* **[!UICONTROL Read-Only]:** Dieses Profil bietet die folgenden Funktionen:

   * [!UICONTROL Objectives]: Nur-Lese-Zugriff

   * [!UICONTROL Simulations]: Nur-Lese-Zugriff

   * [!UICONTROL Portfolio Groups]: Nur-Lese-Zugriff

   * [!UICONTROL Portfolios]: Nur-Lese-Zugriff

   * [!UICONTROL Campaigns]: Nur-Lese-Zugriff

   * [!UICONTROL Ad Groups]: Nur-Lese-Zugriff

* **[!UICONTROL Admin]:** Dieses Profil gewährt vollen Zugriff auf alle verfügbaren Funktionen und ermöglicht Benutzern das Erstellen neuer Client-Instanzen (wie veraltete Advertiser-Konten mit einer oder mehreren Instanzen pro Organisations-ID). Weisen Sie dieses Recht niemandem zu, es sei denn, Sie haben eine ordnungsgemäße geschäftliche Begründung.

## Aufgaben für Administratoren

### Melden Sie sich bei Adobe Admin Console an und öffnen Sie es für Search, Social und Commerce

>[!PREREQUISITES]
>
>Sie müssen über Administratorzugriff auf Search, Social und Commerce verfügen, um sich bei Admin Console anzumelden.

1. Navigieren Sie zu https://adminconsole.adobe.com/enterprise/.

1. (Wenn Sie nicht bei Experience Cloud angemeldet sind) Melden Sie sich bei Experience Cloud an:

   1. Geben Sie Ihre [!DNL Adobe]-ID ein und klicken Sie auf **[!UICONTROL Continue]**.

   1. Wählen Sie entweder **[!UICONTROL Personal Account]&quot; oder &#x200B;** [!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. Wählen Sie die entsprechende Experience Cloud-Organisation aus.

      Admin Console öffnet die Registerkarte [!UICONTROL Overview] .

   1. Klicken Sie unter [!UICONTROL Product & services] auf &quot;[!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name]&quot;.

      Die Produktseite öffnet sich auf der Registerkarte [!UICONTROL Product profiles] für Suche, Social und Commerce. Zu den zusätzlichen Registerkarten gehören [!UICONTROL Users] und [!UICONTROL Product Admins].

### Workflow für Systemadministratoren

Folgen Sie diesem Workflow für jede Client-Instanz von Search, Social und Commerce.

1. [Melden Sie sich bei Adobe Admin Console an und öffnen Sie es für Search, Social und Commerce](#open-admin-console).

1. (Optional) [Einen weiteren Systemadministrator hinzufügen](https://helpx.adobe.com/de/enterprise/using/admin-roles.html#enterprise) als Sicherung.

1. Delegieren der Produkt- und Benutzerverwaltung durch [Hinzufügen von ](https://helpx.adobe.com/de/enterprise/using/admin-roles.html#enterprise)&quot;

### Workflow für Produktadministratoren

Folgen Sie diesem Workflow für jede Client-Instanz von Search, Social und Commerce.

1. [Melden Sie sich bei Adobe Admin Console an und öffnen Sie es für Search, Social und Commerce](#open-admin-console).

1. Erstellen Sie bei Bedarf Endbenutzer [einzeln](https://helpx.adobe.com/de/enterprise/using/manage-users-individually.html) oder [zusammen](https://helpx.adobe.com/de/enterprise/using/bulk-upload-users.html).

1. (Optional) Erstellen Sie [Benutzergruppen](https://helpx.adobe.com/de/enterprise/using/user-groups.html) für die Instanz und weisen Sie jeder Benutzergruppe Benutzer zu.

   Wenn die Instanz viele Benutzer hat, erstellen Sie Benutzergruppen, um sicherzustellen, dass Benutzern auf Grundlage ihres Fachwissens die richtigen Profile zugewiesen werden. (Siehe Schritt 4 für das Zuweisen von Benutzergruppen zu Produktprofilen.) Sie können Benutzergruppen basierend auf dem Geschäftsbereich, den Anforderungen an den Benutzerzugriff, dem Einstellungsdatum der Benutzer oder anderen Kriterien erstellen.

   >[!IMPORTANT]
   >
   >Die Namen von Benutzergruppen sollten die Rechte, die der Benutzergruppe zugewiesen werden sollen, klar angeben. Wenn Sie beispielsweise eine Benutzergruppe mit „Schreibgeschützt“-Rechten erstellen möchten, schließen Sie „Schreibgeschützt“ in den Namen der Benutzergruppe ein, z. B. „Acme_Uk_ReadOnly“ oder „Acme_ReadOnly“.

1. (Optional) [Erstellen benutzerdefinierter Produktprofile](https://helpx.adobe.com/de/enterprise/using/manage-product-profiles.html) mit definierten Berechtigungssätzen.

   Benutzerdefinierte Profile werden zusätzlich zu den vier bereits verfügbaren Standardproduktprofilen hinzugefügt.

   Jedes Produktprofil für eine Organisation muss über einen eindeutigen Namen verfügen. Wenn Ihr Unternehmen mehrere Search-, Social- und Commerce-Instanzen verwendet (z. B. Acme_US und Acme_JP), können Sie einen Produktprofilnamen nicht in mehreren Instanzen duplizieren. **Best Practice:** Verwenden Sie die `<Name>_<Instance>,` der Benennungskonvention wie „Simulations_Only_JP“.

   **Achtung:** Produktberechtigungen sind sehr detailliert. Seien Sie vorsichtig, wenn Sie benutzerdefinierte Produktprofile konfigurieren oder Funktionen weglassen, die Sie einbeziehen möchten.

1. [Weisen Sie jeden Benutzer oder jede Benutzergruppe dem entsprechenden Produktprofil ](https://helpx.adobe.com/de/enterprise/using/manage-product-profiles.html) manuell oder stapelweise zu.

## Vollständiges Benutzerhandbuch für die Administration und zusätzliche Links

* Weitere Informationen zur Benutzerverwaltung mit Adobe Admin Console finden Sie unter &quot;[Adobe Enterprise &amp; Teams Administration Guide](https://helpx.adobe.com/de/enterprise/admin-guide.html)&quot;, einschließlich der [Admin Console-Übersicht](https://helpx.adobe.com/de/enterprise/using/admin-console.html).

* Admin Console: [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
