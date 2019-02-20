---
title: Ontwerpdetails - Artikeltracering in het magazijn | Microsoft Docs
description: De verwerking van serie- en lotnummers is hoofdzakelijk een magazijntaak. Daarom hebben alle inkomende en uitgaande magazijndocumenten standaardfunctionaliteit voor het toewijzen en selecteren van artikeltraceringsnummers. Omdat het reserveringsysteem echter op artikelposten is gebaseerd, worden magazijnactiviteitsdocumenten die alleen magazijnposten registreren, niet volledig ondersteund.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 01/15/2019
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 5d6d2d9527e81a92987f6b8fcdbe8e087c3c537a
ms.openlocfilehash: e780dba122374bd80e48ca6bbc74b7540e034ac6
ms.contentlocale: nl-be
ms.lasthandoff: 01/22/2019

---
# <a name="design-details-item-tracking-in-the-warehouse"></a><span data-ttu-id="e7938-104">Ontwerpdetails: Artikeltracering in het magazijn</span><span class="sxs-lookup"><span data-stu-id="e7938-104">Design Details: Item Tracking in the Warehouse</span></span>
<span data-ttu-id="e7938-105">De verwerking van serie- en lotnummers is hoofdzakelijk een magazijntaak. Daarom hebben alle inkomende en uitgaande magazijndocumenten standaardfunctionaliteit voor het toewijzen en selecteren van artikeltraceringsnummers.</span><span class="sxs-lookup"><span data-stu-id="e7938-105">Serial number and lot number handling is primarily a warehouse task and therefore all inbound and outbound warehouse documents have standard functionality for assigning and selecting item tracking numbers.</span></span>  

<span data-ttu-id="e7938-106">Omdat het reserveringsysteem echter op artikelposten is gebaseerd, worden magazijnactiviteitsdocumenten die alleen magazijnposten registreren, niet volledig ondersteund.</span><span class="sxs-lookup"><span data-stu-id="e7938-106">However, because the reservation system is based on item ledger entries, warehouse activity documents that register only warehouse entries are not fully supported.</span></span> <span data-ttu-id="e7938-107">Omdat reserveringen en artikeltraceringsnummers alleen op locatieniveau kunnen worden verwerkt, en niet op het niveau van de opslaglocatie en de zone, kan de pagina **Artikeltraceringsregels** niet worden geopend vanuit magazijnactiviteitsdocumenten.</span><span class="sxs-lookup"><span data-stu-id="e7938-107">Because reservations and item tracking numbers can be handled only at the location level, not at the bin and zone level, the **Item Tracking Lines** page cannot be opened from warehouse activity documents.</span></span> <span data-ttu-id="e7938-108">Hetzelfde geldt voor de pagina **Reservering**.</span><span class="sxs-lookup"><span data-stu-id="e7938-108">The same applies to the **Reservation** page.</span></span>  

<span data-ttu-id="e7938-109">Nadat een serienummer of lotnummer is toegevoegd aan een artikel op een magazijnlocatie, kan het vrijelijk binnen het magazijn worden verplaatst en geherclassificeerd met behulp van een onafhankelijke artikeltraceringstructuur die niet gerelateerd is aan het reserveringsysteem.</span><span class="sxs-lookup"><span data-stu-id="e7938-109">After a serial or lot number has been added to an item at a warehouse location, it can be moved and reclassified freely within the warehouse by using an independent item tracking structure that is unrelated to the reservation system.</span></span> <span data-ttu-id="e7938-110">De velden **Serienummer** en **Lotnr.** zijn rechtstreeks toegankelijk op magazijndocumentregels.</span><span class="sxs-lookup"><span data-stu-id="e7938-110">**Serial No.** and **Lot No.** fields are accessed directly on warehouse document lines.</span></span> <span data-ttu-id="e7938-111">Wanneer het serie- of lotnummer later wordt gebruikt bij uitgaande posten, wordt het gesynchroniseerd met het reserveringssysteem als onderdeel van de normale opslaglocatieherwaardering.</span><span class="sxs-lookup"><span data-stu-id="e7938-111">When the serial or lot number later partakes in outbound posting, it is synchronized with the reservation system as a part of ordinary bin adjustment.</span></span> <span data-ttu-id="e7938-112">Zie [Ontwerpdetails: Integratie met voorraad](design-details-integration-with-inventory.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e7938-112">For more information, see [Design Details: Integration with Inventory](design-details-integration-with-inventory.md).</span></span>  

<span data-ttu-id="e7938-113">Het reserveringsysteem houdt echter rekening met magazijnactiviteiten wanneer beschikbaarheid wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="e7938-113">However, the reservation system does take warehouse activities into consideration when it calculates availability.</span></span> <span data-ttu-id="e7938-114">Artikelen die zijn toegewezen aan picks, of zijn geregistreerd als gepickt, kunnen bijvoorbeeld niet worden gereserveerd.</span><span class="sxs-lookup"><span data-stu-id="e7938-114">For example, items that are allocated to picks, or registered as picked, cannot be reserved.</span></span> <span data-ttu-id="e7938-115">Zie voor meer informatie [Ontwerpdetails: Magazijnbeschikbaarheid](design-details-availability-in-the-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="e7938-115">For more information, see [Design Details: Warehouse Availability](design-details-availability-in-the-warehouse.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e7938-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e7938-116">See Also</span></span>  
[<span data-ttu-id="e7938-117">Ontwerpdetails: Artikeltracering</span><span class="sxs-lookup"><span data-stu-id="e7938-117">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)  
[<span data-ttu-id="e7938-118">Ontwerpdetails: Integratie met voorraad</span><span class="sxs-lookup"><span data-stu-id="e7938-118">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)  
[<span data-ttu-id="e7938-119">Ontwerpdetails: Magazijnbeschikbaarheid</span><span class="sxs-lookup"><span data-stu-id="e7938-119">Design Details: Warehouse Availability</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="e7938-120">Ontwerpdetails: Ontwerp artikeltracering</span><span class="sxs-lookup"><span data-stu-id="e7938-120">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)

