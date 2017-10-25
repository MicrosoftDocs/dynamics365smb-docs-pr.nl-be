---
title: 'Procedure: Vooruitbetalingsfacturen maken | Microsoft Docs'
description: Leer omgaan met situaties waarin u of uw leverancier vooruitbetaling verlangt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 04d7703df0c1b5e4da8996f00b5f1eed293cbf56
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-prepayment-invoices"></a><span data-ttu-id="93021-103">Procedure: vooruitbetalingsfacturen maken</span><span class="sxs-lookup"><span data-stu-id="93021-103">How to: Create Prepayment Invoices</span></span>
<span data-ttu-id="93021-104">Als uw klanten u moeten betalen voordat u een order naar ze verzendt of als uw leverancier wil dat u betaalt voordat een order naar u wordt verzonden, kunt u de functie voor vooruitbetalingen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="93021-104">If you require your customers to submit payment before you ship an order to them, or if your vendor requires you to submit payment before they ship an order to you, you can use the prepayment functionality.</span></span>  

<span data-ttu-id="93021-105">Nadat u een verkoop- of inkooporder hebt gemaakt, kunt u een vooruitbetalingsnota maken.</span><span class="sxs-lookup"><span data-stu-id="93021-105">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="93021-106">U kunt de standaardpercentages gebruiken voor elke verkoop- of inkoopregel, of u kunt het bedrag naar wens aanpassen.</span><span class="sxs-lookup"><span data-stu-id="93021-106">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="93021-107">U kunt bijvoorbeeld een totaalbedrag opgeven voor de hele order.</span><span class="sxs-lookup"><span data-stu-id="93021-107">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="93021-108">In de volgende procedure wordt beschreven hoe u een vooruitbetaling voor een verkooporder factureert.</span><span class="sxs-lookup"><span data-stu-id="93021-108">The following procedure describes how to invoice a prepayment for a sales orders.</span></span> <span data-ttu-id="93021-109">De stappen zijn vergelijkbaar voor inkooporders.</span><span class="sxs-lookup"><span data-stu-id="93021-109">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="93021-110">Een vooruitbetalingsfactuur maken</span><span class="sxs-lookup"><span data-stu-id="93021-110">To create a prepayment invoice</span></span>  
1. <span data-ttu-id="93021-111">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkooporders** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="93021-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="93021-112">Maak een nieuwe verkooporder.</span><span class="sxs-lookup"><span data-stu-id="93021-112">Create a new sales order.</span></span> <span data-ttu-id="93021-113">Zie [Procedure: Producten verkopen](sales-how-sell-products.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="93021-113">For more information, see [How to: sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="93021-114">Op het sneltabblad **Vooruitbetaling**, wordt het veld **vooruitbetaling %** op de kop automatisch ingevuld als de klantenkaart een standaardvooruitbetalingspercentage bevat.</span><span class="sxs-lookup"><span data-stu-id="93021-114">On the **Prepayment** FastTab, the **Prepayment %** field will be filled in automatically if there is a default prepayment percentage on the customer card.</span></span> <span data-ttu-id="93021-115">U kunt de inhoud van het veld wijzigen.</span><span class="sxs-lookup"><span data-stu-id="93021-115">You can change the contents of the field.</span></span> <span data-ttu-id="93021-116">Het vooruitbetalingspercentage wordt alleen vanuit de kop gekopieerd naar regels waarnaar het standaardvooruitbetalingspercentage van het artikel niet wordt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="93021-116">The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.</span></span>  

    <span data-ttu-id="93021-117">Een vinkje in het veld **Vooruitbetaling comprimeren** betekent dat regels worden gecombineerd op de factuur in de volgende gevallen:</span><span class="sxs-lookup"><span data-stu-id="93021-117">If the **Compress Prepayment** field is selected, lines will be combined on the invoice if:</span></span>  
    - <span data-ttu-id="93021-118">Ze hebben dezelfde grootboekrekening voor vooruitbetalingen zoals bepaald door de boekingsgroepinstellingen.</span><span class="sxs-lookup"><span data-stu-id="93021-118">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="93021-119">Ze hebben dezelfde dimensies.</span><span class="sxs-lookup"><span data-stu-id="93021-119">They have the same dimensions.</span></span>  

    <span data-ttu-id="93021-120">Laat het veld leeg als u een vooruitbetalingsnota wilt opgeven met één regel voor elke verkooporderregel die een vooruitbetalingspercentage heeft.</span><span class="sxs-lookup"><span data-stu-id="93021-120">Leave the field blank if you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage.</span></span>  

3. <span data-ttu-id="93021-121">Vul de verkoopregels in.</span><span class="sxs-lookup"><span data-stu-id="93021-121">Fill in the sales lines.</span></span>  

    <span data-ttu-id="93021-122">Als er standaardvooruitbetalingspercentages zijn ingesteld voor uw artikelen, wordt de standaardwaarde automatisch naar het veld **Vooruitbetaling %** op de regel gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="93021-122">If default prepayment percentages have been set up for your items, they are automatically copied to the **Prepayment %** field on the line.</span></span> <span data-ttu-id="93021-123">Zo niet, dan wordt het vooruitbetalingspercentage gekopieerd uit de kop.</span><span class="sxs-lookup"><span data-stu-id="93021-123">Otherwise, the prepayment percentage is copied from the header.</span></span> <span data-ttu-id="93021-124">U kunt de inhoud van het veld **Vooruitbetaling %** op de regel wijzigen.</span><span class="sxs-lookup"><span data-stu-id="93021-124">You can change the contents of the **Prepayment %** field on the line.</span></span>  
4. <span data-ttu-id="93021-125">Als u één vooruitbetalingspercentage wilt toepassen op de hele order, wijzigt u het veld **Vooruitbetaling %** op de kop nadat u de regels hebt ingevuld.</span><span class="sxs-lookup"><span data-stu-id="93021-125">If you want to apply one prepayment percentage to the entire order, change the **Prepayment %** field on the header after filling in the lines.</span></span>  
5. <span data-ttu-id="93021-126">Als u het totale vooruitbetalingsbedrag wilt weergeven, kiest u de actie **Statistieken**.</span><span class="sxs-lookup"><span data-stu-id="93021-126">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="93021-127">Als u het totale vooruitbetaalde bedrag voor de order wilt aanpassen, kunt u de inhoud van het veld **Vooruitbetaling** in het venster **Verkooporderstatistiek** wijzigen.</span><span class="sxs-lookup"><span data-stu-id="93021-127">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field in the **Sales Order Statistics** window.</span></span>  

    <span data-ttu-id="93021-128">Als het veld **Prijzen inclusief btw** is geselecteerd, kan het veld **Vooruitbetalingsbedrag incl. btw** worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="93021-128">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="93021-129">Als u de inhoud van het veld **Vooruitbetalingsbedrag** wijzigt, wordt het bedrag proportioneel verdeeld over alle regels, met uitzondering van de regels met een **0** in het veld **Vooruitbetalingsbedrag %**.</span><span class="sxs-lookup"><span data-stu-id="93021-129">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  
6. <span data-ttu-id="93021-130">Als u een testrapport wilt afdrukken voordat u de vooruitbetalingsfactuur boekt, kiest u de actie **Vooruitbetaling** en kiest u vervolgens de actie **Testrapport vooruitbetaling**.</span><span class="sxs-lookup"><span data-stu-id="93021-130">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
7. <span data-ttu-id="93021-131">Als u de vooruitbetalingsfactuur wilt boeken, kiest u de actie **Vooruitbetaling** en kiest u vervolgens de actie **Vooruitbetalingsfactuur boeken**.</span><span class="sxs-lookup"><span data-stu-id="93021-131">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="93021-132">Als u de vooruitbetalingsfactuur wilt boeken en afdrukken, kiest u de actie **Vooruitbetalingsfactuur boeken en afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="93021-132">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="93021-133">U kunt extra vooruitbetalingsnota's verzenden voor de order.</span><span class="sxs-lookup"><span data-stu-id="93021-133">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="93021-134">Verhoog hiervoor het vooruitbetalingsbedrag op een of meer regels, pas zo nodig de documentdatum aan en boek de vooruitbetalingsfactuur.</span><span class="sxs-lookup"><span data-stu-id="93021-134">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="93021-135">Er wordt een nieuwe factuur gemaakt voor het verschil tussen de tot nu toe gefactureerde vooruitbetalingsbedragen en het nieuwe vooruitbetalingsbedrag.</span><span class="sxs-lookup"><span data-stu-id="93021-135">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="93021-136">Als u zich in Noord-Amerika bevindt, kunt u het vooruitbetalingspercentage niet wijzigen nadat de vooruitbetalingsfactuur is geboekt.</span><span class="sxs-lookup"><span data-stu-id="93021-136">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="93021-137">Dit wordt voorkomen in de Noord-Amerikaanse versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] omdat de berekening van de sales tax anders niet correct is.</span><span class="sxs-lookup"><span data-stu-id="93021-137">This is prevented in the North American version of [!INCLUDE[d365fin](includes/d365fin_md.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="93021-138">Als u klaar bent om de rest van de factuur te boeken, boekt u deze net zoals andere facturen. Het vooruitbetalingsbedrag wordt automatisch afgetrokken van het verschuldigde bedrag.</span><span class="sxs-lookup"><span data-stu-id="93021-138">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="93021-139">Zie ook</span><span class="sxs-lookup"><span data-stu-id="93021-139">See Also</span></span>  
[<span data-ttu-id="93021-140">Vooruitbetalingen factureren</span><span class="sxs-lookup"><span data-stu-id="93021-140">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="93021-141">Procedure: Vooruitbetalingen verkoop instellen en factureren</span><span class="sxs-lookup"><span data-stu-id="93021-141">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="93021-142">Financiën</span><span class="sxs-lookup"><span data-stu-id="93021-142">Finance</span></span>](finance.md)  
<span data-ttu-id="93021-143">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="93021-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

