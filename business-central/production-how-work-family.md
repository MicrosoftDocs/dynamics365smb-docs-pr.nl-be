---
title: Artikelfamilies gebruiken in productie | Microsoft Docs
description: De belangrijkste taak bij het aanpassen van een basisagenda voor uw bedrijf of voor een van uw zakelijke partners is het invoeren van wijzigingen in de statuswaarden Werkdag en Vrije dag.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 4e89cee3fb8b3c079cebf0665a1e068ac1f46fae
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="work-with-production-families"></a><span data-ttu-id="8c393-103">Werken met productfamilies</span><span class="sxs-lookup"><span data-stu-id="8c393-103">Work with Production Families</span></span>
<span data-ttu-id="8c393-104">Een productfamilie is een verzameling afzonderlijke artikelen die vanwege een vergelijkbaar productieproces onderling gerelateerd zijn.</span><span class="sxs-lookup"><span data-stu-id="8c393-104">A production family is a group of individual items whose relationship is based on the similarity of their manufacturing processes.</span></span> <span data-ttu-id="8c393-105">Door de vorming van productfamilies kunnen sommige artikelen twee keer of vaker worden geproduceerd tijdens één verwerking, wat het materiaalverbruik optimaliseert.</span><span class="sxs-lookup"><span data-stu-id="8c393-105">By forming production families, some items can be manufactured twice or more in one production, which will optimize material consumption.</span></span>

<span data-ttu-id="8c393-106">In het veld **Aantal** van het venster **Familie** voert u het aantal in dat wordt geproduceerd nadat de hele familie één keer is geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="8c393-106">In the **Quantity** field in the **Family** window, you enter the quantity that will be produced when the whole family has been manufactured once.</span></span>

## <a name="example"></a><span data-ttu-id="8c393-107">Opmerking</span><span class="sxs-lookup"><span data-stu-id="8c393-107">Example</span></span>
<span data-ttu-id="8c393-108">Bij een stansproces kunnen uit één vel tegelijkertijd vier stuks van het ene artikel en tien stuks van een ander artikel worden geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="8c393-108">In punching processes, four pieces of the same item can be produced from one sheet and 10 pieces of another, different, item at the same time.</span></span> <span data-ttu-id="8c393-109">De stansmachine produceert de veertien stuks in één stap.</span><span class="sxs-lookup"><span data-stu-id="8c393-109">The punching machine will punch all 14 pieces in one step.</span></span>

<span data-ttu-id="8c393-110">Wanneer u productfamilies vormt, vermindert u de uitvalhoeveelheid. Wat bij de productie van grote artikelen doorgaans wordt beschouwd als uitval, wordt nu gebruikt voor de productie van kleinere artikelen.</span><span class="sxs-lookup"><span data-stu-id="8c393-110">Forming production families reduces the scrap quantity because what would normally be leftover scrap, when producing big pieces, will be used instead to produce small items.</span></span>

## <a name="to-set-up-a-production-family"></a><span data-ttu-id="8c393-111">Een productfamilie instellen</span><span class="sxs-lookup"><span data-stu-id="8c393-111">To set up a production family</span></span>
1. <span data-ttu-id="8c393-112">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Productfamilies** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="8c393-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Families**, and then choose the related link.</span></span>
2. <span data-ttu-id="8c393-113">Vul de benodigde velden in.</span><span class="sxs-lookup"><span data-stu-id="8c393-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-familily"></a><span data-ttu-id="8c393-114">Produceren op basis van een productfamilie</span><span class="sxs-lookup"><span data-stu-id="8c393-114">To produce based on a production familily</span></span>
1. <span data-ttu-id="8c393-115">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vast geplande productieorders** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="8c393-115">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Firm Planned Prod. Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="8c393-116">Maak een nieuwe productieorder.</span><span class="sxs-lookup"><span data-stu-id="8c393-116">Create a new production order.</span></span> <span data-ttu-id="8c393-117">Zie voor meer informatie [Productieorders maken](production-how-to-create-production-orders.md).</span><span class="sxs-lookup"><span data-stu-id="8c393-117">For more information, see [Create Production orders](production-how-to-create-production-orders.md).</span></span>
3. <span data-ttu-id="8c393-118">Selecteer in het veld **Brontype** de optie **Familie**.</span><span class="sxs-lookup"><span data-stu-id="8c393-118">In the **Source Type** field, select **Family**.</span></span>  
4. <span data-ttu-id="8c393-119">Selecteer de relevante productfamilie in het veld **Bronnr.**</span><span class="sxs-lookup"><span data-stu-id="8c393-119">In the **Source No.** field, select the relevant production family.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c393-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8c393-120">See Also</span></span>
[<span data-ttu-id="8c393-121">Productiestuklijsten maken</span><span class="sxs-lookup"><span data-stu-id="8c393-121">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)  
[<span data-ttu-id="8c393-122">Productie instellen</span><span class="sxs-lookup"><span data-stu-id="8c393-122">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="8c393-123">[Productie](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="8c393-123">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="8c393-124">[Gepland](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="8c393-124">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="8c393-125">Voorraad</span><span class="sxs-lookup"><span data-stu-id="8c393-125">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="8c393-126">Inkoop</span><span class="sxs-lookup"><span data-stu-id="8c393-126">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="8c393-127">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8c393-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

