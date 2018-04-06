---
title: 'Ontwerpdetails: Boekingsinterfacestructuur | Microsoft Docs'
description: In dit onderwerp vindt u een overzicht van de algemene procedures in de boekingsinterfacestructuur.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4d5aede731958f6f07b361cf2b4f2351bb5ad06a
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="3decc-103">Ontwerpdetails: boekingsinterfacestructuur</span><span class="sxs-lookup"><span data-stu-id="3decc-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="3decc-104">In de boekingsinterfacestructuur van [!INCLUDE[d365fin](includes/d365fin_md.md)] zijn er verschillende algemene procedures die dezelfde structuur gebruiken:</span><span class="sxs-lookup"><span data-stu-id="3decc-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="3decc-105">RunWithCheck- en RunWithoutCheck-aanroepprocedurecode - algemene boekingsinterface voor dagboekregel.</span><span class="sxs-lookup"><span data-stu-id="3decc-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen. Jnl Line.</span></span>  
* <span data-ttu-id="3decc-106">CustPostApplyCustLedgEntry - klantvereffening boeken, aangeroepen vanaf codeunit 226 custEntry - Geboekte posten vereffenen.</span><span class="sxs-lookup"><span data-stu-id="3decc-106">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="3decc-107">VendPostApplyVendLedgEntry - leveranciersvereffening boeken, aangeroepen vanaf codeunit 227 VendEntry - Geboekte posten vereffenen.</span><span class="sxs-lookup"><span data-stu-id="3decc-107">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="3decc-108">UnapplyCustLedgEntry - ongedaan maken van klantvereffening boeken, aangeroepen vanaf codeunit 226 custEntry - Geboekte posten vereffenen</span><span class="sxs-lookup"><span data-stu-id="3decc-108">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="3decc-109">UnapplyVendLedgEntry - ongedaan maken van leveranciersvereffening boeken, aangeroepen vanaf codeunit 227 VendEntry - Geboekte posten vereffenen</span><span class="sxs-lookup"><span data-stu-id="3decc-109">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3decc-110">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3decc-110">See Also</span></span>  
[<span data-ttu-id="3decc-111">Ontwerpdetails: boekingsenginestructuur</span><span class="sxs-lookup"><span data-stu-id="3decc-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)
