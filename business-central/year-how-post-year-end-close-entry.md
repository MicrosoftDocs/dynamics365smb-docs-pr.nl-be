---
title: Jaareinde-ultimopost controleren en boeken | Microsoft Docs
description: Beschrijft hoe u het dagboek opent dat u hebt opgegeven in de batchverwerking Afsluiten WenV-rekening en vervolgens de jaareinde-ultimopost controleert en boekt.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: cd555cc389ff7d9e306645475ef042f7ee9bc934
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "817100"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="964fd-103">De jaareinde-ultimopost boeken</span><span class="sxs-lookup"><span data-stu-id="964fd-103">Post the Year-End Closing Entry</span></span>
<span data-ttu-id="964fd-104">Nadat u de batchverwerking **Afsluiten WenV-rekening** hebt gebruikt om de jaareinde-ultimopost of -posten te boeken, moet u het dagboek openen dat u in de batchverwerking hebt opgegeven en vervolgens de posten herzien en boeken.</span><span class="sxs-lookup"><span data-stu-id="964fd-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="964fd-105">De jaareinde-ultimopost boeken</span><span class="sxs-lookup"><span data-stu-id="964fd-105">To post the year end closing entry</span></span>
1. <span data-ttu-id="964fd-106">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Fin. dagboek** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="964fd-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="964fd-107">Selecteer op de pagina **Diversendagboek** in het veld **Batchnaam** de batch die de ultimoposten bevat.</span><span class="sxs-lookup"><span data-stu-id="964fd-107">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="964fd-108">Controleer de posten.</span><span class="sxs-lookup"><span data-stu-id="964fd-108">Review the entries.</span></span>
4. <span data-ttu-id="964fd-109">Kies de actie **Boeken** om het dagboek te boeken.</span><span class="sxs-lookup"><span data-stu-id="964fd-109">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="964fd-110">Als een fout wordt gedetecteerd, wordt een foutbericht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="964fd-110">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="964fd-111">Als de boeking is geslaagd, worden de geboekte posten uit het dagboek gehaald.</span><span class="sxs-lookup"><span data-stu-id="964fd-111">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="964fd-112">Nadat de boeking is voltooid, wordt een post geboekt in elke resultatenrekening zodat het saldo nul wordt en het jaarresultaat wordt overgebracht naar de balans.</span><span class="sxs-lookup"><span data-stu-id="964fd-112">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="964fd-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="964fd-113">See Also</span></span>
[<span data-ttu-id="964fd-114">Boekhoudperioden afsluiten</span><span class="sxs-lookup"><span data-stu-id="964fd-114">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="964fd-115">Boeken afsluiten</span><span class="sxs-lookup"><span data-stu-id="964fd-115">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="964fd-116">Afsluiten WenV-rekening</span><span class="sxs-lookup"><span data-stu-id="964fd-116">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="964fd-117">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="964fd-117">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
