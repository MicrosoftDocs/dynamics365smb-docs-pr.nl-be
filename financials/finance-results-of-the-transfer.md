---
title: Resultaten van de overdracht | Microsoft Docs
description: In dit onderwerp wordt beschreven wat er gebeurt wanneer u grootboekposten overbrengt naar kostenposten.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d479727b8d0cbb4b4ec9f127136f4e0578b8afb7
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="1e3c8-103">Resultaten van het overbrengen van grootboekposten naar kostenposten</span><span class="sxs-lookup"><span data-stu-id="1e3c8-103">Results of Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="1e3c8-104">Tijdens de overdracht van grootboekposten naar kostenposten, maakt [!INCLUDE[d365fin](includes/d365fin_md.md)] verbindingen aan in de posten in de tabel **Grootboekpost**, de tabel **Kostenpost** en de tabel **Kostenregister** om de verbindingen tussen kostenposten en grootboekposten te kunnen traceren.</span><span class="sxs-lookup"><span data-stu-id="1e3c8-104">During the transfer of general ledger entries to cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates connections in the entries in the **G/L Entry** table, the **Cost Entry** table, and the **Cost Register** table to make it possible to trace the connections between cost entries and general ledger entries.</span></span>  

## <a name="general-ledger-entries"></a><span data-ttu-id="1e3c8-105">Grootboekposten</span><span class="sxs-lookup"><span data-stu-id="1e3c8-105">General Ledger Entries</span></span>  
<span data-ttu-id="1e3c8-106">Voor elke grootboekpost die wordt overgebracht naar kostprijsboekhouding, vult [!INCLUDE[d365fin](includes/d365fin_md.md)] de kosten in het veld **Postnr.** in.</span><span class="sxs-lookup"><span data-stu-id="1e3c8-106">For each general ledger entry that is transferred to cost accounting, [!INCLUDE[d365fin](includes/d365fin_md.md)] fills the cost **Entry No.** field.</span></span>  

## <a name="cost-entries"></a><span data-ttu-id="1e3c8-107">Kostenposten</span><span class="sxs-lookup"><span data-stu-id="1e3c8-107">Cost Entries</span></span>  
<span data-ttu-id="1e3c8-108">Voor elke kostenpost slaat [!INCLUDE[d365fin](includes/d365fin_md.md)] het nummer van de bijbehorende grootboekpost op in het veld **Grootboekpostnr.** in de tabel **Kostenpost**.</span><span class="sxs-lookup"><span data-stu-id="1e3c8-108">For each cost entry, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the corresponding general ledger entry in the **G/L Entry No.** field in the **Cost Entry** table.</span></span>  

<span data-ttu-id="1e3c8-109">Voor gecombineerde kostenposten slaat [!INCLUDE[d365fin](includes/d365fin_md.md)] het nummer van de laatste grootboekpost op; dit is de post met het hoogste nummer.</span><span class="sxs-lookup"><span data-stu-id="1e3c8-109">For combined cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the last general ledger entry, which is the entry with the highest entry number.</span></span>  

<span data-ttu-id="1e3c8-110">Het veld **Grootboekrekening** in de tabel **Kostenpost** bevat het nummer van de grootboekrekening waaruit de kostenpost afkomstig is.</span><span class="sxs-lookup"><span data-stu-id="1e3c8-110">The **G/L Account** field in the **Cost Entry** table contains the number of the general ledger account that the cost entry came from.</span></span>  

<span data-ttu-id="1e3c8-111">Voor enkele kostenposten wordt de boekingstekst door [!INCLUDE[d365fin](includes/d365fin_md.md)] uit de grootboekpost overgebracht naar het tekstveld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="1e3c8-111">For single cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfers the posting text from the general ledger entry to the **Description** text field.</span></span> <span data-ttu-id="1e3c8-112">Voor gecombineerde posten laat dit tekstveld zien dat deze posten als gecombineerde posten zijn overgebracht.</span><span class="sxs-lookup"><span data-stu-id="1e3c8-112">For combined entries, the text field shows these entries are transferred as combined entries.</span></span> <span data-ttu-id="1e3c8-113">Voor een gecombineerde post voor de maand oktober 2013 luidt de tekst mogelijk bijvoorbeeld **Gecombineerde posten, oktober 2013**.</span><span class="sxs-lookup"><span data-stu-id="1e3c8-113">For example, for a combined entry for the month of October in 2013, the text can be **Combined Entries, October 2013**.</span></span>  

## <a name="cost-register"></a><span data-ttu-id="1e3c8-114">Kostenregister</span><span class="sxs-lookup"><span data-stu-id="1e3c8-114">Cost Register</span></span>  
<span data-ttu-id="1e3c8-115">In de tabel **Kostenregister**, wordt door [!INCLUDE[d365fin](includes/d365fin_md.md)] een post gemaakt met de bronoverdracht van het grootboek.</span><span class="sxs-lookup"><span data-stu-id="1e3c8-115">In the **Cost Register** table, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates an entry with the source transfer from general ledger.</span></span> <span data-ttu-id="1e3c8-116">Door de post worden de eerste en laatste nummers van de overgebrachte grootboekposten vastgelegd, evenals de eerste en laatste nummers van de kostenposten die zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1e3c8-116">The entry records the first and last entry numbers of the general ledger entries that are transferred, in addition to the first and last entry numbers of the cost entries that are created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1e3c8-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1e3c8-117">See Also</span></span>  
<span data-ttu-id="1e3c8-118">[Grootboekposten overbrengen naar kostenposten](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="1e3c8-118">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
<span data-ttu-id="1e3c8-119">[Criteria voor het overbrengen van grootboekposten naar kostenposten.](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="1e3c8-119">[Criteria for Transferring General Ledger Entries to Cost Entries](finance-criteria-for-transferring-general-ledger-entries-to-cost-entries.md) </span></span>  
<span data-ttu-id="1e3c8-120">[Automatische overdracht en gecombineerde posten](finance-automatic-transfer-combined-entries.md) </span><span class="sxs-lookup"><span data-stu-id="1e3c8-120">[Automatic Transfer and Combined Entries](finance-automatic-transfer-combined-entries.md) </span></span>  
[<span data-ttu-id="1e3c8-121">Kostenposten overbrengen en boeken</span><span class="sxs-lookup"><span data-stu-id="1e3c8-121">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)  

