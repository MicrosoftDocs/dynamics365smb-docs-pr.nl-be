---
title: Business Central gebruiken in Power BI-rapporten | Microsoft Docs
description: Maak uw gegevens als gegevensbron in Power BI beschikbaar en maak krachtige rapporten met de status van uw bedrijf.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 07/08/2019
ms.author: edupont
ms.openlocfilehash: c86f1c3c40f80ec993d0a3a89154047ddf9e8126
ms.sourcegitcommit: 519623f9a5134c9ffa97eeaed0841ae59835f453
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755253"
---
# <a name="using-include-prodlongincludesprodlongmd-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="3d3e3-103">[!INCLUDE [prodlong](includes/prodlong.md)] gebruiken als Power BI-gegevensbron voor het maken van rapporten</span><span class="sxs-lookup"><span data-stu-id="3d3e3-103">Using [!INCLUDE [prodlong](includes/prodlong.md)] as Power BI Data Source for Building Reports</span></span>

<span data-ttu-id="3d3e3-104">U kunt uw [!INCLUDE[prodlong](includes/prodlong.md)]-gegevens als gegevensbron beschikbaar maken in Power BI en krachtige rapporten maken met de status van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-104">You can make your [!INCLUDE[prodlong](includes/prodlong.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

<span data-ttu-id="3d3e3-105">U moet een geldig account bij [!INCLUDE[prodshort](includes/prodshort.md)] en Power BI hebben.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power BI.</span></span> <span data-ttu-id="3d3e3-106">U moet ook [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) downloaden.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-106">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span> <span data-ttu-id="3d3e3-107">Zie voor meer informatie [Snelle start: verbinden met gegevens in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span><span class="sxs-lookup"><span data-stu-id="3d3e3-107">For more information, see [Quickstart: Connect to data in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span></span>  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="3d3e3-108">[!INCLUDE[prodshort](includes/prodshort.md)] als gegevensbron toevoegen in Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3d3e3-108">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power BI Desktop</span></span>

1. <span data-ttu-id="3d3e3-109">Kies in Power BI Desktop in het linkernavigatievenster **Gegevens ophalen**.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-109">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="3d3e3-110">Kies op de pagina **Gegevens ophalen** **Online Services**, kies **Microsoft Dynamics 365 Business Central** en kies vervolgens de knop **Verbinden**.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-110">On the **Get Data** page, choose **Online Services**, choose **Microsoft Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="3d3e3-111">Power BI geeft een wizard weer die u door het verbindingsproces begeleidt.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-111">Power BI displays a wizard that will guide you through the connection process.</span></span> <span data-ttu-id="3d3e3-112">U wordt gevraagd u aan te melden bij [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="3d3e3-112">You will be prompted to sign into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="3d3e3-113">Selecteer **Aanmelden** en kies het account waaronder u zich wilt aanmelden.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-113">Select **Sign in** and choose the account you would like to sign in as.</span></span> <span data-ttu-id="3d3e3-114">Dit moet hetzelfde account zijn als waarmee u zich aanmeldt bij [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="3d3e3-114">This should be the same account you sign into [!INCLUDE [prodshort](includes/prodshort.md)] with.</span></span>
4. <span data-ttu-id="3d3e3-115">Kies de knop **Verbinding maken** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-115">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="3d3e3-116">De Power BI-wizard bevat een lijst met Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-bedrijven en -gegevensbronnen.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-116">The Power BI wizard shows a list of Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] companies and data sources.</span></span> <span data-ttu-id="3d3e3-117">Met deze gegevensbron worden alle webservices vertegenwoordigd die u hebt gepubliceerd vanuit elk bedrijf in [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="3d3e3-117">These data source represent all the web services that you have published from each company in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

  ![powerbi_webservices.png](media/across-how-use-financials-data-source-powerbi/powerbi_webservices.png)

5. <span data-ttu-id="3d3e3-119">U kunt ook een nieuwe webservice-URL in [!INCLUDE [prodshort](includes/prodshort.md)] maken met behulp van de actie **Gegevensset maken** op de pagina **Webservices** met de begeleide instelling **Rapportage instellen** of door de actie **Bewerken in Excel** in de lijsten te kiezen.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-119">Alternatively, create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] by using the **Create Data Set** action on the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>
6. <span data-ttu-id="3d3e3-120">Geef de gegevens op die u aan uw gegevensmodel wilt toevoegen en kies vervolgens de knop **Laden**.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-120">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
7. <span data-ttu-id="3d3e3-121">Herhaal de vorige stappen om aanvullende [!INCLUDE [prodshort](includes/prodshort.md)]- of andere gegevens aan uw Power BI-gegevensmodel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-121">Repeat the previous steps to add additional [!INCLUDE [prodshort](includes/prodshort.md)], or other data, to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="3d3e3-122">Zodra u met succes verbinding hebt gemaakt met [!INCLUDE [prodshort](includes/prodshort.md)], wordt u niet opnieuw gevraagd zich aan te melden.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-122">Once you have successfully connected to [!INCLUDE [prodshort](includes/prodshort.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="3d3e3-123">Zodra de gegevens zijn geladen, worden deze in de rechternavigatie op de pagina weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-123">Once the data is loaded it will appear in the right navigation on the page.</span></span> <span data-ttu-id="3d3e3-124">Nu hebt u met succes een koppeling gemaakt naar uw [!INCLUDE [prodshort](includes/prodshort.md)]-gegevens en kunt u uw Power BI-rapport gaan maken.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-124">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your Power BI report.</span></span>  

<span data-ttu-id="3d3e3-125">Voordat u uw rapport maakt, is het raadzaam dat u het [!INCLUDE [prodshort](includes/prodshort.md)]-themabestand importeert.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-125">Before building your report, we recommend that you import the [!INCLUDE [prodshort](includes/prodshort.md)] theme file.</span></span>  <span data-ttu-id="3d3e3-126">Het themabestand maakt een kleurenpalet, zodat u rapporten kunt maken met dezelfde kleurstijl als de [!INCLUDE [prodshort](includes/prodshort.md)]-apps zonder aangepaste kleuren te hoeven definiëren voor elk visueel element.</span><span class="sxs-lookup"><span data-stu-id="3d3e3-126">The theme file will create a color palette so that you can build reports with the same color styling as the [!INCLUDE [prodshort](includes/prodshort.md)] apps without requiring you to define custom colors for each visual.</span></span>

<span data-ttu-id="3d3e3-127">Zie voor meer informatie de [documentatie van Power BI](/power-bi/consumer/power-bi-consumer-landing/).</span><span class="sxs-lookup"><span data-stu-id="3d3e3-127">For more information, see the [Power BI documentation](/power-bi/consumer/power-bi-consumer-landing/).</span></span>

## <a name="see-also"></a><span data-ttu-id="3d3e3-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3d3e3-128">See Also</span></span>

[<span data-ttu-id="3d3e3-129">Uw bedrijfsgegevens inschakelen voor Power BI</span><span class="sxs-lookup"><span data-stu-id="3d3e3-129">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="3d3e3-130">Bedrijfsinformatie</span><span class="sxs-lookup"><span data-stu-id="3d3e3-130">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="3d3e3-131">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="3d3e3-131">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="3d3e3-132">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="3d3e3-132">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="3d3e3-133">[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="3d3e3-133">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="3d3e3-134">Financiën</span><span class="sxs-lookup"><span data-stu-id="3d3e3-134">Finance</span></span>](finance.md)  
[<span data-ttu-id="3d3e3-135">Snelle start: Uw gegevens verbinden in Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="3d3e3-135">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
