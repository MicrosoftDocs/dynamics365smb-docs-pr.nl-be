---
title: 'Ontwerpdetails: Boekingsinterfacestructuur | Microsoft Docs'
description: In dit onderwerp vindt u een overzicht van de algemene procedures in de boekingsinterfacestructuur.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: posting, interface, design
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 236cbcc45ccca23905dcb79a491236c80b2bdebf
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816422"
---
# <a name="design-details-posting-interface-structure"></a><span data-ttu-id="c1ecd-103">Ontwerpdetails: boekingsinterfacestructuur</span><span class="sxs-lookup"><span data-stu-id="c1ecd-103">Design Details: Posting Interface Structure</span></span>
<span data-ttu-id="c1ecd-104">In de boekingsinterfacestructuur van [!INCLUDE[d365fin](includes/d365fin_md.md)] zijn er verschillende algemene procedures die dezelfde structuur gebruiken:</span><span class="sxs-lookup"><span data-stu-id="c1ecd-104">In the [!INCLUDE[d365fin](includes/d365fin_md.md)] posting interface structure, there are several global procedures that use the same structure:</span></span>  
  
* <span data-ttu-id="c1ecd-105">RunWithCheck- en RunWithoutCheck-aanroepprocedurecode - algemene boekingsinterface voor dagboekregel.</span><span class="sxs-lookup"><span data-stu-id="c1ecd-105">RunWithCheck and RunWithoutCheck call procedure Code – generic posting interface for Gen. Jnl Line.</span></span>  
* <span data-ttu-id="c1ecd-106">CustPostApplyCustLedgEntry - klantvereffening boeken, aangeroepen vanaf codeunit 226 custEntry - Geboekte posten vereffenen.</span><span class="sxs-lookup"><span data-stu-id="c1ecd-106">CustPostApplyCustLedgEntry – post customer application, called from codeunit 226 CustEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="c1ecd-107">VendPostApplyVendLedgEntry - leveranciersvereffening boeken, aangeroepen vanaf codeunit 227 VendEntry - Geboekte posten vereffenen.</span><span class="sxs-lookup"><span data-stu-id="c1ecd-107">VendPostApplyVendLedgEntry – post vendor application, called from codeunit 227 VendEntry-Apply Posted Entries.</span></span>  
* <span data-ttu-id="c1ecd-108">UnapplyCustLedgEntry - ongedaan maken van klantvereffening boeken, aangeroepen vanaf codeunit 226 custEntry - Geboekte posten vereffenen</span><span class="sxs-lookup"><span data-stu-id="c1ecd-108">UnapplyCustLedgEntry – post unapply of customer application, called from codeunit 226 CustEntry-Apply Posted Entries</span></span>  
* <span data-ttu-id="c1ecd-109">UnapplyVendLedgEntry - ongedaan maken van leveranciersvereffening boeken, aangeroepen vanaf codeunit 227 VendEntry - Geboekte posten vereffenen</span><span class="sxs-lookup"><span data-stu-id="c1ecd-109">UnapplyVendLedgEntry – post unapply of vendor application, called from codeunit 227 VendEntry-Apply Posted Entries</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c1ecd-110">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c1ecd-110">See Also</span></span>  
[<span data-ttu-id="c1ecd-111">Ontwerpdetails: boekingsenginestructuur</span><span class="sxs-lookup"><span data-stu-id="c1ecd-111">Design Details: Posting Engine Structure</span></span>](design-details-posting-engine-structure.md)