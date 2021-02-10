---
title: Extra regels toevoegen om uitgebreide beschrijvingen te definiëren
description: U kunt extra regels toevoegen om de standaardtekst uit te breiden die een artikel, grootboekrekening en andere gegevens beschrijft.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9e443a44135bbdaf75f6a064370983592797b10b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4756929"
---
# <a name="add-extended-text"></a><span data-ttu-id="c912a-103">Tekstuitbreiding toevoegen</span><span class="sxs-lookup"><span data-stu-id="c912a-103">Add Extended Text</span></span>

<span data-ttu-id="c912a-104">U kunt de beschrijving voor artikelen, voorraadeenheden, grootboekrekeningen en resources uitbreiden door extra regels toe te voegen als uitgebreide tekst.</span><span class="sxs-lookup"><span data-stu-id="c912a-104">You can extend the description for items, stock-keeping units, general ledger accounts, and resources by adding extra lines as extended text.</span></span> <span data-ttu-id="c912a-105">U kunt ook voorwaarden stellen voor het gebruik van de extra regels.</span><span class="sxs-lookup"><span data-stu-id="c912a-105">You can also set up conditions for use of the extra lines.</span></span>  

<span data-ttu-id="c912a-106">In de volgende sectie wordt beschreven hoe u uitgebreide tekst kunt toevoegen aan een beschrijving van een artikel.</span><span class="sxs-lookup"><span data-stu-id="c912a-106">The following section describes how to add extended text to a description of an item.</span></span> <span data-ttu-id="c912a-107">Maar dezelfde stappen zijn van toepassing op SKU's, grootboekrekeningen en resources.</span><span class="sxs-lookup"><span data-stu-id="c912a-107">But the same steps apply to stock-keeping units, general ledger accounts, and resources.</span></span>  

## <a name="to-define-extended-text-for-an-description"></a><span data-ttu-id="c912a-108">Uitgebreide tekst definiëren voor een beschrijving</span><span class="sxs-lookup"><span data-stu-id="c912a-108">To define extended text for an description</span></span>

1. <span data-ttu-id="c912a-109">Open de kaart voor een artikel waaraan u uitgebreide tekst wilt toevoegen, en kies vervolgens de actie **Tekstuitbreiding**.</span><span class="sxs-lookup"><span data-stu-id="c912a-109">Open the card for an item that you want to add extended text to, and then choose the **Extended Text** action.</span></span>
2. <span data-ttu-id="c912a-110">Vul de velden **Code** en **Omschrijving** in.</span><span class="sxs-lookup"><span data-stu-id="c912a-110">Fill in the **Code** and **Description** fields.</span></span>
3. <span data-ttu-id="c912a-111">Kies **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="c912a-111">Choose the **New**.</span></span>
4. <span data-ttu-id="c912a-112">Vul het veld **Taalcode** in of selecteer het selectievakje **Alle taalcodes** als u taalcodes gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c912a-112">Fill in the **Language Code** field or select the **All Language Codes** check box if you use language codes.</span></span>
5. <span data-ttu-id="c912a-113">Vul de velden **Begindatum** en **Einddatum** in als u een beperking wilt instellen voor de data waarop de tekstuitbreiding kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c912a-113">Fill in the **Starting Date** and **Ending Date** fields if you want to limit the dates on which the extended text is used.</span></span>
6. <span data-ttu-id="c912a-114">Voer in het veld **Tekst** de uitgebreide tekst in.</span><span class="sxs-lookup"><span data-stu-id="c912a-114">In the **Text** field, write the extended text.</span></span>
7. <span data-ttu-id="c912a-115">Schakel relevante selectievakjes in voor de documentsoorten waarvoor u de uitgebreide tekst wilt afdrukken.</span><span class="sxs-lookup"><span data-stu-id="c912a-115">Select relevant check boxes for the document types where you want the extended text printed.</span></span>
8. <span data-ttu-id="c912a-116">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c912a-116">Close the page.</span></span>

<span data-ttu-id="c912a-117">U kunt deze uitgebreide tekst nu aan documenten toevoegen.</span><span class="sxs-lookup"><span data-stu-id="c912a-117">You can now add this extended text to documents.</span></span> <span data-ttu-id="c912a-118">De volgende procedure legt uit hoe u uitgebreide tekst aan een verkooporder kunt toevoegen, maar dezelfde stappen zijn van toepassing op elk ander document dat u voor de uitgebreide tekst hebt gespecificeerd.</span><span class="sxs-lookup"><span data-stu-id="c912a-118">The following procedure explains how to add extended text to a sales order, but the same steps apply to any other document that you specified for the extended text.</span></span>  

## <a name="to-add-an-extended-item-text-on-a-sales-order-line"></a><span data-ttu-id="c912a-119">Een uitgebreide artikeltekst op een verkooporderregel toevoegen</span><span class="sxs-lookup"><span data-stu-id="c912a-119">To add an extended item text on a sales order line</span></span>

1. <span data-ttu-id="c912a-120">Open een verkooporder met een verkoopregel voor een artikel waarvoor uitgebreide tekst is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="c912a-120">Open a sales order with a sales line for an item that has extended text defined.</span></span> <span data-ttu-id="c912a-121">Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c912a-121">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
2. <span data-ttu-id="c912a-122">Selecteer de desbetreffende regel en kies de actie **Tekstuitbreiding invoegen**.</span><span class="sxs-lookup"><span data-stu-id="c912a-122">Select the line in question, and then choose the **Insert Ext. Text** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="c912a-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c912a-123">See Also</span></span>

[<span data-ttu-id="c912a-124">Voorraad instellen</span><span class="sxs-lookup"><span data-stu-id="c912a-124">Setting Up Inventory</span></span>](inventory-setup-inventory.md)  
<span data-ttu-id="c912a-125">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c912a-125">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>
