---
title: Valutawisselkoersen bijwerken | Microsoft Docs
description: Als u meerdere valuta's in uw bedrijf wilt gebruiken, kunt u een code voor elke gebruikte valuta instellen en een externe wisselkoersservice gebruiken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 12/19/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa1e7b13cf6cc56df1a6922a9b123e7cc19580c6
ms.openlocfilehash: 7fafae0cba12ba985de2faa795b434d4c670a8ca
ms.contentlocale: nl-be
ms.lasthandoff: 12/19/2018

---
# <a name="update-currency-exchange-rates"></a><span data-ttu-id="6f1c2-103">Valutawisselkoersen bijwerken</span><span class="sxs-lookup"><span data-stu-id="6f1c2-103">Update Currency Exchange Rates</span></span>
<span data-ttu-id="6f1c2-104">Aangezien bedrijven steeds vaker in andere landen/regio's opereren, is het belangrijk dat zij kunnen handelen en financiën in meer dan één valuta kunnen controleren of rapporteren.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-104">As companies operate in increasingly more countries/regions, it becomes more important that they be able to trade and report financials in more than one currency.</span></span> <span data-ttu-id="6f1c2-105">U moet een code instellen voor elke gebruikte valuta als u in andere valuta's dan uw lokale valuta inkoopt of verkoopt, in een andere valuta tegoeden of schulden hebt of grootboektransacties in verschillende valuta's vastlegt.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-105">You must set up a code for each currency you use if you buy or sell in currencies other than your local currency, have receivables or payables in other currencies, or record G/L transactions in different currencies.</span></span>

<span data-ttu-id="6f1c2-106">Uw grootboek is ingesteld om uw lokale valuta (LV) te gebruiken, maar u kunt het ook instellen om een andere valuta te gebruiken, waaraan een huidige wisselkoers is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-106">Your general ledger is set up to use your local currency (LCY), but you can set it up to also use another currency with a current exchange rate assigned.</span></span> <span data-ttu-id="6f1c2-107">Door een tweede valuta in te stellen als een zogenaamde aanvullende rapportagevaluta, legt [!INCLUDE[d365fin](includes/d365fin_md.md)] bedragen automatisch vast in zowel de LV als deze aanvullende rapportagevaluta voor elke grootboekpost en andere posten, zoals btw-posten.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-107">By designating a second currency as a so-called additional reporting currency, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically record amounts in both LCY and this additional reporting currency on each G/L entry and other entries, such as VAT entries.</span></span> <span data-ttu-id="6f1c2-108">Zie voor meer informatie [Een extra rapportagevaluta instellen](finance-how-setup-additional-currencies.md).</span><span class="sxs-lookup"><span data-stu-id="6f1c2-108">For more information, see [Set Up an Additional Reporting Currency](finance-how-setup-additional-currencies.md).</span></span>

## <a name="adjusting-exchange-rates"></a><span data-ttu-id="6f1c2-109">Wisselkoersen corrigeren</span><span class="sxs-lookup"><span data-stu-id="6f1c2-109">Adjusting Exchange Rates</span></span>
<span data-ttu-id="6f1c2-110">Aangezien valutakoersen constant wisselen, moeten de extra valuta-equivalenten in uw systeem periodiek worden gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-110">Because exchange rates fluctuate constantly, additional currency equivalents in your system must be adjusted periodically.</span></span> <span data-ttu-id="6f1c2-111">Als deze correcties niet worden uitgevoerd, kunnen de bedragen die omgerekend zijn van vreemde (of extra) valuta's en geboekt zijn in het grootboek in LV misleidend zijn.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-111">If these adjustments are not done, amounts that have been converted from foreign (or additional) currencies and posted to the general ledger in LCY may be misleading.</span></span> <span data-ttu-id="6f1c2-112">Bovendien moeten dagelijkse posten die geboekt zijn doordat een dagwisselkoers is ingevoerd in het programma worden bijgewerkt nadat de dagwisselkoersgegevens zijn ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-112">In addition, daily entries posted before a daily exchange rate is entered into the program must be updated after the daily exchange rate information is entered.</span></span> <span data-ttu-id="6f1c2-113">De batchverwerking Wisselkoers herwaarderen wordt gebruikt om de wisselkoersen van de geboekte klant, leverancier en bankrekeningposten te corrigeren.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-113">The Adjust Exchange Rates batch job is used to adjust the exchange rates of posted customer, vendor and bank account entries.</span></span> <span data-ttu-id="6f1c2-114">U kunt er tevens extra rapportagevalutabedragen in grootboekposten mee bijwerken.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-114">It can also update additional reporting currency amounts on G/L entries.</span></span>

## <a name="to-set-up-a-currency-exchange-rate-service"></a><span data-ttu-id="6f1c2-115">Een wisselkoersservice instellen</span><span class="sxs-lookup"><span data-stu-id="6f1c2-115">To set up a currency exchange rate service</span></span>
<span data-ttu-id="6f1c2-116">U kunt een externe service gebruiken om valutawisselkoersen actueel te houden, zoals FloatRates.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-116">You can use an external service to keep your currency exchange rates up to date, such as FloatRates.</span></span>

1. <span data-ttu-id="6f1c2-117">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Valutawisselkoersservices** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currency Exchange Rate Services**, and then choose the related link.</span></span>
2. <span data-ttu-id="6f1c2-118">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-118">Choose the **New** action.</span></span>
3. <span data-ttu-id="6f1c2-119">Vul op de pagina **Valutawisselkoersservice** indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-119">On the **Currency Exchange Rate Service** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="6f1c2-120">Kies het selectievakje **Ingeschakeld** om de service in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-120">Choose the **Enabled** check box to enable the service.</span></span>

## <a name="to-update-currency-exchange-rates-through-a-service"></a><span data-ttu-id="6f1c2-121">Valutawisselkoersen bijwerken met een service</span><span class="sxs-lookup"><span data-stu-id="6f1c2-121">To update currency exchange rates through a service</span></span>
1. <span data-ttu-id="6f1c2-122">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Valuta's** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Currencies**, and then choose the related link.</span></span>
2. <span data-ttu-id="6f1c2-123">Kies de actie **Wisselkoersen bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-123">Choose the **Update Exchange Rates** action.</span></span>

<span data-ttu-id="6f1c2-124">De waarde in het veld **Wisselkoers** op de pagina **Valuta's** wordt bijgewerkt met de laatste wisselkoers.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-124">The value in the **Exchange Rate** field on the **Currencies** page is updated with the latest currency exchange rate.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f1c2-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6f1c2-125">See Also</span></span>
[<span data-ttu-id="6f1c2-126">Een extra rapportagevaluta instellen.</span><span class="sxs-lookup"><span data-stu-id="6f1c2-126">Set Up an Additional Reporting Currency</span></span>](finance-how-setup-additional-currencies.md)  
[<span data-ttu-id="6f1c2-127">Afsluitingsjaren en -perioden</span><span class="sxs-lookup"><span data-stu-id="6f1c2-127">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="6f1c2-128">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6f1c2-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

