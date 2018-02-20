---
title: De QuickBooks-extensie Migratie gebruiken | Microsoft Docs
description: Beschrijft hoe u de extensie gebruikt om klanten, leveranciers, artikelen en rekeningen van QuickBooks Desktop naar Finance and Operations, Business edition te importeren.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 14e0aea700bbb46a612d8e462ace22b10faac7e2
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="the-quickbooks-data-migration-extension-for-finance-and-operations-business-edition"></a><span data-ttu-id="eba8b-103">De QuickBooks-extensie Gegevensmigratie voor Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="eba8b-103">The QuickBooks Data Migration Extension for Finance and Operations, Business edition</span></span>
<span data-ttu-id="eba8b-104">Met deze extensie kunt u gemakkelijk klanten, leveranciers, artikelen en accounts vanuit QuickBooks naar [!INCLUDE[d365fin](includes/d365fin_md.md)] migreren.</span><span class="sxs-lookup"><span data-stu-id="eba8b-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="eba8b-105">Als uw bedrijf momenteel QuickBooks gebruikt, kunt u de relevante gegevens exporteren en vervolgens een begeleide instelling openen om de gegevens naar [!INCLUDE[d365fin](includes/d365fin_md.md)] te uploaden.</span><span class="sxs-lookup"><span data-stu-id="eba8b-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
<span data-ttu-id="eba8b-106">Zie [Gegevens importeren uit andere financiële systemen](upload-data.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="eba8b-106">For more information, see [Importing Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-quickbooks-desktop"></a><span data-ttu-id="eba8b-107">Gegevens vanuit QuickBooks Desktop exporteren</span><span class="sxs-lookup"><span data-stu-id="eba8b-107">Exporting Data from QuickBooks Desktop</span></span>
<span data-ttu-id="eba8b-108">U moet een gedeelte van of al uw bestaande klanten, leveranciers, voorraadartikelen en accounts exporteren naar een IIF-bestand (Intuit Interchange Format).</span><span class="sxs-lookup"><span data-stu-id="eba8b-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to an Intuit Interchange Format (IIF) file.</span></span> <span data-ttu-id="eba8b-109">De extensie QuickBooks Data Migration bevat een standaardtoewijzing van QuickBooks-gegevens zodat u uw bestaande gegevens kunt gebruiken om uw nieuwe [!INCLUDE[d365fin](includes/d365fin_md.md)]-bedrijf te testen.</span><span class="sxs-lookup"><span data-stu-id="eba8b-109">The QuickBooks Data Migration extension includes a default mapping of QuickBooks data so that you can use your existing data to test your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="eba8b-110">De standaardtoewijzing is in de meeste gevallen voldoende, maar u kunt de toewijzing in de handleiding voor begeleide instelling wijzigen.</span><span class="sxs-lookup"><span data-stu-id="eba8b-110">The default mapping will be sufficient in the vast majority of cases, but you can change the mapping in the assisted setup guide.</span></span>  
<span data-ttu-id="eba8b-111">In QuickBooks bevat het menu Bestand een hulpprogramma om lijsten te exporteren.</span><span class="sxs-lookup"><span data-stu-id="eba8b-111">In QuickBooks, the File menu includes a utility to export lists.</span></span> <span data-ttu-id="eba8b-112">Voor de doelen in [!INCLUDE[d365fin](includes/d365fin_md.md)] kunt u de volgende lijsten exporteren:</span><span class="sxs-lookup"><span data-stu-id="eba8b-112">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following lists:</span></span>

* <span data-ttu-id="eba8b-113">Klantenoverzicht</span><span class="sxs-lookup"><span data-stu-id="eba8b-113">Customer List</span></span>  
* <span data-ttu-id="eba8b-114">Leveranciersoverzicht</span><span class="sxs-lookup"><span data-stu-id="eba8b-114">Vendor List</span></span>  
* <span data-ttu-id="eba8b-115">Artikeloverzicht</span><span class="sxs-lookup"><span data-stu-id="eba8b-115">Item List</span></span>  
* <span data-ttu-id="eba8b-116">Rekeningoverzicht</span><span class="sxs-lookup"><span data-stu-id="eba8b-116">Account List</span></span>  

<span data-ttu-id="eba8b-117">De geëxporteerde gegevens worden opgeslagen als een IIF-bestand dat u vervolgens kunt uploaden naar [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="eba8b-117">The exported data is saved as an IIF file that you can then upload to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="eba8b-118">De extensie QuickBooks-gegevensmigratie vinden</span><span class="sxs-lookup"><span data-stu-id="eba8b-118">Finding the QuickBooks Data Migration Extension</span></span>
<span data-ttu-id="eba8b-119">De extensie QuickBooks-gegevensmigratie is geïnstalleerd en kan worden gebruikt als geïntegreerd onderdeel van de begeleide instelling Gegevensmigratie.</span><span class="sxs-lookup"><span data-stu-id="eba8b-119">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="eba8b-120">Als u klaar bent om aan de slag te gaan en u uw gegevens hebt geëxporteerd vanuit QuickBooks, klikt u op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voert u **Begeleide instelling** in en klikt u op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="eba8b-120">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="eba8b-121">Kies **Bedrijfsgegevens migreren** en voer de stappen in de handleiding uit.</span><span class="sxs-lookup"><span data-stu-id="eba8b-121">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="eba8b-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="eba8b-122">See Also</span></span>
[<span data-ttu-id="eba8b-123">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="eba8b-123">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="eba8b-124">[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="eba8b-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

