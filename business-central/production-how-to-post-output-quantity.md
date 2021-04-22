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
# <a name="batch-post-output-and-run-times"></a><span data-ttu-id="d74c5-103">Output en bewerkingstijden in batches boeken</span><span class="sxs-lookup"><span data-stu-id="d74c5-103">Batch Post Output and Run Times</span></span>
<span data-ttu-id="d74c5-104">De outputhoeveelheid geeft de voortgang van het werk weer in de vorm van de voltooide hoeveelheid en de gebruikte capaciteit van de afdeling of de bewerkingsplaats.</span><span class="sxs-lookup"><span data-stu-id="d74c5-104">The output quantity represents the work progress in the form of the finished quantity and used capacity of work or machine center.</span></span>

<span data-ttu-id="d74c5-105">U kunt ook het outputdagboek gebruiken om:</span><span class="sxs-lookup"><span data-stu-id="d74c5-105">You can use the output journal to:</span></span>
*  <span data-ttu-id="d74c5-106">Voorraad aan te passen in verband met de output van voltooide artikelen vanuit productie.</span><span class="sxs-lookup"><span data-stu-id="d74c5-106">Adjust inventory in connection with output of finished items from production.</span></span>
*  <span data-ttu-id="d74c5-107">Hoeveelheden en uitval te registreren voor elke bewerking in productierouting.</span><span class="sxs-lookup"><span data-stu-id="d74c5-107">Register quantities and scrap for each operation in production routing.</span></span>
*  <span data-ttu-id="d74c5-108">Instel- en looptijd te registreren voor afdelingen en bewerkingsplaatsen.</span><span class="sxs-lookup"><span data-stu-id="d74c5-108">Register setup and run time for work and machine centers.</span></span>

> [!NOTE]
> <span data-ttu-id="d74c5-109">Als productierouting wordt gebruikt, wordt de voorraad alleen bijgewerkt wanneer u het outputaantal bij de laatste bewerking boekt.</span><span class="sxs-lookup"><span data-stu-id="d74c5-109">If production routing are used, the inventory is updated only when you post output quantity on the last operation.</span></span>

<span data-ttu-id="d74c5-110">Met het venster **Productiedagboek** kunt u dezelfde taken uitvoeren als in het venster **Outputdagboek** en tegelijkertijd de gerelateerde taken voor verbruiksboeking uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="d74c5-110">With the **Production Journal** window, you can perform the same tasks as in the **Output Journal** window and at the same time perform the related consumption posting tasks.</span></span> <span data-ttu-id="d74c5-111">Zie voor meer informatie [Verbruik en output registreren voor één vrijgegeven productieorderregel](production-how-to-register-consumption-and-output.md).</span><span class="sxs-lookup"><span data-stu-id="d74c5-111">For more information, see [Register Consumption and Output for One Released Production order line](production-how-to-register-consumption-and-output.md).</span></span>

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines"></a><span data-ttu-id="d74c5-112">Outputaantallen boeken en/of looptijden registreren voor een of meer productieorderregels</span><span class="sxs-lookup"><span data-stu-id="d74c5-112">To post output quantities and/or register run times for one or more production order lines</span></span>
1. <span data-ttu-id="d74c5-113">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Outputdagboek** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="d74c5-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d74c5-114">Voer in de velden informatie over de productieorder en output en/of looptijd in.</span><span class="sxs-lookup"><span data-stu-id="d74c5-114">Fill in the fields with the production order data and the output data and/or run time.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    <span data-ttu-id="d74c5-115">U kunt de functie **Bewerkingsplan weergeven** om dagboekregels te genereren op basis van productieorders.</span><span class="sxs-lookup"><span data-stu-id="d74c5-115">You can use the **Explode Routing** function to generate journal lines from production orders.</span></span>
  
4. <span data-ttu-id="d74c5-116">Als de bewerking is voltooid, selecteert u het veld **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="d74c5-116">If the operation has been completed, select the **Finished** field.</span></span>  
5. <span data-ttu-id="d74c5-117">Kies de actie **Boeken** om de activiteiten te boeken.</span><span class="sxs-lookup"><span data-stu-id="d74c5-117">Choose the **Post** action to post the operations.</span></span> 
 
<span data-ttu-id="d74c5-118">Capaciteitsboekingen worden bijgewerkt voor de gebruikte werk- of machinecentra met informatie over tijd en hoeveelheid output en uitval.</span><span class="sxs-lookup"><span data-stu-id="d74c5-118">Capacity ledger entries are updated for the used work or machine centers with information about time and quantity of output and scrap.</span></span> <span data-ttu-id="d74c5-119">Als u de laatste bewerking heeft geboekt, wordt het artikel aan de inventaris toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="d74c5-119">If you posted the last operation, the item will be added to the inventory.</span></span> 

## <a name="see-also"></a><span data-ttu-id="d74c5-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d74c5-120">See Also</span></span>  
<span data-ttu-id="d74c5-121">[Handmatig uitval boeken](production-how-to-post-scrap.md)
[Omgekeerde outputboeking](production-how-to-reverse-output-posting.md)
[Productie](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="d74c5-121">[Post Scrap Manually](production-how-to-post-scrap.md)
[Reverse Output Posting](production-how-to-reverse-output-posting.md)
[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="d74c5-122">Productie instellen</span><span class="sxs-lookup"><span data-stu-id="d74c5-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="d74c5-123">[Gepland](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="d74c5-123">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="d74c5-124">Voorraad</span><span class="sxs-lookup"><span data-stu-id="d74c5-124">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="d74c5-125">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d74c5-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]
