---
title: De extensie C5-gegevensmigratie gebruiken | Microsoft Docs
description: Gebruik deze extensie om klanten, leveranciers, artikelen en grootboekrekeningen te migreren van Microsoft Dynamics C5 2012 naar Business Central.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: a10c05116e97cdf000bd46258a9d67f4c9910c90
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---

# <a name="the-c5-data-migration-extension"></a><span data-ttu-id="8fb3e-103">De extensie C5-gegevensmigratie</span><span class="sxs-lookup"><span data-stu-id="8fb3e-103">The C5 Data Migration Extension</span></span>
<span data-ttu-id="8fb3e-104">Deze extensie maakt het eenvoudidiger om klanten, leveranciers, artikelen en uw grootboekrekeningen van Microsoft Dynamics C5 2012 te migreren naar [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8fb3e-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="8fb3e-105">U kunt historische posten voor grootboekrekeningen ook migreren.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="8fb3e-106">Het bedrijf in [!INCLUDE[d365fin](includes/d365fin_md.md)] mag geen gegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="8fb3e-107">Bovendien mag u, nadat u een migratie start, geen klanten, leveranciers, artikelen of rekeningen maken totdat de migratie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="8fb3e-108">Welke gegevens worden gemigreerd?</span><span class="sxs-lookup"><span data-stu-id="8fb3e-108">What Data is Migrated?</span></span>
<span data-ttu-id="8fb3e-109">De volgende gegevens worden voor elke entiteit gemigreerd:</span><span class="sxs-lookup"><span data-stu-id="8fb3e-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="8fb3e-110">**Klanten**</span><span class="sxs-lookup"><span data-stu-id="8fb3e-110">**Customers**</span></span>
* <span data-ttu-id="8fb3e-111">Contacten</span><span class="sxs-lookup"><span data-stu-id="8fb3e-111">Contacts</span></span>  
* <span data-ttu-id="8fb3e-112">Vestiging</span><span class="sxs-lookup"><span data-stu-id="8fb3e-112">Location</span></span>
* <span data-ttu-id="8fb3e-113">Land</span><span class="sxs-lookup"><span data-stu-id="8fb3e-113">Country</span></span>
* <span data-ttu-id="8fb3e-114">Klantdimensies (afdeling, centrum, doel)</span><span class="sxs-lookup"><span data-stu-id="8fb3e-114">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="8fb3e-115">Verzendwijze</span><span class="sxs-lookup"><span data-stu-id="8fb3e-115">Shipment method</span></span>
* <span data-ttu-id="8fb3e-116">Verkoper</span><span class="sxs-lookup"><span data-stu-id="8fb3e-116">Sales Person</span></span>
* <span data-ttu-id="8fb3e-117">Betalingsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="8fb3e-117">Payment terms</span></span>
* <span data-ttu-id="8fb3e-118">Betalingswijze</span><span class="sxs-lookup"><span data-stu-id="8fb3e-118">Payment method</span></span>
* <span data-ttu-id="8fb3e-119">Klantenprijsgroep</span><span class="sxs-lookup"><span data-stu-id="8fb3e-119">Customer price group</span></span>
* <span data-ttu-id="8fb3e-120">Klantenfactuurkorting</span><span class="sxs-lookup"><span data-stu-id="8fb3e-120">Customer invoice discount</span></span>

<span data-ttu-id="8fb3e-121">Als u rekeningen migreert, worden de volgende gegevens ook gemigreerd:</span><span class="sxs-lookup"><span data-stu-id="8fb3e-121">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="8fb3e-122">Klantboekingsinstelling</span><span class="sxs-lookup"><span data-stu-id="8fb3e-122">Customer posting setup</span></span>
* <span data-ttu-id="8fb3e-123">Dagboekbatch</span><span class="sxs-lookup"><span data-stu-id="8fb3e-123">General journal batch</span></span>
* <span data-ttu-id="8fb3e-124">Open transacties (klantenposten)</span><span class="sxs-lookup"><span data-stu-id="8fb3e-124">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="8fb3e-125">**Leveranc.**</span><span class="sxs-lookup"><span data-stu-id="8fb3e-125">**Vendors**</span></span>
* <span data-ttu-id="8fb3e-126">Contacten</span><span class="sxs-lookup"><span data-stu-id="8fb3e-126">Contacts</span></span>
* <span data-ttu-id="8fb3e-127">Vestiging</span><span class="sxs-lookup"><span data-stu-id="8fb3e-127">Location</span></span>
* <span data-ttu-id="8fb3e-128">Land</span><span class="sxs-lookup"><span data-stu-id="8fb3e-128">Country</span></span>
* <span data-ttu-id="8fb3e-129">Leveranciersdimensies (afdeling, centrum, doel)</span><span class="sxs-lookup"><span data-stu-id="8fb3e-129">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="8fb3e-130">Factuurkorting</span><span class="sxs-lookup"><span data-stu-id="8fb3e-130">Invoice discount</span></span>
* <span data-ttu-id="8fb3e-131">Verzendwijze</span><span class="sxs-lookup"><span data-stu-id="8fb3e-131">Shipment method</span></span>
* <span data-ttu-id="8fb3e-132">Inkoper</span><span class="sxs-lookup"><span data-stu-id="8fb3e-132">Purchaser</span></span>
* <span data-ttu-id="8fb3e-133">Betalingsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="8fb3e-133">Payment terms</span></span>
* <span data-ttu-id="8fb3e-134">Betalingswijze</span><span class="sxs-lookup"><span data-stu-id="8fb3e-134">Payment method</span></span>
* <span data-ttu-id="8fb3e-135">Leveranciersfactuurkorting</span><span class="sxs-lookup"><span data-stu-id="8fb3e-135">Vendor invoice discount</span></span>

<span data-ttu-id="8fb3e-136">Als u rekeningen migreert, worden de volgende gegevens ook gemigreerd:</span><span class="sxs-lookup"><span data-stu-id="8fb3e-136">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="8fb3e-137">Leveranciersboekingsinstelling</span><span class="sxs-lookup"><span data-stu-id="8fb3e-137">Vendor posting setup</span></span>
* <span data-ttu-id="8fb3e-138">Dagboekbatch</span><span class="sxs-lookup"><span data-stu-id="8fb3e-138">General journal batch</span></span>
* <span data-ttu-id="8fb3e-139">Open transacties (leveranciersposten)</span><span class="sxs-lookup"><span data-stu-id="8fb3e-139">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="8fb3e-140">**Artikelen**</span><span class="sxs-lookup"><span data-stu-id="8fb3e-140">**Items**</span></span>
* <span data-ttu-id="8fb3e-141">Vestiging</span><span class="sxs-lookup"><span data-stu-id="8fb3e-141">Location</span></span>
* <span data-ttu-id="8fb3e-142">Land</span><span class="sxs-lookup"><span data-stu-id="8fb3e-142">Country</span></span>
* <span data-ttu-id="8fb3e-143">Artikeldimensies (afdeling, centrum, doel)</span><span class="sxs-lookup"><span data-stu-id="8fb3e-143">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="8fb3e-144">Verkoopregelkortingen</span><span class="sxs-lookup"><span data-stu-id="8fb3e-144">Sales line discounts</span></span>
* <span data-ttu-id="8fb3e-145">Klantenkortingsgroepen</span><span class="sxs-lookup"><span data-stu-id="8fb3e-145">Customer discount groups</span></span>
* <span data-ttu-id="8fb3e-146">Artikelkortingsgroepen</span><span class="sxs-lookup"><span data-stu-id="8fb3e-146">Item discount groups</span></span>
* <span data-ttu-id="8fb3e-147">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="8fb3e-147">Sales price</span></span>
* <span data-ttu-id="8fb3e-148">Tariefnummer</span><span class="sxs-lookup"><span data-stu-id="8fb3e-148">Tariff number</span></span>
* <span data-ttu-id="8fb3e-149">Maateenheden</span><span class="sxs-lookup"><span data-stu-id="8fb3e-149">Units of measure</span></span>
* <span data-ttu-id="8fb3e-150">Artikeltraceringscode</span><span class="sxs-lookup"><span data-stu-id="8fb3e-150">Item tracking code</span></span>
* <span data-ttu-id="8fb3e-151">Klantenprijsgroep</span><span class="sxs-lookup"><span data-stu-id="8fb3e-151">Customer price group</span></span>
* <span data-ttu-id="8fb3e-152">Assemblagestuklijsten</span><span class="sxs-lookup"><span data-stu-id="8fb3e-152">Assembly BOMs</span></span>

<span data-ttu-id="8fb3e-153">Als u rekeningen migreert, worden de volgende gegevens ook gemigreerd:</span><span class="sxs-lookup"><span data-stu-id="8fb3e-153">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="8fb3e-154">Voorraadboekingsinstelling</span><span class="sxs-lookup"><span data-stu-id="8fb3e-154">Inventory posting setup</span></span>
* <span data-ttu-id="8fb3e-155">Algemene boekingsinstelling</span><span class="sxs-lookup"><span data-stu-id="8fb3e-155">General posting setup</span></span>
* <span data-ttu-id="8fb3e-156">Artikeldagboekbatch</span><span class="sxs-lookup"><span data-stu-id="8fb3e-156">Item journal batch</span></span>
* <span data-ttu-id="8fb3e-157">Open transacties (artikelposten)</span><span class="sxs-lookup"><span data-stu-id="8fb3e-157">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="8fb3e-158">Als er open transacties zijn die vreemde valuta's gebruiken, wordt de wisselkoers voor deze valuta ook gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-158">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="8fb3e-159">Andere wisselkoersen worden niet gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-159">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="8fb3e-160">**Rekeningschema**</span><span class="sxs-lookup"><span data-stu-id="8fb3e-160">**Chart of Accounts**</span></span>  
* <span data-ttu-id="8fb3e-161">Standaarddimensies: afdeling, kostenplaats, doel</span><span class="sxs-lookup"><span data-stu-id="8fb3e-161">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="8fb3e-162">Historische G/L-transacties</span><span class="sxs-lookup"><span data-stu-id="8fb3e-162">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="8fb3e-163">Historische G/L-transacties worden iets anders behandeld.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-163">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="8fb3e-164">Wanneer u gegevens migreert, stelt u de parameter **Huidige periode** in.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-164">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="8fb3e-165">Deze parameter bepaalt hoe G/L-transacties worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-165">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="8fb3e-166">Transacties na deze datum worden afzonderlijk gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-166">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="8fb3e-167">Transacties vóór deze datum worden bijeengevoegd per rekening en als één bedrag gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-167">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="8fb3e-168">Stel dat er transacties zijn in 2015, 2016, 2017 en 2018, en dat u 1 januari 2017 opgeeft in het veld Huidige periode.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-168">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="8fb3e-169">Voor elke rekening worden bedragen voor transacties op of vóór 31 december 2106 in één dagboekregel gecombineerd voor elke grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-169">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="8fb3e-170">Alle transacties na deze datum worden afzonderlijk gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-170">All trascations after this date will be migrated individually.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="8fb3e-171">Gegevens te migreren</span><span class="sxs-lookup"><span data-stu-id="8fb3e-171">To migrate data</span></span>
<span data-ttu-id="8fb3e-172">Er zijn slechts enkele stappen nodig om gegevens vanuit C5 te exporteren en deze te importeren in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="8fb3e-172">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="8fb3e-173">Gebruik in C5 de functie **Database exporteren** om de gegevens te exporteren.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-173">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="8fb3e-174">Verzend vervolgens de exportmap naar een gecomprimeerde (gezipte) map.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-174">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="8fb3e-175">Kies in [!INCLUDE[d365fin](includes/d365fin_md.md)] het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gegevensmigratie** in en kies vervolgens **Gegevensmigratie**.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-175">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="8fb3e-176">Voer de stappen uit in het handleiding met begeleide instellingen.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-176">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="8fb3e-177">Zorg dat u **Importeren vanuit Microsoft Dynamics C5 2012** als gegevensbron kiest.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-177">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note]
> <span data-ttu-id="8fb3e-178">Bedrijven voegen vaak velden toe om C5 aan te passen aan de behoeften van hun specifieke branche.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-178">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="8fb3e-179">migreert geen gegevens van aangepaste velden.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-179">does not migrate data from custom fields.</span></span> <span data-ttu-id="8fb3e-180">Ook mislukt de migratie als u meer dan 10 aangepaste velden hebt.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-180">Also, migration will fail if you have more than 10 custom fields.</span></span>

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="8fb3e-181">De status van de migratie weergeven</span><span class="sxs-lookup"><span data-stu-id="8fb3e-181">Viewing the Status of the Migration</span></span>
<span data-ttu-id="8fb3e-182">Gebruik het venster **Overzicht van gegevensmigratie** om het resultaat van de migratie bekijken.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-182">Use the **Data Migration Overview** window to monitor the success of the migration.</span></span> <span data-ttu-id="8fb3e-183">De pagina bevat gegevens zoals het aantal entiteiten dat de migratie omvat, de status van de migratie, het aantal items dat is gemigreerd en of dat is gelukt.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-183">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="8fb3e-184">De pagina toont ook het aantal fouten, en stelt u in staat te onderzoeken wat er mis is gegaan. Ook bent u zo in staat om, indien mogelijk, gemakkelijk naar de entiteit gaan en de problemen op te lossen.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-184">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="8fb3e-185">Zie de volgende sectie in dit onderwerp voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-185">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="8fb3e-186">Terwijl u op de resultaten van de migratie wacht, moet u de pagina vernieuwen om de resultaten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-186">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="8fb3e-187">Dubbele boekingen voorkomen</span><span class="sxs-lookup"><span data-stu-id="8fb3e-187">How to Avoid Double-Posting</span></span>
<span data-ttu-id="8fb3e-188">Om dubbele boekingen te helpen voorkomen worden de volgende tegenrekeningen gebruikt voor open transacties:</span><span class="sxs-lookup"><span data-stu-id="8fb3e-188">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  

* <span data-ttu-id="8fb3e-189">Voor leveranciers wordt de leveranciersrekening uit de leveranciersboekingsgroep gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-189">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="8fb3e-190">Voor klanten wordt de klantenrekening uit de klantenboekingsgroep gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-190">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="8fb3e-191">Voor artikelen wordt een algemene boekingsinstelling gemaakt waarbij de correctierekening de rekening is die is opgegeven als de voorraadrekening in de voorraadboekingsinstelling.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-191">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="8fb3e-192">Fouten corrigeren</span><span class="sxs-lookup"><span data-stu-id="8fb3e-192">Correcting Errors</span></span>
<span data-ttu-id="8fb3e-193">Als er iets misgaat en zich een fout voordoet, wordt in het veld **Status** **Voltooid met fouten** weergegeven en in het veld **Aantal fouten** aangegeven hoeveel fouten er zijn.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-193">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="8fb3e-194">Als u een lijst met fouten wilt zien, kunt u het venster met de **Fouten met gegevensmigratie** openen door het volgende te kiezen:</span><span class="sxs-lookup"><span data-stu-id="8fb3e-194">To view a list of the errors, you can open the **Data Migration Errors** window by choosing:</span></span>  

* <span data-ttu-id="8fb3e-195">Het aantal in het veld **Aantal fouten** voor de entiteit.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-195">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="8fb3e-196">Op de entiteit en vervolgens op de actie **Fouten weergeven** te klikken.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-196">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="8fb3e-197">In het venster **Fouten met gegevensmigratie** kunt u een foutbericht kiezen om een fout op te lossen en vervolgens **Record bewerken** kiezen om de gemigreerde gegevens voor de entiteit weer te geven.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-197">In the **Data Migration Errors** window, to fix an error you can choose an error message, and then choose **Edit Record** to view the migrated data for the entity.</span></span> <span data-ttu-id="8fb3e-198">Als u meerdere fouten moet corrigeren, kunt u **Fouten bulksgewijs corrigeren** kiezen om de entiteiten in een lijst te bewerken.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-198">If you have several errors to fix, you can choose **Bulk-Fix Errors** to edit the entities in a list.</span></span> <span data-ttu-id="8fb3e-199">U moet echter nog afzonderlijke records openen als de fout is veroorzaakt door een gerelateerd item.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-199">You still need to open individual records if the error was caused by a related entry though.</span></span> <span data-ttu-id="8fb3e-200">Een leverancier wordt bijvoorbeeld niet gemigreerd als een e-mailadres van een van de contactpersonen een ongeldige indeling heeft.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-200">For example, a vendor will not be migrated if an email address one of their contacts has an invalid format.</span></span>

<span data-ttu-id="8fb3e-201">Nadat u een of meer fouten hebt opgelost, kunt u **Migreren** kiezen om alleen de entiteiten te migreren die u hebt hersteld, zonder dat u geheel op nieuw moet beginnen met de migratie.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-201">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="8fb3e-202">Als u meer dan één fout hebt verholpen, kunt u de functie **Meer selecteren** gebruiken om meerdere regels te selecteren om te migreren.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-202">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="8fb3e-203">Of u kunt fouten die niet noodzakelijkerwijs moeten worden opgelost, selecteren en vervolgens **Selecties overslaan** kiezen.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-203">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="8fb3e-204">Als u artikelen hebt die op een stuklijst zijn opgenomen, moet u mogelijk meer dan eens migreren als het oorspronkelijke artikel niet is gemaakt vóór de varianten die ernaar verwijzen..</span><span class="sxs-lookup"><span data-stu-id="8fb3e-204">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="8fb3e-205">Als een artikelvariant eerst is gemaakt, kan de verwijzing naar het oorspronkelijke artikel een foutbericht produceren.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-205">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="8fb3e-206">Het verifiëren van gegevens na de migratie</span><span class="sxs-lookup"><span data-stu-id="8fb3e-206">Verifying Data After Migrating</span></span>
<span data-ttu-id="8fb3e-207">Eén manier om te controleren of uw gegevens correct zijn gemigreerd is te kijken naar de volgende pagina's in C5 en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8fb3e-207">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="8fb3e-208">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="8fb3e-208">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="8fb3e-209">Te gebruiken batchverwerking</span><span class="sxs-lookup"><span data-stu-id="8fb3e-209">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="8fb3e-210">Klantenposten</span><span class="sxs-lookup"><span data-stu-id="8fb3e-210">Customer Entries</span></span>| <span data-ttu-id="8fb3e-211">Financiële dagboeken</span><span class="sxs-lookup"><span data-stu-id="8fb3e-211">General Journals</span></span>| <span data-ttu-id="8fb3e-212">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="8fb3e-212">CUSTMIGR</span></span> |
|<span data-ttu-id="8fb3e-213">Leveranciersposten</span><span class="sxs-lookup"><span data-stu-id="8fb3e-213">Vendor Entries</span></span>| <span data-ttu-id="8fb3e-214">Financiële dagboeken</span><span class="sxs-lookup"><span data-stu-id="8fb3e-214">General Journals</span></span>| <span data-ttu-id="8fb3e-215">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="8fb3e-215">VENDMIGR</span></span>|
|<span data-ttu-id="8fb3e-216">Artikelposten</span><span class="sxs-lookup"><span data-stu-id="8fb3e-216">Item Entries</span></span>| <span data-ttu-id="8fb3e-217">Artikeldagboeken</span><span class="sxs-lookup"><span data-stu-id="8fb3e-217">Item Journals</span></span>| <span data-ttu-id="8fb3e-218">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="8fb3e-218">ITEMMIGR</span></span> |
|<span data-ttu-id="8fb3e-219">Grootboekposten</span><span class="sxs-lookup"><span data-stu-id="8fb3e-219">G/L Entries</span></span>| <span data-ttu-id="8fb3e-220">Financiële dagboeken</span><span class="sxs-lookup"><span data-stu-id="8fb3e-220">General Journals</span></span>| <span data-ttu-id="8fb3e-221">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="8fb3e-221">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="8fb3e-222">De gegevensmigratie beëindigen</span><span class="sxs-lookup"><span data-stu-id="8fb3e-222">Stopping Data Migration</span></span>
<span data-ttu-id="8fb3e-223">U kunt de migratie van gegevens stoppen door **Alle migraties stoppen** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-223">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="8fb3e-224">Als u dat doet, worden alle wachtende migraties ook beëindigd.</span><span class="sxs-lookup"><span data-stu-id="8fb3e-224">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="8fb3e-225">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8fb3e-225">See Also</span></span>
<span data-ttu-id="8fb3e-226">[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="8fb3e-226">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="8fb3e-227">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="8fb3e-227">Getting Started</span></span>](product-get-started.md)

