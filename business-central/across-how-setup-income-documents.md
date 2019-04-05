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
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 6072dcf536211ddad76c6423421033dd43f534b0
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "815910"
---
# <a name="set-up-incoming-documents"></a><span data-ttu-id="27eee-103">Inkomende documenten instellen</span><span class="sxs-lookup"><span data-stu-id="27eee-103">Set Up Incoming Documents</span></span>
<span data-ttu-id="27eee-104">Als u dagboekregels van inkomende documentrecords maakt, moet u op de pagina **Instellingen van inkomende documenten** vastleggen welke dagboeksjabloon en batch moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="27eee-104">If you create general journal lines from incoming document records, you must specify on the **Incoming Documents Setup** page which journal template and batch to use.</span></span>

<span data-ttu-id="27eee-105">Als u niet wilt dat gebruikers facturen of dagboekregels maken van inkomende documentrecords, tenzij de documenten zijn goedgekeurd, moet u fiatteurs instellen op de pagina **Fiatteurs inkomende documenten**.</span><span class="sxs-lookup"><span data-stu-id="27eee-105">If you do not want users to create invoices or general journal lines from incoming document records unless the documents are first approved, you must set up approvers on the **Incoming Document Approvers** page.</span></span>

<span data-ttu-id="27eee-106">Als u PDF- en afbeeldingsbestanden naar elektronische documenten wilt omzetten waarnaar u kunt converteren, bijvoorbeeld inkoopfacturen in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u eerst de OCR-functie instellen en de service inschakelen.</span><span class="sxs-lookup"><span data-stu-id="27eee-106">To turn PDF and image files into electronic documents that you can convert to, for example, purchase invoices inside [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first set up the OCR feature and enable the service.</span></span>

<span data-ttu-id="27eee-107">Wanneer de functie Inkomende documenten is ingesteld, kunt u verschillende functies gebruiken om onkostenbewijzen te controleren, OCR-taken te beheren en inkomende documentbestanden handmatig of automatisch te converteren naar de relevante documenten of dagboekregels.</span><span class="sxs-lookup"><span data-stu-id="27eee-107">When the Incoming Documents feature is set up, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="27eee-108">De externe bestanden kunnen worden gekoppeld in elke procesfase, inclusief naar geboekte documenten en naar de resulterende leverancier, klant en grootboekposten.</span><span class="sxs-lookup"><span data-stu-id="27eee-108">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span> <span data-ttu-id="27eee-109">Zie [Inkomende documenten verwerken](across-process-income-documents.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="27eee-109">For more information, see [Processing Incoming Documents](across-process-income-documents.md).</span></span>

## <a name="to-set-up-the-incoming-documents-feature"></a><span data-ttu-id="27eee-110">De functie Inkomende documenten instellen</span><span class="sxs-lookup"><span data-stu-id="27eee-110">To set up the Incoming Documents feature</span></span>
1. <span data-ttu-id="27eee-111">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellingen inkomende documenten** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="27eee-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="27eee-112">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="27eee-112">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a><span data-ttu-id="27eee-113">Fiatteurs van inkomende documentrecords instellen</span><span class="sxs-lookup"><span data-stu-id="27eee-113">To set up approvers of incoming document records</span></span>
1. <span data-ttu-id="27eee-114">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellingen inkomende documenten** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="27eee-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Document Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="27eee-115">Kies op de pagina **Instellingen van inkomende documenten** de actie **Fiatteurs**.</span><span class="sxs-lookup"><span data-stu-id="27eee-115">On the **Incoming Documents Setup** page, choose the **Approvers** action.</span></span>

    <span data-ttu-id="27eee-116">De pagina **Fiatteurs inkomende documenten** bevat alle gebruikers die zijn ingesteld in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="27eee-116">The **Incoming Document Approvers** page shows all users that are set up in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
3. <span data-ttu-id="27eee-117">Selecteer een of meer gebruikers die een inkomend document kunnen goedkeuren voordat een verwant document of verwante dagboekregel kan worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="27eee-117">Select one or more users that can approve an incoming document before a related document or journal line can be created.</span></span>

<span data-ttu-id="27eee-118">Wanneer fiatteurs zijn ingesteld op de pagina **Fiatteurs inkomende documenten**, kunnen alleen die gebruikers een inkomend document goedkeuren als het selectievakje **Goedkeuring vereist voor maken** is ingeschakeld op de pagina **Instellingen inkomende documenten**.</span><span class="sxs-lookup"><span data-stu-id="27eee-118">When approvers have been set up on the **Incoming Document Approvers** page, only those users can approve an incoming document if the **Require Approval To Create** check box on the **Incoming Documents Setup** page is selected.</span></span>

> [!NOTE]  
>   <span data-ttu-id="27eee-119">Deze goedkeuringsinstellingen zijn niet gerelateerd aan goedkeuringswerkstromen.</span><span class="sxs-lookup"><span data-stu-id="27eee-119">This approval setup is not related to approval workflows.</span></span> <span data-ttu-id="27eee-120">Zie voor meer informatie [Goedkeuringswerkstromen gebruiken](across-how-use-approval-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="27eee-120">For more information, see [Use Approval Workflows](across-how-use-approval-workflows.md).</span></span>

## <a name="to-set-up-an-ocr-service"></a><span data-ttu-id="27eee-121">Een OCR-service instellen</span><span class="sxs-lookup"><span data-stu-id="27eee-121">To set up an OCR service</span></span>
1. <span data-ttu-id="27eee-122">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellingen van OCR-service** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="27eee-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **OCR Service Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="27eee-123">Vul de benodigde velden in.</span><span class="sxs-lookup"><span data-stu-id="27eee-123">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> <span data-ttu-id="27eee-124">Uw aanmeldgegevens worden automatisch versleuteld.</span><span class="sxs-lookup"><span data-stu-id="27eee-124">You login data is automatically encrypted.</span></span>

## <a name="see-also"></a><span data-ttu-id="27eee-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="27eee-125">See Also</span></span>
[<span data-ttu-id="27eee-126">Inkomende documenten verwerken</span><span class="sxs-lookup"><span data-stu-id="27eee-126">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="27eee-127">Inkomende documenten</span><span class="sxs-lookup"><span data-stu-id="27eee-127">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="27eee-128">Inkoop</span><span class="sxs-lookup"><span data-stu-id="27eee-128">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="27eee-129">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="27eee-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
