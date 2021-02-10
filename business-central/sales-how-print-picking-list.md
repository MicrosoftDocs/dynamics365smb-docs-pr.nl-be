---
title: Een voorraadpicklijst vanuit een verkooporder afdrukken
description: U kunt een voorraadpicklijst rechtstreeks afdrukken vanuit een verkooporder, verkoop, factuur en andere uitgaande verkoopdocumenten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 47ae132d862d2c05bef4ea0d0af26688bdd16588
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758229"
---
# <a name="print-the-picking-list"></a><span data-ttu-id="c341a-103">De picklijst afdrukken</span><span class="sxs-lookup"><span data-stu-id="c341a-103">Print the Picking List</span></span>
<span data-ttu-id="c341a-104">U kunt een voorraadpicklijst rechtstreeks afdrukken vanuit een verkooporder, een verkoopfactuur of een ander document dat de verzending van artikelen initieert.</span><span class="sxs-lookup"><span data-stu-id="c341a-104">You can print an inventory picking list directly from a sales order, a sales invoice, or any other document that initiates shipment of items.</span></span>

<span data-ttu-id="c341a-105">Dit rapport wordt doorgaans gebruikt in bedrijven zonder speciale functionaliteit voor magazijnbeheer, zodat een voorraadmedewerker de picklijst eenvoudig kan bekijken of afdrukken vanuit het gerelateerde verkoopdocument.</span><span class="sxs-lookup"><span data-stu-id="c341a-105">This report is typically used in companies without dedicated functionality for warehouse management, so that an inventory worker can simply view or print the picking list from the related sales document.</span></span> <span data-ttu-id="c341a-106">In bedrijven met grotere volumes of complexere processen wordt picking gepland en uitgevoerd in speciale magazijndocumenten.</span><span class="sxs-lookup"><span data-stu-id="c341a-106">In companies with higher volume or more complex processes, picking is planned and performed in dedicated warehouse documents.</span></span> <span data-ttu-id="c341a-107">Zie [Artikelen picken](warehouse-pick-items.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c341a-107">For more information, see [Pick Items](warehouse-pick-items.md).</span></span>

## <a name="to-print-a-picking-list-from-a-sales-order"></a><span data-ttu-id="c341a-108">Een voorraadpicklijst vanuit een verkooporder afdrukken</span><span class="sxs-lookup"><span data-stu-id="c341a-108">To print a picking list from a sales order</span></span>  
<span data-ttu-id="c341a-109">De volgende procedure is gebaseerd op een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="c341a-109">The following procedure is based on a sales order.</span></span> <span data-ttu-id="c341a-110">De stappen zijn vergelijkbaar voor alle verkoopdocumenten die kunnen worden gebruikt om de verzending van artikelen te starten.</span><span class="sxs-lookup"><span data-stu-id="c341a-110">The steps are similar for all sales documents that can be used to initiate shipment of items.</span></span>

1. <span data-ttu-id="c341a-111">Kies het pictogram ![Pagina of rapport zoeken](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voer **Verkooporders** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="c341a-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c341a-112">Open de verkooporder waarvoor u artikelen wilt picken.</span><span class="sxs-lookup"><span data-stu-id="c341a-112">Open the sales order that you want to pick items for.</span></span>  
3. <span data-ttu-id="c341a-113">Kies de actie **Rapporteren** en kies vervolgens de actie **Picklijst per order**.</span><span class="sxs-lookup"><span data-stu-id="c341a-113">Choose the **Report** action, and then choose the **Picking List by Order** action.</span></span>  
4. <span data-ttu-id="c341a-114">Kies de knop **Afdrukken** om de picklijst af te drukken of kies de knop **Voorbeeld** om deze op het scherm weer te geven.</span><span class="sxs-lookup"><span data-stu-id="c341a-114">Choose the **Print** button to print the picking list or choose the **Preview** button to view it on the screen.</span></span>

<span data-ttu-id="c341a-115">U kunt de picklijst ook als document opslaan, bijvoorbeeld om naar iemand te sturen of als bijlage aan de verkooporder toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="c341a-115">You can also save the picking list as a document, for example, to send to someone or to add as an attachment to the sales order.</span></span> <span data-ttu-id="c341a-116">Zie voor meer informatie [Bijlagen, koppelingen en notities op kaarten en in documenten beheren](ui-how-add-link-to-record.md).</span><span class="sxs-lookup"><span data-stu-id="c341a-116">For more information, see [Manage Attachments, Links, and Notes on Cards and Documents](ui-how-add-link-to-record.md).</span></span>

> [!NOTE]
> <span data-ttu-id="c341a-117">Als u de functie **Stuklijst weergeven** in de klantorder hebt gebruikt, worden alleen de componenten van het gerelateerde assemblageartikel weergegeven in het rapport.</span><span class="sxs-lookup"><span data-stu-id="c341a-117">If you used the **Explode BOM** function on the sales order, then only the components of the related assembly item are shown in the report.</span></span> <span data-ttu-id="c341a-118">Zie [Werken met stuklijsten](inventory-how-work-BOMs.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c341a-118">For more information, see [Work with Bills of Material](inventory-how-work-BOMs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c341a-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c341a-119">See Also</span></span>  
[<span data-ttu-id="c341a-120">Voorraad</span><span class="sxs-lookup"><span data-stu-id="c341a-120">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="c341a-121">Artikelen picken</span><span class="sxs-lookup"><span data-stu-id="c341a-121">Pick Items</span></span>](warehouse-pick-items.md)  
<span data-ttu-id="c341a-122">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c341a-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>   
