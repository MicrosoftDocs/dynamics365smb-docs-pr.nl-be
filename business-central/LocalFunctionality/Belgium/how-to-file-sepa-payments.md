---
title: SEPA-betalingen indienen
description: In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u SEPA-kredietoverboekingen (Single Euro Payments Area) gebruiken om SEPA-betalingen in te dienen bij de bank.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: effecef4471b12032fb4e3d2ab3b198fd0e1a249
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="file-sepa-payments"></a><span data-ttu-id="ae1ac-103">SEPA-betalingen indienen</span><span class="sxs-lookup"><span data-stu-id="ae1ac-103">File SEPA Payments</span></span>
<span data-ttu-id="ae1ac-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u SEPA-kredietoverboekingen (Single Euro Payments Area) gebruiken om SEPA-betalingen in te dienen bij de bank.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can use Single Euro Payments Area (SEPA) credit transfers to file SEPA payments with the bank.</span></span>  

<span data-ttu-id="ae1ac-105">SEPA verenigt de betalingsmethoden in deelnemende Europese landen/regio's, zodat internationale betalingen even gemakkelijk te verwerken worden als binnenlandse betalingen.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-105">SEPA unifies payment methods in participating European countries/regions, which makes international payments as easy to process as domestic payments.</span></span> <span data-ttu-id="ae1ac-106">Europese burgers en bedrijven kunnen betalingen in euro's verrichten en ontvangen, binnen of buiten nationale grenzen, onder dezelfde basisomstandigheden, -rechten en -verplichtingen, ongeacht de locatie.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-106">European citizens and companies can make and receive payments in euros, whether within or across national borders, with the same basic conditions, rights, and obligations, regardless of location.</span></span>  

<span data-ttu-id="ae1ac-107">Voordat u een SEPA-betaling kunt indienen, moet u de volgende beheertaken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="ae1ac-107">Before you can file a SEPA payment you must complete the following administration tasks:</span></span>  

- <span data-ttu-id="ae1ac-108">Stel een nieuw exportprotocol in.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-108">Set up a new export protocol.</span></span> <span data-ttu-id="ae1ac-109">Zie Exportprotocol voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-109">For more information, see Export Protocol.</span></span>  
- <span data-ttu-id="ae1ac-110">Schakel in de tabel **Land/regio** het veld **SEPA toegestaan** in voor elk land in de EEA-zone.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-110">In the **Country/Region** table, select the **SEPA Allowed** field for each country that belongs to the EEA zone.</span></span>  
- <span data-ttu-id="ae1ac-111">Controleer of de waarde in het veld **Valuta Euro** in de tabel **Boekhoudinstellingen** overeenkomt met de valuta op de betalingsregels.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-111">Verify that the **Currency Euro** field in the **General Ledger Setup** table corresponds with the currency in the payment lines.</span></span>  
- <span data-ttu-id="ae1ac-112">Controleer of het veld **Bankrekening van voorkeur** in de tabel **Leverancier** de IBAN en SWIFT-code bevat.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-112">Verify that the vendor’s **Preferred Bank Account** field in the **Vendor** table contains the IBAN and SWIFT code.</span></span>  

## <a name="to-file-a-sepa-payment"></a><span data-ttu-id="ae1ac-113">Een SEPA-betaling indienen</span><span class="sxs-lookup"><span data-stu-id="ae1ac-113">To file a SEPA payment</span></span>  

1.  <span data-ttu-id="ae1ac-114">Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **SEPA-betalingen indienen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-114">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **File SEPA Payments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ae1ac-115">Vul de velden in zoals beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-115">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="ae1ac-116">Veld</span><span class="sxs-lookup"><span data-stu-id="ae1ac-116">Field</span></span>|<span data-ttu-id="ae1ac-117">Description</span><span class="sxs-lookup"><span data-stu-id="ae1ac-117">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="ae1ac-118">**Dagboeksjabloon**</span><span class="sxs-lookup"><span data-stu-id="ae1ac-118">**Journal Template Name**</span></span>|<span data-ttu-id="ae1ac-119">Geef de dagboeksjabloon voor het SEPA-betalingsrapport op.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-119">Specify the general journal template for the SEPA payment report.</span></span>|  
    |<span data-ttu-id="ae1ac-120">**Dagboekbatch**</span><span class="sxs-lookup"><span data-stu-id="ae1ac-120">**Journal Batch**</span></span>|<span data-ttu-id="ae1ac-121">Geef de dagboekbatch voor het SEPA-betalingsrapport op.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-121">Specify the general journal batch for the SEPA payment report.</span></span>|  
    |<span data-ttu-id="ae1ac-122">**Dagboekregels boeken**</span><span class="sxs-lookup"><span data-stu-id="ae1ac-122">**Post General Journal Lines**</span></span>|<span data-ttu-id="ae1ac-123">Geef op of u de betalingsregels naar het grootboek wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-123">Specify if you want to transfer the payment lines to the general ledger.</span></span>|  
    |<span data-ttu-id="ae1ac-124">**Dimensies opnemen**</span><span class="sxs-lookup"><span data-stu-id="ae1ac-124">**Include Dimensions**</span></span>|<span data-ttu-id="ae1ac-125">Hier kunt u de dimensies invoeren die u in het SEPA-betalingsrapport wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-125">Enter the dimensions that you want to include in the SEPA payment report.</span></span> <span data-ttu-id="ae1ac-126">De optie is alleen beschikbaar als het veld **Alg. dagb.regels samenvatten** in het veld **Elektronisch bankieren instellen** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-126">The option is only available if the **Summarize Gen. Jnl. Lines** field in the **Electronic Banking Setup** window is selected.</span></span>|  
    |<span data-ttu-id="ae1ac-127">**Uitvoeringsdatum**</span><span class="sxs-lookup"><span data-stu-id="ae1ac-127">**Execution Date**</span></span>|<span data-ttu-id="ae1ac-128">Voer een uitvoeringsdatum in als u op de betalingsregels een datum wilt hebben die afwijkt van de boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-128">Enter an execution date if you want an execution date that differs from the posting date on the payment lines.</span></span>|  
    |<span data-ttu-id="ae1ac-129">**Bestandsnaam**</span><span class="sxs-lookup"><span data-stu-id="ae1ac-129">**File Name**</span></span>|<span data-ttu-id="ae1ac-130">Voer de naam in van het bestand, inclusief station en map, waarin u het rapport wilt afdrukken.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-130">Enter the name of the file, including the drive and folder, to which you want to print the report.</span></span>|  

3.  <span data-ttu-id="ae1ac-131">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae1ac-131">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ae1ac-132">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ae1ac-132">See Also</span></span>  
 <span data-ttu-id="ae1ac-133">[Exportprotocollen instellen](how-to-set-up-export-protocols.md) </span><span class="sxs-lookup"><span data-stu-id="ae1ac-133">[Set Up Export Protocols](how-to-set-up-export-protocols.md) </span></span>  
 <span data-ttu-id="ae1ac-134">[SEPA-betalingen in andere valuta's dan de euro indienen](how-to-file-non-euro-sepa-payments.md) </span><span class="sxs-lookup"><span data-stu-id="ae1ac-134">[File Non-Euro SEPA Payments](how-to-file-non-euro-sepa-payments.md) </span></span>  
 [<span data-ttu-id="ae1ac-135">SEPA-betalingen activeren</span><span class="sxs-lookup"><span data-stu-id="ae1ac-135">Activate SEPA Payments</span></span>](how-to-activate-sepa-payments.md)

