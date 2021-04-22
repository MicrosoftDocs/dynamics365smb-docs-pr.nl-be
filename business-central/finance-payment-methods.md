---
title: Betalingsmethoden instellen
description: U gebruikt betalingswijzen, bijvoorbeeld cheque, bankoverschrijving, contant geld of PayPal, om te bepalen hoe verkoop- en inkoopfacturen worden betaald.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 1e836b43392cd915a77c5ee85d5a322753dcd5df
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773967"
---
# <a name="set-up-payment-methods"></a><span data-ttu-id="65453-103">Betalingsmethoden instellen</span><span class="sxs-lookup"><span data-stu-id="65453-103">Set Up Payment Methods</span></span>

<span data-ttu-id="65453-104">Betalingswijzen definiëren hoe u wilt dat klanten u betalen en hoe u uw leveranciers wilt betalen.</span><span class="sxs-lookup"><span data-stu-id="65453-104">Payment methods define the way you prefer for customers to pay you, and how you like to pay your vendors.</span></span> <span data-ttu-id="65453-105">De methode kan voor elke klant of leverancier variëren.</span><span class="sxs-lookup"><span data-stu-id="65453-105">The method can vary for each customer or vendor.</span></span> <span data-ttu-id="65453-106">Voorbeelden van gangbare betalingswijzen zijn **bank**, **contant**, **cheque** of **rekening**.</span><span class="sxs-lookup"><span data-stu-id="65453-106">Examples of typical payment methods are **bank**, **cash**, **check**, or **account**.</span></span>

<span data-ttu-id="65453-107">U kunt een betalingswijze aan klanten en leveranciers toewijzen zodat altijd dezelfde wijze wordt gebruikt op de verkoop- en inkoopdocumenten die u voor hen maakt.</span><span class="sxs-lookup"><span data-stu-id="65453-107">You can assign a payment method to customers and vendors so that the same method is always used on the sales and purchase documents you create for them.</span></span> <span data-ttu-id="65453-108">Indien nodig kunt u de methode in het verkoop- of inkoopdocument wijzigen.</span><span class="sxs-lookup"><span data-stu-id="65453-108">If needed, you can change the method on the sales or purchase document.</span></span> <span data-ttu-id="65453-109">Bijvoorbeeld wanneer u een bepaalde inkoopfactuur in contant geld in plaats van met cheque wilt betalen.</span><span class="sxs-lookup"><span data-stu-id="65453-109">For example, if you want to pay a particular purchase invoice in cash rather than by check.</span></span> <span data-ttu-id="65453-110">Dit verandert niet de standaardbetalingswijze die aan de leverancier is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="65453-110">This does not change the default payment method assigned to the vendor.</span></span>

<span data-ttu-id="65453-111">Voor verkoop- en inkoopdocumenten worden dezelfde betalingswijzen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="65453-111">The same payment methods are used for sales and purchase documents.</span></span> <span data-ttu-id="65453-112">Bijvoorbeeld een _cash_ betalingswijze wordt gebruikt als u betalingen doet en wanneer u ze ontvangt.</span><span class="sxs-lookup"><span data-stu-id="65453-112">For example, a _cash_ payment method is used both when you make payments and when you receive them.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="65453-113">weet dat wanneer u een verkoopfactuur maakt, u verwacht betaling te ontvangen en voor inkoopfacturen het tegenovergestelde.</span><span class="sxs-lookup"><span data-stu-id="65453-113">knows that when you are creating a sales invoice you expect to receive payment, and the opposite for purchase invoices.</span></span>

<span data-ttu-id="65453-114">Creditnota's voor retouren zijn echter uitzonderingen, omdat geld in tegenovergestelde richtingen stroomt, van u naar uw klant en van uw leverancier naar u.</span><span class="sxs-lookup"><span data-stu-id="65453-114">Credit memos for returns, however, are exceptions because money is flowing in the opposite directions, from you to your customer and from your vendor to you.</span></span> <span data-ttu-id="65453-115">Daarom wordt geen standaardbetalingswijze toegewezen aan creditnota's.</span><span class="sxs-lookup"><span data-stu-id="65453-115">Therefore, a default payment method is not assigned to credit memos.</span></span> <span data-ttu-id="65453-116">Er is echter een oplossing als u betalingsvoorwaarden voor de klant of leverancier hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="65453-116">There is, however, a workaround if you have specified terms of payment for the customer or vendor.</span></span> <span data-ttu-id="65453-117">Hoewel het veld **Cont.-kort. op creditnota's berekenen** hier niet bedoeld voor is, wordt als u het selectievakje op de pagina **Betalingscondities** inschakelt, een standaardbetalingswijze toegevoegd wanneer u een creditnota maakt.</span><span class="sxs-lookup"><span data-stu-id="65453-117">Though the **Calc. Pmt. Disc. on Cr. Memos** field is not intended for this, if you choose the check box on the **Payment Terms** page a default payment method will be added when you create a credit memo.</span></span> <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys?rel=0]

## <a name="to-set-up-a-payment-method"></a><span data-ttu-id="65453-118">Een betalingswijze instellen</span><span class="sxs-lookup"><span data-stu-id="65453-118">To set up a payment method</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="65453-119">biedt een paar betalingswijzen die bedrijven vaak gebruiken.</span><span class="sxs-lookup"><span data-stu-id="65453-119">provides a few payment methods that businesses often use.</span></span> <span data-ttu-id="65453-120">U kunt er echter zo veel toevoegen als u wilt.</span><span class="sxs-lookup"><span data-stu-id="65453-120">You can, however, add as many as you need.</span></span>

1. <span data-ttu-id="65453-121">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsmethoden** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="65453-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="65453-122">Vul de vereiste velden in.</span><span class="sxs-lookup"><span data-stu-id="65453-122">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="65453-123">Wijs desgewenst betalingsvoorwaarden toe aan uw betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="65453-123">Optionally, add payment terms to your payment method.</span></span> <span data-ttu-id="65453-124">Zie voor meer informatie [Betalingsvoorwaarden instellen](finance-payment-terms.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="65453-124">For more information, see [Set Up Payment Terms](finance-payment-terms.md).</span></span>  

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a><span data-ttu-id="65453-125">Een betalingswijze aan een klant of leverancier toewijzen</span><span class="sxs-lookup"><span data-stu-id="65453-125">To assign a payment method to a customer or vendor</span></span>

1. <span data-ttu-id="65453-126">Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klant** of **Leverancier** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="65453-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer** or **Vendor**, and then choose the related link.</span></span>
2. <span data-ttu-id="65453-127">Kies in het veld **Betalingswijze** de methode die standaard moet worden gebruikt voor de klant of leverancier.</span><span class="sxs-lookup"><span data-stu-id="65453-127">In the **Payment Method Code** field, choose the method to use by default for the customer or vendor.</span></span>

## <a name="see-also"></a><span data-ttu-id="65453-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="65453-128">See Also</span></span>

[<span data-ttu-id="65453-129">Nieuwe klanten registreren</span><span class="sxs-lookup"><span data-stu-id="65453-129">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="65453-130">Betalingsvoorwaarden instellen</span><span class="sxs-lookup"><span data-stu-id="65453-130">Set Up Payment Terms</span></span>](finance-payment-terms.md)  
[<span data-ttu-id="65453-131">Financiën</span><span class="sxs-lookup"><span data-stu-id="65453-131">Finance</span></span>](finance.md)  
<span data-ttu-id="65453-132">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="65453-132">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]