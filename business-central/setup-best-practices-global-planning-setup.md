---
title: Aanbevolen procedures voor instellen van algemene planning | Microsoft Docs
description: Het sneltabblad Planning op de pagina Productie-instellingen bevat verschillende velden die de algemene regels voor de voorraadplanning definiëren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3f70e720cd8639038f7c06de7f6b2f338652e8e4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757779"
---
# <a name="setup-best-practices-global-planning-setup"></a><span data-ttu-id="d76f5-103">Aanbevolen procedures instellen: Instellen algemene planning</span><span class="sxs-lookup"><span data-stu-id="d76f5-103">Setup Best Practices: Global Planning Setup</span></span>
<span data-ttu-id="d76f5-104">Het sneltabblad **Planning** op de pagina **Productie-instellingen** bevat verschillende velden die de algemene regels voor de voorraadplanning definiëren.</span><span class="sxs-lookup"><span data-stu-id="d76f5-104">The **Planning** FastTab on the **Manufacturing Setup** page contains several fields that define global rules for supply planning.</span></span>  

 <span data-ttu-id="d76f5-105">De volgende tabel bevat de aanbevolen procedures voor het instellen van de geselecteerde globale planningparametervelden.</span><span class="sxs-lookup"><span data-stu-id="d76f5-105">The following table provides best practices on how to set up selected global planning parameter fields.</span></span> <span data-ttu-id="d76f5-106">Voor meer informatie over een veld, kiest u de koppeling in de kolom **Veld instellen**.</span><span class="sxs-lookup"><span data-stu-id="d76f5-106">For more information about a field, choose the link in the **Setup field** column.</span></span>  

|<span data-ttu-id="d76f5-107">Veld instellen</span><span class="sxs-lookup"><span data-stu-id="d76f5-107">Setup field</span></span>|<span data-ttu-id="d76f5-108">Aanbevolen procedure</span><span class="sxs-lookup"><span data-stu-id="d76f5-108">Best practice</span></span>|<span data-ttu-id="d76f5-109">Opmerking</span><span class="sxs-lookup"><span data-stu-id="d76f5-109">Comment</span></span>|  
|-----------------|-------------------|-------------|  
|<span data-ttu-id="d76f5-110">Prognose op vestigingen gebruiken</span><span class="sxs-lookup"><span data-stu-id="d76f5-110">Use Forecast on Locations</span></span>|<span data-ttu-id="d76f5-111">Selecteer als u prognoses hebt voor specifieke locaties.</span><span class="sxs-lookup"><span data-stu-id="d76f5-111">Select if you have forecasts for specific locations.</span></span>||  
|<span data-ttu-id="d76f5-112">Onderdelen op vestiging</span><span class="sxs-lookup"><span data-stu-id="d76f5-112">Components at Location</span></span>|<span data-ttu-id="d76f5-113">Als artikelen niet als SKU's zijn gedefinieerd, selecteert u de vestigingscode van het hoofdmagazijn.</span><span class="sxs-lookup"><span data-stu-id="d76f5-113">If items are not defined as SKUs, select the location code of your main warehouse.</span></span>|<span data-ttu-id="d76f5-114">Dit geldt ook als u alleen het inkoopvoorstel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d76f5-114">This also applies if you only use the requisition worksheet.</span></span>|  
|<span data-ttu-id="d76f5-115">Blanco-overflowniveau</span><span class="sxs-lookup"><span data-stu-id="d76f5-115">Blank Overflow Level</span></span>|<span data-ttu-id="d76f5-116">Selecteer **Standaardberekening toestaan** als u migreert van Microsoft Dynamics NAV 5.0 of eerder.</span><span class="sxs-lookup"><span data-stu-id="d76f5-116">Select **Allow Default Calculation** if you are migrating from Microsoft Dynamics NAV 5.0 or earlier.</span></span>|<span data-ttu-id="d76f5-117">Alleen gebruiken als u toestaat dat alle of sommige van uw objecten het bestelpunt overschrijden.</span><span class="sxs-lookup"><span data-stu-id="d76f5-117">Use only if you want to allow all or some of your items to overflow the reorder point.</span></span>|  
|<span data-ttu-id="d76f5-118">Standaard dempingsperiode</span><span class="sxs-lookup"><span data-stu-id="d76f5-118">Default Dampener Period</span></span>|<span data-ttu-id="d76f5-119">Ingesteld tussen 1D en 5D.</span><span class="sxs-lookup"><span data-stu-id="d76f5-119">Set between 1D and 5D.</span></span><br /><br /> <span data-ttu-id="d76f5-120">Indien planning in [!INCLUDE[prod_short](includes/prod_short.md)] nieuw is voor u stelt u een langere periode in.</span><span class="sxs-lookup"><span data-stu-id="d76f5-120">If new to planning in [!INCLUDE[prod_short](includes/prod_short.md)], then set a longer period.</span></span>|<span data-ttu-id="d76f5-121">Wanneer gebruikers meer vertrouwd zijn met de verschillende redenen voor planningsboodschappen, kort dan de dempingsperiode in om meer wijzigingssuggesties toe te staan.</span><span class="sxs-lookup"><span data-stu-id="d76f5-121">When users are more familiar with the different reasons for action messages, then shorten the dampener period to allow more change suggestions.</span></span>|  
|<span data-ttu-id="d76f5-122">Demping standaardhoeveelheid %</span><span class="sxs-lookup"><span data-stu-id="d76f5-122">Default Dampener Quantity %</span></span>|<span data-ttu-id="d76f5-123">Tussen 5 en 20 procent van de lotgrootte van het item instellen.</span><span class="sxs-lookup"><span data-stu-id="d76f5-123">Set between 5 and 20 percent of the item’s lot size.</span></span>||  

## <a name="see-also"></a><span data-ttu-id="d76f5-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d76f5-124">See Also</span></span>  
 <span data-ttu-id="d76f5-125">[Aanbevolen procedures instellen: Voorraadplanning](setup-best-practices-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="d76f5-125">[Setup Best Practices: Supply Planning](setup-best-practices-supply-planning.md) </span></span>  
 <span data-ttu-id="d76f5-126">[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="d76f5-126">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
 [<span data-ttu-id="d76f5-127">Complexe toepassingsgebieden instellen met aanbevolen procedures</span><span class="sxs-lookup"><span data-stu-id="d76f5-127">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="d76f5-128">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d76f5-128">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
