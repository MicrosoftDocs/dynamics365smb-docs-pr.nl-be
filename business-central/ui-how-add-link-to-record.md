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
ms.date: 10/21/2019
ms.author: sgroespe
ms.openlocfilehash: 88e6a04a8e4a992b6a5df3fee87104eba7b5510e
ms.sourcegitcommit: be1e2c49a8434d3f440d5a201508af9c3c8cc87f
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/22/2019
ms.locfileid: "2649800"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="d69ca-103">Bijlagen, koppelingen en notities op kaarten en in documenten beheren</span><span class="sxs-lookup"><span data-stu-id="d69ca-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="d69ca-104">In het feitenblok op de meeste kaarten en documenten kunt u bestanden bijvoegen, koppelingen toevoegen en notities schrijven.</span><span class="sxs-lookup"><span data-stu-id="d69ca-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="d69ca-105">Voor koppelingen en notities kunt u dit ook op de lijstpagina doen door eerst de bijbehorende regel te selecteren.</span><span class="sxs-lookup"><span data-stu-id="d69ca-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="d69ca-106">Als u een van deze bijgevoegde informatietypen wilt bekijken of wijzigen, moet u eerst het tabblad **Bijlagen** openen in het feitenblok.</span><span class="sxs-lookup"><span data-stu-id="d69ca-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="d69ca-107">Het getal achter de titel van het tabblad geeft aan hoeveel bijgevoegde bestanden, koppelingen of notities er zijn voor de kaart of het document.</span><span class="sxs-lookup"><span data-stu-id="d69ca-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="d69ca-108">Bijlagen, koppelingen en notities blijven gekoppeld terwijl de kaart of het document wordt verwerkt in andere staten, zoals van een lopende verkooporder naar een geboekte verkoopfactuur.</span><span class="sxs-lookup"><span data-stu-id="d69ca-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="d69ca-109">Geen van de bijlagetypen wordt echter door het systeem uitgevoerd, bijvoorbeeld bij het afdrukken of bij het opslaan in een bestand.</span><span class="sxs-lookup"><span data-stu-id="d69ca-109">Note, however, that none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="d69ca-110">Een bestand bijvoegen bij een inkoopfactuur</span><span class="sxs-lookup"><span data-stu-id="d69ca-110">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="d69ca-111">U kunt elk type bestand met tekst, afbeelding of video aan een kaart of document toevoegen.</span><span class="sxs-lookup"><span data-stu-id="d69ca-111">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="d69ca-112">Dit is bijvoorbeeld handig als u de factuur van een leverancier wilt opslaan als PDF-bestand op de bijbehorende inkoopfactuur in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d69ca-112">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="d69ca-113">Bestanden die zijn gekoppeld met de functie Inkomende documenten, worden niet opgenomen op het tabblad **Bijlagen**. Zie voor meer informatie [Inkomende documenten](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="d69ca-113">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="d69ca-114">De volgende procedure is gebaseerd op een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="d69ca-114">The following procedure is based on a sales order.</span></span> <span data-ttu-id="d69ca-115">De stappen lijken op alle andere ondersteunde documenten en kaarten.</span><span class="sxs-lookup"><span data-stu-id="d69ca-115">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="d69ca-116">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="d69ca-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="d69ca-117">Open de verkooporder waaraan u een bestand wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="d69ca-117">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="d69ca-118">Open het feitenblok **Bijlagen**.</span><span class="sxs-lookup"><span data-stu-id="d69ca-118">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="d69ca-119">Kies de waarde achter het veld **Documenten**, zoals '0'.</span><span class="sxs-lookup"><span data-stu-id="d69ca-119">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="d69ca-120">Kies op de pagina **Gekoppelde documenten**, in het veld **Bijlage** de knop **Bestand selecteren**.</span><span class="sxs-lookup"><span data-stu-id="d69ca-120">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** button.</span></span>
5. <span data-ttu-id="d69ca-121">Selecteer een bestand van een willekeurige locatie en kies de knop **Openen**.</span><span class="sxs-lookup"><span data-stu-id="d69ca-121">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="d69ca-122">Het bestand wordt nu gekoppeld aan de inkoopfactuur.</span><span class="sxs-lookup"><span data-stu-id="d69ca-122">The file is now attached to the purchase invoice.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="d69ca-123">Een koppeling toevoegen vanuit een artikelkaart</span><span class="sxs-lookup"><span data-stu-id="d69ca-123">To add a link from an item card</span></span>
<span data-ttu-id="d69ca-124">U kunt een koppeling vanuit een kaart of document toevoegen aan een URL of pad.</span><span class="sxs-lookup"><span data-stu-id="d69ca-124">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="d69ca-125">Dit is bijvoorbeeld handig als u een artikelkaart wilt koppelen aan de artikelcatalogus van de leverancier.</span><span class="sxs-lookup"><span data-stu-id="d69ca-125">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="d69ca-126">De volgende procedure is gebaseerd op een artikelkaart.</span><span class="sxs-lookup"><span data-stu-id="d69ca-126">The following procedure is based on an item card.</span></span> <span data-ttu-id="d69ca-127">De stappen lijken op alle andere ondersteunde documenten en kaarten.</span><span class="sxs-lookup"><span data-stu-id="d69ca-127">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="d69ca-128">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="d69ca-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="d69ca-129">Selecteer het item waaruit u een koppeling wilt toevoegen en kies vervolgens het tabblad **Bijlagen** in het feitenblok.</span><span class="sxs-lookup"><span data-stu-id="d69ca-129">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="d69ca-130">Kies in de **Koppelingen** het pictogram **+**.</span><span class="sxs-lookup"><span data-stu-id="d69ca-130">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="d69ca-131">Voer in het veld **Koppelingsadres** de koppeling in.</span><span class="sxs-lookup"><span data-stu-id="d69ca-131">In the **Link Address** field, enter the link.</span></span>

    <span data-ttu-id="d69ca-132">De koppeling moet een geldige internet- of intranet-URL zijn.</span><span class="sxs-lookup"><span data-stu-id="d69ca-132">The link must be a valid internet or intranet URL.</span></span>

5. <span data-ttu-id="d69ca-133">Voer in het veld **Beschrijving** informatie over de koppeling in.</span><span class="sxs-lookup"><span data-stu-id="d69ca-133">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="d69ca-134">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="d69ca-134">Choose the **OK** button.</span></span>

<span data-ttu-id="d69ca-135">De koppeling is nu gekoppeld aan de artikelkaart.</span><span class="sxs-lookup"><span data-stu-id="d69ca-135">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="d69ca-136">Een notitie over een klantorder schrijven</span><span class="sxs-lookup"><span data-stu-id="d69ca-136">To write a note on a sales order</span></span>
<span data-ttu-id="d69ca-137">U kunt bijvoorbeeld een notitie op een document of kaart schrijven om speciale instructies aan andere gebruikers van het document of de kaart te communiceren.</span><span class="sxs-lookup"><span data-stu-id="d69ca-137">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="d69ca-138">U kunt bestandskoppelingen en URL's opnemen in notities.</span><span class="sxs-lookup"><span data-stu-id="d69ca-138">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="d69ca-139">Opmerkingen over het tabblad **Bijlagen** zijn niet gerelateerd aan interne notitiefunctionaliteit, die voornamelijk wordt gebruikt om te communiceren tussen werkstroomgebruikers.</span><span class="sxs-lookup"><span data-stu-id="d69ca-139">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="d69ca-140">Zie voor meer informatie [Werkstroomberichten instellen](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="d69ca-140">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="d69ca-141">De volgende procedure is gebaseerd op een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="d69ca-141">The following procedure is based on a sales order.</span></span> <span data-ttu-id="d69ca-142">De stappen lijken op alle andere ondersteunde documenten en kaarten.</span><span class="sxs-lookup"><span data-stu-id="d69ca-142">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="d69ca-143">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="d69ca-143">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="d69ca-144">Selecteer de verkooporder waarin u een notitie wilt schrijven en kies vervolgens het tabblad **Bijlagen** in het feitenblok.</span><span class="sxs-lookup"><span data-stu-id="d69ca-144">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="d69ca-145">Kies in de sectie **Notities** het pictogram **+**.</span><span class="sxs-lookup"><span data-stu-id="d69ca-145">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="d69ca-146">Schrijf in het veld **Notitie** tekst, zoals "Dit is een dringende bestelling."</span><span class="sxs-lookup"><span data-stu-id="d69ca-146">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="d69ca-147">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="d69ca-147">Choose the **OK** button.</span></span>

<span data-ttu-id="d69ca-148">De notitie is nu aan de verkooporder toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="d69ca-148">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="d69ca-149">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d69ca-149">See Also</span></span>  
<span data-ttu-id="d69ca-150">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d69ca-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="d69ca-151">Inkomende documenten</span><span class="sxs-lookup"><span data-stu-id="d69ca-151">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="d69ca-152">Werkstroomberichten instellen</span><span class="sxs-lookup"><span data-stu-id="d69ca-152">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
