---
title: 'Procedure: Vooruitbetalingsfacturen maken | Microsoft Docs'
description: Leer omgaan met situaties waarin u of uw leverancier vooruitbetaling verlangt.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5f227cc73531111ae15f69d6fba5ac541e28560c
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746878"
---
# <a name="create-prepayment-invoices"></a><span data-ttu-id="b12b6-103">Vooruitbetalingsfacturen maken</span><span class="sxs-lookup"><span data-stu-id="b12b6-103">Create Prepayment Invoices</span></span>

<span data-ttu-id="b12b6-104">Als u van uw klanten wilt dat ze betalen voordat u een bestelling naar hen verzendt, kunt u de vooruitbetalingsfunctie gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b12b6-104">If you require your customers to submit payment before you ship an order to them, you can use the prepayment functionality.</span></span> <span data-ttu-id="b12b6-105">Hetzelfde geldt als uw leverancier van u verlangt dat u een betaling doet voordat zij een bestelling naar u verzenden.</span><span class="sxs-lookup"><span data-stu-id="b12b6-105">The same applies if your vendor requires you to submit payment before they ship an order to you.</span></span>  

<span data-ttu-id="b12b6-106">U kunt het vooruitbetalingsproces starten wanneer u een verkoop- of inkooporder maakt.</span><span class="sxs-lookup"><span data-stu-id="b12b6-106">You can start the prepayment process when you create a sales or purchase order.</span></span> <span data-ttu-id="b12b6-107">Als u een standaard vooruitbetalingspercentage heeft voor deze klant of leverancier, wordt dat automatisch opgenomen in de resulterende vooruitbetalingsfactuur.</span><span class="sxs-lookup"><span data-stu-id="b12b6-107">If you have a default prepayment percentage for this customer or vendor, that will be included automatically in the resulting prepayment invoice.</span></span> <span data-ttu-id="b12b6-108">U kunt ook een percentage voor vooruitbetaling opgeven voor het hele document.</span><span class="sxs-lookup"><span data-stu-id="b12b6-108">You can also specify a prepayment percentage to the entire document.</span></span>

<span data-ttu-id="b12b6-109">Nadat u een verkoop- of inkooporder hebt gemaakt, kunt u een vooruitbetalingsnota maken.</span><span class="sxs-lookup"><span data-stu-id="b12b6-109">After you create a sales or purchase order, you can create a prepayment invoice.</span></span> <span data-ttu-id="b12b6-110">U kunt de standaardpercentages gebruiken voor elke verkoop- of inkoopregel, of u kunt het bedrag naar wens aanpassen.</span><span class="sxs-lookup"><span data-stu-id="b12b6-110">You can use the default percentages for each sales or purchase line, or you can adjust the amount as necessary.</span></span> <span data-ttu-id="b12b6-111">U kunt bijvoorbeeld een totaalbedrag opgeven voor de hele order.</span><span class="sxs-lookup"><span data-stu-id="b12b6-111">For example, you can specify a total amount for the entire order.</span></span>  

<span data-ttu-id="b12b6-112">In de volgende procedure wordt beschreven hoe u een vooruitbetaling voor een verkooporder factureert.</span><span class="sxs-lookup"><span data-stu-id="b12b6-112">The following procedure describes how to invoice a prepayment for a sales order.</span></span> <span data-ttu-id="b12b6-113">De stappen zijn vergelijkbaar voor inkooporders.</span><span class="sxs-lookup"><span data-stu-id="b12b6-113">The steps are similar for purchase orders.</span></span>  

## <a name="to-create-a-prepayment-invoice"></a><span data-ttu-id="b12b6-114">Een vooruitbetalingsfactuur maken</span><span class="sxs-lookup"><span data-stu-id="b12b6-114">To create a prepayment invoice</span></span>

1. <span data-ttu-id="b12b6-115">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="b12b6-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="b12b6-116">Maak een nieuwe verkooporder voor de relevante klant.</span><span class="sxs-lookup"><span data-stu-id="b12b6-116">Create a new sales order for the relevant customer.</span></span> <span data-ttu-id="b12b6-117">Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b12b6-117">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>  

    <span data-ttu-id="b12b6-118">Op het sneltabblad **Vooruitbetaling** geeft het veld **Vooruitbetaling %** het percentage aan dat moet worden gebruikt om het vooruitbetalingsbedrag te berekenen.</span><span class="sxs-lookup"><span data-stu-id="b12b6-118">On the **Prepayment** FastTab, the **Prepayment %** field specifies the percentage to use to calculate the prepayment amount.</span></span> <span data-ttu-id="b12b6-119">Als er een standaard vooruitbetalingspercentage is op de klantenkaart, wordt het veld automatisch ingevuld.</span><span class="sxs-lookup"><span data-stu-id="b12b6-119">If there is a default prepayment percentage on the customer card, the field is filled in automatically.</span></span> <span data-ttu-id="b12b6-120">U kunt het percentage wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b12b6-120">You can change the percentage.</span></span> <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    <span data-ttu-id="b12b6-121">Kies het veld **Vooruitbetaling comprimeren** als u regels op de vooruitbetalingsfactuur wilt maken die regels uit de verkooporder combineren als:</span><span class="sxs-lookup"><span data-stu-id="b12b6-121">Choose the **Compress Prepayment** field if you want to create lines on the prepayment invoice that combine lines from the sales order if:</span></span>  

    - <span data-ttu-id="b12b6-122">Ze hebben dezelfde grootboekrekening voor vooruitbetalingen zoals bepaald door de boekingsgroepinstellingen.</span><span class="sxs-lookup"><span data-stu-id="b12b6-122">They have the same general ledger account for prepayments as determined by the general posting setup.</span></span>  
    - <span data-ttu-id="b12b6-123">Ze hebben dezelfde dimensies.</span><span class="sxs-lookup"><span data-stu-id="b12b6-123">They have the same dimensions.</span></span>  

    <span data-ttu-id="b12b6-124">Als u een vooruitbetalingsfactuur wilt opgeven met één regel voor elke verkooporderregel die een vooruitbetalingspercentage heeft, kiest u het veld **Vooruitbetaling comprimeren** niet.</span><span class="sxs-lookup"><span data-stu-id="b12b6-124">If you want to specify a prepayment invoice with one line for each sales order line that has a prepayment percentage, then do not choose the **Compress Prepayment** field.</span></span>  

    <span data-ttu-id="b12b6-125">De vervaldatum voor de vooruitbetaling wordt automatisch berekend op basis van de waarde van de **Code betalingscond. vooruitbetaling**.</span><span class="sxs-lookup"><span data-stu-id="b12b6-125">The due date for the prepayment is calculated automatically based on the value of the **Prepmt. Payment Terms Code**.</span></span>

3. <span data-ttu-id="b12b6-126">Vul de verkoopregels in.</span><span class="sxs-lookup"><span data-stu-id="b12b6-126">Fill in the sales lines.</span></span>  

    <span data-ttu-id="b12b6-127">Als u een standaard vooruitbetalingspercentage heeft opgegeven voor de klant of op het sneltabblad **Vooruitbetaling** voor dit document, wordt deze waarde naar elke regel gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="b12b6-127">If you have specified a default prepayment percentage either for the customer or on the **Prepayment** FastTab on this document, this value is copied to each line.</span></span> <span data-ttu-id="b12b6-128">U kunt de inhoud van het veld **Vooruitbetaling %** op de regel wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b12b6-128">You can change the contents of the **Prepayment %** field on the line.</span></span>  

4. <span data-ttu-id="b12b6-129">Als u het totale vooruitbetalingsbedrag wilt weergeven, kiest u de actie **Statistieken**.</span><span class="sxs-lookup"><span data-stu-id="b12b6-129">To view the total prepayment amount, choose the **Statistics** action.</span></span>

    <span data-ttu-id="b12b6-130">Als u het totale vooruitbetaalde bedrag voor de order wilt aanpassen, kunt u de inhoud van het veld **Vooruitbetaling** op de pagina **Verkooporderstatistiek** wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b12b6-130">If you want to adjust the total prepayment amount for the order, you can change the contents of the **Prepayment Amount** field on the **Sales Order Statistics** page.</span></span>  

    <span data-ttu-id="b12b6-131">Als het veld **Prijzen inclusief btw** is geselecteerd, kan het veld **Vooruitbetalingsbedrag incl. btw** worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="b12b6-131">If the **Prices Including VAT** field is selected, the **Prepayment Amount Incl. VAT** field is editable.</span></span>  

    <span data-ttu-id="b12b6-132">Als u de inhoud van het veld **Vooruitbetalingsbedrag** wijzigt, wordt het bedrag proportioneel verdeeld over alle regels, met uitzondering van de regels met een **0** in het veld **Vooruitbetalingsbedrag %**.</span><span class="sxs-lookup"><span data-stu-id="b12b6-132">If you change the contents of the **Prepayment Amount** field, the amount will be distributed proportionately between all lines, except those that have **0** in the **Prepayment %** field.</span></span>  

5. <span data-ttu-id="b12b6-133">Als u een testrapport wilt afdrukken voordat u de vooruitbetalingsfactuur boekt, kiest u de actie **Vooruitbetaling** en kiest u vervolgens de actie **Testrapport vooruitbetaling**.</span><span class="sxs-lookup"><span data-stu-id="b12b6-133">To print a test report before posting the prepayment invoice, choose the **Prepayment** action, and then choose the **Prepayment Test Report** action.</span></span>  
6. <span data-ttu-id="b12b6-134">Als u de vooruitbetalingsfactuur wilt boeken, kiest u de actie **Vooruitbetaling** en kiest u vervolgens de actie **Vooruitbetalingsfactuur boeken**.</span><span class="sxs-lookup"><span data-stu-id="b12b6-134">To post the prepayment invoice, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action.</span></span>  

    <span data-ttu-id="b12b6-135">Als u de vooruitbetalingsfactuur wilt boeken en afdrukken, kiest u de actie **Vooruitbetalingsfactuur boeken en afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="b12b6-135">To post and print the prepayment invoice, choose the **Post and Print Prepmt. Invoice** action.</span></span>  

<span data-ttu-id="b12b6-136">U kunt extra vooruitbetalingsnota's verzenden voor de order.</span><span class="sxs-lookup"><span data-stu-id="b12b6-136">You can issue additional prepayment invoices for the order.</span></span> <span data-ttu-id="b12b6-137">Verhoog hiervoor het vooruitbetalingsbedrag op een of meer regels, pas zo nodig de documentdatum aan en boek de vooruitbetalingsfactuur.</span><span class="sxs-lookup"><span data-stu-id="b12b6-137">To do this, increase the prepayment amount on one or more lines, adjust the document date if necessary, and post the prepayment invoice.</span></span> <span data-ttu-id="b12b6-138">Er wordt een nieuwe factuur gemaakt voor het verschil tussen de tot nu toe gefactureerde vooruitbetalingsbedragen en het nieuwe vooruitbetalingsbedrag.</span><span class="sxs-lookup"><span data-stu-id="b12b6-138">A new invoice will be created for the difference between the prepayment amounts invoiced so far and the new prepayment amount.</span></span>  

> [!NOTE]  
> <span data-ttu-id="b12b6-139">Als u zich in Noord-Amerika bevindt, kunt u het vooruitbetalingspercentage niet wijzigen nadat de vooruitbetalingsfactuur is geboekt.</span><span class="sxs-lookup"><span data-stu-id="b12b6-139">If you are located in North America, you cannot change the prepayment percentage after the prepayment invoice has been posted.</span></span> <span data-ttu-id="b12b6-140">Dit wordt voorkomen in de Noord-Amerikaanse versie van [!INCLUDE[prod_short](includes/prod_short.md)] omdat de berekening van de sales tax anders niet correct is.</span><span class="sxs-lookup"><span data-stu-id="b12b6-140">This is prevented in the North American version of [!INCLUDE[prod_short](includes/prod_short.md)] because the calculation of sales tax will otherwise be incorrect.</span></span>  

 <span data-ttu-id="b12b6-141">Als u klaar bent om de rest van de factuur te boeken, boekt u deze net zoals andere facturen. Het vooruitbetalingsbedrag wordt automatisch afgetrokken van het verschuldigde bedrag.</span><span class="sxs-lookup"><span data-stu-id="b12b6-141">When you are ready to post the rest of the invoice, post it as you would post any invoice, and the prepayment amount will automatically be deducted from the amount due.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b12b6-142">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b12b6-142">See Also</span></span>

[<span data-ttu-id="b12b6-143">Vooruitbetalingen factureren</span><span class="sxs-lookup"><span data-stu-id="b12b6-143">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="b12b6-144">Procedure: Vooruitbetalingen verkoop instellen en factureren</span><span class="sxs-lookup"><span data-stu-id="b12b6-144">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="b12b6-145">Financiën</span><span class="sxs-lookup"><span data-stu-id="b12b6-145">Finance</span></span>](finance.md)  
<span data-ttu-id="b12b6-146">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b12b6-146">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
