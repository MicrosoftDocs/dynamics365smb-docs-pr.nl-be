---
title: Records maken van inkomende documenten| Microsoft Docs
description: U kunt records maken van inkomende documenten, zoals e-facturen, en OCR-taken, eCommerce en documentuitwisseling beheren.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 33ca7a06aa8c903bb6f65af298748417ac460f63
ms.contentlocale: nl-be
ms.lasthandoff: 11/26/2018

---
# <a name="create-incoming-document-records"></a><span data-ttu-id="340ad-103">Inkomende documentrecords maken</span><span class="sxs-lookup"><span data-stu-id="340ad-103">Create Incoming Document Records</span></span>
<span data-ttu-id="340ad-104">Op de pagina **Inkomende documenten** kunt u verschillende functies gebruiken om onkostenbewijzen te controleren, OCR-taken te beheren en inkomende documentbestanden handmatig of automatisch te converteren naar de relevante documenten of dagboekregels.</span><span class="sxs-lookup"><span data-stu-id="340ad-104">On the **Incoming Documents** page, you can use different functions to review expense receipts, manage OCR tasks, and convert incoming document files, manually or automatically, to the relevant documents or journal lines.</span></span> <span data-ttu-id="340ad-105">De externe bestanden kunnen worden gekoppeld in elke procesfase, inclusief naar geboekte documenten en naar de resulterende leverancier, klant en grootboekposten.</span><span class="sxs-lookup"><span data-stu-id="340ad-105">The external files can be attached at any process stage, including to posted documents and to the resulting vendor, customer, and general ledger entries.</span></span>

<span data-ttu-id="340ad-106">Als u een extern document wilt registreren in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u eerst een inkomende documentrecord maken of voltooien.</span><span class="sxs-lookup"><span data-stu-id="340ad-106">To record an external document in [!INCLUDE[d365fin](includes/d365fin_md.md)], you must first create or complete an incoming document record.</span></span> <span data-ttu-id="340ad-107">U kunt dit handmatig doen of u kunt een foto van het externe document maken en vervolgens de inkomende documentrecord maken met het afbeeldingsbestand bijgevoegd.</span><span class="sxs-lookup"><span data-stu-id="340ad-107">You can do this manually, or you can take a photo of the external document and then create the incoming document record with the image file attached.</span></span>

<span data-ttu-id="340ad-108">Voordat u de functie Inkomende documenten gebruikt, moet u de benodigde instellingen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="340ad-108">Before you can use the Incoming Documents feature, you must perform the required setup.</span></span> <span data-ttu-id="340ad-109">Zie voor meer informatie [Inkomende documenten instellen](across-how-setup-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="340ad-109">For more information, see [Set Up Incoming Documents](across-how-setup-income-documents.md).</span></span>

## <a name="to-approve-or-reject-an-incoming-document"></a><span data-ttu-id="340ad-110">Een inkomend document goedkeuren of weigeren</span><span class="sxs-lookup"><span data-stu-id="340ad-110">To approve or reject an incoming document</span></span>
<span data-ttu-id="340ad-111">Als u gebruikers niet wilt toestaan om facturen of dagboekregels te maken van inkomende documentrecords, tenzij ze zijn goedgekeurd, kunt u goedkeurders instellen die de records moeten goedkeuren voordat ze kunnen worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="340ad-111">If you do want to allow users to create invoices or general journal lines from incoming document records unless they are approved, you can set up approvers who must approve the records before they can be processed.</span></span>

1. <span data-ttu-id="340ad-112">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkomende documenten** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="340ad-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="340ad-113">Selecteer de regel met het document dat u wilt goedkeuren of weigeren en kies vervolgens de actie **Goedkeuren** of **Weigeren**.</span><span class="sxs-lookup"><span data-stu-id="340ad-113">Select the line with the document that you want to approve or reject, and then choose the **Approve** or **Reject** actions.</span></span>

<span data-ttu-id="340ad-114">Als u de inkomende documentrecord goedkeurt, wordt het selectievakje **Vrijgegeven** op de regel van het inkomende document geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="340ad-114">If you approve the incoming document record, the **Released** check box on the incoming document line is selected.</span></span> <span data-ttu-id="340ad-115">De gebruiker die verantwoordelijk is voor het aanmaken van, bijvoorbeeld, inkoopfacturen kan doorgaan om de record te verwerken.</span><span class="sxs-lookup"><span data-stu-id="340ad-115">The user in charge of creating, for example, purchase invoices can proceed to process the record.</span></span>

## <a name="to-create-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="340ad-116">Een inkomende documentrecord maken door een foto te maken</span><span class="sxs-lookup"><span data-stu-id="340ad-116">To create an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="340ad-117">De volgende procedure geldt alleen voor de [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet- en Telefoon-client.</span><span class="sxs-lookup"><span data-stu-id="340ad-117">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="340ad-118">Kies op de app-balk de tegel **Inkomend document maken van camera** en ga vervolgens naar stap 4.</span><span class="sxs-lookup"><span data-stu-id="340ad-118">On the app bar, choose the **Create Incoming Document from Camera** tile, and then go to step 4.</span></span>
2. <span data-ttu-id="340ad-119">U kunt ook op de app-bar de optieknop kiezen, **Inkomende documenten** kiezen en **Alle** kiezen.</span><span class="sxs-lookup"><span data-stu-id="340ad-119">Alternatively, on the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
3. <span data-ttu-id="340ad-120">Kies op de pagina **Inkomende documenten** de selectieknop en kies vervolgens **Maken van camera**.</span><span class="sxs-lookup"><span data-stu-id="340ad-120">On the **Incoming Documents** page, choose the ellipsis button, and then choose **Create from Camera**.</span></span> <span data-ttu-id="340ad-121">De camera op de tablet of de telefoon wordt ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="340ad-121">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="340ad-122">Maak een foto van een document, zoals een inkoopontvangst, dat u wilt verwerken als een inkomend document en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="340ad-122">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="340ad-123">Er wordt een nieuwe documentrecord gemaakt met de afbeelding gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="340ad-123">A new incoming document record is created, with the image attached.</span></span>

## <a name="to-attach-an-image-to-an-incoming-document-record-by-taking-a-photo"></a><span data-ttu-id="340ad-124">Een afbeelding aan een inkomende documentrecord koppelen door een foto te maken</span><span class="sxs-lookup"><span data-stu-id="340ad-124">To attach an image to an incoming document record by taking a photo</span></span>
> [!NOTE]  
>   <span data-ttu-id="340ad-125">De volgende procedure geldt alleen voor de [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet- en Telefoon-client.</span><span class="sxs-lookup"><span data-stu-id="340ad-125">The following procedure only applies to the [!INCLUDE[d365fin](includes/d365fin_md.md)] Tablet and Phone clients.</span></span>

1. <span data-ttu-id="340ad-126">Kies op de app-bar de optieknop, kies **Inkomende documenten** en kies **Alle**.</span><span class="sxs-lookup"><span data-stu-id="340ad-126">On the app bar, choose the options button, choose **Incoming Documents**, and then choose **All**.</span></span>
2. <span data-ttu-id="340ad-127">Open de kaart voor een bestaande inkomende documentrecord.</span><span class="sxs-lookup"><span data-stu-id="340ad-127">Open the card for an existing incoming document record.</span></span>
3. <span data-ttu-id="340ad-128">Kies op de pagina **Inkomende documenten** de selectieknop en kies vervolgens **Afbeelding van camera bijvoegen**.</span><span class="sxs-lookup"><span data-stu-id="340ad-128">On the **Incoming Document** page, choose the ellipsis button, and then choose **Attach Image from Camera**.</span></span> <span data-ttu-id="340ad-129">De camera op de tablet of de telefoon wordt ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="340ad-129">The camera on the tablet or phone is activated.</span></span>
4. <span data-ttu-id="340ad-130">Maak een foto van een document, zoals een inkoopontvangst, dat u wilt verwerken als een inkomend document en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="340ad-130">Take a photo of a document, such as a purchase receipt, that you want to process as an incoming document, and then choose the **OK** button.</span></span>

    <span data-ttu-id="340ad-131">De afbeelding wordt gekoppeld aan de inkomende documentrecord.</span><span class="sxs-lookup"><span data-stu-id="340ad-131">The image is attached to the incoming document record.</span></span>

## <a name="to-create-an-incoming-document-record-manually"></a><span data-ttu-id="340ad-132">Een inkomend documentrecord handmatig maken</span><span class="sxs-lookup"><span data-stu-id="340ad-132">To create an incoming document record manually</span></span>
1. <span data-ttu-id="340ad-133">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkomende documenten** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="340ad-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Incoming Documents**, and then choose the related link.</span></span>
2. <span data-ttu-id="340ad-134">Kies de actie **Maken van bestand**.</span><span class="sxs-lookup"><span data-stu-id="340ad-134">Choose the **Create from File** action.</span></span>  
3. <span data-ttu-id="340ad-135">Selecteer op de pagina **Bestand invoegen** een bestand en kies vervolgens **Openen**.</span><span class="sxs-lookup"><span data-stu-id="340ad-135">On the **Insert File** page, select a file, and then choose **Open**.</span></span> <span data-ttu-id="340ad-136">Het bestand wordt automatisch gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="340ad-136">The file is automatically attached.</span></span>
4. <span data-ttu-id="340ad-137">U kunt ook de actie **Nieuw** kiezen.</span><span class="sxs-lookup"><span data-stu-id="340ad-137">Alternatively, choose the **New** action.</span></span>
5. <span data-ttu-id="340ad-138">Als u een bestand wilt bijvoegen, kiest u de actie **Bestand koppelen**.</span><span class="sxs-lookup"><span data-stu-id="340ad-138">To attach a file, choose the **Attach File** action.</span></span>
6. <span data-ttu-id="340ad-139">Op de pagina **Bestand invoegen**, selecteert u het bestand dat het betreffende inkomende document vertegenwoordigt. Kies vervolgens de knop **Openen**.</span><span class="sxs-lookup"><span data-stu-id="340ad-139">On the **Insert File** page, select the file that represents the incoming document in question, and then choose the **Open** button.</span></span>
7. <span data-ttu-id="340ad-140">Vul op de pagina **Inkomende documenten** indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="340ad-140">On the **Incoming Document** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="340ad-141">Zie ook</span><span class="sxs-lookup"><span data-stu-id="340ad-141">See Also</span></span>
[<span data-ttu-id="340ad-142">Inkomende documenten verwerken</span><span class="sxs-lookup"><span data-stu-id="340ad-142">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="340ad-143">Inkomende documenten</span><span class="sxs-lookup"><span data-stu-id="340ad-143">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="340ad-144">Inkoop</span><span class="sxs-lookup"><span data-stu-id="340ad-144">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="340ad-145">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="340ad-145">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

