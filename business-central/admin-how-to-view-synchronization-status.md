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
ms.openlocfilehash: 11e29674c2d12031fdf4e7f66e767be4fcc74795
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620896"
---
# <a name="view-the-status-of-a-synchronization"></a><span data-ttu-id="e203b-103">De status van een synchronisatie weergeven</span><span class="sxs-lookup"><span data-stu-id="e203b-103">View the Status of a Synchronization</span></span>
<span data-ttu-id="e203b-104">U kunt de status van de afzonderlijke synchronisatietaken weergeven die voor [!INCLUDE[crm_md](includes/crm_md.md)]-integratie zijn uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e203b-104">You can view the status of the individual synchronization jobs that have been run for [!INCLUDE[crm_md](includes/crm_md.md)] integration.</span></span> <span data-ttu-id="e203b-105">Hieronder vallen synchronisatietaken die zijn uitgevoerd vanuit de verwerkingswachtrij en handmatige synchronisatietaken die zijn uitgevoerd op records vanuit de [!INCLUDE[d365fin](includes/d365fin_md.md)]-client.</span><span class="sxs-lookup"><span data-stu-id="e203b-105">This includes synchronization jobs that have been run from the job queue and manual synchronization jobs that were performed on records from [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="e203b-106">Dit is handig bij het oplossen van synchronisatieproblemen omdat u toegang hebt tot details van specifieke fouten die optreden.</span><span class="sxs-lookup"><span data-stu-id="e203b-106">This is helpful when troubleshooting synchronization problems because it gives you access to details about specific errors.</span></span>

### <a name="to-view-synchronization-issues-for-coupled-records"></a><span data-ttu-id="e203b-107">Synchronisatieproblemen weergeven voor gekoppelde records</span><span class="sxs-lookup"><span data-stu-id="e203b-107">To view synchronization issues for coupled records</span></span>
1. <span data-ttu-id="e203b-108">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Synchronisatiefouten met gekoppelde gegevens** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="e203b-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Coupled Data Synchronization Errors**, and then choose the related link.</span></span>
2. <span data-ttu-id="e203b-109">De pagina **Synchronisatiefouten met gekoppelde gegevens** bevat problemen die zijn opgetreden toen u gekoppelde records synchroniseerde.</span><span class="sxs-lookup"><span data-stu-id="e203b-109">The **Coupled Data Synchronization Errors** page shows issues that occurred when you synchronized coupled records.</span></span> <span data-ttu-id="e203b-110">U kunt records filteren en sorteren en acties zoals **Herstellen** of **Records verwijderen** uitvoeren om problemen een voor een op te lossen.</span><span class="sxs-lookup"><span data-stu-id="e203b-110">You can filter and sort records and take actions such as **Restore** or **Delete Records** to resolve issues one by one.</span></span>

### <a name="to-view-synchronization-log-for-specific-manually-synchronized-record"></a><span data-ttu-id="e203b-111">Het synchronisatielogboek weergeven voor een specifieke (handmatig gesynchroniseerde) record</span><span class="sxs-lookup"><span data-stu-id="e203b-111">To view synchronization log for specific (manually synchronized) record</span></span>
1. <span data-ttu-id="e203b-112">Open bijvoorbeeld een klant-, artikel- of andere record die gegevens synchroniseert tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en Sales.</span><span class="sxs-lookup"><span data-stu-id="e203b-112">Open, for example, a customer, item or any other record that is synchronizing data between [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales.</span></span>
2. <span data-ttu-id="e203b-113">Kies de actie **Synchronisatielogbestand** om het synchronisatielogbestand voor een geselecteerde record weer te geven.</span><span class="sxs-lookup"><span data-stu-id="e203b-113">Choose the **Synchronization Log** action to view the synchronization log for a selected record.</span></span> <span data-ttu-id="e203b-114">Bijvoorbeeld een specifieke klant die u handmatig hebt gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="e203b-114">For example, a specific customer you synchronized manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="e203b-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e203b-115">See Also</span></span>  
[<span data-ttu-id="e203b-116">Dynamics 365 for Sales-integratie instellen in Business Central</span><span class="sxs-lookup"><span data-stu-id="e203b-116">Setting Up Dynamics 365 for Sales Integration in Business Central</span></span>](admin-setting-up-integration-with-dynamics-sales.md)  
[<span data-ttu-id="e203b-117">Dynamics 365 for Sales gebruiken vanuit Business Central</span><span class="sxs-lookup"><span data-stu-id="e203b-117">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
