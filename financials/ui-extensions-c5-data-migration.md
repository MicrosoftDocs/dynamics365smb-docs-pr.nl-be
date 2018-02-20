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
ms.date: 11/21/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d3b8d3d01ce75da59c1cce873077955776963ce9
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---

# <a name="the-c5-data-migration-extension-for-finance-and-operations-business-edition"></a><span data-ttu-id="7add4-103">De extensie C5-gegevensmigratie voor Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="7add4-103">The C5 Data Migration Extension for Finance and Operations, Business edition</span></span>
<span data-ttu-id="7add4-104">Deze extensie maakt het eenvoudidiger om klanten, leveranciers, artikelen en uw grootboekrekeningen van Microsoft Dynamics C5 2012 te migreren naar [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7add4-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="7add4-105">U kunt historische posten voor grootboekrekeningen ook migreren.</span><span class="sxs-lookup"><span data-stu-id="7add4-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="7add4-106">Het bedrijf in [!INCLUDE[d365fin](includes/d365fin_md.md)] mag geen gegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="7add4-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="7add4-107">Bovendien mag u, nadat u een migratie start, geen klanten, leveranciers, artikelen of rekeningen maken totdat de migratie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="7add4-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

##<a name="what-data-is-migrated"></a><span data-ttu-id="7add4-108">Welke gegevens worden gemigreerd?</span><span class="sxs-lookup"><span data-stu-id="7add4-108">What Data is Migrated?</span></span>
<span data-ttu-id="7add4-109">De volgende gegevens worden voor elke entiteit gemigreerd:</span><span class="sxs-lookup"><span data-stu-id="7add4-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="7add4-110">**Klanten**</span><span class="sxs-lookup"><span data-stu-id="7add4-110">**Customers**</span></span>
* <span data-ttu-id="7add4-111">Vestiging</span><span class="sxs-lookup"><span data-stu-id="7add4-111">Location</span></span>
* <span data-ttu-id="7add4-112">Land</span><span class="sxs-lookup"><span data-stu-id="7add4-112">Country</span></span>
* <span data-ttu-id="7add4-113">Klantdimensies (afdeling, centrum, doel)</span><span class="sxs-lookup"><span data-stu-id="7add4-113">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="7add4-114">Verzendwijze</span><span class="sxs-lookup"><span data-stu-id="7add4-114">Shipment method</span></span>
* <span data-ttu-id="7add4-115">Verkoper</span><span class="sxs-lookup"><span data-stu-id="7add4-115">Sales Person</span></span>
* <span data-ttu-id="7add4-116">Betalingsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="7add4-116">Payment terms</span></span>
* <span data-ttu-id="7add4-117">Betalingswijze</span><span class="sxs-lookup"><span data-stu-id="7add4-117">Payment method</span></span>
* <span data-ttu-id="7add4-118">Klantenprijsgroep</span><span class="sxs-lookup"><span data-stu-id="7add4-118">Customer price group</span></span>
* <span data-ttu-id="7add4-119">Klantenfactuurkorting</span><span class="sxs-lookup"><span data-stu-id="7add4-119">Customer invoice discount</span></span>

<span data-ttu-id="7add4-120">Als u rekeningen migreert, worden de volgende gegevens ook gemigreerd:</span><span class="sxs-lookup"><span data-stu-id="7add4-120">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="7add4-121">Klantboekingsinstelling</span><span class="sxs-lookup"><span data-stu-id="7add4-121">Customer posting setup</span></span>
* <span data-ttu-id="7add4-122">Dagboekbatch</span><span class="sxs-lookup"><span data-stu-id="7add4-122">General journal batch</span></span>
* <span data-ttu-id="7add4-123">Open transacties (klantenposten)</span><span class="sxs-lookup"><span data-stu-id="7add4-123">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="7add4-124">**Leveranc.**</span><span class="sxs-lookup"><span data-stu-id="7add4-124">**Vendors**</span></span>
* <span data-ttu-id="7add4-125">Vestiging</span><span class="sxs-lookup"><span data-stu-id="7add4-125">Location</span></span>
* <span data-ttu-id="7add4-126">Land</span><span class="sxs-lookup"><span data-stu-id="7add4-126">Country</span></span>
* <span data-ttu-id="7add4-127">Leveranciersdimensies (afdeling, centrum, doel)</span><span class="sxs-lookup"><span data-stu-id="7add4-127">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="7add4-128">Factuurkorting</span><span class="sxs-lookup"><span data-stu-id="7add4-128">Invoice discount</span></span>
* <span data-ttu-id="7add4-129">Verzendwijze</span><span class="sxs-lookup"><span data-stu-id="7add4-129">Shipment method</span></span>
* <span data-ttu-id="7add4-130">Inkoper</span><span class="sxs-lookup"><span data-stu-id="7add4-130">Purchaser</span></span>
* <span data-ttu-id="7add4-131">Betalingsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="7add4-131">Payment terms</span></span>
* <span data-ttu-id="7add4-132">Betalingswijze</span><span class="sxs-lookup"><span data-stu-id="7add4-132">Payment method</span></span>
* <span data-ttu-id="7add4-133">Leveranciersfactuurkorting</span><span class="sxs-lookup"><span data-stu-id="7add4-133">Vendor invoice discount</span></span>

<span data-ttu-id="7add4-134">Als u rekeningen migreert, worden de volgende gegevens ook gemigreerd:</span><span class="sxs-lookup"><span data-stu-id="7add4-134">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="7add4-135">Leveranciersboekingsinstelling</span><span class="sxs-lookup"><span data-stu-id="7add4-135">Vendor posting setup</span></span>
* <span data-ttu-id="7add4-136">Dagboekbatch</span><span class="sxs-lookup"><span data-stu-id="7add4-136">General journal batch</span></span>
* <span data-ttu-id="7add4-137">Open transacties (leveranciersposten)</span><span class="sxs-lookup"><span data-stu-id="7add4-137">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="7add4-138">**Artikelen**</span><span class="sxs-lookup"><span data-stu-id="7add4-138">**Items**</span></span>
* <span data-ttu-id="7add4-139">Vestiging</span><span class="sxs-lookup"><span data-stu-id="7add4-139">Location</span></span>
* <span data-ttu-id="7add4-140">Land</span><span class="sxs-lookup"><span data-stu-id="7add4-140">Country</span></span>
* <span data-ttu-id="7add4-141">Artikeldimensies (afdeling, centrum, doel)</span><span class="sxs-lookup"><span data-stu-id="7add4-141">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="7add4-142">Verkoopregelkortingen</span><span class="sxs-lookup"><span data-stu-id="7add4-142">Sales line discounts</span></span>
* <span data-ttu-id="7add4-143">Klantenkortingsgroepen</span><span class="sxs-lookup"><span data-stu-id="7add4-143">Customer discount groups</span></span>
* <span data-ttu-id="7add4-144">Artikelkortingsgroepen</span><span class="sxs-lookup"><span data-stu-id="7add4-144">Item discount groups</span></span>
* <span data-ttu-id="7add4-145">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="7add4-145">Sales price</span></span>
* <span data-ttu-id="7add4-146">Tariefnummer</span><span class="sxs-lookup"><span data-stu-id="7add4-146">Tariff number</span></span>
* <span data-ttu-id="7add4-147">Maateenheden</span><span class="sxs-lookup"><span data-stu-id="7add4-147">Units of measure</span></span>
* <span data-ttu-id="7add4-148">Artikeltraceringscode</span><span class="sxs-lookup"><span data-stu-id="7add4-148">Item tracking code</span></span>
* <span data-ttu-id="7add4-149">Klantenprijsgroep</span><span class="sxs-lookup"><span data-stu-id="7add4-149">Customer price group</span></span>

<span data-ttu-id="7add4-150">Als u rekeningen migreert, worden de volgende gegevens ook gemigreerd:</span><span class="sxs-lookup"><span data-stu-id="7add4-150">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="7add4-151">Voorraadboekingsinstelling</span><span class="sxs-lookup"><span data-stu-id="7add4-151">Inventory posting setup</span></span>
* <span data-ttu-id="7add4-152">Algemene boekingsinstelling</span><span class="sxs-lookup"><span data-stu-id="7add4-152">General posting setup</span></span>
* <span data-ttu-id="7add4-153">Artikeldagboekbatch</span><span class="sxs-lookup"><span data-stu-id="7add4-153">Item journal batch</span></span>
* <span data-ttu-id="7add4-154">Open transacties (artikelposten)</span><span class="sxs-lookup"><span data-stu-id="7add4-154">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="7add4-155">Als er open transacties zijn die vreemde valuta's gebruiken, wordt de wisselkoers voor deze valuta ook gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="7add4-155">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="7add4-156">Andere wisselkoersen worden niet gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="7add4-156">Other exchange rates are not migrated.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="7add4-157">Gegevens te migreren</span><span class="sxs-lookup"><span data-stu-id="7add4-157">To migrate data</span></span>
<span data-ttu-id="7add4-158">Er zijn slechts enkele stappen nodig om gegevens vanuit C5 te exporteren en deze te importeren in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="7add4-158">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="7add4-159">Gebruik in C5 de functie **Database exporteren** om de gegevens te exporteren.</span><span class="sxs-lookup"><span data-stu-id="7add4-159">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="7add4-160">Verzend vervolgens de exportmap naar een gecomprimeerde (gezipte) map.</span><span class="sxs-lookup"><span data-stu-id="7add4-160">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="7add4-161">Klik in [!INCLUDE[d365fin](includes/d365fin_md.md)] op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gegevensmigratie** in en kies vervolgens **Gegevensmigratie**.</span><span class="sxs-lookup"><span data-stu-id="7add4-161">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="7add4-162">Voer de stappen uit in het handleiding met begeleide instellingen.</span><span class="sxs-lookup"><span data-stu-id="7add4-162">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="7add4-163">Zorg dat u **Importeren vanuit Microsoft Dynamics C5 2012** als gegevensbron kiest.</span><span class="sxs-lookup"><span data-stu-id="7add4-163">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="7add4-164">Bedrijven voegen vaak velden toe om C5 aan te passen aan de behoeften van hun specifieke branche.</span><span class="sxs-lookup"><span data-stu-id="7add4-164">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="7add4-165"> migreert geen gegevens van aangepaste velden.</span><span class="sxs-lookup"><span data-stu-id="7add4-165"> does not migrate data from custom fields.</span></span> <span data-ttu-id="7add4-166">Ook mislukt de migratie als u meer dan 10 aangepaste velden hebt.</span><span class="sxs-lookup"><span data-stu-id="7add4-166">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="7add4-167">De status van de migratie weergeven</span><span class="sxs-lookup"><span data-stu-id="7add4-167">Viewing the Status of the Migration</span></span>
<span data-ttu-id="7add4-168">Gebruik de pagina **Gegevensmigratieoverzicht** om het resultaat van de migratie bekijken.</span><span class="sxs-lookup"><span data-stu-id="7add4-168">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="7add4-169">De pagina bevat gegevens zoals het aantal entiteiten dat de migratie omvat, de status van de migratie, het aantal items dat is gemigreerd en of dat is gelukt.</span><span class="sxs-lookup"><span data-stu-id="7add4-169">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="7add4-170">De pagina toont ook het aantal fouten, en stelt u in staat te onderzoeken wat er mis is gegaan. Ook bent u zo in staat om, indien mogelijk, gemakkelijk naar de entiteit gaan en de problemen op te lossen.</span><span class="sxs-lookup"><span data-stu-id="7add4-170">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="7add4-171">Zie de volgende sectie in dit onderwerp voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7add4-171">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="7add4-172">Terwijl u op de resultaten van de migratie wacht, moet u de pagina vernieuwen om de resultaten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="7add4-172">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="7add4-173">Fouten corrigeren</span><span class="sxs-lookup"><span data-stu-id="7add4-173">Correcting Errors</span></span>
<span data-ttu-id="7add4-174">Als er iets misgaat en zich een fout voordoet, wordt in het veld **Status** **Voltooid met fouten** weergegeven en in het veld **Aantal fouten** aangegeven hoeveel fouten er zijn.</span><span class="sxs-lookup"><span data-stu-id="7add4-174">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="7add4-175">Als u een lijst met fouten wilt zien, kunt u de pagina met de **gegevensmigratiefouten** openen door het volgende te selecteren:</span><span class="sxs-lookup"><span data-stu-id="7add4-175">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="7add4-176">Het aantal in het veld **Aantal fouten** voor de entiteit.</span><span class="sxs-lookup"><span data-stu-id="7add4-176">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="7add4-177">Op de entiteit en vervolgens op de actie **Fouten weergeven** te klikken.</span><span class="sxs-lookup"><span data-stu-id="7add4-177">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="7add4-178">Op de pagina met de **gegevensmigratiefouten** kunt een foutbericht kiezen om een fout op te lossen, selecteert u vervolgens **Record bewerken** om een pagina te openen met de gemigreerde gegevens voor de entiteit.</span><span class="sxs-lookup"><span data-stu-id="7add4-178">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="7add4-179">Nadat u een of meer fouten hebt opgelost, kunt u **Migreren** kiezen om alleen de entiteiten te migreren die u hebt hersteld, zonder dat u geheel op nieuw moet beginnen met de migratie.</span><span class="sxs-lookup"><span data-stu-id="7add4-179">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="7add4-180">Als u meer dan één fout hebt verholpen, kunt u de functie **Meer selecteren** gebruiken om meerdere regels te selecteren om te migreren.</span><span class="sxs-lookup"><span data-stu-id="7add4-180">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="7add4-181">Of u kunt fouten die niet noodzakelijkerwijs moeten worden opgelost, selecteren en vervolgens **Selecties overslaan** kiezen.</span><span class="sxs-lookup"><span data-stu-id="7add4-181">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="7add4-182">Als u artikelen hebt die op een stuklijst zijn opgenomen, moet u mogelijk meer dan eens migreren als het oorspronkelijke artikel niet is gemaakt vóór de varianten die ernaar verwijzen..</span><span class="sxs-lookup"><span data-stu-id="7add4-182">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="7add4-183">Als een artikelvariant eerst is gemaakt, kan de verwijzing naar het oorspronkelijke artikel een foutbericht produceren.</span><span class="sxs-lookup"><span data-stu-id="7add4-183">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="7add4-184">Het verifiëren van gegevens na de migratie</span><span class="sxs-lookup"><span data-stu-id="7add4-184">Verifying Data After Migrating</span></span>
<span data-ttu-id="7add4-185">Eén manier om te controleren of uw gegevens correct zijn gemigreerd is te kijken naar de volgende pagina's in C5 en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7add4-185">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="7add4-186">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="7add4-186">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="7add4-187">Klantenposten</span><span class="sxs-lookup"><span data-stu-id="7add4-187">Customer Entries</span></span>| <span data-ttu-id="7add4-188">Financiële dagboeken</span><span class="sxs-lookup"><span data-stu-id="7add4-188">General Journals</span></span>|
|<span data-ttu-id="7add4-189">Leveranciersposten</span><span class="sxs-lookup"><span data-stu-id="7add4-189">Vendor Entries</span></span>| <span data-ttu-id="7add4-190">Financiële dagboeken</span><span class="sxs-lookup"><span data-stu-id="7add4-190">General Journals</span></span>|
|<span data-ttu-id="7add4-191">Artikelposten</span><span class="sxs-lookup"><span data-stu-id="7add4-191">Item Entries</span></span>| <span data-ttu-id="7add4-192">Artikeldagboeken</span><span class="sxs-lookup"><span data-stu-id="7add4-192">Item Journals</span></span>|

<span data-ttu-id="7add4-193">In [!INCLUDE[d365fin](includes/d365fin_md.md)] krijgt de batch voor de gemigreerde gegevens de naam **C5MIGRATE**.</span><span class="sxs-lookup"><span data-stu-id="7add4-193">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span>

## <a name="stopping-data-migration"></a><span data-ttu-id="7add4-194">De gegevensmigratie beëindigen</span><span class="sxs-lookup"><span data-stu-id="7add4-194">Stopping Data Migration</span></span>
<span data-ttu-id="7add4-195">U kunt de migratie van gegevens stoppen door **Alle migraties stoppen** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="7add4-195">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="7add4-196">Als u dat doet, worden alle wachtende migraties ook beëindigd.</span><span class="sxs-lookup"><span data-stu-id="7add4-196">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="7add4-197">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7add4-197">See Also</span></span>
<span data-ttu-id="7add4-198">[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="7add4-198">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="7add4-199">[Welkom bij [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="7add4-199">[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span></span>  

