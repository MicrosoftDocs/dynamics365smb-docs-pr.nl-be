---
title: De extensie C5-gegevensmigratie gebruiken | Microsoft Docs
description: Gebruik deze extensie om klanten, leveranciers, artikelen en grootboekrekeningen te migreren van Microsoft Dynamics C5 2012 naar Financials.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 09/26/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 2d7d533662936116ffa40ded07b68e845fed810b
ms.contentlocale: nl-be
ms.lasthandoff: 11/10/2017

---

# <a name="the-c5-data-migration-extension-for-dynamics-365-for-finance-and-operations-business-edition"></a><span data-ttu-id="09f34-103">De extensie C5-gegevensmigratie voor Dynamics 365 for Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="09f34-103">The C5 Data Migration Extension for Dynamics 365 for Finance and Operations, Business Edition</span></span>
<span data-ttu-id="09f34-104">Deze extensie maakt het eenvoudidiger om klanten, leveranciers, artikelen en uw grootboekrekeningen van Microsoft Dynamics C5 2012 te migreren naar [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="09f34-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
  
> [!Note] 
> <span data-ttu-id="09f34-105">Het bedrijf in [!INCLUDE[d365fin](includes/d365fin_md.md)] mag geen gegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="09f34-105">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="09f34-106">Bovendien mag u, nadat u een migratie start, geen klanten, leveranciers, artikelen of rekeningen maken totdat de migratie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="09f34-106">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="09f34-107">Gegevens te migreren</span><span class="sxs-lookup"><span data-stu-id="09f34-107">To migrate data</span></span>
<span data-ttu-id="09f34-108">Er zijn slechts enkele stappen nodig om gegevens vanuit C5 te exporteren en deze te importeren in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="09f34-108">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  
  
1. <span data-ttu-id="09f34-109">Gebruik in C5 de functie **Database exporteren** om de gegevens te exporteren.</span><span class="sxs-lookup"><span data-stu-id="09f34-109">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="09f34-110">Verzend vervolgens de exportmap naar een gecomprimeerde (gezipte) map.</span><span class="sxs-lookup"><span data-stu-id="09f34-110">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="09f34-111">Klik in [!INCLUDE[d365fin](includes/d365fin_md.md)] op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gegevensmigratie** in en kies vervolgens **Gegevensmigratie**.</span><span class="sxs-lookup"><span data-stu-id="09f34-111">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="09f34-112">Voer de stappen uit in het handleiding met begeleide instellingen.</span><span class="sxs-lookup"><span data-stu-id="09f34-112">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="09f34-113">Zorg dat u **Importeren vanuit Microsoft Dynamics C5 2012** als gegevensbron kiest.</span><span class="sxs-lookup"><span data-stu-id="09f34-113">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note] 
> <span data-ttu-id="09f34-114">Bedrijven voegen vaak velden toe om C5 aan te passen aan de behoeften van hun specifieke branche.</span><span class="sxs-lookup"><span data-stu-id="09f34-114">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="09f34-115"> migreert geen gegevens van aangepaste velden.</span><span class="sxs-lookup"><span data-stu-id="09f34-115"> does not migrate data from custom fields.</span></span> <span data-ttu-id="09f34-116">Ook mislukt de migratie als u meer dan 10 aangepaste velden hebt.</span><span class="sxs-lookup"><span data-stu-id="09f34-116">Also, migration will fail if you have more than 10 custom fields.</span></span> 

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="09f34-117">De status van de migratie weergeven</span><span class="sxs-lookup"><span data-stu-id="09f34-117">Viewing the Status of the Migration</span></span>
<span data-ttu-id="09f34-118">Gebruik de pagina **Gegevensmigratieoverzicht** om het resultaat van de migratie bekijken.</span><span class="sxs-lookup"><span data-stu-id="09f34-118">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="09f34-119">De pagina bevat gegevens zoals het aantal entiteiten dat de migratie omvat, de status van de migratie, het aantal items dat is gemigreerd en of dat is gelukt.</span><span class="sxs-lookup"><span data-stu-id="09f34-119">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="09f34-120">De pagina toont ook het aantal fouten, en stelt u in staat te onderzoeken wat er mis is gegaan. Ook bent u zo in staat om, indien mogelijk, gemakkelijk naar de entiteit gaan en de problemen op te lossen.</span><span class="sxs-lookup"><span data-stu-id="09f34-120">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="09f34-121">Zie de volgende sectie in dit onderwerp voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="09f34-121">For more information, see the next section in this topic.</span></span> 

> [!Note] 
> <span data-ttu-id="09f34-122">Terwijl u op de resultaten van de migratie wacht, moet u de pagina vernieuwen om de resultaten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="09f34-122">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="09f34-123">Fouten corrigeren</span><span class="sxs-lookup"><span data-stu-id="09f34-123">Correcting Errors</span></span>
<span data-ttu-id="09f34-124">Als er iets misgaat en zich een fout voordoet, wordt in het veld **Status** **Voltooid met fouten** weergegeven en in het veld **Aantal fouten** aangegeven hoeveel fouten er zijn.</span><span class="sxs-lookup"><span data-stu-id="09f34-124">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="09f34-125">Als u een lijst met fouten wilt zien, kunt u de pagina met de **gegevensmigratiefouten** openen door het volgende te selecteren:</span><span class="sxs-lookup"><span data-stu-id="09f34-125">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>

* <span data-ttu-id="09f34-126">Het aantal in het veld **Aantal fouten** voor de entiteit.</span><span class="sxs-lookup"><span data-stu-id="09f34-126">The number in the **Error Count** field for the entity.</span></span> 
* <span data-ttu-id="09f34-127">Op de entiteit en vervolgens op de actie **Fouten weergeven** te klikken.</span><span class="sxs-lookup"><span data-stu-id="09f34-127">The entity, and then the **Show Errors** action.</span></span> 

<span data-ttu-id="09f34-128">Op de pagina met de **gegevensmigratiefouten** kunt een foutbericht kiezen om een fout op te lossen, selecteert u vervolgens **Record bewerken** om een pagina te openen met de gemigreerde gegevens voor de entiteit.</span><span class="sxs-lookup"><span data-stu-id="09f34-128">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="09f34-129">Nadat u een of meer fouten hebt opgelost, kunt u **Migreren** kiezen om alleen de entiteiten te migreren die u hebt hersteld, zonder dat u geheel op nieuw moet beginnen met de migratie.</span><span class="sxs-lookup"><span data-stu-id="09f34-129">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="09f34-130">Als u meer dan één fout hebt verholpen, kunt u de functie **Meer selecteren** gebruiken om meerdere regels te selecteren om te migreren.</span><span class="sxs-lookup"><span data-stu-id="09f34-130">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="09f34-131">Of u kunt fouten die niet noodzakelijkerwijs moeten worden opgelost, selecteren en vervolgens **Selecties overslaan** kiezen.</span><span class="sxs-lookup"><span data-stu-id="09f34-131">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="09f34-132">Als u artikelen hebt die op een stuklijst zijn opgenomen, moet u mogelijk meer dan eens migreren als het oorspronkelijke artikel niet is gemaakt vóór de varianten die ernaar verwijzen..</span><span class="sxs-lookup"><span data-stu-id="09f34-132">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="09f34-133">Als een artikelvariant eerst is gemaakt, kan de verwijzing naar het oorspronkelijke artikel een foutbericht produceren.</span><span class="sxs-lookup"><span data-stu-id="09f34-133">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="09f34-134">Het verifiëren van gegevens na de migratie</span><span class="sxs-lookup"><span data-stu-id="09f34-134">Verifying Data After Migrating</span></span> 
<span data-ttu-id="09f34-135">Als u wilt controleren of uw gegevens juist zijn gemigreerd, kunt u de volgende pagina´s in C5 en [!INCLUDE[d365fin](includes/d365fin_md.md)] bekijken.</span><span class="sxs-lookup"><span data-stu-id="09f34-135">If you want to verify that your data migrated correctly, you can look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="09f34-136">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="09f34-136">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="09f34-137">Klantenposten</span><span class="sxs-lookup"><span data-stu-id="09f34-137">Customer Entries</span></span>| <span data-ttu-id="09f34-138">Financiële dagboeken</span><span class="sxs-lookup"><span data-stu-id="09f34-138">General Journals</span></span>|
|<span data-ttu-id="09f34-139">Leveranciersposten</span><span class="sxs-lookup"><span data-stu-id="09f34-139">Vendor Entries</span></span>| <span data-ttu-id="09f34-140">Financiële dagboeken</span><span class="sxs-lookup"><span data-stu-id="09f34-140">General Journals</span></span>|
|<span data-ttu-id="09f34-141">Artikelposten</span><span class="sxs-lookup"><span data-stu-id="09f34-141">Item Entries</span></span>| <span data-ttu-id="09f34-142">Artikeldagboeken</span><span class="sxs-lookup"><span data-stu-id="09f34-142">Item Journals</span></span>|

<span data-ttu-id="09f34-143">In [!INCLUDE[d365fin](includes/d365fin_md.md)] krijgt de batch voor de gemigreerde gegevens de naam **C5MIGRATE**.</span><span class="sxs-lookup"><span data-stu-id="09f34-143">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span> 

## <a name="stopping-data-migration"></a><span data-ttu-id="09f34-144">De gegevensmigratie beëindigen</span><span class="sxs-lookup"><span data-stu-id="09f34-144">Stopping Data Migration</span></span>
<span data-ttu-id="09f34-145">U kunt de migratie van gegevens stoppen door **Alle migraties stoppen** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="09f34-145">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="09f34-146">Als u dat doet, worden alle wachtende migraties ook beëindigd.</span><span class="sxs-lookup"><span data-stu-id="09f34-146">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="09f34-147">Zie ook</span><span class="sxs-lookup"><span data-stu-id="09f34-147">See Also</span></span>
<span data-ttu-id="09f34-148">[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="09f34-148">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="09f34-149">[Welkom bij [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="09f34-149">[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span></span>  

