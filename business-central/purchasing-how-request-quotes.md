---
title: Een inkooporder maken om een aanbod op te vragen | Microsoft Docs
description: Beschrijft hoe u een verkoopaanbieding of een offerteaanvraagdocument maakt om uw aanbod aan een klant vast te leggen om producten onder bepaalde voorwaarden te verkopen.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: bae0ddeb2a3b22d4f29c04628a54754f4d608ec9
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191031"
---
# <a name="request-quotes"></a><span data-ttu-id="bfaf9-103">Offertes aanvragen</span><span class="sxs-lookup"><span data-stu-id="bfaf9-103">Request Quotes</span></span>
<span data-ttu-id="bfaf9-104">U kunt een inkoopofferte als conceptversie van de inkooporder gebruiken. De order kan vervolgens in een inkoopfactuur of een order worden omgezet.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or an order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="bfaf9-105">Een inkoopofferte maken</span><span class="sxs-lookup"><span data-stu-id="bfaf9-105">To create a purchase quote</span></span>
1. <span data-ttu-id="bfaf9-106">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopoffertes** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="bfaf9-107">Maak een nieuw document op dezelfde manier als u een inkooporder maakt.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="bfaf9-108">Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="bfaf9-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="bfaf9-109">Een inkoopofferte omzetten in een inkooporder</span><span class="sxs-lookup"><span data-stu-id="bfaf9-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="bfaf9-110">Wanneer u de leveranciersofferte hebt geaccepteerd, kunt u deze omzetten naar een inkoopfactuur of order om de inkoop te verwerken.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-110">When you have accepted the vendor's quote, you can convert it to a purchase invoice or order to process the purchase.</span></span>

1. <span data-ttu-id="bfaf9-111">Open eeen inkoopofferte die klaar is om te worden geconverteerd en kies de actie **Order maken**.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="bfaf9-112">De inkoopofferte wordt verwijderd uit de database.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="bfaf9-113">Een inkoopfactuur of -order wordt gemaakt op basis van de informatie in de inkoopofferte waarin u de inkoop kunt verwerken.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-113">A purchase invoice or a purchase order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="bfaf9-114">Op de inkoopfactuur of inkooporder vermeldt het veld **Offertenr.** het nummer van de inkoopofferte van waaruit het is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="bfaf9-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="bfaf9-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="bfaf9-115">See Also</span></span>
[<span data-ttu-id="bfaf9-116">Inkoop</span><span class="sxs-lookup"><span data-stu-id="bfaf9-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="bfaf9-117">Inkoop instellen</span><span class="sxs-lookup"><span data-stu-id="bfaf9-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="bfaf9-118">Documenten per e-mail verzenden</span><span class="sxs-lookup"><span data-stu-id="bfaf9-118">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="bfaf9-119">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bfaf9-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
