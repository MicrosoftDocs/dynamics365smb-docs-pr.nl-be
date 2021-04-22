---
title: De jaareinde-ultimopost boeken
description: Beschrijft hoe u het dagboek opent dat u hebt opgegeven in de batchverwerking Afsluiten WenV-rekening en vervolgens de jaareinde-ultimopost controleert en boekt.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5c822685ae5723bc6b13f9fedad45dbddefdb956
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5776604"
---
# <a name="post-the-year-end-closing-entry"></a><span data-ttu-id="edf71-103">De jaareinde-ultimopost boeken</span><span class="sxs-lookup"><span data-stu-id="edf71-103">Post the Year-End Closing Entry</span></span>

<span data-ttu-id="edf71-104">Nadat u de batchverwerking **Afsluiten WenV-rekening** hebt gebruikt om de jaareinde-ultimopost of -posten te boeken, moet u het dagboek openen dat u in de batchverwerking hebt opgegeven en vervolgens de posten herzien en boeken.</span><span class="sxs-lookup"><span data-stu-id="edf71-104">After you use the **Close Income Statement** batch job to generate the year-end closing entry or entries, you must open the journal you specified in the batch job, and then review and post the entries.</span></span>  

> [!TIP]
> <span data-ttu-id="edf71-105">Afhankelijk van de werkprocessen van uw organisatie, kunt u ervoor kiezen om boekhoudkundige perioden en boekjaren wel of niet af te sluiten in [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="edf71-105">Depending on your organizations work processes, you can choose to close or not close accounting periods and fiscal years in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="edf71-106">Bij de volgende procedure wordt ervan uitgegaan dat u het boekjaar hebt afgesloten met de optie *Boekhoudperioden*, een jaarafsluitingspost hebt gegenereerd met behulp van de batchverwerking **Resultatenrekeningen sluiten** en nu klaar bent om de jaarafsluitingspost te boeken samen met de uitstellende vermogensrekeningboekingen.</span><span class="sxs-lookup"><span data-stu-id="edf71-106">The following procedure assumes that you have closed the fiscal year using the *Accounting Periods* option, generated a year-end closing entry using the **Close Income Statement** batch job, and are now ready to post the year-end closing entry along with the offsetting equity account entries.</span></span> <span data-ttu-id="edf71-107">Uw organisatie kan ervoor kiezen om anders te werken, zoals het boeken van de jaarafsluitingspost als onderdeel van het afsluiten van het boekjaar.</span><span class="sxs-lookup"><span data-stu-id="edf71-107">Your organization can choose to work differently, such as post the year-end closing entry as part of closing the fiscal year.</span></span>

## <a name="to-post-the-year-end-closing-entry"></a><span data-ttu-id="edf71-108">De jaareinde-ultimopost boeken</span><span class="sxs-lookup"><span data-stu-id="edf71-108">To post the year end closing entry</span></span>

1. <span data-ttu-id="edf71-109">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Dagboek** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="edf71-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="edf71-110">Selecteer op de pagina **Diversendagboek** in het veld **Batchnaam** de batch die de ultimoposten bevat.</span><span class="sxs-lookup"><span data-stu-id="edf71-110">On the **General Journal** page, in the **Batch Name** field, select the batch that contains the closing entries.</span></span>
3. <span data-ttu-id="edf71-111">Controleer de posten.</span><span class="sxs-lookup"><span data-stu-id="edf71-111">Review the entries.</span></span>
4. <span data-ttu-id="edf71-112">Kies de actie **Boeken** om het dagboek te boeken.</span><span class="sxs-lookup"><span data-stu-id="edf71-112">To post the journal, choose the **Post** action.</span></span>

> [!NOTE]  
> <span data-ttu-id="edf71-113">Als een fout wordt gedetecteerd, wordt een foutbericht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="edf71-113">If an error is detected, an error message is displayed.</span></span> <span data-ttu-id="edf71-114">Als de boeking is geslaagd, worden de geboekte posten uit het dagboek gehaald.</span><span class="sxs-lookup"><span data-stu-id="edf71-114">If the posting is successful, the posted entries are removed from the journal.</span></span> <span data-ttu-id="edf71-115">Nadat de boeking is voltooid, wordt een post geboekt in elke resultatenrekening zodat het saldo nul wordt en het jaarresultaat wordt overgebracht naar de balans.</span><span class="sxs-lookup"><span data-stu-id="edf71-115">After posting is complete, an entry is posted to each income statement account so that its balance becomes zero and the year's result is transferred to the balance sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="edf71-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="edf71-116">See Also</span></span>

[<span data-ttu-id="edf71-117">Boekhoudperioden afsluiten</span><span class="sxs-lookup"><span data-stu-id="edf71-117">Close Accounting Periods</span></span>](year-close-account-periods.md)  
[<span data-ttu-id="edf71-118">Boeken afsluiten</span><span class="sxs-lookup"><span data-stu-id="edf71-118">Closing Books</span></span>](year-close-books.md)  
[<span data-ttu-id="edf71-119">Afsluiten WenV-rekening</span><span class="sxs-lookup"><span data-stu-id="edf71-119">Close Income Statement</span></span>](year-close-income-statement.md)  
<span data-ttu-id="edf71-120">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="edf71-120">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]