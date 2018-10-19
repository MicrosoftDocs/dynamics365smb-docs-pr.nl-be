---
title: Meerdere rentetarieven instellen
description: "U kunt rentefacturen berekenen met meerdere rentepercentages voor een bepaalde periode. De renteberekening is voor alle financiële kosten soortgelijk, met alleen variatie alleen in het rentepercentage voor een specifieke periode."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 3d4c111af62db5858b81b76f9f51a9093c01e5e6
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-multiple-interest-rates"></a>Meerdere rentetarieven instellen
Meerdere rentepercentages worden gebruikt voor verschillende perioden voor vertraagde betalingen in handelstransacties. Bijvoorbeeld, een overheid specificeert de maximumrente die voor een klant mag worden gerekend. Het rentepercentage kan twee keer per jaar op 1 januari en 1 juli worden gewijzigd. Het rentepercentage tussen bedrijven (B2B) is overeengekomen door de partijen en er is geen limiet aan die klantgroep. Het aangekondigde tarief is gewoonlijk vier procent boven de normale bankrente.

Wanneer u rentefactuurcondities maakt en aanmaningscondities, als sanctie voor vertraagde betaling, kunt u meerdere rentepercentages opgeven zodat de sanctietoeslag wordt berekend op basis van verschillende rentepercentages in verschillende perioden. Zie voor meer informatie [Openstaande saldi innen](receivables-collect-outstanding-balances.md).

## <a name="to-set-up-multiple-interest-rates"></a>Meerdere rentetarieven instellen  
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rentefactuurcondities** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer in het venster **Rentefactuurcondities** de gewenste rentefactuurconditie en kies de actie **Rentepercentages**.  
3.  Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Kies de knop **OK**.  
5.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Aanmaningscondities** in en kies vervolgens de gerelateerde koppeling.  
6.  Selecteer in het venster **Aanmaningscondities** de gewenste aanmaningsconditie en kies de actie **Niveaus**.  
7.  Selecteer in het venster **Aanmaningsniveaus** het veld **Rente berekenen**.  

Wanneer u een rentefactuur verzendt, bevat de factuur de rentefacturen met meerdere rentepercentages in een bepaalde periode. De factuur bevat ook de contactgegevens van de klant, het bedrijf dat de factuur verzendt, het extra bedrag en het totale bedrag. De openingspost op de factuur wordt vet weergegeven. De rentefacturen worden berekend met meerdere rentepercentages voor een bepaalde periode en worden afgedrukt na de openingspost van de factuur.  

## <a name="see-also"></a>Zie ook  
[Openstaande saldi innen](receivables-collect-outstanding-balances.md)  
[Financiën instellen](finance-setup-finance.md)

