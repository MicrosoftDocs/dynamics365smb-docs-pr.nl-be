---
title: 'Ontwerpdetails: Voorraadperioden | Microsoft Docs'
description: Geantidateerde boekingen of kostprijscorrecties zijn vaak van invloed op saldi en voorraadwaarderingen voor boekhoudperioden die kunnen worden beschouwd als gesloten. Dit kan nadelige gevolgen hebben bij nauwkeurig rapporteren, vooral binnen mondiale bedrijven. U kunt de functie Voorraadperioden gebruiken om dergelijke problemen te voorkomen door voorraadperioden te openen of te sluiten om boekingen in een opgegeven periode te beperken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: feaa4362da3165e951fb2bc12845bdbadc2e3d97
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307096"
---
# <a name="design-details-inventory-periods"></a>Ontwerpdetails: Voorraadperioden
Geantidateerde boekingen of kostprijscorrecties zijn vaak van invloed op saldi en voorraadwaarderingen voor boekhoudperioden die kunnen worden beschouwd als gesloten. Dit kan nadelige gevolgen hebben bij nauwkeurig rapporteren, vooral binnen mondiale bedrijven. U kunt de functie Voorraadperioden gebruiken om dergelijke problemen te voorkomen door voorraadperioden te openen of te sluiten om boekingen in een opgegeven periode te beperken.  

 Een voorraadperiode is een periode die wordt bepaald door een einddatum, waarin u voorraadtransacties boekt. Als u een voorraadperiode afsluit, kunnen geen gewijzigde waarden meer worden geboekt in de afgesloten periode. Dit omvatten nieuwe waardeboekingen, verwachte of gefactureerde boekingen, wijzigingen in bestaande waarden en kostenherwaarderingen. U kunt echter toch vereffenen met een open artikelpost die valt in de afgesloten periode. Zie [Ontwerpdetails: artikelvereffening](design-details-item-application.md) voor meer informatie.  

 Om te zorgen dat alle transactieposten in een afgesloten periode definitief zijn, moet aan de volgende voorwaarden worden voldaan voordat een voorraadperiode kan worden afgesloten:  

-   Alle uitgaande artikelposten in de periode moeten worden gesloten (geen negatieve voorraad).  
-   Alle artikelkosten in de periode moeten worden bijgewerkt.  
-   Van alle vrijgegeven en gereedgemelde productieorders in de periode moeten de kosten worden aangepast.  

 Wanneer u een voorraadperiode hebt afgesloten, wordt een voorraadperiodepost gemaakt door het nummer te gebruiken van het laatste artikeljournaal dat in de voorraadperiode bestaat. Bovendien worden de tijd, de datum, en de gebruikercode van de gebruiker die de periode sluit, in de voorraadperiodepost geregistreerd. Door deze gegevens te gebruiken met het laatste artikeljournaal voor de vorige periode kunt u zien welke voorraadtransacties zijn geboekt in de voorraadperiode. Het is ook mogelijk een voorraadperiode opnieuw te openen als u moet boeken in een afgesloten periode. Wanneer u een voorraadperiode opnieuw opent, wordt een voorraadperiodepost gemaakt.  

## <a name="see-also"></a>Zie ook  
 [Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md) [Voorraadkosten beheren](finance-manage-inventory-costs.md) [Financiën](finance.md)  
 [Werken met Business Central](ui-work-product.md)
