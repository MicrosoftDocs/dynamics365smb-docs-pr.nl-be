---
title: 'Procedure: Werken met stuklijsten| Microsoft Docs'
description: Assemblagestuklijsten geven aan welke artikelen of resources vereist zijn voor het assembleren van het artikel dat de assemblagestuklijst vertegenwoordigt. Assemblagestuklijsten bevatten gewoonlijk artikelen, maar kunnen ook een of meer resources bevatten die de assemblageactiviteiten uitvoeren.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: ce75a9d292e12c58efc51c4db2fbc5a37b7553c7
ms.openlocfilehash: f55dcf4b391ae42ab46a22b729597a96645d9b71
ms.contentlocale: nl-be
ms.lasthandoff: 05/05/2017


---
# <a name="how-to-work-with-bills-of-materials"></a>Procedure: Werken met stuklijsten+
**Opmerking**: de huidige versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] bevat alleen het eerste deel van de assemblagebeheerfunctie. Op dit moment kunt u alleen assemblagestuklijsten maken en vervolgens de gerelateerde bovenliggende artikelen verwerken als reguliere voorraadartikelen. In een toekomstige update kunt u de werkelijke assemblage van artikelen van onderdelen beheren, of in assembleren voor voorraad- of assembleren voor order-stromen, en u kunt onderdelen als kits verkopen.

U gebruikt stuklijsten om bovenliggende artikelen te structureren die u verkoopt als kits bestaande uit de onderdelen van de bovenliggende artikelen, of die u voor orders of voor voorraad assembleert.

In [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt naar een stuklijst verwezen als een "assemblagestuklijst". Met assemblagestuklijsten wordt opgegeven welke onderdelen in bovenliggende artikelen zijn opgenomen. In deze documentatie wordt naar een bovenliggend artikel verwezen als een "assemblageartikel".

Assemblagestuklijsten bevatten gewoonlijk artikelen, maar kunnen ook een of meer resources bevatten die het assemblageartikel samenstellen.

Assemblagestuklijsten kunnen meerdere niveaus bevatten, wat betekent dat een onderdeel op de assemblagestuklijst zelf ook een assemblageartikel kan zijn. In dat geval bevat het veld **Assemblagestuklijst** op de assemblagestuklijstregel **Ja**.

Er gelden speciale vereisten voor artikelen op assemblagestuklijsten met betrekking tot beschikbaarheid. Zie het gedeelte "De beschikbaarheid van een artikel bekijken op basis van het gebruik ervan in assemblagestuklijsten" in [Procedure: Een beschikbaarheidoverzicht krijgen](inventory-how-availability-overview.md).

**Opmerking**: voor deze functionaliteit is vereist dat uw ervaring is ingesteld op **Pakket**. Zie [Uw Financials-ervaring aanpassen](ui-experiences.md) voor meer informatie.

## <a name="to-create-an-assembly-bom"></a>Een assemblagestuklijst maken
Als u een bovenliggend artikel wilt definiëren dat bestaat uit andere artikelen, en mogelijk uit resources die nodig zijn om het bovenliggende artikel samen te stellen, moet u een assemblagestuklijst maken.  

Het maken van een assemblagestuklijst bestaat uit twee delen:
- Een nieuw artikel instellen
- De stuklijststructuur van het assemblageartikel definiëren.

1. Stel een nieuw artikel in. Zie [Procedure: Nieuwe artikelen registreren](inventory-how-register-new-items.md) voor meer informatie.

    Ga verder om onderdelen of resources in de assemblagestuklijst in te voeren.  
2. Kies in het venster **Artikel** voor een assemblageartikel de actie **Assemblage** en kies vervolgens de actie **Assemblagestuklijst**.
3. Vul indien nodig de velden in het venster **Assemblagestuklijst** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a>De onderdelen van een assemblageartikel weergeven terwijl het is ingesprongen volgens de stuklijststructuur
Vanuit het venster **Assemblagestuklijst** kunt u een afzonderlijk venster openen dat de onderdelen en resources bevat die zijn ingesprongen op basis van hun stuklijstpositie onder het assemblageartikel.

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart voor een assemblageartikel. (Het veld **Assemblagestuklijst** in het venster **Artikelen** bevat **Ja**.)
3. Kies in het venster **Artikel** de actie **Assemblage** en kies vervolgens de actie **Assemblagestuklijst**.
4. Kies in het venster **Assemblagestuklijst** de actie **Stuklijst weergeven**.

## <a name="to-buy-sell-or-transfer-assembly-items"></a>Assemblageartikelen inkopen, verkopen of verplaatsen
Omdat de huidige versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] alleen de mogelijkheid bevat om assemblagestuklijsten te definiëren en toe te wijzen aan artikelen, kunt u assemblageartikelen op documentregels alleen als gewone artikelen verwerken.

**Let op**: de voorraadhoeveelheid van stuklijstonderdelen wordt niet gecorrigeerd als u dat doet.

## <a name="see-also"></a>Zie ook
[Procedure: Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Procedure: Een beschikbaarheidoverzicht krijgen](inventory-how-availability-overview.md)     
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)

