---
title: De QuickBooks-extensie Migratie gebruiken | Microsoft Docs
description: Beschrijft hoe u de extensie gebruikt om klanten, leveranciers, artikelen en rekeningen van QuickBooks Desktop naar Dynamics 365 Financials te importeren.
services: project-madeira
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
ms.openlocfilehash: 37d90316ea0be5489fb5abe33645de3fe0d3cf90
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017

---
# <a name="the-quickbooks-data-migration-extension-for-dynamics-365-for-financials"></a><span data-ttu-id="821e1-103">De extensie QuickBooks Data Migration voor Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="821e1-103">The QuickBooks Data Migration Extension for Dynamics 365 for Financials</span></span>
<span data-ttu-id="821e1-104">Met deze extensie kunt u gemakkelijk klanten, leveranciers, artikelen en accounts vanuit QuickBooks naar [!INCLUDE[d365fin](includes/d365fin_md.md)] migreren.</span><span class="sxs-lookup"><span data-stu-id="821e1-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="821e1-105">Als uw bedrijf momenteel QuickBooks gebruikt, kunt u de relevante gegevens exporteren en vervolgens een begeleide instelling openen om de gegevens naar [!INCLUDE[d365fin](includes/d365fin_md.md)] te uploaden.</span><span class="sxs-lookup"><span data-stu-id="821e1-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="821e1-106">Zie [Gegevens importeren uit andere financiële systemen](upload-data.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="821e1-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks"></a><span data-ttu-id="821e1-107">Gegevens vanuit QuickBooks exporteren</span><span class="sxs-lookup"><span data-stu-id="821e1-107">Exporting Data from QuickBooks</span></span>
<span data-ttu-id="821e1-108">U moet een gedeelte van of al uw bestaande klanten, leveranciers, voorraadartikelen en accounts exporteren naar een IIF-bestand (Intuit Interchange Format).</span><span class="sxs-lookup"><span data-stu-id="821e1-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="821e1-109">De extensie QuickBooks Data Migration bevat een standaardtoewijzing van QuickBooks-gegevens zodat u uw bestaande gegevens kunt gebruiken om uw nieuwe [!INCLUDE[d365fin](includes/d365fin_md.md)]-bedrijf te testen.</span><span class="sxs-lookup"><span data-stu-id="821e1-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="821e1-110">De standaardtoewijzing is in de meeste gevallen voldoende, maar u kunt de toewijzing in de handleiding voor begeleide instelling wijzigen.</span><span class="sxs-lookup"><span data-stu-id="821e1-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="821e1-111">In QuickBooks bevat het menu Bestand een hulpprogramma om lijsten te exporteren.</span><span class="sxs-lookup"><span data-stu-id="821e1-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="821e1-112">Voor de doelen in [!INCLUDE[d365fin](includes/d365fin_md.md)] kunt u de volgende lijsten exporteren:</span><span class="sxs-lookup"><span data-stu-id="821e1-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="821e1-113">Klantenoverzicht</span><span class="sxs-lookup"><span data-stu-id="821e1-113">Customer List</span></span>  
* <span data-ttu-id="821e1-114">Leveranciersoverzicht</span><span class="sxs-lookup"><span data-stu-id="821e1-114">Vendor List</span></span>  
* <span data-ttu-id="821e1-115">Artikeloverzicht</span><span class="sxs-lookup"><span data-stu-id="821e1-115">Item List</span></span>  
* <span data-ttu-id="821e1-116">Rekeningoverzicht</span><span class="sxs-lookup"><span data-stu-id="821e1-116">Account List</span></span>  

<span data-ttu-id="821e1-117">De geëxporteerde gegevens worden opgeslagen als een IIF-bestand dat u vervolgens kunt uploaden naar [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="821e1-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="821e1-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="821e1-118">See Also</span></span>
[<span data-ttu-id="821e1-119">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="821e1-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="821e1-120">[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies ](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="821e1-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

