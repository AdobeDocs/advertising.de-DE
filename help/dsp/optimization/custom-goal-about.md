---
title: Über benutzerdefinierte Ziele
description: Erfahren Sie mehr über benutzerdefinierte Ziele, um Ihre Erfolgsereignisse in Paketen zu definieren, die für den niedrigsten CPA oder den höchsten ROAS optimiert sind.
feature: DSP Optimization
exl-id: 806450b9-ce32-4f5c-a2ac-ba8e435ce36d
source-git-commit: eda0459472c1e4a8297daf69454de0fcb3d4f8ca
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# Über benutzerdefinierte Ziele

Benutzerdefinierte Ziele definieren die Erfolgsereignisse, die ein Advertiser benötigt, um seine Geschäftsziele zu erreichen. Jedes Paket, das Optimierungsziele verwendet, die auf &quot;[!UICONTROL - Custom Goal]&quot; (z. B. &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot;) muss ein benutzerdefiniertes Ziel enthalten, das dazu beiträgt, das Gesamtoptimierungsziel zu erreichen. Sie können benutzerdefinierte Ziele als *Ziele* in [!DNL Advertising Search, Social, & Commerce].

![benutzerdefinierte Ziele](/help/dsp/assets/objective-goals.png)

Jedes benutzerdefinierte Ziel besteht aus einer oder mehreren Konversionsmetriken und den relativen Gewichtungen dieser Metriken. Zu den verfügbaren Konversionsmetriken gehören alle Metriken, die mit dem Adobe Advertising-Konversionspol und über Adobe Analytics verfolgt werden.

>[!NOTE]
>
>* [!DNL Analytics] -Dimensionen und -segmente stehen nicht zur Adobe Advertising-Optimierung zur Verfügung.
>* Um Analytics-Ereignisse in DSP zu verwenden, konfigurieren Sie mit Ihrem Adobe-Account-Team eine Integration auf Advertiser-Ebene.
>* [!DNL Analytics] Benutzerdefinierte Ereignisse folgen dieser Benennungskonvention: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Beispiel: `custom_event_16_examplersid`

Angenommen, drei Konversionsmetriken sind für ein bestimmtes Kampagnenkit relevant: &quot;PDF-Download&quot;im Wert von 20 USD, &quot;E-Mail-Anmeldung&quot;im Wert von 30 USD und &quot;Auftragsbestätigung&quot;im Wert von 40 USD. Wenn Sie Gewichtung gemäß dem einmaligen Geldwert der Kundenaktion geben möchten, beträgt das relative Gewicht der Eigenschaften 1, 2 und 1.5.

Siehe [Best Practices zum Erstellen benutzerdefinierter Ziele](custom-goal-best-practices.md) Tipps zur Konfiguration Ihrer benutzerdefinierten Ziele.

Einmal [Erstellen eines benutzerdefinierten Ziels](custom-goal-create.md), können Sie [Zuweisen zu einem Paket](/help/dsp/campaign-management/packages/package-settings.md) für die Berichterstellung und algorithmische Optimierung mit Adobe Sensei.

>[!MORELIKETHIS]
>
>* [Benutzerdefiniertes Ziel erstellen](custom-goal-create.md)
>* [Best Practices zum Erstellen eines benutzerdefinierten Ziels](custom-goal-best-practices.md)
>* [Optimierungsziele und Verwendung](optimization-goals.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
> * [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)
