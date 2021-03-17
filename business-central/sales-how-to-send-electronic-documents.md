---
title: Elektronische documenten verzenden
description: Leer hoe u facturen elektronisch verzendt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: d547f031d9d33c0d7cd5f8b20398fd7b6dbe0393
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5383012"
---
# <a name="send-electronic-documents"></a><span data-ttu-id="f322f-103">Elektronische documenten verzenden</span><span class="sxs-lookup"><span data-stu-id="f322f-103">Send Electronic Documents</span></span>

<span data-ttu-id="f322f-104">De algemene versie van [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt het verzenden van elektronische facturen en creditnota's in de PEPPOL-indeling, een indeling die wordt ondersteund door de grootste aanbieders van documentuitwisselingsservices.</span><span class="sxs-lookup"><span data-stu-id="f322f-104">The generic version of [!INCLUDE[prod_short](includes/prod_short.md)] supports sending electronic invoices and credit memos in the PEPPOL format, a format that the largest document exchange service providers support.</span></span> <span data-ttu-id="f322f-105">Een aanbieder van documentuitwisselingsservices verzendt elektronische documenten tussen handelspartners.</span><span class="sxs-lookup"><span data-stu-id="f322f-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="f322f-106">Om ondersteuning te bieden voor elektronische documentindelingen, gebruikt u het kader voor gegevensuitwisseling.</span><span class="sxs-lookup"><span data-stu-id="f322f-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="f322f-107">In de algemene versie van [!INCLUDE[prod_short](includes/prod_short.md)] is een service voor documentuitwisseling vooraf geconfigureerd zodat u deze kunt instellen voor uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="f322f-107">In the generic version of [!INCLUDE[prod_short](includes/prod_short.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="f322f-108">Zie [Een service voor documentuitwisseling instellen](across-how-to-set-up-a-document-exchange-service.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f322f-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span> <span data-ttu-id="f322f-109">In sommige gevallen moet u echter een app installeren.</span><span class="sxs-lookup"><span data-stu-id="f322f-109">However, in some cases, you must install an app.</span></span> <span data-ttu-id="f322f-110">Zie voor meer informatie [Veelgestelde vragen over elektronische facturering](faq-electronic-invoicing.yml).</span><span class="sxs-lookup"><span data-stu-id="f322f-110">For more information, see [Electronic Invoicing FAQ](faq-electronic-invoicing.yml).</span></span>  

 <span data-ttu-id="f322f-111">Als u een verkoopfactuur als elektronisch PEPPOL-document wilt verzenden, selecteert u de optie **Elektronisch document** in het dialoogvenster **Boeken en verzenden**.</span><span class="sxs-lookup"><span data-stu-id="f322f-111">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box.</span></span> <span data-ttu-id="f322f-112">U kunt ook het standaardprofiel voor documentverzending van de klant instellen vanuit dat dialoogvenster.</span><span class="sxs-lookup"><span data-stu-id="f322f-112">You can also set up the customer's default document sending profile from that dialog box.</span></span> <span data-ttu-id="f322f-113">Eerst moet u diverse stamgegevens instellen, zoals bedrijfsgegevens, klanten, artikelen en eenheden.</span><span class="sxs-lookup"><span data-stu-id="f322f-113">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="f322f-114">Deze worden gebruikt om de zakelijke partners en artikelen te identificeren wanneer gegevens worden geconverteerd in velden in [Verzending en ontvangst van elektronische documenten instellen](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="f322f-114">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="f322f-115">Een elektronische verkoopfactuur verzenden</span><span class="sxs-lookup"><span data-stu-id="f322f-115">To send an electronic sales invoice</span></span>

1. <span data-ttu-id="f322f-116">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopfacturen** in en kies de gerelateerde koppeling</span><span class="sxs-lookup"><span data-stu-id="f322f-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2. <span data-ttu-id="f322f-117">Maak een nieuwe verkoopfactuur.</span><span class="sxs-lookup"><span data-stu-id="f322f-117">Create a new sales invoice.</span></span>  

3. <span data-ttu-id="f322f-118">Wanneer de verkoopfactuur klaar is voor facturering, kiest u de actie **Boeken en verzenden**.</span><span class="sxs-lookup"><span data-stu-id="f322f-118">When the sales invoice is ready to be invoiced, choose the **Post and Send** action.</span></span>  

     <span data-ttu-id="f322f-119">Als het standaardverzendprofiel van de klant **Elektronisch document** is, wordt het weergegeven in het dialoogvenster **Boeken en bevestiging verzenden**.</span><span class="sxs-lookup"><span data-stu-id="f322f-119">If the customer's default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box.</span></span> <span data-ttu-id="f322f-120">Op deze manier hoeft u alleen maar de knop **Ja** te kiezen om de factuur elektronisch in de geselecteerde indeling te boeken en te verzenden.</span><span class="sxs-lookup"><span data-stu-id="f322f-120">This way, you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4. <span data-ttu-id="f322f-121">In het dialoogvenster **Boeken en bevestiging verzenden** kiest u de Knop AssistEdit rechts van het veld **Document verzenden naar**.</span><span class="sxs-lookup"><span data-stu-id="f322f-121">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5. <span data-ttu-id="f322f-122">Kies in het dialoogvenster **Document verzenden naar** in het veld **Elektronisch document** de optie **Via service voor documentuitwisseling**.</span><span class="sxs-lookup"><span data-stu-id="f322f-122">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6. <span data-ttu-id="f322f-123">Kies in het veld **Indeling** de optie **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="f322f-123">In the **Format** field, choose **PEPPOL**.</span></span>  

7. <span data-ttu-id="f322f-124">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="f322f-124">Choose the **OK** button.</span></span> <span data-ttu-id="f322f-125">Het dialoogvenster **Boeken en bevestiging verzenden** verschijnt.</span><span class="sxs-lookup"><span data-stu-id="f322f-125">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="f322f-126">**Elektronisch document (PEPPOL)** is toegevoegd aan het veld **Document verzenden naar**.</span><span class="sxs-lookup"><span data-stu-id="f322f-126">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8. <span data-ttu-id="f322f-127">Kies de knop **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f322f-127">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="f322f-128">De verkoopfactuur wordt geboekt en naar de klant verzonden in de PEPPOL-indeling.</span><span class="sxs-lookup"><span data-stu-id="f322f-128">The sales invoice is posted and sent to the customer in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f322f-129">U kunt ook een geboekte verkoopfactuur als een elektronisch document verzenden.</span><span class="sxs-lookup"><span data-stu-id="f322f-129">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="f322f-130">De procedure is hetzelfde als beschreven in dit onderwerp voor niet-geboekte verkoopdocumenten.</span><span class="sxs-lookup"><span data-stu-id="f322f-130">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="f322f-131">Kies op de pagina **Geboekte verkoopfactuur** de actie **Activiteitenlogboek** om de status van en elektronische document weer te geven.</span><span class="sxs-lookup"><span data-stu-id="f322f-131">On the **Posted Sales Invoice** page, choose the **Activity Log** action to view the status of the electronic document.</span></span>  

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="f322f-132">Zie Gerelateerde training op [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="f322f-132">See Related Training at [Microsoft Learn](/learn/modules/electronic-documents-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="f322f-133">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f322f-133">See Also</span></span>

[<span data-ttu-id="f322f-134">Verkopen factureren</span><span class="sxs-lookup"><span data-stu-id="f322f-134">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="f322f-135">Verzendprofielen van documenten instellen</span><span class="sxs-lookup"><span data-stu-id="f322f-135">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="f322f-136">Verzending en ontvangst van elektronische documenten instellen</span><span class="sxs-lookup"><span data-stu-id="f322f-136">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="f322f-137">Een service voor documentuitwisseling instellen</span><span class="sxs-lookup"><span data-stu-id="f322f-137">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="f322f-138">Definities voor gegevensuitwisseling instellen</span><span class="sxs-lookup"><span data-stu-id="f322f-138">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="f322f-139">Gegevens elektronisch uitwisselen</span><span class="sxs-lookup"><span data-stu-id="f322f-139">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="f322f-140">Veelgestelde vragen over elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="f322f-140">Electronic Invoicing FAQ</span></span>](faq-electronic-invoicing.yml)  
[<span data-ttu-id="f322f-141">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="f322f-141">General Business Functionality</span></span>](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]