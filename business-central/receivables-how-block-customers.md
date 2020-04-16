---
title: Verkopen aan klanten blokkeren en artikelen blokkeren voor verkoop of inkoop
description: In Business Central kan een artikel worden gemarkeerd als geblokkeerd voor verkoop, geblokkeerd voor inkoop of geblokkeerd voor alle doeleinden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 832963169f4c81d65b105ca71722435554d8e262
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3193767"
---
# <a name="block-customers"></a><span data-ttu-id="728bc-103">Klanten blokkeren</span><span class="sxs-lookup"><span data-stu-id="728bc-103">Block Customers</span></span>
<span data-ttu-id="728bc-104">U kunt een klant blokkeren, bijvoorbeeld vanwege insolventie, zodat de klant niet aan verkoopdocumenten kan worden toegevoegd of zodat geen transacties voor de klant kunnen worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="728bc-104">You can block a customer, for example because of insolvency, so that the customer cannot be added to sales documents or so that no transactions can be posted for the customer.</span></span>

<span data-ttu-id="728bc-105">Naast het blokkeren van een klant kunt u een klanttransactie voor de klant op afwachten instellen in verband met aanmaningen.</span><span class="sxs-lookup"><span data-stu-id="728bc-105">In addition to blocking a customer, you can set receivable transactions for the customer to be on hold in connection with reminders.</span></span> <span data-ttu-id="728bc-106">Zie voor meer informatie [Openstaande saldi innen](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="728bc-106">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>   

<span data-ttu-id="728bc-107">De volgende tabel beschrijft de verschillende blokkeeropties.</span><span class="sxs-lookup"><span data-stu-id="728bc-107">The following table describes the different blocking options.</span></span>  

|<span data-ttu-id="728bc-108">Optie</span><span class="sxs-lookup"><span data-stu-id="728bc-108">Option</span></span>|<span data-ttu-id="728bc-109">Description</span><span class="sxs-lookup"><span data-stu-id="728bc-109">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="728bc-110">**Leeg**</span><span class="sxs-lookup"><span data-stu-id="728bc-110">**Blank**</span></span>|<span data-ttu-id="728bc-111">Transacties zijn toegestaan voor deze klant.</span><span class="sxs-lookup"><span data-stu-id="728bc-111">Transactions are allowed for this customer.</span></span>|
|<span data-ttu-id="728bc-112">**Verzending**</span><span class="sxs-lookup"><span data-stu-id="728bc-112">**Ship**</span></span>|<span data-ttu-id="728bc-113">Voor deze klant kunnen geen nieuwe orders en nieuwe verzendingen worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="728bc-113">New orders and new shipments cannot be created for this customer.</span></span> <span data-ttu-id="728bc-114">Bestaande verzendingen die nog niet zijn gefactureerd, kunnen worden gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="728bc-114">Existing shipments not yet invoiced can be invoiced.</span></span>|  
|<span data-ttu-id="728bc-115">**Factureren**</span><span class="sxs-lookup"><span data-stu-id="728bc-115">**Invoice**</span></span>|<span data-ttu-id="728bc-116">Voor deze klant kunnen geen nieuwe orders, nieuwe verzendingen en nieuwe facturen worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="728bc-116">New orders, new shipments, and new invoices cannot be created for this customer.</span></span> <span data-ttu-id="728bc-117">Bestaande verzendingen die nog niet zijn gefactureerd, kunnen niet worden gefactureerd.</span><span class="sxs-lookup"><span data-stu-id="728bc-117">Existing shipments not yet invoiced cannot be invoiced.</span></span>|  
|<span data-ttu-id="728bc-118">**Alle**</span><span class="sxs-lookup"><span data-stu-id="728bc-118">**All**</span></span>|<span data-ttu-id="728bc-119">Voor deze klant is geen enkele transactie, inclusief betalingen, toegestaan.</span><span class="sxs-lookup"><span data-stu-id="728bc-119">No transaction is allowed for this customer, including payments.</span></span>|  

## <a name="to-block-a-customer"></a><span data-ttu-id="728bc-120">Een klant blokkeren</span><span class="sxs-lookup"><span data-stu-id="728bc-120">To block a customer</span></span>  
1. <span data-ttu-id="728bc-121">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="728bc-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="728bc-122">Selecteer een klant en kies vervolgens de actie **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="728bc-122">Select a customer, and then choose the **Edit** action.</span></span>
3. <span data-ttu-id="728bc-123">Vul het veld **Geblokkeerd** in met een van de hierboven beschreven opties.</span><span class="sxs-lookup"><span data-stu-id="728bc-123">Fill in the **Blocked** field with one of the options described above.</span></span>

## <a name="see-also"></a><span data-ttu-id="728bc-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="728bc-124">See Also</span></span>  
[<span data-ttu-id="728bc-125">Nieuwe klanten registreren</span><span class="sxs-lookup"><span data-stu-id="728bc-125">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="728bc-126">Openstaande saldi innen</span><span class="sxs-lookup"><span data-stu-id="728bc-126">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="728bc-127">Tegoeden beheren</span><span class="sxs-lookup"><span data-stu-id="728bc-127">Managing Receivables</span></span>](receivables-manage-receivables.md)  
