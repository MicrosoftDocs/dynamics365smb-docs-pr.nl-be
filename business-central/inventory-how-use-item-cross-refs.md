---
title: Artikelkruisverwijzingen gebruiken
description: Stel verwijzingen in tussen de beschrijvingen die u en uw leverancier voor een artikel gebruiken, zodat u de artikelbeschrijving van de leverancier op inkoopdocumenten kunt invoegen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 01/12/2021
ms.author: edupont
ms.openlocfilehash: 2f500d7df80235b8f092fc3f0a7ae8fd27cd8aea
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377635"
---
# <a name="use-item-cross-references"></a><span data-ttu-id="a6cbe-103">Artikelkruisverwijzingen gebruiken</span><span class="sxs-lookup"><span data-stu-id="a6cbe-103">Use Item Cross References</span></span>
<span data-ttu-id="a6cbe-104">Als u een kruisverwijzing instelt tussen de artikelbeschrijving die u voor een artikel gebruikt, en de beschrijving die de leverancier van dat artikel gebruikt, wordt de artikelbeschrijving van de leverancier automatisch in inkoopdocumenten voor de leverancier ingevuld wanneer u het veld **Kruisverwijzingsnr..**</span><span class="sxs-lookup"><span data-stu-id="a6cbe-104">If you set up a cross reference between the item description that you use for an item and the description that the vendor of that item uses, then the vendor's item description is automatically inserted on purchase documents for the vendor when you fill in the **Cross-Reference No.**</span></span> <span data-ttu-id="a6cbe-105">invult.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-105">field.</span></span> <span data-ttu-id="a6cbe-106">Dezelfde functionaliteit geldt voor klantartikelnummers in verkoopdocumenten.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-106">The same functionality applies for customer item numbers on sales documents.</span></span>

<span data-ttu-id="a6cbe-107">In de volgende procedures wordt beschreven hoe u artikelkruisverwijzingen aan de inkoopkant gebruikt.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-107">The following procedures describe how to use item cross references on the purchase side.</span></span> <span data-ttu-id="a6cbe-108">De stappen zijn vergelijkbaar voor de verkoopkant.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-108">The steps are similar for the sales side.</span></span>

> [!NOTE]
> <span data-ttu-id="a6cbe-109">Het komt steeds vaker voor dat artikel-id's zoals GTIN's of GUID's 30 of meer tekens bevatten, wat meer is dan de huidige functie voor artikelkruisverwijzingen aankan.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-109">It's becoming more common for item identifiers such as GTINs or GUIDs to contain 30 or more characters, which is more than the current feature for item cross references can handle.</span></span> <span data-ttu-id="a6cbe-110">Als u referenties moet gebruiken die meer dan 30 tekens bevatten, kan uw beheerder de functie **Langere itemreferenties schrijven** functie op de pagina [Functiebeheer](https://businesscentral.dynamics.com/?page=2610) gebruiken (koppeling vereist dat u een [!INCLUDE[prod_short](includes/prod_short.md)]-tenant hebt).</span><span class="sxs-lookup"><span data-stu-id="a6cbe-110">If you need to use references that contain more than 30 characters, your administrator can turn on the **Write longer item references** feature on the [Feature Management](https://businesscentral.dynamics.com/?page=2610) page (link requires that you have a [!INCLUDE[prod_short](includes/prod_short.md)] tenant).</span></span> <span data-ttu-id="a6cbe-111">Hoe u verwijzingen gebruikt, verandert niet, maar de namen van zaken als pagina's en knoppen wel.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-111">How you use references doesn't change, but the names of things like pages and buttons will.</span></span> <span data-ttu-id="a6cbe-112">De pagina **Artikelkruisverwijzingposten** wordt bijvoorbeeld de pagina **Artikelverwijzingsposten**.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-112">For example, the **Item Cross-Reference Entries** page will become the **Item Reference Entries** page.</span></span>

## <a name="to-set-up-an-item-cross-reference-to-a-vendors-item-description"></a><span data-ttu-id="a6cbe-113">Een artikelkruisverwijzing naar de artikelbeschrijving van een leverancier instellen</span><span class="sxs-lookup"><span data-stu-id="a6cbe-113">To set up an item cross reference to a vendor's item description</span></span>

1. <span data-ttu-id="a6cbe-114">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="a6cbe-115">Open de kaart voor een artikel waarvoor u een kruisverwijzing wilt maken naar de artikelomschrijving die de leverancier gebruikt voor het artikel.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-115">Open the card for an item for which you want to create a cross reference to the item description that the vendor uses for that item.</span></span>
3. <span data-ttu-id="a6cbe-116">Kies de actie **Kruisverwijzingen**.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-116">Choose the **Cross References** action.</span></span>

     <span data-ttu-id="a6cbe-117">Als u de actie **Kruisverwijzingen** niet kunt vinden, kiest u ervoor om meer opties weer te geven en zoekt u de actie vervolgens onder **Gerelateerd** > **Artikel**.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-117">If you cannot find the **Cross References** action, choose to view more options, and then find it under **Related** > **Item**.</span></span>
  
4. <span data-ttu-id="a6cbe-118">Vul op een nieuwe regel op de pagina **Artikelkruisverwijzingposten** de velden naar wens in.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-118">On a new line on the **Item Cross-Reference Entries** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]<span data-ttu-id="a6cbe-119">.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-119">.</span></span>

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a><span data-ttu-id="a6cbe-120">De artikelomschrijving van een leverancier invoeren in een inkooporder</span><span class="sxs-lookup"><span data-stu-id="a6cbe-120">To enter a vendor's item description on a purchase order</span></span>

1. <span data-ttu-id="a6cbe-121">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-121">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="a6cbe-122">Maak een inkooporder voor de leverancier voor wie u een artikelkruisverwijzing hebt ingesteld in de vorige procedure.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-122">Create a purchase order for the vendor that you set up an item cross reference for in the previous procedure.</span></span>
3. <span data-ttu-id="a6cbe-123">Maak een inkoopregel voor het artikel waarvoor u een artikelkruisverwijzing hebt ingesteld in de vorige procedure.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-123">Create a purchase line for the item that you set up an item cross reference for in the previous procedure.</span></span>
4. <span data-ttu-id="a6cbe-124">Selecteer in het veld **Kruisverwijzingssoortnr.**</span><span class="sxs-lookup"><span data-stu-id="a6cbe-124">In the **Cross-Reference No.**</span></span> <span data-ttu-id="a6cbe-125">de artikelkruisverwijzing die u hebt gemaakt, en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-125">field, select the item cross reference that you have created, and then choose the **OK** button.</span></span>

<span data-ttu-id="a6cbe-126">Het veld **Omschrijving** op de regel wordt overschreven met de artikelomschrijving van de leverancier, zoals ingesteld in de artikelkruisverwijzingspost.</span><span class="sxs-lookup"><span data-stu-id="a6cbe-126">The **Description** field on the line is overwritten with the vendor's item description, as set up on the item cross-reference entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6cbe-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a6cbe-127">See Also</span></span>
[<span data-ttu-id="a6cbe-128">Nieuwe artikelen registreren</span><span class="sxs-lookup"><span data-stu-id="a6cbe-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="a6cbe-129">Voorraad</span><span class="sxs-lookup"><span data-stu-id="a6cbe-129">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="a6cbe-130">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a6cbe-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]