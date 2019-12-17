---
title: Betalingsmethoden instellen| Microsoft Docs
description: U gebruikt betalingswijzen, bijvoorbeeld cheque, bankoverschrijving, contant geld of PayPal, om te bepalen hoe verkoop- en inkoopfacturen worden betaald.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, bank transfer, cash, PayPal
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 753b9f30648059a68c22b524008e21c6c866d19c
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2882554"
---
# <a name="defining-payment-methods"></a><span data-ttu-id="7d23c-103">Betalingsmethoden definiëren</span><span class="sxs-lookup"><span data-stu-id="7d23c-103">Defining Payment Methods</span></span>
<span data-ttu-id="7d23c-104">Betalingswijzen definiëren hoe u wilt dat klanten u betalen en hoe u uw leveranciers wilt betalen.</span><span class="sxs-lookup"><span data-stu-id="7d23c-104">Payment methods define the way you prefer for customers to pay you, and how you like to pay your vendors.</span></span> <span data-ttu-id="7d23c-105">De methode kan voor elke klant of leverancier variëren.</span><span class="sxs-lookup"><span data-stu-id="7d23c-105">The method can vary for each customer or vendor.</span></span> <span data-ttu-id="7d23c-106">Voorbeelden van gangbare betalingswijzen zijn **bank**, **contant**, **cheque** of **rekening**.</span><span class="sxs-lookup"><span data-stu-id="7d23c-106">Examples of typical payment methods are **bank**, **cash**, **check**, or **account**.</span></span>

<span data-ttu-id="7d23c-107">U kunt een betalingswijze aan klanten en leveranciers toewijzen zodat altijd dezelfde wijze wordt gebruikt op de verkoop- en inkoopdocumenten die u voor hen maakt.</span><span class="sxs-lookup"><span data-stu-id="7d23c-107">You can assign a payment method to customers and vendors so that the same method is always used on the sales and purchase documents you create for them.</span></span> <span data-ttu-id="7d23c-108">Indien nodig kunt u de methode in het verkoop- of inkoopdocument wijzigen.</span><span class="sxs-lookup"><span data-stu-id="7d23c-108">If needed, you can change the method on the sales or purchase document.</span></span> <span data-ttu-id="7d23c-109">Bijvoorbeeld wanneer u een bepaalde inkoopfactuur in contant geld in plaats van met cheque wilt betalen.</span><span class="sxs-lookup"><span data-stu-id="7d23c-109">For example, if you want to pay a particular purchase invoice in cash rather than by check.</span></span> <span data-ttu-id="7d23c-110">Dit verandert niet de standaardbetalingswijze die aan de leverancier is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="7d23c-110">This does not change the default payment method assigned to the vendor.</span></span>

<span data-ttu-id="7d23c-111">Voor verkoop- en inkoopdocumenten worden dezelfde betalingswijzen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7d23c-111">The same payment methods are used for sales and purchase documents.</span></span> <span data-ttu-id="7d23c-112">Bijvoorbeeld een _cash_ betalingswijze wordt gebruikt als u betalingen doet en wanneer u ze ontvangt.</span><span class="sxs-lookup"><span data-stu-id="7d23c-112">For example, a _cash_ payment method is used both when you make payments and when you receive them.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="7d23c-113">weet dat wanneer u een verkoopfactuur maakt, u verwacht betaling te ontvangen en voor inkoopfacturen het tegenovergestelde.</span><span class="sxs-lookup"><span data-stu-id="7d23c-113">knows that when you are creating a sales invoice you expect to receive payment, and the opposite for purchase invoices.</span></span>

<span data-ttu-id="7d23c-114">Creditnota's voor retouren zijn echter uitzonderingen, omdat geld in tegenovergestelde richtingen stroomt, van u naar uw klant en van uw leverancier naar u.</span><span class="sxs-lookup"><span data-stu-id="7d23c-114">Credit memos for returns, however, are exceptions because money is flowing in the opposite directions, from you to your customer and from your vendor to you.</span></span> <span data-ttu-id="7d23c-115">Daarom wordt geen standaardbetalingswijze toegewezen aan creditnota's.</span><span class="sxs-lookup"><span data-stu-id="7d23c-115">Therefore, a default payment method is not assigned to credit memos.</span></span> <span data-ttu-id="7d23c-116">Er is echter een oplossing als u betalingsvoorwaarden voor de klant of leverancier hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="7d23c-116">There is, however, a workaround if you have specified terms of payment for the customer or vendor.</span></span> <span data-ttu-id="7d23c-117">Hoewel het veld **Cont.-kort. op creditnota's berekenen** hier niet bedoeld voor is, wordt als u het selectievakje op de pagina **Betalingscondities** inschakelt, een standaardbetalingswijze toegevoegd wanneer u een creditnota maakt.</span><span class="sxs-lookup"><span data-stu-id="7d23c-117">Though the **Calc. Pmt. Disc. on Cr. Memos** field is not intended for this, if you choose the check box on the **Payment Terms** page a default payment method will be added when you create a credit memo.</span></span> <br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE476Ys]

## <a name="to-set-up-a-payment-method"></a><span data-ttu-id="7d23c-118">Een betalingswijze instellen</span><span class="sxs-lookup"><span data-stu-id="7d23c-118">To set up a payment method</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="7d23c-119">biedt een paar betalingswijzen die bedrijven vaak gebruiken.</span><span class="sxs-lookup"><span data-stu-id="7d23c-119">provides a few payment methods that businesses often use.</span></span> <span data-ttu-id="7d23c-120">U kunt er echter zo veel toevoegen als u wilt.</span><span class="sxs-lookup"><span data-stu-id="7d23c-120">You can, however, add as many as you need.</span></span>

1. <span data-ttu-id="7d23c-121">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsmethoden** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="7d23c-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Methods**, and then choose the related link.</span></span>
2. <span data-ttu-id="7d23c-122">Vul de benodigde velden in.</span><span class="sxs-lookup"><span data-stu-id="7d23c-122">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-payment-method-to-a-customer-or-vendor"></a><span data-ttu-id="7d23c-123">Een betalingswijze aan een klant of leverancier toewijzen</span><span class="sxs-lookup"><span data-stu-id="7d23c-123">To assign a payment method to a customer or vendor</span></span>
1. <span data-ttu-id="7d23c-124">Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klant** of **Leverancier** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="7d23c-124">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer** or **Vendor**, and then choose the related link.</span></span>
2. <span data-ttu-id="7d23c-125">Kies in het veld **Betalingswijze** de methode die standaard moet worden gebruikt voor de klant of leverancier.</span><span class="sxs-lookup"><span data-stu-id="7d23c-125">In the **Payment Method Code** field, choose the method to use by default for the customer or vendor.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d23c-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7d23c-126">See Also</span></span>
[<span data-ttu-id="7d23c-127">Nieuwe klanten registreren</span><span class="sxs-lookup"><span data-stu-id="7d23c-127">Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="7d23c-128">Financiën</span><span class="sxs-lookup"><span data-stu-id="7d23c-128">Finance</span></span>](finance.md)  
<span data-ttu-id="7d23c-129">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7d23c-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
