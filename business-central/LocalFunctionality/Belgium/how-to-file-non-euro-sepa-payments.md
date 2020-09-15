---
title: SEPA-betalingen in andere valuta's dan de euro indienen
description: In de Belgische versie van Business Central kunt u niet-euro SEPA-betalingen bij de bank archiveren. Dit is handig als u betalingen verzendt naar andere landen/regio's die SEPA niet gebruiken en voor andere valuta's dan de euro.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: de0f65c55f3866e16c7fa53d9c0b606786cd8913
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778473"
---
# <a name="file-non-euro-sepa-payments"></a><span data-ttu-id="1ede8-104">SEPA-betalingen in andere valuta's dan de euro indienen</span><span class="sxs-lookup"><span data-stu-id="1ede8-104">File Non-Euro SEPA Payments</span></span>
<span data-ttu-id="1ede8-105">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u SEPA-betalingen in andere valuta's dan de euro indienen bij de bank.</span><span class="sxs-lookup"><span data-stu-id="1ede8-105">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can file non-euro SEPA payments with the bank.</span></span> <span data-ttu-id="1ede8-106">Dit is handig als u betalingen verzendt naar andere landen/regio's die SEPA niet gebruiken en voor andere valuta's dan de euro.</span><span class="sxs-lookup"><span data-stu-id="1ede8-106">This is useful when you make payments to other countries that do not use SEPA and for currencies other than the euro.</span></span>  

<span data-ttu-id="1ede8-107">Voordat u een dergelijke SEPA-betalingen kunt indienen, moet u de volgende beheertaken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="1ede8-107">Before you can file a non-euro SEPA payment you must complete the following administration tasks:</span></span>  

- <span data-ttu-id="1ede8-108">Stel een nieuw exportprotocol voor een niet-euro-SEPA in.</span><span class="sxs-lookup"><span data-stu-id="1ede8-108">Set up a new export protocol for a non-euro SEPA.</span></span>  
- <span data-ttu-id="1ede8-109">Schakel in de tabel **Land/regio** het veld **SEPA toegestaan** uit voor elk land in de EEA-zone.</span><span class="sxs-lookup"><span data-stu-id="1ede8-109">In the **Country/Region** table, clear the **SEPA Allowed** field for each country that belongs to the EEA zone.</span></span>  
- <span data-ttu-id="1ede8-110">Controleer of de waarde in het veld **Valuta Euro** in de tabel **Boekhoudinstellingen** niet in euro's is.</span><span class="sxs-lookup"><span data-stu-id="1ede8-110">Verify that the **Currency Euro** field in the **General Ledger Setup** table is not in euro currency.</span></span>  
- <span data-ttu-id="1ede8-111">Controleer of het veld **Bankrekening van voorkeur** in de tabel **Leverancier** de IBAN en SWIFT-code bevat.</span><span class="sxs-lookup"><span data-stu-id="1ede8-111">Verify that the vendor’s **Preferred Bank Account** field in the **Vendor** table contains the IBAN and SWIFT code.</span></span>  

## <a name="to-file-a-non-euro-sepa-payment"></a><span data-ttu-id="1ede8-112">Een SEPA-betaling in andere valuta's dan de euro indienen</span><span class="sxs-lookup"><span data-stu-id="1ede8-112">To file a non-euro SEPA payment</span></span>  

1.  <span data-ttu-id="1ede8-113">Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **SEPA-betalingen in andere valuta's dan de euro indienen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="1ede8-113">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **File Non Euro SEPA Payments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1ede8-114">Vul de velden in zoals beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="1ede8-114">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="1ede8-115">Veld</span><span class="sxs-lookup"><span data-stu-id="1ede8-115">Field</span></span>|<span data-ttu-id="1ede8-116">Description</span><span class="sxs-lookup"><span data-stu-id="1ede8-116">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="1ede8-117">**Dagboeksjabloon**</span><span class="sxs-lookup"><span data-stu-id="1ede8-117">**Journal Template Name**</span></span>|<span data-ttu-id="1ede8-118">Geef de dagboeksjabloon voor het SEPA-betalingsrapport op.</span><span class="sxs-lookup"><span data-stu-id="1ede8-118">Specify the general journal template for the non-euro SEPA payment report.</span></span>|  
    |<span data-ttu-id="1ede8-119">**Dagboekbatch**</span><span class="sxs-lookup"><span data-stu-id="1ede8-119">**Journal Batch**</span></span>|<span data-ttu-id="1ede8-120">Geef de dagboekbatch voor het SEPA-betalingsrapport op.</span><span class="sxs-lookup"><span data-stu-id="1ede8-120">Specify the general journal batch for the non-euro SEPA payment report.</span></span>|  
    |<span data-ttu-id="1ede8-121">**Dagboekregels boeken**</span><span class="sxs-lookup"><span data-stu-id="1ede8-121">**Post General Journal Lines**</span></span>|<span data-ttu-id="1ede8-122">Geef op of u de betalingsregels naar het grootboek wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="1ede8-122">Specify if you want to transfer the payment lines to the general ledger.</span></span>|  
    |<span data-ttu-id="1ede8-123">**Dimensies opnemen**</span><span class="sxs-lookup"><span data-stu-id="1ede8-123">**Include Dimensions**</span></span>|<span data-ttu-id="1ede8-124">Hier kunt u de dimensies invoeren die u in het SEPA-betalingsrapport wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="1ede8-124">Enter the dimensions that you want to include in the non-euro SEPA payment report.</span></span> <span data-ttu-id="1ede8-125">De optie is alleen beschikbaar als het veld **Alg. dagb.regels samenvatten** op de pagina **Elektronisch bankieren instellen** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="1ede8-125">The option is available only if the **Summarize Gen. Jnl. Lines** field on the **Electronic Banking Setup** page is selected.</span></span>|  
    |<span data-ttu-id="1ede8-126">**Uitvoeringsdatum**</span><span class="sxs-lookup"><span data-stu-id="1ede8-126">**Execution Date**</span></span>|<span data-ttu-id="1ede8-127">Voer een uitvoeringsdatum in als u op de betalingsregels een datum wilt hebben die afwijkt van de boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="1ede8-127">Enter an execution date if you want an execution date that differs from the posting date on the payment lines.</span></span>|  
    |<span data-ttu-id="1ede8-128">**Bestandsnaam**</span><span class="sxs-lookup"><span data-stu-id="1ede8-128">**File Name**</span></span>|<span data-ttu-id="1ede8-129">Voer de naam in van het bestand, inclusief station en map, waarin u het rapport wilt afdrukken.</span><span class="sxs-lookup"><span data-stu-id="1ede8-129">Enter the name of the file, including the drive and folder, to which you want to print the report.</span></span>|  

3.  <span data-ttu-id="1ede8-130">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ede8-130">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1ede8-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1ede8-131">See Also</span></span>  
 <span data-ttu-id="1ede8-132">[SEPA-betalingen indienen](how-to-file-sepa-payments.md) </span><span class="sxs-lookup"><span data-stu-id="1ede8-132">[File SEPA Payments](how-to-file-sepa-payments.md) </span></span>  
 <span data-ttu-id="1ede8-133">[SEPA-betalingen activeren](how-to-activate-sepa-payments.md) </span><span class="sxs-lookup"><span data-stu-id="1ede8-133">[Activate SEPA Payments](how-to-activate-sepa-payments.md) </span></span>  
 [<span data-ttu-id="1ede8-134">SEPA-betalingen</span><span class="sxs-lookup"><span data-stu-id="1ede8-134">SEPA Payments</span></span>](sepa-payments.md)
