---
title: 'Procedure: artikelen assembleren'
description: Als het veld Aanvullingsmethode op de artikelkaart Assemblage bevat, is de standaardbevoorradingsmethode van het artikel het assembleren van gedefinieerde onderdelen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 06/14/2021
ms.author: edupont
ms.openlocfilehash: 6fd6e5e90c8307c76868570642a216387d86641d
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435506"
---
# <a name="assemble-items"></a>artikelen samenstellen
Als het veld **Aanvullingsmethode** op de artikelkaart **Assemblage** bevat, is de standaardbevoorradingsmethode van het artikel het assembleren van gedefinieerde onderdelen en mogelijk door een gedefinieerde bron.  

De onderdelen en bronnen die voor dit soort assemblageartikel worden gebruikt, moeten worden gedefinieerd in een assemblagestuklijst. Zie [Werken met stuklijsten](inventory-how-work-BOMs.md) voor meer informatie.  

Assemblageartikelen kunnen voor twee verschillende assemblageprocessen ingesteld worden:  

-   Op voorraad assembleren.  
-   Op order assembleren.  

Meestal gebruikt u **Op voorraad assembleren** voor artikelen die u voorafgaand aan de verkoop wilt assembleren, zoals het voorbereiden op een kit-campagne, en in voorraad wilt houden totdat ze worden besteld. Deze artikelen betreffen meestal standaardartikelen, zoals verpakte kits die u niet aanbiedt voor het aanpassen van aanvragen van klanten.  

U gebruikt meestal **Op order assembleren** voor artikelen die u niet op voorraad wilt hebben, omdat u verwacht deze op speciale klantverzoeken af te kunnen stemmen of omdat u de voorraadkosten wilt minimaliseren door deze net op tijd te leveren. Zie voor meer informatie [Op order geassembleerde artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md).  

Zie voor meer informatie over hoe u een component instelt [Op voorraad assembleren of Op order assembleren begrijpen](assembly-assemble-to-order-or-assemble-to-stock.md).  

Deze instellingen zijn standaardinstellingen die beheren hoe de verkoop en regels voor assemblageorders aanvankelijk worden verwerkt. U kunt van deze standaardinstellingen afwijken en het assemblageartikel op de meest optimale manier leveren bij de verwerking van een verkoop. Zie voor meer informatie [Voorraadartikelen in assembleren-op-order-stromen verkopen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md) en [Op-order-assembleren-artikelen en voorraadartikelen samen verkopen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).

> [!NOTE]  
> Assemblycomponenten worden op een speciale manier verwerkt in standaardmagazijnconfiguraties. Zie voor meer informatie de sectie 'Op-order-assembleren-artikelen in voorraadpicks afhandelen' in [Artikelen picken met een voorraadpick](warehouse-how-to-pick-items-with-inventory-picks.md).   

In deze procedure maakt en verwerkt u een assemblageorder voor artikelen die op voorraad geassembleerd worden, wat betekent dat er geen gekoppelde verkooporder is. De stappen zijn het starten van de assemblageorder, afhandelen van eventuele problemen met de beschikbaarheid van onderdelen en gedeeltelijk boeken van output van het assemblageartikel .

## <a name="to-assemble-an-item"></a>Een item assembleren  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Assemblageorders** in en kies vervolgens de gerelateerde koppeling  
2.  Kies de actie **Nieuw**. De pagina **Nieuwe assemblageorder** wordt geopend.  
3.  Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Selecteer in het veld **Artikelnr.** het assemblageartikel dat u wilt verwerken. Het veld is gefilterd, zodat alleen de artikelen die zijn ingesteld voor assemblage weergegeven worden, wat betekent dat ze een assemblagestuklijst toegewezen hebben gekregen.  
5.  Voer in het veld **Aantal** het aantal eenheden in dat u van het artikel wilt assembleren.  

    > [!NOTE]  
    >  Indien een of meer onderdelen niet beschikbaar zijn om op de opgegeven vervaldatum aan het opgegeven aantal assemblageartikelen te voldoen, wordt de pagina **Beschikbaarheid assemblage** automatisch geopend met gedetailleerde informatie over het aantal assemblageartikelen dat kan worden geassembleerd op basis van de beschikbare onderdelen. Zie voor meer informatie [Beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md). Wanneer u de pagina sluit, wordt de assemblageorder met waarschuwingen omtrent de beschikbaarheid op de regels van het betrokken onderdeel gemaakt.  

    De regels van de assemblageorder worden automatisch gevuld met de inhoud van de assemblagestuklijst en aantallen volgens de orderkop van de assemblageorder.  

    > [!NOTE]  
    >  Indien de pagina **Beschikbaarheid assemblage** werd geopend toen u de assemblage-orderkop invulde, staat bij iedere betrokken orderregel van de assemblage **Ja** in het veld **Waarschuwing beschikbaarheid** met een koppeling naar gedetailleerde beschikbaarheidsinformatie. Zie voor meer informatie Beschikbaarheid controleren. U kunt een beschikbaarheidsprobleem van een onderdeel oplossen door de begindatum uit te stellen, het onderdeel te vervangen door een ander item of een beschikbare vervanging te selecteren indien deze is gedefinieerd.  

6.  Geef in het veld **Te assembleren aantal** op hoeveel eenheden van het assemblageartikel u als uitvoer wilt boeken, de volgende keer dat u de assemblageorder boekt. Dit aantal mag lager zijn dan de waarde in het veld **Aantal** om het gedeeltelijk boeken van uitvoer aan te geven.  

    > [!NOTE]  
    >  Om ervoor te zorgen dat het boeken van het verbruik van onderdelen overeenkomt met het boeken van de output van het assemblageartikel, worden de velden met aantallen in de orderregels van de assemblageorder automatisch aangepast aan de waarde die u in het veld **Te assembleren aantal** invoert.  
7.  Geef op orderregels van assemblageorders van het type **Item** of **Bron**, in het veld **Te verbruiken aantal**, het aantal eenheden op dat u als verbruikt wilt boeken, de volgende keer dat u de assemblageorder boekt.
8.  Wanneer u gereed bent om gedeeltelijk of volledig te boeken, kiest u de actie **Boeken**.  

    > [!NOTE]  
    >  Indien er in de regels van de assemblageorder nog steeds waarschuwingen aanwezig zijn, wordt de boeking geblokkeerd. Een bericht over welke onderdelen niet in voorraad zijn wordt weergegeven.  

Nadat het boeken is voltooid, wordt het assemblageartikel als uitvoer geboekt naar de vestigingscode en mogelijke opslaglocatiecode die op de assemblageorder zijn gedefinieerd. De locatie voor handmatig gemaakte assemblageorders kan worden gekopieerd van de instelling **Standaard locatie voor Orders**. Voor assembleren-op-order kan de vestigingscode van de verkooporderregel worden gekopieerd.  

## <a name="see-also"></a>Zie ook
[Assemblagebeheer](assembly-assemble-items.md)  
[Werken met stuklijsten](inventory-how-work-BOMs.md)  
[Voorraad](inventory-manage-inventory.md)  
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]