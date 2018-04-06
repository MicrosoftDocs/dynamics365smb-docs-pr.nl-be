---
title: 'Procedure: vaste verrekenprijzen aanpassen | Microsoft Docs'
description: U moet regelmatig de vaste verrekenprijzen van onderdelen bijwerken en de nieuwe kosten tot aan het hoofdartikel berekenen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/09/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 53716a78d7538e034c097506205a840b1243c4cf
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="update-standard-costs"></a><span data-ttu-id="2adc1-103">Vaste verrekenprijs bijwerken</span><span class="sxs-lookup"><span data-stu-id="2adc1-103">Update Standard Costs</span></span>
<span data-ttu-id="2adc1-104">U moet regelmatig de vaste verrekenprijzen van onderdelen bijwerken en de nieuwe kosten tot aan het hoofdartikel berekenen.</span><span class="sxs-lookup"><span data-stu-id="2adc1-104">You must periodically update the standard costs of components and roll the new costs up to the parent item.</span></span> <span data-ttu-id="2adc1-105">Het proces bestaat meestal uit de volgende vier stappen:</span><span class="sxs-lookup"><span data-stu-id="2adc1-105">The process typically consists of the following four steps:</span></span>  

1.  <span data-ttu-id="2adc1-106">Kosten bijwerken op het niveau van onderdeel en capaciteit.</span><span class="sxs-lookup"><span data-stu-id="2adc1-106">Update costs at the component and capacity levels.</span></span> <span data-ttu-id="2adc1-107">Zie voor meer informatie de batchverwerking **Vaste verrekenprijs artikel voorstellen**.</span><span class="sxs-lookup"><span data-stu-id="2adc1-107">For more information, see the **Suggest Item Standard Cost** batch job.</span></span>  
2.  <span data-ttu-id="2adc1-108">Het consolideren en berekenen van de materiaal- en capaciteitskosten om de totale productiekosten van de artikelen te berekenen.</span><span class="sxs-lookup"><span data-stu-id="2adc1-108">Consolidate and roll up the component and capacity costs to calculate the total manufacturing or assembly cost of the items.</span></span>  
3.  <span data-ttu-id="2adc1-109">De vaste verrekenprijzen implementeren die worden ingevoerd wanneer u de vorige batchverwerkingen uitvoert.</span><span class="sxs-lookup"><span data-stu-id="2adc1-109">Implement the standard costs that are entered when you run the previous batch jobs.</span></span> <span data-ttu-id="2adc1-110">De vaste verrekenprijzen worden pas van kracht nadat ze zijn geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="2adc1-110">The standard costs do not take effect until they are implemented.</span></span> <span data-ttu-id="2adc1-111">Zie voor meer informatie Vaste verrekenprijswijzigingen doorvoeren.</span><span class="sxs-lookup"><span data-stu-id="2adc1-111">For more information, see Implement Standard Cost Changes.</span></span>  
4.  <span data-ttu-id="2adc1-112">De wijzigingen implementeren om het veld **Kostprijs** op de artikelkaart bij te werken en voorraadherwaardering uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="2adc1-112">Implement the changes to update the **Unit Cost** field on the item card and perform inventory revaluation.</span></span> <span data-ttu-id="2adc1-113">Zie [Voorraad herwaarderen](inventory-how-revalue-inventory.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="2adc1-113">For more information, see [Revalue Inventory](inventory-how-revalue-inventory.md).</span></span>  

<span data-ttu-id="2adc1-114">Zie [Vaste verrekenprijs berekenen](finance-about-calculating-standard-cost.md) voor nadere informatie.</span><span class="sxs-lookup"><span data-stu-id="2adc1-114">For more information, see [About Calculating Standard Cost](finance-about-calculating-standard-cost.md).</span></span>  
## <a name="to-update-standard-costs"></a><span data-ttu-id="2adc1-115">Vaste verrekenprijs aanpassen</span><span class="sxs-lookup"><span data-stu-id="2adc1-115">To update standard costs</span></span>  
1.  <span data-ttu-id="2adc1-116">Voer de batchverwerking **Kostprijs herwaarderen - Artikelposten** uit.</span><span class="sxs-lookup"><span data-stu-id="2adc1-116">Run the **Adjust Cost-Item Entries** batch job.</span></span>  
2.  <span data-ttu-id="2adc1-117">Voer de batchverwerking **Voorraadwaarde boeken** uit.</span><span class="sxs-lookup"><span data-stu-id="2adc1-117">Run the **Post Inventory Cost to G/L** batch job.</span></span>  
3.  <span data-ttu-id="2adc1-118">Open het **Vaste-verrekenprijsvoorstel** en gebruik een of meer van de volgende functies:</span><span class="sxs-lookup"><span data-stu-id="2adc1-118">Open the **Standard Cost Worksheet** and use one or more of the following functions:</span></span>  

    1.  <span data-ttu-id="2adc1-119">Voer de batchverwerking **Vaste verrekenprijs artikel voorstellen** uit.</span><span class="sxs-lookup"><span data-stu-id="2adc1-119">Run the **Suggest Item Standard Cost** batch job.</span></span>  
    2.  <span data-ttu-id="2adc1-120">Bekijk de resultaten en breng desgewenst wijzigingen aan.</span><span class="sxs-lookup"><span data-stu-id="2adc1-120">Review the results and make changes as necessary.</span></span>  
    3.  <span data-ttu-id="2adc1-121">Voer de batchverwerking **Vaste verrekenprijs capaciteit voorstellen** uit.</span><span class="sxs-lookup"><span data-stu-id="2adc1-121">Run the **Suggest Capacity Standard Cost** batch job.</span></span>  
    4.  <span data-ttu-id="2adc1-122">Bekijk de resultaten en breng desgewenst wijzigingen aan.</span><span class="sxs-lookup"><span data-stu-id="2adc1-122">Review the results and make changes as necessary.</span></span>
    5. <span data-ttu-id="2adc1-123">Voer de batchverwerking **Vaste verrekenprijs berekenen** uit.</span><span class="sxs-lookup"><span data-stu-id="2adc1-123">Run the **Roll Up Standard Cost** batch job.</span></span>
    6.  <span data-ttu-id="2adc1-124">Bekijk de resultaten en breng desgewenst wijzigingen aan.</span><span class="sxs-lookup"><span data-stu-id="2adc1-124">Review the results and make changes as necessary.</span></span>
    7.  <span data-ttu-id="2adc1-125">Voer de batchverwerking **Vaste verrekenprijswijzigingen doorvoeren** uit.</span><span class="sxs-lookup"><span data-stu-id="2adc1-125">Run the **Implement Standard Cost Changes** batch job.</span></span>  
4.  <span data-ttu-id="2adc1-126">Bekijk en boek het venster **Herwaarderingsdagboek**, waarin de posten uit de vorige stappen in dit proces zijn ingevuld.</span><span class="sxs-lookup"><span data-stu-id="2adc1-126">Review and post the **Revaluation Journal** window, which has been populated with entries from the previous steps in this process.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2adc1-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2adc1-127">See Also</span></span>  
 <span data-ttu-id="2adc1-128">[Informatie over het berekenen van vaste verrekenprijzen](finance-about-calculating-standard-cost.md) </span><span class="sxs-lookup"><span data-stu-id="2adc1-128">[About Calculating Standard Cost](finance-about-calculating-standard-cost.md) </span></span>  
 <span data-ttu-id="2adc1-129">[Voorraadkosten beheren](finance-manage-inventory-costs.md) </span><span class="sxs-lookup"><span data-stu-id="2adc1-129">[Managing Inventory Costs](finance-manage-inventory-costs.md) </span></span>  
 <span data-ttu-id="2adc1-130">[Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md) [[Financiën](finance.md)</span><span class="sxs-lookup"><span data-stu-id="2adc1-130">[Design Details: Costing Methods](design-details-costing-methods.md) [[Finance](finance.md)</span></span>  
 <span data-ttu-id="2adc1-131">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2adc1-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

