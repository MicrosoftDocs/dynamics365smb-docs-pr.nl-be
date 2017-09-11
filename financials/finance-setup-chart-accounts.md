---
title: De rekeningschema's instellen| Microsoft Docs
description: U wijzigt de standaardrekeningen in het rekeningschema en u kunt nieuwe rekeningen toevoegen.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ceb01999525139cabc7c31e2304f738dcc9267f8
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="4ab3c-103">De rekeningschema's instellen of wijzigen</span><span class="sxs-lookup"><span data-stu-id="4ab3c-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="4ab3c-104">Het rekeningschema bevat de grootboekrekeningen die uw financiële gegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="4ab3c-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]<span data-ttu-id="4ab3c-105"> bevat een standaardrekeningschema dat gereed is voor ondersteuning van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="4ab3c-105"> includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="4ab3c-106">Echter, kunt u de standaardrekeningen wijzigen en u kunt nieuwe rekeningen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="4ab3c-106">However, you can change the default accounts, and you can add new accounts.</span></span>  

## <a name="adding-or-changing-accounts"></a><span data-ttu-id="4ab3c-107">Rekeningen toevoegen of wijzigen</span><span class="sxs-lookup"><span data-stu-id="4ab3c-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="4ab3c-108">Vanuit het rekeningschema kunt u elke grootboekrekening openen en instellingen toevoegen of wijzigen.</span><span class="sxs-lookup"><span data-stu-id="4ab3c-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="4ab3c-109">U kunt een grootboekrekening verwijderen.</span><span class="sxs-lookup"><span data-stu-id="4ab3c-109">You can delete a general ledger account.</span></span> <span data-ttu-id="4ab3c-110">Echter, voordat u deze verwijdert, moet het volgende waar zijn:</span><span class="sxs-lookup"><span data-stu-id="4ab3c-110">However, before you delete it, the following must be true:</span></span>  

* <span data-ttu-id="4ab3c-111">Het saldo op de rekening moet nul zijn.</span><span class="sxs-lookup"><span data-stu-id="4ab3c-111">The balance on the account must be zero.</span></span>  
* <span data-ttu-id="4ab3c-112">Het veld **Grootboekrek.-verwijdering toestaan voor** moet zijn ingesteld in het venster **Grootboekinstelling** en de rekening mag geen grootboekposten op of na die datum hebben.</span><span class="sxs-lookup"><span data-stu-id="4ab3c-112">The **Allow G/L Acc. Deletion Before** field must be set in the **General Ledger Setup** window, and the account must not have ledger entries on or after that date.</span></span>  
* <span data-ttu-id="4ab3c-113">Als het veld **Grootboekrek.-gebruik controleren** in het venster **Grootboekinstellingen** is geselecteerd, mag de rekening niet worden gebruikt in boekingsgroepen of boekingsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="4ab3c-113">If the **Check G/L Account Usage** field in the **General Ledger Setup** window is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="4ab3c-114"> voorkomt dat u een grootboekrekening verwijdert die gegevens bevat die nodig zijn in het rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="4ab3c-114"> will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4ab3c-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="4ab3c-115">See Also</span></span>
[<span data-ttu-id="4ab3c-116">Het grootboek en het rekeningschema</span><span class="sxs-lookup"><span data-stu-id="4ab3c-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="4ab3c-117">Bankrekeningen beheren</span><span class="sxs-lookup"><span data-stu-id="4ab3c-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="4ab3c-118">Werken met dimensies</span><span class="sxs-lookup"><span data-stu-id="4ab3c-118">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="4ab3c-119">Importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="4ab3c-119">Importing from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="4ab3c-120">Procedure: Met GIFI-codes werken in Canada</span><span class="sxs-lookup"><span data-stu-id="4ab3c-120">How to: Work With GIFI Codes in Canada</span></span>](ca-finance-work-gifi-codes.md)  
<span data-ttu-id="4ab3c-121">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4ab3c-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
