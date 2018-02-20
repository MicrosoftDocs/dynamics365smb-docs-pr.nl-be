---
title: Excel gebruiken om gegevens in Financials te importeren | Microsoft Docs
description: Gebruik het standaardconfiguratiepakket om klantgegevens in Excel toe te voegen en vervolgens weer in Finance and Operations, Business edition te importeren.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 07/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: d6ef2eccb465afffb0f16ec9de1ceac9e9a4e3fc
ms.contentlocale: nl-be
ms.lasthandoff: 02/02/2018

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a><span data-ttu-id="90f29-103">Gegevens importeren uit oudere boekhoudsoftware door middel van een configuratiepakket.</span><span class="sxs-lookup"><span data-stu-id="90f29-103">Importing Data from Legacy Accounting Software using a Configuration Package</span></span>
<span data-ttu-id="90f29-104">U kunt gegevens en bepaalde transactiegegevens van andere financiële systemen importeren op basis van het standaardconfiguratiepakket in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="90f29-104">You can import master data and some transactional data from other finance systems based on the default configuration package in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="90f29-105">In het venster **Pakketten voor configuratie** kunt u met het pakket werken om de gegevens te importeren en te valideren voordat u het pakket toepast.</span><span class="sxs-lookup"><span data-stu-id="90f29-105">In the **Configuration Packages** window, you can work with the package to import and validate the data before you apply the package.</span></span>  

<span data-ttu-id="90f29-106">Als u vertrouwd bent met RapidStart-services voor Microsoft Dynamics, zijn configuratiezendingen ook bekend voor u.</span><span class="sxs-lookup"><span data-stu-id="90f29-106">If you are familiar with RapidStart Services for Microsoft Dynamics, you are also familiar with configuration packages.</span></span> <span data-ttu-id="90f29-107">Het standaardconfiguratiepakket ondersteunt de vaakst gebruikte soorten gegevens die u van een verouderd systeem wilt importeren.</span><span class="sxs-lookup"><span data-stu-id="90f29-107">The default configuration package supports the most common types of data that you want to import from a legacy system.</span></span> <span data-ttu-id="90f29-108">In Excel kunt u de gegevens vervolgens van het verouderde systeem toevoegen en instellen op basis van de bedrijfslogica van [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="90f29-108">In Excel, you can then add the data from the legacy system and set it up according to the business logic of the [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

> [!TIP]  
>   <span data-ttu-id="90f29-109">U kunt ook gegevensmigratiewizards gebruiken om gegevens in QuickBooks of Dynamics GP te importeren.</span><span class="sxs-lookup"><span data-stu-id="90f29-109">Alternatively, use data migration wizards to import data from QuickBooks or Dynamics GP.</span></span> <span data-ttu-id="90f29-110">Zie voor meer informatie [QuickBooks-gegevensmigratie](ui-extensions-quickbooks-data-migration.md) of [Dynamics GP-gegevensmigratie](ui-extensions-dynamicsgp-data-migration.md).</span><span class="sxs-lookup"><span data-stu-id="90f29-110">For more information, see [QuickBooks Data Migration](ui-extensions-quickbooks-data-migration.md) or [Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md).</span></span>  

## <a name="working-with-data-in-excel"></a><span data-ttu-id="90f29-111">Werken met gegevens in Excel</span><span class="sxs-lookup"><span data-stu-id="90f29-111">Working with Data in Excel</span></span>
<span data-ttu-id="90f29-112">Wanneer u het standaardconfiguratiepakket exporteert naar Excel, bevat de gegenereerde werkmap een werkblad voor elke tabel in het pakket.</span><span class="sxs-lookup"><span data-stu-id="90f29-112">When you export the default configuration package to Excel, the generated workbook contains a worksheet for each table in the package.</span></span> <span data-ttu-id="90f29-113">Om uw taken te vereenvoudigen, kunt u de XML-manipulatiehulpprogramma's gebruiken die in Excel zijn ingebouwd.</span><span class="sxs-lookup"><span data-stu-id="90f29-113">To simplify your tasks, you can take advantage of the XML manipulation tools that are built into Excel.</span></span> <span data-ttu-id="90f29-114">U kunt ook ingebouwde functies van Excel gebruiken om te helpen met het opmaken van gegevens en deze in de correcte cel te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="90f29-114">You can also use Excel built-in functions to help with data formatting and to put data in the correct cell.</span></span> <span data-ttu-id="90f29-115">Voeg bijvoorbeeld een werkblad toe en kopieer de verouderde gegevens naar het werkblad.</span><span class="sxs-lookup"><span data-stu-id="90f29-115">For example, add a blank worksheet and copy the legacy data to it.</span></span> <span data-ttu-id="90f29-116">Maak vervolgens een Excel-formule om gegevens in het transformatiewerkblad te koppelen met de velden in het geëxporteerde werkblad en de oude klantgegevens.</span><span class="sxs-lookup"><span data-stu-id="90f29-116">Then make an Excel formula to map data in the transformation worksheet between the fields in the exported worksheet and customer legacy data.</span></span> <span data-ttu-id="90f29-117">Nadat u alle gegevens hebt gekoppeld, kopieert u het gegevensbereik naar het werkblad met de tabel.</span><span class="sxs-lookup"><span data-stu-id="90f29-117">After you have mapped all of the data, copy the range of data onto the table worksheet.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="90f29-118">Wijzig de kolommen in de werkbladen niet.</span><span class="sxs-lookup"><span data-stu-id="90f29-118">Do not change the columns in the worksheets.</span></span> <span data-ttu-id="90f29-119">Als ze worden verplaatst, gewijzigd of verwijderd, kan het werkblad niet worden geïmporteerd in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="90f29-119">If they are moved, changed, or deleted, the worksheet cannot be imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="tables-in-the-default-configuration-package"></a><span data-ttu-id="90f29-120">Tabellen in het standaardconfiguratiepakket</span><span class="sxs-lookup"><span data-stu-id="90f29-120">Tables in the Default Configuration Package</span></span>
<span data-ttu-id="90f29-121">Het standaardconfiguratiepakket ondersteunt de volgende tabellen:</span><span class="sxs-lookup"><span data-stu-id="90f29-121">The default configuration package supports the following tables:</span></span>

-   <span data-ttu-id="90f29-122">Betalingsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="90f29-122">Payment Terms</span></span>
-   <span data-ttu-id="90f29-123">Klantenprijsgroep</span><span class="sxs-lookup"><span data-stu-id="90f29-123">Customer Price Group</span></span>
-   <span data-ttu-id="90f29-124">Verzendwijze</span><span class="sxs-lookup"><span data-stu-id="90f29-124">Shipment Method</span></span>
-   <span data-ttu-id="90f29-125">Verkoper/Inkoper</span><span class="sxs-lookup"><span data-stu-id="90f29-125">Salesperson/Purchaser</span></span>
-   <span data-ttu-id="90f29-126">Vestiging</span><span class="sxs-lookup"><span data-stu-id="90f29-126">Location</span></span>
-   <span data-ttu-id="90f29-127">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="90f29-127">GL Account</span></span>
-   <span data-ttu-id="90f29-128">Klant</span><span class="sxs-lookup"><span data-stu-id="90f29-128">Customer</span></span>
-   <span data-ttu-id="90f29-129">Leverancier</span><span class="sxs-lookup"><span data-stu-id="90f29-129">Vendor</span></span>
-   <span data-ttu-id="90f29-130">Artikel</span><span class="sxs-lookup"><span data-stu-id="90f29-130">Item</span></span>
-   <span data-ttu-id="90f29-131">Verkoopkop</span><span class="sxs-lookup"><span data-stu-id="90f29-131">Sales Header</span></span>
-   <span data-ttu-id="90f29-132">Verkoopregel</span><span class="sxs-lookup"><span data-stu-id="90f29-132">Sales Line</span></span>
-   <span data-ttu-id="90f29-133">Inkoopkop</span><span class="sxs-lookup"><span data-stu-id="90f29-133">Purchase Header</span></span>
-   <span data-ttu-id="90f29-134">Inkoopregel</span><span class="sxs-lookup"><span data-stu-id="90f29-134">Purchase Line</span></span>
-   <span data-ttu-id="90f29-135">Fin. dagboekregel</span><span class="sxs-lookup"><span data-stu-id="90f29-135">Gen. Journal Line</span></span>
-   <span data-ttu-id="90f29-136">Artikeldagboekregel</span><span class="sxs-lookup"><span data-stu-id="90f29-136">Item Journal Line</span></span>
-   <span data-ttu-id="90f29-137">Klantboekingsgroep</span><span class="sxs-lookup"><span data-stu-id="90f29-137">Customer Posting Group</span></span>
-   <span data-ttu-id="90f29-138">Leveranciersboekingsgroep</span><span class="sxs-lookup"><span data-stu-id="90f29-138">Vendor Posting Group</span></span>
-   <span data-ttu-id="90f29-139">Voorraadboekingsgroep</span><span class="sxs-lookup"><span data-stu-id="90f29-139">Inventory Posting Group</span></span>
-   <span data-ttu-id="90f29-140">Eenheid</span><span class="sxs-lookup"><span data-stu-id="90f29-140">Unit of Measure</span></span>
-   <span data-ttu-id="90f29-141">Bedrijfsboekingsgroep</span><span class="sxs-lookup"><span data-stu-id="90f29-141">Gen. Business Posting Group</span></span>
-   <span data-ttu-id="90f29-142">Productboekingsgroep</span><span class="sxs-lookup"><span data-stu-id="90f29-142">Gen. Product Posting Group</span></span>
-   <span data-ttu-id="90f29-143">Boekingsgroepinstellingen</span><span class="sxs-lookup"><span data-stu-id="90f29-143">General Posting Setup</span></span>
-   <span data-ttu-id="90f29-144">Regio</span><span class="sxs-lookup"><span data-stu-id="90f29-144">Territory</span></span>
-   <span data-ttu-id="90f29-145">Artikelcategorie</span><span class="sxs-lookup"><span data-stu-id="90f29-145">Item Category</span></span>
-   <span data-ttu-id="90f29-146">Verkoopprijs</span><span class="sxs-lookup"><span data-stu-id="90f29-146">Sales Price</span></span>
-   <span data-ttu-id="90f29-147">Inkoopprijs</span><span class="sxs-lookup"><span data-stu-id="90f29-147">Purchase Price</span></span>

## <a name="importing-customer-data"></a><span data-ttu-id="90f29-148">Klantgegevens importeren</span><span class="sxs-lookup"><span data-stu-id="90f29-148">Importing Customer Data</span></span>
<span data-ttu-id="90f29-149">Nadat de klantgegevens zijn ingevoerd in Excel, importeert u de gegevens in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="90f29-149">After the customer data has been entered in Excel, you import the data into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="90f29-150">In het venster **Pakketten voor configuratie** importeert u de gegevens van het Excel-bestand, en kunt u controleren of de gegevens consistent zijn met [!INCLUDE[d365fin](includes/d365fin_md.md)] voordat u het pakket toepast.</span><span class="sxs-lookup"><span data-stu-id="90f29-150">In the **Configuration Packages** window, you import the data from the Excel file, and you can validate that the data is consistent with [!INCLUDE[d365fin](includes/d365fin_md.md)] before you apply the package.</span></span>

## <a name="see-also"></a><span data-ttu-id="90f29-151">Zie ook</span><span class="sxs-lookup"><span data-stu-id="90f29-151">See Also</span></span>
[<span data-ttu-id="90f29-152">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="90f29-152">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
[<span data-ttu-id="90f29-153">QuickBooks-gegevensmigratie</span><span class="sxs-lookup"><span data-stu-id="90f29-153">QuickBooks Data Migration</span></span>](ui-extensions-quickbooks-data-migration.md)  
[<span data-ttu-id="90f29-154">Dynamics GP Data Migration</span><span class="sxs-lookup"><span data-stu-id="90f29-154">Dynamics GP Data Migration</span></span>](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

