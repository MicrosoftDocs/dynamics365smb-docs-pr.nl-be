---
title: Sectoren voor contactbedrijven instellen | Microsoft Docs
description: Beschrijft hoe u een sector instelt en aan een contactbedrijf toewijst, bijvoorbeeld de detailhandel of de auto-industrie.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7fef570e7e56e348a25ae660fa9248b529d0bfde
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-industry-groups-for-contact-companies"></a><span data-ttu-id="5f8da-103">Procedure: Sectoren instellen voor contactbedrijven</span><span class="sxs-lookup"><span data-stu-id="5f8da-103">How to: Set Up Industry Groups for Contact Companies</span></span>
<span data-ttu-id="5f8da-104">U gebruikt sectoren om het soort industrie aan te geven waartoe uw contacten behoren, bijvoorbeeld de detailhandel of de automobielindustrie.</span><span class="sxs-lookup"><span data-stu-id="5f8da-104">You use industry groups to indicate the type of industry to which your contacts belong, for example, the retail industry or the automobile industry.</span></span>

<span data-ttu-id="5f8da-105">Sectoren gebruiken voor contacten is een proces van twee stappen.</span><span class="sxs-lookup"><span data-stu-id="5f8da-105">Using industry groups on contacts is a two-step process.</span></span> <span data-ttu-id="5f8da-106">Eerst definieert u de sectorcode.</span><span class="sxs-lookup"><span data-stu-id="5f8da-106">First, you define the industry group code.</span></span> <span data-ttu-id="5f8da-107">U hoeft deze stap slechts eenmaal uit te voeren voor elke sector.</span><span class="sxs-lookup"><span data-stu-id="5f8da-107">You only have to perform this step one time for each industry group.</span></span> <span data-ttu-id="5f8da-108">Als u een sectorcode hebt, kunt u beginnen de code toe te wijzen aan contactbedrijven.</span><span class="sxs-lookup"><span data-stu-id="5f8da-108">Once you have an industry group code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="5f8da-109">Als u de contacten wilt synchroniseren met leveranciers, klanten of bankrekeningen in een ander onderdeel van de toepassing, kunt u een zakenrelatie instellen.</span><span class="sxs-lookup"><span data-stu-id="5f8da-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-an-industry-group-code"></a><span data-ttu-id="5f8da-110">Een sectorcode definiëren</span><span class="sxs-lookup"><span data-stu-id="5f8da-110">To define an industry group code</span></span>
<span data-ttu-id="5f8da-111">De sectorcode bepaalt het type of de categorie van de groep, zoals ADVERTENTIE voor reclame of PERS voor tv en radio.</span><span class="sxs-lookup"><span data-stu-id="5f8da-111">The industry group code defines the type or category of the group, such as ADVERT for advertising, or PRESS, for TV and radio.</span></span> <span data-ttu-id="5f8da-112">U kunt meerdere sectorcodes hebben.</span><span class="sxs-lookup"><span data-stu-id="5f8da-112">You can have several industry group codes.</span></span> <span data-ttu-id="5f8da-113">Als u de sectoren wilt definiëren, gebruikt u het venster **Sectoren**.</span><span class="sxs-lookup"><span data-stu-id="5f8da-113">To define the industry groups, you use the **Industry Groups** window.</span></span>

1. <span data-ttu-id="5f8da-114">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Sectoren** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="5f8da-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Industry Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="5f8da-115">Kies de actie **Nieuw** en vul een code en een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="5f8da-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="5f8da-116">De code kan maximaal uit 11 tekens bestaan en kan elke combinatie zijn van cijfers en letters.</span><span class="sxs-lookup"><span data-stu-id="5f8da-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <span data-ttu-id="5f8da-117"><a name="AssignIndustryGroupContact">Sectoren toewijzen aan een contact</a></span><span class="sxs-lookup"><span data-stu-id="5f8da-117"><a name="AssignIndustryGroupContact"></a> To assign industry groups to a contact</span></span>
<span data-ttu-id="5f8da-118">U kunt geen sectoren toewijzen aan een contactpersoon, alleen aan contactbedrijven.</span><span class="sxs-lookup"><span data-stu-id="5f8da-118">You cannot assign industry groups to a contact person - only companies.</span></span>

1. <span data-ttu-id="5f8da-119">Open het contact.</span><span class="sxs-lookup"><span data-stu-id="5f8da-119">Open the contact.</span></span>
2. <span data-ttu-id="5f8da-120">Kies de actie **Bedrijf** en kies vervolgens de actie **Sectoren**.</span><span class="sxs-lookup"><span data-stu-id="5f8da-120">Choose the **Company** action, and then the **Industry Groups** action.</span></span> <span data-ttu-id="5f8da-121">Het venster **Contact sectoren** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="5f8da-121">The **Contact Industry Groups** window opens.</span></span>
3. <span data-ttu-id="5f8da-122">Selecteer in het veld **Sectorcode** de sectorgroepen die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="5f8da-122">In the **Industry Groups Code** field, select the industry groups you want to assign.</span></span>

<span data-ttu-id="5f8da-123">Herhaal deze stappen om het gewenste aantal sectoren toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="5f8da-123">Repeat these steps to assign as many industry groups as you want.</span></span> <span data-ttu-id="5f8da-124">U kunt sectoren ook toewijzen vanuit het contactoverzicht door dezelfde procedure te volgen.</span><span class="sxs-lookup"><span data-stu-id="5f8da-124">You can also assign industry groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="5f8da-125">Het aantal sectoren dat u aan het contact hebt toegewezen, wordt weergegeven in het veld **Aantal sectoren** in het gedeelte **Segmentatie** in het venster **Contact**.</span><span class="sxs-lookup"><span data-stu-id="5f8da-125">The number of industry groups that you have assigned to the contact is displayed in the **No. of Industry Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="5f8da-126">Nadat u sectoren hebt toegewezen aan de contacten, kunt u deze gegevens gebruiken om contacten voor de segmenten te selecteren.</span><span class="sxs-lookup"><span data-stu-id="5f8da-126">After you have assigned industry groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="5f8da-127">Zie voor meer informatie [Procedure: Contacten toevoegen aan segmenten](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="5f8da-127">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5f8da-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5f8da-128">See Also</span></span>
[<span data-ttu-id="5f8da-129">Contactbedrijven maken</span><span class="sxs-lookup"><span data-stu-id="5f8da-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="5f8da-130">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5f8da-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

