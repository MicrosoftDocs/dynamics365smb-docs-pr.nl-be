---
title: Bijlagen, koppelingen en notities aan records toevoegen | Microsoft Docs
description: Koppel een hyperlink aan een document of een website aan een bepaalde record, zoals een klant of document.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/27/2020
ms.author: sgroespe
ms.openlocfilehash: 9d456fba507977121809124d1de0d23a098406f5
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324426"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="7a415-103">Bijlagen, koppelingen en notities op kaarten en in documenten beheren</span><span class="sxs-lookup"><span data-stu-id="7a415-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="7a415-104">In het feitenblok op de meeste kaarten en documenten kunt u bestanden bijvoegen, koppelingen toevoegen en notities schrijven.</span><span class="sxs-lookup"><span data-stu-id="7a415-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="7a415-105">Voor koppelingen en notities kunt u dit ook op de lijstpagina doen door eerst de bijbehorende regel te selecteren.</span><span class="sxs-lookup"><span data-stu-id="7a415-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="7a415-106">Als u een van deze bijgevoegde informatietypen wilt bekijken of wijzigen, moet u eerst het tabblad **Bijlagen** openen in het feitenblok.</span><span class="sxs-lookup"><span data-stu-id="7a415-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="7a415-107">Het getal achter de titel van het tabblad geeft aan hoeveel bijgevoegde bestanden, koppelingen of notities er zijn voor de kaart of het document.</span><span class="sxs-lookup"><span data-stu-id="7a415-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="7a415-108">Bijlagen, koppelingen en notities blijven gekoppeld terwijl de kaart of het document wordt verwerkt in andere staten, zoals van een lopende verkooporder naar een geboekte verkoopfactuur.</span><span class="sxs-lookup"><span data-stu-id="7a415-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="7a415-109">Geen van de bijlagetypen wordt echter door het systeem uitgevoerd, bijvoorbeeld bij het afdrukken of bij het opslaan in een bestand.</span><span class="sxs-lookup"><span data-stu-id="7a415-109">However, none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

> [!NOTE]
> <span data-ttu-id="7a415-110">Wanneer u een verkooporder of inkooporder gedeeltelijk verzendt en factureert, wordt de bijlage alleen aan de definitieve factuur van die order toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="7a415-110">When you partially ship and invoice a sales order or purchase order, the attachment will only be attached to the final invoice of that order.</span></span> <span data-ttu-id="7a415-111">Wanneer u factureert met de functie Uitstel, wordt de bijlage alleen gekoppeld aan de grootboekposten voor het document, maar niet voor de uitstelposten.</span><span class="sxs-lookup"><span data-stu-id="7a415-111">Likewise, when you invoice using the Deferrals feature, the attachment is only attached to the G/L entries for the document but not for the deferral entries.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="7a415-112">Een bestand bijvoegen bij een inkoopfactuur</span><span class="sxs-lookup"><span data-stu-id="7a415-112">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="7a415-113">U kunt elk type bestand met tekst, afbeelding of video aan een kaart of document toevoegen.</span><span class="sxs-lookup"><span data-stu-id="7a415-113">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="7a415-114">Dit is bijvoorbeeld handig als u de factuur van een leverancier wilt opslaan als PDF-bestand op de bijbehorende inkoopfactuur in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="7a415-114">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="7a415-115">Bestanden die zijn gekoppeld met de functie Inkomende documenten, worden niet opgenomen op het tabblad **Bijlagen**. Zie voor meer informatie [Inkomende documenten](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="7a415-115">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="7a415-116">De volgende procedure is gebaseerd op een inkoopfactuur.</span><span class="sxs-lookup"><span data-stu-id="7a415-116">The following procedure is based on a purchase invoice.</span></span> <span data-ttu-id="7a415-117">De stappen lijken op alle andere ondersteunde documenten en kaarten.</span><span class="sxs-lookup"><span data-stu-id="7a415-117">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="7a415-118">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="7a415-118">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="7a415-119">Open de verkooporder waaraan u een bestand wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="7a415-119">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="7a415-120">Open het feitenblok **Bijlagen**.</span><span class="sxs-lookup"><span data-stu-id="7a415-120">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="7a415-121">Kies de waarde achter het veld **Documenten**, zoals '0'.</span><span class="sxs-lookup"><span data-stu-id="7a415-121">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="7a415-122">Kies op de pagina **Gekoppelde documenten** in het veld **Bijlage** de actie **Bestand selecteren**.</span><span class="sxs-lookup"><span data-stu-id="7a415-122">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** action.</span></span>
5. <span data-ttu-id="7a415-123">Selecteer een bestand van een willekeurige locatie en kies de knop **Openen**.</span><span class="sxs-lookup"><span data-stu-id="7a415-123">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="7a415-124">Het bestand wordt nu gekoppeld aan de inkoopfactuur.</span><span class="sxs-lookup"><span data-stu-id="7a415-124">The file is now attached to the purchase invoice.</span></span>

## <a name="to-view-an-attached-file"></a><span data-ttu-id="7a415-125">Een gekoppeld bestand weergeven</span><span class="sxs-lookup"><span data-stu-id="7a415-125">To view an attached file</span></span>
1. <span data-ttu-id="7a415-126">Open het feitenblok **Bijlagen**.</span><span class="sxs-lookup"><span data-stu-id="7a415-126">In the FactBox, open the **Attachments** tab.</span></span>
2. <span data-ttu-id="7a415-127">Kies de waarde achter het veld **Documenten**, zoals '1'.</span><span class="sxs-lookup"><span data-stu-id="7a415-127">Choose the value behind the **Documents** field, such as "1".</span></span>
3. <span data-ttu-id="7a415-128">Kies op de pagina **Gekoppelde documenten** de actie **Voorbeeld**.</span><span class="sxs-lookup"><span data-stu-id="7a415-128">On the **Attached Documents** page, choose the **Preview** action.</span></span>
4. <span data-ttu-id="7a415-129">Open het gedownloade bestand.</span><span class="sxs-lookup"><span data-stu-id="7a415-129">Open the downloaded file.</span></span>

## <a name="to-save-a-document-as-a-pdf-attachment"></a><span data-ttu-id="7a415-130">Een document als PDF-bijlage opslaan</span><span class="sxs-lookup"><span data-stu-id="7a415-130">To save a document as a PDF attachment</span></span>
<span data-ttu-id="7a415-131">Wanneer u een document als bestand moet opslaan, kunt u de actie **Bijvoegen als PDF** gebruiken om de huidige documentinhoud vast te leggen als een PDF-bestand als bijlage bij het feitenblok van het document.</span><span class="sxs-lookup"><span data-stu-id="7a415-131">Whenever you need to save a document as a file, you can use the **Attach as PDF** action to capture the current document content as a PDF file attached to the FactBox of the document.</span></span> <span data-ttu-id="7a415-132">Dit is bijvoorbeeld handig wanneer documenten meerdere stappen in een proces volgen, zoals een verkoopproces of een goedkeuringswerkstroom, en u wilt verwijzen naar een afdruk van de vorige stap.</span><span class="sxs-lookup"><span data-stu-id="7a415-132">This is useful, for example, when documents follow multiple steps in a process, such as a sales process or an approval workflow, and you want to refer to a printout of the previous step.</span></span>

<span data-ttu-id="7a415-133">De volgende procedure is gebaseerd op een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="7a415-133">The following procedure is based on a sales order.</span></span> <span data-ttu-id="7a415-134">De stappen zijn vergelijkbaar voor alle ondersteunde documenten.</span><span class="sxs-lookup"><span data-stu-id="7a415-134">The steps are similar for all supported documents.</span></span>

1. <span data-ttu-id="7a415-135">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="7a415-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="7a415-136">Selecteer een verkooporder en kies de actie **Bijvoegen als PDF**.</span><span class="sxs-lookup"><span data-stu-id="7a415-136">Select a sales order, and then choose the **Attach as PDF** action.</span></span>

<span data-ttu-id="7a415-137">Een PDF-bestand met de huidige inhoud van de verkooporder wordt toegevoegd aan het tabblad **Bijlagen** in het feitenblok.</span><span class="sxs-lookup"><span data-stu-id="7a415-137">A PDF file with the current content of the sales order is added to the **Attachments** tab in the FactBox.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="7a415-138">Een koppeling toevoegen vanuit een artikelkaart</span><span class="sxs-lookup"><span data-stu-id="7a415-138">To add a link from an item card</span></span>
<span data-ttu-id="7a415-139">U kunt een koppeling vanuit een kaart of document toevoegen aan een URL of pad.</span><span class="sxs-lookup"><span data-stu-id="7a415-139">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="7a415-140">Dit is bijvoorbeeld handig als u een artikelkaart wilt koppelen aan de artikelcatalogus van de leverancier.</span><span class="sxs-lookup"><span data-stu-id="7a415-140">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="7a415-141">De volgende procedure is gebaseerd op een artikelkaart.</span><span class="sxs-lookup"><span data-stu-id="7a415-141">The following procedure is based on an item card.</span></span> <span data-ttu-id="7a415-142">De stappen lijken op alle andere ondersteunde documenten en kaarten.</span><span class="sxs-lookup"><span data-stu-id="7a415-142">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="7a415-143">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="7a415-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="7a415-144">Selecteer het item waaruit u een koppeling wilt toevoegen en kies vervolgens het tabblad **Bijlagen** in het feitenblok.</span><span class="sxs-lookup"><span data-stu-id="7a415-144">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="7a415-145">Kies in de **Koppelingen** het pictogram **+**.</span><span class="sxs-lookup"><span data-stu-id="7a415-145">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="7a415-146">Voer in het veld **Koppelingsadres** de koppeling in.</span><span class="sxs-lookup"><span data-stu-id="7a415-146">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="7a415-147">De koppeling moet een geldige internet- of intranet-URL zijn.</span><span class="sxs-lookup"><span data-stu-id="7a415-147">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="7a415-148">Voer in het veld **Beschrijving** informatie over de koppeling in.</span><span class="sxs-lookup"><span data-stu-id="7a415-148">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="7a415-149">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="7a415-149">Choose the **OK** button.</span></span>

<span data-ttu-id="7a415-150">De koppeling is nu gekoppeld aan de artikelkaart.</span><span class="sxs-lookup"><span data-stu-id="7a415-150">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="7a415-151">Een notitie over een klantorder schrijven</span><span class="sxs-lookup"><span data-stu-id="7a415-151">To write a note on a sales order</span></span>
<span data-ttu-id="7a415-152">U kunt bijvoorbeeld een notitie op een document of kaart schrijven om speciale instructies aan andere gebruikers van het document of de kaart te communiceren.</span><span class="sxs-lookup"><span data-stu-id="7a415-152">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="7a415-153">U kunt bestandskoppelingen en URL's opnemen in notities.</span><span class="sxs-lookup"><span data-stu-id="7a415-153">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="7a415-154">Opmerkingen over het tabblad **Bijlagen** zijn niet gerelateerd aan interne notitiefunctionaliteit, die voornamelijk wordt gebruikt om te communiceren tussen werkstroomgebruikers.</span><span class="sxs-lookup"><span data-stu-id="7a415-154">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="7a415-155">Zie voor meer informatie [Werkstroomberichten instellen](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="7a415-155">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="7a415-156">De volgende procedure is gebaseerd op een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="7a415-156">The following procedure is based on a sales order.</span></span> <span data-ttu-id="7a415-157">De stappen lijken op alle andere ondersteunde documenten en kaarten.</span><span class="sxs-lookup"><span data-stu-id="7a415-157">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="7a415-158">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="7a415-158">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="7a415-159">Selecteer de verkooporder waarin u een notitie wilt schrijven en kies vervolgens het tabblad **Bijlagen** in het feitenblok.</span><span class="sxs-lookup"><span data-stu-id="7a415-159">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="7a415-160">Kies in de sectie **Notities** het pictogram **+**.</span><span class="sxs-lookup"><span data-stu-id="7a415-160">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="7a415-161">Schrijf in het veld **Notitie** tekst, zoals "Dit is een dringende bestelling."</span><span class="sxs-lookup"><span data-stu-id="7a415-161">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="7a415-162">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="7a415-162">Choose the **OK** button.</span></span>

<span data-ttu-id="7a415-163">De notitie is nu aan de verkooporder toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="7a415-163">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a415-164">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7a415-164">See Also</span></span>  
<span data-ttu-id="7a415-165">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7a415-165">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="7a415-166">Inkomende documenten</span><span class="sxs-lookup"><span data-stu-id="7a415-166">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="7a415-167">Werkstroomberichten instellen</span><span class="sxs-lookup"><span data-stu-id="7a415-167">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
