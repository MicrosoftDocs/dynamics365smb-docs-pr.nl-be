---
title: 'Procedure: Open artikelposten die uit een vaste vereffening in het artikeldagboek voortkomen sluiten | Microsoft Docs'
description: U kunt het veld **Vereffenen van post** op de pagina **Artikeldagboek** gebruiken om een vaste vereffening tussen een inkomende transactie en de oorspronkelijke uitgaande transactie te maken. Bijvoorbeeld om de uitgaande transactie te corrigeren of de retourzending te verwerken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: e3f210b86168d34ec775f85b416b6d0e365cce88
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816264"
---
# <a name="close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal"></a><span data-ttu-id="f079b-104">Open artikelposten die uit een vaste vereffening in het artikeldagboek voortkomen sluiten</span><span class="sxs-lookup"><span data-stu-id="f079b-104">Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal</span></span>
<span data-ttu-id="f079b-105">U kunt het veld **Vereffenen van post** op de pagina **Artikeldagboek** gebruiken om een vaste vereffening tussen een inkomende transactie en de oorspronkelijke uitgaande transactie te maken.</span><span class="sxs-lookup"><span data-stu-id="f079b-105">You can use the **Applies-from Entry** field on the **Item Journal** page to create a fixed application between an inbound transaction and the original outbound transaction.</span></span> <span data-ttu-id="f079b-106">Bijvoorbeeld om de uitgaande transactie te corrigeren of de retourzending te verwerken.</span><span class="sxs-lookup"><span data-stu-id="f079b-106">For example, to correct the outbound transaction or to process its return.</span></span> <span data-ttu-id="f079b-107">Zie voor meer informatie Vereffenen van post.</span><span class="sxs-lookup"><span data-stu-id="f079b-107">For more information, see Applies-from Entry.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="f079b-108">Vaste vereffeningen die op deze manier worden uitgevoerd, worden alleen toegepast op de kosten, niet op de hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="f079b-108">Fixed applications made in this manner only apply the cost, not the quantity.</span></span> <span data-ttu-id="f079b-109">Bijgevolg sluit de geboekte positieve artikelpost niet de toegepaste uitgaande post en blijft deze zelf ook geopend.</span><span class="sxs-lookup"><span data-stu-id="f079b-109">Accordingly, the posted positive item ledger entry will not close the applied outbound entry and will itself remain open.</span></span> <span data-ttu-id="f079b-110">Dit geldt ook wanneer u een vaste vereffening voor een positieve post toepast op een negatieve post die niet is afgesloten door een gewone positieve post. In dat geval blijven de negatieve en de positieve posten geopend.</span><span class="sxs-lookup"><span data-stu-id="f079b-110">This also applies when you post a fixed application for a positive entry to a negative entry that has not been closed by a regular positive entry, then both the negative and the positive entries will remain open.</span></span>  
>   
>  <span data-ttu-id="f079b-111">Dit betekent dat u een voorraadperiode waarin een dergelijke vermelding bestaat, niet kunt sluiten.</span><span class="sxs-lookup"><span data-stu-id="f079b-111">This also means that you cannot close an inventory period if such an entry exists.</span></span>  

<span data-ttu-id="f079b-112">De volgende procedure laat zien hoe u dergelijke posten kunt sluiten door het uitvoeren van twee corrigerende boekingen in het artikeldagboek.</span><span class="sxs-lookup"><span data-stu-id="f079b-112">The following procedure shows how to close such entries by performing two corrective postings in the item journal.</span></span>  

## <a name="to-close-open-item-ledger-entries-that-result-from-a-fixed-application-in-the-item-journal"></a><span data-ttu-id="f079b-113">Openstaande artikelposten die uit een vaste vereffening in het artikeldagboek voortkomen sluiten</span><span class="sxs-lookup"><span data-stu-id="f079b-113">To close open item ledger entries that result from a fixed application in the item journal</span></span>  

1.  <span data-ttu-id="f079b-114">Gebruik het veld **Vereffenen van post** om een positieve aanpassing met de overeenkomstige hoeveelheid te boeken.</span><span class="sxs-lookup"><span data-stu-id="f079b-114">Use the **Applies-from Entry** field to post a positive adjustment with the corresponding quantity.</span></span> <span data-ttu-id="f079b-115">De oorspronkelijke negatieve post met een vaste vereffening wordt gesloten.</span><span class="sxs-lookup"><span data-stu-id="f079b-115">This closes the original negative entry with a fixed application.</span></span>  
2.  <span data-ttu-id="f079b-116">Gebruik het veld **Vereffenen van post** om een negatieve vereffening te boeken.</span><span class="sxs-lookup"><span data-stu-id="f079b-116">Use the **Applies-to Entry** field to post a negative adjustment.</span></span> <span data-ttu-id="f079b-117">De oorspronkelijke positieve correctiepost met een vaste vereffening wordt gesloten.</span><span class="sxs-lookup"><span data-stu-id="f079b-117">This closes the original corrective positive entry with a fixed application.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f079b-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f079b-118">See Also</span></span>  
[<span data-ttu-id="f079b-119">Artikelposten verwijderen en opnieuw toepassen</span><span class="sxs-lookup"><span data-stu-id="f079b-119"> Remove and Reapply Item Ledger Entries</span></span>](finance-how-to-remove-and-reapply-item-entries.md)  
 <span data-ttu-id="f079b-120">[Verkoopretouren en annuleringen verwerken](sales-how-process-sales-returns-cancellations.md) </span><span class="sxs-lookup"><span data-stu-id="f079b-120">[Process Sales Returns and Cancellations](sales-how-process-sales-returns-cancellations.md) </span></span>  
 <span data-ttu-id="f079b-121">[Voorraadwaardering en kostprijsberekening instellen](finance-set-up-inventory-valuation-and-costing.md) </span><span class="sxs-lookup"><span data-stu-id="f079b-121">[Setting Up Inventory Valuation and Costing](finance-set-up-inventory-valuation-and-costing.md) </span></span>  
 <span data-ttu-id="f079b-122">[Voorraadkosten beheren](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="f079b-122">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 [<span data-ttu-id="f079b-123">Ontwerpdetails: Waarderingsmethoden</span><span class="sxs-lookup"><span data-stu-id="f079b-123">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)
