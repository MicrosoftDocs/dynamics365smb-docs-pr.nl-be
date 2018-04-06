---
title: Positive Pay-bestanden exporteren| Microsoft Docs
description: U kunt zorgen dat uw bank alleen gevalideerde cheques en bedragen verrekent door een Positive Pay-bestand te exporteren dat gegevens over leveranciers en betalingen bevat.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: check, clearing
ms.date: 06/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: db5811c3ba22df76e2c0cab4b190777d0705f72a
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="export-a-positive-pay-file"></a><span data-ttu-id="e29d0-103">Een Positive Pay-bestand exporteren</span><span class="sxs-lookup"><span data-stu-id="e29d0-103">Export a Positive Pay file</span></span>
<span data-ttu-id="e29d0-104">Om ervoor te zorgen dat uw bank alleen gevalideerde cheques en bedragen verrekent, kunt u een Positive Pay-bestand exporteren dat leveranciersgegevens, het chequenummer en het betalingsbedrag bevat, die u naar de bank verzendt wanneer u betalingen verwerkt.</span><span class="sxs-lookup"><span data-stu-id="e29d0-104">To make sure that your bank only clears validated checks and amounts, you can export a Positive Pay file that contains vendor information, check number, and payment amount, which you send to the bank for reference when you process payments.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="e29d0-105"> is vooraf geconfigureerd om Positive Pay-bestanden te ondersteunen voor Bank of America en City Bank.</span><span class="sxs-lookup"><span data-stu-id="e29d0-105"> is preconfigured to support Positive Pay files for Bank of America and City Bank.</span></span>

## <a name="to-set-up-a-bank-account-for-positive-pay"></a><span data-ttu-id="e29d0-106">Een bankrekening voor Positive Pay instellen</span><span class="sxs-lookup"><span data-stu-id="e29d0-106">To set up a bank account for Positive Pay</span></span>
1. <span data-ttu-id="e29d0-107">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="e29d0-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="e29d0-108">Open de kaart voor de bank waarvoor u Positive Pay wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e29d0-108">Open the card for the bank that you want to use Positive Pay for.</span></span>
3. <span data-ttu-id="e29d0-109">Voer in het veld **Positive Pay-exportcode** POSPAYBANK in.</span><span class="sxs-lookup"><span data-stu-id="e29d0-109">In the **Positive Pay Export Code** field, enter POSPAYBANK.</span></span>
4. <span data-ttu-id="e29d0-110">Sluit het venster.</span><span class="sxs-lookup"><span data-stu-id="e29d0-110">Close the window.</span></span>

## <a name="to-export-a-positive-pay-file"></a><span data-ttu-id="e29d0-111">Een Positive Pay-bestand exporteren</span><span class="sxs-lookup"><span data-stu-id="e29d0-111">To export a Positive Pay file</span></span>
1. <span data-ttu-id="e29d0-112">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="e29d0-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="e29d0-113">Selecteer de bankrekening waarvoor u een Positive Pay-bestand wilt exporteren.</span><span class="sxs-lookup"><span data-stu-id="e29d0-113">Select the bank account that you want to export a Positive Pay file for.</span></span>
3. <span data-ttu-id="e29d0-114">Kies de actie **Positive Pay exporteren**.</span><span class="sxs-lookup"><span data-stu-id="e29d0-114">Choose **Positive Pay Export** action.</span></span>

    <span data-ttu-id="e29d0-115">Het venster **Positive Pay exporteren** wordt geopend met betalingen die voor de bankrekening zijn uitgevoerd sinds de laatste uploaddatum, zoals weergegeven in het veld **Laatste uploaddatum** en het veld **Laatste uploadtijd**.</span><span class="sxs-lookup"><span data-stu-id="e29d0-115">The **Positive Pay Export** window opens displaying payments that have been made for the bank account since the last upload date, as shown in the **Last Upload Date** and **Last Upload Time** fields.</span></span>
4. <span data-ttu-id="e29d0-116">In het veld **Afkapdatum voor uploaden** geeft u een datum op waarvóór betalingen niet worden opgenomen in het geëxporteerde bestand.</span><span class="sxs-lookup"><span data-stu-id="e29d0-116">In the **Cutoff Upload Date** field, specify a date before which payments are not included in the exported file.</span></span>
5. <span data-ttu-id="e29d0-117">Kies de actie **Exporteren**.</span><span class="sxs-lookup"><span data-stu-id="e29d0-117">Choose the **Export** action.</span></span>
6. <span data-ttu-id="e29d0-118">Kies in het venster **Bestand exporteren** de knop **Opslaan** en sla vervolgens het bestand op een geschikte locatie op.</span><span class="sxs-lookup"><span data-stu-id="e29d0-118">In the **Export File** window, choose the **Save** button, and then save the file to a convenient location.</span></span>
7. <span data-ttu-id="e29d0-119">Upload het bestand naar uw elektronische banksite.</span><span class="sxs-lookup"><span data-stu-id="e29d0-119">Upload the file to your electronic bank site.</span></span>
8. <span data-ttu-id="e29d0-120">Noteer of kopieer het bevestigingsnummer dat wordt weergegeven wanneer de bestandsupload is gelukt.</span><span class="sxs-lookup"><span data-stu-id="e29d0-120">Write down or copy the confirmation number that is displayed when the file upload is successful.</span></span>

<span data-ttu-id="e29d0-121">Geëxporteerde Positive Pay-records weergeven</span><span class="sxs-lookup"><span data-stu-id="e29d0-121">To view exported Positive Pay records</span></span>

1. <span data-ttu-id="e29d0-122">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="e29d0-122">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="e29d0-123">Selecteer de bankrekening waarvoor u Positive Pay-exportrecords wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="e29d0-123">Select the bank account that you want to view Positive Pay export records for.</span></span>
3. <span data-ttu-id="e29d0-124">Kies de actie **Positive Pay-posten**.</span><span class="sxs-lookup"><span data-stu-id="e29d0-124">Choose the **Positive Pay Entries** action.</span></span>

    <span data-ttu-id="e29d0-125">In het venster **Positive Pay-posten** kunt u alle Positive Pay-exportrecords voor de bankrekening zien.</span><span class="sxs-lookup"><span data-stu-id="e29d0-125">In the **Positive Pay Entries** window, you can see all the Positive Pay export records for the bank account.</span></span>
4. <span data-ttu-id="e29d0-126">Voer in het veld **Bevestigingsnummer** voor elke exportrecord het bevestigingsnummer in dat u ontvangt als de bestandsupload naar de bank is gelukt.</span><span class="sxs-lookup"><span data-stu-id="e29d0-126">In the **Confirmation Number** field, enter, for each export record, the confirmation number that you receive when the file upload to the bank is successful.</span></span>
5. <span data-ttu-id="e29d0-127">Als u de relateerde betalingsregels wilt weergeven, kiest u de actie **Details van Positive Pay-post**.</span><span class="sxs-lookup"><span data-stu-id="e29d0-127">To view the related payment lines, choose the **Positive Pay Entry Details** action.</span></span>

<span data-ttu-id="e29d0-128">Positive Pay-bestanden opnieuw exporteren</span><span class="sxs-lookup"><span data-stu-id="e29d0-128">To reexport Positive Pay files</span></span>

1. <span data-ttu-id="e29d0-129">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankrekeningen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="e29d0-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="e29d0-130">Selecteer de bankrekening waarvoor u Positive Pay-bestanden opnieuw wilt exporteren.</span><span class="sxs-lookup"><span data-stu-id="e29d0-130">Select the bank account that you want to reexport Positive Pay files for.</span></span>
3. <span data-ttu-id="e29d0-131">Kies de actie **Positive Pay-posten**.</span><span class="sxs-lookup"><span data-stu-id="e29d0-131">Choose the **Positive Pay Entries** action.</span></span>
4. <span data-ttu-id="e29d0-132">Selecteer de regel van het Positive Pay-exportbestand dat u opnieuw wilt exporteren.</span><span class="sxs-lookup"><span data-stu-id="e29d0-132">Select the line for the Positive Pay export file that you want to reexport.</span></span>
5. <span data-ttu-id="e29d0-133">Kies in het venster **Positive Pay-posten** de actie **Positive Pay opnieuw exporteren naar bestand**.</span><span class="sxs-lookup"><span data-stu-id="e29d0-133">In the **Positive Pay Entries** window, choose the **Reexport Positive Pay to File** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="e29d0-134">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e29d0-134">See Also</span></span>
[<span data-ttu-id="e29d0-135">Financiën</span><span class="sxs-lookup"><span data-stu-id="e29d0-135">Finance</span></span>](finance.md)  
[<span data-ttu-id="e29d0-136">Financiën instellen</span><span class="sxs-lookup"><span data-stu-id="e29d0-136">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="e29d0-137">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="e29d0-137">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="e29d0-138">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e29d0-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

