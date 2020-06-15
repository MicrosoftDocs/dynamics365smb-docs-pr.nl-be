---
title: Een integratie met Dynamics 365 Sales upgraden | Microsoft Docs
description: Leren hoe u Dynamics 365 Business Central voorbereidt op integratie met Dynamics 365 Sales.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 2a5f58ac904ea05f4410ac9e1b804df1cb01c609
ms.sourcegitcommit: 4545bb597dd9dc4c563b30af762977ee1d815497
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410680"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="0e44c-103">Een integratie met Dynamics 365 Sales upgraden</span><span class="sxs-lookup"><span data-stu-id="0e44c-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="0e44c-104">integreert ook met [!INCLUDE[d365fin](includes/cds_long_md.md)], waardoor het eenvoudig is om gegevens te verbinden en te synchroniseren met andere Dynamics 365-toepassingen, zoals [!INCLUDE[crm_md](includes/crm_md.md)], of zelfs apps die u zelf bouwt.</span><span class="sxs-lookup"><span data-stu-id="0e44c-104">integrates with [!INCLUDE[d365fin](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="0e44c-105">Als u voor de eerste keer integreert, raden we u aan dit te doen via [!INCLUDE[d365fin](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0e44c-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> <span data-ttu-id="0e44c-106">Zie voor meer informatie [Integratie met Common Data Service](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="0e44c-106">For more information, see [Integration with Common Data Service](admin-common-data-service.md).</span></span>

<span data-ttu-id="0e44c-107">Als u al [!INCLUDE[crm_md](includes/crm_md.md)] hebt geïntegreerd met [!INCLUDE[d365fin](includes/d365fin_md.md)], kunt u gegevens blijven synchroniseren met uw setup.</span><span class="sxs-lookup"><span data-stu-id="0e44c-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="0e44c-108">Als u echter een upgrade op [!INCLUDE[d365fin](includes/d365fin_md.md)] uitvoert of uw [!INCLUDE[crm_md](includes/crm_md.md)]-integratie uitschakelt, moet u om het weer in te schakelen verbinding maken via [!INCLUDE[d365fin](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0e44c-108">However, if you upgrade [!INCLUDE[d365fin](includes/d365fin_md.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[d365fin](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="0e44c-109">Opnieuw verbinding maken via [!INCLUDE[d365fin](includes/cds_long_md.md)] past standaard synchronisatie-instellingen toe en overschrijft alle configuraties die u hebt.</span><span class="sxs-lookup"><span data-stu-id="0e44c-109">Reconnecting through [!INCLUDE[d365fin](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="0e44c-110">Zo worden de standaardtabeltoewijzingen toegepast.</span><span class="sxs-lookup"><span data-stu-id="0e44c-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-common-data-service"></a><span data-ttu-id="0e44c-111">Uw verbinding upgraden om Common Data Service te gebruiken</span><span class="sxs-lookup"><span data-stu-id="0e44c-111">To upgrade your connection to use Common Data Service</span></span>
1. <span data-ttu-id="0e44c-112">Open de pagina **Microsoft Dynamics 365-verbinding instellen**, kies de schakelaar **Inschakelen** om uw bestaande verbinding met [!INCLUDE[crm_md](includes/crm_md.md)] uit te schakelen.</span><span class="sxs-lookup"><span data-stu-id="0e44c-112">Open the **Microsoft Dynamics 365 Connection Setup** page, choose the **Enable** toggle to turn off your existing connection to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="0e44c-113">Open de pagina **Common Data Service-verbinding instellen** en kies de schakelaar **Inschakelen** om de verbinding in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="0e44c-113">Open the **Common Data Service Connection Setup** page, and choose the **Enable** toggle to turn on the connection.</span></span>
  
   <span data-ttu-id="0e44c-114">Nadat u de CDS-verbinding hebt ingeschakeld, wordt de Business Central CDS-basisintegratieoplossing geïmplementeerd naar Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="0e44c-114">After you enable the CDS connection, the Business Central CDS Base Integration Solution is deployed to Common Data Service.</span></span>
3. <span data-ttu-id="0e44c-115">Verwijder de Microsoft Dynamics 365 Business Central Integratie-oplossing uit uw Dynamics 365 Sales volgens [Een oplossingsonderwerp de-installeren of verwijderen](/powerapps/developer/common-data-service/uninstall-delete-solution)</span><span class="sxs-lookup"><span data-stu-id="0e44c-115">Uninstall the Microsoft Dynamics 365 Business Central Integration solution from your Dynamics 365 Sales following [Uninstall or delete a solution topic](/powerapps/developer/common-data-service/uninstall-delete-solution)</span></span> 

4. <span data-ttu-id="0e44c-116">Kies op de pagina Microsoft Dynamics 365-verbinding instellen de schakelaar Inschakelen om de verbinding met [!INCLUDE[crm_md](includes/crm_md.md)] in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="0e44c-116">On the Microsoft Dynamics 365 Connection Setup page, choose the Enable toggle to turn on the connection to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   <span data-ttu-id="0e44c-117">Nadat u de Sales-verbinding hebt ingeschakeld, wordt de Business Central-integratieoplossing geïmplementeerd naar Sales.</span><span class="sxs-lookup"><span data-stu-id="0e44c-117">After you enable the Sales connection, the Business Central Integration Solution is deployed to Sales.</span></span> <span data-ttu-id="0e44c-118">Dit maakt integratie mogelijk met entiteiten die specifiek zijn voor [!INCLUDE[crm_md](includes/crm_md.md)], zoals verkooporders, offertes en facturen.</span><span class="sxs-lookup"><span data-stu-id="0e44c-118">This enables integration with entities that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="0e44c-119">Kies **Integratieoplossing opnieuw implementeren** om de bijgewerkte Business Central-integratieoplossing te installeren en configureren.</span><span class="sxs-lookup"><span data-stu-id="0e44c-119">Choose **Redeploy Integration Solution** to install and configure the upgraded Business Central Integration Solution.</span></span>
6. <span data-ttu-id="0e44c-120">Kies op de pagina **Sales-verbinding instellen** **Standaardsynchronisatie-instellingen** om de integratietabeltoewijzingen te initialiseren voor [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="0e44c-120">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="0e44c-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0e44c-121">See Also</span></span>
[<span data-ttu-id="0e44c-122">Integreren met Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="0e44c-122">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="0e44c-123">Integreren met Common Data Service</span><span class="sxs-lookup"><span data-stu-id="0e44c-123">Integrating with Common Data Service</span></span>](admin-common-data-service.md)
