---
title: SEPA-betalingen indienen
description: In Business Central kunt u SEPA-kredietoverboekingen (Single Euro Payments Area) gebruiken om SEPA-betalingen in te dienen bij de bank.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: aacb7668739e5c97492b128d3c6800e9bd60b47c
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677171"
---
# <a name="file-sepa-payments"></a><span data-ttu-id="2ff48-103">SEPA-betalingen indienen</span><span class="sxs-lookup"><span data-stu-id="2ff48-103">File SEPA Payments</span></span>
<span data-ttu-id="2ff48-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u SEPA-kredietoverboekingen (Single Euro Payments Area) gebruiken om SEPA-betalingen in te dienen bij de bank.</span><span class="sxs-lookup"><span data-stu-id="2ff48-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can use Single Euro Payments Area (SEPA) credit transfers to file SEPA payments with the bank.</span></span>  

<span data-ttu-id="2ff48-105">SEPA verenigt de betalingsmethoden in deelnemende Europese landen/regio's, zodat internationale betalingen even gemakkelijk te verwerken worden als binnenlandse betalingen.</span><span class="sxs-lookup"><span data-stu-id="2ff48-105">SEPA unifies payment methods in participating European countries/regions, which makes international payments as easy to process as domestic payments.</span></span> <span data-ttu-id="2ff48-106">Europese burgers en bedrijven kunnen betalingen in euro's verrichten en ontvangen, binnen of buiten nationale grenzen, onder dezelfde basisomstandigheden, -rechten en -verplichtingen, ongeacht de locatie.</span><span class="sxs-lookup"><span data-stu-id="2ff48-106">European citizens and companies can make and receive payments in euros, whether within or across national borders, with the same basic conditions, rights, and obligations, regardless of location.</span></span>  

<span data-ttu-id="2ff48-107">Voordat u een SEPA-betaling kunt indienen, moet u de volgende beheertaken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="2ff48-107">Before you can file a SEPA payment, you must complete the following administration tasks:</span></span>  

- <span data-ttu-id="2ff48-108">Stel een nieuw exportprotocol in.</span><span class="sxs-lookup"><span data-stu-id="2ff48-108">Set up a new export protocol.</span></span>
- <span data-ttu-id="2ff48-109">Schakel in de tabel **Land/regio** het veld **SEPA toegestaan** in voor elk land in de EEA-zone.</span><span class="sxs-lookup"><span data-stu-id="2ff48-109">In the **Country/Region** table, select the **SEPA Allowed** field for each country that belongs to the EEA zone.</span></span>  
- <span data-ttu-id="2ff48-110">Controleer of de waarde in het veld **Valuta Euro** in de tabel **Boekhoudinstellingen** overeenkomt met de valuta op de betalingsregels.</span><span class="sxs-lookup"><span data-stu-id="2ff48-110">Verify that the **Currency Euro** field in the **General Ledger Setup** table corresponds with the currency in the payment lines.</span></span>  
- <span data-ttu-id="2ff48-111">Controleer of het veld **Bankrekening van voorkeur** in de tabel **Leverancier** de IBAN en SWIFT-code bevat.</span><span class="sxs-lookup"><span data-stu-id="2ff48-111">Verify that the vendor’s **Preferred Bank Account** field in the **Vendor** table contains the IBAN and SWIFT code.</span></span>  

## <a name="to-file-a-sepa-payment"></a><span data-ttu-id="2ff48-112">Een SEPA-betaling indienen</span><span class="sxs-lookup"><span data-stu-id="2ff48-112">To file a SEPA payment</span></span>  

1.  <span data-ttu-id="2ff48-113">Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **SEPA-betalingen indienen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="2ff48-113">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **File SEPA Payments**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="2ff48-114">Vul de velden in zoals beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="2ff48-114">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="2ff48-115">Veld</span><span class="sxs-lookup"><span data-stu-id="2ff48-115">Field</span></span>|<span data-ttu-id="2ff48-116">Description</span><span class="sxs-lookup"><span data-stu-id="2ff48-116">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="2ff48-117">**Dagboeksjabloon**</span><span class="sxs-lookup"><span data-stu-id="2ff48-117">**Journal Template Name**</span></span>|<span data-ttu-id="2ff48-118">Geef de dagboeksjabloon voor het SEPA-betalingsrapport op.</span><span class="sxs-lookup"><span data-stu-id="2ff48-118">Specify the general journal template for the SEPA payment report.</span></span>|  
    |<span data-ttu-id="2ff48-119">**Dagboekbatch**</span><span class="sxs-lookup"><span data-stu-id="2ff48-119">**Journal Batch**</span></span>|<span data-ttu-id="2ff48-120">Geef de dagboekbatch voor het SEPA-betalingsrapport op.</span><span class="sxs-lookup"><span data-stu-id="2ff48-120">Specify the general journal batch for the SEPA payment report.</span></span>|  
    |<span data-ttu-id="2ff48-121">**Dagboekregels boeken**</span><span class="sxs-lookup"><span data-stu-id="2ff48-121">**Post General Journal Lines**</span></span>|<span data-ttu-id="2ff48-122">Geef op of u de betalingsregels naar het grootboek wilt overbrengen.</span><span class="sxs-lookup"><span data-stu-id="2ff48-122">Specify if you want to transfer the payment lines to the general ledger.</span></span>|  
    |<span data-ttu-id="2ff48-123">**Dimensies opnemen**</span><span class="sxs-lookup"><span data-stu-id="2ff48-123">**Include Dimensions**</span></span>|<span data-ttu-id="2ff48-124">Hier kunt u de dimensies invoeren die u in het SEPA-betalingsrapport wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="2ff48-124">Enter the dimensions that you want to include in the SEPA payment report.</span></span> <span data-ttu-id="2ff48-125">De optie is alleen beschikbaar als het veld **Alg. dagb.regels samenvatten** op de pagina **Elektronisch bankieren instellen** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="2ff48-125">The option is available only if the **Summarize Gen. Jnl. Lines** field on the **Electronic Banking Setup** page is selected.</span></span>|  
    |<span data-ttu-id="2ff48-126">**Uitvoeringsdatum**</span><span class="sxs-lookup"><span data-stu-id="2ff48-126">**Execution Date**</span></span>|<span data-ttu-id="2ff48-127">Voer een uitvoeringsdatum in als u op de betalingsregels een datum wilt hebben die afwijkt van de boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="2ff48-127">Enter an execution date if you want an execution date that differs from the posting date on the payment lines.</span></span>|  
    |<span data-ttu-id="2ff48-128">**Bestandsnaam**</span><span class="sxs-lookup"><span data-stu-id="2ff48-128">**File Name**</span></span>|<span data-ttu-id="2ff48-129">Voer de naam in van het bestand, inclusief station en map, waarin u het rapport wilt afdrukken.</span><span class="sxs-lookup"><span data-stu-id="2ff48-129">Enter the name of the file, including the drive and folder, to which you want to print the report.</span></span>|  

3.  <span data-ttu-id="2ff48-130">Kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="2ff48-130">Choose the **OK** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2ff48-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2ff48-131">See Also</span></span>  
 <span data-ttu-id="2ff48-132">[Exportprotocollen instellen](how-to-set-up-export-protocols.md) </span><span class="sxs-lookup"><span data-stu-id="2ff48-132">[Set Up Export Protocols](how-to-set-up-export-protocols.md) </span></span>  
 <span data-ttu-id="2ff48-133">[SEPA-betalingen in andere valuta's dan de euro indienen](how-to-file-non-euro-sepa-payments.md) </span><span class="sxs-lookup"><span data-stu-id="2ff48-133">[File Non-Euro SEPA Payments](how-to-file-non-euro-sepa-payments.md) </span></span>  
 [<span data-ttu-id="2ff48-134">SEPA-betalingen activeren</span><span class="sxs-lookup"><span data-stu-id="2ff48-134">Activate SEPA Payments</span></span>](how-to-activate-sepa-payments.md)
