---
title: Artikelposten sluiten die afkomstig zijn van het gebruik van een vaste vereffening
description: Leer hoe u een vaste vereffening kunt gebruiken tussen een inkomende transactie en de oorspronkelijke uitgaande transactie te maken in het artikeldagboek.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 01/14/2020
ms.author: edupont
ms.openlocfilehash: 2cc663d580da4738247b9fcdbe5fc4504c37fa73
ms.sourcegitcommit: 311e86d6abb9b59a5483324d8bb4cd1be7949248
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5013883"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="6de0b-103">Open artikelposten die uit een vaste vereffening in het artikeldagboek voortkomen sluiten</span><span class="sxs-lookup"><span data-stu-id="6de0b-103">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>

<span data-ttu-id="6de0b-104">U kunt het veld **Vereffenen van post** op de pagina **Artikeldagboek** gebruiken om een vaste vereffening tussen een inkomende transactie en de oorspronkelijke uitgaande transactie te maken.</span><span class="sxs-lookup"><span data-stu-id="6de0b-104">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="6de0b-105">Bijvoorbeeld om de uitgaande transactie te corrigeren of de retourzending te verwerken.</span><span class="sxs-lookup"><span data-stu-id="6de0b-105">For example, to correct the outbound transaction or to process its return.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="6de0b-106">Vaste vereffeningen die op deze manier worden uitgevoerd, worden alleen toegepast op de kosten, niet op de hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="6de0b-106">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="6de0b-107">Bijgevolg sluit de geboekte positieve artikelpost niet de toegepaste uitgaande post en blijft deze zelf ook geopend.</span><span class="sxs-lookup"><span data-stu-id="6de0b-107">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="6de0b-108">Dit geldt ook wanneer u een vaste vereffening voor een positieve post toepast op een negatieve post die niet is afgesloten door een gewone positieve post. In dat geval blijven de negatieve en de positieve posten geopend.</span><span class="sxs-lookup"><span data-stu-id="6de0b-108">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>
> <span data-ttu-id="6de0b-109">Dit betekent dat u een voorraadperiode waarin een dergelijke vermelding bestaat, niet kunt sluiten.</span><span class="sxs-lookup"><span data-stu-id="6de0b-109">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="6de0b-110">U kunt vereffeningsposten in bepaalde omstandigheden wijzigen en opnieuw toepassen met de pagina **Vereffeningsvoorstel**.</span><span class="sxs-lookup"><span data-stu-id="6de0b-110">You can change and reapply application entries under certain conditions by using the **Application Worksheet** page.</span></span>  

<span data-ttu-id="6de0b-111">De volgende procedure laat zien hoe u dergelijke posten kunt sluiten door het uitvoeren van twee corrigerende boekingen in het artikeldagboek.</span><span class="sxs-lookup"><span data-stu-id="6de0b-111">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="6de0b-112">Openstaande artikelposten die uit een vaste vereffening in het artikeldagboek voortkomen sluiten</span><span class="sxs-lookup"><span data-stu-id="6de0b-112">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1. <span data-ttu-id="6de0b-113">Gebruik het veld **Vereffenen van post** om een positieve aanpassing met de overeenkomstige hoeveelheid te boeken.</span><span class="sxs-lookup"><span data-stu-id="6de0b-113">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="6de0b-114">De oorspronkelijke negatieve post met een vaste vereffening wordt gesloten.</span><span class="sxs-lookup"><span data-stu-id="6de0b-114">This closes the original negative entry with a fixed application.</span></span>  

    <span data-ttu-id="6de0b-115">Met het veld **Vereffenen van post** wordt het nummer opgegeven van de uitgaande artikelpost waarvan de kosten worden doorgestuurd naar de inkomende artikelpost tijdens het boeken van een inkomende transactie van het type **Pos. correctie** of **Inkoop** naar het artikeldagboek.</span><span class="sxs-lookup"><span data-stu-id="6de0b-115">The **Applies-from Entry** field specifies the number of the outbound item ledger entry whose cost is forwarded to the inbound item ledger entry when you post an inbound transaction of type **Positive Adjmt.** or **Purchase** with the item journal.</span></span>  
2. <span data-ttu-id="6de0b-116">Gebruik het veld **Vereffenen van post** om een negatieve vereffening te boeken.</span><span class="sxs-lookup"><span data-stu-id="6de0b-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="6de0b-117">De oorspronkelijke positieve correctiepost met een vaste vereffening wordt gesloten.</span><span class="sxs-lookup"><span data-stu-id="6de0b-117">This closes the original corrective positive entry with a fixed application.</span></span>  

    <span data-ttu-id="6de0b-118">Met het veld **Vereffenen met post** wordt opgegeven of het aantal op de artikeldagboekregel moet worden vereffend met een reeds geboekt document.</span><span class="sxs-lookup"><span data-stu-id="6de0b-118">The **Applies-to Entry** field specifies if the quantity in the item journal line should be applied to an already-posted document.</span></span> <span data-ttu-id="6de0b-119">Als dat het geval is, voert u hier het nummer in van de artikelpost waarmee de artikeldagboekregel moet worden vereffend.</span><span class="sxs-lookup"><span data-stu-id="6de0b-119">If this is the case, enter the entry number of the item ledger entry to which the item journal line should be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="6de0b-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6de0b-120">See Also</span></span>

[<span data-ttu-id="6de0b-121">Artikelposten verwijderen en opnieuw toepassen</span><span class="sxs-lookup"><span data-stu-id="6de0b-121">Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
[<span data-ttu-id="6de0b-122">Verkoopretouren en annuleringen verwerken</span><span class="sxs-lookup"><span data-stu-id="6de0b-122">Process Sales Returns and Cancellations</span></span>](sales-how-process-sales-returns-cancellations.md)  
[<span data-ttu-id="6de0b-123">Voorraadwaardering en kostprijsberekening instellen</span><span class="sxs-lookup"><span data-stu-id="6de0b-123">Setting Up Inventory Valuation and Costing</span></span>](finance-set-up-inventory-valuation-and-costing.md)  
[<span data-ttu-id="6de0b-124">Voorraadkosten beheren</span><span class="sxs-lookup"><span data-stu-id="6de0b-124">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="6de0b-125">Ontwerpdetails: Waarderingsmethoden</span><span class="sxs-lookup"><span data-stu-id="6de0b-125">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)
