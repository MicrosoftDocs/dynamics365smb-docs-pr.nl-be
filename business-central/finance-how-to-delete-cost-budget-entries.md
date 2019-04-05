---
title: 'Procedure: kostenbudgetposten verwijderen | Microsoft Docs'
description: Door middel van de batchtaak Kostenbudgetposten verwijderen annuleert u kostenbegrotingsposten uit het kostenbudgetregister.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 7a5647bcb5a58cdf0a38ec037994d6cbe7a9504d
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816470"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="b7eda-103">Kostenbudgetposten verwijderen</span><span class="sxs-lookup"><span data-stu-id="b7eda-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="b7eda-104">Door middel van de batchtaak **Kostenbudgetposten verwijderen** annuleert u kostenbegrotingsposten uit het kostenbudgetregister.</span><span class="sxs-lookup"><span data-stu-id="b7eda-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="b7eda-105">Om hiaten in de kostenbudgetposten en kostenregisterposten te voorkomen, kunt u één enkele post of een reeks posten middenin een lijst met registerposten niet verwijderen.</span><span class="sxs-lookup"><span data-stu-id="b7eda-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="b7eda-106">Kostenbudgetposten verwijderen</span><span class="sxs-lookup"><span data-stu-id="b7eda-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="b7eda-107">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostenbudgetposten verwijderen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="b7eda-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="b7eda-108">Het veld **Naar journaalnr.**</span><span class="sxs-lookup"><span data-stu-id="b7eda-108">The **To Register No.**</span></span> <span data-ttu-id="b7eda-109">bevat het nummer van de laatste journaalpost en kan niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="b7eda-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="b7eda-110">U kunt het veld **Van journaalnr.** gebruiken</span><span class="sxs-lookup"><span data-stu-id="b7eda-110">You can use the **From Register No.**</span></span> <span data-ttu-id="b7eda-111">om een nummer voor een journaalpost te selecteren waar de verwijdering moet beginnen.</span><span class="sxs-lookup"><span data-stu-id="b7eda-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="b7eda-112">Kies de knop **OK** om de geselecteerde kostenbegrotingsposten te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="b7eda-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b7eda-113">Om te voorkomen dat kostenbegrotingsposten onbedoeld worden verwijderd, kunt u journaalposten sluiten door de regels als **gesloten** te markeren in het veld **Gesloten** op de pagina **Kostenbudgetregisters**.</span><span class="sxs-lookup"><span data-stu-id="b7eda-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b7eda-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b7eda-114">See Also</span></span>  
<span data-ttu-id="b7eda-115">[Kosten verantwoorden](finance-manage-cost-accounting.md)
[Kostenbudgetten maken](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="b7eda-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="b7eda-116">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b7eda-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
