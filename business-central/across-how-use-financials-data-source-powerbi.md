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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 4f140303f037ea4a914cba1ded44fd453bcdfabb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187904"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="2812f-103">[!INCLUDE [prodlong](includes/prodlong.md)] gebruiken als Power BI-gegevensbron voor het maken van rapporten</span><span class="sxs-lookup"><span data-stu-id="2812f-103">Using [!INCLUDE [prodlong](includes/prodlong.md)] as Power BI Data Source for Building Reports</span></span>

<span data-ttu-id="2812f-104">U kunt uw [!INCLUDE[prodlong](includes/prodlong.md)]-gegevens als gegevensbron beschikbaar maken in Power BI en krachtige rapporten maken met de status van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="2812f-104">You can make your [!INCLUDE[prodlong](includes/prodlong.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

<span data-ttu-id="2812f-105">U moet een geldig account bij [!INCLUDE[prodshort](includes/prodshort.md)] en Power BI hebben.</span><span class="sxs-lookup"><span data-stu-id="2812f-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power BI.</span></span> <span data-ttu-id="2812f-106">U moet ook [Power BI Desktop](https://powerbi.microsoft.com/desktop/) downloaden.</span><span class="sxs-lookup"><span data-stu-id="2812f-106">You must also download [Power BI Desktop](https://powerbi.microsoft.com/desktop/).</span></span> <span data-ttu-id="2812f-107">Zie voor meer informatie [Snelle start: verbinden met gegevens in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span><span class="sxs-lookup"><span data-stu-id="2812f-107">For more information, see [Quickstart: Connect to data in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span></span>  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="2812f-108">[!INCLUDE[prodshort](includes/prodshort.md)] als gegevensbron toevoegen in Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2812f-108">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power BI Desktop</span></span>

1. <span data-ttu-id="2812f-109">Kies in Power BI Desktop in het linkernavigatievenster **Gegevens ophalen**.</span><span class="sxs-lookup"><span data-stu-id="2812f-109">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="2812f-110">Kies op de pagina **Gegevens ophalen** **Online Services**, kies **Microsoft Dynamics 365 Business Central** en kies vervolgens de knop **Verbinden**.</span><span class="sxs-lookup"><span data-stu-id="2812f-110">On the **Get Data** page, choose **Online Services**, choose **Microsoft Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="2812f-111">Power BI geeft een wizard weer die u door het verbindingsproces begeleidt, inclusief aanmelden bij [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2812f-111">Power BI displays a wizard that will guide you through the connection process, including signing into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="2812f-112">Kies **Aanmelden** en kies vervolgens het relevante account.</span><span class="sxs-lookup"><span data-stu-id="2812f-112">Choose **Sign in**, and then choose the relevant account.</span></span> <span data-ttu-id="2812f-113">Gebruik hetzelfde account als waarmee u zich aanmeldt bij [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2812f-113">Use the same account that you sign into [!INCLUDE [prodshort](includes/prodshort.md)] with.</span></span>
4. <span data-ttu-id="2812f-114">Kies de knop **Verbinding maken** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="2812f-114">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="2812f-115">De wizard Power BI bevat een lijst met Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-omgevingen, -bedrijven en -gegevensbronnen.</span><span class="sxs-lookup"><span data-stu-id="2812f-115">The Power BI wizard shows a list of Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] environments, companies, and data sources.</span></span> <span data-ttu-id="2812f-116">Met deze gegevensbronnen worden alle webservices vertegenwoordigd die u hebt gepubliceerd vanuit [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2812f-116">These data sources represent all the web services that you have published from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

    <span data-ttu-id="2812f-117">U kunt ook een nieuwe webservice-URL maken in [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="2812f-117">You can also create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] instead.</span></span> <span data-ttu-id="2812f-118">Kies een van de volgende methoden:</span><span class="sxs-lookup"><span data-stu-id="2812f-118">Choose one of the following methods:</span></span>

      - <span data-ttu-id="2812f-119">De actie **Gegevensset maken** op de pagina **Webservices** gebruiken</span><span class="sxs-lookup"><span data-stu-id="2812f-119">Use the **Create Data Set** action on the **Web Services** page</span></span>
      - <span data-ttu-id="2812f-120">De begeleide instelling **Rapportage instellen** gebruiken</span><span class="sxs-lookup"><span data-stu-id="2812f-120">Use the **Set Up Reporting** Assisted Setup guide</span></span>
      - <span data-ttu-id="2812f-121">De actie **Bewerken in Excel** kiezen in een lijst</span><span class="sxs-lookup"><span data-stu-id="2812f-121">Choose the **Edit in Excel** action in any lists</span></span>

5. <span data-ttu-id="2812f-122">Geef de gegevens op die u aan uw gegevensmodel wilt toevoegen en kies vervolgens de knop **Laden**.</span><span class="sxs-lookup"><span data-stu-id="2812f-122">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
6. <span data-ttu-id="2812f-123">Herhaal de vorige stappen om aanvullende [!INCLUDE [prodshort](includes/prodshort.md)]- of andere gegevens aan uw Power BI-gegevensmodel toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="2812f-123">Repeat the previous steps to add additional [!INCLUDE [prodshort](includes/prodshort.md)], or other data, to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="2812f-124">Zodra u met succes verbinding hebt gemaakt met [!INCLUDE [prodshort](includes/prodshort.md)], wordt u niet opnieuw gevraagd zich aan te melden.</span><span class="sxs-lookup"><span data-stu-id="2812f-124">Once you have successfully connected to [!INCLUDE [prodshort](includes/prodshort.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="2812f-125">Zodra de gegevens zijn geladen, ziet u deze in de rechternavigatie op de pagina.</span><span class="sxs-lookup"><span data-stu-id="2812f-125">Once the data is loaded, you can see it in the right navigation on the page.</span></span> <span data-ttu-id="2812f-126">U hebt met succes een koppeling gemaakt naar uw [!INCLUDE [prodshort](includes/prodshort.md)]-gegevens en kunt u uw Power BI-rapport gaan maken.</span><span class="sxs-lookup"><span data-stu-id="2812f-126">You have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data, and you can begin building your Power BI report.</span></span>  

<span data-ttu-id="2812f-127">Voordat u uw rapport maakt, is het raadzaam dat u het [!INCLUDE [prodshort](includes/prodshort.md)]-themabestand importeert.</span><span class="sxs-lookup"><span data-stu-id="2812f-127">Before building your report, we recommend that you import the [!INCLUDE [prodshort](includes/prodshort.md)] theme file.</span></span>  <span data-ttu-id="2812f-128">Het themabestand maakt een kleurenpalet, zodat u rapporten kunt maken met dezelfde kleurstijl als de [!INCLUDE [prodshort](includes/prodshort.md)]-apps zonder aangepaste kleuren te hoeven definiëren voor elk visueel element.</span><span class="sxs-lookup"><span data-stu-id="2812f-128">The theme file will create a color palette so that you can build reports with the same color styling as the [!INCLUDE [prodshort](includes/prodshort.md)] apps without requiring you to define custom colors for each visual.</span></span>

<span data-ttu-id="2812f-129">Zie voor meer informatie de [documentatie van Power BI](/power-bi/consumer/).</span><span class="sxs-lookup"><span data-stu-id="2812f-129">For more information, see the [Power BI documentation](/power-bi/consumer/).</span></span>

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="2812f-130">Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="2812f-130">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="2812f-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2812f-131">See Also</span></span>

[<span data-ttu-id="2812f-132">Uw bedrijfsgegevens inschakelen voor Power BI</span><span class="sxs-lookup"><span data-stu-id="2812f-132">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="2812f-133">Bedrijfsinformatie</span><span class="sxs-lookup"><span data-stu-id="2812f-133">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="2812f-134">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="2812f-134">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="2812f-135">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="2812f-135">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="2812f-136">[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="2812f-136">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="2812f-137">Financiën</span><span class="sxs-lookup"><span data-stu-id="2812f-137">Finance</span></span>](finance.md)  
[<span data-ttu-id="2812f-138">Snelle start: Uw gegevens verbinden in Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2812f-138">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
