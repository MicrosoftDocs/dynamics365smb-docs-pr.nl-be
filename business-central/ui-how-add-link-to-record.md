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
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 84d58193fa7ee272b372403d63702348fbfb1f77
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315288"
---
# <a name="manage-attachments-links-and-notes-on-cards-and-documents"></a><span data-ttu-id="5f751-103">Bijlagen, koppelingen en notities op kaarten en in documenten beheren</span><span class="sxs-lookup"><span data-stu-id="5f751-103">Manage Attachments, Links, and Notes on Cards and Documents</span></span>

<span data-ttu-id="5f751-104">In het feitenblok op de meeste kaarten en documenten kunt u bestanden bijvoegen, koppelingen toevoegen en notities schrijven.</span><span class="sxs-lookup"><span data-stu-id="5f751-104">In the FactBox on most cards and documents, you can attach files, add links, and write notes.</span></span> <span data-ttu-id="5f751-105">Voor koppelingen en notities kunt u dit ook op de lijstpagina doen door eerst de bijbehorende regel te selecteren.</span><span class="sxs-lookup"><span data-stu-id="5f751-105">For links and notes, you can also do this on the list page by first selecting the related line.</span></span>

<span data-ttu-id="5f751-106">Als u een van deze bijgevoegde informatietypen wilt bekijken of wijzigen, moet u eerst het tabblad **Bijlagen** openen in het feitenblok.</span><span class="sxs-lookup"><span data-stu-id="5f751-106">To view or change any of these attached information types, you must first open the **Attachments** tab in the FactBox.</span></span> <span data-ttu-id="5f751-107">Het getal achter de titel van het tabblad geeft aan hoeveel bijgevoegde bestanden, koppelingen of notities er zijn voor de kaart of het document.</span><span class="sxs-lookup"><span data-stu-id="5f751-107">The number behind the tab title indicates how many attached files, links, or notes exist for the card or document.</span></span>

<span data-ttu-id="5f751-108">Bijlagen, koppelingen en notities blijven gekoppeld terwijl de kaart of het document wordt verwerkt in andere staten, zoals van een lopende verkooporder naar een geboekte verkoopfactuur.</span><span class="sxs-lookup"><span data-stu-id="5f751-108">Attachments, links, and notes stay attached as the card or document is processed into other states, such as from an ongoing sales order to a posted sales invoice.</span></span> <span data-ttu-id="5f751-109">Geen van de bijlagetypen wordt echter door het systeem uitgevoerd, bijvoorbeeld bij het afdrukken of bij het opslaan in een bestand.</span><span class="sxs-lookup"><span data-stu-id="5f751-109">Note, however, that none of the attachment types are output from the system, for example, when printing or when saving to a file.</span></span>

## <a name="to-attach-a-file-to-a-purchase-invoice"></a><span data-ttu-id="5f751-110">Een bestand bijvoegen bij een inkoopfactuur</span><span class="sxs-lookup"><span data-stu-id="5f751-110">To attach a file to a purchase invoice</span></span>
<span data-ttu-id="5f751-111">U kunt elk type bestand met tekst, afbeelding of video aan een kaart of document toevoegen.</span><span class="sxs-lookup"><span data-stu-id="5f751-111">You can attach any type of file, containing text, image, or video, to a card or document.</span></span> <span data-ttu-id="5f751-112">Dit is bijvoorbeeld handig als u de factuur van een leverancier wilt opslaan als PDF-bestand op de bijbehorende inkoopfactuur in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5f751-112">This is useful, for example, when you want to store a vendor's invoice as a PDF file on the related purchase invoice in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]
> <span data-ttu-id="5f751-113">Bestanden die zijn gekoppeld met de functie Inkomende documenten, worden niet opgenomen op het tabblad **Bijlagen**. Zie voor meer informatie [Inkomende documenten](across-income-documents.md).</span><span class="sxs-lookup"><span data-stu-id="5f751-113">Files attached with the Incoming Documents feature are not included on the **Attachments** tab. For more information, see [Incoming Documents](across-income-documents.md).</span></span>

<span data-ttu-id="5f751-114">De volgende procedure is gebaseerd op een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="5f751-114">The following procedure is based on a sales order.</span></span> <span data-ttu-id="5f751-115">De stappen lijken op alle andere ondersteunde documenten en kaarten.</span><span class="sxs-lookup"><span data-stu-id="5f751-115">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="5f751-116">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="5f751-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="5f751-117">Open de verkooporder waaraan u een bestand wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="5f751-117">Open the sales order that you want to attach a file to.</span></span>
3. <span data-ttu-id="5f751-118">Open het feitenblok **Bijlagen**.</span><span class="sxs-lookup"><span data-stu-id="5f751-118">In the FactBox, open the **Attachments** tab.</span></span>
4. <span data-ttu-id="5f751-119">Kies de waarde achter het veld **Documenten**, zoals '0'.</span><span class="sxs-lookup"><span data-stu-id="5f751-119">Choose the value behind the **Documents** field, such as "0".</span></span>
5. <span data-ttu-id="5f751-120">Kies op de pagina **Gekoppelde documenten**, in het veld **Bijlage** de knop **Bestand selecteren**.</span><span class="sxs-lookup"><span data-stu-id="5f751-120">On the **Attached Documents** page, in the **Attachment** field, choose the **Select File** button.</span></span>
5. <span data-ttu-id="5f751-121">Selecteer een bestand van een willekeurige locatie en kies de knop **Openen**.</span><span class="sxs-lookup"><span data-stu-id="5f751-121">Select a file from any location, and then choose the **Open** button.</span></span>

<span data-ttu-id="5f751-122">Het bestand wordt nu gekoppeld aan de inkoopfactuur.</span><span class="sxs-lookup"><span data-stu-id="5f751-122">The file is now attached to the purchase invoice.</span></span>

## <a name="to-add-a-link-from-an-item-card"></a><span data-ttu-id="5f751-123">Een koppeling toevoegen vanuit een artikelkaart</span><span class="sxs-lookup"><span data-stu-id="5f751-123">To add a link from an item card</span></span>
<span data-ttu-id="5f751-124">U kunt een koppeling vanuit een kaart of document toevoegen aan een URL of pad.</span><span class="sxs-lookup"><span data-stu-id="5f751-124">You can add a link from a card or document to any URL or path.</span></span> <span data-ttu-id="5f751-125">Dit is bijvoorbeeld handig als u een artikelkaart wilt koppelen aan de artikelcatalogus van de leverancier.</span><span class="sxs-lookup"><span data-stu-id="5f751-125">This is useful, for example, when you want to link an item card with the supplier's item catalog.</span></span>

<span data-ttu-id="5f751-126">De volgende procedure is gebaseerd op een artikelkaart.</span><span class="sxs-lookup"><span data-stu-id="5f751-126">The following procedure is based on an item card.</span></span> <span data-ttu-id="5f751-127">De stappen lijken op alle andere ondersteunde documenten en kaarten.</span><span class="sxs-lookup"><span data-stu-id="5f751-127">The steps are similar for all other supported cards and documents.</span></span>

1. <span data-ttu-id="5f751-128">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="5f751-128">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="5f751-129">Selecteer het item waaruit u een koppeling wilt toevoegen en kies vervolgens het tabblad **Bijlagen** in het feitenblok.</span><span class="sxs-lookup"><span data-stu-id="5f751-129">Select the item that you want to add a link from, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="5f751-130">Kies in de **Koppelingen** het pictogram **+**.</span><span class="sxs-lookup"><span data-stu-id="5f751-130">In the **Links**, choose the **+** icon.</span></span>
4. <span data-ttu-id="5f751-131">Voer in het veld **Koppelingsadres** de koppeling in.</span><span class="sxs-lookup"><span data-stu-id="5f751-131">In the **Link Address** field, enter the link.</span></span>

    - <span data-ttu-id="5f751-132">Als u een koppeling wilt maken met een bestand op uw computer of netwerk, voert u het volledige pad en de bestandsnaam in, bijvoorbeeld **C:\My Documents\invoice1.doc**.</span><span class="sxs-lookup"><span data-stu-id="5f751-132">To link to a file on your computer or network, enter the full path and file name, such as **C:\My Documents\invoice1.doc**.</span></span>
    - <span data-ttu-id="5f751-133">Als u een koppeling met een website wilt toevoegen, voert u het internetadres (URL) in, bijvoorbeeld **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="5f751-133">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    - <span data-ttu-id="5f751-134">Als u een koppeling met een programma wilt toevoegen, voert u een bepaalde tekenreeks in om het programma te openen.</span><span class="sxs-lookup"><span data-stu-id="5f751-134">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="5f751-135">Als u Outlook bijvoorbeeld wilt openen met een nieuwe lege e-mail naar een bepaalde alias, voert u **mailto:testalias** in.</span><span class="sxs-lookup"><span data-stu-id="5f751-135">For example, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5. <span data-ttu-id="5f751-136">Voer in het veld **Beschrijving** informatie over de koppeling in.</span><span class="sxs-lookup"><span data-stu-id="5f751-136">In the **Description** field, enter any information about the link.</span></span>  
6. <span data-ttu-id="5f751-137">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="5f751-137">Choose the **OK** button.</span></span>

<span data-ttu-id="5f751-138">De koppeling is nu gekoppeld aan de artikelkaart.</span><span class="sxs-lookup"><span data-stu-id="5f751-138">The link is now attached to the item card.</span></span>  

## <a name="to-write-a-note-on-a-sales-order"></a><span data-ttu-id="5f751-139">Een notitie over een klantorder schrijven</span><span class="sxs-lookup"><span data-stu-id="5f751-139">To write a note on a sales order</span></span>
<span data-ttu-id="5f751-140">U kunt bijvoorbeeld een notitie op een document of kaart schrijven om speciale instructies aan andere gebruikers van het document of de kaart te communiceren.</span><span class="sxs-lookup"><span data-stu-id="5f751-140">You can write a note on a document or card, for example, to communicate special instructions to other users of the document or card.</span></span> <span data-ttu-id="5f751-141">U kunt bestandskoppelingen en URL's opnemen in notities.</span><span class="sxs-lookup"><span data-stu-id="5f751-141">You can include file links and URLs in notes.</span></span>

> [!NOTE]
> <span data-ttu-id="5f751-142">Opmerkingen over het tabblad **Bijlagen** zijn niet gerelateerd aan interne notitiefunctionaliteit, die voornamelijk wordt gebruikt om te communiceren tussen werkstroomgebruikers.</span><span class="sxs-lookup"><span data-stu-id="5f751-142">Notes on the **Attachments** tab are not related to internal notes functionality, which is mainly used to communicate between workflow users.</span></span> <span data-ttu-id="5f751-143">Zie voor meer informatie [Werkstroomberichten instellen](across-setting-up-workflow-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="5f751-143">For more information, see [Setting Up Workflow Notifications](across-setting-up-workflow-notifications.md).</span></span>

<span data-ttu-id="5f751-144">De volgende procedure is gebaseerd op een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="5f751-144">The following procedure is based on a sales order.</span></span> <span data-ttu-id="5f751-145">De stappen lijken op alle andere ondersteunde documenten en kaarten.</span><span class="sxs-lookup"><span data-stu-id="5f751-145">The steps are similar for all other supported documents and cards.</span></span>

1. <span data-ttu-id="5f751-146">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="5f751-146">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Sales Orders**, and then choose the related link.</span></span>
2. <span data-ttu-id="5f751-147">Selecteer de verkooporder waarin u een notitie wilt schrijven en kies vervolgens het tabblad **Bijlagen** in het feitenblok.</span><span class="sxs-lookup"><span data-stu-id="5f751-147">Select the sales order that you want to write a note on, and then choose the **Attachments** tab in the FactBox.</span></span>
3. <span data-ttu-id="5f751-148">Kies in de sectie **Notities** het pictogram **+**.</span><span class="sxs-lookup"><span data-stu-id="5f751-148">In the **Notes** section, choose the **+** icon.</span></span>
4. <span data-ttu-id="5f751-149">Schrijf in het veld **Notitie** tekst, zoals "Dit is een dringende bestelling."</span><span class="sxs-lookup"><span data-stu-id="5f751-149">In the **Note** field, write any text, such as "This is an urgent order.".</span></span>
5. <span data-ttu-id="5f751-150">Kies de knop **Ok**.</span><span class="sxs-lookup"><span data-stu-id="5f751-150">Choose the **OK** button.</span></span>

<span data-ttu-id="5f751-151">De notitie is nu aan de verkooporder toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="5f751-151">The note is now attached to the sales order.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f751-152">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5f751-152">See Also</span></span>  
<span data-ttu-id="5f751-153">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5f751-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="5f751-154">Inkomende documenten</span><span class="sxs-lookup"><span data-stu-id="5f751-154">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="5f751-155">Werkstroomberichten instellen</span><span class="sxs-lookup"><span data-stu-id="5f751-155">Setting Up Workflow Notifications</span></span>](across-setting-up-workflow-notifications.md)  
