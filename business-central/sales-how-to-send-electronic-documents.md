---
title: Elektronische documenten verzenden | Microsoft Docs
description: Leer hoe u facturen elektronisch verzendt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 507fd934ee30d2bcacbb298d0ab18fa351621922
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="send-electronic-documents"></a><span data-ttu-id="73638-103">Elektronische documenten verzenden</span><span class="sxs-lookup"><span data-stu-id="73638-103">Send Electronic Documents</span></span>
<span data-ttu-id="73638-104">De algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] ondersteunt het verzenden van elektronische facturen en creditnota's in de PEPPOL-indeling, die wordt ondersteund door de grootste aanbieders van documentuitwisselingsservices.</span><span class="sxs-lookup"><span data-stu-id="73638-104">The generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)] supports sending electronic invoices and credit memos in the PEPPOL format, which is supported by the largest document exchange service providers.</span></span> <span data-ttu-id="73638-105">Een aanbieder van documentuitwisselingsservices verzendt elektronische documenten tussen handelspartners.</span><span class="sxs-lookup"><span data-stu-id="73638-105">A document exchange service provider dispatches electronic documents between trading partners.</span></span> <span data-ttu-id="73638-106">Om ondersteuning te bieden voor elektronische documentindelingen, gebruikt u het kader voor gegevensuitwisseling.</span><span class="sxs-lookup"><span data-stu-id="73638-106">To provide support for other electronic document formats, you use the data exchange framework.</span></span>  

 <span data-ttu-id="73638-107">In de algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] is een service voor documentuitwisseling vooraf geconfigureerd zodat u deze kunt instellen voor uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="73638-107">In the generic version of [!INCLUDE[d365fin](includes/d365fin_md.md)], a document exchange service is preconfigured and ready to be set up for your company.</span></span> <span data-ttu-id="73638-108">Zie [Een service voor documentuitwisseling instellen](across-how-to-set-up-a-document-exchange-service.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="73638-108">For more information, see [Set Up a Document Exchange Service](across-how-to-set-up-a-document-exchange-service.md).</span></span>  

 <span data-ttu-id="73638-109">Als u een verkoopfactuur als elektronisch PEPPOL-document wilt versturen, selecteert u de optie **Elektronisch document** in het dialoogvenster **Boeken en verzenden**. Hierin kunt u dit ook instellen als standaardprofiel voor documentverzending van de klant.</span><span class="sxs-lookup"><span data-stu-id="73638-109">To send a sales invoice as an electronic PEPPOL document, you select the **Electronic Document** option in the **Post and Send** dialog box from where you can also set up the customer’s default document sending profile.</span></span> <span data-ttu-id="73638-110">Eerst moet u diverse stamgegevens instellen, zoals bedrijfsgegevens, klanten, artikelen en eenheden.</span><span class="sxs-lookup"><span data-stu-id="73638-110">First, you must set up various master data, such as company information, customers, items, and units of measure.</span></span> <span data-ttu-id="73638-111">Deze worden gebruikt om de zakelijke partners en artikelen te identificeren wanneer gegevens worden geconverteerd in velden in [Verzending en ontvangst van elektronische documenten instellen](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="73638-111">These are used to identify the business partners and items when converting data in fields in [Set Up Electronic Document Sending and Receiving](across-how-to-set-up-electronic-document-sending-and-receiving.md).</span></span>  

### <a name="to-send-an-electronic-sales-invoice"></a><span data-ttu-id="73638-112">Een elektronische verkoopfactuur verzenden</span><span class="sxs-lookup"><span data-stu-id="73638-112">To send an electronic sales invoice</span></span>  

1.  <span data-ttu-id="73638-113">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="73638-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="73638-114">Maak een nieuwe verkoopfactuur.</span><span class="sxs-lookup"><span data-stu-id="73638-114">Create a new sales invoice.</span></span>  

3.  <span data-ttu-id="73638-115">Als de verkoopfactuur gereed is voor facturering, kiest u op het tabblad **Acties** in de groep **Boeken** de optie **Boeken en verzenden**.</span><span class="sxs-lookup"><span data-stu-id="73638-115">When the sales invoice is ready to be invoiced, on the **Actions** tab, in the **Posting** group, choose **Post and Send**.</span></span>  

     <span data-ttu-id="73638-116">Als het standaardverzendprofiel van de klant **Elektronisch document** is, wordt dit aangegeven in het dialoogvenster **Boeken en bevestiging verzenden** en hoeft u alleen maar de knop **Ja** te kiezen om de factuur te boeken en elektronisch te verzenden in de geselecteerde indeling.</span><span class="sxs-lookup"><span data-stu-id="73638-116">If the customer’s default sending profile is **Electronic Document**, then it will be shown in the **Post and Send Confirmation** dialog box and you just have to choose the **Yes** button to post and send the invoice electronically in the selected format.</span></span>  

4.  <span data-ttu-id="73638-117">In het dialoogvenster **Boeken en bevestiging verzenden** kiest u de Knop AssistEdit rechts van het veld **Document verzenden naar**.</span><span class="sxs-lookup"><span data-stu-id="73638-117">In the **Post and Send Confirmation** dialog box, choose the AssistEdit button to the right of the **Send Document to** field.</span></span>  

5.  <span data-ttu-id="73638-118">Kies in het dialoogvenster **Document verzenden naar** in het veld **Elektronisch document** de optie **Via service voor documentuitwisseling**.</span><span class="sxs-lookup"><span data-stu-id="73638-118">In the **Send Document to** dialog box, in the **Electronic Document** field, choose **Through Document Exchange Service**.</span></span>  

6.  <span data-ttu-id="73638-119">Kies in het veld **Indeling** de optie **PEPPOL**.</span><span class="sxs-lookup"><span data-stu-id="73638-119">In the **Format** field, choose **PEPPOL**.</span></span>  

7.  <span data-ttu-id="73638-120">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="73638-120">Choose the **OK** button.</span></span> <span data-ttu-id="73638-121">Het dialoogvenster **Boeken en bevestiging verzenden** verschijnt.</span><span class="sxs-lookup"><span data-stu-id="73638-121">The **Post and Send Confirmation** dialog box appears.</span></span> <span data-ttu-id="73638-122">**Elektronisch document (PEPPOL)** is toegevoegd aan het veld **Document verzenden naar**.</span><span class="sxs-lookup"><span data-stu-id="73638-122">**Electronic Document (PEPPOL)** is added to the **Send Document to** field.</span></span>  

8.  <span data-ttu-id="73638-123">Kies de knop **Ja**.</span><span class="sxs-lookup"><span data-stu-id="73638-123">Choose the **Yes** button.</span></span>  

     <span data-ttu-id="73638-124">De verkoopfactuur wordt geboekt en aan de klant gezonden als elektronisch document in de indeling PEPPOL.</span><span class="sxs-lookup"><span data-stu-id="73638-124">The sales invoice is posted and sent to the customer as an electronic document in the PEPPOL format.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="73638-125">U kunt ook een geboekte verkoopfactuur als een elektronisch document verzenden.</span><span class="sxs-lookup"><span data-stu-id="73638-125">You can also send a posted sales invoice as an electronic document.</span></span> <span data-ttu-id="73638-126">De procedure is hetzelfde als beschreven in dit onderwerp voor niet-geboekte verkoopdocumenten.</span><span class="sxs-lookup"><span data-stu-id="73638-126">The procedure is the same as described in this topic for non-posted sales documents.</span></span> <span data-ttu-id="73638-127">Kies in het venster **Geboekte verkoopfactuur**, op het tabblad **Acties**, in de groep **Algemeen** de optie **Activiteitenlogbestand** om de status van het elektronische document te bekijken.</span><span class="sxs-lookup"><span data-stu-id="73638-127">In the **Posted Sales Invoice** window, on the **Actions** tab, in the **General** group, choose **Activity Log** to view the status of the electronic document.</span></span> <span data-ttu-id="73638-128">Zie voor meer informatie **Activiteitenlogbestand**.</span><span class="sxs-lookup"><span data-stu-id="73638-128">For more information, see **Activity Log**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="73638-129">Zie ook</span><span class="sxs-lookup"><span data-stu-id="73638-129">See Also</span></span>  
[<span data-ttu-id="73638-130">Verkopen factureren</span><span class="sxs-lookup"><span data-stu-id="73638-130">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="73638-131">Verzendprofielen van documenten instellen</span><span class="sxs-lookup"><span data-stu-id="73638-131">Set Up Document Sending Profiles</span></span>](sales-how-setup-document-send-profiles.md)  
[<span data-ttu-id="73638-132">Verzending en ontvangst van elektronische documenten instellen</span><span class="sxs-lookup"><span data-stu-id="73638-132">Set Up Electronic Document Sending and Receiving</span></span>](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[<span data-ttu-id="73638-133">Een service voor documentuitwisseling instellen</span><span class="sxs-lookup"><span data-stu-id="73638-133">Set Up a Document Exchange Service</span></span>](across-how-to-set-up-a-document-exchange-service.md)  
[<span data-ttu-id="73638-134">Definities voor gegevensuitwisseling instellen</span><span class="sxs-lookup"><span data-stu-id="73638-134">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="73638-135">Gegevens elektronisch uitwisselen</span><span class="sxs-lookup"><span data-stu-id="73638-135">Exchanging Data Electronically</span></span>](across-data-exchange.md)  
[<span data-ttu-id="73638-136">Algemene bedrijfsfunctionaliteit</span><span class="sxs-lookup"><span data-stu-id="73638-136">General Business Functionality</span></span>](ui-across-business-areas.md)  

