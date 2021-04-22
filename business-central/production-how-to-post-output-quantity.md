---
title: Productie-output en bewerkingstijd in batches boeken
description: De outputhoeveelheid geeft de voortgang van het werk weer in de vorm van de voltooide hoeveelheid en de gebruikte capaciteit van de afdeling of de bewerkingsplaats.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 923f68b13619013dd54062438c66192a682868bc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787889"
---
# <a name="batch-post-output-and-run-times"></a>Output en bewerkingstijden in batches boeken
De outputhoeveelheid geeft de voortgang van het werk weer in de vorm van de voltooide hoeveelheid en de gebruikte capaciteit van de afdeling of de bewerkingsplaats.

U kunt ook het outputdagboek gebruiken om:
*  Voorraad aan te passen in verband met de output van voltooide artikelen vanuit productie.
*  Hoeveelheden en uitval te registreren voor elke bewerking in productierouting.
*  Instel- en looptijd te registreren voor afdelingen en bewerkingsplaatsen.

> [!NOTE]
> Als productierouting wordt gebruikt, wordt de voorraad alleen bijgewerkt wanneer u het outputaantal bij de laatste bewerking boekt.

Met het venster **Productiedagboek** kunt u dezelfde taken uitvoeren als in het venster **Outputdagboek** en tegelijkertijd de gerelateerde taken voor verbruiksboeking uitvoeren. Zie voor meer informatie [Verbruik en output registreren voor één vrijgegeven productieorderregel](production-how-to-register-consumption-and-output.md).

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a>Outputaantallen boeken en/of looptijden registreren voor een of meer productieorderregels
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Outputdagboek** in en kies de desbetreffende koppeling.  
2. Voer in de velden informatie over de productieorder en output en/of looptijd in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    U kunt de functie **Bewerkingsplan weergeven** om dagboekregels te genereren op basis van productieorders.
  
4. Als de bewerking is voltooid, selecteert u het veld **Voltooid**.  
5. Kies de actie **Boeken** om de activiteiten te boeken. 
 
Capaciteitsboekingen worden bijgewerkt voor de gebruikte werk- of machinecentra met informatie over tijd en hoeveelheid output en uitval. Als u de laatste bewerking heeft geboekt, wordt het artikel aan de inventaris toegevoegd. 

## <a name="see-also"></a>Zie ook  
[Handmatig uitval boeken](production-how-to-post-scrap.md)
[Omgekeerde outputboeking](production-how-to-reverse-output-posting.md)
[Productie](production-manage-manufacturing.md)    
[Productie instellen](production-configure-production-processes.md)  
[Gepland](production-planning.md)      
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
