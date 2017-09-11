---
title: "Zoekcriteria in filters definiëren | Microsoft Docs"
description: Beschrijft hoe u met filters werkt, zoals het Snelfilter, om de resultaten te verfijnen die u krijgt wanneer u gegevens zoekt.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 86ca45493081d9dbd229548f7c560e1df4e1c7c3
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017

---
# <a name="entering-criteria-in-filters"></a><span data-ttu-id="51a92-103">Criteria in filters invoeren</span><span class="sxs-lookup"><span data-stu-id="51a92-103">Entering Criteria in Filters</span></span>
<span data-ttu-id="51a92-104">Wanneer u naar gegevens, zoals klantnamen, adressen of productgroepen wilt zoeken, voert u criteria in.</span><span class="sxs-lookup"><span data-stu-id="51a92-104">When you want to search for data, such as customer names, addresses, or product groups, you enter criteria.</span></span> <span data-ttu-id="51a92-105">In zoekcriteria kunt u alle cijfers en letters gebruiken die u normaal in het specifieke veld gebruikt.</span><span class="sxs-lookup"><span data-stu-id="51a92-105">In search criteria you can use all the numbers and letters that you normally use in the specific field.</span></span> <span data-ttu-id="51a92-106">Daarnaast kunt u speciale symbolen gebruiken om de resultaten verder te filteren.</span><span class="sxs-lookup"><span data-stu-id="51a92-106">In addition, you can use special symbols to further filter the results.</span></span>

## <a name="searching-using-the-quick-filter"></a><span data-ttu-id="51a92-107">Zoeken met het Snelfilter</span><span class="sxs-lookup"><span data-stu-id="51a92-107">Searching using the Quick Filter</span></span>
<span data-ttu-id="51a92-108">U kunt filters toevoegen aan alle pagina's met het Snelfilter.</span><span class="sxs-lookup"><span data-stu-id="51a92-108">You can add filters to all pages by using the Quick Filter.</span></span> <span data-ttu-id="51a92-109">Het Snelfilter wordt ingeschakeld door het vergrootglaspictogram in de rechterbovenhoek van een pagina te kiezen.</span><span class="sxs-lookup"><span data-stu-id="51a92-109">The Quick Filter is enabled by choosing the magnifier icon in the top right corner of a page.</span></span> <span data-ttu-id="51a92-110">Dit type filter wordt gebruikt voor een snelle invoer van criteria.</span><span class="sxs-lookup"><span data-stu-id="51a92-110">This filtering type is used for a fast entry of criteria.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="51a92-111">Het snelfilter biedt een eenvoudig toegang tot filtergegevens door onbewerkte tekst in te voeren, maar biedt ook veel opties voor zoekcriteria.</span><span class="sxs-lookup"><span data-stu-id="51a92-111">The Quick Filter provides an easy access to filter data by entering plain text, but does also provide a lot of search criteria options.</span></span> <span data-ttu-id="51a92-112">Afhankelijk van of u normale tekst of tekst met symbolen invoert, werkt het snelfilter anders.</span><span class="sxs-lookup"><span data-stu-id="51a92-112">Depending on whether you enter plain text or text including symbols, the Quick Filter behaves differently.</span></span>  

* <span data-ttu-id="51a92-113">Als u gewone tekst in de zoekcriteria opgeeft, worden de zoekcriteria geïnterpreteerd als een hoofdletterongevoelige zoekactie die bepaalde tekst bevat.</span><span class="sxs-lookup"><span data-stu-id="51a92-113">If you enter plain text in the search criteria, the search criteria is interpreted as a case insensitive search that contains certain text.</span></span>  
* <span data-ttu-id="51a92-114">Als u tekst inclusief symbolen in de zoekcriteria opgeeft, worden de zoekcriteria precies zo geïnterpreteerd als u ze hebt ingevoerd en wordt onderscheid gemaakt tussen hoofdletters en kleine letters.</span><span class="sxs-lookup"><span data-stu-id="51a92-114">If you enter text including symbols in the search criteria, the search criteria is interpreted exactly as you entered it, and the search is case sensitive.</span></span>

### <a name="quick-filter-criteria"></a><span data-ttu-id="51a92-115">Snelfiltercriteria</span><span class="sxs-lookup"><span data-stu-id="51a92-115">Quick filter criteria</span></span>
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH><span data-ttu-id="51a92-116">Zoekcriteria</span><span class="sxs-lookup"><span data-stu-id="51a92-116">Search Criteria</span></span></TH>
    <TH><span data-ttu-id="51a92-117">Geïnterpreteerd als...</span><span class="sxs-lookup"><span data-stu-id="51a92-117">Interpreted as...</span></span></TH>
    <TH><span data-ttu-id="51a92-118">Retourneert...</span><span class="sxs-lookup"><span data-stu-id="51a92-118">Returns...</span></span></TH>
  </TR>
  <TR>
    <TD><span data-ttu-id="51a92-119">man</span><span class="sxs-lookup"><span data-stu-id="51a92-119">man</span></span></TD>
    <TD><span data-ttu-id="51a92-120">@&#42;man&#42;</span><span class="sxs-lookup"><span data-stu-id="51a92-120">@&#42;man&#42;</span></span></TD>
    <TD><span data-ttu-id="51a92-121">Alle records met de tekst <b>man</b> en ongevoelig voor hoofdletters en kleine letters.</span><span class="sxs-lookup"><span data-stu-id="51a92-121">All records that contain the text <b>man</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="51a92-122">se</span><span class="sxs-lookup"><span data-stu-id="51a92-122">se</span></span></TD>
    <TD><span data-ttu-id="51a92-123">@&#42;zo&#42;</span><span class="sxs-lookup"><span data-stu-id="51a92-123">@&#42;se&#42;</span></span></TD>
    <TD><span data-ttu-id="51a92-124">Alle records met de tekst <b>se</b> en ongevoelig voor hoofdletters en kleine letters.</span><span class="sxs-lookup"><span data-stu-id="51a92-124">All records that contain the text <b>se</b> and case insensitive.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="51a92-125">Man&#42;</span><span class="sxs-lookup"><span data-stu-id="51a92-125">Man&#42;</span></span></TD>
    <TD><span data-ttu-id="51a92-126">Begint met <b>Man</b> en is hoofdlettergevoelig.</span><span class="sxs-lookup"><span data-stu-id="51a92-126">Starts with <b>Man</b> and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="51a92-127">Alle records die beginnen met de tekst <b>Man</b>.</span><span class="sxs-lookup"><span data-stu-id="51a92-127">All records that start with the text <b>Man</b>.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="51a92-128">'man'</span><span class="sxs-lookup"><span data-stu-id="51a92-128">'man'</span></span></TD>
    <TD><span data-ttu-id="51a92-129">Een exacte tekst en gevoelig voor hoofdletters en kleine letters.</span><span class="sxs-lookup"><span data-stu-id="51a92-129">An exact text and case sensitive.</span></span></TD>
    <TD><span data-ttu-id="51a92-130">Alle records die precies overeenkomen met <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="51a92-130">All records that match <b>man</b> exactly.</span></span></TD>
  </TR>
  <TR>
    <TD><span data-ttu-id="51a92-131">@man*</span><span class="sxs-lookup"><span data-stu-id="51a92-131">@man*</span></span> </TD>
    <TD><span data-ttu-id="51a92-132">Begint met en is niet hoofdlettergevoelig.</span><span class="sxs-lookup"><span data-stu-id="51a92-132">Starts with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="51a92-133">Alle records die beginnen met <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="51a92-133">All records that start with <b>man</b>.</span></span></TD>
  </TR>
    <TR>
    <TD><span data-ttu-id="51a92-134">@&#42;man</span><span class="sxs-lookup"><span data-stu-id="51a92-134">@&#42;man</span></span></TD>
    <TD><span data-ttu-id="51a92-135">Eindigt met en is niet hoofdlettergevoelig.</span><span class="sxs-lookup"><span data-stu-id="51a92-135">Ends with and case insensitive.</span></span></TD>
    <TD><span data-ttu-id="51a92-136">Alle records die eindigen met <b>man</b>.</span><span class="sxs-lookup"><span data-stu-id="51a92-136">All records that end with <b>man</b>.</span></span></TD>
  </TR>
</TABLE>

> [!NOTE]  
>   <span data-ttu-id="51a92-137">U kunt geen jokerteken gebruiken bij het filteren op opsommingsvelden, zoals het veld **Status** op verkooporders.</span><span class="sxs-lookup"><span data-stu-id="51a92-137">You cannot use a wildcard when filtering on enumeration fields, such as the **Status** field on sales orders.</span></span> <span data-ttu-id="51a92-138">Om een filter voor deze veldsoort in te voeren, kunt u de numerieke waarde als een filterparameter invoeren.</span><span class="sxs-lookup"><span data-stu-id="51a92-138">To enter a filter for this type of field, you can enter the numeric value as a filtering parameter.</span></span> <span data-ttu-id="51a92-139">Bijvoorbeeld: gebruik in het veld **Status** op een verkooporder met de waarden **Open**, **Vrijgegeven**, **Wacht op goedkeuring** en **Wacht op vooruitbetaling** de waarden **0**, **1**, **2** en **3** om voor deze opties te filteren.</span><span class="sxs-lookup"><span data-stu-id="51a92-139">For example, in the **Status** field on a sales order that has the values **Open**, **Released**, **Pending Approval**, and **Pending Prepayment**, use the values **0**, **1**, **2**, and **3** to filter for these options.</span></span>  

## <a name="see-also"></a><span data-ttu-id="51a92-140">Zie ook</span><span class="sxs-lookup"><span data-stu-id="51a92-140">See Also</span></span>
<span data-ttu-id="51a92-141">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="51a92-141">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

