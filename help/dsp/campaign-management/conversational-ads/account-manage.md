---
title: '[!DNL ChatGPT Ads] von Werbekonten für Konversationen verwalten'
description: Erfahren Sie, wie Sie Konten für [!DNL ChatGPT Ads]-Chat-Card-Anzeigen erstellen und verwalten. Dies ist eine Beta-Funktion, mit der Anzeigen in Konversationen mit KI-Assistenten platziert werden.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: cb25ab04e8fef5d00935e5325a897b1de97e2674
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%
---
# [!DNL ChatGPT Ads] von Werbekonten für Konversationen verwalten

*Beta-Funktion*

Durch die Integration von Adobe DSP mit [!DNL OpenAI Ads] können Sie [!DNL ChatGPT Ads] Chat-Kartenanzeigen ausführen, die in [!DNL ChatGPT] Konversationen angezeigt werden. Für diese Funktion erstellt DSP ein Werbekonto für Gespräche und kauft Medien im Namen Ihres Unternehmens. Der Zugriff auf das Werbekonto über ads.openai.com ist nicht möglich. Verwenden Sie diese Funktion, um KI-Medien zu testen, ohne eine direkte Beziehung zu [!DNL ChatGPT Ads] herzustellen.

Sie verwalten Ihre [!DNL ChatGPT Ads] Werbekonten für Konversationen - einschließlich der Kampagnen, Anzeigengruppen und Anzeigen - getrennt von Ihren regulären DSP-Kampagnen, die anders strukturiert sind. Außerdem werden [Leistungsdaten für -Kampagnen [!DNL ChatGPT Ads]  Anzeigengruppen und Anzeigen](campaign-manage.md#campaign-views-about) getrennt von Ihren DSP-Kampagnen angezeigt.

## Eignung

Die folgende Eigenschaft bestimmt die Eignung für diese Funktion:

* **Bestehende [!DNL Search, Social, & Commerce]-Kunden:** Wenn Ihr Advertiser bereits [!DNL Search, Social, & Commerce] verwendet, [erstellen und verwalten Sie seine [!DNL ChatGPT Ads] Kampagnen in Search, Social und Commerce](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md) anstatt in DSP.

* **Eingeschränkte Branchen:** Werbetreibende in eingeschränkten Kategorien (z. B. Finanzen oder Gesundheitswesen) können keine dialogorientierten Werbekonten oder Kampagnen erstellen.

Wenn der ausgewählte Advertiser nicht geeignet ist, geben die Registerkarten [!UICONTROL Accounts] und [!UICONTROL Campaigns] den Grund an. Sie können mit dem Advertiser-Selektor immer noch zu einem anderen Advertiser wechseln.

Um die Funktion zu verwenden, wenden Sie sich an Ihr Adobe Account Team , um den Onboarding-Prozess zu starten.

## Fakturierung

Die [!DNL ChatGPT Ads] wird Ihnen am Ende des Monats zusammen mit Ihren anderen Rechnungen in Rechnung gestellt. Dabei werden die Rechnungswährung und die Zeitzone für die Rechnungsstellung für Ihr DSP-Konto verwendet (unabhängig von der [Währung und Zeitzone für das  [!DNL ChatGPT Ads] -Konto](#account-settings)). Bei Fragen zur Rechnungsstellung wenden Sie sich an Ihr Adobe Account Team.

## Die Ansicht [!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts] {#accounts-view}

Auf der Registerkarte [!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts] werden die [!DNL OpenAI] Konten für den ausgewählten Advertiser aufgelistet. Zu den Informationen für jedes Konto gehören:

**[!UICONTROL Status]:** Ob das Konto derzeit Anzeigen ausführt: *Aktiv* oder *Paused*. Sie können den Status eines Kontos nicht ändern. Wenden Sie sich an Ihr Adobe-Accountteam, wenn Sie ein Konto anhalten oder reaktivieren möchten.

**[!UICONTROL Review status]:** Der [!DNL OpenAI] Überprüfungsstatus: *Wird*, *Genehmigt* oder *Nicht genehmigt*. Halten Sie den Cursor aus folgendem Grund über den Status, falls einer verfügbar ist.

**[!UICONTROL Active campaigns]:** Die Anzahl der derzeit aktiven Kampagnen im Konto.

**[!UICONTROL Cost]:** Die Gesamtausgaben des Kontos.

### Verfügbare Aktionen

* [Kontobeschränkungen anzeigen](#account-limits)

<!-- * [Refresh information about your accounts](#refresh) -- Add topic below. -->

* [Konto erstellen](#account-create)

* [Konto bearbeiten](#account-edit)

* [Kontoliste aktualisieren](#account-refresh)

* [Zurück zum DSP-Hauptmenü](#return-to-menu)

## Konten verwalten

### Kontobeschränkungen anzeigen {#account-limits}

Mit einem Konto-Limit werden die Gesamtausgaben eines Kontos über einen bestimmten Datumsbereich begrenzt. Sie können die Limits eines Kontos anzeigen, aber nur Ihr Adobe-Account-Team kann die Limits erstellen, bearbeiten oder entfernen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Conversational Ads Beta]**.

1. Halten Sie in der **[!UICONTROL Accounts]** den Cursor über die Zeile Konto und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL View account limit]**.

Auf der Seite [!UICONTROL Account limits] werden alle Beschränkungen für das Konto aufgelistet:

**[!UICONTROL Name]:** Der Name des Limits.

**[!UICONTROL Amount]:** Die Gesamtausgabenobergrenze für den Limitzeitraum.

**[!UICONTROL Period]:** Der Datumsbereich, für den die Beschränkung gilt.

**[!UICONTROL Status]:** *aktiv*, *bevorsteht* oder *abgeschlossen*.

**[!UICONTROL Spent]:** Der Betrag, der innerhalb des Limits bisher ausgegeben wurde.

>[!NOTE]
>
>Sie können abgeschlossene Limits nicht bearbeiten oder entfernen und Limitperioden für dasselbe Konto können sich nicht überschneiden.

### Erstellen eines [!DNL ChatGPT Ads] Werbekontos für Konversationen {#account-create}

Um mehr als zwei [!DNL ChatGPT Ads]-Konten für einen Advertiser zu erstellen, wenden Sie sich an Ihr Adobe-Account-Team.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Conversational Ads Beta]**.

1. Führen Sie einen der folgenden Schritte aus:

   * (Nur Ihr erstes Konto) Klicken Sie auf dem Willkommensbildschirm auf **[!UICONTROL Create an Account]**.

   * Wählen Sie in der **[!UICONTROL Accounts]** einen Advertiser aus und klicken Sie dann auf **[!UICONTROL Create Account]**.

1. Geben Sie die [Kontoeinstellungen](#account-settings) an.

1. Aktivieren Sie das Kontrollkästchen **[!UICONTROL I agree to the Terms and Conditions]** .

1. Klicken Sie auf **[!UICONTROL Create account]**.

Neue Konten werden in angehaltenem Zustand erstellt, während [!DNL OpenAI] sie überprüft. DSP aktiviert das Konto, sobald es genehmigt wurde.

### Bearbeiten eines [!DNL ChatGPT Ads] Werbekontos {#account-edit}

Sie können den legalen Unternehmensnamen und die Website eines Kontos bearbeiten, nachdem Sie sie erstellt haben.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Conversational Ads Beta]**.

1. Halten Sie in der **[!UICONTROL Accounts]** den Cursor über die Zeile Konto und klicken Sie auf **[!UICONTROL ...]>[!UICONTROL Edit account]**.

1. Bearbeiten Sie die **[!UICONTROL Legal Business Name]** und/oder **[!UICONTROL Advertiser Website]**. Weitere Informationen zu den Feldern finden Sie unter [Kontoeinstellungen](#account-settings).

1. Klicken Sie auf **[!UICONTROL Save changes]**.

>[!IMPORTANT]
>
>Durch Speichern der Änderungen wird [!DNL OpenAI] Überprüfung des Kontos neu gestartet. Das Konto wird erst dann erneut Anzeigen schalten, wenn das Konto erneut genehmigt wurde.

### Kontoliste aktualisieren {#account-refresh}

Erneutes Anzeigen der Liste der Konten, wenn andere Benutzer möglicherweise Änderungen oder Ergänzungen vorgenommen haben.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Conversational Ads Beta]**.

1. Klicken Sie in der **[!UICONTROL Accounts]** auf **[!UICONTROL Refresh]** über der Kontoliste.

### Zurück zum DSP-Hauptmenü {#return-to-menu}

* Klicken Sie über dem Hauptmenü auf **[!UICONTROL Back to DSP]**.

### [!DNL ChatGPT Ads] Konversationsanzeige-Kontoeinstellungen {#account-settings}

**[!UICONTROL Legal Business Name]:** Der registrierte Unternehmensname der Organisation.

**[!UICONTROL Advertiser Website]:** Die URL der Website des Werbetreibenden, beginnend mit `http://` oder `https://`.

**[!UICONTROL Country]:** Das Land, in dem die Organisation gesetzlich registriert ist (nicht das Land, in dem Sie Anzeigen schalten). Es muss dasselbe Land sein, das auch für den DSP-Vertrag der Organisation verwendet wird. Sie können diesen Wert nach dem Speichern des Kontos nicht mehr ändern.

**[!UICONTROL Currency]:** (Schreibgeschützt) Die Währung, die Ihr Adobe-Konto-Team für das [!DNL ChatGPT Ads] Konto einrichtet. Dies kann sich von der Währung für Ihr DSP-Konto unterscheiden, die an anderer Stelle in DSP angezeigt wird. **Hinweis:** Unabhängig von diesem Wert werden alle Nutzungsrechnungen in der *Abrechnungswährung)* DSP-Konto erstellt.

**[!UICONTROL Timezone]:** (Schreibgeschützt) Die Zeitzone, die Ihr Adobe-Konto-Team für das [!DNL ChatGPT Ads] Konto eingerichtet hat. Dies kann sich von der Zeitzone für Ihr DSP-Konto unterscheiden, die an anderer Stelle in DSP sichtbar ist. **Hinweis:** Unabhängig von diesem Wert stellen alle Nutzungsrechnungen die *Zeitzone für die Abrechnung* dar, die für das DSP-Konto verwendet wird.

**[!UICONTROL Favicon]:** Eine Bilddatei, die als Website-Favicon für das Konto verwendet werden soll.<!-- How is this used within this context? --> Der Browser zeigt das Favicon an verschiedenen Stellen an, z. B. in der Adressleiste, auf der Registerkarte oder in Lesezeichen. Die Datei muss im JPG-, PNG- oder WEBP-Format und mindestens 256 x 256 Pixel groß sein.

Um ein Symbol hochzuladen, klicken Sie auf **[!UICONTROL Upload favicon]**, suchen Sie nach einer Datei auf Ihrem Gerät oder Netzwerk und wählen Sie diese aus.

**[!UICONTROL I agree to the Terms and Conditions]:** Ein Kontrollkästchen, das angibt, dass Sie allen rechtlichen Bedingungen zustimmen. Aktivieren Sie das Kontrollkästchen, um ein Konto zu erstellen oder die Kontoeinstellungen zu aktualisieren.

>[!MORELIKETHIS]
>
>* [Verwalten von konversativen Anzeigenkampagnen](campaign-manage.md)
