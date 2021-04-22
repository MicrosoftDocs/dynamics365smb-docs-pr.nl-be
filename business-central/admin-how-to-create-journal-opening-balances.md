---
title: Beginsaldi van dagboeken maken | Microsoft Docs
description: Business Central bevat verschillende batchverwerkingen die u helpen bij de overdracht van oude rekeningsaldi naar een nieuw geconfigureerd bedrijf. U kunt deze gegevens gemakkelijk overbrengen met dagboekboekingen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5e1bb8e34e70d1d906850c157107b9b9701c6c50
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779869"
---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="ff425-104">Beginsaldi van dagboeken maken</span><span class="sxs-lookup"><span data-stu-id="ff425-104">Create Journal Opening Balances</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="ff425-105">bevat verschillende batchverwerkingen die u helpen bij de overdracht van oude rekeningsaldi naar een nieuw geconfigureerd bedrijf.</span><span class="sxs-lookup"><span data-stu-id="ff425-105">includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="ff425-106">U kunt deze gegevens eenvoudig overbrengen met het klantendagboek, leveranciersdagboek, artikeldagboek of financieel dagboek.</span><span class="sxs-lookup"><span data-stu-id="ff425-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="ff425-107">De eerste stap is het maken van een configuratiepakket dat de instellingentabellen voor deze dagboeken bevat.</span><span class="sxs-lookup"><span data-stu-id="ff425-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="ff425-108">In de volgende procedure wordt ervan uitgegaan dat deze stap is voltooid.</span><span class="sxs-lookup"><span data-stu-id="ff425-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="ff425-109">Zie [Bedrijfsconfiguratie instellen](admin-set-up-company-configuration.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ff425-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="ff425-110">In de procedure worden de daaropvolgende stappen beschreven, waaronder de toepassing van het pakket dat wordt geleverd door een partner.</span><span class="sxs-lookup"><span data-stu-id="ff425-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="ff425-111">Voordat u begint, moet u ervoor zorgen dat u de rolcentrumpagina Beheer gebruikt, omdat dit de juiste context voor uw configuratiewerk is.</span><span class="sxs-lookup"><span data-stu-id="ff425-111">Before you start, make sure that you are using the Administration Role Center page because it provides the correct context for your configuration work.</span></span> <span data-ttu-id="ff425-112">Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="ff425-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="ff425-113">De posten in een dagboek toepassen op een nieuw bedrijf</span><span class="sxs-lookup"><span data-stu-id="ff425-113">To apply the entries in a journal to a new company</span></span>

1. <span data-ttu-id="ff425-114">Configureer een nieuw bedrijf en pas een configuratiepakket toe.</span><span class="sxs-lookup"><span data-stu-id="ff425-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="ff425-115">Zie voor meer informatie [Een bedrijf configureren met de wizard RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="ff425-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="ff425-116">Het nieuwe bedrijf bevat geen informatie over beginsaldi van dagboeken.</span><span class="sxs-lookup"><span data-stu-id="ff425-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="ff425-117">Open het configuratiewerkblad en importeer bestaande gegevens over klanten, artikelen, leveranciers en het grootboek.</span><span class="sxs-lookup"><span data-stu-id="ff425-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="ff425-118">Zie voor meer informatie [Klantgegevens migreren](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="ff425-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  

    <span data-ttu-id="ff425-119">Nu beschikt u over hoofdgegevens.</span><span class="sxs-lookup"><span data-stu-id="ff425-119">Now you have master data in place.</span></span> <span data-ttu-id="ff425-120">Vervolgens voegt u de beginsaldi toe.</span><span class="sxs-lookup"><span data-stu-id="ff425-120">Next, you add the opening balances.</span></span> <span data-ttu-id="ff425-121">De volgende stappen beschrijven hoe u dagboekregels voor grootboekrekeningen maakt, maar hetzelfde geldt voor het maken van dagboekregels voor klanten, leveranciers en artikelen.</span><span class="sxs-lookup"><span data-stu-id="ff425-121">The following steps describe how to create journal lines for G/L accounts, but the same apply to creating journal lines for customers, vendors, and items.</span></span>  
3. <span data-ttu-id="ff425-122">Kies de actie **Grootboekrekeningregels maken**.</span><span class="sxs-lookup"><span data-stu-id="ff425-122">Choose the **Create G/L Acct. Journal Lines** action.</span></span>  
4. <span data-ttu-id="ff425-123">Vul het sneltabblad **Opties** in en stel zo nodig filters in.</span><span class="sxs-lookup"><span data-stu-id="ff425-123">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="ff425-124">Voer bijvoorbeeld in het veld **Dagboeksjabloon** een naam in.</span><span class="sxs-lookup"><span data-stu-id="ff425-124">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="ff425-125">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="ff425-125">Choose the **OK** button.</span></span> <span data-ttu-id="ff425-126">De records bevinden zich nu in het dagboek, maar de bedragen zijn leeg.</span><span class="sxs-lookup"><span data-stu-id="ff425-126">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="ff425-127">Exporteer de dagboektabel naar Excel en voer handmatig de gegevens voor boeking en tegenrekening in vanuit de oude gegevens.</span><span class="sxs-lookup"><span data-stu-id="ff425-127">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="ff425-128">Importeer en pas de tabelgegevens toe op het nieuwe bedrijf.</span><span class="sxs-lookup"><span data-stu-id="ff425-128">Import and apply the table information into the new company.</span></span> <span data-ttu-id="ff425-129">De dagboekregels zijn gereed om te worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="ff425-129">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="ff425-130">Selecteer op het configuratiewerkblad de dagboekregeltabel en kies de actie **Databasegegevens**.</span><span class="sxs-lookup"><span data-stu-id="ff425-130">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="ff425-131">Controleer de informatie en kies de actie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="ff425-131">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="ff425-132">Herhaal de stappen voor het importeren en boeken van andere beginsaldi.</span><span class="sxs-lookup"><span data-stu-id="ff425-132">Repeat the steps to import and post any other opening balances.</span></span>  

> [!TIP]
> <span data-ttu-id="ff425-133">U kunt dezelfde batchtaken gebruiken om beginsaldi toe te voegen wanneer u een nieuwe klant of leverancier registreert waarmee u eerder zaken hebt gedaan, maar niet geregistreerd in [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="ff425-133">You can use the same batch jobs to add opening balances whenever you register a new customer or vendor that you have done business with before but not registered in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="ff425-134">Zoek gewoon naar de relevante taak en kies vervolgens de relevante koppeling.</span><span class="sxs-lookup"><span data-stu-id="ff425-134">Just search for the relevant task, and then choose the relevant link.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff425-135">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ff425-135">See Also</span></span>

[<span data-ttu-id="ff425-136">Configuraties toepassen op nieuwe bedrijven</span><span class="sxs-lookup"><span data-stu-id="ff425-136">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="ff425-137">Een bedrijf instellen met RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="ff425-137">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="ff425-138">Beheer</span><span class="sxs-lookup"><span data-stu-id="ff425-138">Administration</span></span>](admin-setup-and-administration.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]