---
title: Belgische btw
description: Met Belgische uitbreidingen van de btw-rapportagefunctie kunt u btw-transactiedetails afdrukken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 15eb179bde51923f8fdba45f0ea3848eef5ab9ac
ms.sourcegitcommit: 5b6dd8d881c0eb65ece6936a94dfda3185574335
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/28/2019
ms.locfileid: "1710956"
---
# <a name="belgian-vat"></a><span data-ttu-id="b0063-103">Belgische btw</span><span class="sxs-lookup"><span data-stu-id="b0063-103">Belgian VAT</span></span>
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="b0063-104">bevat Belgische uitbreidingen op de btw-rapportagefunctie waarmee u btw-transactiedetails kunt afdrukken.</span><span class="sxs-lookup"><span data-stu-id="b0063-104">includes Belgian enhancements to the VAT reporting feature that enables you to print VAT transaction details.</span></span> <span data-ttu-id="b0063-105">U moet de volgende rapporten aan de Belgische belastingdienst versturen:</span><span class="sxs-lookup"><span data-stu-id="b0063-105">You must send the following reports to the Belgian tax authorities:</span></span>  

-   <span data-ttu-id="b0063-106">Aangifte per maand/kwartaal - Dit rapport wordt gebruikt om maandelijkse of driemaandelijkse btw-aangiftes te maken, afhankelijk van uw bedrijfsinkomsten.</span><span class="sxs-lookup"><span data-stu-id="b0063-106">Monthly/Quarterly declaration - This report is used to create monthly or quarterly VAT declarations, depending on your company revenue.</span></span>  

-   <span data-ttu-id="b0063-107">Jaarlijkse btw-lijst (op papier/schijf) - Dit rapport wordt gebruikt om jaarlijks alle gefactureerde bedragen te rapporteren voor goederen en services aan alle Belgische bedrijven met een geregistreerd btw-nummer.</span><span class="sxs-lookup"><span data-stu-id="b0063-107">VAT annual listing (on paper/disk) - This report is used to annually report all amounts invoiced for both goods and services to all Belgian companies with a registered VAT number.</span></span>  

-   <span data-ttu-id="b0063-108">Btw-VIES-lijst (op papier/schijf) - Dit rapport wordt gebruikt om de verkoop te rapporteren van goederen naar andere landen.</span><span class="sxs-lookup"><span data-stu-id="b0063-108">VAT-VIES listing (on paper/disk) - This report is used to report the sales of goods to other countries.</span></span>  

<span data-ttu-id="b0063-109">U moet ook een gedrukt afschrift met details van de btw-transacties verstrekken aan de Belgische belastingdienst.</span><span class="sxs-lookup"><span data-stu-id="b0063-109">You are also required to provide a printed statement detailing the VAT transactions to the Belgian tax authorities.</span></span> <span data-ttu-id="b0063-110">Zie Btw-aangifte voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b0063-110">For more information, see VAT Statement.</span></span>  

## <a name="non-deductible-vat"></a><span data-ttu-id="b0063-111">Niet-aftrekbare btw</span><span class="sxs-lookup"><span data-stu-id="b0063-111">Non-Deductible VAT</span></span>  
 <span data-ttu-id="b0063-112">In België kan btw volledig of gedeeltelijk aftrekbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="b0063-112">In Belgium, VAT can be fully or partially deductible.</span></span> <span data-ttu-id="b0063-113">Kosten zoals representatiekosten of aankopen van auto's zijn slechts deels aftrekbaar en de transactie moet opgeven hoeveel van de btw niet-aftrekbaar is.</span><span class="sxs-lookup"><span data-stu-id="b0063-113">Expenses such as representation cost or purchases of cars are only partially deductible, and the transaction must specify how much of the VAT is non-deductible.</span></span> <span data-ttu-id="b0063-114">U maakt bijvoorbeeld een grootboekrekening voor vaste activa, bijvoorbeeld auto's, en een andere rekening voor representatiekosten.</span><span class="sxs-lookup"><span data-stu-id="b0063-114">For example, you create a general ledger account for fixed assets such as cars, and another account for representation cost.</span></span> <span data-ttu-id="b0063-115">Voor elke rekening moet u opgeven hoeveel van de gerapporteerde btw niet-aftrekbaar is door het veld **Percentage niet-aftrekbare btw** in te stellen.</span><span class="sxs-lookup"><span data-stu-id="b0063-115">For each account, you specify how much of the reported VAT is non-deductible by setting the **Percentage Non deductible VAT** field.</span></span> <span data-ttu-id="b0063-116">Wanneer u een transactie boekt wordt de aftrekbare btw dan geboekt naar de corresponderende btw-rekening en wordt de niet-aftrekbare btw opgeteld bij het basisbedrag en geboekt naar dezelfde rekening als een materieel of immaterieel activum.</span><span class="sxs-lookup"><span data-stu-id="b0063-116">Then, when you post a transaction, the deductible VAT will post to the corresponding VAT account, and the non-deductible VAT will be added to the base amount and posted to the same account as a tangible or intangible asset.</span></span>  

 <span data-ttu-id="b0063-117">Voor vaste activa wordt de niet-aftrekbare btw afgeschreven zoals de basisaanschafkosten van het vaste activum.</span><span class="sxs-lookup"><span data-stu-id="b0063-117">For fixed assets, the non-deductible VAT depreciates just like the base acquisition cost of the fixed asset.</span></span> <span data-ttu-id="b0063-118">U moet aparte VA-boekingsgroepen instellen voor elk percentage niet-aftrekbare btw.</span><span class="sxs-lookup"><span data-stu-id="b0063-118">You must set up separate fixed asset posting groups for each percentage of non-deductible VAT.</span></span> <span data-ttu-id="b0063-119">U moet dit doen aangezien elke VA-boekingsgroep boekt naar een grootboekrekening, waarbij het veld **Percentage niet-aftrekbare btw** opgeeft hoeveel btw moet worden geboekt naar dezelfde rekening als het vaste activum.</span><span class="sxs-lookup"><span data-stu-id="b0063-119">You must do this because each fixed asset posting group posts to a general ledger account where the **Percentage Non deductible VAT** field specifies how much VAT must post to the same account as the fixed asset.</span></span>  

 <span data-ttu-id="b0063-120">Als u het veld **Inclusief niet-aftrekbare btw** inschakelt op een btw-aangifteregel, wordt niet aftrekbare btw opgenomen in het btw-bedrag.</span><span class="sxs-lookup"><span data-stu-id="b0063-120">If you select the **Incl. Non Deductible VAT** field in a VAT statement line, non-deductible VAT is included in the VAT amount.</span></span> <span data-ttu-id="b0063-121">Het rapport **Btw-vereffening berekenen en boeken** telt het niet-aftrekbare deel van dat bedrag op bij de velden **Niet-aftrekbaar btw-bedrag** en **Niet-aftrekbaar btw-bedrag (bronvaluta)** in de resulterende btw-posten.</span><span class="sxs-lookup"><span data-stu-id="b0063-121">The **Calc. and Post VAT Settlement** report adds the non-deductible part of that amount to the **Non Ded. VAT Amount** and **Non Ded. Source Curr. VAT Amt.** fields in the resulting VAT entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b0063-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b0063-122">See Also</span></span>  
 <span data-ttu-id="b0063-123">[Belgische lokale functionaliteit](belgium-local-functionality.md) </span><span class="sxs-lookup"><span data-stu-id="b0063-123">[Belgium Local Functionality](belgium-local-functionality.md) </span></span>  
 <span data-ttu-id="b0063-124">[Periodieke btw-rapporten afdrukken](how-to-print-periodic-vat-reports.md) </span><span class="sxs-lookup"><span data-stu-id="b0063-124">[Print Periodic VAT Reports](how-to-print-periodic-vat-reports.md) </span></span>  
 [<span data-ttu-id="b0063-125">Niet-aftrekbare btw instellen</span><span class="sxs-lookup"><span data-stu-id="b0063-125">Set Up Non-Deductible VAT</span></span>](how-to-set-up-non-deductible-vat.md)
