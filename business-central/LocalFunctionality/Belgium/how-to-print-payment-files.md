---
title: Betalingsbestanden afdrukken
description: Als u een testrapport hebt afgedrukt en alle fouten hebt gecorrigeerd, kunt u betalingsdagboekregels naar een betalingsbestand afdrukken.
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
ms.openlocfilehash: 7fb0ddd7f635f20d61163b0bfae950c9aa065230
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="print-payment-files"></a><span data-ttu-id="e301a-103">Betalingsbestanden afdrukken</span><span class="sxs-lookup"><span data-stu-id="e301a-103">Print Payment Files</span></span>
<span data-ttu-id="e301a-104">Als u een testrapport hebt afgedrukt en alle fouten hebt gecorrigeerd, kunt u betalingsdagboekregels naar een betalingsbestand afdrukken.</span><span class="sxs-lookup"><span data-stu-id="e301a-104">After you have printed a test report and corrected all errors, you can print the payment journal lines to a payment file.</span></span>  

<span data-ttu-id="e301a-105">Een betalingsbestand bevat binnenlandse, internationale of SEPA-betalingen (in euro's of in een andere valuta).</span><span class="sxs-lookup"><span data-stu-id="e301a-105">A payment file contains either domestic, international, SEPA, or non-euro SEPA payments.</span></span> <span data-ttu-id="e301a-106">Het bestand kan per schijf of via een modem of Isabel (Interbanks Standards Association Belgium) worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="e301a-106">The file can be sent to a bank either on disk, by modem, or via Interbanks Standards Association Belgium (Isabel).</span></span> <span data-ttu-id="e301a-107">U kunt slechts één bestand per boekingsdatum en valutacode maken.</span><span class="sxs-lookup"><span data-stu-id="e301a-107">You can only create one file for each posting date and each currency code.</span></span> <span data-ttu-id="e301a-108">Wanneer u de betalingen naar een bestand exporteert, wordt er een bijbehorende notitie afgedrukt die ook naar de bank kan worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="e301a-108">When you export the payments to a file, an accompanying note is printed, which can also be sent to the bank.</span></span>  

<span data-ttu-id="e301a-109">In het betalingsdagboek wordt het veld **Status** op de geëxporteerde regels ingesteld op **Geboekt**.</span><span class="sxs-lookup"><span data-stu-id="e301a-109">In the payment journal, the **Status** field on the exported lines will be set to **Posted**.</span></span>  

## <a name="to-print-a-payment-file"></a><span data-ttu-id="e301a-110">Een betalingsbestand afdrukken</span><span class="sxs-lookup"><span data-stu-id="e301a-110">To print a payment file</span></span>  

1.  <span data-ttu-id="e301a-111">Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsdagboek** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="e301a-111">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="e301a-112">Vul op het sneltabblad **Opties** de velden in zoals in de volgende tabel wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="e301a-112">On the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="e301a-113">Veld</span><span class="sxs-lookup"><span data-stu-id="e301a-113">Field</span></span>|<span data-ttu-id="e301a-114">Description</span><span class="sxs-lookup"><span data-stu-id="e301a-114">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="e301a-115">**Batchnaam**</span><span class="sxs-lookup"><span data-stu-id="e301a-115">**Batch Name**</span></span>|<span data-ttu-id="e301a-116">Geef de batchnaam van het betalingsdagboek op.</span><span class="sxs-lookup"><span data-stu-id="e301a-116">Specify the batch name of the payment journal.</span></span>|  
    |<span data-ttu-id="e301a-117">**Bankrekening**</span><span class="sxs-lookup"><span data-stu-id="e301a-117">**Bank Account**</span></span>|<span data-ttu-id="e301a-118">Geef de bankrekening van het betalingsdagboek op.</span><span class="sxs-lookup"><span data-stu-id="e301a-118">Specify the bank account of the payment journal.</span></span>|  
    |<span data-ttu-id="e301a-119">**Exportprotocol**</span><span class="sxs-lookup"><span data-stu-id="e301a-119">**Export Protocol**</span></span>|<span data-ttu-id="e301a-120">Geef de exportprotocolcode van de betalingsdagboekregel op.</span><span class="sxs-lookup"><span data-stu-id="e301a-120">Specify the export protocol code of the payment journal line.</span></span> <span data-ttu-id="e301a-121">Exportprotocollen bepalen welk betalingsbestand in het betalingsdagboek wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="e301a-121">Export protocols control which payment file will be generated in the payment journal.</span></span><br /><br /> <span data-ttu-id="e301a-122">U kunt een combinatie van exportindelingen in één batch hebben, bijvoorbeeld binnenlandse, internationale en SEPA-betalingen.</span><span class="sxs-lookup"><span data-stu-id="e301a-122">You can have a mixture of export formats in a single batch, such as domestic, international, SEPA, or a combination of these.</span></span> <span data-ttu-id="e301a-123">Wanneer u de betalingsregels naar een bestand exporteert, kunt u echter slechts één exportindeling, of exportprotocol, gebruiken.</span><span class="sxs-lookup"><span data-stu-id="e301a-123">However, when exporting the payment lines to a file, you can only use one export format, or export protocol.</span></span> <span data-ttu-id="e301a-124">**Opmerking:** door het exportprotocol op te geven, geeft u ook het validatietype op dat wordt uitgevoerd in het betalingsdagboek.</span><span class="sxs-lookup"><span data-stu-id="e301a-124">**Note:**  By defining the export protocol, you also define the type of validation that will be performed in the payment journal.</span></span>|  

3.  <span data-ttu-id="e301a-125">Kies de actie **Betalingsregels controleren**.</span><span class="sxs-lookup"><span data-stu-id="e301a-125">Choose the **Check Payment Lines** action.</span></span>

    <span data-ttu-id="e301a-126">Het venster **Logboeken voor controlefouten exporteren** bevat eventuele fouten die kunnen bestaan.</span><span class="sxs-lookup"><span data-stu-id="e301a-126">The **Export Check Error Logs** window displays any errors that may exist.</span></span> <span data-ttu-id="e301a-127">Als er fouten zijn, moet u deze oplossen voordat u verder kunt gaan.</span><span class="sxs-lookup"><span data-stu-id="e301a-127">If there are errors, you must fix the errors before you can continue.</span></span>

4. <span data-ttu-id="e301a-128">Als er geen fouten zijn, kiest u de actie **Betalingsregels exporteren**.</span><span class="sxs-lookup"><span data-stu-id="e301a-128">If there are no errors, choose the **Export Payment Lines** action.</span></span>  

    <span data-ttu-id="e301a-129">Vervolgens wordt het rapport geopend dat u in het veld **Testrapport-id** in **Betalingsdagboeksjablonen** hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="e301a-129">The report that you specified in the **Test Report ID** field in the **EB Payment Journal Templates** will open.</span></span>  

5.  <span data-ttu-id="e301a-130">Klik op **Afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="e301a-130">Choose the **Print** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e301a-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e301a-131">See Also</span></span>  
 <span data-ttu-id="e301a-132">[Elektronisch bankieren voor België](belgian-electronic-banking.md) </span><span class="sxs-lookup"><span data-stu-id="e301a-132">[Belgian Electronic Banking](belgian-electronic-banking.md) </span></span>  
 <span data-ttu-id="e301a-133">[Belgische elektronische betalingen](belgian-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="e301a-133">[Belgian Electronic Payments](belgian-electronic-payments.md) </span></span>  
 <span data-ttu-id="e301a-134">[Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md) </span><span class="sxs-lookup"><span data-stu-id="e301a-134">[Set Up Electronic Banking](how-to-set-up-electronic-banking.md) </span></span>  
 <span data-ttu-id="e301a-135">[IBLC-BLWI-transactiecodes instellen](how-to-set-up-iblc-blwi-transaction-codes.md) </span><span class="sxs-lookup"><span data-stu-id="e301a-135">[Set Up IBLC-BLWI Transaction Codes](how-to-set-up-iblc-blwi-transaction-codes.md) </span></span>  
 <span data-ttu-id="e301a-136">[Leveranciers voor automatische betalingsvoorstellen instellen](how-to-set-up-vendors-for-automatic-payment-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="e301a-136">[Set Up Vendors for Automatic Payment Suggestions](how-to-set-up-vendors-for-automatic-payment-suggestions.md) </span></span>  
 <span data-ttu-id="e301a-137">[Betalingsvoorstellen genereren](how-to-generate-payment-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="e301a-137">[Generate Payment Suggestions](how-to-generate-payment-suggestions.md) </span></span>  
 <span data-ttu-id="e301a-138">[Betalingsdagboeksjablonen en -batches maken](how-to-create-payment-journal-templates-and-batches.md) </span><span class="sxs-lookup"><span data-stu-id="e301a-138">[Create Payment Journal Templates and Batches](how-to-create-payment-journal-templates-and-batches.md) </span></span>  
 <span data-ttu-id="e301a-139">[Elektronische betalingen testen](how-to-test-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="e301a-139">[Test Electronic Payments](how-to-test-electronic-payments.md) </span></span>  
 [<span data-ttu-id="e301a-140">Regels voor elektronische betalingen beheren</span><span class="sxs-lookup"><span data-stu-id="e301a-140">Manage Electronic Payment Lines</span></span>](how-to-manage-electronic-payment-lines.md)

