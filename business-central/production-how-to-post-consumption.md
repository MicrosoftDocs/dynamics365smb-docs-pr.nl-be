---
title: Verbruik in batches boeken | Microsoft Docs
description: Als de afboekingsmethode **Handmatig** is, moet u de materialen handmatig boeken met behulp van een verbruiksdagboek.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b7799e652394e8b9b96a168c0cb8945ec332734e
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="batch-post-production-consumption"></a><span data-ttu-id="9e4a5-103">Productieverbruik in batches boeken</span><span class="sxs-lookup"><span data-stu-id="9e4a5-103">Batch Post Production Consumption</span></span>
<span data-ttu-id="9e4a5-104">Als de afboekingsmethode **Handmatig** is, moet u de materialen handmatig boeken met behulp van een verbruiksdagboek.</span><span class="sxs-lookup"><span data-stu-id="9e4a5-104">If the flushing method is **Manual**, you must post the components manually, using a consumption journal.</span></span>

<span data-ttu-id="9e4a5-105">U kunt het systeem ook zo instellen materialen automatisch worden geboekt (\*afgeboekt\*\*) als u productieorders start of voltooit.</span><span class="sxs-lookup"><span data-stu-id="9e4a5-105">You can also set the system up to automatically post (*flush*) components when you start or finish production orders.</span></span> <span data-ttu-id="9e4a5-106">Zie voor meer informatie [Afboeking van materialen op basis van de uitvoer van een bewerking inschakelen](production-how-to-flush-components-according-to-operation-output.md).</span><span class="sxs-lookup"><span data-stu-id="9e4a5-106">For more information, see [Enable Flushing of Components According to Operation Output](production-how-to-flush-components-according-to-operation-output.md).</span></span>

## <a name="to-post-consumption-for-one-or-more-production-order-lines"></a><span data-ttu-id="9e4a5-107">Verbruik boeken voor een of meer productieorderregels</span><span class="sxs-lookup"><span data-stu-id="9e4a5-107">To post consumption for one or more production order lines</span></span>  
1.  <span data-ttu-id="9e4a5-108">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verbruiksdagboek** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="9e4a5-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Consumption Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9e4a5-109">Voer in de velden informatie over de productieorder en verbruik in.</span><span class="sxs-lookup"><span data-stu-id="9e4a5-109">Fill in the fields with the production order data and the consumption data.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    <span data-ttu-id="9e4a5-110">Als het magazijn waar de materialen zijn opgeslagen opslaglocaties gebruikt, maar geen pickverwerking vereist, kunt u een opslaglocatie toewijzen aan de dagboekregel om aan te geven waar de artikelen uit het magazijn moeten worden gehaald.</span><span class="sxs-lookup"><span data-stu-id="9e4a5-110">If the warehouse location where the components are stored is set up to use bins but does not require pick processing, assign a bin code to the journal line to indicate where the items should be taken from in the warehouse.</span></span> <span data-ttu-id="9e4a5-111">Zie [Picken voor productie of assemblage](warehouse-how-to-pick-for-production.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="9e4a5-111">For more information, see [Pick for Production or Assembly](warehouse-how-to-pick-for-production.md).</span></span>  
3.  <span data-ttu-id="9e4a5-112">Kies de actie **Boeken** om het verbruik te boeken.</span><span class="sxs-lookup"><span data-stu-id="9e4a5-112">Choose the **Post** action to post the consumption.</span></span> <span data-ttu-id="9e4a5-113">De betreffende artikelposten worden verminderd.</span><span class="sxs-lookup"><span data-stu-id="9e4a5-113">The related item ledger entries are reduced.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e4a5-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9e4a5-114">See Also</span></span>  
<span data-ttu-id="9e4a5-115">[Productie](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="9e4a5-115">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="9e4a5-116">Productie instellen</span><span class="sxs-lookup"><span data-stu-id="9e4a5-116">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="9e4a5-117">[Gepland](production-planning.md)    </span><span class="sxs-lookup"><span data-stu-id="9e4a5-117">[Planning](production-planning.md)    </span></span>  
[<span data-ttu-id="9e4a5-118">Voorraad</span><span class="sxs-lookup"><span data-stu-id="9e4a5-118">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="9e4a5-119">Inkoop</span><span class="sxs-lookup"><span data-stu-id="9e4a5-119">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="9e4a5-120">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9e4a5-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

