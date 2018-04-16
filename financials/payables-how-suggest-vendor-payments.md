---
title: De batchverwerking Betalingsvoorstellen maken gebruiken| Microsoft Docs
description: U kunt leveranciersbetalingsinstellingen opgeven om voorstellen of voorstellen voor betalingen te krijgen die binnenkort moeten worden betaald of waar een korting beschikbaar is.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: acef03f32124c5983846bc6ed0c4d332c9c8b347
ms.openlocfilehash: af35aa77bfe288fb810dd2b9b06be6026e012da7
ms.contentlocale: nl-be
ms.lasthandoff: 04/16/2018

---
# <a name="suggest-vendor-payments"></a><span data-ttu-id="ef34f-103">Leveranciersbetalingen voorstellen</span><span class="sxs-lookup"><span data-stu-id="ef34f-103">Suggest Vendor Payments</span></span>
<span data-ttu-id="ef34f-104">In het venster **Betalingsdagboek** kunt u door middel van de batchverwerking **Leveranciersbetalingen voorstellen** betalingsregels laten voorstellen.</span><span class="sxs-lookup"><span data-stu-id="ef34f-104">In the **Payment Journal** window, you can use the **Suggest Vendor Payments** batch job to suggest payment lines.</span></span> <span data-ttu-id="ef34f-105">Regels voor zaken als betalingen die binnenkort moeten worden betaald, of betalingen waarbij een contantkorting beschikbaar is, worden weergegeven op basis van de instellingen.</span><span class="sxs-lookup"><span data-stu-id="ef34f-105">Lines for things like payments that are due soon, or payments where a payment discount is available, are suggested based on your settings.</span></span>

<span data-ttu-id="ef34f-106">Om optimaal van voorgestelde regels te profiteren, moet u uw leveranciers eerst naar prioriteit indelen.</span><span class="sxs-lookup"><span data-stu-id="ef34f-106">To benefit fully from suggested lines, you must first prioritize your vendors.</span></span> <span data-ttu-id="ef34f-107">Zie voor meer informatie [Leveranciers in een prioriteitsvolgorde plaatsen](purchasing-how-prioritize-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="ef34f-107">For more information, see [Prioritize Vendors](purchasing-how-prioritize-vendors.md).</span></span>  

<span data-ttu-id="ef34f-108">De leveranciersposten die **Afwachten** zijn, worden niet opgenomen.</span><span class="sxs-lookup"><span data-stu-id="ef34f-108">Vendor entries that are not **On Hold** are not included.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="ef34f-109">Als u wilt profiteren van contantkortingen en een beschikbaar bedrag hebt ingevoerd, wordt dit bedrag gebruikt voor de volgende posten:</span><span class="sxs-lookup"><span data-stu-id="ef34f-109">If you want to take advantage of payment discounts, and have entered an available amount, the amount will be used for:</span></span>  

* <span data-ttu-id="ef34f-110">Prioritaire openstaande leveranciersposten eerst, in volgorde van prioriteit.</span><span class="sxs-lookup"><span data-stu-id="ef34f-110">Prioritized overdue vendor entries first in order of priority.</span></span>  
* <span data-ttu-id="ef34f-111">Achterstallige posten zonder prioriteitsnummer.</span><span class="sxs-lookup"><span data-stu-id="ef34f-111">Overdue vendor entries that are not prioritized.</span></span>  
* <span data-ttu-id="ef34f-112">Openstaande leveranciersposten die voor contantkortingen in aanmerking komen, geordend op leveranciersnummer.</span><span class="sxs-lookup"><span data-stu-id="ef34f-112">Open vendor entries that qualify for payment discounts, arranged by vendor number.</span></span>  

## <a name="to-use-the-suggest-vendor-payments-function"></a><span data-ttu-id="ef34f-113">De functie Leveranciersbetalingen voorstellen gebruiken</span><span class="sxs-lookup"><span data-stu-id="ef34f-113">To use the Suggest Vendor Payments function</span></span>
1. <span data-ttu-id="ef34f-114">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsdagboeken** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ef34f-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ef34f-115">Open het desbetreffende dagboek en kies vervolgens de actie **Leveranciersbetalingen voorstellen**.</span><span class="sxs-lookup"><span data-stu-id="ef34f-115">Open the relevant journal, and then choose the **Suggest Vendor Payments** action.</span></span>  
3. <span data-ttu-id="ef34f-116">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="ef34f-116">Fill in the fields as necessary.</span></span> [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="ef34f-117">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="ef34f-117">Choose the **OK** button.</span></span>  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a><span data-ttu-id="ef34f-118">De vervaldatum als boekingsdatum invoegen op betalingsdagboekregels</span><span class="sxs-lookup"><span data-stu-id="ef34f-118">To insert the due date as posting date on payment journal lines</span></span>
<span data-ttu-id="ef34f-119">Wanneer u de batchverwerking **Leveranciersbetalingen voorstellen** gebruikt om betalingsregels voor uw leveranciers te maken, kunt u twee speciale velden invullen om te zorgen dat de gegenereerde regels de vervaldatum gebruiken om de boekingsdatum te berekenen.</span><span class="sxs-lookup"><span data-stu-id="ef34f-119">When you use the **Suggest Vendor Payments** batch job to create payment lines for your vendors, you can fill two special fields to make sure that the generated lines use the due date to calculate the posting date.</span></span> <span data-ttu-id="ef34f-120">Deze velden zijn **Bereken boekingsdatum via vervaldatum vereffeningsdoc.** en **Vervaldatumafwijking vereffeningsdoc.**.</span><span class="sxs-lookup"><span data-stu-id="ef34f-120">These fields are **Calculate Posting Date from Applies-to-Doc Due Date** and **Applies-to-Doc Due Date Offset**.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="ef34f-121">U kunt het veld **Bereken boekingsdatum via vervaldatum vereffeningsdoc.** niet samen gebruiken met het veld **Contantkorting nemen** of het veld **Een regel per leverancier**.</span><span class="sxs-lookup"><span data-stu-id="ef34f-121">You cannot use the **Calculate Posting Date from Applies-to-Doc Due Date** field together with the **Find Payment Discounts** field or the **Summarize per Vendor** field.</span></span> <span data-ttu-id="ef34f-122">Als de boekingsdatum is gebaseerd op de vervaldatum, worden enkele contantkortingen mogelijk niet correct berekend, omdat de boekingsdatum na de vervaldatum voor contantkorting ligt.</span><span class="sxs-lookup"><span data-stu-id="ef34f-122">If the posting date is based on the due date, some payment discounts may not calculate correctly because the posting date is after the payment discount date.</span></span>  

<span data-ttu-id="ef34f-123">En als de berekende boekingsdatum in het verleden ligt, wordt de boekingsdatum voorwaarts verplaatst naar de volgende werkdatum en wordt een waarschuwing weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ef34f-123">Also, if the calculated posting date is in the past, then the posting date is moved up to the work date, and a warning is displayed.</span></span>  

<span data-ttu-id="ef34f-124">U kunt eventueel handmatig betalingsregels maken, waarbij de vervaldatum wordt gebruikt om de boekingsdatum te berekenen.</span><span class="sxs-lookup"><span data-stu-id="ef34f-124">Alternatively, you can manually create payment lines using the due date to calculate the posting date.</span></span> <span data-ttu-id="ef34f-125">Nadat u posten hebt vereffend, kunt u met de actie **Boekingssdatum berekenen** de boekingsdatum op de dagboekregel bijwerken met de vervaldatum van de gerelateerde inkoopfactuur.</span><span class="sxs-lookup"><span data-stu-id="ef34f-125">After you apply vendor ledger entries, you can use the **Calculate Posting Date** action to update the posting date on the journal line with the due date of the related purchase invoice.</span></span> <span data-ttu-id="ef34f-126">Zie voor meer informatie [Inkooptransacties handmatig vereffenen](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="ef34f-126">For more information, see [Apply Purchase Transactions Manually](payables-how-apply-purchase-transactions-manually.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="ef34f-127">Als de inkoopfactuur achterstallig is, wordt de boekingsdatum ingesteld op de werkdatum en wordt het lettertype op de regel rood.</span><span class="sxs-lookup"><span data-stu-id="ef34f-127">If the purchase invoice is overdue, the posting date is set to the work date, and the font on the line becomes red.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ef34f-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ef34f-128">See Also</span></span>
[<span data-ttu-id="ef34f-129">Betalingsverplichtingen beheren</span><span class="sxs-lookup"><span data-stu-id="ef34f-129">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="ef34f-130">Betalingen uitvoeren</span><span class="sxs-lookup"><span data-stu-id="ef34f-130">Making Payments</span></span>](payables-make-payments.md)  
[<span data-ttu-id="ef34f-131">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="ef34f-131">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="ef34f-132">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ef34f-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

