---
title: Artikelkruisverwijzingen gebruiken | Microsoft Docs
description: Als u een kruisverwijzing instelt tussen de artikelbeschrijving die u voor een artikel gebruikt, en de beschrijving die de leverancier van dat artikel gebruikt, wordt de artikelbeschrijving van de leverancier automatisch in inkoopdocumenten voor de leverancier ingevuld wanneer u het veld **Kruisverwijzingsnr.** invult.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 1b914c3c1c5e640894f1ee48639c547421c27be4
ms.sourcegitcommit: 0c6f4382fad994fb6aea9dcde3b2dc25382c5968
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484046"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="f1c7c-104">Artikelkruisverwijzingen gebruiken</span><span class="sxs-lookup"><span data-stu-id="f1c7c-104">Use Item Cross References</span></span>
<span data-ttu-id="f1c7c-105">Als u een kruisverwijzing instelt tussen de artikelbeschrijving die u voor een artikel gebruikt, en de beschrijving die de leverancier van dat artikel gebruikt, wordt de artikelbeschrijving van de leverancier automatisch in inkoopdocumenten voor de leverancier ingevuld wanneer u het veld **Kruisverwijzingsnr..**</span><span class="sxs-lookup"><span data-stu-id="f1c7c-105">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="f1c7c-106">invult.</span><span class="sxs-lookup"><span data-stu-id="f1c7c-106">field.</span></span> <span data-ttu-id="f1c7c-107">Dezelfde functionaliteit geldt voor klantartikelnummers in verkoopdocumenten.</span><span class="sxs-lookup"><span data-stu-id="f1c7c-107">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="f1c7c-108">In de volgende procedures wordt beschreven hoe u artikelkruisverwijzingen aan de inkoopkant gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f1c7c-108">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="f1c7c-109">De stappen zijn vergelijkbaar voor de verkoopkant.</span><span class="sxs-lookup"><span data-stu-id="f1c7c-109">The steps are similar for the sales side.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="f1c7c-110">Een artikelkruisverwijzing naar de artikelbeschrijving van een leverancier instellen</span><span class="sxs-lookup"><span data-stu-id="f1c7c-110">To set up an item cross reference to a vendor's item description</span></span>

1. <span data-ttu-id="f1c7c-111">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="f1c7c-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="f1c7c-112">Open de kaart voor een artikel waarvoor u een kruisverwijzing wilt maken naar de artikelomschrijving die de leverancier gebruikt voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="f1c7c-112">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="f1c7c-113">Kies de actie **Kruisverwijzingen**.</span><span class="sxs-lookup"><span data-stu-id="f1c7c-113">Choose the **Cross References** action.</span></span>

     <span data-ttu-id="f1c7c-114">Als u de actie **Kruisverwijzingen** niet kunt vinden, kiest u ervoor om meer opties weer te geven en zoekt u deze vervolgens onder **Navigeren**, **Artikel**.</span><span class="sxs-lookup"><span data-stu-id="f1c7c-114">If you cannot find the **Cross References** action, choose to view more options, and then find it under **Navigate**, **Item**.</span></span>
  
4. <span data-ttu-id="f1c7c-115">Vul op een nieuwe regel op de pagina **Artikelkruisverwijzingposten** de velden naar wens in.</span><span class="sxs-lookup"><span data-stu-id="f1c7c-115">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="f1c7c-116">.</span><span class="sxs-lookup"><span data-stu-id="f1c7c-116">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="f1c7c-117">De artikelomschrijving van een leverancier invoeren in een inkooporder</span><span class="sxs-lookup"><span data-stu-id="f1c7c-117">To enter a vendor's item description on a purchase order</span></span>

1. <span data-ttu-id="f1c7c-118">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="f1c7c-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="f1c7c-119">Maak een inkooporder voor de leverancier voor wie u een artikelkruisverwijzing hebt ingesteld in de vorige procedure.</span><span class="sxs-lookup"><span data-stu-id="f1c7c-119">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="f1c7c-120">Maak een inkoopregel voor het artikel waarvoor u een artikelkruisverwijzing hebt ingesteld in de vorige procedure.</span><span class="sxs-lookup"><span data-stu-id="f1c7c-120">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="f1c7c-121">Selecteer in het veld **Kruisverwijzingssoortnr.**</span><span class="sxs-lookup"><span data-stu-id="f1c7c-121">In the **Cross-Reference No.**</span></span> <span data-ttu-id="f1c7c-122">de artikelkruisverwijzing die u hebt gemaakt, en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1c7c-122">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="f1c7c-123">Het veld **Omschrijving** op de regel wordt overschreven met de artikelomschrijving van de leverancier, zoals ingesteld in de artikelkruisverwijzingspost.</span><span class="sxs-lookup"><span data-stu-id="f1c7c-123">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1c7c-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f1c7c-124">See Also</span></span>
[<span data-ttu-id="f1c7c-125">Nieuwe artikelen registreren</span><span class="sxs-lookup"><span data-stu-id="f1c7c-125">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="f1c7c-126">Voorraad</span><span class="sxs-lookup"><span data-stu-id="f1c7c-126">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="f1c7c-127">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f1c7c-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
