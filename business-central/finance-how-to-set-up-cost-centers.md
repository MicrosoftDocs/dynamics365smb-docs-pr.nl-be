---
title: Kostenplaatsen instellen | Microsoft Docs
description: Kostenplaatsen zijn afdelingen die verantwoordelijk zijn voor kosten en opbrengsten. Het schema van kostenplaatsen is vergelijkbaar met de dimensiegegevens voor het grootboek.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 7362518cbade8132fb07f49e7b2e9be67c4bce29
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-cost-centers"></a><span data-ttu-id="59e55-104">Kostenplaatsen instellen</span><span class="sxs-lookup"><span data-stu-id="59e55-104">Set Up Cost Centers</span></span>
<span data-ttu-id="59e55-105">Kostenplaatsen zijn afdelingen die verantwoordelijk zijn voor kosten en opbrengsten.</span><span class="sxs-lookup"><span data-stu-id="59e55-105">Cost centers are departments that are responsible for costs and income.</span></span> <span data-ttu-id="59e55-106">Het schema van kostenplaatsen is vergelijkbaar met de dimensiegegevens voor het grootboek.</span><span class="sxs-lookup"><span data-stu-id="59e55-106">The chart of cost centers is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="59e55-107">U kunt het schema van kostenplaatsen op de volgende manieren instellen:</span><span class="sxs-lookup"><span data-stu-id="59e55-107">You can set up the chart of cost centers in the following ways:</span></span>  

-   <span data-ttu-id="59e55-108">Door de dimensiewaarden in het grootboek over te brengen naar het schema van kostenplaatsen.</span><span class="sxs-lookup"><span data-stu-id="59e55-108">Transfer dimension values in the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="59e55-109">U kunt elke gewenste aanpassing na de overdracht aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="59e55-109">You can make any necessary adjustments after the transfer.</span></span>  
-   <span data-ttu-id="59e55-110">Door een nieuw schema van kostenplaatsen te maken dat onafhankelijk is van het grootboek of door een nieuwe kostenplaats toe te voegen aan een bestaand schema van kostenplaatsen.</span><span class="sxs-lookup"><span data-stu-id="59e55-110">Create a new chart of cost center that is independent of the general ledger or add a new cost center to an existing chart of cost center.</span></span> <span data-ttu-id="59e55-111">U moet elke kostenplaats afzonderlijk maken.</span><span class="sxs-lookup"><span data-stu-id="59e55-111">You must create each cost center individually.</span></span>  

## <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers"></a><span data-ttu-id="59e55-112">Dimensiewaarden in het grootboek overbrengen naar het schema van kostenplaatsen</span><span class="sxs-lookup"><span data-stu-id="59e55-112">To transfer dimension values in the general ledger to the chart of cost centers</span></span>  
1.  <span data-ttu-id="59e55-113">Stel een dimensie als kostenplaats in met het venster **Dimensies kostprijsboekhouding bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="59e55-113">Set up a dimension to be the cost center dimension in the **Update Cost Acctg. Dimensions** window.</span></span> <span data-ttu-id="59e55-114">Alleen de waarden uit deze dimensie worden overgebracht.</span><span class="sxs-lookup"><span data-stu-id="59e55-114">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="59e55-115">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostenplaatsschema** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="59e55-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Centers**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="59e55-116">Op het tabblad **Acties** in de groep **Functies** kiest u **Kostenplaatsen ophalen uit dimensie** om dimensiewaarden over te brengen naar het schema van kostenplaatsen.</span><span class="sxs-lookup"><span data-stu-id="59e55-116">On the **Actions** tab, in the **Functions** group, choose **Get Cost Centers from Dimension** to transfer dimension values to the chart of cost centers.</span></span> <span data-ttu-id="59e55-117">Met deze functie worden de dimensiewaarden die u in stap 1 hebt gedefinieerd overgebracht.</span><span class="sxs-lookup"><span data-stu-id="59e55-117">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="59e55-118">U kunt het veld **Kostenplaatsdimensie afstemmen** zo instellen dat hiermee een eenrichtingssynchronisatie van dimensiewaarden uit het grootboek op het kostenplaatsschema wordt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="59e55-118">You can set up the **Align Cost Center Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost centers.</span></span> <span data-ttu-id="59e55-119">U kunt geen synchronisatie van het schema van kostenplaatsen met dimensiewaarden uit het grootboek definiëren.</span><span class="sxs-lookup"><span data-stu-id="59e55-119">You cannot define a synchronization of the chart of cost centers to dimension values from the general ledger.</span></span>  

<span data-ttu-id="59e55-120">Het schema van kostenplaatsen bevat nu alle opgegeven dimensiewaarden van het grootboek waaronder titels en subtotalen.</span><span class="sxs-lookup"><span data-stu-id="59e55-120">The chart of cost centers now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-window"></a><span data-ttu-id="59e55-121">Nieuwe kostenplaatsen maken in het venster Kostenplaatsschema</span><span class="sxs-lookup"><span data-stu-id="59e55-121">To create new cost centers in the Chart of Cost Centers window</span></span>  
<span data-ttu-id="59e55-122">U kunt kostenplaatsen instellen en onderhouden op de kaart **Kostenplaatskaart** of in het venster **Kostenplaatsschema**.</span><span class="sxs-lookup"><span data-stu-id="59e55-122">You can set up and maintain cost centers in either the **Cost Center Card** card or in the **Chart of Cost Centers** window.</span></span> <span data-ttu-id="59e55-123">In deze procedure stelt u kostenplaatsen in het venster **Kostenplaatsschema** in.</span><span class="sxs-lookup"><span data-stu-id="59e55-123">In this procedure, you set up cost centers in the **Chart of Cost Centers** window.</span></span>  

1. <span data-ttu-id="59e55-124">Open het venster **Kostenplaatsschema** in de bewerkmodus.</span><span class="sxs-lookup"><span data-stu-id="59e55-124">Open the **Chart of Cost Centers** window in edit mode.</span></span>  
2. <span data-ttu-id="59e55-125">Voer in het veld **Code** de kostenplaatscode in.</span><span class="sxs-lookup"><span data-stu-id="59e55-125">In the **Code** field, enter the cost center code.</span></span> <span data-ttu-id="59e55-126">Alle kostenplaatsen moeten een code hebben.</span><span class="sxs-lookup"><span data-stu-id="59e55-126">All cost centers must have a code.</span></span>  
3. <span data-ttu-id="59e55-127">Voer in het veld **Naam** de naam van de kostenplaats in.</span><span class="sxs-lookup"><span data-stu-id="59e55-127">In the **Name** field, enter the cost center name.</span></span>  
4. <span data-ttu-id="59e55-128">Kies de vervolgkeuzepijl in het veld **Regelsoort** om het doel van de kostenplaats aan te geven.</span><span class="sxs-lookup"><span data-stu-id="59e55-128">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost center.</span></span>  

    - <span data-ttu-id="59e55-129">Voor kostenplaatsen van het soort **Totaal** moet u het veld **Samentelling** invullen.</span><span class="sxs-lookup"><span data-stu-id="59e55-129">For cost centers of the **Total** type, you must fill in the **Totaling** field.</span></span> <span data-ttu-id="59e55-130">Gebruik de operator **of**, die uit een verticale lijn (**&#124;**) bestaat om bereiken voor kostenplaatsen in te stellen.</span><span class="sxs-lookup"><span data-stu-id="59e55-130">Use the **or** operator, which is a vertical line (**&#124;**) to set ranges of cost centers.</span></span>  
    - <span data-ttu-id="59e55-131">Voor kostenplaatsen van het regelsoort **Eindtotaal** wordt dit veld automatisch ingevuld wanneer u de inspringfunctie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="59e55-131">For cost centers of the **End-Total** line type, this field is filled in automatically when you use the indent function.</span></span>  
5.  <span data-ttu-id="59e55-132">Vul de velden **Sorteervolgorde** en **Kostensubtype** in.</span><span class="sxs-lookup"><span data-stu-id="59e55-132">Fill in the **Sorting Order** and **Cost Subtype** fields.</span></span>  
6.  <span data-ttu-id="59e55-133">Kies de volgende lege regel om een nieuwe kostenplaats te maken en herhaal vervolgens stap 2 tot en met 5.</span><span class="sxs-lookup"><span data-stu-id="59e55-133">Choose the next empty line to create a new cost center, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="59e55-134">Nadat u alle kostenplaatsen hebt ingesteld, kiest u de actie **Kostenplaatsen inspringen**.</span><span class="sxs-lookup"><span data-stu-id="59e55-134">After you have set up all the cost centers, choose the **Indent Cost Centers** action.</span></span> <span data-ttu-id="59e55-135">Kies de knop **Ja**.</span><span class="sxs-lookup"><span data-stu-id="59e55-135">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="59e55-136">Als u definities in de velden **Samentelling** voor de kostenplaatsen **Eindtotaal** hebt ingevoerd voordat u de inspringfunctie uitvoerde, moet u deze opnieuw invoeren.</span><span class="sxs-lookup"><span data-stu-id="59e55-136">If you have entered definitions in the **Totaling** fields for **End-Total** cost centers before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="59e55-137">De functie overschrijft de waarden in alle velden **Eindtotaal**.</span><span class="sxs-lookup"><span data-stu-id="59e55-137">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="59e55-138">Zie ook</span><span class="sxs-lookup"><span data-stu-id="59e55-138">See Also</span></span>  
[<span data-ttu-id="59e55-139">Kosten verantwoorden</span><span class="sxs-lookup"><span data-stu-id="59e55-139">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="59e55-140">[Kostenboekhouding instellen](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="59e55-140">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="59e55-141">[Terminologie in kostprijsboekhouding](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="59e55-141">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="59e55-142">Kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="59e55-142">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="59e55-143">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="59e55-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

