---
title: Beginsaldi van dagboeken maken | Microsoft Docs
description: Business Central bevat verschillende batchverwerkingen die u helpen bij de overdracht van oude rekeningsaldi naar een nieuw geconfigureerd bedrijf. U kunt deze gegevens gemakkelijk overbrengen met dagboekboekingen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8ffb5b8b90d0fdd4f3e1bd90271db8568c05d41e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753979"
---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="0b70b-104">Beginsaldi van dagboeken maken</span><span class="sxs-lookup"><span data-stu-id="0b70b-104">Create Journal Opening Balances</span></span>

[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="0b70b-105">bevat verschillende batchverwerkingen die u helpen bij de overdracht van oude rekeningsaldi naar een nieuw geconfigureerd bedrijf.</span><span class="sxs-lookup"><span data-stu-id="0b70b-105">includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="0b70b-106">U kunt deze gegevens eenvoudig overbrengen met het klantendagboek, leveranciersdagboek, artikeldagboek of financieel dagboek.</span><span class="sxs-lookup"><span data-stu-id="0b70b-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="0b70b-107">De eerste stap is het maken van een configuratiepakket dat de instellingentabellen voor deze dagboeken bevat.</span><span class="sxs-lookup"><span data-stu-id="0b70b-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="0b70b-108">In de volgende procedure wordt ervan uitgegaan dat deze stap is voltooid.</span><span class="sxs-lookup"><span data-stu-id="0b70b-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="0b70b-109">Zie [Bedrijfsconfiguratie instellen](admin-set-up-company-configuration.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="0b70b-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="0b70b-110">In de procedure worden de daaropvolgende stappen beschreven, waaronder de toepassing van het pakket dat wordt geleverd door een partner.</span><span class="sxs-lookup"><span data-stu-id="0b70b-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="0b70b-111">Voordat u begint, moet u ervoor zorgen dat u de rolcentrumpagina Beheer gebruikt, omdat dit de juiste context voor uw configuratiewerk is.</span><span class="sxs-lookup"><span data-stu-id="0b70b-111">Before you start, make sure that you are using the Administration Role Center page because it provides the correct context for your configuration work.</span></span> <span data-ttu-id="0b70b-112">Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="0b70b-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="0b70b-113">De posten in een dagboek toepassen op een nieuw bedrijf</span><span class="sxs-lookup"><span data-stu-id="0b70b-113">To apply the entries in a journal to a new company</span></span>

1. <span data-ttu-id="0b70b-114">Configureer een nieuw bedrijf en pas een configuratiepakket toe.</span><span class="sxs-lookup"><span data-stu-id="0b70b-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="0b70b-115">Zie voor meer informatie [Een bedrijf configureren met de wizard RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="0b70b-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="0b70b-116">Het nieuwe bedrijf bevat geen informatie over beginsaldi van dagboeken.</span><span class="sxs-lookup"><span data-stu-id="0b70b-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="0b70b-117">Open het configuratiewerkblad en importeer bestaande gegevens over klanten, artikelen, leveranciers en het grootboek.</span><span class="sxs-lookup"><span data-stu-id="0b70b-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="0b70b-118">Zie voor meer informatie [Klantgegevens migreren](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="0b70b-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  

    <span data-ttu-id="0b70b-119">Nu beschikt u over hoofdgegevens.</span><span class="sxs-lookup"><span data-stu-id="0b70b-119">Now you have master data in place.</span></span> <span data-ttu-id="0b70b-120">Vervolgens voegt u de beginsaldi toe.</span><span class="sxs-lookup"><span data-stu-id="0b70b-120">Next, you add the opening balances.</span></span> <span data-ttu-id="0b70b-121">De volgende stappen beschrijven hoe u dagboekregels voor grootboekrekeningen maakt, maar hetzelfde geldt voor het maken van dagboekregels voor klanten, leveranciers en artikelen.</span><span class="sxs-lookup"><span data-stu-id="0b70b-121">The following steps describe how to create journal lines for G/L accounts, but the same apply to creating journal lines for customers, vendors, and items.</span></span>  
3. <span data-ttu-id="0b70b-122">Kies de actie **Grootboekrekeningregels maken**.</span><span class="sxs-lookup"><span data-stu-id="0b70b-122">Choose the **Create G/L Acct. Journal Lines** action.</span></span>  
4. <span data-ttu-id="0b70b-123">Vul het sneltabblad **Opties** in en stel zo nodig filters in.</span><span class="sxs-lookup"><span data-stu-id="0b70b-123">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="0b70b-124">Voer bijvoorbeeld in het veld **Dagboeksjabloon** een naam in.</span><span class="sxs-lookup"><span data-stu-id="0b70b-124">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="0b70b-125">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b70b-125">Choose the **OK** button.</span></span> <span data-ttu-id="0b70b-126">De records bevinden zich nu in het dagboek, maar de bedragen zijn leeg.</span><span class="sxs-lookup"><span data-stu-id="0b70b-126">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="0b70b-127">Exporteer de dagboektabel naar Excel en voer handmatig de gegevens voor boeking en tegenrekening in vanuit de oude gegevens.</span><span class="sxs-lookup"><span data-stu-id="0b70b-127">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="0b70b-128">Importeer en pas de tabelgegevens toe op het nieuwe bedrijf.</span><span class="sxs-lookup"><span data-stu-id="0b70b-128">Import and apply the table information into the new company.</span></span> <span data-ttu-id="0b70b-129">De dagboekregels zijn gereed om te worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="0b70b-129">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="0b70b-130">Selecteer op het configuratiewerkblad de dagboekregeltabel en kies de actie **Databasegegevens**.</span><span class="sxs-lookup"><span data-stu-id="0b70b-130">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="0b70b-131">Controleer de informatie en kies de actie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="0b70b-131">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="0b70b-132">Herhaal de stappen voor het importeren en boeken van andere beginsaldi.</span><span class="sxs-lookup"><span data-stu-id="0b70b-132">Repeat the steps to import and post any other opening balances.</span></span>  

> [!TIP]
> <span data-ttu-id="0b70b-133">U kunt dezelfde batchtaken gebruiken om beginsaldi toe te voegen wanneer u een nieuwe klant of leverancier registreert waarmee u eerder zaken hebt gedaan, maar niet geregistreerd in [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="0b70b-133">You can use the same batch jobs to add opening balances whenever you register a new customer or vendor that you have done business with before but not registered in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="0b70b-134">Zoek gewoon naar de relevante taak en kies vervolgens de relevante koppeling.</span><span class="sxs-lookup"><span data-stu-id="0b70b-134">Just search for the relevant task, and then choose the relevant link.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b70b-135">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0b70b-135">See Also</span></span>

[<span data-ttu-id="0b70b-136">Configuraties toepassen op nieuwe bedrijven</span><span class="sxs-lookup"><span data-stu-id="0b70b-136">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="0b70b-137">Een bedrijf instellen met RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="0b70b-137">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="0b70b-138">Beheer</span><span class="sxs-lookup"><span data-stu-id="0b70b-138">Administration</span></span>](admin-setup-and-administration.md)  
