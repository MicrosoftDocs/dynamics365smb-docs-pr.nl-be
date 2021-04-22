---
title: Verkoop aan klanten blokkeren
description: Indien nodig kunt u voorkomen dat een klant wordt opgenomen in verkoopdocumenten en andere verkooptransacties.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1caf2fb0586cf704e5fc1354b3b4a0be096dc709
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781750"
---
# <a name="block-customers"></a><span data-ttu-id="7a836-103">Klanten blokkeren</span><span class="sxs-lookup"><span data-stu-id="7a836-103">Block Customers</span></span>
<span data-ttu-id="7a836-104">U kunt een klant blokkeren, bijvoorbeeld vanwege insolventie, zodat de klant niet aan verkoopdocumenten kan worden toegevoegd of zodat geen transacties voor de klant kunnen worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="7a836-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="7a836-105">Naast het blokkeren van een klant kunt u een klanttransactie voor de klant op afwachten instellen in verband met aanmaningen.</span><span class="sxs-lookup"><span data-stu-id="7a836-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="7a836-106">Zie voor meer informatie [Openstaande saldi innen](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="7a836-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="7a836-107">De volgende tabel beschrijft de opties voor het blokkeren van klanten.</span><span class="sxs-lookup"><span data-stu-id="7a836-107">The following table describes the options for blocking customers.</span></span>  

|<span data-ttu-id="7a836-108">Optie</span><span class="sxs-lookup"><span data-stu-id="7a836-108">Option</span></span>|<span data-ttu-id="7a836-109">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="7a836-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="7a836-110">**Leeg**</span><span class="sxs-lookup"><span data-stu-id="7a836-110">**Blank**</span></span>|<span data-ttu-id="7a836-111">Transacties zijn toegestaan voor deze klant.</span><span class="sxs-lookup"><span data-stu-id="7a836-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="7a836-112">**Verzending**</span><span class="sxs-lookup"><span data-stu-id="7a836-112">**Ship**</span></span>|<span data-ttu-id="7a836-113">Voor deze klant kunnen geen nieuwe orders en nieuwe verzendingen worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7a836-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="7a836-114">Bestaande verzendingen die nog niet zijn gefactureerd, kunnen worden gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="7a836-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="7a836-115">**Factureren**</span><span class="sxs-lookup"><span data-stu-id="7a836-115">**Invoice**</span></span>|<span data-ttu-id="7a836-116">Voor deze klant kunnen geen nieuwe orders, nieuwe verzendingen en nieuwe facturen worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7a836-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="7a836-117">Bestaande verzendingen die nog niet zijn gefactureerd, kunnen niet worden gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="7a836-117">Existing shipments not yet invoiced cannot be invoiced.</span></span> <span data-ttu-id="7a836-118">U kunt nog steeds herinneringen en rentefacturen naar de klant sturen.</span><span class="sxs-lookup"><span data-stu-id="7a836-118">You can still send reminders and finance charge memos to the customer.</span></span>|  
|<span data-ttu-id="7a836-119">**Alle**</span><span class="sxs-lookup"><span data-stu-id="7a836-119">**All**</span></span>|<span data-ttu-id="7a836-120">Voor deze klant is geen enkele transactie, inclusief betalingen, toegestaan.</span><span class="sxs-lookup"><span data-stu-id="7a836-120">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="7a836-121">Een klant blokkeren</span><span class="sxs-lookup"><span data-stu-id="7a836-121">To block a customer</span></span>  
1. <span data-ttu-id="7a836-122">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="7a836-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="7a836-123">Selecteer een klant en kies vervolgens de actie **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="7a836-123">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="7a836-124">Kies in het veld **Geblokkeerd** wat u wilt blokkeren, zoals beschreven in de bovenstaande tabel.</span><span class="sxs-lookup"><span data-stu-id="7a836-124">In the **Blocked** field, choose what to block, as described in the table above.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a836-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7a836-125">See Also</span></span>  
[<span data-ttu-id="7a836-126">Nieuwe klanten registreren</span><span class="sxs-lookup"><span data-stu-id="7a836-126">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="7a836-127">Openstaande saldi innen</span><span class="sxs-lookup"><span data-stu-id="7a836-127">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="7a836-128">Tegoeden beheren</span><span class="sxs-lookup"><span data-stu-id="7a836-128">Managing Receivables</span></span>](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]