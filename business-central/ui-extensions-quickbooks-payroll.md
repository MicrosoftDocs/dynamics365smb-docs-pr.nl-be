---
title: De QuickBooks-extensie Salarisbestand importeren gebruiken | Microsoft Docs
description: Dit onderwerp beschrijft hoe u de extensie gebruikt om salaris- en loontransacties te importeren uit de salarisservice van QuickBooks.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, salary, wage
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: eae93ea8cf81a2fad6af2c3810f94d5292eef93f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757104"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="82cb7-103">De QuickBooks-extensie Salarisbestand importeren</span><span class="sxs-lookup"><span data-stu-id="82cb7-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="82cb7-104">Gebruik de QuickBooks-extensie Salarisbestand importeren om loonlijsttransacties te importeren uit QuickBooks in grootboekrekeningen in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="82cb7-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="82cb7-105">Dit is bijvoorbeeld handig als u overstapt van QuickBooks op [!INCLUDE[prod_short](includes/prod_short.md)] of als u uw salarisadministratie uitbesteedt, maar deze ook wilt bijhouden in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="82cb7-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[prod_short](includes/prod_short.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="82cb7-106">Stappen om salarisgegevens te importeren</span><span class="sxs-lookup"><span data-stu-id="82cb7-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="82cb7-107">De eerste stap is voor u, of wellicht uw accountant, om de exportfuncties in QuickBooks te gebruiken om de salarisgegevens naar een .IIF-bestand te exporteren.</span><span class="sxs-lookup"><span data-stu-id="82cb7-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="82cb7-108">De tweede stap is de pagina **Dagboeken** in [!INCLUDE[prod_short](includes/prod_short.md)] te openen en de actie **Salaristransacties importeren** te gebruiken om het bestand te importeren.</span><span class="sxs-lookup"><span data-stu-id="82cb7-108">The second step is to open the **General Journals** page in [!INCLUDE[prod_short](includes/prod_short.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="82cb7-109">Tijdens het importproces koppelt u de grootboekrekeningen uit QuickBooks aan corresponderende rekeningen [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="82cb7-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="82cb7-110">De laatste stap is de loonlijsttransacties in [!INCLUDE[prod_short](includes/prod_short.md)] te boeken op basis van de rekeningtoewijzing.</span><span class="sxs-lookup"><span data-stu-id="82cb7-110">The final step is to post the payroll transactions in [!INCLUDE[prod_short](includes/prod_short.md)] according to the account mapping.</span></span> 

<span data-ttu-id="82cb7-111">Zie [Salaristransacties importeren](finance-how-import-payroll-transactions.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="82cb7-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="82cb7-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="82cb7-112">See Also</span></span>
<span data-ttu-id="82cb7-113">[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="82cb7-113">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="82cb7-114">[Financiën](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="82cb7-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="82cb7-115">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="82cb7-115">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
