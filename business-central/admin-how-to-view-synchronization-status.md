---
title: De status van een synchronisatie weergeven | Microsoft Docs
description: Leer hoe u de status van een afzonderlijke synchronisatietaak weergeeft.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, sync, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: d55d8d5ab916cee6600deaf891702a625d76d7ee
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "940565"
---
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="de8e8-103">De status van een synchronisatie weergeven</span><span class="sxs-lookup"><span data-stu-id="de8e8-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="de8e8-104">U kunt de status van de afzonderlijke synchronisatietaken weergeven die voor [!INCLUDE[crm_md](includes/crm_md.md)]-integratie zijn uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="de8e8-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="de8e8-105">Hieronder vallen synchronisatietaken die zijn uitgevoerd vanuit de verwerkingswachtrij en handmatige synchronisatietaken die zijn uitgevoerd op records vanuit de [!INCLUDE[d365fin](includes/d365fin_md.md)]-client.</span><span class="sxs-lookup"><span data-stu-id="de8e8-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="de8e8-106">Dit is handig bij het oplossen van synchronisatieproblemen omdat u toegang hebt tot details van specifieke fouten die optreden.</span><span class="sxs-lookup"><span data-stu-id="de8e8-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-all-synchronization-issues"></a><span data-ttu-id="de8e8-107">Alle synchronisatieproblemen weergeven</span><span class="sxs-lookup"><span data-stu-id="de8e8-107">To view all synchronization issues</span></span>
1. <span data-ttu-id="de8e8-108">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Synchronisatiefouten met gekoppelde gegevens** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="de8e8-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="de8e8-109">Op de pagina **Synchronisatiefouten met gekoppelde gegevens** kunt u alle problemen weergeven die zijn opgetreden tijdens de synchronisatie van gegevens tussen [!INCLUDE[crm_md](includes/crm_md.md)] en [!INCLUDE[d365fin](includes/d365fin_md.md)], records op de pagina filteren en sorteren op tabel of foutbericht, en acties ondernemen zoals **Opnieuw** of **Koppeling verwijderen** om problemen een voor een of massaal op te lossen.</span><span class="sxs-lookup"><span data-stu-id="de8e8-109">On the **Coupled Data Synchronization Errors** page you can view of all issues that occurred in synchronization of data between [!INCLUDE[crm_md](includes/crm_md.md)] and [!INCLUDE[d365fin](includes/d365fin_md.md)], filter and sort records in the page by table, error message and take actions such as **Retry** or **Remove Coupling** to resolve issues one by one or in bulk.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="de8e8-110">Het synchronisatielogboek weergeven voor een specifieke (handmatig gesynchroniseerde) record</span><span class="sxs-lookup"><span data-stu-id="de8e8-110">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="de8e8-111">Open bijvoorbeeld de klant-, artikel- of andere record die gegevens synchroniseert tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en Sales</span><span class="sxs-lookup"><span data-stu-id="de8e8-111">Open, for example, customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales</span></span>
2. <span data-ttu-id="de8e8-112">Kies de actie **Synchronisatielogbestand** om het synchronisatielogbestand voor de geselecteerde record weer te geven, bijvoorbeeld een specifieke klant die u handmatig hebt gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="de8e8-112">Choose **Synchronization Log** action to view the synchronization log for selected record, for example, specific customer you synchronized manually</span></span>

## <a name="see-also"></a><span data-ttu-id="de8e8-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="de8e8-113">See Also</span></span>  
[<span data-ttu-id="de8e8-114">Dynamics 365 for Sales-integratie instellen in Business Central</span><span class="sxs-lookup"><span data-stu-id="de8e8-114">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="de8e8-115">Dynamics 365 for Sales gebruiken vanuit Business Central</span><span class="sxs-lookup"><span data-stu-id="de8e8-115">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
