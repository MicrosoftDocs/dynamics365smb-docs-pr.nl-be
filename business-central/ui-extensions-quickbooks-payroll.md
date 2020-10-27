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
ms.openlocfilehash: a63e2139ee4a3ac42e30724d8b7015cc0d968cd9
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3923482"
---
# <a name="the-quickbooks-payroll-file-import-extension"></a><span data-ttu-id="8bf48-103">De QuickBooks-extensie Salarisbestand importeren</span><span class="sxs-lookup"><span data-stu-id="8bf48-103">The QuickBooks Payroll File Import Extension</span></span>
<span data-ttu-id="8bf48-104">Gebruik de QuickBooks-extensie Salarisbestand importeren om loonlijsttransacties te importeren uit QuickBooks in grootboekrekeningen in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8bf48-104">Use the QuickBooks Payroll File Import extension to import payroll transactions from QuickBooks to general ledger accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="8bf48-105">Dit is bijvoorbeeld handig als u overstapt van QuickBooks op [!INCLUDE[d365fin](includes/d365fin_md.md)] of als u uw salarisadministratie uitbesteedt, maar deze ook wilt bijhouden in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8bf48-105">For example, this is useful when you are transitioning from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)], or if you outsource your payroll but also want to keep track of it in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="steps-to-import-payroll-data"></a><span data-ttu-id="8bf48-106">Stappen om salarisgegevens te importeren</span><span class="sxs-lookup"><span data-stu-id="8bf48-106">Steps to Import Payroll Data</span></span>
<span data-ttu-id="8bf48-107">De eerste stap is voor u, of wellicht uw accountant, om de exportfuncties in QuickBooks te gebruiken om de salarisgegevens naar een .IIF-bestand te exporteren.</span><span class="sxs-lookup"><span data-stu-id="8bf48-107">The first step is for you, or maybe your accountant, to use the export features in QuickBooks to export the payroll data to an .IIF file.</span></span> <span data-ttu-id="8bf48-108">De tweede stap is de pagina **Dagboeken** in [!INCLUDE[d365fin](includes/d365fin_md.md)] te openen en de actie **Salaristransacties importeren** te gebruiken om het bestand te importeren.</span><span class="sxs-lookup"><span data-stu-id="8bf48-108">The second step is to open the **General Journals** page in [!INCLUDE[d365fin](includes/d365fin_md.md)] and use the **Import Payroll Transactions** action to import the file.</span></span> <span data-ttu-id="8bf48-109">Tijdens het importproces koppelt u de grootboekrekeningen uit QuickBooks aan corresponderende rekeningen [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8bf48-109">During the import process you map the general ledger accounts from QuickBooks to corresponding accounts in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="8bf48-110">De laatste stap is de loonlijsttransacties in [!INCLUDE[d365fin](includes/d365fin_md.md)] te boeken op basis van de rekeningtoewijzing.</span><span class="sxs-lookup"><span data-stu-id="8bf48-110">The final step is to post the payroll transactions in [!INCLUDE[d365fin](includes/d365fin_md.md)] according to the account mapping.</span></span> 

<span data-ttu-id="8bf48-111">Zie [Salaristransacties importeren](finance-how-import-payroll-transactions.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8bf48-111">For more information, see [Import Payroll Transactions](finance-how-import-payroll-transactions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8bf48-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8bf48-112">See Also</span></span>
<span data-ttu-id="8bf48-113">[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="8bf48-113">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
<span data-ttu-id="8bf48-114">[Financiën](finance.md)  </span><span class="sxs-lookup"><span data-stu-id="8bf48-114">[Finance](finance.md)  </span></span>  
<span data-ttu-id="8bf48-115">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8bf48-115">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
