---
title: Geboekte verkoop- en inkoopdocumenten bewerken | Microsoft Docs
description: Meer informatie over de verschillende boekingsfuncties om inkoopdocumenten te boeken en hoe u geboekte documenten kunt bijwerken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ef23d98aaeeb63c17e836fd25b547703787264da
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776209"
---
# <a name="edit-posted-documents"></a><span data-ttu-id="b7bba-103">Geboekte documenten bewerken</span><span class="sxs-lookup"><span data-stu-id="b7bba-103">Edit Posted Documents</span></span>

<span data-ttu-id="b7bba-104">Soms moet u een geboekt document bijwerken omdat informatie die relevant is voor het document is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="b7bba-104">Sometimes you have to update a posted document because information that is relevant to the document has changed.</span></span> <span data-ttu-id="b7bba-105">In een geboekt verkoopdocument kan dit bijvoorbeeld het trackingnummer van de expediteur zijn.</span><span class="sxs-lookup"><span data-stu-id="b7bba-105">On a posted sales document, this can be the shipping agent's package tracking number, for example.</span></span> <span data-ttu-id="b7bba-106">In een geboekt inkoopdocument kan dit een betalingsverwijzing zijn.</span><span class="sxs-lookup"><span data-stu-id="b7bba-106">On a posted purchase document, this can be a payment reference text.</span></span>

<span data-ttu-id="b7bba-107">U voert de wijziging uit op een bewerkbare versie van het originele document, aangegeven met "**- Bijwerken**" in de paginatitel.</span><span class="sxs-lookup"><span data-stu-id="b7bba-107">You perform the change on an editable version of the original document, indicated by "**- Update**" in the page title.</span></span> <span data-ttu-id="b7bba-108">De pagina bevat een subset van de velden in het originele document, waarvan sommige niet-bewerkbare velden zijn die alleen ter informatie worden getoond.</span><span class="sxs-lookup"><span data-stu-id="b7bba-108">The page contains a subset of the fields on the original document, of which some are non-editable fields that are shown for information only.</span></span>

<span data-ttu-id="b7bba-109">De functionaliteit is beschikbaar voor de volgende documenten in alle ondersteunde markten:</span><span class="sxs-lookup"><span data-stu-id="b7bba-109">The functionality is available for the following documents across all supported markets:</span></span>

- <span data-ttu-id="b7bba-110">Geboekte verkoopverzending</span><span class="sxs-lookup"><span data-stu-id="b7bba-110">Posted Sales Shipment</span></span>
- <span data-ttu-id="b7bba-111">Geboekte inkoopfactuur</span><span class="sxs-lookup"><span data-stu-id="b7bba-111">Posted Purchase Invoice</span></span>
- <span data-ttu-id="b7bba-112">Geboekte retourverzending</span><span class="sxs-lookup"><span data-stu-id="b7bba-112">Posted Return Shipment</span></span>
- <span data-ttu-id="b7bba-113">Geboekte retourontvangst</span><span class="sxs-lookup"><span data-stu-id="b7bba-113">Posted Return Receipt</span></span>

<span data-ttu-id="b7bba-114">De volgende aanvullende documenten kunnen worden bewerkt in de opgegeven landen of regio's:</span><span class="sxs-lookup"><span data-stu-id="b7bba-114">The following additional documents can be edited in the specified countries or regions:</span></span>

- <span data-ttu-id="b7bba-115">ES: Geboekte verkoopfactuur, Geboekte verkoopcreditnota, Geboekte inkoopcreditnota</span><span class="sxs-lookup"><span data-stu-id="b7bba-115">ES: Posted Sales Invoice, Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="b7bba-116">APAC: Geboekte verkoopcreditnota, Geboekte inkoopcreditnota</span><span class="sxs-lookup"><span data-stu-id="b7bba-116">APAC: Posted Sales Credit Memo, Posted Purchase Credit Memo</span></span>
- <span data-ttu-id="b7bba-117">RU: Geboekte verkoopcreditnota</span><span class="sxs-lookup"><span data-stu-id="b7bba-117">RU: Posted Sales Credit Memo</span></span>
- <span data-ttu-id="b7bba-118">IT: Geboekte overdracht, Geboekte servicezending</span><span class="sxs-lookup"><span data-stu-id="b7bba-118">IT: Posted Transfer Shipment, Posted Service Shipment</span></span>

## <a name="to-edit-a-posted-sales-shipment"></a><span data-ttu-id="b7bba-119">Een geboekte verkoopverzending bewerken</span><span class="sxs-lookup"><span data-stu-id="b7bba-119">To edit a posted sales shipment</span></span>

<span data-ttu-id="b7bba-120">Hieronder wordt uitgelegd hoe u een geboekte verkoopverzending kunt bewerken.</span><span class="sxs-lookup"><span data-stu-id="b7bba-120">The following explains how to edit a posted sales shipment.</span></span> <span data-ttu-id="b7bba-121">De stappen zijn vergelijkbaar voor de andere ondersteunde documenten.</span><span class="sxs-lookup"><span data-stu-id="b7bba-121">The steps are similar for the other supported documents.</span></span>

1. <span data-ttu-id="b7bba-122">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte verkoopverzendingen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="b7bba-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Posted Sales Shipments**, and then choose the related link.</span></span>
2. <span data-ttu-id="b7bba-123">Selecteer het document dat u wilt bewerken en kies vervolgens de actie **Document bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="b7bba-123">Select the document that you want to edit, and then choose the **Update Document** action.</span></span> <span data-ttu-id="b7bba-124">U kunt ook het document openen en vervolgens de actie kiezen.</span><span class="sxs-lookup"><span data-stu-id="b7bba-124">Alternatively, open the document and then choose the action.</span></span>
3. <span data-ttu-id="b7bba-125">Bewerk op de pagina **Geboekte verkoopzending - Bijwerken** het veld **Traceringsnummer (zending)**</span><span class="sxs-lookup"><span data-stu-id="b7bba-125">On the **Posted Sales Shipment - Update** page, edit the **Package Tracking No.**</span></span> <span data-ttu-id="b7bba-126">bijvoorbeeld.</span><span class="sxs-lookup"><span data-stu-id="b7bba-126">field, for example.</span></span>
4. <span data-ttu-id="b7bba-127">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="b7bba-127">Choose the **OK** button.</span></span>

<span data-ttu-id="b7bba-128">De geboekte verkoopverzending wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="b7bba-128">The posted sales shipment is updated.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7bba-129">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b7bba-129">See Also</span></span>

[<span data-ttu-id="b7bba-130">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="b7bba-130">General Business Functionality</span></span>](ui-across-business-areas.md)  
[<span data-ttu-id="b7bba-131">Inkoop</span><span class="sxs-lookup"><span data-stu-id="b7bba-131">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="b7bba-132">Documenten en dagboeken boeken</span><span class="sxs-lookup"><span data-stu-id="b7bba-132">Posting Documents and Journals</span></span>](ui-post-documents-journals.md)  
<span data-ttu-id="b7bba-133">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b7bba-133">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]