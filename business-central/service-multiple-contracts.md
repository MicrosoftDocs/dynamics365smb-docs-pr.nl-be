---
title: Meervoudige contracten | Microsoft Docs
description: Afhankelijk van uw serviceovereenkomst met een klant, moet u een serviceartikel mogelijk verwerken onder meer dan één servicecontract.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 13c641512a0e3e2722460daa238d12c0162ad8b6
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389686"
---
# <a name="multiple-contracts"></a><span data-ttu-id="3e0cc-103">Meervoudige contracten</span><span class="sxs-lookup"><span data-stu-id="3e0cc-103">Multiple Contracts</span></span>
<span data-ttu-id="3e0cc-104">Afhankelijk van uw serviceovereenkomst met een klant, moet u een serviceartikel mogelijk verwerken onder meer dan één servicecontract.</span><span class="sxs-lookup"><span data-stu-id="3e0cc-104">Depending on your service level agreements with a customer, you may have to handle a service item under more than one service contract.</span></span>  
  
<span data-ttu-id="3e0cc-105">Bij de verwerking van een serviceartikel onder meerdere contracten, kunt u het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="3e0cc-105">By handling a service item under multiple contracts, you can do the following:</span></span>  
  
* <span data-ttu-id="3e0cc-106">Verschillende contracten verzenden voor hetzelfde serviceartikel.</span><span class="sxs-lookup"><span data-stu-id="3e0cc-106">Issue different contracts for the same service item.</span></span>  
* <span data-ttu-id="3e0cc-107">Onderdelen afzonderlijk onderhouden.</span><span class="sxs-lookup"><span data-stu-id="3e0cc-107">Service parts separately.</span></span>  
* <span data-ttu-id="3e0cc-108">Rekening houden met verschillende bekwaamheden die vereist zijn voor het uitvoeren van onderhoud op verschillende aspecten van een serviceartikel, zoals mechanische componenten en software.</span><span class="sxs-lookup"><span data-stu-id="3e0cc-108">Consider different skills that are required to service different aspects of a service item, such as mechanical components and software.</span></span>  
* <span data-ttu-id="3e0cc-109">Verschillende responstijden en frequenties opgeven voor het onderhoud van verschillende delen van een serviceartikel.</span><span class="sxs-lookup"><span data-stu-id="3e0cc-109">Specify different response times and frequencies in servicing different parts of a service item.</span></span>  
* <span data-ttu-id="3e0cc-110">Rekening houden met verschillende soorten activiteiten die op een serviceartikel moeten worden uitgevoerd, wanneer er voor het serviceartikel verschillende soorten onderhoud nodig zijn in verschillende perioden.</span><span class="sxs-lookup"><span data-stu-id="3e0cc-110">Address different kinds of activities to be performed on a service item when the service item requires different types of service in different time periods.</span></span>  
* <span data-ttu-id="3e0cc-111">Een relevant contractnummer selecteren en toewijzen aan een serviceartikelregel als u een serviceorder maakt.</span><span class="sxs-lookup"><span data-stu-id="3e0cc-111">Select and assign an appropriate contract number to a service item line when you are creating a service order.</span></span>  
* <span data-ttu-id="3e0cc-112">Relevante financiële informatie verwerken met betrekking tot serviceartikelen en serviceovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="3e0cc-112">Handle relevant financial information about service items and service level agreements.</span></span>  
  
<span data-ttu-id="3e0cc-113">Bij het gebruik van meervoudige contracten kunt u de volgende voorbeelden in aanmerking nemen.</span><span class="sxs-lookup"><span data-stu-id="3e0cc-113">You can consider the following examples of using the multiple contracts functionality.</span></span>  
  
## <a name="creating-multiple-contracts-per-service-item"></a><span data-ttu-id="3e0cc-114">Meervoudige contracten maken per serviceartikel</span><span class="sxs-lookup"><span data-stu-id="3e0cc-114">Creating Multiple Contracts per Service Item</span></span>  
<span data-ttu-id="3e0cc-115">U kunt handmatig een servicecontract of servicecontractofferte maken voor serviceartikelen die al zijn geregistreerd in niet-geannuleerde contracten van dezelfde klant.</span><span class="sxs-lookup"><span data-stu-id="3e0cc-115">You can manually create a service contract or contract quote for service items already registered in non-canceled contracts owned by the same customer.</span></span> <span data-ttu-id="3e0cc-116">Hiervoor volgt u de standaardprocedure voor het maken van servicecontracten en servicecontractoffertes.</span><span class="sxs-lookup"><span data-stu-id="3e0cc-116">To do this, follow the standard procedure of creating service contracts and service contract quotes.</span></span> <span data-ttu-id="3e0cc-117">Zie voor meer informatie [Werken met servicecontracten en servicecontractoffertes](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span><span class="sxs-lookup"><span data-stu-id="3e0cc-117">For more information, see [Work with Service Contracts and Service Contract Quotes](service-how-to-create-service-contracts-and-service-contract-quotes.md).</span></span>  
  
<span data-ttu-id="3e0cc-118">Als u op een contractregel een serviceartikel toevoegt dat is geregistreerd in andere servicecontracten of servicecontractoffertes, wordt een bericht weergegeven met de waarschuwing dat het serviceartikel al hoort bij een of meer servicecontracten of servicecontractoffertes.</span><span class="sxs-lookup"><span data-stu-id="3e0cc-118">When you add a service item on a contract line that is registered in other service contracts or contract quotes, a warning message is displayed stating that the service item already belongs to one or more service contracts or contract quotes.</span></span> <span data-ttu-id="3e0cc-119">Als u dit bericht bevestigt, wordt alle relevante informatie over het serviceartikel gekopieerd naar een nieuwe contractregel.</span><span class="sxs-lookup"><span data-stu-id="3e0cc-119">If you confirm this message, all relevant service item information is copied to a newly created contract line.</span></span>  
  
## <a name="copying-documents"></a><span data-ttu-id="3e0cc-120">Documenten kopiëren</span><span class="sxs-lookup"><span data-stu-id="3e0cc-120">Copying Documents</span></span>  
<span data-ttu-id="3e0cc-121">Met de actie **Kopiëren uit document** kunt u automatisch een servicecontract of contractofferte maken voor serviceartikelen die al zijn geregistreerd in andere servicecontracten of contractoffertes.</span><span class="sxs-lookup"><span data-stu-id="3e0cc-121">You can automatically create a service contract or contract quote for service items that are already registered in other service contracts or contract quotes by using the **Copy from Document** action.</span></span>  
  
## <a name="creating-service-orders-for-multiple-contracts"></a><span data-ttu-id="3e0cc-122">Serviceorders maken voor meervoudige contracten</span><span class="sxs-lookup"><span data-stu-id="3e0cc-122">Creating Service Orders for Multiple Contracts</span></span>  
<span data-ttu-id="3e0cc-123">U kunt handmatig een serviceorder maken voor een serviceartikel dat is geregistreerd in meervoudige actieve contracten.</span><span class="sxs-lookup"><span data-stu-id="3e0cc-123">You can manually create a service order for a service item that is registered in multiple active contracts.</span></span> <span data-ttu-id="3e0cc-124">Een servicecontract is actief als het is ondertekend en niet is verlopen.</span><span class="sxs-lookup"><span data-stu-id="3e0cc-124">A service contract is active when it is signed and not expired.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e0cc-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3e0cc-125">See Also</span></span>  
[<span data-ttu-id="3e0cc-126">Servicecontracten voldoen</span><span class="sxs-lookup"><span data-stu-id="3e0cc-126">Fulfilling Service Contracts</span></span>](service-fulfill-service-contracts.md)  
[<span data-ttu-id="3e0cc-127">Serviceorders maken</span><span class="sxs-lookup"><span data-stu-id="3e0cc-127">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]