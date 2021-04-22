---
title: Een rekeningschema instellen
description: U wijzigt de standaardrekeningen in het rekeningschema en u kunt nieuwe rekeningen toevoegen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5257a2ea50ed18366de899607b81e50684f16ffc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773892"
---
# <a name="setting-up-or-changing-the-chart-of-accounts"></a><span data-ttu-id="82c8a-103">De rekeningschema's instellen of wijzigen</span><span class="sxs-lookup"><span data-stu-id="82c8a-103">Setting Up or Changing the Chart of Accounts</span></span>
<span data-ttu-id="82c8a-104">Het rekeningschema bevat de grootboekrekeningen die uw financiële gegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="82c8a-104">The chart of accounts shows the ledger accounts that store your financial data.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="82c8a-105">bevat een standaardrekeningschema dat gereed is voor ondersteuning van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="82c8a-105">includes a standard chart of accounts that is ready to support your business.</span></span>
<span data-ttu-id="82c8a-106">Echter, kunt u de standaardrekeningen wijzigen en u kunt nieuwe rekeningen toevoegen.</span><span class="sxs-lookup"><span data-stu-id="82c8a-106">However, you can change the default accounts, and you can add new accounts.</span></span>
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]


## <a name="adding-or-changing-accounts"></a><span data-ttu-id="82c8a-107">Rekeningen toevoegen of wijzigen</span><span class="sxs-lookup"><span data-stu-id="82c8a-107">Adding or Changing Accounts</span></span>
<span data-ttu-id="82c8a-108">Vanuit het rekeningschema kunt u elke grootboekrekening openen en instellingen toevoegen of wijzigen.</span><span class="sxs-lookup"><span data-stu-id="82c8a-108">From the chart of accounts, you can open each G/L account and add or change settings.</span></span>

> [!NOTE]  
>   <span data-ttu-id="82c8a-109">U kunt een grootboekrekening verwijderen.</span><span class="sxs-lookup"><span data-stu-id="82c8a-109">You can delete a general ledger account.</span></span> <span data-ttu-id="82c8a-110">Echter, voordat u deze verwijdert, moet het volgende waar zijn:</span><span class="sxs-lookup"><span data-stu-id="82c8a-110">However, before you delete it, the following must be true:</span></span>  
>  
>   * <span data-ttu-id="82c8a-111">Het saldo op de rekening moet nul zijn.</span><span class="sxs-lookup"><span data-stu-id="82c8a-111">The balance on the account must be zero.</span></span>  
>   * <span data-ttu-id="82c8a-112">Het veld **Grootboekrek.-verwijdering toestaan voor** moet zijn ingesteld op de pagina **Grootboekinstelling** en de rekening mag geen grootboekposten op of na die datum hebben.</span><span class="sxs-lookup"><span data-stu-id="82c8a-112">The **Allow G/L Acc. Deletion Before** field must be set on the **General Ledger Setup** page, and the account must not have ledger entries on or after that date.</span></span>  
>   * <span data-ttu-id="82c8a-113">Als het veld **Grootboekrek.-gebruik controleren** op de pagina **Grootboekinstellingen** is geselecteerd, mag de rekening niet worden gebruikt in boekingsgroepen of boekingsinstellingen.</span><span class="sxs-lookup"><span data-stu-id="82c8a-113">If the **Check G/L Account Usage** field on the **General Ledger Setup** page is selected, then the account must not be used in any posting groups or posting setup.</span></span>  

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="82c8a-114">voorkomt dat u een grootboekrekening verwijdert die gegevens bevat die nodig zijn in het rekeningschema.</span><span class="sxs-lookup"><span data-stu-id="82c8a-114">will prevent you from deleting a general ledger account that stores data that is needed in the chart of accounts.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="82c8a-115">Zie Gerelateerde training op [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="82c8a-115">See Related Training at [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="82c8a-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="82c8a-116">See Also</span></span>
[<span data-ttu-id="82c8a-117">Het grootboek en het rekeningschema</span><span class="sxs-lookup"><span data-stu-id="82c8a-117">The General Ledger and the Chart of Accounts</span></span>](finance-general-ledger.md)  
[<span data-ttu-id="82c8a-118">Bankrekeningen reconciliëren</span><span class="sxs-lookup"><span data-stu-id="82c8a-118">Reconciling Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="82c8a-119">Werken met dimensies</span><span class="sxs-lookup"><span data-stu-id="82c8a-119">Working with Dimensions</span></span>](finance-dimensions.md)  
[<span data-ttu-id="82c8a-120">Gegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="82c8a-120">Importing Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="82c8a-121">Werken met rekeningschema's</span><span class="sxs-lookup"><span data-stu-id="82c8a-121">Work with Account Schedules</span></span>](bi-how-work-account-schedule.md)  
<span data-ttu-id="82c8a-122">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="82c8a-122">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]