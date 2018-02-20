---
title: Uw gegevens verbinden met Flow| Microsoft Docs
description: U kunt uw Financials-gegevens als gegevensbron beschikbaar maken en een OData-URL van uw webservices opgeven om een geautomatiseerde werkstroom te maken.
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ef4d841723b6bb0af37695a8c3ed1d805319be78
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="0fcc9-103">[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken in een geautomatiseerde werkstroom</span><span class="sxs-lookup"><span data-stu-id="0fcc9-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="0fcc9-104">U kunt uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens als onderdeel van een werkstroom in Microsoft Flow gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0fcc9-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="0fcc9-105">U moet een geldige account bij [!INCLUDE[d365fin](includes/d365fin_md.md)] en Flow hebben.</span><span class="sxs-lookup"><span data-stu-id="0fcc9-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="0fcc9-106">[!INCLUDE[d365fin](includes/d365fin_md.md)] als gegevensbron in Flow toevoegen</span><span class="sxs-lookup"><span data-stu-id="0fcc9-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="0fcc9-107">Navigeer in uw browser naar [flow.microsoft.com](https://flow.microsoft.com/en-us/) en meld u aan.</span><span class="sxs-lookup"><span data-stu-id="0fcc9-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="0fcc9-108">Kies **Mijn Flows** vanuit het lint boven aan de pagina.</span><span class="sxs-lookup"><span data-stu-id="0fcc9-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="0fcc9-109">Kies in het venster **Mijn Flows** de optie **Geheel nieuw maken**.</span><span class="sxs-lookup"><span data-stu-id="0fcc9-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="0fcc9-110">Selecteer in de lijst met beschikbare triggers een van de beschikbare [!INCLUDE[d365fin](includes/d365fin_md.md)]-triggers:</span><span class="sxs-lookup"><span data-stu-id="0fcc9-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="0fcc9-111">*Wanneer een record wordt gemaakt*,</span><span class="sxs-lookup"><span data-stu-id="0fcc9-111">*When a record is created*,</span></span>  
    <span data-ttu-id="0fcc9-112">*Wanneer een record wordt verwijderd*,</span><span class="sxs-lookup"><span data-stu-id="0fcc9-112">*When a record is deleted*,</span></span>  
    <span data-ttu-id="0fcc9-113">*Wanneer een record wordt gewijzigd*,</span><span class="sxs-lookup"><span data-stu-id="0fcc9-113">*When a record is modified*,</span></span>  
    <span data-ttu-id="0fcc9-114">*Wanneer een klantgoedkeuring wordt aangevraagd*,</span><span class="sxs-lookup"><span data-stu-id="0fcc9-114">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="0fcc9-115">*Wanneer goedkeuring van een dagboekbatch wordt aangevraagd*,</span><span class="sxs-lookup"><span data-stu-id="0fcc9-115">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="0fcc9-116">*Wanneer goedkeuring van een dagboekregel wordt aangevraagd*,</span><span class="sxs-lookup"><span data-stu-id="0fcc9-116">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="0fcc9-117">*Wanneer goedkeuring van een artikel wordt aangevraagd*,</span><span class="sxs-lookup"><span data-stu-id="0fcc9-117">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="0fcc9-118">*Wanneer goedkeuring van een inkoopdocument wordt aangevraagd*,</span><span class="sxs-lookup"><span data-stu-id="0fcc9-118">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="0fcc9-119">*Wanneer goedkeuring van een verkoopdocument wordt aangevraagd*, of</span><span class="sxs-lookup"><span data-stu-id="0fcc9-119">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="0fcc9-120">*Wanneer goedkeuring van een leverancier wordt aangevraagd*.</span><span class="sxs-lookup"><span data-stu-id="0fcc9-120">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="0fcc9-121">Flow vraagt u om de gegevens die nodig zijn om verbinding te maken met uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens.</span><span class="sxs-lookup"><span data-stu-id="0fcc9-121">Flow will prompt you for the information that is required to connect to your [!INCLUDE[d365fin](includes/d365fin_md.md)] data.</span></span> <span data-ttu-id="0fcc9-122">Als u een van de volgende triggers hebt geselecteerd, moet u een bedrijfsnaam en een tabelnaam selecteren: *Wanneer een record wordt gemaakt*, *Wanneer een record wordt gewijzigd* of *Wanneer een record wordt verwijderd*.</span><span class="sxs-lookup"><span data-stu-id="0fcc9-122">If you selected one of the following triggers: *When a record is created*, *When a record is modified*, or *When a record is deleted*, you must select a company name and table name.</span></span> <span data-ttu-id="0fcc9-123">Met andere triggers is alleen de bedrijfsnaam nodig om verbinding te maken.</span><span class="sxs-lookup"><span data-stu-id="0fcc9-123">With any other trigger, only the company name is required to connect.</span></span>

   <span data-ttu-id="0fcc9-124">Met Flow wordt een lijst met bedrijven en tabellen weergegeven die beschikbaar zijn in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0fcc9-124">Flow will show a list of companies and tables that are available from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="0fcc9-125">Met deze tabellen, of eindpunten, worden alle webservices vertegenwoordigd die u hebt gepubliceerd vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0fcc9-125">These tables, or end points, represent all the web services that you have published from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

   <span data-ttu-id="0fcc9-126">U kunt ook een nieuwe webservice-URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] maken met behulp van de actie **Gegevensset maken** op de pagina **Webservices** met de begeleide instelling **Rapportage instellen** of door de actie **Bewerken in Excel** in de lijsten te kiezen.</span><span class="sxs-lookup"><span data-stu-id="0fcc9-126">Alternatively, create a new web service URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] by using the **Create Data Set** action in the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>

<span data-ttu-id="0fcc9-127">Nu hebt u met succes een verbinding gemaakt met uw Finance and Operations, Business edition-gegevens en kunt u uw stroom gaan maken.</span><span class="sxs-lookup"><span data-stu-id="0fcc9-127">At this point, you have successfully connected to your Finance and Operations, Business edition data and are ready to begin building your flow.</span></span> <span data-ttu-id="0fcc9-128">Zie de [Flow-documentatie](https://flow.microsoft.com/documentation/getting-started/) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="0fcc9-128">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="0fcc9-129">Zie voor het oplossen van problemen met Microsoft Flow [Problemen oplossen met integratie met Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="0fcc9-129">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0fcc9-130">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0fcc9-130">See Also</span></span>
<span data-ttu-id="0fcc9-131">[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="0fcc9-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="0fcc9-132">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="0fcc9-132">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="0fcc9-133">[Gebruikers en machtigingen beheren](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="0fcc9-133">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="0fcc9-134">[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="0fcc9-134">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="0fcc9-135">Financiën</span><span class="sxs-lookup"><span data-stu-id="0fcc9-135">Finance</span></span>](finance.md)  

