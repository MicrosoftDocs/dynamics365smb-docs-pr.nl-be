---
title: Aanbevolen procedures voor instellen van algemene planning | Microsoft Docs
description: "Het sneltabblad **Planning** in het venster **Productie-instellingen** bevat verschillende velden die de algemene regels voor de voorraadplanning definiëren."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f1a4e3a30d4d665a83ab599ad19dfd3760d744b2
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="setup-best-practices-global-planning-setup"></a><span data-ttu-id="46c99-103">Aanbevolen procedures instellen: Instellen algemene planning</span><span class="sxs-lookup"><span data-stu-id="46c99-103">Setup Best Practices: Global Planning Setup</span></span>
<span data-ttu-id="46c99-104">Het sneltabblad **Planning** in het venster **Productie-instellingen** bevat verschillende velden die de algemene regels voor de voorraadplanning definiëren.</span><span class="sxs-lookup"><span data-stu-id="46c99-104">The **Planning** FastTab in the **Manufacturing Setup** window contains several fields that define global rules for supply planning.</span></span>  

 <span data-ttu-id="46c99-105">De volgende tabel bevat de aanbevolen procedures voor het instellen van de geselecteerde globale planningparametervelden.</span><span class="sxs-lookup"><span data-stu-id="46c99-105">The following table provides best practices on how to set up selected global planning parameter fields.</span></span> <span data-ttu-id="46c99-106">Voor meer informatie over een veld, kiest u de koppeling in de kolom **Veld instellen**.</span><span class="sxs-lookup"><span data-stu-id="46c99-106">For more information about a field, choose the link in the **Setup field** column.</span></span>  

|<span data-ttu-id="46c99-107">Veld instellen</span><span class="sxs-lookup"><span data-stu-id="46c99-107">Setup field</span></span>|<span data-ttu-id="46c99-108">Aanbevolen procedure</span><span class="sxs-lookup"><span data-stu-id="46c99-108">Best practice</span></span>|<span data-ttu-id="46c99-109">Opmerking</span><span class="sxs-lookup"><span data-stu-id="46c99-109">Comment</span></span>|  
|-----------------|-------------------|-------------|  
|<span data-ttu-id="46c99-110">Prognose op vestigingen gebruiken</span><span class="sxs-lookup"><span data-stu-id="46c99-110">Use Forecast on Locations</span></span>|<span data-ttu-id="46c99-111">Selecteer als u prognoses hebt voor specifieke locaties.</span><span class="sxs-lookup"><span data-stu-id="46c99-111">Select if you have forecasts for specific locations.</span></span>||  
|<span data-ttu-id="46c99-112">Onderdelen op vestiging</span><span class="sxs-lookup"><span data-stu-id="46c99-112">Components at Location</span></span>|<span data-ttu-id="46c99-113">Als artikelen niet als SKU's zijn gedefinieerd, selecteert u de vestigingscode van het hoofdmagazijn.</span><span class="sxs-lookup"><span data-stu-id="46c99-113">If items are not defined as SKUs, select the location code of your main warehouse.</span></span>|<span data-ttu-id="46c99-114">Dit geldt ook als u alleen het inkoopvoorstel gebruikt.</span><span class="sxs-lookup"><span data-stu-id="46c99-114">This also applies if you only use the requisition worksheet.</span></span>|  
|<span data-ttu-id="46c99-115">Blanco-overflowniveau</span><span class="sxs-lookup"><span data-stu-id="46c99-115">Blank Overflow Level</span></span>|<span data-ttu-id="46c99-116">Selecteer **Standaardberekening toestaan** als u migreert van Microsoft Dynamics NAV 5.0 of eerder.</span><span class="sxs-lookup"><span data-stu-id="46c99-116">Select **Allow Default Calculation** if you are migrating from Microsoft Dynamics NAV 5.0 or earlier.</span></span>|<span data-ttu-id="46c99-117">Alleen gebruiken als u toestaat dat alle of sommige van uw objecten het bestelpunt overschrijden.</span><span class="sxs-lookup"><span data-stu-id="46c99-117">Use only if you want to allow all or some of your items to overflow the reorder point.</span></span>|  
|<span data-ttu-id="46c99-118">Standaard dempingsperiode</span><span class="sxs-lookup"><span data-stu-id="46c99-118">Default Dampener Period</span></span>|<span data-ttu-id="46c99-119">Ingesteld tussen 1D en 5D.</span><span class="sxs-lookup"><span data-stu-id="46c99-119">Set between 1D and 5D.</span></span><br /><br /> <span data-ttu-id="46c99-120">Indien planning in [!INCLUDE[d365fin](includes/d365fin_md.md)] nieuw is voor u stelt u een langere periode in.</span><span class="sxs-lookup"><span data-stu-id="46c99-120">If new to planning in [!INCLUDE[d365fin](includes/d365fin_md.md)], then set a longer period.</span></span>|<span data-ttu-id="46c99-121">Wanneer gebruikers meer vertrouwd zijn met de verschillende redenen voor planningsboodschappen, kort dan de dempingsperiode in om meer wijzigingssuggesties toe te staan.</span><span class="sxs-lookup"><span data-stu-id="46c99-121">When users are more familiar with the different reasons for action messages, then shorten the dampener period to allow more change suggestions.</span></span>|  
|<span data-ttu-id="46c99-122">Demping standaardhoeveelheid</span><span class="sxs-lookup"><span data-stu-id="46c99-122">Default Dampener Quantity</span></span>|<span data-ttu-id="46c99-123">Tussen 5 en 20 procent van de lotgrootte van het item instellen.</span><span class="sxs-lookup"><span data-stu-id="46c99-123">Set between 5 and 20 percent of the item’s lot size.</span></span>||  

## <a name="see-also"></a><span data-ttu-id="46c99-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="46c99-124">See Also</span></span>  
 <span data-ttu-id="46c99-125">[Aanbevolen procedures instellen: Voorraadplanning](setup-best-practices-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="46c99-125">[Setup Best Practices: Supply Planning](setup-best-practices-supply-planning.md) </span></span>  
 <span data-ttu-id="46c99-126">[Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="46c99-126">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
 [<span data-ttu-id="46c99-127">Complexe toepassingsgebieden instellen met aanbevolen procedures</span><span class="sxs-lookup"><span data-stu-id="46c99-127">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="46c99-128">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="46c99-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

