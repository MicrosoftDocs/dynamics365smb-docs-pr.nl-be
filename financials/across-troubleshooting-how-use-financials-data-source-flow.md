---
title: Problemen oplossen met integratie met Microsoft Flow| Microsoft Docs
description: Problemen oplossen met hoe u uw Financials-gegevens als gegevensbron beschikbaar kunt maken en een OData-URL van uw webservices kunt opgeven om een geautomatiseerde werkstroom te maken.
documentationcenter: 
author: SusanneWindfeldPedersen
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
ms.openlocfilehash: 4c28b5b6dce6152399cf599877180e806227b5ef
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="troubleshooting-integration-with-microsoft-flow---request-url-too-long"></a><span data-ttu-id="0080c-103">Problemen oplossen met integratie met Microsoft Flow - Aanvraag-URL te lang</span><span class="sxs-lookup"><span data-stu-id="0080c-103">Troubleshooting Integration with Microsoft Flow - Request URL Too Long</span></span>
<span data-ttu-id="0080c-104">U kunt uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens als onderdeel van een werkstroom in Microsoft Flow gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0080c-104">You can use your [!INCLUDE[d365fin](includes/d365fin_md.md)] data as part of a workflow in Microsoft Flow.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="0080c-105">U moet een geldige account bij [!INCLUDE[d365fin](includes/d365fin_md.md)] en Flow hebben.</span><span class="sxs-lookup"><span data-stu-id="0080c-105">You must have a valid account with [!INCLUDE[d365fin](includes/d365fin_md.md)] and with Flow.</span></span>  

<span data-ttu-id="0080c-106">Als u een Microsoft Flow maakt met de [!INCLUDE[d365fin](includes/d365fin_md.md)]-connector, kan er een foutbericht worden weergegeven dat de gevraagde URL te lang is na het maken van de stroom, zoals de volgende: **RequestUriTooLong**.</span><span class="sxs-lookup"><span data-stu-id="0080c-106">If you are creating a Microsoft Flow using the [!INCLUDE[d365fin](includes/d365fin_md.md)] connector, you may receive an error message stating that the requsted URL is too long after creating the flow, such as the following: **RequestUriTooLong**.</span></span>

## <a name="cause"></a><span data-ttu-id="0080c-107">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="0080c-107">Cause</span></span>
<span data-ttu-id="0080c-108">Voor een te activeren stroom wordt gezocht naar wijzigingen in uw gegevens.</span><span class="sxs-lookup"><span data-stu-id="0080c-108">For a flow to trigger, it looks for changes in your data.</span></span> <span data-ttu-id="0080c-109">Wanneer wordt bepaald of uw gegevens zijn gewijzigd, vergelijken de connectors de gegevens in de cache met de nieuwe gegevens die uit de bron zijn aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="0080c-109">When determining if your data has changed, the connectors compare the cached data to the new data requested from the source.</span></span>  

<span data-ttu-id="0080c-110">Als de gegevensaanvraag een URL maakt die te lang is, mislukt het.</span><span class="sxs-lookup"><span data-stu-id="0080c-110">If the data request creates a URL that is too long, it will fail.</span></span> <span data-ttu-id="0080c-111">Veel voorkomende oorzaken zijn:</span><span class="sxs-lookup"><span data-stu-id="0080c-111">Common causes may include:</span></span>
- <span data-ttu-id="0080c-112">Over het algemeen een brontabel met meer dan 250 rijen</span><span class="sxs-lookup"><span data-stu-id="0080c-112">Generally, any source table with over 250 rows</span></span>
- <span data-ttu-id="0080c-113">Brontabellen die duizenden records bevatten</span><span class="sxs-lookup"><span data-stu-id="0080c-113">Source tables containing multiple thousands of records</span></span>

## <a name="workaround"></a><span data-ttu-id="0080c-114">Oplossing</span><span class="sxs-lookup"><span data-stu-id="0080c-114">Workaround</span></span>
<span data-ttu-id="0080c-115">Volg deze stappen als oplossing.</span><span class="sxs-lookup"><span data-stu-id="0080c-115">Follow these steps as a workaround.</span></span>
1. <span data-ttu-id="0080c-116">Kies ervoor de stroom te bewerken die is mislukt.</span><span class="sxs-lookup"><span data-stu-id="0080c-116">Choose to edit the flow that is failing.</span></span>
2. <span data-ttu-id="0080c-117">Vouw **Geavanceerde opties weergegeven** uit op de stroomtrigger.</span><span class="sxs-lookup"><span data-stu-id="0080c-117">Expand the **Show advanced options** on the flow trigger.</span></span>
3. <span data-ttu-id="0080c-118">Voer in het veld **Aantal overslaan** het aantal records in dat moet worden overgeslagen.</span><span class="sxs-lookup"><span data-stu-id="0080c-118">In the **Skip Count** field, enter the number of records to skip.</span></span>  
<span data-ttu-id="0080c-119">Als de tabel die u als gegevensbron gebruikt, bijvoorbeeld 4000 records bevat, voert u 4000 in als het aantal records dat moet worden overgeslagen.</span><span class="sxs-lookup"><span data-stu-id="0080c-119">For example, if the table that you are using as a data source has 4,000 records, enter 4,000 as the number of records to skip.</span></span>
4. <span data-ttu-id="0080c-120">Werk uw stroom bij.</span><span class="sxs-lookup"><span data-stu-id="0080c-120">Update your flow.</span></span>

> [!NOTE]  
> <span data-ttu-id="0080c-121">De connector is nu in bèta.</span><span class="sxs-lookup"><span data-stu-id="0080c-121">The connector is currently in Beta.</span></span> <span data-ttu-id="0080c-122">Updates op hoe gegevenswijzigingen worden behandeld in een toekomstige versie.</span><span class="sxs-lookup"><span data-stu-id="0080c-122">Updates to how data changes are targeted for a future release.</span></span>


## <a name="see-also"></a><span data-ttu-id="0080c-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0080c-123">See Also</span></span>
<span data-ttu-id="0080c-124">[[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken in een geautomatiseerde werkstroom](across-how-use-financials-data-source-flow.md)</span><span class="sxs-lookup"><span data-stu-id="0080c-124">[Using [!INCLUDE[d365fin](includes/d365fin_md.md)] in an Automated Workflow](across-how-use-financials-data-source-flow.md)</span></span>  
<span data-ttu-id="0080c-125">[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="0080c-125">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
[<span data-ttu-id="0080c-126">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="0080c-126">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="0080c-127">[Gebruikers en machtigingen beheren](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="0080c-127">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="0080c-128">[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="0080c-128">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="0080c-129">Financiën</span><span class="sxs-lookup"><span data-stu-id="0080c-129">Finance</span></span>](finance.md)  

