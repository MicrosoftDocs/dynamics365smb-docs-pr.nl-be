---
title: SEPA-betalingen indienen
description: In Business Central kunt u SEPA-kredietoverboekingen (Single Euro Payments Area) gebruiken om SEPA-betalingen in te dienen bij de bank.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c4784e9181c188634084123ed8cb94b7da8eff6b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379550"
---
# <a name="file-sepa-payments"></a><span data-ttu-id="ca786-103">SEPA-betalingen indienen</span><span class="sxs-lookup"><span data-stu-id="ca786-103">File SEPA Payments</span></span>
<span data-ttu-id="ca786-104">In [!INCLUDE[prod_short](../../includes/prod_short.md)] kunt u SEPA-kredietoverboekingen (Single Euro Payments Area) gebruiken om SEPA-betalingen in te dienen bij de bank.</span><span class="sxs-lookup"><span data-stu-id="ca786-104">In [!INCLUDE[prod_short](../../includes/prod_short.md)], you can use Single Euro Payments Area (SEPA) credit transfers to file SEPA payments with the bank.</span></span>  

<span data-ttu-id="ca786-105">SEPA verenigt de betalingsmethoden in deelnemende Europese landen/regio's, zodat internationale betalingen even gemakkelijk te verwerken worden als binnenlandse betalingen.</span><span class="sxs-lookup"><span data-stu-id="ca786-105">SEPA unifies payment methods in participating European countries/regions, which makes international payments as easy to process as domestic payments.</span></span> <span data-ttu-id="ca786-106">Europese burgers en bedrijven kunnen betalingen in euro's verrichten en ontvangen, binnen of buiten nationale grenzen, onder dezelfde basisomstandigheden, -rechten en -verplichtingen, ongeacht de locatie.</span><span class="sxs-lookup"><span data-stu-id="ca786-106">European citizens and companies can make and receive payments in euros, whether within or across national borders, with the same basic conditions, rights, and obligations, regardless of location.</span></span>  

<span data-ttu-id="ca786-107">Voordat u een SEPA-betaling kunt indienen, moet u de volgende beheertaken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="ca786-107">Before you can file a SEPA payment, you must complete the following administration tasks:</span></span>  

- <span data-ttu-id="ca786-108">Stel een nieuw exportprotocol in.</span><span class="sxs-lookup"><span data-stu-id="ca786-108">Set up a new export protocol.</span></span>
- <span data-ttu-id="ca786-109">Schakel in de tabel **Land/regio** het veld **SEPA toegestaan** in voor elk land in de EEA-zone.</span><span class="sxs-lookup"><span data-stu-id="ca786-109">In the **Country/Region** table, select the **SEPA Allowed** field for each country that belongs to the EEA zone.</span></span>  
- <span data-ttu-id="ca786-110">Controleer of de waarde in het veld **Valuta Euro** in de tabel **Boekhoudinstellingen** overeenkomt met de valuta op de betalingsregels.</span><span class="sxs-lookup"><span data-stu-id="ca786-110">Verify that the **Currency Euro** field in the **General Ledger Setup** table corresponds with the currency in the payment lines.</span></span>  
- <span data-ttu-id="ca786-111">Controleer of het veld **Bankrekening van voorkeur** in de tabel **Leverancier** de IBAN en SWIFT-code bevat.</span><span class="sxs-lookup"><span data-stu-id="ca786-111">Verify that the vendor’s **Preferred Bank Account** field in the **Vendor** table contains the IBAN and SWIFT code.</span></span>  

## <a name="to-file-a-sepa-payment"></a><span data-ttu-id="ca786-112">Een SEPA-betaling indienen</span><span class="sxs-lookup"><span data-stu-id="ca786-112">To file a SEPA payment</span></span>  

1.  <span data-ttu-id="ca786-113">Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **SEPA-betalingen indienen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ca786-113">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **File SEPA Payments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ca786-114">Vul de velden in zoals beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="ca786-114">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="ca786-115">Veld</span><span class="sxs-lookup"><span data-stu-id="ca786-115">Field</span></span>|<span data-ttu-id="ca786-116">Description</span><span class="sxs-lookup"><span data-stu-id="ca786-116">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="ca786-117">**Dagboeksjabloon**</span><span class="sxs-lookup"><span data-stu-id="ca786-117">**Journal Template Name**</span></span>|<span data-ttu-id="ca786-118">Geef de dagboeksjabloon voor het SEPA-betalingsrapport op.</span><span class="sxs-lookup"><span data-stu-id="ca786-118">Specify the general journal template for the SEPA payment report.</span></span>|  
    |<span data-ttu-id="ca786-119">**Dagboekbatch**</span><span class="sxs-lookup"><span data-stu-id="ca786-119">**Journal Batch**</span></span>|<span data-ttu-id="ca786-120">Geef de dagboekbatch voor het SEPA-betalingsrapport op.</span><span class="sxs-lookup"><span data-stu-id="ca786-120">Specify the general journal batch for the SEPA payment report.</span></span>|  
    |<span data-ttu-id="ca786-121">**Dagboekregels boeken**</span><span class="sxs-lookup"><span data-stu-id="ca786-121">**Post General Journal Lines**</span></span>|<span data-ttu-id="ca786-122">Geef op of u de betalingsregels naar het grootboek wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="ca786-122">Specify if you want to transfer the payment lines to the general ledger.</span></span>|  
    |<span data-ttu-id="ca786-123">**Dimensies opnemen**</span><span class="sxs-lookup"><span data-stu-id="ca786-123">**Include Dimensions**</span></span>|<span data-ttu-id="ca786-124">Hier kunt u de dimensies invoeren die u in het SEPA-betalingsrapport wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="ca786-124">Enter the dimensions that you want to include in the SEPA payment report.</span></span> <span data-ttu-id="ca786-125">De optie is alleen beschikbaar als het veld **Alg. dagb.regels samenvatten** op de pagina **Elektronisch bankieren instellen** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="ca786-125">The option is available only if the **Summarize Gen. Jnl. Lines** field on the **Electronic Banking Setup** page is selected.</span></span>|  
    |<span data-ttu-id="ca786-126">**Uitvoeringsdatum**</span><span class="sxs-lookup"><span data-stu-id="ca786-126">**Execution Date**</span></span>|<span data-ttu-id="ca786-127">Voer een uitvoeringsdatum in als u op de betalingsregels een datum wilt hebben die afwijkt van de boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="ca786-127">Enter an execution date if you want an execution date that differs from the posting date on the payment lines.</span></span>|  
    |<span data-ttu-id="ca786-128">**Bestandsnaam**</span><span class="sxs-lookup"><span data-stu-id="ca786-128">**File Name**</span></span>|<span data-ttu-id="ca786-129">Voer de naam in van het bestand, inclusief station en map, waarin u het rapport wilt afdrukken.</span><span class="sxs-lookup"><span data-stu-id="ca786-129">Enter the name of the file, including the drive and folder, to which you want to print the report.</span></span>|  

3.  <span data-ttu-id="ca786-130">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca786-130">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ca786-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ca786-131">See Also</span></span>  
 <span data-ttu-id="ca786-132">[Exportprotocollen instellen](how-to-set-up-export-protocols.md) </span><span class="sxs-lookup"><span data-stu-id="ca786-132">[Set Up Export Protocols](how-to-set-up-export-protocols.md) </span></span>  
 <span data-ttu-id="ca786-133">[SEPA-betalingen in andere valuta's dan de euro indienen](how-to-file-non-euro-sepa-payments.md) </span><span class="sxs-lookup"><span data-stu-id="ca786-133">[File Non-Euro SEPA Payments](how-to-file-non-euro-sepa-payments.md) </span></span>  
 [<span data-ttu-id="ca786-134">SEPA-betalingen activeren</span><span class="sxs-lookup"><span data-stu-id="ca786-134">Activate SEPA Payments</span></span>](how-to-activate-sepa-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]