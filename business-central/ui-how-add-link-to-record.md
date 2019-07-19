---
title: Vanuit een record naar externe gegevens of programma's koppelen | Microsoft Docs
description: Koppel een hyperlink aan een document of een website aan een bepaalde record, zoals een klant of document.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/12/2019
ms.author: jswymer
ms.openlocfilehash: 781f43daf6482c7e29696dc7a03aa021550cde7d
ms.sourcegitcommit: f2e3b571eab6e01d9f5aa8ef47056b6bd313dcbd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/13/2019
ms.locfileid: "1629769"
---
# <a name="add-links-to-websites-documents-or-programs-on-records"></a><span data-ttu-id="12689-103">Koppelingen naar websites, documenten of programma's voor records toevoegen</span><span class="sxs-lookup"><span data-stu-id="12689-103">Add Links to Websites, Documents, or Programs on Records</span></span>
<span data-ttu-id="12689-104">Voor een bepaalde record, zoals een klant, document of verkooporder, kunt u een koppeling naar een extern document, een website of een programma toevoegen.</span><span class="sxs-lookup"><span data-stu-id="12689-104">On a specific record, such as a customer, document, or sales order, you can add a link to an external document, website, or program.</span></span> <span data-ttu-id="12689-105">Of u wilt een koppeling die wordt geopend, e-mailen naar een bepaalde geadresseerde als u het selecteert.</span><span class="sxs-lookup"><span data-stu-id="12689-105">Or, you may want a link that opens a new empty email to a specific recipient when you select it.</span></span> <span data-ttu-id="12689-106">De kaartpagina voor sommige records, zoals klanten- en leverancierskaarten, bevatten een veld **Startpagina** waarin u een internetadres (URL) kunt opgeven.</span><span class="sxs-lookup"><span data-stu-id="12689-106">The card page for some records, such as customer and vendor cards, include a **Home Page** field where you can enter an Internet address (URL).</span></span> <span data-ttu-id="12689-107">Als u andere koppelingen wilt opnemen, kunt u de methode gebruiken die in dit artikel wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="12689-107">To include other links, you can use the method described in this article.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="12689-108">Momenteel is deze mogelijkheid alleen beschikbaar in [!INCLUDE [prodshort](includes/prodshort.md)] on-premises implementaties met de oude Dynamics NAV Windows-client.</span><span class="sxs-lookup"><span data-stu-id="12689-108">Currently, this capability is available only in [!INCLUDE [prodshort](includes/prodshort.md)] on-premises deployments with the legacy Dynamics NAV Windows client.</span></span>  

<span data-ttu-id="12689-109">Stel dat u afgedrukte facturen van leveranciers ontvangt.</span><span class="sxs-lookup"><span data-stu-id="12689-109">Another example could be when you receive printed invoices from vendors.</span></span> <span data-ttu-id="12689-110">U kunt deze scannen en als PDF-bestanden opslaan op een SharePoint-site.</span><span class="sxs-lookup"><span data-stu-id="12689-110">You can scan them and store them as .pdf files on a SharePoint site.</span></span> <span data-ttu-id="12689-111">Vervolgens kunt u in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] een koppeling vanuit een inkoopfactuur naar de betreffende factuur in SharePoint maken.</span><span class="sxs-lookup"><span data-stu-id="12689-111">Then you can make a link from a purchase invoice in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] to the corresponding invoice on  SharePoint.</span></span> <span data-ttu-id="12689-112">Ook kunt u een koppeling maken van een artikelkaart naar de overeenkomstige pagina in de onlinecatalogus van uw leverancier.</span><span class="sxs-lookup"><span data-stu-id="12689-112">Or, you can make a link from an item card to the corresponding page in your vendor's online catalog.</span></span>

## <a name="to-add-a-link-on-a-record"></a><span data-ttu-id="12689-113">Een koppeling aan een record toevoegen</span><span class="sxs-lookup"><span data-stu-id="12689-113">To add a link on a record</span></span>   

1.  <span data-ttu-id="12689-114">Open de record waaraan u de koppeling wilt koppelen, zoals een klantenkaart of een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="12689-114">Open the record that you want to attach the link to, such as a customer card or sales order.</span></span> <span data-ttu-id="12689-115">Als u de koppeling aan een bepaalde regel wilt koppelen, bijvoorbeeld aan een regel in een dagboek, selecteert u de regel.</span><span class="sxs-lookup"><span data-stu-id="12689-115">If you want to attach the link to a specific line, such as a journal line, select the line.</span></span>  

2.  <span data-ttu-id="12689-116">Kies de actie **Koppelingen** om de pagina **Koppelingen** te openen met alle koppelingen die aan die record zijn toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="12689-116">Choose the **Links** action to open the **Links** pages that shows all the current links that are added to the record.</span></span>

3. <span data-ttu-id="12689-117">Als u een nieuwe koppeling wilt toevoegen, kiest u **+nieuw**.</span><span class="sxs-lookup"><span data-stu-id="12689-117">To add a new link, choose **+new**.</span></span>

4.  <span data-ttu-id="12689-118">Voer in het veld **Koppelingsadres** het volgende in</span><span class="sxs-lookup"><span data-stu-id="12689-118">In the **Link Address** field, enter</span></span>

    -   <span data-ttu-id="12689-119">Als u een koppeling met een bestand op uw computer of netwerk wilt toevoegen, voert u het volledige pad en de bestandsnaam in, bijvoorbeeld **C:\My Documents\invoice1.doc**.</span><span class="sxs-lookup"><span data-stu-id="12689-119">To link to a file on your computer or network, enter the full path and file name, such as  **C:\My Documents\invoice1.doc**.</span></span>
    -   <span data-ttu-id="12689-120">Als u een koppeling met een website wilt toevoegen, voert u het internetadres (URL) in, bijvoorbeeld **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="12689-120">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="12689-121">Als u een koppeling met een programma wilt toevoegen, voert u een bepaalde tekenreeks in om het programma te openen.</span><span class="sxs-lookup"><span data-stu-id="12689-121">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="12689-122">Als u OneNote op een bepaalde pagina wilt openen, voert u bijvoorbeeld **onenote:///C:\My Documents/test.one** in.</span><span class="sxs-lookup"><span data-stu-id="12689-122">For example, to open OneNote with a specific page, enter **onenote:///C:\My Documents/test.one**.</span></span> <span data-ttu-id="12689-123">Als u Outlook wilt openen met een nieuwe lege e-mail naar een bepaalde alias, voert u **mailto:testalias** in.</span><span class="sxs-lookup"><span data-stu-id="12689-123">Or, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5.  <span data-ttu-id="12689-124">Vul het veld **Beschrijving** in met informatie over de koppeling.</span><span class="sxs-lookup"><span data-stu-id="12689-124">Fill in the **Description** field with information about the link.</span></span>  

6.  <span data-ttu-id="12689-125">Kies de knop **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="12689-125">Choose the **Save** button.</span></span>  

## <a name="to-delete-a-link-from-a-record"></a><span data-ttu-id="12689-126">Een koppeling uit een record verwijderen</span><span class="sxs-lookup"><span data-stu-id="12689-126">To delete a link from a record</span></span>  

<span data-ttu-id="12689-127">Als u een koppeling wilt verwijderen, kunt u op de pagina **Koppelingen** eerst **…** en vervolgens **Verwijderen** selecteren.</span><span class="sxs-lookup"><span data-stu-id="12689-127">To delete a link, on the **Links** page, you can select **...** and then **Delete**.</span></span>

<span data-ttu-id="12689-128">Als u één record verwijdert, bijvoorbeeld een verkooporderregel, een verkooporder of een klant, worden alle koppelingen verwijderd die aan die record zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="12689-128">If you delete a single record, such as a sales order line, a sales order, or a customer, then all the links attached to the record are deleted.</span></span> <span data-ttu-id="12689-129">Als u records echter verwijdert met een batchtaak, zoals de batchtaak **Gefact. verk.-orders verw.**, worden de koppelingen nog wel opgeslagen in de database.</span><span class="sxs-lookup"><span data-stu-id="12689-129">However, if you delete records using a batch job, such as the **Delete Invoiced Sales Orders** batch job, then the links are still stored in the database.</span></span> <span data-ttu-id="12689-130">U kunt ze uit de database verwijderen door de code-unit **Bestandskoppelingen zonder recordreferentie verwijderen** uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="12689-130">To delete the links from the database, run the **Delete Orphaned Record Links** codeunit.</span></span> <span data-ttu-id="12689-131">Als u dit wilt doen, kiest u het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Koppelingen zonder recordreferentie verwijderen** in en kiest u vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="12689-131">To do this, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Orphaned Record Links**, and then choose the related link.</span></span>   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a><span data-ttu-id="12689-132">Zie ook</span><span class="sxs-lookup"><span data-stu-id="12689-132">See Also</span></span>  
<span data-ttu-id="12689-133">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="12689-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
