---
title: Documenten zonder bijlagen zoeken| Microsoft Docs
Description: You can search for general ledger entries for posted purchase and sales documents that do not have incoming electronic documents, such as imported invoices.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: af0e886189750123dbee80e528e7c9d9b2c04f9f
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="ed4a4-102">Geboekte documenten zonder inkomende documentrecords zoeken</span><span class="sxs-lookup"><span data-stu-id="ed4a4-102">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="ed4a4-103">Vanuit de vensters **Rekeningschema** en **Grootboekposten** kunt u zoeken naar grootboekposten voor geboekte inkoop- en verkoopdocumenten die geen inkomende documentrecords hebben, en deze centraal koppelen aan bestaande records of nieuwe records maken met gekoppelde documentbestanden.</span><span class="sxs-lookup"><span data-stu-id="ed4a4-103">From the **Chart of Accounts** and **General Ledger Entries** windows, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="ed4a4-104">Geboekte documenten zonder inkomende documentrecords zoeken</span><span class="sxs-lookup"><span data-stu-id="ed4a4-104">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="ed4a4-105">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rekeningschema** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ed4a4-105">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="ed4a4-106">Selecteer een regel voor een grootboekrekening waarvan de grootboekposten die u wilt zien, geboekte inkoop- en verkoopdocumenten zijn zonder inkomende documentrecords en kies vervolgens de actie **Geboekte documenten zonder inkomend document**.</span><span class="sxs-lookup"><span data-stu-id="ed4a4-106">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="ed4a4-107">U kunt ook de actie **Posten** kiezen.</span><span class="sxs-lookup"><span data-stu-id="ed4a4-107">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="ed4a4-108">Kies in het venster **Grootboekposten** de actie **Geboekte documenten zonder inkomend document**.</span><span class="sxs-lookup"><span data-stu-id="ed4a4-108">In the **General Ledger Entries** window, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="ed4a4-109">Het venster **Geboekte documenten zonder inkomend document** wordt geopend en toont geboekte inkoop- en verkoopdocumenten zonder inkomende documentrecords die worden gerepresenteerd door grootboekposten in de Grootboekrekening waarvoor u het venster hebt geopend.</span><span class="sxs-lookup"><span data-stu-id="ed4a4-109">The **Posted Documents without Incoming Document** window opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the window for.</span></span> <span data-ttu-id="ed4a4-110">Het venster kan maximaal 1000 regels weergeven.</span><span class="sxs-lookup"><span data-stu-id="ed4a4-110">The window can show a maximum of 1000 lines.</span></span> <span data-ttu-id="ed4a4-111">Standaard bevat het veld **Datumfilter** daarom een filter dat de regels beperkt tot posten met een boekingsdatum vanaf het begin van de boekhoudperiode tot de werkdatum.</span><span class="sxs-lookup"><span data-stu-id="ed4a4-111">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="ed4a4-112">Gevonden documenten koppelen aan bestaande inkomende documentrecords</span><span class="sxs-lookup"><span data-stu-id="ed4a4-112">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="ed4a4-113">Selecteer in het venster **Geboekte documenten zonder inkomend document** de regel voor een geboekt document dat u wilt koppelen aan een bestaande inkomende documentrecord en kies vervolgens de actie **Inkomend document selecteren** .</span><span class="sxs-lookup"><span data-stu-id="ed4a4-113">In the **Posted Documents without Incoming Document** window, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="ed4a4-114">Selecteer in het venster **Inkomende documenten** de inkomende documentrecord die u wilt koppelen aan het gevonden geboekte document en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed4a4-114">In the **Incoming Documents** window, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="ed4a4-115">Selecteer in het venster **Geboekte documenten zonder inkomend document** de inkomende documentrecord die nu is gekoppeld aan het geboekte document, zoals u kunt zien in het feitenblok **Inkomende documentbestanden**.</span><span class="sxs-lookup"><span data-stu-id="ed4a4-115">In the **Posted Documents without Incoming Document** window, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="ed4a4-116">Als er geen relevante inkomende documentrecord in het venster **Inkomende documenten** staat, kunt u er een maken.</span><span class="sxs-lookup"><span data-stu-id="ed4a4-116">If a relevant incoming document record does not exist in the **Incoming Documents** window, then you can create it.</span></span> <span data-ttu-id="ed4a4-117">Zie [Inkomende documentrecords maken](across-how-create-income-document-records.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ed4a4-117">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ed4a4-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ed4a4-118">See Also</span></span>
[<span data-ttu-id="ed4a4-119">Inkomende documenten verwerken</span><span class="sxs-lookup"><span data-stu-id="ed4a4-119">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="ed4a4-120">Inkomende documenten</span><span class="sxs-lookup"><span data-stu-id="ed4a4-120">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="ed4a4-121">Inkoop</span><span class="sxs-lookup"><span data-stu-id="ed4a4-121">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="ed4a4-122">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ed4a4-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

