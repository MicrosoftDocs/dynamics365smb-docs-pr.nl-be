---
title: Verzendmethoden instellen
description: U kunt een code instellen voor al uw aangeboden verzendmethoden en er gegevens over opgeven.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoterms
ms.date: 03/09/2021
ms.author: edupont
ms.openlocfilehash: 096b609d26ad24785f90634d725d751ac57b346e
ms.sourcegitcommit: 35f7e24c301926b39094aa64fe608afd04fdb8e1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573313"
---
# <a name="set-up-shipment-methods"></a><span data-ttu-id="1790c-103">Verzendmethoden instellen</span><span class="sxs-lookup"><span data-stu-id="1790c-103">Set Up Shipment Methods</span></span>

<span data-ttu-id="1790c-104">Verzendmethoden zijn vaak afhankelijk van de artikelen, klanten en leveranciers.</span><span class="sxs-lookup"><span data-stu-id="1790c-104">Shipment methods often depend on the items, the customers, and the vendors.</span></span> <span data-ttu-id="1790c-105">Een klant die op een eiland woont, zal aangeven dat artikelen altijd per vliegtuig of per boot moeten worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="1790c-105">For example, if the customer lives on an island, they can choose to have items always shipped by air or always by sea.</span></span> <span data-ttu-id="1790c-106">Sommige klanten kunnen levering op de volgende dag vereisen.</span><span class="sxs-lookup"><span data-stu-id="1790c-106">Some customers may require next day delivery.</span></span> <span data-ttu-id="1790c-107">Sommigen willen de order ophalen.</span><span class="sxs-lookup"><span data-stu-id="1790c-107">Some may want to pick up the order.</span></span> <span data-ttu-id="1790c-108">Op de klantenkaart en de leverancierskaart kunt u opgeven welke soort levering is gewenst.</span><span class="sxs-lookup"><span data-stu-id="1790c-108">On the customer and vendor cards, you can specify what sort of delivery is desired.</span></span>

<span data-ttu-id="1790c-109">U stelt de omschrijving en de code voor elke verzendmethode in op de pagina **Verzendwijze**.</span><span class="sxs-lookup"><span data-stu-id="1790c-109">You set up the description and code for each shipment method on the **Shipment Methods** page.</span></span> <span data-ttu-id="1790c-110">U kunt bijvoorbeeld de code FOB instellen en Free on Board invoeren in het veld **Omschrijving**.</span><span class="sxs-lookup"><span data-stu-id="1790c-110">For example, you can set up the code FOB, and enter Free on Board in the **Description** field.</span></span> <span data-ttu-id="1790c-111">Vervolgens kunt u de code invoeren in de velden **Code van verzendwijze**, elders in het systeem, bijvoorbeeld op een klantenkaart.</span><span class="sxs-lookup"><span data-stu-id="1790c-111">You can then enter the code in **Shipment Method Code** fields elsewhere in the system, such as on a customer card.</span></span> <span data-ttu-id="1790c-112">Als u vervolgens orders, facturen, creditnota's, enzovoort maakt, wordt automatisch de omschrijving ingevoerd die bij de code hoort.</span><span class="sxs-lookup"><span data-stu-id="1790c-112">Then when you create new orders, invoices, credit memos, and so on, the system will enter the description represented by the code.</span></span> <span data-ttu-id="1790c-113">U kunt het indien nodig in het document wijzigen.</span><span class="sxs-lookup"><span data-stu-id="1790c-113">You can change it on the document as needed.</span></span>

## <a name="to-set-up-a-shipment-method"></a><span data-ttu-id="1790c-114">Een verzendwijze instellen</span><span class="sxs-lookup"><span data-stu-id="1790c-114">To set up a shipment method</span></span>

1. <span data-ttu-id="1790c-115">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verzendmethoden** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="1790c-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Shipment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="1790c-116">Kies op de pagina **Verzendmethoden** de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="1790c-116">On the **Shipment Methods** page, choose the **New** action.</span></span>
3. <span data-ttu-id="1790c-117">Geef op de nieuwe regel een code en omschrijving op voor de verzendwijze.</span><span class="sxs-lookup"><span data-stu-id="1790c-117">On the new line, specify a code and description for the shipment method.</span></span>

> [!TIP]
> <span data-ttu-id="1790c-118">Als u Incoterms gebruikt, stelt u verzendmethoden in om de relevante Incoterms-regels weer te geven.</span><span class="sxs-lookup"><span data-stu-id="1790c-118">If you use Incoterms, set up shipment methods to represent the relevant Incoterms rules.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1790c-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1790c-119">See Also</span></span>

[<span data-ttu-id="1790c-120">Expediteurs instellen</span><span class="sxs-lookup"><span data-stu-id="1790c-120">Set Up Shipping Agents</span></span>](sales-how-to-set-up-shipping-agents.md)  
[<span data-ttu-id="1790c-121">Pakketten traceren</span><span class="sxs-lookup"><span data-stu-id="1790c-121">Track Packages</span></span>](sales-how-track-packages.md)  
[<span data-ttu-id="1790c-122">Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="1790c-122">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="1790c-123">Voorraad</span><span class="sxs-lookup"><span data-stu-id="1790c-123">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="1790c-124">Magazijnbeheer instellen</span><span class="sxs-lookup"><span data-stu-id="1790c-124">Setting Up Warehouse Management</span></span>](warehouse-setup-warehouse.md)  
[<span data-ttu-id="1790c-125">Assemblagebeheer</span><span class="sxs-lookup"><span data-stu-id="1790c-125">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="1790c-126">Ontwerpdetails: Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="1790c-126">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="1790c-127">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1790c-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="1790c-128">Incoterms op iccwbo.org</span><span class="sxs-lookup"><span data-stu-id="1790c-128">Incoterms on iccwbo.org</span></span>](https://iccwbo.org/resources-for-business/incoterms-rules)  

[!INCLUDE[footer-include](includes/footer-banner.md)]