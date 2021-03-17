---
title: Outputboeking tegenboeken | Microsoft Docs
description: Het kan voorkomen dat een outputboeking moet worden tegengeboekt. Dit is bijvoorbeeld het geval als er een gegevensinvoerfout is gemaakt en er een onjuiste hoeveelheid output is geboekt op een productieorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5901ad209149c113497d676a5c86379fc8424a0e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392761"
---
# <a name="reverse-output-posting"></a><span data-ttu-id="353a2-104">Outputboeking tegenboeken</span><span class="sxs-lookup"><span data-stu-id="353a2-104">Reverse Output Posting</span></span>
<span data-ttu-id="353a2-105">Het kan voorkomen dat een outputboeking moet worden tegengeboekt.</span><span class="sxs-lookup"><span data-stu-id="353a2-105">There are times when output posting must be reversed.</span></span> <span data-ttu-id="353a2-106">Dit is bijvoorbeeld het geval als er een gegevensinvoerfout is gemaakt en er een onjuiste hoeveelheid output is geboekt op een productieorder.</span><span class="sxs-lookup"><span data-stu-id="353a2-106">An example of this would be if a data entry error occurred and an incorrect amount of output is posted to a production order.</span></span>  

## <a name="to-reverse-an-output-posting"></a><span data-ttu-id="353a2-107">Een outputboeking tegenboeken</span><span class="sxs-lookup"><span data-stu-id="353a2-107">To reverse an output posting</span></span>  
1.  <span data-ttu-id="353a2-108">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Outputdagboek** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="353a2-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Output Journal**, and then choose the related link.</span></span> <span data-ttu-id="353a2-109">Selecteer uw batch.</span><span class="sxs-lookup"><span data-stu-id="353a2-109">Select your batch.</span></span>  
2. <span data-ttu-id="353a2-110">Vul de benodigde velden in.</span><span class="sxs-lookup"><span data-stu-id="353a2-110">Fill in the fields as necessary.</span></span> <span data-ttu-id="353a2-111">Zie voor meer informatie [Output en bewerkingstijd in batches boeken](production-how-to-post-output-quantity.md).</span><span class="sxs-lookup"><span data-stu-id="353a2-111">For more information, see [Batch Post Output and Run Times](production-how-to-post-output-quantity.md).</span></span>
3.  <span data-ttu-id="353a2-112">Selecteer in het veld **Vereffenen met post** de bijbehorende artikelpost.</span><span class="sxs-lookup"><span data-stu-id="353a2-112">In the **Applies-To Entry** field, select the associated item ledger entry.</span></span> <span data-ttu-id="353a2-113">Hiermee voert u een tegenboeking uit van de capaciteit en artikelposten.</span><span class="sxs-lookup"><span data-stu-id="353a2-113">This reverses the capacity and item ledger entries.</span></span>  
4. <span data-ttu-id="353a2-114">Boek de tegenboeking door het dagboek te boeken.</span><span class="sxs-lookup"><span data-stu-id="353a2-114">Post the reversal by posting the journal.</span></span>  

<span data-ttu-id="353a2-115">De posten van het outputdagboek worden als positieve herwaardering geboekt op de artikelposten.</span><span class="sxs-lookup"><span data-stu-id="353a2-115">The output journal entries are posted to the item ledger as a positive adjustment.</span></span>  

## <a name="see-also"></a><span data-ttu-id="353a2-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="353a2-116">See Also</span></span>  
 <span data-ttu-id="353a2-117">[Productie](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="353a2-117">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
 [<span data-ttu-id="353a2-118">Productie instellen</span><span class="sxs-lookup"><span data-stu-id="353a2-118">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
 <span data-ttu-id="353a2-119">[Gepland](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="353a2-119">[Planning](production-planning.md)    </span></span>  
 [<span data-ttu-id="353a2-120">Voorraad</span><span class="sxs-lookup"><span data-stu-id="353a2-120">Inventory</span></span>](inventory-manage-inventory.md)  
 [<span data-ttu-id="353a2-121">Inkoop</span><span class="sxs-lookup"><span data-stu-id="353a2-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
 <span data-ttu-id="353a2-122">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="353a2-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]