---
title: Kostenobjecten instellen | Microsoft Docs
description: Leer hoe u kostenobjecten instelt. Kostenobjecten lijken op dimensies voor het grootboek.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/13/2018
ms.author: sgroespe
redirect_url: finance-set-up-cost-accounting
ms.translationtype: HT
ms.sourcegitcommit: 67400e424305cc705db5c1bd52a8e4de17ecc5a9
ms.openlocfilehash: 28ab54dea21385083eb61e5dc8a7df44aef0ea21
ms.contentlocale: nl-be
ms.lasthandoff: 11/20/2018

---
# <a name="set-up-cost-objects"></a><span data-ttu-id="20667-103">Kostenobjecten instellen</span><span class="sxs-lookup"><span data-stu-id="20667-103">Set Up Cost Objects</span></span>
<span data-ttu-id="20667-104">Kostenobjecten zijn projecten, producten of diensten van een bedrijf.</span><span class="sxs-lookup"><span data-stu-id="20667-104">Cost objects are projects, products, or services of a company.</span></span> <span data-ttu-id="20667-105">Het schema van kostenobjecten is vergelijkbaar met de dimensiegegevens voor het grootboek.</span><span class="sxs-lookup"><span data-stu-id="20667-105">The chart of cost objects is similar to the dimension information for the general ledger.</span></span> <span data-ttu-id="20667-106">U kunt het schema van kostenobjecten op de volgende manieren instellen:</span><span class="sxs-lookup"><span data-stu-id="20667-106">You can set up the chart of cost objects in the following ways:</span></span>  

* <span data-ttu-id="20667-107">Door de dimensiewaarden in het grootboek over te brengen naar het schema van kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="20667-107">Transfer dimension values in the general ledger to the chart of cost objects.</span></span> <span data-ttu-id="20667-108">U kunt elke gewenste aanpassing na de overdracht aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="20667-108">You can make any necessary adjustments after the transfer.</span></span>  
* <span data-ttu-id="20667-109">Door een nieuw schema van kostenobjecten te maken dat onafhankelijk is van het grootboek of door een nieuw kostenobject toe te voegen aan een bestaand schema van kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="20667-109">Create a new chart of cost object that is independent of the general ledger or add a new cost object to an existing chart of cost objects.</span></span> <span data-ttu-id="20667-110">U moet elk kostenobject afzonderlijk maken.</span><span class="sxs-lookup"><span data-stu-id="20667-110">You must create each cost object individually.</span></span>  

## <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects"></a><span data-ttu-id="20667-111">Door de dimensiewaarden vanuit het grootboek over te brengen naar het schema van kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="20667-111">To transfer dimension values from the general ledger to the chart of cost objects</span></span>  
1.  <span data-ttu-id="20667-112">Stel een dimensie als kostenobjectdimensie in met het venster **CA-dimensies bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="20667-112">Set a dimension to be the cost object dimension in the **Update CA Dimensions** window.</span></span> <span data-ttu-id="20667-113">Alleen de waarden uit deze dimensie worden overgebracht.</span><span class="sxs-lookup"><span data-stu-id="20667-113">Only the values from this dimension are transferred.</span></span>  
2.  <span data-ttu-id="20667-114">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostenobjectschema** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="20667-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Objects**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="20667-115">Kies de actie **Kostenobjecten ophalen uit dimensie** om dimensiewaarden over te brengen naar het schema van kostenobjecten.</span><span class="sxs-lookup"><span data-stu-id="20667-115">Choose the **Get Cost Objects from Dimension** action to transfer dimension values to the chart of cost objects.</span></span> <span data-ttu-id="20667-116">Met deze functie worden de dimensiewaarden die u in stap 1 hebt gedefinieerd overgebracht.</span><span class="sxs-lookup"><span data-stu-id="20667-116">The function transfers the dimension values that you defined in step 1.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="20667-117">U kunt het veld **Kostenobjectdimensie afstemmen** zo instellen dat hiermee een eenrichtingssynchronisatie van dimensiewaarden uit het grootboek op het schema van kostenobjecten wordt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="20667-117">You can set up the **Align Cost Object Dimension**  field to define a one-way synchronization of dimension values from the general ledger to the chart of cost objects.</span></span> <span data-ttu-id="20667-118">U kunt geen synchronisatie van het schema van kostenobjecten met dimensiewaarden uit het grootboek definiëren.</span><span class="sxs-lookup"><span data-stu-id="20667-118">You cannot define a synchronization of the chart of cost objects to dimension values from the general ledger.</span></span>  

<span data-ttu-id="20667-119">Het schema van kostenobjecten bevat nu alle opgegeven dimensiewaarden van het grootboek waaronder titels en subtotalen.</span><span class="sxs-lookup"><span data-stu-id="20667-119">The chart of cost objects now contains all specified dimension values from the general ledger and includes titles and subtotals.</span></span>  

## <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-window"></a><span data-ttu-id="20667-120">Nieuwe kostenobjecten maken in het venster Kostenobjectschema</span><span class="sxs-lookup"><span data-stu-id="20667-120">To create new cost objects in the Chart of Cost Objects window</span></span>  
<span data-ttu-id="20667-121">U kunt kostenobjecten instellen en onderhouden op de kaart **Kostenobjectkaart** of in het venster **Kostenobjectschema**.</span><span class="sxs-lookup"><span data-stu-id="20667-121">You can set up and maintain cost objects in either the **Cost Object Card** card or in the **Chart of Cost Objects** window.</span></span> <span data-ttu-id="20667-122">In deze procedure stelt u kostenobjecten in het venster **Kostenobjectschema** in.</span><span class="sxs-lookup"><span data-stu-id="20667-122">In this procedure, you set up cost objects in the **Chart of Cost Objects** window.</span></span>  

1.  <span data-ttu-id="20667-123">Open het venster **Kostenobjectschema** in de bewerkmodus.</span><span class="sxs-lookup"><span data-stu-id="20667-123">Open the **Chart of Cost Objects** window in edit mode.</span></span>  
2.  <span data-ttu-id="20667-124">Voer in het veld **Code** de kostenobjectcode in.</span><span class="sxs-lookup"><span data-stu-id="20667-124">In the **Code** field, enter the cost object code.</span></span> <span data-ttu-id="20667-125">Alle kostenobjecten moeten een code hebben.</span><span class="sxs-lookup"><span data-stu-id="20667-125">All cost objects must have a code.</span></span>  
3.  <span data-ttu-id="20667-126">Voer in het veld **Naam** de naam van het kostenobject in.</span><span class="sxs-lookup"><span data-stu-id="20667-126">In the **Name** field, enter the cost object name.</span></span>  
4.  <span data-ttu-id="20667-127">Kies de vervolgkeuzepijl in het veld **Regelsoort** om het doel van het kostenobject aan te geven.</span><span class="sxs-lookup"><span data-stu-id="20667-127">Choose the drop-down arrow in the **Line Type** field to specify the purpose of the cost object.</span></span>  

    * <span data-ttu-id="20667-128">Voor kostenobjecten van het regelsoort **Totaal** vult u het veld **Totaal van/tot** in.</span><span class="sxs-lookup"><span data-stu-id="20667-128">For cost objects of the **Total** line type, fill in the **Total From/To** field.</span></span> <span data-ttu-id="20667-129">Gebruik de operator **of**, die uit een verticale lijn (**&#124;**) bestaat om bereiken voor kostenobjecten in te stellen.</span><span class="sxs-lookup"><span data-stu-id="20667-129">Use the **or** operator, which is a vertical line (**&#124;**), to set ranges of cost objects.</span></span>  
    * <span data-ttu-id="20667-130">Voor kostenobjecten van het regelsoort **Eindtotaal** wordt dit veld automatisch ingevuld wanneer u de inspringfunctie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="20667-130">For cost objects of the **End-Total** line type, this field is filled in automatically when you use  the indent function.</span></span>  
5.  <span data-ttu-id="20667-131">Vul het veld **Sorteervolgorde** in.</span><span class="sxs-lookup"><span data-stu-id="20667-131">Fill in the **Sorting Order** field.</span></span>  
6.  <span data-ttu-id="20667-132">Kies de volgende lege regel om een nieuw kostenobject te maken en herhaal vervolgens stap 2 tot en met 5.</span><span class="sxs-lookup"><span data-stu-id="20667-132">Chose the next empty line to create a new cost object, and then repeat steps 2 through 5.</span></span>  
7.  <span data-ttu-id="20667-133">Nadat u alle kostenobjecten hebt ingesteld, kiest u de actie **Kostenobjecten inspringen**.</span><span class="sxs-lookup"><span data-stu-id="20667-133">After you have set up all the cost objects, choose the **Indent Cost Objects** action.</span></span> <span data-ttu-id="20667-134">Kies de knop **Ja**.</span><span class="sxs-lookup"><span data-stu-id="20667-134">Choose the **Yes** button.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="20667-135">Als u definities in de velden **Totaal van/tot** voor de kostenobjecten **Eindtotaal** hebt ingevoerd voordat u de inspringfunctie uitvoert, moet u deze opnieuw invoeren.</span><span class="sxs-lookup"><span data-stu-id="20667-135">If you have entered definitions in the **Total From/To** fields for **End-Total** cost objects before you run the indent function, then you must enter them again.</span></span> <span data-ttu-id="20667-136">De functie overschrijft de waarden in alle velden **Eindtotaal**.</span><span class="sxs-lookup"><span data-stu-id="20667-136">The function overwrites the values in all **End-Total** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="20667-137">Zie ook</span><span class="sxs-lookup"><span data-stu-id="20667-137">See Also</span></span>  
[<span data-ttu-id="20667-138">Kosten verantwoorden</span><span class="sxs-lookup"><span data-stu-id="20667-138">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
<span data-ttu-id="20667-139">[Kostenplaatsen en kostenobjecten voor rekeningschema's definiëren](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="20667-139">[Defining Cost Centers and Cost Objects for Chart of Accounts](finance-defining-cost-centers-and-cost-objects-for-chart-of-accounts.md) </span></span>  
<span data-ttu-id="20667-140">[Saldi tussen kostensoort, kostenplaats en kostenobject](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span><span class="sxs-lookup"><span data-stu-id="20667-140">[Balances Between Cost Type, Cost Center, and Cost Object](finance-balances-between-cost-type-cost-center-and-cost-object.md) </span></span>  
<span data-ttu-id="20667-141">[Kostenboekhouding instellen](finance-set-up-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="20667-141">[Setting Up Cost Accounting](finance-set-up-cost-accounting.md) </span></span>  
<span data-ttu-id="20667-142">[Terminologie in kostprijsboekhouding](finance-terminology-in-cost-accounting.md) </span><span class="sxs-lookup"><span data-stu-id="20667-142">[Terminology in Cost Accounting](finance-terminology-in-cost-accounting.md) </span></span>  
[<span data-ttu-id="20667-143">Kostprijsboekhouding</span><span class="sxs-lookup"><span data-stu-id="20667-143">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
<span data-ttu-id="20667-144">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="20667-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

