---
title: Vooruitbetalingen corrigeren | Microsoft Docs
description: Nadat u een vooruitbetalingsfactuur voor de order hebt geboekt, kunt u een correctie aanbrengen op een order. U kunt nieuwe regels toevoegen aan een order na het verzenden van een vooruitbetaling en vervolgens kunt u een andere vooruitbetalingsfactuur boeken, maar u kunt een regel niet uit een order verwijderen nadat een vooruitbetaling voor de regel is gefactureerd.
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: b19b86b3d5168ee6fa053141af4022f5040743cb
ms.contentlocale: nl-be
ms.lasthandoff: 11/26/2018

---
# <a name="correct-prepayments"></a><span data-ttu-id="42ca8-104">Vooruitbetalingen storneren</span><span class="sxs-lookup"><span data-stu-id="42ca8-104">Correct Prepayments</span></span>
<span data-ttu-id="42ca8-105">Nadat u een vooruitbetalingsfactuur voor de order hebt geboekt, kunt u een correctie aanbrengen op een order.</span><span class="sxs-lookup"><span data-stu-id="42ca8-105">You can make a correction to an order after you have posted a prepayment invoice for the order.</span></span> <span data-ttu-id="42ca8-106">U kunt nieuwe regels toevoegen aan een order na het verzenden van een vooruitbetaling en vervolgens kunt u een andere vooruitbetalingsfactuur boeken, maar u kunt een regel niet uit een order verwijderen nadat een vooruitbetaling voor de regel is gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="42ca8-106">You can add new lines to an order after issuing a prepayment, and then you can post another prepayment invoice, but you cannot delete a line from an order after a prepayment has been invoiced for the line.</span></span>  

## <a name="to-correct-a-prepayment"></a><span data-ttu-id="42ca8-107">Een vooruitbetalingen storneren</span><span class="sxs-lookup"><span data-stu-id="42ca8-107">To correct a prepayment</span></span>
<span data-ttu-id="42ca8-108">De volgende procedure toont hoe u een vooruitbetalingscreditnota verzendt om alle gefactureerde vooruitbetalingen voor een verkooporder te annuleren.</span><span class="sxs-lookup"><span data-stu-id="42ca8-108">The following procedure shows how to issue a prepayment credit memo to cancel all invoiced prepayments for a sales order.</span></span>  
1. <span data-ttu-id="42ca8-109">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="42ca8-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>  
2. <span data-ttu-id="42ca8-110">Open de betreffende verkooporder.</span><span class="sxs-lookup"><span data-stu-id="42ca8-110">Open the relevant sales order.</span></span>
3. <span data-ttu-id="42ca8-111">Kies de actie **Vooruitbetaling** en kies vervolgens de actie **Vooruitbetalingscreditnota boeken** of **Vooruitbetalingscreditnota boeken en afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="42ca8-111">Choose the **Prepayment** action, and then choose the **Post Prepayment Credit Memo** action or the **Post and Print Prepmt. Cr. Memo** action.</span></span>  
4. <span data-ttu-id="42ca8-112">Corrigeer op de pagina **Verkoopcreditnota** de relevante posten, zoals voor elke verkoopcreditnota.</span><span class="sxs-lookup"><span data-stu-id="42ca8-112">On the **Sales Credit Memo** page, proceed to correct the relevant entries, as for any sales credit memo.</span></span> <span data-ttu-id="42ca8-113">Zie [Verkoopretouren of annuleringen verwerken](sales-how-process-sales-returns-cancellations.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="42ca8-113">For more information, see [Process Sales Returns or Cancellations](sales-how-process-sales-returns-cancellations.md).</span></span>     

    > [!NOTE]  
    > <span data-ttu-id="42ca8-114">Als u het bedrag in het veld **Regelbedrag** wilt verminderen, moet u eerst het vooruitbetalingspercentage op de regel verhogen zodat de waarde in het veld **Regelbedrag vooruitbetaling** niet tot onder de waarde in het veld **Gefactureerde vooruitbetaling** wordt verlaagd.</span><span class="sxs-lookup"><span data-stu-id="42ca8-114">To Reduce the amount in the **Line Amount** field, you must first increase the prepayment percentage on the line so that the value in the **Prepmt. Line Amount** field is not decreased below the value in the **Prepmt. Amt. Inv.** field.</span></span>

5. <span data-ttu-id="42ca8-115">Als u een vooruitbetalingsfactuur wilt maken voor nieuwe regels in de verkoopcreditnota, kiest u de actie **Vooruitbetaling** en kiest u vervolgens de actie **Vooruitbetalingsfactuur boeken** of **Vooruitbetalingsfactuur boeken en afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="42ca8-115">To make a prepayment invoice for any new lines in the sales credit memo, choose the **Prepayment** action, and then choose the **Post Prepayment Invoice** action or the **Post and Print Prepmt. Invoice** action.</span></span>  
6. <span data-ttu-id="42ca8-116">Als u een extra vooruitbetalingsfactuur wilt verzenden, verhoogt u het vooruitbetalingsbedrag op een of meer regels en past u de vooruitbetalingsfactuur aan.</span><span class="sxs-lookup"><span data-stu-id="42ca8-116">To issue an additional prepayment invoice, increase the prepayment amount on one or more lines and post the prepayment invoice.</span></span> <span data-ttu-id="42ca8-117">Er wordt een nieuwe factuur gemaakt voor het verschil tussen de tot nu toe gefactureerde vooruitbetalingsbedragen en de nieuwe vooruitbetalingsbedragen.</span><span class="sxs-lookup"><span data-stu-id="42ca8-117">A new invoice will be created for the difference between the prepayment amounts invoiced and the new prepayment amounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="42ca8-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="42ca8-118">See Also</span></span>  
[<span data-ttu-id="42ca8-119">Vooruitbetalingen factureren</span><span class="sxs-lookup"><span data-stu-id="42ca8-119">Invoicing Prepayments</span></span>](finance-invoice-prepayments.md)  
[<span data-ttu-id="42ca8-120">Procedure: Vooruitbetalingen verkoop instellen en factureren</span><span class="sxs-lookup"><span data-stu-id="42ca8-120">Walkthrough: Setting Up and Invoicing Sales Prepayments</span></span>](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[<span data-ttu-id="42ca8-121">Financiën</span><span class="sxs-lookup"><span data-stu-id="42ca8-121">Finance</span></span>](finance.md)  
<span data-ttu-id="42ca8-122">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="42ca8-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

