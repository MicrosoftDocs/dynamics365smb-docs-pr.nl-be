---
title: De weergave van een rapport wijzigen door een andere lay-out te kiezen | Microsoft Docs
description: U kunt verschillende lay-outs voor een lijst gebruiken en schakelen tussen lay-outs om te bepalen hoe een rapport eruitziet.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 98a2e773dbde6ba4ba0493e2b0dc7b632bbea4d0
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="change-which-layout-is-currently-used-on-a-report"></a>Wijzigen welke lay-out momenteel in een rapport wordt gebruikt
Een rapport kan worden ingesteld met meerdere rapportlay-outs, waartussen u indien nodig kunt schakelen.

Afhankelijk van de lay-outs die voor een rapport beschikbaar zijn, kunt u ervoor kiezen een ingebouwde RDLC-rapportlay-out, een ingebouwde Word-rapportlay-out of een aangepaste lay-out te maken. Zie [Rapportlay-outs beheren](ui-manage-report-layouts.md) voor meer informatie over RDLC- en Word-rapportlay-outs, ingebouwde en aangepaste lay-outs.

## <a name="to-change-the-layout-that-is-used-on-a-report"></a>De lay-out wijzigen die in een rapport wordt gebruikt
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Selectie rapportlay-out** in en kies vervolgens de gerelateerde koppeling.  
   Het venster **Selectie rapportlay-out** bevat een overzicht van alle rapporten die beschikbaar zijn voor het bedrijf dat in het veld Bedrijf boven aan het venster wordt opgegeven. Met het veld Geselecteerde lay-out wordt de lay-out opgegeven die momenteel in het rapport wordt gebruikt.
2. Stel het veld **Bedrijf** boven in het venster in op het bedrijf dat het rapport bevat.
3. Als u de lay-out wilt wijzigen die door een rapport wordt gebruikt, stelt u in de rij voor het rapport in de lijst het veld **Geselecteerde lay-out** in op een van de volgende opties:
   * RDLC (ingebouwd), gebruikt de ingebouwde RDLC-rapportlay-out in het rapport.
   * Word (ingebouwd), gebruikt de ingebouwde Word-rapportlay-out in het rapport.
   * Aangepast, gebruikt een aangepaste lay-out in het rapport.  
     U kunt zien welke aangepaste lay-outs voor het rapport beschikbaar zijn in het feitenblok Rapportlay-outonderdeel. Als er geen aangepaste lay-outs voor het rapport zijn, moet u er eerst een maken. Als u deze optie kiest, gaat u naar de volgende procedure om de aangepaste lay-out op te geven die u wilt gebruiken.

    > [!NOTE]  
    >   Als u **RDLC (ingebouwd)** of **Word (ingebouwd)** kiest en een foutbericht krijgt dat het rapport geen lay-out van de opgegeven soort heeft, moet u een andere lay-outoptie kiezen of een aangepaste rapportlay-out maken van het soort dat u wilt gebruiken.

Als u een ingebouwde RDLC- of Word-rapportlay-out hebt geselecteerd, is er verder geen actie vereist en wordt de lay-out gebruikt als het rapport de volgende keer wordt uitgevoerd.

## <a name="to-specify-a-custom-layout-on-a-report"></a>Een aangepaste lay-out opgeven voor een rapport
1. U geeft vanuit het venster **Aangepaste rapportlay-outs** op welke aangepaste lay-out moet worden gebruikt in het rapport. Als het venster **Aangepaste rapportlay-outs** niet open is, kiest u in het veld **Beschrijving rapportlay-out** de opzoekknop.
2. Selecteer in het venster **Aangepaste rapportlay-outs** de rij voor de aangepaste lay-out die u wilt gebruiken, en sluit vervolgens het venster.

U keert naar het venster **Selectie rapportlay-out** terug. De naam van de geselecteerde aangepaste lay-out wordt weergegeven in het veld **Beschrijving aangepaste lay-out**. De aangepaste lay-out wordt de volgende keer dat u het rapport uitvoert, gebruikt.

## <a name="see-also"></a>Zie ook
[Rapportlay-outs beheren](ui-manage-report-layouts.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

