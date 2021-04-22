---
title: Een nieuw bedrijf maken | Microsoft Docs
description: Om RapidStart Services te kunnen gebruiken worden tabellen en pagina's gemaakt, maar ze bevatten geen gegevens.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c21d86c67c6020d1a32da4816246bc7aaf96c2ca
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779894"
---
# <a name="create-a-new-company"></a><span data-ttu-id="f24cf-103">Een nieuw bedrijf maken</span><span class="sxs-lookup"><span data-stu-id="f24cf-103">Create a New Company</span></span>
<span data-ttu-id="f24cf-104">Als u RapidStart Services voor [!INCLUDE[prod_short](includes/prod_short.md)] wilt gebruiken, maakt u eerst een nieuw bedrijf waarvoor u een klantimplementatie wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="f24cf-104">To use RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], you first create a new company for which you want to perform a customer implementation.</span></span> <span data-ttu-id="f24cf-105">Bij het maken van een nieuw bedrijf worden de standaard [!INCLUDE[prod_short](includes/prod_short.md)]-tabellen en pagina's gemaakt, maar deze zijn leeg.</span><span class="sxs-lookup"><span data-stu-id="f24cf-105">When you create a new company, the standard [!INCLUDE[prod_short](includes/prod_short.md)] tables and pages are created, but there is no data in them.</span></span>

<span data-ttu-id="f24cf-106">Bovendien kunt u specifieke instellingsgegevens op uw bedrijf toepassen nadat u het hebt geïnitialiseerd.</span><span class="sxs-lookup"><span data-stu-id="f24cf-106">In addition, you can apply specific setup data to your company after you initialize it.</span></span> <span data-ttu-id="f24cf-107">Deze gegevens worden in een configuratiepakket (een .rapidstart-bestand) verstrekt welke de inhoud in een gecomprimeerde indeling levert.</span><span class="sxs-lookup"><span data-stu-id="f24cf-107">The information is provided in a configuration package, a .rapidstart file, which delivers content in a compressed format.</span></span>  

<span data-ttu-id="f24cf-108">Voorbeeldconfiguratiepakketten, inclusief land-/regiospecifieke bestanden, zijn opgenomen bij het demonstratiebedrijf CRONUS.</span><span class="sxs-lookup"><span data-stu-id="f24cf-108">Example configuration packages, including country/region-specific files, are included with the CRONUS demonstration company.</span></span> <span data-ttu-id="f24cf-109">Gebruik de volgende procedures om het voorbeeldconfiguratiepakket met een nieuw bedrijf te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f24cf-109">Use the following procedures to use the example configuration package with a new company.</span></span>  

## <a name="to-use-the-sample-basicconfig-configuration-package"></a><span data-ttu-id="f24cf-110">Het voorbeeldconfiguratiepakket BASICCONFIG gebruiken</span><span class="sxs-lookup"><span data-stu-id="f24cf-110">To use the sample BASICCONFIG configuration package</span></span>  
1. <span data-ttu-id="f24cf-111">Open het bedrijf CRONUS International Ltd.</span><span class="sxs-lookup"><span data-stu-id="f24cf-111">Open the CRONUS International Ltd. company.</span></span> <span data-ttu-id="f24cf-112">Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="f24cf-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>
2. <span data-ttu-id="f24cf-113">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratiepakketten** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="f24cf-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Configuration Packages**, and then choose the related link.</span></span>  
3. <span data-ttu-id="f24cf-114">Kies het pakket BASICCONFIG in de lijst en kies vervolgens de actie **Pakket exporteren**.</span><span class="sxs-lookup"><span data-stu-id="f24cf-114">Choose the BASICCONFIG package from the list, and then choose the **Export Package** action.</span></span>  

<span data-ttu-id="f24cf-115">Gebruik de onderstaande procedure om een nieuw bedrijf aan te maken en gebruik het pakket BASICCONFIG als deel van het proces.</span><span class="sxs-lookup"><span data-stu-id="f24cf-115">Use the following procedure to create a new company, and use the BASICCONFIG package as part of the process.</span></span>  

## <a name="to-create-a-new-company"></a><span data-ttu-id="f24cf-116">Een nieuw bedrijf maken</span><span class="sxs-lookup"><span data-stu-id="f24cf-116">To create a new company</span></span>  
1. <span data-ttu-id="f24cf-117">Maak een nieuw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="f24cf-117">Create a new company.</span></span> <span data-ttu-id="f24cf-118">Zie [Nieuwe bedrijven maken in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f24cf-118">For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).</span></span>
2. <span data-ttu-id="f24cf-119">Vanuit het rolcentrum RapidStart Services-implementatie kunt u het configuratiepakket nu importeren dat u vanuit het bedrijf CRONUS International Ltd. hebt geëxporteerd.</span><span class="sxs-lookup"><span data-stu-id="f24cf-119">From the RapidStart Services Implementer Role Center, you can now import the configuration package that you exported from the CRONUS International Ltd. company.</span></span>

<span data-ttu-id="f24cf-120">Nadat u een nieuw bedrijf maakt, worden sommige tabellen automatisch ingevuld, zelfs als er geen bedrijfssjabloon is toegepast.</span><span class="sxs-lookup"><span data-stu-id="f24cf-120">After you create a new company, some tables are automatically filled in, even if no company template is applied.</span></span> <span data-ttu-id="f24cf-121">U kunt bijvoorbeeld de standaardcodes bekijken voor het boeken en voor batchtransacties op de pagina **Broncode**.</span><span class="sxs-lookup"><span data-stu-id="f24cf-121">For example, you can review the standard codes for posting and batch transactions on the **Source Code** page.</span></span> <span data-ttu-id="f24cf-122">Als u een lokale versie van [!INCLUDE[prod_short](includes/prod_short.md)] hebt, moet u deze tabel bekijken en rekening houden met de lokale taal.</span><span class="sxs-lookup"><span data-stu-id="f24cf-122">If you provide a local version of [!INCLUDE[prod_short](includes/prod_short.md)], you should review this table and consider any local language issues.</span></span>

## <a name="about-data-tables"></a><span data-ttu-id="f24cf-123">Gegevenstabellen</span><span class="sxs-lookup"><span data-stu-id="f24cf-123">About Data Tables</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)]<span data-ttu-id="f24cf-124">-gegevenstabellen worden geleverd in twee basistypen: Hoofd en Instellingen.</span><span class="sxs-lookup"><span data-stu-id="f24cf-124">, data tables come in two basic types: Master and Setup.</span></span> <span data-ttu-id="f24cf-125">Wanneer u een bedrijfsconfiguratie opzet, kunt u deze typen gebruiken om een gerichte configuratiestrategie te hanteren.</span><span class="sxs-lookup"><span data-stu-id="f24cf-125">When you are setting up a company configuration, you can use these types to focus your configuration strategy.</span></span>  

### <a name="master-data-tables"></a><span data-ttu-id="f24cf-126">Hoofdgegevenstabellen</span><span class="sxs-lookup"><span data-stu-id="f24cf-126">Master Data Tables</span></span>  
<span data-ttu-id="f24cf-127">In de volgende tabel worden enkele voorbeelden van de hoofdgegevenstabellen weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f24cf-127">The following table lists some of the master data tables.</span></span> <span data-ttu-id="f24cf-128">Wanneer u een nieuw bedrijf initialiseert, zijn deze tabellen leeg.</span><span class="sxs-lookup"><span data-stu-id="f24cf-128">When you initialize a new company, these tables are empty.</span></span>  

|<span data-ttu-id="f24cf-129">Tabelnr.</span><span class="sxs-lookup"><span data-stu-id="f24cf-129">Table No.</span></span>|<span data-ttu-id="f24cf-130">Tabelnaam</span><span class="sxs-lookup"><span data-stu-id="f24cf-130">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="f24cf-131">15</span><span class="sxs-lookup"><span data-stu-id="f24cf-131">15</span></span>|<span data-ttu-id="f24cf-132">Grootboekrekening</span><span class="sxs-lookup"><span data-stu-id="f24cf-132">G/L Account</span></span>|  
|<span data-ttu-id="f24cf-133">18</span><span class="sxs-lookup"><span data-stu-id="f24cf-133">18</span></span>|<span data-ttu-id="f24cf-134">Klant</span><span class="sxs-lookup"><span data-stu-id="f24cf-134">Customer</span></span>|  
|<span data-ttu-id="f24cf-135">23</span><span class="sxs-lookup"><span data-stu-id="f24cf-135">23</span></span>|<span data-ttu-id="f24cf-136">Leverancier</span><span class="sxs-lookup"><span data-stu-id="f24cf-136">Vendor</span></span>|  
|<span data-ttu-id="f24cf-137">27</span><span class="sxs-lookup"><span data-stu-id="f24cf-137">27</span></span>|<span data-ttu-id="f24cf-138">Artikel</span><span class="sxs-lookup"><span data-stu-id="f24cf-138">Item</span></span>|  
|<span data-ttu-id="f24cf-139">5050</span><span class="sxs-lookup"><span data-stu-id="f24cf-139">5050</span></span>|<span data-ttu-id="f24cf-140">Contactpersoon</span><span class="sxs-lookup"><span data-stu-id="f24cf-140">Contact</span></span>|  

### <a name="setup-data-tables"></a><span data-ttu-id="f24cf-141">Instellingsgegevenstabellen</span><span class="sxs-lookup"><span data-stu-id="f24cf-141">Setup Data Tables</span></span>  
<span data-ttu-id="f24cf-142">De volgende tabel bevat enkele van de instellingsgegevenstabellen, waarin u instelinformatie vastlegt in de configuratievragenlijst.</span><span class="sxs-lookup"><span data-stu-id="f24cf-142">The following table lists some of the setup data tables, in which you capture setup information in the configuration questionnaire.</span></span> <span data-ttu-id="f24cf-143">Deze tabellen bevatten basislijngegevens wanneer het bedrijf wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f24cf-143">These tables contain baseline information when the company is created.</span></span>  

|<span data-ttu-id="f24cf-144">Tabelnr.</span><span class="sxs-lookup"><span data-stu-id="f24cf-144">Table No.</span></span>|<span data-ttu-id="f24cf-145">Tabelnaam</span><span class="sxs-lookup"><span data-stu-id="f24cf-145">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="f24cf-146">98</span><span class="sxs-lookup"><span data-stu-id="f24cf-146">98</span></span>|<span data-ttu-id="f24cf-147">Grootboekinstellingen</span><span class="sxs-lookup"><span data-stu-id="f24cf-147">General Ledger Setup</span></span>|  
|<span data-ttu-id="f24cf-148">311</span><span class="sxs-lookup"><span data-stu-id="f24cf-148">311</span></span>|<span data-ttu-id="f24cf-149">Verkoopinstellingen</span><span class="sxs-lookup"><span data-stu-id="f24cf-149">Sales & Receivables Setup</span></span>|  
|<span data-ttu-id="f24cf-150">312</span><span class="sxs-lookup"><span data-stu-id="f24cf-150">312</span></span>|<span data-ttu-id="f24cf-151">Inkoopinstellingen</span><span class="sxs-lookup"><span data-stu-id="f24cf-151">Purchases & Payables Setup</span></span>|  
|<span data-ttu-id="f24cf-152">313</span><span class="sxs-lookup"><span data-stu-id="f24cf-152">313</span></span>|<span data-ttu-id="f24cf-153">Voorraadinstelling</span><span class="sxs-lookup"><span data-stu-id="f24cf-153">Inventory Setup</span></span>|  

<span data-ttu-id="f24cf-154">Behalve instellingsgegevenstabellen bevat [!INCLUDE[prod_short](includes/prod_short.md)] ook instellingstabellen waarin kerngegevens over het bedrijf en de bedrijfsprocessen worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="f24cf-154">In addition to setup data tables, [!INCLUDE[prod_short](includes/prod_short.md)] also has setup-type data tables that specify core information about the company and its business processes.</span></span> <span data-ttu-id="f24cf-155">In de volgende tabel wordt een aantal ervan weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f24cf-155">The following table lists some of them.</span></span>  

|<span data-ttu-id="f24cf-156">Tabelnr.</span><span class="sxs-lookup"><span data-stu-id="f24cf-156">Table No.</span></span>|<span data-ttu-id="f24cf-157">Tabelnaam</span><span class="sxs-lookup"><span data-stu-id="f24cf-157">Table Name</span></span>|  
|-------------------|--------------------|  
|<span data-ttu-id="f24cf-158">3</span><span class="sxs-lookup"><span data-stu-id="f24cf-158">3</span></span>|<span data-ttu-id="f24cf-159">Betalingsvoorwaarden</span><span class="sxs-lookup"><span data-stu-id="f24cf-159">Payment Terms</span></span>|  
|<span data-ttu-id="f24cf-160">4</span><span class="sxs-lookup"><span data-stu-id="f24cf-160">4</span></span>|<span data-ttu-id="f24cf-161">Valuta</span><span class="sxs-lookup"><span data-stu-id="f24cf-161">Currency</span></span>|  
|<span data-ttu-id="f24cf-162">6</span><span class="sxs-lookup"><span data-stu-id="f24cf-162">6</span></span>|<span data-ttu-id="f24cf-163">Klantenprijsgroepen</span><span class="sxs-lookup"><span data-stu-id="f24cf-163">Customer Price Groups</span></span>|  
|<span data-ttu-id="f24cf-164">5700</span><span class="sxs-lookup"><span data-stu-id="f24cf-164">5700</span></span>|<span data-ttu-id="f24cf-165">SKU</span><span class="sxs-lookup"><span data-stu-id="f24cf-165">Stockkeeping Unit</span></span>|

  

## <a name="see-also"></a><span data-ttu-id="f24cf-166">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f24cf-166">See Also</span></span>  
[<span data-ttu-id="f24cf-167">Configuraties toepassen op nieuwe bedrijven</span><span class="sxs-lookup"><span data-stu-id="f24cf-167">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="f24cf-168">Een bedrijf instellen met RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="f24cf-168">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="f24cf-169">Beheer</span><span class="sxs-lookup"><span data-stu-id="f24cf-169">Administration</span></span>](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]