---
title: Inkomende documenten instellen| Microsoft Docs
description: Gebruik de functie inkomende documenten om elektronische documenten te maken, OCR-taken te beheren, facturen te importeren en afbeeldingsbestanden te converteren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 08/10/2020
ms.author: edupont
ms.openlocfilehash: 1b0942c53f435a79cae733fe4d7287e628cf7478
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3780522"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="d6025-103">Inkomende documenten instellen</span><span class="sxs-lookup"><span data-stu-id="d6025-103">Set Up Incoming Documents</span></span>

<span data-ttu-id="d6025-104">Als u dagboekregels van inkomende documentrecords maakt, moet u op de pagina **Instellingen van inkomende documenten** vastleggen welke dagboeksjabloon en batch moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d6025-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="d6025-105">Als u niet wilt dat gebruikers facturen of dagboekregels maken van inkomende documentrecords, tenzij de documenten zijn goedgekeurd, moet u werkstroomfiatteurs instellen.</span><span class="sxs-lookup"><span data-stu-id="d6025-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="d6025-106">Als u PDF- en afbeeldingsbestanden naar elektronische documenten wilt omzetten waarnaar u kunt converteren, bijvoorbeeld inkoopfacturen in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u eerst de OCR-functie instellen en de service inschakelen.</span><span class="sxs-lookup"><span data-stu-id="d6025-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span> <span data-ttu-id="d6025-107">Kies een servicepakket dat past bij uw organisatie en/of land/regio.</span><span class="sxs-lookup"><span data-stu-id="d6025-107">Choose a service package that is appropriate for your organization and/or country/region.</span></span> <span data-ttu-id="d6025-108">U kunt ook handmatig items maken die de externe documenten vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="d6025-108">Alternatively, you can create entries manually to represent the external documents.</span></span>  

<span data-ttu-id="d6025-109">Wanneer de functie Inkomende documenten is ingesteld, kunt u verschillende functies gebruiken om onkostenbewijzen te controleren, OCR-taken te beheren en inkomende documentbestanden handmatig of automatisch te converteren naar de relevante documenten of dagboekregels.</span><span class="sxs-lookup"><span data-stu-id="d6025-109">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="d6025-110">De externe bestanden kunnen worden gekoppeld in elke procesfase, inclusief naar geboekte documenten en naar de resulterende leverancier, klant en grootboekposten.</span><span class="sxs-lookup"><span data-stu-id="d6025-110">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="d6025-111">Zie [Inkomende documenten verwerken](across-process-income-documents.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d6025-111">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="d6025-112">De functie Inkomende documenten instellen</span><span class="sxs-lookup"><span data-stu-id="d6025-112">To set up the Incoming Documents feature</span></span>

1. <span data-ttu-id="d6025-113">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellingen inkomende documenten** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="d6025-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="d6025-114">Vul de vereiste velden in.</span><span class="sxs-lookup"><span data-stu-id="d6025-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="d6025-115">Als onderdeel van de instelling moet u beslissen of u goedkeuring van inkomende documenten wilt hebben.</span><span class="sxs-lookup"><span data-stu-id="d6025-115">As part of the setup, you must decide if you want to require approval of incoming documents.</span></span> <span data-ttu-id="d6025-116">Om goedkeuring te vereisen moet u goedkeurders en goedkeuringswerkstromen instellen.</span><span class="sxs-lookup"><span data-stu-id="d6025-116">To require approval, you must set up approvers and approval workflows.</span></span> <span data-ttu-id="d6025-117">Als uw organisatie niet van plan is goedkeuring te vereisen, kunt u de volgende sectie overslaan.</span><span class="sxs-lookup"><span data-stu-id="d6025-117">If your organization does not intend to require approval, you can skip the next section.</span></span>  

<span data-ttu-id="d6025-118">Ten slotte, als u een service gebruikt om PDF- of afbeeldingsbestanden te converteren die inkomende documenten vertegenwoordigen, moet u deze instellen.</span><span class="sxs-lookup"><span data-stu-id="d6025-118">Finally, you if you use a service to convert PDF or image files representing incoming documents, you must it set up.</span></span> <span data-ttu-id="d6025-119">Anders kunt u die sectie ook overslaan.</span><span class="sxs-lookup"><span data-stu-id="d6025-119">Otherwise, you can also skip that section.</span></span>  

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="d6025-120">Fiatteurs van inkomende documentrecords instellen</span><span class="sxs-lookup"><span data-stu-id="d6025-120">To set up approvers of incoming document records</span></span>

<span data-ttu-id="d6025-121">Stel eventueel een goedkeuringsproces in voor de inkomende documenten.</span><span class="sxs-lookup"><span data-stu-id="d6025-121">Optionally, set up an approval process for the incoming documents.</span></span> <span data-ttu-id="d6025-122">Fiatteurs van inkomende documenten moeten worden ingesteld als gebruikers van goedkeuringswerkstromen.</span><span class="sxs-lookup"><span data-stu-id="d6025-122">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="d6025-123">Voordat u werkstromen met goedkeuringsstappen kunt maken, moet u de werkstroomgebruikers instellen die betrokken zijn bij goedkeuringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="d6025-123">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="d6025-124">Op de pagina **Gebruikersinstellingen voor goedkeuring** kunt u ook maximumbedragen instellen voor specifieke typen aanvragen en vervangende fiatteurs aanwijzen aan wie goedkeuringsaanvragen worden gedelegeerd als de oorspronkelijke fiatteur afwezig is.</span><span class="sxs-lookup"><span data-stu-id="d6025-124">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="d6025-125">Zie voor meer informatie [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="d6025-125">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="d6025-126">Een OCR-service instellen</span><span class="sxs-lookup"><span data-stu-id="d6025-126">To set up an OCR service</span></span>

1. <span data-ttu-id="d6025-127">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **OCR-service-instellingen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="d6025-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="d6025-128">Vul de vereiste velden in.</span><span class="sxs-lookup"><span data-stu-id="d6025-128">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="d6025-129">Uw aanmeldgegevens worden automatisch versleuteld.</span><span class="sxs-lookup"><span data-stu-id="d6025-129">You login data is automatically encrypted.</span></span>

<span data-ttu-id="d6025-130">Zie [OCR gebruiken om PDF- en afbeeldingsbestanden te converteren naar elektronische documenten](across-how-use-ocr-pdf-images-files.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d6025-130">For more information, see [Use OCR to Turn PDF and Image Files into Electronic Documents](across-how-use-ocr-pdf-images-files.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="d6025-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d6025-131">See Also</span></span>

[<span data-ttu-id="d6025-132">Inkomende documenten verwerken</span><span class="sxs-lookup"><span data-stu-id="d6025-132">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="d6025-133">Inkomende documenten</span><span class="sxs-lookup"><span data-stu-id="d6025-133">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="d6025-134">Inkoop</span><span class="sxs-lookup"><span data-stu-id="d6025-134">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="d6025-135">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d6025-135">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
