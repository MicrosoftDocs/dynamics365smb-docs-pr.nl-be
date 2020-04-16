---
title: Op voorraad assembleren of Op order assembleren begrijpen | Microsoft Docs
description: Componenten kunnen worden geleverd door deze te assembleren bij bestelling of door deze te assembleren om op voorraad te worden gehouden tot deze nodig zijn voor een verkooporder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 1f34ee61fa532aa7600baa8883d182cbad545493
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186824"
---
# <a name="understanding-assemble-to-order-and-assemble-to-stock"></a>Op voorraad assembleren of Op order assembleren begrijpen
Assemblage-artikelen kunnen worden opgegeven in de volgende twee processen:  

-   Op order assembleren.  
-   Op voorraad assembleren.  

## <a name="assemble-to-order"></a>Op order assembleren  
U gebruikt meestal *Op order assembleren* voor artikelen die u niet op voorraad wilt hebben omdat u verwacht deze op speciale klantverzoeken af te kunnen stemmen of omdat u de voorraadkosten wilt minimaliseren. De ondersteunende functionaliteit omvat:  

-   De mogelijkheid om assemblage-artikelen aan te passen bij het opnemen van een verkooporder.  
-   Een overzicht met betrekking tot de beschikbaarheid van het assemblageartikel en de bijbehorende onderdelen.  
-   De mogelijkheid om assemblagecomponenten direct te reserveren om een onmiddellijk afhandeling te garanderen.  
-   Een functie voor het vaststellen van de winstgevendheid van de aangepaste door het berekenen van prijzen en kosten.  
-   Integratie met betrekking tot het magazijn om de assemblage en verzending te vereenvoudigen.  
-   De mogelijkheid om op basis van orders te assembleren op het punt waarop een verkoopofferte of een raamcontract wordt gemaakt.  
-   De mogelijkheid om voorraadaantallen te combineren met aantallen voor assembleren op basis van orders.  

Het artikel wordt in het proces voor assembleren op basis van orders geassembleerd in reactie op een verkooporder, waarbij er sprake is van een één-op-één koppeling tussen de assemblageorder en de verkooporder.  

Wanneer u een artikel voor assembleren op basis van orders invoert op een verkoopregel, wordt er automatisch een assemblageorder gemaakt met een kop die is gebaseerd op de verkoopregel en met regels die zijn gebaseerd op de assemblagestuklijst van het artikel vermenigvuldigd met het bestelaantal. U kunt de pagina met **regels voor op order assembleren** gebruiken om de gekoppelde assemblageorderregels weer te geven om u te helpen bij het aanpassen van het assemblageartikel en het vaststellen van een leveringsdatum die is gebaseerd op informatie over de beschikbaarheid van componenten. Zie voor meer informatie [Op order geassembleerde artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md).  

> [!NOTE]  
>  Hoewel dit geen onderdeel van het standaardproces is, kunt u voorraadaantallen verkopen met aantallen voor assembleren op basis van orders. Zie voor meer informatie [Voorraadartikelen verkopen in assembleren-op-order-stromen](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).  

 Als u dit proces wilt inschakelen, moet het veld **Assemblagebeleid** op de artikelkaart zijn ingesteld op **Assemblage voor order**.  

## <a name="assemble-to-stock"></a>Op voorraad assembleren  
 U gebruikt gewoonlijk *Op voorraad assembleren* voor artikelen die u voorafgaand aan de verkoop wilt assembleren, zoals bij het voorbereiden op een kit-campagne, en die u in voorraad wilt houden totdat deze worden besteld. Deze artikelen betreffen meestal standaardartikelen, zoals verpakte kits die u niet aanbiedt voor het aanpassen van aanvragen van klanten.  

 In het proces voor het assembleren voor voorraad, wordt het artikel geassembleerd zonder dat er sprake is van een onmiddellijke verkoopvraag en wordt het artikel opgeslagen als een voorraadartikel voor latere verkoop of verbruik als een halffabricaat. Zie [Artikelen assembleren](assembly-how-to-assemble-items.md) voor meer informatie. Vanaf dit punt wordt het artikel gepickt en verwerkt als één artikel en wordt het behandeld als een voltooid productieartikel.  

 Wanneer u een artikel voor het assembleren voor voorraad op een verkoopregel invoert, is de regel hetzelfde als bij elk ander artikel dat uit de voorraad wordt verkocht. Beschikbaarheid wordt bijvoorbeeld alleen gecontroleerd voor het assemblageartikel alleen.  

> [!NOTE]  
>  Hoewel het geen onderdeel is van het standaardproces, kunt u een artikel assembleren ten behoeve van orders wanneer dit is ingesteld voor assembleren voor de voorraad. Zie voor meer informatie [Op-order-assembleren-artikelen en voorraadartikelen samen verkopen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

 Als u dit proces wilt inschakelen, moet het veld **Assemblagebeleid** op de artikelkaart zijn ingesteld op **Op voorraad assembleren**.  

## <a name="combination-scenarios"></a>Combinatiescenario 's  
 Een algemeen beginsel van assemblagebeheer is dat in het geval van combinatie op een verkooporderregel, aantallen voor het assembleren voor orders moeten worden verzonden voor voorraadaantallen.  

 Als een assemblageorder is gekoppeld aan een verkooporderregel, wordt de waarde in het veld **Aant. op order assembleren** op de verkooporderregel gekopieerd naar het veld **Te assembleren aantal**, via het veld **Aantal** in de assemblageorderkoptekst. Zie voor meer informatie [Op order geassembleerde artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md).  

 Daarnaast is de waarde in het veld **Te assembleren aantal** gerelateerd aan het veld **Te verzenden aantal** op de verkooporderregel. Deze relatie beheert de verzending van aantallen voor assembleren voor orders zowel gedeeltelijk als volledig. Dit geldt zowel wanneer het volledige verkoopregelaantal wordt geassembleerd ten behoeve van orders, als in combinatiescenario's waarin een deel van het verkoopregelaantal wordt geassembleerd voor orders en een ander deel wordt verzonden vanuit de voorraad. In het combinatiescenario beschikt u echter over extra flexibiliteit met betrekking tot deelverzending omdat u het veld **Te assembleren aantal** binnen vooraf gedefinieerde regels kunt wijzigen om op te geven hoeveel eenheden vanuit voorraad en hoeveel eenheden via assemblage voor orders moeten worden verzonden.  

 Als het volledige aantal op de verkoopregel op order moet worden geassembleerd en verzonden, wordt de waarde in het veld **Te verzenden aantal** gekopieerd naar het veld **Te assembleren aantal** op de gekoppelde assemblageorder als u het te verzenden aantal wijzigt. Dit zorgt ervoor dat het te verzenden aantal volledig wordt geleverd door het aantal assembleren voor order.  

 Echter, in combinatiescenario's wordt de hele waarde in **Te verzenden aantal** niet gekopieerd naar het veld **Te assembleren aantal** op de assemblageorderkop. In plaats daarvan wordt er een standaardwaarde ingevoegd in het veld **Te assembleren aantal** die volgens een vooraf gedefinieerde regel wordt berekend op basis van het veld **Te verzenden aantal**. Deze regel zorgt ervoor dat aantallen voor assemblage voor orders eerst worden verzonden.  

 Als u wilt afwijken van deze standaardprocedure omdat u bijvoorbeeld alleen een groter of een kleiner aantal dan het aantal in het veld **Te verzenden aantal** wilt assembleren, kunt u vervolgens het veld **Te assembleren aantal** wijzigen, maar alleen binnen vooraf gedefinieerde regels, zoals deze hieronder zijn beschreven.  

 Een voorbeeld van waarom u het assemblage-aantal mogelijk wilt wijzigen, is dat u een gedeeltelijke verzending van voorraadaantallen wilt boeken voordat de assemblage-uitvoer wordt verzonden.  

 Hierna worden de regels uitgelegd voor het definiëren van de minimum- en maximumwaarden die u handmatig in het veld **Te assembleren aantal** kunt invoeren wanneer u in een combinatiescenario wilt afwijken van de standaardwaarde. In de tabel wordt een combinatiescenario weergegeven waarbij het veld **Te verzenden aantal** op de gekoppelde verkooporderregel wordt gewijzigd van 7 in 4, waardoor **Te assembleren aantal** wordt ingesteld op de standaardwaarde 4.  

||Verkooporderregel|Assemblageorderkop|  
|-|----------------------|---------------------------|  
||**Aantal**|**Te verzenden aantal**|**Aant. op order assembleren**|**Verzonden aantal**|**Aantal**|**Te assembleren aantal**|**Geassembleerde hoeveelheid**|**Resterend aantal**|  
|Eerste|10|7|7|0|7|7|0|7|  
|Wijzigen||4||||4 (standaard ingevoegd)|||  

 Gebaseerd op de bovenstaande situatie, kunt u het veld **Te assembleren aantal** alleen als volgt wijzigen:  

-   Het minimumaantal dat u kunt invoeren is 1. Dit is omdat u ten minste één eenheid moet assembleren om de vier eenheden te kunnen verkopen, waarbij wordt aangenomen dat de overige drie eenheden in de voorraad beschikbaar zijn.  
-   Het maximumaantal dat u kunt invoeren is 4. Zo wordt ervoor gezorgd dat u niet meer van dit assembleren-voor-order artikel assembleert dan wat nodig is voor de verkoop.  

## <a name="see-also"></a>Zie ook  
[Assemblagebeheer](assembly-assemble-items.md)  
[Werken met stuklijsten](inventory-how-work-BOMs.md)  
[Voorraad](inventory-manage-inventory.md)  
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
