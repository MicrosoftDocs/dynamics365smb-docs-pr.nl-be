---
title: Nieuwe waardeposten maken voor artikelen in de voorraad| Microsoft Docs
description: Beschrijft hoe u de waardeposten vermeerdert of vermindert van een of meer artikelen in de voorraad door de huidige, berekende waarde ervan te boeken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: costing, inventory cost, value entries
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 602381b34a057120cc53deca4dd293f939777dc5
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1243101"
---
# <a name="revalue-inventory"></a><span data-ttu-id="1bde1-103">Voorraad herwaarderen</span><span class="sxs-lookup"><span data-stu-id="1bde1-103">Revalue Inventory</span></span>
<span data-ttu-id="1bde1-104">Gebruik het herwaarderingsdagboek als u de voorraadwaarde van een artikel of een bepaalde artikelpost wilt vermeerderen of verminderen.</span><span class="sxs-lookup"><span data-stu-id="1bde1-104">If you want to appreciate or depreciate an item or a specific item ledger entry, you must use the revaluation journal.</span></span>

## <a name="to-revalue-inventory"></a><span data-ttu-id="1bde1-105">Voorraad herwaarderen</span><span class="sxs-lookup"><span data-stu-id="1bde1-105">To revalue inventory</span></span>
1. <span data-ttu-id="1bde1-106">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Herwaarderingsdagboek** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="1bde1-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Revaluation Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="1bde1-107">Kies de actie **Voorraadwaarde berekenen**.</span><span class="sxs-lookup"><span data-stu-id="1bde1-107">Choose the **Calculate Inventory Value** action.</span></span>
3. <span data-ttu-id="1bde1-108">Vul op de pagina **Voorraadwaarde berekenen** indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="1bde1-108">On the **Calculate Inventory Value** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="1bde1-109">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="1bde1-109">Choose the **OK** button.</span></span>
5. <span data-ttu-id="1bde1-110">Voer op elke regel op de pagina **Herwaarderingsdagboek** het veld **Kostprijs (Geherwaardeerd)** in en voer de nieuwe eenheidskosten in.</span><span class="sxs-lookup"><span data-stu-id="1bde1-110">On each line on the **Revaluation Journal** page, in the **Unit Cost (Revalued)** field, enter the new unit cost.</span></span> <span data-ttu-id="1bde1-111">U kunt ook het nieuwe totale bedrag in het veld **Voorraadwaarde (Geherwaardeerd)** invoeren.</span><span class="sxs-lookup"><span data-stu-id="1bde1-111">Alternatively, enter the new total amount in the **Inventory Value (Revalued)** field.</span></span>

    <span data-ttu-id="1bde1-112">De bijbehorende velden worden automatisch bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="1bde1-112">The relevant fields are automatically updated.</span></span> <span data-ttu-id="1bde1-113">In het veld **Bedrag** wordt de werkelijke wijziging in de voorraadwaarde voor de geselecteerde artikelpost weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1bde1-113">Note that the **Amount** field shows the actual change in inventory value for the selected item ledger entry.</span></span> <span data-ttu-id="1bde1-114">Het verschil tussen de waarden in de velden **Voorraadwaarde (Berekend)** en **Voorraadwaarde (Geherwaardeerd)** wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="1bde1-114">It calculates the difference between the **Inventory Value (Calculated)** field and the **Inventory Value (Revalued)** field.</span></span>
6. <span data-ttu-id="1bde1-115">Wanneer u alle regels in het herwaarderingsdagboek hebt ingevuld, kiest u de actie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="1bde1-115">When you have completed all lines in the revaluation journal, choose the **Post** action.</span></span>

<span data-ttu-id="1bde1-116">Nieuwe waardeposten worden nu gemaakt om de herwaarderingen weer te geven die u hebt geboekt.</span><span class="sxs-lookup"><span data-stu-id="1bde1-116">New value entries are now created to reflect the revaluations that you have posted.</span></span> <span data-ttu-id="1bde1-117">U kunt de nieuwe waarden op de desbetreffende artikelkaarten bekijken.</span><span class="sxs-lookup"><span data-stu-id="1bde1-117">You can see the new values on the respective item cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="1bde1-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1bde1-118">See Also</span></span>
[<span data-ttu-id="1bde1-119">Ontwerpdetails: Herwaardering</span><span class="sxs-lookup"><span data-stu-id="1bde1-119">Design Details: Revaluation</span></span>](design-details-revaluation.md)  
[<span data-ttu-id="1bde1-120">Voorraad</span><span class="sxs-lookup"><span data-stu-id="1bde1-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="1bde1-121">Verkoop</span><span class="sxs-lookup"><span data-stu-id="1bde1-121">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="1bde1-122">Inkoop</span><span class="sxs-lookup"><span data-stu-id="1bde1-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="1bde1-123">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1bde1-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
