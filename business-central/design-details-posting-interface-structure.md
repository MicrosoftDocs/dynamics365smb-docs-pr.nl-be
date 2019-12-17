---
title: 'Ontwerpdetails: Boekingsinterfacestructuur | Microsoft Docs'
description: In dit onderwerp vindt u een overzicht van de algemene procedures in de boekingsinterfacestructuur.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7600e8ebfee6b6eda6f872b0de2f4c8238338340
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2880100"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="32553-103">Ontwerpdetails: boekingsinterfacestructuur</span><span class="sxs-lookup"><span data-stu-id="32553-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="32553-104">In de boekingsinterfacestructuur van [!INCLUDE[d365fin](includes/d365fin_md.md)] zijn er verschillende algemene procedures die dezelfde structuur gebruiken:</span><span class="sxs-lookup"><span data-stu-id="32553-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="32553-105">RunWithCheck- en RunWithoutCheck-aanroepprocedurecode - algemene boekingsinterface voor</span><span class="sxs-lookup"><span data-stu-id="32553-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="32553-106">dagboekregel.</span><span class="sxs-lookup"><span data-stu-id="32553-106">Jnl Line.</span></span>  
* <span data-ttu-id="32553-107">CustPostApplyCustLedgEntry - klantvereffening boeken, aangeroepen vanaf codeunit 226 custEntry - Geboekte posten vereffenen.</span><span class="sxs-lookup"><span data-stu-id="32553-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="32553-108">VendPostApplyVendLedgEntry - leveranciersvereffening boeken, aangeroepen vanaf codeunit 227 VendEntry - Geboekte posten vereffenen.</span><span class="sxs-lookup"><span data-stu-id="32553-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="32553-109">UnapplyCustLedgEntry - ongedaan maken van klantvereffening boeken, aangeroepen vanaf codeunit 226 custEntry - Geboekte posten vereffenen</span><span class="sxs-lookup"><span data-stu-id="32553-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="32553-110">UnapplyVendLedgEntry - ongedaan maken van leveranciersvereffening boeken, aangeroepen vanaf codeunit 227 VendEntry - Geboekte posten vereffenen</span><span class="sxs-lookup"><span data-stu-id="32553-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="32553-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="32553-111">See Also</span></span>  
[<span data-ttu-id="32553-112">Ontwerpdetails: boekingsenginestructuur</span><span class="sxs-lookup"><span data-stu-id="32553-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)