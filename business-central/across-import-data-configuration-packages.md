---
title: Excel gebruiken om gegevens in Financials te importeren | Microsoft Docs
description: Gebruik het standaardconfiguratiepakket om klantgegevens in Excel toe te voegen en weer in Business Central te importeren.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4526e8b11c9cbae36c7db58259499fbfa1b0c243
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a><span data-ttu-id="9a7ae-103">Gegevens importeren uit oudere boekhoudsoftware door middel van een configuratiepakket.</span><span class="sxs-lookup"><span data-stu-id="9a7ae-103">Importing Data from Legacy Accounting Software using a Configuration Package</span></span>
<span data-ttu-id="9a7ae-104">U kunt gegevens en bepaalde transactiegegevens van andere financiële systemen importeren op basis van het standaardconfiguratiepakket in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9a7ae-104">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="9a7ae-105">In het venster **Pakketten voor configuratie** kunt u met het pakket werken om de gegevens te importeren en te valideren voordat u het pakket toepast.</span><span class="sxs-lookup"><span data-stu-id="9a7ae-105">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

> [!NOTE]  
> <span data-ttu-id="9a7ae-106">Voor groter implementatiewerk kunt u RapidStart Services voor [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken. Dat is een uitgebreide werkset voor het instellen van nieuwe oplossingen op basis van de bedrijfsvereisten en instellingsgegevens van de klant.</span><span class="sxs-lookup"><span data-stu-id="9a7ae-106">Configuration packages are part of RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], an extensive toolkit for setting up new solutions based on customers' business requirements and setup data.</span></span> <span data-ttu-id="9a7ae-107">RapidStart Services bieden ook functionaliteit voor het importeren van bedrijfsgegevens.</span><span class="sxs-lookup"><span data-stu-id="9a7ae-107">RapidStart Services also offers functionality for import of legacy data.</span></span> <span data-ttu-id="9a7ae-108">Zie voor meer informatie [Een bedrijf instellen met RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span><span class="sxs-lookup"><span data-stu-id="9a7ae-108">For more information, see [Setting Up a Company With RapidStart Services](admin-set-up-a-company-with-rapidstart.md).</span></span>

> [!TIP]  
>   <span data-ttu-id="9a7ae-109">U kunt ook gegevensmigratiewizards gebruiken om gegevens in QuickBooks of Dynamics GP te importeren.</span><span class="sxs-lookup"><span data-stu-id="9a7ae-109">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="9a7ae-110">Zie voor meer informatie [QuickBooks-gegevensmigratie](ui-extensions-quickbooks-data-migration.md) of [Dynamics GP-gegevensmigratie](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="9a7ae-110">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>  

## <a name="working-with-data-in-excel"></a><span data-ttu-id="9a7ae-111">Werken met gegevens in Excel</span><span class="sxs-lookup"><span data-stu-id="9a7ae-111">Working with Data in Excel</span></span>
<span data-ttu-id="9a7ae-112">Wanneer u het standaardconfiguratiepakket exporteert naar Excel, bevat de gegenereerde werkmap een werkblad voor elke tabel in het pakket.</span><span class="sxs-lookup"><span data-stu-id="9a7ae-112">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="9a7ae-113">Om uw taken te vereenvoudigen, kunt u de XML-manipulatiehulpprogramma's gebruiken die in Excel zijn ingebouwd.</span><span class="sxs-lookup"><span data-stu-id="9a7ae-113">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="9a7ae-114">U kunt ook ingebouwde functies van Excel gebruiken om te helpen met het opmaken van gegevens en deze in de correcte cel te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="9a7ae-114">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="9a7ae-115">Voeg bijvoorbeeld een werkblad toe en kopieer de verouderde gegevens naar het werkblad.</span><span class="sxs-lookup"><span data-stu-id="9a7ae-115">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="9a7ae-116">Maak vervolgens een Excel-formule om gegevens in het transformatiewerkblad te koppelen met de velden in het geëxporteerde werkblad en de oude klantgegevens.</span><span class="sxs-lookup"><span data-stu-id="9a7ae-116">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="9a7ae-117">Nadat u alle gegevens hebt gekoppeld, kopieert u het gegevensbereik naar het werkblad met de tabel.</span><span class="sxs-lookup"><span data-stu-id="9a7ae-117">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="9a7ae-118">Wijzig de kolommen in de werkbladen niet.</span><span class="sxs-lookup"><span data-stu-id="9a7ae-118">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="9a7ae-119">Als ze worden verplaatst, gewijzigd of verwijderd, kan het werkblad niet worden geïmporteerd in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9a7ae-119">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="9a7ae-120">Tabellen in het standaardconfiguratiepakket</span><span class="sxs-lookup"><span data-stu-id="9a7ae-120">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="9a7ae-121">Het standaardconfiguratiepakket ondersteunt de volgende tabellen:</span><span class="sxs-lookup"><span data-stu-id="9a7ae-121">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="9a7ae-122">Betalingsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="9a7ae-122">Payment Terms</span></span>
-   <span data-ttu-id="9a7ae-123">Klantenprijsgroep</span><span class="sxs-lookup"><span data-stu-id="9a7ae-123">Customer Price Group</span></span>
-   <span data-ttu-id="9a7ae-124">Verzendwijze</span><span class="sxs-lookup"><span data-stu-id="9a7ae-124">Shipment Method</span></span>
-   <span data-ttu-id="9a7ae-125">Verkoper/Inkoper</span><span class="sxs-lookup"><span data-stu-id="9a7ae-125">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="9a7ae-126">Vestiging</span><span class="sxs-lookup"><span data-stu-id="9a7ae-126">Location</span></span>
-   <span data-ttu-id="9a7ae-127">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="9a7ae-127">GL Account</span></span>
-   <span data-ttu-id="9a7ae-128">Klant</span><span class="sxs-lookup"><span data-stu-id="9a7ae-128">Customer</span></span>
-   <span data-ttu-id="9a7ae-129">Leverancier</span><span class="sxs-lookup"><span data-stu-id="9a7ae-129">Vendor</span></span>
-   <span data-ttu-id="9a7ae-130">Artikel</span><span class="sxs-lookup"><span data-stu-id="9a7ae-130">Item</span></span>
-   <span data-ttu-id="9a7ae-131">Verkoopkop</span><span class="sxs-lookup"><span data-stu-id="9a7ae-131">Sales Header</span></span>
-   <span data-ttu-id="9a7ae-132">Verkoopregel</span><span class="sxs-lookup"><span data-stu-id="9a7ae-132">Sales Line</span></span>
-   <span data-ttu-id="9a7ae-133">Inkoopkop</span><span class="sxs-lookup"><span data-stu-id="9a7ae-133">Purchase Header</span></span>
-   <span data-ttu-id="9a7ae-134">Inkoopregel</span><span class="sxs-lookup"><span data-stu-id="9a7ae-134">Purchase Line</span></span>
-   <span data-ttu-id="9a7ae-135">Fin. dagboekregel</span><span class="sxs-lookup"><span data-stu-id="9a7ae-135">Gen. Journal Line</span></span>
-   <span data-ttu-id="9a7ae-136">Artikeldagboekregel</span><span class="sxs-lookup"><span data-stu-id="9a7ae-136">Item Journal Line</span></span>
-   <span data-ttu-id="9a7ae-137">Klantboekingsgroep</span><span class="sxs-lookup"><span data-stu-id="9a7ae-137">Customer Posting Group</span></span>
-   <span data-ttu-id="9a7ae-138">Leveranciersboekingsgroep</span><span class="sxs-lookup"><span data-stu-id="9a7ae-138">Vendor Posting Group</span></span>
-   <span data-ttu-id="9a7ae-139">Voorraadboekingsgroep</span><span class="sxs-lookup"><span data-stu-id="9a7ae-139">Inventory Posting Group</span></span>
-   <span data-ttu-id="9a7ae-140">Eenheid</span><span class="sxs-lookup"><span data-stu-id="9a7ae-140">Unit of Measure</span></span>
-   <span data-ttu-id="9a7ae-141">Bedrijfsboekingsgroep</span><span class="sxs-lookup"><span data-stu-id="9a7ae-141">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="9a7ae-142">Productboekingsgroep</span><span class="sxs-lookup"><span data-stu-id="9a7ae-142">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="9a7ae-143">Boekingsgroepinstellingen</span><span class="sxs-lookup"><span data-stu-id="9a7ae-143">General Posting Setup</span></span>
-   <span data-ttu-id="9a7ae-144">Regio</span><span class="sxs-lookup"><span data-stu-id="9a7ae-144">Territory</span></span>
-   <span data-ttu-id="9a7ae-145">Artikelcategorie</span><span class="sxs-lookup"><span data-stu-id="9a7ae-145">Item Category</span></span>
-   <span data-ttu-id="9a7ae-146">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="9a7ae-146">Sales Price</span></span>
-   <span data-ttu-id="9a7ae-147">Inkoopprijs</span><span class="sxs-lookup"><span data-stu-id="9a7ae-147">Purchase Price</span></span>

## <a name="importing-customer-data"></a><span data-ttu-id="9a7ae-148">Klantgegevens importeren</span><span class="sxs-lookup"><span data-stu-id="9a7ae-148">Importing Customer Data</span></span>
<span data-ttu-id="9a7ae-149">Nadat de klantgegevens zijn ingevoerd in Excel, importeert u de gegevens in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9a7ae-149">After the customer data has been entered in Excel, you import the data into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="9a7ae-150">In het venster **Pakketten voor configuratie** importeert u de gegevens van het Excel-bestand, en kunt u controleren of de gegevens consistent zijn met [!INCLUDE[d365fin](includes/d365fin_md.md)] voordat u het pakket toepast.</span><span class="sxs-lookup"><span data-stu-id="9a7ae-150">In the **Configuration Packages** window, you import the data from the Excel file, and you can validate that the data is consistent with [!INCLUDE[d365fin](includes/d365fin_md.md)] before you apply the package.</span></span>

## <a name="see-also"></a><span data-ttu-id="9a7ae-151">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9a7ae-151">See Also</span></span>
[<span data-ttu-id="9a7ae-152">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="9a7ae-152">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="9a7ae-153">Een bedrijf met RapidStart Services instellen</span><span class="sxs-lookup"><span data-stu-id="9a7ae-153">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="9a7ae-154">QuickBooks-gegevensmigratie</span><span class="sxs-lookup"><span data-stu-id="9a7ae-154">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="9a7ae-155">Dynamics GP-gegevensmigratie</span><span class="sxs-lookup"><span data-stu-id="9a7ae-155">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

