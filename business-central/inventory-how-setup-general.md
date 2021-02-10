---
title: Algemene voorraadinstellingen definiëren
description: Beschrijft hoe u de algemene voorraadinstellingen definieert, zodat u uw magazijn en voorraad kunt beheren.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e3ecf8d206e50244c19a820bdb67d2992cbefe36
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746378"
---
# <a name="set-up-general-inventory-information"></a><span data-ttu-id="d11e8-103">Algemene voorraadgegevens instellen</span><span class="sxs-lookup"><span data-stu-id="d11e8-103">Set Up General Inventory Information</span></span>

<span data-ttu-id="d11e8-104">U geeft uw algemene voorraadinstellingen op de pagina **Voorraadinstelling** op.</span><span class="sxs-lookup"><span data-stu-id="d11e8-104">You specify your general inventory setup on the **Inventory Setup** page.</span></span>

## <a name="to-set-up-general-inventory-information"></a><span data-ttu-id="d11e8-105">Algemene voorraadgegevens instellen</span><span class="sxs-lookup"><span data-stu-id="d11e8-105">To set up general inventory information</span></span>

1. <span data-ttu-id="d11e8-106">Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraad instellen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="d11e8-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="d11e8-107">Vul op de pagina **Voorraadinstelling** de benodigde velden in.</span><span class="sxs-lookup"><span data-stu-id="d11e8-107">On the **Inventory Setup** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="d11e8-108">Voor gedetailleerde informatie over de kostprijsvelden **Autom. voorraadwaarde boeken**, **Verw. kostprijs naar GB boeken** en **Standaardwaarderingsmethode** raadpleegt u [Voorraadkosten afstemmen op grootboek](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md) en [Ontwerpdetails: Verwachte kostenboeking](design-details-expected-cost-posting.md).</span><span class="sxs-lookup"><span data-stu-id="d11e8-108">For detailed information about the costing fields, **Automatic Cost Posting**, **Expected Cost Posting to G/L**, and **Default Costing Method**, see [Reconcile Inventory Costs with the General Ledger](finance-how-to-post-inventory-costs-to-the-general-ledger.md), [Design Details: Inventory Costing](design-details-inventory-costing.md), and [Design Details: Expected Cost Posting](design-details-expected-cost-posting.md).</span></span> <span data-ttu-id="d11e8-109">Zie voor meer informatie over kostprijsberekening in het algemeen [Voorraadkosten beheren](finance-manage-inventory-costs.md).</span><span class="sxs-lookup"><span data-stu-id="d11e8-109">For more information about costing in general, see [Managing Inventory Costs](finance-manage-inventory-costs.md).</span></span>  

<span data-ttu-id="d11e8-110">Als u een inslagtijd wilt instellen voor de berekening van de ordertoezegging op de inkoopregel, kunt u deze instellen als standaardwaarde voor de voorraad, op de pagina **Voorraadinstellingen**, en de vestiging.</span><span class="sxs-lookup"><span data-stu-id="d11e8-110">If you want to include warehouse handling time in the order promising calculation on the purchase line, you can set it up as a default for the inventory, on the **Inventory Setup** page, and for your location.</span></span> <span data-ttu-id="d11e8-111">Zie voor meer informatie [Ordertoezeggingsdatums berekenen](sales-how-to-calculate-order-promising-dates.md).</span><span class="sxs-lookup"><span data-stu-id="d11e8-111">For more information, see [Calculate Order Promising Dates](sales-how-to-calculate-order-promising-dates.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="d11e8-112">De schakelaar **Automatische kostenaanpassing** is standaard ingeschakeld om ervoor te zorgen dat voorraadwaarden altijd correct zijn in het grootboek, waardoor uw verkoop- en winststatistieken up-to-date blijven.</span><span class="sxs-lookup"><span data-stu-id="d11e8-112">The **Automatic Cost Adjustment** toggle is turned on by default to ensure that inventory values are always correct in the general ledger, which in turn keeps your sales and profit statistics up to date.</span></span> <span data-ttu-id="d11e8-113">Kostenwijzigingen vanuit inkomende posten, zoals voor inkopen of productie-output, worden toegewezen aan de bijbehorende uitgaande posten, zoals verkopen of transfers.</span><span class="sxs-lookup"><span data-stu-id="d11e8-113">Cost changes from inbound entries, such as those for purchases or production output, are assigned to the related outbound entries, such as sales or transfers.</span></span> <span data-ttu-id="d11e8-114">Dit is handig voor nieuwe [!INCLUDE[prod_short](includes/prod_short.md)]-klanten en kleine bedrijven met relatief lage voorraadtransactieniveaus.</span><span class="sxs-lookup"><span data-stu-id="d11e8-114">This is helpful for new [!INCLUDE[prod_short](includes/prod_short.md)] customers and small businesses with relatively low inventory transaction levels.</span></span> <span data-ttu-id="d11e8-115">Als een bedrijf echter groeit en de voorraadniveaus toenemen, kan dit de systeemprestaties vertragen.</span><span class="sxs-lookup"><span data-stu-id="d11e8-115">However, as a business grows and inventory levels increase, this can slow down system performance.</span></span> <span data-ttu-id="d11e8-116">Om verminderde prestaties tijdens het boeken te minimaliseren, selecteert u een tijdoptie om te definiëren hoe ver terug in de tijd vanaf de werkdatum een inkomende transactie kan plaatsvinden om mogelijk een aanpassing van gerelateerde uitgaande waardeposten te activeren.</span><span class="sxs-lookup"><span data-stu-id="d11e8-116">To minimize reduced performance during posting, select a time option to define how far back in time from the work date an inbound transaction can occur to potentially trigger adjustment of related outbound value entries.</span></span> <span data-ttu-id="d11e8-117">Als alternatief kunt u de kosten met regelmatige tussenpozen handmatig aanpassen met de batchverwerking Kostprijs herwaarderen - Artikelposten.</span><span class="sxs-lookup"><span data-stu-id="d11e8-117">Alternatively, you can manually adjust costs at regular intervals with the Adjust Cost - Item Entries batch job.</span></span>

## <a name="see-also"></a><span data-ttu-id="d11e8-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d11e8-118">See Also</span></span>
[<span data-ttu-id="d11e8-119">Voorraad instellen</span><span class="sxs-lookup"><span data-stu-id="d11e8-119">Set Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="d11e8-120">[Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md)  </span><span class="sxs-lookup"><span data-stu-id="d11e8-120">[Design Details: Costing Methods](design-details-costing-methods.md)  </span></span>  
[<span data-ttu-id="d11e8-121">Voorraad beheren</span><span class="sxs-lookup"><span data-stu-id="d11e8-121">Manage Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="d11e8-122">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d11e8-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="d11e8-123">Wijzigen welke functies worden weergegeven</span><span class="sxs-lookup"><span data-stu-id="d11e8-123">Change Which Features are Displayed</span></span>](ui-experiences.md)  
[<span data-ttu-id="d11e8-124">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="d11e8-124">General Business Functionality</span></span>](ui-across-business-areas.md)
