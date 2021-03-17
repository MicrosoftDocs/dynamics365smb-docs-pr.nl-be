---
title: Veel artikelafbeeldingen uit een ZIP-bestand importeren | Microsoft Docs
description: U kunt meerdere artikelafbeeldingen in één keer importeren. Geef uw afbeeldingsbestanden namen die corresponderen met uw artikelnummers, comprimeer ze in een zip-bestand en gebruik vervolgens de pagina Artikelafbeeldingen importeren om te bepalen welke artikelafbeeldingen worden geïmporteerd.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: product, image
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 116475162c9a6fb275772e0447fd456b7e1627bf
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393111"
---
# <a name="import-multiple-item-pictures"></a><span data-ttu-id="ff345-104">Meerdere artikelafbeeldingen importeren</span><span class="sxs-lookup"><span data-stu-id="ff345-104">Import Multiple Item Pictures</span></span>
<span data-ttu-id="ff345-105">U kunt meerdere artikelafbeeldingen in één keer importeren.</span><span class="sxs-lookup"><span data-stu-id="ff345-105">You can import multiple item pictures in one go.</span></span> <span data-ttu-id="ff345-106">Geef uw afbeeldingsbestanden namen die corresponderen met uw artikelnummers, comprimeer ze in een zip-bestand en gebruik vervolgens de pagina **Artikelafbeeldingen importeren** om te bepalen welke artikelafbeeldingen worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="ff345-106">Simply name your picture files with names corresponding to your item numbers, compress them to a ZIP file, and then use the **Import Item Pictures** page to manage which item pictures to import.</span></span>

<span data-ttu-id="ff345-107">Alle algemene bestandsindelingen worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="ff345-107">All common file formats are supported.</span></span>

## <a name="to-name-picture-files-by-the-item-names-and-prepare-the-zip-file"></a><span data-ttu-id="ff345-108">Afbeeldingsbestanden noemen naar de artikelnamen en het ZIP-bestand voorbereiden</span><span class="sxs-lookup"><span data-stu-id="ff345-108">To name picture files by the item names and prepare the ZIP file</span></span>
1. <span data-ttu-id="ff345-109">Benoem elk bestand op de locatie waar uw artikelafbeeldingen zijn opgeslagen volgens het nummer van het gerelateerde artikel.</span><span class="sxs-lookup"><span data-stu-id="ff345-109">At the location where your item pictures are stored, name each files according to the number of the related item.</span></span> <span data-ttu-id="ff345-110">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="ff345-110">For example:</span></span>

    |<span data-ttu-id="ff345-111">Artikelnr.</span><span class="sxs-lookup"><span data-stu-id="ff345-111">Item No.</span></span>|<span data-ttu-id="ff345-112">Bestandsnaam</span><span class="sxs-lookup"><span data-stu-id="ff345-112">File Name</span></span>|
    |-|-|
    |<span data-ttu-id="ff345-113">1000</span><span class="sxs-lookup"><span data-stu-id="ff345-113">1000</span></span>|<span data-ttu-id="ff345-114">1000.bmp</span><span class="sxs-lookup"><span data-stu-id="ff345-114">1000.bmp</span></span>|
    |<span data-ttu-id="ff345-115">1001</span><span class="sxs-lookup"><span data-stu-id="ff345-115">1001</span></span>|<span data-ttu-id="ff345-116">1001.bmp</span><span class="sxs-lookup"><span data-stu-id="ff345-116">1001.bmp</span></span>|
    |<span data-ttu-id="ff345-117">1002</span><span class="sxs-lookup"><span data-stu-id="ff345-117">1002</span></span>|<span data-ttu-id="ff345-118">1002.bmp</span><span class="sxs-lookup"><span data-stu-id="ff345-118">1002.bmp</span></span>|

2. <span data-ttu-id="ff345-119">Verzamel alle bestanden in een ZIP-bestand.</span><span class="sxs-lookup"><span data-stu-id="ff345-119">Collect all the files in a ZIP file.</span></span> <span data-ttu-id="ff345-120">Selecteer bijvoorbeeld in Windows Verkenner de bestanden, en kies **Verzenden naar**, **Gecomprimeerde (gezipte) map**.</span><span class="sxs-lookup"><span data-stu-id="ff345-120">For example, in Windows Explorer, select the files, and then choose **Send to**, **Compressed (zipped) folder**.</span></span>     

## <a name="to-import-item-pictures"></a><span data-ttu-id="ff345-121">Artikelafbeeldingen importeren</span><span class="sxs-lookup"><span data-stu-id="ff345-121">To import item pictures</span></span>
1. <span data-ttu-id="ff345-122">Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraad instellen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="ff345-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Inventory Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="ff345-123">Kies de actie **Artikelafbeeldingen importeren**.</span><span class="sxs-lookup"><span data-stu-id="ff345-123">Choose the **Import Item Pictures** action.</span></span>
3. <span data-ttu-id="ff345-124">Selecteer in het veld **Een ZIP-bestand selecteren** de relevante ZIP-map en kies de knop **Openen**.</span><span class="sxs-lookup"><span data-stu-id="ff345-124">In the **Select a ZIP file** field, select the relevant ZIP folder, and then choose the **Open** button.</span></span>

    <span data-ttu-id="ff345-125">Er wordt een regel voor elk artikel en afbeelding gemaakt op de pagina **Artikelafbeeldingen importeren**.</span><span class="sxs-lookup"><span data-stu-id="ff345-125">A line for each item and picture is created on the **Import Item Pictures** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ff345-126">Voor artikelkaarten die al een afbeelding hebben, wordt het selectievakje **Afbeelding bestaat al** geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="ff345-126">For item cards that already have a picture, the **Picture Already Exists** check box is selected.</span></span> <span data-ttu-id="ff345-127">Als u geen bestaande afbeeldingen wilt vervangen, schakelt u het selectievakje **Afbeeldingen vervangen** uit.</span><span class="sxs-lookup"><span data-stu-id="ff345-127">If you do not want any existing pictures to be replaced, deselect the **Replace Pictures** check box.</span></span> <span data-ttu-id="ff345-128">Als u geen afzonderlijke bestaande afbeeldingen wilt vervangen, verwijdert u de desbetreffende regels.</span><span class="sxs-lookup"><span data-stu-id="ff345-128">If you do not want individual existing pictures to be replaced, delete the lines in question.</span></span>

3. <span data-ttu-id="ff345-129">Kies de actie **Afbeeldingen importeren**.</span><span class="sxs-lookup"><span data-stu-id="ff345-129">Choose the **Import Pictures** action.</span></span>

<span data-ttu-id="ff345-130">Het veld **Status importeren** wordt bijgewerkt om aan te geven of de afbeeldingsimport is voltooid of overgeslagen.</span><span class="sxs-lookup"><span data-stu-id="ff345-130">The **Import Status** field is updated to show if the picture import was skipped or completed.</span></span>       

## <a name="see-also"></a><span data-ttu-id="ff345-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ff345-131">See Also</span></span>
[<span data-ttu-id="ff345-132">Nieuwe artikelen registreren</span><span class="sxs-lookup"><span data-stu-id="ff345-132">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="ff345-133">Nummerreeksen maken</span><span class="sxs-lookup"><span data-stu-id="ff345-133">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="ff345-134">Voorraad</span><span class="sxs-lookup"><span data-stu-id="ff345-134">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="ff345-135">Inkoop</span><span class="sxs-lookup"><span data-stu-id="ff345-135">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="ff345-136">Verkoop</span><span class="sxs-lookup"><span data-stu-id="ff345-136">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="ff345-137">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ff345-137">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]