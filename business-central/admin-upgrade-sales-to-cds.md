---
title: Een integratie met Dynamics 365 Sales upgraden
description: Leer hoe u uw Dynamics 365 Business Central-integratie met Dynamics 365 Sales naar de nieuwste versie overzet.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales, crm, integration, integrating
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 772052fc88e0b8be7ec5276600b0c237e2d2f8b2
ms.sourcegitcommit: a76475f124e79440a5bba20577b335c4d50a2d83
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025820"
---
# <a name="upgrading-an-integration-with-dynamics-365-sales"></a><span data-ttu-id="42ddd-103">Een integratie met Dynamics 365 Sales upgraden</span><span class="sxs-lookup"><span data-stu-id="42ddd-103">Upgrading an Integration with Dynamics 365 Sales</span></span>
[!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="42ddd-104">integreert ook met [!INCLUDE[prod_short](includes/cds_long_md.md)], waardoor het eenvoudig is om gegevens te verbinden en te synchroniseren met andere Dynamics 365-toepassingen, zoals [!INCLUDE[crm_md](includes/crm_md.md)], of zelfs apps die u zelf bouwt.</span><span class="sxs-lookup"><span data-stu-id="42ddd-104">integrates with [!INCLUDE[prod_short](includes/cds_long_md.md)], which makes it easy to connect and synchronize data with other Dynamics 365 applications, such as [!INCLUDE[crm_md](includes/crm_md.md)], or even apps that you build yourself.</span></span> <span data-ttu-id="42ddd-105">Als u voor de eerste keer integreert, raden we u aan dit te doen via [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="42ddd-105">If you are integrating for the first time, we recommend that you do so through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> <span data-ttu-id="42ddd-106">Zie voor meer informatie [Integratie met Dataverse](admin-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="42ddd-106">For more information, see [Integration with Dataverse](admin-common-data-service.md).</span></span>

<span data-ttu-id="42ddd-107">Als u al [!INCLUDE[crm_md](includes/crm_md.md)] hebt geïntegreerd met [!INCLUDE[prod_short](includes/prod_short.md)], kunt u gegevens blijven synchroniseren met uw setup.</span><span class="sxs-lookup"><span data-stu-id="42ddd-107">If you have already integrated [!INCLUDE[crm_md](includes/crm_md.md)] with [!INCLUDE[prod_short](includes/prod_short.md)], you can continue to synchronize data using your setup.</span></span> <span data-ttu-id="42ddd-108">Als u echter een upgrade op [!INCLUDE[prod_short](includes/prod_short.md)] uitvoert of uw [!INCLUDE[crm_md](includes/crm_md.md)]-integratie uitschakelt, moet u om het weer in te schakelen verbinding maken via [!INCLUDE[prod_short](includes/cds_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="42ddd-108">However, if you upgrade [!INCLUDE[prod_short](includes/prod_short.md)], or turn off your [!INCLUDE[crm_md](includes/crm_md.md)] integration, to turn it on again you must connect through [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span> 

> [!NOTE]
> <span data-ttu-id="42ddd-109">Opnieuw verbinding maken via [!INCLUDE[prod_short](includes/cds_long_md.md)] past standaard synchronisatie-instellingen toe en overschrijft alle configuraties die u hebt.</span><span class="sxs-lookup"><span data-stu-id="42ddd-109">Reconnecting through [!INCLUDE[prod_short](includes/cds_long_md.md)] will apply default synchronization settings, and will overwrite any configurations you have.</span></span> <span data-ttu-id="42ddd-110">Zo worden de standaardtabeltoewijzingen toegepast.</span><span class="sxs-lookup"><span data-stu-id="42ddd-110">For example, the default table mappings will be applied.</span></span>

## <a name="to-upgrade-your-connection-to-use-dataverse"></a><span data-ttu-id="42ddd-111">Uw verbinding upgraden om Dataverse te gebruiken</span><span class="sxs-lookup"><span data-stu-id="42ddd-111">To upgrade your connection to use Dataverse</span></span>
1. <span data-ttu-id="42ddd-112">Open de pagina **Microsoft Dynamics 365-verbinding instellen** en zet de schakelaar **Ingeschakeld** uit om de verbinding met [!INCLUDE[crm_md](includes/crm_md.md)] te verbreken.</span><span class="sxs-lookup"><span data-stu-id="42ddd-112">Open the **Microsoft Dynamics 365 Connection Setup** page, and then turn off the **Enabled** toggle to disconnect from [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
2. <span data-ttu-id="42ddd-113">Open de pagina **Dataverse-verbinding instellen** en kies de schakelaar **Ingeschakeld** om de verbinding met [!INCLUDE[prod_short](includes/cds_long_md.md)] in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="42ddd-113">Open the **Dataverse Connection Setup** page, and choose the **Enabled** toggle to turn on the connection to [!INCLUDE[prod_short](includes/cds_long_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="42ddd-114">Nadat u de verbinding hebt ingeschakeld, wordt de Business Central-integratieoplossing geïmplementeerd naar Dataverse.</span><span class="sxs-lookup"><span data-stu-id="42ddd-114">After you enable the connection, the Business Central Integration Solution is deployed to Dataverse.</span></span>
3. <span data-ttu-id="42ddd-115">Kies **Integratieoplossing opnieuw implementeren** om de Business Central-integratieoplossing opnieuw te installeren.</span><span class="sxs-lookup"><span data-stu-id="42ddd-115">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
4. <span data-ttu-id="42ddd-116">Ga naar de pagina **Microsoft Dynamics 365-verbinding instellen** en zet de schakelaar **Ingeschakeld** aan om weer verbinding te maken met [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="42ddd-116">On the **Microsoft Dynamics 365 Connection Setup** page, turn on the **Enabled** toggle to reconnect to [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>
  
   > [!NOTE]
   > <span data-ttu-id="42ddd-117">Nadat u de verbinding hebt ingeschakeld, wordt de Business Central-integratieoplossing geïmplementeerd naar [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="42ddd-117">After you enable the connection, the Business Central Integration Solution is deployed to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="42ddd-118">Dit maakt integratie mogelijk met tabellen die specifiek zijn voor [!INCLUDE[crm_md](includes/crm_md.md)], zoals verkooporders, offertes en facturen.</span><span class="sxs-lookup"><span data-stu-id="42ddd-118">This enables integration with tables that are specific to [!INCLUDE[crm_md](includes/crm_md.md)], such as sales orders, quotes, and invoices.</span></span>
5. <span data-ttu-id="42ddd-119">Kies **Integratieoplossing opnieuw implementeren** om de Business Central-integratieoplossing opnieuw te installeren.</span><span class="sxs-lookup"><span data-stu-id="42ddd-119">Choose **Redeploy Integration Solution** to reinstall the Business Central Integration Solution.</span></span>
6. <span data-ttu-id="42ddd-120">Kies op de pagina **Sales-verbinding instellen** **Standaardsynchronisatie-instellingen** om de integratietabeltoewijzingen te initialiseren voor [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="42ddd-120">On the **Sales Connection Setup** page, choose **Use Default Synchronization Setup** to initialize the integration table mappings for [!INCLUDE[crm_md](includes/crm_md.md)].</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="42ddd-121">Als de actie **Standaardsynchronisatie-instellingen gebruiken** wordt gebruikt, worden de standaardtoewijzingen van de integratietabel toegepast.</span><span class="sxs-lookup"><span data-stu-id="42ddd-121">Using the **Use Default Synchronization Setup** action will apply the default integration table mappings.</span></span> <span data-ttu-id="42ddd-122">Alle aangepaste toewijzingen worden overschreven.</span><span class="sxs-lookup"><span data-stu-id="42ddd-122">All custom mappings will be overwritten.</span></span> <span data-ttu-id="42ddd-123">Als u aangepaste toewijzingen hebt die u wilt behouden, raden we u aan deze naar Excel te exporteren of met uw Microsoft-partner te overleggen over andere manieren om uw aangepaste toewijzingen te behouden.</span><span class="sxs-lookup"><span data-stu-id="42ddd-123">If you have custom mappings that you want to keep, we recommend that you export them to Excel or talk to your Microsoft partner about other ways to keep your custom mappings.</span></span>    

## <a name="see-also"></a><span data-ttu-id="42ddd-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="42ddd-124">See Also</span></span>
[<span data-ttu-id="42ddd-125">Integreren met Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="42ddd-125">Integrating with Dynamics 365 Sales</span></span>](admin-prepare-dynamics-365-for-sales-for-integration.md)  
[<span data-ttu-id="42ddd-126">Integreren met Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="42ddd-126">Integrating with Microsoft Dataverse</span></span>](admin-common-data-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]