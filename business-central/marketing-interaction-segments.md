---
title: Segmenten en gerelateerde interactie traceren| Microsoft Docs
description: "Meer informatie over het maken van segmenten om groepen contacten te definiëren en interacties op te geven voor segmenten."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 1fcec3051fdabae818528742fba5d9ca57a721c8
ms.contentlocale: nl-be
ms.lasthandoff: 11/26/2018

---
# <a name="managing-interactions-for-segments"></a><span data-ttu-id="a4050-103">Interactie voor segmenten beheren</span><span class="sxs-lookup"><span data-stu-id="a4050-103">Managing Interactions for Segments</span></span>
<span data-ttu-id="a4050-104">De pagina **Segment** is een soort werkblad waarop u het volgende kunt doen:</span><span class="sxs-lookup"><span data-stu-id="a4050-104">The **Segment** page is a type of worksheet where you can:</span></span>

* <span data-ttu-id="a4050-105">Segmenten maken.</span><span class="sxs-lookup"><span data-stu-id="a4050-105">Create segments.</span></span>
* <span data-ttu-id="a4050-106">De segmentcriteria opslaan die u hebt gebruikt om contacten te selecteren.</span><span class="sxs-lookup"><span data-stu-id="a4050-106">Save the segmentation criteria you have used to select contacts.</span></span>
* <span data-ttu-id="a4050-107">Het segment registreren en interacties vastleggen voor de contacten in het segment.</span><span class="sxs-lookup"><span data-stu-id="a4050-107">Log the segment and record interactions involving the contacts within the segment.</span></span>

## <a name="segmenting"></a><span data-ttu-id="a4050-108">Segmenten maken</span><span class="sxs-lookup"><span data-stu-id="a4050-108">Segmenting</span></span>
<span data-ttu-id="a4050-109">Er zijn verschillende manieren om segmenten te maken:</span><span class="sxs-lookup"><span data-stu-id="a4050-109">There are several ways to create segments:</span></span>

* <span data-ttu-id="a4050-110">U kunt de contacten die u wilt opnemen in het segment handmatig invoeren op de segmentregels.</span><span class="sxs-lookup"><span data-stu-id="a4050-110">You can manually enter the contacts you want to include in the segment in the segment lines.</span></span>
* <span data-ttu-id="a4050-111">U kunt contacten selecteren.</span><span class="sxs-lookup"><span data-stu-id="a4050-111">You can select contacts.</span></span>
* <span data-ttu-id="a4050-112">U kunt een geregistreerd segment opnieuw gebruiken als basis voor een nieuw segment.</span><span class="sxs-lookup"><span data-stu-id="a4050-112">You can reuse a logged segment as the basis to create a new one.</span></span>
* <span data-ttu-id="a4050-113">U kunt opgeslagen segmentcriteria opnieuw gebruiken.</span><span class="sxs-lookup"><span data-stu-id="a4050-113">You can reuse saved segmentation criteria.</span></span>

## <a name="interactions"></a><span data-ttu-id="a4050-114">Interacties</span><span class="sxs-lookup"><span data-stu-id="a4050-114">Interactions</span></span>
<span data-ttu-id="a4050-115">Op de pagina **Segment** kunt u tegelijkertijd interacties maken voor verschillende contacten.</span><span class="sxs-lookup"><span data-stu-id="a4050-115">On the **Segment** page, you can create interactions for several contacts simultaneously.</span></span> <span data-ttu-id="a4050-116">U kunt bijvoorbeeld een segment samenvoegen met een Microsoft Word-document, zodat u een brief kunt verzenden naar alle contacten in het segment.</span><span class="sxs-lookup"><span data-stu-id="a4050-116">For example, you can merge a segment with a Microsoft Word document, so that you can send a letter to all the contacts in the segment.</span></span>

<span data-ttu-id="a4050-117">U kunt informatie opgeven over de interactie voor het segment in de **Segment**-kop.</span><span class="sxs-lookup"><span data-stu-id="a4050-117">You can specify information about the interaction for the segment on the **Segment** header.</span></span> <span data-ttu-id="a4050-118">U kunt bijvoorbeeld bepalen welke interactiesjabloon u voor alle contacten wilt gebruiken, een omschrijving, correspondentietype, enzovoort opgeven.</span><span class="sxs-lookup"><span data-stu-id="a4050-118">For example, you can decide which interaction template you want to use for all the contacts, specify a description, a correspondence type, and so on.</span></span> <span data-ttu-id="a4050-119">U kunt deze gegevens echter voor elk contact wijzigen op de segmentregel, bijvoorbeeld door een andere omschrijving op te geven voor één contact.</span><span class="sxs-lookup"><span data-stu-id="a4050-119">However, you can modify this information in the segment line for each particular contact, for example, by specifying another description for one contact.</span></span> <span data-ttu-id="a4050-120">Als u een segment samenvoegt met een Microsoft Word-document, kunt u het te verzenden document persoonlijk aanpassen voor één of meer contacten in het segment, bijvoorbeeld door persoonlijke opmerkingen toe te voegen aan het document.</span><span class="sxs-lookup"><span data-stu-id="a4050-120">If you are merging a segment with a Microsoft Word document, you can personalize the document to be sent for one or several of the contacts within the segment, for example, by adding individualized comments to the document.</span></span>

## <a name="logging"></a><span data-ttu-id="a4050-121">Registreren</span><span class="sxs-lookup"><span data-stu-id="a4050-121">Logging</span></span>
<span data-ttu-id="a4050-122">Wanneer u op de pagina **Segment** klikt op **Logbestand**, worden de interacties vastgelegd op de pagina **Interactielogpost** en wordt het segment geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="a4050-122">On the **Segment** page, when you choose **Log**, the application records the interactions on the **Interaction Log Entry** page, and logs the segment.</span></span> <span data-ttu-id="a4050-123">Alleen op de pagina **Geregistreerde segmenten** kunt u het segment bekijken dat u hebt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="a4050-123">After you have logged the segment, you can only find it on the **Logged Segments** page.</span></span>

<span data-ttu-id="a4050-124">Op de pagina **Geregistreerde segmenten** kunt u besluiten een follow-upsegment te maken met dezelfde contacten als het segment dat u hebt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="a4050-124">On the **Logged Segments** page, you can decide to create a follow-up segment containing the same contacts as the segment you have logged.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4050-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a4050-125">See Also</span></span>
[<span data-ttu-id="a4050-126">Segmenten maken</span><span class="sxs-lookup"><span data-stu-id="a4050-126">Create Segments</span></span>](marketing-how-create-segment.md)  
[<span data-ttu-id="a4050-127">Interacties maken voor segmenten</span><span class="sxs-lookup"><span data-stu-id="a4050-127">Create Interactions for Segments</span></span>](marketing-how-create-interactions.md)  
[<span data-ttu-id="a4050-128">Segmenten beheren</span><span class="sxs-lookup"><span data-stu-id="a4050-128">Managing Segments</span></span>](marketing-segments.md)  
[<span data-ttu-id="a4050-129">Interacties vastleggen met contacten</span><span class="sxs-lookup"><span data-stu-id="a4050-129">Recording Interactions With Contacts</span></span>](marketing-interactions.md)  
[<span data-ttu-id="a4050-130">Verkoopopportunities beheren</span><span class="sxs-lookup"><span data-stu-id="a4050-130">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="a4050-131">Contactpersonen maken en beheren</span><span class="sxs-lookup"><span data-stu-id="a4050-131">Creating and Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="a4050-132">Werken met Business Central</span><span class="sxs-lookup"><span data-stu-id="a4050-132">Working with Business Central</span></span>](ui-work-product.md)

