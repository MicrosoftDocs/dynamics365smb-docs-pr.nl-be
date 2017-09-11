---
title: Werken met stuklijsten om onderdelen te beheren| Microsoft Docs
description: U maakt een assemblagestuklijst om de onderdelen of resources op te geven die vereist zijn om het artikel samen te stellen dat de assemblagestuklijst vertegenwoordigt, en kunt u de onderdelen voor een component weergeven.
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
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e6aef60ee5b206b0ae978f72b92e6f8778290509
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-work-with-bills-of-material"></a><span data-ttu-id="55dad-103">Procedure: Werken met stuklijsten</span><span class="sxs-lookup"><span data-stu-id="55dad-103">How to: Work with Bills of Material</span></span>
> [!NOTE]  
>   <span data-ttu-id="55dad-104">De huidige versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] bevat alleen het eerste deel van de assemblagebeheerfunctie.</span><span class="sxs-lookup"><span data-stu-id="55dad-104">The current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the first part of the Assembly Management feature.</span></span> <span data-ttu-id="55dad-105">Op dit moment kunt u alleen assemblagestuklijsten maken en vervolgens de gerelateerde bovenliggende artikelen verwerken als reguliere voorraadartikelen.</span><span class="sxs-lookup"><span data-stu-id="55dad-105">For now, you can only create assembly BOMs and then handle the related parent items as normal inventory items.</span></span> <span data-ttu-id="55dad-106">In een toekomstige update kunt u de werkelijke assemblage van artikelen van onderdelen beheren, of in assembleren voor voorraad- of assembleren voor order-stromen, en u kunt onderdelen als kits verkopen.</span><span class="sxs-lookup"><span data-stu-id="55dad-106">In a future update, you can manage the actual assembly of items from components, either in assemble-to-stock or assemble-to-order flows, and you can sell components as kits.</span></span>

<span data-ttu-id="55dad-107">U gebruikt stuklijsten om bovenliggende artikelen te structureren die u verkoopt als kits bestaande uit de onderdelen van de bovenliggende artikelen, of die u voor orders of voor voorraad assembleert.</span><span class="sxs-lookup"><span data-stu-id="55dad-107">You use bills of materials (BOMs) to structure parent items that you sell as kits consisting of the parent's components or that you assemble to order or to stock.</span></span>

<span data-ttu-id="55dad-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt naar een stuklijst verwezen als een "assemblagestuklijst".</span><span class="sxs-lookup"><span data-stu-id="55dad-108">In [!INCLUDE[d365fin](includes/d365fin_md.md)], a bill of materials is referred to as an "assembly BOM".</span></span> <span data-ttu-id="55dad-109">Met assemblagestuklijsten wordt opgegeven welke onderdelen in bovenliggende artikelen zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="55dad-109">Assembly BOMs specify which components are contained in parent items.</span></span> <span data-ttu-id="55dad-110">In deze documentatie wordt naar een bovenliggend artikel verwezen als een "assemblageartikel".</span><span class="sxs-lookup"><span data-stu-id="55dad-110">In this documentation, a parent item is referred to as an "assembly item".</span></span>

<span data-ttu-id="55dad-111">Assemblagestuklijsten bevatten gewoonlijk artikelen, maar kunnen ook een of meer resources bevatten die het assemblageartikel samenstellen.</span><span class="sxs-lookup"><span data-stu-id="55dad-111">Assembly BOMs usually contain items but can also contain one or more resources that are required to put the assembly item together.</span></span>

<span data-ttu-id="55dad-112">Assemblagestuklijsten kunnen meerdere niveaus bevatten, wat betekent dat een onderdeel op de assemblagestuklijst zelf ook een assemblageartikel kan zijn.</span><span class="sxs-lookup"><span data-stu-id="55dad-112">Assembly BOMs can have multiple levels, which means that a component on the assembly BOM can be an assembly item itself.</span></span> <span data-ttu-id="55dad-113">In dat geval bevat het veld **Assemblagestuklijst** op de assemblagestuklijstregel **Ja**.</span><span class="sxs-lookup"><span data-stu-id="55dad-113">In that case, the **Assembly BOM** field on the assembly BOM line contains **Yes**.</span></span>

<span data-ttu-id="55dad-114">Er gelden speciale vereisten voor artikelen op assemblagestuklijsten met betrekking tot beschikbaarheid.</span><span class="sxs-lookup"><span data-stu-id="55dad-114">Special requirements apply to items on assembly BOMs with regards to availability.</span></span> <span data-ttu-id="55dad-115">Zie het gedeelte 'De beschikbaarheid van een artikel bekijken op basis van het gebruik ervan in assemblagestuklijsten' in [Procedure: De beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md).</span><span class="sxs-lookup"><span data-stu-id="55dad-115">For more information, see the "To see the availability of an item by its use in assembly BOMs" section in [How to: View the Availability of Items](inventory-how-availability-overview.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="55dad-116">Deze functionaliteit vereist dat uw ervaring is ingesteld op **Pakket**.</span><span class="sxs-lookup"><span data-stu-id="55dad-116">This functionality requires that your experience is set to **Suite**.</span></span> <span data-ttu-id="55dad-117">Zie [Uw Financials-ervaring aanpassen](ui-experiences.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="55dad-117">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>

## <a name="to-create-an-assembly-bom"></a><span data-ttu-id="55dad-118">Een assemblagestuklijst maken</span><span class="sxs-lookup"><span data-stu-id="55dad-118">To create an assembly BOM</span></span>
<span data-ttu-id="55dad-119">Als u een bovenliggend artikel wilt definiëren dat bestaat uit andere artikelen, en mogelijk uit resources die nodig zijn om het bovenliggende artikel samen te stellen, moet u een assemblagestuklijst maken.</span><span class="sxs-lookup"><span data-stu-id="55dad-119">To define a parent item that consists of other items, and potentially of resources required to put the parent together, you must create an assembly BOM.</span></span>  

<span data-ttu-id="55dad-120">Het maken van een assemblagestuklijst bestaat uit twee delen:</span><span class="sxs-lookup"><span data-stu-id="55dad-120">There are two parts to creating an assembly BOM:</span></span>
- <span data-ttu-id="55dad-121">Een nieuw artikel instellen</span><span class="sxs-lookup"><span data-stu-id="55dad-121">Setting up a new item</span></span>
- <span data-ttu-id="55dad-122">De stuklijststructuur van het assemblageartikel definiëren.</span><span class="sxs-lookup"><span data-stu-id="55dad-122">Defining the BOM structure of the assembly item.</span></span>

1. <span data-ttu-id="55dad-123">Stel een nieuw artikel in.</span><span class="sxs-lookup"><span data-stu-id="55dad-123">Set up a new item.</span></span> <span data-ttu-id="55dad-124">Zie [Procedure: Nieuwe artikelen registreren](inventory-how-register-new-items.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="55dad-124">For more information, see [How to: Register New Items](inventory-how-register-new-items.md).</span></span>

    <span data-ttu-id="55dad-125">Ga verder om onderdelen of resources in de assemblagestuklijst in te voeren.</span><span class="sxs-lookup"><span data-stu-id="55dad-125">Proceed to enter components or resources on the assembly BOM.</span></span>  
2. <span data-ttu-id="55dad-126">Kies in het venster **Artikel** voor een assemblageartikel de actie **Assemblage** en kies vervolgens de actie **Assemblagestuklijst**.</span><span class="sxs-lookup"><span data-stu-id="55dad-126">In the **Item Card** window for an assembly item, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
3. <span data-ttu-id="55dad-127">Vul indien nodig de velden in het venster **Assemblagestuklijst** in.</span><span class="sxs-lookup"><span data-stu-id="55dad-127">In the **Assembly BOM** window, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-view-the-components-of-an-assembly-item-indented-according-to-the-bom-structure"></a><span data-ttu-id="55dad-128">De onderdelen van een assemblageartikel weergeven terwijl het is ingesprongen volgens de stuklijststructuur</span><span class="sxs-lookup"><span data-stu-id="55dad-128">To view the components of an assembly item indented according to the BOM structure</span></span>
<span data-ttu-id="55dad-129">Vanuit het venster **Assemblagestuklijst** kunt u een afzonderlijk venster openen dat de onderdelen en resources bevat die zijn ingesprongen op basis van hun stuklijstpositie onder het assemblageartikel.</span><span class="sxs-lookup"><span data-stu-id="55dad-129">From the **Assembly BOM** window, you can open a separate window that shows the components and any resources indented according to their BOM position under the assembly item.</span></span>

1. <span data-ttu-id="55dad-130">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="55dad-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="55dad-131">Open de kaart voor een assemblageartikel.</span><span class="sxs-lookup"><span data-stu-id="55dad-131">Open the card for an assembly item.</span></span> <span data-ttu-id="55dad-132">(Het veld **Assemblagestuklijst** in het venster **Artikelen** bevat **Ja**.)</span><span class="sxs-lookup"><span data-stu-id="55dad-132">(The **Assembly BOM** field in the **Items** window contains **Yes**.)</span></span>
3. <span data-ttu-id="55dad-133">Kies in het venster **Artikel** de actie **Assemblage** en kies vervolgens de actie **Assemblagestuklijst**.</span><span class="sxs-lookup"><span data-stu-id="55dad-133">In the **Item Card** window, choose the **Assembly** action, and then choose the **Assembly BOM** action.</span></span>
4. <span data-ttu-id="55dad-134">Kies in het venster **Assemblagestuklijst** de actie **Stuklijst weergeven**.</span><span class="sxs-lookup"><span data-stu-id="55dad-134">In the **Assembly BOM** window, choose the **Show BOM** action.</span></span>

## <a name="to-buy-sell-or-transfer-assembly-items"></a><span data-ttu-id="55dad-135">Assemblageartikelen inkopen, verkopen of verplaatsen</span><span class="sxs-lookup"><span data-stu-id="55dad-135">To buy, sell, or transfer assembly items</span></span>
<span data-ttu-id="55dad-136">Omdat de huidige versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] alleen de mogelijkheid bevat om assemblagestuklijsten te definiëren en toe te wijzen aan artikelen, kunt u assemblageartikelen op documentregels alleen als gewone artikelen verwerken.</span><span class="sxs-lookup"><span data-stu-id="55dad-136">Because the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] only contains the ability to define and assign assembly BOMs to items, you can handle assembly items on document lines as normal items only.</span></span>

<span data-ttu-id="55dad-137">**Let op**: de voorraadhoeveelheid van stuklijstonderdelen wordt niet gecorrigeerd als u dat doet.</span><span class="sxs-lookup"><span data-stu-id="55dad-137">**Caution**: The inventory quantity of BOM components will not be adjusted if you do so.</span></span>

## <a name="see-also"></a><span data-ttu-id="55dad-138">Zie ook</span><span class="sxs-lookup"><span data-stu-id="55dad-138">See Also</span></span>
[<span data-ttu-id="55dad-139">Procedure: Nieuwe artikelen registreren</span><span class="sxs-lookup"><span data-stu-id="55dad-139">How to: Register New Items</span></span>](inventory-how-register-new-items.md)  
<span data-ttu-id="55dad-140">[Procedure: beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md)   </span><span class="sxs-lookup"><span data-stu-id="55dad-140">[How to: View the Availability of Items](inventory-how-availability-overview.md)   </span></span>  
[<span data-ttu-id="55dad-141">Voorraad</span><span class="sxs-lookup"><span data-stu-id="55dad-141">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="55dad-142">[Werken met [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="55dad-142">[Working with [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)</span></span>

