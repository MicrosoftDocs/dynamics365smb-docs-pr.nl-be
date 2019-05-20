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
ms.openlocfilehash: 260365ce5f1e88bb1cc243a1af16b184ba95a9a4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1237668"
---
# <a name="belgian-vat"></a><span data-ttu-id="f29dd-103">Belgische btw</span><span class="sxs-lookup"><span data-stu-id="f29dd-103">Belgian VAT</span></span>
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="f29dd-104">bevat Belgische uitbreidingen op de btw-rapportagefunctie waarmee u btw-transactiedetails kunt afdrukken.</span><span class="sxs-lookup"><span data-stu-id="f29dd-104">includes Belgium enhancements to VAT reporting feature that enables you to print VAT transaction details.</span></span> <span data-ttu-id="f29dd-105">U moet de volgende rapporten aan de Belgische belastingdienst versturen:</span><span class="sxs-lookup"><span data-stu-id="f29dd-105">You must send the following reports to the Belgian tax authorities:</span></span>  

-   <span data-ttu-id="f29dd-106">Aangifte per maand/kwartaal - Dit rapport wordt gebruikt om maandelijkse of driemaandelijkse btw-aangiftes te maken, afhankelijk van uw bedrijfsinkomsten.</span><span class="sxs-lookup"><span data-stu-id="f29dd-106">Monthly/Quarterly declaration - This report is used to create monthly or quarterly VAT declarations, depending on your company revenue.</span></span>  

-   <span data-ttu-id="f29dd-107">Jaarlijkse btw-lijst (op papier/schijf) - Dit rapport wordt gebruikt om jaarlijks alle gefactureerde bedragen te rapporteren voor goederen en services aan alle Belgische bedrijven met een geregistreerd btw-nummer.</span><span class="sxs-lookup"><span data-stu-id="f29dd-107">VAT annual listing (on paper/disk) - This report is used to annually report all amounts invoiced for both goods and services to all Belgian companies with a registered VAT number.</span></span>  

-   <span data-ttu-id="f29dd-108">Btw-VIES-lijst (op papier/schijf) - Dit rapport wordt gebruikt om de verkoop te rapporteren van goederen naar andere landen.</span><span class="sxs-lookup"><span data-stu-id="f29dd-108">VAT-VIES listing (on paper/disk) - This report is used to report the sales of goods to other countries.</span></span>  

<span data-ttu-id="f29dd-109">U moet ook een gedrukt afschrift met details van de btw-transacties verstrekken aan de Belgische belastingdienst.</span><span class="sxs-lookup"><span data-stu-id="f29dd-109">You are also required to provide a printed statement detailing the VAT transactions to the Belgian tax authorities.</span></span> <span data-ttu-id="f29dd-110">Zie Btw-aangifte voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f29dd-110">For more information, see VAT Statement.</span></span>  

## <a name="non-deductible-vat"></a><span data-ttu-id="f29dd-111">Niet-aftrekbare btw</span><span class="sxs-lookup"><span data-stu-id="f29dd-111">Non-Deductible VAT</span></span>  
 <span data-ttu-id="f29dd-112">In België kan btw volledig of gedeeltelijk aftrekbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="f29dd-112">In Belgium, VAT can be fully or partially deductible.</span></span> <span data-ttu-id="f29dd-113">Kosten zoals representatiekosten of aankopen van auto's zijn slechts deels aftrekbaar en de transactie moet opgeven hoeveel van de btw niet-aftrekbaar is.</span><span class="sxs-lookup"><span data-stu-id="f29dd-113">Expenses such as representation cost or purchases of cars are only partially deductible, and the transaction must specify how much of the VAT is non-deductible.</span></span> <span data-ttu-id="f29dd-114">U maakt bijvoorbeeld een grootboekrekening voor vaste activa, bijvoorbeeld auto's, en een andere rekening voor representatiekosten.</span><span class="sxs-lookup"><span data-stu-id="f29dd-114">For example, you create a general ledger account for fixed assets such as cars, and another account for representation cost.</span></span> <span data-ttu-id="f29dd-115">Voor elke rekening moet u opgeven hoeveel van de gerapporteerde btw niet-aftrekbaar is door het veld Percentage niet-aftrekbare btw in te stellen.</span><span class="sxs-lookup"><span data-stu-id="f29dd-115">For each account, you specify how much of the reported VAT is non-deductible by setting the Percentage Non deductible VAT field.</span></span> <span data-ttu-id="f29dd-116">Wanneer u een transactie boekt wordt de aftrekbare btw dan geboekt naar de corresponderende btw-rekening en wordt de niet-aftrekbare btw opgeteld bij het basisbedrag en geboekt naar dezelfde rekening als het materiële of immateriële activum.</span><span class="sxs-lookup"><span data-stu-id="f29dd-116">Then, when you post a transaction, the deductible VAT will post to the corresponding VAT account, and the non-deductible VAT will be added to the base amount and posted to the same account as the tangible or intangible asset.</span></span>  

 <span data-ttu-id="f29dd-117">Voor vaste activa wordt de niet-aftrekbare btw afgeschreven zoals de basisaanschafkosten van het vaste activum.</span><span class="sxs-lookup"><span data-stu-id="f29dd-117">For fixed assets, the non-deductible VAT depreciates just like the base acquisition cost of the fixed asset.</span></span> <span data-ttu-id="f29dd-118">U moet aparte VA-boekingsgroepen instellen voor elk percentage niet-aftrekbare btw, aangezien elke VA-boekingsgroep boekt naar een grootboekrekening, waarbij het veld Percentage niet-aftrekbare btw opgeeft hoeveel btw moet worden geboekt naar dezelfde rekening als het vaste activum.</span><span class="sxs-lookup"><span data-stu-id="f29dd-118">You must set up separate fixed asset posting groups for each percentage of non-deductible VAT since each fixed asset posting group posts to a general ledger account where the Percentage Non deductible VAT field specifies how much VAT must post to the same account as the fixed asset.</span></span>  

 <span data-ttu-id="f29dd-119">Als u het veld Inclusief niet-aftrekbare btw inschakelt op een btw-aangifteregel, wordt niet aftrekbare btw opgenomen in het btw-bedrag.</span><span class="sxs-lookup"><span data-stu-id="f29dd-119">If you select the Incl. Non Deductible VAT field in a VAT statement line, non-deductible VAT is included in the VAT amount.</span></span> <span data-ttu-id="f29dd-120">Het rapport **Btw-vereffening berekenen en boeken** telt het niet-aftrekbare deel van dat bedrag op bij de velden **Niet-aftrekbaar btw-bedrag** en **Niet-aftrekbaar btw-bedrag (bronvaluta)** in de resulterende btw-posten.</span><span class="sxs-lookup"><span data-stu-id="f29dd-120">The **Calc. and Post VAT Settlement** report adds the non-deductible part of that amount to the **Non Ded. VAT Amount** and **Non Ded. Source Curr. VAT Amt.** fields in the resulting VAT entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f29dd-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f29dd-121">See Also</span></span>  
 <span data-ttu-id="f29dd-122">[Belgische lokale functionaliteit](belgium-local-functionality.md) </span><span class="sxs-lookup"><span data-stu-id="f29dd-122">[Belgium Local Functionality](belgium-local-functionality.md) </span></span>  
 <span data-ttu-id="f29dd-123">[Periodieke btw-rapporten afdrukken](how-to-print-periodic-vat-reports.md) </span><span class="sxs-lookup"><span data-stu-id="f29dd-123">[Print Periodic VAT Reports](how-to-print-periodic-vat-reports.md) </span></span>  
 [<span data-ttu-id="f29dd-124">Niet-aftrekbare btw instellen</span><span class="sxs-lookup"><span data-stu-id="f29dd-124">Set Up Non-Deductible VAT</span></span>](how-to-set-up-non-deductible-vat.md)
