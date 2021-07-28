---
title: Meerdere rentetarieven instellen
description: Dit onderwerp vertelt u hoe u rentefacturen berekent met meerdere rentepercentages voor een bepaalde periode.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 1a4a47ef587a4d49c92e63f746a3b973f3f40ad9
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435971"
---
# <a name="set-up-multiple-interest-rates"></a>Meerdere rentetarieven instellen
Meerdere rentepercentages worden gebruikt voor verschillende perioden voor vertraagde betalingen in handelstransacties. Bijvoorbeeld, een overheid specificeert de maximumrente die voor een klant mag worden gerekend. Het rentepercentage kan twee keer per jaar op 1 januari en 1 juli worden gewijzigd. Het rentepercentage tussen bedrijven (B2B) is overeengekomen door de partijen en er is geen limiet aan die klantgroep. Het aangekondigde tarief is gewoonlijk vier procent boven de normale bankrente.

Wanneer u rentefactuurcondities maakt en aanmaningscondities, als sanctie voor vertraagde betaling, kunt u meerdere rentepercentages opgeven zodat de sanctietoeslag wordt berekend op basis van verschillende rentepercentages in verschillende perioden. Zie voor meer informatie [Openstaande saldi innen](receivables-collect-outstanding-balances.md).

## <a name="to-set-up-multiple-interest-rates"></a>Meerdere rentetarieven instellen  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Rentefactuurcondities** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer op de pagina **Rentefactuurcondities** de gewenste rentefactuurconditie en kies de actie **Rentepercentages**.  
3.  Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Kies de knop **Ok**.  
5.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Aanmaningscondities** in en kies vervolgens de gerelateerde koppeling.  
6.  Selecteer op de pagina **Aanmaningscondities** de gewenste aanmaningsconditie en kies de actie **Niveaus**.  
7.  Selecteer op de pagina **Aanmaningsniveaus** het veld **Rente berekenen**.  

Wanneer u een rentefactuur verzendt, bevat de factuur de rentefacturen met meerdere rentepercentages in een bepaalde periode. De factuur bevat ook de contactgegevens van de klant, het bedrijf dat de factuur verzendt, het extra bedrag en het totale bedrag. De openingspost op de factuur wordt vet weergegeven. De rentefacturen worden berekend met meerdere rentepercentages voor een bepaalde periode en worden afgedrukt na de openingspost van de factuur.  

## <a name="see-also"></a>Zie ook  
[Openstaande saldi innen](receivables-collect-outstanding-balances.md)  
[Financiën instellen](finance-setup-finance.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]