---
title: Betalingsbestanden afdrukken in de Belgische versie
description: Als u een testrapport hebt afgedrukt en alle fouten hebt gecorrigeerd, kunt u betalingsdagboekregels naar een betalingsbestand afdrukken in de Belgische versie van Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a2536af3bc33354a782a840c4320cc61a217af7a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779221"
---
# <a name="print-payment-files"></a><span data-ttu-id="3f933-103">Betalingsbestanden afdrukken</span><span class="sxs-lookup"><span data-stu-id="3f933-103">Print Payment Files</span></span>

<span data-ttu-id="3f933-104">Als u een testrapport hebt afgedrukt en alle fouten hebt gecorrigeerd, kunt u betalingsdagboekregels naar een betalingsbestand afdrukken.</span><span class="sxs-lookup"><span data-stu-id="3f933-104">After you have printed a test report and corrected all errors, you can print the payment journal lines to a payment file.</span></span>  

<span data-ttu-id="3f933-105">Een betalingsbestand bevat binnenlandse, internationale of SEPA-betalingen (in euro's of in een andere valuta).</span><span class="sxs-lookup"><span data-stu-id="3f933-105">A payment file contains either domestic, international, SEPA, or non-euro SEPA payments.</span></span> <span data-ttu-id="3f933-106">Het bestand kan per schijf of via een modem of Isabel (Interbanks Standards Association Belgium) worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="3f933-106">The file can be sent to a bank either on disk, by modem, or via Interbanks Standards Association Belgium (Isabel).</span></span> <span data-ttu-id="3f933-107">U kunt slechts één bestand per boekingsdatum en valutacode maken.</span><span class="sxs-lookup"><span data-stu-id="3f933-107">You can create only one file for each posting date and each currency code.</span></span> <span data-ttu-id="3f933-108">Wanneer u de betalingen naar een bestand exporteert, wordt er een bijbehorende notitie afgedrukt die ook naar de bank kan worden verzonden.</span><span class="sxs-lookup"><span data-stu-id="3f933-108">When you export the payments to a file, an accompanying note is printed, which can also be sent to the bank.</span></span>  

<span data-ttu-id="3f933-109">In het betalingsdagboek wordt het veld **Status** op de geëxporteerde regels ingesteld op **Geboekt**.</span><span class="sxs-lookup"><span data-stu-id="3f933-109">In the payment journal, the **Status** field on the exported lines will be set to **Posted**.</span></span>  

## <a name="to-print-a-payment-file"></a><span data-ttu-id="3f933-110">Een betalingsbestand afdrukken</span><span class="sxs-lookup"><span data-stu-id="3f933-110">To print a payment file</span></span>  

1. <span data-ttu-id="3f933-111">Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboek** in en kies vervolgens de koppeling om de pagina **EB-betalingsdagboek** te openen.</span><span class="sxs-lookup"><span data-stu-id="3f933-111">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journal**, and then choose the link to open the **EB Payment Journal** page.</span></span>  
2. <span data-ttu-id="3f933-112">Selecteer in het veld **Batchnaam** de vereiste dagboekbatch.</span><span class="sxs-lookup"><span data-stu-id="3f933-112">In the **Batch Name** field, select the required journal batch.</span></span>  
3. <span data-ttu-id="3f933-113">Selecteer in het veld **Exportprotocol** het exportprotocol.</span><span class="sxs-lookup"><span data-stu-id="3f933-113">In the **Export Protocol** field, select the export protocol.</span></span>  

    <span data-ttu-id="3f933-114">Exportprotocollen bepalen welk betalingsbestand in het betalingsdagboek wordt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="3f933-114">Export protocols control which payment file will be generated in the payment journal.</span></span> <span data-ttu-id="3f933-115">U kunt een combinatie van exportindelingen in één batch hebben, bijvoorbeeld binnenlandse, internationale en SEPA-betalingen.</span><span class="sxs-lookup"><span data-stu-id="3f933-115">You can have a mixture of export formats in a single batch, such as domestic, international, SEPA, or a combination of these.</span></span> <span data-ttu-id="3f933-116">Wanneer u de betalingsregels naar een bestand exporteert, kunt u slechts één exportindeling, of exportprotocol, gebruiken.</span><span class="sxs-lookup"><span data-stu-id="3f933-116">However, when exporting the payment lines to a file, you can use only one export format, or export protocol.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="3f933-117">Door het exportprotocol op te geven, geeft u ook het validatietype op dat wordt uitgevoerd in het betalingsdagboek.</span><span class="sxs-lookup"><span data-stu-id="3f933-117">By defining the export protocol, you also define the type of validation that will be performed in the payment journal.</span></span>
4. <span data-ttu-id="3f933-118">Voer de betalingsdagboekregelinformatie in en kies vervolgens de actie **Betalingsregels controleren**.</span><span class="sxs-lookup"><span data-stu-id="3f933-118">Enter the payment journal line information, and then choose the **Check Payment Lines** action.</span></span>

    <span data-ttu-id="3f933-119">De pagina **Logboeken voor controlefouten exporteren** bevat eventuele fouten.</span><span class="sxs-lookup"><span data-stu-id="3f933-119">The **Export Check Error Logs** page displays any errors that exist.</span></span> <span data-ttu-id="3f933-120">Als er fouten zijn, moet u deze oplossen voordat u kunt doorgaan.</span><span class="sxs-lookup"><span data-stu-id="3f933-120">If there are errors, you must fix them before you can continue.</span></span>

5. <span data-ttu-id="3f933-121">Als er geen fouten zijn, kiest u de actie **Betalingsregels exporteren**.</span><span class="sxs-lookup"><span data-stu-id="3f933-121">If there are no errors, choose the **Export Payment Lines** action.</span></span>  

    <span data-ttu-id="3f933-122">Vervolgens wordt het rapport geopend dat u in het veld **Testrapport-id** in **Betalingsdagboeksjablonen** hebt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="3f933-122">The report that you specified in the **Test Report ID** field in the **EB Payment Journal Templates** will open.</span></span>  

6. <span data-ttu-id="3f933-123">Klik op **Afdrukken**.</span><span class="sxs-lookup"><span data-stu-id="3f933-123">Choose the **Print** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3f933-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3f933-124">See Also</span></span>

[<span data-ttu-id="3f933-125">Elektronisch bankieren voor België</span><span class="sxs-lookup"><span data-stu-id="3f933-125">Belgian Electronic Banking</span></span>](belgian-electronic-banking.md)  
[<span data-ttu-id="3f933-126">Belgische elektronische betalingen</span><span class="sxs-lookup"><span data-stu-id="3f933-126">Belgian Electronic Payments</span></span>](belgian-electronic-payments.md)  
[<span data-ttu-id="3f933-127">Leveranciers voor automatische betalingsvoorstellen instellen</span><span class="sxs-lookup"><span data-stu-id="3f933-127">Set Up Vendors for Automatic Payment Suggestions</span></span>](how-to-set-up-vendors-for-automatic-payment-suggestions.md)  
[<span data-ttu-id="3f933-128">Leveranciersbetalingen voorstellen</span><span class="sxs-lookup"><span data-stu-id="3f933-128">Suggest Vendor Payments</span></span>](../../payables-how-suggest-vendor-payments.md)  
[<span data-ttu-id="3f933-129">Betalingsdagboeksjablonen en -batches maken</span><span class="sxs-lookup"><span data-stu-id="3f933-129">Create Payment Journal Templates and Batches</span></span>](how-to-create-payment-journal-templates-and-batches.md)  
[<span data-ttu-id="3f933-130">Elektronische betalingen testen</span><span class="sxs-lookup"><span data-stu-id="3f933-130">Test Electronic Payments</span></span>](how-to-test-electronic-payments.md)  
