---
title: Business Central Intelligente cloud-extensies voor Cloudmigratie | Microsoft Docs
description: Gebruik de cloudmigratie-extensies om uw on-premises gegevens naar Business Central online te migreren. Deze extensies verplaatsen uw on-premises gegevens naar de cloud, zodat u Business Central online kunt gebruiken met uw bestaande gegevens.
author: jenolson
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.reviewer: edupont
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: f2d8d556ca4628a66c10f323f47137cd35732a68
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757304"
---
# <a name="intelligent-cloud-extensions-for-cloud-migration"></a><span data-ttu-id="b11a3-104">Intelligente cloud-extensies voor cloudmigratie</span><span class="sxs-lookup"><span data-stu-id="b11a3-104">Intelligent Cloud Extensions for Cloud Migration</span></span>

<span data-ttu-id="b11a3-105">Afhankelijk van uw on-premises oplossing moet u verschillende extensies gebruiken om uw gegevens te verbinden met [!INCLUDE[prod_short](includes/prod_short.md)] online om uw oplossing naar de cloud te migreren.</span><span class="sxs-lookup"><span data-stu-id="b11a3-105">Depending on your on-premises solution, you must use different extensions to connect your data with [!INCLUDE[prod_short](includes/prod_short.md)] online for purposes of migrating your solution to the cloud.</span></span>  

<span data-ttu-id="b11a3-106">Als u een van de ondersteunde on-premises producten gebruikt, kunt u uw cloudomgeving configureren op basis van een productspecifieke extensie.</span><span class="sxs-lookup"><span data-stu-id="b11a3-106">If you are using one of the supported on-premises products, you can configure your cloud environment based on a product-specific extension.</span></span> <span data-ttu-id="b11a3-107">Zodra uw cloudomgeving is geconfigureerd, kunt u gegevens migreren van uw on-premises oplossing naar [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b11a3-107">Once your cloud environment is configured, you will be able to migrate data from your on-premises solution to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="b11a3-108">Zo kunt u optimaal gebruikmaken van wat de cloud uw bedrijf te bieden heeft, zoals verbeterde inzichten in uw bedrijf, kunstmatige intelligentie, toegang met meerdere apparaten en overal en altijd toegang.</span><span class="sxs-lookup"><span data-stu-id="b11a3-108">This will enable you to take full advantage of what the cloud has to offer your business such as, enhanced insights into your business, artificial intelligence, multiple device access, and anytime, anywhere access.</span></span>  

<span data-ttu-id="b11a3-109">Zie voor meer informatie [On-premises gegevens migreren naar Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in de beheerinhoud voor [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="b11a3-109">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="business-central-on-premises"></a><span data-ttu-id="b11a3-110">Business Central on-premises</span><span class="sxs-lookup"><span data-stu-id="b11a3-110">Business Central on-premises</span></span>

<span data-ttu-id="b11a3-111">Als u een on-premises implementatie van [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt, verkrijgt u de extensie **Intelligente cloud Basis** en de extensie **Business Central Intelligente cloud** en voert u vervolgens de begeleide instelling **Instelling van Cloudmigratie** uit.</span><span class="sxs-lookup"><span data-stu-id="b11a3-111">If you are using an on-premises deployment of [!INCLUDE[prod_short](includes/prod_short.md)], get the **Intelligent Cloud Base** extension and the **Business Central Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="dynamics-gp"></a><span data-ttu-id="b11a3-112">Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="b11a3-112">Dynamics GP</span></span>

<span data-ttu-id="b11a3-113">Als u Dynamics GP gebruikt, verkrijgt u de **extensie Intelligente cloud Basis** en de **extensie Dynamics GP Intelligente cloud** en voert u vervolgens de begeleide instelling **Instelling van Cloudmigratie** uit.</span><span class="sxs-lookup"><span data-stu-id="b11a3-113">If you are using Dynamics GP,  get the **Intelligent Cloud Base Extension** extension and the **Dynamics GP Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="b11a3-114">Migreren van Dynamics GP met behulp van de begeleide instelling **Instelling van Cloudmigratie** wordt momenteel alleen ondersteund voor de volgende markten: Verenigde Staten, Canada, Verenigd Koninkrijk.</span><span class="sxs-lookup"><span data-stu-id="b11a3-114">Migrating from Dynamics GP using the **Cloud Migration Setup** assisted setup guide is currently only supported for the following markets: United States, Canada, United Kingdom.</span></span>

## <a name="dynamics-sl"></a><span data-ttu-id="b11a3-115">Dynamics SL</span><span class="sxs-lookup"><span data-stu-id="b11a3-115">Dynamics SL</span></span>

<span data-ttu-id="b11a3-116">Als u Dynamics SL gebruikt, verkrijgt u de extensie **Intelligente cloud Basis**, de extensie **Microsoft Dynamics SL Intelligente cloud** en de extensie **Microsoft Dynamics SL-historie slimme lijsten** en voert u vervolgens de begeleide instelling **Instelling van Cloudmigratie** uit.</span><span class="sxs-lookup"><span data-stu-id="b11a3-116">If you are using Dynamics SL, get the **Intelligent Cloud Base** extension, the **Microsoft Dynamics SL Intelligent Cloud** extension and the **Microsoft Dynamics SL History SmartLists** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b11a3-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b11a3-117">See Also</span></span>

[<span data-ttu-id="b11a3-118">Intelligente inzichten</span><span class="sxs-lookup"><span data-stu-id="b11a3-118">Intelligent Insights</span></span>](about-intelligent-cloud.md)  
[<span data-ttu-id="b11a3-119">Extensie Intelligente cloud Basis</span><span class="sxs-lookup"><span data-stu-id="b11a3-119">Intelligent Cloud Base Extension</span></span>](ui-extensions-intelligent-cloud.md)  
