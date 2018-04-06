---
title: Power BI verbinden met Business Central | Microsoft Docs
description: Inzicht, bedrijfsinformatie en KPI's krijgen uit uw Business Central-gegevens is gemakkelijk met Power BI en de Business Central-inhoudspakketten.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 03/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 315d4b188cdd834e82676a0c5ef77272ad873eb7
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-business-central-content-packs"></a><span data-ttu-id="99407-103">Power BI verbinden met Business Central-inhoudspakketten</span><span class="sxs-lookup"><span data-stu-id="99407-103">Connecting Power BI to Business Central Content Packs</span></span>
<span data-ttu-id="99407-104">Inzicht krijgen in uw Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-gegevens is gemakkelijk met Power BI en de inhoudspakketten van Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="99407-104">Getting insights into your Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data is easy with Power BI and the Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] content packs.</span></span> <span data-ttu-id="99407-105">Power BI haalt uw gegevens op en maakt vervolgens een kant-en-klaar dashboard en rapporteert op basis van die gegevens.</span><span class="sxs-lookup"><span data-stu-id="99407-105">Power BI retrieves your data then builds an out-of-the-box dashboard and reports based on that data.</span></span>

> [!NOTE]  
>  <span data-ttu-id="99407-106">U moet een geldig account bij [!INCLUDE[d365fin](includes/d365fin_md.md)] en Power BI hebben.</span><span class="sxs-lookup"><span data-stu-id="99407-106">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Power BI.</span></span> <span data-ttu-id="99407-107">Ook moet u [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) downloaden.</span><span class="sxs-lookup"><span data-stu-id="99407-107">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span>  
>  <span data-ttu-id="99407-108">Voor Power BI-inhoudspakketten zijn machtigingen vereist voor de tabellen waaruit de gegevens worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="99407-108">Power BI content packs require permissions to the tables where data is retrieved from.</span></span> <span data-ttu-id="99407-109">Meer details over de vereisten worden verderop beschreven.</span><span class="sxs-lookup"><span data-stu-id="99407-109">More details on the requirements are described below.</span></span>  

## <a name="how-to-connect"></a><span data-ttu-id="99407-110">Verbinding maken</span><span class="sxs-lookup"><span data-stu-id="99407-110">How to Connect</span></span>
1. <span data-ttu-id="99407-111">Selecteer **Gegevens ophalen** onder in het linkernavigatiedeelvenster.</span><span class="sxs-lookup"><span data-stu-id="99407-111">Select **Get Data** at the bottom of the left navigation pane.</span></span>  
<span data-ttu-id="99407-112">![Navigeren om gegevens op te halen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span><span class="sxs-lookup"><span data-stu-id="99407-112">![Navigating to Get Data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)</span></span>
2. <span data-ttu-id="99407-113">Selecteer **Ophalen** in het vak **Diensten**.</span><span class="sxs-lookup"><span data-stu-id="99407-113">In the **Services** box, select **Get**.</span></span> <span data-ttu-id="99407-114">Hierdoor wordt een venster geopend met de **AppSource** en **Apps voor Power BI-apps**.</span><span class="sxs-lookup"><span data-stu-id="99407-114">This will open a window with the **AppSource** and **Apps for Power BI apps**.</span></span>  
<span data-ttu-id="99407-115">![Inhoudspakketten kiezen uit online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span><span class="sxs-lookup"><span data-stu-id="99407-115">![Choose content packs from online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)</span></span>
3. <span data-ttu-id="99407-116">Selecteer **Apps** op het tabblad **Apps voor Power BI-apps** en kies het inhoudspakket van **Microsoft Dynamics 365 Business Central**-inhoudspakket dat u wilt gebruiken. Selecteer vervolgens **Nu ophalen**.</span><span class="sxs-lookup"><span data-stu-id="99407-116">Select **Apps** from the **Apps for Power BI apps** tab, and choose the **Microsoft Dynamics 365 Business Central** content pack that you want to use, and then select **Get it now**.</span></span>  
<span data-ttu-id="99407-117">![Selecteer Dynamics 365 Business Central en selecteer Nu ophalen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span><span class="sxs-lookup"><span data-stu-id="99407-117">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)</span></span>
4. <span data-ttu-id="99407-118">Voer wanneer daarom wordt gevraagd de naam van *uw bedrijf* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="99407-118">When prompted, enter the name of *your company* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="99407-119">Dit is niet de weergavenaam.</span><span class="sxs-lookup"><span data-stu-id="99407-119">This is not the display name.</span></span>  
<span data-ttu-id="99407-120">![Selecteer Dynamics 365 Business Central en selecteer Nu ophalen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span><span class="sxs-lookup"><span data-stu-id="99407-120">![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)</span></span>
5. <span data-ttu-id="99407-121">Nadat verbinding is gemaakt, worden automatisch een dashboard, rapport en gegevensset geladen in uw Power BI-werkruimte.</span><span class="sxs-lookup"><span data-stu-id="99407-121">Once connected, a dashboard, report and dataset will automatically be loaded into your Power BI workspace.</span></span> <span data-ttu-id="99407-122">Wanneer dit is voltooid, worden de tegels bijgewerkt met gegevens uit uw account.</span><span class="sxs-lookup"><span data-stu-id="99407-122">When completed, the tiles will update with data from your account.</span></span>
<span data-ttu-id="99407-123">![Selecteer Dynamics 365 Business Central en selecteer Nu ophalen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span><span class="sxs-lookup"><span data-stu-id="99407-123">![Select Dynamics 365 Business Central  and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)</span></span>

## <a name="what-now"></a><span data-ttu-id="99407-124">Wat nu?</span><span class="sxs-lookup"><span data-stu-id="99407-124">What Now?</span></span>

- <span data-ttu-id="99407-125">[Wijzig de tegels](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in het dashboard.</span><span class="sxs-lookup"><span data-stu-id="99407-125">[Change the tiles](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in the dashboard.</span></span>  
- <span data-ttu-id="99407-126">[Selecteer een tegel](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) om het onderliggende rapport te openen.</span><span class="sxs-lookup"><span data-stu-id="99407-126">[Select a tile](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) to open the underlying report.</span></span>  
- <span data-ttu-id="99407-127">Terwijl uw gegevensset wordt gepland om dagelijks te worden vernieuwd, kunt u het vernieuwingsschema wijzigen of op verzoek proberen te vernieuwen met **Nu vernieuwen**.</span><span class="sxs-lookup"><span data-stu-id="99407-127">While your dataset will be scheduled to refreshed daily, you can change the refresh schedule or try refreshing it on demand using **Refresh Now**.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="99407-128">Systeemvereisten</span><span class="sxs-lookup"><span data-stu-id="99407-128">System Requirements</span></span>
<span data-ttu-id="99407-129">Als u de gegevens [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] in Power BI wilt importeren, moet u machtigingen hebben voor de webservices die worden gebruikt om gegevens op te halen.</span><span class="sxs-lookup"><span data-stu-id="99407-129">To import your [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] data into Power BI, you need to have permissions to the web services used to retrieve data.</span></span> <span data-ttu-id="99407-130">De webservices die voor elk inhoudspakket vereist zijn omvatten:</span><span class="sxs-lookup"><span data-stu-id="99407-130">The web services required for each content pack include:</span></span>

<span data-ttu-id="99407-131">**Microsoft Dynamics 365 Business Central – CRM**</span><span class="sxs-lookup"><span data-stu-id="99407-131">**Microsoft Dynamics 365 Business Central – CRM**</span></span>
- <span data-ttu-id="99407-132">SalesOpportunities</span><span class="sxs-lookup"><span data-stu-id="99407-132">SalesOpportunities</span></span>
- <span data-ttu-id="99407-133">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="99407-133">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="99407-134">**Microsoft Dynamics 365 Business Central – Verkoop**</span><span class="sxs-lookup"><span data-stu-id="99407-134">**Microsoft Dynamics 365 Business Central – Sales**</span></span>
- <span data-ttu-id="99407-135">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="99407-135">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="99407-136">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="99407-136">SalesDashboard</span></span>
- <span data-ttu-id="99407-137">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="99407-137">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="99407-138">**Microsoft Dynamics 365 Business Central – Financiën**</span><span class="sxs-lookup"><span data-stu-id="99407-138">**Microsoft Dynamics 365 Business Central – Finance**</span></span>
- <span data-ttu-id="99407-139">PowerBIFinance</span><span class="sxs-lookup"><span data-stu-id="99407-139">PowerBIFinance</span></span>
- <span data-ttu-id="99407-140">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="99407-140">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="99407-141">**Microsoft Dynamics 365 Business Central – Projecten**</span><span class="sxs-lookup"><span data-stu-id="99407-141">**Microsoft Dynamics 365 Business Central – Jobs**</span></span>
- <span data-ttu-id="99407-142">Projectoverzicht</span><span class="sxs-lookup"><span data-stu-id="99407-142">Job List</span></span>
- <span data-ttu-id="99407-143">Projectplanningsregels</span><span class="sxs-lookup"><span data-stu-id="99407-143">Job Planning Lines</span></span>
- <span data-ttu-id="99407-144">Projecttaakregels</span><span class="sxs-lookup"><span data-stu-id="99407-144">Job Task Lines</span></span>

<span data-ttu-id="99407-145">**Microsoft Dynamics 365 Business Central – Lijst met klanten**</span><span class="sxs-lookup"><span data-stu-id="99407-145">**Microsoft Dynamics 365 Business Central – Customers List**</span></span>
- <span data-ttu-id="99407-146">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="99407-146">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="99407-147">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="99407-147">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="99407-148">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="99407-148">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="99407-149">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="99407-149">SalesDashboard</span></span>
- <span data-ttu-id="99407-150">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="99407-150">Power_BI_Customer_List</span></span>
- <span data-ttu-id="99407-151">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="99407-151">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="99407-152">**Microsoft Dynamics 365 Business Central – Lijst met artikelen**</span><span class="sxs-lookup"><span data-stu-id="99407-152">**Microsoft Dynamics 365 Business Central – Items List**</span></span>
- <span data-ttu-id="99407-153">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="99407-153">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="99407-154">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="99407-154">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="99407-155">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="99407-155">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="99407-156">Artikelen</span><span class="sxs-lookup"><span data-stu-id="99407-156">Items</span></span>
- <span data-ttu-id="99407-157">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="99407-157">SalesDashboard</span></span>
- <span data-ttu-id="99407-158">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="99407-158">ExcelTemplateViewCompany</span></span>

<span data-ttu-id="99407-159">**Microsoft Dynamics 365 Business Central – Lijst met leveranciers**</span><span class="sxs-lookup"><span data-stu-id="99407-159">**Microsoft Dynamics 365 Business Central – Vendors List**</span></span>
- <span data-ttu-id="99407-160">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="99407-160">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="99407-161">Power_BI_Item_Purchase_List</span><span class="sxs-lookup"><span data-stu-id="99407-161">Power_BI_Item_Purchase_List</span></span>
- <span data-ttu-id="99407-162">Power_BI_Item_Sales_List</span><span class="sxs-lookup"><span data-stu-id="99407-162">Power_BI_Item_Sales_List</span></span>
- <span data-ttu-id="99407-163">Artikelen</span><span class="sxs-lookup"><span data-stu-id="99407-163">Items</span></span>
- <span data-ttu-id="99407-164">SalesDashboard</span><span class="sxs-lookup"><span data-stu-id="99407-164">SalesDashboard</span></span>
- <span data-ttu-id="99407-165">Power_BI_Customer_List</span><span class="sxs-lookup"><span data-stu-id="99407-165">Power_BI_Customer_List</span></span>
- <span data-ttu-id="99407-166">ItemSalesbyCustomer</span><span class="sxs-lookup"><span data-stu-id="99407-166">ItemSalesbyCustomer</span></span>
- <span data-ttu-id="99407-167">Power_BI_Vendor_List</span><span class="sxs-lookup"><span data-stu-id="99407-167">Power_BI_Vendor_List</span></span>
- <span data-ttu-id="99407-168">ExcelTemplateViewCompany</span><span class="sxs-lookup"><span data-stu-id="99407-168">ExcelTemplateViewCompany</span></span>

## <a name="web-services"></a><span data-ttu-id="99407-169">Webservices</span><span class="sxs-lookup"><span data-stu-id="99407-169">Web Services</span></span>
<span data-ttu-id="99407-170">Een eenvoudige manier om de webservices te vinden is te zoeken naar webservices in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="99407-170">An easy way to find the web services is to search for web services in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="99407-171">In de lijst moet u ervoor zorgen het vakje Publiceren is gemarkeerd voor de hierboven genoemde webservices.</span><span class="sxs-lookup"><span data-stu-id="99407-171">In the list make sure the Publish box is marked for the web services listed above.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="99407-172">Problemen oplossen</span><span class="sxs-lookup"><span data-stu-id="99407-172">Troubleshooting</span></span>
<span data-ttu-id="99407-173">Het dashboard van Power BI gebruikt de gepubliceerde webservices die hierboven worden genoemd en bevat gegevens van het demobedrijf of uw eigen bedrijf als u gegevens importeert uit uw huidige financiële oplossing.</span><span class="sxs-lookup"><span data-stu-id="99407-173">The Power BI dashboard relies on the published web services that are listed above, and it will show data from the demonstration company or your own company if you import data from your current finance solution.</span></span> <span data-ttu-id="99407-174">Als er echter iets verkeerd gaat, biedt deze sectie een oplossing voor de meest voorkomende problemen.</span><span class="sxs-lookup"><span data-stu-id="99407-174">However, if something goes wrong, this section provides a workaround for the most typical issues.</span></span>

### <a name="incorrect-company-name"></a><span data-ttu-id="99407-175">Onjuiste bedrijfsnaam</span><span class="sxs-lookup"><span data-stu-id="99407-175">Incorrect Company Name</span></span>  
<span data-ttu-id="99407-176">Een veel voorkomende fout is de weergavenaam van het bedrijf in te voeren in plaats van de bedrijfsnaam.</span><span class="sxs-lookup"><span data-stu-id="99407-176">A common mistake is to enter the company display name instead of the company name.</span></span> <span data-ttu-id="99407-177">Als u de bedrijfsnaam wilt vinden, zoekt u naar **Bedrijven**.</span><span class="sxs-lookup"><span data-stu-id="99407-177">To find the company name search for **Companies**.</span></span> <span data-ttu-id="99407-178">Gebruik vervolgens het veld **Naam** wanneer u uw bedrijfsnaam invoert.</span><span class="sxs-lookup"><span data-stu-id="99407-178">Then use the **Name** field when entering your company name.</span></span>

### <a name="incorrect-user-name-and-password"></a><span data-ttu-id="99407-179">Onjuiste gebruikersnaam en wachtwoord</span><span class="sxs-lookup"><span data-stu-id="99407-179">Incorrect User Name and Password</span></span>  
<span data-ttu-id="99407-180">De gebruikersnaam en het wachtwoord die worden gebruikt om verbinding te maken, zijn hetzelfde als wat wordt gebruikt om verbinding te maken met uw Microsoft Office 365-account.</span><span class="sxs-lookup"><span data-stu-id="99407-180">The user name and password used to connect will be the same as what is used to connect to your Microsoft Office 365 account.</span></span>  

<span data-ttu-id="99407-181">De inhoudspakketten vereisen ook dat u een Microsoft-[!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] hebt.</span><span class="sxs-lookup"><span data-stu-id="99407-181">The content packs also require that you have a Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account.</span></span> <span data-ttu-id="99407-182">Zodra u uw aanmeldingsgegevens invoert, worden eventuele Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-tenants waartoe u toegang hebt, automatisch gevonden.</span><span class="sxs-lookup"><span data-stu-id="99407-182">Once you enter your credentials, we will auto discover any Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] tenants you have access to.</span></span> <span data-ttu-id="99407-183">Als u geen gelicentieerd of proef Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-account hebt, wordt een foutbericht weergegeven.</span><span class="sxs-lookup"><span data-stu-id="99407-183">If you do not have a licensed or trial Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] account, you will receive an error message.</span></span>

### <a name="the-key-didnt-match-any-rows-in-the-table"></a><span data-ttu-id="99407-184">De sleutel kwam met geen rijen uit de tabel overeen</span><span class="sxs-lookup"><span data-stu-id="99407-184">The Key Didn't Match Any Rows in the Table</span></span>
<span data-ttu-id="99407-185">Als u niet een geldige bedrijfsnaam invoert tijdens het verbindingsproces, kunt u de foutmelding "De sleutel kwam met geen rijen uit de tabel overeen" krijgen.</span><span class="sxs-lookup"><span data-stu-id="99407-185">If you enter a non valid company name during the connection process, you may get the error message "The key didn't match any rows in the table".</span></span> <span data-ttu-id="99407-186">Geef de juiste bedrijfsnaam op en probeer opnieuw verbinding te maken.</span><span class="sxs-lookup"><span data-stu-id="99407-186">Provide the correct company name and try connecting again.</span></span>

## <a name="see-also"></a><span data-ttu-id="99407-187">Zie ook</span><span class="sxs-lookup"><span data-stu-id="99407-187">See Also</span></span>
[<span data-ttu-id="99407-188">Aan de slag met Power BI</span><span class="sxs-lookup"><span data-stu-id="99407-188">Get started with Power BI</span></span>](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
<span data-ttu-id="99407-189">[Power BI - Basisconcepten](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Bedrijfsinformatie](bi.md)</span><span class="sxs-lookup"><span data-stu-id="99407-189">[Power BI - Basic Concepts](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Business Intelligence](bi.md)</span></span>  
<span data-ttu-id="99407-190">[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="99407-190">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="99407-191">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="99407-191">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="99407-192">[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="99407-192">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="99407-193">Financiën</span><span class="sxs-lookup"><span data-stu-id="99407-193">Finance</span></span>](finance.md)  
<span data-ttu-id="99407-194">[Rapportage instellen voor [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span><span class="sxs-lookup"><span data-stu-id="99407-194">[Setup Reporting for [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)</span></span>  

