---
title: Uw gegevens verbinden met Flow| Microsoft Docs
description: U kunt uw Financials-gegevens als gegevensbron beschikbaar maken en een OData-URL van uw webservices opgeven om een geautomatiseerde werkstroom te maken.
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 01/25/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 23e9ebbb75d23595d568d022526e551bf590a979
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a><span data-ttu-id="1e4af-103">[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken in een geautomatiseerde werkstroom</span><span class="sxs-lookup"><span data-stu-id="1e4af-103">Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow</span></span>
<span data-ttu-id="1e4af-104">U kunt uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens als onderdeel van een werkstroom in Microsoft Flow gebruiken.</span><span class="sxs-lookup"><span data-stu-id="1e4af-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="1e4af-105">U moet een geldige account bij [!INCLUDE[d365fin](includes/d365fin_md.md)] en Flow hebben.</span><span class="sxs-lookup"><span data-stu-id="1e4af-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a><span data-ttu-id="1e4af-106">[!INCLUDE[d365fin](includes/d365fin_md.md)] als gegevensbron in Flow toevoegen</span><span class="sxs-lookup"><span data-stu-id="1e4af-106">To add [!INCLUDE[d365fin](includes/d365fin_md.md)] as a data source in Flow</span></span>
1. <span data-ttu-id="1e4af-107">Navigeer in uw browser naar [flow.microsoft.com](https://flow.microsoft.com/en-us/) en meld u aan.</span><span class="sxs-lookup"><span data-stu-id="1e4af-107">In your browser, navigate to [flow.microsoft.com](https://flow.microsoft.com/en-us/), and then sign in.</span></span>
2. <span data-ttu-id="1e4af-108">Kies **Mijn Flows** vanuit het lint boven aan de pagina.</span><span class="sxs-lookup"><span data-stu-id="1e4af-108">Choose **My Flows** from the ribbon at the top of the page.</span></span>
3. <span data-ttu-id="1e4af-109">Kies in het venster **Mijn Flows** de optie **Geheel nieuw maken**.</span><span class="sxs-lookup"><span data-stu-id="1e4af-109">In the **My Flows** window, choose the **Create from blank** option.</span></span>
4. <span data-ttu-id="1e4af-110">Selecteer in de lijst met beschikbare triggers een van de beschikbare [!INCLUDE[d365fin](includes/d365fin_md.md)]-triggers:</span><span class="sxs-lookup"><span data-stu-id="1e4af-110">From the list of available triggers, select one of the [!INCLUDE[d365fin](includes/d365fin_md.md)] triggers available:</span></span>  
    <span data-ttu-id="1e4af-111">*Wanneer een klantgoedkeuring wordt aangevraagd*,</span><span class="sxs-lookup"><span data-stu-id="1e4af-111">*When a customer approval is requested*,</span></span>  
    <span data-ttu-id="1e4af-112">*Wanneer goedkeuring van een dagboekbatch wordt aangevraagd*,</span><span class="sxs-lookup"><span data-stu-id="1e4af-112">*When a general journal batch approval is requested*,</span></span>  
    <span data-ttu-id="1e4af-113">*Wanneer goedkeuring van een dagboekregel wordt aangevraagd*,</span><span class="sxs-lookup"><span data-stu-id="1e4af-113">*When a general journal line approval is requested*,</span></span>  
    <span data-ttu-id="1e4af-114">*Wanneer goedkeuring van een artikel wordt aangevraagd*,</span><span class="sxs-lookup"><span data-stu-id="1e4af-114">*When an item approval is requested*,</span></span>  
    <span data-ttu-id="1e4af-115">*Wanneer goedkeuring van een inkoopdocument wordt aangevraagd*,</span><span class="sxs-lookup"><span data-stu-id="1e4af-115">*When a purchase document approval is requested*,</span></span>  
    <span data-ttu-id="1e4af-116">*Wanneer goedkeuring van een verkoopdocument wordt aangevraagd*, of</span><span class="sxs-lookup"><span data-stu-id="1e4af-116">*When a sales document approval is requested*, or</span></span>  
    <span data-ttu-id="1e4af-117">*Wanneer goedkeuring van een leverancier wordt aangevraagd*.</span><span class="sxs-lookup"><span data-stu-id="1e4af-117">*When a vendor aproval is requested*.</span></span>
5. <span data-ttu-id="1e4af-118">Flow vraagt u een bedrijf in uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-tenant te selecteren.</span><span class="sxs-lookup"><span data-stu-id="1e4af-118">Flow will prompt you to select a company within your [!INCLUDE[d365fin](includes/d365fin_md.md)] tenant.</span></span> <span data-ttu-id="1e4af-119">Aangezien elke stap in Flow onafhankelijk is van de volgende, moet u het bedrijf mogelijk meerdere malen definiëren wanneer u een [!INCLUDE[d365fin](includes/d365fin_md.md)]-sjabloon gebruikt.</span><span class="sxs-lookup"><span data-stu-id="1e4af-119">Because each step in the Flow is independent of the next, you may be required to define the company multiple times when using a [!INCLUDE[d365fin](includes/d365fin_md.md)] template.</span></span>

<span data-ttu-id="1e4af-120">Nu hebt u met succes een verbinding gemaakt met uw Business Central-gegevens en kunt u uw stroom gaan maken.</span><span class="sxs-lookup"><span data-stu-id="1e4af-120">At this point, you have successfully connected to your Business Central data and are ready to begin building your flow.</span></span> <span data-ttu-id="1e4af-121">Zie de [Flow-documentatie](https://flow.microsoft.com/documentation/getting-started/) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1e4af-121">For more information, see the [Flow documentation](https://flow.microsoft.com/documentation/getting-started/).</span></span>

<span data-ttu-id="1e4af-122">Zie voor het oplossen van problemen met Microsoft Flow [Problemen oplossen met integratie met Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span><span class="sxs-lookup"><span data-stu-id="1e4af-122">For troubleshooting your Microsoft Flow, see [Troubleshooting Integration with Microsoft Flow](across-troubleshooting-how-use-financials-data-source-flow.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1e4af-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1e4af-123">See Also</span></span>
<span data-ttu-id="1e4af-124">[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="1e4af-124">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="1e4af-125">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="1e4af-125">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="1e4af-126">[Gebruikers en machtigingen beheren](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="1e4af-126">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="1e4af-127">[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="1e4af-127">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="1e4af-128">Financiën</span><span class="sxs-lookup"><span data-stu-id="1e4af-128">Finance</span></span>](finance.md)  

