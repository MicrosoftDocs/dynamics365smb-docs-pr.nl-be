---
title: De extensie C5-gegevensmigratie gebruiken | Microsoft Docs
description: Gebruik deze extensie om klanten, leveranciers, artikelen en grootboekrekeningen te migreren van Microsoft Dynamics C5 2012 naar Business Central.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: cdf14002e28b777441a803fc7804fdac8afe5b77
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194343"
---
# <a name="the-c5-data-migration-extension"></a><span data-ttu-id="5d844-103">De extensie C5-gegevensmigratie</span><span class="sxs-lookup"><span data-stu-id="5d844-103">The C5 Data Migration Extension</span></span>
<span data-ttu-id="5d844-104">Deze extensie maakt het eenvoudidiger om klanten, leveranciers, artikelen en uw grootboekrekeningen van Microsoft Dynamics C5 2012 te migreren naar [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5d844-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="5d844-105">U kunt historische posten voor grootboekrekeningen ook migreren.</span><span class="sxs-lookup"><span data-stu-id="5d844-105">You can also migrate historical entries for general ledger accounts.</span></span>

> [!Note]
> <span data-ttu-id="5d844-106">Het bedrijf in [!INCLUDE[d365fin](includes/d365fin_md.md)] mag geen gegevens bevatten.</span><span class="sxs-lookup"><span data-stu-id="5d844-106">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="5d844-107">Bovendien mag u, nadat u een migratie start, geen klanten, leveranciers, artikelen of rekeningen maken totdat de migratie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="5d844-107">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="what-data-is-migrated"></a><span data-ttu-id="5d844-108">Welke gegevens worden gemigreerd?</span><span class="sxs-lookup"><span data-stu-id="5d844-108">What Data is Migrated?</span></span>
<span data-ttu-id="5d844-109">De volgende gegevens worden voor elke entiteit gemigreerd:</span><span class="sxs-lookup"><span data-stu-id="5d844-109">The following data is migrated for each entity:</span></span>

<span data-ttu-id="5d844-110">**Klanten**</span><span class="sxs-lookup"><span data-stu-id="5d844-110">**Customers**</span></span>
* <span data-ttu-id="5d844-111">Contacten</span><span class="sxs-lookup"><span data-stu-id="5d844-111">Contacts</span></span>  
* <span data-ttu-id="5d844-112">Vestiging</span><span class="sxs-lookup"><span data-stu-id="5d844-112">Location</span></span>
* <span data-ttu-id="5d844-113">Land</span><span class="sxs-lookup"><span data-stu-id="5d844-113">Country</span></span>
* <span data-ttu-id="5d844-114">Klantdimensies (afdeling, centrum, doel)</span><span class="sxs-lookup"><span data-stu-id="5d844-114">Customer dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="5d844-115">Verzendwijze</span><span class="sxs-lookup"><span data-stu-id="5d844-115">Shipment method</span></span>
* <span data-ttu-id="5d844-116">Verkoper</span><span class="sxs-lookup"><span data-stu-id="5d844-116">Sales Person</span></span>
* <span data-ttu-id="5d844-117">Betalingsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="5d844-117">Payment terms</span></span>
* <span data-ttu-id="5d844-118">Betalingswijze</span><span class="sxs-lookup"><span data-stu-id="5d844-118">Payment method</span></span>
* <span data-ttu-id="5d844-119">Klantenprijsgroep</span><span class="sxs-lookup"><span data-stu-id="5d844-119">Customer price group</span></span>
* <span data-ttu-id="5d844-120">Klantenfactuurkorting</span><span class="sxs-lookup"><span data-stu-id="5d844-120">Customer invoice discount</span></span>

<span data-ttu-id="5d844-121">Als u rekeningen migreert, worden de volgende gegevens ook gemigreerd:</span><span class="sxs-lookup"><span data-stu-id="5d844-121">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="5d844-122">Klantboekingsinstelling</span><span class="sxs-lookup"><span data-stu-id="5d844-122">Customer posting setup</span></span>
* <span data-ttu-id="5d844-123">Dagboekbatch</span><span class="sxs-lookup"><span data-stu-id="5d844-123">General journal batch</span></span>
* <span data-ttu-id="5d844-124">Open transacties (klantenposten)</span><span class="sxs-lookup"><span data-stu-id="5d844-124">Open transactions (customer ledger entries)</span></span>

<span data-ttu-id="5d844-125">**Leveranc.**</span><span class="sxs-lookup"><span data-stu-id="5d844-125">**Vendors**</span></span>
* <span data-ttu-id="5d844-126">Contacten</span><span class="sxs-lookup"><span data-stu-id="5d844-126">Contacts</span></span>
* <span data-ttu-id="5d844-127">Vestiging</span><span class="sxs-lookup"><span data-stu-id="5d844-127">Location</span></span>
* <span data-ttu-id="5d844-128">Land</span><span class="sxs-lookup"><span data-stu-id="5d844-128">Country</span></span>
* <span data-ttu-id="5d844-129">Leveranciersdimensies (afdeling, centrum, doel)</span><span class="sxs-lookup"><span data-stu-id="5d844-129">Vendor dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="5d844-130">Factuurkorting</span><span class="sxs-lookup"><span data-stu-id="5d844-130">Invoice discount</span></span>
* <span data-ttu-id="5d844-131">Verzendwijze</span><span class="sxs-lookup"><span data-stu-id="5d844-131">Shipment method</span></span>
* <span data-ttu-id="5d844-132">Inkoper</span><span class="sxs-lookup"><span data-stu-id="5d844-132">Purchaser</span></span>
* <span data-ttu-id="5d844-133">Betalingsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="5d844-133">Payment terms</span></span>
* <span data-ttu-id="5d844-134">Betalingswijze</span><span class="sxs-lookup"><span data-stu-id="5d844-134">Payment method</span></span>
* <span data-ttu-id="5d844-135">Leveranciersfactuurkorting</span><span class="sxs-lookup"><span data-stu-id="5d844-135">Vendor invoice discount</span></span>

<span data-ttu-id="5d844-136">Als u rekeningen migreert, worden de volgende gegevens ook gemigreerd:</span><span class="sxs-lookup"><span data-stu-id="5d844-136">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="5d844-137">Leveranciersboekingsinstelling</span><span class="sxs-lookup"><span data-stu-id="5d844-137">Vendor posting setup</span></span>
* <span data-ttu-id="5d844-138">Dagboekbatch</span><span class="sxs-lookup"><span data-stu-id="5d844-138">General journal batch</span></span>
* <span data-ttu-id="5d844-139">Open transacties (leveranciersposten)</span><span class="sxs-lookup"><span data-stu-id="5d844-139">Open transactions (vendor ledger entries)</span></span>

<span data-ttu-id="5d844-140">**Artikelen**</span><span class="sxs-lookup"><span data-stu-id="5d844-140">**Items**</span></span>
* <span data-ttu-id="5d844-141">Vestiging</span><span class="sxs-lookup"><span data-stu-id="5d844-141">Location</span></span>
* <span data-ttu-id="5d844-142">Land</span><span class="sxs-lookup"><span data-stu-id="5d844-142">Country</span></span>
* <span data-ttu-id="5d844-143">Artikeldimensies (afdeling, centrum, doel)</span><span class="sxs-lookup"><span data-stu-id="5d844-143">Item dimensions (department, center, purpose)</span></span>
* <span data-ttu-id="5d844-144">Verkoopregelkortingen</span><span class="sxs-lookup"><span data-stu-id="5d844-144">Sales line discounts</span></span>
* <span data-ttu-id="5d844-145">Klantenkortingsgroepen</span><span class="sxs-lookup"><span data-stu-id="5d844-145">Customer discount groups</span></span>
* <span data-ttu-id="5d844-146">Artikelkortingsgroepen</span><span class="sxs-lookup"><span data-stu-id="5d844-146">Item discount groups</span></span>
* <span data-ttu-id="5d844-147">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="5d844-147">Sales price</span></span>
* <span data-ttu-id="5d844-148">Tariefnummer</span><span class="sxs-lookup"><span data-stu-id="5d844-148">Tariff number</span></span>
* <span data-ttu-id="5d844-149">Maateenheden</span><span class="sxs-lookup"><span data-stu-id="5d844-149">Units of measure</span></span>
* <span data-ttu-id="5d844-150">Artikeltraceringscode</span><span class="sxs-lookup"><span data-stu-id="5d844-150">Item tracking code</span></span>
* <span data-ttu-id="5d844-151">Klantenprijsgroep</span><span class="sxs-lookup"><span data-stu-id="5d844-151">Customer price group</span></span>
* <span data-ttu-id="5d844-152">Assemblagestuklijsten</span><span class="sxs-lookup"><span data-stu-id="5d844-152">Assembly BOMs</span></span>

<span data-ttu-id="5d844-153">Als u rekeningen migreert, worden de volgende gegevens ook gemigreerd:</span><span class="sxs-lookup"><span data-stu-id="5d844-153">If you migrate accounts, the following data is also migrated:</span></span>

* <span data-ttu-id="5d844-154">Voorraadboekingsinstelling</span><span class="sxs-lookup"><span data-stu-id="5d844-154">Inventory posting setup</span></span>
* <span data-ttu-id="5d844-155">Algemene boekingsinstelling</span><span class="sxs-lookup"><span data-stu-id="5d844-155">General posting setup</span></span>
* <span data-ttu-id="5d844-156">Artikeldagboekbatch</span><span class="sxs-lookup"><span data-stu-id="5d844-156">Item journal batch</span></span>
* <span data-ttu-id="5d844-157">Open transacties (artikelposten)</span><span class="sxs-lookup"><span data-stu-id="5d844-157">Open transactions (item ledger entries)</span></span>

> [!Note]
> <span data-ttu-id="5d844-158">Als er open transacties zijn die vreemde valuta's gebruiken, wordt de wisselkoers voor deze valuta ook gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="5d844-158">If there are open transactions that use foreign currencies, the exchange rates for those currencies are also migrated.</span></span> <span data-ttu-id="5d844-159">Andere wisselkoersen worden niet gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="5d844-159">Other exchange rates are not migrated.</span></span>

<span data-ttu-id="5d844-160">**Rekeningschema**</span><span class="sxs-lookup"><span data-stu-id="5d844-160">**Chart of Accounts**</span></span>  
* <span data-ttu-id="5d844-161">Standaarddimensies: afdeling, kostenplaats, doel</span><span class="sxs-lookup"><span data-stu-id="5d844-161">Standard dimensions: Department, Cost Center, Purpose</span></span>  
* <span data-ttu-id="5d844-162">Historische G/L-transacties</span><span class="sxs-lookup"><span data-stu-id="5d844-162">Historical G/L transactions</span></span>  

> [!Note]
> <span data-ttu-id="5d844-163">Historische G/L-transacties worden iets anders behandeld.</span><span class="sxs-lookup"><span data-stu-id="5d844-163">Historical G/L transactions are treated a little differently.</span></span> <span data-ttu-id="5d844-164">Wanneer u gegevens migreert, stelt u de parameter **Huidige periode** in.</span><span class="sxs-lookup"><span data-stu-id="5d844-164">When you migrate data you set a **Current Period** parameter.</span></span> <span data-ttu-id="5d844-165">Deze parameter bepaalt hoe G/L-transacties worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="5d844-165">This parameter specifies how to process G/L transactions.</span></span> <span data-ttu-id="5d844-166">Transacties na deze datum worden afzonderlijk gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="5d844-166">Transactions after this date are migrated individually.</span></span> <span data-ttu-id="5d844-167">Transacties vóór deze datum worden bijeengevoegd per rekening en als één bedrag gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="5d844-167">Transactions before this date are aggregated per account and migrated as a single amount.</span></span> <span data-ttu-id="5d844-168">Stel dat er transacties zijn in 2015, 2016, 2017 en 2018, en dat u 1 januari 2017 opgeeft in het veld Huidige periode.</span><span class="sxs-lookup"><span data-stu-id="5d844-168">For example, let's say there are transactions in 2015, 2016, 2017, 2018, and you specify January 01, 2017 in the Current Period field.</span></span> <span data-ttu-id="5d844-169">Voor elke rekening worden bedragen voor transacties op of vóór 31 december 2106 in één dagboekregel gecombineerd voor elke grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="5d844-169">For each account, amounts for transactions on or before December 31, 2106, will be aggregated in a single general journal line for each G/L account.</span></span> <span data-ttu-id="5d844-170">Alle transacties na deze datum worden afzonderlijk gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="5d844-170">All trascations after this date will be migrated individually.</span></span>

## <a name="file-size-requirements"></a><span data-ttu-id="5d844-171">Vereisten voor bestandsgrootte</span><span class="sxs-lookup"><span data-stu-id="5d844-171">File Size Requirements</span></span>
<span data-ttu-id="5d844-172">Het grootste bestand dat u kunt uploaden naar [!INCLUDE[d365fin](includes/d365fin_md.md)] is 150 MB.</span><span class="sxs-lookup"><span data-stu-id="5d844-172">The largest file size you can upload to [!INCLUDE[d365fin](includes/d365fin_md.md)] is 150 MB.</span></span> <span data-ttu-id="5d844-173">Als het bestand dat u uit C5 exporteert, groter is, overweeg dan gegevens in meerdere bestanden te migreren.</span><span class="sxs-lookup"><span data-stu-id="5d844-173">If the file you export from C5 is larger than that, consider migrating data in multiple files.</span></span> <span data-ttu-id="5d844-174">Exporteer bijvoorbeeld een of twee typen entiteiten uit C5, zoals klanten en leveranciers, naar een bestand en exporteer artikelen naar een ander bestand, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="5d844-174">For example, export one or two types of entities from C5, such as customers and vendors, to a file, and then export items to another file, and so on.</span></span> <span data-ttu-id="5d844-175">U kunt afzonderlijke bestanden importeren in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5d844-175">You can import files individually in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="5d844-176">Gegevens te migreren</span><span class="sxs-lookup"><span data-stu-id="5d844-176">To migrate data</span></span>
<span data-ttu-id="5d844-177">Er zijn slechts enkele stappen nodig om gegevens vanuit C5 te exporteren en deze te importeren in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="5d844-177">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

1. <span data-ttu-id="5d844-178">Gebruik in C5 de functie **Database exporteren** om de gegevens te exporteren.</span><span class="sxs-lookup"><span data-stu-id="5d844-178">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="5d844-179">Verzend vervolgens de exportmap naar een gecomprimeerde (gezipte) map.</span><span class="sxs-lookup"><span data-stu-id="5d844-179">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="5d844-180">Kies in [!INCLUDE[d365fin](includes/d365fin_md.md)] het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gegevensmigratie** in en kies vervolgens **Gegevensmigratie**.</span><span class="sxs-lookup"><span data-stu-id="5d844-180">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="5d844-181">Voer de stappen uit in het handleiding met begeleide instellingen.</span><span class="sxs-lookup"><span data-stu-id="5d844-181">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="5d844-182">Zorg dat u **Importeren vanuit Microsoft Dynamics C5 2012** als gegevensbron kiest.</span><span class="sxs-lookup"><span data-stu-id="5d844-182">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="5d844-183">De status van de migratie weergeven</span><span class="sxs-lookup"><span data-stu-id="5d844-183">Viewing the Status of the Migration</span></span>
<span data-ttu-id="5d844-184">Gebruik de pagina **Gegevensmigratieoverzicht** om het resultaat van de migratie bekijken.</span><span class="sxs-lookup"><span data-stu-id="5d844-184">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="5d844-185">De pagina bevat gegevens zoals het aantal entiteiten dat de migratie omvat, de status van de migratie, het aantal items dat is gemigreerd en of dat is gelukt.</span><span class="sxs-lookup"><span data-stu-id="5d844-185">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="5d844-186">De pagina toont ook het aantal fouten, en stelt u in staat te onderzoeken wat er mis is gegaan. Ook bent u zo in staat om, indien mogelijk, gemakkelijk naar de entiteit gaan en de problemen op te lossen.</span><span class="sxs-lookup"><span data-stu-id="5d844-186">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="5d844-187">Zie de volgende sectie in dit onderwerp voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="5d844-187">For more information, see the next section in this topic.</span></span>  

> [!Note]
> <span data-ttu-id="5d844-188">Terwijl u op de resultaten van de migratie wacht, moet u de pagina vernieuwen om de resultaten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="5d844-188">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="how-to-avoid-double-posting"></a><span data-ttu-id="5d844-189">Dubbele boekingen voorkomen</span><span class="sxs-lookup"><span data-stu-id="5d844-189">How to Avoid Double-Posting</span></span>
<span data-ttu-id="5d844-190">Om dubbele boekingen te helpen voorkomen worden de volgende tegenrekeningen gebruikt voor open transacties:</span><span class="sxs-lookup"><span data-stu-id="5d844-190">To help avoid double-posting to the general ledger, the following balance accounts are used for open transactions:</span></span>  

* <span data-ttu-id="5d844-191">Voor leveranciers wordt de leveranciersrekening uit de leveranciersboekingsgroep gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5d844-191">For vendors, we use the A/P account from the vendor posting group.</span></span>  
* <span data-ttu-id="5d844-192">Voor klanten wordt de klantenrekening uit de klantenboekingsgroep gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5d844-192">For customers, we use the A/R account from the customer posting group.</span></span>  
* <span data-ttu-id="5d844-193">Voor artikelen wordt een algemene boekingsinstelling gemaakt waarbij de correctierekening de rekening is die is opgegeven als de voorraadrekening in de voorraadboekingsinstelling.</span><span class="sxs-lookup"><span data-stu-id="5d844-193">For items, we create a general posting setup where the adjustment account is the account specified as the inventory account on the inventory posting setup.</span></span>  

## <a name="correcting-errors"></a><span data-ttu-id="5d844-194">Fouten corrigeren</span><span class="sxs-lookup"><span data-stu-id="5d844-194">Correcting Errors</span></span>
<span data-ttu-id="5d844-195">Als er iets misgaat en zich een fout voordoet, wordt in het veld **Status** **Voltooid met fouten** weergegeven en in het veld **Aantal fouten** aangegeven hoeveel fouten er zijn.</span><span class="sxs-lookup"><span data-stu-id="5d844-195">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="5d844-196">Als u een lijst met fouten wilt zien, kunt u de pagina met de **gegevensmigratiefouten** openen door het volgende te selecteren:</span><span class="sxs-lookup"><span data-stu-id="5d844-196">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>  

* <span data-ttu-id="5d844-197">Het aantal in het veld **Aantal fouten** voor de entiteit.</span><span class="sxs-lookup"><span data-stu-id="5d844-197">The number in the **Error Count** field for the entity.</span></span>  
* <span data-ttu-id="5d844-198">Op de entiteit en vervolgens op de actie **Fouten weergeven** te klikken.</span><span class="sxs-lookup"><span data-stu-id="5d844-198">The entity, and then the **Show Errors** action.</span></span>  

<span data-ttu-id="5d844-199">Op de pagina **Fouten met gegevensmigratie** kunt u een foutbericht kiezen om een fout op te lossen en vervolgens **Record bewerken** kiezen om de gemigreerde gegevens voor de entiteit weer te geven.</span><span class="sxs-lookup"><span data-stu-id="5d844-199">On the **Data Migration Errors** page, to fix an error you can choose an error message, and then choose **Edit Record** to view the migrated data for the entity.</span></span> <span data-ttu-id="5d844-200">Als u meerdere fouten moet corrigeren, kunt u **Fouten bulksgewijs corrigeren** kiezen om de entiteiten in een lijst te bewerken.</span><span class="sxs-lookup"><span data-stu-id="5d844-200">If you have several errors to fix, you can choose **Bulk-Fix Errors** to edit the entities in a list.</span></span> <span data-ttu-id="5d844-201">U moet echter nog afzonderlijke records openen als de fout is veroorzaakt door een gerelateerd item.</span><span class="sxs-lookup"><span data-stu-id="5d844-201">You still need to open individual records if the error was caused by a related entry though.</span></span> <span data-ttu-id="5d844-202">Een leverancier wordt bijvoorbeeld niet gemigreerd als een e-mailadres van een van de contactpersonen een ongeldige indeling heeft.</span><span class="sxs-lookup"><span data-stu-id="5d844-202">For example, a vendor will not be migrated if an email address one of their contacts has an invalid format.</span></span>

<span data-ttu-id="5d844-203">Nadat u een of meer fouten hebt opgelost, kunt u **Migreren** kiezen om alleen de entiteiten te migreren die u hebt hersteld, zonder dat u geheel op nieuw moet beginnen met de migratie.</span><span class="sxs-lookup"><span data-stu-id="5d844-203">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="5d844-204">Als u meer dan één fout hebt verholpen, kunt u de functie **Meer selecteren** gebruiken om meerdere regels te selecteren om te migreren.</span><span class="sxs-lookup"><span data-stu-id="5d844-204">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="5d844-205">Of u kunt fouten die niet noodzakelijkerwijs moeten worden opgelost, selecteren en vervolgens **Selecties overslaan** kiezen.</span><span class="sxs-lookup"><span data-stu-id="5d844-205">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="5d844-206">Als u artikelen hebt die op een stuklijst zijn opgenomen, moet u mogelijk meer dan eens migreren als het oorspronkelijke artikel niet is gemaakt vóór de varianten die ernaar verwijzen..</span><span class="sxs-lookup"><span data-stu-id="5d844-206">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="5d844-207">Als een artikelvariant eerst is gemaakt, kan de verwijzing naar het oorspronkelijke artikel een foutbericht produceren.</span><span class="sxs-lookup"><span data-stu-id="5d844-207">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="5d844-208">Het verifiëren van gegevens na de migratie</span><span class="sxs-lookup"><span data-stu-id="5d844-208">Verifying Data After Migrating</span></span>
<span data-ttu-id="5d844-209">Eén manier om te controleren of uw gegevens correct zijn gemigreerd is te kijken naar de volgende pagina's in C5 en [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5d844-209">One way to verify that your data migrated correctly is to look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="5d844-210">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="5d844-210">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]| <span data-ttu-id="5d844-211">Te gebruiken batchverwerking</span><span class="sxs-lookup"><span data-stu-id="5d844-211">Batch Job to Use</span></span> |
|-----|-----|-----|
|<span data-ttu-id="5d844-212">Klantenposten</span><span class="sxs-lookup"><span data-stu-id="5d844-212">Customer Entries</span></span>| <span data-ttu-id="5d844-213">Financiële dagboeken</span><span class="sxs-lookup"><span data-stu-id="5d844-213">General Journals</span></span>| <span data-ttu-id="5d844-214">CUSTMIGR</span><span class="sxs-lookup"><span data-stu-id="5d844-214">CUSTMIGR</span></span> |
|<span data-ttu-id="5d844-215">Leveranciersposten</span><span class="sxs-lookup"><span data-stu-id="5d844-215">Vendor Entries</span></span>| <span data-ttu-id="5d844-216">Financiële dagboeken</span><span class="sxs-lookup"><span data-stu-id="5d844-216">General Journals</span></span>| <span data-ttu-id="5d844-217">VENDMIGR</span><span class="sxs-lookup"><span data-stu-id="5d844-217">VENDMIGR</span></span>|
|<span data-ttu-id="5d844-218">Artikelposten</span><span class="sxs-lookup"><span data-stu-id="5d844-218">Item Entries</span></span>| <span data-ttu-id="5d844-219">Artikeldagboeken</span><span class="sxs-lookup"><span data-stu-id="5d844-219">Item Journals</span></span>| <span data-ttu-id="5d844-220">ITEMMIGR</span><span class="sxs-lookup"><span data-stu-id="5d844-220">ITEMMIGR</span></span> |
|<span data-ttu-id="5d844-221">Grootboekposten</span><span class="sxs-lookup"><span data-stu-id="5d844-221">G/L Entries</span></span>| <span data-ttu-id="5d844-222">Financiële dagboeken</span><span class="sxs-lookup"><span data-stu-id="5d844-222">General Journals</span></span>| <span data-ttu-id="5d844-223">GLACMIGR</span><span class="sxs-lookup"><span data-stu-id="5d844-223">GLACMIGR</span></span> |

## <a name="stopping-data-migration"></a><span data-ttu-id="5d844-224">De gegevensmigratie beëindigen</span><span class="sxs-lookup"><span data-stu-id="5d844-224">Stopping Data Migration</span></span>
<span data-ttu-id="5d844-225">U kunt de migratie van gegevens stoppen door **Alle migraties stoppen** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="5d844-225">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="5d844-226">Als u dat doet, worden alle wachtende migraties ook beëindigd.</span><span class="sxs-lookup"><span data-stu-id="5d844-226">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d844-227">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5d844-227">See Also</span></span>
<span data-ttu-id="5d844-228">[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="5d844-228">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="5d844-229">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="5d844-229">Getting Started</span></span>](product-get-started.md)
