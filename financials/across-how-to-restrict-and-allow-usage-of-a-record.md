---
title: Het gebruik van een record verhinderen en toestaan | Microsoft Docs
description: Als u wilt voorkomen dat een record wordt gebruikt bij bepaalde activiteiten, bijvoorbeeld totdat de record is goedgekeurd, kunt u twee werkstroomantwoorden opnemen in een werkstroom die het gebruik van de record bestuurt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4636cdedc2c99d1aa7cfc2dc361f7135aa3c4199
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="restrict-and-allow-usage-of-a-record"></a><span data-ttu-id="d0edc-103">Gebruik van een record beperken en toestaan</span><span class="sxs-lookup"><span data-stu-id="d0edc-103">Restrict and Allow Usage of a Record</span></span>
<span data-ttu-id="d0edc-104">Als u wilt voorkomen dat een record wordt gebruikt bij bepaalde activiteiten, bijvoorbeeld totdat de record is goedgekeurd, kunt u twee werkstroomantwoorden opnemen in een werkstroom die het gebruik van de record bestuurt.</span><span class="sxs-lookup"><span data-stu-id="d0edc-104">If you want to restrict a record from being used in certain activities, for example, until the record has been approved, you can incorporate two workflow responses in a workflow that controls the usage of the record.</span></span> <span data-ttu-id="d0edc-105">Eén werkstroomantwoord beperkt het gebruik van de record zoals gedefinieerd door de werkstroomgebeurtenis en -voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="d0edc-105">One workflow response will restrict usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="d0edc-106">Een andere werkstroomantwoord staat het gebruik van de record toe zoals gedefinieerd door de werkstroomgebeurtenis en -voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="d0edc-106">Another workflow response will allow usage of the record as defined by the workflow event and conditions.</span></span> <span data-ttu-id="d0edc-107">Er bestaan twee responsen in de generieke versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] voor dit doel: **Gebruik van een record beperken**</span><span class="sxs-lookup"><span data-stu-id="d0edc-107">Two responses exist in the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] for this purpose: **Restrict usage of a record.**</span></span> <span data-ttu-id="d0edc-108">en **Gebruik van een record toestaan**.</span><span class="sxs-lookup"><span data-stu-id="d0edc-108">and **Allow usage of a record.**.</span></span>

> [!NOTE]  
>  <span data-ttu-id="d0edc-109">De algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] helpt verhinderen dat een record wordt geboekt, als betaling wordt geëxporteerd en als cheque wordt afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="d0edc-109">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] offers support for restricting a record from being posted, from being exported as a payment, and from being printed as a check.</span></span> <span data-ttu-id="d0edc-110">Als een Microsoft-partner andere beperkingen wil ondersteunen, moet deze de toepassingscode aanpassen.</span><span class="sxs-lookup"><span data-stu-id="d0edc-110">To support other restrictions, a Microsoft partner must customize the application code.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d0edc-111">De werkstroomfunctionaliteit om te verhinderen en toe te staan dat records worden gebruikt houdt geen verband met de functionaliteit om het boeken van artikel-, klant- en leveranciersrecords te blokkeren.</span><span class="sxs-lookup"><span data-stu-id="d0edc-111">The workflow functionality to restrict and allow records from being used is not related to the functionality to block item, customer, and vendor records from being posted.</span></span>

<span data-ttu-id="d0edc-112">In de volgende procedure wordt beschreven hoe u het boeken van inkooporders kunt verhinderen totdat deze zijn goedgekeurd.</span><span class="sxs-lookup"><span data-stu-id="d0edc-112">The following procedure describes how to restrict purchase orders from being posted until they have been approved.</span></span> <span data-ttu-id="d0edc-113">De nieuwe werkstroom wordt gebaseerd op de bestaande werkstroomsjabloon Goedkeuringswerkstroom inkoopfactuur.</span><span class="sxs-lookup"><span data-stu-id="d0edc-113">The new workflow will be based on the existing Purchase Invoice Approval Workflow workflow template.</span></span>  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a><span data-ttu-id="d0edc-114">Een werkstroomstap maken die voorkomt dat niet-goedgekeurde inkooporders worden geboekt</span><span class="sxs-lookup"><span data-stu-id="d0edc-114">To create a workflow step that restricts posting of unapproved purchase orders</span></span>  
1. <span data-ttu-id="d0edc-115">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Werkstromen** in en klik op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="d0edc-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d0edc-116">Maak in het venster **Werkstromen** een nieuwe werkstroom genaamd Goedkeuringswerkstroom inkooporder.</span><span class="sxs-lookup"><span data-stu-id="d0edc-116">In the **Workflows** window, create a new workflow named Purchase Order Approval Workflow.</span></span> <span data-ttu-id="d0edc-117">Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="d0edc-117">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  
3. <span data-ttu-id="d0edc-118">Kies de actie **Kopiëren van werkstroomsjabloon**.</span><span class="sxs-lookup"><span data-stu-id="d0edc-118">Choose the **Copy From Workflow Template** action.</span></span>  
4. <span data-ttu-id="d0edc-119">Kies het veld **Bronwerkstroomcode** en kies vervolgens in het venster **Werkstroomsjablonen** de werkstroomsjabloon Goedkeuringswerkstroom inkooporder.</span><span class="sxs-lookup"><span data-stu-id="d0edc-119">Choose the **Source Workflow Code** field, and then, in the **Workflow Templates** window, choose the Purchase Invoice Approval Workflow workflow template.</span></span>  

     <span data-ttu-id="d0edc-120">Zoals u ziet, draait het bij de eerste twee werkstroomstappen om het verhinderen en vervolgens het toestaan van het gebruik van inkoopfacturen.</span><span class="sxs-lookup"><span data-stu-id="d0edc-120">Notice that the first two workflow steps are about restricting and then allowing usage of purchase invoices.</span></span> <span data-ttu-id="d0edc-121">Ga door met het wijzigen van de gebeurtenisvoorwaarde in de eerste stap van de werkstroom om op te geven dat deze van toepassing is op inkooporders.</span><span class="sxs-lookup"><span data-stu-id="d0edc-121">Proceed to change the event condition on the first step of the new workflow to specify that it applies to purchase orders.</span></span>  
5. <span data-ttu-id="d0edc-122">Kies op het sneltabblad **Werkstroomstappen** het veld **Gebeurtenisvoorwaarden** en selecteer vervolgens voor het filter **Documentsoort** de optie **Order**.</span><span class="sxs-lookup"><span data-stu-id="d0edc-122">On the **Workflow Steps** FastTab, choose the **Event Conditions** field, and then, for the **Document Type** filter, select **Order**.</span></span>  
6. <span data-ttu-id="d0edc-123">Ga door om andere werkstroomstappen te bewerken, te verwijderen of toe te voegen in een bedrijfsproces dat begint door het boeken van niet-goedgekeurde inkooporders te verhinderen.</span><span class="sxs-lookup"><span data-stu-id="d0edc-123">Proceed to edit, delete, or add other workflow steps to fit a business process that begins by restricting unapproved purchase orders from being posted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d0edc-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d0edc-124">See Also</span></span>  
<span data-ttu-id="d0edc-125">[Werkstromen maken](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="d0edc-125">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
[<span data-ttu-id="d0edc-126">Werkstroom</span><span class="sxs-lookup"><span data-stu-id="d0edc-126">Workflow</span></span>](across-workflow.md)   

