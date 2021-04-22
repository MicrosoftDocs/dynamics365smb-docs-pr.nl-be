---
title: De extensie Betalingen en afstemmingen (DK) gebruiken | Microsoft Docs
description: Deze extensie maakt het eenvoudig bestanden te exporteren die vooraf zijn ingedeeld om te voldoen aan de vereisten van de bank betreffende elektronische verzendingen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: fdd8fced06d8efd5ab6959267bfc0171c4decdd2
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5785097"
---
# <a name="the-payments-and-reconciliations-dk-extension"></a><span data-ttu-id="5cb6f-103">De extensie Betalingen en afstemmingen (DK)</span><span class="sxs-lookup"><span data-stu-id="5cb6f-103">The Payments and Reconciliations (DK) Extension</span></span>

<span data-ttu-id="5cb6f-104">Snelle, foutloze betalingen doen door bestanden te exporteren die specifiek voor uitwisselingen met uw leverancier of bank zijn ingedeeld.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-104">Make fast, error-free payments by exporting files that are formatted specifically for exchanges with your vendor or bank.</span></span> <span data-ttu-id="5cb6f-105">Deze bestanden versnellen de betalings- en afstemmingprocessen, en voorkomen fouten die kunnen optreden als u handmatig de gegevens op een bankwebsite invoert.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-105">These files speed up the payment and reconciliation processes, and eliminate errors that can happen when you manually enter the information on a bank website.</span></span>  

<span data-ttu-id="5cb6f-106">De extensie ondersteunt bestandsindelingen voor diverse Deense banken.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-106">This extension supports file formats for several Danish banks.</span></span> <span data-ttu-id="5cb6f-107">Wanneer u betalingsgegevens naar een bestand exporteert, verpakt de extensie de gegevens in de indeling die door de bank wordt vereist.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-107">When you export payment information to a file, the extension packages the data into the format that your bank requires.</span></span> <span data-ttu-id="5cb6f-108">Deze indelingen zijn onder andere Bankdata-V3, BEC, SDC en FIK, die door allerlei banken worden gebruikt, en een aantal bankspecifiekere indelingen, zoals Danske Bank en Nordea.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-108">For example, the formats include Bankdata-V3, BEC, SDC, and FIK, which many different banks use, and some that are more specialized for certain banks, for example, Danske Bank and Nordea.</span></span> <span data-ttu-id="5cb6f-109">De extensie bevat ook sommige indelingen voor het importeren van en de reconciliatie van bankafschriften.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-109">The extension also includes some formats for importing and reconciling bank statements.</span></span>  

> [!Note]
> <span data-ttu-id="5cb6f-110">Als u de extensie wilt gebruiken, moet u weten welke indeling voor uw bank of leverancier is vereist.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-110">To use the extension, you must know the format that your bank or vendor requires.</span></span> <span data-ttu-id="5cb6f-111">Sommige banken of leveranciers verstrekken deze informatie op hun website, maar het kan ook nodig zijn om contact op te nemen met hun klantenservice om deze informatie op te vragen.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-111">Some banks or vendors provide this information on their websites; however, you might need to contact their customer service to get the information.</span></span>  

## <a name="supported-bank-formats"></a><span data-ttu-id="5cb6f-112">Indelingen voor banken die worden ondersteund</span><span class="sxs-lookup"><span data-stu-id="5cb6f-112">Supported Bank Formats</span></span>
<span data-ttu-id="5cb6f-113">De extensie kan de volgende activiteiten voor betalingbestanden vereffenen:</span><span class="sxs-lookup"><span data-stu-id="5cb6f-113">This extension can apply the following file formats for payment files:</span></span>  

* <span data-ttu-id="5cb6f-114">Bankdata-V3</span><span class="sxs-lookup"><span data-stu-id="5cb6f-114">BANKDATA-V3</span></span>  
* <span data-ttu-id="5cb6f-115">BEC-INDLAND</span><span class="sxs-lookup"><span data-stu-id="5cb6f-115">BEC-INDLAND</span></span>  
* <span data-ttu-id="5cb6f-116">BEC-CSV</span><span class="sxs-lookup"><span data-stu-id="5cb6f-116">BEC-CSV</span></span>  
* <span data-ttu-id="5cb6f-117">DANSKEBANK-CMKV</span><span class="sxs-lookup"><span data-stu-id="5cb6f-117">DANSKEBANK-CMKV</span></span>  
* <span data-ttu-id="5cb6f-118">DANSKEBANK-CMKXKSX</span><span class="sxs-lookup"><span data-stu-id="5cb6f-118">DANSKEBANK-CMKXKSX</span></span>  
* <span data-ttu-id="5cb6f-119">DANSKEBANK</span><span class="sxs-lookup"><span data-stu-id="5cb6f-119">DANSKEBANK</span></span>  
* <span data-ttu-id="5cb6f-120">FIK71</span><span class="sxs-lookup"><span data-stu-id="5cb6f-120">FIK71</span></span>  
* <span data-ttu-id="5cb6f-121">NORDEA-ERHVERV-CSV</span><span class="sxs-lookup"><span data-stu-id="5cb6f-121">NORDEA-ERHVERV-CSV</span></span>  
* <span data-ttu-id="5cb6f-122">NORDEA</span><span class="sxs-lookup"><span data-stu-id="5cb6f-122">NORDEA</span></span>  
* <span data-ttu-id="5cb6f-123">NORDEA-UNITEL-V3</span><span class="sxs-lookup"><span data-stu-id="5cb6f-123">NORDEA-UNITEL-V3</span></span>  
* <span data-ttu-id="5cb6f-124">SDC</span><span class="sxs-lookup"><span data-stu-id="5cb6f-124">SDC</span></span>  
* <span data-ttu-id="5cb6f-125">SDC-CSV</span><span class="sxs-lookup"><span data-stu-id="5cb6f-125">SDC-CSV</span></span>  

## <a name="to-set-up-the-extension"></a><span data-ttu-id="5cb6f-126">De extensie instellen</span><span class="sxs-lookup"><span data-stu-id="5cb6f-126">To set up the extension</span></span>

<span data-ttu-id="5cb6f-127">Er zijn een aantal stappen vereist als u aan de slag wilt.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-127">There are a few steps to get started.</span></span>  

* <span data-ttu-id="5cb6f-128">Sta het exporteren van betalingsgegevens toe.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-128">Allow payment data exports.</span></span> <span data-ttu-id="5cb6f-129">Ter bescherming van uw gegevens, is dit niet direct beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-129">To help protect your data, this is not readily available.</span></span>  
* <span data-ttu-id="5cb6f-130">Stel inkoop en crediteuren in, zodat externe documentnummers op facturen niet zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-130">Set up purchase and payables so that you do not require external document numbers on invoices.</span></span> <span data-ttu-id="5cb6f-131">Indien nodig kunt u het referentienummer gebruiken om naar een bepaalde factuur te verwijzen.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-131">If needed, you can use the reference number to refer to a specific invoice.</span></span>  
* <span data-ttu-id="5cb6f-132">Geef de betalingswijze voor elke leverancier op.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-132">Specify the payment method for each vendor.</span></span> <span data-ttu-id="5cb6f-133">Betalingswijzen bepalen hoe u facturen van de leverancier betaalt.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-133">Payment methods define how you pay invoices from the vendor.</span></span> <span data-ttu-id="5cb6f-134">Bijvoorbeeld bank, contant, cheque of rekening.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-134">For example, Bank, Cash, Check, or Account.</span></span>  
* <span data-ttu-id="5cb6f-135">Geef het type indeling op dat voor elk van uw bankrekeningen moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-135">Specify the type of format to use for each of your bank accounts.</span></span> <span data-ttu-id="5cb6f-136">Voorbeelden zijn NORDEA, DANSKEBANK, SDC enzovoort.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-136">For example, NORDEA, DANSKEBANK, SDC, and so on.</span></span>  

<span data-ttu-id="5cb6f-137">Daarnaast moet u leveranciers toewijzen aan een binnenlandse **bedrijfsboekingsgroep** en een **leveranciersboekingsgroep**.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-137">Additionally, you must assign vendors to a domestic **Gen. Bus. Posting Group** and a **Vendor Posting Group**.</span></span> <span data-ttu-id="5cb6f-138">De instelling Land/regio voor de leverancier moet Denemarken (DK) zijn.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-138">The Country/Region setting for the vendor must be Denmark (DK).</span></span> <span data-ttu-id="5cb6f-139">Zie [Boekingsgroepen instellen](finance-posting-groups.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-139">For more information, see [Setting Up Posting Groups](finance-posting-groups.md).</span></span>  

### <a name="to-allow-prod_short-to-export-payment-data"></a><span data-ttu-id="5cb6f-140">[!INCLUDE[prod_short](includes/prod_short.md)] toestaan betalingsgegevens te exproteren</span><span class="sxs-lookup"><span data-stu-id="5cb6f-140">To allow [!INCLUDE[prod_short](includes/prod_short.md)] to export payment data</span></span>

1. <span data-ttu-id="5cb6f-141">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboek** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-141">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5cb6f-142">Kies op de pagina **Betalingsdagboek bewerken** de batch **Bank**.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-142">On the **Edit Payment Journal** page, choose the **Bank** batch.</span></span>  
3. <span data-ttu-id="5cb6f-143">Schakel het selectievakje **Exporteren betaling toestaan** in.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-143">Choose the **Allow Payment Export** check box.</span></span>  

### <a name="to-specify-a-payment-method-for-a-vendor"></a><span data-ttu-id="5cb6f-144">Een betalingswijze voor een leverancier opgeven</span><span class="sxs-lookup"><span data-stu-id="5cb6f-144">To specify a payment method for a vendor</span></span>

<span data-ttu-id="5cb6f-145">De volgende tabel bevat de combinaties van de betalingswijzen FIK en GIRO die door [!INCLUDE[prod_short](includes/prod_short.md)] worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-145">The following table shows the combinations of FIK and GIRO payment methods that [!INCLUDE[prod_short](includes/prod_short.md)] supports.</span></span>

|<span data-ttu-id="5cb6f-146">Combinatie</span><span class="sxs-lookup"><span data-stu-id="5cb6f-146">Combination</span></span>|<span data-ttu-id="5cb6f-147">Soort 01</span><span class="sxs-lookup"><span data-stu-id="5cb6f-147">Type 01</span></span> | <span data-ttu-id="5cb6f-148">Soort 04</span><span class="sxs-lookup"><span data-stu-id="5cb6f-148">Type 04</span></span> | <span data-ttu-id="5cb6f-149">Soort 71</span><span class="sxs-lookup"><span data-stu-id="5cb6f-149">Type 71</span></span> | <span data-ttu-id="5cb6f-150">Soort 73</span><span class="sxs-lookup"><span data-stu-id="5cb6f-150">Type 73</span></span> |
|----|--------|---------|---------|---------|
|<span data-ttu-id="5cb6f-151">Girorekeningnr of FIK-crediteurennr?</span><span class="sxs-lookup"><span data-stu-id="5cb6f-151">Giro Account No. or FIK Creditor No.?</span></span> | <span data-ttu-id="5cb6f-152">Girorekeningnr</span><span class="sxs-lookup"><span data-stu-id="5cb6f-152">Giro Account No.</span></span> | <span data-ttu-id="5cb6f-153">Girorekeningnr</span><span class="sxs-lookup"><span data-stu-id="5cb6f-153">Giro Account No.</span></span> | <span data-ttu-id="5cb6f-154">FIK-crediteurennummer</span><span class="sxs-lookup"><span data-stu-id="5cb6f-154">FIK Creditor No.</span></span> | <span data-ttu-id="5cb6f-155">FIK-crediteurennummer</span><span class="sxs-lookup"><span data-stu-id="5cb6f-155">FIK Creditor No.</span></span>|
|<span data-ttu-id="5cb6f-156">Bericht aan ontvanger toestaan?</span><span class="sxs-lookup"><span data-stu-id="5cb6f-156">Allows Message to Recipient?</span></span> | <span data-ttu-id="5cb6f-157">Ja</span><span class="sxs-lookup"><span data-stu-id="5cb6f-157">Yes</span></span> |<span data-ttu-id="5cb6f-158">Nee</span><span class="sxs-lookup"><span data-stu-id="5cb6f-158">No</span></span> |<span data-ttu-id="5cb6f-159">Nee</span><span class="sxs-lookup"><span data-stu-id="5cb6f-159">No</span></span> | <span data-ttu-id="5cb6f-160">Ja</span><span class="sxs-lookup"><span data-stu-id="5cb6f-160">Yes</span></span> |
|<span data-ttu-id="5cb6f-161">Bevat betalingreferentienummer?</span><span class="sxs-lookup"><span data-stu-id="5cb6f-161">Contains Payment Reference number?</span></span> | <span data-ttu-id="5cb6f-162">Nr.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-162">No</span></span> | <span data-ttu-id="5cb6f-163">Ja, 16 cijfers.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-163">Yes, 16 digits.</span></span> | <span data-ttu-id="5cb6f-164">Ja, 15 cijfers.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-164">Yes, 15 digits.</span></span> | <span data-ttu-id="5cb6f-165">Nee</span><span class="sxs-lookup"><span data-stu-id="5cb6f-165">No</span></span>|

1. <span data-ttu-id="5cb6f-166">Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciers** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-166">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5cb6f-167">Open de kaart, vouw het tabblad **Betalingen** uit, kies in het veld **Betalingswijze** de betalingswijze.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-167">Open the card, expand the **Payments** tab, in the **Payment Method** field choose the payment method.</span></span>  
3. <span data-ttu-id="5cb6f-168">Afhankelijk van uw selectie moet u andere velden invullen.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-168">Depending on your selection, you must complete other fields.</span></span> <span data-ttu-id="5cb6f-169">Zie de bovenstaande tabel voor een omschrijving van de combinaties.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-169">See the table above for a description of the combinations.</span></span>  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a><span data-ttu-id="5cb6f-170">De indeling opgeven die voor een bankrekening moet worden gebruikt</span><span class="sxs-lookup"><span data-stu-id="5cb6f-170">To specify the format to use for a bank account</span></span>

1. <span data-ttu-id="5cb6f-171">Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankrekeningen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-171">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5cb6f-172">Open de kaart voor de bankrekening.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-172">Open the card for the bank account.</span></span>  
3. <span data-ttu-id="5cb6f-173">In het veld **Exportindeling betaling** kiest u de indeling voor uw exportbestand.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-173">In the **Payment Export Format** field, choose the format for your export file.</span></span>  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a><span data-ttu-id="5cb6f-174">De betalingsgevens FIK of Giro voor facturen van leveranciers kiezen</span><span class="sxs-lookup"><span data-stu-id="5cb6f-174">Choosing the FIK or Giro payment information for vendor invoices</span></span>

1. <span data-ttu-id="5cb6f-175">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-175">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="5cb6f-176">Kies de leverancier.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-176">Choose the vendor.</span></span> <span data-ttu-id="5cb6f-177">Dit moet een Deense leverancier zijn met een adres in Denemarken.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-177">Remember, this must be a Danish vendor with an address in Denmark.</span></span>
3. <span data-ttu-id="5cb6f-178">Maak een factuur.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-178">Create an invoice.</span></span> <span data-ttu-id="5cb6f-179">De velden **Betalingswijze** en **Leveranciersnummer** worden ingevuld op basis van instellingen op de leverancierskaart.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-179">The **Payment Method** and **Vendor Number** fields are filled in based on settings on the Vendor card.</span></span> <span data-ttu-id="5cb6f-180">U kunt desgewenst wijzigingen aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-180">You can change them if you want.</span></span>
4. <span data-ttu-id="5cb6f-181">In het veld **Betalingsreferentie** voert u het nummer van 15 cijfers van de factuur van de leverancier in.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-181">In the **Payment Reference** field, enter the 15-digit number from the vendor invoice.</span></span>  

    > [!Tip]
    > <span data-ttu-id="5cb6f-182">U hoeft slechts de laatste 11 cijfers van het nummer toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-182">You only have to add the last 11 digits of the number.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="5cb6f-183">voegt vier nullen aan het begin van het nummer toe.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-183">will add four zeros to the beginning of the number.</span></span>  

5. <span data-ttu-id="5cb6f-184">Boek de factuur.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-184">Post the invoice.</span></span>

## <a name="to-use-the-extension-to-export-payment-data"></a><span data-ttu-id="5cb6f-185">De extensie gebruiken om betalingsgegevens te exporteren</span><span class="sxs-lookup"><span data-stu-id="5cb6f-185">To use the extension to export payment data</span></span>

1. <span data-ttu-id="5cb6f-186">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboeken** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="5cb6f-187">Kies de actie **Leveranciersbetalingsdagboeken voorstellen**.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-187">Choose the **Suggest Vendor Payment Journals** action.</span></span>  

    > [!Tip]
    > <span data-ttu-id="5cb6f-188">Als u alleen bepaalde betalingen wilt exporteren, gebruikt u de opties om de gegevens te filteren.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-188">If you want to export only specific payments, use the options for filtering the data.</span></span>  

3. <span data-ttu-id="5cb6f-189">Indien nodig kunt u filters toevoegen als u alleen bepaalde betalingen wilt exporteren.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-189">If needed, you can add filters to export only specific payments.</span></span>  
4. <span data-ttu-id="5cb6f-190">Selecteer **Elektronische betaling** in het veld **Betalingssoort**.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-190">In the **Bank Payment Type** field, choose **Electronic Payment**.</span></span>  
5. <span data-ttu-id="5cb6f-191">Kies de actie **Exporteren**.</span><span class="sxs-lookup"><span data-stu-id="5cb6f-191">Choose the **Export** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5cb6f-192">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5cb6f-192">See also</span></span>

<span data-ttu-id="5cb6f-193">[Business Central aanpassen voor [!INCLUDE[prod_short](includes/prod_short.md)] met extensies](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="5cb6f-193">[Customizing Business Central for [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="5cb6f-194">Betalingen verzamelen via automatische incasso van SEPA</span><span class="sxs-lookup"><span data-stu-id="5cb6f-194">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="5cb6f-195">Werken met diversendagboeken</span><span class="sxs-lookup"><span data-stu-id="5cb6f-195">Working with General Journals</span></span>](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]