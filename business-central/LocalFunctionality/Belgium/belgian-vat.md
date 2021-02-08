---
title: Belgische btw
description: Met Belgische uitbreidingen van de btw-rapportagefunctie kunt u btw-transactiedetails afdrukken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 264677a4366f9169b8c8c816c6ce2745e78bda60
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4747519"
---
# <a name="belgian-vat"></a>Belgische btw
[!INCLUDE[prod_short](../../includes/prod_short.md)] bevat Belgische uitbreidingen op de btw-rapportagefunctie waarmee u btw-transactiedetails kunt afdrukken. U moet de volgende rapporten aan de Belgische belastingdienst versturen:  

-   Aangifte per maand/kwartaal - Dit rapport wordt gebruikt om maandelijkse of driemaandelijkse btw-aangiftes te maken, afhankelijk van uw bedrijfsinkomsten.  

-   Jaarlijkse btw-lijst (op papier/schijf) - Dit rapport wordt gebruikt om jaarlijks alle gefactureerde bedragen te rapporteren voor goederen en services aan alle Belgische bedrijven met een geregistreerd btw-nummer.  

-   Btw-VIES-lijst (op papier/schijf) - Dit rapport wordt gebruikt om de verkoop te rapporteren van goederen naar andere landen.  

U moet ook een gedrukt afschrift met details van de btw-transacties verstrekken aan de Belgische belastingdienst. Zie Btw-aangifte voor meer informatie.  

## <a name="non-deductible-vat"></a>Niet-aftrekbare btw  
 In België kan btw volledig of gedeeltelijk aftrekbaar zijn. Kosten zoals representatiekosten of aankopen van auto's zijn slechts deels aftrekbaar en de transactie moet opgeven hoeveel van de btw niet-aftrekbaar is. U maakt bijvoorbeeld een grootboekrekening voor vaste activa, bijvoorbeeld auto's, en een andere rekening voor representatiekosten. Voor elke rekening moet u opgeven hoeveel van de gerapporteerde btw niet-aftrekbaar is door het veld **Percentage niet-aftrekbare btw** in te stellen. Wanneer u een transactie boekt wordt de aftrekbare btw dan geboekt naar de corresponderende btw-rekening en wordt de niet-aftrekbare btw opgeteld bij het basisbedrag en geboekt naar dezelfde rekening als een materieel of immaterieel activum.  

 Voor vaste activa wordt de niet-aftrekbare btw afgeschreven zoals de basisaanschafkosten van het vaste activum. U moet aparte VA-boekingsgroepen instellen voor elk percentage niet-aftrekbare btw. U moet dit doen aangezien elke VA-boekingsgroep boekt naar een grootboekrekening, waarbij het veld **Percentage niet-aftrekbare btw** opgeeft hoeveel btw moet worden geboekt naar dezelfde rekening als het vaste activum.  

 Als u het veld **Inclusief niet-aftrekbare btw** inschakelt op een btw-aangifteregel, wordt niet aftrekbare btw opgenomen in het btw-bedrag. Het rapport **Btw-vereffening berekenen en boeken** telt het niet-aftrekbare deel van dat bedrag op bij de velden **Niet-aftrekbaar btw-bedrag** en **Niet-aftrekbaar btw-bedrag (bronvaluta)** in de resulterende btw-posten.  

## <a name="see-also"></a>Zie ook  
 [Belgische lokale functionaliteit](belgium-local-functionality.md)   
 [Periodieke btw-rapporten afdrukken](how-to-print-periodic-vat-reports.md)   
 [Niet-aftrekbare btw instellen](how-to-set-up-non-deductible-vat.md)
