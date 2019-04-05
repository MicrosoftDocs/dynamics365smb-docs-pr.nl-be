---
title: SEPA-betalingen in andere valuta's dan de euro indienen
description: In de Belgische versie van Business Central kunt u niet-euro SEPA-betalingen bij de bank archiveren. Dit is handig als u betalingen verzendt naar andere landen die SEPA niet gebruiken en voor andere valuta's dan de euro.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: d8da10aae616dd14e34b34492af312bcf1227495
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "826417"
---
# <a name="file-non-euro-sepa-payments"></a><span data-ttu-id="ea872-104">SEPA-betalingen in andere valuta's dan de euro indienen</span><span class="sxs-lookup"><span data-stu-id="ea872-104">File Non-Euro SEPA Payments</span></span>
<span data-ttu-id="ea872-105">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u SEPA-betalingen in andere valuta's dan de euro indienen bij de bank.</span><span class="sxs-lookup"><span data-stu-id="ea872-105">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can file non-euro SEPA payments with the bank.</span></span> <span data-ttu-id="ea872-106">Dit is handig als u betalingen verzendt naar andere landen die SEPA niet gebruiken en voor andere valuta's dan de euro.</span><span class="sxs-lookup"><span data-stu-id="ea872-106">This is useful when you make payments to other countries that do not use SEPA and for currencies other than the euro.</span></span>  

<span data-ttu-id="ea872-107">Voordat u een dergelijke SEPA-betalingen kunt indienen, moet u de volgende beheertaken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="ea872-107">Before you can file a non-euro SEPA payment you must complete the following administration tasks:</span></span>  

- <span data-ttu-id="ea872-108">Stel een nieuw exportprotocol voor een niet-euro-SEPA in.</span><span class="sxs-lookup"><span data-stu-id="ea872-108">Set up a new export protocol for a non-euro SEPA.</span></span> <span data-ttu-id="ea872-109">Zie Exportprotocol voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ea872-109">For more information, see Export Protocol.</span></span>  
- <span data-ttu-id="ea872-110">Schakel in de tabel **Land/regio** het veld **SEPA toegestaan** uit voor elk land in de EEA-zone.</span><span class="sxs-lookup"><span data-stu-id="ea872-110">In the **Country/Region** table, clear the **SEPA Allowed** field for each country that belongs to the EEA zone.</span></span>  
- <span data-ttu-id="ea872-111">Controleer of de waarde in het veld **Valuta Euro** in de tabel **Boekhoudinstellingen** niet in euro's is.</span><span class="sxs-lookup"><span data-stu-id="ea872-111">Verify that the **Currency Euro** field in the **General Ledger Setup** table is not in euro currency.</span></span>  
- <span data-ttu-id="ea872-112">Controleer of het veld **Bankrekening van voorkeur** in de tabel **Leverancier** de IBAN en SWIFT-code bevat.</span><span class="sxs-lookup"><span data-stu-id="ea872-112">Verify that the vendor’s **Preferred Bank Account** field in the **Vendor** table contains the IBAN and SWIFT code.</span></span>  

## <a name="to-file-a-non-euro-sepa-payment"></a><span data-ttu-id="ea872-113">Een SEPA-betaling in andere valuta's dan de euro indienen</span><span class="sxs-lookup"><span data-stu-id="ea872-113">To file a non-euro SEPA payment</span></span>  

1.  <span data-ttu-id="ea872-114">Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **SEPA-betalingen in andere valuta's dan de euro indienen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ea872-114">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **File Non Euro SEPA Payments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ea872-115">Vul de velden in zoals beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="ea872-115">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="ea872-116">Veld</span><span class="sxs-lookup"><span data-stu-id="ea872-116">Field</span></span>|<span data-ttu-id="ea872-117">Description</span><span class="sxs-lookup"><span data-stu-id="ea872-117">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="ea872-118">**Dagboeksjabloon**</span><span class="sxs-lookup"><span data-stu-id="ea872-118">**Journal Template Name**</span></span>|<span data-ttu-id="ea872-119">Geef de dagboeksjabloon voor het SEPA-betalingsrapport op.</span><span class="sxs-lookup"><span data-stu-id="ea872-119">Specify the general journal template for the non-euro SEPA payment report.</span></span>|  
    |<span data-ttu-id="ea872-120">**Dagboekbatch**</span><span class="sxs-lookup"><span data-stu-id="ea872-120">**Journal Batch**</span></span>|<span data-ttu-id="ea872-121">Geef de dagboekbatch voor het SEPA-betalingsrapport op.</span><span class="sxs-lookup"><span data-stu-id="ea872-121">Specify the general journal batch for the non-euro SEPA payment report.</span></span>|  
    |<span data-ttu-id="ea872-122">**Dagboekregels boeken**</span><span class="sxs-lookup"><span data-stu-id="ea872-122">**Post General Journal Lines**</span></span>|<span data-ttu-id="ea872-123">Geef op of u de betalingsregels naar het grootboek wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="ea872-123">Specify if you want to transfer the payment lines to the general ledger.</span></span>|  
    |<span data-ttu-id="ea872-124">**Dimensies opnemen**</span><span class="sxs-lookup"><span data-stu-id="ea872-124">**Include Dimensions**</span></span>|<span data-ttu-id="ea872-125">Hier kunt u de dimensies invoeren die u in het SEPA-betalingsrapport wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="ea872-125">Enter the dimensions that you want to include in the non-euro SEPA payment report.</span></span> <span data-ttu-id="ea872-126">De optie is alleen beschikbaar als het veld **Alg. dagb.regels samenvatten** op de pagina **Elektronisch bankieren instellen** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="ea872-126">The option is only available if the **Summarize Gen. Jnl. Lines** field on the **Electronic Banking Setup** page is selected.</span></span>|  
    |<span data-ttu-id="ea872-127">**Uitvoeringsdatum**</span><span class="sxs-lookup"><span data-stu-id="ea872-127">**Execution Date**</span></span>|<span data-ttu-id="ea872-128">Voer een uitvoeringsdatum in als u op de betalingsregels een datum wilt hebben die afwijkt van de boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="ea872-128">Enter an execution date if you want an execution date that differs from the posting date on the payment lines.</span></span>|  
    |<span data-ttu-id="ea872-129">**Bestandsnaam**</span><span class="sxs-lookup"><span data-stu-id="ea872-129">**File Name**</span></span>|<span data-ttu-id="ea872-130">Voer de naam in van het bestand, inclusief station en map, waarin u het rapport wilt afdrukken.</span><span class="sxs-lookup"><span data-stu-id="ea872-130">Enter the name of the file, including the drive and folder, to which you want to print the report.</span></span>|  

3.  <span data-ttu-id="ea872-131">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="ea872-131">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ea872-132">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ea872-132">See Also</span></span>  
 <span data-ttu-id="ea872-133">[SEPA-betalingen indienen](how-to-file-sepa-payments.md) </span><span class="sxs-lookup"><span data-stu-id="ea872-133">[File SEPA Payments](how-to-file-sepa-payments.md) </span></span>  
 <span data-ttu-id="ea872-134">[SEPA-betalingen activeren](how-to-activate-sepa-payments.md) </span><span class="sxs-lookup"><span data-stu-id="ea872-134">[Activate SEPA Payments](how-to-activate-sepa-payments.md) </span></span>  
 [<span data-ttu-id="ea872-135">SEPA-betalingen</span><span class="sxs-lookup"><span data-stu-id="ea872-135">SEPA Payments</span></span>](sepa-payments.md)
