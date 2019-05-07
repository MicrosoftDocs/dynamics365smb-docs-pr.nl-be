---
title: 'Procedure: grootboekposten overbrengen naar kostenposten | Microsoft Docs'
description: U kunt grootboekposten overbrengen naar kostenposten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: a33fb434cc239de951d18783911c879587a3ace0
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/16/2019
ms.locfileid: "939046"
---
# <a name="transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="43cf7-103">Grootboekposten overbrengen naar kostenposten</span><span class="sxs-lookup"><span data-stu-id="43cf7-103">Transfer General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="43cf7-104">U kunt grootboekposten overbrengen naar kostenposten.</span><span class="sxs-lookup"><span data-stu-id="43cf7-104">You can transfer general ledger entries to cost entries.</span></span>  

<span data-ttu-id="43cf7-105">Voordat u begint met de bewerking om grootboekposten over te brengen naar kostenposten, moet u de overdracht voorbereiden zodat wordt voorkomen dat u fouten handmatig moet corrigeren die tijdens de boeking worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="43cf7-105">Before you run the process for transferring general ledger entries to cost entries, you must prepare the transfer to avoid manual correction posting.</span></span>  

## <a name="to-prepare-the-transfer"></a><span data-ttu-id="43cf7-106">De overdracht voorbereiden</span><span class="sxs-lookup"><span data-stu-id="43cf7-106">To prepare the transfer</span></span>  

1.  <span data-ttu-id="43cf7-107">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instelling van kostprijsboekhouding** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="43cf7-107">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Cost Accounting Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="43cf7-108">Controleer op de pagina **Instelling kostprijsboekhouding** of het veld **Begindatum voor GB-overdracht** op de juiste waarde is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="43cf7-108">On the **Cost Accounting Setup** page, verify that the **Starting Date for G/L Transfer** field is set to the correct value.</span></span>  
3.  <span data-ttu-id="43cf7-109">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostensoortschema** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="43cf7-109">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Cost Types**, and then choose the related link.</span></span>  
4.  <span data-ttu-id="43cf7-110">Controleer op de pagina **Kostensoortkaart** of het veld **Grootboekrekeningbereik** juist gekoppeld is voor elke kostensoort om posten uit het grootboek te halen.</span><span class="sxs-lookup"><span data-stu-id="43cf7-110">On the **Cost Type Card** page, verify that the **G/L Account Range** field is linked correctly for each cost type to take entries from the general ledger.</span></span>  
5.  <span data-ttu-id="43cf7-111">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="43cf7-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="43cf7-112">Voor elke gewenste grootboekrekening controleert u op de pagina **Grootboekrekening** of het veld **Nr. kostensoort**</span><span class="sxs-lookup"><span data-stu-id="43cf7-112">For each relevant general ledger account, on the **G/L Account Card** page, verify that the **Cost Type No.**</span></span> <span data-ttu-id="43cf7-113">juist is gekoppeld aan een kostensoort.</span><span class="sxs-lookup"><span data-stu-id="43cf7-113">field is linked correctly to a cost type.</span></span> <span data-ttu-id="43cf7-114">Zie [Kostenboekhouding instellen](finance-set-up-cost-accounting.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="43cf7-114">For more information, see [Setting Up Cost Accounting](finance-set-up-cost-accounting.md).</span></span>  
7.  <span data-ttu-id="43cf7-115">Controleer of alle relevante grootboekposten over dimensiewaarden beschikken die overeenkomen met een kostenplaats en een kostenobject.</span><span class="sxs-lookup"><span data-stu-id="43cf7-115">Verify that all relevant general ledger entries have dimension values that correspond to a cost center and a cost object.</span></span>  

## <a name="to-transfer-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="43cf7-116">Grootboekposten overbrengen naar kostenposten.</span><span class="sxs-lookup"><span data-stu-id="43cf7-116">To transfer general ledger entries to cost entries</span></span>  
1.  <span data-ttu-id="43cf7-117">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekposten overbrengen naar kostprijsboekhouding** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="43cf7-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Transfer GL Entries to CA**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="43cf7-118">Klik op **Ja** om de overdracht te starten.</span><span class="sxs-lookup"><span data-stu-id="43cf7-118">Choose the **Yes** button to start the transfer.</span></span> <span data-ttu-id="43cf7-119">Tijdens de bewerking worden alle grootboekposten overgebracht die niet al zijn overgebracht.</span><span class="sxs-lookup"><span data-stu-id="43cf7-119">The process transfers all general ledger entries that have not already been transferred.</span></span>  

    <span data-ttu-id="43cf7-120">Tijdens de overdracht worden door het proces verbindingen in de posten in de tabel **Kostenpost** en de tabel **Kostenregister** gemaakt.</span><span class="sxs-lookup"><span data-stu-id="43cf7-120">During the transfer, the process creates connections in the entries in the **Cost Entry** table and the **Cost Register** table.</span></span> <span data-ttu-id="43cf7-121">Hierdoor kunt de bron van de kostenposten traceren.</span><span class="sxs-lookup"><span data-stu-id="43cf7-121">This makes it possible to trace the source of cost entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="43cf7-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="43cf7-122">See Also</span></span>  
<span data-ttu-id="43cf7-123">[Kostenposten overbrengen en boeken](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="43cf7-123">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
[<span data-ttu-id="43cf7-124">Kostenboekhouding instellen</span><span class="sxs-lookup"><span data-stu-id="43cf7-124">Setting Up Cost Accounting</span></span>](finance-set-up-cost-accounting.md)   
