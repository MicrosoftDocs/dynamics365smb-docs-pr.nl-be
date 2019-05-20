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
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: f4dc7b1f4f946e7b6e3772e84603169e3ace4af7
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250532"
---
# <a name="setup-best-practices-global-planning-setup"></a><span data-ttu-id="b2ac1-103">Aanbevolen procedures instellen: Instellen algemene planning</span><span class="sxs-lookup"><span data-stu-id="b2ac1-103">Setup Best Practices: Global Planning Setup</span></span>
<span data-ttu-id="b2ac1-104">Het sneltabblad **Planning** op de pagina **Productie-instellingen** bevat verschillende velden die de algemene regels voor de voorraadplanning definiëren.</span><span class="sxs-lookup"><span data-stu-id="b2ac1-104">The **Planning** FastTab on the **Manufacturing Setup** page contains several fields that define global rules for supply planning.</span></span>  

 <span data-ttu-id="b2ac1-105">De volgende tabel bevat de aanbevolen procedures voor het instellen van de geselecteerde globale planningparametervelden.</span><span class="sxs-lookup"><span data-stu-id="b2ac1-105">The following table provides best practices on how to set up selected global planning parameter fields.</span></span> <span data-ttu-id="b2ac1-106">Voor meer informatie over een veld, kiest u de koppeling in de kolom **Veld instellen**.</span><span class="sxs-lookup"><span data-stu-id="b2ac1-106">For more information about a field, choose the link in the **Setup field** column.</span></span>  

|<span data-ttu-id="b2ac1-107">Veld instellen</span><span class="sxs-lookup"><span data-stu-id="b2ac1-107">Setup field</span></span>|<span data-ttu-id="b2ac1-108">Aanbevolen procedure</span><span class="sxs-lookup"><span data-stu-id="b2ac1-108">Best practice</span></span>|<span data-ttu-id="b2ac1-109">Opmerking</span><span class="sxs-lookup"><span data-stu-id="b2ac1-109">Comment</span></span>|  
|-----------------|-------------------|-------------|  
|<span data-ttu-id="b2ac1-110">Prognose op vestigingen gebruiken</span><span class="sxs-lookup"><span data-stu-id="b2ac1-110">Use Forecast on Locations</span></span>|<span data-ttu-id="b2ac1-111">Selecteer als u prognoses hebt voor specifieke locaties.</span><span class="sxs-lookup"><span data-stu-id="b2ac1-111">Select if you have forecasts for specific locations.</span></span>||  
|<span data-ttu-id="b2ac1-112">Onderdelen op vestiging</span><span class="sxs-lookup"><span data-stu-id="b2ac1-112">Components at Location</span></span>|<span data-ttu-id="b2ac1-113">Als artikelen niet als SKU's zijn gedefinieerd, selecteert u de vestigingscode van het hoofdmagazijn.</span><span class="sxs-lookup"><span data-stu-id="b2ac1-113">If items are not defined as SKUs, select the location code of your main warehouse.</span></span>|<span data-ttu-id="b2ac1-114">Dit geldt ook als u alleen het inkoopvoorstel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b2ac1-114">This also applies if you only use the requisition worksheet.</span></span>|  
|<span data-ttu-id="b2ac1-115">Blanco-overflowniveau</span><span class="sxs-lookup"><span data-stu-id="b2ac1-115">Blank Overflow Level</span></span>|<span data-ttu-id="b2ac1-116">Selecteer **Standaardberekening toestaan** als u migreert van Microsoft Dynamics NAV 5.0 of eerder.</span><span class="sxs-lookup"><span data-stu-id="b2ac1-116">Select **Allow Default Calculation** if you are migrating from Microsoft Dynamics NAV 5.0 or earlier.</span></span>|<span data-ttu-id="b2ac1-117">Alleen gebruiken als u toestaat dat alle of sommige van uw objecten het bestelpunt overschrijden.</span><span class="sxs-lookup"><span data-stu-id="b2ac1-117">Use only if you want to allow all or some of your items to overflow the reorder point.</span></span>|  
|<span data-ttu-id="b2ac1-118">Standaard dempingsperiode</span><span class="sxs-lookup"><span data-stu-id="b2ac1-118">Default Dampener Period</span></span>|<span data-ttu-id="b2ac1-119">Ingesteld tussen 1D en 5D.</span><span class="sxs-lookup"><span data-stu-id="b2ac1-119">Set between 1D and 5D.</span></span><br /><br /> <span data-ttu-id="b2ac1-120">Indien planning in [!INCLUDE[d365fin](includes/d365fin_md.md)] nieuw is voor u stelt u een langere periode in.</span><span class="sxs-lookup"><span data-stu-id="b2ac1-120">If new to planning in [!INCLUDE[d365fin](includes/d365fin_md.md)], then set a longer period.</span></span>|<span data-ttu-id="b2ac1-121">Wanneer gebruikers meer vertrouwd zijn met de verschillende redenen voor planningsboodschappen, kort dan de dempingsperiode in om meer wijzigingssuggesties toe te staan.</span><span class="sxs-lookup"><span data-stu-id="b2ac1-121">When users are more familiar with the different reasons for action messages, then shorten the dampener period to allow more change suggestions.</span></span>|  
|<span data-ttu-id="b2ac1-122">Demping standaardhoeveelheid</span><span class="sxs-lookup"><span data-stu-id="b2ac1-122">Default Dampener Quantity</span></span>|<span data-ttu-id="b2ac1-123">Tussen 5 en 20 procent van de lotgrootte van het item instellen.</span><span class="sxs-lookup"><span data-stu-id="b2ac1-123">Set between 5 and 20 percent of the item’s lot size.</span></span>||  

## <a name="see-also"></a><span data-ttu-id="b2ac1-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b2ac1-124">See Also</span></span>  
 <span data-ttu-id="b2ac1-125">[Aanbevolen procedures instellen: Voorraadplanning](setup-best-practices-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="b2ac1-125">[Setup Best Practices: Supply Planning](setup-best-practices-supply-planning.md) </span></span>  
 <span data-ttu-id="b2ac1-126">[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="b2ac1-126">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
 [<span data-ttu-id="b2ac1-127">Complexe toepassingsgebieden instellen met aanbevolen procedures</span><span class="sxs-lookup"><span data-stu-id="b2ac1-127">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="b2ac1-128">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b2ac1-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
