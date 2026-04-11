---
title: Bearbeiten  [!DNL Google Ads]  Konversionswertregel
description: Erfahren Sie, wie Sie  [!DNL Google Ads] -/Konversionswertregeln bearbeiten.
source-git-commit: e15d34f3f32a8565735e53f1ce40e71008dbb4d9
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Bearbeiten einer [!DNL Google Ads] Konversionswertregel

Sie können eine Konversionswertregel in Konten/Kampagnen bearbeiten, für die Konversionen auf individueller Kontoebene oder darunter verfolgt werden. Sie können keine Regel für ein Konto mit kontoübergreifenden Konversionen bearbeiten, die auf Master-Kontoebene verfolgt werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Standardmäßig ist die Registerkarte **[!UICONTROL Campaign]** ausgewählt, um alle Regeln auf Kampagnenebene anzuzeigen.

1. (Optional) Um stattdessen alle Regeln auf Kontoebene anzuzeigen, klicken Sie auf die Registerkarte **[!UICONTROL Account]** .

1. Aktivieren Sie das Kontrollkästchen neben der Regel.

1. In der Symbolleiste für Massenaktionen

   * Um pausierte Regeln zu aktivieren, klicken Sie auf (/help/search-social-commerce/assets/edit-new.png „Bearbeiten).

1. Bearbeiten Sie die [Einstellungen für Konversionsregeln](google-conversion-value-rule-settings.md).

   Die Bedingungstypen für eine vorhandene Regel können nicht bearbeitet werden, die Bedingungen und Wertanpassungen können jedoch bearbeitet werden.

   Sie müssen eine primäre Bedingung und eine Wertanpassung konfigurieren. Sie können optional eine sekundäre Bedingung konfigurieren.

   **Hinweis:** Wenn Sie eine sekundäre Bedingung hinzufügen, muss sie vom gleichen Bedingungstyp sein wie andere Regeln im Konto. Wenn beispielsweise Regel 1 oder andere Regeln im Konto die sekundäre Bedingung „Standort“ aufweisen, muss, wenn die anderen Regeln eine sekundäre Bedingung enthalten, die sekundäre Bedingung „Standort“ sein. Wenn Sie eine sekundäre Bedingung einbeziehen, wird die sekundäre Bedingung mit dem booleschen Operator ALL mit der primären Bedingung verbunden, sodass beide Bedingungen erfüllt sein müssen, um eine Wertanpassung zu initiieren.

1. Klicken Sie auf **[!UICONTROL Review and Save]** , um die Einstellungen zu überprüfen.

1. Klicken Sie auf **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Über [!DNL Google Ads] Konversionswertregeln](about-google-conversion-value-rules.md)
>* [Erstellen  [!DNL Google Ads]  Konversionswertregel](create-google-conversion-value-rule.md)
>* [Ändern des Status  [!DNL Google Ads]  Konversionswertregel](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] Regeleinstellungen für Konversionswerte](google-conversion-value-rule-settings.md)

