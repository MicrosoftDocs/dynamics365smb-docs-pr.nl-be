---
title: Belgische btw
description: Met Belgische uitbreidingen van de btw-rapportagefunctie kunt u btw-transactiedetails afdrukken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 01/31/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 243c13d8f0dccaf8fb3e26dc0ab97ea6975cd0af
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="belgian-vat"></a>Belgische btw
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] bevat Belgische uitbreidingen op de btw-rapportagefunctie waarmee u btw-transactiedetails kunt afdrukken. U moet de volgende rapporten aan de Belgische belastingdienst versturen:  

-   Aangifte per maand/kwartaal - Dit rapport wordt gebruikt om maandelijkse of driemaandelijkse btw-aangiftes te maken, afhankelijk van uw bedrijfsinkomsten.  

-   Jaarlijkse btw-lijst (op papier/schijf) - Dit rapport wordt gebruikt om jaarlijks alle gefactureerde bedragen te rapporteren voor goederen en services aan alle Belgische bedrijven met een geregistreerd btw-nummer.  

-   Btw-VIES-lijst (op papier/schijf) - Dit rapport wordt gebruikt om de verkoop te rapporteren van goederen naar andere landen.  

U moet ook een gedrukt afschrift met details van de btw-transacties verstrekken aan de Belgische belastingdienst. Zie Btw-aangifte voor meer informatie.  

## <a name="non-deductible-vat"></a>Niet-aftrekbare btw  
 In België kan btw volledig of gedeeltelijk aftrekbaar zijn. Kosten zoals representatiekosten of aankopen van auto's zijn slechts deels aftrekbaar en de transactie moet opgeven hoeveel van de btw niet-aftrekbaar is. U maakt bijvoorbeeld een grootboekrekening voor vaste activa, bijvoorbeeld auto's, en een andere rekening voor representatiekosten. Voor elke rekening moet u opgeven hoeveel van de gerapporteerde btw niet-aftrekbaar is door het veld Percentage niet-aftrekbare btw in te stellen. Wanneer u een transactie boekt wordt de aftrekbare btw dan geboekt naar de corresponderende btw-rekening en wordt de niet-aftrekbare btw opgeteld bij het basisbedrag en geboekt naar dezelfde rekening als het materiële of immateriële activum.  

 Voor vaste activa wordt de niet-aftrekbare btw afgeschreven zoals de basisaanschafkosten van het vaste activum. U moet aparte VA-boekingsgroepen instellen voor elk percentage niet-aftrekbare btw, aangezien elke VA-boekingsgroep boekt naar een grootboekrekening, waarbij het veld Percentage niet-aftrekbare btw opgeeft hoeveel btw moet worden geboekt naar dezelfde rekening als het vaste activum.  

 Als u het veld Inclusief niet-aftrekbare btw inschakelt op een btw-aangifteregel, wordt niet aftrekbare btw opgenomen in het btw-bedrag. Het rapport **Btw-vereffening berekenen en boeken** telt het niet-aftrekbare deel van dat bedrag op bij de velden **Niet-aftrekbaar btw-bedrag** en **Niet-aftrekbaar btw-bedrag (bronvaluta)** in de resulterende btw-posten.  

## <a name="see-also"></a>Zie ook  
 [Belgische lokale functionaliteit](belgium-local-functionality.md)   
 [Periodieke btw-rapporten afdrukken](how-to-print-periodic-vat-reports.md)   
 [Niet-aftrekbare btw instellen](how-to-set-up-non-deductible-vat.md)

