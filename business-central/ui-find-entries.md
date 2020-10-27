---
title: Posten zoeken | Microsoft Docs
description: In dit artikel wordt beschreven hoe u gerelateerde documenten en posten zoekt
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: find
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 870cd32dc2408236ed8997e1f939c00d1bf519e4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927803"
---
# <a name="finding-related-entries-for-posted-documents"></a><span data-ttu-id="1d90d-103">Gerelateerde posten zoeken voor geboekte documenten</span><span class="sxs-lookup"><span data-stu-id="1d90d-103">Finding Related Entries for Posted Documents</span></span> 

<span data-ttu-id="1d90d-104">In dit artikel leert u hoe u documenten en posten kunt vinden die aan elkaar gerelateerd zijn op basis van gemeenschappelijke informatie, zoals:</span><span class="sxs-lookup"><span data-stu-id="1d90d-104">In this article, you learn how to find documents and entries that are related to each other based on a common information, like:</span></span>

- <span data-ttu-id="1d90d-105">Documentnummer of boekingsdatum</span><span class="sxs-lookup"><span data-stu-id="1d90d-105">Document number or posting date</span></span>
- <span data-ttu-id="1d90d-106">Type zakelijk contact, nummer of extern documentnummer</span><span class="sxs-lookup"><span data-stu-id="1d90d-106">Business contact type, number, or external document number</span></span>
- <span data-ttu-id="1d90d-107">Serienummer of lotnummer van artikel</span><span class="sxs-lookup"><span data-stu-id="1d90d-107">Item serial number or lot number</span></span>

<span data-ttu-id="1d90d-108">Deze functie is ook handig als u wilt zoeken naar posten uit bepaalde transacties.</span><span class="sxs-lookup"><span data-stu-id="1d90d-108">This feature is useful for finding the ledger entries that resulted from certain transactions.</span></span> <span data-ttu-id="1d90d-109">Wanneer u op documentnummer zoekt, kunt u het overzicht afdrukken vanuit het rapport Documentposten.</span><span class="sxs-lookup"><span data-stu-id="1d90d-109">When you search by document number, you can print the summary from the Document Entries report.</span></span>

## <a name="get-started"></a><span data-ttu-id="1d90d-110">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="1d90d-110">Get started</span></span>

<span data-ttu-id="1d90d-111">De functie voor het vinden van posten is beschikbaar op de meeste pagina's waarop geboekte documenten of geboekte documentenposten worden weergegeven, voor zowel lijsten als kaarten.</span><span class="sxs-lookup"><span data-stu-id="1d90d-111">The find entries feature is readily available on most pages that display posted documents or posted documents entries - for both lists and cards.</span></span> <span data-ttu-id="1d90d-112">Dus de eerste stap is het openen van een van deze pagina's.</span><span class="sxs-lookup"><span data-stu-id="1d90d-112">So the first step is open one of these pages.</span></span> <span data-ttu-id="1d90d-113">Kies vervolgens de actie **Posten zoeken** of druk op de toetsen Alt+G.</span><span class="sxs-lookup"><span data-stu-id="1d90d-113">Then, either choose the **Find Entries** action or press the Alt+G keys.</span></span>

<span data-ttu-id="1d90d-114">De pagina **Posten zoeken** bevat alle gerelateerde documenten en posten op basis van het documentnummer en de boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="1d90d-114">The **Find Entries** page  includes all related documents and entries based on the document no. and posting date.</span></span> <span data-ttu-id="1d90d-115">De pagina is onderverdeeld in drie secties:</span><span class="sxs-lookup"><span data-stu-id="1d90d-115">The page is divided into three sections:</span></span>

- <span data-ttu-id="1d90d-116">De bovenste sectie bevat velden en acties die u gebruikt om uw zoekopdracht te filteren.</span><span class="sxs-lookup"><span data-stu-id="1d90d-116">The top section displays fields and actions that you use for filtering your search.</span></span>
- <span data-ttu-id="1d90d-117">In de middelste sectie worden gerelateerde documenten weergegeven op basis van de zoekopdracht.</span><span class="sxs-lookup"><span data-stu-id="1d90d-117">The middle section displays related documents based on the search.</span></span>
- <span data-ttu-id="1d90d-118">De onderste sectie geeft informatie weer over het brondocument dat is gevonden door te zoeken.</span><span class="sxs-lookup"><span data-stu-id="1d90d-118">The bottom section displays information about the source document that was found by searching.</span></span>


<!--
 There are two ways to open this page:

- Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Find Entries**, and then choose the related link.

    With this way, the **Find Entries** page might be empty, and you'll have to start searching for entries from scratch.
    
- Open a page that displays posted documents or posted documents entries, either a list or a card. Then, locate and select the **Find Entries** action.

    With this way, the **Find Entries**, page will include all related documents and entries based on the document no. and posting date.


    > [!TIP]
    > If you are on a page that has the **Find Entries** action, press crtl+G to open the **Find Entries** page directly. 
-->

## <a name="search-for-entries"></a><span data-ttu-id="1d90d-119">Zoeken naar posten</span><span class="sxs-lookup"><span data-stu-id="1d90d-119">Search for entries</span></span>

<span data-ttu-id="1d90d-120">U kunt posten zoeken op basis van informatie over het document, de zakelijke contactpersoon of de artikelreferentie.</span><span class="sxs-lookup"><span data-stu-id="1d90d-120">You can search for entries based on information about either the document, business contact, or item reference.</span></span> <span data-ttu-id="1d90d-121">Als u de zoekopdracht wilt wijzigen, selecteert u **Acties** , **Zoeken op** en vervolgens een van de volgende acties:</span><span class="sxs-lookup"><span data-stu-id="1d90d-121">To change the search, select **Actions** , **Find By** , then one of the following actions:</span></span>

|<span data-ttu-id="1d90d-122">Actie</span><span class="sxs-lookup"><span data-stu-id="1d90d-122">Action</span></span>|<span data-ttu-id="1d90d-123">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="1d90d-123">Description</span></span>|
|------|-----------|
|<span data-ttu-id="1d90d-124">Zoeken op document</span><span class="sxs-lookup"><span data-stu-id="1d90d-124">Find by Document</span></span>|<span data-ttu-id="1d90d-125">Bekijk posten op basis van een specifiek documentnummer of boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="1d90d-125">View entries based on a specific document number or posting date.</span></span>|
|<span data-ttu-id="1d90d-126">Zakelijke contactpersoon</span><span class="sxs-lookup"><span data-stu-id="1d90d-126">Business Contact</span></span> |<span data-ttu-id="1d90d-127">Bekijk posten op basis van een specifiek contacttype, contactnummer, en/of extern documentnummer.</span><span class="sxs-lookup"><span data-stu-id="1d90d-127">View entries based on a specific contact type, contact number, anr/or external document number.</span></span> <span data-ttu-id="1d90d-128">U kunt documentgegevens invoeren die zijn toegewezen door een leverancier of klant.</span><span class="sxs-lookup"><span data-stu-id="1d90d-128">You can enter document information that was assigned by a vendor or a customer.</span></span> <span data-ttu-id="1d90d-129">Gebruik de beschikbare velden om te zoeken naar leveranciersdocumenten met de nummers die de leverancier aan de documenten heeft toegewezen.</span><span class="sxs-lookup"><span data-stu-id="1d90d-129">Use the available fields to search for vendor documents by using the numbers that the vendor has assigned the documents.</span></span>|
|<span data-ttu-id="1d90d-130">Artikelreferentie</span><span class="sxs-lookup"><span data-stu-id="1d90d-130">Item reference</span></span>|<span data-ttu-id="1d90d-131">Bekijk posten op basis van een serienummer of lotnummer.</span><span class="sxs-lookup"><span data-stu-id="1d90d-131">View entires based on a serial number or lot number.</span></span> <span data-ttu-id="1d90d-132">U kunt het lotnummer of serienummer invoeren of filteren op het lotnummer of serienummer waarnaar u wilt zoeken.</span><span class="sxs-lookup"><span data-stu-id="1d90d-132">You can enter the lot number or serial number, or filter on the lot number or serial number that you want to search for.</span></span> <span data-ttu-id="1d90d-133">Deze actie is handig om te zien of een bepaald artikeltraceringsnummer is gebruikt, van welke leverancier het afkomstig is of aan welke klant het is verkocht.</span><span class="sxs-lookup"><span data-stu-id="1d90d-133">This action is useful to see where a specific item tracking number was used, what vendor it came from, or what customer it was sold to.</span></span>|

<span data-ttu-id="1d90d-134">Nadat u een selectie hebt gemaakt, voert u de relevante zoekinformatie in de velden bovenaan in.</span><span class="sxs-lookup"><span data-stu-id="1d90d-134">After you make a selection, enter the relevant search information in the fields at the top.</span></span> <span data-ttu-id="1d90d-135">Gebruik de knopinfo van de velden om te helpen.</span><span class="sxs-lookup"><span data-stu-id="1d90d-135">Use the tooltips on the fields to help.</span></span> <span data-ttu-id="1d90d-136">Kies als u klaar bent **Zoeken** om het zoeken te starten.</span><span class="sxs-lookup"><span data-stu-id="1d90d-136">When you're finished, choose **Find** to start the search.</span></span> <span data-ttu-id="1d90d-137">Als u een filter wijzigt, moet u opnieuw **Zoeken** kiezen.</span><span class="sxs-lookup"><span data-stu-id="1d90d-137">If you change any of the filters, you have to choose **Find** again.</span></span>

> [!TIP]
> <span data-ttu-id="1d90d-138">Voor een paar voorbeelden over het gebruik van **Posten zoeken** raadpleegt u [Artikelen met artikeltracering traceren](inventory-how-to-trace-item-tracked-items.md) en [Procedure: Serie-/lotnummers traceren](walkthrough-tracing-serial-lot-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="1d90d-138">For a couple examples about using **Find Entries** , see [Trace Item-Tracked Items](inventory-how-to-trace-item-tracked-items.md) and [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="1d90d-139">Zie Gerelateerde training op [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="1d90d-139">See Related Training at [Microsoft Learn](/learn/modules/user-interface-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="1d90d-140">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1d90d-140">See Also</span></span>

[<span data-ttu-id="1d90d-141">Werken met Business Central</span><span class="sxs-lookup"><span data-stu-id="1d90d-141">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="1d90d-142">Een pagina-actie toevoegen aan uw rolcentrum</span><span class="sxs-lookup"><span data-stu-id="1d90d-142">Add a Page Action to Your Role Center</span></span>](ui-bookmarks.md)  
[<span data-ttu-id="1d90d-143">Artikelen met artikeltracering traceren</span><span class="sxs-lookup"><span data-stu-id="1d90d-143">Trace Item-Tracked Items</span></span>](inventory-how-to-trace-item-tracked-items.md)  
