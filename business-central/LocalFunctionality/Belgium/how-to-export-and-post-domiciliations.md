---
title: Domiciliëringen exporteren en boeken
description: U kunt domiciliëringen naar uw bank verzenden door de gegevens naar een bestand te exporteren. Wanneer u naar een bestand exporteert, kunt u ervoor kiezen de regels automatisch naar het grootboek te boeken.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0c461f311366139ca6b5d4f64a77b97ec64b946a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773276"
---
# <a name="export-and-post-domiciliations"></a><span data-ttu-id="6aa9d-104">Domiciliëringen exporteren en boeken</span><span class="sxs-lookup"><span data-stu-id="6aa9d-104">Export and Post Domiciliations</span></span>
<span data-ttu-id="6aa9d-105">U kunt domiciliëringen naar uw bank verzenden door de gegevens naar een bestand te exporteren.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-105">You can submit domiciliations to your bank by exporting the data to a file.</span></span> <span data-ttu-id="6aa9d-106">Wanneer u naar een bestand exporteert, kunt u ervoor kiezen de regels automatisch naar het grootboek te boeken.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-106">When you export to a file, you can choose to automatically post the lines to the general ledger.</span></span>  

<span data-ttu-id="6aa9d-107">Afhankelijk van de instelling van het veld **Exportindeling van incasso van SEPA** op de pagina **Bankrekeningkaart**, wordt met de actie **Bestandsdomiciliëringen** een van deze aanvraagpagina's geopend:</span><span class="sxs-lookup"><span data-stu-id="6aa9d-107">Depending on setup of the **SEPA Direct Debit Exp. Format** field on the **Bank Account Card** page, the **File Domiciliations** action opens either of these request pages:</span></span>  

- <span data-ttu-id="6aa9d-108">De pagina **Dagboekregels maken**, voor de indeling SEPA Incasso.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-108">**Create Gen. Jnl. Lines** page – for the SEPA Direct Debit format.</span></span>  
- <span data-ttu-id="6aa9d-109">De pagina **Bestandsdomiciliëringen**, voor binnenlandse indelingen.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-109">**File Domiciliations** page – for domestic formats.</span></span>  

## <a name="to-export-and-post-domiciliations-in-sepa-format"></a><span data-ttu-id="6aa9d-110">Domiciliëringen exporteren en boeken in SEPA-indeling</span><span class="sxs-lookup"><span data-stu-id="6aa9d-110">To export and post domiciliations in SEPA format</span></span>  

1.  <span data-ttu-id="6aa9d-111">Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Domiciliëringsdagboeken** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-111">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Domiciliation Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6aa9d-112">Selecteer in het veld **Batchnaam** de vereiste dagboekbatch en kies vervolgens de actie **Bestandsdomiciliëringen**.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-112">In the **Batch Name** field, select the required journal batch, and then choose the **File Domiciliations** action.</span></span>  
3.  <span data-ttu-id="6aa9d-113">Vul op de pagina **Dagboekregels maken** de velden in zoals wordt beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-113">On the **Create Gen. Jnl. Lines** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="6aa9d-114">Veld</span><span class="sxs-lookup"><span data-stu-id="6aa9d-114">Field</span></span>|<span data-ttu-id="6aa9d-115">Description</span><span class="sxs-lookup"><span data-stu-id="6aa9d-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="6aa9d-116">**Dagboeksjabloon**</span><span class="sxs-lookup"><span data-stu-id="6aa9d-116">**Journal Template Name**</span></span>|<span data-ttu-id="6aa9d-117">Selecteer de dagboeksjabloon waaruit de domiciliëringen worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-117">Select the general journal template that the domiciliations will be posted from.</span></span>|  
    |<span data-ttu-id="6aa9d-118">**Dagboekbatch**</span><span class="sxs-lookup"><span data-stu-id="6aa9d-118">**Journal Batch**</span></span>|<span data-ttu-id="6aa9d-119">Selecteer de algemene dagboekbatch waaruit de dagboekregels worden overgebracht.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-119">Select the general journal batch that the journal lines will be transferred from.</span></span>|  
    |<span data-ttu-id="6aa9d-120">**Dagboekregels boeken**</span><span class="sxs-lookup"><span data-stu-id="6aa9d-120">**Post General Journal Lines**</span></span>|<span data-ttu-id="6aa9d-121">Selecteer deze optie om naar het grootboek te boeken.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-121">Select to post to the general ledger.</span></span>|  

4.  <span data-ttu-id="6aa9d-122">Klik op **OK** om het bestand te exporteren.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-122">Choose the **OK** button to export the file.</span></span>  
5.  <span data-ttu-id="6aa9d-123">Kies de locatie van waar u het bestand naar uw bank wilt uploaden en kies **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-123">Choose an appropriate location from where you upload the file to your bank, and then choose **Save**.</span></span>  
6.  <span data-ttu-id="6aa9d-124">Kies de knop **Ja** om de domiciliëringsdagboekregels automatisch te boeken.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-124">Choose the **Yes** button to automatically post the domiciliation journal lines.</span></span>  

    <span data-ttu-id="6aa9d-125">Als u het selectievakje **Dagboekregels boeken** niet hebt ingeschakeld, moet u de domiciliëringen handmatig in het dagboek boeken.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-125">If you did not select the **Post General Journal Lines** check box, you will have to post the domiciliations manually in the general journal.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="6aa9d-126">Nadat u domiciliëringen in het dagboek hebt geboekt, verwijdert u de geboekte domiciliëringen op de pagina **Domiciliëringsdagboek**.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-126">After you have posted domiciliations in the general journal, delete the posted domiciliations on the **Domiciliation Journal** page.</span></span> <span data-ttu-id="6aa9d-127">Hiervoor selecteert u alle regels met de status **Geboekt** en kiest u de knop **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-127">To do this, select all lines with status **Posted**, and then choose the **Delete** button.</span></span>  

## <a name="to-export-and-post-domiciliations-in-isabel-format"></a><span data-ttu-id="6aa9d-128">Domiciliëringen exporteren en boeken in Isabel-indeling</span><span class="sxs-lookup"><span data-stu-id="6aa9d-128">To export and post domiciliations in Isabel format</span></span>  

1.  <span data-ttu-id="6aa9d-129">Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Domiciliëringsdagboeken** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-129">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Domiciliation Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="6aa9d-130">Selecteer in het veld **Batchnaam** de vereiste dagboekbatch en kies vervolgens de actie **Bestandsdomiciliëringen**.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-130">In the **Batch Name** field, select the required journal batch, and then choose the **File Domiciliations** action.</span></span>  
3.  <span data-ttu-id="6aa9d-131">Vul op de pagina **Bestandsdomiciliëringen** de velden in zoals wordt beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-131">On the **File Domiciliations** page, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="6aa9d-132">Veld</span><span class="sxs-lookup"><span data-stu-id="6aa9d-132">Field</span></span>|<span data-ttu-id="6aa9d-133">Description</span><span class="sxs-lookup"><span data-stu-id="6aa9d-133">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="6aa9d-134">**Dagboeksjabloon**</span><span class="sxs-lookup"><span data-stu-id="6aa9d-134">**Journal Template Name**</span></span>|<span data-ttu-id="6aa9d-135">Selecteer de dagboeksjabloon waaruit de domiciliëringen worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-135">Select the general journal template that the domiciliations will be posted from.</span></span>|  
    |<span data-ttu-id="6aa9d-136">**Dagboekbatch**</span><span class="sxs-lookup"><span data-stu-id="6aa9d-136">**Journal Batch**</span></span>|<span data-ttu-id="6aa9d-137">Selecteer de algemene dagboekbatch waaruit de dagboekregels worden overgebracht.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-137">Select the general journal batch that the journal lines will be transferred from.</span></span>|  
    |<span data-ttu-id="6aa9d-138">**Dagboekregels boeken**</span><span class="sxs-lookup"><span data-stu-id="6aa9d-138">**Post General Journal Lines**</span></span>|<span data-ttu-id="6aa9d-139">Selecteer deze optie om naar het grootboek te boeken.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-139">Select to post to the general ledger.</span></span>|  
    |<span data-ttu-id="6aa9d-140">**Spildatum**</span><span class="sxs-lookup"><span data-stu-id="6aa9d-140">**Pivot Date**</span></span>|<span data-ttu-id="6aa9d-141">Voer een spildatum in als u op de domiciliëringsregels een datum wilt hebben die afwijkt van de boekingsdatum.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-141">Enter a pivot date if you want a date that differs from the posting date on the domiciliation lines.</span></span> <span data-ttu-id="6aa9d-142">De ingevoerde datum overschrijft de boekingsdatum op de geselecteerde dagboekregels.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-142">The date entered will overwrite the posting date on the selected journal lines.</span></span>|  
    |<span data-ttu-id="6aa9d-143">**Inschrijvingsnr.**</span><span class="sxs-lookup"><span data-stu-id="6aa9d-143">**Inscription No.**</span></span>|<span data-ttu-id="6aa9d-144">Voer het inschrijvingsnummer in dat zich op de schijf voor intracommunautaire aangiften bevindt.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-144">Enter the inscription number that is on the intra-community declaration disk.</span></span> <span data-ttu-id="6aa9d-145">Dit nummer is opgenomen in het bestand en de begeleidende notitie.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-145">The number is included in the file and on the accompanying note.</span></span>|  
    |<span data-ttu-id="6aa9d-146">**Bestandsnaam**</span><span class="sxs-lookup"><span data-stu-id="6aa9d-146">**File Name**</span></span>|<span data-ttu-id="6aa9d-147">Geef de naam op van het exportbestand dat u maakt.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-147">Enter the name of the export file that you are creating.</span></span>|  

4.  <span data-ttu-id="6aa9d-148">Kies de knop **Afdrukken** om de domiciliëringen te exporteren en de begeleidende notitie af te drukken. Kies de knop **Voorbeeld** om deze op het scherm weer te geven.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-148">Choose the **Print** button to export the domiciliations and print the accompanying note, or choose the **Preview** button to view it on the screen.</span></span> <span data-ttu-id="6aa9d-149">Als u het bestand nu niet wilt exporteren, kiest u de knop **Annuleren** om het venster te sluiten.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-149">If you do not want to export the file now, choose the **Cancel** button.</span></span>  
5.  <span data-ttu-id="6aa9d-150">Kies de knop **OK** om het rapport naar de printer te verzenden.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-150">Choose the **OK** button to send the report to the printer.</span></span>  
6.  <span data-ttu-id="6aa9d-151">Kies de knop **Ja** om de domiciliëringsdagboekregels automatisch te boeken.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-151">Choose the **Yes** button to automatically post the domiciliation journal lines.</span></span>  

    <span data-ttu-id="6aa9d-152">Als u het selectievakje **Dagboekregels boeken** niet hebt ingeschakeld, moet u de domiciliëringen handmatig in het dagboek boeken.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-152">If you did not select the **Post General Journal Lines** check box, you will have to post the domiciliations manually in the general journal.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="6aa9d-153">Nadat u domiciliëringen in het dagboek hebt geboekt, verwijdert u de geboekte domiciliëringen op de pagina **Domiciliëringsdagboek**.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-153">After you have posted domiciliations in the general journal, delete the posted domiciliations on the **Domiciliation Journal** page.</span></span> <span data-ttu-id="6aa9d-154">Hiervoor selecteert u alle regels met de status **Geboekt** en kiest u de knop **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="6aa9d-154">To do this, select all lines with status **Posted**, and then choose the **Delete** button.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6aa9d-155">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6aa9d-155">See Also</span></span>  
 <span data-ttu-id="6aa9d-156">[Incasso via domiciliëring](direct-debit-using-domiciliation.md) </span><span class="sxs-lookup"><span data-stu-id="6aa9d-156">[Direct Debit Using Domiciliation](direct-debit-using-domiciliation.md) </span></span>  
 <span data-ttu-id="6aa9d-157">[Domiciliëringen instellen](how-to-set-up-domiciliations.md) </span><span class="sxs-lookup"><span data-stu-id="6aa9d-157">[Set Up Domiciliations](how-to-set-up-domiciliations.md) </span></span>  
 <span data-ttu-id="6aa9d-158">[Domiciliëringsvoorstellen genereren](how-to-generate-domiciliation-suggestions.md) </span><span class="sxs-lookup"><span data-stu-id="6aa9d-158">[Generate Domiciliation Suggestions](how-to-generate-domiciliation-suggestions.md) </span></span>  
 <span data-ttu-id="6aa9d-159">[Domiciliëringen testen](how-to-test-domiciliations.md) </span><span class="sxs-lookup"><span data-stu-id="6aa9d-159">[Test Domiciliations](how-to-test-domiciliations.md) </span></span>  
 [<span data-ttu-id="6aa9d-160">Domiciliëringsregels bewerken en verwijderen</span><span class="sxs-lookup"><span data-stu-id="6aa9d-160">Edit and Delete Domiciliation Lines</span></span>](how-to-edit-and-delete-domiciliation-lines.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]