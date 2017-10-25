---
title: De Quickbooks-extensie Salarisbestand importeren gebruiken | Microsoft Docs
description: Beschrijft hoe u de extensie gebruikt om salaris- en loontransacties te importeren uit de salarisservice van Quickbooks.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 03/29/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: b719a7d2b6b5590ae63920b63aaba8c2313a8661
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="the-quickbooks-payroll-file-import-extension-to-dynamics-365-for-financials"></a><span data-ttu-id="f7f15-103">De extensie voor import van Quickbooks-salarisbestanden naar Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="f7f15-103">The Quickbooks Payroll File Import Extension to Dynamics 365 for Financials</span></span>
<span data-ttu-id="f7f15-104">Als u salarisbetalingen en gerelateerde transacties wilt verantwoorden, moet u financiële transacties die zijn uitgevoerd door uw leverancier van salarisverwerking, importeren en boeken naar het grootboek.</span><span class="sxs-lookup"><span data-stu-id="f7f15-104">To account for salary payments and related transactions, you must import and post financial transactions made by your payroll provider to the general ledger.</span></span>

<span data-ttu-id="f7f15-105">Hiervoor importeert u eerst een bestand dat u van de leverancier van salarisverwerking ontvangt, in het venster **Fin. dagboek**.</span><span class="sxs-lookup"><span data-stu-id="f7f15-105">To do this, you first import a file that you receive from the payroll provider into the **General Journal** window.</span></span> <span data-ttu-id="f7f15-106">Vervolgens kunt u de externe rekeningen in het loonlijstbestand toewijzen aan de betreffende grootboekrekeningen.</span><span class="sxs-lookup"><span data-stu-id="f7f15-106">Then you map the external accounts in the payroll file to the relevant G/L accounts.</span></span> <span data-ttu-id="f7f15-107">Als laatste boekt u de loonlijsttransacties op basis van de rekeningtoewijzing.</span><span class="sxs-lookup"><span data-stu-id="f7f15-107">Lastly, you post the payroll transactions according to the account mapping.</span></span> <span data-ttu-id="f7f15-108">Zie [Procedure: Salaristransacties importeren](finance-how-import-payroll-transactions.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f7f15-108">For more information, see [How to: Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

<span data-ttu-id="f7f15-109">Met de Quickbooks-extensie voor import van salarisbestanden kunt u salaristransacties importeren uit de Quickbooks-salarisservice.</span><span class="sxs-lookup"><span data-stu-id="f7f15-109">The Quickbooks Payroll File Import extension allows you to import payroll transaction from the Quickbooks Payroll service.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7f15-110">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f7f15-110">See Also</span></span>
<span data-ttu-id="f7f15-111">[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="f7f15-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="f7f15-112">[Financiën](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="f7f15-112">[Finance](finance.md)  </span></span>  
<span data-ttu-id="f7f15-113">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f7f15-113">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

