---
title: De weergave van een rapport wijzigen door een andere lay-out te kiezen | Microsoft Docs
description: U kunt verschillende lay-outs voor een lijst gebruiken en schakelen tussen lay-outs om te bepalen hoe een rapport eruitziet.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: c9eb0f1270a431c0996bffdd610cdebeaf85c216
ms.openlocfilehash: 54cc709845a79f33034ced2e720948733216cc04
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-change-which-layout-is-currently-used-on-a-report"></a><span data-ttu-id="836d5-103">Procedure: Wijzigen welke lay-out momenteel in een rapport wordt gebruikt</span><span class="sxs-lookup"><span data-stu-id="836d5-103">How to: Change Which Layout is Currently Used on a Report</span></span>
<span data-ttu-id="836d5-104">Een rapport kan worden ingesteld met meerdere rapportlay-outs, waartussen u indien nodig kunt schakelen.</span><span class="sxs-lookup"><span data-stu-id="836d5-104">A report can be set up with more than one report layout, which you can then switch among as needed.</span></span>

<span data-ttu-id="836d5-105">Afhankelijk van de lay-outs die voor een rapport beschikbaar zijn, kunt u ervoor kiezen een ingebouwde RDLC-rapportlay-out, een ingebouwde Word-rapportlay-out of een aangepaste lay-out te maken.</span><span class="sxs-lookup"><span data-stu-id="836d5-105">Depending on the layouts that are available for a report, you can choose to use a built-in RDLC report layout, a built-in Word report layout, or a custom layout.</span></span> <span data-ttu-id="836d5-106">Zie [Rapportlay-outs beheren](ui-manage-report-layouts.md) voor meer informatie over RDLC- en Word-rapportlay-outs, ingebouwde en aangepaste lay-outs.</span><span class="sxs-lookup"><span data-stu-id="836d5-106">For more information about RDLC and Word report layouts, built-in and custom layouts, and more, see [Manage Report Layouts](ui-manage-report-layouts.md).</span></span>

## <a name="to-change-the-layout-that-is-used-on-a-report"></a><span data-ttu-id="836d5-107">De lay-out wijzigen die in een rapport wordt gebruikt</span><span class="sxs-lookup"><span data-stu-id="836d5-107">To change the layout that is used on a report</span></span>
1. <span data-ttu-id="836d5-108">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Search for Page or Report icon"), voer **Selectie van rapportlay-out** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="836d5-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Report Layout Selection**, and then choose the related link.</span></span>  
   <span data-ttu-id="836d5-109">Het venster **Selectie rapportlay-out** bevat een overzicht van alle rapporten die beschikbaar zijn voor het bedrijf dat in het veld Bedrijf boven aan het venster wordt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="836d5-109">The **Report Layout Selection** window lists all the reports that are available for the company that is specified in the Company field at the top of the window.</span></span> <span data-ttu-id="836d5-110">Met het veld Geselecteerde lay-out wordt de lay-out opgegeven die momenteel in het rapport wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="836d5-110">The Selected Layout field specifies the layout that is currently used on the report.</span></span>
2. <span data-ttu-id="836d5-111">Stel het veld **Bedrijf** boven in het venster in op het bedrijf dat het rapport bevat.</span><span class="sxs-lookup"><span data-stu-id="836d5-111">Set the **Company** field at the top of the window to the company that includes the report.</span></span>
3. <span data-ttu-id="836d5-112">Als u de lay-out wilt wijzigen die door een rapport wordt gebruikt, stelt u in de rij voor het rapport in de lijst het veld **Geselecteerde lay-out** in op een van de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="836d5-112">To change the layout that is used by a report, in the row for the report in the list, set the **Selected Layout** field to one of the following options:</span></span>
   * <span data-ttu-id="836d5-113">RDLC (ingebouwd), gebruikt de ingebouwde RDLC-rapportlay-out in het rapport.</span><span class="sxs-lookup"><span data-stu-id="836d5-113">RDLC (built-in), uses the built-in RDLC report layout on the report.</span></span>
   * <span data-ttu-id="836d5-114">Word (ingebouwd), gebruikt de ingebouwde Word-rapportlay-out in het rapport.</span><span class="sxs-lookup"><span data-stu-id="836d5-114">Word (built-in), uses the built-in Word report layout on the report.</span></span>
   * <span data-ttu-id="836d5-115">Aangepast, gebruikt een aangepaste lay-out in het rapport.</span><span class="sxs-lookup"><span data-stu-id="836d5-115">Custom, uses a custom layout on the report.</span></span>  
     <span data-ttu-id="836d5-116">U kunt zien welke aangepaste lay-outs voor het rapport beschikbaar zijn in het feitenblok Rapportlay-outonderdeel.</span><span class="sxs-lookup"><span data-stu-id="836d5-116">You can see which custom layouts are available for the report in the Report Layouts Part FactBox.</span></span> <span data-ttu-id="836d5-117">Als er geen aangepaste lay-outs voor het rapport zijn, moet u er eerst een maken.</span><span class="sxs-lookup"><span data-stu-id="836d5-117">If there are no custom layouts for the report, then you will have to create one first.</span></span> <span data-ttu-id="836d5-118">Als u deze optie kiest, gaat u naar de volgende procedure om de aangepaste lay-out op te geven die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="836d5-118">If you choose this option, go to the next procedure to specify the custom layout that you want to use.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="836d5-119">Als u **RDLC (ingebouwd)** of **Word (ingebouwd)** kiest en een foutbericht krijgt dat het rapport geen lay-out van de opgegeven soort heeft, moet u een andere lay-outoptie kiezen of een aangepaste rapportlay-out maken van het soort dat u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="836d5-119">If you choose **RDLC (built-in)** or **Word (built-in)** and you get an error message that the report does not have a layout of the specified type, then you must choose another layout option or create a custom report layout of the type that you want to use.</span></span>

<span data-ttu-id="836d5-120">Als u een ingebouwde RDLC- of Word-rapportlay-out hebt geselecteerd, is er verder geen actie vereist en wordt de lay-out gebruikt als het rapport de volgende keer wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="836d5-120">If you selected a built-in RDLC or Word report layout, then no further action is required and the layout will be used the next time the report is run.</span></span>

## <a name="to-specify-a-custom-layout-on-a-report"></a><span data-ttu-id="836d5-121">Een aangepaste lay-out opgeven voor een rapport</span><span class="sxs-lookup"><span data-stu-id="836d5-121">To specify a custom layout on a report</span></span>
1. <span data-ttu-id="836d5-122">U geeft vanuit het venster **Aangepaste rapportlay-outs** op welke aangepaste lay-out moet worden gebruikt in het rapport.</span><span class="sxs-lookup"><span data-stu-id="836d5-122">You specify which custom layout to use on the report from the **Custom Report Layouts** window.</span></span> <span data-ttu-id="836d5-123">Als het venster **Aangepaste rapportlay-outs** niet open is, kiest u in het veld **Beschrijving rapportlay-out** de opzoekknop.</span><span class="sxs-lookup"><span data-stu-id="836d5-123">If the **Custom Report Layouts** window is not open, then in the **Report Layout Description** field, choose the lookup button.</span></span>
2. <span data-ttu-id="836d5-124">Selecteer in het venster **Aangepaste rapportlay-outs** de rij voor de aangepaste lay-out die u wilt gebruiken, en sluit vervolgens het venster.</span><span class="sxs-lookup"><span data-stu-id="836d5-124">In the **Custom Report Layouts** window, select the row for custom layout that you want to use, and then close the window.</span></span>

<span data-ttu-id="836d5-125">U keert naar het venster **Selectie rapportlay-out** terug.</span><span class="sxs-lookup"><span data-stu-id="836d5-125">You return to the **Report Layout Selection** window.</span></span> <span data-ttu-id="836d5-126">De naam van de geselecteerde aangepaste lay-out wordt weergegeven in het veld **Beschrijving aangepaste lay-out**.</span><span class="sxs-lookup"><span data-stu-id="836d5-126">The name of the selected custom layout displays in the **Custom Layout Description** field.</span></span> <span data-ttu-id="836d5-127">De aangepaste lay-out wordt de volgende keer dat u het rapport uitvoert, gebruikt.</span><span class="sxs-lookup"><span data-stu-id="836d5-127">The custom layout will be used the next time that you run the report.</span></span>

## <a name="see-also"></a><span data-ttu-id="836d5-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="836d5-128">See Also</span></span>
[<span data-ttu-id="836d5-129">Rapportlay-outs beheren</span><span class="sxs-lookup"><span data-stu-id="836d5-129">Managing Report Layouts</span></span>](ui-manage-report-layouts.md)  
<span data-ttu-id="836d5-130">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="836d5-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

