---
title: De methode voor elektronische betalingen kiezen | Microsoft Docs
description: Verwerk betalingen aan uw leveranciers door samen met de betalingsgegevens van de dagboekregels een bestand te exporteren.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 20ae505bc76b8971c678de9e2664653aa5032d6e
ms.contentlocale: nl-be
ms.lasthandoff: 09/27/2017

---
# <a name="make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a><span data-ttu-id="46faf-103">Betalingen verrichten met de conversieservice van bankgegevens of SEPA-overmaking</span><span class="sxs-lookup"><span data-stu-id="46faf-103">Make Payments with Bank Data Conversion Service or SEPA Credit Transfer</span></span>
<span data-ttu-id="46faf-104">U kunt in het venster **Betalingsdagboek** betalingen naar uw leveranciers verwerken door samen met de betalingsgegevens van de dagboekregels een bestand te exporteren.</span><span class="sxs-lookup"><span data-stu-id="46faf-104">In the **Payment Journal** window, you can process payments to your vendors by exporting a file together with the payment information from the journal lines.</span></span> <span data-ttu-id="46faf-105">Vervolgens kunt u het bestand uploaden naar uw elektronische banksite waar de gerelateerde overboekingen worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="46faf-105">You can then upload the file to your electronic bank where the related money transfers are processed.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="46faf-106"> ondersteunt de indeling voor SEPA-kredietoverboekingen, maar in uw land of regio kunnen andere indelingen voor elektronische betalingen beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="46faf-106"> supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>   

 <span data-ttu-id="46faf-107">Voor het mogelijk maken van SEPA-kredietoverboekingen moet u eerst een bankrekening, leverancier, en dagboekbatch instellen waarop het betalingsdagboek is gebaseerd.</span><span class="sxs-lookup"><span data-stu-id="46faf-107">To enable SEPA credit transfers, you must first set up a bank account, a vendor, and the general journal batch that the payment journal is based on.</span></span> <span data-ttu-id="46faf-108">Bereid vervolgens betalingen aan leveranciers voor door het venster **Betalingsdagboek** automatisch te vullen met verschuldigde betalingen met een opgegeven boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="46faf-108">You then prepare payments to vendors by automatically filling the **Payment Journal** window with due payments with specified posting dates.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="46faf-109">Wanneer u hebt gecontroleerd dat de betalingen zijn verwerkt door de bank, kunt u doorgaan met het boeken van de betalingsdagboekregels.</span><span class="sxs-lookup"><span data-stu-id="46faf-109">When you have verified that the payments are successfully processed by the bank, you can proceed to post the payment journal lines.</span></span>  

 <span data-ttu-id="46faf-110">In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.</span><span class="sxs-lookup"><span data-stu-id="46faf-110">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="46faf-111">**Als u dit wilt doen**</span><span class="sxs-lookup"><span data-stu-id="46faf-111">**To**</span></span>|<span data-ttu-id="46faf-112">**Zie**</span><span class="sxs-lookup"><span data-stu-id="46faf-112">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="46faf-113">Activeer de conversieservice voor bankgegevens om een bankafschriftbestand te laten converteren naar een indeling die u kunt importeren of om uw geëxporteerde betalingsbestanden te laten converteren naar de indeling die uw bank vereist.</span><span class="sxs-lookup"><span data-stu-id="46faf-113">Activate the Bank Data Conversion Service feature to have any bank statement file converted to a format that you can import or to have your exported payment files converted to the format that your bank requires.</span></span>|[<span data-ttu-id="46faf-114">Procedure: Conversieservice voor bankgegevens instellen</span><span class="sxs-lookup"><span data-stu-id="46faf-114">How to: Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)|  
|<span data-ttu-id="46faf-115">Stel een bankrekening, leverancier en betalingsdagboek in voor SEPA-kredietoverboeking.</span><span class="sxs-lookup"><span data-stu-id="46faf-115">Set up a bank account, a vendor, and a payment journal for SEPA credit transfer.</span></span>|[<span data-ttu-id="46faf-116">Procedure: SEPA-krediettransfer instellen</span><span class="sxs-lookup"><span data-stu-id="46faf-116">How to: Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)|  
|<span data-ttu-id="46faf-117">Vul het betalingsdagboek met regels voor verschuldigde betalingen aan leveranciers, met de mogelijkheid boekingsdatums in te voegen op basis van de vervaldatum van de verwante inkoopdocumenten.</span><span class="sxs-lookup"><span data-stu-id="46faf-117">Fill the payment journal with lines for due payments to vendors, with the option to insert posting dates based on the due date of the related purchase documents.</span></span>|[<span data-ttu-id="46faf-118">Betalingsverplichtingen beheren</span><span class="sxs-lookup"><span data-stu-id="46faf-118">Manage Payables</span></span>](payables-manage-payables.md)|  
|<span data-ttu-id="46faf-119">Exporteer betalingsdagboekregels naar een bestand in de SEPA-overmakingsindeling.</span><span class="sxs-lookup"><span data-stu-id="46faf-119">Export payment journal lines to a file in the SEPA Credit Transfer format.</span></span>|[<span data-ttu-id="46faf-120">Procedure: Betalingen naar een bankbestand exporteren</span><span class="sxs-lookup"><span data-stu-id="46faf-120">How to: Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  
|<span data-ttu-id="46faf-121">Controleer welke betalingen zijn geëxporteerd en in welke bestanden.</span><span class="sxs-lookup"><span data-stu-id="46faf-121">Review which payments have been exported and into which files.</span></span>|<span data-ttu-id="46faf-122">Krediettransferregisters</span><span class="sxs-lookup"><span data-stu-id="46faf-122">Credit Transfer Registers</span></span>|  
|<span data-ttu-id="46faf-123">Wanneer de elektronische betaling is verwerkt door de bank, boekt u de betalingen.</span><span class="sxs-lookup"><span data-stu-id="46faf-123">When the electronic payment is successfully processed by the bank, post the payments.</span></span>|[<span data-ttu-id="46faf-124">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="46faf-124">Working with General Journals</span></span>](ui-work-general-journals.md)|  

## <a name="see-also"></a><span data-ttu-id="46faf-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="46faf-125">See Also</span></span>  
[<span data-ttu-id="46faf-126">Procedure: Conversieservice voor bankgegevens instellen</span><span class="sxs-lookup"><span data-stu-id="46faf-126">How to: Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="46faf-127">Procedure: SEPA-krediettransfer instellen</span><span class="sxs-lookup"><span data-stu-id="46faf-127">How to: Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)  
<span data-ttu-id="46faf-128">[Betalingsverplichtingen beheren](payables-manage-payables.md) </span><span class="sxs-lookup"><span data-stu-id="46faf-128">[Manage Payables](payables-manage-payables.md) </span></span>  
[<span data-ttu-id="46faf-129">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="46faf-129">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="46faf-130">Betalingen verzamelen via automatische incasso van SEPA</span><span class="sxs-lookup"><span data-stu-id="46faf-130">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)   

