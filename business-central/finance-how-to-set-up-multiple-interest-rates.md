---
title: Meerdere rentetarieven instellen
description: U kunt rentefacturen berekenen met meerdere rentepercentages voor een bepaalde periode. De renteberekening is voor alle financiële kosten soortgelijk, met alleen variatie alleen in het rentepercentage voor een specifieke periode.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: fd52a1cb3f139f5c21b4c1f0d6ce86f7aac7167c
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882650"
---
# <a name="set-up-multiple-interest-rates"></a>Meerdere rentetarieven instellen
Meerdere rentepercentages worden gebruikt voor verschillende perioden voor vertraagde betalingen in handelstransacties. Bijvoorbeeld, een overheid specificeert de maximumrente die voor een klant mag worden gerekend. Het rentepercentage kan twee keer per jaar op 1 januari en 1 juli worden gewijzigd. Het rentepercentage tussen bedrijven (B2B) is overeengekomen door de partijen en er is geen limiet aan die klantgroep. Het aangekondigde tarief is gewoonlijk vier procent boven de normale bankrente.

Wanneer u rentefactuurcondities maakt en aanmaningscondities, als sanctie voor vertraagde betaling, kunt u meerdere rentepercentages opgeven zodat de sanctietoeslag wordt berekend op basis van verschillende rentepercentages in verschillende perioden. Zie voor meer informatie [Openstaande saldi innen](receivables-collect-outstanding-balances.md).

## <a name="to-set-up-multiple-interest-rates"></a>Meerdere rentetarieven instellen  
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rentefactuurcondities** in en kies de gerelateerde koppeling.  
2.  Selecteer op de pagina **Rentefactuurcondities** de gewenste rentefactuurconditie en kies de actie **Rentepercentages**.  
3.  Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Kies de knop **OK**.  
5.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Aanmaningscondities** in en kies de gerelateerde koppeling.  
6.  Selecteer op de pagina **Aanmaningscondities** de gewenste aanmaningsconditie en kies de actie **Niveaus**.  
7.  Selecteer op de pagina **Aanmaningsniveaus** het veld **Rente berekenen**.  

Wanneer u een rentefactuur verzendt, bevat de factuur de rentefacturen met meerdere rentepercentages in een bepaalde periode. De factuur bevat ook de contactgegevens van de klant, het bedrijf dat de factuur verzendt, het extra bedrag en het totale bedrag. De openingspost op de factuur wordt vet weergegeven. De rentefacturen worden berekend met meerdere rentepercentages voor een bepaalde periode en worden afgedrukt na de openingspost van de factuur.  

## <a name="see-also"></a>Zie ook  
[Openstaande saldi innen](receivables-collect-outstanding-balances.md)  
[Financiën instellen](finance-setup-finance.md)
