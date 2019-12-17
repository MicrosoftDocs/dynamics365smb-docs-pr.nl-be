---
title: 'Procedure: kostenbudgetposten verwijderen | Microsoft Docs'
description: Door middel van de batchtaak Kostenbudgetposten verwijderen annuleert u kostenbegrotingsposten uit het kostenbudgetregister.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 04510e87789e6d69b33009be7ebbaf7a405d0dff
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882717"
---
# <a name="delete-cost-budget-entries"></a><span data-ttu-id="d3e96-103">Kostenbudgetposten verwijderen</span><span class="sxs-lookup"><span data-stu-id="d3e96-103">Delete Cost Budget Entries</span></span>
<span data-ttu-id="d3e96-104">Door middel van de batchtaak **Kostenbudgetposten verwijderen** annuleert u kostenbegrotingsposten uit het kostenbudgetregister.</span><span class="sxs-lookup"><span data-stu-id="d3e96-104">You use the **Delete Cost Budget Entries** batch job to cancel cost budget entries from the cost budget register.</span></span>  

<span data-ttu-id="d3e96-105">Om hiaten in de kostenbudgetposten en kostenregisterposten te voorkomen, kunt u één enkele post of een reeks posten middenin een lijst met registerposten niet verwijderen.</span><span class="sxs-lookup"><span data-stu-id="d3e96-105">To prevent any gaps in the cost budget entries and cost register entries, you cannot delete a single entry or a batch of entries in the middle of the list of register entries.</span></span>  

### <a name="to-delete-a-cost-budget-entry"></a><span data-ttu-id="d3e96-106">Kostenbudgetposten verwijderen</span><span class="sxs-lookup"><span data-stu-id="d3e96-106">To delete a cost budget entry</span></span>  

1.  <span data-ttu-id="d3e96-107">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostenbudgetposten verwijderen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="d3e96-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Cost Budget Entries**, and then choose the related link.</span></span>  

    <span data-ttu-id="d3e96-108">Het veld **Naar journaalnr.**</span><span class="sxs-lookup"><span data-stu-id="d3e96-108">The **To Register No.**</span></span> <span data-ttu-id="d3e96-109">bevat het nummer van de laatste journaalpost en kan niet worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="d3e96-109">field contains the last register entry number and cannot be changed.</span></span>  

    <span data-ttu-id="d3e96-110">U kunt het veld **Van journaalnr.** gebruiken</span><span class="sxs-lookup"><span data-stu-id="d3e96-110">You can use the **From Register No.**</span></span> <span data-ttu-id="d3e96-111">om een nummer voor een journaalpost te selecteren waar de verwijdering moet beginnen.</span><span class="sxs-lookup"><span data-stu-id="d3e96-111">field to select a register entry number from which the deletion should begin.</span></span>  
2.  <span data-ttu-id="d3e96-112">Kies de knop **OK** om de geselecteerde kostenbegrotingsposten te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="d3e96-112">Choose the **OK** button to delete the selected cost budget entries.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d3e96-113">Om te voorkomen dat kostenbegrotingsposten onbedoeld worden verwijderd, kunt u journaalposten sluiten door de regels als **gesloten** te markeren in het veld **Gesloten** op de pagina **Kostenbudgetregisters**.</span><span class="sxs-lookup"><span data-stu-id="d3e96-113">To avoid an accidental deletion of cost budget entries, you can close register entries by marking the lines as **Closed** in the **Closed** field on the **Cost Budget Registers** page.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d3e96-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d3e96-114">See Also</span></span>  
<span data-ttu-id="d3e96-115">[Kosten verantwoorden](finance-manage-cost-accounting.md)
[Kostenbudgetten maken](finance-create-cost-budgets.md)</span><span class="sxs-lookup"><span data-stu-id="d3e96-115">[Accounting for Costs](finance-manage-cost-accounting.md)
[Creating Cost Budgets](finance-create-cost-budgets.md)</span></span>  
<span data-ttu-id="d3e96-116">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d3e96-116">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
