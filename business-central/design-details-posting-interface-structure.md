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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 1e80b905d96fc2204b61b03c0970257755b9e105
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3787358"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="5f2c9-103">Ontwerpdetails: boekingsinterfacestructuur</span><span class="sxs-lookup"><span data-stu-id="5f2c9-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="5f2c9-104">In de boekingsinterfacestructuur van [!INCLUDE[d365fin](includes/d365fin_md.md)] zijn er verschillende algemene procedures die dezelfde structuur gebruiken:</span><span class="sxs-lookup"><span data-stu-id="5f2c9-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="5f2c9-105">RunWithCheck- en RunWithoutCheck-aanroepprocedurecode - algemene boekingsinterface voor</span><span class="sxs-lookup"><span data-stu-id="5f2c9-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen.</span></span> <span data-ttu-id="5f2c9-106">dagboekregel.</span><span class="sxs-lookup"><span data-stu-id="5f2c9-106">Jnl Line.</span></span>  
* <span data-ttu-id="5f2c9-107">CustPostApplyCustLedgEntry - klantvereffening boeken, aangeroepen vanaf codeunit 226 custEntry - Geboekte posten vereffenen.</span><span class="sxs-lookup"><span data-stu-id="5f2c9-107">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="5f2c9-108">VendPostApplyVendLedgEntry - leveranciersvereffening boeken, aangeroepen vanaf codeunit 227 VendEntry - Geboekte posten vereffenen.</span><span class="sxs-lookup"><span data-stu-id="5f2c9-108">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="5f2c9-109">UnapplyCustLedgEntry - ongedaan maken van klantvereffening boeken, aangeroepen vanaf codeunit 226 custEntry - Geboekte posten vereffenen</span><span class="sxs-lookup"><span data-stu-id="5f2c9-109">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="5f2c9-110">UnapplyVendLedgEntry - ongedaan maken van leveranciersvereffening boeken, aangeroepen vanaf codeunit 227 VendEntry - Geboekte posten vereffenen</span><span class="sxs-lookup"><span data-stu-id="5f2c9-110">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f2c9-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5f2c9-111">See Also</span></span>  
[<span data-ttu-id="5f2c9-112">Ontwerpdetails: boekingsenginestructuur</span><span class="sxs-lookup"><span data-stu-id="5f2c9-112">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)