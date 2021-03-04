---
title: Posten zoeken | Microsoft Docs
description: In dit artikel wordt beschreven hoe u gerelateerde documenten en posten zoekt
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 870cd32dc2408236ed8997e1f939c00d1bf519e4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927803"
---
# <a name="finding-related-entries-for-posted-documents"></a>Gerelateerde posten zoeken voor geboekte documenten 

In dit artikel leert u hoe u documenten en posten kunt vinden die aan elkaar gerelateerd zijn op basis van gemeenschappelijke informatie, zoals:

- Documentnummer of boekingsdatum
- Type zakelijk contact, nummer of extern documentnummer
- Serienummer of lotnummer van artikel

Deze functie is ook handig als u wilt zoeken naar posten uit bepaalde transacties. Wanneer u op documentnummer zoekt, kunt u het overzicht afdrukken vanuit het rapport Documentposten.

## <a name="get-started"></a>Aan de slag

De functie voor het vinden van posten is beschikbaar op de meeste pagina's waarop geboekte documenten of geboekte documentenposten worden weergegeven, voor zowel lijsten als kaarten. Dus de eerste stap is het openen van een van deze pagina's. Kies vervolgens de actie **Posten zoeken** of druk op de toetsen Alt+G.

De pagina **Posten zoeken** bevat alle gerelateerde documenten en posten op basis van het documentnummer en de boekingsdatum. De pagina is onderverdeeld in drie secties:

- De bovenste sectie bevat velden en acties die u gebruikt om uw zoekopdracht te filteren.
- In de middelste sectie worden gerelateerde documenten weergegeven op basis van de zoekopdracht.
- De onderste sectie geeft informatie weer over het brondocument dat is gevonden door te zoeken.


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a>Zoeken naar posten

U kunt posten zoeken op basis van informatie over het document, de zakelijke contactpersoon of de artikelreferentie. Als u de zoekopdracht wilt wijzigen, selecteert u **Acties** , **Zoeken op** en vervolgens een van de volgende acties:

|Actie|Omschrijving|
|------|-----------|
|Zoeken op document|Bekijk posten op basis van een specifiek documentnummer of boekingsdatum.|
|Zakelijke contactpersoon |Bekijk posten op basis van een specifiek contacttype, contactnummer, en/of extern documentnummer. U kunt documentgegevens invoeren die zijn toegewezen door een leverancier of klant. Gebruik de beschikbare velden om te zoeken naar leveranciersdocumenten met de nummers die de leverancier aan de documenten heeft toegewezen.|
|Artikelreferentie|Bekijk posten op basis van een serienummer of lotnummer. U kunt het lotnummer of serienummer invoeren of filteren op het lotnummer of serienummer waarnaar u wilt zoeken. Deze actie is handig om te zien of een bepaald artikeltraceringsnummer is gebruikt, van welke leverancier het afkomstig is of aan welke klant het is verkocht.|

Nadat u een selectie hebt gemaakt, voert u de relevante zoekinformatie in de velden bovenaan in. Gebruik de knopinfo van de velden om te helpen. Kies als u klaar bent **Zoeken** om het zoeken te starten. Als u een filter wijzigt, moet u opnieuw **Zoeken** kiezen.

> [!TIP]
> Voor een paar voorbeelden over het gebruik van **Posten zoeken** raadpleegt u [Artikelen met artikeltracering traceren](inventory-how-to-trace-item-tracked-items.md) en [Procedure: Serie-/lotnummers traceren](walkthrough-tracing-serial-lot-numbers.md).

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Werken met Business Central](ui-work-product.md)  
[Een pagina-actie toevoegen aan uw rolcentrum](ui-bookmarks.md)  
[Artikelen met artikeltracering traceren](inventory-how-to-trace-item-tracked-items.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]