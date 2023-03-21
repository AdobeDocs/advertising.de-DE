---
title: Benutzerdefiniertes Ziel erstellen
description: Benutzerdefiniertes Ziel erstellen
feature: DSP Optimization
exl-id: 81b0acfa-085d-495b-9516-576b952b1307
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%

---

# Benutzerdefiniertes Ziel erstellen

Sie können benutzerdefinierte Ziele als *Ziele* Innerhalb [!DNL Advertising Search, Social, & Commerce].

Um ein benutzerdefiniertes Ziel zu erstellen, muss das DSP Konto mit einem [!DNL Search, Social, & Commerce] -Konto mit derselben Adobe Experience Cloud-Organisations-ID aus der [!DNL Search, Social, & Commerce] Clienteinstellungen. Wenn Ihr DSP-Konto nicht mit einem [!DNL Search, Social, & Commerce] Wenden Sie sich an Ihr Adobe Account Team.

>[!TIP]
>
>Siehe [Best Practices zum Erstellen benutzerdefinierter Ziele](custom-goal-best-practices.md) Tipps zur Konfiguration Ihrer benutzerdefinierten Ziele.

1. Anmelden [!DNL Advertising Search, Social, & Commerce] unter (Benutzer in Nordamerika) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) oder (alle anderen Benutzer) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. Stellen Sie sicher, dass die Metriken, die Sie in Ihr Ziel aufnehmen möchten, verfolgt wurden, im Produkt verfügbar sind und einen Anzeigenamen enthalten:
   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** > **[!UICONTROL Admin]>[!UICONTROL Transaction Properties]**.
   1. Suchen Sie die Metrik und stellen Sie sicher, dass **[!UICONTROL Show in UI and Reports]** für die Metrik aktiviert ist.
   1. Wenn die Metrik keinen Wert im **[!UICONTROL Display Name]** klicken Sie in die Zelle, geben Sie den Anzeigenamen ein und klicken Sie auf **[!UICONTROL Apply].**
1. Erstellen Sie das benutzerdefinierte Ziel als *Ziel*:
   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL Objectives]**.
   1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Create objective].**
   1. Geben Sie die Zieleinstellungen ein:
      1. Im **[!UICONTROL Change Objective Name]** Geben Sie den Zielnamen ein.

         Der Zielname wird im [!UICONTROL Custom Goals] in den DSP Paketeinstellungen.

      1. Verknüpfen Sie Eigenschaften mit dem Ziel:

         >[!NOTE]
         >
         > Alle für den Advertiser verfolgten Transaktionseigenschaften werden standardmäßig im [!UICONTROL Available Properties] Liste.

         * Um eine CSV-Datei mit Eigenschaften und deren Gewichtungen zu importieren, klicken Sie auf **[!UICONTROL Import]** und suchen Sie die zu importierende Datei.

            Die importierten Eigenschaften müssen bereits für den Werber vorhanden sein. Bei den Namen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

            Die importierten Eigenschaften ersetzen alle angegebenen vorhandenen Eigenschaften.

         * Um die erste Eigenschaft mit der Standardgewichtung (1) manuell anzugeben, wählen Sie aus einer Liste aller für den Advertiser verfolgten Transaktionseigenschaften aus.

         * Um manuell eine weitere Eigenschaft mit der Standardgewichtung (1) hinzuzufügen, klicken Sie auf **[!UICONTROL +]** .

            >[!TIP]
            >
            > Um in der Liste nach einer Eigenschaft zu suchen, geben Sie eine Zeichenfolge an einer beliebigen Stelle im Eigenschaftsnamen ein.

         * Um mehrere Eigenschaften manuell hinzuzufügen, klicken Sie auf **[!UICONTROL Add Multiple Properties].** Klicken Sie für jede Eigenschaft, die Sie hinzufügen möchten, auf den Eigenschaftsnamen im [!UICONTROL Available Properties] und ziehen Sie sie in die [!UICONTROL Added Properties] Spalte. Wenn Sie alle Eigenschaften hinzugefügt haben, klicken Sie auf **[!UICONTROL Add]**.

            >[!TIP]
            >
            >* Um in der Liste nach einer Eigenschaft zu suchen, geben Sie eine Zeichenfolge von einer beliebigen Stelle im Eigenschaftsnamen im Eingabefeld ein.
            >* Um die Liste zu filtern und Eigenschaften auszuschließen, die in Berichten ausgeschlossen sind, wählen Sie die Option aus **[!UICONTROL Hide properties excluded from reports].**


         * (Wenn das Ziel mehrere Eigenschaften enthält) Um die Gewichtung einer Eigenschaft in Bezug auf die anderen Eigenschaften im Ziel zu ändern, geben Sie Werte in die **[!UICONTROL Weight]** -Feld(e).
      1. Klicken Sie unten in den Einstellungen auf **[!UICONTROL Save]**.


Nachdem Sie ein Ziel erstellt haben, können Sie es einem DSP als benutzerdefiniertes Ziel zuweisen, wenn das Optimierungsziel lautet[!UICONTROL Highest ROAS - Custom Goal]&quot; oder &quot;[!UICONTROL Lowest CPA - Custom Goal].&quot;

>[!TIP]
>
>Für eine optimale Leistung müssen die kombinierten Metriken im benutzerdefinierten Ziel (Ziel) mindestens zehn Konversionen pro Tag umfassen. Andernfalls empfiehlt es sich, dem Ziel zusätzliche unterstützende Ereignisse (Transaktionseigenschaften) wie Produktseiten oder Anwendungen hinzuzufügen. Siehe [Best Practices zum Erstellen eines benutzerdefinierten Ziels](custom-goal-best-practices.md) für Leitlinien.

>[!MORELIKETHIS]
>
>* [Über benutzerdefinierte Ziele](custom-goal-about.md)
>* [Best Practices zum Erstellen eines benutzerdefinierten Ziels](custom-goal-best-practices.md)
>* [Optimierungsziele und Verwendung](optimization-goals.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
> * [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)

