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
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 1d0130dde256706460e58e5efc445bc5f4d5c595
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="06a16-103">De rekeningschema's instellen of wijzigen</span><span class="sxs-lookup"><span data-stu-id="06a16-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="06a16-104">Het rekeningschema bevat de grootboekrekeningen die uw financiële gegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="06a16-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="06a16-105"> bevat een standaardrekeningschema dat gereed is voor ondersteuning van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="06a16-105"> includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="06a16-106">Echter, kunt u de standaardrekeningen wijzigen en u kunt nieuwe rekeningen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="06a16-106">However, you can change the default accounts, and you can add new accounts.</span></span>  

## <a name="adding-or-changing-accounts"></a><span data-ttu-id="06a16-107">Rekeningen toevoegen of wijzigen</span><span class="sxs-lookup"><span data-stu-id="06a16-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="06a16-108">Vanuit het rekeningschema kunt u elke grootboekrekening openen en instellingen toevoegen of wijzigen.</span><span class="sxs-lookup"><span data-stu-id="06a16-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="06a16-109">U kunt een grootboekrekening verwijderen.</span><span class="sxs-lookup"><span data-stu-id="06a16-109">You can delete a general ledger account.</span></span> <span data-ttu-id="06a16-110">Echter, voordat u deze verwijdert, moet het volgende waar zijn:</span><span class="sxs-lookup"><span data-stu-id="06a16-110">However, before you delete it, the following must be true:</span></span>  

* <span data-ttu-id="06a16-111">Het saldo op de rekening moet nul zijn.</span><span class="sxs-lookup"><span data-stu-id="06a16-111">The balance on the account must be zero.</span></span>  
* <span data-ttu-id="06a16-112">Het veld **Grootboekrek.-verwijdering toestaan voor** moet zijn ingesteld in het venster **Grootboekinstelling** en de rekening mag geen grootboekposten op of na die datum hebben.</span><span class="sxs-lookup"><span data-stu-id="06a16-112">The **Allow G/L Acc. Deletion Before** field must be set in the **General Ledger Setup** window, and the account must not have ledger entries on or after that date.</span></span>  
* <span data-ttu-id="06a16-113">Als het veld **Grootboekrek.-gebruik controleren** in het venster **Grootboekinstellingen** is geselecteerd, mag de rekening niet worden gebruikt in boekingsgroepen of boekingsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="06a16-113">If the **Check G/L Account Usage** field in the **General Ledger Setup** window is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="06a16-114"> voorkomt dat u een grootboekrekening verwijdert die gegevens bevat die nodig zijn in het rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="06a16-114"> will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-also"></a><span data-ttu-id="06a16-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="06a16-115">See Also</span></span>
[<span data-ttu-id="06a16-116">Het grootboek en het rekeningschema</span><span class="sxs-lookup"><span data-stu-id="06a16-116">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="06a16-117">Bankrekeningen beheren</span><span class="sxs-lookup"><span data-stu-id="06a16-117">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="06a16-118">Werken met dimensies</span><span class="sxs-lookup"><span data-stu-id="06a16-118">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="06a16-119">Importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="06a16-119">Importing from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="06a16-120">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="06a16-120">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

