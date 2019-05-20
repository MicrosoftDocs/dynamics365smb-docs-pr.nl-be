---
title: Resultaten van de overdracht | Microsoft Docs
description: In dit onderwerp wordt beschreven wat er gebeurt wanneer u grootboekposten overbrengt naar kostenposten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: general ledger, transfer, cost entries
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 590c1501f9da2c7c343b5c2f3617df873fcd3b7a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242503"
---
# <a name="results-of-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="5cb3c-103">Resultaten van het overbrengen van grootboekposten naar kostenposten</span><span class="sxs-lookup"><span data-stu-id="5cb3c-103">Results of Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="5cb3c-104">Tijdens de overdracht van grootboekposten naar kostenposten, maakt [!INCLUDE[d365fin](includes/d365fin_md.md)] verbindingen aan in de posten in de tabel **Grootboekpost**, de tabel **Kostenpost** en de tabel **Kostenregister** om de verbindingen tussen kostenposten en grootboekposten te kunnen traceren.</span><span class="sxs-lookup"><span data-stu-id="5cb3c-104">During the transfer of general ledger entries to cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates connections in the entries in the **G/L Entry** table, the **Cost Entry** table, and the **Cost Register** table to make it possible to trace the connections between cost entries and general ledger entries.</span></span>  

## <a name="general-ledger-entries"></a><span data-ttu-id="5cb3c-105">Grootboekposten</span><span class="sxs-lookup"><span data-stu-id="5cb3c-105">General Ledger Entries</span></span>  
<span data-ttu-id="5cb3c-106">Voor elke grootboekpost die wordt overgebracht naar kostprijsboekhouding, vult [!INCLUDE[d365fin](includes/d365fin_md.md)] de kosten in het veld **Postnr.** in.</span><span class="sxs-lookup"><span data-stu-id="5cb3c-106">For each general ledger entry that is transferred to cost accounting, [!INCLUDE[d365fin](includes/d365fin_md.md)] fills the cost **Entry No.** field.</span></span>  

## <a name="cost-entries"></a><span data-ttu-id="5cb3c-107">Kostenposten</span><span class="sxs-lookup"><span data-stu-id="5cb3c-107">Cost Entries</span></span>  
<span data-ttu-id="5cb3c-108">Voor elke kostenpost slaat [!INCLUDE[d365fin](includes/d365fin_md.md)] het nummer van de bijbehorende grootboekpost op in het veld **Grootboekpostnr.** in de tabel **Kostenpost**.</span><span class="sxs-lookup"><span data-stu-id="5cb3c-108">For each cost entry, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the corresponding general ledger entry in the **G/L Entry No.** field in the **Cost Entry** table.</span></span>  

<span data-ttu-id="5cb3c-109">Voor gecombineerde kostenposten slaat [!INCLUDE[d365fin](includes/d365fin_md.md)] het nummer van de laatste grootboekpost op; dit is de post met het hoogste nummer.</span><span class="sxs-lookup"><span data-stu-id="5cb3c-109">For combined cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] saves the entry number of the last general ledger entry, which is the entry with the highest entry number.</span></span>  

<span data-ttu-id="5cb3c-110">Het veld **Grootboekrekening** in de tabel **Kostenpost** bevat het nummer van de grootboekrekening waaruit de kostenpost afkomstig is.</span><span class="sxs-lookup"><span data-stu-id="5cb3c-110">The **G/L Account** field in the **Cost Entry** table contains the number of the general ledger account that the cost entry came from.</span></span>  

<span data-ttu-id="5cb3c-111">Voor enkele kostenposten wordt de boekingstekst door [!INCLUDE[d365fin](includes/d365fin_md.md)] uit de grootboekpost overgebracht naar het tekstveld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="5cb3c-111">For single cost entries, [!INCLUDE[d365fin](includes/d365fin_md.md)] transfers the posting text from the general ledger entry to the **Description** text field.</span></span> <span data-ttu-id="5cb3c-112">Voor gecombineerde posten laat dit tekstveld zien dat deze posten als gecombineerde posten zijn overgebracht.</span><span class="sxs-lookup"><span data-stu-id="5cb3c-112">For combined entries, the text field shows these entries are transferred as combined entries.</span></span> <span data-ttu-id="5cb3c-113">Voor een gecombineerde post voor de maand oktober 2013 luidt de tekst mogelijk bijvoorbeeld **Gecombineerde posten, oktober 2013**.</span><span class="sxs-lookup"><span data-stu-id="5cb3c-113">For example, for a combined entry for the month of October in 2013, the text can be **Combined Entries, October 2013**.</span></span>  

## <a name="cost-register"></a><span data-ttu-id="5cb3c-114">Kostenregister</span><span class="sxs-lookup"><span data-stu-id="5cb3c-114">Cost Register</span></span>  
<span data-ttu-id="5cb3c-115">In de tabel **Kostenregister**, wordt door [!INCLUDE[d365fin](includes/d365fin_md.md)] een post gemaakt met de bronoverdracht van het grootboek.</span><span class="sxs-lookup"><span data-stu-id="5cb3c-115">In the **Cost Register** table, [!INCLUDE[d365fin](includes/d365fin_md.md)] creates an entry with the source transfer from general ledger.</span></span> <span data-ttu-id="5cb3c-116">Door de post worden de eerste en laatste nummers van de overgebrachte grootboekposten vastgelegd, evenals de eerste en laatste nummers van de kostenposten die zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="5cb3c-116">The entry records the first and last entry numbers of the general ledger entries that are transferred, in addition to the first and last entry numbers of the cost entries that are created.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5cb3c-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5cb3c-117">See Also</span></span>  
[<span data-ttu-id="5cb3c-118">Kostenposten overbrengen en boeken</span><span class="sxs-lookup"><span data-stu-id="5cb3c-118">Transferring and Posting Cost Entries</span></span>](finance-transfer-and-post-cost-entries.md)   
