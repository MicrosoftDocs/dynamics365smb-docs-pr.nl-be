---
title: Gegevens uit Dynamics GP migreren met de extensie Gegevensmigratie | Microsoft Docs
description: Gebruik de Dynamics GP-extensie Gegevensmigratie om klanten, leveranciers, voorraadartikelen en rekeningen te migreren van Dynamics GP naar Dynamics 365 for Financials.
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 31b698aea884da162cc18f16a912ebd57e35aed9
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017

---
# <a name="the-dynamics-gp-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="9ece1-103">De extensie Dynamics GP Data Migration voor Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="9ece1-103">The Dynamics GP Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="9ece1-104">Met deze extensie kunt u gemakkelijk klanten, leveranciers, voorraadartikelen en accounts vanuit Dynamics GP naar [!INCLUDE[d365fin](includes/d365fin_md.md)] migreren.</span><span class="sxs-lookup"><span data-stu-id="9ece1-104">This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="9ece1-105">Als uw bedrijf momenteel Dynamics GP gebruikt, kunt u de relevante masterrecords exporteren en vervolgens een handleiding voor begeleide instelling openen om de gegevens toe te voegen aan [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="9ece1-105">If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="9ece1-106">Zie [Bedrijfsgegevens migreren uit andere financiële systemen](upload-data.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="9ece1-106">For more information, see [Migrate Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-dynamics-gp"></a><span data-ttu-id="9ece1-107">Gegevens exporteren uit Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="9ece1-107">Exporting Data from Dynamics GP</span></span>
<span data-ttu-id="9ece1-108">U moet gegevens van sommige of alle bestaande klanten, leveranciers, voorraadartikelen en rekeningen naar een bestand geëxporteerd hebben door middel van de Dynamics GP-functionaliteit voor gegevensexport.</span><span class="sxs-lookup"><span data-stu-id="9ece1-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export.</span></span> <span data-ttu-id="9ece1-109">Voor de doelen in [!INCLUDE[d365fin](includes/d365fin_md.md)] kunt u de volgende soorten gegevens exporteren:</span><span class="sxs-lookup"><span data-stu-id="9ece1-109">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:</span></span>

* <span data-ttu-id="9ece1-110">Rekening</span><span class="sxs-lookup"><span data-stu-id="9ece1-110">Account</span></span>  
* <span data-ttu-id="9ece1-111">Klant</span><span class="sxs-lookup"><span data-stu-id="9ece1-111">Customer</span></span>  
* <span data-ttu-id="9ece1-112">Artikel</span><span class="sxs-lookup"><span data-stu-id="9ece1-112">Item</span></span>  
* <span data-ttu-id="9ece1-113">Leverancier</span><span class="sxs-lookup"><span data-stu-id="9ece1-113">Vendor</span></span>  

<span data-ttu-id="9ece1-114">De extensie Dynamics GP Data Migration wijst automatisch de geëxporteerde gegevens toe, zodat de gegevens snel beschikbaar zijn in uw nieuwe [!INCLUDE[d365fin](includes/d365fin_md.md)]-bedrijf.</span><span class="sxs-lookup"><span data-stu-id="9ece1-114">The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="9ece1-115">Tijdens het proces worden ondersteunende configuratiegegevens gemaakt, zoals boekingsgroepen.</span><span class="sxs-lookup"><span data-stu-id="9ece1-115">During the process, supporting setup information is created, such as posting groups.</span></span> <span data-ttu-id="9ece1-116">Voorraadartikelen worden in het systeem ingevoerd met FIFO als methode voor kostenwaardering.</span><span class="sxs-lookup"><span data-stu-id="9ece1-116">Inventory items will be brought into the system with FIFO as the cost valuation method.</span></span> <span data-ttu-id="9ece1-117">Rekeningen worden ingesteld als de hoofdrekeningsegment uit Dynamics GP met dimensies, omdat [!INCLUDE[d365fin](includes/d365fin_long_md.md)] geen rekeningsegmenten kent.</span><span class="sxs-lookup"><span data-stu-id="9ece1-117">Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.</span></span>

## <a name="see-also"></a><span data-ttu-id="9ece1-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9ece1-118">See Also</span></span>
[<span data-ttu-id="9ece1-119">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="9ece1-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="9ece1-120">[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="9ece1-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

