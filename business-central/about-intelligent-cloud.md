---
title: Intelligente inzichten en cloudmigratie | Microsoft Docs
description: Verbinding maken met intelligente inzichten met Business Central vanuit uw on-premises oplossing. Leer hoe u naar de cloud kunt migreren.
author: bmeier94
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms. search.keywords: cloud, edge
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: ca7fd910e70deaebbf8912eecfe6d9c25ddfcc4e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385136"
---
# <a name="intelligent-insights-with-prod_short-online"></a><span data-ttu-id="feee0-104">Intelligente inzichten met [!INCLUDE[prod_short](includes/prod_short.md)] Online</span><span class="sxs-lookup"><span data-stu-id="feee0-104">Intelligent Insights with [!INCLUDE[prod_short](includes/prod_short.md)] Online</span></span>

<span data-ttu-id="feee0-105">Als gebruiker van [!INCLUDE[prod_short](includes/prod_short.md)] online hebt u volledige toegang tot scenario's die zijn gebaseerd op de Intelligente cloud, zoals KPI's die zijn gebaseerd op Machine Learning of wanneer u uw gegevens bekijkt in Power BI.</span><span class="sxs-lookup"><span data-stu-id="feee0-105">As a user of [!INCLUDE[prod_short](includes/prod_short.md)] online, you have full access to scenarios that are based on the intelligent cloud, such as KPIs that are based on machine learning, or when you view your data in Power BI.</span></span> <span data-ttu-id="feee0-106">Terwijl [!INCLUDE[prod_short](includes/prod_short.md)] echter een cloud-eerst service is, kunnen ook klanten die hun volledige werklast on-premises of op de intelligente rand, verbonden met de cloud, moeten uitvoeren, dat ook doen.</span><span class="sxs-lookup"><span data-stu-id="feee0-106">However, while [!INCLUDE[prod_short](includes/prod_short.md)] is a cloud-first service, also those customers who need to run their workloads fully on-premises or on the intelligent edge connected to the cloud can do so.</span></span>  

<span data-ttu-id="feee0-107">Als u geïnteresseerd bent in [!INCLUDE[prod_short](includes/prod_short.md)], kunt u zich online aanmelden voor een gratis proefversie of kunt u ervoor kiezen te werken met een partner om [!INCLUDE[prod_short](includes/prod_short.md)] lokaal te implementeren op uw keuze van hardware.</span><span class="sxs-lookup"><span data-stu-id="feee0-107">If you are interested in [!INCLUDE[prod_short](includes/prod_short.md)], you can sign up for a free trial online, or you can choose to work with a partner to deploy [!INCLUDE[prod_short](includes/prod_short.md)] locally to your own choice of hardware.</span></span> <span data-ttu-id="feee0-108">Vervolgens kunt u bepalen of u intelligente inzichten wilt door verbinding te maken met een tenant in de cloud.</span><span class="sxs-lookup"><span data-stu-id="feee0-108">You can then decide to get intelligent insights by connecting to a tenant in the cloud.</span></span> <span data-ttu-id="feee0-109">Dientengevolge worden de gegevens uit uw geïmplementeerde [!INCLUDE[prod_short](includes/prod_short.md)] on-premises naar de cloud gerepliceerd voor intelligente cloudscenario's.</span><span class="sxs-lookup"><span data-stu-id="feee0-109">As a result, the data from your [!INCLUDE[prod_short](includes/prod_short.md)] on-premises deployment replicates to the cloud for intelligent cloud scenarios.</span></span>  

<span data-ttu-id="feee0-110">Verbinding maken met de Intelligente cloud vanuit een on-premises oplossing vereist dat uw beheerder informatie over uw database opgeeft.</span><span class="sxs-lookup"><span data-stu-id="feee0-110">Connecting to the intelligent cloud from an on-premises solution requires your administrator to specify information about your database.</span></span> <span data-ttu-id="feee0-111">De tools waarmee u uw on-premises implementatie kunt verbinden met [!INCLUDE[prod_short](includes/prod_short.md)] online zijn hetzelfde als die ook worden gebruikt voor migratie van on-premises naar online.</span><span class="sxs-lookup"><span data-stu-id="feee0-111">The tools used to connect your on-premises deployment to [!INCLUDE[prod_short](includes/prod_short.md)] online are the same that are also used to migration from on-premises to online.</span></span> <span data-ttu-id="feee0-112">Zie voor meer informatie [On-premises gegevens migreren naar Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in de beheerinhoud voor [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="feee0-112">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="viewing-intelligent-cloud-insights-in-prod_short-online"></a><span data-ttu-id="feee0-113">Intelligente cloud-inzichten weergeven in [!INCLUDE[prod_short](includes/prod_short.md)] Online</span><span class="sxs-lookup"><span data-stu-id="feee0-113">Viewing Intelligent Cloud Insights in [!INCLUDE[prod_short](includes/prod_short.md)] Online</span></span>

<span data-ttu-id="feee0-114">In uw [!INCLUDE[prod_short](includes/prod_short.md)] online-bedrijf bevat de pagina **Intelligente cloud-inzichten** vier belangrijke aandachtspunten voor de meeste bedrijven:</span><span class="sxs-lookup"><span data-stu-id="feee0-114">In your [!INCLUDE[prod_short](includes/prod_short.md)] online company, the **Intelligent Cloud Insights** page shows four key points of interest for most businesses:</span></span>

- <span data-ttu-id="feee0-115">Cashbeschikbaarheid</span><span class="sxs-lookup"><span data-stu-id="feee0-115">Cash availability</span></span>
- <span data-ttu-id="feee0-116">Winstgevendheid van verkoop</span><span class="sxs-lookup"><span data-stu-id="feee0-116">Sales profitability</span></span>
- <span data-ttu-id="feee0-117">Nettowinst</span><span class="sxs-lookup"><span data-stu-id="feee0-117">Net income</span></span>
- <span data-ttu-id="feee0-118">Voorraadwaarde</span><span class="sxs-lookup"><span data-stu-id="feee0-118">Inventory value</span></span>

<span data-ttu-id="feee0-119">Naast de KPI-grafieken krijgt u informatie over potentiële aandachtspunten, inclusief achterstallige betalingen.</span><span class="sxs-lookup"><span data-stu-id="feee0-119">Next to the KPI charts, you get insights into potential areas of concern, including overdue payments.</span></span> <span data-ttu-id="feee0-120">Kies elk inzicht om in te zoomen op de gegevens.</span><span class="sxs-lookup"><span data-stu-id="feee0-120">Choose each insight to drill into the data.</span></span>  

> [!div class="mx-imgBorder"]
> <span data-ttu-id="feee0-121">![Intelligente cloud-inzichten](media/across-intelligent-cloud/intelligentcloudApril19.png "Geeft de pagina Intelligente cloud-inzichten weer in Business Central")</span><span class="sxs-lookup"><span data-stu-id="feee0-121">![Intelligent cloud insights](media/across-intelligent-cloud/intelligentcloudApril19.png "Shows the Intelligent Cloud Insights page in Business Central")</span></span>

<span data-ttu-id="feee0-122">De pagina maakt ook verbinding met Power BI voor nog meer inzichten.</span><span class="sxs-lookup"><span data-stu-id="feee0-122">The page also connects to Power BI for even more insights.</span></span>

## <a name="viewing-intelligent-insights-on-premises"></a><span data-ttu-id="feee0-123">Intelligente cloud-inzichten on-premises weergeven</span><span class="sxs-lookup"><span data-stu-id="feee0-123">Viewing Intelligent Insights On-Premises</span></span>

<span data-ttu-id="feee0-124">Wanneer uw Dynamics 365 doorverkopende partner de juiste licentie heeft verkregen voor uw on-premises oplossing om verbinding met de cloud te maken via [!INCLUDE[prod_short](includes/prod_short.md)], kan uw beheerder de verbinding instellen.</span><span class="sxs-lookup"><span data-stu-id="feee0-124">When your Dynamics 365 reselling partner has acquired the right license for your on-premises solution to connect to the cloud through [!INCLUDE[prod_short](includes/prod_short.md)], your administrator can set up the connection.</span></span> <span data-ttu-id="feee0-125">Als dat is gebeurd, kunt u dezelfde inzichten uit de cloud weergeven in uw on-premises toepassing</span><span class="sxs-lookup"><span data-stu-id="feee0-125">Once that is done, you can view the same insights from the cloud in your on-premises application.</span></span> <span data-ttu-id="feee0-126">Afhankelijk van de on-premises oplossing kan de pagina **Intelligente cloud-inzichten** in de homepage worden ingesloten of een aparte pagina zijn, zoals in [!INCLUDE[prod_short](includes/prod_short.md)] online en on-premises.</span><span class="sxs-lookup"><span data-stu-id="feee0-126">Depending on the on-premises solution, the **Intelligent Cloud Insights** page can be embedded in the Home page or be a separate page as in [!INCLUDE[prod_short](includes/prod_short.md)] online and on-premises.</span></span>  

## <a name="see-also"></a><span data-ttu-id="feee0-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="feee0-127">See Also</span></span>

[<span data-ttu-id="feee0-128">Welkom bij Business Central</span><span class="sxs-lookup"><span data-stu-id="feee0-128">Welcome to Business Central</span></span>](index.md)  
[<span data-ttu-id="feee0-129">Intelligente cloud-extensies voor cloudmigratie</span><span class="sxs-lookup"><span data-stu-id="feee0-129">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="feee0-130">On-premises gegevens migreren naar Business Central Online</span><span class="sxs-lookup"><span data-stu-id="feee0-130">Migrating On-Premises Data to Business Central Online</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]