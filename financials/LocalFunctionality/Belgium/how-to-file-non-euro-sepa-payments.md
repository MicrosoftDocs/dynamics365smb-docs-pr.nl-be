---
title: SEPA-betalingen in andere valuta's dan de euro indienen
description: In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u SEPA-betalingen in andere valuta's dan de euro indienen bij de bank. Dit is handig als u betalingen verzendt naar andere landen die SEPA niet gebruiken en voor andere valuta's dan de euro.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: d9bb21b1c22be883f504517d7e714254f5cfd2bf
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="file-non-euro-sepa-payments"></a><span data-ttu-id="2439a-104">SEPA-betalingen in andere valuta's dan de euro indienen</span><span class="sxs-lookup"><span data-stu-id="2439a-104">File Non-Euro SEPA Payments</span></span>
<span data-ttu-id="2439a-105">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u SEPA-betalingen in andere valuta's dan de euro indienen bij de bank.</span><span class="sxs-lookup"><span data-stu-id="2439a-105">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can file non-euro SEPA payments with the bank.</span></span> <span data-ttu-id="2439a-106">Dit is handig als u betalingen verzendt naar andere landen die SEPA niet gebruiken en voor andere valuta's dan de euro.</span><span class="sxs-lookup"><span data-stu-id="2439a-106">This is useful when you make payments to other countries that do not use SEPA and for currencies other than the euro.</span></span>  

<span data-ttu-id="2439a-107">Voordat u een dergelijke SEPA-betalingen kunt indienen, moet u de volgende beheertaken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="2439a-107">Before you can file a non-euro SEPA payment you must complete the following administration tasks:</span></span>  

- <span data-ttu-id="2439a-108">Stel een nieuw exportprotocol voor een niet-euro-SEPA in.</span><span class="sxs-lookup"><span data-stu-id="2439a-108">Set up a new export protocol for a non-euro SEPA.</span></span> <span data-ttu-id="2439a-109">Zie Exportprotocol voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="2439a-109">For more information, see Export Protocol.</span></span>  
- <span data-ttu-id="2439a-110">Schakel in de tabel **Land/regio** het veld **SEPA toegestaan** uit voor elk land in de EEA-zone.</span><span class="sxs-lookup"><span data-stu-id="2439a-110">In the **Country/Region** table, clear the **SEPA Allowed** field for each country that belongs to the EEA zone.</span></span>  
- <span data-ttu-id="2439a-111">Controleer of de waarde in het veld **Valuta Euro** in de tabel **Boekhoudinstellingen** niet in euro's is.</span><span class="sxs-lookup"><span data-stu-id="2439a-111">Verify that the **Currency Euro** field in the **General Ledger Setup** table is not in euro currency.</span></span>  
- <span data-ttu-id="2439a-112">Controleer of het veld **Bankrekening van voorkeur** in de tabel **Leverancier** de IBAN en SWIFT-code bevat.</span><span class="sxs-lookup"><span data-stu-id="2439a-112">Verify that the vendor’s **Preferred Bank Account** field in the **Vendor** table contains the IBAN and SWIFT code.</span></span>  

## <a name="to-file-a-non-euro-sepa-payment"></a><span data-ttu-id="2439a-113">Een SEPA-betaling in andere valuta's dan de euro indienen</span><span class="sxs-lookup"><span data-stu-id="2439a-113">To file a non-euro SEPA payment</span></span>  

1.  <span data-ttu-id="2439a-114">Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **SEPA-betalingen in andere valuta's dan de euro indienen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="2439a-114">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **File Non Euro SEPA Payments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2439a-115">Vul de velden in zoals beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="2439a-115">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="2439a-116">Veld</span><span class="sxs-lookup"><span data-stu-id="2439a-116">Field</span></span>|<span data-ttu-id="2439a-117">Description</span><span class="sxs-lookup"><span data-stu-id="2439a-117">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="2439a-118">**Dagboeksjabloon**</span><span class="sxs-lookup"><span data-stu-id="2439a-118">**Journal Template Name**</span></span>|<span data-ttu-id="2439a-119">Geef de dagboeksjabloon voor het SEPA-betalingsrapport op.</span><span class="sxs-lookup"><span data-stu-id="2439a-119">Specify the general journal template for the non-euro SEPA payment report.</span></span>|  
    |<span data-ttu-id="2439a-120">**Dagboekbatch**</span><span class="sxs-lookup"><span data-stu-id="2439a-120">**Journal Batch**</span></span>|<span data-ttu-id="2439a-121">Geef de dagboekbatch voor het SEPA-betalingsrapport op.</span><span class="sxs-lookup"><span data-stu-id="2439a-121">Specify the general journal batch for the non-euro SEPA payment report.</span></span>|  
    |<span data-ttu-id="2439a-122">**Dagboekregels boeken**</span><span class="sxs-lookup"><span data-stu-id="2439a-122">**Post General Journal Lines**</span></span>|<span data-ttu-id="2439a-123">Geef op of u de betalingsregels naar het grootboek wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="2439a-123">Specify if you want to transfer the payment lines to the general ledger.</span></span>|  
    |<span data-ttu-id="2439a-124">**Dimensies opnemen**</span><span class="sxs-lookup"><span data-stu-id="2439a-124">**Include Dimensions**</span></span>|<span data-ttu-id="2439a-125">Hier kunt u de dimensies invoeren die u in het SEPA-betalingsrapport wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="2439a-125">Enter the dimensions that you want to include in the non-euro SEPA payment report.</span></span> <span data-ttu-id="2439a-126">De optie is alleen beschikbaar als het veld **Alg. dagb.regels samenvatten** in het veld **Elektronisch bankieren instellen** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="2439a-126">The option is only available if the **Summarize Gen. Jnl. Lines** field in the **Electronic Banking Setup** window is selected.</span></span>|  
    |<span data-ttu-id="2439a-127">**Uitvoeringsdatum**</span><span class="sxs-lookup"><span data-stu-id="2439a-127">**Execution Date**</span></span>|<span data-ttu-id="2439a-128">Voer een uitvoeringsdatum in als u op de betalingsregels een datum wilt hebben die afwijkt van de boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="2439a-128">Enter an execution date if you want an execution date that differs from the posting date on the payment lines.</span></span>|  
    |<span data-ttu-id="2439a-129">**Bestandsnaam**</span><span class="sxs-lookup"><span data-stu-id="2439a-129">**File Name**</span></span>|<span data-ttu-id="2439a-130">Voer de naam in van het bestand, inclusief station en map, waarin u het rapport wilt afdrukken.</span><span class="sxs-lookup"><span data-stu-id="2439a-130">Enter the name of the file, including the drive and folder, to which you want to print the report.</span></span>|  

3.  <span data-ttu-id="2439a-131">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="2439a-131">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2439a-132">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2439a-132">See Also</span></span>  
 <span data-ttu-id="2439a-133">[SEPA-betalingen indienen](how-to-file-sepa-payments.md) </span><span class="sxs-lookup"><span data-stu-id="2439a-133">[File SEPA Payments](how-to-file-sepa-payments.md) </span></span>  
 <span data-ttu-id="2439a-134">[SEPA-betalingen activeren](how-to-activate-sepa-payments.md) </span><span class="sxs-lookup"><span data-stu-id="2439a-134">[Activate SEPA Payments](how-to-activate-sepa-payments.md) </span></span>  
 [<span data-ttu-id="2439a-135">SEPA-betalingen</span><span class="sxs-lookup"><span data-stu-id="2439a-135">SEPA Payments</span></span>](sepa-payments.md)

