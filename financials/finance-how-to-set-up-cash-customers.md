---
title: 'Procedure: Contant betalende klanten instellen| Microsoft Docs'
description: In dit onderwerp worden de stappen voor het instellen van klanten die contant betalen beschreven.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/11/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: a6be13d3f2fcc683e8d711691f9d994f64458f85
ms.contentlocale: nl-be
ms.lasthandoff: 04/16/2018

---
# <a name="set-up-cash-customers"></a><span data-ttu-id="44b9b-103">Contant betalende klanten instellen</span><span class="sxs-lookup"><span data-stu-id="44b9b-103">Set Up Cash Customers</span></span>
<span data-ttu-id="44b9b-104">U kunt geen factuur zonder klantnummer maken.</span><span class="sxs-lookup"><span data-stu-id="44b9b-104">You cannot create an invoice without a customer number.</span></span> <span data-ttu-id="44b9b-105">Dit geldt ook voor contante verkopen waarbij u geen gegevens voor een klantenrekening hoeft in te voeren.</span><span class="sxs-lookup"><span data-stu-id="44b9b-105">This is true, even if you make a cash sale and do not have anything to record in a customer account.</span></span>  

## <a name="to-set-up-a-cash-customer"></a><span data-ttu-id="44b9b-106">Een contant betalende klant instellen</span><span class="sxs-lookup"><span data-stu-id="44b9b-106">To set up a cash customer</span></span>  
1. <span data-ttu-id="44b9b-107">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Klant** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="44b9b-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer**, and then choose the related link.</span></span>  
2. <span data-ttu-id="44b9b-108">Maak een nieuwe **klant**-kaart.</span><span class="sxs-lookup"><span data-stu-id="44b9b-108">Create a new **Customer** card.</span></span> <span data-ttu-id="44b9b-109">Zie voor meer informatie [Nieuwe klanten registreren](sales-how-register-new-customers.md).</span><span class="sxs-lookup"><span data-stu-id="44b9b-109">For more information, see [Register New Customers](sales-how-register-new-customers.md).</span></span>
3. <span data-ttu-id="44b9b-110">Selecteer in het veld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="44b9b-110">In the **No.**</span></span> <span data-ttu-id="44b9b-111">bijvoorbeeld **Kas** in.</span><span class="sxs-lookup"><span data-stu-id="44b9b-111">field, enter **Cash**, for example.</span></span>  
4. <span data-ttu-id="44b9b-112">Geef in het veld **Naam** bijvoorbeeld **Contante verkoop** op.</span><span class="sxs-lookup"><span data-stu-id="44b9b-112">In the **Name** field, enter **Cash Sale**, for example.</span></span>  
5. <span data-ttu-id="44b9b-113">Vul op het sneltabblad **Facturering** de velden **Klantboekingsgroep** en **Bedrijfsboekingsgroep** in.</span><span class="sxs-lookup"><span data-stu-id="44b9b-113">On the **Invoicing** FastTab, fill in the **Customer Posting Group** and the **Gen. Bus. Posting Group** fields.</span></span>  

   <span data-ttu-id="44b9b-114">U hebt nu voldoende gegevens voor de klant ingesteld om deze te factureren.</span><span class="sxs-lookup"><span data-stu-id="44b9b-114">Now you have set up a customer that contains sufficient information for invoicing.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="44b9b-115">Mogelijk hebt u een boekingsgroep gekozen die tevens wordt gebruikt voor binnenlandse verkopen op krediet.</span><span class="sxs-lookup"><span data-stu-id="44b9b-115">You may have chosen a posting group that is also used for domestic credit sales.</span></span> <span data-ttu-id="44b9b-116">Als u afzonderlijke gegevens over contante verkopen wilt bijhouden, bijvoorbeeld met een speciale verkoop- of centralisatierekening, kunt u hiervoor een extra boekingsgroep instellen.</span><span class="sxs-lookup"><span data-stu-id="44b9b-116">If you want to maintain separate data on cash sales, for example, with a special sales or receivables account, you can set up an extra posting group for this purpose.</span></span>  
>   
>  <span data-ttu-id="44b9b-117">U moet altijd een nummer opgeven voor een centralisatierekening in de boekingsgroep, ook al bedraagt het saldo op deze rekening altijd 0 nadat u een factuur hebt geboekt.</span><span class="sxs-lookup"><span data-stu-id="44b9b-117">You must enter a number for a receivables account for the posting group, even though the balance in this account will always be 0 after you post an invoice.</span></span>  

## <a name="see-also"></a><span data-ttu-id="44b9b-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="44b9b-118">See Also</span></span>
[<span data-ttu-id="44b9b-119">Tegoeden beheren</span><span class="sxs-lookup"><span data-stu-id="44b9b-119">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="44b9b-120">[Nieuwe klanten registreren](sales-how-register-new-customers.md)  </span><span class="sxs-lookup"><span data-stu-id="44b9b-120">[Register New Customers](sales-how-register-new-customers.md)  </span></span>  
[<span data-ttu-id="44b9b-121">Financiën</span><span class="sxs-lookup"><span data-stu-id="44b9b-121">Finance</span></span>](finance.md)  


