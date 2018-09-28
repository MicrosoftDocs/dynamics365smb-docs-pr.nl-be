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
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: d9b6d697ef48951fc656fc30ad94b128cd64ccea
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="managing-interactions-for-segments"></a><span data-ttu-id="9443a-103">Interactie voor segmenten beheren</span><span class="sxs-lookup"><span data-stu-id="9443a-103">Managing Interactions for Segments</span></span>
<span data-ttu-id="9443a-104">Het venster **Segment** is een soort werkblad waarop u het volgende kunt doen:</span><span class="sxs-lookup"><span data-stu-id="9443a-104">The **Segment** window is a type of worksheet where you can:</span></span>

* <span data-ttu-id="9443a-105">Segmenten maken.</span><span class="sxs-lookup"><span data-stu-id="9443a-105">Create segments.</span></span>
* <span data-ttu-id="9443a-106">De segmentcriteria opslaan die u hebt gebruikt om contacten te selecteren.</span><span class="sxs-lookup"><span data-stu-id="9443a-106">Save the segmentation criteria you have used to select contacts.</span></span>
* <span data-ttu-id="9443a-107">Het segment registreren en interacties vastleggen voor de contacten in het segment.</span><span class="sxs-lookup"><span data-stu-id="9443a-107">Log the segment and record interactions involving the contacts within the segment.</span></span>

## <a name="segmenting"></a><span data-ttu-id="9443a-108">Segmenten maken</span><span class="sxs-lookup"><span data-stu-id="9443a-108">Segmenting</span></span>
<span data-ttu-id="9443a-109">Er zijn verschillende manieren om segmenten te maken:</span><span class="sxs-lookup"><span data-stu-id="9443a-109">There are several ways to create segments:</span></span>

* <span data-ttu-id="9443a-110">U kunt de contacten die u wilt opnemen in het segment handmatig invoeren op de segmentregels.</span><span class="sxs-lookup"><span data-stu-id="9443a-110">You can manually enter the contacts you want to include in the segment in the segment lines.</span></span>
* <span data-ttu-id="9443a-111">U kunt contacten selecteren.</span><span class="sxs-lookup"><span data-stu-id="9443a-111">You can select contacts.</span></span>
* <span data-ttu-id="9443a-112">U kunt een geregistreerd segment opnieuw gebruiken als basis voor een nieuw segment.</span><span class="sxs-lookup"><span data-stu-id="9443a-112">You can reuse a logged segment as the basis to create a new one.</span></span>
* <span data-ttu-id="9443a-113">U kunt opgeslagen segmentcriteria opnieuw gebruiken.</span><span class="sxs-lookup"><span data-stu-id="9443a-113">You can reuse saved segmentation criteria.</span></span>

## <a name="interactions"></a><span data-ttu-id="9443a-114">Interacties</span><span class="sxs-lookup"><span data-stu-id="9443a-114">Interactions</span></span>
<span data-ttu-id="9443a-115">In het venster **Segment** kunt u tegelijkertijd interacties maken voor verschillende contacten.</span><span class="sxs-lookup"><span data-stu-id="9443a-115">In the **Segment** window, you can create interactions for several contacts simultaneously.</span></span> <span data-ttu-id="9443a-116">U kunt bijvoorbeeld een segment samenvoegen met een Microsoft Word-document, zodat u een brief kunt verzenden naar alle contacten in het segment.</span><span class="sxs-lookup"><span data-stu-id="9443a-116">For example, you can merge a segment with a Microsoft Word document, so that you can send a letter to all the contacts in the segment.</span></span>

<span data-ttu-id="9443a-117">U kunt informatie opgeven over de interactie voor het segment in de **Segment**-kop.</span><span class="sxs-lookup"><span data-stu-id="9443a-117">You can specify information about the interaction for the segment on the **Segment** header.</span></span> <span data-ttu-id="9443a-118">U kunt bijvoorbeeld bepalen welke interactiesjabloon u voor alle contacten wilt gebruiken, een omschrijving, correspondentietype, enzovoort opgeven.</span><span class="sxs-lookup"><span data-stu-id="9443a-118">For example, you can decide which interaction template you want to use for all the contacts, specify a description, a correspondence type, and so on.</span></span> <span data-ttu-id="9443a-119">U kunt deze gegevens echter voor elk contact wijzigen op de segmentregel, bijvoorbeeld door een andere omschrijving op te geven voor één contact.</span><span class="sxs-lookup"><span data-stu-id="9443a-119">However, you can modify this information in the segment line for each particular contact, for example, by specifying another description for one contact.</span></span> <span data-ttu-id="9443a-120">Als u een segment samenvoegt met een Microsoft Word-document, kunt u het te verzenden document persoonlijk aanpassen voor één of meer contacten in het segment, bijvoorbeeld door persoonlijke opmerkingen toe te voegen aan het document.</span><span class="sxs-lookup"><span data-stu-id="9443a-120">If you are merging a segment with a Microsoft Word document, you can personalize the document to be sent for one or several of the contacts within the segment, for example, by adding individualized comments to the document.</span></span>

## <a name="logging"></a><span data-ttu-id="9443a-121">Registreren</span><span class="sxs-lookup"><span data-stu-id="9443a-121">Logging</span></span>
<span data-ttu-id="9443a-122">Wanneer u in het venster **Segment** klikt op **Logbestand**, worden de interacties vastgelegd in de tabel **Interactielogpost** en wordt het segment geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="9443a-122">In the **Segment** window, when you choose **Log**, the application records the interactions in the **Interaction Log Entry** window, and logs the segment.</span></span> <span data-ttu-id="9443a-123">Alleen in het venster **Geregistreerde segmenten** kunt u het segment bekijken dat u hebt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="9443a-123">After you have logged the segment, you can only find it in the **Logged Segments** window.</span></span>

<span data-ttu-id="9443a-124">In het venster **Geregistreerde segmenten** kunt u besluiten een follow-upsegment te maken met dezelfde contacten als het segment dat u hebt geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="9443a-124">In the **Logged Segments** window, you can decide to create a follow-up segment containing the same contacts as the segment you have logged.</span></span>

## <a name="see-also"></a><span data-ttu-id="9443a-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9443a-125">See Also</span></span>
[<span data-ttu-id="9443a-126">Segmenten maken</span><span class="sxs-lookup"><span data-stu-id="9443a-126">Create Segments</span></span>](marketing-how-create-segment.md)  
[<span data-ttu-id="9443a-127">Interacties maken voor segmenten</span><span class="sxs-lookup"><span data-stu-id="9443a-127">Create Interactions for Segments</span></span>](marketing-how-create-interactions.md)  
[<span data-ttu-id="9443a-128">Segmenten beheren</span><span class="sxs-lookup"><span data-stu-id="9443a-128">Managing Segments</span></span>](marketing-segments.md)  
[<span data-ttu-id="9443a-129">Interacties vastleggen met contacten</span><span class="sxs-lookup"><span data-stu-id="9443a-129">Recording Interactions With Contacts</span></span>](marketing-interactions.md)  
[<span data-ttu-id="9443a-130">Verkoopopportunities beheren</span><span class="sxs-lookup"><span data-stu-id="9443a-130">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="9443a-131">Contactpersonen maken en beheren</span><span class="sxs-lookup"><span data-stu-id="9443a-131">Creating and Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="9443a-132">Werken met Business Central</span><span class="sxs-lookup"><span data-stu-id="9443a-132">Working with Business Central</span></span>](ui-work-product.md)

