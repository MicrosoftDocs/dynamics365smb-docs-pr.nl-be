---
title: Webbronnen voor contactbedrijven instellen | Microsoft Docs
description: "U kunt internet- of webbronnen definiëren en toewijzen aan een contactbedrijf om te helpen aangeven hoe u informatie wilt zoeken over uw contacten."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 6e78a86ba3d29948b07777d0a346c1ef58d088e6
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-web-sources-for-contact-companies"></a><span data-ttu-id="d62cc-103">Procedure: Webbronnen voor contactbedrijven instellen</span><span class="sxs-lookup"><span data-stu-id="d62cc-103">How to: Set Up Web Sources for Contact Companies</span></span>
<span data-ttu-id="d62cc-104">U kunt webbronnen gebruiken met uw contactbedrijven om bijvoorbeeld zoekengines en websites op internet aan te geven die u wilt gebruiken om informatie over de contacten te zoeken.</span><span class="sxs-lookup"><span data-stu-id="d62cc-104">You can use web sources with your contact companies to identify, for example, search engines and web sites, on the Internet that you want to use to search for information about the contacts.</span></span> <span data-ttu-id="d62cc-105">Als u webbronnen wilt toewijzen, moet u aangeven welk zoekprogramma en welk zoekwoord wordt gebruikt bij het zoeken naar de vereiste informatie.</span><span class="sxs-lookup"><span data-stu-id="d62cc-105">When assigning web sources, you specify which search engine and search word the application will use to find the requested information.</span></span>

<span data-ttu-id="d62cc-106">Webbronnen gebruiken voor contacten is een proces van twee stappen.</span><span class="sxs-lookup"><span data-stu-id="d62cc-106">Using web sources on contacts is a two-step process.</span></span> <span data-ttu-id="d62cc-107">Eerst definieert u de webbroncode.</span><span class="sxs-lookup"><span data-stu-id="d62cc-107">First, you define the web source code.</span></span> <span data-ttu-id="d62cc-108">U hoeft deze stap slechts eenmaal uit te voeren voor elke webbron.</span><span class="sxs-lookup"><span data-stu-id="d62cc-108">You only have to perform this step one time for each web source.</span></span> <span data-ttu-id="d62cc-109">Als u een webbroncode hebt, kunt u beginnen de code toe te wijzen aan contactpersonen.</span><span class="sxs-lookup"><span data-stu-id="d62cc-109">Once you have a web source code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-web-source-code"></a><span data-ttu-id="d62cc-110">Een webbroncode definiëren</span><span class="sxs-lookup"><span data-stu-id="d62cc-110">to define a web source code</span></span>
1. <span data-ttu-id="d62cc-111">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Webbronnen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="d62cc-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Web Sources**, and then choose the related link.</span></span>
2. <span data-ttu-id="d62cc-112">Kies de **Nieuw**-acties.</span><span class="sxs-lookup"><span data-stu-id="d62cc-112">Choose the **New** actions.</span></span>
3. <span data-ttu-id="d62cc-113">Vul de velden **Code**, **Omschrijving** en **URL** in.</span><span class="sxs-lookup"><span data-stu-id="d62cc-113">Fill in the **Code**, **Description**, and **URL** fields.</span></span>

    <span data-ttu-id="d62cc-114">Typ %1 in het veld **URL** om een tijdelijke aanduiding in te voegen voor een zoekwoord in de URL.</span><span class="sxs-lookup"><span data-stu-id="d62cc-114">Type %1 in the **URL** field to insert a placeholder for a search word in the URL.</span></span> <span data-ttu-id="d62cc-115">Wanneer u de webbron start vanaf een contact, wordt %1 automatisch vervangen door de zoekterm die u in het venster **Contact webbronnen** hebt ingevoerd, bijvoorbeeld de naam van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="d62cc-115">When you launch the web source from a contact, the %1 is replaced with the search word, for example, the name of the company that you have entered in the **Contact Web Sources** window.</span></span>

<span data-ttu-id="d62cc-116">Herhaal deze stappen om het gewenste aantal webbronnen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="d62cc-116">Repeat these steps to set up as many web sources as you want.</span></span>

## <a name="to-assign-web-sources-to-a-contact-company"></a><span data-ttu-id="d62cc-117">Webbronnen toewijzen aan een contactbedrijf</span><span class="sxs-lookup"><span data-stu-id="d62cc-117">to assign web sources to a contact company</span></span>
<span data-ttu-id="d62cc-118">Als u webbronnen wilt toewijzen, moet u aangeven welk zoekprogramma en welk zoekwoord wordt gebruikt bij het zoeken naar de vereiste informatie.</span><span class="sxs-lookup"><span data-stu-id="d62cc-118">When assigning web sources, you specify which search engine and search word that the application will use to find the requested information.</span></span>

1. <span data-ttu-id="d62cc-119">Open het contact.</span><span class="sxs-lookup"><span data-stu-id="d62cc-119">Open the contact.</span></span>
2. <span data-ttu-id="d62cc-120">Kies de actie **Bedrijf** en kies vervolgens de actie **Webbronnen**.</span><span class="sxs-lookup"><span data-stu-id="d62cc-120">Choose the **Company** action, and then choose the **Web Sources** action.</span></span> <span data-ttu-id="d62cc-121">Het venster **Contact webbronnen** wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="d62cc-121">The **Contact Web Sources** window opens.</span></span>
3. <span data-ttu-id="d62cc-122">Kies in het veld **Webbroncode** de webbron die u wilt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="d62cc-122">In the **Web Source Code** field, choose the web source you want to assign.</span></span>
4. <span data-ttu-id="d62cc-123">Voer in het veld **Zoekterm** de zoekterm in die moet worden gebruikt bij het zoeken naar de informatie.</span><span class="sxs-lookup"><span data-stu-id="d62cc-123">In the **Search Word** field, enter the search word that you want to use to find the information.</span></span>

<span data-ttu-id="d62cc-124">Herhaal deze stappen om het gewenste aantal webbronnen toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="d62cc-124">Repeat these steps to assign as many web sources as you want.</span></span>

<span data-ttu-id="d62cc-125">U kunt ook webbronnen toewijzen vanuit het venster **Contactoverzicht** door dezelfde procedure te volgen.</span><span class="sxs-lookup"><span data-stu-id="d62cc-125">You can also assign web sources from the **Contact List** window by following the same procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="d62cc-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d62cc-126">See Also</span></span>
[<span data-ttu-id="d62cc-127">Contactbedrijven maken</span><span class="sxs-lookup"><span data-stu-id="d62cc-127">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="d62cc-128">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d62cc-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

