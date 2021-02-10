---
title: Gegevens migreren vanuit Dynamics GP vóór 15.3 | Microsoft Docs
description: Vóór update 15.3 kon u de Dynamics GP-extensie Gegevensmigratie gebruiken om klanten, leveranciers, voorraadartikelen, grootboekrekeningen, openstaande schulden en openstaande tegoeden te migreren van Dynamics GP naar Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2020
ms.author: edupont
ROBOTS: NOINDEX
ms.openlocfilehash: a8f6c35d031cdbe6376ed57ea9ba2e9ce79188b4
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757279"
---
# <a name="the-dynamics-gp-data-migration-extension"></a><span data-ttu-id="1f2c9-103">De Dynamics GP-extensie Gegevensmigratie</span><span class="sxs-lookup"><span data-stu-id="1f2c9-103">The Dynamics GP Data Migration Extension</span></span>

> [!NOTE]
> <span data-ttu-id="1f2c9-104">De extensie is buiten gebruik gesteld in update 15.3.</span><span class="sxs-lookup"><span data-stu-id="1f2c9-104">This extension is deprecated in the 15.3 update.</span></span> <span data-ttu-id="1f2c9-105">We raden gebruikers die willen migreren vanuit Dynamics GP aan om in plaats daarvan de wizard **Cloudmigratie** te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="1f2c9-105">We recommend that users who want to migrate from Dynamics GP start using the **Cloud Migration** wizard instead.</span></span> <span data-ttu-id="1f2c9-106">De extensie **Cloudmigratie** heeft meer robuuste functionaliteit en brengt meer gegevens naar Business Central over vanuit Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="1f2c9-106">The **Cloud Migration** extension has more robust functionality and brings more data into Business Central from Dynamics GP.</span></span> <span data-ttu-id="1f2c9-107">Zie voor meer informatie [Business Central Online migreren vanuit Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) in de beheerinhoud voor [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1f2c9-107">For more information, see [Migrate to Business Central Online from Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="1f2c9-108">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1f2c9-108">See Also</span></span>

[<span data-ttu-id="1f2c9-109">Intelligente cloud-extensies voor cloudmigratie</span><span class="sxs-lookup"><span data-stu-id="1f2c9-109">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="1f2c9-110">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="1f2c9-110">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="1f2c9-111">[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="1f2c9-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="1f2c9-112">Naar Business Central Online migreren vanuit Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="1f2c9-112">Migrate to Business Central Online from Dynamics GP</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp)  
