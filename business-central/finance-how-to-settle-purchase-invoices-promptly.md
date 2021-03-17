---
title: Inkoopfacturen meteen vereffenen
description: Als u de leverancier contant of per cheque moet betalen, kunt u de noodzakelijke boekingen doen op het moment dat u de factuur boekt.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: 60d3cf3c9e141c8df36eaca2c1975b696fdb105b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387261"
---
# <a name="settle-purchase-invoices-promptly"></a><span data-ttu-id="70b7f-103">Inkoopfacturen meteen vereffenen</span><span class="sxs-lookup"><span data-stu-id="70b7f-103">Settle Purchase Invoices Promptly</span></span>

<span data-ttu-id="70b7f-104">Als u de leverancier contant of per cheque moet betalen, kunt u de betaling boeken op het moment dat u de factuur boekt.</span><span class="sxs-lookup"><span data-stu-id="70b7f-104">If you need to pay the vendor by cash or check, you can post the payment when you post the invoice.</span></span>  

> [!NOTE]  
> <span data-ttu-id="70b7f-105">Als u vaak inkoopfacturen contant, met een cheque of met een bankovermaking betaalt, is het verstandig om een bepaalde betalingswijze met een tegenrekening in te stellen en deze betalingswijze in te voeren in het veld **Betalingswijze** op de leverancierskaart.</span><span class="sxs-lookup"><span data-stu-id="70b7f-105">If you frequently pay purchase invoices in cash, check, or bank transfer, it is a good idea to set up a specific payment method with a balancing account and enter this method in the **Payment Method** field on the vendor card.</span></span> <span data-ttu-id="70b7f-106">Telkens wanneer u hierna een nieuwe factuur maakt, wordt automatisch het tegenrekeningnummer op de factuurkop ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="70b7f-106">The balancing account number is inserted automatically on the invoice header every time you create a new invoice.</span></span> <span data-ttu-id="70b7f-107">Zie [Betalingsmethoden definiëren](finance-payment-methods.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="70b7f-107">For more information, see [Defining Payment Methods](finance-payment-methods.md).</span></span>  

## <a name="to-settle-purchase-invoices-promptly"></a><span data-ttu-id="70b7f-108">Een inkoopfactuur meteen vereffenen</span><span class="sxs-lookup"><span data-stu-id="70b7f-108">To settle purchase invoices promptly</span></span>

1. <span data-ttu-id="70b7f-109">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="70b7f-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="70b7f-110">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="70b7f-110">Choose the **New** action.</span></span>  
3. <span data-ttu-id="70b7f-111">Voor contante betalingen of bankoverboekingen voert u in het veld **Tegenrekeningnr.** het nummer in van de grootboekrekening of bankrekening.</span><span class="sxs-lookup"><span data-stu-id="70b7f-111">To pay either in cash or by bank transfer, enter the number of the general ledger cash account or the bank account in the **Bal. Account No.** field.</span></span>  

> [!IMPORTANT]  
> <span data-ttu-id="70b7f-112">De velden **Tegenrekeningsoort** en **Tegenrekeningnr.** worden niet standaard weergegeven op de factuurkop.</span><span class="sxs-lookup"><span data-stu-id="70b7f-112">The **Bal. Account Type** and **Bal. Account No.** fields are not included in the standard layout of the invoice header.</span></span> <span data-ttu-id="70b7f-113">Om de betaling van een factuur te boeken moet u contact opnemen met een Microsoft-partner die de velden via code kan toevoegen.</span><span class="sxs-lookup"><span data-stu-id="70b7f-113">In order to post the payment of an invoice, you must contact a Microsoft partner who can add the fields through code.</span></span>  
>
> <span data-ttu-id="70b7f-114">Deze aanpassing is alleen vereist als u geen tegenrekeningen opgeeft op de betaalmethoden zoals hierboven beschreven.</span><span class="sxs-lookup"><span data-stu-id="70b7f-114">This customization is only required if you do not specify balancing accounts on the payment methods as describe above.</span></span>

## <a name="see-also"></a><span data-ttu-id="70b7f-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="70b7f-115">See Also</span></span>

[<span data-ttu-id="70b7f-116">Betalingsverplichtingen beheren</span><span class="sxs-lookup"><span data-stu-id="70b7f-116">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="70b7f-117">Inkoop</span><span class="sxs-lookup"><span data-stu-id="70b7f-117">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="70b7f-118">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="70b7f-118">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]