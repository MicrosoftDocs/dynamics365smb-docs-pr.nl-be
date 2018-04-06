---
title: Beginsaldi van dagboeken maken | Microsoft Docs
description: Business Central bevat verschillende batchverwerkingen die u helpen bij de overdracht van oude rekeningsaldi naar een nieuw geconfigureerd bedrijf. U kunt deze gegevens gemakkelijk overbrengen met dagboekboekingen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: fc8e8f34220643b7cd3fd357aea3807641cee911
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="2be43-104">Beginsaldi van dagboeken maken</span><span class="sxs-lookup"><span data-stu-id="2be43-104">Create Journal Opening Balances</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="2be43-105"> bevat verschillende batchverwerkingen die u helpen bij de overdracht van oude rekeningsaldi naar een nieuw geconfigureerd bedrijf.</span><span class="sxs-lookup"><span data-stu-id="2be43-105"> includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="2be43-106">U kunt deze gegevens eenvoudig overbrengen met het klantendagboek, leveranciersdagboek, artikeldagboek of financieel dagboek.</span><span class="sxs-lookup"><span data-stu-id="2be43-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="2be43-107">De eerste stap is het maken van een configuratiepakket dat de instellingentabellen voor deze dagboeken bevat.</span><span class="sxs-lookup"><span data-stu-id="2be43-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="2be43-108">In de volgende procedure wordt ervan uitgegaan dat deze stap is voltooid.</span><span class="sxs-lookup"><span data-stu-id="2be43-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="2be43-109">Zie [Bedrijfsconfiguratie instellen](admin-set-up-company-configuration.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="2be43-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="2be43-110">In de procedure worden de daaropvolgende stappen beschreven, waaronder de toepassing van het pakket dat wordt geleverd door een partner.</span><span class="sxs-lookup"><span data-stu-id="2be43-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="2be43-111">Voordat u begint, moet u ervoor zorgen dat u zich bevindt op de rolcentrumpagina RapidStart Services-implementatie, want dat is de juiste context voor uw configuratiewerk.</span><span class="sxs-lookup"><span data-stu-id="2be43-111">Before you start, make sure that you are on the RapidStart Services Implementer Role Center page as it provides the correct context for your configuration work.</span></span> <span data-ttu-id="2be43-112">Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="2be43-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="2be43-113">De posten in een dagboek toepassen op een nieuw bedrijf</span><span class="sxs-lookup"><span data-stu-id="2be43-113">To apply the entries in a journal to a new company</span></span>  
1. <span data-ttu-id="2be43-114">Configureer een nieuw bedrijf en pas er een configuratiepakket op toe.</span><span class="sxs-lookup"><span data-stu-id="2be43-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="2be43-115">Zie voor meer informatie [Een bedrijf configureren met de wizard RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="2be43-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="2be43-116">Het nieuwe bedrijf bevat geen informatie over beginsaldi van dagboeken.</span><span class="sxs-lookup"><span data-stu-id="2be43-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="2be43-117">Open het configuratiewerkblad en importeer bestaande gegevens over klanten, artikelen, leveranciers en het grootboek.</span><span class="sxs-lookup"><span data-stu-id="2be43-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="2be43-118">Zie voor meer informatie [Klantgegevens migreren](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="2be43-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  
3. <span data-ttu-id="2be43-119">Kies bijvoorbeeld de actie **Grootboekjournaalregels maken**.</span><span class="sxs-lookup"><span data-stu-id="2be43-119">Choose, for example, the **Create G/L Journal Lines** action.</span></span>  
4. <span data-ttu-id="2be43-120">Vul het sneltabblad **Opties** in en stel zo nodig filters in.</span><span class="sxs-lookup"><span data-stu-id="2be43-120">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="2be43-121">Voer bijvoorbeeld in het veld **Dagboeksjabloon** een naam in.</span><span class="sxs-lookup"><span data-stu-id="2be43-121">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="2be43-122">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="2be43-122">Choose the **OK** button.</span></span> <span data-ttu-id="2be43-123">De records bevinden zich nu in het dagboek, maar de bedragen zijn leeg.</span><span class="sxs-lookup"><span data-stu-id="2be43-123">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="2be43-124">Exporteer de dagboektabel naar Excel en voer handmatig de gegevens voor boeking en tegenrekening in vanuit de oude gegevens.</span><span class="sxs-lookup"><span data-stu-id="2be43-124">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="2be43-125">Importeer en pas de tabelgegevens toe op het nieuwe bedrijf.</span><span class="sxs-lookup"><span data-stu-id="2be43-125">Import and apply the table information into the new company.</span></span> <span data-ttu-id="2be43-126">De dagboekregels zijn gereed om te worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="2be43-126">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="2be43-127">Selecteer op het configuratiewerkblad de dagboekregeltabel en kies de actie **Databasegegevens**.</span><span class="sxs-lookup"><span data-stu-id="2be43-127">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="2be43-128">Controleer de informatie en kies de actie **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="2be43-128">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="2be43-129">Herhaal de stappen voor het importeren en boeken van andere beginsaldi.</span><span class="sxs-lookup"><span data-stu-id="2be43-129">Repeat the steps to import and post any other opening balances.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2be43-130">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2be43-130">See Also</span></span>  
[<span data-ttu-id="2be43-131">Configuraties toepassen op nieuwe bedrijven</span><span class="sxs-lookup"><span data-stu-id="2be43-131">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="2be43-132">Een bedrijf met RapidStart Services instellen</span><span class="sxs-lookup"><span data-stu-id="2be43-132">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="2be43-133">Beheer</span><span class="sxs-lookup"><span data-stu-id="2be43-133">Administration</span></span>](admin-setup-and-administration.md)

