---
title: Intrastat-aangiftes van derden exporteren
description: In België moet u de Intrastat-aangifte door een derde laten invullen. Dit moet een extern persoon of een bedrijf zijn.
services: project-madeira
documentationcenter: ''
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: soalex
ms.openlocfilehash: 0cd44ebf58ab72bfd4825473e38915a2b993684c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775004"
---
# <a name="export-intrastat-third-party-declarations"></a><span data-ttu-id="5bbe1-104">Intrastat-aangiftes van derden exporteren</span><span class="sxs-lookup"><span data-stu-id="5bbe1-104">Export Intrastat Third-Party Declarations</span></span>
<span data-ttu-id="5bbe1-105">In België moet u de Intrastat-aangifte door een derde laten invullen.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-105">In Belgium, you must have a third-party declarant fill out the Intrastat declaration.</span></span> <span data-ttu-id="5bbe1-106">Dit moet een extern persoon of een bedrijf zijn.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-106">The third-party declarant must be an external person or company.</span></span> 

## <a name="to-export-the-third-party-declaration"></a><span data-ttu-id="5bbe1-107">De aangifte van derden exporteren</span><span class="sxs-lookup"><span data-stu-id="5bbe1-107">To export the third-party declaration</span></span>  
<span data-ttu-id="5bbe1-108">Voordat u het bestand exporteert, is het verstandig een voorbeeld van het rapport te bekijken.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-108">Before you export the file, it's a good idea to preview the report.</span></span> <span data-ttu-id="5bbe1-109">Zie voor meer informatie [Het rapport Intrastat - Formulier afdrukken](how-to-print-the-intrastat-form-report.md).</span><span class="sxs-lookup"><span data-stu-id="5bbe1-109">For more information, see [Print the Intrastat Form Report](how-to-print-the-intrastat-form-report.md).</span></span>  

1.  <span data-ttu-id="5bbe1-110">Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Intrastat-dagboeken** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-110">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Intrastat Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5bbe1-111">Kies de actie **Bestand maken**.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-111">Choose the **Create File** action.</span></span>  
3.  <span data-ttu-id="5bbe1-112">Vul de velden in zoals beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-112">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="5bbe1-113">Veld</span><span class="sxs-lookup"><span data-stu-id="5bbe1-113">Field</span></span>|<span data-ttu-id="5bbe1-114">Description</span><span class="sxs-lookup"><span data-stu-id="5bbe1-114">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="5bbe1-115">**Nulaangifte**</span><span class="sxs-lookup"><span data-stu-id="5bbe1-115">**Nihil declaration**</span></span>|<span data-ttu-id="5bbe1-116">Selecteer deze optie als u geen handelstransacties met EU-landen/regio's hebt en een lege aangifte wilt versturen.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-116">Select if you do not have any trade transactions with European Union (EU) countries/regions and want to send an empty declaration.</span></span>|  
    |<span data-ttu-id="5bbe1-117">**Gegevens van tegenpartij**</span><span class="sxs-lookup"><span data-stu-id="5bbe1-117">**Counter party info**</span></span>|<span data-ttu-id="5bbe1-118">Schakel dit veld in om gegevens van de tegenpartij op te nemen in het Intrastat-bestand (nieuwe vereiste vanaf 2019).</span><span class="sxs-lookup"><span data-stu-id="5bbe1-118">Check this field to include counter party information in the Intrastat file (new requirement from 2019).</span></span> <span data-ttu-id="5bbe1-119">De gegevens van de tegenpartij die worden toegevoegd aan het bestand, zijn afkomstig uit de velden **Land/regio van oorsprong** en **Partner-id** in het Intrastat-dagboek.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-119">The counter party information added to the file is taken from the **Country/Region of Origin Code** and **Partner ID** fields from the Intrastat Journal.</span></span>|  
    |<span data-ttu-id="5bbe1-120">**Ondernemingsnr./btw-nr.**</span><span class="sxs-lookup"><span data-stu-id="5bbe1-120">**Enterprise No./VAT Reg. No.**</span></span>|<span data-ttu-id="5bbe1-121">Voer het ondernemings- of btw-nummer in.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-121">Enter the enterprise or VAT registration number.</span></span>|  
    
4.  <span data-ttu-id="5bbe1-122">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-122">Choose the **OK** button.</span></span>  

<span data-ttu-id="5bbe1-123">Vervolgens moet de aangifte naar de OneGate-portal worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="5bbe1-123">Next, submit the declaration to the OneGate portal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5bbe1-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5bbe1-124">See Also</span></span>  
 <span data-ttu-id="5bbe1-125">[Belgische Intrastat-rapportage](belgian-intrastat-reporting.md) </span><span class="sxs-lookup"><span data-stu-id="5bbe1-125">[Belgian Intrastat Reporting](belgian-intrastat-reporting.md) </span></span>  
 <span data-ttu-id="5bbe1-126">[Aangiftesoorten instellen](how-to-set-up-declaration-types.md) </span><span class="sxs-lookup"><span data-stu-id="5bbe1-126">[Set Up Declaration Types](how-to-set-up-declaration-types.md) </span></span>  
 <span data-ttu-id="5bbe1-127">[Belgische tariefcodes instellen](how-to-set-up-belgian-tariff-numbers.md) </span><span class="sxs-lookup"><span data-stu-id="5bbe1-127">[Set Up Belgian Tariff Numbers](how-to-set-up-belgian-tariff-numbers.md) </span></span>  
 <span data-ttu-id="5bbe1-128">[Intrastat-nummers instellen](how-to-set-up-intrastat-establishment-numbers.md) </span><span class="sxs-lookup"><span data-stu-id="5bbe1-128">[Set Up Intrastat Establishment Numbers](how-to-set-up-intrastat-establishment-numbers.md) </span></span>  
 [<span data-ttu-id="5bbe1-129">Het rapport Intrastat - Formulier afdrukken</span><span class="sxs-lookup"><span data-stu-id="5bbe1-129">Print the Intrastat Form Report</span></span>](how-to-print-the-intrastat-form-report.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]