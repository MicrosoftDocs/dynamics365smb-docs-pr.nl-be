---
title: Betalingsbestanden afdrukken
description: Als u een testrapport hebt afgedrukt en alle fouten hebt gecorrigeerd, kunt u betalingsdagboekregels naar een betalingsbestand afdrukken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: ec0174d20ad7e4f31037302931200dcf89657c35
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778452"
---
# <a name="print-payment-files"></a><span data-ttu-id="425e4-103">Betalingsbestanden afdrukken</span><span class="sxs-lookup"><span data-stu-id="425e4-103">Print Payment Files</span></span>
<span data-ttu-id="425e4-104">Als u een testrapport hebt afgedrukt en alle fouten hebt gecorrigeerd, kunt u betalingsdagboekregels naar een betalingsbestand afdrukken.</span><span class="sxs-lookup"><span data-stu-id="425e4-104">After you have printed a test report and corrected all errors, you can print the payment journal lines to a payment file.</span></span>  

<span data-ttu-id="425e4-105">Een betalingsbestand bevat binnenlandse, internationale of SEPA-betalingen (in euro's of in een andere valuta).</span><span class="sxs-lookup"><span data-stu-id="425e4-105">A payment file contains either domestic, international, SEPA, or non-euro SEPA payments.</span></span> <span data-ttu-id="425e4-106">Het bestand kan per schijf of via een modem of Isabel (Interbanks Standards Association Belgium) worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="425e4-106">The file can be sent to a bank either on disk, by modem, or via Interbanks Standards Association Belgium (Isabel).</span></span> <span data-ttu-id="425e4-107">U kunt slechts één bestand per boekingsdatum en valutacode maken.</span><span class="sxs-lookup"><span data-stu-id="425e4-107">You can create only one file for each posting date and each currency code.</span></span> <span data-ttu-id="425e4-108">Wanneer u de betalingen naar een bestand exporteert, wordt er een bijbehorende notitie afgedrukt die ook naar de bank kan worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="425e4-108">When you export the payments to a file, an accompanying note is printed, which can also be sent to the bank.</span></span>  

<span data-ttu-id="425e4-109">In het betalingsdagboek wordt het veld **Status** op de geëxporteerde regels ingesteld op **Geboekt**.</span><span class="sxs-lookup"><span data-stu-id="425e4-109">In the payment journal, the **Status** field on the exported lines will be set to **Posted**.</span></span>  

## <a name="to-print-a-payment-file"></a><span data-ttu-id="425e4-110">Een betalingsbestand afdrukken</span><span class="sxs-lookup"><span data-stu-id="425e4-110">To print a payment file</span></span>  

1.  <span data-ttu-id="425e4-111">Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboek** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="425e4-111">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journal**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="425e4-112">Vul de velden in zoals beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="425e4-112">Fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="425e4-113">Veld</span><span class="sxs-lookup"><span data-stu-id="425e4-113">Field</span></span>|<span data-ttu-id="425e4-114">Description</span><span class="sxs-lookup"><span data-stu-id="425e4-114">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="425e4-115">**Batchnaam**</span><span class="sxs-lookup"><span data-stu-id="425e4-115">**Batch Name**</span></span>|<span data-ttu-id="425e4-116">Geef de batchnaam van het betalingsdagboek op.</span><span class="sxs-lookup"><span data-stu-id="425e4-116">Specify the batch name of the payment journal.</span></span>|  
    |<span data-ttu-id="425e4-117">**Bankrekening**</span><span class="sxs-lookup"><span data-stu-id="425e4-117">**Bank Account**</span></span>|<span data-ttu-id="425e4-118">Geef de bankrekening van het betalingsdagboek op.</span><span class="sxs-lookup"><span data-stu-id="425e4-118">Specify the bank account of the payment journal.</span></span>|  
    |<span data-ttu-id="425e4-119">**Exportprotocol**</span><span class="sxs-lookup"><span data-stu-id="425e4-119">**Export Protocol**</span></span>|<span data-ttu-id="425e4-120">Geef de exportprotocolcode van de betalingsdagboekregel op.</span><span class="sxs-lookup"><span data-stu-id="425e4-120">Specify the export protocol code of the payment journal line.</span></span> <span data-ttu-id="425e4-121">Exportprotocollen bepalen welk betalingsbestand in het betalingsdagboek wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="425e4-121">Export protocols control which payment file will be generated in the payment journal.</span></span><br /><br /> <span data-ttu-id="425e4-122">U kunt een combinatie van exportindelingen in één batch hebben, bijvoorbeeld binnenlandse, internationale en SEPA-betalingen.</span><span class="sxs-lookup"><span data-stu-id="425e4-122">You can have a mixture of export formats in a single batch, such as domestic, international, SEPA, or a combination of these.</span></span> <span data-ttu-id="425e4-123">Wanneer u de betalingsregels naar een bestand exporteert, kunt u slechts één exportindeling, of exportprotocol, gebruiken.</span><span class="sxs-lookup"><span data-stu-id="425e4-123">However, when exporting the payment lines to a file, you can use only one export format, or export protocol.</span></span> <span data-ttu-id="425e4-124">**Opmerking:** door het exportprotocol op te geven, geeft u ook het validatietype op dat wordt uitgevoerd in het betalingsdagboek.</span><span class="sxs-lookup"><span data-stu-id="425e4-124">**Note:**  By defining the export protocol, you also define the type of validation that will be performed in the payment journal.</span></span>|  

3.  <span data-ttu-id="425e4-125">Kies de actie **Betalingsregels controleren**.</span><span class="sxs-lookup"><span data-stu-id="425e4-125">Choose the **Check Payment Lines** action.</span></span>

    <span data-ttu-id="425e4-126">De pagina **Logboeken voor controlefouten exporteren** bevat eventuele fouten.</span><span class="sxs-lookup"><span data-stu-id="425e4-126">The **Export Check Error Logs** page displays any errors that exist.</span></span> <span data-ttu-id="425e4-127">Als er fouten zijn, moet u deze oplossen voordat u kunt doorgaan.</span><span class="sxs-lookup"><span data-stu-id="425e4-127">If there are errors, you must fix them before you can continue.</span></span>

4. <span data-ttu-id="425e4-128">Als er geen fouten zijn, kiest u de actie **Betalingsregels exporteren**.</span><span class="sxs-lookup"><span data-stu-id="425e4-128">If there are no errors, choose the **Export Payment Lines** action.</span></span>  

    <span data-ttu-id="425e4-129">Vervolgens wordt het rapport geopend dat u in het veld **Testrapport-id** in **Betalingsdagboeksjablonen** hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="425e4-129">The report that you specified in the **Test Report ID** field in the **EB Payment Journal Templates** will open.</span></span>  

5.  <span data-ttu-id="425e4-130">Klik op **Afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="425e4-130">Choose the **Print** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="425e4-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="425e4-131">See Also</span></span>  
 <span data-ttu-id="425e4-132">[Elektronisch bankieren voor België](belgian-electronic-banking.md) </span><span class="sxs-lookup"><span data-stu-id="425e4-132">[Belgian Electronic Banking](belgian-electronic-banking.md) </span></span>  
 <span data-ttu-id="425e4-133">[Belgische elektronische betalingen](belgian-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="425e4-133">[Belgian Electronic Payments](belgian-electronic-payments.md) </span></span>  
 <span data-ttu-id="425e4-134">[Elektronisch bankieren instellen](how-to-set-up-electronic-banking.md) </span><span class="sxs-lookup"><span data-stu-id="425e4-134">[Set Up Electronic Banking](how-to-set-up-electronic-banking.md) </span></span>  
 <span data-ttu-id="425e4-135">[IBLC-BLWI-transactiecodes instellen](how-to-set-up-iblc-blwi-transaction-codes.md) </span><span class="sxs-lookup"><span data-stu-id="425e4-135">[Set Up IBLC-BLWI Transaction Codes](how-to-set-up-iblc-blwi-transaction-codes.md) </span></span>  
 <span data-ttu-id="425e4-136">[Leveranciers voor automatische betalingsvoorstellen instellen](how-to-set-up-vendors-for-automatic-payment-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="425e4-136">[Set Up Vendors for Automatic Payment Suggestions](how-to-set-up-vendors-for-automatic-payment-suggestions.md) </span></span>  
 <span data-ttu-id="425e4-137">[Betalingsvoorstellen genereren](how-to-generate-payment-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="425e4-137">[Generate Payment Suggestions](how-to-generate-payment-suggestions.md) </span></span>  
 <span data-ttu-id="425e4-138">[Betalingsdagboeksjablonen en -batches maken](how-to-create-payment-journal-templates-and-batches.md) </span><span class="sxs-lookup"><span data-stu-id="425e4-138">[Create Payment Journal Templates and Batches](how-to-create-payment-journal-templates-and-batches.md) </span></span>  
 <span data-ttu-id="425e4-139">[Elektronische betalingen testen](how-to-test-electronic-payments.md) </span><span class="sxs-lookup"><span data-stu-id="425e4-139">[Test Electronic Payments](how-to-test-electronic-payments.md) </span></span>  
 [<span data-ttu-id="425e4-140">Regels voor elektronische betalingen beheren</span><span class="sxs-lookup"><span data-stu-id="425e4-140">Manage Electronic Payment Lines</span></span>](how-to-manage-electronic-payment-lines.md)
