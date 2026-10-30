---
title: Kopieren Sie untergeordnete Knoten auf derselben Ebene in einen anderen Zielknoten.
description: Erfahren Sie, wie Sie alle untergeordneten Knoten eines übergeordneten Zielknotens auf derselben Ebene in einen anderen Zielknoten kopieren
feature: Creative Experiences
exl-id: b3705689-57b6-41ce-9e00-2358bd195c93
TQID: 'https://experienceleague.adobe.com/KLKVrggOQ8V99Cd-2PcFEdwImKvLYkskSD-DPDvpwu0'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%
---
# Kopieren Sie untergeordnete Knoten auf derselben Ebene in einen anderen Zielknoten.

*Nur Erlebnisse mit Targeting mit Entscheidungsbäumen*

Sie können alle untergeordneten Knoten eines übergeordneten Zielknotens (einschließlich aller untergeordneten Ziele und der ihnen zugewiesenen Kreativ-Bundles) auf derselben Ebene in einen anderen Zielknoten kopieren. Sie können die Knoten kopieren, indem Sie entweder a) die kopierten Knoten zum vorhandenen Framework hinzufügen oder b) das vorhandene Framework vollständig ersetzen. <!-- Give the main use case or an example to explain. -->

Diese Funktion wirkt sich nicht auf das für den übergeordneten Knoten angegebene Ziel aus, sondern nur auf die untergeordneten Knoten.

## Verwenden des KI-gesteuerten Editors (Beta) {#ai-editor}

Verwenden Sie beim [&#x200B; (Erstellen](experience-create-targeting.md#ai-editor) oder [Bearbeiten](experience-edit-targeting.md#ai-editor) des Erlebnisses die Canvas-Steuerelemente:

1. Klicken Sie im übergeordneten Knoten, dessen untergeordnete Elemente Sie kopieren möchten, auf **[!UICONTROL ...]** > **[!UICONTROL Copy Children]**.

1. Klicken Sie im Zielknoten auf derselben Ebene auf **[!UICONTROL ...]** und wählen Sie dann eine der folgenden Optionen aus:

   * Um die kopierten untergeordneten Ziele und Kreativen hinzuzufügen, ohne die vorhandenen untergeordneten Elemente zu entfernen, klicken Sie auf **[!UICONTROL Add]**.

   * Um die vorhandenen untergeordneten Ziele und Kreativen durch die kopierten untergeordneten Elemente zu ersetzen, klicken Sie auf **[!UICONTROL Replace]**.

   Eine Aktion wird deaktiviert, wenn sie von der Baumstruktur nicht unterstützt wird. Überprüfen Sie alle Warnungen, bevor Sie fortfahren.

1. Überprüfen Sie die Zielverzweigung und [&#x200B; Sie dann „Erlebnis speichern](#save).

## Verwenden des manuellen Editors {#manual-editor}

[Öffnen Sie den manuellen Editor](experience-edit-targeting.md#experience-open) bevor Sie diese Schritte ausführen.

1. Klicken Sie auf den übergeordneten Knoten, dessen untergeordnete Elemente Sie kopieren möchten, klicken Sie auf ![Hinzufügen](/help/creative/assets/add.png "Hinzufügen"), und wählen Sie dann entweder a\) **[!UICONTROL Copy Children ctrl+c]** aus oder b\) geben Sie **[!UICONTROL Ctrl+C]** ([!DNL Microsoft Windows]) oder **[!UICONTROL Command-C]** ([!DNL Apple Macintosh]) auf Ihrer Tastatur ein.

1. Führen Sie einen der folgenden Schritte aus:

   * Um alle untergeordneten Knoten und Kreativen für einen Knoten zu ersetzen, klicken Sie auf den Knoten, in den Sie die kopierten Informationen einfügen möchten, klicken Sie auf **[!UICONTROL ...]**, und wählen Sie dann entweder a\) **[!UICONTROL Replace ctrl+shift+v]** aus oder b\) geben Sie **[!UICONTROL Ctrl+Shift+V]** ([!DNL Microsoft Windows]) oder **[!UICONTROL Command-Shift-V]** ([!DNL Apple Macintosh]) auf Ihrer Tastatur ein.

   * (Knoten mit mehreren untergeordneten Zielen, ohne „Alle“-Knoten und nur ohne Kreative) Um alle untergeordneten Knoten und Kreativen zu einem Knoten hinzuzufügen, ohne die vorhandenen zu löschen, klicken Sie auf den Knoten, in den Sie die kopierten Informationen einfügen möchten, klicken Sie auf **[!UICONTROL ...]** und wählen Sie entweder a\) **[!UICONTROL Add ctrl+v]** oder b\) **[!UICONTROL Ctrl+V]** ([!DNL Microsoft Windows]) oder **[!UICONTROL Command-V]** ([!DNL Apple Macintosh]) auf der Tastatur aus.

## Erlebnis speichern {#save}

Die folgenden Schritte gelten für beide Editoren.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Fügen Sie einen Zielknoten zur endgültigen Ebene hinzu](experience-target-node-add-final.md)
>* [Fügen Sie zwischen Knoten einen Zielknoten ein](experience-target-node-add-inner.md)
>* [Fügen Sie zwischen Knoten einen gleichrangigen Zielknoten hinzu](experience-target-node-add-sibling.md)
>* [Zuweisen von Kreativen zu einem endgültigen Knoten](experience-assign-creative-bundles.md)
>* [Löschen eines Zielknotens oder eines kreativen Blattknotens](/help/creative/experiences/experience-target-node-delete.md)
>* [Erstellen eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-create-targeting.md)
>* [Bearbeiten eines Erlebnisses mit Entscheidungsbaum-Targeting](experience-edit-targeting.md)
>* [Einstellungen für zielgerichtete Erlebnisse](experience-settings-targeting.md)
