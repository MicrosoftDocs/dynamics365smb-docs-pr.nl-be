---
title: Inkomende documenten instellen| Microsoft Docs
description: Gebruik de functie inkomende documenten om elektronische documenten te maken, OCR-taken te beheren, facturen te importeren en afbeeldingsbestanden te converteren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 0a33652ac230e63607957916308ee960d14a2b47
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188480"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="ccc2a-103">Inkomende documenten instellen</span><span class="sxs-lookup"><span data-stu-id="ccc2a-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="ccc2a-104">Als u dagboekregels van inkomende documentrecords maakt, moet u op de pagina **Instellingen van inkomende documenten** vastleggen welke dagboeksjabloon en batch moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ccc2a-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="ccc2a-105">Als u niet wilt dat gebruikers facturen of dagboekregels maken van inkomende documentrecords, tenzij de documenten zijn goedgekeurd, moet u werkstroomfiatteurs instellen.</span><span class="sxs-lookup"><span data-stu-id="ccc2a-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up workflow approvers.</span></span>

<span data-ttu-id="ccc2a-106">Als u PDF- en afbeeldingsbestanden naar elektronische documenten wilt omzetten waarnaar u kunt converteren, bijvoorbeeld inkoopfacturen in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u eerst de OCR-functie instellen en de service inschakelen.</span><span class="sxs-lookup"><span data-stu-id="ccc2a-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="ccc2a-107">Wanneer de functie Inkomende documenten is ingesteld, kunt u verschillende functies gebruiken om onkostenbewijzen te controleren, OCR-taken te beheren en inkomende documentbestanden handmatig of automatisch te converteren naar de relevante documenten of dagboekregels.</span><span class="sxs-lookup"><span data-stu-id="ccc2a-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="ccc2a-108">De externe bestanden kunnen worden gekoppeld in elke procesfase, inclusief naar geboekte documenten en naar de resulterende leverancier, klant en grootboekposten.</span><span class="sxs-lookup"><span data-stu-id="ccc2a-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="ccc2a-109">Zie [Inkomende documenten verwerken](across-process-income-documents.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ccc2a-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="ccc2a-110">De functie Inkomende documenten instellen</span><span class="sxs-lookup"><span data-stu-id="ccc2a-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="ccc2a-111">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellingen inkomende documenten** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="ccc2a-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="ccc2a-112">Vul de vereiste velden in.</span><span class="sxs-lookup"><span data-stu-id="ccc2a-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="ccc2a-113">Fiatteurs van inkomende documentrecords instellen</span><span class="sxs-lookup"><span data-stu-id="ccc2a-113">To set up approvers of incoming document records</span></span>
<span data-ttu-id="ccc2a-114">Fiatteurs van inkomende documenten moeten worden ingesteld als gebruikers van goedkeuringswerkstromen.</span><span class="sxs-lookup"><span data-stu-id="ccc2a-114">Approvers of incoming documents must be set up as approval workflow users.</span></span>

<span data-ttu-id="ccc2a-115">Voordat u werkstromen met goedkeuringsstappen kunt maken, moet u de werkstroomgebruikers instellen die betrokken zijn bij goedkeuringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="ccc2a-115">Before you can create workflows that involve approval steps, you must set up the workflow users who are involved in approval processes.</span></span> <span data-ttu-id="ccc2a-116">Op de pagina **Gebruikersinstellingen voor goedkeuring** kunt u ook maximumbedragen instellen voor specifieke typen aanvragen en vervangende fiatteurs aanwijzen aan wie goedkeuringsaanvragen worden gedelegeerd als de oorspronkelijke fiatteur afwezig is.</span><span class="sxs-lookup"><span data-stu-id="ccc2a-116">On the **Approval User Setup** page, you also set amount limits for specific types of requests and define substitute approvers to whom approval requests are delegated when the original approver is absent.</span></span> <span data-ttu-id="ccc2a-117">Zie voor meer informatie [Goedkeuringsgebruikers instellen](across-how-to-set-up-approval-users.md).</span><span class="sxs-lookup"><span data-stu-id="ccc2a-117">For more information, see [Set Up Approval Users](across-how-to-set-up-approval-users.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="ccc2a-118">Een OCR-service instellen</span><span class="sxs-lookup"><span data-stu-id="ccc2a-118">To set up an OCR service</span></span>
1. <span data-ttu-id="ccc2a-119">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **OCR-service-instellingen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="ccc2a-119">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="ccc2a-120">Vul de benodigde velden in.</span><span class="sxs-lookup"><span data-stu-id="ccc2a-120">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="ccc2a-121">Uw aanmeldgegevens worden automatisch versleuteld.</span><span class="sxs-lookup"><span data-stu-id="ccc2a-121">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="ccc2a-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ccc2a-122">See Also</span></span>
[<span data-ttu-id="ccc2a-123">Inkomende documenten verwerken</span><span class="sxs-lookup"><span data-stu-id="ccc2a-123">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="ccc2a-124">Inkomende documenten</span><span class="sxs-lookup"><span data-stu-id="ccc2a-124">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="ccc2a-125">Inkoop</span><span class="sxs-lookup"><span data-stu-id="ccc2a-125">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="ccc2a-126">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ccc2a-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
