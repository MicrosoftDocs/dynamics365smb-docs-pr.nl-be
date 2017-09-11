---
title: Sales tax in Canada | Microsoft Docs
description: Leren over lokale sales tax en Goods and Services Tax in Canada.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 571b11f4f18ffd194bdfe1d1d412bca87df4b868
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017

---
# <a name="reporting-sales-tax-and-goodsservices-tax-in-canada"></a><span data-ttu-id="61f19-103">Sales tax en Goods and Services Tax in Canada aangeven</span><span class="sxs-lookup"><span data-stu-id="61f19-103">Reporting Sales Tax and Goods/Services Tax in Canada</span></span>
<span data-ttu-id="61f19-104">In Canada, wanneer een leverancier geen zakelijke aanwezigheid in de provincie heeft waarin inkopen worden gedaan, brengt de leverancier alleen de Goods and Services Tax (GST) of Harmonized Sales Tax (HST) in rekening.</span><span class="sxs-lookup"><span data-stu-id="61f19-104">In Canada, when a vendor does not have a business presence in the province in which purchases are made, the vendor will charge the Goods and Services Tax (GST) or Harmonized Sales Tax (HST) only.</span></span> <span data-ttu-id="61f19-105">Als de provincie echter een Provincial Sales Tax (PST) heeft, moet de inkoper toch de PST berekenen en deze direct aan de provincie betalen.</span><span class="sxs-lookup"><span data-stu-id="61f19-105">However, if the province has a Provincial Sales Tax (PST), then the purchaser must still calculate the PST and pay it directly to the province.</span></span> <span data-ttu-id="61f19-106">Wanneer een Provincial Tax Area Code wordt geselecteerd, gebruikt [!INCLUDE[d365fin](includes/d365fin_md.md)] deze om de PST te berekenen en te boeken, zodat er een belastingschuld is in zowel het grootboek als de belastingpostrecords.</span><span class="sxs-lookup"><span data-stu-id="61f19-106">When a Provincial Tax Area Code is selected, [!INCLUDE[d365fin](includes/d365fin_md.md)] uses it to calculate the PST and post it so that there is a tax liability in both the general ledger and the tax entry records.</span></span> <span data-ttu-id="61f19-107">De hier geselecteerde tax area code moet er daarom een zijn waarin alleen de PST is opgenomen, niet de GST.</span><span class="sxs-lookup"><span data-stu-id="61f19-107">Therefore, the tax area code selected here should be one where only the PST is included, not the GST.</span></span>  

<span data-ttu-id="61f19-108">Zie voor meer informatie over sales tax [Sales tax en belastinggroepen in de VS en Canada](us-finance-sales-tax.md).</span><span class="sxs-lookup"><span data-stu-id="61f19-108">For more information about sales tax, see [Sales Tax and Tax Groups in the US and Canada](us-finance-sales-tax.md).</span></span>  

## <a name="submitting-the-gsthst-file"></a><span data-ttu-id="61f19-109">Het GST/HST-bestand verzenden</span><span class="sxs-lookup"><span data-stu-id="61f19-109">Submitting the GST/HST File</span></span>
<span data-ttu-id="61f19-110">De belastinggegevens in inkoopdocumenten worden gebruikt om een online GST/HST-bestandsoverdracht te genereren dat u moet verschaffen aan de belastingdienst.</span><span class="sxs-lookup"><span data-stu-id="61f19-110">The tax information in purchase documents is used to generate a GST/HST online file transfer that you must provide to the tax authorities.</span></span> <span data-ttu-id="61f19-111">Dit bestand bevat Goods and Services Tax (GST) en Harmonized Sales TAX (HST).</span><span class="sxs-lookup"><span data-stu-id="61f19-111">This file includes goods and services tax (GST) and harmonized sales tax (HST).</span></span> <span data-ttu-id="61f19-112">Het bestand wordt gemaakt in een .tax-bestandsindeling, dat online kan worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="61f19-112">The file is created in a .tax file format, which can be transferred online.</span></span>  

## <a name="see-also"></a><span data-ttu-id="61f19-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="61f19-113">See Also</span></span>
[<span data-ttu-id="61f19-114">Financiën</span><span class="sxs-lookup"><span data-stu-id="61f19-114">Finance</span></span>](finance.md)  
[<span data-ttu-id="61f19-115">Financiën instellen</span><span class="sxs-lookup"><span data-stu-id="61f19-115">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="61f19-116">Sales tax en belastinggroepen in de VS en Canada</span><span class="sxs-lookup"><span data-stu-id="61f19-116">Sales Tax and Tax Groups in the US and Canada</span></span>](us-finance-sales-tax.md)  
<span data-ttu-id="61f19-117">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="61f19-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

