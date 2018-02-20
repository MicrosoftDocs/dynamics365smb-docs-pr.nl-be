---
title: 'Procedure: grootboekposten overbrengen naar kostenposten | Microsoft Docs'
description: U kunt grootboekposten overbrengen naar kostenposten.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 592f42f53593735526ccbd3ddaa69bb0778de0ac
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="17d3c-103">Grootboekposten overbrengen naar kostenposten</span><span class="sxs-lookup"><span data-stu-id="17d3c-103">Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="17d3c-104">U kunt grootboekposten overbrengen naar kostenposten.</span><span class="sxs-lookup"><span data-stu-id="17d3c-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="17d3c-105">Voordat u begint met de bewerking om grootboekposten over te brengen naar kostenposten, moet u de overdracht voorbereiden zodat wordt voorkomen dat u fouten handmatig moet corrigeren die tijdens de boeking worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="17d3c-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="17d3c-106">De overdracht voorbereiden</span><span class="sxs-lookup"><span data-stu-id="17d3c-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="17d3c-107">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Instelling kostprijsboekhouding** en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="17d3c-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="17d3c-108">Controleer in het venster **Instelling kostprijsboekhouding** of het veld **Begindatum voor GB-overdracht** op de juiste waarde is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="17d3c-108">In the **Cost Accounting Setup** window, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="17d3c-109">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Kostensoortschema** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="17d3c-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="17d3c-110">Controleer in het venster **Kostensoortkaart** of het veld **Grootboekrekeningbereik** juist gekoppeld is voor elke kostensoort om posten uit het grootboek te halen.</span><span class="sxs-lookup"><span data-stu-id="17d3c-110">In the **Cost Type Card** window, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="17d3c-111">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rekeningschema** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="17d3c-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="17d3c-112">Voor elke gewenste grootboekrekening controleert u in het venster **Grootboekrekening** of het veld **Nr. kostensoort**</span><span class="sxs-lookup"><span data-stu-id="17d3c-112">For each relevant general ledger account, in the **G/L Account Card** window, verify that the **Cost Type No.**</span></span> <span data-ttu-id="17d3c-113">juist is gekoppeld aan een kostensoort.</span><span class="sxs-lookup"><span data-stu-id="17d3c-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="17d3c-114">Zie voor meer informatie [De relatie tussen de kostensoorten en grootboekrekeningen definiëren](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="17d3c-114">For more information, see [Defining the Relationship Between Cost Types and General Ledger Accounts](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md).</span></span>  
7.  <span data-ttu-id="17d3c-115">Controleer of alle relevante grootboekposten over dimensiewaarden beschikken die overeenkomen met een kostenplaats en een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="17d3c-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="17d3c-116">Grootboekposten overbrengen naar kostenposten.</span><span class="sxs-lookup"><span data-stu-id="17d3c-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="17d3c-117">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Grootboekposten overbrengen naar kostprijsboekhouding** in en klik op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="17d3c-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="17d3c-118">Klik op **Ja** om de overdracht te starten.</span><span class="sxs-lookup"><span data-stu-id="17d3c-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="17d3c-119">Tijdens de bewerking worden alle grootboekposten overgebracht die niet al zijn overgebracht.</span><span class="sxs-lookup"><span data-stu-id="17d3c-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="17d3c-120">Tijdens de overdracht worden door het proces verbindingen in de posten in de tabel **Kostenpost** en de tabel **Kostenregister** gemaakt.</span><span class="sxs-lookup"><span data-stu-id="17d3c-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="17d3c-121">Hierdoor kunt de bron van de kostenposten traceren.</span><span class="sxs-lookup"><span data-stu-id="17d3c-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="17d3c-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="17d3c-122">See Also</span></span>  
 <span data-ttu-id="17d3c-123">[Criteria voor het overbrengen van grootboekposten naar kostenposten.](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="17d3c-123">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="17d3c-124">[Automatische overdracht en gecombineerde posten](finance-automatic-transfer-combined-entries.md) </span><span class="sxs-lookup"><span data-stu-id="17d3c-124">[Automatic Transfer and Combined Entries](finance-automatic-transfer-combined-entries.md) </span></span>  
 <span data-ttu-id="17d3c-125">[Resultaten van de overboeking](finance-results-of-the-transfer.md) </span><span class="sxs-lookup"><span data-stu-id="17d3c-125">[Results of the Transfer](finance-results-of-the-transfer.md) </span></span>  
 <span data-ttu-id="17d3c-126">[Kostenposten overbrengen en boeken](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="17d3c-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="17d3c-127">De relatie tussen de kostensoorten en grootboekrekeningen definiëren</span><span class="sxs-lookup"><span data-stu-id="17d3c-127">Defining the Relationship Between Cost Types and General Ledger Accounts</span></span>](finance-defining-the-relationship-between-cost-types-and-general-ledger-accounts.md)   

